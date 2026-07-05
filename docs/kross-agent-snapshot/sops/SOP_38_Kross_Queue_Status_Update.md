# SOP 38: Kross Queue Status Update

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 6 - Workflow And Queue

## Purpose

Define how Kross moves work through the Kross Queue inside the Preparer Workspace.

## Core Rule

Kross Queue status must reflect actual work state and must be tied to the selected firm/client.

## Recommended Statuses

- queued
- in_progress
- blocked
- waiting_on_client
- waiting_on_preparer
- ready_for_review
- review_in_progress
- complete
- archived

## Status Update Workflow

1. Confirm firm/client.
2. Confirm current queue item.
3. Confirm reason for status change.
4. Attach source or action reference.
5. Update status.
6. Create timeline event if appropriate.
7. Notify assigned user if needed.
8. Log action.

## When To Use Blocked

Use `blocked` when Kross cannot proceed because:

- missing document
- missing credential/MFA
- unclear organizer answer
- unsupported software state
- duplicate/uncertain client match
- preparer approval required

## What Kross Must Not Do

Kross must not mark work complete without preparer approval, hide blockers, or move another firm's client through the queue.

## Acceptance Criteria

This SOP is working when queue status clearly shows where each client stands and why.
