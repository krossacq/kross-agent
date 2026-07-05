# SOP 08: Software Access Inventory

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Document every system Kross Agent needs for one firm, the approved access method, and the boundaries Kross must follow.

## Scope

This SOP applies to Kross Agent for Firms only.

The onboarding/access setup call is human-led by a Tax Mogul Bureau representative.

Kross Command may help create, verify, document, and troubleshoot these connections during onboarding, but Kross Agent does not lead the onboarding call or independently collect/approve access.

Kross Agent uses the approved access only after human-led setup is complete and only inside the assigned firm's workspace.

## Required Systems

Every firm access inventory must cover:

1. Kross Agent email through agentmail.to
2. Kross Acquisitions / GHL subaccount
3. Tax Mogul white-label TaxSlayer Pro
4. Tax Mogul Client Portal / Preparer Workspace
5. Firm-selected meeting recorder
6. SBTPG or Refund Advantage

## Master Access Matrix

| System | Required Access Method | Agent Email? | API Key? | Key Boundary |
| --- | --- | --- | --- | --- |
| Kross Acquisitions / GHL | API key/private integration | No, unless UI login is later needed | Yes | Kross may act only inside the firm's approved GHL subaccount/location. |
| Tax Mogul white-label TaxSlayer Pro | Login credentials and browser control | Yes | No | Kross may only use `https://thetaxmogul.cloudtaxoffice.com/`. |
| Tax Mogul Client Portal / Preparer Workspace | Firm-scoped Kross user and/or backend service access | Yes for UI login | To be confirmed | Kross may access only that firm's portal/workspace and authorized client records. |
| Meeting recorder | API/webhook/OAuth/export access | Maybe | Usually yes | Platform must provide reliable transcript access for automation. |
| SBTPG or Refund Advantage | Login credentials/reporting user | Yes | No unless later confirmed | Kross may pull reports only; it must not move money or change settings. |

## Access Inventory Fields

Record for each system:

- firm_id
- firm name
- system name
- access method
- login URL
- account username/email
- API key location, if applicable
- credential storage location
- MFA method
- permission level
- approved actions
- restricted actions
- setup date
- setup by
- last verified date
- offboarding instructions

## Tax Software Restriction

Kross Agent is approved for the Tax Mogul white-label TaxSlayer Pro software only:

- `https://thetaxmogul.cloudtaxoffice.com/`

Kross Agent must not operate in:

- Any other TaxSlayer white-label URL
- OLT
- TaxWise
- Drake
- ProSeries
- Any other tax software

unless Sydne explicitly adds that platform, creates access rules, and builds/approves platform-specific SOPs.

## Portal Access Record

The human setup rep records the portal access method chosen for the firm.

For MVP, the expected access method is:

- Firm-scoped Kross user login through the Tax Mogul Portal / Preparer Workspace.

If a dedicated Kross Agent API key or service access exists for that firm later, the human setup rep records it in the access inventory.

Kross Agent should not assume an access method. Kross uses only the access method documented for that firm.

## Acceptance Criteria

This SOP is working when:

- Every firm has a complete access inventory.
- Every system has an approved access method.
- Credentials are referenced by secure storage location, not written in the SOP.
- Kross is restricted to the approved firm and approved tools.
- Tax software access is limited to the Tax Mogul white-label TaxSlayer URL unless intentionally expanded later.
