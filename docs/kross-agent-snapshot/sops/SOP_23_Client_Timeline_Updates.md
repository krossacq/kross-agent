# SOP 23: Client Timeline Updates

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how Kross Agent adds approved updates to a client's timeline inside the Tax Mogul Client Portal / Preparer Workspace.

## Core Rule

The client timeline is the chronological record of important client workflow activity.

Kross may add timeline entries only for the selected client inside the active firm workspace.

## Timeline Entry Types

Timeline entries may include:

- organizer started
- organizer submitted
- document requested
- document uploaded
- call transcript imported
- call summary approved
- missing document identified
- open question created
- client message drafted
- client message sent
- quote sent
- invoice sent/requested
- Kross queue status changed
- data entry started
- data entry blocked
- sent to preparer review
- payroll/report note added

## Required Timeline Fields

Each entry should include:

- firm_id
- client_id
- event_type
- title
- summary
- source_type
- source_id
- visibility
- created_by
- created_at

## Internal vs Client-Facing Timeline Entries

Internal timeline entries may include:

- preparer notes
- risk flags
- review concerns
- AI draft activity
- data-entry exceptions
- support notes

Client-facing timeline entries may include:

- approved document requests
- approved next steps
- approved deadlines
- approved status updates

Client-facing entries require approval.

## Kross Timeline Workflow

1. Confirm firm/client context.
2. Identify event type.
3. Confirm source.
4. Draft timeline entry.
5. Assign visibility.
6. Require approval if client-facing or sensitive.
7. Save timeline entry.
8. Log action.

## What Kross Must Not Add

Kross must not add:

- unapproved tax conclusions
- raw AI reasoning
- internal notes to client-visible timeline
- another client's information
- another firm's information
- credentials or access details
- unnecessary SSNs/TINs/bank details

## Timeline vs Official Memory

Timeline entries record events.

Official client memory summarizes current understanding.

Example:

- Timeline event: "Client uploaded W-2 on March 3."
- Official memory update: "W-2 income documents received for 2025 tax year."

Kross should not confuse event history with current official memory.

## Audit Requirements

Log when timeline entries are:

- created
- edited
- approved
- made client-visible
- archived
- used in AI retrieval

## Acceptance Criteria

This SOP is working when:

- Timeline entries are attached to the correct firm/client.
- Entries have clear source references.
- Internal entries stay internal.
- Client-visible entries require approval.
- Kross distinguishes event history from official memory.

