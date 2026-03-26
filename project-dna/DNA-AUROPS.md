# DNA — AUROPS s.r.o.

**Typ projektu:** Jednostránkový web autoservisu + havárijní služba (landing page)
**Klient:** AUROPS s.r.o. (servisní partner: UH CAR, s.r.o.)
**Datum dokončení:** 2026-03-26
**GitHub:** supercigan/AUROPS

---

## Vizuální archetype

**Speed & Precision / Emergency** — Téměř černé void pozadí s razantní signal oranžovou. Animated diagonal speed lines v hero evokují pohyb a rychlost. Oranžová jako automotive signální barva — urgentní, přímá, energická. Celkový dojem: profesionální autoservis s 24/7 pohotovostní službou — vzbuzuje důvěru i pocit naléhavosti.

---

## Barevná paleta

| Proměnná       | Hex       | Role                                       |
|----------------|-----------|--------------------------------------------|
| `--void`       | `#0C0E12` | Hero, nav scrolled, footer, hlavní tmavá   |
| `--void-mid`   | `#141720` | Tmavé sekce (Proč my)                      |
| `--void-soft`  | `#1C2030` | Jemné tmavé prvky                          |
| `--orange`     | `#F05F2E` | Primární akcent — signal orange            |
| `--orange-d`   | `#C94A1F` | Hover oranžové                             |
| `--orange-l`   | `#FEF0EA` | Světlé oranžové plochy (ikony, záhlaví)    |
| `--orange-ll`  | `#FFF9F6` | Extra světlé oranžové pozadí               |
| `--ash`        | `#F2F4F8` | Světlé sekce (services, contact bg)        |
| `--ash-d`      | `#E4E8F0` | Bordery na světlém                         |
| `--white`      | `#FFFFFF` | Čistá bílá (karty, formulář)               |
| `--text-dark`  | `#0C0E12` | Hlavní text                                |
| `--text-mid`   | `#4A5168` | Sekundární text                            |
| `--text-light` | `#8890A4` | Potlačený text                             |
| `--border`     | `#DDE2EC` | Bordery                                    |

**Charakter palety:** Void near-black + signal orange. Jeden akcent, žádná sekundární barva. V kontextu DNA projektů zcela unikátní — žádný předchozí projekt nepoužil čistou signální oranžovou.

---

## Typografie

| Řez     | Font    | Použití                                         |
|---------|---------|-------------------------------------------------|
| Nadpisy | **Sora**   | H1–H4, nav logo, section labels, tlačítka    |
| Tělo    | **Outfit** | Odstavce, popisky, formulář, navigace        |

- H1: `clamp(2.8rem, 5.5vw, 4.8rem)`, weight 800, line-height 1.15
- H2: `clamp(2rem, 3.8vw, 3rem)`, weight 700
- H3: `clamp(1rem, 1.8vw, 1.15rem)`, weight 700
- Section label: 0.72rem, letter-spacing 0.22em, uppercase, orange linka 32px vlevo (2px)
- Tlačítka: Sora 0.9rem, weight 600, border-radius 8px
- **Nav logo text: 1.65rem / 800** — osvědčená proporce
- **Nav logo ikona: 40×40px, SVG 22×22px** — kompaktní, oranžový čtverec s bílým trojúhelníkem + oranžový vnitřní trojúhelník

---

## Layout a struktura sekcí

```
1. NAV            — Fixed, průhledný → void při scrollu, hamburger na mobilu
2. HERO           — Animated diagonal speed lines (CSS), badge s pulsující tečkou,
                    H1 "Kompletní servis vašeho vozidla" (accent na "vozidla"),
                    sub-heading, 2 CTA, hero-bottom info bar (havárie/provoz/partner)
3. EMERGENCY STRIP — Full-width orange banner, 2 velká tel. čísla — KLÍČOVÁ sekce
4. SLUŽBY         — 12 karet 4×3 grid (padding: 4rem 5% 5rem)
                    Orange left-border scaleY(0→1) on hover + translateY(-4px)
5. PROČ MY        — Void-mid sekce, 4 benefity číslované 01–04 (opacity 0.35)
6. KONTAKT        — Split: info panel vlevo / formulář vpravo (ash bg)
7. FOOTER         — 3 sloupce: brand+popis | navigace | kontakt
8. WATERMARK      — SVG tiled pattern fixed overlay (dual-layer, viz níže)
```

---

## Klíčové UI vzory

- **Animated diagonal speed lines:** `repeating-linear-gradient(-62deg)` + CSS `transform: translate` animation (14s linear infinite) — evokuje pohyb/rychlost, CSS-only, **nikdy dříve nepoužito v DNA projektech**
- **Hero shape:** Diagonal orange gradient polygon na pravé straně (clip-path) + radial orange glow bottom-right
- **Hero badge:** pill `rgba(240,95,46,0.1)` border, pulsující tečka `@keyframes blink`
- **Emergency strip:** Full-width orange, 2 tel. čísla Sora 800 1.25rem — jednoznačný signál dostupnosti
- **Section label:** orange linka 32px/2px vlevo + Outfit uppercase 0.72rem 0.22em tracking
- **Service karty:** 4×3 grid oddělený 1.5px borderem, `display:flex; flex-direction:column; align-items:flex-start`, left-border scaleY na hover + translateY(-4px)
- **Why čísla:** 01–04 Sora 3.2rem 800, color orange, opacity 0.35 — viditelná kotva tmavé sekce
- **Fade-up animace:** IntersectionObserver, delay třídy d1–d6 (0.1–0.6s), threshold 0.12
- **Tlačítka:** border-radius 8px, primary orange + ghost white border
- **Watermark (dual-layer):** SVG `<pattern>` 280×150px, rotate(-28deg), tmavá vrstva `rgba(0,0,0,0.09)` + světlá `rgba(255,255,255,0.09)` — viditelný na obou typech pozadí

---

## Ikony — přehled a zdůvodnění

| Služba | Feather icon path | Proč |
|--------|-------------------|------|
| Předprodejní prohlídka | `<circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/>` | Lupa = hledání/inspekce |
| Kompletní servis | wrench path | Klasický nástroj = servis |
| Geometrie kol 3D | crosshair (circle + 4 lines) | Zaměřovač = přesnost/alignment |
| Tlumiče a podvozek | sliders (parallel lines + crossings) | Nastavení/regulace = tlumič |
| PC Diagnostika OBD | monitor + stand | Počítač = diagnostika |
| Diagnostika Citroën | **shield-check** | Štít s fajfkou = certifikovaný specialista |
| Multi-brand diagnostika | layers (stacked polygons) | Vrstvy = více značek |
| Karoserie a lak | pencil/edit | Tužka = úprava/oprava povrchu |
| Elektroinstalace | zap/lightning | Blesk = elektřina |
| Klimatizace | wind lines | Vzduch = klimatizace |
| Výměna autoskel | **windshield trapezoid + wiper arc** | Trapézoid = čelní sklo, oblouk = stěrač |
| Tažná zařízení | chain/link | Řetěz/spoj = tažné zařízení |

---

## Watermark — technické detaily

```html
<!-- position: fixed, z-index: 9999, pointer-events: none -->
<svg>
  <pattern id="wm-dark" width="280" height="150" patternTransform="rotate(-28)">
    <text fill="rgba(0,0,0,0.09)">Demoverze – Tomáš Smolík</text>
  </pattern>
  <pattern id="wm-light" width="280" height="150" patternTransform="rotate(-28)">
    <text fill="rgba(255,255,255,0.09)">Demoverze – Tomáš Smolík</text>
  </pattern>
  <rect fill="url(#wm-dark)"/>
  <rect fill="url(#wm-light)"/>
</svg>
```

Smazání: odstranit celý `<div id="watermark">` blok.

---

## Technický stack

- Čistý HTML/CSS/JS — jeden soubor `index.html`
- Google Fonts (Sora + Outfit)
- Formulář: lokální simulace (success stav bez odesílání) — Formspree nutno doplnit
- Deploy: GitHub → supercigan/AUROPS → Vercel (automaticky z master)

---

## Co se osvědčilo

- **Signal orange na void dark** — v kontextu všech DNA projektů zcela unikátní, silný a okamžitě zapamatovatelný
- **Sora + Outfit** — oba fonty nové v DNA, Sora má geometrickou preciznost vhodnou pro technický autoservis
- **Animated diagonal speed lines** — subtilní CSS animace bez canvas, evokuje pohyb/rychlost
- **Emergency strip** — nejdůležitější rozhodnutí: havárijní čísla prominentně hned za hero
- **Dual-layer watermark** — tmavá + světlá vrstva současně = viditelný na jakémkoli pozadí

## Co příště udělat jinak

- Adresa AUROPS není na původním webu — příště zjistit před spuštěním
- E-mail taktéž chybí — příště ověřit s klientem
- Puppeteer screenshoty: fade-up elementy mají opacity:0 a IntersectionObserver se nespustí bez scrollu → vždy injektovat `style: '.fade-up { opacity:1!important; transform:none!important }'` před screenshotem
