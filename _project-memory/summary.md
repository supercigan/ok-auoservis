# OK Autoservis — Project Summary

**Název projektu:** O.K. Autoservis & Pneuservis
**Datum zahájení:** 2026-03-25
**GitHub:** https://github.com/supercigan/ok-auoservis
**Klient:** O.K. Autoservis | ksaautoservice@seznam.cz | +420 776 072 890

---

## Co je hotovo

- [x] Vytvořen `_project-memory/summary.md`
- [x] Přečteny všechny DNA soubory (M-Autoservis, Zámečnictví, Centrum Zdraví, Kosmetický salon, Pedikúra)
- [x] Scraping okautoservis.cz — všechny sekce, služby, kontakt, ceník klimatizace
- [x] Navržena unikátní paleta a fonty (liší se od všech předchozích projektů)
- [x] Vytvořen kompletní `index.html` — jednostránkový web
- [x] GitHub repo vytvořeno a kód pushnutý na master

## Struktura webu

```
NAV       → Fixed, průhledný → carbon při scrollu, červená border-bottom
HERO      → Grid textura, masivní "O.K." titulek, červená racing stripe
STATS     → 4 stat items: 20+ let, 8 služeb, 60' klima, 2 dny STK
AUTOSERVIS → 8 karet ve 4×2 gridu (bílé karty, červená top border na hover)
KLIMATIZACE → Tmavá sekce, ceník R134a/R1234yf/připojení, garance 60 min
PNEUSERVIS → 3 karty: Osobní, Dodávky, Nákladní
PROČ MY   → Dark carbon, 4 benefits s čísly 01–04
KONTAKT   → Split: kontakt+hodiny vlevo, formulář vpravo
FOOTER    → 3 sloupce: brand | navigace | hodiny
```

## Vizuální identita

**Archetype:** Carbon & Racing Red — "Raw Automotive Power"

**Paleta:**
- `--carbon: #141416` — hero, nav, footer
- `--red: #C8202A` — primary accent
- `--slate: #F0F2F5` — světlé sekce

**Fonty:**
- Barlow Condensed 800 — nadpisy (nepoužit v žádném předchozím projektu)
- Barlow 400/500 — tělo

**Hero dekorace:** CSS grid texture (technický výkres) + červená bottom racing stripe

**Karty:** červená top border scaleX na hover (ne spotlight, ne lightbox)

---

## Co se řeší

- Formspree ID není nastaveno — je tam placeholder `YOURFORMID`
- Fotky nejsou k dispozici — hero je čistě typografický

---

## Důležitá rozhodnutí

- Paleta Carbon+Red zvolena jako maximálně odlišná od M-Autoservis (navy+amber) i ostatních
- Barlow Condensed jako font — motorsport, kondenzovaný, industriální — neobjevuje se v žádné DNA
- Klimatizace dostala vlastní sekci s ceníkem (bylo prominentně na původním webu)
- Hero: masivní "O.K." jako display element — brand jméno samo se stává vizuálem
- Pneuservis: 3 samostatné karty pro osobní/dodávky/nákladní (až 12 tun)
- Grid textura hero = odlišení od canvas animace (M-Autoservis) a SVG linií (Zámečnictví)

---

## Příští kroky

- [ ] Nastavit Formspree ID (nebo jiný email backend)
- [ ] Ověřit s klientem otevírací dobu (aktuálně Po–Pá 8:00–16:00)
- [ ] Případně doplnit fotky vozidel/dílny
- [ ] Napojit Vercel na GitHub repo
- [ ] Vytvořit DNA soubor po dokončení projektu
