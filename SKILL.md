---
name: html-ppt
description: HTML PPT Studio — author professional static HTML presentations in many styles, layouts, and animations, all driven by templates. Use when the user asks for a presentation, PPT, slides, keynote, deck, slideshow, "幻灯片", "演讲稿", "做一份 PPT", "做一份 slides", a reveal-style HTML deck, a 小红书 图文, or any kind of multi-slide pitch/report/sharing document that should look tasteful and be usable with keyboard navigation. Triggers include keywords like "presentation", "ppt", "slides", "deck", "keynote", "reveal", "slideshow", "幻灯片", "演讲稿", "分享稿", "小红书图文", "talk slides", "pitch deck", "tech sharing", "technical presentation".
---

# html-ppt — HTML PPT Studio

Author professional HTML presentations as static files. One theme file = one
look. One layout file = one page type. One animation class = one entry effect.
All pages share a token-based design system in `assets/base.css`.

## Install

```bash
npx skills add https://github.com/lewislulu/html-ppt-skill
```

One command, no build. Pure static HTML/CSS/JS with only CDN webfonts.

## What the skill gives you

- **36 themes** (`assets/themes/*.css`) — minimal-white, editorial-serif, soft-pastel, sharp-mono, arctic-cool, sunset-warm, catppuccin-latte/mocha, dracula, tokyo-night, nord, solarized-light, gruvbox-dark, rose-pine, neo-brutalism, glassmorphism, bauhaus, swiss-grid, terminal-green, xiaohongshu-white, rainbow-gradient, aurora, blueprint, memphis-pop, cyberpunk-neon, y2k-chrome, retro-tv, japanese-minimal, vaporwave, midcentury, corporate-clean, academic-paper, news-broadcast, pitch-deck-vc, magazine-bold, engineering-whiteprint
- **15 full-deck templates** (`templates/full-decks/<name>/`) — complete multi-slide decks with scoped `.tpl-<name>` CSS. 8 extracted from real-world decks (xhs-white-editorial, graphify-dark-graph, knowledge-arch-blueprint, hermes-cyber-terminal, obsidian-claude-gradient, testing-safety-alert, xhs-pastel-card, dir-key-nav-minimal), 7 scenario scaffolds (pitch-deck, product-launch, tech-sharing, weekly-report, xhs-post 3:4, course-module, **presenter-mode-reveal** — 演讲者模式专用)
- **31 layouts** (`templates/single-page/*.html`) with realistic demo data
- **27 CSS animations** (`assets/animations/animations.css`) via `data-anim`
- **20 canvas FX animations** (`assets/animations/fx/*.js`) via `data-fx` — particle-burst, confetti-cannon, firework, starfield, matrix-rain, knowledge-graph (force-directed), neural-net (pulses), constellation, orbit-ring, galaxy-swirl, word-cascade, letter-explode, chain-react, magnetic-field, data-stream, gradient-blob, sparkle-trail, shockwave, typewriter-multi, counter-explosion
- **Keyboard runtime** (`assets/runtime.js`) — arrows, T (theme), A (anim), F/O, **S (presenter mode: magnetic-card popup with CURRENT / NEXT / SCRIPT / TIMER cards)**, N (notes drawer), R (reset timer in presenter)
- **FX runtime** (`assets/animations/fx-runtime.js`) — auto-inits `[data-fx]` on slide enter, cleans up on leave
- **Showcase decks** for themes / layouts / animations / full-decks gallery
- **Headless Chrome render script** for PNG export

## 📚 Quick Catalog (embedded — no network needed)

### 36 Themes
**Light & calm:** `minimal-white` · `editorial-serif` · `soft-pastel` · `solarized-light` · `catppuccin-latte` · `xiaohongshu-white`

**Bold & statement:** `sharp-mono` · `neo-brutalism` · `bauhaus` · `swiss-grid` · `memphis-pop`

**Cool & dark:** `catppuccin-mocha` · `dracula` · `tokyo-night` · `nord` · `gruvbox-dark` · `rose-pine` · `arctic-cool`

**Warm & vibrant:** `sunset-warm` · `midcentury` · `retro-tv`

**Effect-heavy:** `glassmorphism` · `aurora` · `rainbow-gradient` · `blueprint` · `terminal-green` · `cyberpunk-neon` · `vaporwave` · `y2k-chrome`

**Corporate / professional:** `corporate-clean` · `pitch-deck-vc` · `academic-paper` · `news-broadcast` · `engineering-whiteprint` · `magazine-bold` · `japanese-minimal`

### 31 Layouts
**Openers:** `cover` · `toc` · `section-divider`
**Text:** `bullets` · `two-column` · `three-column` · `big-quote`
**Data:** `stat-highlight` · `kpi-grid` · `table` · `chart-bar` · `chart-line` · `chart-pie` · `chart-radar`
**Code:** `code` · `diff` · `terminal`
**Diagrams:** `flow-diagram` · `arch-diagram` · `mindmap` · `timeline` · `roadmap` · `gantt` · `process-steps`
**Comparison:** `comparison` · `pros-cons` · `todo-checklist`
**Visuals:** `image-hero` · `image-grid`
**Closers:** `cta` · `thanks`

### 15 Full-Deck Templates
**Extracted:** `xhs-white-editorial` · `graphify-dark-graph` · `knowledge-arch-blueprint` · `hermes-cyber-terminal` · `obsidian-claude-gradient` · `testing-safety-alert` · `xhs-pastel-card` · `dir-key-nav-minimal`
**Scaffolds:** `pitch-deck` · `product-launch` · `tech-sharing` · `weekly-report` · `xhs-post` · `course-module` · `presenter-mode-reveal` 🎤

### Top 10 CSS Animations
`fade-up` (body entry) · `rise-in` (titles) · `stagger-list` (bullets/grids) · `blur-in` (cover) · `counter-up` (KPIs) · `glitch-in` (tech) · `parallax-tilt` (hover cards) · `confetti-burst` (thanks) · `kenburns` (image hero) · `page-turn-3d` (editorial)

### Canvas FX (add `<script src="../assets/animations/fx-runtime.js"></script>`)
`particle-burst` · `confetti-cannon` · `firework` · `starfield` · `matrix-rain` · `knowledge-graph` · `neural-net` · `constellation` · `galaxy-swirl` · `typewriter-multi` · `counter-explosion`

For full detail, load: `references/themes.md` · `references/layouts.md` · `references/animations.md` · `references/full-decks.md` · `references/presenter-mode.md` · `references/authoring-guide.md`

## When to use

Use when the user asks for any kind of slide-based output or wants to turn
text/notes into a presentable deck. Prefer this over building from scratch.

## 🌱 Deck Intake — 需求收集流程

**Before writing a single slide, collect and confirm the following.
If the user gives you rich content upfront, derive these from it and
propose your conclusions for confirmation. Do NOT start coding until
the user confirms or corrects.**

### Step 1: Identify intent & scenario

Ask or derive:
- **What is this deck for?** (技术分享 / 融资路演 / 周报 / 小红书图文 / 产品发布 / 课程教学 / …)
- **How will it be delivered?** (现场演讲 / 录播 / 纯静态展示 / 小红书图文)
- **Total duration?** (5min / 20min / 45min / 1h / 无所谓)

Map to a full-deck template candidate:

| Scenario | Recommended template |
|---|---|
| 技术分享 / 会议演讲 | `tech-sharing` or `presenter-mode-reveal` |
| 融资路演 / VC meeting | `pitch-deck` or `pitch-deck-vc` |
| 产品发布会 | `product-launch` |
| 周报 / 状态同步 | `weekly-report` |
| 小红书图文 (竖版) | `xhs-post` (3:4 810×1080) |
| 课程教学模块 | `course-module` |
| 代码 / 工具 review | `hermes-cyber-terminal` or `obsidian-claude-gradient` |
| 方向键极简演讲 | `dir-key-nav-minimal` |

### Step 2: Confirm theme

Choose from the 36 themes based on audience + tone:

- **工程师 / 开发者** → `tokyo-night` / `catppuccin-mocha` / `dracula` / `terminal-green`
- **设计师 / 产品经理** → `editorial-serif` / `aurora` / `soft-pastel` / `glassmorphism`
- **管理层 / 投资人** → `corporate-clean` / `minimal-white` / `pitch-deck-vc` / `swiss-grid`
- **小红书 / 消费者** → `xiaohongshu-white` / `soft-pastel` / `rainbow-gradient` / `magazine-bold`
- **学术 / 研究报告** → `academic-paper` / `engineering-whiteprint` / `nord`
- **赛博 / 黑客 / 发布会** → `cyberpunk-neon` / `vaporwave` / `neo-brutalism`

Offer 2-3 candidates and let the user pick.
Set `data-themes="a,b,c"` on `<body>` so T key cycles through all offered options.

### Step 3: Agree on slide count

Estimate from duration:
- 5 min talk → 4–6 slides
- 20 min talk → 8–12 slides
- 45 min talk → 12–16 slides
- 1 hour talk → 16–22 slides
- Static deck / 小红书图文 → 6–12 slides (no hard limit)

Confirm this before scaffolding.

### Step 4: Draft the outline (recommended for non-trivial decks)

Propose a slide structure before writing any HTML:
```
cover → [toc] → section-1 → [2-4 content] → section-2 → [2-4 content] → … → cta → thanks
```
Name each slide: "Slide 3: 问题背景", "Slide 7: 方案架构".
This catches scope creep before any HTML is written.

A good intake confirmation message looks like:

> 我可以帮你做这份 PPT！先确认四件事：
> 1. **用途 / 时长**：技术分享，约 20 分钟，对吧？
> 2. **受众**：团队内部工程师？
> 3. **风格**：我建议用 `tokyo-night`（深色技术风），备选 `corporate-clean`（浅色正式）。你倾向哪个？
> 4. **页数**：预计 8–10 页左右，先按这个做，有问题再调整。
>
> 确认后我就开始动手。

Only proceed to scaffold after user confirmation (or if user explicitly says "做吧，不用确认了").

## 🧭 Layout Selection Guide

For each slide, pick exactly ONE layout. Never use the same layout for two consecutive content slides.

### Decision tree

```
开篇页？
└── cover.html                          (大标题 + 副标题 + kicker pill)

目录页？
└── toc.html                            (2×3 编号卡片网格)

章节分隔？
└── section-divider.html                (大字编号 + 章节名)

内容页？
├── 文字为主（bullet list）？
│   └── bullets.html
├── 两栏对比（概念 + 示例）？
│   └── two-column.html
├── 三栏并排（三个支柱）？
│   └── three-column.html
└── 一段话引用？
    └── big-quote.html

数据页？
├── 一个超大数字 + 说明？
│   └── stat-highlight.html            (配 .counter 动画)
├── 4 个 KPI 卡片？
│   └── kpi-grid.html
├── 表格数据？
│   └── table.html
└── 图表？
    ├── 柱状图 → chart-bar.html
    ├── 折线图 → chart-line.html
    ├── 饼图 → chart-pie.html
    └── 雷达图 → chart-radar.html

代码 / 终端？
├── 语法高亮代码 → code.html            (highlight.js)
├── 差异化视图 → diff.html              (+/- 对比)
└── 终端窗口 → terminal.html            (模拟 terminal chrome)

图解 / 流程？
├── 流程图（5节点管道）？
│   └── flow-diagram.html
├── 架构图（3层网格）？
│   └── arch-diagram.html
├── 思维导图（SVG 动画）？
│   └── mindmap.html
├── 时间线（横向）？
│   └── timeline.html
├── 路线图（NOW/NEXT/LATER）？
│   └── roadmap.html
├── 甘特图（12周多轨）？
│   └── gantt.html
└── 步骤图（4步卡片）？
    └── process-steps.html

对比 / 决策？
├── Before / After？
│   └── comparison.html
├── 优缺点？
│   └── pros-cons.html
└── Checklist？
    └── todo-checklist.html

视觉页？
├── 全幅图片 + 文字叠加？
│   └── image-hero.html                (Ken Burns 动效背景)
└── 图片网格（Bento 布局）？
    └── image-grid.html

结尾页？
├── 行动号召（CTA）？
│   └── cta.html
└── 感谢页？
    └── thanks.html                     (confetti burst 动画)
```

**`bullets.html` is the safest fallback for generic content.**

## Quick start

1. **Scaffold a new deck.** From the repo root:
   ```bash
   ./scripts/new-deck.sh my-talk
   open examples/my-talk/index.html
   ```
2. **Pick a theme.** Open the deck and press `T` to cycle. Or hard-code it:
   ```html
   <link rel="stylesheet" id="theme-link" href="../assets/themes/aurora.css">
   ```
   See the Quick Catalog above for all 36 theme names.
3. **Pick layouts.** Copy `<section class="slide">...</section>` blocks out of
   files in `templates/single-page/` into your deck. Replace the demo data.
   See the Layout Selection Guide above to pick the right one.
4. **Add animations.** Put `data-anim="fade-up"` (or `class="anim-fade-up"`) on
   any element. On `<ul>`/grids, use `anim-stagger-list` for sequenced reveals.
   For canvas FX, use `<div data-fx="knowledge-graph">...</div>` and include
   `<script src="../assets/animations/fx-runtime.js"></script>`.
5. **Use a full-deck template.** Copy `templates/full-decks/<name>/` into
   `examples/my-talk/` as a starting point. Each folder is self-contained with
   scoped CSS. Gallery at `templates/full-decks-index.html`.
6. **Render to PNG.**
   ```bash
   ./scripts/render.sh templates/theme-showcase.html       # one shot
   ./scripts/render.sh examples/my-talk/index.html 12      # 12 slides
   ```

## Authoring rules (important)

- **Always start from a template.** Don't author slides from scratch — copy the
  closest layout from `templates/single-page/` first, then replace content.
- **Use tokens, not literal colors.** Every color, radius, shadow should come
  from CSS variables defined in `assets/base.css` and overridden by a theme.
  Good: `color: var(--text-1)`. Bad: `color: #111`.
- **Don't invent new layout files.** Prefer composing existing ones. Only add
  a new `templates/single-page/*.html` if none of the 30 fit.
- **Respect chrome slots.** `.deck-header`, `.deck-footer`, `.slide-number`
  and the progress bar are provided by `assets/base.css` + `runtime.js`.
- **Keyboard-first.** Always include `<script src="../assets/runtime.js"></script>`
  so the deck supports ← → / T / A / F / S / O / hash deep-links.
- **One `.slide` per logical page.** `runtime.js` makes `.slide.is-active`
  visible; all others are hidden.
- **Supply notes.** Wrap speaker notes in `<div class="notes">…</div>` inside
  each slide. Press S to open the overlay.
- **NEVER put presenter-only text on the slide itself.** Descriptive text like
  "这一页展示了……" or "Speaker: 这里可以补充……" or small explanatory captions
  aimed at the presenter MUST go inside `<div class="notes">`, NOT as visible
  `<p>` / `<span>` elements on the slide. The `.notes` class is `display:none`
  by default — it only appears in the S overlay. Slides should contain ONLY
  audience-facing content (titles, bullet points, data, charts, images).

## ✅ Deck QA Checklist — 交付前自审

**Before reporting the deck as done, verify every item below.
Fix any item that fails before delivery.**

### Content QA
- [ ] Every slide has a `data-title` attribute.
- [ ] No slide contains more than **6 bullet points**.
- [ ] No slide contains a visible paragraph longer than **3 lines** (split or move to notes).
- [ ] No raw hex colors in markup — all colors use `var(--text-1)`, `var(--accent)`, etc.
- [ ] Every `<section class="slide">` has exactly one layout class (not multiple competing ones).
- [ ] No `.notes` content accidentally visible to audience (`.notes { display:none }` not overridden).

### Presenter Mode QA (only if using presenter mode)
- [ ] Every slide has an `<aside class="notes">` or `<div class="notes">`.
- [ ] Each notes block is **150–300 Chinese characters**.
  Run this to check:
  ```bash
  python3 -c "import re; html=open('index.html').read(); notes=re.findall(r'<aside class="notes">(.*?)</aside>',html,re.DOTALL); [print(f'notes len={len(n.strip())}: {n.strip()[:50]}') for n in notes]"
  ```
  Flag any with len < 150 or len > 300.
- [ ] Notes use **spoken Chinese** — no "因此" / "该" / "进行" / "综上所述".
- [ ] Keywords in notes are wrapped in `<strong>`.
- [ ] Transition sentences are standalone paragraphs.
- [ ] `runtime.js` is included (`<script src="../assets/runtime.js">`).

### Technical QA
- [ ] `← →` / `Space` navigation works.
- [ ] Press `T` — theme cycling works (if `data-themes` set).
- [ ] Press `O` — overview grid shows all slides without clipping.
- [ ] Press `F` — fullscreen works.
- [ ] No broken resource paths (fonts.css, base.css, runtime.js, theme link).
- [ ] All `<script>` tags are before `</body>`.
- [ ] If `data-fx` used — canvas FX renders without console errors.
- [ ] If `xhs-post` template — viewport is `810×1080` (3:4 portrait).

### File delivery QA
- [ ] Output is at `examples/<deck-name>/index.html`.
- [ ] PNG render succeeds if export was requested.
- [ ] File is self-contained (only CDN webfonts + optional CDN highlight.js/chart.js).
- [ ] You tell the user where the file is and how to open it.

### QA failure handling
If any item fails: fix it immediately, re-run the check, report what you fixed.

## 🎤 Presenter Mode — Step-by-Step Workflow

When the user needs speaker notes / 逐字稿 / 演讲者视图, follow this exact sequence:

### Step 1: Template selection
```bash
cp -r templates/full-decks/presenter-mode-reveal examples/<deck-name>
```

### Step 2: Customize theme
Edit `data-themes` on `<html>` to list 2-5 candidate themes.
Default: tokyo-night · dracula · catppuccin-mocha · nord · corporate-clean.
Set active theme via `<link id="theme-link" href="…/assets/themes/tokyo-night.css">`.

### Step 3: Write slide content
Replace content in each `<section class="slide">` block.
**Keep slides clean — audience sees only what's on the slide.**
Do NOT put speaker cues, transition prompts, or explanatory notes on the slide body.

### Step 4: Write 逐字稿 in `<aside class="notes">`

**Three rules (non-negotiable):**

**Rule 1 — Prompt signals, not lines:**
```html
<!-- ❌ WRONG — reads like a script -->
<p>大家好，欢迎来到今天的分享。今天我将要给大家介绍一下我们团队在过去三个月做的工作。</p>

<!-- ✅ RIGHT — bold keywords, transitions as separate paragraphs -->
<p>欢迎！今天分享我们团队<strong>过去 3 个月</strong>的工作。</p>
<p>先说<em>背景</em>——三个月前我们遇到了<strong>三个核心问题</strong>：延迟高、成本炸、稳定性差。</p>
<p>接下来逐个讲解怎么解的。</p>
```

**Rule 2 — 150–300 characters per slide:**
Count characters (not words) in each notes block.
Flag anything outside this range — too short = insufficient prompts, too long = can't scan.

**Rule 3 — Spoken Chinese, not written Chinese:**

| ❌ Avoid | ✅ Use instead |
|---|---|
| 因此、所以、于是 | 然后、接下来、这样 |
| 该方案、本产品、本系统 | 这个方案、我们这个、它 |
| 进行（优化/分析/评估） | 优化、分析、评估 |
| 综上所述、总之 | 简单来说、也就是说 |
| 然而（书面） | 但是（口语）、不过 |

### Step 5: Verify
After writing all notes, check character count per block:
```bash
python3 -c "
import re
html = open('examples/<deck-name>/index.html').read()
notes = re.findall(r'<aside class="notes">(.*?)</aside>', html, re.DOTALL)
for i, n in enumerate(notes, 1):
    stripped = n.strip()
    chars = len(stripped)
    print(f'Slide {i}: {chars} chars  [{"OK" if 150<=chars<=300 else "FLAGGED"}]  {stripped[:60]}')
"
```

### Step 6: Report to user
Tell the user:
- File location: `examples/<deck-name>/index.html`
- Press `S` to open presenter window
- `← →` syncs both windows; `F` fullscreens audience view

## Writing guide

See [references/authoring-guide.md](references/authoring-guide.md) for a
step-by-step walkthrough: file structure, naming, how to transform an outline
into a deck, how to choose layouts and themes per audience, how to do a
Chinese + English deck, and how to export.

## Catalogs (load when needed)

- [references/themes.md](references/themes.md) — all 36 themes with when-to-use.
- [references/layouts.md](references/layouts.md) — all 31 layout types.
- [references/animations.md](references/animations.md) — 27 CSS + 20 canvas FX animations.
- [references/full-decks.md](references/full-decks.md) — all 15 full-deck templates.
- [references/presenter-mode.md](references/presenter-mode.md) — **演讲者模式 + 逐字稿编写指南（技术分享/演讲必看）**.
- [references/authoring-guide.md](references/authoring-guide.md) — full workflow.

## File structure

```
html-ppt/
├── SKILL.md                 (this file)
├── references/              (detailed catalogs, load as needed)
├── assets/
│   ├── base.css             (tokens + primitives — do not edit per deck)
│   ├── fonts.css            (webfont imports)
│   ├── runtime.js           (keyboard + presenter + overview + theme cycle)
│   ├── themes/*.css         (36 token overrides, one per theme)
│   └── animations/
│       ├── animations.css   (27 named CSS entry animations)
│       ├── fx-runtime.js    (auto-init [data-fx] on slide enter)
│       └── fx/*.js          (20 canvas FX modules: particles/graph/fireworks…)
├── templates/
│   ├── deck.html                  (minimal 6-slide starter)
│   ├── theme-showcase.html        (36 slides, iframe-isolated per theme)
│   ├── layout-showcase.html       (iframe tour of all 31 layouts)
│   ├── animation-showcase.html    (20 FX + 27 CSS animation slides)
│   ├── full-decks-index.html      (gallery of all 14 full-deck templates)
│   ├── full-decks/<name>/         (14 scoped multi-slide deck templates)
│   └── single-page/*.html         (31 layout files with demo data)
├── scripts/
│   ├── new-deck.sh                (scaffold a deck from deck.html)
│   └── render.sh                  (headless Chrome → PNG)
└── examples/demo-deck/            (complete working deck)
```

## Rendering to PNG

`scripts/render.sh` wraps headless Chrome at
`/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`. For multi-slide
capture, runtime.js exposes `#/N` deep-links, and render.sh iterates 1..N.

```bash
./scripts/render.sh templates/single-page/kpi-grid.html        # single page
./scripts/render.sh examples/demo-deck/index.html 8 out-dir    # 8 slides, custom dir
```

## Keyboard cheat sheet

```
←  →  Space  PgUp  PgDn  Home  End    navigate
F                                       fullscreen
S                                       open presenter window (magnetic cards: current/next/script/timer)
N                                       quick notes drawer (bottom overlay)
R                                       reset timer (in presenter window)
?preview=N                              URL param — force preview-only mode (single slide, no chrome)
O                                       slide overview grid
T                                       cycle themes (reads data-themes attr)
A                                       cycle demo animation on current slide
#/N in URL                              deep-link to slide N
Esc                                     close all overlays
```

## License & author

MIT. Copyright (c) 2026 lewis <sudolewis@gmail.com>.
