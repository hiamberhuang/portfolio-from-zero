# Portfolio From Zero ｜ 从 0 到 1 做个人作品集网站

> A complete, opinionated playbook for building and shipping a personal portfolio website from scratch — **domain → deployment → being found by Google and AI search.**
>
> 一套完整、有主张的 playbook：从零搭建并上线个人作品集网站——**买域名 → 部署 → 被 Google 和 AI 搜索找到**。

Built by a non-engineer who shipped her own site in a weekend and used it to switch careers into AI marketing. The thesis: **the leverage in a portfolio is storytelling, not code — and AI handles the other 80%.**

> 作者是个非工程师，用一个周末搭出自己的网站，并靠它转行进了 AI 营销。核心主张：**作品集的杠杆是 storytelling，不是代码——剩下 80% 的活 AI 全包了。**

🌐 Live reference build 在线示例: **[amberhuang.world](https://amberhuang.world)**
📄 Chinese narrated walkthrough 中文逐字讲解（飞书）: **[full guide doc](https://my.feishu.cn/docx/NKGbdzDzoo7SvkxpJeVcbkbFnpc)**

---

## What this is ｜ 这是什么

An [Agent Skill](https://www.anthropic.com/news/skills) — drop it into Claude (or any agent that reads `SKILL.md`) and it walks you, stage by stage, through building your own portfolio site. Equally usable as a plain reading guide.

> 一个 [Agent Skill](https://www.anthropic.com/news/skills)——丢进 Claude（或任何能读 `SKILL.md` 的 agent），它会一步步带你搭出自己的作品集网站。当成纯阅读指南看也完全可以。

---

## The 8 stages ｜ 8 个阶段

| Stage 阶段 | What 内容 | Time 耗时 |
|---|---|---|
| 1 · Purpose 目的 | Why are you building this? 为什么做这个站？ | 10 min |
| 2 · Domain 域名 | Buy a real domain without the cost traps 买域名避开费用坑 | 30 min |
| 3 · Inspiration 灵感 | Collect references until your taste is visible 收集参考直到看清自己审美 | 1–2 h |
| 4 · Storyline 故事线 | **The JD-Mirror method — the core JD 镜像法（核心）** | 2–3 h |
| 5 · Design 设计 | Mock-first for anything complex 复杂视效先画图 | — |
| 6 · Build 搭建 | Drive the AI build without it collapsing 驱动 AI build 不崩 | 8–12 h |
| 7 · Deploy 部署 | Cloudflare Pages in 30 minutes 30 分钟上线 | 30 min |
| 8 · SEO & discovery 搜索 | Found by Google *and* ChatGPT/Perplexity/Claude 被 Google 和 AI 搜到 | 1 h |

**Total: one focused weekend (~24h). ｜ 总计：一个专注的周末（约 24 小时）。**

---

## The core idea: JD-Mirror ｜ 核心方法：JD 镜像

Most people freeze on *what to say about themselves.* The fix: mirror the job description of the role you want most. Extract its 4–6 required capabilities, and make each one a section of your site answered with your own evidence. When the hiring manager opens the site, it feels built for them — because it was.

> 大多数人卡在*该说自己什么*。解法：镜像你最想去的岗位的 JD，抽出它要的 4–6 个核心能力，每个能力做成网站的一个 section、用你自己的证据回应。招聘方打开网站会觉得"这是为我做的"——因为确实是。

Full method 完整方法: [`references/storytelling-jd-mirror.md`](references/storytelling-jd-mirror.md)

---

## Structure ｜ 结构

```
portfolio-from-zero/
├── SKILL.md                          # the staged agent workflow 分阶段 agent 工作流
├── references/                       # bilingual deep-dives 双语深度文档
│   ├── domain-buying.md              # registrar comparison + cost traps 注册商对比 + 费用坑
│   ├── inspiration-sites.md          # galleries + taste workflow 灵感库 + 收集流程
│   ├── storytelling-jd-mirror.md     # THE method 核心方法
│   ├── design-and-build.md           # mock-first + AI prompting 先 mock + AI prompting
│   ├── deploy.md                     # Cloudflare Pages step-by-step 部署步骤
│   └── seo-and-discovery.md          # schema / sitemap / llms.txt / GSC
└── evals/
    └── evals.json
```

---

## Who it's for ｜ 适合谁

Career-switchers, job-hunters, freelancers building advisory inbound, and anyone doing build-in-public who wants a hub that compounds.

> 转行的人、求职的人、想靠 advisory 接活的 freelancer，以及任何做 build-in-public、想要一个能持续复利的内容枢纽的人。

---

## License ｜ 许可

MIT. Use it, fork it, ship your own site. ｜ MIT 协议，随便用、fork、做你自己的站。

If it helped, say hi ｜ 觉得有用就来打个招呼 — [amberhuang.world](https://amberhuang.world) · hi@amberhuang.world
