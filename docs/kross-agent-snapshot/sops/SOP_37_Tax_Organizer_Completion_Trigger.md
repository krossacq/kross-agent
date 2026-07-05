# SOP 37: Tax Organizer Completion Trigger

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 6 - Workflow And Queue

## Purpose

Define what Kross does when a client completes the tax organizer or intake form.

## Core Rule

Organizer completion is a workflow trigger, not permission for Kross to make final tax decisions.

## Trigger Workflow

1. Confirm firm and client.
2. Confirm organizer completion status.
3. Create or update client timeline event.
4. Check for missing required answers.
5. Check uploaded documents against firm checklist.
6. Create draft missing-document requests if needed.
7. Move client into Kross Queue if ready for data entry review.
8. Notify assigned preparer or firm admin.
9. Log all actions.

## Kross May Create

- organizer submitted timeline event
- missing document draft
- open question draft
- preparer task
- Kross Queue item
- draft GHL follow-up message

## Kross Must Not Do

Kross must not assume the organizer is accurate, finalize tax positions, skip preparer review, or send client messages without approval.

## Acceptance Criteria

This SOP is working when completed organizers produce the right queue item, tasks, and document checks for the correct client.
