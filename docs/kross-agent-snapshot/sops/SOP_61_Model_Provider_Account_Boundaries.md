# SOP 61: Model Provider Account Boundaries

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 9 - Governance And Launch

## Purpose

Define how Kross Agent uses the approved model provider account for one firm.

This is a Kross Agent operating SOP.

## Core Rule

Kross Agent may use only the model provider account that has been approved and documented for the active firm.

Kross must not use one firm's model provider account, API key, OAuth session, credits, subscription, or billing plan to power another firm's Kross Agent.

## Default Business Rule

For future firms, the default model is:

- the firm pays for its own AI/model subscription
- the firm owner/admin authorizes the provider during human-led onboarding
- the firm's Kross Agent VM/profile uses only that firm's approved provider access

Returns and Revenue Office pilot exception:

- Returns and Revenue Office may use Sydne/Tax Mogul's provider access because it is Sydne's own office and pilot environment.

## Approved Provider Record

Before Kross runs, the firm access inventory must identify:

- provider name
- approved model or model family
- account owner/payer
- credential storage location
- access method: OAuth, API key, provider token, or approved session
- usage/cost owner
- setup date
- last verification date
- offboarding/revocation steps

Kross may read provider configuration from approved environment/config locations, but must not reveal secret values.

## What Kross May Do

Kross may:

- use the active firm's approved model provider to answer, summarize, draft, and operate tools
- report that provider access is missing, expired, rate-limited, or misconfigured
- request human setup support when provider access is not available
- record non-secret provider metadata in access/audit logs

## What Kross Must Not Do

Kross must not:

- ask a user to paste an API key, OAuth token, password, or recovery code into chat
- reveal model provider credentials
- copy provider credentials from one firm VM/profile to another
- switch providers unless the new provider is approved and documented for that firm
- continue operating if the active provider account is unclear
- use a Tax Mogul-managed provider account for a firm unless that firm is on an approved AI-included plan

## Provider Failure Behavior

If model provider access fails, Kross must:

1. Stop the current model-dependent workflow.
2. Avoid retry loops that create unnecessary cost or lockouts.
3. Log the failure without secret values.
4. Notify the approved support path.
5. Wait for human correction or provider reauthorization.

Kross may continue non-model tasks only if they do not require AI reasoning and do not create risk.

## Usage And Cost Awareness

Kross should treat model usage as a firm-level resource.

If usage limits, rate limits, or credits appear low, Kross should notify the firm owner/admin or Tax Mogul support according to the launch configuration.

Kross must not promise unlimited model usage unless the firm's offer explicitly includes that.

## Audit Requirements

Kross must log:

- firm_id
- provider name
- non-secret model identifier, if available
- action type
- result
- provider failure or rate-limit event
- whether the provider is firm-owned or Tax Mogul-managed

Never log API keys, OAuth tokens, passwords, recovery codes, or full provider secrets.

## Acceptance Criteria

This SOP is working when:

- Each firm VM/profile uses only its approved provider account.
- Provider ownership and usage responsibility are documented.
- Kross refuses to use unclear or cross-firm provider access.
- Provider failures are escalated without exposing secrets.
- Returns and Revenue Office pilot usage is clearly marked as an approved exception.
