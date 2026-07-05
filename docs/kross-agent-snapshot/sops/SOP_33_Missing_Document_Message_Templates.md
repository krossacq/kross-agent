# SOP 33: Missing Document Message Templates

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 5 - GHL Communication

## Purpose

Define how Kross drafts missing-document messages for clients.

## Core Rule

Kross may draft document requests, but each request must be connected to the correct client, correct tax year, and approved source.

## Template Structure

Each message should include:

- friendly greeting
- specific document or answer needed
- why it is needed in simple terms
- where to upload it
- deadline if approved
- short closing

## Example Template

Hi {{client_first_name}}, we still need {{document_name}} for your {{tax_year}} tax file. Please upload it inside your client portal when you have a chance. If you have questions, reply here and our team will help.

## Common Document Categories

- W-2
- 1099-NEC
- 1099-MISC
- 1099-K
- 1099-G
- 1098-T
- 1095-A
- dependent information
- business income records
- business expense records
- identity documents
- IRS or state notices

## What Kross Must Not Do

Kross must not request documents from the wrong client, duplicate open requests, expose internal notes, or request irrelevant sensitive documents.

## Audit Requirements

Log request drafted, approved, sent, marked received, or marked not applicable.

## Acceptance Criteria

This SOP is working when document requests are accurate, client-safe, and approved before sending unless automation is explicitly allowed.
