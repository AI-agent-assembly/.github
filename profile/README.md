# AI Agent Assembly

[![Core CI](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml/badge.svg)](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Core release](https://img.shields.io/github/v/release/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/releases/latest)
[![Discussions](https://img.shields.io/badge/community-Discussions-blue?logo=github)](https://github.com/AI-agent-assembly/agent-assembly/discussions)

AI Agent Assembly is an open-source governance platform for AI agents. It enforces policy, tracks budget, and audits every action your agents take across three independent interception layers — in-process SDKs, a sidecar proxy, and eBPF kernel hooks — so you can ship multi-agent fleets without losing control of what they do.

## Developer Start Here

### Repository Status

| Repo | Purpose | Version | Base branch health | Activity |
| --- | --- | --- | --- | --- |
| [![agent-assembly](https://img.shields.io/badge/agent--assembly-core-000000?logo=rust)](https://github.com/AI-agent-assembly/agent-assembly) | Core Rust monorepo: gateway, policy engine, CLI, API, dashboard | [![release](https://img.shields.io/github/v/release/AI-agent-assembly/agent-assembly?label=release&logo=github)](https://github.com/AI-agent-assembly/agent-assembly/releases/latest) | [![CI](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly?label=issues)](https://github.com/AI-agent-assembly/agent-assembly/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly?label=PRs)](https://github.com/AI-agent-assembly/agent-assembly/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly?label=last)](https://github.com/AI-agent-assembly/agent-assembly/commits/master) |
| [![python-sdk](https://img.shields.io/badge/python--sdk-SDK-3776AB?logo=python&logoColor=white)](https://github.com/AI-agent-assembly/python-sdk) | Python SDK (PyO3 native + pure-Python client) | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/python-sdk?label=tag&logo=python)](https://github.com/AI-agent-assembly/python-sdk/tags) | [![CI](https://github.com/AI-agent-assembly/python-sdk/actions/workflows/ci.yaml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/python-sdk/actions/workflows/ci.yaml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/python-sdk?label=issues)](https://github.com/AI-agent-assembly/python-sdk/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/python-sdk?label=PRs)](https://github.com/AI-agent-assembly/python-sdk/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/python-sdk?label=last)](https://github.com/AI-agent-assembly/python-sdk/commits/master) |
| [![node-sdk](https://img.shields.io/badge/node--sdk-SDK-339933?logo=node.js&logoColor=white)](https://github.com/AI-agent-assembly/node-sdk) | TypeScript SDK (napi-rs native + JS client) | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/node-sdk?label=tag&logo=npm)](https://github.com/AI-agent-assembly/node-sdk/tags) | [![Tests](https://github.com/AI-agent-assembly/node-sdk/actions/workflows/test-matrix.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/node-sdk/actions/workflows/test-matrix.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/node-sdk?label=issues)](https://github.com/AI-agent-assembly/node-sdk/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/node-sdk?label=PRs)](https://github.com/AI-agent-assembly/node-sdk/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/node-sdk?label=last)](https://github.com/AI-agent-assembly/node-sdk/commits/master) |
| [![go-sdk](https://img.shields.io/badge/go--sdk-SDK-00ADD8?logo=go&logoColor=white)](https://github.com/AI-agent-assembly/go-sdk) | Go SDK | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/go-sdk?label=tag&logo=go)](https://github.com/AI-agent-assembly/go-sdk/tags) | [![Go test](https://github.com/AI-agent-assembly/go-sdk/actions/workflows/go-test.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/go-sdk/actions/workflows/go-test.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/go-sdk?label=issues)](https://github.com/AI-agent-assembly/go-sdk/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/go-sdk?label=PRs)](https://github.com/AI-agent-assembly/go-sdk/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/go-sdk?label=last)](https://github.com/AI-agent-assembly/go-sdk/commits/master) |
| [![.github](https://img.shields.io/badge/.github-org--profile-181717?logo=github)](https://github.com/AI-agent-assembly/.github) | Organization profile, templates, support, and community files | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/.github?label=tag&logo=github)](https://github.com/AI-agent-assembly/.github/tags) | [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/.github?label=last)](https://github.com/AI-agent-assembly/.github/commits/master) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/.github?label=issues)](https://github.com/AI-agent-assembly/.github/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/.github?label=PRs)](https://github.com/AI-agent-assembly/.github/pulls) |
| [![homebrew-agent-assembly](https://img.shields.io/badge/homebrew--agent--assembly-tap-FBB040?logo=homebrew&logoColor=black)](https://github.com/AI-agent-assembly/homebrew-agent-assembly) | Homebrew tap for `aasm` | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/homebrew-agent-assembly?label=tag&logo=homebrew)](https://github.com/AI-agent-assembly/homebrew-agent-assembly/tags) | [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/homebrew-agent-assembly?label=last)](https://github.com/AI-agent-assembly/homebrew-agent-assembly/commits/master) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/homebrew-agent-assembly?label=issues)](https://github.com/AI-agent-assembly/homebrew-agent-assembly/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/homebrew-agent-assembly?label=PRs)](https://github.com/AI-agent-assembly/homebrew-agent-assembly/pulls) |
| [![agent-assembly-docs](https://img.shields.io/badge/agent--assembly--docs-docs-4051B5?logo=materialformkdocs&logoColor=white)](https://github.com/AI-agent-assembly/agent-assembly-docs) | Public documentation site | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/agent-assembly-docs?label=tag&logo=github)](https://github.com/AI-agent-assembly/agent-assembly-docs/tags) | [![Deploy](https://github.com/AI-agent-assembly/agent-assembly-docs/actions/workflows/deploy.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/agent-assembly-docs/actions/workflows/deploy.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly-docs?label=issues)](https://github.com/AI-agent-assembly/agent-assembly-docs/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly-docs?label=PRs)](https://github.com/AI-agent-assembly/agent-assembly-docs/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly-docs?label=last)](https://github.com/AI-agent-assembly/agent-assembly-docs/commits/master) |
| [![agent-assembly-spec](https://img.shields.io/badge/agent--assembly--spec-spec-6E40C9?logo=openapiinitiative&logoColor=white)](https://github.com/AI-agent-assembly/agent-assembly-spec) | Shared specifications and protocol contracts | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/agent-assembly-spec?label=tag&logo=github)](https://github.com/AI-agent-assembly/agent-assembly-spec/tags) | [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly-spec?label=last)](https://github.com/AI-agent-assembly/agent-assembly-spec/commits/master) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly-spec?label=issues)](https://github.com/AI-agent-assembly/agent-assembly-spec/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly-spec?label=PRs)](https://github.com/AI-agent-assembly/agent-assembly-spec/pulls) |
| [![agent-assembly-cloud](https://img.shields.io/badge/agent--assembly--cloud-private-111827?logo=fastapi&logoColor=white)](https://github.com/AI-agent-assembly/agent-assembly-cloud) | Cloud control plane and SaaS web/API components | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/agent-assembly-cloud?label=tag&logo=github)](https://github.com/AI-agent-assembly/agent-assembly-cloud/tags) | [![API](https://github.com/AI-agent-assembly/agent-assembly-cloud/actions/workflows/api.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/agent-assembly-cloud/actions/workflows/api.yml?query=branch%3Amaster) [![FE](https://github.com/AI-agent-assembly/agent-assembly-cloud/actions/workflows/fe.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/agent-assembly-cloud/actions/workflows/fe.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly-cloud?label=issues)](https://github.com/AI-agent-assembly/agent-assembly-cloud/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly-cloud?label=PRs)](https://github.com/AI-agent-assembly/agent-assembly-cloud/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly-cloud?label=last)](https://github.com/AI-agent-assembly/agent-assembly-cloud/commits/master) |
| [![agent-assembly-enterprise](https://img.shields.io/badge/agent--assembly--enterprise-private-7A1FA2?logo=rust&logoColor=white)](https://github.com/AI-agent-assembly/agent-assembly-enterprise) | Enterprise gateway and private enterprise features | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/agent-assembly-enterprise?label=tag&logo=github)](https://github.com/AI-agent-assembly/agent-assembly-enterprise/tags) | [![CI](https://github.com/AI-agent-assembly/agent-assembly-enterprise/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/agent-assembly-enterprise/actions/workflows/ci.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/agent-assembly-enterprise?label=issues)](https://github.com/AI-agent-assembly/agent-assembly-enterprise/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/agent-assembly-enterprise?label=PRs)](https://github.com/AI-agent-assembly/agent-assembly-enterprise/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/agent-assembly-enterprise?label=last)](https://github.com/AI-agent-assembly/agent-assembly-enterprise/commits/master) |
| [![inner-document](https://img.shields.io/badge/inner--document-private-455A64?logo=readthedocs&logoColor=white)](https://github.com/AI-agent-assembly/inner-document) | Private internal documentation and runbooks | [![tag](https://img.shields.io/github/v/tag/AI-agent-assembly/inner-document?label=tag&logo=github)](https://github.com/AI-agent-assembly/inner-document/tags) | [![CI](https://github.com/AI-agent-assembly/inner-document/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/AI-agent-assembly/inner-document/actions/workflows/ci.yml?query=branch%3Amaster) | [![issues](https://img.shields.io/github/issues/AI-agent-assembly/inner-document?label=issues)](https://github.com/AI-agent-assembly/inner-document/issues) [![PRs](https://img.shields.io/github/issues-pr/AI-agent-assembly/inner-document?label=PRs)](https://github.com/AI-agent-assembly/inner-document/pulls) [![last commit](https://img.shields.io/github/last-commit/AI-agent-assembly/inner-document?label=last)](https://github.com/AI-agent-assembly/inner-document/commits/master) |

Private repository badges require GitHub access to the organization.

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

## Release and Homebrew Notes

- `agent-assembly` is currently in a pre-stable alpha channel.
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
