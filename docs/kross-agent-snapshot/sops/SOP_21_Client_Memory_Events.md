# SOP 21: Client Memory Events

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how Kross Agent records important client timeline/memory events.

## Core Rule

Client memory events must be attached to the correct firm and the correct client.

Kross must never create a memory event without confirmed firm_id and client_id.

## What Counts As A Memory Event

Memory events may include:

- call summary approved
- missing document identified
- document received
- open question created
- preparer task created
- client next step approved
- quote sent
- invoice requested
- review handoff created
- data entry issue flagged
- payroll/report-related client event, if applicable

## Required Event Fields

Each event should include:

- firm_id
- client_id
- event_type
- title
- summary/body
- source_type
- source_id
- visibility
- created_by
- approved_by, if applicable
- created_at

## Visibility

Events may be:

- internal
- preparer_only
- owner_admin_only
- client_visible

Client-visible events require approval.

## Event Creation Rules

Kross may draft or create internal events when:

- firm/client context is confirmed
- the event is tied to an approved source or current action
- the event does not expose sensitive data unnecessarily

Kross must get human approval before:

- making an event client-visible
- creating events that include refund/balance-due details
- creating events that include tax advice or final determinations
- creating events from uncertain/conflicting information

## Source References

Every event should reference its source where possible:

- call record
- call summary
- organizer
- document
- GHL conversation
- preparer note
- Kross action

## Audit Requirements

Log when memory events are:

- created
- edited
- approved
- made client-visible
- archived
- used in AI retrieval

## Acceptance Criteria

This SOP is working when:

- Events are attached to the correct firm/client.
- Events have clear source references.
- Client-visible events require approval.
- Internal events do not appear in the client portal.
- Kross does not create events from uncertain client matches.

