# SOP 30: Call Summary Approval And Save To Memory

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how a draft AI call summary becomes approved client memory, timeline events, tasks, document requests, and client-facing next steps.

## Core Rule

Kross must keep four things separate:

- AI draft
- human-edited version
- approved official memory
- client-facing summary/next steps

Kross must not merge draft AI content into official memory without human approval.

## Approval Workflow

1. Kross generates draft call summary.
2. Kross extracts recommended memory updates, missing documents, open questions, tasks, and client-facing next steps.
3. Preparer/admin reviews the draft.
4. Reviewer edits the summary if needed.
5. Reviewer approves, rejects, or requests revision.
6. Approved summary is saved to the client timeline.
7. Approved memory updates are merged into the client memory profile.
8. Approved tasks are created in the Preparer Workspace.
9. Approved missing-document requests are created.
10. Approved client-facing next steps become visible or become a draft GHL message.
11. Original transcript remains attached to the call record.
12. All actions are logged.

## Approval Roles

Approval may be granted by:

- Firm Owner
- Firm Admin, if allowed
- assigned Preparer, if allowed
- authorized Platform Admin only through approved support access

Clients cannot approve internal summaries or official memory updates.

## Save-To-Memory Rules

When saving to memory, Kross must:

- confirm firm_id
- confirm client_id
- confirm approver permission
- preserve source reference
- avoid overwriting conflicting data without review
- separate internal notes from client-facing content
- log the merge

## Rejected Or Needs Revision

If a summary is rejected or needs revision:

- do not update official memory
- do not publish client-facing next steps
- keep the draft for audit/history if required
- show the reason if provided
- allow regeneration or manual edit

## Conflict Handling

If the approved summary conflicts with existing memory:

1. Show existing value.
2. Show proposed value.
3. Require reviewer decision.
4. Save only the approved final value.
5. Log the conflict and resolution.

## What Kross Must Not Do

Kross must not:

- approve its own summary
- silently overwrite official client memory
- expose internal preparer notes to the client
- create client-facing items from rejected drafts
- create tasks or document requests for the wrong client
- use another firm's knowledge or another client's memory
- make final tax/legal determinations without preparer approval

## Audit Requirements

Log:

- summary generated
- summary viewed
- summary edited
- approval requested
- approved
- rejected
- memory updated
- timeline event created
- tasks created
- missing document requests created
- client-facing next steps published
- GHL draft created or sent

## Acceptance Criteria

This SOP is working when:

- draft summaries do not become official automatically
- approved summaries are saved to the correct client timeline
- approved memory updates merge into the correct client profile
- internal and client-facing content remain separate
- all sensitive actions are logged
