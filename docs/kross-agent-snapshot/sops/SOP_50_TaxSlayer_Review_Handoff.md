# SOP 50: TaxSlayer Review Handoff

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 7 - TaxSlayer Data Entry

## Purpose

Define how Kross hands a TaxSlayer return back to the preparer after data entry assistance.

## Core Rule

Kross does not finalize, file, or transmit returns. Every return must go to preparer review.

## Handoff Includes

- data entered
- documents used
- fields skipped
- exceptions
- missing documents
- open questions
- risk flags
- areas requiring professional judgment
- TaxSlayer status

## Workflow

1. Stop data entry at approved handoff point.
2. Save work if supported.
3. Create data-entry summary.
4. Attach exception log.
5. Move Kross Queue to `ready_for_review`.
6. Notify preparer.
7. Log handoff.

## Acceptance Criteria

This SOP is working when preparer review receives a complete, transparent data-entry handoff.
