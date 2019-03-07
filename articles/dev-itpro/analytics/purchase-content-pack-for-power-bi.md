---
title: „Power BI“ turinys Pirkimo išlaidų analizė
description: Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "313847"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="fd359-104">„Power BI“ turinys Pirkimo išlaidų analizė</span><span class="sxs-lookup"><span data-stu-id="fd359-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd359-105">Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**.</span><span class="sxs-lookup"><span data-stu-id="fd359-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="fd359-106">Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.</span><span class="sxs-lookup"><span data-stu-id="fd359-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="fd359-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="fd359-107">Overview</span></span>

<span data-ttu-id="fd359-108">„Power BI“ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti stebėti pirkimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="fd359-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="fd359-109">Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.</span><span class="sxs-lookup"><span data-stu-id="fd359-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="fd359-110">Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)</span><span class="sxs-lookup"><span data-stu-id="fd359-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="fd359-111">Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)</span><span class="sxs-lookup"><span data-stu-id="fd359-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="fd359-112">Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą.</span><span class="sxs-lookup"><span data-stu-id="fd359-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="fd359-113">Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="fd359-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="fd359-114">Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas.</span><span class="sxs-lookup"><span data-stu-id="fd359-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="fd359-115">Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="fd359-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="fd359-116">Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="fd359-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="fd359-117">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="fd359-117">Accessing the Power BI content</span></span>
<span data-ttu-id="fd359-118">„Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** \> **Užklausos ir ataskaitos** \> **Pirkimo našumo analizė** \> **Pirkimo ir išlaidų analizė**).</span><span class="sxs-lookup"><span data-stu-id="fd359-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="fd359-119">Į „Power BI“ turinį įtrauktos metrikos</span><span class="sxs-lookup"><span data-stu-id="fd359-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="fd359-120">„Power BI“ turinyje **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="fd359-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="fd359-121">Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės</span><span class="sxs-lookup"><span data-stu-id="fd359-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="fd359-122">Toliau pateikiamoje lentelėje apžvelgiamos vizualizacijos.</span><span class="sxs-lookup"><span data-stu-id="fd359-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fd359-123">Ataskaitų puslapis</span><span class="sxs-lookup"><span data-stu-id="fd359-123">Report page</span></span></th>
<th><span data-ttu-id="fd359-124">Diagramos</span><span class="sxs-lookup"><span data-stu-id="fd359-124">Charts</span></span></th>
<th><span data-ttu-id="fd359-125">Išklotinės</span><span class="sxs-lookup"><span data-stu-id="fd359-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fd359-126">Pirkimas pagal tiekėją</span><span class="sxs-lookup"><span data-stu-id="fd359-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-127">10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="fd359-128">Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="fd359-129">Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="fd359-130">Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd359-131">Iš viso pirkimų</span><span class="sxs-lookup"><span data-stu-id="fd359-131">Total purchase</span></span></li>
<li><span data-ttu-id="fd359-132">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="fd359-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="fd359-133">Bendras # tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="fd359-133">Total # vendors</span></span></li>
<li><span data-ttu-id="fd359-134">Bendras # aktyvių tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="fd359-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd359-135">Pirkimas pagal produktą</span><span class="sxs-lookup"><span data-stu-id="fd359-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-136">Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="fd359-137">Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="fd359-138">10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd359-139">Iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="fd359-139">Total # of products</span></span></li>
<li><span data-ttu-id="fd359-140">Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="fd359-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="fd359-141">Produktų, sudarančių 80 % pirkimo, skaičius</span><span class="sxs-lookup"><span data-stu-id="fd359-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd359-142">Pirkimas pagal laikotarpį\*</span><span class="sxs-lookup"><span data-stu-id="fd359-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-143">Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="fd359-144">Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="fd359-145">Bendras pirkimo YOY augimas (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="fd359-146">Įsigijimo išrašas (matrica)</span><span class="sxs-lookup"><span data-stu-id="fd359-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="fd359-147">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="fd359-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="fd359-148">YOY pirkimo augimas %</span><span class="sxs-lookup"><span data-stu-id="fd359-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="fd359-149">Pirkimas pagal tiekėjo vietą</span><span class="sxs-lookup"><span data-stu-id="fd359-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-150">Pirkimas pagal miestą</span><span class="sxs-lookup"><span data-stu-id="fd359-150">Purchase by city</span></span></li>
<li><span data-ttu-id="fd359-151">Pirkimo YOY augimas %</span><span class="sxs-lookup"><span data-stu-id="fd359-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="fd359-152">Pirkimas pagal šalį</span><span class="sxs-lookup"><span data-stu-id="fd359-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="fd359-153">Pirkimo išlaidų analizė pagal laiką</span><span class="sxs-lookup"><span data-stu-id="fd359-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-154">Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="fd359-155">Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="fd359-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="fd359-156">Pirkimo išlaidų analizė pagal tiekėją</span><span class="sxs-lookup"><span data-stu-id="fd359-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="fd359-157">10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</span><span class="sxs-lookup"><span data-stu-id="fd359-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="fd359-158">10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</span><span class="sxs-lookup"><span data-stu-id="fd359-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="fd359-159">10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</span><span class="sxs-lookup"><span data-stu-id="fd359-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="fd359-160">\* Pirkimas šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="fd359-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="fd359-161">Duomenų modelis ir objektai</span><span class="sxs-lookup"><span data-stu-id="fd359-161">Data model and entities</span></span>
<span data-ttu-id="fd359-162">Tolesniais duomenimis pildomi „Power BI“ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai.</span><span class="sxs-lookup"><span data-stu-id="fd359-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="fd359-163">Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="fd359-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="fd359-164">Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="fd359-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="fd359-165">Daugiau informacijos žr. temoje [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="fd359-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="fd359-166">Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="fd359-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="fd359-167">Norint agreguotus kubo matavimo vienetus paruošti objektų saugykloje, juos reikia padaryti visuotinai įdiegiamus.</span><span class="sxs-lookup"><span data-stu-id="fd359-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="fd359-168">Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje [„Power BI“ integravimo su objektų saugykla apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="fd359-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="fd359-169">Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.</span><span class="sxs-lookup"><span data-stu-id="fd359-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="fd359-170">Objektas</span><span class="sxs-lookup"><span data-stu-id="fd359-170">Entity</span></span>        | <span data-ttu-id="fd359-171">Pagrindiniai agreguoti matavimo vienetai</span><span class="sxs-lookup"><span data-stu-id="fd359-171">Key aggregate measurements</span></span> | <span data-ttu-id="fd359-172">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="fd359-172">Data source</span></span>                                 | <span data-ttu-id="fd359-173">Laukas</span><span class="sxs-lookup"><span data-stu-id="fd359-173">Field</span></span>              | <span data-ttu-id="fd359-174">aprašymas</span><span class="sxs-lookup"><span data-stu-id="fd359-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="fd359-175">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="fd359-175">Invoice lines</span></span> | <span data-ttu-id="fd359-176">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="fd359-176">Purchase</span></span>                   | <span data-ttu-id="fd359-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="fd359-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="fd359-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="fd359-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="fd359-179">Suma, išreikšta apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="fd359-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="fd359-180">Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="fd359-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="fd359-181">Mato vnt.</span><span class="sxs-lookup"><span data-stu-id="fd359-181">Measure</span></span>               | <span data-ttu-id="fd359-182">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="fd359-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd359-183">Pirkimas esamais metais</span><span class="sxs-lookup"><span data-stu-id="fd359-183">Purchase current year</span></span> | <span data-ttu-id="fd359-184">Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])</span><span class="sxs-lookup"><span data-stu-id="fd359-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="fd359-185">Pirkimas pastaraisiais metais</span><span class="sxs-lookup"><span data-stu-id="fd359-185">Purchase last year</span></span>    | <span data-ttu-id="fd359-186">Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="fd359-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="fd359-187">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="fd359-187">YOY purchase growth</span></span>   | <span data-ttu-id="fd359-188">YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]</span><span class="sxs-lookup"><span data-stu-id="fd359-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="fd359-189">Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.</span><span class="sxs-lookup"><span data-stu-id="fd359-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="fd359-190">Objektas</span><span class="sxs-lookup"><span data-stu-id="fd359-190">Entity</span></span>                 | <span data-ttu-id="fd359-191">Atributų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="fd359-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="fd359-192">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="fd359-192">Vendors</span></span>                | <span data-ttu-id="fd359-193">Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="fd359-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="fd359-194">Produktai</span><span class="sxs-lookup"><span data-stu-id="fd359-194">Products</span></span>               | <span data-ttu-id="fd359-195">Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="fd359-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="fd359-196">Įsigijimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="fd359-196">Procurement categories</span></span> | <span data-ttu-id="fd359-197">Įsigijimo kategorija, įsigijimo kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="fd359-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="fd359-198">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="fd359-198">Legal entities</span></span>         | <span data-ttu-id="fd359-199">Juridinio subjekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="fd359-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="fd359-200">Datos</span><span class="sxs-lookup"><span data-stu-id="fd359-200">Dates</span></span>                  | <span data-ttu-id="fd359-201">Datos, metų poslinkis</span><span class="sxs-lookup"><span data-stu-id="fd359-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="fd359-202">Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys.</span><span class="sxs-lookup"><span data-stu-id="fd359-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="fd359-203">Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="fd359-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="fd359-204">Taip pat galite pakeisti įmonės filtrą.</span><span class="sxs-lookup"><span data-stu-id="fd359-204">You can also change the company filter.</span></span>
