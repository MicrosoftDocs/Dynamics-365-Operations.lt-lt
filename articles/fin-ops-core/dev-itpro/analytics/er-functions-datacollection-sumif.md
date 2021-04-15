---
title: ER SUMIF funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SUMIF funkcija.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747112"
---
# <a name="sumif-er-function"></a><span data-ttu-id="6a9b3-103">ER SUMIF funkcija</span><span class="sxs-lookup"><span data-stu-id="6a9b3-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a9b3-104">`SUMIF` funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="6a9b3-105">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9b3-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6a9b3-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="6a9b3-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6a9b3-107">Arguments</span></span>

<span data-ttu-id="6a9b3-108">`key name for summing`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6a9b3-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="6a9b3-109">Reikšmė, kurią pateikia reiškinys, sukonfigūruotas modulio Elektroninės ataskaitos (ER) formato komponento, kuriam sumavimo tikslais reikia naudoti susiejimo reikšmę, ypatybėje **Surinktų duomenų rakto pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="6a9b3-110">Ypatybę **Surinktų duomenų rakto reikšmė** galima sukonfigūruoti ER formato, esančio komponente **Common\\File**, kuriame įjungta parinktis **Rinkti išeigos informaciją**, komponentui **Seka** arba **XML elementas**.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="6a9b3-111">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="6a9b3-111">Return values</span></span>

<span data-ttu-id="6a9b3-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="6a9b3-112">*Real*</span></span>

<span data-ttu-id="6a9b3-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6a9b3-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="6a9b3-114">Usage notes</span></span>

<span data-ttu-id="6a9b3-115">Kai dabartinio komponento **Common\\File parinktis** **Rinkti išeigos informaciją** yra išjungta, ši funkcija pateikia **0** (nulio) reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="6a9b3-116">`condition range` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="6a9b3-117">`condition value` argumente pakaitos simbolį **„\*“** galima naudoti norint vaizduoti kelis simbolius.</span><span class="sxs-lookup"><span data-stu-id="6a9b3-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="6a9b3-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6a9b3-118">Example</span></span>

<span data-ttu-id="6a9b3-119">Norėdami apie tai, kaip naudoti šią funkciją, gauti daugiau informacijos, žr. užduočių vedlį [ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant](tasks/er-format-counting-summing-1.md) (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis).</span><span class="sxs-lookup"><span data-stu-id="6a9b3-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="6a9b3-120">Daugiau informacijos ir funkcijos naudojimo pavyzdžių žr. [Sekos elementų ER formatais vykdymo atidėjimas](er-defer-sequence-element.md#Example) ir [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="6a9b3-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a9b3-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6a9b3-121">Additional resources</span></span>

[<span data-ttu-id="6a9b3-122">Duomenų rinkinio funkcijos</span><span class="sxs-lookup"><span data-stu-id="6a9b3-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]