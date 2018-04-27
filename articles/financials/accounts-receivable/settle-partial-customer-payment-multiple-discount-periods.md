---
title: "Dalinio kliento mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas"
description: "Šiame straipsnyje parodoma, kaip sudengiami daliniai kliento mokėjimai, kai yra keli nuolaidos laikotarpiai."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ac64ece82abe75f3cba437b1ec1af499fbbce8e4
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Dalinio kliento mokėjimo, turinčio kelis nuolaidos laikotarpius, sudengimas

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje parodoma, kaip sudengiami daliniai kliento mokėjimai, kai yra keli nuolaidos laikotarpiai.

„Fabrikam“ 4031 klientui siūlo du mokėjimo nuolaidos laikotarpius. Klientas gauna 2 procentų mokėjimo nuolaidą, jei SF yra apmokama per penkias dienas, arba 1 procento mokėjimo nuolaidą, jei SF apmokama per 14 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoice"></a>PVM sąskaita faktūra
Birželio 25 d. Eglė 4031 klientui įveda ir užregistruoja sąskaitą faktūrą 1 000,00 sumai. Peržiūrėdama šios sąskaitos faktūros mokėjimo nuolaidą, Eglė mato, kad 4031 klientas gaus 20,00 nuolaidą, jei sąskaita faktūra bus apmokėta iki birželio 30 d. Jei sąskaita faktūra bus apmokėta iki liepos 9 d., klientas gaus 10,00 nuolaidą.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-06-30          | 20,00                | 980,00                         |
| 2015-07-09           | 10,00                | 990,00                         |
| 2015-07-25          | 0,00                 | 1000,00                       |

Arnas gali šią operaciją peržiūrėti puslapyje **Kliento operacijos**.

| Kvitas   | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10030 | PVM sąskaita faktūra          | 2015-06-25 | 10030   | 1000,00                             |                                       | 1000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Dalinis mokėjimas prieš mokėjimo nuolaidos datą
Birželio 28 d. 4031 klientas atliko 294,00 dalinį mokėjimą. Kadangi birželio 28 d. patenka į pirmąjį mokėjimo nuolaidos laikotarpį, klientui taikoma 6,00 nuolaida. Puslapyje **Sudengti operacijas** lauko **Mokėjimo nuolaidos suma** reikšmė yra 20,00, o **Taikytinos mokėjimo nuolaidos suma** reikšmė yra 6,00.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10030 | 4031    | 2015-06-25 | 2015-07-25 | 10030   | 1000,00                       | USD      | 294,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje. Jei lauko **Sudengtina suma** reikšmės nepakeisite į **294,00**, rodomos lauko **Mokėjimo nuolaidos suma** reikšmės skirsis. Tačiau užregistravus mokėjimą bus taikoma 6,00 mokėjimo nuolaida, nes sudengimo funkcija automatiškai koreguoja lauko **Sudengtina suma** reikšmę.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-06-30 |
| Mokėjimo nuolaidos suma         | 20,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 6,00      |

Kai Arnas užregistruoja mokėjimą, SF balansas yra 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Dalinis mokėjimas prieš antrąją mokėjimo nuolaidos datą
Liepos 8 d. klientas sumoka likusią SF sumą. Pritaikoma 7,00 nuolaida (1 procento), nes mokėjimas atliktas per antrąjį mokėjimo nuolaidos laikotarpį.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10030 | 4031    | 2015-06-25 | 2015-07-25 | 10030   | 700,00                               |                                       | USD      | 693,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 30,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 6,00      |
| Taikytinos mokėjimo nuolaidos suma | 7,00      |

Dabar SF balansas yra 0,00. Arnas peržiūri šią operaciją puslapyje **Kliento operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10030  | PVM sąskaita faktūra          | 2015-06-25 | 10030   | 1000,00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Mokėjimas         | 6/28/2015 |         |                                      | 294,00                                | 0,00    | USD      |
| NUOL-10030 |  Mokėjimo nuolaida   | 2015-06-28 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Mokėjimas         | 2015-07-08  |         |                                      | 693,00                                | 0,00    | USD      |
| NUOL-1031  |  Mokėjimo nuolaida   | 2015-07-08  |         |                                      | 7,00                                  | 0,00    | USD      |






