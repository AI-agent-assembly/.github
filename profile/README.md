# AI Agent Assembly

[![Core CI](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml/badge.svg)](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Core release](https://img.shields.io/github/v/release/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/releases/latest)
[![Discussions](https://img.shields.io/badge/community-Discussions-blue?logo=github)](https://github.com/AI-agent-assembly/agent-assembly/discussions)
[![Python SDK tag](https://img.shields.io/github/v/tag/AI-agent-assembly/python-sdk?label=python-sdk)](https://github.com/AI-agent-assembly/python-sdk/tags)
[![Node SDK tag](https://img.shields.io/github/v/tag/AI-agent-assembly/node-sdk?label=node-sdk)](https://github.com/AI-agent-assembly/node-sdk/tags)
[![Go SDK tag](https://img.shields.io/github/v/tag/AI-agent-assembly/go-sdk?label=go-sdk)](https://github.com/AI-agent-assembly/go-sdk/tags)
[![Open issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/issues)
[![Open PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/pulls)
[![Last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/commits/master)

AI Agent Assembly is an open-source governance platform for AI agents. It enforces policy, tracks budget, and audits every action your agents take across three independent interception layers — in-process SDKs, a sidecar proxy, and eBPF kernel hooks — so you can ship multi-agent fleets without losing control of what they do.

## Developer Start Here

### Core + SDK repositories

| Repo | Purpose | Current state |
| --- | --- | --- |
| [agent-assembly](https://github.com/AI-agent-assembly/agent-assembly) | Core Rust monorepo: gateway, policy engine, CLI, API, dashboard | Latest release: [`v0.0.1-alpha.1`](https://github.com/AI-agent-assembly/agent-assembly/releases/tag/v0.0.1-alpha.1) |
| [python-sdk](https://github.com/AI-agent-assembly/python-sdk) | Python SDK (PyO3 native + pure-Python client) | Tagged: `v0.0.1-alpha.1` |
| [node-sdk](https://github.com/AI-agent-assembly/node-sdk) | TypeScript SDK (napi-rs native + JS client) | Tagged: `v0.0.1-alpha.1` |
| [go-sdk](https://github.com/AI-agent-assembly/go-sdk) | Go SDK | Tagged: `v0.0.1-alpha.1` |
| [agent-assembly-cloud](https://github.com/AI-agent-assembly/agent-assembly-cloud) | Cloud control plane and SaaS web/API components | Active development |
| [homebrew-agent-assembly](https://github.com/AI-agent-assembly/homebrew-agent-assembly) | Homebrew tap for `aasm` | Formula exists (`Formula/aasm.rb`) |

### Install channels

#### Homebrew (macOS, Linux)

```sh
brew install agent-assembly/tap/aasm
```

#### Python — pip, uv, or poetry

```sh
# pip
pip install agent-assembly-python

# uv
uv add agent-assembly-python

# poetry
poetry add agent-assembly-python
```

#### Node.js — pnpm (recommended), npm, or yarn

```sh
# pnpm (recommended)
pnpm add @agent-assembly/sdk

# npm
npm install @agent-assembly/sdk

# yarn
yarn add @agent-assembly/sdk
```

#### Docker

```sh
docker pull ghcr.io/agent-assembly/python:latest
```

#### curl one-line installer

```sh
curl -fsSL https://get.agentassembly.dev | sh
```

## Release and Homebrew state (2026-05-27)

- `agent-assembly` latest release: `v0.0.1-alpha.1` (pre-stable alpha channel).
- SDK repos (`python-sdk`, `node-sdk`, `go-sdk`) are tagged at `v0.0.1-alpha.1`.
- Homebrew tap has `Formula/aasm.rb` with `version "0.0.1"`, but checksum placeholders are still all zero, so this should be treated as pre-stable/bootstrap state until real release artifacts and checksums are published.

## Full Production Highlights

### Core differentiation

1. Lowest-intrusion integration: one-line init across major agent frameworks.
2. Three-layer interception: semantic to protocol to kernel, with selectable depth.
3. Secret Injection: real credentials never appear in LLM context windows.
4. Tool Execution Sandbox: isolated execution to reduce security risk.
5. Human-in-the-loop Gate: high-risk actions require human review.

### Enterprise governance

1. Agent Identity and Zero-trust A2A
2. Cost and Token Budget Governance
3. Org / Team / Agent hierarchy management
4. Audit Trail and Compliance Export

### Deployment flexibility

1. Local Dev Mode (zero-config, OSS)
2. Self-hosted Control Plane (enterprise on-prem)
3. SaaS Cloud (`agent-assembly-cloud`)

> Prioritize these three above the fold: lowest-intrusion integration, Secret Injection, and Human-in-the-loop Gate.
