---
title: Konkrečių verslo sričių kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie konkrečių verslo sričių funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8f0812e4262a264ffc89b72e0f4fc8c55d6c6822095f550c8f05296bb057a38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712338"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Konkrečių verslo sričių kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) konkrečių verslo sričių funkcijas, galima atlikti skaičiavimus ir duomenų prieigos užklausas, susijusias su „Microsoft Dynamics 365 Finance“ diegimu. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija| Aprašymas |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD10 reiškinį pagal nurodyto sąskaitos faktūros numerio skaitmenis. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią vieną finansinės dimensijos ID, paimtą iš nurodytos eilutės. Nurodytoje eilutėje visos dimensijos pateikiamos kaip kableliais atskirtų ID sąrašas. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, nurodančią rezultatą konvertuojant nurodytą piniginę sumą iš nurodytos pirminės valiutos į nurodytą norimą valiutą naudojant nurodytos įmonės parametrus nurodytą dieną. |
| [CurCredRef](er-functions-other-curcredref.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo kreditoriaus nuorodą pagal nurodyto sąskaitos faktūros numerio skaitmenis. |
| [FA_Balance](er-functions-other-fabalance.md) | Ši funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo, ataskaitinių metų ir ataskaitos datos ilgalaikio turto balanso duomenys. |
| [FA_Sum](er-functions-other-fasum.md) | Ši funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo ir datų laikotarpio ilgalaikio turto sumų duomenys. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią juridinio subjekto (įmonės), prie kurio šiuo metu prisijungęs vartotojas, kodą. |
| [ISOCredRef](er-functions-other-isocredref.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**, jei nurodytoje eilutėje rodomas tinkamas tarptautinis banko sąskaitos numeris (IBAN). Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**. |
| [Mod_97](er-functions-other-mod97.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD97 reiškinį pagal nurodyto sąskaitos faktūros numerio skaitmenis. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią naują sugeneruotą numeracijos reikšmę pagal nurodytą numeraciją, aprėptį ir aprėpties ID. Aprėpties ID yra lygus įmonės kodui pagal kontekstą, kuriame paleistas ER formatas. |
| [RoundAmount](er-functions-other-roundamount.md) | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, nurodančią rezultatą, kai nurodyta suma suapvalinama iki nurodyto skaitmenų po kablelio skaičiaus pagal nurodytą apvalinimo taisyklę. |
| [TableName2ID](er-functions-other-tablename2id.md) | Ši funkcija pateikia nurodyto lentelės pavadinimo lentelės ID skaitinį vaizdavimą kaip tipo *Sveikasis skaičius* reikšmę. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]