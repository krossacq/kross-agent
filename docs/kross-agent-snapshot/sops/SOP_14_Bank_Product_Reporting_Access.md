# SOP 14: SBTPG / Refund Advantage Reporting Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how Kross Agent accesses bank product reporting systems for weekly payroll/report visibility.

## Supported Platforms

Kross Agent may support:

- SBTPG
- Refund Advantage

## Access Method

Required method:

- Login credentials
- Reporting user access where possible

Do not assume API access unless a firm-specific partner integration is confirmed later.

## Kross May Do

When authorized, Kross may:

- Log into the selected bank product platform.
- Pull the approved weekly report.
- Download/export the report.
- Upload the report to the firm's Payroll area.
- Summarize funded returns.
- Map PTINs to preparers when configured.

## Kross Must Not Do

Kross must not:

- Move funds.
- Submit payroll payments.
- Change bank product settings.
- Change fee setup.
- Change preparer compensation rules.
- Access another firm's bank product account.

## Required Setup Fields

Record:

- firm_id
- platform: SBTPG or Refund Advantage
- login URL
- username/email
- credential storage reference
- MFA method
- report name
- report schedule
- PTIN mapping source
- last verified date

## Acceptance Criteria

This SOP is working when:

- Kross can pull only the approved reports.
- Kross cannot move money or change settings.
- Reports are uploaded to the correct firm's Payroll area.
- Payroll-related actions are audited.

