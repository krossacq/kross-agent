# SOP 27: Missing Document Extraction

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how Kross Agent identifies missing documents from a client call transcript or summary.

## Core Rule

Kross may identify possible missing documents, but a human should review before client-facing document requests are sent or displayed.

## Sources Kross May Use

Kross may identify missing documents from:

- call transcript
- approved call summary
- client organizer answers
- firm document checklist
- Tax Mogul Bureau default document templates
- preparer notes
- existing document requests
- uploaded document list

## Extraction Workflow

1. Confirm firm and client.
2. Review transcript or approved summary.
3. Compare mentioned documents against uploaded documents and open requests.
4. Identify missing documents.
5. Label each item as confirmed, likely, or needs_review.
6. Draft document request items.
7. Ask for human review before making client-facing.
8. Log extraction and approval.

## Missing Document Fields

Each missing document item should include:

- firm_id
- client_id
- document name
- document category
- tax year
- reason needed
- source_type
- source_id
- status
- visibility
- requested_by
- approved_by
- created_at

## Statuses

Recommended statuses:

- draft
- pending_review
- requested
- received
- not_applicable
- blocked
- archived

## Client-Facing Rules

Kross may draft client-facing document requests, but must not send or publish them without approval unless the firm has an approved automation rule.

Client-facing requests must be clear, simple, and limited to what the client needs to provide.

## What Kross Must Not Do

Kross must not:

- request documents from the wrong client
- duplicate existing open requests
- mark a document as received without evidence
- expose internal reasoning to the client
- request sensitive documents that are not relevant to the client's situation
- imply a final tax position based only on missing document extraction

## Audit Requirements

Log:

- missing document detected
- source used
- request drafted
- request approved
- request sent or made visible
- document marked received
- item marked not applicable

## Acceptance Criteria

This SOP is working when:

- missing document items are tied to firm_id and client_id
- duplicate requests are avoided
- client-facing requests require approval
- document status changes are logged
