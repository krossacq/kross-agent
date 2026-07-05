# SOP 35: Client Message Approval And Send

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define the approval flow before Kross sends or schedules client-facing communication.

## Core Rule

Human review is required before sending client-facing messages unless the firm has explicitly approved the exact automation type.

## Approval Workflow

1. Kross drafts message.
2. Kross identifies source context.
3. Kross labels message type and risk level.
4. Authorized human reviews.
5. Human edits, approves, rejects, or requests revision.
6. Kross sends/schedules only after approval.
7. Kross logs the action and stores message reference.

## Authorized Approvers

Approvers may include Firm Owner, Firm Admin, assigned Preparer, or approved support admin through support access.

## Auto-Send Rule

Auto-send is allowed only for pre-approved low-risk templates and only when client identity, channel, and firm scope are confirmed.

## Audit Requirements

Log draft, approval, approver, final message, send time, channel, recipient, and related client record.

## Acceptance Criteria

This SOP is working when Kross cannot send sensitive or custom messages without approval.
