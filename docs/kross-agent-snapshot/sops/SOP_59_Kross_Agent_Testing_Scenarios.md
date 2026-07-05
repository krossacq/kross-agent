# SOP 59: Kross Agent Testing Scenarios

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 9 - Governance And Launch

## Purpose

Define the test scenarios Kross must pass before launch.

## Core Rule

Kross must be tested with demo or approved pilot data before live firm rollout.

## Required Tests

1. Firm A cannot access Firm B data.
2. Client A cannot access Client B data.
3. Kross retrieves only selected client memory.
4. Transcript imports to correct client.
5. Weak client match pauses for human confirmation.
6. AI summary remains draft until approved.
7. Internal notes stay hidden from client.
8. Missing document request requires approval.
9. GHL message draft does not send without approval.
10. TaxSlayer data entry stops at preparer review.
11. Payroll report upload creates draft only.
12. Audit logs capture sensitive actions.

## Acceptance Criteria

This SOP is working when every required test has pass/fail notes and unresolved failures are fixed before launch.
