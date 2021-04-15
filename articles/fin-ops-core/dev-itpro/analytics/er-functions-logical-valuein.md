---
title: VALUEIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama VALUEIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 08/18/2020
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
ms.openlocfilehash: 909aef5e52817a67e400f3132cb5d6ecc8a18906
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751755"
---
# <a name="valuein-er-function"></a><span data-ttu-id="2af31-103">VALUEIN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2af31-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2af31-104">`VALUEIN` funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2af31-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="2af31-105">Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="2af31-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="2af31-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2af31-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af31-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2af31-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="2af31-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2af31-108">Arguments</span></span>

<span data-ttu-id="2af31-109">`input`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="2af31-109">`input`: *Field*</span></span>

<span data-ttu-id="2af31-110">Tinkamas *Įrašų sąrašo* tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="2af31-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="2af31-111">Šio elemento vertė bus sugretinta.</span><span class="sxs-lookup"><span data-stu-id="2af31-111">The value of this item will be matched.</span></span>

<span data-ttu-id="2af31-112">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="2af31-112">`list`: *Record list*</span></span>

<span data-ttu-id="2af31-113">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="2af31-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="2af31-114">`list item expression`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="2af31-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="2af31-115">Tinkama sąlyginė išraiška nurodo išraišką, kuri nurodo vieną sugretinimui naudotiną konkretaus sąrašo lauką arba kurioje toks laukas yra.</span><span class="sxs-lookup"><span data-stu-id="2af31-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="2af31-116">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="2af31-116">Return values</span></span>

<span data-ttu-id="2af31-117">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="2af31-117">*Boolean*</span></span>

<span data-ttu-id="2af31-118">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2af31-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2af31-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="2af31-119">Usage notes</span></span>

<span data-ttu-id="2af31-120">Paprastai funkcija `VALUEIN` paverčiama sąlygų **OR** rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="2af31-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="2af31-121">Jei **ARBA** sąlygų sąrašas yra didelis, o maksimalus bendras SQL sakinio ilgis gali būti viršytas, apsvarstykite galimybę naudoti [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) funkciją.</span><span class="sxs-lookup"><span data-stu-id="2af31-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="2af31-122">Kai kuriais atvejais, ji gali būti paverčiama į duomenų bazės SQL sakinį naudojant `EXISTS JOIN` operatorių.</span><span class="sxs-lookup"><span data-stu-id="2af31-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="2af31-123">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2af31-123">Example 1</span></span>

<span data-ttu-id="2af31-124">Nustatote šį savo modelio susiejimo duomenų šaltinį **Sąrašas**, priklausantį tipui *Apskaičiuotasis laukas*.</span><span class="sxs-lookup"><span data-stu-id="2af31-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="2af31-125">Šiame duomenų šaltinyje yra išraiška `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="2af31-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="2af31-126">Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, List.Value)` išraiška, jis grąžinamas **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="2af31-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="2af31-127">Tokiu atveju funkcija `VALUEIN` paverčiama toliau nurodytu sąlygų rinkiniu: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, kai `("B" = "b")` lygu **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="2af31-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="2af31-128">Kai duomenų šaltinis iškviečiamas, jei jis sukonfigūruotas kaip `VALUEIN ("B", List, LEFT(List.Value, 0))` išraiška, jis grąžinamas **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="2af31-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="2af31-129">Tokiu atveju `VALUEIN` funkcija paverčiama toliau nurodyta sąlyga: `("B" = "")` nelygu **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="2af31-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="2af31-130">Viršutinė esant tokiai sąlygai įvesto teksto simbolių skaičiaus riba yra 32 768 simboliai.</span><span class="sxs-lookup"><span data-stu-id="2af31-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="2af31-131">Todėl neturėtumėte kurti duomenų šaltinių, kuriuose vykdant galėtų būti viršijama ši riba.</span><span class="sxs-lookup"><span data-stu-id="2af31-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="2af31-132">Tais atvejais, kai viršijama riba, programa sustabdoma ir pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="2af31-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="2af31-133">Pavyzdžiui, ši situacija gali susiklostyti, jei duomenų šaltinis sukonfigūruojamas kaip `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, o sąrašuose **List1** ir **List2** yra didelis įrašų kiekis.</span><span class="sxs-lookup"><span data-stu-id="2af31-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="2af31-134">Kai kuriais atvejais funkcija `VALUEIN`, naudojantis operatoriumi `EXISTS JOIN`, paverčiama duomenų bazės išrašu.</span><span class="sxs-lookup"><span data-stu-id="2af31-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="2af31-135">Tai įvyksta naudojantis funkcija  [`FILTER`](er-functions-list-filter.md) ir kai patenkinamos šios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="2af31-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="2af31-136">Funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio parinktis **ASK FOR QUERY** išjungta.</span><span class="sxs-lookup"><span data-stu-id="2af31-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="2af31-137">Vykdant šį duomenų šaltinį nebus taikoma jokių papildomų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="2af31-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="2af31-138">Nesukonfigūruota jokių įdėtųjų funkcijos `VALUEIN`, kuria naudojantis pateikiamas įrašų sąrašas, duomenų šaltinio išraiškų.</span><span class="sxs-lookup"><span data-stu-id="2af31-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="2af31-139">Funkcijos `VALUEIN` sąrašo elementas nurodo konkretaus duomenų šaltinio lauką, o ne jo išraišką ar metodą.</span><span class="sxs-lookup"><span data-stu-id="2af31-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="2af31-140">Apsvarstykite galimybę naudoti šią parinktį vietoj [`WHERE`](er-functions-list-where.md) funkcijos, aprašytos anksčiau šiame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="2af31-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="2af31-141">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2af31-141">Example 2</span></span>

<span data-ttu-id="2af31-142">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="2af31-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="2af31-143">Duomenų šaltinis **In**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="2af31-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="2af31-144">Šis duomenų šaltinis nurodo „Intrastat“ lentelę.</span><span class="sxs-lookup"><span data-stu-id="2af31-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="2af31-145">Duomenų šaltinis **Port**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="2af31-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="2af31-146">Šis duomenų šaltinis nurodo lentelę „IntrastatPort“.</span><span class="sxs-lookup"><span data-stu-id="2af31-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="2af31-147">Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, sukuriamas SQL išrašas filtruotiems „Intrastat“ lentelės įrašams grąžinti.</span><span class="sxs-lookup"><span data-stu-id="2af31-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="2af31-148">Galutinis laukų **dataAreaId** SQL išrašas kuriamas naudojantis operatoriumi `IN`.</span><span class="sxs-lookup"><span data-stu-id="2af31-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="2af31-149">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2af31-149">Example 3</span></span>

<span data-ttu-id="2af31-150">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="2af31-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="2af31-151">Tipo *Apskaičiuotasis laukas* duomenų šaltinis **Le**.</span><span class="sxs-lookup"><span data-stu-id="2af31-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="2af31-152">Šiame duomenų šaltinyje yra išraiška `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="2af31-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="2af31-153">Duomenų šaltinis **In**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="2af31-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="2af31-154">Šis duomenų šaltinis nurodo lentelę „Intrastat“, o parinktis **Kryžminė įmonė** yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="2af31-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="2af31-155">Kai iškviečiamas duomenų šaltinis, kuris sukonfigūruotas kaip išraiška `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, galutiniame SQL yra toliau nurodyta sąlyga.</span><span class="sxs-lookup"><span data-stu-id="2af31-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="2af31-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2af31-156">Additional resources</span></span>

[<span data-ttu-id="2af31-157">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="2af31-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="2af31-158">VALUEINLARGE funkcijos</span><span class="sxs-lookup"><span data-stu-id="2af31-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]