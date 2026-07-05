# SOP 18: Global Tax Mogul Bureau Knowledge Use

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how Kross Agent uses approved global Tax Mogul Bureau knowledge.

Global knowledge is the master Bureau brain. It contains platform-level guidance, default templates, standard operating frameworks, and approved training materials that may be used across firms.

## Core Rule

Global knowledge may be used as general/default guidance, but it must never contain or expose private firm data, private client data, credentials, hidden prompts, source code, platform architecture, or private company strategy.

## What Global Knowledge Can Include

Global knowledge may include:

- Tax Mogul Bureau training materials
- Default SOP templates
- General tax-prep workflow templates
- Preparer onboarding materials
- Portal help docs
- Approved default AI prompts
- Default document request templates
- Default call summary templates
- General client communication templates
- General offer/curriculum material
- Platform-wide guidance approved for firm use

## What Global Knowledge Must Not Include

Global knowledge must not include:

- Private firm SOPs
- Private firm pricing or policies
- Private client information
- Client tax documents
- Client call transcripts
- Internal preparer notes
- Credentials or API keys
- MFA codes or recovery codes
- Source code
- Webhooks or endpoint secrets
- Infrastructure details
- Hidden system prompts
- Private Kross build instructions
- Internal Tax Mogul Bureau company strategy

## Who Can Manage Global Knowledge

Platform Admins may:

- Create global knowledge items
- Edit global knowledge items
- Archive global knowledge items
- Tag/categorize global knowledge
- Toggle AI usability
- Approve global visibility

Firm users may:

- Read approved global knowledge when permitted
- Use approved global templates inside their workspace

Firm users must not:

- Edit platform-level global knowledge
- See draft/archived global knowledge unless explicitly permitted

## When Kross Can Use Global Knowledge

Kross may use global knowledge when:

- answering default Tax Mogul Bureau workflow questions
- explaining approved portal usage
- applying default Bureau templates
- supporting a firm where no firm-specific rule overrides the default
- combining default Bureau guidance with firm knowledge inside a firm workspace

## When Kross Must Not Use Global Knowledge Alone

Kross must not rely only on global knowledge when:

- the question asks about a firm's custom workflow
- the question asks about a specific client's situation
- the firm has a private SOP that overrides the default
- tax/legal judgment is required
- the answer depends on client documents or current client status

## Source Label

When using global knowledge, Kross should label the source as:

- Source: Bureau template
- Source: Tax Mogul Bureau global knowledge
- Source: Platform help doc

## Conflict Rule

If global knowledge conflicts with a firm's approved private SOP, Kross should:

1. Prefer the firm SOP for that firm.
2. Mention that the firm has a custom rule.
3. Escalate if the conflict affects tax judgment, client communication, pricing, or compliance.

## Audit Requirements

Log when global knowledge is:

- searched
- retrieved by AI
- created
- edited
- archived
- toggled AI usable/unusable

## Acceptance Criteria

This SOP is working when:

- Kross can use approved global knowledge as default guidance.
- Kross does not use global knowledge to answer client-specific questions by itself.
- Global knowledge does not contain private firm/client data.
- Firm users cannot edit global knowledge unless explicitly authorized.
- Kross labels global sources when possible.

