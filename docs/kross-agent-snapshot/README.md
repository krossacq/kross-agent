# Kross Agent Snapshot

This folder is the Tax Mogul Bureau Kross Agent snapshot layer built on top of the Hermes agent foundation.

Hermes is the base agent engine.

Kross Agent is the firm-level tax office operations agent installed for each approved tax firm.

## Snapshot Purpose

The purpose of this snapshot is to define what gets installed, taught, and enforced when a firm receives its own Kross Agent.

Kross Agent helps a firm with:

- firm knowledge retrieval
- client memory retrieval
- call transcript processing
- AI call summaries
- missing document detection
- open questions and preparer tasks
- GHL client communication drafts
- Kross Queue status updates
- TaxSlayer data-entry staging
- TaxSlayer exception logging
- preparer review handoff
- SBTPG / Refund Advantage report summaries
- payroll draft summaries

## Important Separation

Kross Agent is not Kross Command.

Kross Agent operates inside one firm workspace and must stay scoped to that firm and selected client.

Kross Command is the bureau-level deployment/support agent and should live in a separate repository.

## Folder Contents

- `KROSS_SNAPSHOT_PURPOSE.md` explains this snapshot's role.
- `sops/` contains the current Kross Agent SOP drafts.

## Launch Rule

Do not install this snapshot into live client operations until the testing scenarios in:

`sops/SOP_59_Kross_Agent_Testing_Scenarios.md`

have been run and passed.

## Security Rule

Kross Agent must never:

- mix firm data
- mix client data
- expose internal Tax Mogul Bureau build details
- reveal credentials or secrets
- send client-facing messages without approved rules
- file, finalize, or transmit tax returns without human preparer approval
