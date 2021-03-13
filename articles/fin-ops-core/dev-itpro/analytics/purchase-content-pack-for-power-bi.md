---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093447"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="d0842-103">„Power BI“ turinys Pirkimo išlaidų analizė</span><span class="sxs-lookup"><span data-stu-id="d0842-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0842-104">Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**.</span><span class="sxs-lookup"><span data-stu-id="d0842-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="d0842-105">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="d0842-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="d0842-106">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="d0842-106">Overview</span></span>

<span data-ttu-id="d0842-107">„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti sekti pirkimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="d0842-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="d0842-108">Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.</span><span class="sxs-lookup"><span data-stu-id="d0842-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="d0842-109">Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)</span><span class="sxs-lookup"><span data-stu-id="d0842-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="d0842-110">Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)</span><span class="sxs-lookup"><span data-stu-id="d0842-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="d0842-111">Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą.</span><span class="sxs-lookup"><span data-stu-id="d0842-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="d0842-112">Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="d0842-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="d0842-113">Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas.</span><span class="sxs-lookup"><span data-stu-id="d0842-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="d0842-114">Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="d0842-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="d0842-115">Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="d0842-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="d0842-116">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="d0842-116">Accessing the Power BI content</span></span>
<span data-ttu-id="d0842-117">„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).</span><span class="sxs-lookup"><span data-stu-id="d0842-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="d0842-118">Į „Power BI“ turinį įtrauktos metrikos</span><span class="sxs-lookup"><span data-stu-id="d0842-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="d0842-119">„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="d0842-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="d0842-120">Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės</span><span class="sxs-lookup"><span data-stu-id="d0842-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="d0842-121">Toliau pateikiamuose skyriuose apžvelgiamos vizualizacijos.</span><span class="sxs-lookup"><span data-stu-id="d0842-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="d0842-122">Pirkimo pagal tiekėjo ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-122">Purchase by vendor report page</span></span>
<span data-ttu-id="d0842-123">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-123">**Charts**</span></span>
- <span data-ttu-id="d0842-124">10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="d0842-125">Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="d0842-126">Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="d0842-127">Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="d0842-128">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="d0842-128">**Tiles**</span></span>
- <span data-ttu-id="d0842-129">Iš viso pirkimų</span><span class="sxs-lookup"><span data-stu-id="d0842-129">Total purchase</span></span>
- <span data-ttu-id="d0842-130">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="d0842-130">YOY purchase growth</span></span>
- <span data-ttu-id="d0842-131">Bendras # tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="d0842-131">Total # vendors</span></span>
- <span data-ttu-id="d0842-132">Bendras # aktyvių tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="d0842-132">Total # of active vendors</span></span>

<span data-ttu-id="d0842-133">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="d0842-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="d0842-134">Pirkimo pagal produkto ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-134">Purchase by product report page</span></span>

<span data-ttu-id="d0842-135">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-135">**Charts**</span></span>
- <span data-ttu-id="d0842-136">Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="d0842-137">Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="d0842-138">10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="d0842-139">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="d0842-139">**Tiles**</span></span>
- <span data-ttu-id="d0842-140">Iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="d0842-140">Total # of products</span></span></li>
- <span data-ttu-id="d0842-141">Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="d0842-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="d0842-142">Produktų, sudarančių 80 % pirkimo, skaičius</span><span class="sxs-lookup"><span data-stu-id="d0842-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="d0842-143">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="d0842-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="d0842-144">Pirkimo pagal laikotarpio ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-144">Purchase by period report page</span></span>
<span data-ttu-id="d0842-145">Šiame puslapyje pateikiami pirkimai šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="d0842-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="d0842-146">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-146">**Charts**</span></span> 
- <span data-ttu-id="d0842-147">Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="d0842-148">Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="d0842-149">Bendras pirkimo YOY augimas (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="d0842-150">Įsigijimo išrašas (matrica)</span><span class="sxs-lookup"><span data-stu-id="d0842-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="d0842-151">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="d0842-151">**Tiles**</span></span>
- <span data-ttu-id="d0842-152">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="d0842-152">YOY purchase growth</span></span>
- <span data-ttu-id="d0842-153">YOY pirkimo augimas %</span><span class="sxs-lookup"><span data-stu-id="d0842-153">YOY purchase growth %</span></span>

<span data-ttu-id="d0842-154">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="d0842-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="d0842-155">Pirkimo pagal vietos ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="d0842-156">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-156">**Charts**</span></span>
- <span data-ttu-id="d0842-157">Pirkimas pagal miestą</span><span class="sxs-lookup"><span data-stu-id="d0842-157">Purchase by city</span></span>
- <span data-ttu-id="d0842-158">Pirkimo YOY augimas %</span><span class="sxs-lookup"><span data-stu-id="d0842-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="d0842-159">Pirkimas pagal šalį</span><span class="sxs-lookup"><span data-stu-id="d0842-159">Purchase by country</span></span>

<span data-ttu-id="d0842-160">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="d0842-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="d0842-161">Pirkimo išlaidų analizės pagal laiką ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="d0842-162">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-162">**Charts**</span></span> 
- <span data-ttu-id="d0842-163">Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="d0842-164">Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="d0842-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="d0842-165">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="d0842-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="d0842-166">Pirkimo išlaidų analizės pagal tiekėją ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="d0842-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="d0842-167">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="d0842-167">**Charts**</span></span> 
- <span data-ttu-id="d0842-168">10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</span><span class="sxs-lookup"><span data-stu-id="d0842-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="d0842-169">10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</span><span class="sxs-lookup"><span data-stu-id="d0842-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="d0842-170">10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</span><span class="sxs-lookup"><span data-stu-id="d0842-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="d0842-171">**Pavyzdys** 
</span><span class="sxs-lookup"><span data-stu-id="d0842-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="d0842-172">Duomenų modelis ir objektai</span><span class="sxs-lookup"><span data-stu-id="d0842-172">Data model and entities</span></span>
<span data-ttu-id="d0842-173">Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai.</span><span class="sxs-lookup"><span data-stu-id="d0842-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="d0842-174">Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="d0842-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="d0842-175">Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="d0842-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="d0842-176">Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="d0842-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="d0842-177">Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="d0842-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="d0842-178">Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus.</span><span class="sxs-lookup"><span data-stu-id="d0842-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="d0842-179">Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [Power BI integravimas su objektų saugykla](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="d0842-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="d0842-180">Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.</span><span class="sxs-lookup"><span data-stu-id="d0842-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="d0842-181">Objektas</span><span class="sxs-lookup"><span data-stu-id="d0842-181">Entity</span></span>        | <span data-ttu-id="d0842-182">Pagrindiniai agreguoti matavimo vienetai</span><span class="sxs-lookup"><span data-stu-id="d0842-182">Key aggregate measurements</span></span> | <span data-ttu-id="d0842-183">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="d0842-183">Data source</span></span>                                 | <span data-ttu-id="d0842-184">Laukas</span><span class="sxs-lookup"><span data-stu-id="d0842-184">Field</span></span>              | <span data-ttu-id="d0842-185">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d0842-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="d0842-186">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="d0842-186">Invoice lines</span></span> | <span data-ttu-id="d0842-187">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="d0842-187">Purchase</span></span>                   | <span data-ttu-id="d0842-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="d0842-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="d0842-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="d0842-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="d0842-190">Suma, išreikšta apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="d0842-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="d0842-191">Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="d0842-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="d0842-192">Mato vnt.</span><span class="sxs-lookup"><span data-stu-id="d0842-192">Measure</span></span>               | <span data-ttu-id="d0842-193">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d0842-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0842-194">Pirkimas esamais metais</span><span class="sxs-lookup"><span data-stu-id="d0842-194">Purchase current year</span></span> | <span data-ttu-id="d0842-195">Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])</span><span class="sxs-lookup"><span data-stu-id="d0842-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="d0842-196">Pirkimas pastaraisiais metais</span><span class="sxs-lookup"><span data-stu-id="d0842-196">Purchase last year</span></span>    | <span data-ttu-id="d0842-197">Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="d0842-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="d0842-198">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="d0842-198">YOY purchase growth</span></span>   | <span data-ttu-id="d0842-199">YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]</span><span class="sxs-lookup"><span data-stu-id="d0842-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="d0842-200">Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.</span><span class="sxs-lookup"><span data-stu-id="d0842-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="d0842-201">Objektas</span><span class="sxs-lookup"><span data-stu-id="d0842-201">Entity</span></span>                 | <span data-ttu-id="d0842-202">Atributų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="d0842-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="d0842-203">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="d0842-203">Vendors</span></span>                | <span data-ttu-id="d0842-204">Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="d0842-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="d0842-205">Produktai</span><span class="sxs-lookup"><span data-stu-id="d0842-205">Products</span></span>               | <span data-ttu-id="d0842-206">Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d0842-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="d0842-207">Įsigijimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="d0842-207">Procurement categories</span></span> | <span data-ttu-id="d0842-208">Įsigijimo kategorija, įsigijimo kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="d0842-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="d0842-209">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="d0842-209">Legal entities</span></span>         | <span data-ttu-id="d0842-210">Juridinio subjekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d0842-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="d0842-211">Datos</span><span class="sxs-lookup"><span data-stu-id="d0842-211">Dates</span></span>                  | <span data-ttu-id="d0842-212">Datos, metų poslinkis</span><span class="sxs-lookup"><span data-stu-id="d0842-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="d0842-213">Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys.</span><span class="sxs-lookup"><span data-stu-id="d0842-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="d0842-214">Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="d0842-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="d0842-215">Taip pat galite pakeisti įmonės filtrą.</span><span class="sxs-lookup"><span data-stu-id="d0842-215">You can also change the company filter.</span></span>
