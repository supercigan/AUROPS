# DNA — AUROPS s.r.o.

**Typ projektu:** Jednostránkový web autoservisu + havárijní služba (landing page)
**Klient:** AUROPS s.r.o. (servisní partner: UH CAR, s.r.o.)
**Datum dokončení:** 2026-03-26

---

## Vizuální archetype

**Speed & Precision / Emergency** — Téměř černé void pozadí s razantní signal oranžovou. Animated diagonal speed lines v hero evokují pohyb a rychlost. Oranžová jako automotive signální barva — urgentní, přímá, energická. Celkový dojem: profesionální autoservis s 24/7 pohotovostní službou — vzbuzuje důvěru i pocit naléhavosti.

---

## Barevná paleta

| Proměnná       | Hex       | Role                                       |
|----------------|-----------|--------------------------------------------|
| `--void`       | `#0C0E12` | Hero, nav scrolled, footer, hlavní tmavá   |
| `--void-mid`   | `#141720` | Tmavé sekce (Why AUROPS)                   |
| `--void-soft`  | `#1C2030` | Jemné tmavé prvky                          |
| `--orange`     | `#F05F2E` | Primární akcent — signal orange            |
| `--orange-d`   | `#C94A1F` | Hover oranžové                             |
| `--orange-l`   | `#FEF0EA` | Světlé oranžové plochy (ikony, záhlaví)    |
| `--orange-ll`  | `#FFF9F6` | Extra světlé oranžové pozadí               |
| `--ash`        | `#F2F4F8` | Světlé sekce (services)                    |
| `--ash-d`      | `#E4E8F0` | Bordery na světlém                         |
| `--white`      | `#FFFFFF` | Čistá bílá                                 |
| `--text-dark`  | `#0C0E12` | Hlavní text                                |
| `--text-mid`   | `#4A5168` | Sekundární text                            |
| `--text-light` | `#8890A4` | Potlačený text                             |
| `--border`     | `#DDE2EC` | Bordery                                    |

**Charakter palety:** Void near-black + signal orange. Žádná modrá, zelená, červená, amber — čistá oranžová jako jediný akcent. V kontextu DNA projektů zcela unikátní kombinace.

---

## Typografie

| Řez     | Font    | Použití                                         |
|---------|---------|-------------------------------------------------|
| Nadpisy | Sora    | H1–H4, nav logo, section labels, tlačítka       |
| Tělo    | Outfit  | Odstavce, popisky, formulář, navigace           |

- H1: `clamp(2.8rem, 5.5vw, 4.8rem)`, weight 800, line-height 1.15
- H2: `clamp(2rem, 3.8vw, 3rem)`, weight 700
- H3: `clamp(1rem, 1.8vw, 1.15rem)`, weight 700
- Section label: 0.72rem, letter-spacing 0.22em, uppercase, orange linka 32px vlevo
- Tlačítka: Sora 0.9rem, weight 600, border-radius 8px
- **Nav logo text: 1.65rem / 800** — osvědčená proporce
- **Nav logo ikona: 40×40px, SVG 22×22px** — kompaktní

---

## Layout a struktura sekcí

```
1. NAV            — Fixed, průhledný → void při scrollu
2. HERO           — Animated diagonal speed lines (CSS), badge, H1 + accent word,
                    subheading, 2 CTA, hero-bottom info bar (3 items)
3. EMERGENCY STRIP — Full-width orange banner, 2 phone numbers prominently (unikátní!)
4. SLUŽBY         — 12 karet 4×3 grid, orange left-border scaleY on hover
5. PROČ MY        — Void-mid sekce, 4 benefity číslované 01–04
6. KONTAKT        — Split: info panel vlevo / formulář vpravo (ash bg)
7. FOOTER         — 3 sloupce: brand+popis | nav | kontakt
```

---

## Klíčové UI vzory

- **Animated diagonal speed lines:** `repeating-linear-gradient(-62deg)` + CSS `transform: translate` animation — evokuje pohyb/rychlost, CSS-only, nikdy dříve nepoužito v DNA projektech
- **Hero shape:** Diagonal orange gradient polygon na pravé straně + radial orange glow bottom-right
- **Hero badge:** pill s pulsující tečkou + text o firmě
- **Emergency strip:** Full-width orange sekce hned za hero — 2 tel. čísla velkým Sora 800 písmem — jednoznačný signál urgentní dostupnosti
- **Section label:** orange linka 32px vlevo + Outfit uppercase 0.72rem 0.22em tracking
- **Service karty:** 4×3 grid oddělený 1.5px borderem, left-border scaleY(0→1) na hover + translateY(-4px)
- **Why čísla:** 01–04 v oranžové, opacity 0.18 — vizuální kotva tmavé sekce
- **Fade-up animace:** IntersectionObserver, delay třídy d1–d6 (0.1–0.6s)
- **Tlačítka:** border-radius 8px, primary orange + ghost white

---

## Technický stack

- Čistý HTML/CSS/JS — jeden soubor `index.html`
- Google Fonts (Sora + Outfit)
- Formulář: lokální simulace (bez odesílání)
- Deploy: GitHub → supercigan/AUROPS → Vercel

---

## Co se osvědčilo

- **Signal orange na void dark** — v kontextu všech DNA projektů zcela unikátní, silný a zapamatovatelný
- **Sora + Outfit** — oba fonty nové v DNA, Sora má geometrickou preciznost vhodnou pro technický autoservis
- **Animated diagonal speed lines** — subtilní CSS animace bez canvas, evokuje pohyb a rychlost
- **Emergency strip** — nejdůležitější rozhodnutí: vyzdvihuje havárijní službu na přední místo
- **Orange pulsující badge-dot** v hero — upoutá pozornost, signalizuje aktivní stav firmy

## Co příště udělat jinak

- Adresa AUROPS není na původním webu — příště zjistit před spuštěním
- Email taktéž chybí — příště ověřit s klientem
