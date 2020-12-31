---
title: VALUEINLARGE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama VALUEINLARGE elektroninės ataskaitos (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 26a7148a4caa80a191688145bac625bdf0bf83b2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686911"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="cd7f5-103">VALUEINLARGE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="cd7f5-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd7f5-104">`VALUEINLARGE` funkcija nustato, ar nurodyta *Int64* arba *Sveikojo skaičiaus* tipo įvestis atitinka bet kurią pateiktame sąraše nurodytos prekės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="cd7f5-105">Ši funkcija grąžina *Bulio logikos* reikšmę **TEISINGA**, jei nurodyta įvestis sutampa su nurodyto reiškinio vykdymo rezultatu bent vienam pateikto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="cd7f5-106">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="cd7f5-107">Norėdami suprasti skirtumą su `VALUEIN` funkcija, žr. [Usage note](#usage_note) skyrių, esantį vėliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7f5-108">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="cd7f5-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="cd7f5-109">Argumentai</span><span class="sxs-lookup"><span data-stu-id="cd7f5-109">Arguments</span></span>

<span data-ttu-id="cd7f5-110">`input`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="cd7f5-110">`input`: *Field*</span></span>

<span data-ttu-id="cd7f5-111">Tinkamas *Įrašų sąrašo* tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="cd7f5-112">Šio elemento vertė bus sugretinta.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-112">The value of this item will be matched.</span></span>

<span data-ttu-id="cd7f5-113">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="cd7f5-113">`list`: *Record list*</span></span>

<span data-ttu-id="cd7f5-114">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="cd7f5-115">`list item expression`: *Išraiška*</span><span class="sxs-lookup"><span data-stu-id="cd7f5-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="cd7f5-116">Tinkama sąlyginė išraiška nurodo išraišką, kuri nurodo vieną sugretinimui naudotiną konkretaus sąrašo lauką arba kurioje toks laukas yra.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="cd7f5-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="cd7f5-117">Return values</span></span>

<span data-ttu-id="cd7f5-118">*Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="cd7f5-118">*Boolean*</span></span>

<span data-ttu-id="cd7f5-119">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="cd7f5-120"><a name="usage_note">Naudojimo pastabos</a></span><span class="sxs-lookup"><span data-stu-id="cd7f5-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="cd7f5-121">Kai nurodyta įvestis atitinka *Int64* arba *Sveikojo skaičiaus* tipo duomenų šaltinio prekę ir kalbą, kuri gali būti konvertuojama į tiesioginį SQL sakinį, pateiktas sąrašas konvertuojamas į laikinąją SQL lentelę, o gretinimas yra atliekamas duomenų bazėje vykdant vieną `EXISTS JOIN` užklausą.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="cd7f5-122">Kitu atveju ši funkcija veikia kaip [`VALUEIN`](er-functions-logical-valuein.md) funkcija.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="cd7f5-123">Kai nurodyta įvestis atitinka duomenų šaltinio prekę, kuri sukurta ne kaip *Int64* ir *Sveikojo skaičiaus* tipo prekė, kūrimo laiku įvyksta klaida, informuojanti, kad `VALUEINLARGE` funkcija netaikoma sukonfigūruotai ER išraiškai.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="cd7f5-124">Kai vykdoma funkcijos `VALUEINLARGE` išraiška ir šioje vykdymo apimtyje naudojama daugiau nei viena laikina lentelė, įvyksta vykdymo klaida.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="cd7f5-125">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cd7f5-125">Example</span></span>

<span data-ttu-id="cd7f5-126">Apibrėžkite šiuos modelio susiejimo duomenų šaltinius:</span><span class="sxs-lookup"><span data-stu-id="cd7f5-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="cd7f5-127">Duomenų šaltinis **In**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="cd7f5-128">Šis duomenų šaltinis nurodo **Intrastat** lentelę.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="cd7f5-129">**Visos įmonės** pasirinktis nustatoma kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="cd7f5-130">*Apskaičiuotojo lauko* tipo duomenų šaltinis **InMemory**.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="cd7f5-131">Šiame duomenų šaltinyje yra išraiška `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="cd7f5-132">*Apskaičiuotojo lauko* tipo duomenų šaltinis **InFiltered**.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="cd7f5-133">Šiame duomenų šaltinyje yra išraiška `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="cd7f5-134">Kai duomenų šaltinis **InFiltered** traktuojamas įmonės **DEMF** kontekste, programos duomenų bazėje sukuriama nauja laikina lentelė, į kurią įterpiamas įrašo identifikacijos kodų atminties sąrašas ir sugeneruojamas šis SQL sakinys, kad būtų grąžinti filtruoti **Intrastat** lentelės įrašai.</span><span class="sxs-lookup"><span data-stu-id="cd7f5-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="cd7f5-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cd7f5-135">Additional resources</span></span>

[<span data-ttu-id="cd7f5-136">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="cd7f5-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="cd7f5-137">VALUEIN funkcijos</span><span class="sxs-lookup"><span data-stu-id="cd7f5-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
