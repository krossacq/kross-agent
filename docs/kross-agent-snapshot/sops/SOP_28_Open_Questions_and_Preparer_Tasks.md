# SOP 28: Open Questions And Preparer Tasks

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how Kross Agent extracts open questions and preparer tasks from client calls.

## Core Rule

Kross may draft questions and tasks, but the firm remains responsible for reviewing and deciding what should be assigned, sent, or completed.

## Open Questions

Open questions are unanswered items that need follow-up, such as:

- client needs to confirm income details
- client needs to explain a business expense
- client needs to confirm dependent information
- preparer needs to verify eligibility
- client needs to clarify IRS/state notice details
- firm needs to confirm pricing, quote, or invoice details

## Preparer Tasks

Preparer tasks are internal actions, such as:

- review uploaded document
- verify organizer answer
- ask client for missing detail
- prepare quote
- send invoice after approval
- check TaxSlayer entry issue
- review risk flag
- approve memory update
- approve client-facing summary

## Extraction Workflow

1. Confirm firm and client.
2. Review transcript or summary.
3. Extract open questions.
4. Extract preparer tasks.
5. Separate client-facing questions from internal-only tasks.
6. Assign draft priority and due date if available.
7. Attach source reference.
8. Save as draft or pending review.
9. Request human approval for client-facing items.
10. Log creation and updates.

## Required Fields

Each question/task should include:

- firm_id
- client_id
- type
- title
- description
- assigned_to, if known
- due_date, if known
- priority
- status
- visibility
- source_type
- source_id
- created_by
- created_at

## Visibility Rules

Internal-only tasks may be visible to authorized firm users.

Client-facing questions or next steps require approval before they appear in the client portal or are sent through GHL.

## What Kross Must Not Do

Kross must not:

- assign tasks to unauthorized users
- expose internal preparer notes to clients
- mark tasks complete without evidence
- create client-facing questions from uncertain facts without review
- create tasks for another firm or client
- include sensitive data in task titles when not necessary

## Audit Requirements

Log:

- task/question drafted
- task/question assigned
- visibility changed
- client-facing approval
- task completed
- task archived
- task used in AI retrieval

## Acceptance Criteria

This SOP is working when:

- open questions and tasks are separated
- internal and client-facing visibility is respected
- tasks are attached to the correct firm/client
- client-facing items require approval
