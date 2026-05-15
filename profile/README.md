# AI Agent Assembly

[![CI](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml/badge.svg)](https://github.com/AI-agent-assembly/agent-assembly/actions/workflows/ci.yml)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Latest release](https://img.shields.io/github/v/release/AI-agent-assembly/agent-assembly)](https://github.com/AI-agent-assembly/agent-assembly/releases/latest)

AI Agent Assembly is an open-source governance platform for AI agents. It enforces policy, tracks budget, and audits every action your agents take across three independent interception layers — in-process SDKs, a sidecar proxy, and eBPF kernel hooks — so you can ship multi-agent fleets without losing control of what they do.

## Quick Start

### Homebrew (macOS, Linux)

```sh
brew install agent-assembly/tap/aasm
```

### Python — pip, uv, or poetry

```sh
# pip
pip install agent-assembly-python

# uv
uv add agent-assembly-python

# poetry
poetry add agent-assembly-python
```

### Node.js — pnpm (recommended), npm, or yarn

```sh
# pnpm (recommended)
pnpm add @agent-assembly/sdk

# npm
npm install @agent-assembly/sdk

# yarn
yarn add @agent-assembly/sdk
```

### Docker

```sh
docker pull ghcr.io/agent-assembly/python:latest
```

### curl one-line installer

```sh
curl -fsSL https://get.agentassembly.dev | sh
```

## Repositories

- [agent-assembly](https://github.com/AI-agent-assembly/agent-assembly) — Core Rust monorepo: gateway, policy engine, three-layer interception, CLI, API, dashboard
- [python-sdk](https://github.com/AI-agent-assembly/python-sdk) — Python SDK (PyO3 native + pure-Python client)
- [node-sdk](https://github.com/AI-agent-assembly/node-sdk) — TypeScript SDK (napi-rs native + JS client)
- [go-sdk](https://github.com/AI-agent-assembly/go-sdk) — Go SDK
