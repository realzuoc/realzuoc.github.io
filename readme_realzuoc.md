# 🖋️ Customization of Default font and post DIY font in main.css

This document describes how font styles are managed across the homepage and blog posts in this Jekyll site, including per-post customization and automatic rendering of Japanese and Chinese characters.

---

## 🔧 Font Architecture Overview

The site uses a layered font strategy:

1. **Default global font**: Latin content throughout the site uses a system sans-serif stack defined in `_variables.scss`.
2. **Per-post override**: Individual blog posts may specify their own `font` in the front matter.
3. **CJK-specific rendering**: Chinese and Japanese characters automatically use appropriate serif fonts via Unicode fallback — no need to tag content manually.

---

## 📁 Font Setup in `main.scss`

### 1. Font Imports

```scss
@import url('https://fonts.googleapis.com/css2?family=Yuji+Syuku&display=swap');        // Japanese
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif+SC&display=swap');     // Simplified Chinese
@import url('https://fonts.googleapis.com/css?family=Rosario');                         // Optional post-level font
```

### 2. Global Site Font (Latin Default)

```scss
body {
  font-family: 
    "Trebuchet MS", 
    "Yuji Syuku",           // Japanese
    "Noto Serif SC",        // Chinese
    Helvetica,
    sans-serif;
}
```

---

## 📝 Per-Post Font Customization

You can specify a custom font for individual posts by adding the `font:` key in the post's front matter:

```yaml
---
layout: post
title: "Custom Font Example"
date: 2025-03-20
font: "Rosario"
---
```

This variable will populate the `--post-font` CSS custom property.

### SCSS to Handle Per-Post Fonts

```scss
article.post {
  font-family: 
    var(--post-font, "Trebuchet MS"),
    "Yuji Syuku",
    "Noto Serif SC",
    Helvetica,
    sans-serif;
}

article.post h1,
article.post h2,
article.post h3,
article.post h4,
article.post h5,
article.post h6 {
  font-family: 
    var(--post-font, "Trebuchet MS"),
    "Yuji Syuku",
    "Noto Serif SC",
    Helvetica,
    sans-serif;
}
```

---

## 🧪 Testing Your Fonts

Use the following multilingual test sentence in a post:

```
This is English. これは日本語の文章です。 这是中文句子。
```

### To inspect:
1. Right-click the text → "Inspect"
2. Open "Computed" tab → check `font-family`

Expected:
- `This is English.` → `Rosario` or default Latin font
- `これは日本語...` → `Yuji Syuku`
- `这是中文...` → `Noto Serif SC`

---

## 🧩 Troubleshooting

| Issue | Likely Cause | Solution |
|------|--------------|----------|
| Latin text is using a CJK font | Font stack order incorrect | Make sure Latin font is **first** in the `font-family` |
| Chinese/Japanese not using desired fonts | Rosario includes fallback glyphs | Use `Rosario&subset=latin` when importing |
| No effect when setting `font:` in front matter | CSS custom property not applied | Ensure `post.html` contains this line:<br>`<article class="post" style="--post-font: '{{ page.font }}';">` |

---

## 💡 Optional Enhancements

- Add `font-display: swap` to improve font loading behavior
- Use `subset=text=` in font URLs to reduce load time
- Host fonts locally for privacy or offline usage

---

## 📂 Files Involved

- `main.scss` — Font imports and global/post/CJK font logic
- `_variables.scss` — Global font definitions (`$global-font-family`)
- `_layouts/post.html` — Injects per-post `--post-font` variable
- Markdown posts — Define `font:` in front matter as needed

---

## ✅ Example Post Front Matter

```yaml
---
layout: post
title: "Winter Hike in Kamikōchi"
date: 2025-03-20
font: "Rosario"
tags: [Travel, Photography]
---
```

This sets Rosario as the font for all Latin text in this post, while still allowing CJK content to fall back to proper fonts automatically.
