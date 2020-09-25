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
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743620"
---
# <a name="countif-er-function"></a><span data-ttu-id="87a9b-103">ER COUNTIF funkcija</span><span class="sxs-lookup"><span data-stu-id="87a9b-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87a9b-104">`COUNTIF` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="87a9b-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="87a9b-105">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="87a9b-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a9b-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="87a9b-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="87a9b-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="87a9b-107">Arguments</span></span>

<span data-ttu-id="87a9b-108">`condition range`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="87a9b-108">`condition range`: *String*</span></span>

<span data-ttu-id="87a9b-109">Reikšmė, kurią pateika reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="87a9b-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="87a9b-110">`condition value`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="87a9b-110">`condition value`: *String*</span></span>

<span data-ttu-id="87a9b-111">Reikšmė, kurią pateika reiškinys, sukonfigūruotas ER formato komponento ypatybėje **Surinktų duomenų rakto reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="87a9b-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="87a9b-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="87a9b-112">Return values</span></span>

<span data-ttu-id="87a9b-113">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="87a9b-113">*Integer*</span></span>

<span data-ttu-id="87a9b-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="87a9b-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="87a9b-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="87a9b-115">Usage notes</span></span>

<span data-ttu-id="87a9b-116">Ypatybes **Surinktų duomenų rakto pavadinimas** ir **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="87a9b-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="87a9b-117">Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.</span><span class="sxs-lookup"><span data-stu-id="87a9b-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="87a9b-118">`condition range` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="87a9b-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="87a9b-119">`condition value` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="87a9b-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="87a9b-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="87a9b-120">Example</span></span>

<span data-ttu-id="87a9b-121">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="87a9b-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87a9b-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="87a9b-122">Additional resources</span></span>

[<span data-ttu-id="87a9b-123">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="87a9b-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
