# Kross Agent Blueprint

Version: 0.1
Owner: Sydne Jones
Product layer: Tax firm installed agent

## Agent Family

There are two separate Kross roles.

### Kross Command

Kross Command supports Sydne at the bureau level.

Primary responsibility:
- After a tax professional purchases and joins the Tax Moco Bureau, Kross Command helps build, configure, connect, and maintain that firm's setup.

Kross Command is not the focus of this document.

### Kross Agent

Kross Agent is installed inside each tax firm's office.

Primary responsibility:
- Help that tax office operate more efficiently by understanding client situations, assisting with client communication, performing data entry workflows, updating the preparer workspace, and producing payroll/reporting outputs.

Kross Agent is the focus of this document.

## Product Context

Sydne has already built a multi-tenant tax office platform with:

- Client portal
- Preparer workspace
- Tax organizer / intake flow
- Client stages and return status tracking
- Document collection
- Quote and invoice workflows
- Kross queue / review workflow
- Payroll area
- Referral tracking
- Firm/team management
- Connection to Kross Acquisitions, Sydne's GHL agency

The core industry problem is the disconnect between client acquisition and client workflow execution. Tax professionals often have leads, text/email conversations, intake forms, tax software, document requests, return review, and payroll reporting living in separate systems.

The platform already connects the tax workflow to GHL pipeline stages through webhooks. That means the software can know where a client is in the tax process, and GHL can trigger the right communication and opportunity movement.

Kross Agent adds the labor layer on top of that system.

## Mission

Kross Agent helps a tax office turn client information into action.

Kross Agent should:

- Understand each taxpayer's situation through calls, transcripts, summaries, organizer answers, documents, and communication history.
- Learn how the tax preparer thinks, answers questions, handles edge cases, and communicates with clients.
- Help respond to taxpayer questions in the firm's preferred tone.
- Enter client information into tax preparation software after the organizer is complete.
- Update the preparer workspace when Kross completes its part of the workflow.
- Communicate with taxpayers through GHL when the preparer gives instructions.
- Pull weekly bank product payroll reports and upload/report them inside the preparer workspace.

## Core Systems

Kross Agent may need access to:

- Tax Moco / Tax Mogul client portal
- Tax Moco / Tax Mogul preparer workspace
- GHL / Kross Acquisitions client communication system
- Fathom, Fireflies, or another call recorder/transcription tool
- Tax Mogul white-label TaxSlayer Pro software at `https://thetaxmogul.cloudtaxoffice.com/`
- Santa Barbara TPG
- Refund Advantage
- Firm Slack or Telegram channel
- Secure document storage
- Agent memory / knowledge base

## Software Access Model

Kross Agent needs controlled access to the software it is expected to operate.

Each firm should have a Kross Agent access profile that documents:

- Dedicated Kross Agent email address, created through agentmail.to during the onboarding call
- Software name
- Purpose of access
- Login URL or app location
- Account owner
- Username or service account identifier
- Permission level
- MFA method
- Credential storage location
- Whether Kross can act automatically or only with approval
- Emergency lockout/offboarding steps

Access should be role-based wherever possible. Kross should use its own account or service account instead of a preparer's personal login unless the software does not support separate users.

Each firm should create or provide a dedicated Kross Agent email through agentmail.to during the onboarding call. This email becomes Kross Agent's operational identity for software invitations, tax prep software access where supported, meeting recorder notifications, secure account recovery, and other agent-specific setup needs.

### Required Access Categories

Kross Agent needs access in these categories.

| Category | Access Needed | Purpose |
| --- | --- | --- |
| Preparer workspace | Kross user or service role | Read client records, read organizer answers/documents, update Kross queue, add notes, upload payroll reports. |
| Client portal admin view | Controlled internal access | Understand what the client submitted and what they still need. |
| GHL subaccount/location | User/API access | Read conversations, send approved messages, update notes/tags/opportunities. |
| Tax prep software | Firm-specific Kross login or controlled remote access for Tax Mogul's white-label TaxSlayer Pro URL only | Enter organizer data into the return and save for preparer review inside `https://thetaxmogul.cloudtaxoffice.com/`. |
| Meeting recorder | Transcript/API/webhook/export access or agent email login | Pull Fathom, Fireflies, or other call transcripts and summaries. |
| Bank product software | Reporting-only access where possible | Pull weekly funded/paid return reports from Santa Barbara TPG or Refund Advantage. |
| File/document storage | Read/download access | Review uploaded tax documents needed for data entry. |
| Slack/Telegram | Bot/app access | Receive preparer instructions and provide updates. |
| Agent memory/knowledge base | Read/write access | Store firm rules, client summaries, SOP outcomes, and learned preferences. |

### Access Boundaries

Kross Agent should have the minimum permissions required to complete its assigned work.

Kross Agent should not have unrestricted owner/admin access unless there is no alternative and the owner explicitly approves it.

Kross Agent should not:

- Create or delete firm users without owner approval.
- Change billing settings.
- Change GHL workflow logic.
- Change tax software configuration.
- Change bank product configuration.
- Submit payroll payments.
- File or transmit returns.
- Delete client records or documents.
- Export bulk client data unless explicitly approved.

### Credential Handling

Credentials should be stored in a secure credential manager or approved secret store, not inside SOP files, prompts, screenshots, transcripts, or plain-text notes.

Kross Agent may reference where a credential is stored, but should not reveal the secret value in normal conversation or logs.

Every firm should have an offboarding process that removes or disables Kross access from:

- GHL
- Tax prep software
- Bank product software
- Meeting recorder
- Portal/preparer workspace
- Slack/Telegram
- File storage
- VM/server access

## Capability 1: Meeting Intelligence

Purpose:
- Convert client calls into useful tax-office intelligence.

Inputs:
- Fathom transcript
- Fireflies transcript
- Other meeting recorder transcript
- Call summary
- Associated client profile
- Tax preparer notes

Kross Agent should extract:

- Client name
- Tax year(s) discussed
- Filing situation
- Household situation
- Dependents discussed
- Employment/self-employment context
- Business income context
- Documents mentioned
- Missing documents
- Questions the client asked
- Concerns or objections
- Promises made by the preparer
- Next steps
- Tone/style of how the preparer answered the client
- Any special handling instructions

Kross Agent should then:

- Create a concise client summary.
- Add the summary/transcript reference to the client profile inside the portal.
- Update the client context so Kross can better answer future questions.
- Learn the tax preparer's reasoning style and communication preferences over time.

Important distinction:
- Kross Agent should not blindly treat every transcript statement as tax truth. It should store what was said, identify uncertainty, and flag anything that needs preparer review.

## Capability 2: Client Service Through GHL

Purpose:
- Help the tax office respond to taxpayer questions and move stalled clients forward.

Inputs:
- GHL conversation history
- Client portal status
- Organizer status
- Document checklist
- Meeting intelligence summaries
- Tax preparer instructions
- Firm communication style

Kross Agent should be able to:

- Answer general process questions.
- Remind clients to complete the organizer.
- Ask clients for missing documents.
- Send review call booking links.
- Ask whether the client wants to move forward after a quote.
- Send invoices when instructed.
- Follow up when a client is stuck.
- Escalate questions to the preparer when the answer requires judgment.

Examples:

- "Ask Mary Johnson to upload her 1095-A."
- "Text Tanya Reed to rebook her review call."
- "Send this client their quote and ask if they want to move forward."
- "Send an invoice for $425."

Default communication rules:

- Be clear, warm, and professional.
- Do not sound robotic.
- Match the firm's voice when known.
- Do not over-explain unless the client asks.
- Do not make guarantees about refunds, filing outcomes, timing, or IRS/state decisions.
- Escalate uncertain tax advice to the preparer.

## Capability 3: Tax Data Entry

Purpose:
- After a taxpayer completes the client intake/organizer, Kross Agent enters the information into the tax preparation software.

Trigger:
- Client completes the intake form / tax organizer.
- System moves the client into the Kross queue.
- Kross Agent receives a task to begin data entry.

Inputs:
- Completed intake/organizer
- Uploaded documents
- Prior-year data if available
- Tax year
- Client profile
- Firm-specific tax prep software
- Firm-specific data entry SOP

Workflow:

1. Open the client's profile in the preparer workspace.
2. Review organizer completion and uploaded documents.
3. Open the tax preparation software.
4. Enter client data according to the SOP.
5. Track fields completed and fields skipped.
6. Flag missing or unclear information.
7. Save progress.
8. Update the Kross tab/status from `in_progress` to `review`.
9. Add a note for the preparer explaining what was completed and what needs review.

Kross Agent should not:

- File a return.
- Finalize tax positions without preparer review.
- Override preparer judgment.
- Guess at missing tax information.
- Invent numbers.
- Ignore inconsistencies.

## Capability 4: Review Support, Quotes, Invoices, and Missing Items

Purpose:
- Let the preparer use Kross Agent as an execution assistant after Kross completes the first pass of data entry.

Preparer may instruct Kross Agent to:

- Request missing documents.
- Send a quote.
- Send refund/balance-due summary language approved by the preparer.
- Ask whether the client wants to move forward.
- Send an invoice.
- Book or rebook a review call.
- Update the client status after communication.

Kross Agent should:

- Use GHL to find the client profile.
- Send the approved message.
- Log the action.
- Update the preparer workspace when needed.
- Watch for replies and summarize them for the preparer.

Approval rule:
- Kross Agent can send simple missing-document and scheduling messages automatically if they follow approved templates.
- Kross Agent should require preparer approval before sending refund amounts, balance due amounts, final pricing, invoices, or tax-position explanations unless the preparer has explicitly provided the exact message/value.

## Capability 5: Weekly Payroll Reporting

Purpose:
- Help the office understand which returns are being funded and which preparers should be paid.

Systems:
- Santa Barbara TPG
- Refund Advantage
- Preparer workspace payroll tab

Workflow:

1. On a weekly schedule, log into the correct bank product software.
2. Pull the report showing funded/paid returns for the week.
3. Download/export the report.
4. Upload the report into the preparer workspace under Payroll.
5. Parse PTIN numbers to identify the preparer tied to each return.
6. Calculate or prepare payroll visibility based on firm settings:
   - Commission split
   - Flat pay per return
   - Other firm-defined pay rules
7. Add a summary for the office owner.

Kross Agent should not:

- Move money.
- Submit payroll payments.
- Change bank product settings.
- Change preparer compensation settings without owner approval.

## Agent Memory

Kross Agent needs memory at four levels.

### Firm Memory

- Firm name
- Owner/preparer names
- Team roles
- Preferred tone
- Business rules
- Pricing rules
- Commission/payroll rules
- Tax software used
- Bank product software used
- GHL location/subaccount details
- Approved templates
- Escalation rules

### Preparer Memory

- How each preparer explains tax concepts
- How each preparer handles common questions
- Preparer-specific preferences
- PTIN mapping
- Communication style

### Client Memory

- Client profile
- Tax year(s)
- Organizer answers
- Documents received
- Meeting summaries
- Current stage
- Missing items
- Quote/invoice status
- Communication history
- Special concerns

### SOP Memory

- How to use the portal
- How to use GHL
- How to use the tax software
- How to complete data entry
- How to pull payroll reports
- How to escalate issues

## MVP Scope

The first launchable version of Kross Agent should focus on the smallest useful set of tasks.

Recommended MVP:

1. Meeting transcript intake and client summary posting.
2. Missing document / stalled client communication through GHL.
3. Kross queue data-entry task management with manual or semi-automated status updates.
4. Preparer-directed client messages for quotes, invoices, and review calls.
5. Payroll report upload workflow, even if parsing/calculation starts semi-manual.

Data entry automation should be built carefully. For MVP, the first milestone can be a guided or supervised data entry flow before Kross is trusted to run the full process unattended.

## Approval Boundaries

Kross Agent can usually do without approval:

- Summarize calls.
- Store transcript summaries.
- Identify missing information.
- Draft client messages.
- Send approved-template reminders.
- Update internal notes.
- Move a task from waiting to in progress when triggered.
- Upload non-financial reports when following the SOP.

Kross Agent needs approval before:

- Sending refund/balance-due numbers.
- Sending final quotes unless values are provided by the preparer.
- Sending invoices unless the preparer gives the amount.
- Giving tax advice.
- Making tax elections.
- Marking a return ready to file.
- Submitting or filing anything.
- Changing pricing rules.
- Changing payroll rules.
- Deleting client records or documents.
- Changing GHL workflows/pipelines.
- Changing tax software settings.

Kross Agent should escalate when:

- A client asks a tax/legal/compliance question requiring judgment.
- Organizer answers conflict with documents.
- Documents are missing or unclear.
- A transcript contains a promise, refund statement, or unusual fact pattern.
- The software behaves differently than expected.
- Login, MFA, or permission issues occur.

## First SOPs To Build

These are the documents Kross Agent needs before it can become a reusable snapshot.

1. Client call transcript intake SOP
2. Client profile summary SOP
3. GHL client response SOP
4. Missing document request SOP
5. Quote and invoice communication SOP
6. Tax organizer completion trigger SOP
7. Tax software data entry SOP
8. Kross queue status update SOP
9. Preparer review handoff SOP
10. Santa Barbara TPG payroll report SOP
11. Refund Advantage payroll report SOP
12. PTIN-to-preparer payroll mapping SOP
13. Escalation and approval SOP
14. Firm onboarding memory SOP

## Open Questions

These need to be answered as we turn the blueprint into buildable SOPs.

1. What is the exact tax prep software Kross Agent should learn first?
2. Does each firm use the same tax software, or can it vary by firm?
3. What fields are already stored in the client portal after organizer completion?
4. Is there an API for the tax prep software, or will Kross use browser/computer control?
5. Where should transcripts be uploaded from: Fathom/Fireflies webhook, manual upload, email parser, or GHL note?
6. Where exactly in the portal should transcript summaries live?
7. Should Kross send messages automatically from templates, or draft first for approval in MVP?
8. What are the standard missing-document message templates?
9. What are the standard quote/invoice message templates?
10. Which payroll platform should be supported first: Santa Barbara TPG or Refund Advantage?
11. How are commission splits/pay-per-return rules currently stored?
12. Should client-facing Kross be branded as Kross, or should it speak invisibly as the tax office?

## Build Sequence

Recommended order:

1. Define Kross Agent role and approval boundaries.
2. Build the SOP index.
3. Build the meeting intelligence workflow first.
4. Build the GHL communication workflow second.
5. Build the Kross queue / data-entry handoff workflow third.
6. Build supervised tax software data entry fourth.
7. Build payroll report workflow fifth.
8. Package the finished instructions into a reusable Kross Agent snapshot/repository.
9. Only after that, connect Kross Agent to the server/VM infrastructure.

## Current Strategic Decision

Start with Kross Agent before server infrastructure.

Reason:
- The server is where the agent will live, but the agent's value comes from its SOPs, memory structure, approval rules, and tax-office workflows. Building the Kross Agent blueprint first makes the later VM/server setup much clearer.
