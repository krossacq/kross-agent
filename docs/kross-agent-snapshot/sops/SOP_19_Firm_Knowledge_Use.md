# SOP 19: Firm Knowledge Use

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 3 - Memory

## Purpose

Define how Kross Agent uses one firm's private knowledge base inside the Tax Mogul Client Portal / Preparer Workspace.

## Core Rule

Firm knowledge belongs to one firm only. Kross Agent may use firm knowledge only inside that firm's authorized workspace.

Kross must never use Firm A's knowledge while working inside Firm B.

## What Firm Knowledge Can Include

Firm knowledge may include:

- firm SOPs
- intake process
- tax-prep workflow
- review process
- document checklist
- communication style
- pricing/packages
- niche-specific notes
- call scripts
- preparer instructions
- escalation rules
- internal policies
- preferred AI prompts
- client service standards
- turnaround time rules
- custom templates
- payroll rules
- PTIN/preparer mapping rules

## Required Knowledge Item Fields

Each firm knowledge item should include:

- firm_id
- title
- content/body
- category
- tags
- status
- visibility
- is_ai_accessible or ai_usable
- source reference
- created_by
- updated_by
- created_at
- updated_at

## When Kross Can Use Firm Knowledge

Kross may use firm knowledge when:

- active firm/workspace is confirmed
- requesting user is authorized
- knowledge belongs to the active firm
- knowledge is active
- knowledge is marked AI usable, if that setting exists
- visibility permits the current context

## When Kross Must Not Use Firm Knowledge

Kross must not use firm knowledge when:

- no firm/workspace is confirmed
- user is not authorized
- item belongs to another firm
- item is archived/inactive
- item is not AI usable
- answer is client-facing and the item is internal-only

## Firm Knowledge vs Global Knowledge

Firm knowledge can override global/default Bureau guidance for that firm.

If a firm SOP conflicts with global guidance:

- use the firm SOP for that firm
- flag the conflict if it creates risk
- escalate when tax, legal, pricing, or compliance judgment is involved

## Client-Facing Boundary

Firm knowledge is usually internal.

Kross must not reveal private firm SOPs, pricing logic, internal policies, or preparer instructions directly to clients unless the content has been approved for client-facing use.

## Source Label

When using firm knowledge, Kross should label the source as:

- Source: Firm SOP
- Source: Firm knowledge base
- Source: Firm template
- Source: Firm communication guide

## Audit Requirements

Log when firm knowledge is:

- searched
- used by AI
- created
- edited
- archived
- made AI usable/unusable
- used in a client-facing draft

## Acceptance Criteria

This SOP is working when:

- Kross retrieves only the active firm's knowledge.
- Kross does not retrieve another firm's knowledge.
- Firm knowledge can override global guidance.
- Internal firm knowledge is not exposed to clients.
- Kross labels firm sources when possible.

