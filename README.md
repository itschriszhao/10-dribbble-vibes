# 10 Dribbble Vibes

> 10 套高审美网页 UI 风格模板库 — 灵感源自 Dribbble，专为快速搭建有设计感的网页而生。

每套模板都是单文件 HTML + 内联 CSS，无任何依赖，包含 8 个标准模块（Hero / Overview / Table / Card Grid / Detail / Timeline / Quote / Footer）。复制 → 替换占位符 → 上线。

---

## 风格速览

| # | 名称 | 氛围 | 主色 | 适合 | 灵感来源 |
|---|------|------|------|------|---------|
| 01 | **Dribbble Dark** | 潮流、活力、年轻 | `#FF5A5F → #7B61FF → #3D5AFE` | 活动报告、出行 / 旅行报告 | Dribbble dark gradient hero shots、Linear changelog |
| 02 | **Glassmorphism Dark** | 科技、未来、轻盈 | `#0E1530` + 紫蓝光晕 | 产品 Landing、SaaS 介绍 | Apple Vision Pro 官网、Arc browser |
| 03 | **Cyberpunk Neon** | 极客、赛博、强烈 | `#00FFB2` `#FF2EC4` on `#07070C` | 技术 demo、Hack 项目、CTF | t3.chat、Vercel Edge demos、Cyberpunk 2077 UI |
| 04 | **Apple Editorial** | 克制、叙事、高级 | `#000` / `#FFF` / `#86868B` | 个人介绍、产品故事 | apple.com 产品页、Things 3 |
| 05 | **Linear Minimal** | 极简、专业、利落 | `#FFF` + `#5E6AD2` | SaaS 主页、作品集、文档 | linear.app、vercel.com、railway.app |
| 06 | **Stripe Editorial** | 友好、明亮、商业 | 粉橘紫渐变 + 大圆角 | 金融科技、SaaS 落地页 | stripe.com、resend.com |
| 07 | **Pastel Soft** | 温柔、生活、舒缓 | 藕粉 / 雾蓝 / 奶油 | 生活博客、播客、咖啡店 | Notion personal、Are.na、独立播客站 |
| 08 | **Brutalism** | 反叛、强烈、个性 | 黄 / 红 / 蓝 高饱和 + 黑粗框 | 个性博客、艺术家个站、设计工作室 | Figma 早期、Gumroad、awwwards 获奖站 |
| 09 | **Magazine Editorial** | 复古、深度、阅读 | 米色 + 衬线大标题 | 专题报道、采访、深度文章 | NYT cooking、The New Yorker、Pitchfork Reviews |
| 10 | **Dashboard Analytics** | 数据、专业、清晰 | `#F7F8FA` + 蓝 / 绿 / 紫 | 月报年报、数据看板、KPI 报告 | Linear Insights、Vercel Analytics、Posthog |

## 截图

> 截图待补，可直接打开各 `templates/{编号}/template.html` 在浏览器查看。

```bash
# 一次打开全部 10 套
open templates/*/template.html
```

## 使用方式

### 作为 Comate Skill

仓库根目录的 `SKILL.md` 已是 Comate skill 入口。把整个仓库放到：

```
~/.comate/skills/ui-templates/
```

之后在 Comate 里说："做个旅行报告页" / "做个 Landing"，会弹出 10 套风格让你选。

### 直接当 HTML 模板用

```bash
git clone https://github.com/itschriszhao/10-dribbble-vibes.git
cd 10-dribbble-vibes
cp templates/01-dribbble-dark/template.html my-page.html
# 把 [[TITLE]] [[SUBTITLE]] [[ROW_1_C1]] 等占位符替换成你的内容
open my-page.html
```

### 占位符约定

每个 `template.html` 用 `[[XXX]]` 形式标记需替换的内容：

- `[[TITLE]]` `[[SUBTITLE]]` `[[TAG]]` — Hero 文案
- `[[METRIC_1_VALUE]]` `[[METRIC_1_LABEL]]` — Hero 数据 ×4
- `[[OVERVIEW_TITLE]]` `[[OVERVIEW_TEXT]]` — 概览段
- `[[COL_1..5]]` `[[ROW_N_C1..5]]` — 对比表
- `[[CARD_1_TITLE]]` `[[CARD_1_TEXT]]` — 卡片 ×3
- `[[DETAIL_TITLE]]` `[[DETAIL_TEXT]]` — 详情段
- `[[TL_1_TIME]]` `[[TL_1_TITLE]]` `[[TL_1_TEXT]]` — 时间线
- `[[QUOTE]]` `[[QUOTE_AUTHOR]]` — 引言
- `[[FOOTER_LEFT]]` `[[FOOTER_RIGHT]]` — 页脚

## 目录结构

```
10-dribbble-vibes/
├── SKILL.md              # Comate skill 入口（含触发词、决策树）
├── INDEX.md              # 10 套风格速查
├── README.md             # 本文档
├── LICENSE
└── templates/
    ├── 01-dribbble-dark/
    │   ├── template.html # 完整可运行 HTML
    │   └── tokens.md     # 配色 / 字体 / 间距速查
    ├── 02-glassmorphism-dark/
    ├── 03-cyberpunk-neon/
    ├── 04-apple-editorial/
    ├── 05-linear-minimal/
    ├── 06-stripe-editorial/
    ├── 07-pastel-soft/
    ├── 08-brutalism/
    ├── 09-magazine-editorial/
    └── 10-dashboard-analytics/
```

每个 `tokens.md` 包含完整设计变量：配色（HEX）、字体栈、字号阶梯、间距 / 圆角 / 阴影、关键 CSS 片段（渐变、毛玻璃、霓虹发光等）。

## 设计原则

- **单文件可移植**：每个 `template.html` 都是完整 HTML + 内联 CSS，零依赖，离线可用
- **不混搭**：要换风格就整套换，不在一个页面里混用多套
- **不写 JS**：只用 CSS 表现力，避免动效膨胀
- **占位优先**：用 `[[XXX]]` 标记替换点，AI / 人工替换都友好
- **Token 驱动**：所有颜色 / 字号 / 间距都在 `:root` CSS 变量里，改主题只动一处

## 风格 vs 内容对应

不知道选哪个？参考：

- **写报告 / 数据展示** → 01 (Dribbble Dark) 或 10 (Dashboard)
- **个人作品集 / 介绍** → 04 (Apple) 或 05 (Linear)
- **产品 Landing** → 02 (Glassmorphism) 或 06 (Stripe)
- **想要个性 / 反差** → 03 (Cyberpunk) 或 08 (Brutalism)
- **长文 / 深度阅读** → 09 (Magazine)
- **生活方式 / 温柔感** → 07 (Pastel)

## 鸣谢

- 设计灵感来源：[Dribbble](https://dribbble.com)、[Awwwards](https://www.awwwards.com)、[SiteInspire](https://www.siteinspire.com)
- 部分配色与排版借鉴的真实产品：Linear、Vercel、Stripe、Apple、Notion、Are.na

## License

MIT — 见 [LICENSE](./LICENSE)。随便用、改、商用都行，保留版权声明即可。

---

如果这个仓库对你有用，欢迎 star ⭐ 或在你的项目里署名 / 链回。
