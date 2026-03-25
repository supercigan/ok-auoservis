# DNA — O.K. Autoservis & Pneuservis

**Typ projektu:** Jednostránkový web autoservisu (landing page)
**Klient:** O.K. Autoservis, Uherské Hradiště
**Datum dokončení:** 2026-03-25

---

## Vizuální archetype

**Raw Automotive Power** — Carbon black + racing red. Technický grid vzor v hero, masivní kondenzovaná typografie, info panel místo prázdného prostoru. Celkový dojem: agresivní, rychlý, profesionální autoservis — ne kancelář.

---

## Barevná paleta

| Proměnná        | Hex       | Role                              |
|-----------------|-----------|-----------------------------------|
| `--carbon`      | `#141416` | Hero, nav scrolled, footer        |
| `--carbon-mid`  | `#1E1E22` | Why sekce, stats                  |
| `--carbon-soft` | `#2A2A30` | Bordery na tmavém pozadí          |
| `--red`         | `#C8202A` | Primární akcent — automotive red  |
| `--red-d`       | `#A61920` | Hover                             |
| `--red-l`       | `#FDECED` | Světlé pozadí ikon                |
| `--silver`      | `#9EA8B4` | Sekundární text na tmavém         |
| `--slate`       | `#F0F2F5` | Světlé sekce pozadí               |
| `--white`       | `#FFFFFF` | Čistá bílá                        |
| `--text-dark`   | `#141416` | Hlavní text                       |
| `--text-mid`    | `#505A66` | Sekundární text                   |
| `--text-light`  | `#8892A0` | Potlačený text                    |
| `--border`      | `#DDE2E8` | Bordery na světlém                |

**Charakter palety:** Studená industriální — carbon + automotive red. Žádné teplé tóny, žádná modrá ani zelená.

---

## Typografie

| Řez     | Font        | Použití                                    |
|---------|-------------|--------------------------------------------|
| Nadpisy | Bebas Neue  | H1–H4, nav logo, sekce labely, stat čísla  |
| Tělo    | Barlow 400/500 | Odstavce, popisky, formulář             |

- H1 hero "O.K.": `clamp(5rem, 14vw, 11rem)`, line-height 0.9
- H2: `clamp(2.2rem, 4vw, 3.5rem)`, letter-spacing 0.04em
- Section label: Barlow 0.72rem, 600, letter-spacing 0.22em, uppercase, červená
- Bebas Neue je single-weight (400) — font-weight deklarace nemají efekt

---

## Layout a struktura sekcí

```
1. NAV          — Fixed, průhledný → carbon + červená border-bottom při scrollu
2. HERO         — Grid textura (technický výkres), masivní "O.K." vlevo,
                  info panel vpravo (hodiny, adresa, tel, tagy)
                  Červená racing stripe bottom (hero::after 4px)
3. AUTOSERVIS   — 8 karet v gridu 4×2, bílé karty s červenou top border na hover
4. PRODEJ       — 3 karty: MOBIL oleje, Ford dovoz, Ford originální díly
5. KLIMATIZACE  — Tmavá carbon sekce, ghost "AC" text pozadí, ceník chladiv
6. PNEUSERVIS   — Světlá slate sekce, 3 karty (Osobní / Dodávky / Nákladní)
7. PROČ MY      — Dark carbon-mid, 4 benefity s čísly 01–04
8. KONTAKT      — Split: kontakt+hodiny vlevo, formulář vpravo, bílé pozadí
9. FOOTER       — 3 sloupce carbon, červená border-top
```

---

## Klíčové UI vzory

- **Hero grid textura:** `repeating-linear-gradient` mřížka 64×64px, opacity 0.025 — evokuje technický výkres
- **Hero info panel:** poloprůhledný rámeček vpravo s reálnými info (hodiny, adresa, tel, service tagy)
- **Section label:** červená linka 36px nahoře + Barlow uppercase 0.72rem
- **Service karty:** červená top border scaleX(0→1) na hover + translateY(-3px) — bez spotlight efektu
- **Karty v gridu:** oddělené 1.5px borderem (background: var(--border) + gap: 1.5px)
- **Ghost text:** v klimatizace sekci "AC" absolutně pozicované, opacity 0.025
- **Fade-up:** IntersectionObserver, d1–d8 delay třídy (0.1–0.8s)
- **Tlačítka:** border-radius 4px (mírně hranaté, ne capsule)
- **Pneuservis ikony:** červené solid square s bílou ikonou (odlišné od service karet)

---

## Technický stack

- Čistý HTML/CSS/JS — jeden soubor `index.html`
- Google Fonts (Bebas Neue + Barlow)
- Formulář: Formspree (ID nutno doplnit — placeholder `YOURFORMID`)
- Deploy: GitHub → supercigan/ok-auoservis → Vercel (napojit)

---

## Co se osvědčilo

- Hero info panel vpravo — vyplní dead space a zároveň hned ukáže klíčové info
- Bebas Neue pro display titulky — výrazně ostřejší než Barlow Condensed
- Grid textura v hero — subtilní, evokuje technické výkresy, odlišuje od canvas animací
- Racing stripe (4px red border-bottom) na hero — jednoduchý ale efektní detail
- Carbon + red kombinace — dostatečně agresivní pro autoservis, ale čistá a profesionální

## Co se nepovedlo / co příště udělat jinak

- Ikony při prvním generování byly zcela nesmyslné (slunce pro opravy, hvězda pro nehody, srdce pro oleje) — příště projít ikony systematicky před prvním commitem
- Screenshoty z audit session nepatří do gitu — přidat `.gitignore` pro `_project-memory/*.png`
- FORD brand barva (#003399 modrá) clashovala s paletou — inline styly na brand labels jsou past, používat CSS třídy
