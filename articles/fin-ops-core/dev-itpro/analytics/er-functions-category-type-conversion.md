---
title: Tipų konvertavimo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie tipų konvertavimo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917654"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="ae2e2-103">Tipų konvertavimo kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae2e2-104">Naudojant modulio Elektroninės ataskaitos (ER) tipų konvertavimo funkcijas, galima konvertuoti tipų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="ae2e2-105">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="ae2e2-106">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="ae2e2-106">Type conversion functions</span></span>

| <span data-ttu-id="ae2e2-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="ae2e2-107">Function</span></span> | <span data-ttu-id="ae2e2-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ae2e2-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="ae2e2-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="ae2e2-110">Ši funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ae2e2-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="ae2e2-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="ae2e2-112">Ši funkcija pateikia *Int* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="ae2e2-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="ae2e2-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="ae2e2-114">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="ae2e2-115">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="ae2e2-116">Vertė</span><span class="sxs-lookup"><span data-stu-id="ae2e2-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="ae2e2-117">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="ae2e2-118">Tipų konvertavimo funkcijos (datos ir laiko kategorija)</span><span class="sxs-lookup"><span data-stu-id="ae2e2-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="ae2e2-119">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [datos ir laiko kategorijai](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="ae2e2-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="ae2e2-120">Funkcija</span><span class="sxs-lookup"><span data-stu-id="ae2e2-120">Function</span></span> | <span data-ttu-id="ae2e2-121">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ae2e2-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="ae2e2-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="ae2e2-123">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="ae2e2-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="ae2e2-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="ae2e2-125">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Data* reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="ae2e2-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="ae2e2-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="ae2e2-127">Ši funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="ae2e2-128">Tipų konvertavimo kategorijos (sąrašo kategorija)</span><span class="sxs-lookup"><span data-stu-id="ae2e2-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="ae2e2-129">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [sąrašo kategorijai](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="ae2e2-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="ae2e2-130">Funkcija</span><span class="sxs-lookup"><span data-stu-id="ae2e2-130">Function</span></span> | <span data-ttu-id="ae2e2-131">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ae2e2-132">Sąrašas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="ae2e2-133">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę kaip naują sąrašą, sukurtą iš nurodytų tipo *Konteineris (įrašas)* argumentų.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="ae2e2-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="ae2e2-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="ae2e2-135">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal konkretaus tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="ae2e2-136">Skaidyti</span><span class="sxs-lookup"><span data-stu-id="ae2e2-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="ae2e2-137">Ši funkcija nurodytą tipo *Eilutė* reikšmę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="ae2e2-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="ae2e2-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="ae2e2-139">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytoje tipo *Įrašų sąrašas* reikšmėje, reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="ae2e2-140">Reikšmes galima skirti nurodytu skyrikliu.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="ae2e2-141">Tipų konvertavimo kategorijos (teksto kategorija)</span><span class="sxs-lookup"><span data-stu-id="ae2e2-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="ae2e2-142">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [teksto kategorijai](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="ae2e2-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="ae2e2-143">Funkcija</span><span class="sxs-lookup"><span data-stu-id="ae2e2-143">Function</span></span> | <span data-ttu-id="ae2e2-144">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="ae2e2-145">Char</span><span class="sxs-lookup"><span data-stu-id="ae2e2-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="ae2e2-146">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje yra vienas simbolis, kurį nurodo nurodytas „Unicode“ numeris.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="ae2e2-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="ae2e2-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="ae2e2-148">Ši funkcija nurodytą tipo *Eilutė* įvestį konvertuoja į duomenų elementą, kurio tipas – *GUID*.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="ae2e2-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="ae2e2-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="ae2e2-150">Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo konkretų skaičių nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="ae2e2-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="ae2e2-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="ae2e2-152">Ši funkcija pateikia tipo *Konteineris* reikšmę, kuri nurodo konkrečios eilutės greito atsakymo kodo (QR kodo) vaizdą dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="ae2e2-153">Tekstas</span><span class="sxs-lookup"><span data-stu-id="ae2e2-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="ae2e2-154">Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią konkretų numerį, ją konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus.</span><span class="sxs-lookup"><span data-stu-id="ae2e2-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ae2e2-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ae2e2-155">Additional resources</span></span>

[<span data-ttu-id="ae2e2-156">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ae2e2-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="ae2e2-157">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="ae2e2-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ae2e2-158">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="ae2e2-158">Electronic reporting formula language</span></span>](er-formula-language.md)
