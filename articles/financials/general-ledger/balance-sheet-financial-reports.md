---
title: "Balanso finansinės ataskaitos"
description: "Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="aac4f-104">Balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="aac4f-104">Balance sheet financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aac4f-105">Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="aac4f-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="aac4f-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="aac4f-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="aac4f-107">Numatytosios balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="aac4f-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="aac4f-108">Yra dvi numatytosios balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="aac4f-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="aac4f-109">Vienoje ataskaitoje skyriai suspausti.</span><span class="sxs-lookup"><span data-stu-id="aac4f-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="aac4f-110">Kitoje ataskaitoje skyriai yra vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="aac4f-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="aac4f-111">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="aac4f-111">Default report</span></span>                       | <span data-ttu-id="aac4f-112">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="aac4f-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac4f-113">Balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="aac4f-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="aac4f-114">Pateikiamas organizacijos metų finansinės padėties rodinys.</span><span class="sxs-lookup"><span data-stu-id="aac4f-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="aac4f-115">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="aac4f-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="aac4f-116">Pateikiamas organizacijos metų finansinės padėties rodinys.</span><span class="sxs-lookup"><span data-stu-id="aac4f-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="aac4f-117">Turtas, įsipareigojimai ir akcininko kapitalas yra vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="aac4f-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="aac4f-118">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="aac4f-118">Building blocks</span></span>
<span data-ttu-id="aac4f-119">Balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="aac4f-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="aac4f-120">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="aac4f-120">Default report</span></span>                       | <span data-ttu-id="aac4f-121">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="aac4f-121">Row definition</span></span>                       | <span data-ttu-id="aac4f-122">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="aac4f-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="aac4f-123">Balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="aac4f-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="aac4f-124">Balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="aac4f-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="aac4f-125">Nuo šių metų pradžios ir nuokrypis – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="aac4f-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="aac4f-126">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="aac4f-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="aac4f-127">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="aac4f-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="aac4f-128">Stulpelis Nuo šių metų pradžios – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="aac4f-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="aac4f-129">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="aac4f-129">Row definition</span></span>

<span data-ttu-id="aac4f-130">Abiejų balanso ataskaitų eilučių apibrėžimuose pateikiami skyriai, skirti kiekvienai įprastinio balanso daliai.</span><span class="sxs-lookup"><span data-stu-id="aac4f-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="aac4f-131">Ataskaitoje, kurioje duomenys nurodomi vienas šalia kito, pateikiamas stulpelio lūžis, kad įsipareigojimai ir savininko kapitalas būtų rodomi šalia turto.</span><span class="sxs-lookup"><span data-stu-id="aac4f-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="aac4f-132">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti abiejų eilučių aprašus.</span><span class="sxs-lookup"><span data-stu-id="aac4f-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="aac4f-133">Todėl bet kas gali generuoti ataskaitas, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="aac4f-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="aac4f-134">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="aac4f-134">Column definition</span></span>

<span data-ttu-id="aac4f-135">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="aac4f-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="aac4f-136">**Nuo šių metų pradžios ir nuokrypis – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="aac4f-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="aac4f-137">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="aac4f-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="aac4f-138">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="aac4f-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="aac4f-139">**FD** – finansiniai duomenys nuo praėjusių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="aac4f-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="aac4f-140">**CALC** – nuokrypis, gautas nuo šių metų atėmus praėjusius metus</span><span class="sxs-lookup"><span data-stu-id="aac4f-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="aac4f-141">**Stulpelis Nuo šių metų pradžios – Numatytasis:**</span><span class="sxs-lookup"><span data-stu-id="aac4f-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="aac4f-142">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="aac4f-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="aac4f-143">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="aac4f-143">**FD** – Year-to-date financial data for the current year</span></span>

 

<a name="see-also"></a><span data-ttu-id="aac4f-144">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="aac4f-144">See also</span></span>
--------

[<span data-ttu-id="aac4f-145">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="aac4f-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="aac4f-146">Peržiūrėti finansines ataskaitas</span><span class="sxs-lookup"><span data-stu-id="aac4f-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="aac4f-147">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="aac4f-147">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



