# Platform Data Access — A Researcher's Guide

A static website for researchers on getting data access to Meta (Facebook & Instagram),
TikTok, YouTube, X, Reddit and Telegram — built around the EU Digital Services Act
(Article 40) routes available to academics.

**Methlab — Vrije Universiteit Brussel** · Version 1.1 · October 2026

All facts were verified against live official sources in October 2026. Platform access
programs change frequently: always check the linked application pages for current terms
before applying.

## Structure

Plain HTML + CSS, no build step. Open `index.html` or serve the folder as-is
(GitHub Pages compatible).

- `index.html` — overview, time-sensitive changes, platforms at a glance
- `dsa.html` — the EU gateway: DSA Article 40 (40(12) vs 40(4) routes)
- `meta.html`, `tiktok.html`, `youtube.html`, `x.html`, `reddit.html`, `telegram.html` — one chapter per platform
- `toolkit.html` — 4CAT, Zeeschuimer, data donation, web scraping
- `ethics.html` — ethics, GDPR and VUB practicalities
- `references.html` — full reference list
- `styles.css` — shared stylesheet (light + dark themes)

## Keeping it current

Reliable trackers: the [DSA Observatory](https://dsa-observatory.eu), the
[Weizenbaum Institute](https://www.weizenbaum-institut.de) data-access papers, the
[DSA40 Data Access Collaboratory](https://www.dsa40collaboratory.eu), and each
platform's developer changelog.
