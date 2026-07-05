# SOP 11: TaxSlayer White-Label Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define the only approved tax software access for Kross Agent MVP.

## Approved Tax Software

Kross Agent may only operate inside Tax Mogul Bureau's white-label TaxSlayer Pro software:

- `https://thetaxmogul.cloudtaxoffice.com/`

This is Sydne's white-labeled bureau account with TaxSlayer.

## Unsupported Tax Software

Kross Agent must not operate in:

- Any other TaxSlayer white-label URL
- OLT
- TaxWise
- Drake
- ProSeries
- Any other tax software

unless Sydne explicitly adds support later with a separate approved access SOP and navigation/data-entry SOP.

## Access Method

TaxSlayer Pro does not provide the API access Kross needs for data entry.

Required method:

- Login credentials
- Browser/computer control inside the Kross VM
- Human-reviewed data-entry workflow

## Kross May Do

When authorized, Kross may:

- Log into the approved Tax Mogul TaxSlayer URL.
- Open or create returns according to the approved workflow.
- Enter organizer data.
- Save progress.
- Mark work ready for preparer review in the portal.
- Log exceptions and missing information.

## Kross Must Not Do

Kross must not:

- File or transmit returns.
- Use a non-approved TaxSlayer URL.
- Use any unsupported tax software.
- Change firm-level TaxSlayer settings.
- Delete returns.
- Guess missing tax information.
- Override preparer judgment.
- Enter data when client identity or tax year is unclear.

## Required Setup Fields

Record:

- firm_id
- approved URL
- username/email
- credential storage reference
- MFA method
- permission level
- preparer/ERO relationship
- last verified date

## Acceptance Criteria

This SOP is working when:

- Kross only uses `https://thetaxmogul.cloudtaxoffice.com/`.
- Kross refuses other tax software or white-label URLs.
- Kross saves work for preparer review and never files/transmits.
- Kross logs exceptions and missing information.

