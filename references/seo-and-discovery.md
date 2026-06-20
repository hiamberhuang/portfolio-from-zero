# SEO & AI Discovery — the step most tutorials skip｜大多数教程跳过的一步

A site no one can find is a diary. Most guides stop at "it's deployed." This is where the differentiation is — making the site findable by **both Google and AI search** (ChatGPT, Perplexity, Claude).

> 没人找得到的网站就是日记。大多数教程到"部署完"就停了。差异化在这——让网站同时被 **Google 和 AI 搜索**（ChatGPT / Perplexity / Claude）找到。

**Reframe**: for a personal site, "SEO" isn't ranking against 50,000 strangers for a keyword. It's four outcomes:

> **重新定义**：个人站的"SEO"不是为一个关键词跟 5 万陌生人抢排名，而是四个结果：

1. Someone Googles your name → your site appears · 有人搜你名字 → 出你的站
2. You DM the link → a clean preview renders · 你发链接 → 预览好看
3. Someone asks an AI about you → it cites your site · 有人问 AI 你是谁 → 引用你的站
4. A recruiter searches "[name] + [field]" → lands on you · 招聘方搜"名字 + 领域" → 落到你

---

## Phase-1 checklist (~1 hour)｜Phase 1 清单（约 1 小时）

### 1. JSON-LD `Person` schema

Tells Google + AI crawlers who the site is about. The `sameAs` array is the most important property — it merges your identity across LinkedIn / GitHub / Rednote into one entity.

> 告诉 Google + AI 爬虫这站是关于谁的。`sameAs` 数组最关键——把你 LinkedIn / GitHub / 小红书的身份合并成一个实体。

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Your Name",
  "url": "https://yourname.com",
  "jobTitle": "Your Title",
  "worksFor": { "@type": "Organization", "name": "Company" },
  "alumniOf": { "@type": "CollegeOrUniversity", "name": "Your School" },
  "knowsAbout": ["Skill A", "Skill B", "Skill C"],
  "sameAs": [
    "https://www.linkedin.com/in/you/",
    "https://github.com/you"
  ]
}
</script>
```

### 2. `WebSite` schema

A second JSON-LD block declaring the site itself as an entity. · 第二个 JSON-LD 块，把网站本身声明成一个实体。

### 3. `sitemap.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yourname.com/</loc>
    <lastmod>2026-01-01</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

> ⚠️ Real gotcha: the namespace is `sitemaps.org` (**plural**). The singular `sitemap.org` makes Google Search Console silently reject the file. Validate at validator.schema.org.
> ⚠️ 真实的坑：namespace 是 `sitemaps.org`（**复数**）。写成单数 `sitemap.org`，GSC 会静默拒收。上线后用 validator.schema.org 验一遍。

### 4. `robots.txt` (with AI-crawler policy)｜含 AI 爬虫策略

```
User-agent: *
Allow: /

# You WANT AI search to read you · 你希望 AI 搜索读到你
User-agent: GPTBot
Allow: /
User-agent: ClaudeBot
Allow: /
User-agent: PerplexityBot
Allow: /
User-agent: Google-Extended
Allow: /

Sitemap: https://yourname.com/sitemap.xml
```

### 5. `llms.txt` (the AI-search standard)｜AI 搜索标准

A plain-text file at `/llms.txt` telling AI crawlers what the site is + where structured content lives. H1 with your name, a `>` summary, then `##` sections linking cases / background / profiles. New (2024+), most people haven't done it — easy edge.

> `/llms.txt` 纯文本文件，告诉 AI 爬虫这站是什么、结构化内容在哪。H1 写名字、`>` 写摘要、`##` 分块链 case / 背景 / 账号。2024 新标准，大多数人没做——容易领先。

### 6. Register Google Search Console｜注册 GSC

- Add property `https://yourname.com` · 添加资源
- Verify (one-click DNS if on Cloudflare) · 验证（在 Cloudflare 一键 DNS）
- Submit the sitemap — **paste the full URL** `https://yourname.com/sitemap.xml`, not the relative path (GSC's field rejects it) · 提交 sitemap：**填完整 URL**，别填相对路径，GSC 会拒
- URL Inspection → Request Indexing → days become hours · URL 检查 → 请求索引 → 几天压缩到几小时

### 7. Bidirectional `sameAs`｜双向 sameAs

The schema points *out* to your profiles. Now make the profiles point *back*: `yourname.com` in your LinkedIn (About + Featured), GitHub README, Rednote/X bio. Both directions confirm the link — Google trusts the merge far more when it's mutual.

> schema 从站里指向你的账号。现在让账号反向指回来：LinkedIn（About + Featured）、GitHub README、小红书 / X 简介都挂 `yourname.com`。两边都指，Google 才敢合并。

---

## Realistic timeline｜现实时间线

- **3 days 3 天**: `site:yourname.com` resolves · 被索引
- **1–2 weeks 1–2 周**: "[name] + [qualifier]" ranks for you · "名字 + 限定词"排你
- **2–4 weeks 2–4 周**: unique long-tail queries rank #1 · 独占长尾排第一
- **1–3 months 1–3 月**: AI search cites your site · AI 搜索引用你
- **6–12 months+**: maybe page 1 for your bare name (a long game if common) · 也许裸名字进首页（名字常见就是长期仗）

---

## The namesake problem｜同名问题（裸名字排名）

If your name is common, the bare-name query is a long fight. Don't burn energy there first:

> 名字常见的话，裸名字查询是长期仗。别先死磕：

1. **Win the qualified query now**: "[name] + [field/company]". Tell people to search *that.* · 先赢"名字 + 领域/公司"，让别人搜这个
2. **Backlinks are the real lever** for the bare name: every external site that names you + links your site teaches Google "this [name] = this site." · 外部反链才是裸名字的真杠杆
3. **Wikidata** (not Wikipedia — much lower bar): create an item; it feeds Google's entity graph. · Wikidata（不是维基百科，门槛低很多）喂 Google 实体图谱
4. **Consistency**: same name, photo, bio everywhere → one strong entity → Knowledge Panel eligibility. · 全网同名、同照片、同简介 → 一个强实体 → 有资格拿 Knowledge Panel
