---
layout: post
title: "Ukázkový článek s videem"
subtitle: "Jak vložit video přímo do textu"
date: 2026-02-22 10:00:00 +0100
categories: [technika]
---

Toto je ukázkový příspěvek, který demonstruje, jak snadno vložit video přímo do textu článku.

Stačí několik řádků a video se krásně zobrazí mezi odstavci.

## Video z YouTube

Použijte tag `include` s parametrem `youtube`:

{% include video.html youtube="dQw4w9WgXcQ" caption="Toto je popis videa, který se zobrazí pod ním." %}

Text může pokračovat hned za videem. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Vlastní video soubor

Pokud máte vlastní soubor `.mp4`, stačí ho nahrát do složky `assets/video/` a použít:

{% include video.html src="/assets/video/moje-video.mp4" poster="/assets/video/nahled.jpg" caption="Vlastní video." %}

## Video z Vimeo

{% include video.html vimeo="148751763" caption="Video z Vimea." %}

## Závěr

Systém podporuje YouTube, Vimeo i vlastní videa. Vše se automaticky přizpůsobí velikosti obrazovky.
