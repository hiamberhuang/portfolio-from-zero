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
  "I want recruiters to find me when they search my name", or the Chinese equivalents:
  "做个人网站", "搭作品集", "个人作品集网站", "买域名", "网站怎么上线", "怎么被谷歌搜到",
  "我的作品集太普通了", "转行做网站", "vibe coding 做网站". This skill walks the user
  through eight stages: (1) purpose, (2) domain, (3) inspiration, (4) storytelling via
  the JD-Mirror method, (5) mock-first design, (6) AI-assisted build, (7) deploy, and
  (8) SEO + AI discovery. The core thesis: the leverage in a portfolio is storytelling,
  not code — and AI handles the other 80%. Built by a non-engineer who shipped her own
  site in a weekend and used it to switch careers into AI marketing.
---

# Portfolio From Zero ｜ 从 0 到 1 做个人作品集网站

A personal site is not a coding project. It is a **24-hour storytelling project that happens to ship as HTML.**

> 个人网站不是编程项目，而是一个**恰好以 HTML 形式交付的、24 小时的 storytelling 项目**。

The hard part is never the code — AI writes the code now. The hard part is knowing **who you are, where you want to go, and how to make someone believe it in 30 seconds.** This skill is built around that truth.

> 难的从来不是代码——代码 AI 现在就能写。难的是想清楚**你是谁、想去哪、怎么让人 30 秒内相信**。这个 skill 就是围绕这件事建的。

> Companion 配套: Chinese narrated walkthrough → https://my.feishu.cn/docx/NKGbdzDzoo7SvkxpJeVcbkbFnpc
> Live reference build 在线示例 → https://amberhuang.world

## The thesis ｜ 核心主张

1. **The leverage is storytelling, not technology.** A beautiful empty site converts no one.
   > **杠杆是 storytelling，不是技术。** 一个好看但空洞的网站谁都转化不了。
2. **The fastest way to find your storyline is to mirror the job description** of the role you want most (the JD-Mirror method — Stage 4).
   > **找故事线最快的方法是镜像你最想去的岗位 JD**（JD 镜像法——Stage 4）。
3. **AI handles ~80% of the work.** Your job is the 20% that is judgment: purpose, narrative, taste, and the final review.
   > **AI 包了约 80% 的活。** 你负责剩下 20% 的判断：目的、叙事、品味、最后把关。

## How this skill works ｜ 流程

```
Stage 1: Purpose  →  2: Domain  →  3: Inspiration  →  4: Storyline (JD-Mirror)
                                                              ↓
   8: SEO & Discovery  ←  7: Deploy  ←  6: Build with AI  ←  5: Mock-first design
```

Move top-to-bottom, but **never skip Stage 1 and Stage 4** — they are where the value is. Everything else is execution AI can accelerate. Estimated total: **one focused weekend (~24h).**

> 从上到下走，但**永远别跳过 Stage 1 和 Stage 4**——价值都在这。其余都是 AI 能加速的执行。总计约**一个专注的周末（24 小时）**。

---

## Stage 1 — Purpose ｜ 目的 (10 min, do not skip)

> 先让用户回答一个问题：**你为什么做这个站？** 答案决定整条故事线。

Before anything, get the user to answer ONE question: **why are you building this site?** Push for a single primary answer.

- **Career switch / job hunt** → the site must prove you can already do the new job
- **Freelance / advisory inbound** → make the ask frictionless, show selective availability
- **Build-in-public / personal IP** → a hub that compounds your content over time

If the user gives three answers, make them rank. The #1 purpose decides the hero line, the section order, and the call-to-action.

---

## Stage 2 — Domain ｜ 域名 (30 min)

> 帮用户买真域名（不是 github.io 子域名）。最大的坑是首年价 ≠ 续费价。

Help the user buy a real domain. Reasons: long-term asset, branded email (`hi@theirname.com`), and survives any tech-stack change.

**Walk them through the cost traps first** — first-year price ≠ renewal price is the biggest. Full registrar comparison, TLD renewal table, WHOIS-privacy and checkout-upsell guidance: see `references/domain-buying.md`.

Default: **Cloudflare Registrar** (at-cost, free WHOIS privacy, sets up Stage 7 cleanly). `yourname.com` is gold; `.world / .design / .me` are fine; avoid `.info / .biz / .online`.

---

## Stage 3 — Inspiration ｜ 灵感 (1–2 h)

> 用户收集 10–15 个参考站，直到看清自己的审美。产出 3–4 个能说出口的设计 token。

The user collects 10–15 reference sites until a pattern in their own taste emerges. Curated galleries + tagging workflow: see `references/inspiration-sites.md`.

Output: **3–4 nameable design tokens** — a vibe, a color direction, a type direction, a density.

---

## Stage 4 — Storyline: the JD-Mirror method ｜ 故事线：JD 镜像法 (2–3 h, THE core stage)

> 最高杠杆的一步。访客 30 秒内要抓到：你是谁 / 做过什么 / 价值在哪。方法：镜像你最想去的岗位 JD，每条核心能力做成一个 section。

This is the highest-leverage step. A visitor decides in 30 seconds: **who you are, what you've done, where your value is.**

The method: mirror the job description of the role you want most.

1. Find the JD of the single role you want most.
2. Extract its 4–6 core required capabilities.
3. Make each capability a section, answered with your own evidence.

Full method, worked example, the 5-section skeleton (Hero · About · Experience · Cases · Contact), and the "no direct experience" case: see `references/storytelling-jd-mirror.md`.

Output: a section-by-section content outline in the user's own words. This feeds AI in Stage 6.

---

## Stage 5 — Mock-first design ｜ 先 mock 设计

> 简单布局直接交给 AI；复杂视效（3D / 旋转地球 / 复杂动画）一定先画图再让 AI reverse-engineer 成代码。

For anything visually complex, mock it in a design tool first, then hand the code to AI. Asking AI to imagine a complex visual from text produces something ugly almost every time. Decision tree + reverse-engineer-from-screenshot workflow: see `references/design-and-build.md`.

---

## Stage 6 — Build with AI ｜ AI 搭建 (8–12 h)

> 按顺序喂，别一次性梭哈：① design tokens ② 内容 ③ hero ④ 一个 section 一个加 ⑤ 动画/响应式/移动端最后。

Tool options (Claude Code / Cursor / Lovable / Bolt): see `references/design-and-build.md`.

The prompting sequence — feed in this order, never all at once:
1. Design tokens (colors, fonts, spacing)
2. Content (the storyline copy from Stage 4)
3. The hero section
4. One section at a time
5. Animation, responsiveness, mobile last

Three failure modes to warn about: whole-site-in-one-prompt (collapses), no design reference (boilerplate), all-English-no-taste (generic copy).

---

## Stage 7 — Deploy ｜ 部署 (30 min)

> 默认 Cloudflare Pages：免费、全球 CDN、自动 HTTPS，和 Cloudflare 域名一键绑定。

Default: **Cloudflare Pages**. Step-by-step (`wrangler` install → login → `pages deploy` → custom domain) and alternatives (GitHub Pages, Vercel): see `references/deploy.md`.

---

## Stage 8 — SEO & AI discovery ｜ 搜索与 AI 发现 (1 h, the step most tutorials skip)

> 大多数教程到部署就停了。这一步让用户被 Google 和 AI 搜索（ChatGPT/Perplexity/Claude）同时找到。

A site no one can find is a diary. The Phase-1 checklist:

- JSON-LD `Person` + `WebSite` schema (identity + entity recognition)
- `sitemap.xml`
- `robots.txt` (with an explicit AI-crawler policy)
- `llms.txt` (the AI-search standard)
- Register Google Search Console, submit the sitemap, request indexing
- Bidirectional `sameAs`: link the site from LinkedIn / GitHub / Rednote, and link those back

Realistic timeline, the namesake problem, and the exact schema blocks: see `references/seo-and-discovery.md`.

---

## Closing principle ｜ 收尾原则

The site is not the finish line, it's the hub. Keep it alive — one piece of content a month that links back, profiles that point to it, a periodic look at Search Console to see which queries bring people in, then feed that back into the storyline.

> 网站不是终点，是枢纽。让它活着——每月一篇链回它的内容、所有账号都指向它、定期看 Search Console 哪些 query 把人带进来，再反哺回故事线。

A weekend gets it shipped. Consistency makes it compound. ｜ 一个周末让它上线，持续性让它复利。
