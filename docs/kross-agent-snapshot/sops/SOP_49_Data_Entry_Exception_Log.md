# SOP 49: Data Entry Exception Log

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross logs issues, skipped fields, conflicts, and blockers during data entry.

## Core Rule

Kross must never silently skip a data-entry issue.

## Exception Types

- missing document
- unreadable document
- conflicting client data
- unsupported TaxSlayer screen
- missing credential/MFA
- preparer decision required
- uncertain tax treatment
- software error

## Required Fields

- firm_id
- client_id
- return/tax year
- exception type
- description
- source
- field/screen affected
- status
- assigned_to
- created_at

## Acceptance Criteria

This SOP is working when every blocker has a visible log entry and preparer handoff includes unresolved exceptions.
