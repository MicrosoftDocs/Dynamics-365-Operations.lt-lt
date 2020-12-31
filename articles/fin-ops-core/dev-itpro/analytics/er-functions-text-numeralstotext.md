---
title: NUMERALSTOTEXT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMERALSTOTEXT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680223"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="43a19-103">NUMERALSTOTEXT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="43a19-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43a19-104">`NUMERALSTOTEXT`f unkcija grąžina nurodytą skaičių kaip *Eilutės* reikšmę po to, kai ji buvo nurodyta žodžiais (t. y. konvertuota į teksto eilutes) pasirinkta kalba.</span><span class="sxs-lookup"><span data-stu-id="43a19-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a19-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="43a19-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="43a19-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="43a19-106">Arguments</span></span>

<span data-ttu-id="43a19-107">`number`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="43a19-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="43a19-108">Skaitinė reikšmė, nurodanti skaičių, kuris turi būti nurodytas žodžiais.</span><span class="sxs-lookup"><span data-stu-id="43a19-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="43a19-109">`language`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="43a19-109">`language`: *String*</span></span>

<span data-ttu-id="43a19-110">*Eilutės* reikšmė, nurodanti kalbos kodą.</span><span class="sxs-lookup"><span data-stu-id="43a19-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="43a19-111">`currency`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="43a19-111">`currency`: *String*</span></span>

<span data-ttu-id="43a19-112">*Eilutės* reikšmė, nurodanti valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="43a19-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="43a19-113">`print currency name flag`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="43a19-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="43a19-114">*Bulio logikos* reikšmė, nurodanti, ar į nurodytų žodžiais skaičių tekstą reikia įtraukti naują valiutos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="43a19-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="43a19-115">`decimal points`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="43a19-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="43a19-116">*Sveikojo skaičiaus* reikšmė, nurodanti skaičių po kablelio, kurį nurodytų žodžiais skaičių tekstas turėtų pateikti.</span><span class="sxs-lookup"><span data-stu-id="43a19-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="43a19-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="43a19-117">Return values</span></span>

<span data-ttu-id="43a19-118">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="43a19-118">*String*</span></span>

<span data-ttu-id="43a19-119">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="43a19-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="43a19-120">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="43a19-120">Usage notes</span></span>

<span data-ttu-id="43a19-121">Kalbos kodas nėra būtinas.</span><span class="sxs-lookup"><span data-stu-id="43a19-121">The language code is optional.</span></span> <span data-ttu-id="43a19-122">Jei nurodomas kaip tuščia eilutė, naudojamas vykdomo konteksto kalbos kodas.</span><span class="sxs-lookup"><span data-stu-id="43a19-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="43a19-123">Numatytasis kalbos kodas yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="43a19-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="43a19-124">Vykdomo konteksto kalbos kodas apibrėžiamas veikiančios elektroninių ataskaitų (ER) formato elemente **Aplankas** arba **Failas**.</span><span class="sxs-lookup"><span data-stu-id="43a19-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="43a19-125">Valiutos kodas nėra būtinas.</span><span class="sxs-lookup"><span data-stu-id="43a19-125">The currency code is optional.</span></span> <span data-ttu-id="43a19-126">Jei nurodomas kaip tuščia eilutė, naudojama vykdomo konteksto įmonės valiuta.</span><span class="sxs-lookup"><span data-stu-id="43a19-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="43a19-127">Argumentai `print currency name flag`ir `decimal points` analizuojami tik šiais kalbos kodais : **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, ir **RU**.</span><span class="sxs-lookup"><span data-stu-id="43a19-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="43a19-128">Be to, argumentas `print currency name flag` analizuojamas tik įmonėms, kurių šalies arba regiono kontekste palaikomas valiutos pavadinimų linksniavimas.</span><span class="sxs-lookup"><span data-stu-id="43a19-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="43a19-129">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="43a19-129">Example 1</span></span>

<span data-ttu-id="43a19-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` grąžina **„One Thousand Two Hundred Thirty Four and 56“**.</span><span class="sxs-lookup"><span data-stu-id="43a19-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="43a19-131">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="43a19-131">Example 2</span></span>

<span data-ttu-id="43a19-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` grąžina **„sto dwadzieścia“**.</span><span class="sxs-lookup"><span data-stu-id="43a19-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="43a19-133">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="43a19-133">Example 3</span></span>

<span data-ttu-id="43a19-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` grąžina **„сто двадцать евро 21 евроцент“**.</span><span class="sxs-lookup"><span data-stu-id="43a19-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43a19-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="43a19-135">Additional resources</span></span>

[<span data-ttu-id="43a19-136">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="43a19-136">Text functions</span></span>](er-functions-category-text.md)
