# SOP 25: Client Call Matching

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Phase: 4 - Meeting Intelligence

## Purpose

Define how Kross Agent matches a call transcript or meeting record to the correct client profile.

## Core Rule

Kross must match calls conservatively.

If Kross is not confident that the transcript belongs to one specific client inside the active firm, Kross must ask a human to confirm.

## Matching Signals

Kross may use these signals:

- selected client at upload time
- client email
- client phone number
- meeting attendee email
- meeting title
- linked calendar event
- GHL contact ID
- portal client ID
- tax organizer/client portal record
- exact full name match inside the same firm

## Strong Match

A strong match exists when at least one reliable identifier points to one client only, such as:

- portal client ID
- selected client during upload
- exact email match inside active firm
- exact phone match inside active firm
- GHL contact ID already linked to the portal client

Kross may proceed with summarization after a strong match.

## Weak Match

A weak match includes:

- first name only
- last name only
- similar name
- meeting title without email or phone
- transcript mentions that could apply to multiple clients
- duplicate client records

Kross must not process weak matches without human confirmation.

## No Match

If no client match is found, Kross should:

1. Create an unmatched transcript record.
2. Show possible matches, if any.
3. Ask a human to select or create the correct client.
4. Avoid summarization until the client is selected.
5. Log the unmatched status.

## Duplicate Match

If more than one client could match, Kross must:

- pause processing
- display the possible clients to an authorized firm user
- ask for confirmation
- avoid exposing private details in the match list beyond what the user is authorized to see

## What Kross Must Not Do

Kross must not:

- attach a transcript to a client without confirmed firm_id and client_id
- choose between duplicate clients based on guesswork
- use another firm's client records for matching
- reveal transcript content while asking a client-facing user to confirm a match
- merge duplicate clients without human approval

## Audit Requirements

Log:

- automatic match
- manual match
- confidence level, if available
- identifiers used
- duplicate match detected
- no match detected
- user who confirmed the match

## Acceptance Criteria

This SOP is working when:

- strong matches can proceed
- weak matches require human confirmation
- unmatched calls do not become official memory
- duplicate client matches are escalated
- matching is always scoped to one firm
