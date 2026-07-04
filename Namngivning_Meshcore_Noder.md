---
title: "Project Documentation"
date: "$BUILD_DATE$"
---

Rekommendationer för regioner och kanaler för Meshcore-nät i Sverige
===

frav\_se\*, PappaNiklas\*, haxdoggy\*, DanielPaulsson\*, Burt Persson — \
* SysOps för http://had.meshmapper.net/

Kontakt: Discord SWEDEN-MESH #halland
https://discord.com/channels/1359596001240944660/1467977832557973635

Syftet med dokumentet är att ge en rekommendation för hur 1) bas-regioner och 2) bas-kanaler skall organiseras i Sverige. Dess benämns som "bas" då dessa rekommenderas som bas, men att andra regioner och kanaler kan fritt definieras utöver "basen". Definitionen av bas-regioner ger sen bas-kanaler, dvs. definitionen av bas-kanaler bygger på definitionen av bas-regioner. **I resten av dokumentet avses alltid "bas-" när region och kanal nämns.**

Rekommendationen kan läsas som två separata förslag: 1) bas-regioner, och; 2) bas-kanaler. Etablerande av 1) bas-regioner är viktigare än 2) bas-kanaler. 

En enhetlig region och kanaltruktur underlättar kommunikaion, felsökning och samordning. En gemensam konvention gör det möjligt att direkt från region och kanal  utläsa område, kommun och placering utan att konsultera extern dokumentation. **OBS! Detta är rekommendationer!**

---

## Regioner i Svenska Meshcore 

Meshcore regionerna följer SCBs Län och Kommunkoder, se referens 1, med prefix se. 
*Län har [se][xx]
*Kommuner har [se][xx][yy], dvx. kommun yy i län xx. 

| **Exempel: SE-Meshcore region** | **[BESKRIVNING]** |
|---|---|
| **se13** | Hallands län |
| **se1380** | Halmstad kommun |
| **se14** | Västra Götalands län |
| **se1480** | Göteborg kommun |
| **se1481** | Mölndal kommun |

När regioner läggs in i repeatern (med CLI) måste hierarki beaktas, e.g.
region put se *
region put se14 se 
region put se1480 se14

En fullständig lista på regioner finns i appendix


## Kanaler i Svenska Meshcore 

Meshcore kanalerna följer definitioner av regioner. 



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

*1: Län och Kommunkoder: https://www.scb.se/hitta-statistik/regional-statistik-och-kartor/regionala-indelningar/lan-och-kommuner/lan-och-kommuner-i-kodnummerordning/ *


