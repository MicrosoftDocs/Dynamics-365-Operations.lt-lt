---
title: Balanso finansinės ataskaitos
description: Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178998"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="eea24-104">Balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eea24-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eea24-105">Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="eea24-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="eea24-106">Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="eea24-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="eea24-107">Numatytosios balanso finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eea24-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="eea24-108">Yra dvi numatytosios balanso ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="eea24-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="eea24-109">Vienoje ataskaitoje skyriai suspausti.</span><span class="sxs-lookup"><span data-stu-id="eea24-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="eea24-110">Kitoje ataskaitoje skyriai yra vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="eea24-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="eea24-111">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="eea24-111">Default report</span></span>                       | <span data-ttu-id="eea24-112">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="eea24-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea24-113">Balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="eea24-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="eea24-114">Pateikiamas organizacijos metų finansinės padėties rodinys.</span><span class="sxs-lookup"><span data-stu-id="eea24-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="eea24-115">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="eea24-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="eea24-116">Pateikiamas organizacijos metų finansinės padėties rodinys.</span><span class="sxs-lookup"><span data-stu-id="eea24-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="eea24-117">Turtas, įsipareigojimai ir akcininko kapitalas yra vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="eea24-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="eea24-118">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="eea24-118">Building blocks</span></span>
<span data-ttu-id="eea24-119">Balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="eea24-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="eea24-120">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="eea24-120">Default report</span></span>                       | <span data-ttu-id="eea24-121">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="eea24-121">Row definition</span></span>                       | <span data-ttu-id="eea24-122">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="eea24-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="eea24-123">Balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="eea24-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="eea24-124">Balansas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="eea24-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="eea24-125">Nuo šių metų pradžios ir nuokrypis – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="eea24-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="eea24-126">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="eea24-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="eea24-127">Sugretintas balansas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="eea24-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="eea24-128">Stulpelis Nuo šių metų pradžios – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="eea24-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="eea24-129">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="eea24-129">Row definition</span></span>

<span data-ttu-id="eea24-130">Abiejų balanso ataskaitų eilučių apibrėžimuose pateikiami skyriai, skirti kiekvienai įprastinio balanso daliai.</span><span class="sxs-lookup"><span data-stu-id="eea24-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="eea24-131">Ataskaitoje, kurioje duomenys nurodomi vienas šalia kito, pateikiamas stulpelio lūžis, kad įsipareigojimai ir savininko kapitalas būtų rodomi šalia turto.</span><span class="sxs-lookup"><span data-stu-id="eea24-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="eea24-132">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti abiejų eilučių aprašus.</span><span class="sxs-lookup"><span data-stu-id="eea24-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="eea24-133">Todėl bet kas gali generuoti ataskaitas, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="eea24-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="eea24-134">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="eea24-134">Column definition</span></span>

<span data-ttu-id="eea24-135">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="eea24-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="eea24-136">**Nuo šių metų pradžios ir nuokrypis – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="eea24-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="eea24-137">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="eea24-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="eea24-138">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="eea24-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="eea24-139">**FD** – finansiniai duomenys nuo praėjusių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="eea24-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="eea24-140">**CALC** – nuokrypis, gautas nuo šių metų atėmus praėjusius metus</span><span class="sxs-lookup"><span data-stu-id="eea24-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="eea24-141">**Stulpelis Nuo šių metų pradžios – Numatytasis:**</span><span class="sxs-lookup"><span data-stu-id="eea24-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="eea24-142">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="eea24-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="eea24-143">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="eea24-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="eea24-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eea24-144">Additional resources</span></span>
--------

[<span data-ttu-id="eea24-145">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="eea24-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="eea24-146">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="eea24-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="eea24-147">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="eea24-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



