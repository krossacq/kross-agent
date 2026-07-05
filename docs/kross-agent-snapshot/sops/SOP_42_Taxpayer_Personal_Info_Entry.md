# SOP 42: Taxpayer Personal Info Entry

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross enters taxpayer personal information into TaxSlayer.

## Core Rule

Kross may enter data from approved client-provided sources, but must flag uncertainty for preparer review.

## Data Sources

Approved sources may include:

- completed organizer
- client portal profile
- uploaded identification documents
- prior-year context if approved
- preparer notes

## Fields

Fields may include:

- taxpayer name
- spouse name
- SSN/ITIN where available through secure source
- date of birth
- address
- phone/email
- filing status, if confirmed
- occupation, if required

## Rules

Kross must verify the source before entry and avoid displaying sensitive identifiers in notes unless necessary.

## Stop Conditions

Stop and flag if identity fields conflict, SSN/ITIN is missing, filing status is unclear, or client information does not match portal records.

## Acceptance Criteria

This SOP is working when personal information is entered from approved sources and all conflicts are escalated.
