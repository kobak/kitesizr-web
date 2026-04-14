# KiteSizR

Egyoldalas, mobilra optimalizált kite-méret kalkulátor kiteboardosoknak. A kiteboard.hu ökoszisztéma része.

🔗 **Élő verzió:** `index.html` megnyitása böngészőben (offline is működik)

---

## Mi ez?

A KiteSizR segít eldönteni, hogy adott szélhez és testsúlyhoz milyen felületű kite-t érdemes választani. Nem helyettesíti a tapasztalatot, de jó kiindulási pont, ha nem biztos a választásban.

## Főbb funkciók

- **Kite típus:** LEI (tube) vagy Foil (ernyő)
- **Riding stílus:** 5 féle beállítás (freestyle, freeride, foil, light wind, wave)
- **Testsúly és szélkorrekció:** automatikus finomhangolás a bevitt adatok alapján
- **Helyszínválasztó:** bal felső sarokban gyors spot-váltás
- **Mobil-first UI:** Material Design 3 ihlette, érintésre optimalizált felület

## Algoritmus (v2)

A számítás alapképlete:

```
m² = (testsúly / szélsebesség) × alap faktor × stílus korrekció × súly korrekció × szél korrekció
```

| Kite típus | Alap faktor |
|------------|-------------|
| LEI        | 2.2 – 2.4   |
| Foil       | 1.7 – 2.2   |

- **Stílus korrekció:** freestyle-hoz kisebb, light wind-hez nagyobb kite ajánlása
- **Súly korrekció:** extrém testsúlyoknál (+/-) finomhangolás
- **Szél korrekció:** nagyon gyenge vagy nagyon erős szélben valóságosabb méret

> **Cél:** a 5kt hibahatár csökkentése (pl. 9m² vs. 13m² helyes döntése).

## Használat

1. Nyisd meg az `index.html`-t egy böngészőben.
2. Válaszd ki a kite típusát és a riding stílust.
3. Add meg a testsúlyt és a szélsebességet.
4. A javasolt méret azonnal megjelenik.

## Fejlesztői infó

- **Stack:** tiszta HTML + CSS + JavaScript (nincs build lépés)
- **Fájl:** `index.html` (önálló, egyetlen fájl)
- **Nyelv:** magyar UI

---

Készítette: kobak | Támogatja a kiteboard.hu projektet 🌊
