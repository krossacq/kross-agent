# Human SOP: Onboarding Call Access Checklist

Version: 0.1
Purpose: Human-led internal checklist for the onboarding call. This is not a Kross Agent operating SOP and not a client-facing form section.

## Classification

This is a human SOP for Tax Mogul Bureau representatives.

It tells the human onboarding rep what to confirm, create, and document during the onboarding call before Kross Agent receives access.

Kross Agent should not execute this SOP independently.

## Goal

During the onboarding call, help the firm create the Kross Agent operational identity and connect the software Kross needs to do its work.

## Human-Led Call Rule

The onboarding call is led by a human Tax Mogul Bureau representative.

Kross Agent does not independently lead onboarding calls, collect credentials, approve access, or decide which systems a firm should connect.

During the call:

- The human representative explains each access requirement.
- The human representative helps the firm create the agentmail.to email.
- The human representative confirms which systems the firm uses.
- The firm owner/admin approves access.
- Kross Command or internal setup support may assist with documentation and configuration.
- Kross Agent receives access only after the human-led setup and approval process is complete.

## Create Kross Agent Email

Create a dedicated Kross Agent email through agentmail.to during the onboarding call.

Recommended pattern:
- `firmname@agentmail.to`

Use this email for:

- Kross-specific software invitations
- Tax prep software user access where supported
- GHL user invitation if needed
- Meeting recorder notifications or transcript forwarding
- Bank product reporting access where supported
- Account recovery and MFA routing where appropriate

Do not use a preparer's personal email as the default Kross identity unless the software does not support separate users.

## Required Software Access Matrix

| System | Primary Access Method | Agent Email Needed? | API Key Needed? | Notes |
| --- | --- | --- | --- | --- |
| Kross Acquisitions / GHL subaccount | API access | No, unless UI login is later needed | Yes | Kross uses the firm's Kross Acquisitions/GHL API key for structured actions. Do not rely on GHL UI login unless explicitly added later. |
| TaxSlayer Pro via Tax Mogul white-label | Login credentials / browser control | Yes | No | Kross may only work inside Sydne's TaxSlayer white-label software at `https://thetaxmogul.cloudtaxoffice.com/`. No other TaxSlayer white-label, OLT, TaxWise, or tax software is supported unless Sydne explicitly adds it. |
| Tax Mogul Client Portal / Preparer Workspace | Firm-scoped Kross user and/or backend service access | Yes for UI login; API/service key only if the existing app supports it | To be confirmed after app inspection | Kross can access only that firm's specific Tax Mogul Portal workspace. Need developer inspection to confirm whether agent API/service-role access exists or must be built. |
| SBTPG or Refund Advantage | Login credentials / reporting user | Yes | No, unless a partner API is later confirmed | Kross needs credentials for the firm's selected bank product platform. Use reporting-only permissions if available. |
| Meeting recorder: Fathom, Fireflies, Granola, or similar | API/webhook access required for production automation | Maybe | Yes, if the platform uses API keys/OAuth | Firm admin may choose the recorder, but it must support API/webhook/transcript export access for Kross automation. |

## System-by-System Call Steps

### 1. Kross Acquisitions / GHL Subaccount

During onboarding:

1. Confirm the firm's GHL location/subaccount.
2. Confirm whether Kross should use API/private integration, UI login, or both.
3. Capture the approved GHL access method.
4. Confirm which actions Kross can take:
   - Read conversations
   - Send approved messages
   - Add notes
   - Apply tags
   - Move opportunities
   - Trigger workflows
5. Confirm actions Kross cannot take without approval:
   - Edit workflows
   - Change pipeline structure
   - Bulk message clients
   - Change billing or location settings

Recommended:
- API/private integration for standard actions.
- Agent email login only when UI-level access is needed.

### 2. Tax Software

Supported software for MVP:
- TaxSlayer Pro through Tax Mogul's white-label URL only: `https://thetaxmogul.cloudtaxoffice.com/`

Unsupported unless Sydne explicitly adds them later:
- Other TaxSlayer white-label URLs
- OLT
- TaxWise
- Any other tax software

During onboarding:

1. Confirm the firm will use the Tax Mogul white-label TaxSlayer Pro software.
2. Confirm the login URL is `https://thetaxmogul.cloudtaxoffice.com/`.
3. Confirm the firm's TaxSlayer login credentials/access method.
4. Confirm MFA process.
5. Confirm whether Kross is allowed to:
   - Create a new return
   - Open existing returns
   - Enter intake data
   - Save the return
   - Mark work ready for review
6. Confirm Kross is not allowed to:
   - File/transmit returns
   - Override preparer review
   - Change firm-level software settings
   - Delete returns

Recommended:
- Use agent email login plus browser/computer control in the Kross VM.
- Do not allow Kross Agent to operate in any other tax software or white-label URL unless Sydne has intentionally added support and SOPs for that platform.
- Do not build a Chrome extension until the Tax Mogul white-label TaxSlayer workflow is validated repeatedly.

### 3. Tax Mogul Client Portal / Preparer Workspace

During onboarding:

1. Confirm the firm's workspace.
2. Create or confirm the Kross Agent user/service role.
3. Confirm whether Kross uses UI login, backend API/service key, or both.
4. Confirm Kross permissions:
   - Read organizer answers
   - Read uploaded documents
   - Read client profile
   - Add notes/summaries
   - Update Kross queue status
   - Upload payroll reports
5. Confirm restricted actions:
   - Delete clients
   - Delete documents
   - Change firm settings
   - Change team permissions

Recommended:
- Use service/API access for structured backend updates.
- Use agent email login for visible/auditable workspace actions.
- Developer must inspect the existing portal architecture to determine whether API/service-role access already exists or needs to be built.

### 4. SBTPG or Refund Advantage

During onboarding:

1. Confirm which bank product platform the firm uses.
2. Confirm whether the platform supports a reporting-only user.
3. Create/invite Kross Agent using the agentmail.to email if supported.
4. Confirm report name and schedule.
5. Confirm PTIN/preparer mapping.
6. Confirm Kross can download reports and upload them to the payroll tab.
7. Confirm Kross cannot:
   - Move funds
   - Submit payments
   - Change bank product settings
   - Change fee setup

Recommended:
- Reporting-only login if possible.
- If reporting-only access is not available, owner must approve the lowest-access alternative.

### 5. Meeting Recorder

Supported examples:
- Fathom
- Fireflies
- Granola
- Similar call recording/transcription platforms with API/webhook/export access

During onboarding:

1. Confirm which meeting recorder the firm uses.
2. Confirm the recorder supports at least one production-ready integration path:
   - API access
   - Webhooks
   - OAuth/app connection
   - Automatic transcript export/forwarding that Kross can reliably ingest
3. Add the Kross Agent email if the recorder requires a user login or shared access.
4. Confirm where transcripts should go after each call:
   - Tax Mogul client profile
   - Obsidian firm/client memory
   - GHL note
   - All approved destinations
5. Confirm transcript matching rules:
   - Client name
   - Client email
   - Client phone
   - Meeting title
   - Tax year
   - Manual preparer selection when unclear
6. Confirm what Kross can do automatically:
   - Pull transcript
   - Summarize call
   - Extract missing items
   - Draft next steps
   - Add summary to client profile
7. Confirm what requires review:
   - Tax advice
   - Refund/balance-due language
   - Promises made on the call
   - Unclear facts or conflicting statements

Recommended:
- Use webhook/API transcript delivery where possible.
- If the platform cannot provide reliable API/webhook/export access, it should not be treated as supported for automated Kross meeting memory yet.
- Manual upload can be used as a temporary fallback, but not as the preferred production automation.

## Access Decision Rules

Use API key/private integration when:

- The system supports it.
- Kross needs structured, repeatable actions.
- The action can be permission-scoped and logged.
- The action does not require visual judgment.

Use agent email login when:

- The system has no API.
- The system requires normal user UI access.
- Kross needs to receive invites, MFA, notices, or exports.
- Browser/computer control is required.

Use both when:

- API is best for backend updates, but a visible user identity is needed for auditability, notifications, or UI-only tasks.

## Current MVP Recommendation

For the first version of Kross Agent:

| System | MVP Setup |
| --- | --- |
| Kross Acquisitions / GHL | API key/private integration. |
| Tax software | Tax Mogul white-label TaxSlayer login plus VM browser control at `https://thetaxmogul.cloudtaxoffice.com/` only. |
| Tax Mogul Client Portal | Firm-scoped Kross user and/or backend service access; developer must confirm current API/service-role support. |
| SBTPG / Refund Advantage | Agent email login with reporting-only permissions where possible. |
| Meeting recorder | Firm-selected platform with API/webhook/export access. |

## Research Notes

- GHL / HighLevel supports API access through private integrations and OAuth. For Kross MVP, use scoped private integration access where possible.
- Tax prep software should be treated as login/browser-control first. Kross MVP is restricted to Tax Mogul's white-label TaxSlayer URL: `https://thetaxmogul.cloudtaxoffice.com/`.
- Meeting recorder platforms vary. Kross only needs reliable transcript access, so the final method can be API/webhook, transcript forwarding, shared workspace access, or manual upload depending on the platform.
- SBTPG and Refund Advantage should be treated as reporting-login systems until a firm-specific API or partner integration is confirmed.
