---
title: Teksto kategorijos ER funkcijų sąrašas
description: Šiame straipsnyje pateikta informacija apie teksto funkcijas, kurias palaiko elektroninės ataskaitos (ER).
author: kfend
ms.date: 02/28/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e4c7885024586034c062304cce21a25e5b6c8c9b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268800"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Teksto kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) teksto funkcijas, galima atlikti operacijas su duomenų tipo *Eilutė* duomenų šaltiniais. Šiame straipsnyje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [Char](er-functions-text-char.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje yra vienas simbolis, kurį nurodo nurodytas „Unicode“ numeris. |
| [Sujungti](er-functions-text-concatenate.md) | Ši funkcija visas nurodytas teksto eilutes pateikia kaip tipo *Eilutė* reikšmę, jas sujungus į vieną eilutę. |
| [Formatas](er-functions-text-format.md) | Ši funkcija nurodytą eilutę pateikia kaip tipo *Eilutė* reikšmę, suformatuotą visus **%N** pasikartojimus pakeičiant *N*-uoju argumentu. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Ši funkcija nurodytame išvardijimo duomenų šaltinyje ieško konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip tipo *Eilutė* reikšmė. Jei *Enum* reikšmė randama, funkcija ją pateikia. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Ši funkcija ieško konkrečios žymės, kad būtų grąžinama *[...](er-formula-supported-data-types-primitive.md#string)* eilutės vertė, nurodanti nurodytos žymės konvertavimą į nurodytą kalbą. |
| [GuidValue](er-functions-text-guidvalue.md) | Ši funkcija nurodytą tipo *Eilutė* įvestį konvertuoja į duomenų elementą, kurio tipas – *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Ši funkcija analizuoja duomenis „JavaScript Object Notation“ (JSON) formatu, kuris pasiekiamas nurodytu keliu, ir išgaunama skaliarinė reikšmė pagal nurodytą ID. Tada grąžinama išskleista skaliarinė reikšmė kaip *Eilutės* reikšmė. |
| [Kairėn](er-functions-text-left.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius nuo nurodytos eilutės pradžios. |
| [Len](er-functions-text-len.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo konkrečios eilutės simbolių skaičių. |
| [Lower](er-functions-text-lower.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę, ją konvertavus į mažąsias raides. |
| [Mid](er-functions-text-mid.md) | Ši funkcija pateikia tipo *[Eilutė](er-formula-supported-data-types-primitive.md#string)* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradedant nuo nurodytos vietos. |
| [NewGUID](er-functions-text-newguid.md) | Ši funkcija grąžina naujai sugeneruotą *[GUID](er-formula-supported-data-types-primitive.md#guid)* reikšmę. |
| [NumberFormat](er-functions-text-numberformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo konkretų skaičių nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Ši funkcija nurodytą skaičių pateikia kaip tipo *Eilutė* reikšmę po to, kai ji buvo nurodyta žodžiais (t. y. konvertuota į teksto eilutes) pasirinkta kalba. |
| [PadLeft](er-functions-text-padleft.md) | Ši funkcija pateikia tipo *Eilutė* nurodyto ilgio reikšmę, kurioje nurodytos eilutės pradžia užpildyta vienu ar keliais nurodytais simboliais. |
| [QrCode](er-functions-text-qrcode.md) | Ši funkcija pateikia tipo *Konteineris* reikšmę, kuri nurodo konkrečios eilutės greito atsakymo kodo (QR kodo) vaizdą dvejetainiu formatu. |
| [Pakeisti](er-functions-text-replace.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę po to, kai ji visa arba jos dalis buvo pakeista kita eilute. |
| [Dešinėn](er-functions-text-right.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius nuo nurodytos eilutės pabaigos. |
| [Tekstas](er-functions-text-text.md) | Ši funkcija pateikia nurodytą skaičių kaip tipo *Eilutė* reikšmę, jį konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus. |
| [Versti](er-functions-text-translate.md) | Ši funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodyto teksto simbolių pakeitimo kitu pateiktu simbolių rinkiniu rezultatas. |
| [Trim](er-functions-text-trim.md) | Ši funkcija *grąžina* nurodytą teksto eilutę kaip eilutės vertę po skirtuko, grąžinimas, eilučių tiekimas ir formos tiektuvo simboliai buvo pakeisti vienu tarpo simboliu, po to, kai sutrumpinti priekiniai ir galiiniai tarpai ir po kelių tarpų. |
| [Upper](er-functions-text-upper.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę, ją konvertavus į didžiąsias raides. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
