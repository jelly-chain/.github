# Jelly Chain

<p align="center">
  <a href="https://github.com/jelly-chain/jelly-claude"><img src="https://img.shields.io/badge/jelly--claude-main%20agent-01696f?style=for-the-badge" alt="jelly-claude"></a>
  <a href="https://github.com/jelly-chain/SDK"><img src="https://img.shields.io/badge/SDK-multi--repo%20hub-1f2937?style=for-the-badge" alt="SDK"></a>
  <a href="https://github.com/jelly-chain/jelly-claude-skills"><img src="https://img.shields.io/badge/skills-Claude%20Code%20skills-7c3aed?style=for-the-badge" alt="skills"></a>
  <a href="https://github.com/jelly-chain/Solana"><img src="https://img.shields.io/badge/Solana-SDKs-14b8a6?style=for-the-badge" alt="Solana"></a>
  <a href="https://github.com/jelly-chain/BNB"><img src="https://img.shields.io/badge/BNB-SDKs-f59e0b?style=for-the-badge" alt="BNB"></a>
</p>

<p align="center">
  <a href="https://jellychain.fun">Website</a> - 
  <a href="https://t.me/jellyxchain">Telegram</a> - 
  <a href="https://x.com/agentz010">X</a>
</p>

> Multi-chain AI agents, SDKs, and trading infrastructure for Solana, BNB Chain, Ethereum, Base, and prediction markets.

Jelly Chain is the main GitHub home for the Jelly ecosystem, bringing together the Jelly-Claude agent, reusable SDKs, protocol skills, chain-specific tooling, and prediction market infrastructure in one place.

## What Jelly Chain includes

Jelly Chain currently publishes 6 public repositories covering the main agent launcher, a shared SDK hub, skills, agents, and chain-specific SDKs for Solana and BNB Chain.

| Repository | Focus | Stack |
|---|---|---|
| [jelly-claude](https://github.com/jelly-chain/jelly-claude) | Main multi-chain AI coding agent and launcher | TypeScript |
| [SDK](https://github.com/jelly-chain/SDK) | Shared SDK hub for agents and prediction tooling | TypeScript |
| [jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) | Installable protocol and chain skills for Claude Code | Shell |
| [jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) | Legacy agents repo, with templates now moved into the main launcher repo | Markdown |
| [Solana](https://github.com/jelly-chain/Solana) | Solana SDKs and tooling | Python / TypeScript |
| [BNB](https://github.com/jelly-chain/BNB) | BNB Chain SDKs and tooling | Python / TypeScript |

## Core repositories

### jelly-claude

[jelly-claude](https://github.com/jelly-chain/jelly-claude) is the flagship repo and the main entry point for the ecosystem. It was specifically designed for trading and prediction workflows, while also supporting broader multi-chain automation across Solana, BNB, Polygon, Ethereum, Base, DeFi, NFTs, and market infrastructure.

Highlights:
- Multi-chain wallet setup for Solana and EVM flows.
- Built-in skills and agent-template installation through the launcher.
- Trading, prediction market, DeFi, NFT, and automation support.
- Telegram bridge support through `tg-bridge.mjs`.
- Core runtime components for risk, prediction, metrics, queueing, proxy guard, voice, events, and CLI orchestration.
- Direct modules for `alerts`, `analytics`, `bridge`, `defi`, `market`, `portfolio`, `prediction-markets`, `scanner`, and `wallet`.

### SDK

The [SDK](https://github.com/jelly-chain/SDK) repo is the central hub for agent SDKs and shared infrastructure. Based on the repository structure you shared, it includes projects such as `FIFA-SDK`, `SPORT-SDK`, `Prediction-V2-main`, and `market-prediction-sdk-main`.

This repo acts as the reusable development layer for the wider Jelly ecosystem.

### jelly-claude-skills

[jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) provides installable skills for Claude Code. It is the protocol knowledge layer that helps Jelly-Claude interact with chains, DEXs, analytics sources, and prediction market tooling.

Skills are designed to give the agent protocol-specific knowledge, installers, docs, and key templates so users can extend Jelly-Claude quickly.

### jelly-claude-agents

[jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) is now mainly a pointer repo and directs users to the newer `Agent-Templates` location inside the main [jelly-claude](https://github.com/jelly-chain/jelly-claude) repository.

This keeps the current template system centered in the main launcher while preserving the original repo path.

### BNB

The [BNB](https://github.com/jelly-chain/BNB) repository contains BNB Chain SDKs, including Four.meme integrations with both Python and TypeScript implementations based on the repository layout you shared.

This repo supports BNB-native automation, token flows, and chain-specific SDK use cases.

### Solana

The [Solana](https://github.com/jelly-chain/Solana) repository contains Solana-focused SDKs and examples, including a Pump.fun SDK with both Python and TypeScript implementations.

Its Pump.fun tooling is centered on four main actions: `launch`, `buyback`, `lock`, and `claimFees`.

## Agent foundation

The Jelly-Claude agent layer is built on top of [TentacleOS/buddy](https://github.com/TentacleOS/buddy), which you described as a lighter version of [nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw).

Prediction Jelly:
- BNB: `0xf581ee357f11d7478fafd183b4a41347c35a4444`
- SOL: `0xf581ee357f11d7478fafd183b4a41347c35a4444` 
- ETH: `0x871d46dc15fa55d5bb9e912e56bcedccd53acccc`
- BASE: `0xa7826e1d387a59d8e9710799f6cd100027421b07`

Related references:
- Buddy base: [TentacleOS/buddy](https://github.com/TentacleOS/buddy)  CA: SOON
- NanoClaw: [nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw)  CA: `AMg3mkZXNf8Aw8Eu8NCh92DWk7Qahi1jtXc3SDPiqBqU`



## Ecosystem focus

Jelly Chain is built around a practical multi-chain stack:
- AI coding agents and launch wrappers.
- Reusable SDKs for market, prediction, and trading workflows.
- Protocol skills for Claude Code.
- Solana and BNB chain-specific SDKs.
- Prediction market infrastructure and trader automation.
- Telegram-accessible workflows and terminal-first tooling.

## Links

- Website: [jellychain.fun](https://jellychain.fun)
- Telegram: [t.me/jellyxchain](https://t.me/jellyxchain)
- X: [x.com/agentz010](https://x.com/agentz010)
- Main org: [github.com/jelly-chain](https://github.com/jelly-chain)
- Main agent: [github.com/jelly-chain/jelly-claude](https://github.com/jelly-chain/jelly-claude)
- SDK hub: [github.com/jelly-chain/SDK](https://github.com/jelly-chain/SDK)
- Skills: [github.com/jelly-chain/jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills)
- Agents: [github.com/jelly-chain/jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents)
- Solana SDKs: [github.com/jelly-chain/Solana](https://github.com/jelly-chain/Solana)
- BNB SDKs: [github.com/jelly-chain/BNB](https://github.com/jelly-chain/BNB)

## Quick start path

For most users, the best entry point is [jelly-claude](https://github.com/jelly-chain/jelly-claude), then install skills, use the bundled agent templates, and expand into the Solana, BNB, and SDK repositories as needed.

```bash
git clone https://github.com/jelly-chain/jelly-claude
cd jelly-claude
bash setup.sh
```

## Notes

- `jelly-claude` is the main front door for the ecosystem.
- `SDK` acts as the shared infrastructure layer.
- `jelly-claude-skills` adds protocol intelligence.
- `jelly-claude-agents` points to the newer in-repo templates structure.
- `Solana` and `BNB` provide chain-specific SDK implementations.
- `ink-ui` is worth highlighting as part of the terminal UX story, but it should be shown as documentation or media in README rather than executable UI.
