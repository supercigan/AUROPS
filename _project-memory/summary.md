# AUROPS s.r.o. — Project Summary

**Datum zahájení:** 2026-03-26
**Typ projektu:** Jednostránkový web — autoservis + havárijní služba
**GitHub:** supercigan/AUROPS
**Status:** Demoverze dokončena, čeká na schválení klientem

---

## Co je hotovo

- [x] Přečteny všechny DNA soubory (8 projektů) — navržena unikátní identita
- [x] Sebrány informace z původního webu aurops.cz (WebFetch)
- [x] Navržena paleta a typografie (Sora + Outfit, Signal Orange na void dark)
- [x] Vytvořen kompletní `index.html` — jednostránkový web
- [x] Vizuální audit (Puppeteer screenshots) — opraveny chyby
- [x] Přidán watermark: "Demoverze – Tomáš Smolík" (tiled SVG pattern, dual-layer)
- [x] GitHub push (supercigan/AUROPS)
- [x] DNA soubor uložen do C:\Users\karel\DNA-projekty\DNA-AUROPS.md
- [x] DNA kopie v project-dna/DNA-AUROPS.md

### Sekce v index.html:
1. NAV — fixed, transparent → void dark při scrollu, hamburger na mobilu
2. HERO — animated diagonal speed lines, badge s pulsující tečkou, H1 + orange accent, 2 CTA, info bar (havárie / provoz / partner)
3. EMERGENCY STRIP — full-width orange banner, 2 telefonní čísla (774 200 480 / 777 200 497)
4. SLUŽBY — 12 karet ve 4×3 gridu, orange left-border scaleY on hover
5. PROČ MY — void-mid sekce, 4 benefity číslované 01–04
6. KONTAKT — split layout: info vlevo + formulář vpravo (ash bg)
7. FOOTER — 3 sloupce (brand | navigace | kontakt), copyright bar
8. WATERMARK — SVG tiled pattern, -28°, dual-layer (tmavý + světlý)

---

## Opravené chyby (po vizuálním auditu)

| Problém | Oprava |
|---------|--------|
| Ikona Výměna autoskel = tabulka/mřížka | Nahrazena trapézoidem čelního skla + oblouk stěrače |
| Ikona Diagnostika Citroën = absolventská stuha | Nahrazena štítem s fajfkou (certifikovaný specialista) |
| Prázdný prostor nad sekcí Služby | Padding zmenšen 6rem → 4rem |
| Čísla 01–04 v "Proč my" téměř neviditelná | Opacity zvýšena 0.18 → 0.35 |
| Text benefitů příliš tmavý | Kontrast rgba(255,255,255,0.48) → 0.58 |
| Hero info bar — slabý text | font-weight: 600, větší velikost |
| Footer responsive — chybný grid-column span | Odstraněn grid-column: 1/-1 |
| Watermark neviditelný na tmavých sekcích | Přidána druhá světlá vrstva rgba(255,255,255,0.09) |

---

## Důležitá rozhodnutí

| Rozhodnutí | Důvod |
|------------|-------|
| Signal Orange (#F05F2E) | Urgentní/havárijní feel, v DNA projektech zcela unikátní |
| Sora + Outfit | Oba fonty nové v DNA, geometrická preciznost Sory |
| Animated diagonal speed lines v hero | CSS-only, evokuje pohyb/rychlost, nikdy dříve nepoužito |
| Emergency strip hned pod hero | AUROPS zdůrazňuje havárijní službu — prominentní pozice |
| Dual-layer watermark | Tmavý text na světlém + světlý text na tmavém → viditelný všude |

---

## Informace o klientovi

- **Firma:** AUROPS s.r.o.
- **Telefon havárie:** 774 200 480, 777 200 497
- **Partner:** UH CAR, s.r.o. (uhcar.cz)
- **Otevírací doba:** Po–Pá 7:00–17:00
- **Adresa:** neznámá (není na původním webu)
- **E-mail:** neznámý (není na původním webu)

---

## Příští kroky

1. Schválení designu klientem → odstranit watermark
2. Doplnit adresu a email
3. Napojit formulář (Formspree nebo vlastní endpoint)
4. Vercel deploy (automaticky z GitHub master)
