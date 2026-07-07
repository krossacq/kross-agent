# SOP 22: AI Memory Update Approval

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how AI-suggested memory updates become official client memory only after human review and approval.

## Core Rule

AI-generated memory updates are recommendations, not official memory.

Kross must not treat an AI-generated recommendation as official truth until an authorized human approves it.

## When Kross Can Recommend Memory Updates

Kross may recommend updates after:

- transcript import
- call summary generation
- organizer submission
- document review
- client communication review
- preparer notes
- missing document discovery
- open question resolution

## Recommended Update Fields

Each update request should include:

- firm_id
- client_id
- source_type
- source_id
- target_field
- proposed_update
- reason
- approval_status
- created_by or agent_id
- reviewed_by
- reviewed_at
- created_at

## Approval Statuses

Recommended statuses:

- draft
- pending_review
- approved
- rejected
- needs_revision
- archived

## Approval Workflow

1. Kross identifies possible memory update.
2. Kross drafts proposed update.
3. Kross attaches source reference.
4. Kross labels risk/uncertainty if any.
5. Preparer/admin reviews.
6. Reviewer edits if needed.
7. Reviewer approves, rejects, or requests revision.
8. Approved update is merged into official memory.
9. Rejected update is preserved for audit/history but not used as official memory.
10. Action is logged.

## What Counts As Approval

Official memory approval must be explicit. A user saying "save it," "looks good," "create it," "mark ready," or "go ahead" is not enough for live client memory unless the approval clearly names the action being approved.

Acceptable approval examples:

- "I approve saving this memory update."
- "I approve merging this into the client's official memory."
- "I approve creating these internal tasks from this summary."

If approval is unclear, Kross must ask a confirmation question before saving, merging, or creating official records.

Fake/sample test artifacts may be saved only in a clearly labeled test area and must not be represented as official client memory.

## Updates That Require Extra Care

Human review is especially important for:

- filing status
- dependent claims
- business/entity details
- income summaries
- deduction/credit claims
- refund/balance-due references
- IRS/state issue notes
- identity verification
- risk flags
- tax position notes

## Conflict Handling

If proposed update conflicts with existing memory:

- do not overwrite
- flag conflict
- show old value and proposed value
- require human review
- create task if needed

## Client-Facing Rule

Approved memory does not automatically become client-facing.

A separate visibility decision is required before any memory update appears in the client portal.

## Audit Requirements

Log:

- draft created
- approval requested
- approved
- rejected
- revised
- merged into official memory
- made client-facing, if applicable

## Acceptance Criteria

This SOP is working when:

- AI updates stay draft/pending until approved.
- Official memory is updated only after human approval.
- Conflicts are flagged.
- Rejected updates do not become official memory.
- Visibility is handled separately from approval.
