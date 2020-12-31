---
title: Nuolaidos, kuri yra didesnė už apskaičiuotą tiekėjo mokėjimo nuolaidą, pritaikymas
description: Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą. Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą.
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
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445833"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Nuolaidos, kuri yra didesnė už apskaičiuotą tiekėjo mokėjimo nuolaidą, pritaikymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą. Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą. 

Tiekėjas 3051 suteikia „Fabrikam“ 4 procentų mokėjimo nuolaidą, jei sąskaita faktūra apmokama per septynias dienas. Birželio 29 d. April įveda sąskaitą faktūrą 1000,00 sumai. Tiekėjas leidžia April pritaikyti 60,00 nuolaidą vietoj numatytosios 40,00 nuolaidos, kuri galima sąskaitai faktūrai. April įrašo vienkartinį mokėjimą naudodama Mokėtinų sąskaitų mokėjimo žurnalą. Ji įveda mokėjimo tiekėją ir tada atidaro puslapį **Sudengti operacijas**. Eglė pažymi sąskaitą faktūrą ir pakeičia vertę lauke **Mokėjimo nuolaidos suma** į **60,00**.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | SF-10040 | 3051    | 2015-06-29 | 7/29/2015 | 10040   | 1000,00                       | USD      | 940,00           |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | 60,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 60,00     |

April užregistruoja mokėjimų žurnalą. Sąskaita faktūra yra visiškai sudengta naudojant 940.00 mokėjimą ir 60,00 nuolaida.



