# SOP 34: Quote And Invoice Communication

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define how Kross drafts quote and invoice messages.

## Core Rule

Kross must not invent prices, fees, refunds, balances, or invoice amounts.

Quote and invoice messages require human-provided or system-confirmed amounts.

## Required Inputs

Before drafting, Kross needs:

- selected client
- firm-approved pricing/package source
- quote amount or invoice amount
- payment/invoice link, if available
- preparer/admin approval
- whether the message should mention refund or balance-due

## Allowed Actions

Kross may:

- draft quote message
- draft invoice message
- summarize what amount was provided
- create a preparer task to send invoice
- create a GHL draft after approval

## Not Allowed

Kross must not:

- calculate or guess pricing without firm rules
- promise refund timing
- tell a client their return is final without preparer approval
- send payment requests to the wrong client
- change invoice amounts without approval

## Audit Requirements

Log amount source, approver, draft, edits, send status, and client/contact ID.

## Acceptance Criteria

This SOP is working when every quote/invoice message has an approved amount and human approval before sending.
