# SOP 46: 1099-G Unemployment Entry

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross enters unemployment compensation from Form 1099-G.

## Core Rule

Kross may enter 1099-G data exactly as shown on the approved document.

## Required Data

- payer/state
- unemployment compensation
- federal withholding
- state withholding, if applicable
- tax year

## Stop Conditions

Stop if tax year is wrong, form is unreadable, payer/state is unclear, withholding values are missing or conflict, or client mentions unemployment but no form is uploaded.

## Acceptance Criteria

This SOP is working when 1099-G data is entered only from a confirmed document and missing forms are requested.
