# SOP 44: W-2 Entry

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross enters W-2 information into TaxSlayer.

## Core Rule

Kross may enter W-2 data exactly as shown on the uploaded W-2. Kross must not guess missing boxes.

## Required Source

Kross needs a readable W-2 image/PDF or verified extracted data tied to the correct client and tax year.

## Entry Rules

Kross should enter employer information, wages, federal withholding, Social Security wages/tax, Medicare wages/tax, state/local wages, and state/local withholding exactly as provided.

## Stop Conditions

Stop if:

- document is unreadable
- tax year does not match
- employer EIN is missing/unclear
- box values are inconsistent or cut off
- client has multiple W-2s and one is missing

## Acceptance Criteria

This SOP is working when W-2 entries match the uploaded document and exceptions are logged.
