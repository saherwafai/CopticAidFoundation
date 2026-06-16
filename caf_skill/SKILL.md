# Coptic Aid Foundation — Project Skill

This skill gives Claude full context about the Coptic Aid Foundation website project. Load it at the start of any session to pick up exactly where the team left off.

---

## Organization Overview

**Name:** Coptic Aid Foundation  
**Short form:** Never abbreviate to "CAF" in any deliverable or shared document — always write the full name.  
**Type:** Canadian registered charitable organization (federal and provincial recognition)  
**Founded:** ~1992  
**Head office:** 9520 Boul. de l'Acadie, Bureau 229, Montreal, QC H4N 1L8, Canada  
**Phone:** (514) 334-9792 | **Fax:** (514) 334-3653  
**Email:** info@copticaidfoundation.org | **Donations:** donate@copticaidfoundation.org  
**Charitable registration number:** TO BE CONFIRMED  
**Languages:** English, French, Arabic (EN primary, FR/AR in progress)

---

## Mission

Support needy Coptic Christian families, orphans, widows, and university students in Egypt through:
1. Monthly financial aid
2. Small business / micro-projects
3. Emergency relief
4. Education support

No political mandate. Sole goal: help vulnerable families survive with dignity while sustaining their faith.

---

## Key Statistics (current as of June 2025)

| Metric | Value |
|---|---|
| Families receiving monthly aid | 7,150+ |
| University students supported | 728+ |
| Regions across Egypt | 48 |
| Years active | 30+ |
| Board remuneration | 100% volunteer |

---

## Church Endorsement

**Canada — Montreal Diocese:**
- Operates under the auspices of the Diocese of Montreal
- Endorsed by **His Grace Bishop Boulous**, Bishop of Montreal

**Universal Coptic Church:**
- **His Holiness Pope Tawadros II** — current blessing
- **His Holiness Pope Shenouda III** — founding blessing (1992), renewed multiple times
- Official representative in Egypt: **Rev. Fr. Mikhail Sobhi**, St. Mikhael Coptic Orthodox Church, Koufour, Tanta
- 10+ bishops and 30+ priests across Egypt have supported the work

**Supporting Bishops in Egypt (confirm currency before publishing):**
| Name | Diocese |
|---|---|
| His Grace Bishop Paula | Gharbia |
| His Grace Bishop Aghabius | Deir Mwass |
| His Grace Bishop Fam | Temma |
| His Grace Bishop Befnotius | Samallout |
| His Grace Bishop Athanassius | Beni Sweif |
| His Grace Bishop Domadius | Guiza |
| His Grace Bishop Bissada | Akhmeem |
| His Grace Bishop Bakhomios | Elbeheira |
| His Grace Bishop Hedra | Aswan |

---

## Board of Directors (confirm currency before publishing)

| Name | Role |
|---|---|
| Saad Ghali | President and Chair of the Board |
| Adel Wadie Dawoud | Vice-Chair of the Board |
| Wahib Beshay | Accounting |
| Wagih Bassili | Treasurer |
| Fikry Bishara | Operations Manager |
| Joseph E. Tadros | Secretary |
| Galal Iskandar | Family Aid Administrator |
| Fayez Habib Nossair | Family Aid Administrator |
| Samy Swiha | Communications |
| Aida Nagui Sami Abdo | Communications |
| Mina Guirguis | Communications |
| Saher Wafai Azer | IT |

All directors serve as volunteers. No remuneration. Two-year terms. No borrowing from Foundation funds.

---

## Brand Identity

**Logo files (local):**
- Vertical: `/Users/i573101/Desktop/CAF VID 2026/CAF_Logo.svg`
- Horizontal: `/Users/i573101/Desktop/CAF VID 2026/CAF_Logo_Hor.svg`

**Color palette (extracted from logo):**
| Role | Name | Hex |
|---|---|---|
| Primary | Blue | `#2e3690` |
| CTA / Action | Red | `#ec2227` |
| Hope / Accent | Green | `#06a64f` |
| Text / Body | Near-black | `#231f20` |

**Typography direction:** Serif for headlines (dignity, faith) + clean sans-serif for body (readability, trust)

**Tone:** Warm & faithful + clean & credible. Faith-rooted but polished enough to convert a first-time donor. Primary audience: donors.

**No visual identity yet** — colors and logo exist but no full brand guide. Visual design phase not yet started.

---

## Website Project

### Live prototype
- **GitHub repo:** https://github.com/saherwafai/CopticAidFoundation
- **Live site:** https://saherwafai.github.io/CopticAidFoundation/
- **Local files:** `/Users/i573101/Desktop/Coptic Aid Foundation Database/website update/`
- **Repo structure:**
  - `docs/` — website files (served by GitHub Pages from `/docs` on `main` branch)
  - `caf_skill/` — this skill file

### Git setup
- Remote: `https://github.com/saherwafai/CopticAidFoundation.git`
- Branch: `main`
- Token stored in git remote URL (private repo)
- Git user: Saher Azer <saherwafai@gmail.com>

### Technology decisions
| Decision | Choice | Reason |
|---|---|---|
| CMS | WordPress + Polylang | Familiar CMS, easy content updates, best multilingual support for EN/FR/AR with RTL |
| Prototype | Static HTML | Review content and structure before building in WordPress |
| Hosting (prototype) | GitHub Pages | Free, instant, shareable with colleagues |
| Hosting (final) | TBD — shared hosting e.g. SiteGround ~$10/month | |

### Site structure (6 pages)

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Hero, impact bar, 3 pillars, scripture, donor CTA, announcement |
| Mission | `mission.html` | Founding story, church endorsement, biblical foundation, who we serve |
| Impact | `impact.html` | 4 programs, stats, regions, bishops table |
| Give | `give.html` | PayPal, Interac e-Transfer, cheque, tax receipts, FAQ |
| About | `about.html` | Legal status, board of directors, policy, by-laws summary |
| Contact | `contact.html` | Address, phone, email, map placeholder, contact form placeholder |

### Donation methods (currently live)
- **PayPal / Credit card:** PayPal hosted button ID `XHJU69N8X8RLU`
- **Interac e-Transfer:** donate@copticaidfoundation.org (no security question — auto-deposit)
- **Cheque by mail:** to Montreal office address above

### Language structure
```
docs/
├── index.html          ← English (complete)
├── mission.html
├── impact.html
├── give.html
├── about.html
├── contact.html
├── style.css
├── fr/
│   └── index.html      ← French placeholder (translations pending)
└── ar/
    └── index.html      ← Arabic placeholder (RTL dir="rtl" already set up)
```
FR and AR language switcher links currently use `href="#"` — will be updated when translations are ready.

---

## Outstanding Items (as of June 2025)

### Content to confirm
- [ ] Charitable registration number — add to footer and Give page
- [ ] Board of directors list — confirm all names and roles are current
- [ ] Bishops list — confirm which are current and active
- [ ] Family count — currently showing 7,150+ (confirm this is up to date)
- [ ] 2023 tax receipt announcement on home page — update or remove

### Content to write
- [ ] French translations — all 6 pages
- [ ] Arabic translations — all 6 pages
- [ ] One family/project story for Impact page (makes donation appeal much stronger)
- [ ] FAQ answer for in memoriam / tribute giving

### Assets needed
- [ ] Photos: families or communities in Egypt (dignified, warm)
- [ ] Photos: small business projects (sewing, trade, workshop)
- [ ] Photos: emergency relief context
- [ ] Photos: students / education context
- [ ] Photos: archival / founding era if available
- [ ] Photo or document: Pope Tawadros II or official blessing (if permitted)
- [ ] Map: Egypt showing 48 regions of coverage

### Technical work remaining
- [ ] Visual design phase (typography, spacing, final color application)
- [ ] WordPress theme build
- [ ] Polylang multilingual setup
- [ ] Contact form wiring (submissions → info@copticaidfoundation.org)
- [ ] PayPal donate button embed (replace placeholder)
- [ ] Final hosting setup
- [ ] Domain: confirm copticaidfoundation.org points to final hosting

---

## How to Work on This with Claude

1. **Start a session:** Load this skill with `/caf_skill` — Claude will have full project context immediately
2. **Make content changes:** Tell Claude what to update; it will edit the HTML files and push to GitHub
3. **Add a colleague:** Have them clone `https://github.com/saherwafai/CopticAidFoundation` and install this skill locally
4. **Install skill locally:**
   ```
   mkdir -p ~/.claude/skills/caf_skill
   cp caf_skill/SKILL.md ~/.claude/skills/caf_skill/
   ```
5. **Push changes:** After any edit session, Claude will commit and push to GitHub automatically
6. **Keep this file updated:** After major decisions or content changes, update `caf_skill/SKILL.md` and push

---

## Key Rules for Claude Working on This Project

- Never abbreviate to "CAF" in any deliverable or shared document
- All Figma mockup screens (when that phase starts): 1440×900px
- Prototype files live in `docs/` — never move or rename this folder (GitHub Pages depends on it)
- Always push after changes so the live site stays in sync
- Stats to use: 7,150+ families, 728+ university students, 48 regions, 30+ years
- Primary donor audience — every page should have a clear path to Give
