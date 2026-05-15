# AI Agent Assembly

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
