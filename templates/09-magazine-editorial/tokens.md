# 09 · Magazine Editorial — Tokens

## 配色
```css
--bg:    #F4EFE6;   /* 米白纸张 */
--bg-2:  #ECE5D7;
--ink:   #2A1F18;   /* 深棕墨色 */
--ink-2: #5C4A3D;
--ink-3: #8B7763;
--accent:#C0392B;   /* 复古红 */
--gold:  #B08D57;   /* 金 */
--line:  rgba(42,31,24,.18);
```

## 字体
```css
--serif:'Playfair Display','Source Han Serif SC','Songti SC','Times New Roman',serif;
--sans:'Inter','PingFang SC',sans-serif;
```

## 字号（杂志感对比强烈）
- h1: 96px / 0.95 / -.02em / 700 (serif)
- h2: 56px / 1.05 / 700 (serif italic)
- h3: 22px / 1.3 / 600 (serif)
- body: 17px / 1.7 (serif)
- caption: 12px / .12em uppercase (sans)

## 关键特效
```css
/* 首字下沉 */
p::first-letter{font-size:72px;font-weight:700;float:left;line-height:.85;margin:8px 12px 0 0}

/* 多栏排版 */
column-count: 2;
column-gap: 48px;
column-rule: 1px solid var(--line);

/* 引言斜体衬线 */
font-style: italic; font-family: var(--serif);

/* 装饰性细线 */
border-top: 1px solid var(--ink); border-bottom: 3px double var(--ink);
```
