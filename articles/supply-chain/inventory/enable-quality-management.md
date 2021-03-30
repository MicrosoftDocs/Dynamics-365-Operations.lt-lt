---
title: Kokybės valdymo peržiūra
description: Šioje temoje aprašyta, kaip galima naudoti kokybės valdymą „Dynamics 365 Supply Chain Management“, siekiant pagerinti tiekimo grandinės produktų kokybę.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65858838b0fbb245a9330fab4e3b65b36a9eb944
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219370"
---
# <a name="quality-management-overview"></a><span data-ttu-id="06349-103">Kokybės valdymo peržiūra</span><span class="sxs-lookup"><span data-stu-id="06349-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06349-104">Šioje temoje aprašyta, kaip galima naudoti kokybės valdymą „Dynamics 365 Supply Chain Management“, siekiant pagerinti tiekimo grandinės produktų kokybę.</span><span class="sxs-lookup"><span data-stu-id="06349-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="06349-105">Kokybės valdymas gali padėti valdyti apgręžimo laiką tvarkant neatitinkančius produktus, neatsižvelgiant į kilmę.</span><span class="sxs-lookup"><span data-stu-id="06349-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="06349-106">Kadangi diagnostikos tipai yra susiję su koregavimo ataskaitomis, „Supply Chain Management‟ gali planuoti užduotis ir jomis taisyti problemas bei neleisti joms pasikartoti.</span><span class="sxs-lookup"><span data-stu-id="06349-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="06349-107">Be funkcijų, skirtų valdyti neatitikimui, kokybės valdymas apima funkcijas, skirtas problemoms sekti pagal jų tipą (net vidaus problemoms) ir sprendimams identifikuoti kaip trumpalaikiams ar ilgalaikiams.</span><span class="sxs-lookup"><span data-stu-id="06349-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="06349-108">Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnių neatitikimo problemų istoriją ir sprendimus, kurie buvo naudojami joms taisyti.</span><span class="sxs-lookup"><span data-stu-id="06349-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="06349-109">Galite naudoti praeities duomenis ir peržiūrėti ankstesnių kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.</span><span class="sxs-lookup"><span data-stu-id="06349-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="06349-110">Kai nustatote kokybės susiejimą, „Supply Chain Management‟ gali generuoti įvairių verslo procesų, įvykių ir sąlygų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="06349-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="06349-111">Kokybės susiejimas gali apimti konkrečią prekę, konkrečią prekių grupę arba visas prekes.</span><span class="sxs-lookup"><span data-stu-id="06349-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="06349-112">Kokybės valdymo naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="06349-112">Examples of the use of quality management</span></span>
<span data-ttu-id="06349-113">Kokybės valdymas yra lankstus ir gali būti diegiamas įvairiais būdais, siekiant atitikti konkrečių tiekimo grandinės operacijų lygių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="06349-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="06349-114">Toliau pateikti pavyzdžiai iliustruoja galimą šių funkcijų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="06349-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="06349-115">Pagal iš anksto nustatytus kriterijus automatiškai paleisti kokybės kontrolės procesą (sandėlyje registravus pirkimo užsakymą iš konkretaus tiekėjo).</span><span class="sxs-lookup"><span data-stu-id="06349-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="06349-116">Tikrinimo metu blokuoti atsargas, siekiant neleisti naudoti nepatvirtintų atsargų (visiškas pirkimo užsakymų kiekių blokavimas).</span><span class="sxs-lookup"><span data-stu-id="06349-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="06349-117">Kaip kokybės susiejimo dalį naudoti prekių pavyzdžių ėmimą, siekiant apibrėžti dabartinių faktinių atsargų, kurias reikia tikrinti, sumą.</span><span class="sxs-lookup"><span data-stu-id="06349-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="06349-118">Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais, procentine dalimi arba visa numerio lentele.</span><span class="sxs-lookup"><span data-stu-id="06349-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="06349-119">Funkcija _Sandėlio procesų kokybės valdymas_ išplečia kokybės valdymo galimybes.</span><span class="sxs-lookup"><span data-stu-id="06349-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="06349-120">Jei naudojate šią funkciją, žr. [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md) pateiktus pavyzdžius, kaip veikia įgalintas kokybės valdymas.</span><span class="sxs-lookup"><span data-stu-id="06349-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="06349-121">kurkite dalinių kvitų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="06349-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="06349-122">Norėdami kurti kokybės užsakymą, pagrįstą faktiškai su užsakymu gautu kiekiu, formoje **Prekės pavyzdžio ėmimas** turite pažymėti žymės langelį **Pagal atnaujintą kiekį**.</span><span class="sxs-lookup"><span data-stu-id="06349-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="06349-123">Kurti testų tipus, apimančius minimalias, maksimalias ir paskirties testo reikšmes, ir atlikti kokybės–kiekybės tikrinimą su iš anksto nustatytais tikrinimo rezultatais.</span><span class="sxs-lookup"><span data-stu-id="06349-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="06349-124">Nurodyti priimtiną kokybės lygį (AQL), siekiant kontroliuoti leistinus kokybės matavimo nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="06349-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="06349-125">Nurodyti išteklius, kurių reikia tikrinimo operacijai, pvz., tikrinimo sritį ir tikrinimo priemones.</span><span class="sxs-lookup"><span data-stu-id="06349-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="06349-126">Darbas su kokybės susiejimais</span><span class="sxs-lookup"><span data-stu-id="06349-126">Working with quality associations</span></span>
<span data-ttu-id="06349-127">Verslo procesas, kuris naudoja kokybės susiejimą, gali būti susijęs su įvairiais šaltinio dokumentais, pvz., pirkimo užsakymais, pardavimo užsakymais ar gamybos užsakymais.</span><span class="sxs-lookup"><span data-stu-id="06349-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="06349-128">Kiekvienas kokybės susiejimo įrašas apibrėžia bandymų rinkinį, AQL ir pavyzdžių ėmimo planą, kuris taikomas generuojamiems kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="06349-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="06349-129">Turite apibrėžti kiekvieno verslo proceso varianto kokybės susiejimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="06349-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="06349-130">Pavyzdžiui, galite nustatyti kokybės susiejimą, kuris generuoja kokybės užsakymą, kai atnaujinamas pirkimo užsakymo produktų kvitas.</span><span class="sxs-lookup"><span data-stu-id="06349-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="06349-131">Atsižvelgiant į vykdymo plano sąranką, esant atidarytam kokybės užsakymui, gali būti blokuojamas pats paleidimo procesas, arba gali būti blokuojami tolesni procesai, pvz., pirkimo užsakymų SF išrašymas.</span><span class="sxs-lookup"><span data-stu-id="06349-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="06349-132">**Pastaba.** Kol yra atidarytų kokybės užsakymų, automatiškai blokuojamas atsargų kiekių išdavimas.</span><span class="sxs-lookup"><span data-stu-id="06349-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="06349-133">Atsižvelgiant į **Visiško blokavimo** nuostatą **Prekių pavyzdžių** puslapyje, kiekis yra arba kokybės užsakymo kiekis, arba šaltinio dokumento eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="06349-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="06349-134">Nurodyto verslo proceso kokybės susiejimo įrašas identifikuoja įvykį ir sąlygas, kuriems sugeneruotas kokybės užsakymas.</span><span class="sxs-lookup"><span data-stu-id="06349-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="06349-135">Sąlygos gali būti būdingos teritorijai arba juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="06349-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="06349-136">Ardomuosius bandymus apimantis kokybės užsakymas gali būti sugeneruotas tik kai yra turimų įvykio atsargų.</span><span class="sxs-lookup"><span data-stu-id="06349-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="06349-137">Toliau pateikti pavyzdžiai iliustruoja, kaip kokybės susiejimo įrašas apibrėžiamas kiekvieno verslo proceso pokyčiams.</span><span class="sxs-lookup"><span data-stu-id="06349-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="06349-138">Toliau pateiktoje lentelėje apibendrinami kiekvieno pavyzdžio įvykiai ir sąlygos, kuriuos apibrėžia kokybės susiejimo įrašas.</span><span class="sxs-lookup"><span data-stu-id="06349-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="06349-139">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="06349-139">Reference type</span></span></th>
<th><span data-ttu-id="06349-140">Įvykio tipas</span><span class="sxs-lookup"><span data-stu-id="06349-140">Event type</span></span></th>
<th><span data-ttu-id="06349-141">Vykdymas</span><span class="sxs-lookup"><span data-stu-id="06349-141">Execution</span></span></th>
<th><span data-ttu-id="06349-142">Įvykio blokavimas</span><span class="sxs-lookup"><span data-stu-id="06349-142">Event blocking</span></span></th>
<th><span data-ttu-id="06349-143">Dokumento nuoroda</span><span class="sxs-lookup"><span data-stu-id="06349-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="06349-144">Atsargos</span><span class="sxs-lookup"><span data-stu-id="06349-144">Inventory</span></span></td>
<td><span data-ttu-id="06349-145">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="06349-145">Not applicable</span></span></td>
<td><span data-ttu-id="06349-146">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="06349-146">Not applicable</span></span></td>
<td><span data-ttu-id="06349-147">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-147">None</span></span></td>
<td><span data-ttu-id="06349-148">Visi</span><span class="sxs-lookup"><span data-stu-id="06349-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="06349-149">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="06349-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="06349-150">Išrinkimo procesas suplanuotas</span><span class="sxs-lookup"><span data-stu-id="06349-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="06349-151">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-151">Before</span></span></td>
<td><span data-ttu-id="06349-152">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="06349-153">Konkretus ID, Grupė arba tik Viskas.</span><span class="sxs-lookup"><span data-stu-id="06349-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-154">Išrinkimo procesas</span><span class="sxs-lookup"><span data-stu-id="06349-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-155">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="06349-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-156">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06349-157">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="06349-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-158">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-158">Before</span></span></td>
<td><span data-ttu-id="06349-159">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-160">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="06349-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-161">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="06349-162">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="06349-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="06349-163">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="06349-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="06349-164">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-164">Before</span></span></td>
<td><span data-ttu-id="06349-165">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-166">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="06349-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-167">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="06349-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-168">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06349-169">Po</span><span class="sxs-lookup"><span data-stu-id="06349-169">After</span></span></td>
<td><span data-ttu-id="06349-170">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-171">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="06349-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-172">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06349-173">Registracija</span><span class="sxs-lookup"><span data-stu-id="06349-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-174">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="06349-174">Not applicable</span></span></td>
<td><span data-ttu-id="06349-175">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-176">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="06349-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-177">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="06349-178">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="06349-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-179">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-179">Before</span></span></td>
<td><span data-ttu-id="06349-180">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-181">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="06349-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-182">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06349-183">Po</span><span class="sxs-lookup"><span data-stu-id="06349-183">After</span></span></td>
<td><span data-ttu-id="06349-184">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-185">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="06349-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="06349-186">Gamyba</span><span class="sxs-lookup"><span data-stu-id="06349-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-187">Registracija</span><span class="sxs-lookup"><span data-stu-id="06349-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-188">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="06349-188">Not applicable</span></span></td>
<td><span data-ttu-id="06349-189">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="06349-190">Visi</span><span class="sxs-lookup"><span data-stu-id="06349-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-191">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-192">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="06349-193">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-194">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-194">Before</span></span></td>
<td><span data-ttu-id="06349-195">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-196">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-197">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06349-198">Po</span><span class="sxs-lookup"><span data-stu-id="06349-198">After</span></span></td>
<td><span data-ttu-id="06349-199">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-200">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="06349-201">Sulaikymas</span><span class="sxs-lookup"><span data-stu-id="06349-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-202">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="06349-203">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-203">Before</span></span></td>
<td><span data-ttu-id="06349-204">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-205">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-206">Po</span><span class="sxs-lookup"><span data-stu-id="06349-206">After</span></span></td>
<td><span data-ttu-id="06349-207">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-208">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-208">End</span></span></td>
<td><span data-ttu-id="06349-209">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-209">Before</span></span></td>
<td><span data-ttu-id="06349-210">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="06349-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06349-211">Maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="06349-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-212">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="06349-213">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-213">Before</span></span></td>
<td><span data-ttu-id="06349-214">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-215">Konkretus ID, Grupė arba Viskas, ir Konkretaus ištekliaus, Grupė arba Viskas</span><span class="sxs-lookup"><span data-stu-id="06349-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-216">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-217">Po</span><span class="sxs-lookup"><span data-stu-id="06349-217">After</span></span></td>
<td><span data-ttu-id="06349-218">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="06349-219">Sudėtinio produkto gamyba</span><span class="sxs-lookup"><span data-stu-id="06349-219">Co-product production</span></span></td>
<td><span data-ttu-id="06349-220">Registracija</span><span class="sxs-lookup"><span data-stu-id="06349-220">Registration</span></span></td>
<td><span data-ttu-id="06349-221">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="06349-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-222">Nėra</span><span class="sxs-lookup"><span data-stu-id="06349-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="06349-223">Visi</span><span class="sxs-lookup"><span data-stu-id="06349-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="06349-224">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="06349-224">Report as finished</span></span></td>
<td><span data-ttu-id="06349-225">Prieš</span><span class="sxs-lookup"><span data-stu-id="06349-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-226">Po</span><span class="sxs-lookup"><span data-stu-id="06349-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="06349-227">Toliau pateiktoje lentelėje pateikiama daugiau informacijos apie tai, kaip galima generuoti konkrečių tipų procesų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="06349-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="06349-228">Proceso tipas</span><span class="sxs-lookup"><span data-stu-id="06349-228">Type of process</span></span></th>
<th><span data-ttu-id="06349-229">Kai kokybės užsakymus galima generuoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="06349-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="06349-230">Kai kokybės užsakymus galima generuoti, jei reikia ardomojo bandymo.</span><span class="sxs-lookup"><span data-stu-id="06349-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="06349-231">Sąlygų informacija</span><span class="sxs-lookup"><span data-stu-id="06349-231">Condition information</span></span></th>
<th><span data-ttu-id="06349-232">Rankinio generavimo informacija</span><span class="sxs-lookup"><span data-stu-id="06349-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="06349-233">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="06349-233">Purchase order</span></span></td>
<td><span data-ttu-id="06349-234">Prieš užregistruojant kvitų sąrašą arba gautos medžiagos kvitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="06349-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="06349-235">Užregistravus gautos medžiagos kvitą, nes medžiaga turi būti prieinama ardomajam bandymui.</span><span class="sxs-lookup"><span data-stu-id="06349-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="06349-236">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="06349-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="06349-237">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pirkimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-238">Sulaikymo užsakymas</span><span class="sxs-lookup"><span data-stu-id="06349-238">Quarantine order</span></span></td>
<td><span data-ttu-id="06349-239">Prieš sulaikymo užsakymą nurodant baigtu arba po to.</span><span class="sxs-lookup"><span data-stu-id="06349-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="06349-240">Kokybės užsakymų, kuriems reikia atlikti ardomuosius bandymus, generuoti&#39; negalima.</span><span class="sxs-lookup"><span data-stu-id="06349-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="06349-241">Daroma&#39; prielaida, kad sulaikymo užsakymo funkcijos tvarko sunaikintos medžiagos perdavimą.</span><span class="sxs-lookup"><span data-stu-id="06349-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="06349-242">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="06349-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="06349-243">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis sulaikymo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-244">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="06349-244">Sales order</span></span></td>
<td><span data-ttu-id="06349-245">Prieš siunčiamų prekių suplanuotą paėmimo procesą ar važtaraščio naujinimą.</span><span class="sxs-lookup"><span data-stu-id="06349-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="06349-246">Atliekant bet kurį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="06349-246">At any step</span></span></td>
<td><span data-ttu-id="06349-247">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, klientą arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="06349-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="06349-248">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pardavimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-249">Gamybos užsakymas</span><span class="sxs-lookup"><span data-stu-id="06349-249">Production order</span></span></td>
<td><span data-ttu-id="06349-250">Prieš pranešant apie baigtą gamybos užsakymo kiekį, arba po to.</span><span class="sxs-lookup"><span data-stu-id="06349-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="06349-251">Pranešus apie baigtą gamybos užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="06349-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="06349-252">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="06349-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="06349-253">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis gamybos užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-254">Gamybos užsakymas su maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="06349-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="06349-255">Prieš baigiant operacijos ataskaitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="06349-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="06349-256">Pranešus, kad paskutinės operacijos gamyba baigta.</span><span class="sxs-lookup"><span data-stu-id="06349-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="06349-257">Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę ar operacijų išteklių, arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="06349-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="06349-258">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis maršruto operaciją, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="06349-259">Atsargos</span><span class="sxs-lookup"><span data-stu-id="06349-259">Inventory</span></span></td>
<td><span data-ttu-id="06349-260">Kokybės užsakymo negalima automatiškai generuoti atsargų žurnalo operacijai arba perkėlimo užsakymo operacijoms.</span><span class="sxs-lookup"><span data-stu-id="06349-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="06349-261">Prekės&#39; atsargų kiekio kokybės užsakymą reikia kurti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="06349-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="06349-262">Reikia faktiškai turimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="06349-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="06349-263">Kokybės užsakymo automatinio generavimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="06349-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="06349-264">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="06349-264">Purchasing</span></span>

<span data-ttu-id="06349-265">Pirkdami, jei nustatėte lauko **Įvykio tipas** reikšmę **Gavimo dokumentas** ir lauko **Vykdymas** reikšmę **Po**, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="06349-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="06349-266">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė **Taip**, kokybės užsakymas generuojamas kiekvienam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu ir prekės pavyzdžių ėmimo parametrais.</span><span class="sxs-lookup"><span data-stu-id="06349-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="06349-267">Kiekvieną kartą, kai pagal pirkimo užsakymą gaunamas kiekis, remiantis naujai gautu kiekiu generuojami nauji kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="06349-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="06349-268">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė **Ne**, kokybės užsakymas generuojamas pirmajam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="06349-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="06349-269">Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į sekimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="06349-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="06349-270">Kokybės užsakymai negeneruojami vėlesniems kvitams pagal pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="06349-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="06349-271">Gamyba</span><span class="sxs-lookup"><span data-stu-id="06349-271">Production</span></span>

<span data-ttu-id="06349-272">Gamybos aplinkoje, jei nustatėte lauko **Įvykio tipas** reikšmę **Gavimo dokumentas** ir lauko **Skelbti baigtu** reikšmę **Po**, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="06349-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="06349-273">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė **Taip**, kokybės užsakymas generuojamas kiekvienam baigtam kiekiui ir pagal prekės pavyzdžių ėmimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="06349-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="06349-274">Kiekvieną kartą, kai pagal gamybos užsakymą kiekis paskelbiamas baigtu, remiantis naujai baigtu kiekiu generuojami nauji kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="06349-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="06349-275">Ši generavimo logika atitinka pirkimą.</span><span class="sxs-lookup"><span data-stu-id="06349-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="06349-276">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė **Ne**, kokybės užsakymas generuojamas pirmą kartą, kai kiekis paskelbiamas baigtu, remiantis baigtu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="06349-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="06349-277">Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į prekės pavyzdžių ėmimo sekimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="06349-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="06349-278">Kokybės užsakymai negeneruojami vėliau baigtiems kiekiams.</span><span class="sxs-lookup"><span data-stu-id="06349-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="06349-279">Kokybės specifikacija</span><span class="sxs-lookup"><span data-stu-id="06349-279">Quality specification</span></span></th>
<th><span data-ttu-id="06349-280">Pagal atnaujintą kiekį</span><span class="sxs-lookup"><span data-stu-id="06349-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="06349-281">Pagal sekimo dimensiją</span><span class="sxs-lookup"><span data-stu-id="06349-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="06349-282">Rezultatas</span><span class="sxs-lookup"><span data-stu-id="06349-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="06349-283">Procentinė reikšmė: 10 %</span><span class="sxs-lookup"><span data-stu-id="06349-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="06349-284">Taip</span><span class="sxs-lookup"><span data-stu-id="06349-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="06349-285">Paketo numeris: ne</span><span class="sxs-lookup"><span data-stu-id="06349-285">Batch number: No</span></span></p>
<p><span data-ttu-id="06349-286">Serijos numeris: ne</span><span class="sxs-lookup"><span data-stu-id="06349-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="06349-287">Užsakymo kiekis: 100</span><span class="sxs-lookup"><span data-stu-id="06349-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="06349-288">Paskelbti kaip baigtą 30</span><span class="sxs-lookup"><span data-stu-id="06349-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="06349-289">Kokybės užsakymas #1, skirtas 3 (10 % iš 30)</span><span class="sxs-lookup"><span data-stu-id="06349-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="06349-290">Paskelbti kaip baigtą 70</span><span class="sxs-lookup"><span data-stu-id="06349-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="06349-291">Kokybės užsakymas #2, skirtas 7 (10 % likusio užsakymo kiekio, kuris šiuo atveju yra lygus 70)</span><span class="sxs-lookup"><span data-stu-id="06349-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="06349-292">Fiksuotas kiekis: 1</span><span class="sxs-lookup"><span data-stu-id="06349-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="06349-293">Ne</span><span class="sxs-lookup"><span data-stu-id="06349-293">No</span></span></td>
<td>
<p><span data-ttu-id="06349-294">Paketo numeris: ne</span><span class="sxs-lookup"><span data-stu-id="06349-294">Batch number: No</span></span></p>
<p><span data-ttu-id="06349-295">Serijos numeris: ne</span><span class="sxs-lookup"><span data-stu-id="06349-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="06349-296">Užsakymo kiekis: 100</span><span class="sxs-lookup"><span data-stu-id="06349-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="06349-297">Paskelbti kaip baigtą 30</span><span class="sxs-lookup"><span data-stu-id="06349-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="06349-298">Kokybės užsakymas #1, skirtas 1 (pirmajam paskelbtam baigtu kiekiui, kuris turi 1 fiksuotą vertę)</span><span class="sxs-lookup"><span data-stu-id="06349-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="06349-299">Kokybės užsakymas #2, skirtas 1 (likusiam kiekiui, kuris vis dar turi 1 fiksuotą vertę)</span><span class="sxs-lookup"><span data-stu-id="06349-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="06349-300">Paskelbti kaip baigtą 10</span><span class="sxs-lookup"><span data-stu-id="06349-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="06349-301">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="06349-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="06349-302">Paskelbti kaip baigtą 60</span><span class="sxs-lookup"><span data-stu-id="06349-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="06349-303">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="06349-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="06349-304">Fiksuotas kiekis: 1</span><span class="sxs-lookup"><span data-stu-id="06349-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="06349-305">Taip</span><span class="sxs-lookup"><span data-stu-id="06349-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="06349-306">Paketo numeris: taip</span><span class="sxs-lookup"><span data-stu-id="06349-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="06349-307">Serijos numeris: taip</span><span class="sxs-lookup"><span data-stu-id="06349-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="06349-308">Užsakymo kiekis: 10</span><span class="sxs-lookup"><span data-stu-id="06349-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="06349-309">Paskelbti kaip baigtą 3: 1, skirta #b1, #s1; 1, skirta #b2, #s2; 1, skirta #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="06349-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="06349-310">Kokybės užsakymas #1, skirtas 1, paketo #b1, serijos #s1</span><span class="sxs-lookup"><span data-stu-id="06349-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="06349-311">Kokybės užsakymas #2, skirtas 1, paketo #b2, serijos #s2</span><span class="sxs-lookup"><span data-stu-id="06349-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="06349-312">Kokybės užsakymas #3, skirtas 1, paketo #b3, serijos #s3</span><span class="sxs-lookup"><span data-stu-id="06349-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="06349-313">Paskelbti kaip baitą 2: 1, skirta #b4, #s4; 1, skirta #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="06349-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="06349-314">Kokybės užsakymas #4, skirtas 1, paketo #b4, serijos #s4</span><span class="sxs-lookup"><span data-stu-id="06349-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="06349-315">Kokybės užsakymas #5, skirtas 1, paketo #b5, serijos #s5</span><span class="sxs-lookup"><span data-stu-id="06349-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="06349-316"><strong>Pastaba:</strong> paketą galima naudoti pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="06349-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="06349-317">Fiksuotas kiekis: 2</span><span class="sxs-lookup"><span data-stu-id="06349-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="06349-318">Ne</span><span class="sxs-lookup"><span data-stu-id="06349-318">No</span></span></td>
<td>
<p><span data-ttu-id="06349-319">Paketo numeris: taip</span><span class="sxs-lookup"><span data-stu-id="06349-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="06349-320">Serijos numeris: taip</span><span class="sxs-lookup"><span data-stu-id="06349-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="06349-321">Užsakymo kiekis: 10</span><span class="sxs-lookup"><span data-stu-id="06349-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="06349-322">Paskelbti kaip baigtą 4: 1, skirta #b1, #s1; 1, skirta #b2, #s2; 1, skirta #b3, #s3; 1, skirta #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="06349-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="06349-323">Kokybės užsakymas #1, skirtas 1, paketo #b1, serijos #s1</span><span class="sxs-lookup"><span data-stu-id="06349-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="06349-324">Kokybės užsakymas #2, skirtas 1, paketo #b2, serijos #s2</span><span class="sxs-lookup"><span data-stu-id="06349-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="06349-325">Kokybės užsakymas #3, skirtas 1, paketo #b3, serijos #s3</span><span class="sxs-lookup"><span data-stu-id="06349-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="06349-326">Kokybės užsakymas #4, skirtas 1, paketo #b4, serijos #s4</span><span class="sxs-lookup"><span data-stu-id="06349-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="06349-327">Kokybės užsakymas #5, skirtas 2, be nuorodos į paketą ir serijos numerį</span><span class="sxs-lookup"><span data-stu-id="06349-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="06349-328">Paskelbti kaip baigtą 6: 1, skirta #b5, #s5, 1, skirta #b6, #s6; 1, skirta #b7, #s7; 1, skirta #b8, #s8; 1, skirta #b9, #s9; 1, skirta #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="06349-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="06349-329">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="06349-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="06349-330">Funkcija *Sandėlio procesų kokybės valdymas* įtraukia kokybės užsakymų apdorojimo galimybių, skirtų gamybai, kai **Įvykio tipas** nustatytas į *Skelbti baigtu* ir **Vykdymas** nustatytas į *Po*, ir pirkimui, kai **Įvykio tipas** nustatytas į *Registracija*.</span><span class="sxs-lookup"><span data-stu-id="06349-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="06349-331">Daugiau informacijos rasite dalyje [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="06349-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="06349-332">Kokybės valdymo puslapiai</span><span class="sxs-lookup"><span data-stu-id="06349-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06349-333">Puslapis</span><span class="sxs-lookup"><span data-stu-id="06349-333">Page</span></span></th>
<th><span data-ttu-id="06349-334">aprašymas</span><span class="sxs-lookup"><span data-stu-id="06349-334">Description</span></span></th>
<th><span data-ttu-id="06349-335">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="06349-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06349-336">Kokybės susiejimai</span><span class="sxs-lookup"><span data-stu-id="06349-336">Quality associations</span></span></td>
<td><span data-ttu-id="06349-337">Žr. ankstesnius šio straipsnio skyrius.</span><span class="sxs-lookup"><span data-stu-id="06349-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="06349-338">Kokybės susiejimas apibrėžia visą toliau nurodytą generuojamo kokybės užsakymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="06349-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="06349-339">Operacijos įvykį.</span><span class="sxs-lookup"><span data-stu-id="06349-339">The transaction event</span></span></li>
<li><span data-ttu-id="06349-340">Prekių bandymų, kuriuos reikia atlikti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="06349-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="06349-341">AQL.</span><span class="sxs-lookup"><span data-stu-id="06349-341">The AQL</span></span></li>
<li><span data-ttu-id="06349-342">Pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="06349-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="06349-343">Turite apibrėžti kiekvieno verslo proceso varianto, kuriam reikalingas automatinis kokybės užsakymų generavimas, kokybės susiejimą.</span><span class="sxs-lookup"><span data-stu-id="06349-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="06349-344">Pavyzdžiui, galima generuoti pirkimo užsakymų, sulaikymo užsakymų, pardavimo užsakymų ir gamybos užsakymų verslo procesų kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="06349-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06349-345">Testai</span><span class="sxs-lookup"><span data-stu-id="06349-345">Tests</span></span></td>
<td><span data-ttu-id="06349-346">Naudokite šį puslapį atskiriems tikrinimams, kuriais nustatoma, ar produktai atitinka kokybės reikalavimus, nustatyti ir peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="06349-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="06349-347">Bandymų grupei galite priskirti vieną arba kelis atskirus bandymus.</span><span class="sxs-lookup"><span data-stu-id="06349-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="06349-348">Šiuo atveju taip pat nurodote konkretaus bandymo informaciją, pvz., priimtinas matavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="06349-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="06349-349">Matavimo reikšmės naudojamos atliekant kiekybinius bandymus, o bandymų kintamieji naudojami atliekant kokybinius bandymus.</span><span class="sxs-lookup"><span data-stu-id="06349-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="06349-350">Kiekybinio bandymo tipas yra <strong>Sveikasis skaičius</strong> arba <strong>Trupmena</strong> ir taip pat nustatytas jo matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="06349-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="06349-351">Kokybės specifikacijos ir bandymų rezultatai išreiškiami skaičiais.</span><span class="sxs-lookup"><span data-stu-id="06349-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="06349-352">Kokybinio bandymo tipas yra <strong>Pasirinktinis</strong>.</span><span class="sxs-lookup"><span data-stu-id="06349-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="06349-353">Kokybės bandymams reikia pateikti papildomos informacijos apie bandymų kintamąjį, kuris vertinamas ir jo sunumeruotas parinktis.</span><span class="sxs-lookup"><span data-stu-id="06349-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="06349-354">Kokybės specifikacijos ir bandymų rezultatai išreiškiami atsižvelgiant į rezultatą.</span><span class="sxs-lookup"><span data-stu-id="06349-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="06349-355">Gamybos įmonė atlieka du įsigytų medžiagų bandymus: kiekybinį bandymą dėl medžiagos kokybės ir kokybinį bandymą dėl pakuotės sugadinimo.</span><span class="sxs-lookup"><span data-stu-id="06349-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="06349-356">Įmonė nurodo papildomos informacijos, susijusios su kokybės tikrinimu, pateikdama tikrinimo kintamąjį (pažeista pakuotė) ir jo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="06349-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="06349-357">Įmonė naudoja <strong>Bandymų grupių</strong> puslapį, kad bandymų grupei priskirtų šiuos du bandymus ir nurodytų konkretaus bandymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="06349-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="06349-358">Tikrinimų grupė priskiriama kokybės užsakymui tam, kad įmonė galėtų pateikti dviejų tikrinimų rezultatų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="06349-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06349-359">Bandymo grupės</span><span class="sxs-lookup"><span data-stu-id="06349-359">Test groups</span></span></td>
<td><span data-ttu-id="06349-360">Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti bandymų grupei priskirtas bandymų grupes bei atskirus bandymus.</span><span class="sxs-lookup"><span data-stu-id="06349-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="06349-361">Viršutinėje srityje rodomos tikrinimų grupės, o apatinėje srityje rodomi pasirinktai tikrinimų grupei priskirti tikrinimai.</span><span class="sxs-lookup"><span data-stu-id="06349-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="06349-362">Bandymų grupei priskiriate keletą strategijų, pvz., pavyzdžių ėmimo planą, AQL ir ardomojo bandymo reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="06349-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="06349-363">Kai bandymų grupei priskiriate atskirą bandymą, apibrėžiate papildomą informaciją, pvz., seką, dokumentus ir galiojimo datas.</span><span class="sxs-lookup"><span data-stu-id="06349-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="06349-364">Atliekant kiekybinį bandymą, jūsų apibrėžta informacija taip pat apima priimtinas matavimo reikšmes.</span><span class="sxs-lookup"><span data-stu-id="06349-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="06349-365">Atliekant kokybinį bandymą, informacija apima bandymo kintamąjį ir numatytąjį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="06349-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="06349-366">Kokybės užsakymui priskirta bandymų grupė apibrėžia numatytąjį konkrečios prekės bandymų, kuriuos reikia atlikti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="06349-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="06349-367">Tačiau kokybės užsakymo bandymus galite pridėti, naikinti arba keisti.</span><span class="sxs-lookup"><span data-stu-id="06349-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="06349-368">Pateikiami kiekvieno kokybės užsakymo tikrinimo rezultatai.</span><span class="sxs-lookup"><span data-stu-id="06349-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="06349-369">Gamybos įmonė apibrėžia kiekvieno kokybės gairių varianto tikrinimų grupę.</span><span class="sxs-lookup"><span data-stu-id="06349-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="06349-370">Įvairios bandymų grupės atspindi pavyzdžių ėmimo planų skirtumus, bandymų, kuriuos reikia atlikti vienu metu, rinkinius, AQL ir kitus veiksnius.</span><span class="sxs-lookup"><span data-stu-id="06349-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="06349-371">Taip pat skirasi kiekybinių bandymų priimtinos matavimo reikšmės.</span><span class="sxs-lookup"><span data-stu-id="06349-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="06349-372">Kad galiotų įmonės kokybės gairės, ji kiekvienai taisyklei priskiria bandymų grupę, kad <strong>Kokybės susiejimų</strong> puslapyje būtų automatiškai generuojami kokybės užsakymai, ir taip pat bandymų grupę priskiria rankiniu būdu sukurtiems kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="06349-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06349-373">Prekių kokybės grupės</span><span class="sxs-lookup"><span data-stu-id="06349-373">Item quality groups</span></span></td>
<td><span data-ttu-id="06349-374">Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti kokybės grupei priskirtas prekes arba kokybės grupes, priskirtas prekei.</span><span class="sxs-lookup"><span data-stu-id="06349-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="06349-375">Kokybės grupė nurodo bendruosius prekių tikrinimo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="06349-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="06349-376"><strong>Bandymų grupių</strong> puslapyje apibrėžę bandymų reikalavimus, galite apibrėžti taisykles, skirtas automatiškai generuoti kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="06349-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="06349-377">Kad procesas būtų paprastesnis, nenustatinėjate&#39; taisyklių atskiroms prekėms.</span><span class="sxs-lookup"><span data-stu-id="06349-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="06349-378">Vietoj to taisykles apibrėžiate kokybės grupei, naudodami <strong>Kokybės susiejimų</strong> puslapį.</span><span class="sxs-lookup"><span data-stu-id="06349-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="06349-379">Taip pat galite naudoti pasirinktos kokybės grupės <strong>Prekių kokybės grupių</strong> puslapį, kad tai grupei priskirtumėte aktualias prekes.</span><span class="sxs-lookup"><span data-stu-id="06349-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="06349-380">Taip pat galite naudoti pasirinktos prekės <strong>Prekių kokybės grupių</strong> puslapį, kad tai prekei priskirtumėte aktualias kokybės grupes.</span><span class="sxs-lookup"><span data-stu-id="06349-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="06349-381">Gamybos įmonė perka įvairių žaliavų, kurių gaunamų objektų patikrinimo bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="06349-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="06349-382">Įmonė apibrėžia kokybės grupę ir tada tai grupei priskiria prekių numerius, susietus su žaliavomis.</span><span class="sxs-lookup"><span data-stu-id="06349-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="06349-383">Vėliau įmonė perka naują žaliavos tipą, kurio bandymų reikalavimai tokie patys.</span><span class="sxs-lookup"><span data-stu-id="06349-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="06349-384">Užuot nustatydama naujosios medžiagos naujus bandymų reikalavimus, įmonė naujos medžiagos prekės numerį prideda į esamą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="06349-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="06349-385">Ta pati gamybos įmonė taip pat gamina prekes, kurių gamybos bandymų reikalavimai tokie patys, ir siunčia prekes, kurių tie patys reikalavimai bandymams prieš siuntimą.</span><span class="sxs-lookup"><span data-stu-id="06349-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="06349-386">Įmonė apibrėžia dvi papildomas kokybės grupes ir tada kiekvienai grupei priskiria atitinkamus prekių numerius.</span><span class="sxs-lookup"><span data-stu-id="06349-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06349-387">Bandymo kintamieji</span><span class="sxs-lookup"><span data-stu-id="06349-387">Test variables</span></span></td>
<td><span data-ttu-id="06349-388">Naudokite šį puslapį, kad apibrėžtumėte ir peržiūrėtumėte kintamuosius, susietus su kokybiniu bandymu.</span><span class="sxs-lookup"><span data-stu-id="06349-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="06349-389">Apibrėžiate kiekvieno kintamojo sunumeruotus rezultatus, atitinkančius galimas parinktis.</span><span class="sxs-lookup"><span data-stu-id="06349-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="06349-390">Bandymai nustatomi <strong>Bandymų</strong> puslapyje.</span><span class="sxs-lookup"><span data-stu-id="06349-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="06349-391">Kokybinių bandymų tipą turite nustatyti į <strong>Parinktis</strong>.</span><span class="sxs-lookup"><span data-stu-id="06349-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="06349-392">Naudokite <strong>Bandymų grupių</strong> puslapį, kad atskiram bandymui priskirtumėte bandymo kintamąjį.</span><span class="sxs-lookup"><span data-stu-id="06349-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="06349-393">Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą.</span><span class="sxs-lookup"><span data-stu-id="06349-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="06349-394">Šis bandymas turi keletą kintamųjų.</span><span class="sxs-lookup"><span data-stu-id="06349-394">This inspection test has several variables.</span></span> <span data-ttu-id="06349-395">Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“.</span><span class="sxs-lookup"><span data-stu-id="06349-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="06349-396">Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</span><span class="sxs-lookup"><span data-stu-id="06349-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06349-397">Bandymo kintamųjų rezultatai</span><span class="sxs-lookup"><span data-stu-id="06349-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="06349-398">Naudokite šį puslapį galimiems bandymų kintamojo, susieto su kokybiniu bandymu, bandymų rezultatams nustatyti, redaguoti ir peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="06349-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="06349-399">Kiekvienam rezultatui priskiriate <strong>teigiamą</strong> arba <strong>neigiamą</strong> būseną.</span><span class="sxs-lookup"><span data-stu-id="06349-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="06349-400">Turite apibrėžti kiekvieno kokybinio bandymo, kuris apibrėžtas puslapyje <strong>Bandymai</strong>, kintamąjį ir jo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="06349-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="06349-401">(Kokybinių bandymų tipas puslapyje <strong>Bandymai</strong> nustatytas į <strong>Parinktis</strong>). Naudokite puslapį <strong>Bandymų grupės</strong>, kad atskiram kokybiniam bandymui priskirtumėte bandymų kintamąjį ir numatytąjį rezultatą.</span><span class="sxs-lookup"><span data-stu-id="06349-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="06349-402">Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą.</span><span class="sxs-lookup"><span data-stu-id="06349-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="06349-403">Šis bandymas turi keletą kintamųjų.</span><span class="sxs-lookup"><span data-stu-id="06349-403">This inspection test has of several variables.</span></span> <span data-ttu-id="06349-404">Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“.</span><span class="sxs-lookup"><span data-stu-id="06349-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="06349-405">Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</span><span class="sxs-lookup"><span data-stu-id="06349-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="06349-406">Kiekvienam rezultatui priskiriama <strong>teigiama</strong> arba <strong>neigiama</strong> būsena.</span><span class="sxs-lookup"><span data-stu-id="06349-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="06349-407">Kiekvieno kintamojo tikrinimo metu tikrintojas pateikia tikrinimo rezultatų ataskaitą, joje nurodydamas vieną iš rezultatų.</span><span class="sxs-lookup"><span data-stu-id="06349-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="06349-408">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="06349-408">Additional resources</span></span>
--------

[<span data-ttu-id="06349-409">Kokybės valdymo procesai</span><span class="sxs-lookup"><span data-stu-id="06349-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="06349-410">Neatitikimo valdymas</span><span class="sxs-lookup"><span data-stu-id="06349-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="06349-411">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="06349-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]