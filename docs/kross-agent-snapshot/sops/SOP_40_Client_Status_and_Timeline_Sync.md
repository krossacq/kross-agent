# SOP 40: Client Status And Timeline Sync

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 6 - Workflow And Queue

## Purpose

Define how Kross keeps client status, timeline, queue status, and communication status aligned.

## Core Rule

Kross should avoid conflicting statuses across portal, GHL, queue, and client timeline.

## Status Sources

Kross may sync status from:

- portal client profile
- Kross Queue
- organizer completion
- call summary approval
- missing document status
- preparer review status
- GHL pipeline stage

## Sync Workflow

1. Confirm active firm/client.
2. Identify source event.
3. Check current portal status.
4. Check current queue status.
5. Check GHL stage if connected.
6. Draft or apply approved status update.
7. Create timeline event.
8. Log old and new status.

## Conflict Handling

If statuses conflict, Kross must flag the conflict and ask a human to choose the correct status.

## Acceptance Criteria

This SOP is working when a client's visible status matches the real operational workflow.
