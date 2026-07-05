# SOP 15: Dedicated Kross Agent Portal API Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms
Status: Planned enhancement

## Purpose

Define the future dedicated Kross Agent access model for the Tax Mogul Client Portal / Preparer Workspace.

This lets Kross Agent operate from its VM or backend process without relying only on a human-style browser session, while still keeping access firm-scoped, client-scoped, permissioned, and audited.

## Core Rule

Kross Agent must never receive or expose the raw Supabase service role key.

If Kross needs machine-to-machine portal access, the portal must provide a dedicated Kross Agent API layer that validates a scoped agent token and then performs only approved server-side actions.

## Current MVP Path

Until this dedicated API layer is built, Kross Agent should access the portal as a firm-scoped staff user:

- Agent email created through agentmail.to
- Firm workspace invite
- Staff role assigned by human admin
- Existing authenticated portal session and server routes

## Future Access Model

Build a dedicated Kross Agent access layer with:

- Dedicated `kross_agent` or `agent` role
- Firm-scoped agent identity
- Hashed API token storage
- Action-level scopes
- Expiration/revocation
- Audit logs for every agent action
- Client-specific scope checks
- No cross-firm access
- No raw service role exposure

## Suggested Database Additions

### agent_api_keys

Suggested fields:

- id
- firm_id
- agent_name
- token_hash
- token_prefix
- status: active, revoked, expired
- scopes
- allowed_client_ids, nullable
- created_by
- revoked_by
- expires_at
- last_used_at
- last_used_ip
- created_at
- updated_at

### agent_action_logs

If existing `agent_actions` and `audit_logs` are not enough, add a dedicated action log.

Suggested fields:

- id
- firm_id
- client_id, nullable
- agent_api_key_id
- action
- resource_type
- resource_id
- request_metadata
- result_status
- created_at

## Suggested Agent Scopes

Possible scopes:

- `firm_knowledge:read`
- `client_memory:read`
- `client_memory:draft`
- `client_memory:update_approved`
- `client_calls:create`
- `client_calls:summarize`
- `client_tasks:create`
- `client_missing_documents:create`
- `kross_queue:read`
- `kross_queue:update`
- `documents:read_metadata`
- `documents:create_signed_url`
- `payroll_reports:upload`
- `ai_retrieval:run`

Do not create broad wildcard scopes for MVP.

## Required Server Behavior

Every Kross Agent API route must:

1. Validate the agent API token.
2. Confirm token status is active.
3. Confirm token has required scope.
4. Confirm firm_id scope.
5. Confirm client_id scope when applicable.
6. Perform the action server-side.
7. Write an audit log.
8. Return only the minimum necessary data.

## Approved API Route Examples

Possible future routes:

- `POST /api/agent/client-memory/:clientId/retrieve`
- `POST /api/agent/client-memory/:clientId/draft-update`
- `POST /api/agent/client-calls/:clientId/import-transcript`
- `POST /api/agent/client-calls/:clientId/draft-summary`
- `POST /api/agent/tasks/:clientId`
- `POST /api/agent/missing-documents/:clientId`
- `PATCH /api/agent/kross-queue/:clientId/status`
- `POST /api/agent/payroll-reports/upload`

## Forbidden API Access

Kross Agent API must not allow:

- Raw database access from the VM.
- Supabase service role key exposure.
- Unfiltered vector search.
- Cross-firm retrieval.
- Cross-client retrieval unless explicitly scoped and approved.
- Deleting clients.
- Deleting documents.
- Changing firm users or permissions.
- Changing billing.
- Changing platform/global settings.
- Filing or transmitting returns.

## Human Approval Requirements

The API layer must preserve approval rules.

Kross may create drafts for:

- Client memory updates
- Client-facing messages
- Call summaries
- Missing document requests
- Tasks

Official memory updates, sensitive client-facing messages, and tax workflow status changes must require human approval unless an approved automation rule exists.

## Acceptance Criteria

This enhancement is complete when:

- Kross has a dedicated agent identity separate from human staff users.
- API tokens are hashed and revocable.
- Tokens are scoped by firm and action.
- Client actions require client_id scope checks.
- All agent API calls are audited.
- Kross can retrieve/update only approved firm/client context.
- Kross cannot access another firm or unauthorized client.
- The Supabase service role key is never exposed to Kross.

