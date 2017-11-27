---
title: "Pirkimo išlaidų analizės „Power BI“ turinys"
description: "Šioje temoje aprašoma, kas įtraukiama į „Power BI“ turinį Pirkimo išlaidų analizė. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turiniui kurti."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6485f36802fc4e327e223f47d65c4bdca11c1609
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="35b02-104">Pirkimo išlaidų analizės „Power BI“ turinys</span><span class="sxs-lookup"><span data-stu-id="35b02-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="35b02-105">Šioje temoje aprašoma, kas įtraukiama į „Microsoft Power BI“ turinį **Pirkimo išlaidų analizė**.</span><span class="sxs-lookup"><span data-stu-id="35b02-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="35b02-106">Joje paaiškinama, kaip pasiekti „Power BI“ ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, kurie naudojami turiniui kurti.</span><span class="sxs-lookup"><span data-stu-id="35b02-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="35b02-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="35b02-107">Overview</span></span>

<span data-ttu-id="35b02-108">„Power BI‟ turinys **Pirkimo išlaidų analizė** buvo sukurtas siekiant pirkimo vadovams ir vadovams, atsakingiems už biudžetus, padėti stebėti pirkimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="35b02-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="35b02-109">Vadovai pirkimo išlaidas gali analizuoti tolesniais būdais.</span><span class="sxs-lookup"><span data-stu-id="35b02-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="35b02-110">Metinis pirkimas iki datos (pagal tiekėjų grupę ir atskirus tiekėjus, įsigijimo kategoriją ir atskirus produktus ir tiekėjo vietą)</span><span class="sxs-lookup"><span data-stu-id="35b02-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="35b02-111">Pirkimo kiekvienais metais pokytis (pagal tiekėjų grupę ir įsigijimo kategoriją)</span><span class="sxs-lookup"><span data-stu-id="35b02-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="35b02-112">Turinyje naudojami pirkimo operacijų duomenys ir pateikiamas tiek sujungtas visos įmonės pirkimo skaičių rodinys, tiek pirkimo išlaidų analizė pagal tiekėją ir produktą.</span><span class="sxs-lookup"><span data-stu-id="35b02-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="35b02-113">Ataskaitose vaizduojami laikui bėgant atsiradę pirkimo išlaidų pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="35b02-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="35b02-114">Todėl ataskaitas galima naudoti norint vadovus įspėti apie teigiamas ir neigiamas atskirų tiekėjų ir produktų išlaidų tendencijas.</span><span class="sxs-lookup"><span data-stu-id="35b02-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="35b02-115">Be to, diagramose rodomos skirtingų įsigijimo kategorijų ir tiekėjų grupių pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="35b02-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="35b02-116">Todėl naudodami šias diagramas kategorijų ir regionų vadovai gali lengviau nustatyti išlaidų elgesio pokyčius.</span><span class="sxs-lookup"><span data-stu-id="35b02-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="35b02-117">Prieiga prie „Power BI“ turinio</span><span class="sxs-lookup"><span data-stu-id="35b02-117">Accessing the Power BI content</span></span>
<span data-ttu-id="35b02-118">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), „Power BI“ turinys **Pirkimo išlaidų analizė** rodomas puslapyje **Pirkimo ir išlaidų analizė** (**Paraiškos** > **Užklausos ir ataskaitos** > **Pirkimo našumo analizė** > **Pirkimo ir išlaidų analizė**).</span><span class="sxs-lookup"><span data-stu-id="35b02-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="35b02-119">Į „Power BI“ turinį įtrauktos metrikos</span><span class="sxs-lookup"><span data-stu-id="35b02-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="35b02-120">„Power BI‟ turinio pakete **Pirkimo išlaidų analizė** yra ataskaita, sudaryta iš metrikų rinkinio.</span><span class="sxs-lookup"><span data-stu-id="35b02-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="35b02-121">Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės</span><span class="sxs-lookup"><span data-stu-id="35b02-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="35b02-122">Toliau pateikiamoje lentelėje apžvelgiamos vizualizacijos.</span><span class="sxs-lookup"><span data-stu-id="35b02-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35b02-123">Ataskaitų puslapis</span><span class="sxs-lookup"><span data-stu-id="35b02-123">Report page</span></span></th>
<th><span data-ttu-id="35b02-124">Diagramos</span><span class="sxs-lookup"><span data-stu-id="35b02-124">Charts</span></span></th>
<th><span data-ttu-id="35b02-125">Išklotinės</span><span class="sxs-lookup"><span data-stu-id="35b02-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35b02-126">Pirkimas pagal tiekėją</span><span class="sxs-lookup"><span data-stu-id="35b02-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-127">10 svarbiausių tiekėjų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="35b02-128">Bendra pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="35b02-129">Pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="35b02-130">Vidutinė pirkimo suma pagal tiekėjų grupę / šalį / pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="35b02-131">Iš viso pirkimų</span><span class="sxs-lookup"><span data-stu-id="35b02-131">Total purchase</span></span></li>
<li><span data-ttu-id="35b02-132">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="35b02-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="35b02-133">Bendras # tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="35b02-133">Total # vendors</span></span></li>
<li><span data-ttu-id="35b02-134">Bendras # aktyvių tiekėjų skaičius</span><span class="sxs-lookup"><span data-stu-id="35b02-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b02-135">Pirkimas pagal produktą</span><span class="sxs-lookup"><span data-stu-id="35b02-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-136">Pirkti pagal įsigijimo kategoriją / produkto pavadinimą (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="35b02-137">Bendra pirkimo suma pagal įsigijimo kategoriją / produkto pavadinimą (skritulinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="35b02-138">10 populiariausių produktų pagal pirkimą (suspaustos juostos diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="35b02-139">Iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="35b02-139">Total # of products</span></span></li>
<li><span data-ttu-id="35b02-140">Bendra aktyvių produktų procentinė dalis, apimanti iš viso # produktų</span><span class="sxs-lookup"><span data-stu-id="35b02-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="35b02-141">Produktų, sudarančių 80 % pirkimo, skaičius</span><span class="sxs-lookup"><span data-stu-id="35b02-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b02-142">Pirkimas pagal laikotarpį*</span><span class="sxs-lookup"><span data-stu-id="35b02-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-143">Pirkimas pagal mėnesį / dieną (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="35b02-144">Sukauptas pirkimo YOY nuokrypis (krioklio diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="35b02-145">Bendras pirkimo YOY augimas (stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="35b02-146">Įsigijimo išrašas (matrica)</span><span class="sxs-lookup"><span data-stu-id="35b02-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="35b02-147">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="35b02-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="35b02-148">YOY pirkimo augimas %</span><span class="sxs-lookup"><span data-stu-id="35b02-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b02-149">Pirkimas pagal tiekėjo vietą</span><span class="sxs-lookup"><span data-stu-id="35b02-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-150">Pirkimas pagal miestą</span><span class="sxs-lookup"><span data-stu-id="35b02-150">Purchase by city</span></span></li>
<li><span data-ttu-id="35b02-151">Pirkimo YOY augimas %</span><span class="sxs-lookup"><span data-stu-id="35b02-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="35b02-152">Pirkimas pagal šalį</span><span class="sxs-lookup"><span data-stu-id="35b02-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35b02-153">Pirkimo išlaidų analizė pagal laiką</span><span class="sxs-lookup"><span data-stu-id="35b02-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-154">Pirkimas pagal esamų metų mėnesį / dieną (linijinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="35b02-155">Esamų ir pastarųjų metų pirkimas (linijinė ir stulpelinė diagrama)</span><span class="sxs-lookup"><span data-stu-id="35b02-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35b02-156">Pirkimo išlaidų analizė pagal tiekėją</span><span class="sxs-lookup"><span data-stu-id="35b02-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="35b02-157">10 geriausių tiekėjo pirkimo % kiekvienam pirkimui (piltuvėlis)</span><span class="sxs-lookup"><span data-stu-id="35b02-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="35b02-158">10 pagrindinių tiekėjų, kurių išlaidų YOY padidėjęs</span><span class="sxs-lookup"><span data-stu-id="35b02-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="35b02-159">10 pagrindinių tiekėjų, kurių išlaidų YOY sumažėjęs</span><span class="sxs-lookup"><span data-stu-id="35b02-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35b02-160">\* Pirkimas šiais ir praėjusiais metais ir augimas pagal įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="35b02-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="35b02-161">„Power BI“ turinio išplėtimas</span><span class="sxs-lookup"><span data-stu-id="35b02-161">Extending the Power BI content</span></span>
<span data-ttu-id="35b02-162">Naudodami turinio paketus, kurie pateikiami „Microsoft Dynamics Lifecycle Services“ (LCS), žmonėms, kurie neprisijungia prie „Microsoft Dynamics 365“ galite pateikti didžiąją analizę.</span><span class="sxs-lookup"><span data-stu-id="35b02-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="35b02-163">Galite keisti šiuos turinio paketus, kad į juos įtrauktumėte kitas ataskaitas arba vaizdinius, o po to paskelbti turinio paketus savo Power BI.com nuomotojui analizei.</span><span class="sxs-lookup"><span data-stu-id="35b02-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="35b02-164">„Power BI“ turinį **Pirkimo išlaidų analizė** galite rasti LCS bibliotekoje Bendrai naudojamas turtas.</span><span class="sxs-lookup"><span data-stu-id="35b02-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="35b02-165">Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="35b02-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="35b02-166">Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).</span><span class="sxs-lookup"><span data-stu-id="35b02-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="35b02-167">Įsitikinkite, kad atsisiunčiate tą turinį **Pirkimo išlaidų analizė**, kuris taikomas jūsų naudojamai „Dynamics 365‟ versijai.</span><span class="sxs-lookup"><span data-stu-id="35b02-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="35b02-168">Jei naudojate „Microsoft Dynamics 365 for Operations‟ 1611 versiją, norint naudoti šį „Power BI‟ turinį būtina įdiegti KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="35b02-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="35b02-169">Prisijungę prie LCS, KB galite pasiekti adresu https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="35b02-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="35b02-170">Duomenų modelis ir objektai</span><span class="sxs-lookup"><span data-stu-id="35b02-170">Data model and entities</span></span>
<span data-ttu-id="35b02-171">Tolesniais duomenimis pildomi „Power BI‟ turinio **Pirkimo išlaidų analizė** ataskaitų puslapiai.</span><span class="sxs-lookup"><span data-stu-id="35b02-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="35b02-172">Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje.</span><span class="sxs-lookup"><span data-stu-id="35b02-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="35b02-173">Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="35b02-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="35b02-174">Daugiau informacijos žr. temoje [„Power BI‟ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="35b02-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="35b02-175">Agreguoti matavimo vienetai šiame turinyje yra agreguotų matavimo vienetų, kurie buvo pasiekiami „Microsoft Dynamics AX 2012“ ir „Microsoft Dynamics AX 2012 R3“ pirkimo kube, subrinkinys.</span><span class="sxs-lookup"><span data-stu-id="35b02-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="35b02-176">Norint perkelti kubo agreguotus matavimo vienetus į objekto parduotuvę, reikia padaryti juos įdiegiamus.</span><span class="sxs-lookup"><span data-stu-id="35b02-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="35b02-177">Norėdami gauti daugiau informacijos, žr. procedūrą, kaip agreguotus matavimo vienetus paruošti objektų saugykloje ([„Power BI“ integravimo su objektų saugykla apžvalga](power-bi-integration-entity-store.md)).</span><span class="sxs-lookup"><span data-stu-id="35b02-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="35b02-178">Tolesnius pagrindinius agreguotus matavimo vienetus galima gauti tiesiai iš objekto Sąskaitos faktūros eilutės ir jie naudojami kaip turinio pagrindas.</span><span class="sxs-lookup"><span data-stu-id="35b02-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="35b02-179">Objektas</span><span class="sxs-lookup"><span data-stu-id="35b02-179">Entity</span></span>        | <span data-ttu-id="35b02-180">Pagrindiniai agreguoti matavimo vienetai</span><span class="sxs-lookup"><span data-stu-id="35b02-180">Key aggregate measurements</span></span> | <span data-ttu-id="35b02-181">Duomenų šaltinis</span><span class="sxs-lookup"><span data-stu-id="35b02-181">Data source</span></span>                                 | <span data-ttu-id="35b02-182">Laukas</span><span class="sxs-lookup"><span data-stu-id="35b02-182">Field</span></span>              | <span data-ttu-id="35b02-183">aprašymas</span><span class="sxs-lookup"><span data-stu-id="35b02-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="35b02-184">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="35b02-184">Invoice lines</span></span> | <span data-ttu-id="35b02-185">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="35b02-185">Purchase</span></span>                   | <span data-ttu-id="35b02-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="35b02-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="35b02-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="35b02-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="35b02-188">Suma, išreikšta apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="35b02-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="35b02-189">Toliau pateiktoje lentelėje nurodomi pagrindiniai turinyje naudojami matavimo vienetai, apskaičiuojami pagal objektą Sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="35b02-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="35b02-190">Mato vnt.</span><span class="sxs-lookup"><span data-stu-id="35b02-190">Measure</span></span>               | <span data-ttu-id="35b02-191">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="35b02-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b02-192">Pirkimas esamais metais</span><span class="sxs-lookup"><span data-stu-id="35b02-192">Purchase current year</span></span> | <span data-ttu-id="35b02-193">Pirkimas esamais metais = SUM('SF eilutės'\[Pirkimas\])</span><span class="sxs-lookup"><span data-stu-id="35b02-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="35b02-194">Pirkimas pastaraisiais metais</span><span class="sxs-lookup"><span data-stu-id="35b02-194">Purchase last year</span></span>    | <span data-ttu-id="35b02-195">Pirkimas pastaraisiais metais = CALCULATE(SUM('SF eilutės'\[Pirkimas\]), SAMEPERIODLASTYEAR(Datos\[Data\]))</span><span class="sxs-lookup"><span data-stu-id="35b02-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="35b02-196">YOY pirkimo augimas</span><span class="sxs-lookup"><span data-stu-id="35b02-196">YOY purchase growth</span></span>   | <span data-ttu-id="35b02-197">YOY pirkimo augimas = \[Pirkimas esamais metais\] – \[Pirkimas pastaraisiais metais\]</span><span class="sxs-lookup"><span data-stu-id="35b02-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="35b02-198">Šios pagrindinės turinio dimensijos naudojamos kaip filtrai agreguotiems matavimo vienetams segmentuoti, kad būtų galima pasiekti daugiau detalumo ir gauti gilesnių analitinių įžvalgų.</span><span class="sxs-lookup"><span data-stu-id="35b02-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="35b02-199">Objektas</span><span class="sxs-lookup"><span data-stu-id="35b02-199">Entity</span></span>                 | <span data-ttu-id="35b02-200">Atributų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="35b02-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="35b02-201">Tiekėjai</span><span class="sxs-lookup"><span data-stu-id="35b02-201">Vendors</span></span>                | <span data-ttu-id="35b02-202">Tiekėjų grupės, tiekėjo šalis arba regionai, tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="35b02-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="35b02-203">Produktai</span><span class="sxs-lookup"><span data-stu-id="35b02-203">Products</span></span>               | <span data-ttu-id="35b02-204">Produkto numeris, produkto pavadinimas, prekių grupių pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35b02-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="35b02-205">Įsigijimo kategorijos</span><span class="sxs-lookup"><span data-stu-id="35b02-205">Procurement categories</span></span> | <span data-ttu-id="35b02-206">Įsigijimo kategorija, įsigijimo kategorijų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="35b02-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="35b02-207">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="35b02-207">Legal entities</span></span>         | <span data-ttu-id="35b02-208">Juridinio subjekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="35b02-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="35b02-209">Datos</span><span class="sxs-lookup"><span data-stu-id="35b02-209">Dates</span></span>                  | <span data-ttu-id="35b02-210">Datos, metų poslinkis</span><span class="sxs-lookup"><span data-stu-id="35b02-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="35b02-211">Pagal numatytuosius parametrus turinyje rodomi esamų kalendorinių metų duomenys.</span><span class="sxs-lookup"><span data-stu-id="35b02-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="35b02-212">Tačiau ataskaitos filtrų skyriuje datos filtrą galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="35b02-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="35b02-213">Taip pat galite pakeisti įmonės filtrą.</span><span class="sxs-lookup"><span data-stu-id="35b02-213">You can also change the company filter.</span></span>

