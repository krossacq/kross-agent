# SOP 09: Credential and MFA Handling

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how credentials, API keys, MFA codes, and recovery methods are handled for Kross Agent.

## Core Rule

Credentials must never be stored in SOP files, prompts, chat messages, screenshots, transcripts, Obsidian notes, or audit logs.

Kross may reference where a credential is stored, but must not reveal the secret value.

## Credential Types

This SOP covers:

- Agentmail.to email credentials
- GHL API keys/private integration tokens
- TaxSlayer login credentials
- Tax Mogul Portal login/service credentials
- Meeting recorder API keys/OAuth credentials
- SBTPG login credentials
- Refund Advantage login credentials
- MFA methods
- Recovery codes

## Storage Rule

Store credentials only in the approved secure credential manager or secret store.

The access inventory may include:

- system name
- username/email
- credential storage reference
- credential owner
- last verified date

The access inventory must not include:

- password values
- API key values
- MFA codes
- recovery codes

## MFA Rule

If MFA is required:

1. Confirm who owns the MFA method.
2. Confirm whether Kross can complete MFA during supervised sessions.
3. Confirm whether the system supports a service account, authenticator app, or delegated access.
4. Store recovery methods securely.
5. Never paste MFA backup codes into chat or SOPs.

## Kross Agent Behavior

Kross Agent must:

- Ask for a secure credential handoff method if access is missing.
- Refuse to receive passwords in normal chat.
- Refuse to reveal credentials.
- Log access failures without logging secret values.
- Escalate repeated login or MFA failures.

## Acceptance Criteria

This SOP is working when:

- No secrets appear in SOPs, prompts, logs, or transcripts.
- Every credential has a secure storage reference.
- MFA ownership is clear.
- Access failures are logged safely.
- Kross cannot reveal passwords, API keys, MFA codes, or recovery codes.

