---
title: Teksto kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie teksto funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916619"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Teksto kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) teksto funkcijas, galima atlikti operacijas su duomenų tipo *Eilutė* duomenų šaltiniais. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [Char](er-functions-text-char.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje yra vienas simbolis, kurį nurodo nurodytas „Unicode“ numeris. |
| [Sujungti](er-functions-text-concatenate.md) | Ši funkcija visas nurodytas teksto eilutes pateikia kaip tipo *Eilutė* reikšmę, jas sujungus į vieną eilutę. |
| [Formatas](er-functions-text-format.md) | Ši funkcija nurodytą eilutę pateikia kaip tipo *Eilutė* reikšmę, suformatuotą visus **%N** pasikartojimus pakeičiant *N*-uoju argumentu. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Ši funkcija nurodytame išvardijimo duomenų šaltinyje ieško konkrečios *Enum* reikšmės, naudodama išvardijimo pavadinimą, kuris nurodytas kaip tipo *Eilutė* reikšmė. Jei *Enum* reikšmė randama, funkcija ją pateikia. |
| [GuidValue](er-functions-text-guidvalue.md) | Ši funkcija nurodytą tipo *Eilutė* įvestį konvertuoja į duomenų elementą, kurio tipas – *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Ši funkcija analizuoja duomenis „JavaScript Object Notation“ (JSON) formatu, kuris pasiekiamas nurodytu keliu, ir išgaunama skaliarinė reikšmė pagal nurodytą ID. Tada grąžinama išskleista skaliarinė reikšmė kaip *Eilutės* reikšmė. |
| [Kairėn](er-functions-text-left.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius nuo nurodytos eilutės pradžios. |
| [Len](er-functions-text-len.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo konkrečios eilutės simbolių skaičių. |
| [Lower](er-functions-text-lower.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę, ją konvertavus į mažąsias raides. |
| [Mid](er-functions-text-mid.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradedant nuo nurodytos vietos. |
| [NumberFormat](er-functions-text-numberformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo konkretų skaičių nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Ši funkcija nurodytą skaičių pateikia kaip tipo *Eilutė* reikšmę po to, kai ji buvo nurodyta žodžiais (t. y. konvertuota į teksto eilutes) pasirinkta kalba. |
| [PadLeft](er-functions-text-padleft.md) | Ši funkcija pateikia tipo *Eilutė* nurodyto ilgio reikšmę, kurioje nurodytos eilutės pradžia užpildyta vienu ar keliais nurodytais simboliais. |
| [QrCode](er-functions-text-qrcode.md) | Ši funkcija pateikia tipo *Konteineris* reikšmę, kuri nurodo konkrečios eilutės greito atsakymo kodo (QR kodo) vaizdą dvejetainiu formatu. |
| [Pakeisti](er-functions-text-replace.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę po to, kai ji visa arba jos dalis buvo pakeista kita eilute. |
| [Dešinėn](er-functions-text-right.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius nuo nurodytos eilutės pabaigos. |
| [Tekstas](er-functions-text-text.md) | Ši funkcija pateikia nurodytą skaičių kaip tipo *Eilutė* reikšmę, jį konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus. |
| [Versti](er-functions-text-translate.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę po to, kai ji visa arba jos dalis buvo pakeista kita eilute. |
| [Trim](er-functions-text-trim.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę, sutrumpinus priekinius ir galinius tarpus bei pašalinus perteklinius tarpus tarp žodžių. |
| [Upper](er-functions-text-upper.md) | Ši funkcija nurodytą teksto eilutę pateikia kaip tipo *Eilutė* reikšmę, ją konvertavus į didžiąsias raides. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)
