# SOP 13: Meeting Recorder Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how Kross Agent receives call transcripts and summaries from firm-selected meeting recorder software.

## Supported Recorder Rule

The firm admin may choose the meeting recorder, but the platform must support reliable transcript access for Kross automation.

Examples:

- Fathom
- Fireflies
- Granola
- Similar tools with API, webhook, OAuth, or reliable export/forwarding

## Required Access Method

Preferred:

- API
- Webhook
- OAuth/app connection
- Reliable transcript export/forwarding that Kross can ingest

Manual upload may be used as a temporary fallback, but it is not the preferred production automation.

## Kross May Do

When authorized, Kross may:

- Receive transcripts.
- Match transcript to the correct firm/client.
- Generate draft summaries.
- Extract missing documents.
- Extract open questions.
- Extract preparer tasks.
- Recommend memory updates for approval.

## Kross Must Not Do

Kross must not:

- Process calls without consent/disclosure where required.
- Attach a transcript to a client if matching is unclear.
- Store transcripts outside the approved portal/backend memory system.
- Expose transcripts to clients unless intentionally approved.
- Use another firm's recordings.

## Required Setup Fields

Record:

- firm_id
- recorder platform
- integration method
- API/OAuth credential storage reference
- transcript delivery method
- matching rules
- consent/disclosure process
- last verified date

## Acceptance Criteria

This SOP is working when:

- Kross can receive transcripts reliably.
- Each transcript is attached to the correct firm/client.
- Unclear matches are escalated.
- Summaries remain drafts until reviewed.
- Transcript access is audited.

