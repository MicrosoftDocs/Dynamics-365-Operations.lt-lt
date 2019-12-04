---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti.
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
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2d31aaf14f6399baca8531707864c48cd2d56ac2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769976"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="ebc3f-104">„Power BI“ turinys Pirkimo išlaidų analizė</span><span class="sxs-lookup"><span data-stu-id="ebc3f-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebc3f-105">Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="ebc3f-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="ebc3f-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ebc3f-107">Overview</span></span>

<span data-ttu-id="ebc3f-108">„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti sekti pirkimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="ebc3f-109">Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="ebc3f-110">Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="ebc3f-111">Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="ebc3f-112">Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="ebc3f-113">Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="ebc3f-114">Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="ebc3f-115">Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="ebc3f-116">Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="ebc3f-117">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="ebc3f-117">Accessing the Power BI content</span></span>
<span data-ttu-id="ebc3f-118">„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).</span><span class="sxs-lookup"><span data-stu-id="ebc3f-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="ebc3f-119">Į „Power BI“ turinį įtrauktos metrikos</span><span class="sxs-lookup"><span data-stu-id="ebc3f-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="ebc3f-120">„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="ebc3f-121">Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės</span><span class="sxs-lookup"><span data-stu-id="ebc3f-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="ebc3f-122">Toliau pateikiamuose skyriuose apžvelgiamos vizualizacijos.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="ebc3f-123">Pirkimo pagal tiekėjo ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-123">Purchase by vendor report page</span></span>
<span data-ttu-id="ebc3f-124">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-124">**Charts**</span></span>
- <span data-ttu-id="ebc3f-125">10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="ebc3f-126">Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="ebc3f-127">Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="ebc3f-128">Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="ebc3f-129">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-129">**Tiles**</span></span>
- <span data-ttu-id="ebc3f-130">Iš viso pirkimų</span><span class="sxs-lookup"><span data-stu-id="ebc3f-130">Total purchase</span></span>
- <span data-ttu-id="ebc3f-131">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-131">YOY purchase growth</span></span>
- <span data-ttu-id="ebc3f-132">Bendras # tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="ebc3f-132">Total # vendors</span></span>
- <span data-ttu-id="ebc3f-133">Bendras # aktyvių tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="ebc3f-133">Total # of active vendors</span></span>

<span data-ttu-id="ebc3f-134">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="ebc3f-135">Pirkimo pagal produkto ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-135">Purchase by product report page</span></span>

<span data-ttu-id="ebc3f-136">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-136">**Charts**</span></span>
- <span data-ttu-id="ebc3f-137">Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="ebc3f-138">Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="ebc3f-139">10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="ebc3f-140">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-140">**Tiles**</span></span>
- <span data-ttu-id="ebc3f-141">Iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="ebc3f-141">Total # of products</span></span></li>
- <span data-ttu-id="ebc3f-142">Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="ebc3f-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="ebc3f-143">Produktų, sudarančių 80 % pirkimo, skaičius</span><span class="sxs-lookup"><span data-stu-id="ebc3f-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="ebc3f-144">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="ebc3f-145">Pirkimo pagal laikotarpio ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-145">Purchase by period report page</span></span>
<span data-ttu-id="ebc3f-146">Šiame puslapyje pateikiami pirkimai šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="ebc3f-147">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-147">**Charts**</span></span> 
- <span data-ttu-id="ebc3f-148">Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="ebc3f-149">Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="ebc3f-150">Bendras pirkimo YOY augimas (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="ebc3f-151">Įsigijimo išrašas (matrica)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="ebc3f-152">**Išklotinės**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-152">**Tiles**</span></span>
- <span data-ttu-id="ebc3f-153">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-153">YOY purchase growth</span></span>
- <span data-ttu-id="ebc3f-154">YOY pirkimo augimas %</span><span class="sxs-lookup"><span data-stu-id="ebc3f-154">YOY purchase growth %</span></span>

<span data-ttu-id="ebc3f-155">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="ebc3f-156">Pirkimo pagal vietos ataskaitą puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="ebc3f-157">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-157">**Charts**</span></span>
- <span data-ttu-id="ebc3f-158">Pirkimas pagal miestą</span><span class="sxs-lookup"><span data-stu-id="ebc3f-158">Purchase by city</span></span>
- <span data-ttu-id="ebc3f-159">Pirkimo YOY augimas %</span><span class="sxs-lookup"><span data-stu-id="ebc3f-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="ebc3f-160">Pirkimas pagal šalį</span><span class="sxs-lookup"><span data-stu-id="ebc3f-160">Purchase by country</span></span>

<span data-ttu-id="ebc3f-161">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="ebc3f-162">Pirkimo išlaidų analizės pagal laiką ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="ebc3f-163">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-163">**Charts**</span></span> 
- <span data-ttu-id="ebc3f-164">Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="ebc3f-165">Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="ebc3f-166">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="ebc3f-167">Pirkimo išlaidų analizės pagal tiekėją ataskaitos puslapis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="ebc3f-168">**Diagramos**</span><span class="sxs-lookup"><span data-stu-id="ebc3f-168">**Charts**</span></span> 
- <span data-ttu-id="ebc3f-169">10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="ebc3f-170">10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</span><span class="sxs-lookup"><span data-stu-id="ebc3f-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="ebc3f-171">10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</span><span class="sxs-lookup"><span data-stu-id="ebc3f-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="ebc3f-172">**Pavyzdys** 
</span><span class="sxs-lookup"><span data-stu-id="ebc3f-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="ebc3f-173">Duomenų modelis ir objektai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-173">Data model and entities</span></span>
<span data-ttu-id="ebc3f-174">Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="ebc3f-175">Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="ebc3f-176">Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="ebc3f-177">Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="ebc3f-177">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="ebc3f-178">Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="ebc3f-179">Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="ebc3f-180">Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [Power BI integravimas su objektų saugykla](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="ebc3f-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="ebc3f-181">Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="ebc3f-182">Objektas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-182">Entity</span></span>        | <span data-ttu-id="ebc3f-183">Pagrindiniai agreguoti matavimo vienetai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-183">Key aggregate measurements</span></span> | <span data-ttu-id="ebc3f-184">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-184">Data source</span></span>                                 | <span data-ttu-id="ebc3f-185">Laukas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-185">Field</span></span>              | <span data-ttu-id="ebc3f-186">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="ebc3f-187">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="ebc3f-187">Invoice lines</span></span> | <span data-ttu-id="ebc3f-188">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-188">Purchase</span></span>                   | <span data-ttu-id="ebc3f-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="ebc3f-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="ebc3f-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="ebc3f-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="ebc3f-191">Suma, išreikšta apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="ebc3f-192">Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="ebc3f-193">Mato vnt.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-193">Measure</span></span>               | <span data-ttu-id="ebc3f-194">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc3f-195">Pirkimas esamais metais</span><span class="sxs-lookup"><span data-stu-id="ebc3f-195">Purchase current year</span></span> | <span data-ttu-id="ebc3f-196">Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])</span><span class="sxs-lookup"><span data-stu-id="ebc3f-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="ebc3f-197">Pirkimas pastaraisiais metais</span><span class="sxs-lookup"><span data-stu-id="ebc3f-197">Purchase last year</span></span>    | <span data-ttu-id="ebc3f-198">Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="ebc3f-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="ebc3f-199">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-199">YOY purchase growth</span></span>   | <span data-ttu-id="ebc3f-200">YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]</span><span class="sxs-lookup"><span data-stu-id="ebc3f-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="ebc3f-201">Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="ebc3f-202">Objektas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-202">Entity</span></span>                 | <span data-ttu-id="ebc3f-203">Atributų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="ebc3f-204">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-204">Vendors</span></span>                | <span data-ttu-id="ebc3f-205">Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="ebc3f-206">Produktai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-206">Products</span></span>               | <span data-ttu-id="ebc3f-207">Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="ebc3f-208">Įsigijimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="ebc3f-208">Procurement categories</span></span> | <span data-ttu-id="ebc3f-209">Įsigijimo kategorija, įsigijimo kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="ebc3f-210">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="ebc3f-210">Legal entities</span></span>         | <span data-ttu-id="ebc3f-211">Juridinio subjekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ebc3f-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="ebc3f-212">Datos</span><span class="sxs-lookup"><span data-stu-id="ebc3f-212">Dates</span></span>                  | <span data-ttu-id="ebc3f-213">Datos, metų poslinkis</span><span class="sxs-lookup"><span data-stu-id="ebc3f-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="ebc3f-214">Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="ebc3f-215">Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="ebc3f-216">Taip pat galite pakeisti įmonės filtrą.</span><span class="sxs-lookup"><span data-stu-id="ebc3f-216">You can also change the company filter.</span></span>
