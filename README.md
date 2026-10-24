# Forge owner test

Throwaway repository for a hands-on Harness Forge test on 2026-10-24.

## Outside controls

- `codeowners-agent-config` (part A): recommended, not verified. Precaution; availability available. It works as a gate only when:
  - Workflow, scanner and policy files that define a gate are under code owners or come from outside the repository at a pinned ref, and where CODEOWNERS is used, CODEOWNERS owns itself (`outside.ci.workflow-protected`)
  - A CODEOWNERS entry names an owner for every file that configures the agent, including `.agents/`, `.claude/`, `CLAUDE.md`, `.mcp.json`, `.codex/`, `AGENTS.md`, `AGENTS.override.md`, `.devcontainer/`, the CI workflow files and the CODEOWNERS file itself, and the branch rule requires code-owner review (`outside.codeowners.agent-config`)
  - No broader credential or channel the agent can reach, such as a personal token or a metadata endpoint, bypasses the control (`outside.gate.no-broader-bypass`)
  - The control is enforced on the user's plan and repository visibility, or the recommendation says it is not (`outside.gate.plan-enforced`)
  - The agent's identity, including the bot, app, token and the human whose token it uses, is on no bypass or override list of the control (`outside.merge.no-agent-bypass`)
  - Where the control requires approval, approval comes from an identity other than the author, the last pusher and the launching user, and it resets on new pushes (`outside.merge.requester-cannot-approve`)
  - It targets the real refs and resources it protects, such as the default and release branches and tags or the production accounts (`outside.gate.real-refs`)
  - Its configuration is checked periodically, because gate configuration drifts silently (`outside.gate.periodic-verification`)
- `outer-isolation` (part A): recommended, not verified. Precaution; availability available. It works as a gate only when:
  - No broader credential or channel the agent can reach, such as a personal token or a metadata endpoint, bypasses the control (`outside.gate.no-broader-bypass`)
  - The agent's identity, including the bot, app, token and the human whose token it uses, is on no bypass or override list of the control (`outside.merge.no-agent-bypass`)
  - It targets the real refs and resources it protects, such as the default and release branches and tags or the production accounts (`outside.gate.real-refs`)
  - Its configuration is checked periodically, because gate configuration drifts silently (`outside.gate.periodic-verification`)

## Where the skills load

Forge builds `prompt-me` into this repository (`.agents/skills/<name>/`), and a skill there loads only in this repository, although the idea's reach is public. This release packages no plugin: publish this repository, and each user copies each skill's folder to their user skills location: `~/.claude/skills/<name>/` for Claude Code and `~/.agents/skills/<name>/` for Codex. Forge verifies the skills in this repository, not a copy.
