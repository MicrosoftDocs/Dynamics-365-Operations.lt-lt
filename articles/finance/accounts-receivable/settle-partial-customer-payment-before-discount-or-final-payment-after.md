---
title: Nustatyti dalinį mokėjimą prieš nuolaidos datą su galutiniu mokėjimu po nuolaidos datos
description: Šiame straipsnyje aptariamas mokėjimų sudengimo pagal klientų sąskaitas faktūras poveikis. Scenarijumi dėmesys telkiamas ties poveikiu papildomai knygai, o ne didžiajai knygai.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f6b4527a9f176857e0cc6ba4665688dc8721ac1
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780245"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Nustatyti dalinį mokėjimą prieš nuolaidos datą su galutiniu mokėjimu po nuolaidos datos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptariamas mokėjimų sudengimo pagal klientų sąskaitas faktūras poveikis. Scenarijumi dėmesys telkiamas ties poveikiu papildomai knygai, o ne didžiajai knygai.

Fabrikam parduoda prekes 4027 klientui. Fabrikam siūlo 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų. SF turi būti apmokėtos per 30 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoice"></a>PVM sąskaita faktūra
Birželio 25 d. Eglė 4027 klientui sukuria ir užregistruoja sąskaitą faktūrą 1 000,00 sumai. Eglė gali peržiūrėti šią sąskaitą faktūrą naudodama mygtuką **Operacijos**, esantį puslapyje **Klientai**.

| Kvitas   | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10020 | Sąskaita faktūra          | 6/25/2020 | 10020   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Dalinis mokėjimas prieš mokėjimo nuolaidos datą
Liepos 2 d. 4027 klientas atlieka dalinį 297,00 SF mokėjimą. Mokėjimui yra gali būti taikoma mokėjimo nuolaida, nes „Fabrikam“ suteikia galimybę mokėjimo nuolaidas taikyti daliniams mokėjimams, o mokėjimas atliekamas prieš mokėjimo nuolaidos datą. Todėl 4027 klientui pritaikoma 3,00 mokėjimo nuolaida. Arnas įrašo 4027 kliento mokėjimą naudodamas mokėjimų žurnalą. Tada Arnas atidaro puslapį **Sudengti operacijas**, kad Arnie galėtų pažymėti sudengtiną SF.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Pasirinkta | Normalus            | LFSF-10020 | 4027    | 6/25/2020 | 7/25/2020 | 10020   | 1,000.00                             | USD      | 297,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atviras operacijas** apačioje. Jei lauko **Sudengtina suma** reikšmės nepakeisite į 297,00, rodomos lauko **Mokėjimo nuolaidos suma** reikšmės skirsis. Tačiau užregistravus mokėjimą bus taikoma 3,00 mokėjimo nuolaida, nes sudengimo funkcija automatiškai koreguoja lauko **Sudengtina suma** vertę.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Normalus    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 3,00      |

Arnas šį mokėjimą užregistruoja. SF balansas dabar yra 700,00. Galima matyti toliau nurodytas kliento operacijas.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10020  | Sąskaita faktūra          | 6/25/2020 | 10020   | 1,000.00                             |                                       | 700.00  | USD      |
| ARP-10020  |  Mokėjimas         | 7/1/2020  |         |                                      | 297,00                                | 0,00    | USD      |
| NUOL-10020 |  Mokėjimo nuolaida   | 7/1/2020  |         |                                      | 3.00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Likęs mokėjimas po mokėjimo nuolaidos datos
4027 klientas apmoka likusią šios SF sumą liepos 11 d., kuri yra po mokėjimo nuolaidos laikotarpio. Puslapio **Sudengti operacijas** lauke **Įvertinta mokėjimo nuolaida** nuolaidos suma nerodoma, o reikšmė lauke **Mokėjimo nuolaidos suma** yra **0,00**. Kai 4027 klientas mokės likusius 700,00, nebus taikoma jokia papildoma nuolaida.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Pasirinkta | Normalus            | LFSF-10020 | 4027    | 6/25/2020 | 7/25/2020 | 10020   | 700.00                               | USD      | 700.00           |

Nuolaidos informacija rodoma puslapio **Sudengti atviras operacijas** apačioje.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | 0,00      |
| Naudokite mokėjimo nuolaidą            | Normalus    |
| Pritaikyta mokėjimo nuolaida          | 3,00      |
| Taikytinos mokėjimo nuolaidos suma | 0,00      |

Jei Arnas pakeis lauko **Naudoti mokėjimo nuolaidą** reikšmę į **Visada**, bus nepaisoma parametro **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** ir bus pritaikyta mokėjimo nuolaida. Mokėjimo suma pasikeičia į 693,00, o mokėjimo nuolaida yra likę 7,00.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|---------------|---------------------|----------|------------------|
| Pasirinkta | Visada            | LFSF-10020 | 4027    | 6/25/2020 | 7/25/2020 | 10020   | 700.00        |                        | USD      | 693,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atviras operacijas** apačioje.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 7/09/2020 |
| Mokėjimo nuolaidos suma         | 7.00      |
| Naudokite mokėjimo nuolaidą            | Visada    |
| Pritaikyta mokėjimo nuolaida          | 3,00      |
| Taikytinos mokėjimo nuolaidos suma | 7,00      |

Arnas pakeičia lauko **Naudoti mokėjimo nuolaidą** reikšmę atgal į **Įprasta**, nes Arnie nenori klientui taikyti likusios 7,00 mokėjimo nuolaidos. Tada Arnas užregistruoja mokėjimą. Atidaręs puslapį **Kliento operacijos**, Arnas mato, kad SF balansas yra 0,00. Galima naudoti du mokėjimus. Vienas mokėjimas yra už 297,00 su 3,00 mokėjimo nuolaida, o kitas mokėjimas yra už 700,00.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10020  | Sąskaita faktūra          | 6/25/2020 | 10020   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 7/1/2020  |         |                                      | 297,00                                | 0,00    | USD      |
| NUOL-10020 |                  | 7/1/2020  |         |                                      | 3.00                                  | 0,00    | USD      |
| ARP-10021  |                  | 7/11/2020 |         |                                      | 700.00                                | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
