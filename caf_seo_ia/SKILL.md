---
name: caf-seo-ia
description: SEO, GEO, AEO, and Information Architecture audit framework for the Coptic Aid Foundation website — evidence-based, adversarially verified, CAF-specific. Load alongside /caf_skill for full context.
metadata:
  type: project
---

# Coptic Aid Foundation — SEO, GEO, AEO & IA Skill

This skill provides a full audit framework for the Coptic Aid Foundation website across four dimensions:
1. **SEO** — Search Engine Optimization
2. **GEO** — Generative Engine Optimization (AI search engines)
3. **AEO** — Answer Engine Optimization (featured snippets, voice)
4. **IA** — Information Architecture

**Research basis:** All rules marked ✓ survived adversarial 3-vote verification against primary sources (Google, W3C, NNG, Ahrefs). Rules marked ⚠ are best-practice guidance not yet formally verified. Rules marked ✗ were explicitly refuted and must NOT be followed.

**Always load `/caf_skill` first** — this skill builds on foundation knowledge stored there.

---

## How to Run an Audit

When asked to audit the CAF website, score each dimension 1–10 using the checklists below. For each item:
- ✅ Pass (1 point)
- ❌ Fail (0 points)
- ⚠ Partial (0.5 points)

Report: score per dimension, top 3 critical issues, top 3 quick wins, and a prioritized action plan.

---

## Part 1 — Technical SEO

### Performance (Lighthouse 10) ✓ verified
Target: **90+** on all four PageSpeed Insights categories (Performance, Accessibility, Best Practices, SEO) for both desktop and mobile.

Lighthouse 10 performance score weights (verified):
| Metric | Weight |
|---|---|
| Total Blocking Time (TBT) | 30% |
| Largest Contentful Paint (LCP) | 25% |
| Cumulative Layout Shift (CLS) | 25% |
| First Contentful Paint (FCP) | 10% |
| Speed Index | 10% |

Score bands: 0–49 Poor (red) · 50–89 Needs Improvement (orange) · 90–100 Good (green)

**Audit checklist:**
- [ ] PageSpeed Insights score ≥ 90 on mobile
- [ ] PageSpeed Insights score ≥ 90 on desktop
- [ ] LCP ≤ 2.5s
- [ ] CLS ≤ 0.1
- [ ] TBT ≤ 200ms
- [ ] Images compressed and served in next-gen formats (WebP)
- [ ] No render-blocking resources in `<head>`
- [ ] HTTPS enabled on all pages
- [ ] No broken links (4xx errors)
- [ ] XML sitemap present and submitted to Google Search Console
- [ ] robots.txt present and correctly configured
- [ ] Canonical tags on all pages

### Indexability ⚠
- [ ] All 8 pages indexable (not blocked by robots.txt or noindex)
- [ ] Google Search Console verified
- [ ] No duplicate content issues
- [ ] URL structure clean and descriptive (e.g. /mission not /page?id=2)

---

## Part 2 — On-Page SEO

### Title Tags ⚠
- [ ] Every page has a unique title tag
- [ ] Title tags 50–60 characters
- [ ] Primary keyword near the front
- [ ] Foundation name included: "Coptic Aid Foundation"

**CAF-specific title tag patterns:**
- Home: `Coptic Aid Foundation | Helping Coptic Families in Egypt Since the 1980s`
- Mission: `Our Mission | Coptic Aid Foundation`
- Give: `Donate | Coptic Aid Foundation | Canadian Registered Charity`
- Get Involved: `Volunteer | Coptic Aid Foundation`

### Meta Descriptions ⚠
- [ ] Every page has a unique meta description
- [ ] 150–160 characters
- [ ] Includes a call to action
- [ ] Mentions Canada or Montreal (local signal)

### Heading Structure ⚠
- [ ] One H1 per page — matches page topic
- [ ] H2s used for major sections
- [ ] H3s used for subsections only
- [ ] No skipped heading levels
- [ ] Headings contain natural language, not keyword-stuffed text

### Content Quality — E-E-A-T ✓ verified
For a nonprofit serving vulnerable communities (health, social services, financial aid), Google applies YMYL (Your Money or Your Life) standards. Verified E-E-A-T signals:

- [ ] **Experience** — founding story with dates, named individuals, real locations (Tanta, Montreal) — all present in Mission page ✓
- [ ] **Expertise** — board member names and roles listed — present in About page ✓
- [ ] **Authoritativeness** — church endorsements named with titles — present ✓
- [ ] **Trust** — CRA charity registration number (BN: 868786054RC0001) displayed — present ✓
- [ ] **Trust** — CRA verification links — present on Give page ✓
- [ ] **Trust** — Annual report or financial disclosure linked — **missing — add**
- [ ] **Trust** — T3010 CRA filing linked — **missing — add**
- [ ] **Trust** — Bishop endorsement videos (when available) — planned via lightbox ✓

### CAF-Specific Keyword Strategy ⚠
Target keyword clusters (not yet researched — add to future keyword research task):

**Primary (high intent, donor-facing):**
- "donate to Coptic charity Canada"
- "Coptic Aid Foundation"
- "help Coptic families Egypt"
- "Canadian Coptic charity"
- "registered charity Montreal"

**Secondary (mission/awareness):**
- "Coptic Christians poverty Egypt"
- "orphans widows Egypt support"
- "volunteer Coptic organization Montreal"
- "Egyptian Coptic nonprofit"

**French equivalents:**
- "organisme de bienfaisance copte Canada"
- "aide aux familles coptes Egypte"
- "bénévolat fondation copte Montréal"

**Arabic equivalents:**
- "جمعية مساعدة الأقباط كندا"
- "مساعدة الأسر المسيحية في مصر"
- "تبرع لجمعية معونة الأقباط"

---

## Part 3 — Structured Data / Schema Markup

### Organization Schema ✓ verified
Google's Organization structured data has **no required properties** — add as many relevant properties as possible. Verified recommendation:

```json
{
  "@context": "https://schema.org",
  "@type": "NonprofitOrganization",
  "name": "Coptic Aid Foundation",
  "alternateName": ["Fondation d'Aide Copte", "جمعية المعونة القبطية"],
  "url": "https://copticaidfoundation.org",
  "logo": "https://copticaidfoundation.org/assets/brand/caf/CAF_Logo_Hor.svg",
  "description": "Montreal-based Canadian registered charity supporting needy Coptic families, orphans, widows, and university students in Egypt since the 1980s.",
  "foundingDate": "1989",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "9520 Boul. de l'Acadie, Bureau 229",
    "addressLocality": "Montreal",
    "addressRegion": "QC",
    "postalCode": "H4N 1L8",
    "addressCountry": "CA"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-514-334-9792",
    "contactType": "customer service",
    "availableLanguage": ["English", "French", "Arabic"]
  },
  "sameAs": [
    "https://www.facebook.com/copticaidfoundation",
    "https://apps.cra-arc.gc.ca/ebci/hacc/srch/pub/chrtydtls/868786054RR0001"
  ],
  "nonprofitStatus": "Nonprofit501c3"
}
```

⚠ **Important caveat (verified):** There is **no Canadian nonprofit type** in schema.org. The five available enumerations are DE, IT, NL, UK, US only. Canadian charities must use the generic `nonprofitStatus` property. The `Nonprofit501c3` value above is a placeholder — omit or use the closest available value.

### Additional Schema Types to Implement ⚠
- [ ] **FAQPage** — on Give page FAQ section
- [ ] **Event** — when events are published on News & Media
- [ ] **BreadcrumbList** — on all interior pages
- [ ] **WebSite** — on home page (enables sitelinks search box)
- [ ] **Speakable** — on key content sections for voice search eligibility

---

## Part 4 — Multilingual SEO (EN/FR/AR)

### Hreflang Implementation ✓ verified
**Critical rule (verified 3-0):** Hreflang must be **bidirectional and self-referencing**. Every language page must list itself AND all other language versions. If page A references page B, page B must reference page A — otherwise Google ignores the tags.

For CAF's 3-language site, minimum 6 annotation pairs per page:

```html
<!-- On English page -->
<link rel="alternate" hreflang="en" href="https://copticaidfoundation.org/mission.html" />
<link rel="alternate" hreflang="fr" href="https://copticaidfoundation.org/fr/mission.html" />
<link rel="alternate" hreflang="ar" href="https://copticaidfoundation.org/ar/mission.html" />

<!-- On French page — must mirror exactly -->
<link rel="alternate" hreflang="en" href="https://copticaidfoundation.org/mission.html" />
<link rel="alternate" hreflang="fr" href="https://copticaidfoundation.org/fr/mission.html" />
<link rel="alternate" hreflang="ar" href="https://copticaidfoundation.org/ar/mission.html" />

<!-- On Arabic page — must mirror exactly -->
<link rel="alternate" hreflang="en" href="https://copticaidfoundation.org/mission.html" />
<link rel="alternate" hreflang="fr" href="https://copticaidfoundation.org/fr/mission.html" />
<link rel="alternate" hreflang="ar" href="https://copticaidfoundation.org/ar/mission.html" />
```

**Implementation method (verified):** For WordPress + Polylang, use XML sitemap method — most reliable for CMS environments.

**Language code rules (verified):** ISO 639-1 language code always first. Country code optional. Valid: `ar`, `ar-CA`, `fr`, `fr-CA`. Invalid: `CA` alone.

**Multilingual strategy (verified):** Arabic content should target Arabic-speaking diaspora broadly (Egypt, Morocco, Lebanon, Canada) — **not** Canada-only. Multilingual SEO is language-led, not region-led.

### HTML Direction ✓ verified (W3C + MDN primary sources)
**Critical rule:** RTL directionality for Arabic **must** use the HTML `dir` attribute — not CSS alone. CSS can supplement but cannot replace the semantic HTML attribute.

```html
<!-- Arabic pages -->
<html lang="ar" dir="rtl">

<!-- English/French pages -->
<html lang="en" dir="ltr">
<html lang="fr" dir="ltr">
```

Do NOT use CSS `direction: rtl` as the sole method — it fails when CSS doesn't load.

### Multilingual Audit Checklist
- [ ] `lang` attribute on `<html>` element for all 3 language versions
- [ ] `dir="rtl"` on Arabic pages HTML element
- [ ] Hreflang tags on all pages (bidirectional, self-referencing)
- [ ] Hreflang implemented via XML sitemap (WordPress/Polylang)
- [ ] FR and AR pages are full translations — not machine-translated stubs
- [ ] Arabic meta titles and descriptions written in Arabic script
- [ ] French meta titles and descriptions written in French
- [ ] URL structure consistent: `/fr/` prefix for French, `/ar/` prefix for Arabic

---

## Part 5 — GEO (Generative Engine Optimization)

**Research status:** GEO-specific claims did NOT survive adversarial verification in the 2026 research. The research base is thin and contradictory. No verified GEO-specific rules can be stated with confidence.

**What is known (from primary Google source):**
- Google has not published specific optimization criteria for AI Overviews beyond standard indexing and snippet eligibility
- The claim "no special optimization is needed beyond standard SEO" was refuted (0-3)
- The claim "structured content in 1-3 sentence blocks improves AI citation" was refuted (0-3)

**Best available guidance (unverified, apply with caution):**
- Strong E-E-A-T signals (verified credentials, transparent reporting, institutional links) are the best proxy for AI citation trust
- Content that directly answers questions performs better in AI-generated responses
- Named entities (bishop names, founder name, specific locations like Tanta) help AI systems identify and cite specific facts
- CRA registration links provide verifiable external authority signals

**CAF-specific GEO opportunities:**
- The founding story (Tanta → Montreal, Philip Girgis, 1989) is a unique, citable narrative
- Specific stats (7,150+ families, 728+ students, 98¢ of every dollar) are the type of concrete facts AI engines quote
- Church endorsements with named bishops give authority signals AI engines can verify

---

## Part 6 — AEO (Answer Engine Optimization)

**Research status:** AEO-specific claims also did NOT survive adversarial verification. Voice search and featured snippet optimization guidance was not supported by primary sources in 2026.

**Best available guidance (unverified):**
- FAQ sections with clear question/answer structure are eligible for FAQPage rich results
- The Give page FAQ is the highest-priority AEO candidate
- Questions should mirror actual search queries (e.g. "How do I donate to the Coptic Aid Foundation?")
- Answers should be concise (40–60 words) and self-contained

**CAF-specific AEO candidates:**
- "How to donate to a Canadian charity by Interac e-Transfer"
- "What is the Coptic Aid Foundation?"
- "How to volunteer with a Coptic charity in Montreal"
- "Is the Coptic Aid Foundation a registered charity?"

---

## Part 7 — Information Architecture (IA)

### IA vs Navigation ✓ verified (2-1)
IA is the **invisible underlying structure** — the relationships between content. Navigation is the UI layer built on top of it. Fixing navigation without fixing IA leaves structural problems unresolved.

**Current CAF site map (8 pages):**
```
Home
├── Mission
├── Impact & Programs (6 sub-programs)
├── Give
├── News & Media (5 tabs)
├── Get Involved
├── About
└── Contact
```

### Navigation Consistency ✓ verified (WCAG 2.2 SC 3.2.3)
Navigation elements appearing on multiple pages must occur in the **same relative order**. This is both a UX requirement (NNG) and a legal accessibility requirement (WCAG 2.2).

**Current CAF nav order:** Home · Mission · Impact · Give · News & Media · Get Involved · About · Contact
- [ ] Nav order identical on all 8 pages ✓ (synced via nav.html)
- [ ] Footer nav order consistent ✓
- [ ] Active page highlighted ✓
- [ ] Logo links to home on all pages ✓

### IA Audit Checklist

**Content hierarchy:**
- [ ] Each page has one clear primary purpose
- [ ] Most important content appears without scrolling
- [ ] Donate CTA visible on every page
- [ ] Programs described in consistent format across Impact page

**Labeling:**
- [ ] Navigation labels match page H1 headings
- [ ] Labels use familiar language (not internal jargon)
- [ ] "Give" is clear enough — consider "Donate" for older audience
- [ ] "Get Involved" is clear — consider "Volunteer" for directness

**Wayfinding:**
- [ ] Breadcrumbs on interior pages — **missing — add**
- [ ] Active nav item highlighted ✓
- [ ] Page title always visible ✓
- [ ] Back-to-top on long pages (Impact, Mission) — **missing — add**

**Donor journey (critical path):**
- [ ] Home → Give: maximum 1 click ✓
- [ ] Home → Mission: 1 click ✓
- [ ] Give page has 3 donation methods clearly separated ✓
- [ ] Trust signals (CRA links, 98¢ stat) visible on Give page ✓
- [ ] No dead ends — every page has a next action ✓

### IA Research Methods (when redesigning) ✓ verified
When testing the IA before the WordPress build:

**Card sorting (use to discover):**
- **Open card sorting** — ask donors to group and label the 8 pages themselves → reveals their mental model
- **Closed card sorting** — ask donors to sort content into the existing 8 categories → validates current labels
- **Hybrid** — ask donors to sort into existing categories but allow them to create new ones

**Tree testing (use to validate):**
- Build a text-only tree of the current site structure
- Give donors specific tasks: "Find where to donate by Interac e-Transfer"
- Measures findability without visual design confounds
- Run after card sorting — card sorting informs, tree testing validates

Note: No validated participant sample size guidance survived research verification. Consult Optimal Workshop or NNG directly for current guidance.

### RTL/Multilingual IA ✓ verified
- [ ] Arabic pages use `dir="rtl"` on `<html>` element — **not CSS only** ✓ (already in ar/index.html)
- [ ] Language switcher visible and consistent on all pages ✓
- [ ] Language switcher labels in native script: English · Français · العربية ✓
- [ ] Nav order flips for RTL: right-aligned, reversed visual order
- [ ] All UI components (forms, tables, breadcrumbs) mirror for RTL

### WCAG 2.2 Accessibility IA Checklist ⚠
- [ ] SC 3.2.3 Consistent Navigation — same nav order on all pages ✓
- [ ] SC 2.4.1 Bypass Blocks — skip-to-content link
- [ ] SC 2.4.6 Headings and Labels — descriptive headings ✓
- [ ] SC 1.4.3 Contrast — text contrast ≥ 4.5:1 (check green #06a64f on white)
- [ ] SC 2.5.3 Label in Name — visible labels match accessible names
- [ ] Focus indicators visible on all interactive elements
- [ ] All images have alt text
- [ ] Forms have associated labels (contact form, subscribe form)

---

## Part 8 — CAF-Specific Audit Rules

These rules apply only to the Coptic Aid Foundation and synergize with `/caf_skill`:

### Trust signals checklist
- [ ] CRA Business Number (BN: 868786054RC0001) in footer ✓
- [ ] CRA charity details link on Give page ✓
- [ ] "98¢ of every dollar" stat visible on home and Give ✓
- [ ] Board of directors named ✓
- [ ] Founding year and story present ✓
- [ ] Church endorsements named with titles ✓
- [ ] Annual report / T3010 filing linked — **missing**
- [ ] Financial transparency statement — **missing**

### Multilingual content parity
- [ ] All 3 languages have equivalent content — not just translation stubs
- [ ] Stats identical across all 3 languages
- [ ] Donation instructions (Interac, PayPal) in all 3 languages
- [ ] Arabic content targets diaspora broadly (Egypt, Morocco, Lebanon, Canada)

### Local SEO — Montreal
- [ ] Google Business Profile created and verified
- [ ] NAP consistent across all pages: 9520 Boul. de l'Acadie, Bureau 229, Montreal, QC H4N 1L8, (514) 334-9792
- [ ] Facebook page linked from website ✓
- [ ] Schema contactPoint includes availableLanguage: English, French, Arabic

### Content freshness
- [ ] Announcements section updated regularly ✓ (on home page)
- [ ] Newsletter archive updated monthly (News & Media)
- [ ] Stats updated when board confirms new figures
- [ ] Bishop endorsement videos added as they become available

---

## Part 9 — Scoring Rubric

Run a full audit and score each section:

| Dimension | Items | Score /10 |
|---|---|---|
| Technical SEO | 12 checklist items | |
| On-Page SEO | 15 checklist items | |
| Structured Data | 6 checklist items | |
| Multilingual SEO | 8 checklist items | |
| GEO | 5 checklist items | |
| AEO | 4 checklist items | |
| IA — Navigation & Structure | 10 checklist items | |
| IA — Accessibility | 8 checklist items | |
| CAF Trust Signals | 8 checklist items | |
| **Total** | **76 items** | **/10** |

**Scoring guide:**
- 9–10: Excellent — publish-ready
- 7–8: Good — minor fixes before launch
- 5–6: Needs work — address before public promotion
- Below 5: Critical — significant gaps affecting trust and findability

---

## Part 10 — Known Gaps & Future Research

These topics were researched but produced **zero verified claims** — additional research needed:

- Mobile-first IA patterns for nonprofit websites
- IA audit scoring frameworks
- Breadcrumb and wayfinding pattern best practices
- Donation page conversion rate factors tied to IA
- GEO optimization signals for AI search engines (Perplexity, ChatGPT, Gemini)
- AEO / voice search optimization
- Montreal-specific local SEO for charities
- Participant sample sizes for card sorting studies

---

## Sources (verified claims only)

| Source | Type | Used for |
|---|---|---|
| https://developers.google.com/search/docs/specialty/international/localized-versions | Primary | Hreflang rules |
| https://developers.google.com/search/docs/appearance/structured-data/organization | Primary | Organization schema |
| https://schema.org/NonprofitOrganization | Primary | Nonprofit schema |
| https://developer.chrome.com/docs/lighthouse/performance/performance-scoring | Primary | Lighthouse scoring |
| https://www.w3.org/TR/WCAG22/#consistent-navigation | Primary | WCAG 2.2 SC 3.2.3 |
| https://www.w3.org/International/questions/qa-html-dir | Primary | RTL dir attribute |
| https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/dir | Primary | RTL dir attribute |
| https://www.nngroup.com/articles/ia-vs-navigation/ | Primary | IA vs navigation |
| https://www.nngroup.com/articles/card-sorting-definition/ | Primary | Card sorting |
| https://www.nngroup.com/articles/tree-testing/ | Primary | Tree testing |
| https://ahrefs.com/blog/hreflang-tags/ | Secondary | Hreflang implementation |
| https://ahrefs.com/blog/eeat/ | Secondary | E-E-A-T signals |
