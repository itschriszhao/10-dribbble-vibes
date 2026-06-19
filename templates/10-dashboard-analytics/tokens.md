# 10 · Dashboard Analytics — Tokens

## 配色
```css
--bg:    #F7F8FA;
--surf:  #FFFFFF;
--surf-2:#F1F3F8;
--ink:   #111827;
--ink-2: #4B5563;
--ink-3: #9CA3AF;
--line:  #E5E7EB;
--blue:  #3B82F6;
--green: #10B981;
--red:   #EF4444;
--amber: #F59E0B;
--purple:#8B5CF6;
```

## 字体
```css
--font:'Inter',-apple-system,system-ui,'PingFang SC',sans-serif;
--font-num:'JetBrains Mono','SF Mono',ui-monospace,monospace;
font-feature-settings:"tnum"; /* 等宽数字 */
```

## 字号
- h1: 32px / 1.2 / -.01em / 700
- h2: 22px / 1.3 / 600
- h3: 16px / 1.4 / 600
- body: 14px / 1.5
- metric: 30px / 700 mono

## 关键特效
```css
/* KPI 卡片 */
background: var(--surf);
border: 1px solid var(--line);
border-radius: 12px;
padding: 20px;

/* 趋势上 */
color: var(--green); &::before{content:'↑ '}
/* 趋势下 */
color: var(--red); &::before{content:'↓ '}

/* 假图表（CSS 柱状） */
background: linear-gradient(to top, var(--blue) var(--pct), var(--surf-2) var(--pct));
```
