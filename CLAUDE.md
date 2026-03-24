# CLAUDE.md

This file provides guidance to Claude Code when working on the Causuals VDR landing page variant.

## Project

**VDR Landing Page — Causuals variant** — personalized landing page for Richard Hořejší / law firm Causuals. Derived from the generic VDR landing page (`vdr-landing` repo) with expanded feature set per `VDR_navrh_reseni_pro_Causuals_v3_260324.docx`.

**Language:** Czech (čeština) for all content, English for code and technical docs.

## Stack

Static HTML/CSS/JS — no framework, no build step. Identical design system as `vdr-landing`.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Personalized landing page for Causuals (expanded features) |
| `ab-ante-logo.png` | AB ANTE logo (RGB, 2000x977px) |
| `CLAUDE.md` | This file — context for Claude Code |
| `README.md` | Project description and deploy info |

## Design System (inherited from vdr-landing)

- **Fonts:** Source Serif 4 (headings, weight 400), DM Sans (body text)
- **Colors:** Navy `#1A2E4A` (hero, CTA), Copper `#D4722A` (accent, buttons), Cream `#FAFAF8` (bg), Sand `#F4F2EE` (alt sections), White (nav, footer)
- **Nav & Footer:** White background with full-color logo (42px height), navy/muted text
- **Typography:** Fluid via `clamp()` — H1 scales 36–72px, H2 scales 28–42px
- **Container:** 1400px max-width (1600px for nav)
- **Pattern:** Trust & Authority — clean, minimal, professional B2B

## Content Sections

1. **Hero** — elevator pitch pro Causuals + 4 stat boxy (4 role, AI nástroje, Cloud sync, ~1 100 Kč)
2. **Problem** — 3 karty (ad-hoc email/cloud, Excel checklisty, drahé komerční VDR)
3. **Features** — 8 karet ve 2-sloupcovém gridu s badgemi Základ/Volitelný modul
4. **How it works** — 3 kroky (založit transakci, pozvat účastníky, sdílet pod kontrolou)
5. **Security** — 4 položky (RLS izolace, tamper-evident audit, AES-256 + TLS 1.3 + EU hosting, vodoznaky + odebrání přístupu)
6. **CTA** — "Pojďme to projít společně" + kontakty (Jankovský, Žemlička)

**Odstraněné sekce:** Orientační provozní náklady (cenová diskuse probíhá offline).

## Content Differences vs. Generic Landing

This variant is personalized for Causuals and includes:

1. **Extended features (8 cards):** + Secure Viewer, Cloud sync (Drive + OneDrive), AI kategorizace, Full-text search
2. **Microsoft OAuth** mentioned alongside Google OAuth
3. **AI module** as a differentiator (PII detection, DD index categorization)
4. **Security section** expanded with AES-256, TLS 1.3, EU hosting (Frankfurt)
5. **Direct address** to Richard / Causuals — personalized tone
6. **No pricing section** — cost discussion happens offline, not on the page

## Responsive Design

Tested and verified 2026-03-24. Breakpoints: 960px (tablet), 640px (mobile).

| Viewport | Layout | Nav | Grids |
|----------|--------|-----|-------|
| Desktop (1440px) | Multi-column | Full links | 2-col features, 3-col problems/steps |
| Tablet (768px) | Adapted | Hamburger | 2-col features/problems, 1-col security |
| Mobile (375px) | Single-column | Hamburger | All 1-column, full-width CTA buttons |

No horizontal overflow at any viewport. All grids collapse correctly.

## Source Document

Content adapted from: `Virtual DataRoom_pro RH/VDR_navrh_reseni_pro_Causuals_v3_260324.docx` (Verze 3.0, Březen 2026)

## Deploy

Dual deployment:

| Target | URL | Method |
|--------|-----|--------|
| **Vercel** | https://landing-causuals.vercel.app | `vercel --prod` from `landing-causuals/` |
| **FORPSI (ab-ante.cz)** | https://ab-ante.cz/causuals/ | `lftp` to `d112wh.forpsi.com` → `/causuals/` |

Branch: `feature/vdr-causuals-landing` in repo `website-ABA_data-analyze`.
