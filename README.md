# Virtual Data Room — Landing Page pro Causuals

Personalizovaná landing page produktu **AB ANTE Virtual Data Room** pro Richarda Hořejšího a právní kancelář **Causuals**.

Odvozeno z generické VDR landing page s rozšířeným obsahem dle dokumentu `VDR_navrh_reseni_pro_Causuals_v3_260324.docx`.

## Odkazy

| | URL |
|---|---|
| **Causuals (FORPSI)** | https://ab-ante.cz/causuals/ |
| **Causuals (Vercel)** | https://landing-causuals.vercel.app |
| **Generická landing page** | https://vdr-landing.vercel.app |
| **VDR aplikace (demo)** | https://virtual-data-room-fawn.vercel.app |
| **Zdrojový dokument** | `Virtual DataRoom_pro RH/VDR_navrh_reseni_pro_Causuals_v3_260324.docx` |

## Soubory

| Soubor | Popis |
|--------|-------|
| `index.html` | Personalizovaná landing page (rozšířené funkce, AI modul, cloud sync) |
| `ab-ante-logo.png` | Logo AB ANTE (RGB, 2000x977px) |
| `CLAUDE.md` | Kontext pro Claude Code |
| `README.md` | Tento soubor |

## Obsah stránky

1. **Hero** — elevator pitch pro Causuals + 4 stat boxy
2. **Problém** — 3 karty (ad-hoc sdílení, Excel checklisty, drahé komerční VDR)
3. **Funkce** — 8 karet s badgemi Základ / Volitelný modul
4. **Jak to funguje** — 3 kroky
5. **Bezpečnost** — 4 položky (RLS, audit log, AES-256/TLS 1.3/EU, vodoznaky)
6. **CTA** — kontaktní sekce

**Odstraněno:** Sekce nákladů (cenová diskuse probíhá offline).

## Obsah vs. generická verze

| Oblast | Generická | Causuals varianta |
|--------|-----------|-------------------|
| Cílení | Široký trh | Richard Hořejší / Causuals |
| Features | 6 karet | 8 karet (+ Secure Viewer, Cloud sync, AI, Full-text search) |
| Autentizace | Google OAuth + Magic Link | + Microsoft OAuth |
| AI modul | Nezmíněno | AI kategorizace DD indexu, detekce PII |
| Cloud sync | Nezmíněno | Google Drive + OneDrive synchronizace |
| Bezpečnost | 4 položky | + AES-256, TLS 1.3, EU hosting Frankfurt |
| Cena srovnání | ~1 500 vs 10-50 tis | Odstraněno — diskuse offline |

## Design

- **Styl:** Macaly-style AB ANTE brand (Trust & Authority) — shodný s generickou verzí
- **Fonty:** Source Serif 4 (nadpisy), DM Sans (body)
- **Barvy:** Navy `#1A2E4A`, Copper `#D4722A`, Cream `#FAFAF8`
- **Responzivní:** 3 breakpointy (desktop 1440px, tablet 960px, mobil 640px) — otestováno 2026-03-24

## Deploy

Stránka je nasazená na dvou místech:

| Cíl | URL | Metoda |
|-----|-----|--------|
| **FORPSI** (produkce) | https://ab-ante.cz/causuals/ | FTP via `lftp` → `d112wh.forpsi.com:/causuals/` |
| **Vercel** (záloha) | https://landing-causuals.vercel.app | `vercel --prod` z `landing-causuals/` |

FTP přístup viz `nasazeni na web_ftp/readme.md` v OneDrive AB ANTE.

## Kontakt

**AB ANTE s.r.o.** · Perucká 61/13, 120 00 Praha 2 · [ab-ante.cz](https://ab-ante.cz)

- Václav Jankovský · vaclav@ab-ante.cz · +420 775 262 645
- Jiří Žemlička · jirka@ab-ante.cz · +420 602 162 043
