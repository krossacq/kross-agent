# SOP 02: Firm Memory Setup

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Create the private firm-level memory Kross Agent needs to operate inside one tax firm's workspace.

## Scope

This SOP covers the firm brain only.

It does not cover:

- Global Tax Mogul Bureau knowledge.
- Individual client memory profiles.
- Kross Command onboarding automation.

## Firm Memory Principle

Each firm has its own private firm brain.

Firm A's knowledge must never be visible to Firm B. Kross Agent must retrieve firm knowledge only from the active firm workspace.

## Required Firm Memory Categories

Capture these categories during setup:

- Firm name and owner.
- Firm users, roles, and preparers.
- Tax software used.
- Bank product platform used.
- Meeting recorder used.
- GHL subaccount/location.
- Firm intake process.
- Firm tax-prep workflow.
- Firm review process.
- Firm document checklist.
- Firm pricing/packages.
- Firm communication style.
- Firm escalation rules.
- Firm turnaround time rules.
- Firm client service standards.
- Firm call scripts.
- Firm approved client message templates.
- Firm internal policies.
- Firm preferred AI prompts.
- Preparer PTIN mappings.
- Payroll/commission rules, if applicable.

## Firm Knowledge Item Fields

Each firm knowledge item should include:

- `firm_id`
- title
- content
- category
- tags
- status: active, inactive, archived
- visibility: internal, preparer_only, owner_admin_only
- `is_ai_accessible`
- source file/reference
- created by
- updated by
- created at
- updated at

## AI Accessibility Rule

Not every firm note should be usable by AI.

Firm owners/admins should decide whether each knowledge item is available to Kross Agent through the `is_ai_accessible` toggle.

Kross Agent may retrieve only firm knowledge where:

- `firm_id` matches the active firm.
- status is active.
- `is_ai_accessible` is true.
- visibility permits the current user/context.

## Setup Workflow

1. Open the firm's workspace.
2. Confirm firm owner/admin.
3. Confirm firm software stack.
4. Confirm firm roles and preparers.
5. Create or verify firm knowledge categories.
6. Add core firm SOPs and templates.
7. Add pricing and communication rules.
8. Add escalation rules.
9. Add preparer/PTIN mapping if payroll reporting will be used.
10. Mark each item active/inactive.
11. Toggle whether AI can use each item.
12. Run a test retrieval inside the firm workspace.
13. Confirm Kross retrieves only that firm's knowledge.

## Required Categories

Recommended starting categories:

- Intake
- Documents
- Tax Prep Workflow
- Review Process
- Client Communication
- Pricing
- Escalation
- Payroll
- Software Access
- Templates
- Preparer Preferences
- Internal Policies

## Audit Requirements

Log these actions:

- Firm knowledge item created.
- Firm knowledge item edited.
- Firm knowledge item archived/deleted.
- AI accessibility toggled.
- Firm knowledge searched.
- Firm knowledge used by AI.
- User permissions changed.

## Acceptance Criteria

This SOP is working when:

- A firm owner can add/edit/search firm knowledge.
- Firm knowledge is tagged and categorized.
- Kross can retrieve approved firm knowledge inside the correct firm workspace.
- Kross cannot retrieve another firm's knowledge.
- AI access can be toggled on/off per item.
- Firm knowledge changes are audited.

