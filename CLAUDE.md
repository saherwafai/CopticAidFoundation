# Coptic Aid Foundation — Claude Project Instructions

This file is auto-loaded by Claude Code. Read it at the start of every session.

## Load full project context first

Run `/caf_skill` or tell Claude: "load the caf_skill" to get full org knowledge, brand rules, site structure, and design system details from `caf_skill/SKILL.md`.

---

## Non-negotiable rules — follow in every session

1. **Never abbreviate to "CAF"** in any deliverable, file name, or shared document — always write "Coptic Aid Foundation" in full
2. **Never push to GitHub without an explicit "push" instruction** from the user — always show changes locally first
3. **Never use "since 1992"** — service began in the 1980s; registered in Canada 1989
4. **Languages: EN + AR only** — French (FR) has been dropped from scope
5. **Wiki passcode: 284191** — never share in public-facing content, briefings, or commits
6. **All Figma mockup screens: 1440×900px** — nav rail 80px, center pane ~1000px, Joule pane ~360px

---

## Project structure

| Path | What it is |
|---|---|
| `docs/` | Live website files — served by GitHub Pages |
| `docs/theme.css` | Single shared CSS file — all 7 pages link to this |
| `docs/wiki/` | Internal wiki (passcode-protected) |
| `caf_skill/SKILL.md` | Full project knowledge base |
| `caf_seo_ia/SKILL.md` | SEO/IA audit context |
| `assets/` | Brand logos, photos (pending), icons |

---

## Working rules

- All CSS lives in `docs/theme.css` — never add `<style>` blocks to HTML files
- Footer and nav are copy-pasted across all 7 pages — any change must be applied to all files
- Tables must use `<thead>/<tbody>` + `data-label` attributes on `<td>` for mobile reflow
- Run the consistency checklist in SKILL.md § "Consistency & Sanity Check Rules" before every push
- Prototype files live in `docs/` — never rename or move this folder

---

## Live URLs

- **Website:** https://saherwafai.github.io/CopticAidFoundation/
- **GitHub repo:** https://github.com/saherwafai/CopticAidFoundation
- **Wiki:** https://saherwafai.github.io/CopticAidFoundation/wiki/ (passcode: 284191 — private)
- **Local files:** `/Users/i573101/Desktop/Coptic Aid Foundation Database/website update/`

---

## How a session works

1. User describes what to change
2. Claude edits the HTML/CSS files locally
3. User opens the browser to review (`Cmd + Shift + R` to hard-refresh)
4. User says "push" → Claude commits and pushes to main
5. GitHub Pages deploys in ~1 minute

## For a new collaborator

1. Clone the repo: `git clone https://github.com/saherwafai/CopticAidFoundation`
2. Open the folder in Claude Code
3. This file loads automatically — full context is live
4. Read `caf_skill/SKILL.md` for complete org and project knowledge
