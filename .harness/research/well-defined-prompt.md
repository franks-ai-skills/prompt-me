---
slug: well-defined-prompt
search_mode: live
briefs:
- pass: survey
  part_id: null
  digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
- pass: deep
  part_id: A
  digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
findings:
- id: F1
  part_id: null
  claim: SweetPrompt is an existing Claude Code skill that turns a rough request into a codebase-grounded
    prompt, the same core idea as this brief.
  source: https://github.com/Brett777/sweetprompt
  fetched: '2026-10-24'
  quote: SweetPrompt is a Claude Code skill that turns a rough, half-formed request into a precise, codebase-grounded
    prompt.
  context: SweetPrompt is a Claude Code skill that turns a rough, half-formed request into a precise,
    codebase-grounded prompt.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F6
  part_id: null
  claim: The ECC prompt-optimizer skill is advisory only and is told not to execute the user's task.
  source: https://github.com/affaan-m/ECC/blob/main/skills/prompt-optimizer/SKILL.md
  fetched: '2026-10-24'
  quote: Advisory only — do not execute the user's task.
  context: Advisory only — do not execute the user's task.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F7
  part_id: null
  claim: The ECC prompt-optimizer limits its output to an analysis plus an optimized prompt.
  source: https://github.com/affaan-m/ECC/blob/main/skills/prompt-optimizer/SKILL.md
  fetched: '2026-10-24'
  quote: Your ONLY output is an analysis plus an optimized prompt.
  context: Your ONLY output is an analysis plus an optimized prompt.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F9
  part_id: null
  claim: OWASP defines indirect prompt injection as an LLM taking input from external sources such as
    websites or files, which covers the issue URLs and documents this skill gathers.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-24'
  quote: Indirect prompt injections occur when an LLM accepts input from external sources, such as websites
    or files.
  context: Indirect prompt injections occur when an LLM accepts input from external sources, such as websites
    or files.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F10
  part_id: null
  claim: OWASP recommends separating untrusted content and marking it clearly to limit its influence,
    which fits the brief's goal of treating gathered information as reference data only.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-24'
  quote: Separate and clearly denote untrusted content to limit its influence on user prompts.
  context: Separate and clearly denote untrusted content to limit its influence on user prompts.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F12
  part_id: null
  claim: OWASP recommends human-in-the-loop controls for privileged operations, which matches the brief's
    stop-and-review step before acting.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-24'
  quote: Implement human-in-the-loop controls for privileged operations to prevent unauthorized actions.
  context: Implement human-in-the-loop controls for privileged operations to prevent unauthorized actions.
  brief_digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
  source_role: primary
  pass: survey
- id: F24
  part_id: A
  claim: OWASP recommends separating untrusted content and clearly marking it so it has less influence
    on user prompts.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-24'
  quote: Separate and clearly denote untrusted content to limit its influence on user prompts.
  context: Separate and clearly denote untrusted content to limit its influence on user prompts.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F29
  part_id: A
  claim: Patterns in a .gitignore file match relative to that file's own directory, so a .tmp/.gitignore
    containing * applies only inside .tmp/.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-24'
  quote: These patterns match relative to the location of the .gitignore file.
  context: Patterns read from a .gitignore file in the same directory as the path, or in any parent directory
    (up to the top-level of the working tree), with patterns in the higher level files being overridden
    by those in lower level files down to the directory containing the file. These patterns match relative
    to the location of the .gitignore file. A project normally includes such .gitignore files in its repository,
    containing patterns for files generated as part of the project build.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F30
  part_id: A
  claim: In gitignore patterns, an asterisk matches anything except a slash.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-24'
  quote: An asterisk "*" matches anything except a slash.
  context: An asterisk "*" matches anything except a slash. The character "?" matches any one character
    except "/". The range notation, e.g. [a-zA-Z], can be used to match one of the characters in a range.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F31
  part_id: A
  claim: gitignore does not affect files Git already tracks. A drafted prompt that is already tracked
    in .tmp/ stays tracked even after the * rule is added.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-24'
  quote: Files already tracked by Git are not affected; see the NOTES below for details.
  context: A gitignore file specifies intentionally untracked files that Git should ignore. Files already
    tracked by Git are not affected; see the NOTES below for details.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F34
  part_id: A
  claim: Spotlighting is a family of prompt engineering techniques meant to improve an LLM's ability to
    distinguish among multiple sources of input, proposed in response to LLMs mistaking adversarial instructions
    in data for user commands.
  source: https://arxiv.org/abs/2403.14720
  fetched: '2026-10-24'
  quote: We introduce spotlighting, a family of prompt engineering techniques that can be used to improve
    LLMs' ability to distinguish among multiple sources of input.
  context: Often, the LLM will mistake the adversarial instructions as user commands to be followed, creating
    a security vulnerability in the larger system. We introduce spotlighting, a family of prompt engineering
    techniques that can be used to improve LLMs' ability to distinguish among multiple sources of input.
    The key insight is to utilize transformations of an input to provide a reliable and continuous signal
    of its provenance.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F35
  part_id: A
  claim: The key idea of spotlighting is to transform an input so that it carries a reliable and continuous
    signal of where it came from.
  source: https://arxiv.org/abs/2403.14720
  fetched: '2026-10-24'
  quote: The key insight is to utilize transformations of an input to provide a reliable and continuous
    signal of its provenance.
  context: We introduce spotlighting, a family of prompt engineering techniques that can be used to improve
    LLMs' ability to distinguish among multiple sources of input. The key insight is to utilize transformations
    of an input to provide a reliable and continuous signal of its provenance.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F36
  part_id: A
  claim: In the GitHub MCP attack, the agent reads through the repository's issues, reaches the injected
    payload, and then pulls private repository data into context and leaks it into a pull request on the
    public repo.
  source: https://invariantlabs.ai/blog/mcp-github-vulnerability
  fetched: '2026-10-24'
  quote: The agent now goes through the list of issues until it finds the attack payload.
  context: The agent now goes through the list of issues until it finds the attack payload. It willingly
    pulls private repository data into context, and leaks it into a pull request of the pacman repo, which
    is freely accessible to the attacker since it is public.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F37
  part_id: A
  claim: The vulnerability arises even when the tools are fully trusted, because agents are exposed to
    untrusted information when connected to platforms like GitHub.
  source: https://invariantlabs.ai/blog/mcp-github-vulnerability
  fetched: '2026-10-24'
  quote: Instead, the issue emerges even with fully trusted tools, as agents can be exposed to untrusted
    information when connected to external platforms like GitHub.
  context: Unlike previously-discovered tool poisoning attacks with MCP, this vulnerability does not require
    the MCP tools themselves to be compromised. Instead, the issue emerges even with fully trusted tools,
    as agents can be exposed to untrusted information when connected to external platforms like GitHub.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F38
  part_id: A
  claim: Agents connected to GitHub can be exposed to untrusted information even when the tools are fully
    trusted; the attack does not need compromised tools.
  source: https://invariantlabs.ai/blog/mcp-github-vulnerability
  fetched: '2026-10-24'
  quote: Instead, the issue emerges even with fully trusted tools, as agents can be exposed to untrusted
    information when connected to external platforms like GitHub.
  context: Unlike previously-discovered tool poisoning attacks with MCP, this vulnerability does not require
    the MCP tools themselves to be compromised. Instead, the issue emerges even with fully trusted tools,
    as agents can be exposed to untrusted information when connected to external platforms like GitHub.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F39
  part_id: A
  claim: In the described attack, the injected payload sat in the issues of a repository being read by
    the account owner's agent, and that agent then leaked the owner's private repository data.
  source: https://invariantlabs.ai/blog/mcp-github-vulnerability
  fetched: '2026-10-24'
  quote: The agent now goes through the list of issues until it finds the attack payload.
  context: The agent now goes through the list of issues until it finds the attack payload. It willingly
    pulls private repository data into context, and leaks it into a pull request of the pacman repo, which
    is freely accessible to the attacker since it is public.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F40
  part_id: A
  claim: git's --no-optional-locks option skips optional operations that require locks and is equivalent
    to setting GIT_OPTIONAL_LOCKS to 0.
  source: https://git-scm.com/docs/git
  fetched: '2026-10-24'
  quote: This is equivalent to setting the GIT_OPTIONAL_LOCKS to 0.
  context: Do not perform optional operations that require locks. This is equivalent to setting the GIT_OPTIONAL_LOCKS
    to 0.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
- id: F41
  part_id: A
  claim: Setting GIT_OPTIONAL_LOCKS to false stops git status from refreshing the index as a side effect.
  source: https://git-scm.com/docs/git
  fetched: '2026-10-24'
  quote: For example, this will prevent git status from refreshing the index as a side effect.
  context: If this Boolean environment variable is set to false, Git will complete any requested operation
    without performing any optional sub-operations that require taking a lock. For example, this will
    prevent git status from refreshing the index as a side effect. This is useful for processes running
    in the background which do not want to cause lock contention with other operations on the repository.
  brief_digest: 7775bb128c2c1fb6d9beba0c1b5238fa687592f5c0a5f4911cd9242bbeb846ba
  source_role: primary
  pass: deep
support:
- finding_id: F1
  quote_check: pass
  verdict: supported
  worker_ref: support-f1
  finding_digest: e350e0e9d55a3b90beffdddeb1713680531bd036a9a67b02b0f019a779a98e9e
- finding_id: F2
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f2
- finding_id: F3
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f3
- finding_id: F4
  quote_check: fail
  verdict: missing
  worker_ref: support-f4
- finding_id: F5
  quote_check: fail
  verdict: missing
  worker_ref: support-f5
- finding_id: F6
  quote_check: pass
  verdict: supported
  worker_ref: support-f6
  finding_digest: eab54c3aced4bdfdee483e7161e7d016cadff5e03e945fabb658e216c2d958c8
- finding_id: F7
  quote_check: pass
  verdict: supported
  worker_ref: support-f7
  finding_digest: f8b083bd1d8878fad77ccea64447824dec2f44ae96c8482f504a79fee5fa4771
- finding_id: F8
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f8
- finding_id: F9
  quote_check: pass
  verdict: supported
  worker_ref: support-f9
  finding_digest: 1556be4e4d8b9ca0822ab17af61cf03e1e88565dd45716dbda828cc48c499db4
- finding_id: F10
  quote_check: pass
  verdict: supported
  worker_ref: support-f10
  finding_digest: 4b1f91427e55baaf6505233f6d43bb14b83166a18e304e684be7ca0bdfe1fc32
- finding_id: F11
  quote_check: fail
  verdict: missing
  worker_ref: support-f11
- finding_id: F12
  quote_check: pass
  verdict: supported
  worker_ref: support-f12
  finding_digest: 0bcd070eeb53db2b0b8bb081ab55e41b1e143a5e7dd084d7c6d6243f25564c80
- finding_id: F13
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f13
- finding_id: F17
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f17
- finding_id: F18
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f18
- finding_id: F23
  quote_check: pass
  verdict: supported
  worker_ref: support-f23
- finding_id: F24
  quote_check: pass
  verdict: supported
  worker_ref: support-f24
  finding_digest: db51235d67f3b3d31e92178e28a5fd8c78bddd7f287a19f079ccc0eed561a0f8
- finding_id: F25
  quote_check: fail
  verdict: missing
  worker_ref: support-f25
- finding_id: F26
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f26
- finding_id: F27
  quote_check: pass
  verdict: supported
  worker_ref: support-f27
- finding_id: F28
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f28
- finding_id: F29
  quote_check: pass
  verdict: supported
  worker_ref: support-f29
  finding_digest: 9171b241d4bdf28fecb981905b71c74e341e90806ddf88b7d9986d220d9df473
- finding_id: F30
  quote_check: pass
  verdict: supported
  worker_ref: support-f30
  finding_digest: ae6ad6374d96e9c690b309b0391b6c167bdb7c9b5659980b8ed54cfab3770753
- finding_id: F31
  quote_check: pass
  verdict: supported
  worker_ref: support-f31
  finding_digest: 69d3ae19b26f3eb31d48437546f442e45601ae3e4b06ecd9fc67b7af8364cf26
- finding_id: F32
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f32
- finding_id: F33
  quote_check: fail
  verdict: missing
  worker_ref: support-f33
- finding_id: F34
  quote_check: pass
  verdict: supported
  worker_ref: support-f34
  finding_digest: 26f3c53b1c75413d0c1165712cb83ef1bcc24493d3f926916fd462454e5eaf95
- finding_id: F35
  quote_check: pass
  verdict: supported
  worker_ref: support-f35
  finding_digest: f64f910213a04c9a6da4901f86aaa3aafbf15d2e39d3d607f01819c2ad6aa805
- finding_id: F36
  quote_check: pass
  verdict: supported
  worker_ref: support-f36
  finding_digest: a0a2790e2be88780fb29cadfed1a65db476fa2fef7012badb58ee2b7cf73f7a6
- finding_id: F37
  quote_check: pass
  verdict: supported
  worker_ref: support-f37
  finding_digest: 38ba58b629057cf4ac037dec55f26f2104cf324f4c35207f09b0cdc5f4ad10be
- finding_id: F38
  quote_check: pass
  verdict: supported
  worker_ref: support-f38
  finding_digest: e702506bb248cc2ee6f0196b3422741a1f831b2ce5d62e9f5202de81ee19e23c
- finding_id: F39
  quote_check: pass
  verdict: supported
  worker_ref: support-f39
  finding_digest: 5e5c2a45eb060a55b55e434b45005df8c473506e91634462babb008e00f54e84
- finding_id: F40
  quote_check: pass
  verdict: supported
  worker_ref: support-f40
  finding_digest: 64f1176b659888613cdd626de3ec898a778fc6b97ecf3ec743096777eb44c319
- finding_id: F41
  quote_check: pass
  verdict: supported
  worker_ref: support-f41
  finding_digest: 0507d2934b61bf8baaa3f4d546c48a4765bc3300478ca2068e564403532856e0
drift: []
---
Findings grouped by pass and part are in the frontmatter; dropped findings are not kept.
