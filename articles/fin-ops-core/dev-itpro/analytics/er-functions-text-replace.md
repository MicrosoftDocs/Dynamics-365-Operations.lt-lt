---
title: REPLACE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama REPLACE elektroninių ataskaitų (ER) funkcija.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916872"
---
# <span data-ttu-id="447bb-103"><a name="REPLACE">REPLACE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="447bb-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="447bb-104">`REPLACE` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę po to, kai visa arba jos dalis buvo pakeista kita eilute.</span><span class="sxs-lookup"><span data-stu-id="447bb-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="447bb-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="447bb-105">Syntax</span></span>

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="447bb-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="447bb-106">Arguments</span></span>

<span data-ttu-id="447bb-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="447bb-107">`text`: *String*</span></span>

<span data-ttu-id="447bb-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="447bb-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="447bb-109">`pattern`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="447bb-109">`pattern`: *String*</span></span>

<span data-ttu-id="447bb-110">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, kurį reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="447bb-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="447bb-111">Jei `regular expression flag` argumentas yra **TEISINGAS**, šiame argumente yra įprasta išraiška, apibrėžianti ieškos šabloną ir pakaitinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="447bb-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="447bb-112">`replacement`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="447bb-112">`replacement`: *String*</span></span>

<span data-ttu-id="447bb-113">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, naudotinas kaip pakaitas.</span><span class="sxs-lookup"><span data-stu-id="447bb-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="447bb-114">Jei `regular expression flag` argumentas yra **TEISINGAS**, šis argumentas nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="447bb-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="447bb-115">`regular expression flag`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="447bb-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="447bb-116">*Bulio logikos* reikšmė, nurodanti, ar pakeitimui atlikti naudojama įprasta išraiška.</span><span class="sxs-lookup"><span data-stu-id="447bb-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="447bb-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="447bb-117">Return values</span></span>

<span data-ttu-id="447bb-118">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="447bb-118">*String*</span></span>

<span data-ttu-id="447bb-119">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="447bb-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="447bb-120">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="447bb-120">Usage notes</span></span>

<span data-ttu-id="447bb-121">Jei `regular expression flag` argumentas yra **TEISINGAS**, ši funkcija grąžina nurodytą eilutę, po to, kai ji buvo pakeista pagal `pattern` argumentui nurodytą įprastą išraišką.</span><span class="sxs-lookup"><span data-stu-id="447bb-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="447bb-122">Įprasta išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="447bb-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="447bb-123">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, ši funkcija vykdoma kaip [VERSTI](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="447bb-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="447bb-124">Nurodyti `replacement` argumento simboliai naudojami pakeisti rastus simbolius.</span><span class="sxs-lookup"><span data-stu-id="447bb-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="447bb-125">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="447bb-125">Example 1</span></span>

<span data-ttu-id="447bb-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` pritaiko įprastą išraišką, kuri pašalina visus neskaitinius simbolius ir grąžina **„19234564971“**.</span><span class="sxs-lookup"><span data-stu-id="447bb-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="447bb-127">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="447bb-127">Example 2</span></span>

<span data-ttu-id="447bb-128">`REPLACE ("abcdef", "cd", "GH", false)` pakeičia šabloną **„cd“** į eilutę **„GH“** ir grąžinama **„abGHef“**.</span><span class="sxs-lookup"><span data-stu-id="447bb-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="447bb-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="447bb-129">Additional resources</span></span>

[<span data-ttu-id="447bb-130">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="447bb-130">Text functions</span></span>](er-functions-category-text.md)
