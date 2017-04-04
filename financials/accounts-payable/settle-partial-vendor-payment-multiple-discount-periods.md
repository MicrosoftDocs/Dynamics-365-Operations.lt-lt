---
title: "Atsiskaityti dalinis tiekėjo mokėjimą, kuris turi kelis nuolaida laikotarpiai"
description: "Šiame straipsnyje apžvelgiamas scenarijus, kai tiekėjui, kuris siūlo kelias mokėjimo nuolaidas, atliekami keli daliniai mokėjimai."
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
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 4fd4fdf6150d4160d07d8a9b8027a40d1c22cf7d
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Atsiskaityti dalinis tiekėjo mokėjimą, kuris turi kelis nuolaida laikotarpiai

Šiame straipsnyje apžvelgiamas scenarijus, kai tiekėjui, kuris siūlo kelias mokėjimo nuolaidas, atliekami keli daliniai mokėjimai. 

3054 tiekėjas siūlo „Fabrikam“ 2 procentų mokėjimo nuolaidą, jei sąskaita faktūra apmokama per penkias dienas, ir 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų.

## <a name="invoice"></a>PVM sąskaita faktūra
Birželio 28 d., balandžio sukuria 1000,00 3054 tiekėjo SF. Eglė šią operaciją gali peržiūrėti puslapyje **Tiekėjo operacijos**.

| Kvitas   | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis   | Valiuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| SF-10060 | 2015-06-28 | 10060   |                                      | 1000,00                              | –1000,00 | USD      |

Šiai SF galimos toliau nurodytos mokėjimo nuolaidos datos ir sumos.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-07-03           | 20,00                | 980,00                         |
| 2015-07-12          | 10,00                | 990,00                         |
| 2015-07-25          | 0,00                 | 1000,00                       |

## <a name="payment-on-july-2"></a>Mokėjimas liepos 2 d.
Liepos 2 d. balandžio nori mokėti 300.00 pagal šią sąskaitą faktūrą. Ji kuria vienkartinį mokėjimą naudojant į **mokėjimo žurnalo** puslapio dalyje mokėtinos sąskaitos. Ji prideda 3054 tiekėjo eilutę ir įveda mokėjimo sumą **300,00**. Tada Eglė atidaro puslapį **Sudengti operacijas**, kad galėtų pažymėti sudengsimą SF. Ji atnaujina lauko **Sudengtina suma** reikšmę į **300,00** ir pastebi, kad lauko **Taikytinos mokėjimo nuolaidos suma** reikšmė pasikeičia į **6,12**. Kadangi šis mokėjimas buvo atliktas per pirmąjį nuolaidos laikotarpį, pritaikoma 2 procentų nuolaida.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10060 | 3054    | 2015-06-28 | 2015-07-28 | 10060   | 1000,00                       | USD      | 300,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-02 |
| Mokėjimo nuolaidos suma         | –20,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –6,12     |

Kadangi galima mokėjimo nuolaida, Eglė nori pakeisti mokėjimo sumą, kad visa mokėjimo sudengta suma pritaikius nuolaidą būtų 300,00. Ji pakeičia lauko **Sudengtina suma** reikšmę į **294,00** ir pastebi, kad lauko **Taikytinos mokėjimo nuolaidos suma** reikšmė pasikeičia į **6,00**.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10060 | 3054    | 2015-06-28 | 2015-07-28 | 10060   | 1000,00                       | USD      | 294,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-02 |
| Mokėjimo nuolaidos suma         | –20,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –6,00     |

Eglė užregistruoja mokėjimą. Ji gali peržiūrėti operacijas puslapyje **Tiekėjo operacijos**. Ji mato, kad SF rodoma 300,00. Šiai sumai pritaikyta mokėjimo nuolaida 6,00. Todėl likutis yra 700,00.

| Kvitas    | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10060  | 2015-06-28 | 10060   |                                      | 1000,00                              | –700,00 | USD      |
| PROG-10060  | 2015-07-02  |         | 294,00                               |                                       | 0,00    | USD      |
| NUOL-10060 | 2015-07-02  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Mokėjimas liepos 8 d.
Liepos 8 d. Eglė atlieka papildomą mokėjimą pagal sąskaitą faktūrą. Norėdama įvesti sumą, ji atidaro puslapį **Sudengti operacijas** ir tada spustelėja skirtuką **Mokėjimo nuolaida**. Ji mato, kad rodomos dviejų mokėjimo nuolaidų datos ir sumos. Kadangi šis mokėjimas buvo atliktas per antrąjį nuolaidos laikotarpį, galima 1 procento, arba 5,00, nuolaida. Ši suma apskaičiuojama kaip pusė 1 procento nuolaidos, taikomos 1000,00 sumai, arba pusė 10,00.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-07-03           | 20,00                | 680,00                         |
| 2015-07-12          | 10,00                | 690,00                         |
| 2015-07-25          | 0,00                 | 700,00                         |

Eglė nusprendžia mokėti 495,00 ir pritaikyti 5,00 mokėjimo nuolaidą. Todėl dabar visa sudengiama suma yra 500,00.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10060 | 3054    | 2015-06-28 | 2015-07-28 | 10060   | 1000,00                       | USD      | 495,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas **apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | –10,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | –6,00     |
| Taikytinos mokėjimo nuolaidos suma | –5,00     |

Puslapyje **Tiekėjų operacijos** Eglė mato, kad naujas balansas 200,00.

| Kvitas    | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10060  | 2015-06-28 | 10060   |                                      | 1000,00                              | –200,00 | USD      |
| PROG-10060  | 2015-07-02  |         | 294,00                               |                                       | 0,00    | USD      |
| NUOL-10060 | 2015-07-02  |         | 6,00                                 |                                       | 0,00    | USD      |
| PROG-10061  | 2015-07-12 |         | 495,00                               |                                       | 0,00    | USD      |
| NUOL-10061 | 2015-07-12 |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Mokėjimas liepos 20 d.
Liepos 20 d. Eglė sukuria 200,00 galutinį mokėjimą. Nepritaikoma jokia nuolaida, nes mokėjimas atliekamas praėjus abiem nuolaidos laikotarpiams. Sąskaitos faktūros balansas yra 0,00.

| Kvitas    | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10060  | 2015-06-28 | 10060   |                                      | 1000,00                              | –200,00 | USD      |
| PROG-10060  | 2015-07-02  |         | 294,00                               |                                       | 0,00    | USD      |
| NUOL-10060 | 2015-07-02  |         | 6,00                                 |                                       | 0,00    | USD      |
| PROG-10061  | 2015-07-12 |         | 495,00                               |                                       | 0,00    | USD      |
| NUOL-10061 | 2015-07-12 |         | 5,00                                 |                                       | 0,00    | USD      |
| PROG-10062  | 2015-07-20 |         | 200,00                               |                                       | 0,00    | USD      |




