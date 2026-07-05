# SOP 54: Commission Split Calculation

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 8 - Payroll And Bank Product Reporting

## Purpose

Define how Kross drafts commission or per-return payout calculations.

## Core Rule

Kross may calculate drafts using approved firm payroll rules, but a human must approve payroll before payment.

## Supported Pay Rules

Kross may support:

- flat amount per return
- percentage commission
- tiered commission if documented
- override/split if documented

## Required Inputs

- approved funding report
- PTIN-to-preparer mapping
- firm pay rule
- fee/revenue amount used for calculation
- deductions/adjustments if approved

## Must Escalate

Escalate if pay rules are missing, PTIN is unmatched, amount conflicts, split is unclear, or preparer disputes payout.

## Acceptance Criteria

This SOP is working when Kross produces payroll calculation drafts with source report references and human approval requirement.
