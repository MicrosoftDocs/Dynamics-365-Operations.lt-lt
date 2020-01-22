---
title: ER SUMIFS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SUMIFS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917608"
---
# <span data-ttu-id="317dc-103"><a name="SUMIFS">ER SUMIFS funkcija</a></span><span class="sxs-lookup"><span data-stu-id="317dc-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="317dc-104">`SUMIFS` funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="317dc-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="317dc-105">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="317dc-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="317dc-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="317dc-106">Syntax</span></span>

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="317dc-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="317dc-107">Arguments</span></span>

<span data-ttu-id="317dc-108">`key name for summing`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="317dc-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="317dc-109">Reikšmė, kurią pateikia reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento, kuriam sumavimo tikslais reikia naudoti susiejimo reikšmę, ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="317dc-110">Ypatybę **Surinktų duomenų rakto pavadinimas** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Skaitinis** arba **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="317dc-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="317dc-111">`condition 1 range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="317dc-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="317dc-112">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="317dc-113">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="317dc-113">This argument is mandatory.</span></span>

<span data-ttu-id="317dc-114">Ypatybę **Surinktų duomenų rakto pavadinimas** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="317dc-115">`condition 1 value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="317dc-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="317dc-116">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="317dc-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="317dc-117">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="317dc-117">This argument is mandatory.</span></span>

<span data-ttu-id="317dc-118">Ypatybę **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="317dc-119">`condition N range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="317dc-119">`condition N range`: *String*</span></span>

<span data-ttu-id="317dc-120">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="317dc-121">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="317dc-121">These additional arguments are optional.</span></span>

<span data-ttu-id="317dc-122">Ypatybę **Surinktų duomenų rakto pavadinimas** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="317dc-123">`condition N value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="317dc-123">`condition N value`: *String*</span></span>

<span data-ttu-id="317dc-124">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="317dc-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="317dc-125">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="317dc-125">These additional arguments are optional.</span></span>

<span data-ttu-id="317dc-126">Ypatybę **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="317dc-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="317dc-127">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="317dc-127">Return values</span></span>

<span data-ttu-id="317dc-128">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="317dc-128">*Real*</span></span>

<span data-ttu-id="317dc-129">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="317dc-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="317dc-130">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="317dc-130">Usage notes</span></span>

<span data-ttu-id="317dc-131">Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.</span><span class="sxs-lookup"><span data-stu-id="317dc-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="317dc-132">`condition range` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="317dc-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="317dc-133">`condition value` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="317dc-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="317dc-134">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="317dc-134">Example</span></span>

<span data-ttu-id="317dc-135">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="317dc-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="317dc-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="317dc-136">Additional resources</span></span>

[<span data-ttu-id="317dc-137">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="317dc-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
