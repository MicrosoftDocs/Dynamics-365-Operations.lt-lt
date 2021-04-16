---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9741b5f30f5e62b9e80000953113377fe016253
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749374"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="27a0c-103">„Power BI“ turinys Pirkimo išlaidų analizė</span><span class="sxs-lookup"><span data-stu-id="27a0c-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27a0c-104">Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**.</span><span class="sxs-lookup"><span data-stu-id="27a0c-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="27a0c-105">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="27a0c-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="27a0c-106">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="27a0c-106">Overview</span></span>

<span data-ttu-id="27a0c-107">„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti sekti pirkimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="27a0c-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="27a0c-108">Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.</span><span class="sxs-lookup"><span data-stu-id="27a0c-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="27a0c-109">Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)</span><span class="sxs-lookup"><span data-stu-id="27a0c-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="27a0c-110">Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)</span><span class="sxs-lookup"><span data-stu-id="27a0c-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="27a0c-111">Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą.</span><span class="sxs-lookup"><span data-stu-id="27a0c-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="27a0c-112">Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="27a0c-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="27a0c-113">Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas.</span><span class="sxs-lookup"><span data-stu-id="27a0c-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="27a0c-114">Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="27a0c-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="27a0c-115">Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="27a0c-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="27a0c-116">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="27a0c-116">Accessing the Power BI content</span></span>
<span data-ttu-id="27a0c-117">„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).</span><span class="sxs-lookup"><span data-stu-id="27a0c-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="27a0c-118">Į „Power BI“ turinį įtrauktos metrikos</span><span class="sxs-lookup"><span data-stu-id="27a0c-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="27a0c-119">„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="27a0c-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="27a0c-120">Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės</span><span class="sxs-lookup"><span data-stu-id="27a0c-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="27a0c-121">Toliau pateikiamuose skyriuose apžvelgiamos vizualizacijos.</span><span class="sxs-lookup"><span data-stu-id="27a0c-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="27a0c-122">Pirkimo pagal tiekėjo ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-122">Purchase by vendor report page</span></span>
<span data-ttu-id="27a0c-123">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-123">**Charts**</span></span>
- <span data-ttu-id="27a0c-124">10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="27a0c-125">Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="27a0c-126">Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="27a0c-127">Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="27a0c-128">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="27a0c-128">**Tiles**</span></span>
- <span data-ttu-id="27a0c-129">Iš viso pirkimų</span><span class="sxs-lookup"><span data-stu-id="27a0c-129">Total purchase</span></span>
- <span data-ttu-id="27a0c-130">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-130">YOY purchase growth</span></span>
- <span data-ttu-id="27a0c-131">Bendras # tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="27a0c-131">Total # vendors</span></span>
- <span data-ttu-id="27a0c-132">Bendras # aktyvių tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="27a0c-132">Total # of active vendors</span></span>

<span data-ttu-id="27a0c-133">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="27a0c-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="27a0c-134">Pirkimo pagal produkto ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-134">Purchase by product report page</span></span>

<span data-ttu-id="27a0c-135">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-135">**Charts**</span></span>
- <span data-ttu-id="27a0c-136">Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="27a0c-137">Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="27a0c-138">10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="27a0c-139">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="27a0c-139">**Tiles**</span></span>
- <span data-ttu-id="27a0c-140">Iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="27a0c-140">Total # of products</span></span></li>
- <span data-ttu-id="27a0c-141">Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="27a0c-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="27a0c-142">Produktų, sudarančių 80 % pirkimo, skaičius</span><span class="sxs-lookup"><span data-stu-id="27a0c-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="27a0c-143">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="27a0c-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="27a0c-144">Pirkimo pagal laikotarpio ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-144">Purchase by period report page</span></span>
<span data-ttu-id="27a0c-145">Šiame puslapyje pateikiami pirkimai šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="27a0c-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="27a0c-146">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-146">**Charts**</span></span> 
- <span data-ttu-id="27a0c-147">Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="27a0c-148">Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="27a0c-149">Bendras pirkimo YOY augimas (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="27a0c-150">Įsigijimo išrašas (matrica)</span><span class="sxs-lookup"><span data-stu-id="27a0c-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="27a0c-151">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="27a0c-151">**Tiles**</span></span>
- <span data-ttu-id="27a0c-152">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-152">YOY purchase growth</span></span>
- <span data-ttu-id="27a0c-153">YOY pirkimo augimas %</span><span class="sxs-lookup"><span data-stu-id="27a0c-153">YOY purchase growth %</span></span>

<span data-ttu-id="27a0c-154">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="27a0c-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="27a0c-155">Pirkimo pagal vietos ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="27a0c-156">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-156">**Charts**</span></span>
- <span data-ttu-id="27a0c-157">Pirkimas pagal miestą</span><span class="sxs-lookup"><span data-stu-id="27a0c-157">Purchase by city</span></span>
- <span data-ttu-id="27a0c-158">Pirkimo YOY augimas %</span><span class="sxs-lookup"><span data-stu-id="27a0c-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="27a0c-159">Pirkimas pagal šalį</span><span class="sxs-lookup"><span data-stu-id="27a0c-159">Purchase by country</span></span>

<span data-ttu-id="27a0c-160">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="27a0c-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="27a0c-161">Pirkimo išlaidų analizės pagal laiką ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="27a0c-162">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-162">**Charts**</span></span> 
- <span data-ttu-id="27a0c-163">Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="27a0c-164">Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="27a0c-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="27a0c-165">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="27a0c-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="27a0c-166">Pirkimo išlaidų analizės pagal tiekėją ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="27a0c-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="27a0c-167">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="27a0c-167">**Charts**</span></span> 
- <span data-ttu-id="27a0c-168">10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</span><span class="sxs-lookup"><span data-stu-id="27a0c-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="27a0c-169">10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</span><span class="sxs-lookup"><span data-stu-id="27a0c-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="27a0c-170">10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</span><span class="sxs-lookup"><span data-stu-id="27a0c-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="27a0c-171">**Pavyzdys** 
</span><span class="sxs-lookup"><span data-stu-id="27a0c-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="27a0c-172">Duomenų modelis ir objektai</span><span class="sxs-lookup"><span data-stu-id="27a0c-172">Data model and entities</span></span>
<span data-ttu-id="27a0c-173">Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai.</span><span class="sxs-lookup"><span data-stu-id="27a0c-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="27a0c-174">Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="27a0c-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="27a0c-175">Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="27a0c-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="27a0c-176">Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="27a0c-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="27a0c-177">Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="27a0c-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="27a0c-178">Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus.</span><span class="sxs-lookup"><span data-stu-id="27a0c-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="27a0c-179">Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [Power BI integravimas su objektų saugykla](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="27a0c-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="27a0c-180">Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.</span><span class="sxs-lookup"><span data-stu-id="27a0c-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="27a0c-181">Objektas</span><span class="sxs-lookup"><span data-stu-id="27a0c-181">Entity</span></span>        | <span data-ttu-id="27a0c-182">Pagrindiniai agreguoti matavimo vienetai</span><span class="sxs-lookup"><span data-stu-id="27a0c-182">Key aggregate measurements</span></span> | <span data-ttu-id="27a0c-183">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="27a0c-183">Data source</span></span>                                 | <span data-ttu-id="27a0c-184">Laukas</span><span class="sxs-lookup"><span data-stu-id="27a0c-184">Field</span></span>              | <span data-ttu-id="27a0c-185">aprašymas</span><span class="sxs-lookup"><span data-stu-id="27a0c-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="27a0c-186">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="27a0c-186">Invoice lines</span></span> | <span data-ttu-id="27a0c-187">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-187">Purchase</span></span>                   | <span data-ttu-id="27a0c-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="27a0c-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="27a0c-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="27a0c-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="27a0c-190">Suma, išreikšta apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="27a0c-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="27a0c-191">Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="27a0c-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="27a0c-192">Mato vnt.</span><span class="sxs-lookup"><span data-stu-id="27a0c-192">Measure</span></span>               | <span data-ttu-id="27a0c-193">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a0c-194">Pirkimas esamais metais</span><span class="sxs-lookup"><span data-stu-id="27a0c-194">Purchase current year</span></span> | <span data-ttu-id="27a0c-195">Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])</span><span class="sxs-lookup"><span data-stu-id="27a0c-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="27a0c-196">Pirkimas pastaraisiais metais</span><span class="sxs-lookup"><span data-stu-id="27a0c-196">Purchase last year</span></span>    | <span data-ttu-id="27a0c-197">Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="27a0c-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="27a0c-198">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-198">YOY purchase growth</span></span>   | <span data-ttu-id="27a0c-199">YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]</span><span class="sxs-lookup"><span data-stu-id="27a0c-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="27a0c-200">Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.</span><span class="sxs-lookup"><span data-stu-id="27a0c-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="27a0c-201">Objektas</span><span class="sxs-lookup"><span data-stu-id="27a0c-201">Entity</span></span>                 | <span data-ttu-id="27a0c-202">Atributų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="27a0c-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="27a0c-203">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="27a0c-203">Vendors</span></span>                | <span data-ttu-id="27a0c-204">Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="27a0c-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="27a0c-205">Produktai</span><span class="sxs-lookup"><span data-stu-id="27a0c-205">Products</span></span>               | <span data-ttu-id="27a0c-206">Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="27a0c-207">Įsigijimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="27a0c-207">Procurement categories</span></span> | <span data-ttu-id="27a0c-208">Įsigijimo kategorija, įsigijimo kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="27a0c-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="27a0c-209">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="27a0c-209">Legal entities</span></span>         | <span data-ttu-id="27a0c-210">Juridinio subjekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="27a0c-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="27a0c-211">Datos</span><span class="sxs-lookup"><span data-stu-id="27a0c-211">Dates</span></span>                  | <span data-ttu-id="27a0c-212">Datos, metų poslinkis</span><span class="sxs-lookup"><span data-stu-id="27a0c-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="27a0c-213">Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys.</span><span class="sxs-lookup"><span data-stu-id="27a0c-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="27a0c-214">Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="27a0c-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="27a0c-215">Taip pat galite pakeisti įmonės filtrą.</span><span class="sxs-lookup"><span data-stu-id="27a0c-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]