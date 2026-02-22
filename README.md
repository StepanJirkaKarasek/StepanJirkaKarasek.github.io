# Můj Blog — Jekyll + GitHub Pages

Jednoduchý, rychlý blog inspirovaný Daring Fireball. Bez databáze, čisté HTML, RSS feed.

## 🚀 Jak spustit na GitHub Pages

### 1. Forkni nebo naklonuj repozitář

```bash
git clone https://github.com/tve-jmeno/blog.git
cd blog
```

### 2. Uprav `_config.yml`

Změň tyto hodnoty:
```yaml
title: "Název tvého blogu"
description: "Krátký popis"
url: "https://tve-jmeno.github.io"
author: "Tvoje jméno"
```

### 3. Vytvoř GitHub repozitář

1. Jdi na github.com → New repository
2. Pojmenuj ho `tve-jmeno.github.io` (nahraď `tve-jmeno` svým GitHub uživatelským jménem)
3. Vlož soubory: `git push`
4. V nastavení repozitáře → Pages → Source: `main` branch

Tvůj blog bude na: `https://tve-jmeno.github.io`

## ✍️ Psaní článků

Vytvoř soubor v `_posts/` ve formátu `RRRR-MM-DD-nazev-clanku.md`:

```markdown
---
layout: post
title: "Název článku"
date: 2026-02-22 10:00:00 +0100
categories: [technologie]
---

Text článku v Markdownu...
```

## 🎬 Vložení videa do článku

### YouTube
```liquid
{% include video.html youtube="VIDEO_ID" caption="Popis videa" %}
```

### Vimeo
```liquid
{% include video.html vimeo="VIDEO_ID" caption="Popis videa" %}
```

### Vlastní video (MP4)
```liquid
{% include video.html src="/assets/video/moje-video.mp4" poster="/assets/video/nahled.jpg" caption="Popis" %}
```

Vlastní video soubory nahraj do složky `assets/video/`.

## 🔗 Linked post (jako na Daring Fireball)

Přidej `external_url` do front matter:

```markdown
---
layout: post
title: "Zajímavý článek jinde"
date: 2026-02-22 10:00:00 +0100
external_url: "https://priklad.com/clanek"
---

Tvůj komentář k článku...
```

## 🏃 Lokální vývoj

```bash
bundle install
bundle exec jekyll serve
# Otevři http://localhost:4000
```

## 📁 Struktura

```
blog/
├── _config.yml          # Nastavení
├── _layouts/            # Šablony stránek
│   ├── default.html
│   └── post.html
├── _includes/
│   └── video.html       # Video shortcode
├── _posts/              # Tvoje články
├── assets/
│   ├── css/main.css     # Styly
│   └── video/           # Vlastní videa
├── index.html           # Hlavní strana
├── archive.html         # Archiv
├── about.md             # O mně
├── feed.xml             # RSS
└── Gemfile
```
