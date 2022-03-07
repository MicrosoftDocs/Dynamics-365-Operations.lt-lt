---
title: Tipų konvertavimo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie tipų konvertavimo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: a6d678c2a38039285bd835abcbbaf13ec00298c0660c62e7496a5d7405db8f61
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766414"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Tipų konvertavimo kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) tipų konvertavimo funkcijas, galima konvertuoti tipų reikšmes. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="type-conversion-functions"></a>Tipų konvertavimo funkcijos

| Funkcija | Aprašymas |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Ši funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę. |
| [IntValue](er-functions-conversion-intvalue.md)       | Ši funkcija pateikia *Int* reikšmę, kuri nurodo nurodytą eilutę. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės. Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius. |
| [Vertė](er-functions-conversion-value.md)             | Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės. |

## <a name="type-conversion-functions-in-the-container-category"></a>Tipų konvertavimo funkcijos (konteinerio kategorija)

Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [konteinerio](er-functions-category-container.md) kategorijai.

| Funkcija | Aprašymas |
|----------|-------------|
| [„Base64StringToContainer”](er-functions-container-base64stringtocontainer.md) | Ši funkcija konvertuoja nurodytą *Eilutės* tipo įvestį į *Konteinerio tipo* duomenų elementą. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Tipų konvertavimo funkcijos (datos ir laiko kategorija)

Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [datos ir laiko kategorijai](er-functions-category-datetime.md).

| Funkcija | Aprašymas |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Data* reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu. |
| [DateValue](er-functions-datetime-datevalue.md)           | Ši funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos reikšmę. |

## <a name="type-conversion-functions-in-the-list-category"></a>Tipų konvertavimo kategorijos (sąrašo kategorija)

Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [sąrašo kategorijai](er-functions-category-list.md).

| Funkcija | Aprašymas |
|----------|-------------|
| [Sąrašas](er-functions-list-list.md)                 | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę kaip naują sąrašą, sukurtą iš nurodytų tipo *Konteineris (įrašas)* argumentų. |
| [ListOfFields](er-functions-list-listoffields.md) | Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal konkretaus tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą. |
| [Skaidyti](er-functions-list-split.md)               | Ši funkcija nurodytą tipo *Eilutė* reikšmę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę. |
| [StringJoin](er-functions-list-stringjoin.md)     | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytoje tipo *Įrašų sąrašas* reikšmėje, reikšmės. Reikšmes galima skirti nurodytu skyrikliu. |

## <a name="type-conversion-functions-in-the-text-category"></a>Tipų konvertavimo kategorijos (teksto kategorija)

Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [teksto kategorijai](er-functions-category-text.md).

| Funkcija | Aprašymas |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje yra vienas simbolis, kurį nurodo nurodytas „Unicode“ numeris. |
| [GuidValue](er-functions-text-guidvalue.md)       | Ši funkcija nurodytą tipo *Eilutė* įvestį konvertuoja į duomenų elementą, kurio tipas – *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo konkretų skaičių nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [QrCode](er-functions-text-qrcode.md)             | Ši funkcija pateikia tipo *Konteineris* reikšmę, kuri nurodo konkrečios eilutės greito atsakymo kodo (QR kodo) vaizdą dvejetainiu formatu. |
| [Tekstas](er-functions-text-text.md)                 | Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią konkretų numerį, ją konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]