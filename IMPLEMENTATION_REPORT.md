# Implementation Report — October 2026 Audit

**Branch:** `review/full-audit` · **Implemented:** 18 October 2026
All changes proposed in the audit (finding IDs F/C/E/L/S/N + restructure Option A) have been applied and committed. The two working documents from the audit phase (`REVIEW_REPORT.md`, `PROPOSED_CHANGES.md`) have been deleted now that their content is implemented; the full rationale and sources for every change live in the commit messages below and in this report.

## Commits

| Commit | Scope |
|---|---|
| `48f6186` | Factual corrections (F-01…F-16) |
| `996a274` | Consistency fixes (C-04…C-12) |
| `88d954c` | Copy edits (E-01…E-15) |
| `4a1ef44` | Technical fixes + enrichments (L-01…L-03, N-01…N-03, S-01 decision) |
| `e04c42c` | Restructure Option A (also resolves C-01, C-02, C-03, S-02, S-04) |

## 1 · Factual corrections (16 findings)

All six source-contradicted claims are fixed:

- **F-01** Google Trends removed from the Google Researcher Program's coverage; the separate Trends API application is now mentioned instead (youtube.html factsheet + DSA-route section, and more.html's "Google beyond YouTube" bullet). *Source: transparency.google/researcher-engagement.*
- **F-02** "Maximum total processing time: 80 working days" reworded — the 80 working days is the DSC's extendable deadline, and the platform's amendment window and mediation add time (dsa.html). *Source: Delegated Regulation (EU) 2025/2050 Art. 7.*
- **F-03** Telegram library advice corrected: Telethon noted as now developed on Codeberg; Pyrogram unmaintained with the active fork Kurigram; Telepathy-Community no longer called unmaintained (telegram.html). *Source: repository metadata.*
- **F-04** The "banned forever" / "put under observation" quotes re-attributed to Telegram's API-credentials page, and "fake engagement" corrected to the source's "flooding, spamming or abuse" (telegram.html). *Source: core.telegram.org/api/obtaining_api_id.*
- **F-05** Threads content marked as available in the MCL **web interface only**, not the API (meta.html factsheet + data list, index.html Meta card). *Source: transparency.meta.com; MCL docs.*
- **F-16** Failla & Rossetti title corrected to "…a year worth of social data" (references.html). *Source: arXiv 2404.18984.*

Unverified figures softened: **F-07** X's DSA route is now "historically months, often ending without access" instead of "~1.5 months"; **F-08** the collaborators-by-follow-up claim replaced with naming all researchers in the application; **F-09** the unsourced "~7 days" ticket figure removed from reddit.html and the index table; **F-11** Realism-check criticisms attributed to "researchers and civil society" rather than the DSA Observatory specifically; **F-13** the "removed content is least likely to be preserved" sub-claim dropped; **F-14** "February 2026" hedged to "early 2026"; **F-15** the Art. 40(12) framing of Google's program hedged with "In effect".

Precision fixes: **F-06** Wikimedia's higher rate limits now correctly attributed to identified clients (compliant User-Agent or auth), not OAuth; **F-12** VDE fee date softened to "fees introduced in 2026". **F-10 needed no change** — the live sentence already read "published … November 2024 … withdrawn within days".

## 2 · Consistency (11 findings)

- **C-01** Chapter numbering fixed via the restructure renumbering (toolkit → 10, ethics → 11, references → 12 — no more skipped 13).
- **C-02/C-03** more.html now has one display name ("More platforms" in prose/kicker/pager, "More Platforms" in the CSS-uppercased nav); "Alt-tech" is sentence-cased everywhere it survives the merge.
- **C-04** meta.html, toolkit.html and more.html titles (and og:titles) now follow the "… — Platform Data Access" pattern.
- **C-05** The two generic "programme"s changed to "program" (official program names untouched; the site's other British spellings untouched).
- **C-06** "France's Secure Data Access Center" → "the French secure data access centre" (sidesteps the lone US spelling; CASD remains the name).
- **C-07** Audited as conformant after C-11: "Article 40" on first mention per page, "Art. 40(x)" thereafter.
- **C-08** Judgment call: reddit's factsheet label aligned to "Apply at"; its "Terms" label kept (it genuinely links the API terms, not docs); telegram's "Get credentials" kept as a justified deviation.
- **C-09** Index table: "Up to 80 working days+" → "80+ working days".
- **C-10** Durations as numerals: "~15 minutes" (youtube lede), "~10 minutes" (index Telegram card).
- **C-11** dsa sidetoc now matches its heading ("What Article 40 gives you").
- **C-12** References: missing periods added (European Commission, MDN Web Docs); Ausloos & Veale volume, Bekavac & Mayer pages (8276–8299) added; Seiling et al. now cited by DOI 10.34669/WI.WPP/14 (re-verified as registered before the edit).

## 3 · Copy edits (15 findings)

All applied: duplications removed (E-01 "single most important decision", E-10 telegram lede/factsheet repeat, E-11 "field"×2, E-12 "metered"×2, E-13 ethics lede/bullet repeat); long sentences split (E-02 designation paragraph, E-03 index hero lede, E-06 Ad Library callout); rewrites (E-05 Threads/WhatsApp bullet, E-08 YouTube publication-rights sentence, E-09 folded into F-07); micro-fixes (E-04 "shut down", E-07 "can take up to 48 hours to appear"); jargon glossed on first use (E-14: MTProto, CDX API, VLOP in the index table, and the Art. 34 risk list marked "in practice"); tone (E-15: "dead for academics" → "effectively closed to academics").

## 4 · Links & technical

- **L-01** 404.html now uses absolute `/platform-data-access/…` paths for the stylesheet, favicon and every link, so it renders styled with working links when GitHub Pages serves it for nested missing URLs.
- **L-02** PRAW linked to praw.readthedocs.io.
- **L-03** Raw "&" in sidetoc link text escaped as `&amp;` (the two pagers that had it were rewritten by the restructure).
- **S-01** Decision: references.html deliberately keeps no sidetoc — it is one flat list with nothing to navigate to.

## 5 · Enrichments

- **N-01** TikTok's refresh obligation now named precisely: at least every 15 days (tiktok.html and the ethics AI-clauses bullet).
- **N-02** YouTube Researcher Program terms added (courtesy copy ≥ 7 days before publication; 30-day data refresh) plus the June 2026 `videos.batchGetStats` method and its own quota bucket.
- **N-03** Truthbrush noted as now maintained as a community fork.

## 6 · Restructure (Option A, as requested)

`more.html` is now Chapter 9 "More platforms" with two parts:

```
Nav (12 items): Overview · DSA Gateway · Meta · TikTok · YouTube · X ·
                Reddit · Telegram · More Platforms · Toolkit · Ethics · References

more.html — "More platforms" (Chapter 9)
├─ Part I · The wider landscape          #landscape
│   ├─ Bluesky — open by design          #bluesky
│   ├─ Wikipedia and Wikimedia           #wikimedia
│   ├─ Snapchat                          #snapchat
│   └─ In brief: the rest of the field   #brief
└─ Part II · Alt-tech & beyond           #alttech
    ├─ Alt-tech platforms                #alttech-platforms
    ├─ AI assistants                     #ai
    ├─ News and the open web             #openweb
    └─ Podcasts                          #podcasts
```

- `alttech.html` is kept at its URL as a redirect stub (canonical link + meta refresh + `location.replace('more.html' + (location.hash || '#alttech'))`), so **all old deep links keep working** — e.g. `alttech.html#ai` lands on `more.html#ai`.
- Index platform cards 09+10 merged into one "More platforms" card; the at-a-glance alt-tech row links `more.html#alttech`; dsa.html's ChatGPT cross-link retargeted to `more.html#ai`; pagers rewired telegram → more → toolkit.
- The merged page's sidetoc shows both parts with indented subsections (new `.sidetoc .sub` rule in styles.css).
- Option B (grouping by access situation) was **not** applied — the checklist allowed at most one of A/B, and A is the version the brief requested. The Option B idea (regroup Part I/II into "Open by design / DSA routes in brief / No research doors / Beyond platforms") remains available as a later editorial pass if the merged page feels miscellaneous.
- Note from the audit, still worth a glance: the restructure request mentioned "Gemini and the other existing items" as More-platforms content — Gemini lives in the AI-assistants section, which the merge brings into the page as requested. If something different was meant, say so.

## Verification

- The scripted link/anchor check was re-run after the restructure: **every internal link and anchor on all 14 pages resolves** (the checker's only flags were the intentional absolute paths in 404.html, which resolve correctly under GitHub Pages).
- Heading hierarchy of the merged page verified (h1 → two h2 parts → h3 sections → h4 callouts); the nav is identical 12-item markup on every page.
- The Seiling DOI added in C-12 was re-verified as registered via the doi.org handle API before being written in.

## Judgment calls made (user approved "all changes"; some items were flagged as "your call")

1. **R-A over R-B** — A is the requested version; the checklist forbade applying both.
2. **C-06** — sidestepped with a lowercase description rather than adopting Meta's US-spelled proper noun.
3. **C-08** — reddit aligned to "Apply at" but "Terms" kept (renaming it "Docs" would mislabel the link).
4. **E-15** — softened to "effectively closed to academics" (kept the bluntness, dropped the slang).
5. **S-01** — references.html keeps no sidetoc (nothing on the page to navigate to).
