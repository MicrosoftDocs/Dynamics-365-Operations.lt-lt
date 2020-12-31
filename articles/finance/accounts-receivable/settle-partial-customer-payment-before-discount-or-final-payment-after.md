---
title: Dalinis kliento mokėjimas sudengiamas prieš nuolaidos datą, kai paskutinis mokėjimas atliekamas po nuolaidos datos
description: Šiame straipsnyje aptariamas mokėjimų sudengimo pagal klientų sąskaitas faktūras poveikis. Scenarijumi dėmesys telkiamas ties poveikiu papildomai knygai, o ne didžiajai knygai.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a71d0931445f3501f1b74f26c5eef583ab598b3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445890"
---
# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Dalinis kliento mokėjimas sudengiamas prieš nuolaidos datą, kai paskutinis mokėjimas atliekamas po nuolaidos datos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptariamas mokėjimų sudengimo pagal klientų sąskaitas faktūras poveikis. Scenarijumi dėmesys telkiamas ties poveikiu papildomai knygai, o ne didžiajai knygai.

Fabrikam parduoda prekes 4027 klientui. Fabrikam siūlo 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų. SF turi būti apmokėtos per 30 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoice"></a>PVM sąskaita faktūra
Birželio 25 d. Eglė 4027 klientui sukuria ir užregistruoja sąskaitą faktūrą 1 000,00 sumai. Eglė gali peržiūrėti šią sąskaitą faktūrą naudodama mygtuką **Operacijos**, esantį puslapyje **Klientai**.

| Kvitas   | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10020 | PVM sąskaita faktūra          | 2015-06-25 | 10020   | 1000,00                             |                                       | 1000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Dalinis mokėjimas prieš mokėjimo nuolaidos datą
Liepos 2 d. 4027 klientas atlieka dalinį 297,00 SF mokėjimą. Mokėjimui yra gali būti taikoma mokėjimo nuolaida, nes „Fabrikam“ suteikia galimybę mokėjimo nuolaidas taikyti daliniams mokėjimams, o mokėjimas atliekamas prieš mokėjimo nuolaidos datą. Todėl 4027 klientui pritaikoma 3,00 mokėjimo nuolaida. Arnas įrašo 4027 kliento mokėjimą naudodamas mokėjimų žurnalą. Tada Arnas atidaro puslapį **Sudengti operacijas**, kad galėtų pažymėti sudengtiną SF.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10020 | 4027    | 2015-06-25 | 2015-07-25 | 10020   | 1000,00                             | USD      | 297,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas** apačioje. Jei lauko **Sudengtina suma** reikšmės nepakeisite į 297,00, rodomos lauko **Mokėjimo nuolaidos suma** reikšmės skirsis. Tačiau užregistravus mokėjimą bus taikoma 3,00 mokėjimo nuolaida, nes sudengimo funkcija automatiškai koreguoja lauko **Sudengtina suma **vertę.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 3,00      |

Arnas šį mokėjimą užregistruoja. SF balansas dabar yra 700,00. Galima matyti toliau nurodytas kliento operacijas.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10020  | PVM sąskaita faktūra          | 2015-06-25 | 10020   | 1000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Mokėjimas         | 2015-07-01  |         |                                      | 297,00                                | 0,00    | USD      |
| NUOL-10020 |  Mokėjimo nuolaida   | 2015-07-01  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Likęs mokėjimas po mokėjimo nuolaidos datos
4027 klientas apmoka likusią šios SF sumą liepos 11 d., kuri yra po mokėjimo nuolaidos laikotarpio. Puslapio **Sudengti operacijas** lauke **Įvertinta mokėjimo nuolaida** nuolaidos suma nerodoma, o reikšmė lauke **Mokėjimo nuolaidos suma** yra **0,00**. Kai 4027 klientas mokės likusius 700,00, nebus taikoma jokia papildoma nuolaida.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10020 | 4027    | 2015-06-25 | 2015-07-25 | 10020   | 700,00                               | USD      | 700,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas** apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 0,00      |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 3,00      |
| Taikytinos mokėjimo nuolaidos suma | 0,00      |

Jei Arnas pakeis lauko **Naudoti mokėjimo nuolaidą** reikšmę į **Visada**, bus nepaisoma parametro **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** ir bus pritaikyta mokėjimo nuolaida. Mokėjimo suma pasikeičia į 693,00, o mokėjimo nuolaida yra likę 7,00.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Pasirinkta | Visada            | LFSF-10020 | 4027    | 2015-06-25 | 2015-07-25 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas** apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 7,00      |
| Naudokite mokėjimo nuolaidą            | Visada    |
| Pritaikyta mokėjimo nuolaida          | 3,00      |
| Taikytinos mokėjimo nuolaidos suma | 7,00      |

Arnas pakeičia lauko **Naudoti mokėjimo nuolaidą** reikšmę atgal į **Įprasta**, nes jis nenori klientui taikyti likusios 7,00 mokėjimo nuolaidos. Tada Arnas užregistruoja mokėjimą. Atidaręs puslapį **Kliento operacijos**, Arnas mato, kad SF balansas yra 0,00. Jis taip pat mato, kad yra du mokėjimai. Vienas mokėjimas yra už 297,00 su 3,00 mokėjimo nuolaida, o kitas mokėjimas yra už 700,00.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10020  | PVM sąskaita faktūra          | 2015-06-25 | 10020   | 1000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 2015-07-01  |         |                                      | 297,00                                | 0,00    | USD      |
| NUOL-10020 |                  | 2015-07-01  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 7/11/2015 |         |                                      | 700,00                                | 0,00    | USD      |





