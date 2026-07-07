# SOP 57: Kross Offboarding And Access Removal

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 9 - Governance And Launch

## Purpose

Define how Kross Agent access is removed when a firm cancels, pauses, changes ownership, or a credential is compromised.

## Core Rule

When access should end, Kross must be removed from every connected system.

## Systems To Review

- agentmail.to email
- Tax Mogul Portal / Preparer Workspace
- Kross Acquisitions GHL subaccount
- TaxSlayer white-label access
- meeting recorder platform
- SBTPG or Refund Advantage
- storage/reporting access
- AI/model provider access

## Offboarding Workflow

1. Confirm offboarding reason.
2. Disable Kross portal user or API access.
3. Revoke GHL API/private integration access if needed.
4. Disable TaxSlayer login.
5. Revoke bank product reporting login.
6. Disconnect meeting recorder access.
7. Archive or secure agentmail account.
8. Revoke or disconnect model provider OAuth/API access if the firm used a firm-owned provider account.
9. Remove the firm from any Tax Mogul-managed AI usage pool if applicable.
10. Rotate credentials if risk exists.
11. Log all removals.

## Acceptance Criteria

This SOP is working when cancelled or compromised access is fully removed and documented.
