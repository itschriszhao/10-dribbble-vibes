---
name: ui-templates
description: 10 套精选网页 UI 风格模板库（Dribbble Dark、Glassmorphism、Cyberpunk、Apple Editorial、Linear Minimal、Stripe、Pastel、Brutalism、Magazine、Dashboard）。当用户要做落地页、报告、作品集、产品介绍页、博客页、Dashboard 等任何网页 UI，且希望复用现成风格而非从零写 CSS 时使用。触发词：UI 模板 / 配色 / 网页风格 / Dribbble 风 / 换个风格 / 做个落地页 / 报告美化 / landing page / design system。
---

# UI Templates Skill

10 套差异化的单文件 HTML 模板，覆盖深色潮流、极简、毛玻璃、赛博朋克、编辑杂志、看板等主流风格。每套模板包含 8 个标准模块（Hero / Overview / Table / Card Grid / Detail / Timeline / Callout / Footer），可独立运行无依赖。

## 使用流程

**默认行为：每次触发都先弹选择器让用户选风格**（用户已声明记不住编号，必须主动展示完整 10 套清单）。

1. 读取 `INDEX.md` 速查 10 套风格定位
2. **强制：调用 `ask_user_question` 工具，列出全部 10 个选项让用户挑**，每项格式 `编号 · 名称 — 一句话氛围 + 适合场景`，参考下方"选择器模板"。即便用户在请求里说了"做个 dashboard"也要弹选（推荐 1-2 个匹配项放最上面，但仍把 10 个全展示）
3. **唯一跳过选择器的情况**：用户明确给了风格编号或名称（如"用风格 5"、"用 brutalism"、"上次那个 dribbble dark"），直接读对应模板
4. 拿到用户选择后，读取 `templates/{编号-名称}/template.html` 和 `tokens.md`
5. **核心规则：只替换占位文案与数据，保留所有 CSS、布局结构、配色变量、字体栈**。如用户要求改色，改 `:root` 里的 CSS 变量即可
6. 若用户要求模块裁剪，按需删模块；不要重写已有模块的样式
7. 输出单文件 HTML，写入用户指定路径或 `index.html`

## 选择器模板（ask_user_question 用）

```
prompt: "选一套 UI 风格（看不到预览的话可以参考 ~/.comate/skills/ui-templates/templates/{编号}/template.html 直接打开）"
options:
- "01 · Dribbble Dark — 粉紫蓝渐变 / 潮流报告、活动页"
- "02 · Glassmorphism Dark — 深色毛玻璃 / 产品 Landing、SaaS"
- "03 · Cyberpunk Neon — 黑底霓虹绿粉 / 技术 demo、Hack 项目"
- "04 · Apple Editorial — 黑白灰大留白 / 个人介绍、产品故事"
- "05 · Linear Minimal — 极简白+微紫 / SaaS、作品集"
- "06 · Stripe Editorial — 粉橘紫渐变+大圆角 / 金融科技 Landing"
- "07 · Pastel Soft — 莫兰迪藕粉雾蓝 / 生活方式、播客"
- "08 · Brutalism — 黄红蓝高饱和+黑粗框 / 个性博客、艺术家"
- "09 · Magazine Editorial — 米色+衬线大标题 / 长文专题、采访"
- "10 · Dashboard Analytics — 浅色看板+KPI图表 / 月报年报"
```

如果可以，按用户内容类型把最匹配的 1-2 个标记 ⭐ 推荐放最前，剩下 8 个保持原顺序。

## 风格选择决策树

- **报告 / 数据展示**：01-dribbble-dark（潮流活动报告）/ 10-dashboard-analytics（数据看板）
- **个人作品集 / 介绍页**：04-apple-editorial（叙事感）/ 05-linear-minimal（SaaS 简约）
- **产品 Landing**：02-glassmorphism-dark（科技产品）/ 06-stripe-editorial（金融科技）
- **想要个性 / 反差**：03-cyberpunk-neon（黑客极客）/ 08-brutalism（艺术家个站）
- **长文阅读 / 专题**：09-magazine-editorial
- **生活方式 / 温柔感**：07-pastel-soft（播客、生活博客）

## 风格速览

| # | 名称 | 主色 | 适合 |
|---|------|------|------|
| 01 | dribbble-dark | #FF5A5F → #7B61FF → #3D5AFE | 活动报告、潮流页 |
| 02 | glassmorphism-dark | #0E1530 + 紫蓝渐变光晕 | 产品 Landing |
| 03 | cyberpunk-neon | #00FFB2 #FF2EC4 on #07070C | 技术 demo、黑客风 |
| 04 | apple-editorial | #000 / #FFF / #86868B | 故事页、产品叙事 |
| 05 | linear-minimal | #FFF + #5E6AD2 | SaaS、作品集 |
| 06 | stripe-editorial | 粉橘紫渐变 + 大圆角 | 金融科技、SaaS |
| 07 | pastel-soft | 藕粉 / 雾蓝 / 奶油 | 生活方式、播客 |
| 08 | brutalism | 黄/红/蓝高饱和 + 黑粗框 | 个性博客、艺术家 |
| 09 | magazine-editorial | 米色 + 衬线大标题 | 长文专题、采访 |
| 10 | dashboard-analytics | 浅色 + 蓝绿数据色 | 月报年报、看板 |

## 触发词（中英）

UI 模板 / 配色 / 网页风格 / Dribbble / 换个风格 / 做个落地页 / 报告美化 / 给我个 UI / 来个 hero / 套个模板 / ui template / landing page / design system / page style

## 替换约定

模板里使用以下占位符，AI 只替换这些：

- `[[TITLE]]` 主标题
- `[[SUBTITLE]]` 副标题
- `[[TAG]]` 顶部小标签
- `[[METRIC_*]]` Hero 区数据
- `[[SECTION_TITLE]]` 各 section 大标题
- `[[ITEM_*]]` 列表/卡片项
- `[[TABLE_HEADERS]]` `[[TABLE_ROWS]]` 表格内容
- `[[QUOTE]]` `[[QUOTE_AUTHOR]]` 引言
- `[[TIMELINE_*]]` 时间线
- `[[FOOTER]]` 页脚

## 不做的事

- 不引入 Tailwind / Bootstrap 等框架
- 不写 JS 动效（保持单文件可移植）
- 不混搭风格（要换风格就整套换）
