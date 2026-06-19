# 01 · Dribbble Dark — Tokens

## 配色

```css
--bg:        #0E0E10;   /* 主背景 */
--surface:   #18181B;   /* 卡片背景 */
--surface-2: #232328;   /* 次级卡片/表头 */
--border:    #2A2A30;
--text:      #F5F5F7;
--text-2:    #A0A0A8;
--text-3:    #6B6B72;

/* 强调色（渐变三段） */
--accent-1:  #FF5A5F;   /* 珊瑚粉 */
--accent-2:  #7B61FF;   /* 紫罗兰 */
--accent-3:  #3D5AFE;   /* 电光蓝 */

/* Section 主题色（每段不同） */
--c-pick:    #FF5A5F;
--c-gorge:   #7B61FF;
--c-easy:    #3D5AFE;
--c-intense: #FF8A3D;
--c-wild:    #00C896;
```

## 字体

```css
--font-sans: 'Inter', -apple-system, 'PingFang SC', system-ui, sans-serif;
--font-mono: 'JetBrains Mono', 'SF Mono', monospace;
```

## 字号

```
h1: 56px / 1.05 / -0.02em / 700
h2: 36px / 1.15 / -0.01em / 700
h3: 22px / 1.3 / 600
body: 15px / 1.6 / 400
caption: 13px / 1.5 / uppercase tracking 0.08em
```

## 间距 / 圆角 / 阴影

```css
--gap-xs: 8px; --gap-s: 16px; --gap-m: 24px; --gap-l: 48px; --gap-xl: 96px;
--radius-s: 12px; --radius-m: 20px; --radius-l: 32px;
--shadow: 0 20px 60px rgba(0,0,0,.4);
```

## 关键特效

```css
/* Hero 三段渐变 */
background: linear-gradient(135deg, #FF5A5F 0%, #7B61FF 55%, #3D5AFE 100%);

/* 卡片悬浮 */
transition: transform .3s ease;
&:hover { transform: translateY(-4px); }

/* Section 顶 caption */
font-size: 13px; letter-spacing: .12em; text-transform: uppercase; color: var(--text-3);
```
