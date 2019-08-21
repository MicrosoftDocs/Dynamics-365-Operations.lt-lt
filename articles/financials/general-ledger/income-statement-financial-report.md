---
title: Pajamų išrašo finansinė ataskaita
description: Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita. Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839092"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="294c3-104">Pajamų išrašo finansinė ataskaita</span><span class="sxs-lookup"><span data-stu-id="294c3-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="294c3-105">Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="294c3-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="294c3-106">Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="294c3-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="294c3-107">Numatytoji pajamų išrašo ataskaita</span><span class="sxs-lookup"><span data-stu-id="294c3-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="294c3-108">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="294c3-108">Default report</span></span>             | <span data-ttu-id="294c3-109">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="294c3-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294c3-110">Pajamų išrašas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="294c3-110">Income Statement – Default</span></span> | <span data-ttu-id="294c3-111">Pateikiama dabartinio laikotarpio ir laikotarpio nuo metų pradžios organizacijos pelningumo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="294c3-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="294c3-112">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="294c3-112">Building blocks</span></span>
<span data-ttu-id="294c3-113">Pajamų išrašo finansinėje ataskaitoje naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="294c3-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="294c3-114">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="294c3-114">Default report</span></span>             | <span data-ttu-id="294c3-115">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="294c3-115">Row definition</span></span>                     | <span data-ttu-id="294c3-116">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="294c3-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="294c3-117">Pajamų išrašas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="294c3-117">Income Statement - Default</span></span> | <span data-ttu-id="294c3-118">Pajamų išrašo suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="294c3-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="294c3-119">Periodinė ir nuo šių metų pradžios – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="294c3-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="294c3-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="294c3-120">Row definition</span></span>

<span data-ttu-id="294c3-121">Eilutės aprašas, pajamų išrašo suvestinė – Numatytoji, sudaryta iš skyrių, skirtų kiekvienai įprastinio pajamų išrašo daliai.</span><span class="sxs-lookup"><span data-stu-id="294c3-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="294c3-122">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti šios eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="294c3-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="294c3-123">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="294c3-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="294c3-124">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="294c3-124">Column Definition</span></span>

<span data-ttu-id="294c3-125">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="294c3-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="294c3-126">**Periodiniai ir nuo šių metų pradžios – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="294c3-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="294c3-127">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="294c3-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="294c3-128">**FD** – dabartinio laikotarpio finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="294c3-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="294c3-129">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="294c3-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="294c3-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="294c3-130">Additional resources</span></span>
--------

[<span data-ttu-id="294c3-131">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="294c3-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="294c3-132">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="294c3-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="294c3-133">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="294c3-133">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



