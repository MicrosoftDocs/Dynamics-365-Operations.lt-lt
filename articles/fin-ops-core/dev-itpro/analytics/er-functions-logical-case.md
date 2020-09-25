---
title: CASE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CASE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 605bd50005ee4e5866a5be9e16df6da3139ad19c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744772"
---
# <a name="case-er-function"></a><span data-ttu-id="26fce-103">CASE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="26fce-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26fce-104">`CASE` funkcija įvertina nurodytos išraiškos reikšmę pagal nurodytas alternatyvias parinktis ir grąžina pirmosios parinkties, kuri yra lygi nurodytos išraiškos vertei, rezultatą.</span><span class="sxs-lookup"><span data-stu-id="26fce-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="26fce-105">Kitu atveju ji grąžina pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas yra nurodytas kaip paskutinis iškviestos funkcijos argumentas, prieš kurį nėra parinkties.</span><span class="sxs-lookup"><span data-stu-id="26fce-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="26fce-106">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="26fce-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="26fce-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="26fce-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="26fce-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="26fce-108">Arguments</span></span>

<span data-ttu-id="26fce-109">`expression`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)</span><span class="sxs-lookup"><span data-stu-id="26fce-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="26fce-110">Tinkama išraiška, grąžinanti primityviojo duomenų tipo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="26fce-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="26fce-111">`option 1`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)</span><span class="sxs-lookup"><span data-stu-id="26fce-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="26fce-112">Tinkama išraiška, kuri grąžina to paties primityviojo duomenų tipo reikšmę kaip iškvietos `expression` funkcijos argumentą.</span><span class="sxs-lookup"><span data-stu-id="26fce-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="26fce-113">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="26fce-113">This argument is required.</span></span>

<span data-ttu-id="26fce-114">`result 1`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="26fce-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="26fce-115">Grąžintas rezultatas, atitinkantis ankstesnę parinktį.</span><span class="sxs-lookup"><span data-stu-id="26fce-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="26fce-116">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="26fce-116">This argument is required.</span></span>

<span data-ttu-id="26fce-117">`option N`: *Primityvusis duomenų tipas* (Bulio logikos, skaitinis arba tekstinis)</span><span class="sxs-lookup"><span data-stu-id="26fce-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="26fce-118">Tinkama išraiška, kuri grąžina to paties primityviojo duomenų tipo reikšmę kaip iškvietos `expression` funkcijos argumentą.</span><span class="sxs-lookup"><span data-stu-id="26fce-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="26fce-119">Šis argumentas yra pasirinktinis.</span><span class="sxs-lookup"><span data-stu-id="26fce-119">This argument is optional.</span></span>

<span data-ttu-id="26fce-120">`result N`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="26fce-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="26fce-121">Grąžintas rezultatas, atitinkantis ankstesnę parinktį.</span><span class="sxs-lookup"><span data-stu-id="26fce-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="26fce-122">Šis argumentas yra pasirinktinis.</span><span class="sxs-lookup"><span data-stu-id="26fce-122">This argument is optional.</span></span>

<span data-ttu-id="26fce-123">`default result`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="26fce-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="26fce-124">Rezultatas, kuris turėtų būti grąžintas, jei nėra atitikmens.</span><span class="sxs-lookup"><span data-stu-id="26fce-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="26fce-125">Šis argumentas yra pasirinktinis.</span><span class="sxs-lookup"><span data-stu-id="26fce-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="26fce-126">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="26fce-126">Return values</span></span>

<span data-ttu-id="26fce-127">*Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="26fce-127">*Any of the supported data types*</span></span>

<span data-ttu-id="26fce-128">Gauta bet kurio palaikomų duomenų tipo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="26fce-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26fce-129">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="26fce-129">Usage notes</span></span>

<span data-ttu-id="26fce-130">Vykdymo metu pateikiama išimtis, jei nėra atitikmens ir pasirinktinis numatytasis rezultatas nėra apibrėžtas.</span><span class="sxs-lookup"><span data-stu-id="26fce-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="26fce-131">Visi rezultatai ir turi būti nurodyti naudojant tą patį duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="26fce-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="26fce-132">Jei sukonfigūruotų rezultatų duomenų tipai nesutampa, kūrimo metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="26fce-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="26fce-133">Jei pirmasis rezultatas ir *N*-tasis rezultatas yra duomenų tipo *Konteineris (įrašas)* arba *Įrašų sąrašas* reikšmės, rezultatai apima tik tuos laukus, kurie yra abiejose reikšmėse.</span><span class="sxs-lookup"><span data-stu-id="26fce-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="26fce-134">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="26fce-134">Example</span></span>

<span data-ttu-id="26fce-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")`grąžina eilutę **„ŽIEMA“**, jei dabartinė programos seanso data yra nuo spalio iki gruodžio mėn.</span><span class="sxs-lookup"><span data-stu-id="26fce-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="26fce-136">Kitu atveju pateikia tuščią eilutę.</span><span class="sxs-lookup"><span data-stu-id="26fce-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26fce-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="26fce-137">Additional resources</span></span>

[<span data-ttu-id="26fce-138">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="26fce-138">Logical functions</span></span>](er-functions-category-logical.md)
