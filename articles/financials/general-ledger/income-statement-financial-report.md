---
title: "Pajamų išrašo finansinė ataskaita"
description: "Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita. Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai."
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
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="658ed-104">Pajamų išrašo finansinė ataskaita</span><span class="sxs-lookup"><span data-stu-id="658ed-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="658ed-105">Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="658ed-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="658ed-106">Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="658ed-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="658ed-107">Numatytoji pajamų išrašo ataskaita</span><span class="sxs-lookup"><span data-stu-id="658ed-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="658ed-108">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="658ed-108">Default report</span></span>             | <span data-ttu-id="658ed-109">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="658ed-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="658ed-110">Pajamų išrašas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="658ed-110">Income Statement – Default</span></span> | <span data-ttu-id="658ed-111">Pateikiama dabartinio laikotarpio ir laikotarpio nuo metų pradžios organizacijos pelningumo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="658ed-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="658ed-112">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="658ed-112">Building blocks</span></span>
<span data-ttu-id="658ed-113">Pajamų išrašo finansinėje ataskaitoje naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="658ed-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="658ed-114">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="658ed-114">Default report</span></span>             | <span data-ttu-id="658ed-115">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="658ed-115">Row definition</span></span>                     | <span data-ttu-id="658ed-116">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="658ed-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="658ed-117">Pajamų išrašas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="658ed-117">Income Statement - Default</span></span> | <span data-ttu-id="658ed-118">Pajamų išrašo suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="658ed-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="658ed-119">Periodinė ir nuo šių metų pradžios – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="658ed-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="658ed-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="658ed-120">Row definition</span></span>

<span data-ttu-id="658ed-121">Eilutės aprašas, pajamų išrašo suvestinė – Numatytoji, sudaryta iš skyrių, skirtų kiekvienai įprastinio pajamų išrašo daliai.</span><span class="sxs-lookup"><span data-stu-id="658ed-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="658ed-122">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti šios eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="658ed-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="658ed-123">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="658ed-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="658ed-124">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="658ed-124">Column Definition</span></span>

<span data-ttu-id="658ed-125">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="658ed-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="658ed-126">**Periodiniai ir nuo šių metų pradžios – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="658ed-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="658ed-127">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="658ed-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="658ed-128">**FD** – dabartinio laikotarpio finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="658ed-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="658ed-129">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="658ed-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="658ed-130">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="658ed-130">See also</span></span>
--------

[<span data-ttu-id="658ed-131">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="658ed-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="658ed-132">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="658ed-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="658ed-133">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="658ed-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



