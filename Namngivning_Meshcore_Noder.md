---
title: "Project Documentation"
date: "$BUILD_DATE$"
---

Rekommendationer för namngivning av noder i Meshcore-nät
===

frav\_se\*, PappaNiklas\*, haxdoggy\*, DanielPaulsson\*, Burt Persson — \
* SysOps för http://had.meshmapper.net/

Kontakt: Discord SWEDEN-MESH #halland
https://discord.com/channels/1359596001240944660/1467977832557973635

En enhetlig namnstruktur underlättar felsökning och samordning. En gemensam konvention gör det möjligt att direkt från nodnamnet utläsa område, kommun och placering utan att konsultera extern dokumentation. **OBS! Detta är rekommendationer!**

---

## Namnstruktur

```
[SE]-[KOMMUN]-[BESKRIVNING]

ELLER

[SE][LÄNKOMMUNKOD]-[BESKRIVNING]
```

Alla fält obligatoriska. Versaler genomgående, förutom i beskrivning. Inga svenska tecken. Bindestreck (`-`) som enda avskiljare. Max 22 tecken totalt (inkl. bindestreck).


## Exempel

```
SE1380-MrBengtCOMAB12
SE1380-Arnegatan2REP
SE-BST-KattvkRep1
SE-LAH-HallonGrg1BF12
```

---

## Fältbeskrivning

| **Fält** | **Längd** | **Beskrivning** |
|---|---|---|
| **[SE]** | 2 (fast) | Landskod enligt ISO 3166-1 alpha-2. Skall vara SE för noder i Sverige |
| **[KOMMUN]** | 3 (fast) | Förkortning för kommun, t.ex. `BST`, `MAL`. Båda tre bokstäver. Se appendix för rekommenderade förkortningar för kommun. |
| **[LÄNKOMMUNKOD]** |4 (fast) | Län och kommun-koder, e.g. 1380 = Halmstad Kommun i Hallands län
| **[BESKRIVNING]** | max 15 | Placering, ägare eller adress. Se nodtyper nedan. Rekommenderas inledande versal och sedan gemener. Se nodtyper nedan. I slutet av Beskrivning kan de fyra första tecknen i nodens publika nyckel läggas till, t.ex. `A3FB`

## Rekommendationer per nodtyp

| **Nodtyp** | **[BESKRIVNING]** |
|---|---|
| **Repeater** | Fysisk placering, byggnadsnamn eller höjdläge |
| **Room Server** | Fysisk placering eller byggnadsnamn |
| **Companion** | Innehavarens namn eller anropssignal |

---

*Kommunförkortningar: Se Appendix. *
*Län och Kommunkoder: https://www.scb.se/hitta-statistik/regional-statistik-och-kartor/regionala-indelningar/lan-och-kommuner/lan-och-kommuner-i-kodnummerordning/ *


