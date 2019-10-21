---
title: Mokėjimo nuolaidos taikymas ne mokėjimo nuolaidos laikotarpiu
description: Šiame straipsnyje pateikiami du scenarijai, kuriais parodoma, kaip galima taikyti mokėjimo nuolaidą, net jei mokėjimas atliekamas ne mokėjimo nuolaidos laikotarpiu.
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
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a166e9a0d43da80986dd63d6739b104745b115
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189481"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>Mokėjimo nuolaidos taikymas ne mokėjimo nuolaidos laikotarpiu

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami du scenarijai, kuriais parodoma, kaip galima taikyti mokėjimo nuolaidą, net jei mokėjimas atliekamas ne mokėjimo nuolaidos laikotarpiu.

Birželio 28 d. Eglė 3052 tiekėjui sukuria sąskaitą faktūrą 2 000,00 sumai. SF galima 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų.

## <a name="use-cash-discount-option--always"></a>Naudokite mokėjimo nuolaidos pasirinktį = Visada
April sukuria mokėjimą liepos 1 d., o tai yra po nuolaidos datos. April atidaro puslapį **Sudengti operacijas**, norėdama peržiūrėti operacijas, kurias galima sudengti. 

April pažymi sąskaitą faktūrą apmokėti. Netaikoma jokia mokėjimo nuolaida, nes mokėjimas atliktas praėjus nuolaidos laikotarpiui. Tačiau tiekėjas Eglei pateikė patvirtinimą, nuolaidą pritaikyti bet kokiu atveju. Todėl Eglė pakeičia vertę lauke **Naudokite mokėjimo nuolaidą** į **Visada**.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Mokėjimo nuolaidos data | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Visada            | SF-10030 | 3052    | 2015-06-28          | 2015-07-12 | 10030   | -2000,00.                      | USD      | -1980,00.        |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | –20,00    |
| Naudokite mokėjimo nuolaidą            | Visada    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Data, naudojama skaičiuojant nuolaidas = Pasirinkta data
Jei užregistruota ir sąskaita faktūra, ir mokėjimas, mokėjimo nuolaidą vis dar galima taikyti ir sudengus operacijas puslapyje **Sudengti operacijas**. April pakeičia vertę lauke **Data, naudojama skaičiuojant nuolaidas** į **Pasirinkta data**. Tada ji įveda birželio 28 d. datą, kuri patenka į tos sąskaitos faktūros mokėjimo nuolaidos laikotarpį. Ta data naudojama apskaičiuoti operacijos mokėjimo nuolaidą. Puslapyje **Sudengti atviras operacijas** April mato, kad pagal numatytuosius nustatymus rodoma visa 20,00 nuolaida. Sąskaitos faktūros eilutėje rodoma, kad sudengtina suma yra 1980,00.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Mokėjimo nuolaidos data | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta ir paryškinta | Įprastas            | SF-10030 | 3052    | 2015-06-28          | 2015-07-12 | 10030   | -2000,00.                      | USD      | -1980,00.        |
| Pasirinkta                 | Įprastas            | PROG-10030 | 3052    | 7/15/2015          | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje. Pritaikomos nuolaidos suma yra 20,00, nes sudengtina sąskaitos faktūros suma yra numatytoji 1980,00 suma.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | –20,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –20,00    |

April pakeičia lauko **Sudengtina suma** vertę į **500,00**. Vertė lauke **Taikytinos mokėjimo nuolaidos suma** yra apskaičiuota **5,05**.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta ir paryškinta | Įprastas            | SF-10030 | 3052    | 2015-06-28 | 2015-07-12 | 10030   | 2,000.00                       | USD      | –500,00          |
| Pasirinkta                 | Įprastas            | PROG-10030 | 3052    | 7/15/2015 | 7/15/2015 |         | 500,00                         | USD      | 500,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje. Vertė lauke **Taikytinos mokėjimo nuolaidos suma** yra **5,05**, nes sudengtina sąskaitos faktūros suma buvo pakeista į 500,00 mokėjimo sumą.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | –20,00    |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –5,05     |





