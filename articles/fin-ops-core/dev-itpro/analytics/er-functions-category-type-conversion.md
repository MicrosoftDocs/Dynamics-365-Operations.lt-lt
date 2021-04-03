---
title: Tipų konvertavimo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie tipų konvertavimo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561523"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="0fe1b-103">Tipų konvertavimo kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fe1b-104">Naudojant modulio Elektroninės ataskaitos (ER) tipų konvertavimo funkcijas, galima konvertuoti tipų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="0fe1b-105">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="0fe1b-106">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="0fe1b-106">Type conversion functions</span></span>

| <span data-ttu-id="0fe1b-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="0fe1b-107">Function</span></span> | <span data-ttu-id="0fe1b-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0fe1b-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="0fe1b-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="0fe1b-110">Ši funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="0fe1b-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="0fe1b-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="0fe1b-112">Ši funkcija pateikia *Int* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="0fe1b-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="0fe1b-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="0fe1b-114">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="0fe1b-115">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="0fe1b-116">Vertė</span><span class="sxs-lookup"><span data-stu-id="0fe1b-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="0fe1b-117">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="0fe1b-118">Tipų konvertavimo funkcijos (konteinerio kategorija)</span><span class="sxs-lookup"><span data-stu-id="0fe1b-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="0fe1b-119">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [konteinerio](er-functions-category-container.md) kategorijai.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="0fe1b-120">Funkcija</span><span class="sxs-lookup"><span data-stu-id="0fe1b-120">Function</span></span> | <span data-ttu-id="0fe1b-121">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0fe1b-122">„Base64StringToContainer”</span><span class="sxs-lookup"><span data-stu-id="0fe1b-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="0fe1b-123">Ši funkcija konvertuoja nurodytą *Eilutės* tipo įvestį į *Konteinerio tipo* duomenų elementą.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="0fe1b-124">Tipų konvertavimo funkcijos (datos ir laiko kategorija)</span><span class="sxs-lookup"><span data-stu-id="0fe1b-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="0fe1b-125">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [datos ir laiko kategorijai](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="0fe1b-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="0fe1b-126">Funkcija</span><span class="sxs-lookup"><span data-stu-id="0fe1b-126">Function</span></span> | <span data-ttu-id="0fe1b-127">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0fe1b-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="0fe1b-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="0fe1b-129">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="0fe1b-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="0fe1b-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="0fe1b-131">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos tipo *Data* reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="0fe1b-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="0fe1b-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="0fe1b-133">Ši funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos tipo *Eilutė* reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="0fe1b-134">Tipų konvertavimo kategorijos (sąrašo kategorija)</span><span class="sxs-lookup"><span data-stu-id="0fe1b-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="0fe1b-135">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [sąrašo kategorijai](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="0fe1b-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="0fe1b-136">Funkcija</span><span class="sxs-lookup"><span data-stu-id="0fe1b-136">Function</span></span> | <span data-ttu-id="0fe1b-137">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0fe1b-138">Sąrašas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="0fe1b-139">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę kaip naują sąrašą, sukurtą iš nurodytų tipo *Konteineris (įrašas)* argumentų.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="0fe1b-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="0fe1b-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="0fe1b-141">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sukurtą pagal konkretaus tipo *Išvardijimas* arba *Konteineris (įrašas)* argumento struktūrą.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="0fe1b-142">Skaidyti</span><span class="sxs-lookup"><span data-stu-id="0fe1b-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="0fe1b-143">Ši funkcija nurodytą tipo *Eilutė* reikšmę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="0fe1b-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="0fe1b-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="0fe1b-145">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytoje tipo *Įrašų sąrašas* reikšmėje, reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="0fe1b-146">Reikšmes galima skirti nurodytu skyrikliu.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="0fe1b-147">Tipų konvertavimo kategorijos (teksto kategorija)</span><span class="sxs-lookup"><span data-stu-id="0fe1b-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="0fe1b-148">Tolesnėje lentelėje aprašomos tipų konvertavimo funkcijos, priklausančios [teksto kategorijai](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="0fe1b-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="0fe1b-149">Funkcija</span><span class="sxs-lookup"><span data-stu-id="0fe1b-149">Function</span></span> | <span data-ttu-id="0fe1b-150">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="0fe1b-151">Char</span><span class="sxs-lookup"><span data-stu-id="0fe1b-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="0fe1b-152">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje yra vienas simbolis, kurį nurodo nurodytas „Unicode“ numeris.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="0fe1b-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="0fe1b-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="0fe1b-154">Ši funkcija nurodytą tipo *Eilutė* įvestį konvertuoja į duomenų elementą, kurio tipas – *GUID*.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="0fe1b-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="0fe1b-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="0fe1b-156">Ši funkcija pateikia tipo *Eilutė* reikšmę, kuri nurodo konkretų skaičių nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="0fe1b-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="0fe1b-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="0fe1b-158">Ši funkcija pateikia tipo *Konteineris* reikšmę, kuri nurodo konkrečios eilutės greito atsakymo kodo (QR kodo) vaizdą dvejetainiu formatu.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="0fe1b-159">Tekstas</span><span class="sxs-lookup"><span data-stu-id="0fe1b-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="0fe1b-160">Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią konkretų numerį, ją konvertavus į teksto eilutę, kuri formatuojama pagal dabartinio programos egzemplioriaus serverio lokalės parametrus.</span><span class="sxs-lookup"><span data-stu-id="0fe1b-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="0fe1b-161">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0fe1b-161">Additional resources</span></span>

[<span data-ttu-id="0fe1b-162">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="0fe1b-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="0fe1b-163">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="0fe1b-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="0fe1b-164">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="0fe1b-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]