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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040991"
---
# <span data-ttu-id="42026-103"><a name="REPLACE">REPLACE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="42026-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42026-104">`REPLACE` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę po to, kai visa arba jos dalis buvo pakeista kita eilute.</span><span class="sxs-lookup"><span data-stu-id="42026-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="42026-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="42026-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="42026-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="42026-106">Arguments</span></span>

<span data-ttu-id="42026-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="42026-107">`text`: *String*</span></span>

<span data-ttu-id="42026-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="42026-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="42026-109">`pattern`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="42026-109">`pattern`: *String*</span></span>

<span data-ttu-id="42026-110">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, kurį reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="42026-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="42026-111">Jei `regular expression flag` argumentas yra **TEISINGAS**, šiame argumente yra įprasta išraiška, apibrėžianti ieškos šabloną ir pakaitinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="42026-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="42026-112">`replacement`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="42026-112">`replacement`: *String*</span></span>

<span data-ttu-id="42026-113">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, šiame argumente yra tekstas, naudotinas kaip pakaitas.</span><span class="sxs-lookup"><span data-stu-id="42026-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="42026-114">Jei `regular expression flag` argumentas yra **TEISINGAS**, šis argumentas nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="42026-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="42026-115">`regular expression flag`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="42026-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="42026-116">*Bulio logikos* reikšmė, nurodanti, ar pakeitimui atlikti naudojama įprasta išraiška.</span><span class="sxs-lookup"><span data-stu-id="42026-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="42026-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="42026-117">Return values</span></span>

<span data-ttu-id="42026-118">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="42026-118">*String*</span></span>

<span data-ttu-id="42026-119">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="42026-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="42026-120">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="42026-120">Usage notes</span></span>

<span data-ttu-id="42026-121">Jei `regular expression flag` argumentas yra **TEISINGAS**, ši funkcija grąžina nurodytą eilutę, po to, kai ji buvo pakeista pagal `pattern` argumentui nurodytą įprastą išraišką.</span><span class="sxs-lookup"><span data-stu-id="42026-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="42026-122">Įprasta išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="42026-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="42026-123">Jei `regular expression flag` argumentas yra **KLAIDINGAS**, ši funkcija vykdoma kaip [VERSTI](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="42026-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="42026-124">Nurodyti `replacement` argumento simboliai naudojami pakeisti rastus simbolius.</span><span class="sxs-lookup"><span data-stu-id="42026-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="42026-125">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="42026-125">Example 1</span></span>

<span data-ttu-id="42026-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` pritaiko įprastą išraišką, kuri pašalina visus neskaitinius simbolius ir grąžina **„19234564971“**.</span><span class="sxs-lookup"><span data-stu-id="42026-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="42026-127">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="42026-127">Example 2</span></span>

<span data-ttu-id="42026-128">`REPLACE ("abcdef", "cd", "GH", false)` pakeičia šabloną **„cd“** į eilutę **„GH“** ir grąžinama **„abGHef“**.</span><span class="sxs-lookup"><span data-stu-id="42026-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42026-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="42026-129">Additional resources</span></span>

[<span data-ttu-id="42026-130">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="42026-130">Text functions</span></span>](er-functions-category-text.md)
