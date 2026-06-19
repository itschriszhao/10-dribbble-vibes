# AGENT.md — 给 AI Agent 的使用规则

任何 AI 编程 Agent（Cursor / Claude / Copilot / 其他）读到这份文档时，按以下规则使用本仓库的 10 套模板。

## 核心原则

> **只替换内容，不动样式。** 用户选了哪套风格就完整采用那套的配色、字体、布局、间距、阴影。除非用户明确要求改主题色，否则不要碰 CSS。

## 流程

1. **确认风格编号**。如果用户没指定，从下方"风格速查"里挑最匹配的一套，并简单说明为什么选它。
2. **读取模板**：`templates/{编号-名称}/template.html` 与同目录的 `tokens.md`。
3. **复制整份 HTML**到目标位置（用户指定路径，或默认 `index.html`）。
4. **只替换 `[[XXX]]` 占位符**为用户内容：
   - `[[TITLE]]` `[[SUBTITLE]]` `[[TAG]]` — Hero 文案
   - `[[METRIC_1_VALUE]]` / `[[METRIC_1_LABEL]]` — 4 个 Hero 数据
   - `[[OVERVIEW_TITLE]]` `[[OVERVIEW_TEXT]]` — 概览段
   - `[[COL_1..5]]` / `[[ROW_N_C1..5]]` — 表格
   - `[[CARD_1_TITLE]]` / `[[CARD_1_TEXT]]` — 卡片 ×3
   - `[[DETAIL_TITLE]]` `[[DETAIL_TEXT]]` — 详情段
   - `[[TL_1_TIME]]` `[[TL_1_TITLE]]` `[[TL_1_TEXT]]` — 时间线
   - `[[QUOTE]]` `[[QUOTE_AUTHOR]]` — 引言
   - `[[FOOTER_LEFT]]` `[[FOOTER_RIGHT]]` — 页脚
5. **裁剪规则**：用户内容用不到某个模块（比如没引言）就**整段删除该模块**，不要保留空壳，不要重写其他模块的样式。
6. **改色规则**：要换主题色只动 `:root` 里的 CSS 变量。不要在元素上写 inline style 覆盖。
7. **加内容规则**：要扩展时间线 / 卡片数量，复制现有 DOM 结构即可，class 名照旧。

## 风格速查（用于自动匹配）

| # | 名称 | 适合内容 |
|---|------|---------|
| 01 | dribbble-dark | 活动报告、潮流页、出行/旅行报告 |
| 02 | glassmorphism-dark | 产品 Landing、SaaS、科技感首页 |
| 03 | cyberpunk-neon | 技术 demo、黑客 / Hack 项目、CTF |
| 04 | apple-editorial | 个人介绍、产品故事、叙事页 |
| 05 | linear-minimal | SaaS 主页、作品集、文档 |
| 06 | stripe-editorial | 金融科技、SaaS 落地页 |
| 07 | pastel-soft | 生活方式、博客、播客、咖啡店 |
| 08 | brutalism | 个性博客、艺术家个站、设计工作室 |
| 09 | magazine-editorial | 长文专题、采访、深度报道 |
| 10 | dashboard-analytics | 月报年报、数据看板、KPI 展示 |

## 不要做

- 不引入 Tailwind / Bootstrap / 任何 JS 库
- 不混搭多套风格到同一页
- 不修改 `:root` 之外的颜色（除非用户明确要求）
- 不写 JS 动效（保持单文件可移植）
- 不给已有模块重写样式
