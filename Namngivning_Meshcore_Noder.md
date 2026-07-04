---
title: "Project Documentation"
date: "$BUILD_DATE$"
---

Rekommendationer för regioner och kanaler för Meshcore-nät i Sverige
===

frav\_se, PappaNiklas, haxdoggy, DanielPaulsson, Burt Persson — \
SysOps för http://[had|got|swe].meshmapper.net/ 

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
Syftet med kanalnamnet är att minska risken för sammanblandning (dvs. skriva in fel kanal) och vara helttydlig med vilket scope (region) som avses. Namnet på resp kanalen är därför rakt av baserat på läns och kommunkod, dvs. speglar region-namnet. 

| **Exempel: SE-Meshcore region** | **Kanal** | **[BESKRIVNING]** |
|---|---|
| se13 | **\#se13** | Hallands län |
| se1380 | **\#se1380** | Halmstad kommun |
| se14 | **\#se14** | Västra Götalands län |
| se1480 | **\#se1480** | Göteborg kommun |
| se1481 | **\#se1481** | Mölndal kommun |

---

*1: Län och Kommunkoder: https://www.scb.se/hitta-statistik/regional-statistik-och-kartor/regionala-indelningar/lan-och-kommuner/lan-och-kommuner-i-kodnummerordning/ *


