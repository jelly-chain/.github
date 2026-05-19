# Jelly Chain

<p align="center">
  <a href="https://github.com/jelly-chain/jelly-claude"><img src="https://img.shields.io/badge/jelly--claude-main%20agent-01696f?style=for-the-badge" alt="jelly-claude"></a>
  <a href="https://github.com/jelly-chain/SDK"><img src="https://img.shields.io/badge/SDK-multi--repo%20hub-1f2937?style=for-the-badge" alt="SDK"></a>
  <a href="https://github.com/jelly-chain/jelly-claude-skills"><img src="https://img.shields.io/badge/skills-Claude%20Code%20skills-7c3aed?style=for-the-badge" alt="skills"></a>
  <a href="https://github.com/jelly-chain/Solana"><img src="https://img.shields.io/badge/Solana-SDKs-14b8a6?style=for-the-badge" alt="Solana"></a>
  <a href="https://github.com/jelly-chain/BNB"><img src="https://img.shields.io/badge/BNB-SDKs-f59e0b?style=for-the-badge" alt="BNB"></a>
</p>

<p align="center">
  <a href="https://jellychain.fun">Website</a> •
  <a href="https://t.me/jellyxchain">Telegram</a> •
  <a href="https://x.com/agentz010">X</a>
</p>

> Multi-chain AI agents, SDKs, and trading infrastructure for Solana, BNB Chain, Ethereum, Base, and prediction markets.

Jelly Chain is the main GitHub home for the Jelly ecosystem, bringing together the Jelly-Claude AI agent, reusable SDKs, protocol skills, chain-specific tooling, and prediction market infrastructure in one place.

## What Jelly Chain includes

Jelly Chain publishes 6 public repositories covering the main agent launcher, a shared SDK hub, skills, agents, and chain-specific SDKs for Solana and BNB Chain.[web:1]

| Repository | Focus | Stack |
|---|---|---|
| [jelly-claude](https://github.com/jelly-chain/jelly-claude) | Main multi-chain AI coding agent and launcher | TypeScript |
| [SDK](https://github.com/jelly-chain/SDK) | Shared SDK hub for agents and prediction tooling | TypeScript |
| [jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) | Installable protocol and chain skills for Claude Code | Shell |
| [jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) | Legacy agents repo, now pointing to the in-repo templates | Markdown |
| [Solana](https://github.com/jelly-chain/Solana) | Solana SDKs and tooling | Python / TypeScript |
| [BNB](https://github.com/jelly-chain/BNB) | BNB Chain SDKs and tooling | Python / TypeScript |

## Core repositories

### jelly-claude

[jelly-claude](https://github.com/jelly-chain/jelly-claude) is the flagship repo: a multi-chain AI coding agent built around Claude Code with first-class support for trading and prediction flows across Solana, BNB, Polygon, Ethereum, Base, Polymarket, Kalshi, predict.fun, DeFi, NFTs, and more.

Key features:
- Multi-chain wallet setup for Solana and EVM flows.
- Built-in skills and agent-template installation through the launcher.
- Trading, prediction market, DeFi, NFT, and automation workflows.
- Telegram bridge via `tg-bridge.mjs` for remote control.
- Core runtime components for risk, prediction, metrics, queueing, proxy guard, events, voice, and CLI orchestration.
- Standalone modules for `alerts`, `analytics`, `bridge`, `defi`, `market`, `portfolio`, `prediction-markets`, `scanner`, and `wallet`.

### SDK

The [SDK](https://github.com/jelly-chain/SDK) repo is the central hub for agent SDKs and shared infrastructure, including packages like `FIFA-SDK`, `SPORT-SDK`, `Prediction-V2-main`, and `market-prediction-sdk-main`.

It acts as the reusable development layer powering production prediction and trading workflows.

### jelly-claude-skills

[jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) provides installable skills for Claude Code — 27+ skills covering Solana, BNB, Base, Hyperliquid, Polymarket, Kalshi, Birdeye, DexScreener, jellychain.fun analytics, and more.

Skills give the agent protocol-specific knowledge, installers, docs, and key templates so Jelly-Claude gains deep, structured expertise with a single install.

### jelly-claude-agents

[jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) preserves the legacy agents repo and now redirects users to the `Agent-Templates` folder inside the main [jelly-claude](https://github.com/jelly-chain/jelly-claude) repository.

Agent templates define ready-made strategies for prediction markets, DEX trading, DeFi yield, NFT flipping, arbitrage, and monitoring.

### BNB

The [BNB](https://github.com/jelly-chain/BNB) repository ships BNB Chain SDKs, including Four.meme integrations in both Python and TypeScript for automated token and trading flows.

It is the chain-native SDK layer for BNB-specific bots and infra.

### Solana

The [Solana](https://github.com/jelly-chain/Solana) repository ships Solana-focused SDKs and examples, including a Pump.fun SDK with both Python and TypeScript implementations.[web:1]

Pump.fun tooling exposes four core actions — `launch`, `buyback`, `lock`, and `claimFees` — for building full memecoin/creator workflows on Solana.

## Agent foundation

The Jelly-Claude agent layer is built on top of [TentacleOS/buddy](https://github.com/TentacleOS/buddy), a lighter agent framework inspired by [nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw).[web:49]

Prediction Jelly contract addresses:

- BNB: `0xf581ee357f11d7478fafd183b4a41347c35a4444`
- SOL: `GcUANCt1YZK9L8ap128EMrcbhNMYhHR23Ungwd7ypump`
- ETH: `0x871d46dc15fa55d5bb9e912e56bcedccd53acccc`
- BASE: `0xA7826E1d387A59d8E9710799f6cD100027421b07`

Related references:

- Buddy base: [TentacleOS/buddy](https://github.com/TentacleOS/buddy) (CA: coming soon)
- NanoClaw: [nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw) (CA: `AMg3mkZXNf8Aw8Eu8NCh92DWk7Qahi1jtXc3SDPiqBqU`)

---

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
- Main org: [github.com/jelly-chain](https://github.com/jelly-chain)[web:1]
- Main agent: [github.com/jelly-chain/jelly-claude](https://github.com/jelly-chain/jelly-claude)
- SDK hub: [github.com/jelly-chain/SDK](https://github.com/jelly-chain/SDK)
- Skills: [github.com/jelly-chain/jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills)[web:46]
- Agents: [github.com/jelly-chain/jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents)
- Solana SDKs: [github.com/jelly-chain/Solana](https://github.com/jelly-chain/Solana)
- BNB SDKs: [github.com/jelly-chain/BNB](https://github.com/jelly-chain/BNB)
