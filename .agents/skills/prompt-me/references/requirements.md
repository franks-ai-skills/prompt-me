# Requirements

Accepted for this skill (part A's requirements sha256 2fa0d4f50d8d6824cc43d8385bf488bc9081a8e23fcfdb2a4bc28ad3064ea892). Forge's
verification checks the skill against each one. Numbers match the
requirements in SKILL.md; each line gives the rule id, its kind and its
sources.

1. `idea.well-defined-prompt.a.untrusted-block` (must): https://genai.owasp.org/llmrisk/llm01-prompt-injection/, https://arxiv.org/abs/2403.14720
2. `idea.well-defined-prompt.a.no-fetched-instructions` (must not): https://invariantlabs.ai/blog/mcp-github-vulnerability, https://genai.owasp.org/llmrisk/llm01-prompt-injection/
3. `idea.well-defined-prompt.a.read-only-allowlist` (must): https://genai.owasp.org/llmrisk/llm01-prompt-injection/
4. `idea.well-defined-prompt.a.git-no-optional-locks` (should): https://git-scm.com/docs/git
5. `idea.well-defined-prompt.a.issues-untrusted-any-owner` (must): https://invariantlabs.ai/blog/mcp-github-vulnerability
6. `idea.well-defined-prompt.a.tmp-gitignore` (must): https://git-scm.com/docs/gitignore
7. `idea.well-defined-prompt.a.tracked-drafts-note` (should): https://git-scm.com/docs/gitignore
