---
title: "Atsiskaityti dalinis tiekėjo mokėjimų ir galutinio mokėjimo visiškai iki nuolaidos data"
description: "Šiame straipsnyje apžvelgiamas scenarijus, kai pagal tiekėjo SF atliekami daliniai mokėjimai ir pritaikoma mokėjimo nuolaida."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6cd87dc1b34d1d689d5417359e1ec3a34d53afb4
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Atsiskaityti dalinis tiekėjo mokėjimų ir galutinio mokėjimo visiškai iki nuolaidos data

Šiame straipsnyje apžvelgiamas scenarijus, kai pagal tiekėjo SF atliekami daliniai mokėjimai ir pritaikoma mokėjimo nuolaida.

Fabrikam perka prekes iš tiekėjo 3064. Pardavėjas suteikia Fabrikam 1 proc nuolaida, jei sąskaita yra apmokėta per 14 dienų. SF turi būti apmokėtos per 30 dienų. Tiekėjas „Fabrikam‟ taip pat leidžia taikyti mokėjimo nuolaidas, kai mokama dalimis. Sudengimo parametrus yra ant to **sudaro mokėtinų sumų parametrai** puslapis. Birželio 25 d. Eglė 3064 tiekėjui sukuria SF 1000,00 sumai.

## <a name="vendor-invoice-on-june-25"></a>Tiekėjo SF birželio 25 d.
Birželio 25 d., balandžio patenka ir postų 1000,00 3064 tiekėjo SF. Eglė šią operaciją gali peržiūrėti puslapyje **Tiekėjo operacijos**.

| Kvitas   | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis   | Valiuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| SF-10010 | 2015-06-25 | 10010   |                                      | 1000,00                              | –1.000,00 | USD      |

Iš **Tiekėjų** puslapio April atidaro puslapį **Sudengti operacijas**. Ji gali naudoti puslapį **Sudengti operacijas**, norėdama peržiūrėti mokėjimo nuolaidų datas ir sumas. Terminas yra liepos 25 d., o –10.00 mokėjimo nuolaida taikoma, jei SF apmokama iki liepos 9 d..

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10010 | 3064    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 990,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atviras operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | –10,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –10,00    |

Eglė spusteli skirtuką **Mokėjimo nuolaida**, norėdama peržiūrėti nuolaidos sumą.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-07-09           | 10,00                | 990,00                         |
| 2015-07-25          | 0,00                 | 1000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Dalinis mokėjimas liepos 1 d. naudojant puslapį Sudengti operacijas
Eglė gali kurti šio mokėjimo mokėjimų žurnalą, dalyje Mokėtinos sumos atidarydama puslapį **Mokėjimų žurnalas**. Ji sukurti naują žurnalą ir įveda linijos tiekėjo 3064. Ji atidaro su **atsiskaitymams** puslapyje, taip, kad ji gali pažymėti SF sudengti. Eglė pažymi SF ir pakeičia lauko **Sudengtina suma** reikšmę į **–500,00**. Ji mato, kad visos SF lauko **Mokėjimo nuolaidos suma** reikšmė yra **–10,00**, o lauko **Taikytinos mokėjimo nuolaidos suma** reikšmė yra **–5,05**. Todėl SF suma, kurią Eglė sudengia, yra –505,05.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | –500,00          |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | –10,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –5,05     |

Eglė nori sudengti lygiai pusę SF sumos. Todėl ji pakeičia lauko **Sudengtina suma** reikšmę į **–495,00**. Dabar visa sudengiama suma yra 500,00. Šiai sumai pritaikyta –5,00 mokėjimo nuolaida.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | –495,00          |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | –10,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –5,00     |

Eglė uždaro puslapį **Sudengti operacijas**. Žurnale sukuriama mokėjimo eilutė 495,00 sumai ir tada Eglė užregistruoja žurnalą. Balandis galite peržiūrėti tiekėjo operacijų dėl to **tiekėjo operacijų** puslapis. Ji mato, kad sąskaitos faktūros turi-500.00 pusiausvyrą. Ji taip pat mato 495,00 mokėjimą ir 5,00 mokėjimo nuolaidą.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10010  | PVM sąskaita faktūra          | 2015-06-25 | 10010   |                                      | 1000,00                              | –500,00 | USD      |
| PROG-10010  | Mokėjimas          | 2015-07-01  |         | 495,00                               |                                       | 0,00    | USD      |
| NUOL-10010 | Mokėjimo nuolaida    | 2015-07-01  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Likusi suma, sumokama liepos 8 d.
Eglė sumoka likusią 3064 tiekėjo SF sumą liepos 8 d., kuri patenka į mokėjimo nuolaidos laikotarpį. Eglė sukuria mokėjimo žurnalą liepos 8 d. ir pažymi operaciją sudengti. Ji mato, kad suma, kurią reikia sudengti, yra 495,00. Lauko **Įvertinta mokėjimo nuolaida** reikšmė yra **–5,00**, nes anksčiau buvo pritaikyta 5,00 nuolaida.

|                         |        |
|-------------------------|--------|
| Pažymėta bendroji suma            | 495,00 |
| Įvertinta mokėjimo nuolaida | –5,00  |

Informacija apie pažymėtą operaciją rodoma puslapio **Sudengti atviras operacijas** tinklelyje.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 495,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 5,00      |
| Taikytinos mokėjimo nuolaidos suma | 5,00      |

Eglė užregistruoja mokėjimo žurnalą ir peržiūri tiekėjo operacijas puslapyje **Tiekėjo operacijos**. Dabar SF balansas yra 0,00 ir Eglė mato du mokėjimus ir mokėjimo nuolaidas.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10010  | PVM sąskaita faktūra          | 2015-06-25 | 10010   |                                      | 1000,00                              | 0,00    | USD      |
| PROG-10010  |  Mokėjimas         | 2015-07-01  |         | 495,00                               |                                       | 0,00    | USD      |
| NUOL-10010 | Mokėjimo nuolaida    | 2015-07-01  |         | 5,00                                 |                                       | 0,00    | USD      |
| PROG-10011  | Mokėjimas          | 2015-07-08  |         | 495,00                               |                                       | 0,00    | USD      |
| NUOL-10011 | Mokėjimo nuolaida    | 2015-07-08  |         | 5,00                                 |                                       | 0,00    | USD      |




