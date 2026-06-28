# How to Bulk Edit in Breezeway (Everything You Can and Can't Do) 2026

Source: https://rapideyeinspections.com/blog/breezeway-bulk-edit/

_What Breezeway actually supports for bulk edits across properties, tasks, and elements. The exact menu paths, the CSV support-only upload path, and the gaps users complain about most (with real reviewer quotes)._

# How to Bulk Edit in Breezeway (Everything You Can and Can't Do)

A field guide for operators managing 100-plus properties. Covers the Bulk Actions menu on the Properties page, bulk task updates, the CSV import path reserved for Breezeway support, and the specific gaps operators keep running into when they scale. Written for the operator who just tried to update 200 properties at once and found out they can't.

Breezeway does support bulk editing, but the surface is narrower than operators expect. On the Properties page, checking multiple property boxes reveals a Bulk Actions menu that lets you assign Guide Templates and apply a handful of other property-level changes. On tasks, selecting multiple tasks exposes a Bulk Actions flyout that lets you update the Subdepartment. Beyond that, bulk editing is limited: pay structures, per-property task requirements, property elements, and tag-based property selection still require either one-at-a-time edits or a CSV file that Breezeway support has to process for you.

For ops teams running 100-plus properties, the practical approach is to lean on Bulk Actions for the fields it supports, use Property Tags and Groups to batch filters for reporting, and email support@breezeway.io to request the CSV import template for the three specific categories Breezeway will batch-ingest: default people at the department level, default people at the template level, and time and rate settings.

If you manage operations for a portfolio above 50 units, the single most common complaint about Breezeway is that you cannot bulk edit everything you want to. The reviews on G2, Capterra, and Comparent from 2025 and early 2026 return to this point repeatedly. Users at mid-market portfolios say things like "you have to attach everything to the properties one at a time" and "it would be amazing to be able to select all properties under a certain tag and update them all at once." These are accurate descriptions of the platform. Breezeway's bulk edit surface is real but partial, and knowing exactly where it stops saves hours of clicking.

## What Breezeway Bulk Actions Actually Cover

Breezeway exposes Bulk Actions in two main places: the Properties page and the Scheduling page (for tasks). The feature surfaces when you check the boxes next to multiple items. Based on Breezeway's current help documentation, here is what is actually supported as of April 2026.

### What you can bulk edit

- **Assign a Guide Template** to multiple properties at once from the Properties page Bulk Actions menu

- **Update Subdepartment** on multiple tasks in a single flyout

- **Apply Property Tags** to multiple properties for later filtering

- **Commit multiple drafted tasks in a workflow** in bulk from the Scheduling page

- **Export properties, tasks, and subdepartments to CSV** with default columns for external editing

### What you can't bulk edit in the UI

- **Pay rate or pay structure** across properties or tasks (CSV via support only)

- **Default cleaner, inspector, or maintenance worker** per property (CSV via support only)

- **Per-property task requirements and checklist modifiers**

- **Property Elements** in mass quantities

- **Selecting all properties under a tag and updating them in a batch**

- **Recurring tasks that continue indefinitely** without a set end

According to [Breezeway's Guide - Multiple Templates help article](https://help.breezeway.io/en/articles/8399444-guide-multiple-templates), the template assignment flow is the most mature part of the bulk edit experience. Breezeway also recently added Save and Cancel buttons to the Bulk Edit Properties flow for extra confirmation, per their Q4 2025 product updates. That change was a response to the risk of accidentally overwriting a template across hundreds of properties, which happened enough to warrant a guardrail.

## Bulk Edit Properties: The Exact Flow

The Bulk Actions menu for properties is on the Properties page, not the Scheduling or Tasks view. This trips up new admins who try to edit from the wrong screen. The flow Breezeway documents:

- Open the Properties page
Go to the Properties section from your Breezeway dashboard. This page shows every property in your portfolio with filter options at the top.

### Open the Properties page

Go to the Properties section from your Breezeway dashboard. This page shows every property in your portfolio with filter options at the top.

- Filter down to the set you want to edit
Use the Guide Templates filter, Group filter, Tag filter, or search box to narrow the view. This matters because the checkbox selection only applies to what is visible and selected. If you have 400 properties and only want to edit 120, filter first.

### Filter down to the set you want to edit

Use the Guide Templates filter, Group filter, Tag filter, or search box to narrow the view. This matters because the checkbox selection only applies to what is visible and selected. If you have 400 properties and only want to edit 120, filter first.

- Check the boxes next to the properties you want to edit
A Bulk Actions button appears once at least one property is checked. You can also use the header checkbox to select all visible filtered properties at once.

### Check the boxes next to the properties you want to edit

A Bulk Actions button appears once at least one property is checked. You can also use the header checkbox to select all visible filtered properties at once.

- Click Bulk Actions and choose Bulk Edit Properties
From the dropdown you get a list of fields you can change. Guide Template is the most common bulk edit here, along with tag application.

### Click Bulk Actions and choose Bulk Edit Properties

From the dropdown you get a list of fields you can change. Guide Template is the most common bulk edit here, along with tag application.

- Pick the new value and confirm with Save
Breezeway added a confirmation step here after operators accidentally overwrote templates across large portfolios. Read the confirmation carefully. There is no undo for a bulk template reassignment, and if you delete a template, any property using it silently falls back to the Default Template.

### Pick the new value and confirm with Save

Breezeway added a confirmation step here after operators accidentally overwrote templates across large portfolios. Read the confirmation carefully. There is no undo for a bulk template reassignment, and if you delete a template, any property using it silently falls back to the Default Template.

## Bulk Edit Tasks: What You Can Change

Task-level bulk editing is narrower. According to Breezeway's documentation on [Subdepartments](https://help.breezeway.io/en/articles/7939205-subdepartments), the primary bulk action for tasks is Subdepartment reassignment: click one or more tasks, the Bulk Actions option appears, and a flyout lets you update the Subdepartment of the selected tasks in one shot. Subdepartments are also included in default CSV exports and in custom views, so you can audit Subdepartment assignment across the portfolio without clicking into each task.

Everything else on a task (due date, assignee, completion status, attached requirements) still typically has to be edited task-by-task. This is where ops teams at mid-market portfolios lose the most hours. If you need to shift 80 tasks to a new due date because a cleaner quit mid-week, Breezeway does not offer a native "reschedule all selected" action. The workaround operators use is covered further down.

## The CSV Bulk Upload Path (Support Only)

Breezeway does have a CSV bulk upload feature, but it is not self-service. Per [Breezeway's Bulk Uploads help article](https://help.breezeway.io/en/articles/8694484-bulk-uploads), the Support team will process CSV uploads for three specific categories:

- **Default People at the Department Level.** Bulk-assign default cleaners, inspectors, or maintenance workers across your entire portfolio by department.

- **Default People at the Template Level.** Bulk-assign default workers when a specific template triggers.

- **Time and Rate.** Bulk-update time estimates or pay rates (Piece or Hourly) at the template level.

To use it, email support@breezeway.io and ask for the CSV template for the category you need. Breezeway sends back a spreadsheet with the required columns, you fill it in, send it back, and their team processes the upload on their end. Operators who have used this path report the turnaround is usually a few business days.

Two rules to know before you try:

- **Names must match Manage People exactly.** If the cleaner is entered as "Maria G." in Manage People, your CSV has to say "Maria G." character-for-character. A mismatch silently drops the assignment.

- **Multiple users go in one cell, comma-separated.** Do not split them into separate columns.

- **You need Property IDs and Template IDs.** Export your properties and templates first to pull the IDs, then paste them into the CSV.

### For per-property task edits: use the CSV loop

If you need to bulk-edit something the UI does not support (pay rate per template, default workers across a tag, time estimates), the operator-tested loop is: export the relevant CSV from Breezeway, edit externally in your spreadsheet tool of choice, email support to process the changed file. The turnaround is slower than a click but much faster than editing 300 properties one at a time.

## The Gaps Operators Complain About Most

Running through 2025 and 2026 reviews on [G2](https://www.g2.com/products/breezeway/reviews), [Capterra](https://www.capterra.com/p/186514/Breezeway/), and [Comparent](https://www.comparent.com), the same bulk edit gaps come up across operators at very different portfolio sizes. The frequency with which independent reviewers surface the same issue is the clearest signal of what Breezeway still has not fixed.

Three patterns recur across these reviews:

- **Tag-based bulk edit.** Operators build out tag systems to group properties (by market, by owner, by tier) and then cannot use the tag as the basis for a bulk update. The workaround is to filter by tag in the Properties page, select all visible properties, then run Bulk Actions. That works for the fields Bulk Actions covers; it fails for everything else.

- **Elements in mass quantities.** Property Elements (appliances, fixtures, furniture items with attached photos, model numbers, and maintenance history) are one of Breezeway's strongest features for mid-market operators. But there is no native way to bulk-edit elements across properties. If you replaced every dishwasher in 40 properties with a new model, you update 40 Element records one at a time.

- **Recurring tasks with no end date.** Breezeway's automated workflows are reservation-triggered (checkout, check-in, turn). There is no native "every 90 days, forever" trigger. Operators who need truly indefinite recurring tasks (quarterly deep cleans, annual HVAC service) usually layer a calendar reminder workflow outside Breezeway or build a manual task on a recurring schedule they reset each year.

## Bulk Edit Support Matrix

The quick reference for what is supported, what requires support, and what is not available at all.

| Edit type | Self-service UI | CSV via support | Not supported |
| --- | --- | --- | --- |
| Assign Guide Template to many properties | Yes | — | — |
| Apply Property Tags to many properties | Yes | — | — |
| Update Subdepartment on many tasks | Yes | — | — |
| Commit multiple drafted workflow tasks | Yes | — | — |
| Default cleaner/inspector per property | Partial | Yes | — |
| Pay rate (Piece or Hourly) at template level | No | Yes | — |
| Default People at department level | No | Yes | — |
| Reschedule multiple tasks to a new date | Drag-and-drop on schedule view only | — | No native bulk reschedule |
| Bulk edit Property Elements | No | Not in support-covered categories | One-at-a-time only |
| Select by tag, apply arbitrary field update | Only Bulk Actions-supported fields | — | Not for most fields |
| Recurring indefinite tasks | No | No | Not supported natively |

## Three Operator-Tested Workarounds

### Tag-first, then bulk action

Before you build any bulk edit workflow, invest an afternoon in a good tag schema. Tag by market, by owner, by service tier, by property size. The tag filter on the Properties page is the closest thing to "select by tag and bulk edit" Breezeway offers. You still only get the fields Bulk Actions supports, but the filter saves the scrolling.

### Template consolidation for pay and worker assignment

If you find yourself editing default workers across many properties, consolidate templates. The CSV bulk upload that Breezeway support will process targets the template level, not the property level. Fewer, better-defined templates means one CSV edit propagates to many properties. Operators at 200-plus units often run 8 to 15 templates rather than 50 near-duplicates.

### Export, edit in a spreadsheet, email support

For the scenarios that the UI does not cover, the export-edit-support loop is the operator-tested path. Export the relevant data via the default CSV, edit the file, email support@breezeway.io with a clear subject line (e.g., *Bulk update: Default People at Template Level for 42 templates*). Include the spreadsheet as an attachment. Turnaround varies but is typically a few business days and is meaningfully faster than one-at-a-time edits.

## Where This Fits in the Broader Photo Review Problem

The bulk edit gap matters most when you are trying to scale operations review across a mid-market portfolio. Breezeway's photo documentation is the best in class and the reason most professional operators use it. The downside is that once the photos are in the platform, reviewing them does not scale. Breezeway does not analyze photos for damage or missing items natively. At 200 units running two turnovers a week each, you are ingesting 16,000 to 24,000 photos a month. No ops team can manually review that. For a deeper look at this gap, see our reference on [how to review turnover photos at scale](https://rapideyeinspections.com/blog/how-to-review-turnover-photos-at-scale/) and [the hidden cost of missed damage](https://rapideyeinspections.com/blog/hidden-cost-missed-damage-short-term-rentals/).

This is the layer where [RapidEye plugs directly into Breezeway](https://rapideyeinspections.com/blog/add-ai-damage-detection-breezeway-workflow/), analyzing the turnover photos already uploaded through whatever templates you have configured and flagging damage, missing items, and cleanliness failures. No workflow change for cleaners, no bulk edit required. If you are a Breezeway user hitting the photo review wall at scale, this is the companion layer that closes the gap.

### See RapidEye running on your Breezeway photos

Book a 15-minute demo. We run the analysis on your actual turnover photos from Breezeway and show you what your team missed.

## Sources

- Breezeway Help Center. [Guide - Multiple Templates](https://help.breezeway.io/en/articles/8399444-guide-multiple-templates). Bulk Edit Properties flow for assigning Guide Templates, filter options, Save/Cancel confirmation added in Q4 2025.
 https://help.breezeway.io/en/articles/8399444-guide-multiple-templates

- Breezeway Help Center. [Bulk Uploads](https://help.breezeway.io/en/articles/8694484-bulk-uploads). The three categories Breezeway support will process via CSV: Default People at Department Level, Default People at Template Level, Time & Rate.
 https://help.breezeway.io/en/articles/8694484-bulk-uploads

- Breezeway Help Center. [Subdepartments](https://help.breezeway.io/en/articles/7939205-subdepartments). Bulk Actions flyout for updating task Subdepartment, CSV export coverage.
 https://help.breezeway.io/en/articles/7939205-subdepartments

- Breezeway. [Q4 2025 Breezeway Product Updates](https://www.breezeway.io/blog/q4-2025-breezeway-product-updates). Save/Cancel buttons added to the Bulk Edit Properties confirmation step.
 https://www.breezeway.io/blog/q4-2025-breezeway-product-updates

- Capterra. [Breezeway Reviews, Capterra](https://www.capterra.com/p/186514/Breezeway/). User quotes from Janelle M., Nikolai K., Avery D., Sara S., spanning 2025 and 2026, on bulk edit gaps.
 https://www.capterra.com/p/186514/Breezeway/

## Related
