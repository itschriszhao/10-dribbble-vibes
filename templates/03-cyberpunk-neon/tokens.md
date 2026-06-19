# 03 · Cyberpunk Neon — Tokens

## 配色
```css
--bg:        #07070C;
--surface:   #0E0E18;
--grid:      rgba(0,255,178,.06);
--neon-1:    #00FFB2;   /* 霓虹绿 */
--neon-2:    #FF2EC4;   /* 品红 */
--neon-3:    #00E0FF;   /* 青 */
--text:      #E8FFE8;
--text-2:    #7FB59C;
```

## 字体
```css
--font-mono: 'JetBrains Mono','SF Mono',ui-monospace,monospace;
--font-display: 'Space Grotesk','Inter',sans-serif;
```

## 关键特效
```css
/* 霓虹文字发光 */
text-shadow: 0 0 8px var(--neon-1), 0 0 24px rgba(0,255,178,.4);

/* 网格背景 */
background-image: linear-gradient(var(--grid) 1px, transparent 1px), linear-gradient(90deg, var(--grid) 1px, transparent 1px);
background-size: 40px 40px;

/* 故障感边框 */
border: 1px solid var(--neon-1);
box-shadow: inset 0 0 0 1px rgba(0,255,178,.2), 0 0 24px rgba(0,255,178,.15);
```

## 字号
- h1: 72px / 0.95 / 800 (display)
- h2: 32px / 1.1 / 700 (mono uppercase)
- body: 14px / 1.6 mono
