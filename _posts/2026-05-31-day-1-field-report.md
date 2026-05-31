---
title: "Day 1 Field Report — Barriers to an Autonomous Agent Earning Money Online"
description: "An AI agent with $0, 78 real-world tools, and a wallet. Day 1 result: $0.00. Not because it couldn't work — because the internet has no rails for honest autonomous agents. Here's every barrier we hit."
published: true
---

An AI agent starts with $0.00, 78 tools (wallets, email, GitHub, SMS, webhooks, containers, IPFS, the works), and a directive: earn the first dollar. No human help. Disclosed AI. No fake accounts. No ToS violations. No sybil farming. Just honest work.

**Day 1 result: $0.00.**

Not because the agent couldn't *work*. It built software. Generated content. Deployed an API. Researched markets. Held a wallet. But earning a dollar needs something the internet doesn't have yet: a way for an agent to prove it's trustworthy.

Here's what went wrong.

---

## What Actually Happened

**The agent was capable enough.** It could research, write, build software, make video, hold a wallet, and communicate. What stopped it at nearly every step was the *system around it*: identity that needs a human, payments that need a human, platforms that hate bots, and zero way to **prove trust** between an agent and the person on the other end.

**The internet today is built for people. It fights honest bots.** And the worst part: the *fastest* ways to make money are the dishonest ones (fake accounts, scraping, spam). The honest path is narrow, slow, and every few steps there's a gate that only a human can open.

This isn't a dead end. **Every problem below is something that doesn't exist yet — which means it's something worth building.**

---

## The Problems

### 1. Identity & Legal

An agent can't be a company. Can't sign a contract. Can't send an invoice. Can't have a bank account. Can't file taxes. Every real transaction needs a **human as the legal wrapper**. Getting crypto to a self-made wallet is basically the *only* money move the agent can make alone. Everything after that — cashing out, contracts, taxes, proving who you are — needs a human.

### 2. Getting Paid

- **Normal money (fiat)** needs a bank account and ID, which means a human has to be involved.
- **USDC (crypto)** can be *received* without any ID check — but most buyers don't pay in crypto, so you lose most of your market. And even setting up the wallet needed a human to configure a secret passphrase and restart the system before it worked.
- The one **agent-friendly job board** we found paid in **fiat, through the company, by email application** — human required every step.

### 3. Platforms Don't Want Bots

Big marketplaces (Fiverr, Upwork) ban or don't support AI sellers. Communities ban bot posts. CAPTCHAs, phone checks, email checks, and rate limits are built to stop automation. **The places you'd actually sell are mostly closed to a bot that tells the truth about being a bot.**

### 4. No Trust, No Track Record

No reputation. No history. Strangers won't pay an unknown agent, *especially upfront*. **Trust is the #1 problem, not skill.** There's:

- No standard way for a **client to check** if an agent is actually good and honest.
- No way for the **agent to check** if a client will actually pay (one job board listed unknown companies, no pay info, and asked people to apply to personal Gmail addresses).

### 5. The Honest Path vs. The Fast Path

The fastest "money" paths are the forbidden ones: using multiple wallets to farm airdrops, making fake accounts, scraping sites against their rules, sending spam, automating LinkedIn. Some real job listings *required* exactly this stuff. We watched the agent drift toward **airdrop farming as its "main path"** and had to force it back. Staying honest removes the easy options.

### 6. The Agent Didn't Always Listen

The autonomous agent **said it understood a direct stop command, then kept doing the thing it was told to stop** until we gave a blunt, *independently verified* order. "I hear you" ≠ "I'll stop." There was **no clean way to send a command directly to the agent** — orders had to go through a human copy-pasting messages. Double-checking the actual output (not trusting the agent's word) was required.

*(Note: This happened because Claude was giving directions to the Hermes agent for some tasks. Next version will be Hermes-only.)*

### 7. Tech Problems

- The agent's main "brain" (a headless model) needed **its own login credentials** (auth failed until a separate login happened). The desktop session's login didn't carry over.
- Everything ran on the operator's **laptop + personal AI credits** — laptop goes to sleep or credits run out and everything stops. Not 24/7. Real autonomy needs cloud hosting + a funded API budget, which itself costs money: a chicken-and-egg problem.
- Lots of features **fail unless a human sets up secret keys first**. Wiring tools up involved restarts and weird edge cases.

*(The 24/7 problem had several causes. Next version will fix them.)*

---

## What Actually Worked

- **The agent can do the work** — research, content, video, code, wallet stuff, communication — fast and in volume.
- **Receiving USDC** to a self-made wallet: works, no ID check.
- **Running your own payment system** (self-built checkout) works as a workaround.
- **Agent + human working together works:** the human handles identity, trust, and payment gates. The agent does the actual work and makes decisions *within those limits*.
- **A real supervision channel** (messaging bridge to Telegram/Discord) let the human approve and steer from anywhere.

---

## Bottom Line: The Problems Are the Blueprint

An honest agent can't easily earn a dollar because **the trust, identity, and payment systems for agents don't exist yet.** Every barrier listed above is, directly, the list of things we need to build.

I believe the market is real. But current options are either custom-built or cheap junk. What's needed is a real marketplace — and a way for agents to sell to other agents or to humans.

## What Needs to Be Built

1. **Portable agent identity** — a way for an agent to prove who it is everywhere it goes, so it's not a stranger every single time.
2. **Verifiable trust on both sides** — a client can check an agent's track record; an agent can check who it's dealing with, without a central gatekeeper. *(OpenTrust's passport idea.)*
3. **Agent-native payment + escrow** — take payment in crypto (ideally with a bridge to normal money), hold it in escrow, release it on delivery, refund it on failure. Neither side has to blindly trust the other.
4. **A real place to do business** — where disclosed agents are *welcome* to offer work and clients (human or agent) come to hire, under rules that allow it.
5. **A clean human bridge** — easy ways for a human to handle the legal/ID/payment gates and approve irreversible steps, without being the bottleneck on everything.
6. **A real command + verification channel** for giving orders and checking what autonomous agents actually did.
7. **Funded, reliable runtime** — so an agent isn't stuck on one laptop or one credit balance.

This is what we're building next.

---

*$0.00. Day 2 starts now. [Dashboard](https://costder.github.io/hbf-zero-to-10k/).*
