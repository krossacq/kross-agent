# SOP 05: Audit Logging

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define what Kross Agent and the portal must log when sensitive tax-office actions occur.

## Core Rule

Every sensitive action must create an audit trail with enough context to answer:

- Who did it?
- What did they access or change?
- Which firm did it belong to?
- Which client did it belong to, if applicable?
- When did it happen?
- Why did it happen, if support/admin access was used?

## Required Audit Fields

Each audit log should include:

- id
- firm_id
- client_id, nullable
- user_id or agent_id
- actor_type: user, kross_agent, platform_admin, system
- action
- resource_type
- resource_id
- metadata
- ip_address, if available
- user_agent, if available
- created_at

## Sensitive Actions To Audit

Audit these actions:

- Viewing client profile.
- Viewing tax documents.
- Downloading tax documents.
- Uploading documents.
- Deleting documents.
- Editing client memory.
- Running AI summary.
- Saving AI-generated memory.
- Approving or rejecting AI memory updates.
- Searching firm knowledge.
- Searching client memory.
- Running AI retrieval.
- Drafting client-facing messages.
- Sending client-facing messages.
- Changing task status.
- Creating missing-document requests.
- Changing permissions.
- Adding/removing firm users.
- Support/admin access to firm data.
- Exporting data.
- Access failures.
- Permission denials.

## AI Retrieval Logs

Every AI retrieval should log:

- firm_id
- client_id, if applicable
- user_id
- prompt/action type
- retrieval scope: global, firm, client
- source ids retrieved
- visibility filters used
- whether answer was client-facing or internal
- created_at

Do not log sensitive prompt content in a way that creates unnecessary exposure. Store enough metadata for accountability while minimizing risk.

## Support Access Logs

If a Platform Admin or Kross Command accesses firm/client data for support, log:

- support reason
- support ticket/reference, if available
- firm_id
- client_id, if applicable
- admin user
- start time
- end time, if time-limited
- actions taken

## Kross Agent Log Behavior

Kross Agent should create logs when it:

- Generates a summary.
- Recommends memory updates.
- Drafts a client message.
- Sends an approved message.
- Updates queue status.
- Creates a task.
- Pulls payroll reports.
- Uploads payroll reports.
- Encounters missing access or login failure.
- Escalates an issue.

## Prohibited Logging

Do not log:

- Passwords.
- API keys.
- MFA codes.
- Recovery codes.
- Full raw AI chain-of-thought/reasoning.
- Full document contents unless required and secured as a document record.

## Acceptance Criteria

This SOP is working when:

- Sensitive actions create audit records.
- AI retrieval has scoped retrieval logs.
- Support access is reasoned and logged.
- Secrets are not written into logs.
- Audit logs can be filtered by firm, client, user, action, and date.

