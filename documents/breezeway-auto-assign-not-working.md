# Why Isn't Breezeway Auto-Assigning My Cleaner? (2026)

Source: https://rapideyeinspections.com/blog/breezeway-auto-assign-not-working/

_Tasks are showing up unassigned even though you set default workers. Here is the 5-step diagnostic flow, in priority order, that finds the cause. Covers the workflow toggle, property-level defaults, template overrides, Subdepartment mismatches, and the turn-event edge case._

# Why Isn't Breezeway Auto-Assigning My Cleaner?

You set up default workers. The task generated anyway but nobody is on it. Walk this 5-step diagnostic flow in order. Each check is ranked by how often it is actually the problem. The fix is almost always at step 1 or 2, but you have to verify each to know.

Breezeway auto-assigns tasks only when two conditions are both true: the Automated Workflow has the Assign Tasks to Default Workers toggle turned on, and the property has a default worker configured at either the department or template level. Per Breezeway's own documentation, "If the automatic assignment feature is turned off, all tasks will populate as unassigned."

The diagnostic below walks five checks in priority order. Roughly 70 percent of unassigned-task complaints resolve at step 1 (toggle off) or step 2 (no default worker on property). The rest are a mix of template-override conflicts, Subdepartment mismatches, and turn-event edge cases. Do not skip steps. The failure modes stack, and you may have more than one thing wrong.

## The 5-Step Diagnostic Flow

Walk this in order. Each step has a yes/no check, a fix if the answer is no, and a next-step direction if the answer is yes.

Is "Assign Tasks to Default Workers" turned ON in the Automated Workflow?

Go to Settings → Scheduling. Open the Automated Workflow that generates this task. Find the Assign Tasks to Default Workers toggle. Turn it on. Save.

This is the single toggle that controls whether the workflow assigns anyone at all. Per Breezeway's docs: "If the automatic assignment feature is turned off, all tasks will populate as unassigned." You are done. Verify on the next task that generates.

The toggle is on but tasks still appear unassigned. That means the workflow is trying to assign, but has no one to assign to. Move to step 2.

Does the property have a default worker set for this task's department?

Go to the property, click Template Modifiers, select People. Set a Department Default for the relevant department (Housekeeping, Inspection, Maintenance).

If this is a problem across many properties, email support@breezeway.io for the Default People CSV bulk upload template. Fixing 30 properties one at a time is how ops leads lose afternoons.

The property has a default worker set, but this specific task still came up unassigned. Move to step 3. A template-level override may be silently overwriting your department default.

Is there a template-level worker override that is blank or set to a different person?

On the same Template Modifiers → People screen at the property, check each template's row. If a template has its own worker field that is blank, you have two options: clear the override entirely (so the department default applies), or set a specific person for that template.

Per Breezeway's documentation: "The Task Template overrides the department default." A blank template override does not fall back to the department default. It falls through to unassigned.

Template overrides look correct. Move to step 4. Subdepartment mismatches are the next candidate.

Does the default worker's Subdepartment match the template's Subdepartment?

Either move the default worker into the matching Subdepartment, or remove the Subdepartment constraint from the template, or set a new default worker who is actually in the template's Subdepartment.

Subdepartments are Breezeway's routing layer inside a department. If your template is set to the "Deep Clean Crew" Subdepartment but your default cleaner is only in the "Regular Clean Crew" Subdepartment, the auto-assignment logic sees a routing conflict and falls through.

Subdepartments align. Move to step 5. The remaining cause is the turn-event edge case.

Is the unassigned task a same-day turn, when your other checkouts are assigning fine?

You have a Checkout workflow but no Checkout (turn) workflow. Turn events are treated as a distinct event type in Breezeway's Automated Workflow engine, so they need their own rule (or the same rule set to match both event types).

Full walkthrough with the mechanism and the two fix options is in our related guide: [Why Does Breezeway Cancel My Cleaning Between Same-Day Guests?](https://rapideyeinspections.com/blog/breezeway-cancels-cleaning-same-day-turnover/)

You have worked the full diagnostic and none of the five common causes apply. File a ticket at support@breezeway.io with the specific task ID, property, template, and expected default worker. Ask them to trace the auto-scheduler log.

## Two Causes That Don't Fit the Main Flow

### The default worker was deactivated

If the person set as your default was removed from the account or had their access revoked, auto-assignment silently falls through. The property config still shows their name (Breezeway does not automatically clear the reference), but the workflow cannot assign to an inactive user. Check your Manage People list. If the named default is no longer active, that is your cause.

### The workflow is in Draft mode

Draft workflows generate tasks on the schedule without sending assignee notifications. The task may actually be assigned to the correct worker, but they never received a notification, so you see "nobody is working on this" from their side. Check the workflow's Schedule Mode. If it is Draft, flip to Commit. This is not technically an auto-assign failure, but the symptom looks identical to operators on the ground.

## When Multiple Causes Compound

The reason the diagnostic matters is that failures stack. A real pattern we see in published reviews: an operator has 120 properties, the auto-assign toggle is on, 80 properties have default workers set but 40 do not, and among the 80 that do, 15 have template-level blank overrides from a half-finished setup. The result is that auto-assign works "most of the time" and fails silently on 55 properties, which is why the complaint reads as "sometimes it works, sometimes it doesn't."

This compounding is also why one reviewer described Breezeway's auto-assignment as "clunky" and noted "automatic assigning isn't always beneficial" (Christopher S., Operations Manager, Capterra February 2025). The feature is not unreliable; the setup surface just has multiple layers where silent misconfiguration can live.

The fix at scale is auditing all three layers (workflow toggles, property defaults, template overrides) before declaring the feature broken. For the full context on how Breezeway templates and workflows interact, see our [Breezeway Templates and Triggers complete setup guide](https://rapideyeinspections.com/blog/breezeway-templates-and-triggers/).

## Sources

- Breezeway Help Center. [Adjust your Automated Workflows](https://help.breezeway.io/en/articles/8224895-adjust-your-automated-workflows). Primary source for the Assign Tasks to Default Workers toggle behavior: "If the automatic assignment feature is turned off, all tasks will populate as unassigned."
 https://help.breezeway.io/en/articles/8224895-adjust-your-automated-workflows

- Breezeway Help Center. [Add Default Workers to each Property](https://help.breezeway.io/en/articles/8510786-add-default-workers-to-each-property). Primary source for the Template Modifiers → People setup flow and the rule that "The Task Template overrides the department default."
 https://help.breezeway.io/en/articles/8510786-add-default-workers-to-each-property

- Breezeway Help Center. [Subdepartments](https://help.breezeway.io/en/articles/7939205-subdepartments). Subdepartment behavior and its interaction with templates.
 https://help.breezeway.io/en/articles/7939205-subdepartments

- Capterra. [Breezeway Reviews](https://www.capterra.com/p/186514/Breezeway/). Christopher S., Operations Manager, Real Estate, February 2025: "The automated reply system/Breezeway Assist is clunky and does not assign the correct teams to the correct tasks always. This may be more of an internal issue that needs clarification, but automatic assigning isn't always beneficial."
 https://www.capterra.com/p/186514/Breezeway/

## Related
