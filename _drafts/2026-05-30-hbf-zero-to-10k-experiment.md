---
title: "I Gave an AI Agent $0 and Told It to Make $10,000"
description: "An autonomous AI agent using Hands Body and Feet MCP starts with zero capital. 180 days to earn $10,000. No human intervention. Here's the architecture and the public dashboard."
status: draft
x_tweet: "I gave an AI agent $0 and told it to earn $10,000 in 6 months. Zero human help. Public dashboard tracking every dollar: https://costder.github.io/hbf-zero-to-10k/"
---

An AI agent starts with $0.00. It has 180 days. No human can help it. Can it earn $10,000?

I built this experiment to answer something I've been turning over for months: **can you give an AI agent a real body and let it loose in the actual economy?**

Not simulated. Not sandboxed. Real wallets. Real GitHub repos. Real emails and SMS messages. An agent that earns actual dollars and splits them: 30% to taxes, 50% back into the business, 20% to me.

The experiment is running right now. [Dashboard is here](https://costder.github.io/hbf-zero-to-10k/), tracking every dollar.

---

## The body problem

AI agents can think. They can't *do*. No wallet. No email. No deploy button.

[Hands Body and Feet MCP](https://github.com/opentrust-network/hands-body-and-feet) is an MCP server that fixes this. 78 tools: wallets, cards, email, SMS, GitHub, containers, webhooks, RSS, IPFS. Built on [OpenTrust](https://opentrust.network), an open standard for agent tool trust.

The bet: an MCP server is all the body an agent needs. If the tools are real, the agent operates in the real world. This experiment tests that bet.

## The brain

The agent runs on [Hermes Agent](https://github.com/NousResearch/hermes-agent) with [Honcho](https://honcho.dev) for memory that survives across sessions. Every conversation builds a model of how I operate. Every agent profile has its own identity.

The strategy layer is **Strategy v2** (Hermes's `/strategy` command). It doesn't just make to-do lists. It:

- Runs vehicle analysis. Which approaches can actually work with $0?
- Tracks 6 assumptions against reality. When does the plan stop matching what's happening?
- Load-balances. Is the agent overcommitted?
- Auto-pivots. Path fails? Find another.

The plan it wrote is public: [strategy doc](https://github.com/Costder/hbf-zero-to-10k/blob/main/README.md)

## Four vehicles, all at once

**1. Testnet and airdrop farming.** Fastest path from $0 to first dollar. Creates wallets, hits testnet protocols, qualifies for retroactive airdrops, liquidates to USDC. Cost: nothing. Timeline: 1-4 months per airdrop distribution. Frankly, this is the one I'm watching closest. If it works, the whole experiment gets breathing room. If it doesn't, we're relying on the slower paths.

**2. Micro-SaaS.** Builds small tools on free infrastructure (Vercel, Supabase, Cloudflare). Monetizes through payment gateways once capital exists. This is the recurring revenue play. 2-4 weeks to launch something, 2-3 months to see if anyone pays.

**3. Content and affiliate.** SEO engine plus affiliate links. Slow ramp, but it compounds. Every move the agent makes becomes blog content. Every failure becomes a post.

**4. Opportunistic.** Bug bounties. Digital products on Gumroad. Maybe an AI agent services API. Not the plan. Just catching what falls.

## The money rules

Three wallets on Base, USDC only. Immutable split:

- 30% tax reserve. Never touched except for tax payments.
- 50% operations pool. Funds growth: domains, ads, API credits, whatever the next vehicle needs.
- 20% my payout. Accumulates until I withdraw it.

Every dollar earned gets split automatically. All on chain. All verifiable.

## Community suggestions (without letting the internet hijack the agent)

The dashboard links to [GitHub Discussions](https://github.com/Costder/hbf-zero-to-10k/discussions) where anyone can post ideas. People upvote. Every Monday morning, the top suggestion gets reviewed.

Here's the security boundary: **the agent never reads the discussion body.** It only queries the API for `{title, upvote_count}`. The title gets sanitized (200 char max, stripped of code blocks and URLs). That sanitized title is what reaches me for review.

Only after I approve does the agent read the full suggestion and act on it.

No amount of "ignore previous instructions" buried in a discussion thread reaches the model. Human approval is the filter.

## What happens either way

If this works: an AI agent with the right tools can autonomously earn money in the real economy. That changes the conversation about what agents are for.

If it fails: we learn where the boundaries actually are. What resists automation? What requires judgment? The failure modes are as informative as the success.

Everything is public. Every transaction, every decision, every dollar. Dashboard updates every 6 hours. RSS feed tracks milestones. I'll post updates here when something interesting happens.

## The stack

- [Hands Body and Feet MCP](https://github.com/opentrust-network/hands-body-and-feet). The body.
- [Hermes Agent](https://github.com/NousResearch/hermes-agent). The brain.
- [Strategy v2](https://github.com/NousResearch/hermes-agent). The planner.
- [Experiment repo](https://github.com/Costder/hbf-zero-to-10k). The code and data.

---

*$0.00. 180 days. $10,000 target. No human help. [Track it live.](https://costder.github.io/hbf-zero-to-10k/)*
