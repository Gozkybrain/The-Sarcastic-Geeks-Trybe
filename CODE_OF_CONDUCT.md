# Hello World

You know the feeling.

You find the perfect job. You tailor your resume. You write a cover letter that actually says something. You hit submit.

And you're one of a thousand applicants.

Or worse — you get an interview, give them your time, build a project as "proof of work," and they ghost you. The role never existed. It was data collection. A free audit. A marketing funnel disguised as a hiring pipeline.

That's the game right now. And it's rigged.

**We're here to flip it.**

This is an early-warning radar for real opportunities. We detect companies within 30 days of raising funding — the moment they're expanding, hiring, and desperate for talent — *before* they post on LinkedIn, *before* the flood of applicants, *before* the job becomes a ghost listing.

You're not a number here. You're a builder. And this trybe exists to make sure you land — not just apply.

---

## How It Works

This project scans funding rounds daily and enriches every startup with team data, social links, funding details, and news. You get a curated set of projects — each with up to 8 tailored job listings — delivered weekly.

Discover -> Research -> Strategize -> Connect -> Interview -> Negotiate -> Land.

---

## For Users

You get a fresh batch of recently funded startups every week — companies that raised money in the last 30 days and are actively hiring. Each project comes with full intel: founders, funding amount, round stage, social links, recent news, and team backgrounds. Every project has 8 job types: Frontend, Blockchain, UI/UX, Data, Content, Community, Writing, Education.

Before you can use the system, you connect two things in the app — an AI engine (OpenRouter, Claude, local Gemma, or Ollama) and your Notion workspace (paste your integration secret token into the Setup View on any Job Roadmap page). Once connected, hit "Launch Personalized Roadmap" and the AI generates your strategy.


For each job you target, the system generates three things exported directly to your Notion:

1. **Career Roadmap** — role analysis, market positioning, skills to highlight
2. **Proof of Work Projects** — 3 concrete portfolio pieces tied to what the company builds
3. **Application Guide** — 5-step plan with cold DM templates and a ChatGPT prompt for personalized outreach

**Discover → Research → Strategize → Connect → Interview → Negotiate → Land**

---

## For Admins

Admins manage the pipeline. You import raw data from Cryptorank, CoinGecko, and news sources, then merge them into clean `main.json` files.

**Admin workflow:**
1. Run `npm run create <project-name>` to scaffold a new project
2. Source data into `cryptorank.json`, `coingecko.json`, `news.json`
3. Run `node merge-agents.js <project-name>` to merge into `main.json`
4. Generate 8 job listings into `job.json`
5. Clean 
6. Push weekly batch to users



## Billing & Cowries

To use the system, you need three things: `a Notion workspace`, `an AI engine (even the free Gemma that ships with the app works)`, and **`Cowries 🐚`** — the in-app token for the community.

Each roadmap generation costs **25 🐚**. Future features will come with their own pricing too, if needed.

**How to get Cowries:**
- **Play games** — earn them directly in the app
- **Receive from others** — folks can send Cowries to your account
- **Win community activities** — Sarcastic Geeks Trybe runs events with Cowrie prizes

**Launch Day:** Everyone on the waitlist gets **300 🐚 free** when we launch. That's 12 roadmaps — enough to hit the ground running.

---
