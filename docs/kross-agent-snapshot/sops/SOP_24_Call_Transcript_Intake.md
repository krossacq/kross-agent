# SOP 24: Call Transcript Intake

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how Kross Agent receives, imports, and prepares client call transcripts or recordings for review inside the Tax Mogul Client Portal / Preparer Workspace.

## Core Rule

Kross may process a call transcript only when the transcript is attached to the correct firm and the correct client.

If the firm or client cannot be confirmed, Kross must pause and ask a human to select the correct client before processing.

## Approved Transcript Sources

Kross may receive transcripts from approved meeting recorder platforms, including:

- Fathom
- Fireflies
- Granola
- another approved meeting recorder with API, webhook, export, or upload support
- manual transcript upload by an authorized firm user

The meeting recorder must be approved in the firm's software access inventory before Kross uses it.

## Required Intake Fields

Each transcript/call record should include:

- firm_id
- client_id
- call title
- call date
- participants
- transcript source
- source platform
- recording URL or file reference, if available
- transcript file reference
- uploaded/imported by
- import status
- created_at
- updated_at

## Intake Workflow

1. Receive transcript through approved import, webhook, API, or manual upload.
2. Confirm active firm/workspace.
3. Match transcript to the correct client.
4. Confirm user has permission to access that client.
5. Store transcript or transcript reference in secure storage.
6. Create call record in the client profile.
7. Mark call record as `ready_for_summary`.
8. Log transcript import.

## Consent And Disclosure

Before processing a call, Kross must rely on the firm's approved recording/transcription consent process.

If the transcript indicates a client objected to recording or AI processing, Kross must pause processing and escalate to a firm admin or preparer.

## What Kross Must Not Do

Kross must not:

- process calls for an unknown client
- guess client identity from transcript content when confidence is low
- attach a transcript to a client based only on a first name
- expose transcript content to another client or firm
- put raw transcript text into client-facing areas by default
- process unsupported meeting recorder accounts
- use transcript content outside the selected firm/client scope

## Audit Requirements

Log:

- transcript imported
- source platform
- matched firm/client
- user or system that imported it
- summary generation started
- failed or uncertain client match
- transcript viewed
- transcript downloaded
- transcript deleted/archived

## Acceptance Criteria

This SOP is working when:

- every transcript is tied to firm_id and client_id before summarization
- uncertain matches are escalated
- raw transcripts stay internal unless intentionally shared
- transcript imports are logged
- no cross-firm or cross-client transcript retrieval is possible
