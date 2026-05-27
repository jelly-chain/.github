<div align="center">

<pre>
     ██╗███████╗██╗     ██╗  ██╗   ██╗  ██████╗ ███████╗
     ██║██╔════╝██║     ██║  ╚██╗ ██╔╝ ██╔═══██╗██╔════╝
     ██║█████╗  ██║     ██║   ╚████╔╝  ██║   ██║███████╗
██   ██║██╔══╝  ██║     ██║    ╚██╔╝   ██║   ██║╚════██║
╚█████╔╝███████╗███████╗███████╗██║    ╚██████╔╝███████║
 ╚════╝ ╚══════╝╚══════╝╚══════╝╚═╝     ╚═════╝ ╚══════╝
</pre>


[![npm](https://img.shields.io/npm/v/@jellyos/agent?color=14b8a6&style=flat-square)](https://www.npmjs.com/package/@jellyos/agent)
[![Node](https://img.shields.io/badge/node-%3E%3D20-brightgreen?style=flat-square)](https://nodejs.org)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)](LICENSE)

[Website](http://jelly-os.xyz/) • [Telegram](https://t.me/jellyxchain) • [X / Twitter](https://x.com/agentz010) • [API](https://jellychain.fun) •
[Claude Wrapper](https://github.com/jelly-chain/jelly-claude) • [PI Extention](https://github.com/jelly-chain/jellyOS-PI-Framework) • [NPM](https://www.npmjs.com/package/@jellyos/agent) • [NPM Docs](https://github.com/jelly-chain/JellyOS-NPM)

</div>
    
 <p align="center">  
  <a href="https://github.com/jelly-chain/Solana">
    <img src="https://img.shields.io/badge/Solana-SDKs-14b8a6?style=for-the-badge" alt="Solana SDKs">
  </a>
  <a href="https://github.com/jelly-chain/BNB">
    <img src="https://img.shields.io/badge/BNB-SDKs-f59e0b?style=for-the-badge" alt="BNB SDKs">
  </a>
</p>



---

Multi-chain AI agents, SDKs, and trading infrastructure for Solana, BNB Chain, Ethereum, Base, and prediction markets.  
Jelly Chain is the main GitHub home for the Jelly ecosystem, bringing together the Jelly-Claude agent, reusable SDKs, protocol skills, chain-specific tooling, and prediction market infrastructure in one place.


## What Jelly Chain includes

Jelly Chain currently publishes 6 public repositories covering the main agent launcher, a shared SDK hub, skills, agents, and chain-specific SDKs for Solana and BNB Chain.

| Repository | Focus | Stack |
| --- | --- | --- |
| [jellyOS](https://github.com/jelly-chain/jellyos) | Main CLI and agent with it's own launcher | js |
| [jelly-claude](https://github.com/jelly-chain/jelly-claude) | Main multi-chain AI coding agent and launcher | TypeScript |
| [SDK](https://github.com/jelly-chain/SDK) | Shared SDK hub for agents and prediction tooling | TypeScript |
| [jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) | Installable protocol and chain skills for Claude Code | Shell |
| [jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) | Legacy agents repo, templates now live in the main launcher repo | Markdown |
| [Solana](https://github.com/jelly-chain/Solana) | Solana SDKs and tooling | Python / TypeScript |
| [BNB](https://github.com/jelly-chain/BNB) | BNB Chain SDKs and tooling | Python / TypeScript |

---

## Core repositories

### jelly-claude

[jelly-claude](https://github.com/jelly-chain/jelly-claude) is the flagship repo and the main entry point for the ecosystem. It is specifically designed for trading and prediction workflows, while also supporting broader multi-chain automation across Solana, BNB, Polygon, Ethereum, Base, DeFi, NFTs, and market infrastructure.

**Highlights**

- Multi-chain wallet setup for Solana and EVM flows (BNB, Polygon, Ethereum, Base).
- Built-in skills and agent-template installation through the launcher.
- Trading, prediction market, DeFi, NFT, and automation support across multiple protocols.
- Telegram bridge via `tg-bridge.mjs` for remote control and monitoring.
- Core runtime components for:
  - Risk management (`risk.mjs`)
  - Prediction logic (`prediction.mjs`)
  - Metrics and observability (`metrics.mjs`)
  - Queueing and retries (`queue.mjs`, `retry.mjs`)
  - Proxy guard and safety (`proxy-guard.mjs`)
  - Events and notifications (`events.mjs`, `notify.mjs`)
  - Voice and audio workflows (`voice-*.mjs`, `voice-daemon.mjs`, `voice-auto-poller.mjs`)
  - Filesystem and environment protection (`fs.mjs`, `fs-guard.mjs`, `env.mjs`)
- A terminal interface layer built around `core/splash.mjs` and `core/ink-ui` (React Ink-based CLI UI).

#### Modules (v2)

Jelly-Claude exposes a modular CLI layer under `modules/`, so many workflows can run without an active Claude session:

- `modules/market`: signal prediction, backtesting, and Jelly Score computation.
- `modules/portfolio`: multi-chain portfolio snapshots and P&L.
- `modules/scanner`: new token discovery, volume/TVL spikes, and trend scans.
- `modules/alerts`: alert pipeline and status.
- `modules/analytics`: deeper analytics and cross-chain metrics.
- `modules/prediction-markets`: Polymarket/Kalshi/predict.fun workflows.
- `modules/wallet`: wallet-level operations and checks.
- `modules/defi`: DeFi yield search and TVL tracking.
- `modules/bridge`: bridge fee and route comparison.

Example usage:

```bash
node modules/market/run.mjs predict --text "Solana TVL surge breakout" --chain solana
node modules/scanner/run.mjs newTokens --chain bsc --maxAge 30
node modules/prediction-markets/run.mjs polymarkets --limit 10
node modules/portfolio/run.mjs snapshot --solana <your-solana-address>
```

---

### SDK

The [SDK](https://github.com/jelly-chain/SDK) repo is the central hub for agent SDKs and shared infrastructure. It provides a unified place to maintain SDKs used by Jelly-Claude and external agents, including:

- `FIFA-SDK` – football / sports-oriented SDK components.
- `SPORT-SDK` – broader sports prediction tooling.
- `Prediction-V2-main` – upgraded prediction engine and APIs.
- `market-prediction-sdk-main` – market prediction infrastructure for production deployments.

The SDK repo acts as the reusable development layer for building and scaling prediction, trading, and sports/market agents.

---

### jelly-claude-skills

[jelly-claude-skills](https://github.com/jelly-chain/jelly-claude-skills) provides installable skills for Claude Code and acts as the protocol knowledge layer that enables Jelly-Claude to interact with chains, DEXs, analytics sources, and prediction market tooling.

**Key points**

- 20+ skills across Solana, BNB, Base, Hyperliquid, Polymarket, Kalshi, Birdeye, DexScreener, and jellychain.fun analytics.
- Each skill includes:
  - `SKILL.md` – knowledge base for Claude Code.
  - `install.sh` / `install.ps1` – installers for macOS/Linux and Windows.
  - `README.md` – documentation and usage examples.
  - `.keys.example` – key template (actual keys are gitignored).

**Examples**

- Prediction skills: `prediction-skill`, `polymarket-skill`, `kalshi-skill`.
- Wallet/trading skills: `solana-wallet-skill`, `bnb-wallet-skill`, `solana-trading-skill`, `bnb-trading-skill`.
- Solana Foundation skills: `solana-common-errors`, `solana-security-checklist`, `solana-frontend-kit`, and more.
- Analytics skills: `birdeye-skill`, `dexscreener-skill`, `jelly-skill`.

Install skills:

```bash
# Install all skills
bash install-all.sh       # Mac / Linux
.\install-all.ps1         # Windows PowerShell

# Install a single skill
bash skills/jupiter-skill/install.sh
```

---

### jelly-claude-agents

[jelly-claude-agents](https://github.com/jelly-chain/jelly-claude-agents) is a legacy agents repo that now serves mainly as a pointer to the `Agent-Templates` folder inside the main [jelly-claude](https://github.com/jelly-chain/jelly-claude) repository.

Agent templates define ready-made strategy profiles, such as:

- Prediction market traders (Polymarket, Kalshi, predict.fun).
- DEX traders (Jupiter, Raydium, Pump.fun, PancakeSwap).
- DeFi yield optimizers.
- NFT flippers and whale trackers.
- Cross-exchange arbitrage and portfolio rebalancers.
- Risk-guarded and score-based strategies.

Templates can be installed via the Jelly-Claude npm scripts and invoked inside Claude Code using `/agent <name>`.



---
## Deploy on-chain Tokens & Agents 

Soon



---

## Give agents On-chain Identities 

Soon

----



### BNB

The [BNB](https://github.com/jelly-chain/BNB) repository contains BNB Chain SDKs, including Four.meme integrations with both Python and TypeScript implementations.

**Focus**

- Four.meme SDKs for BNB Chain:
  - TypeScript (e.g. `@jellychain/fourmeme-sdk`).
  - Python (`jellychain-fourmeme-sdk`).
- Tools for:
  - Deploying and managing tokens via Four.meme.
  - Building automated trading/launch flows on BNB.
  - Integrating with BNB-native DEXs and on-chain data.

This repo supports BNB-native automation, token flows, and chain-specific SDK use cases.

---

### Solana

The [Solana](https://github.com/jelly-chain/Solana) repository contains Solana-focused SDKs and examples, including a Pump.fun SDK with both Python and TypeScript implementations.

**Pump.fun SDK**

- TypeScript / Node.js: `@jellychain/pumpfun-sdk`.
- Python: `jellychain-pumpfun-sdk`.

Capabilities:

- `launch` – deploy a new Pump.fun token with metadata, IPFS upload, and optional dev-buy.
- `buyback` – buy tokens from the bonding curve with a specified SOL amount.
- `lock` – burn/renounce dev allocation to signal long-term commitment.
- `claimFees` – collect and distribute accumulated Pump.fun creator fees.

This repo is the chain-native SDK layer for Solana memecoin and creator workflows.

---

## Prediction Jelly contracts

Official contract addresses for the Prediction Jelly token across chains:

- **BNB**: `0xf581ee357f11d7478fafd183b4a41347c35a4444`
- **SOL**: `GcUANCt1YZK9L8ap128EMrcbhNMYhHR23Ungwd7ypump`
- **ETH**: `0x871d46dc15fa55d5bb9e912e56bcedccd53acccc`
- **BASE**: `0xA7826E1d387A59d8E9710799f6cD100027421b07`

---

## Agent foundation

The Jelly-Claude agent layer is built on top of [TentacleOS/buddy](https://github.com/TentacleOS/buddy), a lighter agent framework inspired by [nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw).

This foundation provides:

- A modular, container-friendly runtime for multi-agent flows.
- Robust process and error handling.
- Extensibility for custom skills, transports, and chains.

**NanoClaw reference**

- NanoClaw: https://github.com/nanocoai/nanoclaw  


---

## Ink UI

Jelly-Claude includes an `ink-ui` component under `core/ink-ui`, built with [Ink](https://github.com/vadimdemedes/ink), a React-based framework for interactive command-line apps.

GitHub READMEs are static Markdown, so the Ink UI does not run on this page, but the repo showcases:

- A terminal-first UX with live status, logs, and prompts.
- CLI dashboards for agent status, wallets, scores, and alerts.
- A richer UI layer for running trading and prediction workflows than a plain Node process.

Screenshots, GIFs, and usage examples can be added in the `jelly-claude` README to demonstrate the Ink UI experience.

---

## Ecosystem focus

Jelly Chain is built around a practical multi-chain stack:

- AI coding agents and launch wrappers (Jelly-Claude).
- Reusable SDKs for market, prediction, and trading workflows (SDK repo).
- Protocol skills for Claude Code (jelly-claude-skills).
- Solana and BNB chain-specific SDKs (Solana and BNB repos).
- Prediction market infrastructure and trader automation (Polymarket, Kalshi, predict.fun).
- Telegram-accessible workflows and terminal-first UX (tg-bridge + Ink UI).




## Quick start path

For most users, the best entry point is the main Jelly-Claude agent. After cloning the repo, install skills, use the bundled agent templates, and expand into the Solana, BNB, and SDK repositories as needed.

```bash
git clone https://github.com/jelly-chain/jelly-claude
cd jelly-claude
bash setup.sh
```

From there:

- Configure API keys (`.env` for Anthropic/OpenRouter, prediction markets, analytics).
- Install skills: `npm run install-skills`
- Install agents: `npm run install-agents`
- Launch the agent: `npm start` or `bash jelly-claude.sh`
- Optionally enable Telegram control with `--telegram`.

---

## Links

- Website: https://jellychain.fun  
- Telegram: https://t.me/jellyxchain  
- X: https://x.com/agentz010  
- Main org: https://github.com/jelly-chain  
- Main agent: https://github.com/jelly-chain/jelly-claude  
- SDK hub: https://github.com/jelly-chain/SDK  
- Skills: https://github.com/jelly-chain/jelly-claude-skills  
- Agents: https://github.com/jelly-chain/jelly-claude-agents  
- Solana SDKs: https://github.com/jelly-chain/Solana  
- BNB SDKs: https://github.com/jelly-chain/BNB  
