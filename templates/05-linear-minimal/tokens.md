# 05 · Linear Minimal — Tokens

## 配色
```css
--bg:    #FFFFFF;
--bg-2:  #FAFAFB;
--ink:   #08090A;
--ink-2: #6B6F76;
--ink-3: #94979E;
--line:  #E6E6E8;
--accent:#5E6AD2;   /* Linear 紫 */
--accent-2:#26B5CE;
```

## 字体
```css
--font:'Inter','Inter var',-apple-system,'PingFang SC',sans-serif;
font-feature-settings:"cv11","ss01";
```

## 字号
- h1: 56px / 1.1 / -.02em / 600
- h2: 32px / 1.2 / -.01em / 600
- h3: 18px / 1.4 / 600
- body: 15px / 1.6 / 400

## 关键特效
```css
/* 微妙阴影 */
box-shadow:0 1px 3px rgba(0,0,0,.04),0 1px 2px rgba(0,0,0,.02);

/* Linear 风按钮 */
background:var(--ink);color:#fff;padding:10px 18px;border-radius:8px;font-size:14px;font-weight:500;

/* 紫色 marker */
border-left:3px solid var(--accent);
```
