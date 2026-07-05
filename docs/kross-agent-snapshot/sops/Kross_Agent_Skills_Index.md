# Kross Agent Skills Index

Version: 0.1
Scope: Kross Agent for Firms only

## Purpose

This document defines the skill set for Kross Agent inside an individual tax firm's workspace.

Kross Agent is not Kross Command.

- Kross Command helps Tax Mogul Bureau onboard, configure, deploy, and support firms.
- Kross Agent helps one tax firm operate its client workflow after setup.

Kross Agent must stay scoped to the firm and client context it is authorized to access.

## Skill Status Key

- `planned`: Defined but not built.
- `drafting`: SOP or prompt is being written.
- `ready_for_test`: Can be tested manually.
- `validated`: Tested with real or demo workflow.

## Core Skill Groups

### 1. Firm Context Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Firm Profile Reader | planned | Understand firm name, users, roles, software, bank product platform, and operating rules. |
| Firm Knowledge Retriever | planned | Retrieve only that firm's approved private SOPs, templates, pricing rules, and preferences. |
| Firm Voice Matcher | planned | Match the firm's approved communication style when drafting client messages. |
| Firm Escalation Router | planned | Know when to send issues to owner, admin, preparer, or Tax Mogul Bureau support. |

### 2. Client Memory Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Client Context Reader | planned | Read the selected client's memory profile, timeline, tasks, documents, and call summaries. |
| Client Memory Updater | planned | Draft memory updates for human approval before saving official memory. |
| Client Timeline Writer | planned | Add approved events to the client timeline. |
| Missing Info Detector | planned | Identify missing documents, unanswered questions, and incomplete organizer fields. |
| Client Visibility Guard | planned | Separate internal preparer notes from client-facing summaries and next steps. |

### 3. Meeting Intelligence Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Transcript Intake | planned | Import or receive transcripts from Fathom, Fireflies, or manual upload. |
| Call-to-Client Matcher | planned | Match a transcript to the correct firm and client. |
| Call Summary Generator | planned | Create a structured draft call summary for preparer review. |
| Call Action Extractor | planned | Extract missing documents, open questions, deadlines, preparer tasks, and client next steps. |
| Memory Update Recommender | planned | Recommend updates to long-term client memory based on approved call summaries. |

### 4. GHL Communication Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| GHL Contact Finder | planned | Locate the correct client/contact inside the firm's GHL subaccount. |
| Conversation Reader | planned | Read firm-scoped conversation history for the selected client. |
| Approved Message Drafter | planned | Draft missing-document, scheduling, quote, invoice, and follow-up messages. |
| Client Message Sender | planned | Send messages only after approval or when using approved templates. |
| Reply Monitor | planned | Watch for client replies and summarize them for the preparer. |

### 5. Tax Workflow Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Organizer Completion Checker | planned | Confirm whether a client organizer is complete enough for Kross queue. |
| Kross Queue Manager | planned | Move work through queued, in progress, needs review, and blocked states. |
| Data Entry Prep Reviewer | planned | Review organizer answers and documents before opening tax software. |
| Tax Software Navigator | planned | Navigate only Tax Mogul's white-label TaxSlayer Pro software at `https://thetaxmogul.cloudtaxoffice.com/` through browser control. |
| Data Entry Assistant | planned | Enter return data under supervised workflow and save for preparer review. |
| Data Entry Exception Logger | planned | Log missing, conflicting, unclear, or skipped information. |
| Preparer Review Handoff | planned | Summarize what Kross completed and what the preparer must review. |

### 6. Payroll Reporting Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Bank Product Report Puller | planned | Pull weekly reports from SBTPG or Refund Advantage. |
| PTIN Mapper | planned | Match funded returns to preparers by PTIN. |
| Payroll Summary Generator | planned | Prepare a firm-owner summary of funded returns and preparer payout context. |
| Payroll Upload Assistant | planned | Upload the report/summary to the firm's Payroll area. |

### 7. Governance and Safety Skills

| Skill | Status | Purpose |
| --- | --- | --- |
| Scope Guard | planned | Prevent cross-firm or cross-client data mixing. |
| Approval Gatekeeper | planned | Require human approval for sensitive actions. |
| Audit Event Writer | planned | Log sensitive access, AI retrieval, memory updates, and communication actions. |
| Source Citation Helper | planned | Label answer sources such as Firm SOP, Client Memory, Call Summary, or Uploaded Document. |
| Credential Boundary Guard | planned | Avoid exposing credentials, MFA codes, or secrets in prompts, notes, or logs. |

## MVP Skill Set

The first testable Kross Agent should include:

1. Scope Guard
2. Approval Gatekeeper
3. Firm Profile Reader
4. Firm Knowledge Retriever
5. Client Context Reader
6. Transcript Intake
7. Call Summary Generator
8. Call Action Extractor
9. Missing Info Detector
10. Approved Message Drafter
11. Kross Queue Manager
12. Audit Event Writer

## Skills That Must Wait Until Guardrails Are Validated

These are valuable, but should not be trusted until scope, permissions, audit logs, and approval flows are proven:

- Client Message Sender
- Tax Software Navigator
- Data Entry Assistant
- Bank Product Report Puller
- Payroll Upload Assistant
