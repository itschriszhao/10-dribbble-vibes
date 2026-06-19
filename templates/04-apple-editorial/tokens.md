# 04 · Apple Editorial — Tokens

## 配色
```css
--bg:    #FFFFFF;
--bg-2:  #FBFBFD;
--ink:   #1D1D1F;
--ink-2: #6E6E73;
--ink-3: #86868B;
--line:  #D2D2D7;
--accent:#0071E3;   /* Apple 蓝 */
```

## 字体
```css
--font:'SF Pro Display','SF Pro Text',-apple-system,'PingFang SC','Helvetica Neue',sans-serif;
```

## 字号（Apple 标志性大号 + 紧凑字距）
- h1: 96px / 1.05 / -.025em / 600
- h2: 56px / 1.07 / -.022em / 600
- h3: 28px / 1.2 / -.01em / 500
- body: 17px / 1.47 / -.022em
- caption: 13px / 1.4 / .04em uppercase

## 关键特效
```css
/* Apple 标志性大留白 */
section{padding:120px 0}

/* 文字渐变（用于关键大字） */
background: linear-gradient(180deg, #1D1D1F 0%, #6E6E73 100%);
-webkit-background-clip:text;-webkit-text-fill-color:transparent;
```
