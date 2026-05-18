# SLB Capital Advisors — Website Redesign Spec (v1)

**Status:** Draft  
**Date:** 05.18.2026  
**Approach:** Evolved version of current site — preserve brand identity, tighten layout, modernize details  
**Next step:** HTML/CSS prototype based on this spec

---

## Design Philosophy

The current site is clean and professional but passive — it presents information rather than making an argument. The evolved version should feel more *confident and deliberate*: tighter spacing, stronger typographic hierarchy, and sections that each make a distinct point rather than just filling space.

Reference aesthetic cues: Ironwood (quantified credibility, icon-driven value props, team grid), Silver Oak (bold hero statement, credential stats, testimonials).

---

## Color Palette

Confirmed hex values pulled from live site CSS (05.18.2026):

| Role | Name | Hex | Notes |
|---|---|---|---|
| Primary accent / CTA | Blue | `#1270C3` | Links, buttons, nav dropdown bg |
| Dark bg / footer | Dark Blue | `#06121D` | Near-black; use for footer, dark hero overlay |
| Soft accent | Light Blue | `#9BC4E5` | Hover states, secondary highlights |
| Section alternate bg | Light Gray | `#EFF4F8` | Subtle section break (already in use) |
| Secondary text | Gray | `#72716F` | Captions, metadata, supporting copy |
| Body text | Black | `#000000` | Primary text |
| Background | White | `#FFFFFF` | Page background |
| Nav underline / dividers | Light Gray | `#C3C4C6` | Hairline rules (from computed nav styles) |

No new colors introduced. Disciplined use of existing palette only.

---

## Typography

Current site uses **DIN** (geometric sans-serif) for everything — headings and body. Evolving to a mixed pairing:

| Role | Selection | Notes |
|---|---|---|
| Headings (H1–H3) | **Playfair Display** (serif) | Signals expertise and permanence; clear upgrade from DIN headings |
| Body / UI / Nav | **DIN → Inter** | Keep DIN feel but upgrade to Inter for better web rendering and weight range |
| Monospace | Not needed | |

Typographic hierarchy: H1s large and commanding (~56–64px), body generous at 17–18px, captions/metadata clearly subordinate. The serif/sans pairing is the primary visual upgrade over the current site.

---

## Navigation

**Current:** Why SLB / What We Do / The Team / Insights / Media / Contact  
**Proposed changes:** Minor — see below

- Sticky header on scroll (if not already); subtle shadow or border to separate from content
- Consolidate **Media** into **Insights** as a content type filter — reduces nav clutter, strengthens the Insights hub
- Revised nav: **Why SLB · What We Do · The Team · Insights · Contact**
- Add **Case Studies / Rep Transactions** as a nav item or sub-item under What We Do — surfaces the tombstone library at the top level
- Mobile: hamburger menu with full-screen overlay, not a side drawer

---

## Page-by-Page Layout

### Homepage

**1. Hero**
- Full-width, high-quality aerial/architectural photo (city skyline or commercial real estate) with dark navy overlay
- Large serif headline — e.g., *"A Different Kind of Firm. A Singular Focus."* (existing line, already strong)
- One-sentence subhead expanding on the SLB focus
- Single CTA button: "What We Do" — not "Contact Us" (too transactional for first touch)
- No carousel/slider — static, confident

**2. Credentials Bar** *(new section, inspired by Ironwood/Silver Oak)*
- Thin horizontal band, light gray background
- 3 stats side by side: transactions closed, volume, property types covered
- Placeholder: `10+ Transactions Closed · $100M+ in Transaction Volume · 10+ Property Types`
- Anchors credibility before the visitor reads another word

**3. The SLB Difference** *(evolved from current "Why SLB")*
- 3-column icon + headline + 2-sentence description layout
- Topics: Investment banking expertise applied to real estate / Seller-only representation / Deep buyer relationships
- Iconography: simple, line-based, not clip art — matches the minimal tone

**4. What We Do** *(property type coverage + capabilities)*
- Short capabilities blurb first (2–3 sentences): investment banking expertise applied to real estate, seller-only representation, M&A-light positioning — the nuance that differentiates SLB
- Below: property type tile grid — Restaurant / Manufacturing / Healthcare / Data Centers / Distribution / Industrial / etc.
- Each tile: simple line icon + label; clicking expands or links to a dedicated page
- End with: "We've closed transactions across 10+ property types" — ties back to credentials bar

**5. Representative Transactions** *(filterable tombstone display)*
- 3 tombstones shown at a time, randomly selected from the library on each load
- Filter bar above: by property type — pill buttons
- "View All Transactions" link below opens the full public library (no gate)
- Each tombstone: property type label, deal description (tenant name if public, otherwise generic e.g. "Restaurant Portfolio"), transaction size, location, close year
- Placeholder tombstones: "Restaurant Portfolio", "Manufacturing Facility", "Distribution Center", "Healthcare Facility", "Industrial Portfolio", "Net Lease Retail"
- Clean card format — no heavy borders, just subtle shadow and rounded corners

**6. Insights Preview** *(teaser section)*
- 3 most recent Insights articles in a horizontal card layout
- Each card: category tag (Article / Media / Report), headline, author byline, date, Read More link
- Section headline: "From the Desk of SLB" or "Insights"
- CTA at bottom: "View All Insights"

**7. Footer**
- Dark navy background (matches hero — bookends the page)
- 3-column layout: Logo + tagline / Navigation links / Contact info
- Add: LinkedIn link, legal/privacy links
- Copyright line at very bottom

---

### Insights Hub *(consolidates Insights + Media into one destination)*

**Current:** Separate Insights and Media nav items  
**Evolved:** Single "Insights" nav item — filter by content type (Articles / Media / Reports)

- Filterable by content type: Articles / Media / Reports
- Keyword search bar
- Author attribution on every post (author name, headshot thumbnail, title)
- Category/tag pills on each article card
- Featured article at top (larger card, hero image)
- Pagination or infinite scroll below

---

### The Team

**Current:** Likely bio text blocks  
**Evolved:**

- Photo grid layout — consistent headshots, not mixed sizes
- Name, title, and one-line credential under each photo
- Click opens full bio (modal or dedicated page)
- Bio page includes: full background, deal experience highlights, education, LinkedIn link
- Author attribution links back here from Insights articles

---

### What We Do / Rep Transactions

- Dedicated page for the full transactions library (currently may not exist or be limited)
- Full filterable grid: all closed deals with property type, tenant, size, geography
- Can be gated (name/email form) as an optional future enhancement
- Supports the AI SEO strategy — keyword-rich transaction pages indexed by Google

---

### Contact

- Simple, clean form: Name / Company / Email / Phone / Message
- No generic stock photo backgrounds
- Direct contact info visible alongside the form (not buried in footer)
- HubSpot form integration (already in use for NDA workflows)

---

## Functional Enhancements (Carry Forward from RFP)

These were already scoped and should be wired in:

| Feature | Notes |
|---|---|
| Filterable Rep Transactions | See homepage section above + standalone page |
| Insights keyword search + content-type filter | Insights Hub section above |
| Self-service CMS | Vendor to spec — WordPress or Webflow preferred |
| JSON-LD schema markup | FAQPage, Organization, FinancialService, Article |
| Meta descriptions | All pages |
| Image alt text audit | All images |
| Author attribution | Insights articles + team bios |

---

## What This Spec Does NOT Include

- Copywriting (all content provided by SLB per RFP scope)
- New branding / logo changes
- Gated content / lead capture forms (optional future phase)
- Mobile-specific wireframes (prototype phase)

---

## Decisions Locked

| Decision | Choice |
|---|---|
| Hero background | Photo (aerial/architectural) with dark navy overlay |
| Credentials bar stats | 10+ Transactions Closed · $100M+ Volume · 10+ Property Types |
| Tombstone placeholders | Restaurant Portfolio, Manufacturing Facility, Distribution Center, Healthcare Facility, Industrial Portfolio, Net Lease Retail |
| Rep Transactions library | Public — no gate |
| Media nav item | Folded into Insights hub (filter by Articles / Media / Reports) |
| What We Do section | Capabilities blurb + property type tile grid |
| Heading font | Playfair Display |
| Body font | Inter |

## Open Questions to Resolve Before Prototype

1. ~~**Actual hex values** for current SLB brand colors~~ — confirmed 05.18.2026

---

## Next Step

Build HTML/CSS prototype of the homepage using this spec. Start with: Hero → Credentials Bar → The SLB Difference → Rep Transactions preview → Footer.
