---
title: Nustatyti dalinį mokėjimą prieš nuolaidos datą ir galutinį mokėjimą po nuolaidos datos
description: Šiame straipsnyje žingsnis po žingsnio pateiktas scenarijus, kuriame atliekami keli daliniai mokėjimai, kai kurie mokėjimo nuolaidos laikotarpiu, o kiti ne mokėjimo nuolaidos laikotarpiui.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 828c82d88bef1d942af1219505af591d27043fa5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780269"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Nustatyti dalinį mokėjimą prieš nuolaidos datą ir galutinį mokėjimą po nuolaidos datos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje žingsnis po žingsnio pateiktas scenarijus, kuriame atliekami keli daliniai mokėjimai, kai kurie mokėjimo nuolaidos laikotarpiu, o kiti ne mokėjimo nuolaidos laikotarpiui.

„Fabrikam“ perka prekes iš 3057 tiekėjo. „Fabrikam“ gauna 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų. SF turi būti apmokėtos per 30 dienų. Tiekėjas „Fabrikam‟ taip pat leidžia taikyti mokėjimo nuolaidas, kai mokama dalimis. Sudengimo parametrai yra puslapyje **Mokėtinų sumų parametrai**.

## <a name="invoice-on-june-25"></a>Birželio 25 d. SF
Birželio 25 d. Eglė 3057 tiekėjui įveda ir užregistruoja sąskaitą faktūrą 1 000,00 sumai. Eglė šią operaciją gali peržiūrėti puslapyje **Tiekėjo operacijos**.

| Kvitas   | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis   | Valiuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| SF-10020 | Sąskaita faktūra          | 6/25/2020 | 10020   |                                      | 1,000.00                              | -1,000.00 | USD      |

## <a name="partial-payment-on-july-2"></a>Dalinis mokėjimas liepos 2 d.
Liepos 2 d. Eglė nori sudengti 300,00 šios SF. Mokėjimui gali būti taikoma nuolaida, nes „Fabrikam‟ taiko nuolaidas daliniams mokėjimams. Todėl Eglė sumoka 297,00 ir gauna 3,00 nuolaidą. Ji sukuria mokėjimo žurnalą ir įveda eilutę 3057 tiekėjui. Tada ji atidaro puslapį **Sudengti operacijas**, kad galėtų pažymėti sąskaitą faktūrą sudengti.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Normalus            | SF-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | -1,000.00                      | USD      | –297,00          |

Nuolaidos informacija rodoma puslapio **Sudengti atviras operacijas** apačioje.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | -10.00    |
| Naudokite mokėjimo nuolaidą            | Normalus    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –3,00     |

Tada Eglė registruoja mokėjimą. SF balansas dabar yra 700,00. Eglė šią operaciją gali peržiūrėti puslapyje **Tiekėjo operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10020  | Sąskaita faktūra          | 6/25/2020 | 10020   |                                      | 1,000.00                              | –700,00 | USD      |
| PROG-10020  | Mokėjimas          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | USD      |
| NUOL-10020 | Mokėjimo nuolaida    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Liko mokėti liepos 15 d., Naudoti mokėjimo nuolaidą = įprast.
Eglė apmoka likusią SF sumą liepos 15 d., kuri yra po mokėjimo nuolaidos laikotarpio. Puslapyje **Sudengti atidarytas operacijas**, **Įvertintos mokėjimo nuolaidos** lauke nerodoma jokia nuolaidos suma, o reikšmė **Mokėjimo nuolaidos sumos** lauke yra **0,00**. Kai Eglė mokės likusius 700,00, nebus taikoma jokia papildoma nuolaida.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Normalus            | SF-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | –700,00                        | USD      | –700,00          |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje. Eglė mato, kad jai jau pritaikyta 3,00 nuolaida.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | 0,00      |
| Naudokite mokėjimo nuolaidą            | Normalus    |
| Pritaikyta mokėjimo nuolaida          | –3,00     |
| Taikytinos mokėjimo nuolaidos suma | 0,00      |

Tada Eglė registruoja mokėjimą. Atidariusi **Tiekėjo operacijų** puslapį, ji mato, kad SF balansas yra 0,00. Ji taip pat mato, kad yra du mokėjimai. Vienas mokėjimas yra už 297,00 su 3,00 nuolaida, o kitas mokėjimas yra už 700,00.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10020  | Sąskaita faktūra          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| PROG-10020  | Mokėjimas          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | USD      |
| NUOL-10020 | Mokėjimo nuolaida    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| PROG-10021  | Mokėjimas          | 7/15/2020 |         | 700.00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Liko mokėti liepos 15 d., Naudoti mokėjimo nuolaidą = visada
Jei tiekėjas leidžia Eglei pritaikyti nuolaidą, nors ji sumoka po nuolaidos datos, ji gali pakeisti vertę lauke **Naudoti mokėjimo nuolaidą** į **Visada**. **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** bus nepaisoma parametro ir bus pritaikyta nuolaida. Mokėjimo suma yra 693,00, o nuolaida yra likę 7,00.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|----------|----------|------|------|-----------|-----------|---------|-----------------------|---------------------------------------|----------|------------------|
| Pasirinkta | Visada            | SF-10020 | 3057    | 6/25/2020 | 7/25/2020 | 10020   | 700.00                   |                   | USD      | –693,00          |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | 7.00      |
| Naudokite mokėjimo nuolaidą            | Visada    |
| Pritaikyta mokėjimo nuolaida          | –3,00     |
| Taikytinos mokėjimo nuolaidos suma | –7,00     |

Tada Eglė registruoja mokėjimą. Atidariusi **Tiekėjo operacijų** puslapį, ji mato, kad SF balansas yra 0,00. Ji taip pat mato, kad yra du mokėjimai. Vienas mokėjimas yra už 297,00 su 3,00 nuolaida, o kitas mokėjimas yra už 693,00 su 7,00 nuolaida.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10020  | Sąskaita faktūra          | 6/25/2020 | 10020   |                                      | 1,000.00                              | 0,00    | USD      |
| PROG-10020  | Mokėjimas          | 7/1/2020  |         | 297,00                               |                                       | 0,00    | USD      |
| NUOL-10020 | Mokėjimo nuolaida    | 7/1/2020  |         | 3.00                                 |                                       | 0,00    | USD      |
| PROG-10021  | Mokėjimas          | 7/15/2020 |         | 693,00                               |                                       | 0,00    | USD      |
| NUOL-10021 | Mokėjimo nuolaida    | 7/15/2020 |         | 7.00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
