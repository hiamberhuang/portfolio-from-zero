# Portfolio From Zero

> A complete, opinionated playbook for building and shipping a personal portfolio website from scratch — **domain → deployment → being found by Google and AI search.**

Built by a non-engineer who shipped her own site in a weekend and used it to switch careers into AI marketing. The thesis: **the leverage in a portfolio is storytelling, not code — and AI handles the other 80%.**

🌐 Live reference build: **[amberhuang.world](https://amberhuang.world)**
📄 Chinese narrated walkthrough (飞书): **[full guide doc](https://my.feishu.cn/docx/NKGbdzDzoo7SvkxpJeVcbkbFnpc)**

---

## What this is

An [Agent Skill](https://www.anthropic.com/news/skills) — drop it into Claude (or any agent that reads `SKILL.md`) and it walks you, stage by stage, through building your own portfolio site. It's equally usable as a plain reading guide.

## The 8 stages

| Stage | What | Time |
|---|---|---|
| 1 · Purpose | Why are you building this? (decides everything downstream) | 10 min |
| 2 · Domain | Buy a real domain without the cost traps | 30 min |
| 3 · Inspiration | Collect references until your taste is visible | 1–2 h |
| 4 · Storyline | **The JD-Mirror method** — the core | 2–3 h |
| 5 · Design | Mock-first for anything complex | — |
| 6 · Build | Drive the AI build without it collapsing | 8–12 h |
| 7 · Deploy | Cloudflare Pages in 30 minutes | 30 min |
| 8 · SEO & AI discovery | Get found by Google *and* ChatGPT/Perplexity/Claude | 1 h |

**Total: one focused weekend (~24h).**

## The core idea: JD-Mirror

Most people freeze on *what to say about themselves.* The fix: mirror the job description of the role you want most. Extract its 4–6 required capabilities, and make each one a section of your site answered with your own evidence. When the hiring manager opens the site, it feels built for them — because it was. Full method in [`references/storytelling-jd-mirror.md`](references/storytelling-jd-mirror.md).

## Structure

```
portfolio-from-zero/
├── SKILL.md                          # the staged agent workflow
├── references/
│   ├── domain-buying.md              # registrar comparison + cost traps
│   ├── inspiration-sites.md          # galleries + taste-collection workflow
│   ├── storytelling-jd-mirror.md     # THE method
│   ├── design-and-build.md           # mock-first + AI prompting sequence
│   ├── deploy.md                     # Cloudflare Pages step-by-step
│   └── seo-and-discovery.md          # schema / sitemap / llms.txt / GSC
└── evals/
    └── evals.json
```

## Who it's for

Career-switchers, job-hunters, freelancers building advisory inbound, and anyone doing build-in-public who wants a hub that compounds.

## License

MIT. Use it, fork it, ship your own site.

If it helped, say hi — [amberhuang.world](https://amberhuang.world) · hi@amberhuang.world
