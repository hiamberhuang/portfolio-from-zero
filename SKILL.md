---
name: portfolio-from-zero
description: >
  A complete, opinionated playbook for building and shipping a personal portfolio
  website from scratch — domain to deployment to being found by Google and AI search.
  Use this skill whenever the user wants to build a personal website, portfolio site,
  or personal landing page, especially for career-switching, job-hunting, freelance /
  advisory inbound, or build-in-public. Also trigger when the user says things like
  "I want to make a personal website", "help me build my portfolio", "how do I make a
  site like X", "I have no idea what to put on my site", "my portfolio looks generic",
  "how do I buy a domain", "how do I deploy my site", "how do I get my site on Google",
  or "I want recruiters to find me when they search my name". This skill walks the user
  through eight stages: (1) purpose, (2) domain, (3) inspiration, (4) storytelling via
  the JD-Mirror method, (5) mock-first design, (6) AI-assisted build, (7) deploy, and
  (8) SEO + AI discovery. The core thesis: the leverage in a portfolio is storytelling,
  not code — and AI handles the other 80%. Built by a non-engineer who shipped her own
  site in a weekend and used it to switch careers into AI marketing.
---

# Portfolio From Zero

A personal site is not a coding project. It is a **24-hour storytelling project that happens to ship as HTML.**

The hard part is never the code — AI writes the code now. The hard part is knowing **who you are, where you want to go, and how to make someone believe it in 30 seconds.** This skill is built around that truth.

> Companion: a Chinese narrated walkthrough lives at
> https://my.feishu.cn/docx/NKGbdzDzoo7SvkxpJeVcbkbFnpc
> Live reference build: https://amberhuang.world

## The thesis

1. **The leverage is storytelling, not technology.** A beautiful empty site converts no one.
2. **The fastest way to find your storyline is to mirror the job description** of the role you want most (the JD-Mirror method — see Stage 4).
3. **AI handles ~80% of the work.** Your job is the 20% that is judgment: purpose, narrative, taste, and the final review.

## How this skill works

```
Stage 1: Purpose  →  2: Domain  →  3: Inspiration  →  4: Storyline (JD-Mirror)
                                                              ↓
   8: SEO & Discovery  ←  7: Deploy  ←  6: Build with AI  ←  5: Mock-first design
```

Move top-to-bottom, but **never skip Stage 1 and Stage 4** — they are where the value is. Everything else is execution AI can accelerate.

Estimated total: **one focused weekend (~24h).**

---

## Stage 1 — Purpose (10 min, do not skip)

Before anything, get the user to answer ONE question: **why are you building this site?**

Push for a single primary answer. The whole storyline depends on it.

- **Career switch / job hunt** → the site must prove you can already do the new job
- **Freelance / advisory inbound** → the site must make the ask frictionless and show selective availability
- **Build-in-public / personal IP** → the site is a hub that compounds your content over time

If the user gives three answers, make them rank. The #1 purpose decides the hero line, the section order, and the call-to-action.

---

## Stage 2 — Domain (30 min)

Help the user buy a real domain (not a `github.io` subdomain). Reasons: it is a long-term asset, it lets them run `hi@theirname.com` email, and it survives any tech-stack change.

**Before they buy, walk them through the cost traps** — first-year price ≠ renewal price is the single biggest one. Full registrar comparison, TLD renewal-price table, WHOIS-privacy and checkout-upsell guidance: see `references/domain-buying.md`.

Default recommendation: **Cloudflare Registrar** (at-cost pricing, free WHOIS privacy, and it sets up Stage 7 deployment cleanly). `yourname.com` is the gold standard; `.world / .design / .me` are fine creative alternatives; steer away from `.info / .biz / .online`.

---

## Stage 3 — Inspiration (1–2 h)

Before any design, the user collects 10–15 reference sites until a pattern in their own taste emerges. Curated galleries (awwwards, cofolios, godly.website, siteinspire) and a tagging workflow: see `references/inspiration-sites.md`.

The output of this stage is **3–4 design tokens** the user can name out loud: a vibe (minimalist / editorial / playful / 3D), a color direction, a type direction, a layout density.

---

## Stage 4 — Storyline: the JD-Mirror method (2–3 h, THE core stage)

This is the highest-leverage step in the entire skill. Do not let the user rush past it into design.

A visitor decides in the first 30 seconds: **who you are, what you've done, where your value is.** If the site doesn't answer those, no animation saves it.

**The method**: mirror the job description of the role you want most.

1. Find the JD of the single role you most want.
2. Extract its 4–6 core required capabilities.
3. Make each capability a section of your site — answered with your own evidence.

Full method, a worked example, the universal 5-section skeleton (Hero · About · Experience · Cases · Contact), and how to handle the "I don't have direct experience" case: see `references/storytelling-jd-mirror.md`.

Output of this stage: a section-by-section content outline, in the user's own words. This becomes the input you feed AI in Stage 6.

---

## Stage 5 — Mock-first design (part of build, but decide it here)

The rule that saves the most pain: **for anything visually complex (3D, a rotating globe, intricate animation), mock it in a design tool first, then hand the code to AI.** Asking AI to imagine a complex visual from a text description produces something ugly almost every time.

For simple layouts, skip straight to Stage 6 and let AI build directly. Decision tree + the reverse-engineer-from-screenshot workflow: see `references/design-and-build.md`.

---

## Stage 6 — Build with AI (8–12 h)

Tool options (Claude Code / Cursor / Lovable / Bolt) and what each is good for: see `references/design-and-build.md`.

The prompting sequence that works — **feed it in this order, never all at once**:

1. Design tokens (colors, fonts, spacing)
2. Content (the storyline copy from Stage 4)
3. The hero section
4. One section at a time
5. Animation, responsiveness, and mobile last

The three failure modes to warn the user about up front:
- **Asking AI for the whole site in one prompt** → it collapses
- **Giving no design reference** → corporate boilerplate
- **All-English prompts with no taste input** → generic copy

---

## Stage 7 — Deploy (30 min)

Default: **Cloudflare Pages** — free, global CDN, automatic HTTPS, and it pairs with a Cloudflare-registered domain in one click. Step-by-step (`wrangler` install → login → `pages deploy` → custom domain) and alternatives (GitHub Pages, Vercel): see `references/deploy.md`.

---

## Stage 8 — SEO & AI discovery (1 h, the step most tutorials skip)

A site no one can find is a diary. This is where most "how to build a portfolio" guides stop — and where this skill keeps going.

The Phase-1 checklist that makes the user findable by **both Google and AI search engines** (ChatGPT / Perplexity / Claude):

- JSON-LD `Person` + `WebSite` schema (identity + entity recognition)
- `sitemap.xml`
- `robots.txt` (with an explicit AI-crawler policy)
- `llms.txt` (the AI-search standard)
- Register Google Search Console, submit the sitemap, request indexing
- Bidirectional `sameAs`: link the site from LinkedIn / GitHub / Rednote, and link those back

Realistic timeline, the namesake problem (ranking for a common name), and the exact schema blocks: see `references/seo-and-discovery.md`.

---

## Closing principle

Tell the user the truth at the end: **the site is not the finish line, it's the hub.** Keep it alive — one piece of content a month that links back, profiles that point to it, and a periodic look at Search Console to see which queries bring people in, then feed that back into the storyline.

A weekend gets it shipped. Consistency makes it compound.
