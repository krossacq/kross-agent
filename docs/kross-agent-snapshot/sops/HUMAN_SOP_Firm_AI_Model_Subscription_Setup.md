# Human SOP: Firm AI Model Subscription Setup

Version: 0.1
Purpose: Human-led setup checklist for connecting each firm's Kross Agent to the firm's own AI/model subscription.

## Classification

This is a human SOP for Tax Mogul Bureau representatives.

It is not a Kross Agent operating SOP and not a client-facing form section.

Kross Agent should not independently collect model credentials, choose billing plans, approve subscriptions, or decide which account should power a firm's agent.

## Goal

During onboarding, confirm how the firm's Kross Agent will be powered by an approved model provider.

Default future-firm rule:

- Each firm should pay for and authorize its own AI/model subscription.
- Tax Mogul Bureau should not casually power multiple unrelated firms from one shared personal model account.
- If Tax Mogul later sells an "AI usage included" tier, that must be a separate approved pricing/support model with usage tracking.

Returns and Revenue Office pilot exception:

- Returns and Revenue Office may use Sydne/Tax Mogul's model access because it is Sydne's own tax office and pilot environment.

## Approved Provider Options

Approved options may include:

- OpenAI / ChatGPT / Codex provider login
- OpenRouter account and API key
- Nous Portal account
- Another model provider explicitly approved by Sydne and documented for Kross Agent

Do not connect an unsupported provider without an approved provider SOP and documented operating boundary.

## Required Onboarding Decisions

The human onboarding representative must confirm:

1. Which provider will power this firm's Kross Agent.
2. Who owns and pays for the provider account.
3. Which model or model family is approved for the firm.
4. Whether access is through OAuth login, API key, provider token, or another approved method.
5. Where the credential is stored securely.
6. Whether usage limits, spend limits, or rate limits are configured.
7. Whether the firm understands that its agent usage may consume its own provider subscription.
8. What happens if the firm's model subscription expires, runs out of credits, or is revoked.

## Firm-Owned Subscription Rule

For standard future firm onboarding:

- The firm owner/admin should authorize the model provider account during the onboarding call.
- The model account should belong to the firm, not to another firm and not to an individual preparer unless that person owns/administers the firm.
- The Kross Agent VM/profile must be connected only to the approved provider account for that firm.
- One firm's provider account must never be used to power another firm's Kross Agent.

## Tax Mogul-Managed Usage Exception

Tax Mogul Bureau may choose to power a firm's agent from a Tax Mogul-managed provider account only if:

- The offer/pricing explicitly includes AI usage.
- Usage tracking is enabled.
- Cost limits or monitoring are in place.
- The firm is assigned to the correct Tax Mogul-managed account/pool.
- The arrangement is documented in the firm's access inventory.

This is a business/pricing decision, not something Kross Agent decides.

## Setup Steps

During onboarding:

1. Explain that Kross Agent needs a model provider to think, draft, summarize, and use tools.
2. Explain that the default model is firm-paid/firm-owned for future firms.
3. Confirm the provider and plan the firm will use.
4. Have the firm owner/admin complete the provider login or API-key creation step.
5. Store the credential only in the approved secure credential manager or server environment location.
6. Record the credential storage location in the access inventory, not the secret value.
7. Confirm Kross can start and answer using the selected provider.
8. Confirm usage/cost ownership with the firm.
9. Document who completed setup, when, and which provider/model was selected.

## What Not To Store In This SOP

Do not write:

- API key values
- OAuth tokens
- passwords
- recovery codes
- billing card details
- private provider dashboard URLs that expose account details

## Failure Handling

If provider authorization fails:

1. Pause Kross Agent launch.
2. Confirm the firm is logged into the correct provider account.
3. Confirm the subscription/credits are active.
4. Confirm the selected provider is supported.
5. Escalate to Tax Mogul setup support if the issue cannot be resolved during onboarding.

## Acceptance Criteria

This SOP is working when:

- The firm's model provider is documented.
- The account owner/payer is documented.
- The credential storage location is documented without exposing secrets.
- Kross Agent can use the approved provider.
- No firm is accidentally powered by another firm's model account.
- The firm understands whether AI/model usage is their cost or included in a separate Tax Mogul plan.
