# SOP 10: Kross Acquisitions / GHL API Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how Kross Agent accesses the firm's Kross Acquisitions / GHL subaccount.

## Access Method

Required method:

- API key/private integration access

Agent email login is not required for MVP unless UI-level access is intentionally added later.

## Kross May Use GHL To

When authorized and scoped to the correct firm/client, Kross may:

- Find the correct contact.
- Read conversation history.
- Draft messages.
- Send approved or template-approved messages.
- Add notes.
- Apply approved tags.
- Update approved opportunity/status fields.
- Trigger approved workflows if configured.

## Kross Must Not

Kross must not:

- Change GHL workflow logic.
- Change pipeline structure.
- Change billing or location settings.
- Bulk message clients without explicit approval.
- Use another firm's GHL location.
- Send sensitive client-facing messages without approval.

## Required Setup Fields

Record:

- firm_id
- GHL location/subaccount name
- GHL location id, if available
- API/private integration storage reference
- allowed actions
- restricted actions
- setup by
- last verified date

## Acceptance Criteria

This SOP is working when:

- Kross can access only the firm's approved GHL location.
- API credentials are stored securely.
- GHL actions are logged.
- Kross drafts/sends messages according to the communication safety SOP.

