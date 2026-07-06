# Local Mac Pilot: Returns and Revenues Office

This file explains how to run the Kross Agent snapshot locally on Sydne's Mac before moving it to a server/Ubuntu VM.

## Local Profile

Hermes profile name:

`krossagent`

Profile path:

`/Users/sydnejones/.hermes/profiles/krossagent`

Wrapper command:

`krossagent`

## Workspace

Local workspace:

`/Users/sydnejones/.hermes/profiles/krossagent/workspace`

Workspace instruction file:

`/Users/sydnejones/.hermes/profiles/krossagent/workspace/AGENTS.md`

## Start Kross Agent Locally

From Terminal:

```bash
cd "/Users/sydnejones/.hermes/profiles/krossagent/workspace"
krossagent chat
```

Or:

```bash
cd "/Users/sydnejones/.hermes/profiles/krossagent/workspace"
krossagent --tui
```

## Quick Test Prompt

After Kross starts, ask:

```text
Who are you, what firm are you serving, and what are your operating boundaries?
```

Expected answer:

- Kross should identify as Kross Agent.
- Kross should say it is serving Returns and Revenues Office.
- Kross should say it is not Kross Command.
- Kross should mention approval, client data separation, and no final tax filing/transmission.

## Snapshot Source

Kross should use the snapshot SOPs at:

`/Users/sydnejones/Documents/The Tax Mogul Bureau/Kross GitHub Repos/kross-agent/docs/kross-agent-snapshot/sops`

## Important

This local Mac pilot is for testing the agent brain and SOP-following behavior.

It is not the final server-hosted VM deployment.

Do not connect live credentials or run live client workflows until the testing scenarios in `SOP_59_Kross_Agent_Testing_Scenarios.md` pass.
