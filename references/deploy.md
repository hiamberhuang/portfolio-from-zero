# Deploy — get it live in 30 minutes｜30 分钟上线

## Default: Cloudflare Pages｜默认：Cloudflare Pages

Free, global CDN, automatic HTTPS, pairs with a Cloudflare-registered domain in one click.

> 免费、全球 CDN、自动 HTTPS，和 Cloudflare 注册的域名一键绑定。

### Steps｜步骤

1. **Install Wrangler** (Cloudflare's CLI) · 装 Wrangler（Cloudflare 命令行）:
   ```
   npm install -g wrangler
   ```
2. **Log in** (opens browser OAuth) · 登录（浏览器授权）:
   ```
   wrangler login
   ```
3. **Deploy** from the project directory · 在项目目录部署:
   ```
   wrangler pages deploy .
   ```
   First run prompts for a project name; after that every deploy ships a new version. · 首次会让你起项目名，之后每次都是发新版本。
4. **Bind the custom domain** · 绑定自定义域名: Cloudflare dashboard → Workers & Pages → your project → Custom domains → add `yourname.com`. If the domain is on Cloudflare, SSL + DNS are automatic. · 域名在 Cloudflare 上的话，SSL 和 DNS 自动配。

### A scripted deploy｜脚本化部署

```bash
#!/bin/bash
# deploy.sh — sync + ship
wrangler pages deploy . --project-name=your-project --branch=main --commit-dirty=true
```

Then updates are just `bash deploy.sh`. · 之后更新就一句 `bash deploy.sh`。

---

## Gotchas｜坑

- **25 MB per-file limit on Cloudflare Pages.** Compress big videos (720p MP4) or host separately.
  > **单文件 25MB 上限**。大视频压成 720p MP4，或单独托管。
- **Exclude private folders.** If the project dir has confidential material (client decks, drafts), exclude it. Never ship files you wouldn't put on a billboard.
  > **排除私密文件夹**。项目里有机密资料（客户 deck、草稿）就排除掉。别上传你不会放上广告牌的东西。
- **www vs apex.** Add both `yourname.com` and `www.yourname.com`, or set a redirect, so neither 404s.
  > **www 和裸域名**。两个都加，或设重定向，免得有一个 404。

---

## Alternatives｜替代方案

| Host 托管 | Free 免费 | Trade-off 取舍 |
|---|---|---|
| **GitHub Pages** | ✅ | Source repo must be public · 源码仓库必须公开 |
| **Vercel** | ✅ | Great DX, domain config fiddlier · 体验好，域名配置稍麻烦 |
| **Netlify** | ✅ | Solid; one more account · 稳，但多个账号 |

GitHub Pages is the common "free" answer, but public-source means your HTML / asset paths / copy are world-readable. Cloudflare Pages keeps source private while serving publicly.

> GitHub Pages 是常见的免费选项，但源码公开 = 你的 HTML / 资源路径 / 文案全世界可见。Cloudflare Pages 源码私有、站点公开。
