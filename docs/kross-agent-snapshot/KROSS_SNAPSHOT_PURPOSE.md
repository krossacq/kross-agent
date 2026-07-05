# Kross Agent Hermes Snapshot

Purpose: Firm-level Kross Agent installation snapshot.

This repository is the Hermes-based starting point for Kross Agent, the agent installed for each tax firm inside the Tax Mogul Bureau ecosystem.

## Kross Agent Responsibilities

Kross Agent is responsible for firm-level tax office operations such as:

- using approved firm knowledge
- using selected client memory
- processing call transcripts
- drafting call summaries
- identifying missing documents
- drafting client-facing next steps
- drafting GHL client messages after approval
- helping move work through the Kross Queue
- staging TaxSlayer data entry inside the approved Tax Mogul white-label URL
- creating data-entry exception logs
- preparing payroll/reporting summaries from SBTPG or Refund Advantage
- handing work to preparers for review

## Kross Agent Must Not Be Confused With Kross Command

Kross Agent is not the bureau-level deployment/support agent.

Kross Agent should not create firm workspaces, deploy other agents, manage global infrastructure, or expose Tax Mogul Bureau private build details.

## Relationship To Hermes

Hermes is the base agent engine.

Kross Agent is the firm-specific operating layer built on top of Hermes.

## SOP Source

The current Kross Agent SOP drafts live here:

`/Users/sydnejones/Documents/The Tax Mogul Bureau/Kross Agent Skills and SOPs`

## Future Work

Add Kross Agent-specific:

- skills
- SOP bundles
- firm setup templates
- client workflow tools
- GHL tools
- TaxSlayer browser/data-entry tools
- meeting recorder tools
- payroll/reporting tools
- strict memory and permission guardrails
