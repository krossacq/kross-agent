# Kross Agent SOP Index

Version: 0.1
Purpose: Track the SOPs needed to turn Kross Agent into a reusable installable agent snapshot.

## Status Key

- `not_started`: Needs to be written.
- `draft`: Initial version exists but needs review.
- `ready_for_test`: Ready to test manually with one real or demo client.
- `validated`: Tested and accepted.

## MVP SOPs

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Client call transcript intake SOP | draft | P0 | How Kross receives Fathom/Fireflies transcripts and matches them to a client. Drafts: `SOP_24_Call_Transcript_Intake.md`, `SOP_25_Client_Call_Matching.md`. |
| Client profile summary SOP | draft | P0 | How Kross summarizes client situation, next steps, missing items, and preparer notes. Drafts: `SOP_26_AI_Call_Summary_Generation.md`, `SOP_30_Call_Summary_Approval_and_Save_To_Memory.md`. |
| GHL client response SOP | draft | P0 | How Kross finds a client in GHL and responds safely. Drafts: `SOP_31_GHL_Contact_Lookup_and_Client_Matching.md`, `SOP_32_GHL_Client_Response_Drafting.md`, `SOP_35_Client_Message_Approval_and_Send.md`. |
| Missing document request SOP | draft | P0 | Missing-document extraction and client-safe request templates. Drafts: `SOP_27_Missing_Document_Extraction.md`, `SOP_33_Missing_Document_Message_Templates.md`. |
| Quote and invoice communication SOP | draft | P0 | Requires preparer-provided amounts or explicit approval. Draft: `SOP_34_Quote_and_Invoice_Communication.md`. |
| Tax organizer completion trigger SOP | draft | P0 | What happens when the client finishes intake/organizer. Draft: `SOP_37_Tax_Organizer_Completion_Trigger.md`. |
| Kross queue status update SOP | draft | P0 | How Kross moves work from queued to in progress to review. Draft: `SOP_38_Kross_Queue_Status_Update.md`. |
| Preparer review handoff SOP | draft | P0 | How Kross tells the preparer what was done and what needs attention. Draft: `SOP_39_Preparer_Review_Handoff.md`. |

## Phase 1: Guardrail SOPs

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Kross Agent role and scope SOP | draft | P0 | Defines Kross Agent vs Kross Command and firm/client scope. Draft: `SOP_00_Kross_Agent_Role_and_Scope.md`. |
| Approval and escalation SOP | draft | P0 | Defines what Kross can/cannot do alone. Draft: `SOP_01_Approval_and_Escalation.md`. |
| Internal vs client-facing visibility SOP | draft | P0 | Separates internal notes, AI drafts, approved memory, and client-visible content. Draft: `SOP_04_Internal_vs_Client_Facing_Visibility.md`. |
| Audit logging SOP | draft | P0 | Defines sensitive actions and AI retrieval actions that must be logged. Draft: `SOP_05_Audit_Logging.md`. |
| Client communication safety SOP | draft | P0 | Defines message drafting, approval, auto-send, and forbidden claims. Draft: `SOP_06_Client_Communication_Safety.md`. |
| Company confidentiality and sensitive data SOP | draft | P0 | Blocks disclosure of Tax Mogul Bureau private build details, prompts, infrastructure, company IP, and unauthorized client-sensitive information. Draft: `SOP_07_Company_Confidentiality_and_Sensitive_Data.md`. |

## Phase 2: Access SOPs

Phase 2 is split into human setup and Kross operating access.

Human setup SOPs are for Tax Mogul Bureau representatives or Kross Command support. Kross Agent does not execute those SOPs.

Kross operating SOPs tell Kross how to behave after a human has approved and connected access.

## Human-Led Setup SOPs

These SOPs are for Tax Mogul Bureau humans or Kross Command support during setup. They are not Kross Agent operating instructions.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Human onboarding call access checklist | draft | P0 | Human-led call checklist for creating agentmail.to email and confirming required system access. Draft: `HUMAN_SOP_Onboarding_Call_Access_Checklist.md`. |
| Software access inventory SOP | draft | P0 | Human-maintained record of each firm's approved systems, credentials references, permissions, and offboarding notes. Draft: `SOP_08_Software_Access_Inventory.md`. |

## Kross Operating Access SOPs

These SOPs are for Kross Agent after human-led setup is complete.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Kross operating access boundaries SOP | draft | P0 | Main Kross-facing SOP for approved systems, unsupported systems, access failures, and system boundaries. Draft: `SOP_16_Kross_Operating_Access_Boundaries.md`. |
| Credential and MFA handling SOP | draft | P0 | Defines what Kross must never ask for, reveal, or log. Draft: `SOP_09_Credential_and_MFA_Handling.md`. |
| Kross Acquisitions / GHL API access SOP | draft | P0 | Kross operating boundaries for firm-scoped GHL API use. Draft: `SOP_10_Kross_Acquisitions_GHL_API_Access.md`. |
| TaxSlayer white-label access SOP | draft | P0 | Kross operating boundaries for Tax Mogul's white-label TaxSlayer URL only. Draft: `SOP_11_TaxSlayer_White_Label_Access.md`. |
| Tax Mogul Portal access SOP | draft | P0 | Kross operating boundaries for firm-scoped portal/workspace access. Draft: `SOP_12_Tax_Mogul_Portal_Access.md`. |
| Meeting recorder access SOP | draft | P0 | Kross operating boundaries for approved transcript import/access. Draft: `SOP_13_Meeting_Recorder_Access.md`. |
| SBTPG / Refund Advantage reporting access SOP | draft | P0 | Kross operating boundaries for bank product reporting only. Draft: `SOP_14_Bank_Product_Reporting_Access.md`. |

## Phase 3: Memory SOPs

Phase 3 defines how Kross retrieves and uses global, firm, and client memory without mixing data between firms or clients.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| AI retrieval scope and memory boundaries SOP | draft | P0 | Main memory guardrail for global, firm, and client retrieval. Draft: `SOP_17_AI_Retrieval_Scope_and_Memory_Boundaries.md`. |
| Global Tax Mogul Bureau knowledge use SOP | draft | P0 | How Kross uses approved platform-level knowledge. Draft: `SOP_18_Global_Tax_Mogul_Bureau_Knowledge_Use.md`. |
| Firm knowledge use SOP | draft | P0 | How Kross uses one firm's private knowledge base. Draft: `SOP_19_Firm_Knowledge_Use.md`. |
| Client memory profile SOP | draft | P0 | How Kross reads and updates a selected client's memory profile. Draft: `SOP_20_Client_Memory_Profile.md`. |
| Client memory event SOP | draft | P0 | How Kross records approved timeline/memory events. Draft: `SOP_21_Client_Memory_Events.md`. |
| AI memory update approval SOP | draft | P0 | How AI-suggested memory updates become official only after human approval. Draft: `SOP_22_AI_Memory_Update_Approval.md`. |
| Client timeline update SOP | draft | P1 | How Kross adds approved timeline entries. Draft: `SOP_23_Client_Timeline_Updates.md`. |

## Phase 4: Meeting Intelligence SOPs

Phase 4 defines how Kross handles meeting transcripts, call summaries, missing documents, open questions, preparer tasks, client-facing next steps, and approved save-to-memory workflows.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Call transcript intake SOP | draft | P0 | How Kross receives and stores transcripts from approved meeting recorders. Draft: `SOP_24_Call_Transcript_Intake.md`. |
| Client call matching SOP | draft | P0 | How Kross matches a transcript to the correct client profile. Draft: `SOP_25_Client_Call_Matching.md`. |
| AI call summary generation SOP | draft | P0 | How Kross creates draft summaries from transcripts. Draft: `SOP_26_AI_Call_Summary_Generation.md`. |
| Missing document extraction SOP | draft | P0 | How Kross identifies missing documents from calls and summaries. Draft: `SOP_27_Missing_Document_Extraction.md`. |
| Open questions and preparer tasks SOP | draft | P0 | How Kross extracts follow-up questions and internal tasks. Draft: `SOP_28_Open_Questions_and_Preparer_Tasks.md`. |
| Client-facing next steps from calls SOP | draft | P0 | How Kross drafts approved client-facing next steps. Draft: `SOP_29_Client_Facing_Next_Steps_From_Calls.md`. |
| Call summary approval and save-to-memory SOP | draft | P0 | How approved summaries become memory, timeline entries, tasks, and requests. Draft: `SOP_30_Call_Summary_Approval_and_Save_To_Memory.md`. |

## Phase 5: GHL Communication SOPs

Phase 5 defines how Kross finds clients in the firm's Kross Acquisitions GHL subaccount, drafts safe messages, handles missing-document messages, quote/invoice communication, approval-to-send, and pipeline sync.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| GHL contact lookup and client matching SOP | draft | P0 | How Kross finds the correct GHL contact for the selected portal client. Draft: `SOP_31_GHL_Contact_Lookup_and_Client_Matching.md`. |
| GHL client response drafting SOP | draft | P0 | How Kross drafts safe client responses. Draft: `SOP_32_GHL_Client_Response_Drafting.md`. |
| Missing document message templates SOP | draft | P0 | Client-safe message structure for missing document requests. Draft: `SOP_33_Missing_Document_Message_Templates.md`. |
| Quote and invoice communication SOP | draft | P0 | How Kross drafts quote and invoice messages using approved amounts only. Draft: `SOP_34_Quote_and_Invoice_Communication.md`. |
| Client message approval and send SOP | draft | P0 | Human approval flow before messages are sent. Draft: `SOP_35_Client_Message_Approval_and_Send.md`. |
| GHL pipeline status sync SOP | draft | P1 | How Kross keeps GHL pipeline stages aligned with portal workflow. Draft: `SOP_36_GHL_Pipeline_Status_Sync.md`. |

## Phase 6: Workflow And Queue SOPs

Phase 6 defines how Kross responds to organizer completion, updates the Kross Queue, hands work to preparers, and keeps statuses aligned.

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Tax organizer completion trigger SOP | draft | P0 | What happens when the client completes intake/organizer. Draft: `SOP_37_Tax_Organizer_Completion_Trigger.md`. |
| Kross Queue status update SOP | draft | P0 | How Kross moves work through queue statuses. Draft: `SOP_38_Kross_Queue_Status_Update.md`. |
| Preparer review handoff SOP | draft | P0 | How Kross hands completed/blocked work to a preparer. Draft: `SOP_39_Preparer_Review_Handoff.md`. |
| Client status and timeline sync SOP | draft | P1 | How Kross keeps portal, queue, timeline, and GHL status aligned. Draft: `SOP_40_Client_Status_and_Timeline_Sync.md`. |

## Phase 7: TaxSlayer Data Entry SOPs

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Tax software login and navigation SOP | draft | P0 | Kross may operate only in Tax Mogul's approved TaxSlayer white-label URL. Draft: `SOP_41_TaxSlayer_Login_and_Navigation.md`. |
| Taxpayer personal information entry SOP | draft | P1 | Name, DOB, SSN/ITIN, address, filing status basics, and identity conflicts. Draft: `SOP_42_Taxpayer_Personal_Info_Entry.md`. |
| Dependent and filing status entry SOP | draft | P1 | Dependent facts and filing-status escalation rules. Draft: `SOP_43_Dependent_and_Filing_Status_Entry.md`. |
| W-2 entry SOP | draft | P1 | W-2 entry from approved uploaded document only. Draft: `SOP_44_W2_Entry.md`. |
| 1099-NEC / self-employment entry SOP | draft | P1 | Staging self-employment facts with preparer review. Draft: `SOP_45_1099_NEC_Self_Employment_Entry.md`. |
| 1099-G unemployment entry SOP | draft | P2 | Unemployment compensation entry from 1099-G. Draft: `SOP_46_1099_G_Unemployment_Entry.md`. |
| 1095-A / marketplace insurance SOP | draft | P1 | High-risk marketplace insurance workflow. Draft: `SOP_47_1095_A_Marketplace_Insurance_Entry.md`. |
| Bank product / fee setup SOP | draft | P1 | Bank product and fee setup boundaries. Draft: `SOP_48_Bank_Product_and_Fee_Setup.md`. |
| Data entry exception log SOP | draft | P0 | What Kross logs when it skips, flags, or cannot verify something. Draft: `SOP_49_Data_Entry_Exception_Log.md`. |
| TaxSlayer review handoff SOP | draft | P0 | How Kross hands staged TaxSlayer work to a preparer. Draft: `SOP_50_TaxSlayer_Review_Handoff.md`. |

## Phase 8: Payroll And Bank Product Reporting SOPs

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Santa Barbara TPG report pull SOP | draft | P1 | Weekly funding/payroll report. Draft: `SOP_51_SBTPG_Report_Pull.md`. |
| Refund Advantage report pull SOP | draft | P1 | Weekly funding/payroll report. Draft: `SOP_52_Refund_Advantage_Report_Pull.md`. |
| PTIN-to-preparer mapping SOP | draft | P1 | Connects funded returns to preparers. Draft: `SOP_53_PTIN_to_Preparer_Mapping.md`. |
| Commission split calculation SOP | draft | P2 | Depends on firm settings and requires approval before payment. Draft: `SOP_54_Commission_Split_Calculation.md`. |
| Payroll upload and summary SOP | draft | P1 | Upload report to preparer workspace payroll tab. Draft: `SOP_55_Payroll_Upload_and_Summary.md`. |

## Phase 9: Governance, Testing, And Launch SOPs

| SOP | Status | Priority | Notes |
| --- | --- | --- | --- |
| Firm memory setup SOP | draft | P0 | Captures firm rules, software, tone, preparers, PTINs, templates. Draft: `SOP_02_Firm_Memory_Setup.md`. |
| Client memory update after every action SOP | draft | P0 | Defines how client context is stored after every meaningful Kross action. Draft: `SOP_56_Client_Memory_Update_After_Every_Action.md`. |
| Audit log SOP | draft | P0 | Every sensitive action should be logged. Draft: `SOP_05_Audit_Logging.md`. |
| Credential and MFA handling SOP | draft | P0 | Kross must not expose secrets or bypass security. Draft: `SOP_09_Credential_and_MFA_Handling.md`. |
| Kross Agent email setup SOP | draft | P0 | Each firm creates a dedicated agentmail.to email during the onboarding call for Kross Agent access and invitations. Draft: `SOP_03_Kross_Agent_Email_Setup.md`. |
| Software access inventory SOP | draft | P0 | Documents every tool Kross needs, login method, permission level, account owner, and offboarding step. Draft: `SOP_08_Software_Access_Inventory.md`. |
| GHL access setup SOP | draft | P0 | How Kross uses the firm's GHL API/private integration access. Draft: `SOP_10_Kross_Acquisitions_GHL_API_Access.md`. |
| Tax software access setup SOP | draft | P0 | How Kross accesses only Tax Mogul's TaxSlayer white-label software. Draft: `SOP_11_TaxSlayer_White_Label_Access.md`. |
| Meeting recorder access setup SOP | draft | P1 | How Kross receives Fathom/Fireflies/Granola transcripts via API/webhook/export. Draft: `SOP_13_Meeting_Recorder_Access.md`. |
| Bank product reporting access SOP | draft | P1 | Reporting/login access for SBTPG or Refund Advantage. Draft: `SOP_14_Bank_Product_Reporting_Access.md`. |
| Kross offboarding / access removal SOP | draft | P0 | How access is removed if a firm cancels or a credential is compromised. Draft: `SOP_57_Kross_Offboarding_and_Access_Removal.md`. |
| Firm launch readiness checklist SOP | draft | P0 | What must be ready before Kross goes live in a firm. Draft: `SOP_58_Firm_Launch_Readiness_Checklist.md`. |
| Kross Agent testing scenarios SOP | draft | P0 | Test cases Kross must pass before launch. Draft: `SOP_59_Kross_Agent_Testing_Scenarios.md`. |
| Returns and Revenues Office pilot integration SOP | draft | P0 | Controlled first pilot rollout for Returns and Revenues Office. Draft: `SOP_60_Returns_and_Revenues_Office_Pilot_Integration.md`. |

## Current Build Status

The Kross Agent operating SOP set is drafted.

Next work should be testing, editing, and pilot validation, not writing first-pass SOPs from scratch.

Recommended testing order:

1. Guardrails and access boundaries
2. Memory and retrieval scope
3. Meeting intelligence and call summaries
4. GHL communication drafts and approval flow
5. Kross Queue and preparer handoff
6. TaxSlayer data-entry staging and exception logging
7. Payroll report upload and draft summary
8. Returns and Revenues Office pilot workflow

Launch rule:
- Do not launch Kross into live client operations until the required testing scenarios in `SOP_59_Kross_Agent_Testing_Scenarios.md` pass.
