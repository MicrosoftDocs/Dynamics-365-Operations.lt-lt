---
title: Kokybės susiejimai
description: Šioje temoje aprašoma, kaip galite naudoti kokybės susiejimus, norėdami automatiškai generuoti kokybės užsakymus, susijusius su jūsų „Microsoft Dynamics 365 Supply Chain Management“ pardavimo, pirkimo ir gamybos procesais.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956756"
---
# <a name="quality-associations"></a><span data-ttu-id="be177-103">Kokybės susiejimai</span><span class="sxs-lookup"><span data-stu-id="be177-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be177-104">Šioje temoje aprašoma, kaip galite naudoti kokybės susiejimus, norėdami automatiškai generuoti kokybės užsakymus, susijusius su jūsų „Microsoft Dynamics 365 Supply Chain Management“ pardavimo, pirkimo ir gamybos procesais.</span><span class="sxs-lookup"><span data-stu-id="be177-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="be177-105">Kokybės susiejimas apibrėžia visą toliau nurodytą generuojamo kokybės užsakymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="be177-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="be177-106">Operacijos įvykį.</span><span class="sxs-lookup"><span data-stu-id="be177-106">The transaction event</span></span>
- <span data-ttu-id="be177-107">Prekių bandymų, kuriuos reikia atlikti, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="be177-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="be177-108">Priimamas kokybės lygmuo (AQL)</span><span class="sxs-lookup"><span data-stu-id="be177-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="be177-109">Pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-109">The sampling plan</span></span>

<span data-ttu-id="be177-110">Turite apibrėžti kiekvieno verslo proceso varianto, kuriam reikalingas automatinis kokybės užsakymų generavimas, kokybės susiejimą.</span><span class="sxs-lookup"><span data-stu-id="be177-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="be177-111">Pavyzdžiui, galima generuoti pirkimo užsakymų, sulaikymo užsakymų, pardavimo užsakymų ir gamybos užsakymų verslo procesų kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="be177-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="be177-112">Darbas su kokybės susiejimais</span><span class="sxs-lookup"><span data-stu-id="be177-112">Working with quality associations</span></span>

<span data-ttu-id="be177-113">Verslo procesas, kuris naudoja kokybės susiejimą, gali būti susijęs su įvairiais šaltinio dokumentais, pvz., pirkimo užsakymais, pardavimo užsakymais ar gamybos užsakymais.</span><span class="sxs-lookup"><span data-stu-id="be177-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="be177-114">Kiekvienas kokybės susiejimo įrašas apibrėžia bandymų rinkinį, AQL ir pavyzdžių ėmimo planą, kuris taikomas generuojamiems kokybės užsakymams.</span><span class="sxs-lookup"><span data-stu-id="be177-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="be177-115">Turite apibrėžti kiekvieno verslo proceso varianto kokybės susiejimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="be177-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="be177-116">Pavyzdžiui, galite nustatyti kokybės susiejimą, kuris generuoja kokybės užsakymą, kai atnaujinamas pirkimo užsakymo produktų kvitas.</span><span class="sxs-lookup"><span data-stu-id="be177-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="be177-117">Atsižvelgiant į vykdymo plano nustatymą, kol yra atviras kokybės užsakymas, paleidimo procesas gali būti užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="be177-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="be177-118">Kitu atveju vėlesni procesai, pavyzdžiui, pirkimo užsakymų SF išrašymas, gali būti užblokuoti.</span><span class="sxs-lookup"><span data-stu-id="be177-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="be177-119">Kol yra atidarytų kokybės užsakymų, automatiškai blokuojamas atsargų kiekių išdavimas.</span><span class="sxs-lookup"><span data-stu-id="be177-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="be177-120">Atsižvelgiant į **Visiško blokavimo** laukelio nustatymus **Prekių pavyzdžių** puslapyje, kiekis yra arba kokybės užsakymo kiekis, arba šaltinio dokumento eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="be177-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="be177-121">Daugiau informacijos ieškokite Kokybės [prekės bandymo valdymo tikrinimo](quality-item-sampling.md) priemonės.</span><span class="sxs-lookup"><span data-stu-id="be177-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="be177-122">Nurodyto verslo proceso kokybės susiejimo įrašas identifikuoja įvykį ir sąlygas, kuriems sugeneruotas kokybės užsakymas.</span><span class="sxs-lookup"><span data-stu-id="be177-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="be177-123">Sąlygos gali būti būdingos teritorijai arba juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="be177-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="be177-124">Ardomuosius bandymus apimantis kokybės užsakymas gali būti sugeneruotas tik kai yra turimų įvykio atsargų.</span><span class="sxs-lookup"><span data-stu-id="be177-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="be177-125">Norėdami dirbti su kokybės susiejimais, **eikite į Atsargų valdymo \> nustatymo kokybės kontrolės \> kokybės \>susiejimus**.</span><span class="sxs-lookup"><span data-stu-id="be177-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="be177-126">Toliau pateikti pavyzdžiai rodo, kaip kokybės susiejimo įrašas apibrėžiamas kiekvieno verslo proceso pokyčiams.</span><span class="sxs-lookup"><span data-stu-id="be177-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="be177-127">Toliau pateiktoje lentelėje apibendrinami kiekvieno pavyzdžio įvykiai ir sąlygos, kuriuos apibrėžia kokybės susiejimo įrašas.</span><span class="sxs-lookup"><span data-stu-id="be177-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be177-128">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="be177-128">Reference type</span></span></th>
<th><span data-ttu-id="be177-129">Įvykio tipas</span><span class="sxs-lookup"><span data-stu-id="be177-129">Event type</span></span></th>
<th><span data-ttu-id="be177-130">Vykdymas</span><span class="sxs-lookup"><span data-stu-id="be177-130">Execution</span></span></th>
<th><span data-ttu-id="be177-131">Įvykio blokavimas</span><span class="sxs-lookup"><span data-stu-id="be177-131">Event blocking</span></span></th>
<th><span data-ttu-id="be177-132">Dokumento nuoroda</span><span class="sxs-lookup"><span data-stu-id="be177-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be177-133">Atsargos</span><span class="sxs-lookup"><span data-stu-id="be177-133">Inventory</span></span></td>
<td><span data-ttu-id="be177-134">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="be177-134">Not applicable</span></span></td>
<td><span data-ttu-id="be177-135">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="be177-135">Not applicable</span></span></td>
<td><span data-ttu-id="be177-136">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-136">None</span></span></td>
<td><span data-ttu-id="be177-137">Visi</span><span class="sxs-lookup"><span data-stu-id="be177-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="be177-138">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="be177-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="be177-139">Išrinkimo procesas suplanuotas</span><span class="sxs-lookup"><span data-stu-id="be177-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="be177-140">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-140">Before</span></span></td>
<td><span data-ttu-id="be177-141">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="be177-142">Konkretus ID, Grupė arba tik Viskas.</span><span class="sxs-lookup"><span data-stu-id="be177-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-143">Išrinkimo procesas</span><span class="sxs-lookup"><span data-stu-id="be177-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-144">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="be177-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-145">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be177-146">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="be177-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-147">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-147">Before</span></span></td>
<td><span data-ttu-id="be177-148">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-149">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="be177-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-150">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="be177-151">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="be177-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="be177-152">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="be177-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="be177-153">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-153">Before</span></span></td>
<td><span data-ttu-id="be177-154">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-155">Kvitų sąrašas</span><span class="sxs-lookup"><span data-stu-id="be177-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-156">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="be177-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-157">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be177-158">Po</span><span class="sxs-lookup"><span data-stu-id="be177-158">After</span></span></td>
<td><span data-ttu-id="be177-159">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-160">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="be177-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-161">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be177-162">Registracija</span><span class="sxs-lookup"><span data-stu-id="be177-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-163">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="be177-163">Not applicable</span></span></td>
<td><span data-ttu-id="be177-164">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-165">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="be177-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-166">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="be177-167">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="be177-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-168">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-168">Before</span></span></td>
<td><span data-ttu-id="be177-169">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-170">Gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="be177-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-171">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be177-172">Po</span><span class="sxs-lookup"><span data-stu-id="be177-172">After</span></span></td>
<td><span data-ttu-id="be177-173">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-174">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="be177-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="be177-175">Gamyba</span><span class="sxs-lookup"><span data-stu-id="be177-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-176">Registracija</span><span class="sxs-lookup"><span data-stu-id="be177-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-177">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="be177-177">Not applicable</span></span></td>
<td><span data-ttu-id="be177-178">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="be177-179">Visi</span><span class="sxs-lookup"><span data-stu-id="be177-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-180">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="be177-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-181">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="be177-182">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="be177-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-183">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-183">Before</span></span></td>
<td><span data-ttu-id="be177-184">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-185">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="be177-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-186">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be177-187">Po</span><span class="sxs-lookup"><span data-stu-id="be177-187">After</span></span></td>
<td><span data-ttu-id="be177-188">Nėra</span><span class="sxs-lookup"><span data-stu-id="be177-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-189">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="be177-190">Sulaikymas</span><span class="sxs-lookup"><span data-stu-id="be177-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-191">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="be177-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="be177-192">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-192">Before</span></span></td>
<td><span data-ttu-id="be177-193">Pranešti apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="be177-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-194">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-195">Po</span><span class="sxs-lookup"><span data-stu-id="be177-195">After</span></span></td>
<td><span data-ttu-id="be177-196">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-197">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-197">End</span></span></td>
<td><span data-ttu-id="be177-198">Prieš</span><span class="sxs-lookup"><span data-stu-id="be177-198">Before</span></span></td>
<td><span data-ttu-id="be177-199">Pabaigti</span><span class="sxs-lookup"><span data-stu-id="be177-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be177-200">Maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="be177-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-201">Skelbti baigtu</span><span class="sxs-lookup"><span data-stu-id="be177-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="be177-202">Iki</span><span class="sxs-lookup"><span data-stu-id="be177-202">Before</span></span></td>
<td><span data-ttu-id="be177-203">None</span><span class="sxs-lookup"><span data-stu-id="be177-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-204">Konkretus ID, Grupė arba Viskas, ir Konkretaus išteklių Grupė arba Viskas</span><span class="sxs-lookup"><span data-stu-id="be177-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-205">Skelbti baigtu</span><span class="sxs-lookup"><span data-stu-id="be177-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-206">Po</span><span class="sxs-lookup"><span data-stu-id="be177-206">After</span></span></td>
<td><span data-ttu-id="be177-207">None</span><span class="sxs-lookup"><span data-stu-id="be177-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="be177-208">Sudėtinio produkto gamyba</span><span class="sxs-lookup"><span data-stu-id="be177-208">Co-product production</span></span></td>
<td><span data-ttu-id="be177-209">Registracija</span><span class="sxs-lookup"><span data-stu-id="be177-209">Registration</span></span></td>
<td><span data-ttu-id="be177-210">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="be177-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-211">None</span><span class="sxs-lookup"><span data-stu-id="be177-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="be177-212">Visos</span><span class="sxs-lookup"><span data-stu-id="be177-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="be177-213">Skelbti baigtu</span><span class="sxs-lookup"><span data-stu-id="be177-213">Report as finished</span></span></td>
<td><span data-ttu-id="be177-214">Iki</span><span class="sxs-lookup"><span data-stu-id="be177-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-215">Po</span><span class="sxs-lookup"><span data-stu-id="be177-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="be177-216">Funkcija *Sandėlio procesų kokybės valdymas* įtraukia kokybės užsakymų apdorojimo galimybių, skirtų gamybai, kuriame **Įvykio tipas** nustatytas į *Skelbti baigtu* laukelį ir **Vykdymas** nustatytas į *Po* laukelį ir pirkimui, kai **Įvykio tipas** nustatytas į *Registracija*.</span><span class="sxs-lookup"><span data-stu-id="be177-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="be177-217">Dėl platesnės informacijos, žr. [Kokybės valdymas sandėlio apdorojimams](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="be177-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="be177-218">Toliau pateiktoje lentelėje pateikiama daugiau informacijos apie tai, kaip galima generuoti konkrečių tipų procesų kokybės užsakymus.</span><span class="sxs-lookup"><span data-stu-id="be177-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="be177-219">Proceso tipas</span><span class="sxs-lookup"><span data-stu-id="be177-219">Type of process</span></span></th>
<th><span data-ttu-id="be177-220">Kai kokybės užsakymus galima generuoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="be177-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="be177-221">Kai kokybės užsakymus galima generuoti, jei reikia ardomojo bandymo.</span><span class="sxs-lookup"><span data-stu-id="be177-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="be177-222">Sąlygų informacija</span><span class="sxs-lookup"><span data-stu-id="be177-222">Condition information</span></span></th>
<th><span data-ttu-id="be177-223">Rankinio generavimo informacija</span><span class="sxs-lookup"><span data-stu-id="be177-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be177-224">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="be177-224">Purchase order</span></span></td>
<td><span data-ttu-id="be177-225">Prieš užregistruojant kvitų sąrašą arba gautos medžiagos kvitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="be177-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="be177-226">Užregistravus gautos medžiagos kvitą, nes medžiaga turi būti prieinama ardomajam bandymui.</span><span class="sxs-lookup"><span data-stu-id="be177-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="be177-227">Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="be177-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="be177-228">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pirkimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-229">Sulaikymo užsakymas</span><span class="sxs-lookup"><span data-stu-id="be177-229">Quarantine order</span></span></td>
<td><span data-ttu-id="be177-230">Prieš sulaikymo užsakymą nurodant baigtu arba po to.</span><span class="sxs-lookup"><span data-stu-id="be177-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="be177-231">Kokybės užsakymų, kuriems reikia atlikti ardomuosius bandymus, generuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="be177-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="be177-232">Daroma prielaida, kad sulaikymo užsakymo funkcijos tvarko sunaikintos medžiagos perdavimą.</span><span class="sxs-lookup"><span data-stu-id="be177-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="be177-233">Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="be177-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="be177-234">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis sulaikymo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-235">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="be177-235">Sales order</span></span></td>
<td><span data-ttu-id="be177-236">Prieš siunčiamų prekių suplanuotą paėmimo procesą ar važtaraščio naujinimą.</span><span class="sxs-lookup"><span data-stu-id="be177-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="be177-237">Atliekant bet kurį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="be177-237">At any step</span></span></td>
<td><span data-ttu-id="be177-238">Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, klientą arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="be177-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="be177-239">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pardavimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-240">Gamybos užsakymas</span><span class="sxs-lookup"><span data-stu-id="be177-240">Production order</span></span></td>
<td><span data-ttu-id="be177-241">Prieš pranešant apie baigtą gamybos užsakymo kiekį, arba po to.</span><span class="sxs-lookup"><span data-stu-id="be177-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="be177-242">Pranešus apie baigtą gamybos užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="be177-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="be177-243">Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją ar prekę, tiekėją arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="be177-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="be177-244">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis gamybos užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-245">Gamybos užsakymas su maršruto operacija</span><span class="sxs-lookup"><span data-stu-id="be177-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="be177-246">Prieš baigiant operacijos ataskaitą, arba po to.</span><span class="sxs-lookup"><span data-stu-id="be177-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="be177-247">Pranešus, kad paskutinės operacijos gamyba baigta.</span><span class="sxs-lookup"><span data-stu-id="be177-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="be177-248">Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę ar operacijų išteklių, arba šių sąlygų derinį.</span><span class="sxs-lookup"><span data-stu-id="be177-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="be177-249">Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis maršruto operaciją, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</span><span class="sxs-lookup"><span data-stu-id="be177-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="be177-250">Inventorizacijos</span><span class="sxs-lookup"><span data-stu-id="be177-250">Inventory</span></span></td>
<td><span data-ttu-id="be177-251">Kokybės užsakymo negalima automatiškai generuoti atsargų žurnalo operacijai arba perkėlimo užsakymo operacijoms.</span><span class="sxs-lookup"><span data-stu-id="be177-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="be177-252">Prekės atsargų kiekio kokybės užsakymą reikia kurti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="be177-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="be177-253">Reikia faktiškai turimų atsargų.</span><span class="sxs-lookup"><span data-stu-id="be177-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="be177-254">Automatinio kokybės užsakymų generavimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="be177-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="be177-255">Pirkimas</span><span class="sxs-lookup"><span data-stu-id="be177-255">Purchasing</span></span>

<span data-ttu-id="be177-256">Pirkdami, jei nustatėte lauko **Įvykio tipas** reikšmę *Gavimo dokumentas* ir lauko **Vykdymas** reikšmę *Po*, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="be177-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="be177-257">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Taip*, kokybės užsakymas generuojamas kiekvienam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu ir prekės pavyzdžių ėmimo parametrais.</span><span class="sxs-lookup"><span data-stu-id="be177-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="be177-258">Kiekvieną kartą, kai pagal pirkimo užsakymą gaunamas kiekis, remiantis naujai gautu kiekiu generuojami nauji kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="be177-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="be177-259">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Ne*, kokybės užsakymas generuojamas pirmajam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="be177-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="be177-260">Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į sekimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="be177-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="be177-261">Kokybės užsakymai negeneruojami vėlesniems kvitams pagal pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="be177-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="be177-262">Gamyba</span><span class="sxs-lookup"><span data-stu-id="be177-262">Production</span></span>

<span data-ttu-id="be177-263">Gamybos aplinkoje, jei nustatėte lauko **Įvykio tipas** reikšmę *Gavimo dokumentas* ir lauko **Skelbti baigtu** reikšmę *Po*, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="be177-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="be177-264">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Taip*, kokybės užsakymas generuojamas kiekvienam baigtam kiekiui ir pagal prekės pavyzdžių ėmimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="be177-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="be177-265">Kiekvieną kartą, kai pagal gamybos užsakymą kiekis paskelbiamas baigtu, remiantis naujai baigtu kiekiu generuojami nauji kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="be177-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="be177-266">Ši generavimo logika atitinka pirkimą.</span><span class="sxs-lookup"><span data-stu-id="be177-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="be177-267">Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Ne*, kokybės užsakymas generuojamas pirmą kartą, kai kiekis paskelbiamas baigtu, remiantis baigtu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="be177-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="be177-268">Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į prekės pavyzdžių ėmimo sekimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="be177-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="be177-269">Kokybės užsakymai negeneruojami vėliau baigtiems kiekiams.</span><span class="sxs-lookup"><span data-stu-id="be177-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="be177-270">Kokybės specifikacija</span><span class="sxs-lookup"><span data-stu-id="be177-270">Quality specification</span></span></th>
<th><span data-ttu-id="be177-271">Pagal atnaujintą kiekį</span><span class="sxs-lookup"><span data-stu-id="be177-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="be177-272">Pagal sekimo dimensiją</span><span class="sxs-lookup"><span data-stu-id="be177-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="be177-273">Rezultatas</span><span class="sxs-lookup"><span data-stu-id="be177-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="be177-274">Procentinė reikšmė: 10 %</span><span class="sxs-lookup"><span data-stu-id="be177-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="be177-275">Taip</span><span class="sxs-lookup"><span data-stu-id="be177-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="be177-276">Paketo numeris: ne</span><span class="sxs-lookup"><span data-stu-id="be177-276">Batch number: No</span></span></p>
<p><span data-ttu-id="be177-277">Serijos numeris: ne</span><span class="sxs-lookup"><span data-stu-id="be177-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="be177-278">Užsakymo kiekis: 100</span><span class="sxs-lookup"><span data-stu-id="be177-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="be177-279">Paskelbti kaip baigtą 30</span><span class="sxs-lookup"><span data-stu-id="be177-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="be177-280">Kokybės užsakymas #1, skirtas 3 (10 % iš 30)</span><span class="sxs-lookup"><span data-stu-id="be177-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="be177-281">Paskelbti kaip baigtą 70</span><span class="sxs-lookup"><span data-stu-id="be177-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="be177-282">Kokybės užsakymas #2, skirtas 7 (10 % likusio užsakymo kiekio, kuris šiuo atveju yra lygus 70)</span><span class="sxs-lookup"><span data-stu-id="be177-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="be177-283">Fiksuotas kiekis: 1</span><span class="sxs-lookup"><span data-stu-id="be177-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="be177-284">nr.</span><span class="sxs-lookup"><span data-stu-id="be177-284">No</span></span></td>
<td>
<p><span data-ttu-id="be177-285">Paketo numeris: ne</span><span class="sxs-lookup"><span data-stu-id="be177-285">Batch number: No</span></span></p>
<p><span data-ttu-id="be177-286">Serijos numeris: ne</span><span class="sxs-lookup"><span data-stu-id="be177-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="be177-287">Užsakymo kiekis: 100</span><span class="sxs-lookup"><span data-stu-id="be177-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="be177-288">Paskelbti kaip baigtą 30</span><span class="sxs-lookup"><span data-stu-id="be177-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="be177-289">Kokybės užsakymas #1, skirtas 1 (pirmajam paskelbtam baigtu kiekiui, kuris turi 1 fiksuotą vertę)</span><span class="sxs-lookup"><span data-stu-id="be177-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="be177-290">Kokybės užsakymas #2, skirtas 1 (likusiam kiekiui, kuris vis dar turi 1 fiksuotą vertę)</span><span class="sxs-lookup"><span data-stu-id="be177-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="be177-291">Paskelbti kaip baigtą 10</span><span class="sxs-lookup"><span data-stu-id="be177-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="be177-292">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="be177-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="be177-293">Paskelbti kaip baigtą 60</span><span class="sxs-lookup"><span data-stu-id="be177-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="be177-294">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="be177-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="be177-295">Fiksuotas kiekis: 1</span><span class="sxs-lookup"><span data-stu-id="be177-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="be177-296">Taip</span><span class="sxs-lookup"><span data-stu-id="be177-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="be177-297">Paketo numeris: taip</span><span class="sxs-lookup"><span data-stu-id="be177-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="be177-298">Serijos numeris: taip</span><span class="sxs-lookup"><span data-stu-id="be177-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="be177-299">Užsakymo kiekis: 10</span><span class="sxs-lookup"><span data-stu-id="be177-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="be177-300">Baigta, jei numeris b1, s1 serijos numeris – 3: 1; 1 paketo numeriui b2, s2 serijos numeriui; ir 1 paketo numerio b3, s3 serijos numerio</span><span class="sxs-lookup"><span data-stu-id="be177-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="be177-301">Kokybės užsakymas #1, skirtas 1, paketo numeris #b1, serijos #s1</span><span class="sxs-lookup"><span data-stu-id="be177-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="be177-302">Kokybės užsakymas #2, skirtas 1, paketo numeris #b2, serijos #s2</span><span class="sxs-lookup"><span data-stu-id="be177-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="be177-303">Kokybės užsakymas #3, skirtas 1, paketo numeris #b3, serijos #s3</span><span class="sxs-lookup"><span data-stu-id="be177-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="be177-304">Baigta, jei numeris 2: 1, paketo numeris b4, s4 serijos numeris ir 1 paketo numeriui b5, s5 serijos numeriams</span><span class="sxs-lookup"><span data-stu-id="be177-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="be177-305">Kokybės užsakymas #4, skirtas 1, paketo numeris #b4, serijos #s4</span><span class="sxs-lookup"><span data-stu-id="be177-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="be177-306">Kokybės užsakymas #5, skirtas 1, paketo numeris #b5, serijos #s5</span><span class="sxs-lookup"><span data-stu-id="be177-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="be177-307"><strong>Pastaba:</strong> paketą galima naudoti pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="be177-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="be177-308">Fiksuotas kiekis: 2</span><span class="sxs-lookup"><span data-stu-id="be177-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="be177-309">nr.</span><span class="sxs-lookup"><span data-stu-id="be177-309">No</span></span></td>
<td>
<p><span data-ttu-id="be177-310">Paketo numeris: taip</span><span class="sxs-lookup"><span data-stu-id="be177-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="be177-311">Serijos numeris: taip</span><span class="sxs-lookup"><span data-stu-id="be177-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="be177-312">Užsakymo kiekis: 10</span><span class="sxs-lookup"><span data-stu-id="be177-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="be177-313">Baigta, jei numeris b1, s1 serijos numeris – 3: 1; 1 paketo numeriui b2, s2 serijos numeriui; ir 1 paketo numerio b3, s3 serijos numerio ir 1 paketo numeriui b4, serijiniam numeriui s4</span><span class="sxs-lookup"><span data-stu-id="be177-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="be177-314">Kokybės užsakymas #1, skirtas 1, paketo numeris #b1, serijos #s1</span><span class="sxs-lookup"><span data-stu-id="be177-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="be177-315">Kokybės užsakymas #2, skirtas 1, paketo numeris #b2, serijos #s2</span><span class="sxs-lookup"><span data-stu-id="be177-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="be177-316">Kokybės užsakymas #3, skirtas 1, paketo numeris #b3, serijos #s3</span><span class="sxs-lookup"><span data-stu-id="be177-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="be177-317">Kokybės užsakymas #4, skirtas 1, paketo numeris #b4, serijos #s4</span><span class="sxs-lookup"><span data-stu-id="be177-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="be177-318">Kokybės užsakymas #5, skirtas 2, be nuorodos į paketą ir serijos numerį</span><span class="sxs-lookup"><span data-stu-id="be177-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="be177-319">Baigta, jei 6: 1, paketo numeris b5, s5 serijos numeris; 1 paketo numeriui b6, serijos numeris s6; 1 paketo numeriui b7, serijos numeris s7; 1 paketo numeriui b8, serijos numeris s8; 1 paketo numeriui b9, serijos numeris s9; ir 1 paketo numeriui b10, serijos numeris s10</span><span class="sxs-lookup"><span data-stu-id="be177-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="be177-320">Nėra sukurtų kokybės užsakymų.</span><span class="sxs-lookup"><span data-stu-id="be177-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="be177-321">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="be177-321">Additional resources</span></span>

- [<span data-ttu-id="be177-322">Kokybės valdymo procesai</span><span class="sxs-lookup"><span data-stu-id="be177-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="be177-323">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="be177-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="be177-324">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="be177-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
