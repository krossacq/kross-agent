# SOP 47: 1095-A Marketplace Insurance Entry

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross handles marketplace insurance Form 1095-A.

## Core Rule

If the client had marketplace insurance, Kross must require Form 1095-A or preparer direction before the return proceeds.

## Data Kross May Enter

Kross may enter monthly premium, SLCSP, and advance premium tax credit amounts exactly as shown on Form 1095-A.

## Must Escalate

Escalate if:

- client says they had marketplace insurance but no 1095-A is uploaded
- form is corrected/voided
- monthly amounts are missing
- household coverage allocation may apply
- dependents or filing status affect premium tax credit

## Acceptance Criteria

This SOP is working when marketplace insurance issues are never ignored and all 1095-A entries come from the official form.
