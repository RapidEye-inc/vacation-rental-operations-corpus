# Can You Pull Turnover Photos From the Hostaway API?

Source: https://rapideyeinspections.com/blog/hostaway-api-turnover-photos/

_A verified developer reference: the Hostaway API does not expose cleaning or turnover task photos. The task object has no attachment field, there is no task-photo endpoint, and no task webhook. Here is exactly what is and isn't exposed, and how to get turnover photos into an AI review step._

# Can you pull turnover photos from the Hostaway API?

If you are wiring AI damage detection onto your turnovers, the first question is whether you can even get the cleaner's photos out of Hostaway programmatically. We read Hostaway's own API source to find out. The answer is more specific than a yes or no.

**No, not through the documented public API.** As of June 2026, Hostaway does not give you a way to download the before/after photos a cleaner attaches to a turnover task. The task object at GET /v1/tasks contains only metadata: status, assignee, timing, checklist items, cost. There is no attachments, photos, files, or images field, and no separate task-attachment endpoint. File attachments do exist in the API, but only on conversation messages, where each carries a URL that expires after seven days. The result: there is no supported way to bulk-export turnover photos from Hostaway for AI review. Operators who run automated photo inspection capture the images in a system built for it and feed an AI layer directly, rather than scraping the PMS.

## 01What the API actually returns for a task

According to Hostaway's public API reference, the platform shipped task endpoints in August 2023. You authenticate, then call GET /v1/tasks for a list or GET /v1/tasks/{taskId} for one task. Here is the full task object as published in that reference, with one thing worth noticing.

That is the whole shape (trimmed for length; the real object adds more timing and ranking fields, none of them media). According to Hostaway's published task schema, a task tells you *that* a clean happened, who did it, and when, but never *what it looked like*. The checklistItems array holds checklist line items, not photos, and in the documented examples it is empty. There is no GET /v1/tasks/{id}/attachments route anywhere in the reference.

## 02The capability matrix

Here is what the Hostaway API does and does not hand you, mapped to what an operator building an inspection pipeline actually wants.

| What you want | Exposed via API? | Where it lives |
| --- | --- | --- |
| Turnover / cleaning task metadata (status, assignee, timing) | Yes | GET /v1/tasks |
| Task completion status and timestamp | Yes | task.status, task.completedAt |
| Checklist line items on a task | Yes | task.checklistItems[] |
| Before/after photos a cleaner uploaded to a task | No | not in task object; no task-attachment route |
| A webhook when a task is completed | No | only reservation + message webhooks |
| File attachments, generally | Partial | conversation messages only, includeResources=1 |
| Listing photos (the marketing gallery) | Yes | listing image object (guest-facing, not condition) |

The last row is the trap worth naming. Hostaway absolutely exposes photos through its listing image endpoints, so a quick skim of the docs can make it look solved. But those are the staged marketing photos you show guests on Airbnb, with caption, vrboCaption, and sortOrder fields. They have nothing to do with the condition of the unit after a checkout.

## 03The one indirect path, and why it is not an export

The API does model file attachments. According to Hostaway's published attachment-object schema, they appear in the attachments array on conversation messages, the guest-messaging surface. To populate it you must add ?includeResources=1 to the request, otherwise nested resources come back empty. Each attachment looks like this:

That taskId field is genuinely interesting: it proves Hostaway's data model can associate a file with a task. But notice what is missing. There is no endpoint that says "give me every attachment for task 1234." You would have to walk conversations, pull messages with includeResources=1, and filter attachments by taskId yourself, and only the attachments that happen to ride along a conversation message would surface at all. That is a messaging feature, not a turnover-photo pipeline.

The seven-day clock

There is one more catch for anyone who thinks they can cache their way around this. For private attachments, Hostaway's documentation states the url is a temporary link that **expires seven days after it is generated**. You cannot store the URL; once it lapses you have to re-fetch the message to mint a fresh one. If you want to keep the file, you have to download the bytes and store them on your side before the link dies.

## 04For completeness: auth and the task list call

None of the above means the API is weak. It is well-built for what it covers. Authentication is OAuth2 client-credentials: you exchange your Hostaway account ID and API key for a bearer token that is valid for 24 months.

So a realistic, fully-supported Hostaway integration can tell you that the departure clean for a reservation is marked complete, who completed it, and when. It simply cannot tell you whether the unit is actually in good condition, because the photographic evidence never crosses the API boundary.

## 05So how do operators get turnover photos into AI?

If the goal is automated damage detection on every turnover, the practical answer is to stop treating the PMS as the photo source and capture the images where they can actually flow into an AI step.

#### Capture condition photos in a system built for inspection

Breezeway and Turno are designed around required-photo turnover and inspection tasks, so the documentation is structured and consistent rather than scattered across guest threads. Breezeway in particular has become the system of record for turnover photos at many mid-to-large operations, which is exactly why a consistent capture standard matters. See our [turnover inspection and documentation checklist](https://rapideyeinspections.com/blog/str-turnover-inspection-checklist-damage-documentation-photos/) for what to shoot.

#### Trigger your pipeline off the reservation lifecycle

Hostaway does expose reservation and unified webhooks, and every reservation carries its departure date. Use those to time your review around checkout, then collect the photos from wherever they were captured. You are using Hostaway for the signal it is good at (the booking lifecycle), not for media it does not serve.

#### Send the photos to a tool that ingests turnover documentation directly

Rather than rebuilding photo extraction, deduplication, and baseline comparison from scratch against a PMS that was never meant to export condition media, route the captured photos to a layer purpose-built to read them. That is the job an inspection-intelligence tool does.

### This is exactly the gap RapidEye was built to close

RapidEye is AI inspection intelligence for vacation rental managers. It ingests the turnover documentation your cleaners already capture and runs computer-vision damage detection over it, comparing each turnover against the property's own baseline to surface new scratches, stains, and missing items. The point is that you do not have to solve the messy photo-plumbing problem, including the parts a PMS API was never designed to serve, to get AI eyes on every checkout.

If you are evaluating whether this fits your operation, start with [is there AI that reviews Airbnb turnover photos](https://rapideyeinspections.com/blog/is-there-ai-that-reviews-airbnb-turnover-photos/) or [how to review turnover photos at scale](https://rapideyeinspections.com/blog/how-to-review-turnover-photos-at-scale/).

## 06Will this change?

Possibly, and the API itself hints at it. The presence of a taskId on the attachment object means Hostaway's data model already links files to tasks; exposing a clean task-attachment endpoint would be a natural extension. Until Hostaway publishes one, treat turnover task photos as not retrievable through the public API. If you are scoping a build that depends on it, confirm current behavior with Hostaway's API or partnerships team rather than assuming, because undocumented behavior can change without notice. Everything on this page reflects Hostaway's published API reference as of June 14, 2026.

### Related reading

- [AI automations you can build on Hostaway](https://rapideyeinspections.com/blog/hostaway-ai-automations/)

- [Connect Hostaway to Claude (MCP)](https://rapideyeinspections.com/claude-guides/hostaway/)

- [Is there AI that reviews turnover photos?](https://rapideyeinspections.com/blog/is-there-ai-that-reviews-airbnb-turnover-photos/)

- [Review turnover photos at scale](https://rapideyeinspections.com/blog/how-to-review-turnover-photos-at-scale/)

- [Can AI detect damage from photos?](https://rapideyeinspections.com/blog/ai-property-damage-detection-from-photos/)

- [Automate inspections at 200+ units](https://rapideyeinspections.com/blog/how-to-automate-property-inspections-200-vacation-rentals/)

### Sources

- [Hostaway Public API Reference](https://api.hostaway.com/documentation) – the live, authoritative documentation for authentication, the task object, the attachment object, webhooks, and listing images.https://api.hostaway.com/documentation

- [Hostaway/api](https://github.com/Hostaway/api) – the open-source repository that generates the API reference. Task object, attachment object (including the taskId field and seven-day private-URL expiry), and the OAuth2 client-credentials flow with 24-month token TTL were read directly from this source.https://github.com/Hostaway/api

- [Tasks: Create, Manage & Assign Tasks](https://support.hostaway.com/hc/en-us/articles/360036506093-Tasks-Create-Manage-Assign-Tasks) – Hostaway Support (covers in-app task photo uploads by cleaners).https://support.hostaway.com/hc/en-us/articles/360036506093-Tasks-Create-Manage-Assign-Tasks

- [Using Hostaway Webhooks](https://support.hostaway.com/hc/en-us/articles/360009022653-Using-Hostaway-Webhooks) – Hostaway Support (reservation and conversation-message webhook events).https://support.hostaway.com/hc/en-us/articles/360009022653-Using-Hostaway-Webhooks

Last verified: June 14, 2026, against Hostaway's published public API reference and its open-source documentation repository. APIs change; if a task-photo capability ships after this date, this page will be out of date until updated. This is an independent technical reference and is not affiliated with or endorsed by Hostaway.
