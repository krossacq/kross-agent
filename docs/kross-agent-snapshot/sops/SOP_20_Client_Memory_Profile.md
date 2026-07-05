# SOP 20: Client Memory Profile

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how Kross Agent reads, drafts updates for, and uses an individual tax client's memory profile.

## Core Rule

Client memory belongs to one client inside one firm.

Kross may use a client memory profile only when that client is explicitly selected and the user is authorized to access that client.

## What Client Memory Can Include

Client memory may include:

- client name and contact details
- filing status
- entity type
- business type
- prior-year tax context
- current-year tax situation summary
- household/dependent context
- income summary
- deduction/credit context
- business activity summary
- risks/flags
- missing information summary
- approved call summary details
- internal preparer notes
- approved client-facing summary

## Client Memory Must Not Be Treated As Final Tax Judgment

Client memory helps the preparer understand the client.

Kross must not treat memory as final tax/legal determination. If professional judgment is required, Kross must escalate to a preparer.

## Reading Client Memory

Before reading client memory, Kross must confirm:

- firm/workspace
- selected client
- requesting user permission
- internal or client-facing context

If no client is selected, Kross must not retrieve client memory.

## Updating Client Memory

Kross may draft memory updates from:

- approved call summaries
- preparer notes
- organizer answers
- uploaded document metadata or extracted context
- client communication history

Kross must not directly overwrite official memory unless:

- the update has human approval, or
- an approved automation rule explicitly permits it

## Recommended Memory Update Flow

1. Kross identifies a possible memory update.
2. Kross creates a draft/recommended update.
3. Kross labels the source.
4. Human preparer/admin reviews the update.
5. Human edits if needed.
6. Human approves or rejects.
7. Approved update becomes official client memory.
8. The action is logged.

## Internal vs Client-Facing Fields

Client memory may contain both internal and client-facing fields.

Internal fields can include:

- risks/flags
- internal notes
- preparer concerns
- tax judgment reminders

Client-facing fields can include:

- approved next steps
- approved document requests
- approved deadlines
- approved high-level summary

Kross must not expose internal fields in the client portal.

## Conflict Rule

If new information conflicts with existing client memory, Kross must:

1. Flag the conflict.
2. Preserve the source references.
3. Create an internal task or memory update request.
4. Require human review.

Kross must not silently overwrite conflicting memory.

## Audit Requirements

Log when client memory is:

- viewed
- searched
- drafted for update
- approved
- rejected
- edited
- used in AI retrieval

## Acceptance Criteria

This SOP is working when:

- Kross uses client memory only for the selected client.
- Kross does not use client memory without client context.
- AI-suggested updates remain drafts until approved.
- Internal notes remain hidden from clients.
- Conflicts are flagged for review.

