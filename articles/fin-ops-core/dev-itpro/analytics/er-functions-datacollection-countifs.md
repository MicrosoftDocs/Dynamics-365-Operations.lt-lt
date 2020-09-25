---
title: ER COUNTIFS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNTIFS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: a28e2dd263c3f2cabd1c07c4aba8dfb22db01cc4
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745662"
---
# <a name="countifs-er-function"></a><span data-ttu-id="1176c-103">ER COUNTIFS funkcija</span><span class="sxs-lookup"><span data-stu-id="1176c-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1176c-104">`COUNTIFS` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="1176c-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="1176c-105">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1176c-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1176c-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1176c-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="1176c-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1176c-107">Arguments</span></span>

<span data-ttu-id="1176c-108">`condition 1 range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1176c-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="1176c-109">Reikšmė, kurią pateika reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="1176c-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="1176c-110">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="1176c-110">This argument is mandatory.</span></span>

<span data-ttu-id="1176c-111">`condition 1 value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1176c-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="1176c-112">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="1176c-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="1176c-113">Šis argumentas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="1176c-113">This argument is mandatory.</span></span>

<span data-ttu-id="1176c-114">`condition N range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1176c-114">`condition N range`: *String*</span></span>

<span data-ttu-id="1176c-115">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="1176c-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="1176c-116">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="1176c-116">These additional arguments are optional.</span></span>

<span data-ttu-id="1176c-117">`condition N value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1176c-117">`condition N value`: *String*</span></span>

<span data-ttu-id="1176c-118">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="1176c-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="1176c-119">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="1176c-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1176c-120">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="1176c-120">Return values</span></span>

<span data-ttu-id="1176c-121">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="1176c-121">*Integer*</span></span>

<span data-ttu-id="1176c-122">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1176c-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1176c-123">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="1176c-123">Usage notes</span></span>

<span data-ttu-id="1176c-124">Ypatybes **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="1176c-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="1176c-125">Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1176c-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="1176c-126">`condition range` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="1176c-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="1176c-127">`condition value` argumentuose pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="1176c-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="1176c-128">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1176c-128">Example</span></span>

<span data-ttu-id="1176c-129">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="1176c-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1176c-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1176c-130">Additional resources</span></span>

[<span data-ttu-id="1176c-131">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="1176c-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
