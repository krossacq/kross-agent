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

## Offboarding Workflow

1. Confirm offboarding reason.
2. Disable Kross portal user or API access.
3. Revoke GHL API/private integration access if needed.
4. Disable TaxSlayer login.
5. Revoke bank product reporting login.
6. Disconnect meeting recorder access.
7. Archive or secure agentmail account.
8. Rotate credentials if risk exists.
9. Log all removals.

## Acceptance Criteria

This SOP is working when cancelled or compromised access is fully removed and documented.
