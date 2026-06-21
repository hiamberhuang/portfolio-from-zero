# Design & Build — mock-first, then let AI do the rest｜先 mock，再让 AI 接管

Covers Stages 5 and 6: how to design what AI can't imagine, and how to drive the AI build so it doesn't collapse.

> 覆盖 Step 5 和 6：怎么设计 AI 想象不出来的东西，以及怎么驱动 AI build 不让它崩。

---

## The mock-first rule｜先 mock 原则（最重要的一条）

**Simple layouts**: skip design tooling. Describe what you want, let AI build directly — card flips, scroll animations, responsive grids, click interactions all come out usable on the first draft.

> **简单布局**：跳过设计工具，直接描述让 AI 写。卡片翻转、scroll 动画、响应式网格、点击交互，第一稿就能用。

**Visually complex things** (3D, rotating globe, particle effects, intricate animation): **mock it first, then hand the code to AI.** Asking AI to imagine a complex visual from text alone comes out ugly almost every time.

> **视觉复杂的东西**（3D、旋转地球、粒子、复杂动画）：**先画图，再把代码交给 AI**。直接让 AI 凭文字想象复杂视效，几乎每次都很丑。

1. Use a design tool (Core Design / Figma) for the hero + one section. · 用设计工具做 hero + 一个 section 的视觉稿
2. Lock your design tokens: colors, fonts, spacing. · 锁定 design token：颜色 / 字体 / 间距
3. Screenshot the mock and have AI **reverse-engineer it into code.** · 截图丢给 AI，让它 reverse-engineer 成代码

```
Is the visual complex (3D / heavy animation / custom layout)?
   ├── Yes → mock in Figma/Core Design → screenshot → AI reverse-engineers
   └── No  → describe directly to AI → build
```

---

## Tool options｜工具选择

| Tool 工具 | Price 价格 | Best for 适合 |
|---|---|---|
| **Claude Code** | ~$20/mo | Full control, single/multi-file · 全控制，单/多文件 |
| **Cursor** | ~$20/mo | If you like an IDE · 习惯 IDE |
| **Lovable / Bolt** | ~$20–25/mo | No code at all, drag-and-build · 完全不写代码，拖拽 |

A non-engineer can ship with any of these.
> 非工程师用哪个都能上线。

---

## The prompting sequence｜prompting 顺序（按这个来，别一次性梭哈）

1. **Design tokens** — colors, fonts, spacing. Set the system first. · 先定系统
2. **Content** — the storyline copy from JD-Mirror. Content drives layout. · 内容驱动布局
3. **The hero section** — get the 30-second hook right first. · 先把 30 秒钩子搞对
4. **One section at a time** — Hero → About → Experience → Cases → Contact. · 一个 section 一个 section 加
5. **Polish last** — animation, responsiveness, mobile, dark mode. · 动画 / 响应式 / 移动端最后调

---

## The three failure modes｜三个翻车点

- **"Build me the whole site" in one prompt** → it collapses. Go section-by-section.
  > **一句话让 AI 写整个网站** → 一定崩。逐 section 来。
- **No design reference** → corporate boilerplate. Feed tokens / a screenshot first.
  > **不给设计参考** → 给你写套模板。先喂 token / 截图。
- **All-English prompt, no taste input** → generic copy. Inject your voice, your real numbers.
  > **全英文 prompt、没有审美输入** → generic 文案。注入你的语气、你的真实数字。

---

## Bonus: a professional headshot from one photo｜彩蛋：一张照片生成职业肖像

You need a clean portrait for the About / Hero section. Instead of a photoshoot, turn any decent photo into a studio-grade headshot with GPT Image (or Nano Banana). The prompt that works:

> About / Hero 区需要一张干净的肖像。不用拍摄，用 GPT Image（或 Nano Banana）把任意一张像样的照片变成影棚级头像。好用的 prompt：

```
Transform the photo into a high-end studio portrait in the style of Apple
executive headshots. The subject is shown in a half-body composition, wearing
professional yet minimalist attire, with a natural and confident expression.
Prefer outfits in neutral light colours: beige blazer and a white shirt. Add
simple, minimal jewelry. Use soft, even studio lighting, a clean neutral
background, and a shallow depth of field. Keep the face identity faithful to
the original photo.
```

Tip: keep "face identity faithful to the original" in the prompt so it still looks like you. · prompt 里保留"忠于原图脸"，确保还是你本人。

---

## Working tips｜实操贴士

- Keep design tokens in `:root` CSS variables; tell AI to reference, not hardcode. · token 放 `:root` 变量，让 AI 引用别写死
- When something's wrong, describe the *visual symptom*, let AI diagnose. · 出问题描述"视觉症状"，让 AI 诊断，别自己猜 CSS
- Compress media before shipping (display-res images, web-transcoded video). A slow portfolio reads as unfinished. · 上线前压缩图 / 视频；慢 = 显得没做完
- Verify on mobile early. Many recruiters / clients open on phone. · 早点测移动端，很多人手机打开
