# 02 · Glassmorphism Dark — Tokens

## 配色

```css
--bg-base:   #0A0E1F;
--bg-2:      #0E1530;
--blob-1:    #7C3AED;  /* 紫 */
--blob-2:    #2563EB;  /* 蓝 */
--blob-3:    #EC4899;  /* 粉 */
--glass:     rgba(255,255,255,.06);
--glass-bd:  rgba(255,255,255,.12);
--text:      #F4F6FF;
--text-2:    rgba(244,246,255,.72);
--text-3:    rgba(244,246,255,.45);
```

## 字体

```css
--font-sans: 'Inter', -apple-system, system-ui, sans-serif;
```

## 关键特效

```css
/* 背景光晕（Hero 后面 3 个模糊色块） */
.blob{position:absolute;width:560px;height:560px;border-radius:50%;filter:blur(120px);opacity:.5}

/* 毛玻璃卡 */
background: rgba(255,255,255,.06);
backdrop-filter: blur(24px) saturate(180%);
-webkit-backdrop-filter: blur(24px) saturate(180%);
border: 1px solid rgba(255,255,255,.12);
border-radius: 24px;
```

## 字号

```
h1: 64px / 1.05 / -0.02em / 700
h2: 32px / 1.2 / 600
body: 16px / 1.65
```
