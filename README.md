# Coptic Aid Foundation — Website

Public website prototype for the Coptic Aid Foundation, a Montreal-based Canadian registered charity supporting needy Coptic families, orphans, widows, and university students in Egypt since the 1980s.

**Live site:** https://saherwafai.github.io/CopticAidFoundation/

---

## About this project

This is a static HTML prototype hosted on GitHub Pages. It serves as the design reference before migration to WordPress + Polylang.

- 7 pages: Home, About Us, Our Work, Donate, Get Involved, News & Media, Contact
- Internal wiki (passcode-protected)
- Fully responsive — mobile tested at 375px

---

## File structure

```
CopticAidFoundation/
├── CLAUDE.md              ← Auto-loaded by Claude Code (working rules)
├── caf_skill/
│   └── SKILL.md           ← Full project knowledge (org, brand, design, content)
├── caf_seo_ia/
│   └── SKILL.md           ← SEO/IA audit context
├── assets/
│   ├── brand/caf/         ← Logo files (SVG)
│   └── brand/government/  ← CRA / government logos
└── docs/                  ← Live website (GitHub Pages root)
    ├── theme.css          ← Single shared stylesheet — all pages link here
    ├── index.html
    ├── about-us.html
    ├── our-work.html
    ├── donate.html
    ├── get-involved.html
    ├── news.html
    ├── contact.html
    ├── sitemap.xml
    ├── robots.txt
    └── wiki/              ← Internal wiki (passcode-protected)
```

---

## Working with Claude Code

This repo is designed to be maintained through Claude Code — no coding knowledge needed.

**Setup (first time or new computer):**
1. Clone the repo: `git clone https://github.com/saherwafai/CopticAidFoundation`
2. Open the folder in Claude Code
3. `CLAUDE.md` loads automatically — Claude has full project context
4. Read `caf_skill/SKILL.md` if you need to brief a new collaborator

**Making changes:**
- Describe what you want in plain language
- Claude edits the files and shows you locally
- Say "push" to deploy to GitHub Pages (~1 min to go live)

**Viewing locally:**
- Open `docs/index.html` in any browser
- Hard-refresh after changes: `Cmd + Shift + R`

---

## Tech stack

| Layer | Choice |
|---|---|
| Prototype | Static HTML + CSS (this repo) |
| Hosting (prototype) | GitHub Pages |
| CMS (planned) | WordPress + Polylang |
| Languages | English (complete), Arabic (pending) |
| Fonts | Cormorant Garamond (headings) + Inter (body) via Google Fonts |

---

## Design system

All visual styling is in `docs/theme.css`. Never add `<style>` blocks to HTML files.

Key tokens:
- Primary green: `#06a64f`
- Secondary blue: `#2e3690`
- CTA gold: `#c8a84b`
- Headings: Cormorant Garamond (serif)
- Body: Inter (sans-serif)

---

## Org identity

**Official name:** Coptic Aid Foundation  
**French name:** Fondation d'Aide Copte  
**Arabic name:** جمعية المعونة القبطية  
**Charity registration:** BN 868786054RC0001  
**Address:** 9520 Boul. de l'Acadie, Bureau 229, Montreal, QC H4N 1L8  
**Phone:** (514) 334-9792  
**Email:** info@copticaidfoundation.org

> **Note:** Never abbreviate to "CAF" in any document or file name — always write the full name.
