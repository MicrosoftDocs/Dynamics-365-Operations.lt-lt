---
title: Duomenų rinkimo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie duomenų rinkimo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
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
ms.openlocfilehash: b318945c9cd10b237843d26cfdc46fc08e84e268
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917815"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="c8f4d-103">Duomenų rinkimo kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="c8f4d-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8f4d-104">Naudojant modulio Elektroninės ataskaitos (ER) duomenų rinkimo funkcijas, atliekamos vykdomo ER formato skaičiavimo ir sumavimo operacijos pagal išvesties, kuri jau sugeneruota **teksto** arba **XML** formatu, duomenis.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="c8f4d-105">Šis metodas naudojamas norint pagerinti vykdomo ER formato našumą, įvesti bendrąsias sumas generuojamuose dokumentuose ir kitais tikslais.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="c8f4d-106">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="c8f4d-107">Palaikomų funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="c8f4d-107">List of supported functions</span></span>

| <span data-ttu-id="c8f4d-108">Funkcija</span><span class="sxs-lookup"><span data-stu-id="c8f4d-108">Function</span></span> | <span data-ttu-id="c8f4d-109">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c8f4d-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="c8f4d-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="c8f4d-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="c8f4d-111">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, kurioje yra sąrašas reikšmių, kurias pateikė formato elementų ypatybė **Surinktų duomenų rakto reikšmė** ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokumentas, ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="c8f4d-112">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="c8f4d-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="c8f4d-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="c8f4d-114">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="c8f4d-115">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="c8f4d-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="c8f4d-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="c8f4d-117">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="c8f4d-118">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="c8f4d-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="c8f4d-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="c8f4d-120">Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią dabartinio ER formato elemento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="c8f4d-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="c8f4d-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="c8f4d-122">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="c8f4d-123">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="c8f4d-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="c8f4d-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="c8f4d-125">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="c8f4d-126">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8f4d-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="c8f4d-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c8f4d-127">Additional resources</span></span>

[<span data-ttu-id="c8f4d-128">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c8f4d-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="c8f4d-129">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="c8f4d-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="c8f4d-130">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="c8f4d-130">Electronic reporting formula language</span></span>](er-formula-language.md)
