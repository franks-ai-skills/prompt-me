# Forge owner test

Throwaway repository for a hands-on Harness Forge test on 2026-10-24.

## Outside controls

Outside controls are settings the repository owner or operator configures outside the skills' instructions, for example on the Git host or in CI. [Harness Forge](https://github.com/franks-ai-skills/harness-forge) recommends them from the intake answers; it does not set them up or check them. Background: [Outside gates](https://github.com/franks-ai-skills/agent-harness-kb/blob/v0.6.0/docs/guide/outside-gates.md).

- **Code-owner review of agent configuration** (`codeowners-agent-config`): recommended, not verified. Not recorded as required for the goal. Recorded as available during intake; Harness Forge has not verified its setup or enforcement. Why: The agent's own configuration files decide what it may do, so a change to them, also one made through a pull request, takes effect only after a code owner approves it. It works as a gate only when:
  - Workflow, scanner and policy files that define a gate are under code owners or come from outside the repository at a pinned ref, and where CODEOWNERS is used, CODEOWNERS owns itself (`outside.ci.workflow-protected`)
  - A CODEOWNERS entry names an owner for every file that configures the agent, including `.agents/`, `.claude/`, `CLAUDE.md`, `.mcp.json`, `.codex/`, `AGENTS.md`, `AGENTS.override.md`, `.devcontainer/`, the CI workflow files and the CODEOWNERS file itself, and the branch rule requires code-owner review (`outside.codeowners.agent-config`)
  - No broader credential or channel the agent can reach, such as a personal token or a metadata endpoint, bypasses the control (`outside.gate.no-broader-bypass`)
  - The control is enforced on the user's plan and repository visibility, or the recommendation says it is not (`outside.gate.plan-enforced`)
  - The agent's identity, including the bot, app, token and the human whose token it uses, is on no bypass or override list of the control (`outside.merge.no-agent-bypass`)
  - Where the control requires approval, approval comes from an identity other than the author, the last pusher and the launching user, and it resets on new pushes (`outside.merge.requester-cannot-approve`)
  - It targets the real refs and resources it protects, such as the default and release branches and tags or the production accounts (`outside.gate.real-refs`)
  - Its configuration is checked periodically, because gate configuration drifts silently (`outside.gate.periodic-verification`)
- **Isolation around the agent** (`outer-isolation`): recommended, not verified. Not recorded as required for the goal. Recorded as available during intake; Harness Forge has not verified its setup or enforcement. Why: A bypass or no-prompt mode, an untrusted repository, or untrusted input combined with secrets and outbound access needs a boundary outside the harness. It works as a gate only when:
  - No broader credential or channel the agent can reach, such as a personal token or a metadata endpoint, bypasses the control (`outside.gate.no-broader-bypass`)
  - The agent's identity, including the bot, app, token and the human whose token it uses, is on no bypass or override list of the control (`outside.merge.no-agent-bypass`)
  - It targets the real refs and resources it protects, such as the default and release branches and tags or the production accounts (`outside.gate.real-refs`)
  - Its configuration is checked periodically, because gate configuration drifts silently (`outside.gate.periodic-verification`)

## Where the skills load

[Harness Forge](https://github.com/franks-ai-skills/harness-forge) builds `prompt-me` into this repository (`.agents/skills/<name>/`), and a skill there loads only in this repository, although you plan to share them publicly. This release packages no plugin: publish this repository, and each user copies each skill's folder to their user skills location: `~/.claude/skills/<name>/` for Claude Code and `~/.agents/skills/<name>/` for Codex. Harness Forge verifies the skills in this repository, not a copy.

## License

Except where separate terms are stated, this repository is licensed under the GNU Affero General Public License v3.0 only ([AGPL-3.0-only](LICENSE)). Third-party material retains its applicable terms.
