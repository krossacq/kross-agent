# SOP 03: Kross Agent Email Setup

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Create a dedicated operational email identity for Kross Agent during the onboarding call.

## Scope

This SOP covers the Kross Agent email used for one firm's Kross Agent.

This email is not collected on the client-facing onboarding form. It is created or confirmed live during the onboarding call.

The onboarding call is led by a human Tax Mogul Bureau representative. Kross Agent does not independently create its own email, collect credentials, approve access, or lead the firm through onboarding.

## Core Rule

Kross Agent should use its own dedicated email identity wherever possible instead of a preparer's personal email.

Recommended provider:

- agentmail.to

Recommended format:

- `firmname@agentmail.to`

## What The Email Is Used For

Use the Kross Agent email for:

- Tax software invitations when the software supports separate users.
- GHL user invitation if UI login is needed.
- Meeting recorder access, transcript forwarding, or notifications.
- SBTPG / Refund Advantage reporting user access if supported.
- Account recovery notices for Kross-specific accounts.
- Kross-specific software alerts.
- MFA routing only when approved and secure.

## What The Email Is Not Used For

Do not use the Kross Agent email for:

- Personal preparer communication.
- Client-facing communication unless deliberately branded that way.
- Storing passwords in plain text.
- Receiving sensitive files without an approved secure handling workflow.
- Sharing one email across multiple firms.

## Setup Workflow

1. Human representative explains why the firm needs a dedicated Kross Agent email.
2. Human representative helps the firm create or confirm the firm's agentmail.to address.
3. Firm owner/admin approves the email identity for Kross Agent use.
4. Human representative records the email in the internal access inventory, not the public onboarding form.
5. Human representative confirms who owns/administers the email.
6. Human representative confirms password and MFA handling.
7. Human representative or Kross Command uses this email for software invitations where appropriate.
8. Human representative adds the email to the firm's Kross Agent access profile.
9. Human representative confirms offboarding steps for disabling or transferring access.

## Access Inventory Fields

Record:

- Firm name.
- Kross Agent email.
- Email owner/admin.
- Recovery method.
- MFA method.
- Credential storage location.
- Systems invited with this email.
- Date created.
- Created by.
- Offboarding notes.

## Security Rules

- Do not store the password in SOP files, prompts, transcripts, screenshots, or Obsidian.
- Store credentials only in the approved secret store.
- Do not share the same Kross Agent email across firms.
- Disable or revoke the email/access if a firm cancels.
- Log every system connected to the email.

## Acceptance Criteria

This SOP is working when:

- Each firm has a unique Kross Agent email.
- The email is recorded in the internal access inventory.
- The email is used for Kross-specific software access where appropriate.
- Credentials and MFA are handled securely.
- The email can be revoked/offboarded cleanly.
