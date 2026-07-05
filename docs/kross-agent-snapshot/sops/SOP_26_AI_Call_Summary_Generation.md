# SOP 26: AI Call Summary Generation

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how Kross Agent creates draft summaries from client call transcripts.

## Core Rule

AI call summaries are drafts until reviewed and approved by an authorized human.

Kross must not treat an AI summary as official client memory until approval.

## Required Context Before Summarizing

Before summarizing, Kross must confirm:

- active firm
- selected client
- authorized user
- attached call record
- transcript source
- transcript processing consent is not flagged as blocked

## Required Summary Structure

Kross should use this structure:

# Client Call Summary

- Client:
- Firm:
- Call date:
- Participants:
- Purpose of call:

## Summary

Brief summary of what was discussed.

## Tax Situation Updates

Relevant tax situation updates mentioned on the call.

## Missing Documents

Documents still needed from the client.

## Open Questions

Unanswered questions that need follow-up.

## Preparer Tasks

Internal tasks for the preparer/team.

## Client-Facing Next Steps

Only next steps that are safe for the client to see after approval.

## Internal Preparer Notes

Internal notes that should not be visible to the client.

## Recommended Memory Updates

Updates that should be added to the client's long-term memory profile after human approval.

## Deadlines

Dates/deadlines mentioned.

## Source

Call record/transcript reference.

## Summary Rules

Kross should:

- separate facts from assumptions
- flag uncertainty
- preserve important dates
- avoid over-confident tax conclusions
- cite the call record as the source
- keep internal notes separate from client-facing next steps
- identify items that need human review

## What Kross Must Not Do

Kross must not:

- make final tax/legal determinations
- send the summary to the client automatically
- save the draft as official memory without approval
- expose internal preparer notes to the client
- include another client's information
- include another firm's information
- invent missing facts
- hide uncertainty

## Audit Requirements

Log:

- summary generated
- model or summarization process used, if tracked
- source call record
- user who requested summary
- summary edited
- summary approved
- summary rejected
- summary saved to memory

## Acceptance Criteria

This SOP is working when:

- summaries are generated only for confirmed firm/client calls
- draft and approved summaries are separate
- internal notes and client-facing next steps are separate
- every summary has a source
- human approval is required before official memory updates
