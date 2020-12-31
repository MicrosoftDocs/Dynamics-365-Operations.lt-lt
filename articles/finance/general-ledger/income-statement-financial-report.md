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
ms.openlocfilehash: 429283865c66ca5f03608e4a02c3aba5bb5ea7e3
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645582"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="9019c-104">Pajamų išrašo finansinė ataskaita</span><span class="sxs-lookup"><span data-stu-id="9019c-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9019c-105">Šiame straipsnyje aprašyta numatytoji pajamų išrašo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="9019c-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="9019c-106">Be to, jame aprašyti su šia ataskaita susieti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="9019c-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="9019c-107">Numatytoji pajamų išrašo ataskaita</span><span class="sxs-lookup"><span data-stu-id="9019c-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="9019c-108">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="9019c-108">Default report</span></span>             | <span data-ttu-id="9019c-109">Kuo ji naudinga</span><span class="sxs-lookup"><span data-stu-id="9019c-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9019c-110">Pajamų išrašas – numatyt.</span><span class="sxs-lookup"><span data-stu-id="9019c-110">Income Statement – Default</span></span> | <span data-ttu-id="9019c-111">Pateikiama dabartinio laikotarpio ir laikotarpio nuo metų pradžios organizacijos pelningumo apžvalga.</span><span class="sxs-lookup"><span data-stu-id="9019c-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="9019c-112">Kūrimo blokai</span><span class="sxs-lookup"><span data-stu-id="9019c-112">Building blocks</span></span>
<span data-ttu-id="9019c-113">Pajamų išrašo finansinėje ataskaitoje naudojami toliau nurodyti kūrimo blokai.</span><span class="sxs-lookup"><span data-stu-id="9019c-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="9019c-114">Numatytoji ataskaita</span><span class="sxs-lookup"><span data-stu-id="9019c-114">Default report</span></span>             | <span data-ttu-id="9019c-115">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="9019c-115">Row definition</span></span>                     | <span data-ttu-id="9019c-116">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="9019c-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="9019c-117">Pajamų išrašas – Numatytasis</span><span class="sxs-lookup"><span data-stu-id="9019c-117">Income Statement - Default</span></span> | <span data-ttu-id="9019c-118">Pajamų išrašo suvestinė – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="9019c-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="9019c-119">Periodinė ir nuo šių metų pradžios – Numatytoji</span><span class="sxs-lookup"><span data-stu-id="9019c-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="9019c-120">Eilutės apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="9019c-120">Row definition</span></span>

<span data-ttu-id="9019c-121">Eilutės aprašas, pajamų išrašo suvestinė – Numatytoji, sudaryta iš skyrių, skirtų kiekvienai įprastinio pajamų išrašo daliai.</span><span class="sxs-lookup"><span data-stu-id="9019c-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="9019c-122">Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti šios eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="9019c-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="9019c-123">Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="9019c-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="9019c-124">Stulpelio aprašas</span><span class="sxs-lookup"><span data-stu-id="9019c-124">Column Definition</span></span>

<span data-ttu-id="9019c-125">Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.</span><span class="sxs-lookup"><span data-stu-id="9019c-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="9019c-126">**Periodiniai ir nuo šių metų pradžios – Numatytieji stulpelių tipai:**</span><span class="sxs-lookup"><span data-stu-id="9019c-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="9019c-127">**DESC** – Eilutės apibrėžimo aprašymas</span><span class="sxs-lookup"><span data-stu-id="9019c-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="9019c-128">**FD** – dabartinio laikotarpio finansiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="9019c-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="9019c-129">**FD** – finansiniai duomenys nuo šių metų pradžios</span><span class="sxs-lookup"><span data-stu-id="9019c-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="9019c-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9019c-130">Additional resources</span></span>
--------

[<span data-ttu-id="9019c-131">Finansinių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9019c-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="9019c-132">Finansinių ataskaitų peržiūra</span><span class="sxs-lookup"><span data-stu-id="9019c-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="9019c-133">„Dynamics‟ Finansinių ataskaitų tinklaraštis</span><span class="sxs-lookup"><span data-stu-id="9019c-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)



