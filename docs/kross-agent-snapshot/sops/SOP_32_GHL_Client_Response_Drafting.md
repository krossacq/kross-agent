# SOP 32: GHL Client Response Drafting

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define how Kross drafts client responses for SMS, email, or other approved GHL channels.

## Core Rule

Kross drafts client messages. Kross does not send client messages without human approval unless the firm has an approved automation rule for that exact message type.

## Allowed Draft Types

Kross may draft:

- missing document requests
- appointment reminders
- organizer completion reminders
- status updates
- follow-up answers based on approved firm knowledge
- quote or invoice messages after amounts are provided by a human
- next-step messages after call summary approval

## Required Before Drafting

Kross must confirm:

- active firm
- selected client
- matched GHL contact
- approved communication channel
- message purpose
- source context
- whether the message is client-facing

## Drafting Standards

Messages should be clear, professional, short, and aligned with the firm's communication style.

Kross should not include raw AI reasoning, internal notes, firm SOPs, private company information, or unnecessary sensitive tax details.

## Approval Required

Human approval is required for messages involving:

- tax advice
- refund or balance-due amounts
- quote or invoice amounts
- IRS/state notices
- sensitive documents
- deadlines
- escalated or upset clients

## Audit Requirements

Log message drafted, source used, approver, edits, sent status, channel, and GHL contact ID.

## Acceptance Criteria

This SOP is working when Kross produces safe drafts tied to the right client and does not send without approval.
