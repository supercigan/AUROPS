# AUROPS s.r.o. — Project Summary

**Datum zahájení:** 2026-03-26
**Typ projektu:** Jednostránkový web — autoservis + havárijní služba

---

## Co je hotovo

- [x] Přečteny všechny DNA soubory (8 projektů) — navržena unikátní identita
- [x] Sebrány informace z původního webu aurops.cz (WebFetch)
- [x] Navržena paleta a typografie (Sora + Outfit, Signal Orange na void dark)
- [x] Vytvořen kompletní `index.html` — jednostránkový web

### Sekce v index.html:
1. NAV — fixed, transparent → void dark při scrollu
2. HERO — animated diagonal speed lines, badge, H1, 2 CTA, info bar
3. EMERGENCY STRIP — full-width orange banner s telefonními čísly
4. SLUŽBY — 12 karet v 4-sloupcovém gridu, orange left-border on hover
5. PROČ MY — void dark sekce, 4 číslované benefity
6. KONTAKT — split layout: info vlevo + formulář vpravo
7. FOOTER — 3 sloupce, void dark

---

## Co se řeší

- [ ] GitHub push (repo ještě nevytvořen)
- [ ] DNA soubor (napsat po schválení designu)

---

## Důležitá rozhodnutí

| Rozhodnutí | Důvod |
|------------|-------|
| Signal Orange (#F05F2E) jako accent | Urgentní/havárijní feel, žádný z DNA projektů nepoužil čistou oranžovou |
| Sora + Outfit | Oba fonty nové — geometrická preciznost Sory odpovídá autoservisu |
| Animated diagonal speed lines v hero | Evokuje pohyb/rychlost, CSS-only, nikdy dříve nepoužito |
| Emergency strip hned pod hero | AUROPS zdůrazňuje havárijní službu — zaslouží si prominentní pozici |
| 12 služeb ve 4×3 gridu | Přehledné, rovnoměrné, mobile-friendly |
| Void near-black (#0C0E12) | Odlišné od navy (M-autoservis), ink (DH), carbon (OK) |

---

## Informace o klientovi

- **Firma:** AUROPS s.r.o.
- **Telefon havárie:** 774 200 480, 777 200 497
- **Partner:** UH CAR, s.r.o. (uhcar.cz)
- **Otevírací doba:** Po–Pá 7:00–17:00

### Služby (12):
1. Předprodejní prohlídky
2. Kompletní servis
3. Geometrie kol 3D
4. Tlumiče a podvozek
5. PC Diagnostika OBD II
6. Diagnostika Citroën
7. Multi-brand diagnostika (VW/Škoda/Seat/Audi/Ford/Renault)
8. Karoserie a lak
9. Elektroinstalace
10. Klimatizace
11. Výměna autoskel
12. Tažná zařízení

---

## Příští kroky

1. Schválení designu klientem
2. GitHub push → Vercel deploy
3. DNA soubor do C:\Users\karel\DNA-projekty\
4. Doplnit adresu a email (nejsou na původním webu)
