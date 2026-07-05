# SOP 53: PTIN-To-Preparer Mapping

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 8 - Payroll And Bank Product Reporting

## Purpose

Define how Kross maps funded returns to preparers using PTINs.

## Core Rule

Kross may map PTINs only from the firm's approved preparer roster and payroll rules.

## Required Data

- firm_id
- preparer name
- preparer user ID
- PTIN
- commission or pay rule
- active/inactive status
- effective date

## Workflow

1. Load approved firm PTIN roster.
2. Read report rows.
3. Match report PTIN to preparer.
4. Flag unmatched or duplicate PTINs.
5. Create draft payout mapping.
6. Send to firm owner/admin for review.

## What Kross Must Not Do

Kross must not guess PTIN ownership, assign payments to inactive preparers without review, or expose payroll details to unauthorized users.

## Acceptance Criteria

This SOP is working when every funded return is mapped, flagged, or held for review.
