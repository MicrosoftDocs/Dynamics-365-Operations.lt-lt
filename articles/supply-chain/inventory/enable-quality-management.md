---
title: "Kokybės valdymo peržiūra"
description: "Šiame straipsnyje aprašyta, kaip galima naudoti kokybės valdymą „Finance and Operations“, siekiant pagerinti tiekimo grandinės produktų kokybę."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 28ef47e2dc1f9c7e1c0b262c58332dcfea1f7495
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="quality-management-overview"></a><span data-ttu-id="eb176-103">Kokybės valdymo peržiūra</span><span class="sxs-lookup"><span data-stu-id="eb176-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eb176-104">Šiame straipsnyje aprašyta, kaip galima naudoti kokybės valdymą „Finance and Operations“, siekiant pagerinti tiekimo grandinės produktų kokybę.</span><span class="sxs-lookup"><span data-stu-id="eb176-104">This article describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="eb176-105">Kokybės valdymas gali padėti valdyti apgręžimo laiką tvarkant neatitinkančius produktus, neatsižvelgiant į kilmę.</span><span class="sxs-lookup"><span data-stu-id="eb176-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="eb176-106">Kadangi diagnozės tipai yra susiję su koregavimo ataskaitomis, „Microsoft Dynamics 365 for Finance and Operations‟ gali planuoti užduotis ir jomis taisyti problemas bei neleisti joms pasikartoti.</span><span class="sxs-lookup"><span data-stu-id="eb176-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="eb176-107">Be funkcijų, skirtų valdyti neatitikimui, kokybės valdymas apima funkcijas, skirtas problemoms sekti pagal jų tipą (net vidaus problemoms) ir sprendimams identifikuoti kaip trumpalaikiams ar ilgalaikiams.</span><span class="sxs-lookup"><span data-stu-id="eb176-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="eb176-108">Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnių neatitikimo problemų istoriją ir sprendimus, kurie buvo naudojami joms taisyti.</span><span class="sxs-lookup"><span data-stu-id="eb176-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="eb176-109">Galite naudoti praeities duomenis ir peržiūrėti ankstesnių kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.</span><span class="sxs-lookup"><span data-stu-id="eb176-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="eb176-110">Kai nustatote kokybės susiejimą, „Finance and Operations‟ gali generuoti įvairių verslo procesų, įvykių ir sąlygų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="eb176-111">Kokybės susiejimas gali apimti konkrečią prekę, konkrečią prekių grupę arba visas prekes.</span><span class="sxs-lookup"><span data-stu-id="eb176-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="eb176-112">Kokybės valdymo naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="eb176-112">Examples of the use of quality management</span></span>
<span data-ttu-id="eb176-113">Kokybės valdymas yra lankstus ir gali būti diegiamas įvairiais būdais, siekiant atitikti konkrečių tiekimo grandinės operacijų lygių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="eb176-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="eb176-114">Toliau pateikti pavyzdžiai iliustruoja galimą šių funkcijų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="eb176-115">Pagal iš anksto nustatytus kriterijus automatiškai paleisti kokybės kontrolės procesą (sandėlyje registravus pirkimo užsakymą iš konkretaus tiekėjo).</span><span class="sxs-lookup"><span data-stu-id="eb176-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="eb176-116">Tikrinimo metu blokuoti atsargas, siekiant neleisti naudoti nepatvirtintų atsargų (visiškas pirkimo užsakymų kiekių blokavimas).</span><span class="sxs-lookup"><span data-stu-id="eb176-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="eb176-117">Kaip kokybės susiejimo dalį naudoti prekių pavyzdžių ėmimą, siekiant apibrėžti dabartinių faktinių atsargų, kurias reikia tikrinti, sumą.</span><span class="sxs-lookup"><span data-stu-id="eb176-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="eb176-118">Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais arba procentine dalimi.</span><span class="sxs-lookup"><span data-stu-id="eb176-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="eb176-119">kurkite dalinių kvitų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="eb176-120">Norėdami kurti kokybės užsakymą, pagrįstą faktiškai su užsakymu gautu kiekiu, formoje **Prekės pavyzdžio ėmimas** turite pažymėti žymės langelį **Pagal atnaujintą kiekį**.</span><span class="sxs-lookup"><span data-stu-id="eb176-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="eb176-121">Kurti testų tipus, apimančius minimalias, maksimalias ir paskirties testo reikšmes, ir atlikti kokybės–kiekybės tikrinimą su iš anksto nustatytais tikrinimo rezultatais.</span><span class="sxs-lookup"><span data-stu-id="eb176-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="eb176-122">Nurodyti priimtiną kokybės lygį (AQL), siekiant kontroliuoti leistinus kokybės matavimo nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="eb176-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="eb176-123">Nurodyti išteklius, kurių reikia tikrinimo operacijai, pvz., tikrinimo sritį ir tikrinimo priemones.</span><span class="sxs-lookup"><span data-stu-id="eb176-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="eb176-124">Darbas su kokybės susiejimais</span><span class="sxs-lookup"><span data-stu-id="eb176-124">Working with quality associations</span></span>
<span data-ttu-id="eb176-125">Verslo procesas, kuris naudoja kokybės susiejimą, gali būti susijęs su įvairiais šaltinio dokumentais, pvz., pirkimo užsakymais, pardavimo užsakymais ar gamybos užsakymais.</span><span class="sxs-lookup"><span data-stu-id="eb176-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="eb176-126">Kiekvienas kokybės susiejimo įrašas apibrėžia bandymų rinkinį, AQL ir pavyzdžių ėmimo planą, kuris taikomas generuojamiems kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="eb176-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="eb176-127">Turite apibrėžti kiekvieno verslo proceso varianto kokybės susiejimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="eb176-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="eb176-128">Pavyzdžiui, galite nustatyti kokybės susiejimą, kuris generuoja kokybės užsakymą, kai atnaujinamas pirkimo užsakymo produktų kvitas.</span><span class="sxs-lookup"><span data-stu-id="eb176-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="eb176-129">Atsižvelgiant į vykdymo plano sąranką, esant atidarytam kokybės užsakymui, gali būti blokuojamas pats paleidimo procesas, arba gali būti blokuojami tolesni procesai, pvz., pirkimo užsakymų SF išrašymas.</span><span class="sxs-lookup"><span data-stu-id="eb176-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="eb176-130">**Pastaba.** Kol yra atidarytų kokybės užsakymų, automatiškai blokuojamas atsargų kiekių išdavimas.</span><span class="sxs-lookup"><span data-stu-id="eb176-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="eb176-131">Atsižvelgiant į **Visiško blokavimo** nuostatą **Prekių pavyzdžių** puslapyje, kiekis yra arba kokybės užsakymo kiekis, arba šaltinio dokumento eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="eb176-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="eb176-132">Nurodyto verslo proceso kokybės susiejimo įrašas identifikuoja įvykį ir sąlygas, kuriems sugeneruotas kokybės užsakymas.</span><span class="sxs-lookup"><span data-stu-id="eb176-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="eb176-133">Sąlygos gali būti būdingos teritorijai arba juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="eb176-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="eb176-134">Ardomuosius bandymus apimantis kokybės užsakymas gali būti sugeneruotas tik kai yra turimų įvykio atsargų.</span><span class="sxs-lookup"><span data-stu-id="eb176-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="eb176-135">Toliau pateikti pavyzdžiai iliustruoja, kaip kokybės susiejimo įrašas apibrėžiamas kiekvieno verslo proceso pokyčiams.</span><span class="sxs-lookup"><span data-stu-id="eb176-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="eb176-136">Toliau pateiktoje lentelėje apibendrinami kiekvieno pavyzdžio įvykiai ir sąlygos, kuriuos apibrėžia kokybės susiejimo įrašas.</span><span class="sxs-lookup"><span data-stu-id="eb176-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="eb176-137">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="eb176-137">Reference type</span></span></th>
<th><span data-ttu-id="eb176-138">Įvykio tipas</span><span class="sxs-lookup"><span data-stu-id="eb176-138">Event type</span></span></th>
<th><span data-ttu-id="eb176-139">Vykdymas</span><span class="sxs-lookup"><span data-stu-id="eb176-139">Execution</span></span></th>
<th><span data-ttu-id="eb176-140">Įvykio blokavimas</span><span class="sxs-lookup"><span data-stu-id="eb176-140">Event blocking</span></span></th>
<th><span data-ttu-id="eb176-141">Dokumento nuoroda</span><span class="sxs-lookup"><span data-stu-id="eb176-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="eb176-142">Atsargos</span><span class="sxs-lookup"><span data-stu-id="eb176-142">Inventory</span></span></td>
<td><span data-ttu-id="eb176-143">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="eb176-143">Not applicable</span></span></td>
<td><span data-ttu-id="eb176-144">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="eb176-144">Not applicable</span></span></td>
<td><span data-ttu-id="eb176-145">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-145">None</span></span></td>
<td><span data-ttu-id="eb176-146">Visi</span><span class="sxs-lookup"><span data-stu-id="eb176-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="eb176-147">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="eb176-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="eb176-148">Išrinkimo procesas suplanuotas</span><span class="sxs-lookup"><span data-stu-id="eb176-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="eb176-149">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-149">Before</span></span></td>
<td><span data-ttu-id="eb176-150">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="eb176-151">Konkretus ID, Grupė arba tik Viskas.</span><span class="sxs-lookup"><span data-stu-id="eb176-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-152">Išrinkimo procesas</span><span class="sxs-lookup"><span data-stu-id="eb176-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-153">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="eb176-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-154">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb176-155">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="eb176-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-156">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-156">Before</span></span></td>
<td><span data-ttu-id="eb176-157">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-158">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="eb176-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-159">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="eb176-160">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="eb176-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="eb176-161">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="eb176-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="eb176-162">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-162">Before</span></span></td>
<td><span data-ttu-id="eb176-163">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-164">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="eb176-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-165">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="eb176-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-166">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb176-167">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-167">After</span></span></td>
<td><span data-ttu-id="eb176-168">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-169">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="eb176-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-170">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb176-171">Registracija</span><span class="sxs-lookup"><span data-stu-id="eb176-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-172">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="eb176-172">Not applicable</span></span></td>
<td><span data-ttu-id="eb176-173">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-174">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="eb176-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-175">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="eb176-176">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="eb176-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-177">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-177">Before</span></span></td>
<td><span data-ttu-id="eb176-178">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-179">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="eb176-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-180">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb176-181">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-181">After</span></span></td>
<td><span data-ttu-id="eb176-182">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-183">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="eb176-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="eb176-184">Gamyba</span><span class="sxs-lookup"><span data-stu-id="eb176-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-185">Registracija</span><span class="sxs-lookup"><span data-stu-id="eb176-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="eb176-186">Not applicable</span></span></td>
<td><span data-ttu-id="eb176-187">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="eb176-188">Visi</span><span class="sxs-lookup"><span data-stu-id="eb176-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-189">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-190">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="eb176-191">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-192">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-192">Before</span></span></td>
<td><span data-ttu-id="eb176-193">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-194">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-195">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb176-196">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-196">After</span></span></td>
<td><span data-ttu-id="eb176-197">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-198">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="eb176-199">Sulaikymas</span><span class="sxs-lookup"><span data-stu-id="eb176-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-200">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="eb176-201">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-201">Before</span></span></td>
<td><span data-ttu-id="eb176-202">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-203">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-204">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-204">After</span></span></td>
<td><span data-ttu-id="eb176-205">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-206">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-206">End</span></span></td>
<td><span data-ttu-id="eb176-207">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-207">Before</span></span></td>
<td><span data-ttu-id="eb176-208">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="eb176-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb176-209">Maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="eb176-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-210">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="eb176-211">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-211">Before</span></span></td>
<td><span data-ttu-id="eb176-212">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-213">Konkretus ID, Grupė arba Viskas, ir Konkretaus ištekliaus, Grupė arba Viskas</span><span class="sxs-lookup"><span data-stu-id="eb176-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-214">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-215">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-215">After</span></span></td>
<td><span data-ttu-id="eb176-216">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="eb176-217">Sudėtinio produkto gamyba</span><span class="sxs-lookup"><span data-stu-id="eb176-217">Co-product production</span></span></td>
<td><span data-ttu-id="eb176-218">Registracija</span><span class="sxs-lookup"><span data-stu-id="eb176-218">Registration</span></span></td>
<td><span data-ttu-id="eb176-219">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="eb176-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-220">Nėra</span><span class="sxs-lookup"><span data-stu-id="eb176-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="eb176-221">Visi</span><span class="sxs-lookup"><span data-stu-id="eb176-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="eb176-222">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="eb176-222">Report as finished</span></span></td>
<td><span data-ttu-id="eb176-223">Prieš</span><span class="sxs-lookup"><span data-stu-id="eb176-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-224">Po</span><span class="sxs-lookup"><span data-stu-id="eb176-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eb176-225">Toliau pateiktoje lentelėje pateikiama daugiau informacijos apie tai, kaip galima generuoti konkrečių tipų procesų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="eb176-226">Proceso tipas</span><span class="sxs-lookup"><span data-stu-id="eb176-226">Type of process</span></span></th>
<th><span data-ttu-id="eb176-227">Kai kokybės užsakymus galima generuoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="eb176-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="eb176-228">Kai kokybės užsakymus galima generuoti, jei reikia ardomojo bandymo.</span><span class="sxs-lookup"><span data-stu-id="eb176-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="eb176-229">Sąlygų informacija</span><span class="sxs-lookup"><span data-stu-id="eb176-229">Condition information</span></span></th>
<th><span data-ttu-id="eb176-230">Rankinio generavimo informacija</span><span class="sxs-lookup"><span data-stu-id="eb176-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="eb176-231">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="eb176-231">Purchase order</span></span></td>
<td><span data-ttu-id="eb176-232">Prieš užregistruojant kvitų sąrašą arba gautos medžiagos kvitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="eb176-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="eb176-233">Užregistravus gautos medžiagos kvitą, nes medžiaga turi būti prieinama ardomajam bandymui.</span><span class="sxs-lookup"><span data-stu-id="eb176-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="eb176-234">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="eb176-235">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pirkimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-236">Sulaikymo užsakymas</span><span class="sxs-lookup"><span data-stu-id="eb176-236">Quarantine order</span></span></td>
<td><span data-ttu-id="eb176-237">Prieš sulaikymo užsakymą nurodant baigtu arba po to.</span><span class="sxs-lookup"><span data-stu-id="eb176-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="eb176-238">Kokybės užsakymų, kuriems reikia atlikti ardomuosius bandymus, generuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="eb176-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="eb176-239">Daroma prielaida, kad sulaikymo užsakymo funkcijos tvarko sunaikintos medžiagos perdavimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="eb176-240">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="eb176-241">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis sulaikymo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-242">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="eb176-242">Sales order</span></span></td>
<td><span data-ttu-id="eb176-243">Prieš siunčiamų prekių suplanuotą paėmimo procesą ar važtaraščio naujinimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="eb176-244">Atliekant bet kurį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="eb176-244">At any step</span></span></td>
<td><span data-ttu-id="eb176-245">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, klientą arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="eb176-246">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pardavimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-247">Gamybos užsakymas</span><span class="sxs-lookup"><span data-stu-id="eb176-247">Production order</span></span></td>
<td><span data-ttu-id="eb176-248">Prieš pranešant apie baigtą gamybos užsakymo kiekį, arba po to.</span><span class="sxs-lookup"><span data-stu-id="eb176-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="eb176-249">Pranešus apie baigtą gamybos užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="eb176-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="eb176-250">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="eb176-251">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis gamybos užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-252">Gamybos užsakymas su maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="eb176-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="eb176-253">Prieš baigiant operacijos ataskaitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="eb176-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="eb176-254">Pranešus, kad paskutinės operacijos gamyba baigta.</span><span class="sxs-lookup"><span data-stu-id="eb176-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="eb176-255">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę ar operacijų išteklių, arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="eb176-256">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis maršruto operaciją, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eb176-257">Atsargos</span><span class="sxs-lookup"><span data-stu-id="eb176-257">Inventory</span></span></td>
<td><span data-ttu-id="eb176-258">Kokybės užsakymo negalima automatiškai generuoti atsargų žurnalo operacijai arba perkėlimo užsakymo operacijoms.</span><span class="sxs-lookup"><span data-stu-id="eb176-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="eb176-259">Prekės atsargų kiekio kokybės užsakymą reikia kurti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="eb176-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="eb176-260">Reikia faktiškai turimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="eb176-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="eb176-261">Kokybės valdymo puslapiai</span><span class="sxs-lookup"><span data-stu-id="eb176-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eb176-262">Puslapis</span><span class="sxs-lookup"><span data-stu-id="eb176-262">Page</span></span></th>
<th><span data-ttu-id="eb176-263">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="eb176-263">Description</span></span></th>
<th><span data-ttu-id="eb176-264">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="eb176-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eb176-265">Kokybės susiejimai</span><span class="sxs-lookup"><span data-stu-id="eb176-265">Quality associations</span></span></td>
<td><span data-ttu-id="eb176-266">Žr. ankstesnius šio straipsnio skyrius.</span><span class="sxs-lookup"><span data-stu-id="eb176-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="eb176-267">Kokybės susiejimas apibrėžia visą toliau nurodytą generuojamo kokybės užsakymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb176-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="eb176-268">Operacijos įvykį.</span><span class="sxs-lookup"><span data-stu-id="eb176-268">The transaction event</span></span></li>
<li><span data-ttu-id="eb176-269">Prekių bandymų, kuriuos reikia atlikti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="eb176-270">AQL.</span><span class="sxs-lookup"><span data-stu-id="eb176-270">The AQL</span></span></li>
<li><span data-ttu-id="eb176-271">Pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="eb176-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="eb176-272">Turite apibrėžti kiekvieno verslo proceso varianto, kuriam reikalingas automatinis kokybės užsakymų generavimas, kokybės susiejimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-272">You must define a quality associationfor each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="eb176-273">Pavyzdžiui, galima generuoti pirkimo užsakymų, sulaikymo užsakymų, pardavimo užsakymų ir gamybos užsakymų verslo procesų kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="eb176-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb176-274">Testai</span><span class="sxs-lookup"><span data-stu-id="eb176-274">Tests</span></span></td>
<td><span data-ttu-id="eb176-275">Naudokite šį puslapį atskiriems tikrinimams, kuriais nustatoma, ar produktai atitinka kokybės reikalavimus, nustatyti ir peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="eb176-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="eb176-276">Bandymų grupei galite priskirti vieną arba kelis atskirus bandymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="eb176-277">Šiuo atveju taip pat nurodote konkretaus bandymo informaciją, pvz., priimtinas matavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="eb176-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="eb176-278">Matavimo reikšmės naudojamos atliekant kiekybinius bandymus, o bandymų kintamieji naudojami atliekant kokybinius bandymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="eb176-279">Kiekybinio bandymo tipas yra <strong>Sveikasis skaičius</strong> arba <strong>Trupmena</strong> ir taip pat nustatytas jo matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="eb176-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="eb176-280">Kokybės specifikacijos ir bandymų rezultatai išreiškiami skaičiais.</span><span class="sxs-lookup"><span data-stu-id="eb176-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="eb176-281">Kokybinio bandymo tipas yra <strong>Pasirinktinis</strong>.</span><span class="sxs-lookup"><span data-stu-id="eb176-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="eb176-282">Kokybės bandymams reikia pateikti papildomos informacijos apie bandymų kintamąjį, kuris vertinamas ir jo sunumeruotas parinktis.</span><span class="sxs-lookup"><span data-stu-id="eb176-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="eb176-283">Kokybės specifikacijos ir bandymų rezultatai išreiškiami atsižvelgiant į rezultatą.</span><span class="sxs-lookup"><span data-stu-id="eb176-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="eb176-284">Gamybos įmonė atlieka du įsigytų medžiagų bandymus: kiekybinį bandymą dėl medžiagos kokybės ir kokybinį bandymą dėl pakuotės sugadinimo.</span><span class="sxs-lookup"><span data-stu-id="eb176-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="eb176-285">Įmonė nurodo papildomos informacijos, susijusios su kokybės tikrinimu, pateikdama tikrinimo kintamąjį (pažeista pakuotė) ir jo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="eb176-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="eb176-286">Įmonė naudoja <strong>Bandymų grupių</strong> puslapį, kad bandymų grupei priskirtų šiuos du bandymus ir nurodytų konkretaus bandymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb176-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="eb176-287">Tikrinimų grupė priskiriama kokybės užsakymui tam, kad įmonė galėtų pateikti dviejų tikrinimų rezultatų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="eb176-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb176-288">Bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="eb176-288">Test groups</span></span></td>
<td><span data-ttu-id="eb176-289">Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti bandymų grupei priskirtas bandymų grupes bei atskirus bandymus.</span><span class="sxs-lookup"><span data-stu-id="eb176-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="eb176-290">Viršutinėje srityje rodomos tikrinimų grupės, o apatinėje srityje rodomi pasirinktai tikrinimų grupei priskirti tikrinimai.</span><span class="sxs-lookup"><span data-stu-id="eb176-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="eb176-291">Bandymų grupei priskiriate keletą strategijų, pvz., pavyzdžių ėmimo planą, AQL ir ardomojo bandymo reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="eb176-292">Kai bandymų grupei priskiriate atskirą bandymą, apibrėžiate papildomą informaciją, pvz., seką, dokumentus ir galiojimo datas.</span><span class="sxs-lookup"><span data-stu-id="eb176-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="eb176-293">Atliekant kiekybinį bandymą, jūsų apibrėžta informacija taip pat apima priimtinas matavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="eb176-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="eb176-294">Atliekant kokybinį bandymą, informacija apima bandymo kintamąjį ir numatytąjį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="eb176-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="eb176-295">Kokybės užsakymui priskirta bandymų grupė apibrėžia numatytąjį konkrečios prekės bandymų, kuriuos reikia atlikti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="eb176-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="eb176-296">Tačiau kokybės užsakymo bandymus galite pridėti, naikinti arba keisti.</span><span class="sxs-lookup"><span data-stu-id="eb176-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="eb176-297">Pateikiami kiekvieno kokybės užsakymo tikrinimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="eb176-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="eb176-298">Gamybos įmonė apibrėžia kiekvieno kokybės gairių varianto tikrinimų grupę.</span><span class="sxs-lookup"><span data-stu-id="eb176-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="eb176-299">Įvairios bandymų grupės atspindi pavyzdžių ėmimo planų skirtumus, bandymų, kuriuos reikia atlikti vienu metu, rinkinius, AQL ir kitus veiksnius.</span><span class="sxs-lookup"><span data-stu-id="eb176-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="eb176-300">Taip pat skirasi kiekybinių bandymų priimtinos matavimo reikšmės.</span><span class="sxs-lookup"><span data-stu-id="eb176-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="eb176-301">Kad galiotų įmonės kokybės gairės, ji kiekvienai taisyklei priskiria bandymų grupę, kad <strong>Kokybės susiejimų</strong> puslapyje būtų automatiškai generuojami kokybės užsakymai, ir taip pat bandymų grupę priskiria rankiniu būdu sukurtiems kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="eb176-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb176-302">Prekių kokybės grupės</span><span class="sxs-lookup"><span data-stu-id="eb176-302">Item quality groups</span></span></td>
<td><span data-ttu-id="eb176-303">Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti kokybės grupei priskirtas prekes arba kokybės grupes, priskirtas prekei.</span><span class="sxs-lookup"><span data-stu-id="eb176-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="eb176-304">Kokybės grupė nurodo bendruosius prekių tikrinimo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="eb176-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="eb176-305"><strong>Bandymų grupių</strong> puslapyje apibrėžę bandymų reikalavimus, galite apibrėžti taisykles, skirtas automatiškai generuoti kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="eb176-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="eb176-306">Kad procesas būtų paprastesnis, nenustatinėjate taisyklių atskiroms prekėms.</span><span class="sxs-lookup"><span data-stu-id="eb176-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="eb176-307">Vietoj to taisykles apibrėžiate kokybės grupei, naudodami <strong>Kokybės susiejimų</strong> puslapį.</span><span class="sxs-lookup"><span data-stu-id="eb176-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="eb176-308">Taip pat galite naudoti pasirinktos kokybės grupės <strong>Prekių kokybės grupių</strong> puslapį, kad tai grupei priskirtumėte aktualias prekes.</span><span class="sxs-lookup"><span data-stu-id="eb176-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="eb176-309">Taip pat galite naudoti pasirinktos prekės <strong>Prekių kokybės grupių</strong> puslapį, kad tai prekei priskirtumėte aktualias kokybės grupes.</span><span class="sxs-lookup"><span data-stu-id="eb176-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="eb176-310">Gamybos įmonė perka įvairių žaliavų, kurių gaunamų objektų patikrinimo bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="eb176-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="eb176-311">Įmonė apibrėžia kokybės grupę ir tada tai grupei priskiria prekių numerius, susietus su žaliavomis.</span><span class="sxs-lookup"><span data-stu-id="eb176-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="eb176-312">Vėliau įmonė perka naują žaliavos tipą, kurio bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="eb176-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="eb176-313">Užuot nustatydama naujosios medžiagos naujus bandymų reikalavimus, įmonė naujos medžiagos prekės numerį prideda į esamą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="eb176-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="eb176-314">Ta pati gamybos įmonė taip pat gamina prekes, kurių gamybos bandymų reikalavimai tokie patys, ir siunčia prekes, kurių tie patys reikalavimai bandymams prieš siuntimą.</span><span class="sxs-lookup"><span data-stu-id="eb176-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="eb176-315">Įmonė apibrėžia dvi papildomas kokybės grupes ir tada kiekvienai grupei priskiria atitinkamus prekių numerius.</span><span class="sxs-lookup"><span data-stu-id="eb176-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eb176-316">Bandymo kintamieji</span><span class="sxs-lookup"><span data-stu-id="eb176-316">Test variables</span></span></td>
<td><span data-ttu-id="eb176-317">Naudokite šį puslapį, kad apibrėžtumėte ir peržiūrėtumėte kintamuosius, susietus su kokybiniu bandymu.</span><span class="sxs-lookup"><span data-stu-id="eb176-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="eb176-318">Apibrėžiate kiekvieno kintamojo sunumeruotus rezultatus, atitinkančius galimas parinktis.</span><span class="sxs-lookup"><span data-stu-id="eb176-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="eb176-319">Bandymai nustatomi <strong>Bandymų</strong> puslapyje.</span><span class="sxs-lookup"><span data-stu-id="eb176-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="eb176-320">Kokybinių bandymų tipą turite nustatyti į <strong>Parinktis</strong>.</span><span class="sxs-lookup"><span data-stu-id="eb176-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="eb176-321">Naudokite <strong>Bandymų grupių</strong> puslapį, kad atskiram bandymui priskirtumėte bandymo kintamąjį.</span><span class="sxs-lookup"><span data-stu-id="eb176-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="eb176-322">Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą.</span><span class="sxs-lookup"><span data-stu-id="eb176-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="eb176-323">Šis bandymas turi keletą kintamųjų.</span><span class="sxs-lookup"><span data-stu-id="eb176-323">This inspection test has several variables.</span></span> <span data-ttu-id="eb176-324">Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“.</span><span class="sxs-lookup"><span data-stu-id="eb176-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="eb176-325">Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</span><span class="sxs-lookup"><span data-stu-id="eb176-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eb176-326">Bandymo kintamųjų rezultatai</span><span class="sxs-lookup"><span data-stu-id="eb176-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="eb176-327">Naudokite šį puslapį galimiems bandymų kintamojo, susieto su kokybiniu bandymu, bandymų rezultatams nustatyti, redaguoti ir peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="eb176-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="eb176-328">Kiekvienam rezultatui priskiriate <strong>teigiamą</strong> arba <strong>neigiamą</strong> būseną.</span><span class="sxs-lookup"><span data-stu-id="eb176-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="eb176-329">Turite apibrėžti kiekvieno kokybinio bandymo, kuris apibrėžtas puslapyje <strong>Bandymai</strong>, kintamąjį ir jo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="eb176-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="eb176-330">(Kokybinių bandymų tipas puslapyje <strong>Bandymai</strong> nustatytas į <strong>Parinktis</strong>. Naudokite puslapį <strong>Bandymų grupės</strong>, kad atskiram kokybiniam bandymui priskirtumėte bandymų kintamąjį ir numatytąjį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="eb176-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="eb176-331">Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą.</span><span class="sxs-lookup"><span data-stu-id="eb176-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="eb176-332">Šis bandymas turi keletą kintamųjų.</span><span class="sxs-lookup"><span data-stu-id="eb176-332">This inspection test has of several variables.</span></span> <span data-ttu-id="eb176-333">Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“.</span><span class="sxs-lookup"><span data-stu-id="eb176-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="eb176-334">Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</span><span class="sxs-lookup"><span data-stu-id="eb176-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="eb176-335">Kiekvienam rezultatui priskiriama <strong>teigiama</strong> arba <strong>neigiama</strong> būsena.</span><span class="sxs-lookup"><span data-stu-id="eb176-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="eb176-336">Kiekvieno kintamojo tikrinimo metu tikrintojas pateikia tikrinimo rezultatų ataskaitą, joje nurodydamas vieną iš rezultatų.</span><span class="sxs-lookup"><span data-stu-id="eb176-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="eb176-337">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="eb176-337">See also</span></span>
--------

[<span data-ttu-id="eb176-338">Kokybės valdymo procesai</span><span class="sxs-lookup"><span data-stu-id="eb176-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="eb176-339">Neatitikimo valdymo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="eb176-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

