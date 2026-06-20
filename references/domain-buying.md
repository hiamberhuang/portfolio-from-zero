# Domain Buying — what to check before you pay｜买域名前必查清单

Buying a domain looks like a 2-minute task. The traps are all in the fine print.

> 买域名看着是 2 分钟的事，坑全在小字里。

---

## Why buy a real domain (not a free subdomain)｜为什么买真域名

A `yourname.github.io` works, but a real domain is worth the ~$10/year:

- **Long-term asset** — it's yours; nothing tied to a platform that can change its rules
- **Branded email** — run `hi@yourname.com`
- **Tech-stack independence** — rebuild in anything, the address never changes

> 免费的 `yourname.github.io` 也能用，但一年 ~$10 的真域名值得：
> - **长期资产**——是你的，不绑定任何会改规则的平台
> - **品牌邮箱**——能用 `hi@yourname.com`
> - **技术栈独立**——网站用什么重写都行，地址永远不变

---

## The #1 trap: first-year price ≠ renewal price｜最大的坑：首年价 ≠ 续费价

First-year prices are loss-leader "haircut" prices — often $1–5. The renewal can be 3–5× higher. You hold a domain for years, so **the renewal price is the real cost.** Always click through to the renewal price before buying.

> 首年常是 1–5 美元的"骨折价"，续费可能翻 3–5 倍。你是长期持有，所以**续费价才是真实成本**。买之前永远点开 renewal price 看清楚。

---

## TLD renewal prices｜后缀续费价（选之前先查）

| TLD 后缀 | Renewal / year 续费/年 | Notes 备注 |
|---|---|---|
| **.com** | $12–15 | Most stable, the default · 最稳，首选 |
| .world / .design / .me | $20–35 | Creative, pricier than .com · 创意系，比 .com 贵一截 |
| .io | $35–60 | "Tech" feel, expensive · 科技感，但偏贵 |
| .ai | $70–100 | Priciest, often 2-year minimum · 最贵，常要求 2 年起买 |

Avoid `.info / .biz / .online` — cheap upfront, reads cheap.
> 别买 `.info / .biz / .online`——折扣价但显廉价。

---

## Registrar comparison｜注册商对比

| Registrar 注册商 | Renewal 续费 | WHOIS privacy 隐私 | Watch out for 注意 |
|---|---|---|---|
| **Cloudflare Registrar** | At-cost 成本价（最低） | ✅ Free 免费 | DNS must be on Cloudflare · DNS 必须托管在 CF |
| Namecheap | Mid 中 | ✅ Free 免费 | Solid all-rounder · 通用稳妥 |
| Porkbun | Low 低 | ✅ Free 免费 | Best value · 性价比之选 |
| GoDaddy | High 偏贵 | ❌ Often paid 常收费 | Checkout upsells; not recommended · 结账层层加购，不推荐 |

**Default: Cloudflare Registrar.** Wholesale cost, free WHOIS privacy, and it sets up Stage 7 deployment cleanly. The only condition is DNS on Cloudflare — which you want anyway.

> **默认推荐 Cloudflare Registrar**：按成本价卖、免费 WHOIS 隐私，而且和后面 Step 7 的部署（Cloudflare Pages）无缝衔接。唯一前提是 DNS 托管在 Cloudflare——反正你也需要。

---

## WHOIS privacy must be free｜WHOIS 隐私必须免费

Without privacy, your name / email / phone are publicly scrapable. Cloudflare, Namecheap, Porkbun include it free. Look for "free WHOIS privacy included."

> 不加隐私，你的姓名 / 邮箱 / 电话会被公开爬取。Cloudflare、Namecheap、Porkbun 免费送。认准 "free WHOIS privacy included"。

---

## Cancel the checkout upsells｜取消结账加购

The classic GoDaddy pattern: the cart pre-checks email hosting, web hosting, SSL, premium DNS. **SSL should never be paid** — it's free via Let's Encrypt and bundled by Cloudflare. Uncheck everything except the domain.

> GoDaddy 最典型：购物车默认勾选邮箱、hosting、SSL、premium DNS。**SSL 绝不该单独付费**——Let's Encrypt 免费、Cloudflare 自带。除了域名本身，全部取消。

---

## Two more things｜还有两件事

- **Don't let a domain expire.** Redemption can cost $80–250 — many times the renewal. Turn on **auto-renew**.
  > **域名别过期**。进"赎回期"再要回来要 $80–250，是正常续费的好几倍。直接开**自动续费**。
- **Naming**: `yourname.com` is gold. If taken, `.world / .design / .me` read professional.
  > **命名**：`yourname.com` 是金标准。被占了，`.world / .design / .me` 也够专业。
