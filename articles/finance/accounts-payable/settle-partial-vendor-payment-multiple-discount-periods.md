---
title: Dalinio tiekėjo mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas
description: Šiame straipsnyje apžvelgiamas scenarijus, kai tiekėjui, kuris siūlo kelias mokėjimo nuolaidas, atliekami keli daliniai mokėjimai.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 659fb6c98b9ed0589932f8c4a67cb7b08264283c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189596"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Dalinio tiekėjo mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas scenarijus, kai tiekėjui, kuris siūlo kelias mokėjimo nuolaidas, atliekami keli daliniai mokėjimai. 

3054 tiekėjas siūlo „Fabrikam“ 2 procentų mokėjimo nuolaidą, jei sąskaita faktūra apmokama per penkias dienas, ir 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų.

## <a name="invoice"></a>PVM sąskaita faktūra
Birželio 28 d. Eglė 3054 tiekėjui sukuria sąskaitą faktūrą 1 000,00 sumai. Eglė šią operaciją gali peržiūrėti puslapyje **Tiekėjo operacijos**.

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
Liepos 2 d. Eglė nori sumokėti 300,00 pagal šią sąskaitą faktūrą. Ji sukuria vienkartinį mokėjimą naudodama puslapį **Mokėjimų žurnalas** dalyje Mokėtinos sumos. Ji prideda 3054 tiekėjo eilutę ir įveda mokėjimo sumą **300,00**. Tada Eglė atidaro puslapį **Sudengti operacijas**, kad galėtų pažymėti sudengsimą SF. Ji atnaujina lauko **Sudengtina suma** reikšmę į **300,00** ir pastebi, kad lauko **Taikytinos mokėjimo nuolaidos suma** reikšmė pasikeičia į **6,12**. Kadangi šis mokėjimas buvo atliktas per pirmąjį nuolaidos laikotarpį, pritaikoma 2 procentų nuolaida.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10060 | 3054    | 2015-06-28 | 2015-07-28 | 10060   | 1000,00                       | USD      | 300,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

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

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

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
Liepos 8 d. Eglė atlieka papildomą mokėjimą pagal sąskaitą faktūrą. Norėdama įvesti sumą, ji atidaro puslapį **Sudengti operacijas** ir spustelėja skirtuką **Mokėjimo nuolaida**. Ji mato, kad rodomos dviejų mokėjimo nuolaidų datos ir sumos. Kadangi šis mokėjimas buvo atliktas per antrąjį nuolaidos laikotarpį, galima 1 procento, arba 5,00, nuolaida. Ši suma apskaičiuojama kaip pusė 1 procento nuolaidos, taikomos 1000,00 sumai, arba pusė 10,00.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-07-03           | 20,00                | 680,00                         |
| 2015-07-12          | 10,00                | 690,00                         |
| 2015-07-25          | 0,00                 | 700,00                         |

Eglė nusprendžia mokėti 495,00 ir pritaikyti 5,00 mokėjimo nuolaidą. Todėl dabar visa sudengiama suma yra 500,00.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Įprastas            | SF-10060 | 3054    | 2015-06-28 | 2015-07-28 | 10060   | 1000,00                       | USD      | 495,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

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





