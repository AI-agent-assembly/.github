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

## Commit messages

Commits use [Gitmoji](https://gitmoji.dev/) format with a scope and imperative summary:

```
<emoji> (<scope>): <imperative summary>
```

Examples:

- `✨ (gateway): Add /v1/capability/matrix endpoint`
- `🐛 (auth): Fix token expiry check using UTC`
- `♻️ (proxy): Extract MitM handler into a separate module`

Keep each commit small and **bisectable** — one logical change per commit. If you need two sentences to describe a commit, split it into two.

### GitEmoji reference

| Emoji | Scope |
|---|---|
| `✨` | New feature |
| `🐛` | Bug fix |
| `♻️` | Refactor |
| `✅` | Tests |
| `📝` | Documentation |
| `🔧` | Configuration / CI |
| `⬆️` | Dependency upgrade |
| `🗑️` | Removal |
| `🚨` | Lint / type-error fix |
| `🎉` | Initial commit |

## Pull Requests

### Title

```
[<ticket>] <emoji> (<scope>): <imperative summary>
```

Example: `[AAASM-42] ✨ (gateway): Add /v1/capability/matrix endpoint`

### Description

Each repo provides a `.github/PULL_REQUEST_TEMPLATE.md`. Fill it out completely; at minimum the description must include:

- **What changed** — one short paragraph
- **Why** — motivation, context, ticket link
- **How to verify** — manual steps or test reference
- **Related issues** — ticket and any related GitHub issues

### Base branch

PRs always target `master`, even when your branch was created from another feature branch.

### Scope

Keep PRs focused. One concern per PR — don't bundle unrelated changes. If a single ticket needs more than ~500 lines of diff, split it into a sequence of stacked PRs.

## Code review

- At least **one approval** is required before merge.
- Address every reviewer comment before requesting re-review.
- Don't force-push during an active review (only allowed when rebasing onto the latest base branch — never to rewrite review history).
- CI must be green before merge. Don't bypass with `--no-verify` or by disabling checks.
- The reviewer or assignee picks the merge strategy (typically squash or rebase). The repo's default reflects the team's preference.
