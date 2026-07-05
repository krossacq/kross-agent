# SOP 31: GHL Contact Lookup And Client Matching

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define how Kross Agent finds the correct client/contact inside the firm's Kross Acquisitions GoHighLevel subaccount.

## Core Rule

Kross may use GHL only inside the approved firm subaccount. Kross must never search across unrelated GHL subaccounts or use one firm's GHL data for another firm.

## Approved Matching Signals

Kross may match by:

- portal client ID linked to GHL contact ID
- exact email match
- exact phone match
- full name plus email or phone
- existing firm-approved contact mapping

## Weak Match Handling

If the match is weak, duplicate, or uncertain, Kross must pause and ask an authorized firm user to confirm the contact.

## What Kross Must Not Do

Kross must not:

- message a contact without confirmed client identity
- merge GHL contacts without approval
- expose another client's information
- search outside the firm's approved GHL subaccount
- use GHL data to bypass portal permissions

## Audit Requirements

Log GHL lookup, match method, confirmed contact ID, uncertainty, manual confirmation, and any failed lookup.

## Acceptance Criteria

This SOP is working when Kross can find the correct GHL contact for a selected client and pauses on duplicates or uncertainty.
