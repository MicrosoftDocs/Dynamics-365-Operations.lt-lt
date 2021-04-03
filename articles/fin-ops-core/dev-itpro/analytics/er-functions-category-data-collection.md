---
title: Duomenų rinkimo kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie duomenų rinkimo funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba3a1f031a4a98592081b04a4128450aeb8218ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561739"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="4b40e-103">Duomenų rinkimo kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="4b40e-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b40e-104">Naudojant modulio Elektroninės ataskaitos (ER) duomenų rinkimo funkcijas, atliekamos vykdomo ER formato skaičiavimo ir sumavimo operacijos pagal išvesties, kuri jau sugeneruota **teksto** arba **XML** formatu, duomenis.</span><span class="sxs-lookup"><span data-stu-id="4b40e-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="4b40e-105">Šis metodas naudojamas norint pagerinti vykdomo ER formato našumą, įvesti bendrąsias sumas generuojamuose dokumentuose ir kitais tikslais.</span><span class="sxs-lookup"><span data-stu-id="4b40e-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="4b40e-106">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4b40e-107">Palaikomų funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="4b40e-107">List of supported functions</span></span>

| <span data-ttu-id="4b40e-108">Funkcija</span><span class="sxs-lookup"><span data-stu-id="4b40e-108">Function</span></span> | <span data-ttu-id="4b40e-109">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="4b40e-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4b40e-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="4b40e-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="4b40e-111">Ši funkcija pateikia tipo *Įrašų sąrašas* reikšmę, kurioje yra sąrašas reikšmių, kurias pateikė formato elementų ypatybė **Surinktų duomenų rakto reikšmė** ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokumentas, ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="4b40e-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="4b40e-112">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="4b40e-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="4b40e-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="4b40e-114">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="4b40e-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="4b40e-115">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="4b40e-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="4b40e-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="4b40e-117">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, kuri nurodo formato elementų, surinktų, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, skaičių ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="4b40e-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="4b40e-118">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="4b40e-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="4b40e-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="4b40e-120">Ši funkcija pateikia tipo *Eilutė* reikšmę, nurodančią dabartinio ER formato elemento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4b40e-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="4b40e-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="4b40e-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="4b40e-122">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="4b40e-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="4b40e-123">Sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="4b40e-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="4b40e-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="4b40e-125">Ši funkcija pateikia tipo *Realusis skaičius* reikšmę, kuri nurodo reikšmių, kurias pateikė formato elementų susiejimai ir kurios buvo surinktos, kai, naudojant formato elementus, vykdant formatą buvo generuojamas siunčiamas dokuments, sumą ir kuri tenkina nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="4b40e-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="4b40e-126">Kiekvieną sąlygą sudaro raktų intervalas ir rakto reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4b40e-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4b40e-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4b40e-127">Additional resources</span></span>

[<span data-ttu-id="4b40e-128">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="4b40e-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4b40e-129">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="4b40e-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4b40e-130">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="4b40e-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]