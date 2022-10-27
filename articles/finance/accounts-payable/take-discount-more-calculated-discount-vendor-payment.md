---
title: Paimkite daugiau nei apskaičiuota nuolaida pardavėjo mokėjimui
description: Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą. Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27a6ec8fdba495535227d9d893d59edac5588985
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715700"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Paimkite daugiau nei apskaičiuota nuolaida pardavėjo mokėjimui

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą. Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą. 

Tiekėjas 3051 suteikia „Fabrikam“ 4 procentų mokėjimo nuolaidą, jei sąskaita faktūra apmokama per septynias dienas. Birželio 29 d. April įveda sąskaitą faktūrą 1000,00 sumai. Tiekėjas leidžia April pritaikyti 60,00 nuolaidą vietoj numatytosios 40,00 nuolaidos, kuri galima sąskaitai faktūrai. April įrašo vienkartinį mokėjimą naudodama Mokėtinų sąskaitų mokėjimo žurnalą. Ji įveda mokėjimo tiekėją ir tada atidaro puslapį **Sudengti operacijas**. Eglė pažymi sąskaitą faktūrą ir pakeičia vertę lauke **Mokėjimo nuolaidos suma** į **60,00**.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | SF-10040 | 3051    | 2015-06-29 | 7/29/2015 | 10040   | 1000,00                       | USD      | 940,00           |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje.

| Laukas                        | Reikšmė     |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | 60.00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 60,00     |

April užregistruoja mokėjimų žurnalą. Sąskaita faktūra yra visiškai sudengta naudojant 940.00 mokėjimą ir 60,00 nuolaida.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
