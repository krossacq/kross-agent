# SOP 12: Tax Mogul Client Portal / Preparer Workspace Access

Version: 0.1
Owner: Tax Mogul Bureau
Applies to: Kross Agent for Firms

## Purpose

Define how Kross Agent accesses the firm's Tax Mogul Client Portal / Preparer Workspace.

## Current Access Decision

Kross Agent can only access the specific Tax Mogul Portal workspace for the assigned firm.

Code inspection shows the portal is built on:

- Supabase Auth
- Supabase/Postgres
- Row Level Security
- server-side API routes
- server-only Supabase service role usage
- staff membership checks through `organization_members`
- audit logs
- existing memory/knowledge API routes

The portal already has a strong backend foundation for Kross Agent access, but it does not yet appear to have a dedicated Kross Agent API-key authentication model.

## Current Supported Access Path

The current practical access path is:

- Create Kross Agent as a firm-scoped staff user through the normal team/member invite flow.
- Use the Kross Agent email created through agentmail.to.
- Assign Kross Agent a staff role inside that firm's workspace.
- Let Kross operate through authenticated portal sessions and existing server routes.

Current staff roles are:

- admin
- manager
- preparer
- client

There is no confirmed dedicated `agent` role yet.

## Recommended Role For MVP

Recommended MVP role:

- `manager`, if Kross needs broad firm operational access across clients, knowledge, queue, and payroll support.

Alternative:

- `preparer`, if Kross should only access assigned clients.

Long-term recommendation:

- Add a dedicated `agent` or `kross_agent` role with purpose-built permissions instead of reusing human staff roles.
- Add dedicated scoped API-key access for Kross Agent if Kross needs to operate from its VM without a browser session. See `SOP_15_Dedicated_Kross_Agent_Portal_API_Access.md`.

## API / Service Access Status

Existing API routes already support:

- firm knowledge
- global knowledge
- client memory
- call summaries
- AI retrieval
- audit logging

However, these routes currently appear to assume a logged-in staff user session through `requireStaffUser()`.

That means:

- Kross can likely use the portal as an authenticated staff user.
- Kross should not be given the raw Supabase service role key.
- A dedicated machine-to-machine Kross API key flow still needs to be designed and built if Kross will operate from an external VM without a browser session.

## Future Agent API Recommendation

If Kross Agent needs direct backend access from its VM, build a dedicated server-side agent access layer with:

- `agent_api_keys` or equivalent table.
- hashed token storage.
- firm_id scope.
- allowed action scopes.
- expiration/revocation.
- IP/device metadata where useful.
- audit logs for every agent action.
- no browser-exposed service role key.

This agent API should call server-side functions/routes that enforce firm/client scope before using the Supabase service role internally.

## Kross May Access

When authorized and scoped correctly, Kross may:

- Read client organizer answers.
- Read uploaded documents.
- Read selected client memory.
- Add approved summaries.
- Draft memory updates.
- Update Kross queue status.
- Create tasks/document requests when approved.
- Upload payroll report files if configured.

## Kross Must Not Access

Kross must not:

- Access another firm's portal.
- Access another client's profile unless explicitly selected and authorized.
- Delete clients.
- Delete documents.
- Change firm settings.
- Change team permissions.
- Expose internal notes to clients.

## Acceptance Criteria

This SOP is working when:

- Kross portal access is firm-scoped.
- Kross can operate through a firm-scoped authenticated staff account for MVP.
- A dedicated Kross Agent API-key flow is not assumed until it is built.
- Kross actions are audited.
- Kross cannot access another firm or unauthorized client.
