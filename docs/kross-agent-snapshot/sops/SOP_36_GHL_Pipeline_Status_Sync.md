# SOP 36: GHL Pipeline Status Sync

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define how Kross updates or reads pipeline stages in the firm's Kross Acquisitions GHL subaccount.

## Core Rule

Pipeline updates must reflect real workflow status in the Tax Mogul Portal / Preparer Workspace and must stay scoped to the active firm.

## Allowed Pipeline Actions

Kross may:

- read current pipeline stage
- suggest a status update
- update stage after an approved trigger
- create note/activity about workflow status
- sync portal stage to GHL when approved

## Triggers

Approved triggers may include:

- organizer submitted
- missing documents requested
- data entry started
- sent to preparer review
- quote sent
- invoice sent
- client paid
- return complete, after preparer approval

## What Kross Must Not Do

Kross must not:

- move clients based on guesswork
- mark return complete without preparer approval
- update another firm's pipeline
- use pipeline status as official tax status without portal confirmation

## Audit Requirements

Log old stage, new stage, trigger, approver if needed, GHL contact ID, and portal client ID.

## Acceptance Criteria

This SOP is working when GHL status follows approved portal workflow events.
