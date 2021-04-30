---
title: ER SPLIT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SPLIT funkcija.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853448"
---
# <a name="split-er-function"></a><span data-ttu-id="b3c57-103">ER SPLIT funkcija</span><span class="sxs-lookup"><span data-stu-id="b3c57-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3c57-104">`SPLIT` funkcija nurodytą įvesties eilutę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b3c57-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b3c57-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="b3c57-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="b3c57-106">Ši sintaksė naudojama norint nurodytą įvesties eilutę skaidyti į antrines eilutes, iš kurių kiekvienos ilgis nurodomas atskirai.</span><span class="sxs-lookup"><span data-stu-id="b3c57-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="b3c57-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="b3c57-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="b3c57-108">Ši sintaksė naudojama norint nurodytą įvesties eilutę skaidyti į antrines eilutes (pagal nurodytą skyriklį).</span><span class="sxs-lookup"><span data-stu-id="b3c57-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="b3c57-109">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b3c57-109">Arguments</span></span>

<span data-ttu-id="b3c57-110">`input`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="b3c57-110">`input`: *String*</span></span>

<span data-ttu-id="b3c57-111">Skaidytinas tekstas.</span><span class="sxs-lookup"><span data-stu-id="b3c57-111">The text to split.</span></span>

<span data-ttu-id="b3c57-112">`length`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="b3c57-112">`length`: *Integer*</span></span>

<span data-ttu-id="b3c57-113">Maksimalus vienos antrinės eilutės ilgis.</span><span class="sxs-lookup"><span data-stu-id="b3c57-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="b3c57-114">`delimiter`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="b3c57-114">`delimiter`: *String*</span></span>

<span data-ttu-id="b3c57-115">Skyriklis, naudojamas antrinėms eilutėms atskirti.</span><span class="sxs-lookup"><span data-stu-id="b3c57-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3c57-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b3c57-116">Return values</span></span>

<span data-ttu-id="b3c57-117">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b3c57-117">*Record list*</span></span>

<span data-ttu-id="b3c57-118">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b3c57-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b3c57-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="b3c57-119">Usage notes</span></span>

<span data-ttu-id="b3c57-120">Pateikto sąrašo įrašų struktūrą sudaro tipo *Eilutė* laukas **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="b3c57-121">Šiame kiekvieno pateikto sąrašo įrašo lauke pateikiamos sugeneruotos antrinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="b3c57-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="b3c57-122">Jei `delimiter` argumentas tuščias, pateiktą naują sąrašą sudaro vienas įrašas, kuriame yra tipo *Eilutė* laukas **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="b3c57-123">Šiame lauke yra įvesties tekstas.</span><span class="sxs-lookup"><span data-stu-id="b3c57-123">This field contains the input text.</span></span>

<span data-ttu-id="b3c57-124">Jei `input` argumentas tuščias, pateikiamas naujas tuščias sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b3c57-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="b3c57-125">Jei `input` arba `delimiter` argumentas nenurodytas (neapibrėžtas), pateikiama programos išimtis.</span><span class="sxs-lookup"><span data-stu-id="b3c57-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="b3c57-126">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b3c57-126">Example 1</span></span>

<span data-ttu-id="b3c57-127">`SPLIT ("abcd", 3)` pateikia naują sąrašą, sudarytą iš dviejų įrašų, kuriuose yra tipo *Eilutė* laukas **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b3c57-128">Pirmame įraše esančiame lauke **Reikšmė** yra tekstas **„abc“**, o antrame įraše esančiame lauke **Reikšmė** yra tekstas **„d“**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b3c57-129">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b3c57-129">Example 2</span></span>

<span data-ttu-id="b3c57-130">`SPLIT ("XAb aBy", "aB")` pateikia naują sąrašą, sudarytą iš trijų įrašų, kuriuose yra tipo *Eilutė* laukas **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="b3c57-131">Pirmo įrašo lauke **Reikšmė** yra tekstas **„X“**, antro įrašo lauke **Reikšmė** yra tekstas **„&nbsp;“**, o trečio įrašo lauke **Reikšmė** yra tekstas **„y“**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="b3c57-132">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b3c57-132">Example 3</span></span>

<span data-ttu-id="b3c57-133">Galite naudoti funkciją [RODYKLĖ](er-functions-list-index.md), kad pasiektumėte atskirus nurodytos įvesties eilutės elementus.</span><span class="sxs-lookup"><span data-stu-id="b3c57-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="b3c57-134">Jei įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Mano sąrašas** ir jam konfigūruojate išraišką `SPLIT("abc", 1)`, išraiška `INDEX(MyList,2).Value` grąžina teksto reikšmę **„b“**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="b3c57-135">4 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b3c57-135">Example 4</span></span>

<span data-ttu-id="b3c57-136">Funkcija [IŠVARDYTI](er-functions-list-enumerate.md) taip pat jums gali padėti pasiekti atskirus nurodytos įvesties eilutės elementus.</span><span class="sxs-lookup"><span data-stu-id="b3c57-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="b3c57-137">Jei pirmiausia įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Mano sąrašas** ir jam konfigūruojate išraišką `SPLIT("abc", 1)`, o tada įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Sunumeruotas sąrašas** ir jam konfigūruojate išraišką `ENUMERATE(MyList)`, išraiška `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` grąžina teksto reikšmę **„b”**.</span><span class="sxs-lookup"><span data-stu-id="b3c57-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3c57-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b3c57-138">Additional resources</span></span>

[<span data-ttu-id="b3c57-139">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="b3c57-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
