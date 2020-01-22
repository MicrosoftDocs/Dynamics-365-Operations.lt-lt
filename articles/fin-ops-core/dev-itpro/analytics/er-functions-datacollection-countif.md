---
title: ER COUNTIF funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) COUNTIF funkcija.
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
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917700"
---
# <span data-ttu-id="e67dd-103"><a name="COUNTIF">ER COUNTIF funkcija</a></span><span class="sxs-lookup"><span data-stu-id="e67dd-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e67dd-104">`COUNTIF` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="e67dd-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="e67dd-105">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e67dd-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67dd-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="e67dd-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="e67dd-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="e67dd-107">Arguments</span></span>

<span data-ttu-id="e67dd-108">`condition range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e67dd-108">`condition range`: *String*</span></span>

<span data-ttu-id="e67dd-109">Reikšmė, kurią pateika reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="e67dd-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="e67dd-110">`condition value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e67dd-110">`condition value`: *String*</span></span>

<span data-ttu-id="e67dd-111">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="e67dd-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="e67dd-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="e67dd-112">Return values</span></span>

<span data-ttu-id="e67dd-113">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="e67dd-113">*Integer*</span></span>

<span data-ttu-id="e67dd-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e67dd-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e67dd-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="e67dd-115">Usage notes</span></span>

<span data-ttu-id="e67dd-116">Ypatybes **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="e67dd-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="e67dd-117">Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e67dd-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="e67dd-118">`condition range` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="e67dd-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="e67dd-119">`condition value` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="e67dd-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="e67dd-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e67dd-120">Example</span></span>

<span data-ttu-id="e67dd-121">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="e67dd-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e67dd-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e67dd-122">Additional resources</span></span>

[<span data-ttu-id="e67dd-123">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="e67dd-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
