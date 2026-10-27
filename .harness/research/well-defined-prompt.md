---
slug: well-defined-prompt
search_mode: live
briefs:
- pass: survey
  part_id: null
  digest: 23ed0211c08dde6ecde7b5b79cbaf0f08ce0ccb8e6d3d5de65b03f727e5f6b0b
- pass: deep
  part_id: A
  digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
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
- id: F42
  part_id: A
  claim: OWASP describes indirect prompt injection as occurring when an LLM accepts input from external
    sources such as websites or files, which covers fetched issue pages and documents.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-27'
  quote: Indirect prompt injections occur when an LLM accepts input from external sources, such as websites
    or files.
  context: Indirect prompt injections occur when an LLM accepts input from external sources, such as websites
    or files.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F43
  part_id: A
  claim: OWASP recommends separating and clearly marking untrusted content to limit its influence, which
    supports a clearly marked 'Untrusted reference material' block.
  source: https://genai.owasp.org/llmrisk/llm01-prompt-injection/
  fetched: '2026-10-27'
  quote: Separate and clearly denote untrusted content to limit its influence on user prompts.
  context: Separate and clearly denote untrusted content to limit its influence on user prompts.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F46
  part_id: A
  claim: The spotlighting paper says indirect prompt injection works by embedding adversarial instructions
    in untrusted data that is processed alongside user commands.
  source: https://arxiv.org/abs/2403.14720
  fetched: '2026-10-27'
  quote: Indirect prompt injection attacks take advantage of this vulnerability by embedding adversarial
    instructions into untrusted data being processed alongside user commands.
  context: However, the LLM is unable to distinguish which sections of prompt belong to various input
    sources. Indirect prompt injection attacks take advantage of this vulnerability by embedding adversarial
    instructions into untrusted data being processed alongside user commands. Often, the LLM will mistake
    the adversarial instructions as user commands to be followed, creating a security vulnerability in
    the larger system.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F50
  part_id: A
  claim: RFC 3986 deprecates the user:password format in the URI userinfo field, which supports removing
    credentials from remote URLs before they are written to the prompt.
  source: https://www.rfc-editor.org/rfc/rfc3986#section-3.2.1
  fetched: '2026-10-27'
  quote: Use of the format "user:password" in the userinfo field is deprecated.
  context: Use of the format "user:password" in the userinfo field is deprecated.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F51
  part_id: A
  claim: A GitLab Runner issue reports a real case in which a git remote URL leaked the username and a
    temporary token used to fetch the repository.
  source: https://gitlab.com/gitlab-org/gitlab-runner/-/issues/29655
  fetched: '2026-10-27'
  quote: The remote URL leaks the username and temporary token used to fetch the repository for the job.
  context: The remote URL leaks the username and temporary token used to fetch the repository for the
    job.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F52
  part_id: A
  claim: CWE-59 says link-following vulnerabilities are multi-factor vulnerabilities, which is relevant
    to checking .tmp and the draft path for symlinks.
  source: https://cwe.mitre.org/data/definitions/59.html
  fetched: '2026-10-27'
  quote: Link following vulnerabilities are Multi-factor Vulnerabilities (MFV).
  context: Link following vulnerabilities are Multi-factor Vulnerabilities (MFV).
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F53
  part_id: A
  claim: CWE-367 says a resource's state can change between the check and the use, which is why the symlink
    and containment checks are preflight checks and do not guarantee race-free writing.
  source: https://cwe.mitre.org/data/definitions/367.html
  fetched: '2026-10-27'
  quote: The product checks the state of a resource before using that resource, but the resource's state
    can change between the check and the use in a way that invalidates the results of the check.
  context: The product checks the state of a resource before using that resource, but the resource's state
    can change between the check and the use in a way that invalidates the results of the check.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F54
  part_id: A
  claim: Git matches patterns in a .gitignore file relative to that file's location, so a .tmp/.gitignore
    applies to the .tmp directory.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-27'
  quote: These patterns match relative to the location of the .gitignore file.
  context: These patterns match relative to the location of the .gitignore file.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F55
  part_id: A
  claim: Gitignore patterns do not affect files Git already tracks, so a '*' in .tmp/.gitignore does not
    stop drafts that were already committed from being tracked.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-27'
  quote: Files already tracked by Git are not affected; see the NOTES below for details.
  context: Files already tracked by Git are not affected; see the NOTES below for details.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F56
  part_id: A
  claim: In gitignore patterns, an asterisk matches anything except a slash.
  source: https://git-scm.com/docs/gitignore
  fetched: '2026-10-27'
  quote: An asterisk "*" matches anything except a slash.
  context: An asterisk "*" matches anything except a slash.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F58
  part_id: A
  claim: CommonMark allows any ASCII punctuation character to be backslash-escaped, which gives one way
    to escape Markdown delimiters in repository data.
  source: https://spec.commonmark.org/0.31.2/
  fetched: '2026-10-27'
  quote: 'Any ASCII punctuation character may be backslash-escaped:'
  context: 'Any ASCII punctuation character may be backslash-escaped:'
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F59
  part_id: A
  claim: gh issue view shows an issue's title, body and other information.
  source: https://cli.github.com/manual/gh_issue_view
  fetched: '2026-10-27'
  quote: Display the title, body, and other information about an issue.
  context: Display the title, body, and other information about an issue.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F61
  part_id: A
  claim: The vulnerability does not require compromised tools; it arises with fully trusted tools because
    agents connected to platforms like GitHub can be exposed to untrusted information.
  source: https://invariantlabs.ai/blog/mcp-github-vulnerability
  fetched: '2026-10-27'
  quote: Instead, the issue emerges even with fully trusted tools, as agents can be exposed to untrusted
    information when connected to external platforms like GitHub.
  context: Unlike previously-discovered tool poisoning attacks with MCP, this vulnerability does not require
    the MCP tools themselves to be compromised. Instead, the issue emerges even with fully trusted tools,
    as agents can be exposed to untrusted information when connected to external platforms like GitHub.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F64
  part_id: A
  claim: Setting GIT_OPTIONAL_LOCKS to false makes Git skip optional sub-operations that take a lock,
    for example keeping git status from refreshing the index as a side effect.
  source: https://git-scm.com/docs/git
  fetched: '2026-10-27'
  quote: If this Boolean environment variable is set to false, Git will complete any requested operation
    without performing any optional sub-operations that require taking a lock.
  context: If this Boolean environment variable is set to false, Git will complete any requested operation
    without performing any optional sub-operations that require taking a lock. For example, this will
    prevent git status from refreshing the index as a side effect. This is useful for processes running
    in the background which do not want to cause lock contention with other operations on the repository.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
  source_role: primary
  pass: deep
- id: F65
  part_id: A
  claim: The --no-optional-locks option makes Git skip optional operations that need locks, and is equivalent
    to setting GIT_OPTIONAL_LOCKS to 0.
  source: https://git-scm.com/docs/git
  fetched: '2026-10-27'
  quote: Do not perform optional operations that require locks.
  context: Do not perform optional operations that require locks. This is equivalent to setting the GIT_OPTIONAL_LOCKS
    to 0.
  brief_digest: 96b234909beb4706011b6ac3438c9a96e24b77ee0a5d092de7b24928d73caecb
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
- finding_id: F32
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f32
- finding_id: F33
  quote_check: fail
  verdict: missing
  worker_ref: support-f33
- finding_id: F42
  quote_check: pass
  verdict: supported
  worker_ref: support-f42
  finding_digest: 2bbebd9bfb5b30106240697c3935a925572c3b1a82fdeb08258a4c83e3e718f4
- finding_id: F43
  quote_check: pass
  verdict: supported
  worker_ref: support-f43
  finding_digest: 35c593e2d1c998aec6f7aa877bb4f041e0e62827845a58eb2ee6c44badd69b79
- finding_id: F44
  quote_check: fail
  verdict: missing
  worker_ref: support-f44
- finding_id: F45
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f45
- finding_id: F46
  quote_check: pass
  verdict: supported
  worker_ref: support-f46
  finding_digest: cc7f97acc9976b090d816504818f2ff475301e1646df04803a2fe49bc3af9b87
- finding_id: F47
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f47
- finding_id: F48
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f48
- finding_id: F49
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f49
- finding_id: F50
  quote_check: pass
  verdict: supported
  worker_ref: support-f50
  finding_digest: 5a606b1c0b61c742bf44a2ae72a760eaa9e7115258f2ed927db3ba2cd72ed97b
- finding_id: F51
  quote_check: pass
  verdict: supported
  worker_ref: support-f51
  finding_digest: ab4243bab9edb91e395139a128e510375608a910aff270fe6cebbcb229f47b17
- finding_id: F52
  quote_check: pass
  verdict: supported
  worker_ref: support-f52
  finding_digest: 4be35f8a366a303c69a90e338fca4bde3624392fe29a0ef83d1effad71315ecf
- finding_id: F53
  quote_check: pass
  verdict: supported
  worker_ref: support-f53
  finding_digest: 83fde00a9859adb27a3c367bc4d75be9ce0a14984c4b92709d98e40fda435611
- finding_id: F54
  quote_check: pass
  verdict: supported
  worker_ref: support-f54
  finding_digest: e4a592b7520250b0d72931c9d91e84bfd34e243a7a107d76e02f4bc85143326e
- finding_id: F55
  quote_check: pass
  verdict: supported
  worker_ref: support-f55
  finding_digest: 2de19fef8d7ea4e25fdb9ae20e139483dc4d4c6f1c3b56f5d7fff7a96339cceb
- finding_id: F56
  quote_check: pass
  verdict: supported
  worker_ref: support-f56
  finding_digest: 59b21d8e6d86801b4fffe1d66a1561d4271c968c41664f78aa9a8de5b30eee83
- finding_id: F57
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f57
- finding_id: F58
  quote_check: pass
  verdict: supported
  worker_ref: support-f58
  finding_digest: dcc4f74f9e3661db3e9aec1c6ae6e314863ac8f3ad931243b88c429342471a70
- finding_id: F59
  quote_check: pass
  verdict: supported
  worker_ref: support-f59
  finding_digest: b11e1b576c398c0cbe75819b332d522e7a9b9e424ba1ee90a3b4ab4d298801d0
- finding_id: F60
  quote_check: pass
  verdict: supported
  worker_ref: support-f60
- finding_id: F61
  quote_check: pass
  verdict: supported
  worker_ref: support-f61
  finding_digest: 0177447f0b700d38ca5292cea9f3462858303ff761034ca41d412482525115dd
- finding_id: F62
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f62
- finding_id: F63
  quote_check: pass
  verdict: unsupported
  worker_ref: support-f63
- finding_id: F64
  quote_check: pass
  verdict: supported
  worker_ref: support-f64
  finding_digest: ce5acadd2f9d4b36ef6e9de8aa5f44493bb388da75b1896b42d816f3579bccaa
- finding_id: F65
  quote_check: pass
  verdict: supported
  worker_ref: support-f65
  finding_digest: d50f6c649880ea9594597f6f0475770138274c53abba9116859c40a14c57efbf
drift: []
---
Findings grouped by pass and part are in the frontmatter; dropped findings are not kept.
