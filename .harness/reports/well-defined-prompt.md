# Verification report

- Run: `20261027T051310Z-7d1c50be`
- Harness KB version: 0.6.0
- [Harness Forge](https://github.com/franks-ai-skills/harness-forge) verifier: 0.4.0 (source unknown)
- Confirmed configuration digest: d00eeb5e6a1edbb730f3c51db4f2823a4e4748107e673eafc3048c1f5e689b01
- Confirmed parts: A
- Decision record digest: 090b08465ad8dac568bc77e5ca1ec547996454eec44618bf66b97af3db760bc6
- Whole-idea answers and targets: `{"facts": {"bypass_mode": true, "lethal_trifecta": true, "opens_prs": false, "plan_controls": "available", "reach": "public", "target_set": "both", "untrusted_repo": true}, "hosting": {"plan": "free", "platform": "github", "visibility": "public"}, "reach": "public", "targets": ["claude-code", "codex"]}` (digest d050a5bb011e4c946b7b15da35a8c18b60decc2df4dde9debbaa44247b4f5d90)
- Rule content digest: 5434c2fa865952f2d074f180ba164f66ae93214c9c0ed39575b50ba90c124def
- Accepted Idea KB revision: a9d1a41ce855fec682d5d975c28a3a379bd13a4b61c47d4590c778c3e85eea39
- Review scope: Review (recommended): judged A
- Rule overrides: none
- Checker versions digest: 1070f5e9c077925074cc173f075f918ce98998206fdaa029b5527b17b3f3d326

## Worker isolation

Workers ran under `best-effort-v1` with isolation status `not-certified`. Research, source-support and review workers run as independent CLI processes with explicit role inputs and the available restrictions. Complete tool absence and context, file and network isolation are not guaranteed; use trusted projects and operator-approved inputs.

- research worker: claude-code 2.1.311 (Claude Code), model account default, launcher independent-process, configuration ee513860b21a159a1c3b248985d44917ab66d000740c58dab4c94c971fcc9345, controls: command: ["claude", "--print", "--output-format", "stream-json", "--verbose", "--no-session-persistence", "--safe-mode", "--restricted", "--setting-sources", "", "--strict-mcp-config", "--mcp-config", "{\"mcpServers\":{}}", "--disable-slash-commands", "--permission-mode", "dontAsk", "--permission-prompts", "none", "--settings", "{\"disableAllHooks\":true,\"autoMemoryEnabled\":false}", "--tools", "WebFetch,WebSearch", "--allowedTools", "WebFetch,WebSearch", "--json-schema", "{\"type\":\"object\",\"properties\":{\"findings\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"claim\":{\"type\":\"string\"},\"source\":{\"type\":\"string\"},\"fetched\":{\"type\":\"string\"},\"quote\":{\"type\":\"string\"},\"context\":{\"type\":\"string\"},\"source_role\":{\"enum\":[\"primary\",\"practitioner\",\"trade-press\"]},\"requirement_id\":{\"type\":[\"string\",\"null\"]}},\"required\":[\"claim\",\"source\",\"fetched\",\"quote\",\"context\",\"source_role\",\"requirement_id\"],\"additionalProperties\":false}}},\"required\":[\"findings\"],\"additionalProperties\":false}"]; environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER; login: subscription (claude.ai), observed tools: unknown, unknowns: context, file and network isolation are not certified; not every tool-registration path is observable
- source-support worker: claude-code 2.1.311 (Claude Code), model account default, launcher independent-process, configuration f79908e2f8761717b26bb5d87aed5c56e135ba70a0edb97e404129d59e06e708, controls: command: ["claude", "--print", "--output-format", "stream-json", "--verbose", "--no-session-persistence", "--safe-mode", "--restricted", "--setting-sources", "", "--strict-mcp-config", "--mcp-config", "{\"mcpServers\":{}}", "--disable-slash-commands", "--permission-mode", "dontAsk", "--permission-prompts", "none", "--settings", "{\"disableAllHooks\":true,\"autoMemoryEnabled\":false}", "--tools", "", "--allowedTools", "", "--json-schema", "{\"type\":\"object\",\"properties\":{\"verdicts\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"finding_id\":{\"type\":\"string\"},\"verdict\":{\"enum\":[\"supported\",\"unsupported\"]},\"reasoning\":{\"type\":\"string\"}},\"required\":[\"finding_id\",\"verdict\",\"reasoning\"],\"additionalProperties\":false}}},\"required\":[\"verdicts\"],\"additionalProperties\":false}"]; environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER; login: subscription (claude.ai), observed tools: unknown, unknowns: context, file and network isolation are not certified; not every tool-registration path is observable
- review worker: claude-code 2.1.311 (Claude Code), model account default, launcher independent-process, configuration bd41806234b54333f0b42bf98e08945ea9756a175b212e92e0435a771b2beb3f, controls: command: ["claude", "--print", "--output-format", "stream-json", "--verbose", "--no-session-persistence", "--safe-mode", "--restricted", "--setting-sources", "", "--strict-mcp-config", "--mcp-config", "{\"mcpServers\":{}}", "--disable-slash-commands", "--permission-mode", "dontAsk", "--permission-prompts", "none", "--settings", "{\"disableAllHooks\":true,\"autoMemoryEnabled\":false}", "--tools", "Read,Grep,Glob", "--allowedTools", "Read,Grep,Glob", "--json-schema", "{\"type\":\"object\",\"properties\":{\"run_id\":{\"type\":\"string\"},\"verdicts\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"part_id\":{\"type\":\"string\"},\"rule_id\":{\"type\":\"string\"},\"verdict\":{\"enum\":[\"pass\",\"fail\",\"not-applicable\"]},\"reason\":{\"type\":\"string\"},\"citation\":{\"type\":\"string\"}},\"required\":[\"part_id\",\"rule_id\",\"verdict\",\"reason\",\"citation\"],\"additionalProperties\":false}},\"goal_verdicts\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"part_id\":{\"type\":\"string\"},\"verdict\":{\"enum\":[\"met\",\"not-met\"]},\"reason\":{\"type\":\"string\"}},\"required\":[\"part_id\",\"verdict\",\"reason\"],\"additionalProperties\":false}}},\"required\":[\"run_id\",\"verdicts\",\"goal_verdicts\"],\"additionalProperties\":false}"]; environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER; login: subscription (claude.ai), observed tools: unknown, unknowns: context, file and network isolation are not certified; not every tool-registration path is observable
- review worker: claude-code 2.1.311 (Claude Code), model account default, launcher independent-process, configuration bd41806234b54333f0b42bf98e08945ea9756a175b212e92e0435a771b2beb3f, controls: command: ["claude", "--print", "--output-format", "stream-json", "--verbose", "--no-session-persistence", "--safe-mode", "--restricted", "--setting-sources", "", "--strict-mcp-config", "--mcp-config", "{\"mcpServers\":{}}", "--disable-slash-commands", "--permission-mode", "dontAsk", "--permission-prompts", "none", "--settings", "{\"disableAllHooks\":true,\"autoMemoryEnabled\":false}", "--tools", "Read,Grep,Glob", "--allowedTools", "Read,Grep,Glob", "--json-schema", "{\"type\":\"object\",\"properties\":{\"run_id\":{\"type\":\"string\"},\"verdicts\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"part_id\":{\"type\":\"string\"},\"rule_id\":{\"type\":\"string\"},\"verdict\":{\"enum\":[\"pass\",\"fail\",\"not-applicable\"]},\"reason\":{\"type\":\"string\"},\"citation\":{\"type\":\"string\"}},\"required\":[\"part_id\",\"rule_id\",\"verdict\",\"reason\",\"citation\"],\"additionalProperties\":false}},\"goal_verdicts\":{\"type\":\"array\",\"items\":{\"type\":\"object\",\"properties\":{\"part_id\":{\"type\":\"string\"},\"verdict\":{\"enum\":[\"met\",\"not-met\"]},\"reason\":{\"type\":\"string\"}},\"required\":[\"part_id\",\"verdict\",\"reason\"],\"additionalProperties\":false}}},\"required\":[\"run_id\",\"verdicts\",\"goal_verdicts\"],\"additionalProperties\":false}"]; environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER; login: subscription (claude.ai), observed tools: Glob, Grep, Read, StructuredOutput, unknowns: context, file and network isolation are not certified; not every tool-registration path is observable

## Part A

- Harness result: verified
- Goal result: met by the verified build
- Status: verified
- Outside dependencies: none
- Recorded builder: Harness Forge 0.4.0 (source unknown)
- Built outputs: match that build
- Confirmed answers: `{"event_without_agent": false, "every_time": "usually", "irreversible": false, "job": "procedure", "must_survive_compromise": "not-required", "own_context": false, "side_effects": false, "trigger": "user", "who_disables": "contributor"}`
- Goal verdict: met (The files achieve the goal. The skill is user-invoked in both harnesses. It gathers read-only context with an allowlist that applies until approval. It drafts the fixed section layout with untrusted material fenced and labelled, and limits Context to escaped repository data, with commit subjects only under 'git log'. Before any write it runs preflight checks for links and containment, treats missing paths as expected, stops without writing on failure and does not claim race-free writes. It creates .tmp/.gitignore with '*' only when it is missing and saves .tmp/prompt-me-<suffix>.md. It replies with only the path, a one-line intent and the two ways to continue, then stops. All eight accepted requirements are satisfied. The README reports the outside controls as recommended and not verified.)

| Rule | Severity | Check | Result | Reason | Citation | Sources |
| --- | --- | --- | --- | --- | --- | --- |
| `idea.well-defined-prompt.a.git-no-optional-locks` | warning | judged | pass | Every git command listed or used carries --no-optional-locks. | .agents/skills/prompt-me/SKILL.md:13,27,57 | https://git-scm.com/docs/git |
| `idea.well-defined-prompt.a.issues-untrusted-any-owner` | error | judged | pass | Issue and PR titles, bodies and comments are treated as untrusted, 'also when the repository belongs to the user or their organization'. | .agents/skills/prompt-me/SKILL.md:14,38 | https://invariantlabs.ai/blog/mcp-github-vulnerability |
| `idea.well-defined-prompt.a.no-fetched-instructions` | error | judged | pass | Embedded instructions are not acted on or moved into the Task; they are recorded as 'found in source, not adopted'. The Task is derived only from the user's own request. | .agents/skills/prompt-me/SKILL.md:11,38,62 | https://invariantlabs.ai/blog/mcp-github-vulnerability, https://genai.owasp.org/llmrisk/llm01-prompt-injection/ |
| `idea.well-defined-prompt.a.read-only-allowlist` | error | judged | pass | Step 2 lists the allowed read-only actions: file listing and reading, specific git, uname, pwd and ls commands, gh/glab views and user-given URLs. It applies 'until the user approves the draft'. The only writes allowed are .tmp/, a missing .tmp/.gitignore and the prompt file, each after the checks pass. Every command used in later steps is on the list. | .agents/skills/prompt-me/SKILL.md:12,25-32 | https://genai.owasp.org/llmrisk/llm01-prompt-injection/ |
| `idea.well-defined-prompt.a.tmp-gitignore` | error | judged | pass | Step 9 creates .tmp/.gitignore with exactly '*' only when it is missing, leaves an existing one unchanged and never modifies the repository's .gitignore. | .agents/skills/prompt-me/SKILL.md:15,55 | https://git-scm.com/docs/gitignore |
| `idea.well-defined-prompt.a.tracked-drafts-note` | warning | judged | pass | Step 4 runs git ls-files .tmp read-only. Step 10 adds a note to Assumptions & open questions that the .tmp/.gitignore rule does not untrack those files. | .agents/skills/prompt-me/SKILL.md:36,65 | https://git-scm.com/docs/gitignore |
| `idea.well-defined-prompt.a.untrusted-block` | error | judged | pass | Step 10 makes '## Untrusted reference material' the single place for content from issues, PRs, URLs, documents, repository files and commit subjects, with each item labelled by source and fenced. Context is limited to branch names, credential-free remotes, commit hashes and paths, introduced as repository-controlled names and written as code spans sized against backtick runs, with line breaks written as \n. Step 4 keeps commit subjects out of Context, and step 6 quotes file content only in the untrusted section. | .agents/skills/prompt-me/SKILL.md:10,36,40,61,66 | https://genai.owasp.org/llmrisk/llm01-prompt-injection/, https://arxiv.org/abs/2403.14720, https://spec.commonmark.org/0.31.2/ |
| `idea.well-defined-prompt.a.write-preflight` | error | judged | pass | Before any write, the skill runs pwd -P and ls -ld on all three paths. Missing paths are treated as expected. It stops on any link, including dangling ones, on a wrong type, an existing draft, or a check that fails or is unclear, and reports that nothing was written. It says the checks do not detect changes made between the check and the write. | .agents/skills/prompt-me/SKILL.md:17,46-53 | https://cwe.mitre.org/data/definitions/59.html, https://cwe.mitre.org/data/definitions/367.html |
| `outside.ci.workflow-protected` | warning | judged | pass | The README states this condition for codeowners-agent-config, the only control that lists it. | README.md:17 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate |
| `outside.codeowners.agent-config` | warning | judged | pass | The README recommends a CODEOWNERS entry covering .agents/, .claude/, .codex/, AGENTS.md, CODEOWNERS and the other agent configuration files, together with a branch rule that requires code-owner review. | README.md:18 | docs/guide/outside-gates.md#branch-protection-and-merge-rules-the-gate-is-separation-of-identities, https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners |
| `outside.gate.no-broader-bypass` | warning | judged | pass | The README states this condition for both controls. | README.md:19,26 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate |
| `outside.gate.periodic-verification` | warning | judged | pass | The README states periodic verification for both controls. | README.md:24,29 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate |
| `outside.gate.plan-enforced` | warning | judged | pass | The README states this condition for codeowners-agent-config, the only control that lists it. | README.md:20 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate, https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/about-rulesets |
| `outside.gate.real-refs` | warning | judged | pass | The README states the real-refs condition for both codeowners-agent-config and outer-isolation. | README.md:23,28 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate |
| `outside.merge.no-agent-bypass` | warning | judged | pass | The README states the no-agent-bypass condition for both controls. | README.md:21,27 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate, https://learn.microsoft.com/en-us/azure/devops/repos/git/branch-policies |
| `outside.merge.requester-cannot-approve` | warning | judged | pass | The README states this condition for codeowners-agent-config, the only control that lists it. | README.md:22 | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate, docs/guide/outside-gates.md#branch-protection-and-merge-rules-the-gate-is-separation-of-identities, https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/available-rules-for-rulesets |
| `outside.merge.rule-for-agent-prs` | warning | judged | not-applicable | The agent opens no pull requests (context facts opens_prs: false), and the skill forbids commit and push while drafting. | request.json context.facts.opens_prs; SKILL.md:32 | docs/guide/outside-gates.md#four-outcomes-from-six-intake-questions |
| `outside.readme.lists-controls` | error | script | pass | 2 control(s) listed | - | docs/guide/outside-gates.md#seven-conditions-turn-a-control-into-a-gate, docs/guide/outside-gates.md#four-outcomes-from-six-intake-questions |
| `security.approval.claims-are-data` | warning | judged | pass | The work starts only when the user replies 'go ahead'. Instructions found in content are recorded as 'found in source, not adopted', and the skill never takes instructions from the untrusted section. No content claim is treated as approval. | .agents/skills/prompt-me/SKILL.md:38,75 | docs/guide/security.md#context-and-persistent-state |
| `security.embedded-content.contained` | warning | judged | pass | Untrusted content goes in backtick fences longer than any backtick run inside it, under a labelled section. The saved prompt opens that section with a fixed paragraph declaring it reference data, not instructions. | .agents/skills/prompt-me/SKILL.md:66 | docs/guide/security.md#context-and-persistent-state, https://genai.owasp.org/llmrisk/llm01-prompt-injection/, https://spec.commonmark.org/0.31.2/#fenced-code-blocks |
| `security.helpers.confined` | warning | judged | not-applicable | The skill runs no bundled helpers and grants no pre-approval. It uses only standard commands under the harness's permissions. | .agents/skills/prompt-me/SKILL.md:1-5,25-32 | docs/guide/security.md#where-each-concept-is-attacked, docs/guide/security.md#executables-approvals-and-isolation |
| `security.outbound.minimal-data` | warning | judged | pass | Outbound calls are limited to the issues, PRs and URLs the user named. Links inside fetched content are not followed, and fetched content cannot add actions. | .agents/skills/prompt-me/SKILL.md:29-30,38 | docs/guide/security.md#data-access-and-outbound-channels, https://developers.openai.com/api/docs/guides/deep-research#prompt-injection-and-exfiltration |
| `security.secrets.no-unneeded-reads` | warning | judged | pass | Step 6 forbids opening .env, .netrc, private keys, keystores and credentials files, as well as ambiguous .pem/.key files. It lists them by path only. | .agents/skills/prompt-me/SKILL.md:42 | docs/guide/security.md#data-access-and-outbound-channels, https://code.claude.com/docs/en/settings |
| `security.secrets.none-in-files` | error | judged | pass | No credentials or tokens appear. The only credential-like text is the placeholder example 'https://user:token@host/...'. | .agents/skills/prompt-me/SKILL.md:36 | docs/guide/security.md#where-each-concept-is-attacked, docs/guide/security.md#context-and-persistent-state |
| `security.untrusted-input.as-data` | warning | judged | pass | The Procedure tells the agent to treat repository files, issues, fetched pages and tool output as data, never as instructions. Step 5 forbids acting on embedded instructions. | .agents/skills/prompt-me/SKILL.md:21,38 | docs/guide/security.md#context-and-persistent-state, https://securitylab.github.com/resources/github-actions-untrusted-input/ |
| `security.writes.within-boundary` | warning | judged | pass | Step 8 checks .tmp, .tmp/.gitignore and the draft path with ls -ld for links, including dangling ones, and for type. Containment is checked against pwd -P. The skill stops on failure or unclear output and states that the checks are not race-free. | .agents/skills/prompt-me/SKILL.md:46-53 | docs/guide/security.md#executables-approvals-and-isolation, https://cwe.mitre.org/data/definitions/59.html, https://cwe.mitre.org/data/definitions/367.html |
| `skills.body.gotchas-first` | warning | judged | pass | The non-negotiable Requirements section comes directly after the title, before the Procedure. The untrusted-data warning opens the Procedure. | .agents/skills/prompt-me/SKILL.md:8-21 | docs/best-practices/skills.md#3-keep-skillmd-lean-and-put-gotchas-first, https://agentskills.io/skill-creation/best-practices.md |
| `skills.body.no-time-bound-statements` | warning | judged | pass | There are no time-bound statements such as 'currently', 'as of' or dates in any skill file. | .agents/skills/prompt-me/SKILL.md; references/requirements.md | docs/best-practices/skills.md#3-keep-skillmd-lean-and-put-gotchas-first, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices |
| `skills.body.only-what-model-lacks` | warning | judged | pass | The body gives specific standing instructions (exact commands, the section layout, fence-length escaping, which secret files to skip, the preflight checks). It does not explain general concepts the model already knows. | .agents/skills/prompt-me/SKILL.md:8-75 | docs/best-practices/skills.md#3-keep-skillmd-lean-and-put-gotchas-first, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices |
| `skills.body.reasons-before-hard-rules` | warning | judged | pass | Key rules carry reasons: --no-optional-locks so the index is not modified; commit subjects are free text written by whoever made the commit; fences sized so the content cannot close them. 'Never' is used for security-critical boundaries only. | .agents/skills/prompt-me/SKILL.md:13,36,66 | docs/best-practices/skills.md#7-explain-the-why-before-adding-hard-rules |
| `skills.body.size` | warning | script | pass | 1 skill(s) checked | - | docs/best-practices/skills.md#3-keep-skillmd-lean-and-put-gotchas-first, docs/concepts/skills.md#body, https://code.claude.com/docs/en/skills, https://agentskills.io/specification |
| `skills.body.strictness-matches-fragility` | warning | judged | pass | Exact commands and checks are prescribed only for the fragile parts: preflight, escaping and the git lock flag. Other steps leave room for judgment, for example: 'Find the files… most likely touches'. There are no menus of options. | .agents/skills/prompt-me/SKILL.md:44-57 | docs/best-practices/skills.md#5-match-strictness-to-fragility, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices |
| `skills.description.boundary` | warning | judged | pass | The description says: 'Not for doing the task, editing code or answering the question directly.' | .agents/skills/prompt-me/SKILL.md:3 | docs/best-practices/skills.md#2-write-the-description-as-the-trigger-condition, https://agentskills.io/skill-creation/optimizing-descriptions.md |
| `skills.description.concise` | warning | script | pass | 1 skill(s) checked | - | docs/best-practices/skills.md#2-write-the-description-as-the-trigger-condition, docs/research-notes/agent-harness-best-practices/skills.md |
| `skills.description.length` | error | script | pass | 1 skill(s) checked | - | docs/concepts/skills.md#frontmatter, docs/vendors/codex/skills.md#skillmd-frontmatter-that-codex-reads, docs/vendors/opencode/skills.md#format, https://github.com/openai/codex/blob/main/codex-rs/ext/skills/src/loader/mod.rs, https://opencode.ai/docs/skills/ |
| `skills.description.no-workflow-steps` | warning | judged | pass | The description summarizes the inputs, the output file and the fact that it stops for review. It does not list the procedure's steps, such as the preflight checks, the gitignore handling, the section layout or the reply format. | .agents/skills/prompt-me/SKILL.md:3 | docs/best-practices/skills.md#2-write-the-description-as-the-trigger-condition, https://raw.githubusercontent.com/obra/superpowers/main/skills/writing-skills/SKILL.md |
| `skills.description.voice` | warning | judged | pass | The description is in the third person ('Drafts…', 'gathers…'), not 'I can' or 'You can'. | .agents/skills/prompt-me/SKILL.md:3 | docs/best-practices/skills.md#2-write-the-description-as-the-trigger-condition |
| `skills.description.what-and-when` | warning | judged | pass | The description opens with what the skill does ('Drafts a well-defined prompt from the user's request instead of carrying it out'), names the context it gathers and the output file, then gives trigger phrases a user would say. | .agents/skills/prompt-me/SKILL.md:3 | docs/best-practices/skills.md#2-write-the-description-as-the-trigger-condition, https://learn.chatgpt.com/docs/build-skills, https://agentskills.io/skill-creation/optimizing-descriptions.md |
| `skills.frontmatter.valid` | error | script | pass | 1 skill(s) checked | - | docs/vendors/opencode/skills.md#format, docs/vendors/codex/skills.md#skillmd-frontmatter-that-codex-reads, docs/vendors/claude-code/skills.md#format, docs/concepts/skills.md#frontmatter, https://opencode.ai/docs/skills/, https://agentskills.io/specification |
| `skills.goal.no-must-hold-rule-in-skill` | error | judged | not-applicable | a condition in applies_to.when does not hold | - | docs/best-practices/skills.md#13-move-rules-that-must-hold-every-time-into-hooks, https://code.claude.com/docs/en/skills |
| `skills.inputs.from-message` | warning | judged | pass | Step 1 takes the request from the text the user wrote alongside the invocation, and asks for it in one line when it is missing. There is no argument substitution. | .agents/skills/prompt-me/SKILL.md:23 | docs/best-practices/skills.md#8-make-side-effecting-skills-user-invoked-in-both-leads, docs/concepts/skills.md#body |
| `skills.invocation.both-flags` | error | script | pass | 1 skill(s) checked | - | docs/concepts/skills.md#invocation-policy-in-both-leads, docs/best-practices/skills.md#8-make-side-effecting-skills-user-invoked-in-both-leads, https://code.claude.com/docs/en/skills, https://learn.chatgpt.com/docs/build-skills |
| `skills.invocation.side-effects-user-invoked` | error | judged | pass | The skill writes files under .tmp/ and is user-invoked in both targets: disable-model-invocation is true for Claude Code, and allow_implicit_invocation is false for Codex. | .agents/skills/prompt-me/SKILL.md:4; agents/openai.yaml:2 | docs/best-practices/skills.md#8-make-side-effecting-skills-user-invoked-in-both-leads, https://code.claude.com/docs/en/skills, https://learn.chatgpt.com/docs/build-skills |
| `skills.name.format` | error | script | pass | 1 skill(s) checked | - | docs/guide/skills.md#portability, docs/concepts/skills.md#frontmatter, docs/vendors/opencode/skills.md#format, https://opencode.ai/docs/skills/, https://agentskills.io/specification |
| `skills.package.no-auxiliary-docs` | warning | script | pass | 1 skill(s) checked | - | docs/best-practices/skills.md#anti-patterns, https://raw.githubusercontent.com/openai/skills/main/skills/.system/skill-creator/SKILL.md |
| `skills.portable.frontmatter` | warning | script | pass | 1 skill(s) checked | - | docs/concepts/skills.md#frontmatter, docs/best-practices/skills.md#12-keep-one-canonical-copy-with-portable-frontmatter, https://code.claude.com/docs/en/skills |
| `skills.portable.layout` | error | script | pass | 1 skill(s) linked | - | docs/concepts/skills.md#directory-layout, docs/guide/skills.md#portability, https://code.claude.com/docs/en/skills, https://learn.chatgpt.com/docs/build-skills |
| `skills.portable.no-claude-placeholders` | warning | script | pass | 1 skill(s) checked | - | docs/concepts/skills.md#body, docs/guide/skills.md#portability, https://code.claude.com/docs/en/skills |
| `skills.portable.plugin-layout` | error | script | not-applicable | a condition in applies_to.when does not hold | - | docs/concepts/skills.md#directory-layout, docs/vendors/claude-code/plugins.md#standard-layout, docs/vendors/codex/plugins.md#plugin-layout, https://code.claude.com/docs/en/plugins/manifest-reference, https://developers.openai.com/codex/plugins/build |
| `skills.references.load-conditions` | warning | judged | pass | The single reference file is named with its load condition: read it when you need the exact accepted wording, rule id or source. It holds provenance (rule ids, sources) that SKILL.md does not repeat. | .agents/skills/prompt-me/SKILL.md:77-79 | docs/best-practices/skills.md#4-disclose-detail-progressively-with-explicit-triggers, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices, https://agentskills.io/skill-creation/best-practices.md |
| `skills.references.one-level` | warning | script | pass | 1 skill(s) checked | - | docs/best-practices/skills.md#4-disclose-detail-progressively-with-explicit-triggers, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices, https://agentskills.io/specification |
| `skills.references.resolve` | error | script | pass | 1 skill(s) checked | - | docs/best-practices/skills.md#4-disclose-detail-progressively-with-explicit-triggers, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices |
| `skills.reuse.reviewed-and-pinned` | error | judged | not-applicable | a condition in applies_to.when does not hold | - | docs/best-practices/skills.md#security, https://owasp.github.io/www-project-agentic-skills-top-10/ast01 |
| `skills.scope.committed-for-automation` | warning | judged | not-applicable | This is a user-invoked drafting skill; CI or cloud runs do not need it. It is committed in project scope anyway (.agents/skills, with a .claude/skills link). | README.md:33; links .claude/skills/prompt-me | docs/concepts/skills.md#directory-layout, https://code.claude.com/docs/en/skills |
| `skills.scripts.agent-caller` | warning | judged | not-applicable | The skill bundles no scripts. Its only files are SKILL.md, agents/openai.yaml and a reference markdown file. | request.json inputs.files | docs/best-practices/skills.md#6-put-deterministic-logic-in-tested-scripts, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices, https://agentskills.io/skill-creation/using-scripts.md |
| `skills.security.allowed-tools-least-privilege` | warning | judged | not-applicable | The frontmatter has no allowed-tools field, so the skill pre-grants no tools. | .agents/skills/prompt-me/SKILL.md:1-5 | docs/best-practices/skills.md#security, docs/vendors/claude-code/skills.md#limits-and-gotchas, https://code.claude.com/docs/en/skills |
| `skills.security.no-surprising-content` | error | judged | pass | There are no hidden directives, remote fetch-and-run, encoded payloads or credential access. The skill explicitly avoids opening secret-bearing files. | .agents/skills/prompt-me/SKILL.md:42 | docs/best-practices/skills.md#security, https://raw.githubusercontent.com/anthropics/skills/main/skills/skill-creator/SKILL.md |

Contested `skills.body.reasons-before-hard-rules`:
- All-caps ALWAYS or NEVER is a yellow flag; explain the reasoning instead (https://raw.githubusercontent.com/anthropics/skills/main/skills/skill-creator/SKILL.md, https://agentskills.io/skill-creation/evaluating-skills.md)
- Discipline skills need firm prohibitions and rationalization tables (https://raw.githubusercontent.com/obra/superpowers/main/skills/writing-skills/SKILL.md, https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)

Contested `skills.description.voice`:
- Always write in the third person; an inconsistent point of view can cause discovery problems (https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- Use imperative "Use this skill when" phrasing for the trigger (https://agentskills.io/skill-creation/optimizing-descriptions.md, https://raw.githubusercontent.com/obra/superpowers/main/skills/writing-skills/SKILL.md)

## Runtime tests

| Part | Case | Harness | Result | Observed | Reason |
| --- | --- | --- | --- | --- | --- |
| A | prompt-me-explicit | claude-code 2.1.311 (Claude Code) | pass | /prompt-me was invoked | /prompt-me was invoked |
| A | prompt-me-near-miss | claude-code 2.1.311 (Claude Code) | pass | - | no Skill tool call for the candidate |

## Checked files

```
e7adf77f641bb9d234bb7588456cb5a2d9c9c2e4d0ce51f04c5432807262f7a7  .agents/skills/prompt-me/SKILL.md
a1499d95abd8447558c535fe5554adcc3c9b988a0a39264a6283d430effe1e94  .agents/skills/prompt-me/agents/openai.yaml
2fc2ee5467c8c04b2ff623f7670a68fe130add36817cdaa7d5c25c2f64aef4e2  .agents/skills/prompt-me/references/requirements.md
4ffd160f12b8ae12ad745941377e818a46e10d8535ef05a59251eef7ba2543c3  README.md
link  .claude/skills/prompt-me -> ../../.agents/skills/prompt-me
```

## Report data

```json
{
  "answers": {
    "A": {
      "event_without_agent": false,
      "every_time": "usually",
      "irreversible": false,
      "job": "procedure",
      "must_survive_compromise": "not-required",
      "own_context": false,
      "side_effects": false,
      "trigger": "user",
      "who_disables": "contributor"
    }
  },
  "bound_inputs": {
    "cases": {
      "A": "5c702bcaf6876ad3e2f513413d7c3804d066a847889a90667c80b7d48fbb4bfe"
    },
    "checkers": "1070f5e9c077925074cc173f075f918ce98998206fdaa029b5527b17b3f3d326",
    "files": {
      ".agents/skills/prompt-me/SKILL.md": "e7adf77f641bb9d234bb7588456cb5a2d9c9c2e4d0ce51f04c5432807262f7a7",
      ".agents/skills/prompt-me/agents/openai.yaml": "a1499d95abd8447558c535fe5554adcc3c9b988a0a39264a6283d430effe1e94",
      ".agents/skills/prompt-me/references/requirements.md": "2fc2ee5467c8c04b2ff623f7670a68fe130add36817cdaa7d5c25c2f64aef4e2",
      "README.md": "4ffd160f12b8ae12ad745941377e818a46e10d8535ef05a59251eef7ba2543c3"
    },
    "idea": "d050a5bb011e4c946b7b15da35a8c18b60decc2df4dde9debbaa44247b4f5d90",
    "kb_version": "0.6.0",
    "overrides": "4f53cda18c2baa0c0354bb5f9a3ecbe5ed12ab4d8e11ba873c2f11161202b945",
    "parts": {
      "A": "ce465b850f54828c55afcf21adeb9637b1a0810a54bb49a45e12daefcc4e1e2d"
    },
    "revision": "a9d1a41ce855fec682d5d975c28a3a379bd13a4b61c47d4590c778c3e85eea39",
    "rules": "5434c2fa865952f2d074f180ba164f66ae93214c9c0ed39575b50ba90c124def",
    "symlinks": {
      ".claude/skills/prompt-me": "../../.agents/skills/prompt-me"
    },
    "worker": "2bd94f207b2b32c8997150bf523e95d4b3132b3d8a85e458b918baf7bdeefd78"
  },
  "builds": {
    "A": {
      "forge": {
        "commit": "unknown",
        "source": "unknown",
        "tree": "unknown",
        "version": "0.4.0"
      },
      "outputs_changed": []
    }
  },
  "confirmed_parts": [
    "A"
  ],
  "contract_digest": "d00eeb5e6a1edbb730f3c51db4f2823a4e4748107e673eafc3048c1f5e689b01",
  "decision_digest": "090b08465ad8dac568bc77e5ca1ec547996454eec44618bf66b97af3db760bc6",
  "file_hashes": {
    ".agents/skills/prompt-me/SKILL.md": "e7adf77f641bb9d234bb7588456cb5a2d9c9c2e4d0ce51f04c5432807262f7a7",
    ".agents/skills/prompt-me/agents/openai.yaml": "a1499d95abd8447558c535fe5554adcc3c9b988a0a39264a6283d430effe1e94",
    ".agents/skills/prompt-me/references/requirements.md": "2fc2ee5467c8c04b2ff623f7670a68fe130add36817cdaa7d5c25c2f64aef4e2",
    "README.md": "4ffd160f12b8ae12ad745941377e818a46e10d8535ef05a59251eef7ba2543c3"
  },
  "idea_digest": "d050a5bb011e4c946b7b15da35a8c18b60decc2df4dde9debbaa44247b4f5d90",
  "kb_version": "0.6.0",
  "overrides": [],
  "part_map": {
    "dirs": {
      "A": ".agents/skills/prompt-me"
    },
    "files": {
      "A": [
        ".agents/skills/prompt-me/SKILL.md",
        ".agents/skills/prompt-me/agents/openai.yaml",
        ".agents/skills/prompt-me/references/requirements.md",
        "README.md"
      ]
    },
    "links": {
      "A": [
        ".claude/skills/prompt-me"
      ]
    },
    "requirement_parts": [
      "A"
    ]
  },
  "parts": [
    {
      "goal_result": "met by the verified build",
      "goal_verdict": {
        "reason": "The files achieve the goal. The skill is user-invoked in both harnesses. It gathers read-only context with an allowlist that applies until approval. It drafts the fixed section layout with untrusted material fenced and labelled, and limits Context to escaped repository data, with commit subjects only under 'git log'. Before any write it runs preflight checks for links and containment, treats missing paths as expected, stops without writing on failure and does not claim race-free writes. It creates .tmp/.gitignore with '*' only when it is missing and saves .tmp/prompt-me-<suffix>.md. It replies with only the path, a one-line intent and the two ways to continue, then stops. All eight accepted requirements are satisfied. The README reports the outside controls as recommended and not verified.",
        "verdict": "met"
      },
      "harness_result": "verified",
      "outside_dependencies": [],
      "part_id": "A",
      "rule_results": [
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.frontmatter.valid"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.name.format"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.description.length"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.description.concise"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.body.size"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.references.resolve"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.references.one-level"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.package.no-auxiliary-docs"
        },
        {
          "check": "script",
          "reason": "1 skill(s) linked",
          "result": "pass",
          "rule_id": "skills.portable.layout"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.portable.frontmatter"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.portable.no-claude-placeholders"
        },
        {
          "check": "script",
          "reason": "1 skill(s) checked",
          "result": "pass",
          "rule_id": "skills.invocation.both-flags"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:3",
          "reason": "The description opens with what the skill does ('Drafts a well-defined prompt from the user's request instead of carrying it out'), names the context it gathers and the output file, then gives trigger phrases a user would say.",
          "result": "pass",
          "rule_id": "skills.description.what-and-when"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:3",
          "reason": "The description summarizes the inputs, the output file and the fact that it stops for review. It does not list the procedure's steps, such as the preflight checks, the gitignore handling, the section layout or the reply format.",
          "result": "pass",
          "rule_id": "skills.description.no-workflow-steps"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:3",
          "reason": "The description says: 'Not for doing the task, editing code or answering the question directly.'",
          "result": "pass",
          "rule_id": "skills.description.boundary"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:3",
          "reason": "The description is in the third person ('Drafts\u2026', 'gathers\u2026'), not 'I can' or 'You can'.",
          "result": "pass",
          "rule_id": "skills.description.voice"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:8-75",
          "reason": "The body gives specific standing instructions (exact commands, the section layout, fence-length escaping, which secret files to skip, the preflight checks). It does not explain general concepts the model already knows.",
          "result": "pass",
          "rule_id": "skills.body.only-what-model-lacks"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:8-21",
          "reason": "The non-negotiable Requirements section comes directly after the title, before the Procedure. The untrusted-data warning opens the Procedure.",
          "result": "pass",
          "rule_id": "skills.body.gotchas-first"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md; references/requirements.md",
          "reason": "There are no time-bound statements such as 'currently', 'as of' or dates in any skill file.",
          "result": "pass",
          "rule_id": "skills.body.no-time-bound-statements"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:77-79",
          "reason": "The single reference file is named with its load condition: read it when you need the exact accepted wording, rule id or source. It holds provenance (rule ids, sources) that SKILL.md does not repeat.",
          "result": "pass",
          "rule_id": "skills.references.load-conditions"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:44-57",
          "reason": "Exact commands and checks are prescribed only for the fragile parts: preflight, escaping and the git lock flag. Other steps leave room for judgment, for example: 'Find the files\u2026 most likely touches'. There are no menus of options.",
          "result": "pass",
          "rule_id": "skills.body.strictness-matches-fragility"
        },
        {
          "check": "judged",
          "citation": "request.json inputs.files",
          "reason": "The skill bundles no scripts. Its only files are SKILL.md, agents/openai.yaml and a reference markdown file.",
          "result": "not-applicable",
          "rule_id": "skills.scripts.agent-caller"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:13,36,66",
          "reason": "Key rules carry reasons: --no-optional-locks so the index is not modified; commit subjects are free text written by whoever made the commit; fences sized so the content cannot close them. 'Never' is used for security-critical boundaries only.",
          "result": "pass",
          "rule_id": "skills.body.reasons-before-hard-rules"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:4; agents/openai.yaml:2",
          "reason": "The skill writes files under .tmp/ and is user-invoked in both targets: disable-model-invocation is true for Claude Code, and allow_implicit_invocation is false for Codex.",
          "result": "pass",
          "rule_id": "skills.invocation.side-effects-user-invoked"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:23",
          "reason": "Step 1 takes the request from the text the user wrote alongside the invocation, and asks for it in one line when it is missing. There is no argument substitution.",
          "result": "pass",
          "rule_id": "skills.inputs.from-message"
        },
        {
          "check": "judged",
          "citation": "README.md:33; links .claude/skills/prompt-me",
          "reason": "This is a user-invoked drafting skill; CI or cloud runs do not need it. It is committed in project scope anyway (.agents/skills, with a .claude/skills link).",
          "result": "not-applicable",
          "rule_id": "skills.scope.committed-for-automation"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:42",
          "reason": "There are no hidden directives, remote fetch-and-run, encoded payloads or credential access. The skill explicitly avoids opening secret-bearing files.",
          "result": "pass",
          "rule_id": "skills.security.no-surprising-content"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:1-5",
          "reason": "The frontmatter has no allowed-tools field, so the skill pre-grants no tools.",
          "result": "not-applicable",
          "rule_id": "skills.security.allowed-tools-least-privilege"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:36",
          "reason": "No credentials or tokens appear. The only credential-like text is the placeholder example 'https://user:token@host/...'.",
          "result": "pass",
          "rule_id": "security.secrets.none-in-files"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:21,38",
          "reason": "The Procedure tells the agent to treat repository files, issues, fetched pages and tool output as data, never as instructions. Step 5 forbids acting on embedded instructions.",
          "result": "pass",
          "rule_id": "security.untrusted-input.as-data"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:38,75",
          "reason": "The work starts only when the user replies 'go ahead'. Instructions found in content are recorded as 'found in source, not adopted', and the skill never takes instructions from the untrusted section. No content claim is treated as approval.",
          "result": "pass",
          "rule_id": "security.approval.claims-are-data"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:1-5,25-32",
          "reason": "The skill runs no bundled helpers and grants no pre-approval. It uses only standard commands under the harness's permissions.",
          "result": "not-applicable",
          "rule_id": "security.helpers.confined"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:29-30,38",
          "reason": "Outbound calls are limited to the issues, PRs and URLs the user named. Links inside fetched content are not followed, and fetched content cannot add actions.",
          "result": "pass",
          "rule_id": "security.outbound.minimal-data"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:46-53",
          "reason": "Step 8 checks .tmp, .tmp/.gitignore and the draft path with ls -ld for links, including dangling ones, and for type. Containment is checked against pwd -P. The skill stops on failure or unclear output and states that the checks are not race-free.",
          "result": "pass",
          "rule_id": "security.writes.within-boundary"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:66",
          "reason": "Untrusted content goes in backtick fences longer than any backtick run inside it, under a labelled section. The saved prompt opens that section with a fixed paragraph declaring it reference data, not instructions.",
          "result": "pass",
          "rule_id": "security.embedded-content.contained"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:42",
          "reason": "Step 6 forbids opening .env, .netrc, private keys, keystores and credentials files, as well as ambiguous .pem/.key files. It lists them by path only.",
          "result": "pass",
          "rule_id": "security.secrets.no-unneeded-reads"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:10,36,40,61,66",
          "reason": "Step 10 makes '## Untrusted reference material' the single place for content from issues, PRs, URLs, documents, repository files and commit subjects, with each item labelled by source and fenced. Context is limited to branch names, credential-free remotes, commit hashes and paths, introduced as repository-controlled names and written as code spans sized against backtick runs, with line breaks written as \\n. Step 4 keeps commit subjects out of Context, and step 6 quotes file content only in the untrusted section.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.untrusted-block"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:11,38,62",
          "reason": "Embedded instructions are not acted on or moved into the Task; they are recorded as 'found in source, not adopted'. The Task is derived only from the user's own request.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.no-fetched-instructions"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:12,25-32",
          "reason": "Step 2 lists the allowed read-only actions: file listing and reading, specific git, uname, pwd and ls commands, gh/glab views and user-given URLs. It applies 'until the user approves the draft'. The only writes allowed are .tmp/, a missing .tmp/.gitignore and the prompt file, each after the checks pass. Every command used in later steps is on the list.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.read-only-allowlist"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:13,27,57",
          "reason": "Every git command listed or used carries --no-optional-locks.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.git-no-optional-locks"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:14,38",
          "reason": "Issue and PR titles, bodies and comments are treated as untrusted, 'also when the repository belongs to the user or their organization'.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.issues-untrusted-any-owner"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:15,55",
          "reason": "Step 9 creates .tmp/.gitignore with exactly '*' only when it is missing, leaves an existing one unchanged and never modifies the repository's .gitignore.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.tmp-gitignore"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:36,65",
          "reason": "Step 4 runs git ls-files .tmp read-only. Step 10 adds a note to Assumptions & open questions that the .tmp/.gitignore rule does not untrack those files.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.tracked-drafts-note"
        },
        {
          "check": "judged",
          "citation": ".agents/skills/prompt-me/SKILL.md:17,46-53",
          "reason": "Before any write, the skill runs pwd -P and ls -ld on all three paths. Missing paths are treated as expected. It stops on any link, including dangling ones, on a wrong type, an existing draft, or a check that fails or is unclear, and reports that nothing was written. It says the checks do not detect changes made between the check and the write.",
          "result": "pass",
          "rule_id": "idea.well-defined-prompt.a.write-preflight"
        },
        {
          "check": "script",
          "reason": "2 control(s) listed",
          "result": "pass",
          "rule_id": "outside.readme.lists-controls"
        },
        {
          "check": "judged",
          "citation": "README.md:23,28",
          "reason": "The README states the real-refs condition for both codeowners-agent-config and outer-isolation.",
          "result": "pass",
          "rule_id": "outside.gate.real-refs"
        },
        {
          "check": "judged",
          "citation": "README.md:21,27",
          "reason": "The README states the no-agent-bypass condition for both controls.",
          "result": "pass",
          "rule_id": "outside.merge.no-agent-bypass"
        },
        {
          "check": "judged",
          "citation": "README.md:22",
          "reason": "The README states this condition for codeowners-agent-config, the only control that lists it.",
          "result": "pass",
          "rule_id": "outside.merge.requester-cannot-approve"
        },
        {
          "check": "judged",
          "citation": "README.md:17",
          "reason": "The README states this condition for codeowners-agent-config, the only control that lists it.",
          "result": "pass",
          "rule_id": "outside.ci.workflow-protected"
        },
        {
          "check": "judged",
          "citation": "README.md:19,26",
          "reason": "The README states this condition for both controls.",
          "result": "pass",
          "rule_id": "outside.gate.no-broader-bypass"
        },
        {
          "check": "judged",
          "citation": "README.md:20",
          "reason": "The README states this condition for codeowners-agent-config, the only control that lists it.",
          "result": "pass",
          "rule_id": "outside.gate.plan-enforced"
        },
        {
          "check": "judged",
          "citation": "README.md:24,29",
          "reason": "The README states periodic verification for both controls.",
          "result": "pass",
          "rule_id": "outside.gate.periodic-verification"
        },
        {
          "check": "judged",
          "citation": "README.md:18",
          "reason": "The README recommends a CODEOWNERS entry covering .agents/, .claude/, .codex/, AGENTS.md, CODEOWNERS and the other agent configuration files, together with a branch rule that requires code-owner review.",
          "result": "pass",
          "rule_id": "outside.codeowners.agent-config"
        },
        {
          "check": "judged",
          "citation": "request.json context.facts.opens_prs; SKILL.md:32",
          "reason": "The agent opens no pull requests (context facts opens_prs: false), and the skill forbids commit and push while drafting.",
          "result": "not-applicable",
          "rule_id": "outside.merge.rule-for-agent-prs"
        },
        {
          "check": "judged",
          "reason": "a condition in applies_to.when does not hold",
          "result": "not-applicable",
          "rule_id": "skills.goal.no-must-hold-rule-in-skill"
        },
        {
          "check": "script",
          "reason": "a condition in applies_to.when does not hold",
          "result": "not-applicable",
          "rule_id": "skills.portable.plugin-layout"
        },
        {
          "check": "judged",
          "reason": "a condition in applies_to.when does not hold",
          "result": "not-applicable",
          "rule_id": "skills.reuse.reviewed-and-pinned"
        }
      ],
      "status": "verified"
    }
  ],
  "revision_digest": "a9d1a41ce855fec682d5d975c28a3a379bd13a4b61c47d4590c778c3e85eea39",
  "rules_digest": "5434c2fa865952f2d074f180ba164f66ae93214c9c0ed39575b50ba90c124def",
  "run_id": "20261027T051310Z-7d1c50be",
  "runtime_results": [
    {
      "case_id": "prompt-me-explicit",
      "details": null,
      "environment": "throwaway workspace with only the frozen skill and fixtures; invoked as /prompt-me; tools: Skill, Read, Grep, Glob; network: none requested; app.py sha256 3f50741f0940aed0388efcef882bdba673c7febb0268695ccaf53c75b7c45854",
      "expected": "activates",
      "file_hashes": {
        ".agents/skills/prompt-me/SKILL.md": "e7adf77f641bb9d234bb7588456cb5a2d9c9c2e4d0ce51f04c5432807262f7a7",
        ".agents/skills/prompt-me/agents/openai.yaml": "a1499d95abd8447558c535fe5554adcc3c9b988a0a39264a6283d430effe1e94",
        ".agents/skills/prompt-me/references/requirements.md": "2fc2ee5467c8c04b2ff623f7670a68fe130add36817cdaa7d5c25c2f64aef4e2"
      },
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "inventory": "observed",
      "kind": "activation",
      "observed_activation": "/prompt-me was invoked",
      "part_id": "A",
      "prompt": "add input validation to the signup handler in app.py so empty emails are rejected",
      "reason": "/prompt-me was invoked",
      "result": "pass",
      "run_id": "20261027T051310Z-7d1c50be"
    },
    {
      "case_id": "prompt-me-near-miss",
      "details": null,
      "environment": "throwaway workspace with only the frozen skill and fixtures; tools: Skill, Read, Grep, Glob; network: none requested; greeting.txt sha256 6ddd243dd2f21014018d26b20985d9616d387a40a120f08e43a1dc87146734f0",
      "expected": "does-not-activate",
      "file_hashes": {
        ".agents/skills/prompt-me/SKILL.md": "e7adf77f641bb9d234bb7588456cb5a2d9c9c2e4d0ce51f04c5432807262f7a7",
        ".agents/skills/prompt-me/agents/openai.yaml": "a1499d95abd8447558c535fe5554adcc3c9b988a0a39264a6283d430effe1e94",
        ".agents/skills/prompt-me/references/requirements.md": "2fc2ee5467c8c04b2ff623f7670a68fe130add36817cdaa7d5c25c2f64aef4e2"
      },
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "inventory": "observed",
      "kind": "activation",
      "observed_activation": null,
      "part_id": "A",
      "prompt": "Reword the greeting text in greeting.txt so it sounds friendlier; just tell me the new sentence.",
      "reason": "no Skill tool call for the candidate",
      "result": "pass",
      "run_id": "20261027T051310Z-7d1c50be"
    }
  ],
  "scope": "Review (recommended): judged A",
  "scope_parts": [
    "A"
  ],
  "symlinks": {
    ".claude/skills/prompt-me": "../../.agents/skills/prompt-me"
  },
  "tool_versions": {
    "harness-forge-checkers": "1070f5e9c077925074cc173f075f918ce98998206fdaa029b5527b17b3f3d326",
    "harness-forge-verifier-commit": "unknown",
    "harness-forge-verifier-source": "unknown",
    "harness-forge-verifier-tree": "unknown",
    "harness-forge-verifier-version": "0.4.0"
  },
  "whole_idea": {
    "facts": {
      "bypass_mode": true,
      "lethal_trifecta": true,
      "opens_prs": false,
      "plan_controls": "available",
      "reach": "public",
      "target_set": "both",
      "untrusted_repo": true
    },
    "hosting": {
      "plan": "free",
      "platform": "github",
      "visibility": "public"
    },
    "reach": "public",
    "targets": [
      "claude-code",
      "codex"
    ]
  },
  "worker_evidence": [
    {
      "configuration_digest": "ee513860b21a159a1c3b248985d44917ab66d000740c58dab4c94c971fcc9345",
      "configured_controls": [
        "command: [\"claude\", \"--print\", \"--output-format\", \"stream-json\", \"--verbose\", \"--no-session-persistence\", \"--safe-mode\", \"--restricted\", \"--setting-sources\", \"\", \"--strict-mcp-config\", \"--mcp-config\", \"{\\\"mcpServers\\\":{}}\", \"--disable-slash-commands\", \"--permission-mode\", \"dontAsk\", \"--permission-prompts\", \"none\", \"--settings\", \"{\\\"disableAllHooks\\\":true,\\\"autoMemoryEnabled\\\":false}\", \"--tools\", \"WebFetch,WebSearch\", \"--allowedTools\", \"WebFetch,WebSearch\", \"--json-schema\", \"{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"findings\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"claim\\\":{\\\"type\\\":\\\"string\\\"},\\\"source\\\":{\\\"type\\\":\\\"string\\\"},\\\"fetched\\\":{\\\"type\\\":\\\"string\\\"},\\\"quote\\\":{\\\"type\\\":\\\"string\\\"},\\\"context\\\":{\\\"type\\\":\\\"string\\\"},\\\"source_role\\\":{\\\"enum\\\":[\\\"primary\\\",\\\"practitioner\\\",\\\"trade-press\\\"]},\\\"requirement_id\\\":{\\\"type\\\":[\\\"string\\\",\\\"null\\\"]}},\\\"required\\\":[\\\"claim\\\",\\\"source\\\",\\\"fetched\\\",\\\"quote\\\",\\\"context\\\",\\\"source_role\\\",\\\"requirement_id\\\"],\\\"additionalProperties\\\":false}}},\\\"required\\\":[\\\"findings\\\"],\\\"additionalProperties\\\":false}\"]",
        "environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER",
        "login: subscription (claude.ai)"
      ],
      "evidence_refs": [],
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "isolation_status": "not-certified",
      "launcher": "independent-process",
      "model": "account default",
      "observed_behavior": [],
      "observed_tools": {
        "status": "unknown"
      },
      "role": "research",
      "unknowns": [
        "context, file and network isolation are not certified",
        "not every tool-registration path is observable"
      ],
      "worker_policy": "best-effort-v1"
    },
    {
      "configuration_digest": "f79908e2f8761717b26bb5d87aed5c56e135ba70a0edb97e404129d59e06e708",
      "configured_controls": [
        "command: [\"claude\", \"--print\", \"--output-format\", \"stream-json\", \"--verbose\", \"--no-session-persistence\", \"--safe-mode\", \"--restricted\", \"--setting-sources\", \"\", \"--strict-mcp-config\", \"--mcp-config\", \"{\\\"mcpServers\\\":{}}\", \"--disable-slash-commands\", \"--permission-mode\", \"dontAsk\", \"--permission-prompts\", \"none\", \"--settings\", \"{\\\"disableAllHooks\\\":true,\\\"autoMemoryEnabled\\\":false}\", \"--tools\", \"\", \"--allowedTools\", \"\", \"--json-schema\", \"{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"verdicts\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"finding_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdict\\\":{\\\"enum\\\":[\\\"supported\\\",\\\"unsupported\\\"]},\\\"reasoning\\\":{\\\"type\\\":\\\"string\\\"}},\\\"required\\\":[\\\"finding_id\\\",\\\"verdict\\\",\\\"reasoning\\\"],\\\"additionalProperties\\\":false}}},\\\"required\\\":[\\\"verdicts\\\"],\\\"additionalProperties\\\":false}\"]",
        "environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER",
        "login: subscription (claude.ai)"
      ],
      "evidence_refs": [],
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "isolation_status": "not-certified",
      "launcher": "independent-process",
      "model": "account default",
      "observed_behavior": [],
      "observed_tools": {
        "status": "unknown"
      },
      "role": "source-support",
      "unknowns": [
        "context, file and network isolation are not certified",
        "not every tool-registration path is observable"
      ],
      "worker_policy": "best-effort-v1"
    },
    {
      "configuration_digest": "bd41806234b54333f0b42bf98e08945ea9756a175b212e92e0435a771b2beb3f",
      "configured_controls": [
        "command: [\"claude\", \"--print\", \"--output-format\", \"stream-json\", \"--verbose\", \"--no-session-persistence\", \"--safe-mode\", \"--restricted\", \"--setting-sources\", \"\", \"--strict-mcp-config\", \"--mcp-config\", \"{\\\"mcpServers\\\":{}}\", \"--disable-slash-commands\", \"--permission-mode\", \"dontAsk\", \"--permission-prompts\", \"none\", \"--settings\", \"{\\\"disableAllHooks\\\":true,\\\"autoMemoryEnabled\\\":false}\", \"--tools\", \"Read,Grep,Glob\", \"--allowedTools\", \"Read,Grep,Glob\", \"--json-schema\", \"{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"run_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdicts\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"part_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"rule_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdict\\\":{\\\"enum\\\":[\\\"pass\\\",\\\"fail\\\",\\\"not-applicable\\\"]},\\\"reason\\\":{\\\"type\\\":\\\"string\\\"},\\\"citation\\\":{\\\"type\\\":\\\"string\\\"}},\\\"required\\\":[\\\"part_id\\\",\\\"rule_id\\\",\\\"verdict\\\",\\\"reason\\\",\\\"citation\\\"],\\\"additionalProperties\\\":false}},\\\"goal_verdicts\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"part_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdict\\\":{\\\"enum\\\":[\\\"met\\\",\\\"not-met\\\"]},\\\"reason\\\":{\\\"type\\\":\\\"string\\\"}},\\\"required\\\":[\\\"part_id\\\",\\\"verdict\\\",\\\"reason\\\"],\\\"additionalProperties\\\":false}}},\\\"required\\\":[\\\"run_id\\\",\\\"verdicts\\\",\\\"goal_verdicts\\\"],\\\"additionalProperties\\\":false}\"]",
        "environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER",
        "login: subscription (claude.ai)"
      ],
      "evidence_refs": [],
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "isolation_status": "not-certified",
      "launcher": "independent-process",
      "model": "account default",
      "observed_behavior": [],
      "observed_tools": {
        "status": "unknown"
      },
      "role": "review",
      "unknowns": [
        "context, file and network isolation are not certified",
        "not every tool-registration path is observable"
      ],
      "worker_policy": "best-effort-v1"
    },
    {
      "configuration_digest": "bd41806234b54333f0b42bf98e08945ea9756a175b212e92e0435a771b2beb3f",
      "configured_controls": [
        "command: [\"claude\", \"--print\", \"--output-format\", \"stream-json\", \"--verbose\", \"--no-session-persistence\", \"--safe-mode\", \"--restricted\", \"--setting-sources\", \"\", \"--strict-mcp-config\", \"--mcp-config\", \"{\\\"mcpServers\\\":{}}\", \"--disable-slash-commands\", \"--permission-mode\", \"dontAsk\", \"--permission-prompts\", \"none\", \"--settings\", \"{\\\"disableAllHooks\\\":true,\\\"autoMemoryEnabled\\\":false}\", \"--tools\", \"Read,Grep,Glob\", \"--allowedTools\", \"Read,Grep,Glob\", \"--json-schema\", \"{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"run_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdicts\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"part_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"rule_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdict\\\":{\\\"enum\\\":[\\\"pass\\\",\\\"fail\\\",\\\"not-applicable\\\"]},\\\"reason\\\":{\\\"type\\\":\\\"string\\\"},\\\"citation\\\":{\\\"type\\\":\\\"string\\\"}},\\\"required\\\":[\\\"part_id\\\",\\\"rule_id\\\",\\\"verdict\\\",\\\"reason\\\",\\\"citation\\\"],\\\"additionalProperties\\\":false}},\\\"goal_verdicts\\\":{\\\"type\\\":\\\"array\\\",\\\"items\\\":{\\\"type\\\":\\\"object\\\",\\\"properties\\\":{\\\"part_id\\\":{\\\"type\\\":\\\"string\\\"},\\\"verdict\\\":{\\\"enum\\\":[\\\"met\\\",\\\"not-met\\\"]},\\\"reason\\\":{\\\"type\\\":\\\"string\\\"}},\\\"required\\\":[\\\"part_id\\\",\\\"verdict\\\",\\\"reason\\\"],\\\"additionalProperties\\\":false}}},\\\"required\\\":[\\\"run_id\\\",\\\"verdicts\\\",\\\"goal_verdicts\\\"],\\\"additionalProperties\\\":false}\"]",
        "environment names: CLAUDE_CONFIG_DIR, HOME, LANG, LOGNAME, PATH, TMPDIR, USER",
        "login: subscription (claude.ai)"
      ],
      "evidence_refs": [],
      "harness": "claude-code",
      "harness_version": "2.1.311 (Claude Code)",
      "isolation_status": "not-certified",
      "launcher": "independent-process",
      "model": "account default",
      "observed_behavior": [
        "model reported: claude-opus-5-5",
        "apiKeySource: none",
        "skills listed: ",
        "plugins listed: cc-plugin-agents-md (builtin), cc-plugin-plugin-authoring (builtin), cc-plugin-telemetry (builtin)"
      ],
      "observed_tools": {
        "status": "observed",
        "tools": [
          "Glob",
          "Grep",
          "Read",
          "StructuredOutput"
        ]
      },
      "role": "review",
      "unknowns": [
        "context, file and network isolation are not certified",
        "not every tool-registration path is observable"
      ],
      "worker_policy": "best-effort-v1"
    }
  ],
  "worker_violations": []
}
```
