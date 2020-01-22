---
title: VALUEIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama VALUEIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915975"
---
# <span data-ttu-id="8c083-103"><a name="VALUEIN">VALUEIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="8c083-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c083-104">`VALUEIN` funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8c083-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="8c083-105">Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="8c083-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="8c083-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8c083-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c083-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="8c083-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="8c083-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="8c083-108">Arguments</span></span>

<span data-ttu-id="8c083-109">`input`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="8c083-109">`input`: *Field*</span></span>

<span data-ttu-id="8c083-110">Tinkamas *Įrašų sąrašo* tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="8c083-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="8c083-111">Šio elemento vertė bus sugretinta.</span><span class="sxs-lookup"><span data-stu-id="8c083-111">The value of this item will be matched.</span></span>

<span data-ttu-id="8c083-112">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="8c083-112">`list`: *Record list*</span></span>

<span data-ttu-id="8c083-113">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="8c083-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="8c083-114">`list item expression`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="8c083-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="8c083-115">Tinkama sąlyginė išraiška nurodo išraišką, kuri nurodo vieną sugretinimui naudotiną konkretaus sąrašo lauką arba kurioje toks laukas yra.</span><span class="sxs-lookup"><span data-stu-id="8c083-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="8c083-116">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="8c083-116">Return values</span></span>

<span data-ttu-id="8c083-117">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="8c083-117">*Boolean*</span></span>

<span data-ttu-id="8c083-118">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8c083-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8c083-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="8c083-119">Usage notes</span></span>

<span data-ttu-id="8c083-120">Paprastai funkcija `VALUEIN` paverčiama sąlygų **OR** rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="8c083-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="8c083-121">Kai kuriais atvejais, ji gali būti paverčiama į duomenų bazės SQL sakinį naudojant `EXISTS JOIN` operatorių.</span><span class="sxs-lookup"><span data-stu-id="8c083-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="8c083-122">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8c083-122">Example 1</span></span>

<span data-ttu-id="8c083-123">Nustatote šį savo modelio susiejimo duomenų šaltinį **Sąrašas**, priklausantį tipui *Apskaičiuotasis laukas*.</span><span class="sxs-lookup"><span data-stu-id="8c083-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8c083-124">Šiame duomenų šaltinyje yra išraiška `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="8c083-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="8c083-125">Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, List.Value)` išraiška, jis grąžinamas **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="8c083-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="8c083-126">Tokiu atveju funkcija `VALUEIN` paverčiama toliau nurodytu sąlygų rinkiniu: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kai `("B" = "b")` lygu **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="8c083-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="8c083-127">Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, LEFT(List.Value, 0))` išraiška, jis grąžinamas **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="8c083-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="8c083-128">Tokiu atveju `VALUEIN` funkcija paverčiama toliau nurodyta sąlyga: `("B" = "")` nelygu **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="8c083-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="8c083-129">Viršutinė esant tokiai sąlygai įvesto teksto simbolių skaičiaus riba yra 32 768 simboliai.</span><span class="sxs-lookup"><span data-stu-id="8c083-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="8c083-130">Todėl neturėtumėte kurti duomenų šaltinių, kuriuose vykdant galėtų būti viršijama ši riba.</span><span class="sxs-lookup"><span data-stu-id="8c083-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="8c083-131">Tais atvejais, kai viršijama riba, programa sustabdoma ir pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="8c083-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="8c083-132">Pavyzdžiui, ši situacija gali susiklostyti, jei duomenų šaltinis sukonfigūruojamas kaip `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, o sąrašuose **List1** ir **List2** yra didelis įrašų kiekis.</span><span class="sxs-lookup"><span data-stu-id="8c083-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="8c083-133">Kai kuriais atvejais funkcija `VALUEIN`, naudojantis operatoriumi `EXISTS JOIN`, paverčiama duomenų bazės išrašu.</span><span class="sxs-lookup"><span data-stu-id="8c083-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="8c083-134">Taip atsitinka naudojantis funkcija [FILTER](er-functions-list-filter.md) ir esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="8c083-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="8c083-135">Funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio parinktis **ASK FOR QUERY** išjungta.</span><span class="sxs-lookup"><span data-stu-id="8c083-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="8c083-136">Vykdant šį duomenų šaltinį nebus taikoma jokių papildomų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="8c083-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="8c083-137">Nesukonfigūruota jokių įdėtųjų funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio išraiškų.</span><span class="sxs-lookup"><span data-stu-id="8c083-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="8c083-138">Funkcijos `VALUEIN` sąrašo elementas nurodo konkretaus duomenų šaltinio lauką, o ne jo išraišką ar metodą.</span><span class="sxs-lookup"><span data-stu-id="8c083-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="8c083-139">Apsvarstykite galimybę naudoti šią parinktį, o ne pirmiau šiame pavyzdyje aprašytą funkciją [WHERE](er-functions-list-where.md).</span><span class="sxs-lookup"><span data-stu-id="8c083-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="8c083-140">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8c083-140">Example 2</span></span>

<span data-ttu-id="8c083-141">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="8c083-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="8c083-142">Duomenų šaltinis**In**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="8c083-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="8c083-143">Šis duomenų šaltinis nurodo lentelę „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="8c083-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="8c083-144">Duomenų šaltinis**Port**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="8c083-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="8c083-145">Šis duomenų šaltinis nurodo lentelę „IntrastatPort“.</span><span class="sxs-lookup"><span data-stu-id="8c083-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="8c083-146">Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, sukuriamas SQL išrašas filtruotiems „Intrastat“ lentelės įrašams grąžinti.</span><span class="sxs-lookup"><span data-stu-id="8c083-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="8c083-147">Galutinis laukų **dataAreaId** SQL išrašas kuriamas naudojantis operatoriumi `IN`.</span><span class="sxs-lookup"><span data-stu-id="8c083-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="8c083-148">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8c083-148">Example 3</span></span>

<span data-ttu-id="8c083-149">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="8c083-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="8c083-150">Tipo *Apskaičiuotasis laukas* duomenų šaltinis **Le**.</span><span class="sxs-lookup"><span data-stu-id="8c083-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="8c083-151">Šiame duomenų šaltinyje yra išraiška `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="8c083-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="8c083-152">Duomenų šaltinis**In**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="8c083-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="8c083-153">Šis duomenų šaltinis nurodo lentelę „Intrastat“, o parinktis **Kryžminė įmonė** yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="8c083-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="8c083-154">Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, galutiniame SQL yra toliau nurodyta sąlyga.</span><span class="sxs-lookup"><span data-stu-id="8c083-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="8c083-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8c083-155">Additional resources</span></span>

[<span data-ttu-id="8c083-156">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="8c083-156">Logical functions</span></span>](er-functions-category-logical.md)
