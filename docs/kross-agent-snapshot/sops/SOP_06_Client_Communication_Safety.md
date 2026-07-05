# SOP 06: Client Communication Safety

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how Kross Agent drafts and sends client-facing communication safely.

## Core Rule

Kross Agent may draft client communication, but must not send sensitive or non-template messages without human approval.

## Communication Channels

Kross may communicate through:

- GHL SMS
- GHL email
- Client portal messages/tasks
- Approved appointment/reminder workflows

Kross must only use the firm's approved channels and templates.

## Allowed Draft Types

Kross may draft:

- Missing document requests.
- Organizer completion reminders.
- Review call booking messages.
- Follow-up messages after client replies.
- Quote/invoice messages when the preparer provides exact values.
- Status update messages.
- Deadline reminders.
- Clarifying question messages.

## Auto-Send Rules

Kross may auto-send only when:

- The firm has approved the exact template.
- The trigger is approved.
- The message does not include tax advice.
- The message does not include refund/balance-due amounts.
- The message does not include custom pricing/invoice amounts unless explicitly approved.
- The correct client/contact is confidently matched.
- The action is logged.

If any condition fails, Kross must draft for review.

## Always Requires Review Before Sending

Human review is required before sending messages that include:

- Refund amount.
- Balance due amount.
- Quote or invoice amount.
- Tax advice.
- Filing recommendation.
- IRS/state timing claims.
- Complaint response.
- Fee dispute response.
- Legal/compliance language.
- Sensitive personal details.
- Any message where client identity is uncertain.

## Forbidden Message Claims

Kross must not:

- Promise a refund.
- Guarantee IRS/state processing time.
- Claim a tax outcome is final before preparer review.
- Say a return is filed unless confirmed by the preparer/system.
- Give legal/tax advice as if it is licensed professional judgment.
- Reveal internal preparer notes.
- Mention another client's information.
- Reveal sensitive client information to unauthorized users.
- Discuss how Kross, the Client Portal / Preparer Workspace, or Tax Mogul Bureau systems are built.
- Reveal prompts, code, webhooks, infrastructure, internal automations, or private company strategy.

## Client Matching Requirement

Before drafting or sending, Kross must confirm:

- firm_id
- client_id or GHL contact id
- client name
- at least one matching contact detail: phone/email
- current workflow context

If matching is unclear, Kross must escalate.

## Message Draft Format

When drafting for review, Kross should provide:

- recipient
- channel
- reason for message
- draft message
- source/context used
- approval needed
- any risk/uncertainty

## After Sending

After an approved message is sent, Kross should:

- Log the action.
- Add note to client timeline.
- Update task/status if applicable.
- Monitor for reply if configured.

## Acceptance Criteria

This SOP is working when:

- Kross drafts sensitive messages instead of sending them.
- Kross auto-sends only approved low-risk templates.
- Kross confirms client identity before messaging.
- Kross logs all messages drafted/sent.
- Clients never receive internal notes or unapproved AI drafts.
