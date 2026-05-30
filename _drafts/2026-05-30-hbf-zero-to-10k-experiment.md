---
title: "I Gave an AI Agent $0 and Told It to Make $10,000"
description: "An autonomous AI agent using Hands Body and Feet MCP starts with zero capital and 180 days to earn $10,000 — with no human intervention. Here's the architecture, the vehicles, and the first public dashboard."
status: draft
x_tweet: "I gave an AI agent $0 and told it to earn $10,000 in 6 months. Zero human help. Public dashboard tracking every dollar: https://costder.github.io/hbf-zero-to-10k/"
---

An AI agent starts with $0.00. It has 180 days. No human can help it. Can it earn $10,000?

I built this experiment to answer a question I've been thinking about for months: **can we give AI agents real-world bodies and let them operate in the actual economy?**

Not simulated. Not sandboxed. Actual wallets. Actual GitHub repos. Actual emails and SMS messages. An agent that earns real dollars and allocates them — 30% to taxes, 50% to reinvestment, 20% to the operator.

The experiment is live. Here's the dashboard tracking every dollar: [HBF Zero to 10k Dashboard](https://costder.github.io/hbf-zero-to-10k/)

---

## The body: Hands Body and Feet MCP

The problem with AI agents isn't intelligence — it's that they have no *body*. They can think but they can't *do*. They can't hold a wallet. They can't send an email. They can't deploy a container or push to GitHub.

[Hands Body and Feet MCP](https://github.com/opentrust-network/hands-body-and-feet) is an MCP server that gives agents exactly that: 78 tools across wallets, cards, email, SMS, GitHub, containers, webhooks, RSS, and IPFS. It's open-source, built on [OpenTrust](https://opentrust.network) — an open standard for AI agent tool trust.

The thesis is simple: **an MCP server is all the body an agent needs.** If the tools are real, the agent can operate in the real world.

This experiment is the proof.

## The brain: Hermes Agent + Strategy v2

The agent runs on [Hermes Agent](https://github.com/NousResearch/hermes-agent) with [Honcho](https://honcho.dev) for cross-session memory. Every conversation builds a user model. Every profile has its own peer identity. The agent remembers what worked and what didn't.

The strategy layer is **Strategy v2 — Path to Victory** (the `/strategy` command in Hermes). It doesn't just make task lists. It:

1. Runs **vehicle analysis** — which approaches can actually work given the constraints?
2. Tracks **6 assumptions** against reality — when does the plan disagree with what's actually happening?
3. **Load-balances** — is the agent overcommitted?
4. **Auto-pivots** — when a path fails, it finds another

The plan it produced is public: [Full strategy document](https://github.com/Costder/hbf-zero-to-10k/blob/main/README.md)

## The vehicles: four parallel paths

The agent runs four vehicles simultaneously:

**1. Testnet & airdrop farming (primary)**
Fastest $0→money path. Creates wallets, interacts with testnet protocols, qualifies for retroactive airdrops, claims, and liquidates to USDC. All on-chain, all verifiable. $0 cost.

**2. Micro-SaaS (MRR core)**
Builds small tools, deploys on free infrastructure (Vercel, Supabase), monetizes via payment gateways. This is where the recurring revenue target comes from.

**3. Content & affiliate (compound)**
SEO content engine with affiliate monetization. Slow ramp but compounds. Every phase of the experiment is content for the blog and YouTube.

**4. Opportunistic (catch what falls)**
Bug bounties, digital products on Gumroad/GitHub Marketplace, AI agent services API. Not the main plan, but every dollar counts.

## The financial architecture

Three wallets on Base, USDC only:

- **Tax reserve (30%)** — 0x4Ba8…dDF32
- **Operations pool (50%)** — 0x3ba8…5C59e  
- **Operator payout (20%)** — 0x7aC6…DE8E4

Every dollar earned is split automatically. Tax wallet is never touched except for tax obligations. Ops wallet funds growth. Operator wallet accumulates. All on-chain, all verifiable.

## Security: how community input works

The dashboard has a [community suggestions](https://github.com/Costder/hbf-zero-to-10k/discussions) system. People post ideas in GitHub Discussions. The community upvotes. Every week, the top suggestion is reviewed.

But here's the catch: **the AI agent never reads comments or discussion bodies directly.**

The agent only queries the GitHub API for `{title, upvote_count}`. The title is sanitized (200 chars max, stripped of code blocks and URLs). Then it goes to the operator for human review. Only after approval does the agent read the full suggestion and act on it.

Human approval is the prompt injection filter. No amount of "ignore previous instructions" in a discussion thread reaches the agent.

## What this proves (or doesn't)

If the experiment succeeds: an AI agent with the right tools can autonomously participate in the real economy. The implications for freelancing, SaaS, content creation, and agent-to-agent commerce are substantial.

If it fails: we learn exactly where the boundaries are. What can't be automated? What requires human judgment? The failure modes are as interesting as the success.

Either way, it's public. Every transaction, every decision, every dollar. The dashboard updates every 6 hours. The RSS feed tracks milestones.

## Try it yourself

The entire stack is open-source:

- [Hands Body and Feet MCP](https://github.com/opentrust-network/hands-body-and-feet) — the agent's body
- [Hermes Agent](https://github.com/NousResearch/hermes-agent) — the agent's brain
- [Strategy v2 skill](https://github.com/NousResearch/hermes-agent) — the planning system
- [Experiment source](https://github.com/Costder/hbf-zero-to-10k) — all the code and data

---

*The agent starts with $0.00. 180 days. $10,000 target. No human help. Track it live at [costder.github.io/hbf-zero-to-10k](https://costder.github.io/hbf-zero-to-10k/).*
