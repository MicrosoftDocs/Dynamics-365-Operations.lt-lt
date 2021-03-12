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
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146d4b9946c1b29105cff637fa9d8803db3d0c0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988783"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="8803a-104">Pajamų išrašo finansinė ataskaita</span><span class="sxs-lookup"><span data-stu-id="8803a-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8803a-105">Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="8803a-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="8803a-106">Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="8803a-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="8803a-107">Numatytoji pajamų išrašo ataskaita</span><span class="sxs-lookup"><span data-stu-id="8803a-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="8803a-108">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="8803a-108">Default report</span></span>             | <span data-ttu-id="8803a-109">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="8803a-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8803a-110">Pajamų išrašas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="8803a-110">Income Statement – Default</span></span> | <span data-ttu-id="8803a-111">Pateikiama dabartinio laikotarpio ir laikotarpio nuo metų pradžios organizacijos pelningumo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="8803a-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="8803a-112">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="8803a-112">Building blocks</span></span>
<span data-ttu-id="8803a-113">Pajamų išrašo finansinėje ataskaitoje naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="8803a-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="8803a-114">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="8803a-114">Default report</span></span>             | <span data-ttu-id="8803a-115">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="8803a-115">Row definition</span></span>                     | <span data-ttu-id="8803a-116">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="8803a-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="8803a-117">Pajamų išrašas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="8803a-117">Income Statement - Default</span></span> | <span data-ttu-id="8803a-118">Pajamų išrašo suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="8803a-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="8803a-119">Periodinė ir nuo šių metų pradžios – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="8803a-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="8803a-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="8803a-120">Row definition</span></span>

<span data-ttu-id="8803a-121">Eilutės aprašas, pajamų išrašo suvestinė – Numatytoji, sudaryta iš skyrių, skirtų kiekvienai įprastinio pajamų išrašo daliai.</span><span class="sxs-lookup"><span data-stu-id="8803a-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="8803a-122">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti šios eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="8803a-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="8803a-123">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="8803a-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="8803a-124">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="8803a-124">Column Definition</span></span>

<span data-ttu-id="8803a-125">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="8803a-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="8803a-126">**Periodiniai ir nuo šių metų pradžios – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="8803a-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="8803a-127">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="8803a-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8803a-128">**FD** – dabartinio laikotarpio finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="8803a-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="8803a-129">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="8803a-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="8803a-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8803a-130">Additional resources</span></span>
--------

[<span data-ttu-id="8803a-131">Finansinių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="8803a-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="8803a-132">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="8803a-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="8803a-133">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="8803a-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



