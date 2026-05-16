# Contributing to AI Agent Assembly

Thank you for your interest in contributing! AI Agent Assembly is an open-source project and we welcome contributions of all sizes — bug reports, documentation fixes, new features, performance improvements, and more.

This guide describes the org-wide conventions that apply across all repositories under [AI-agent-assembly](https://github.com/AI-agent-assembly). For repo-specific setup (build commands, test runners, language toolchains), see the `CONTRIBUTING.md` in each individual repo — it takes precedence over this file where they differ.

## Prerequisites

- A GitHub account
- Git installed locally
- Familiarity with the language and tooling of the repo you're contributing to
- The repo cloned locally (see each repo's README for setup steps)

## Branch naming

All feature and fix branches follow this four-part format:

```
<release-or-phase>/<ticket-number>/<type>/<short-summary>
```

- `<release-or-phase>` — milestone or sprint identifier (e.g., `v0.0.1`, `phase1`)
- `<ticket-number>` — Jira ticket reference (e.g., `AAASM-1316`)
- `<type>` — change category, one of:

  | Type | When to use |
  |---|---|
  | `feat` | New feature or capability |
  | `fix` | Bug fix |
  | `refactor` | Refactor with no behavior change |
  | `test` | Test-only change |
  | `docs` | Documentation change |
  | `config` | Configuration / CI change |
  | `deps` | Dependency upgrade |
  | `remove` | Deletion or removal |
  | `lint` | Lint or type-error fix |

- `<short-summary>` — 2–4 words in `snake_case`, max 30 characters

Example: `v0.0.1/AAASM-42/feat/add_agent_registry`
