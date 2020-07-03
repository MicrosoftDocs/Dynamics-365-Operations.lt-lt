---
title: Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika
description: Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti atsargų skirstymo pagal terminus ataskaitos rezultatus.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484535"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="fb063-103">Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika</span><span class="sxs-lookup"><span data-stu-id="fb063-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb063-104">Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti **Atsargų skirstymas pagal terminus** ataskaitos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fb063-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="fb063-105">Ši ataskaita sugrupuoja turimos pasirinktos prekės arba prekių grupės kiekį ir atsargų vertes į kelių laikotarpių rinkinius.</span><span class="sxs-lookup"><span data-stu-id="fb063-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="fb063-106">Šioje temoje taip pat parodoma vidinė ataskaitos logika.</span><span class="sxs-lookup"><span data-stu-id="fb063-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="fb063-107">Šioje temoje pateikiami rezultatai rodo rezultatus, kurie pateikiami standartinėje **Atsargų skirstymas pagal terminus** ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="fb063-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="fb063-108">Tačiau bendrai rekomenduojame naudoti [Atsargų skirstymo pagal terminus ataskaitos saugyklos](inventory-aging-report-storage.md) versiją, ypač jei turite daug prekių ir sandėlių, kuriuos reikia sutvarkyti.</span><span class="sxs-lookup"><span data-stu-id="fb063-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="fb063-109">Atsargų skirstymo pagal terminus ataskaitos saugykla išsaugo kiekvieną jūsų sukurtą ataskaitą, parodo rezultatus kaip interaktyvų puslapį ir diagramą ir leidžia eksportuoti visas įrašytas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="fb063-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="fb063-110">Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fb063-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="fb063-111">Šios temos pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiu, aprašytu šioje dalyje.</span><span class="sxs-lookup"><span data-stu-id="fb063-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="fb063-112">Saugyklos dimensijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="fb063-112">Storage dimension setup</span></span>

<span data-ttu-id="fb063-113">Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.</span><span class="sxs-lookup"><span data-stu-id="fb063-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="fb063-114">Pavadinimas arba vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="fb063-114">Name</span></span>      | <span data-ttu-id="fb063-115">Aktyvi</span><span class="sxs-lookup"><span data-stu-id="fb063-115">Active</span></span> | <span data-ttu-id="fb063-116">Faktinės atsargos</span><span class="sxs-lookup"><span data-stu-id="fb063-116">Physical inventory</span></span> | <span data-ttu-id="fb063-117">Finansinės atsargos</span><span class="sxs-lookup"><span data-stu-id="fb063-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="fb063-118">Vieta</span><span class="sxs-lookup"><span data-stu-id="fb063-118">Site</span></span>      | <span data-ttu-id="fb063-119">Taip</span><span class="sxs-lookup"><span data-stu-id="fb063-119">Yes</span></span>    | <span data-ttu-id="fb063-120">Taip</span><span class="sxs-lookup"><span data-stu-id="fb063-120">Yes</span></span>                | <span data-ttu-id="fb063-121">Taip</span><span class="sxs-lookup"><span data-stu-id="fb063-121">Yes</span></span>                 |
| <span data-ttu-id="fb063-122">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="fb063-122">Warehouse</span></span> | <span data-ttu-id="fb063-123">Taip</span><span class="sxs-lookup"><span data-stu-id="fb063-123">Yes</span></span>    | <span data-ttu-id="fb063-124">Taip</span><span class="sxs-lookup"><span data-stu-id="fb063-124">Yes</span></span>                | <span data-ttu-id="fb063-125">nr.</span><span class="sxs-lookup"><span data-stu-id="fb063-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="fb063-126">Atsargų modelis</span><span class="sxs-lookup"><span data-stu-id="fb063-126">Inventory model</span></span>

<span data-ttu-id="fb063-127">Pavyzdinėje sistemoje išleistų produktų atsargų modelis yra *FIFO*, o **Savikaina** atsargų modelio parametras yra *Apima faktinę vertę*.</span><span class="sxs-lookup"><span data-stu-id="fb063-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="fb063-128">Atsargų operacijos</span><span class="sxs-lookup"><span data-stu-id="fb063-128">Inventory transactions</span></span>

<span data-ttu-id="fb063-129">Pavyzdžio sistemoje yra šios išleisto produkto atsargų operacijos, kurio prekės numeris *1000*.</span><span class="sxs-lookup"><span data-stu-id="fb063-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="fb063-130">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="fb063-130">Reference</span></span>      | <span data-ttu-id="fb063-131">Vieta</span><span class="sxs-lookup"><span data-stu-id="fb063-131">Site</span></span> | <span data-ttu-id="fb063-132">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="fb063-132">Warehouse</span></span> | <span data-ttu-id="fb063-133">Gavimas</span><span class="sxs-lookup"><span data-stu-id="fb063-133">Receipt</span></span>   | <span data-ttu-id="fb063-134">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="fb063-134">Issue</span></span> | <span data-ttu-id="fb063-135">Faktinė data</span><span class="sxs-lookup"><span data-stu-id="fb063-135">Physical date</span></span> | <span data-ttu-id="fb063-136">Fin. data</span><span class="sxs-lookup"><span data-stu-id="fb063-136">Financial date</span></span> | <span data-ttu-id="fb063-137">Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-137">Quantity</span></span> | <span data-ttu-id="fb063-138">Išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="fb063-138">Cost amount</span></span> | <span data-ttu-id="fb063-139">Fakt. išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="fb063-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="fb063-140">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-140">Purchase order</span></span> | <span data-ttu-id="fb063-141">1</span><span class="sxs-lookup"><span data-stu-id="fb063-141">1</span></span>    | <span data-ttu-id="fb063-142">11</span><span class="sxs-lookup"><span data-stu-id="fb063-142">11</span></span>        | <span data-ttu-id="fb063-143">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="fb063-143">Purchased</span></span> |       | <span data-ttu-id="fb063-144">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-144">March 15</span></span>      | <span data-ttu-id="fb063-145">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-145">March 15</span></span>       | <span data-ttu-id="fb063-146">10</span><span class="sxs-lookup"><span data-stu-id="fb063-146">10</span></span>       | <span data-ttu-id="fb063-147">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-147">1,000</span></span>       | <span data-ttu-id="fb063-148">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-148">1,000</span></span>                |
| <span data-ttu-id="fb063-149">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-149">Purchase order</span></span> | <span data-ttu-id="fb063-150">2</span><span class="sxs-lookup"><span data-stu-id="fb063-150">2</span></span>    | <span data-ttu-id="fb063-151">21</span><span class="sxs-lookup"><span data-stu-id="fb063-151">21</span></span>        | <span data-ttu-id="fb063-152">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="fb063-152">Purchased</span></span> |       | <span data-ttu-id="fb063-153">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-153">March 15</span></span>      | <span data-ttu-id="fb063-154">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-154">March 15</span></span>       | <span data-ttu-id="fb063-155">10</span><span class="sxs-lookup"><span data-stu-id="fb063-155">10</span></span>       | <span data-ttu-id="fb063-156">2,000</span><span class="sxs-lookup"><span data-stu-id="fb063-156">2,000</span></span>       | <span data-ttu-id="fb063-157">2,000</span><span class="sxs-lookup"><span data-stu-id="fb063-157">2,000</span></span>                |
| <span data-ttu-id="fb063-158">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-158">Purchase order</span></span> | <span data-ttu-id="fb063-159">1</span><span class="sxs-lookup"><span data-stu-id="fb063-159">1</span></span>    | <span data-ttu-id="fb063-160">11</span><span class="sxs-lookup"><span data-stu-id="fb063-160">11</span></span>        | <span data-ttu-id="fb063-161">Gauta</span><span class="sxs-lookup"><span data-stu-id="fb063-161">Received</span></span>  |       | <span data-ttu-id="fb063-162">15 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-162">April 15</span></span>      |                | <span data-ttu-id="fb063-163">5</span><span class="sxs-lookup"><span data-stu-id="fb063-163">5</span></span>        |             | <span data-ttu-id="fb063-164">375</span><span class="sxs-lookup"><span data-stu-id="fb063-164">375</span></span>                  |
| <span data-ttu-id="fb063-165">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-165">Transfer order</span></span> | <span data-ttu-id="fb063-166">1</span><span class="sxs-lookup"><span data-stu-id="fb063-166">1</span></span>    | <span data-ttu-id="fb063-167">11</span><span class="sxs-lookup"><span data-stu-id="fb063-167">11</span></span>        |           | <span data-ttu-id="fb063-168">Parduota</span><span class="sxs-lookup"><span data-stu-id="fb063-168">Sold</span></span>  | <span data-ttu-id="fb063-169">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-169">May 2</span></span>         | <span data-ttu-id="fb063-170">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-170">May 2</span></span>          | <span data-ttu-id="fb063-171">-5</span><span class="sxs-lookup"><span data-stu-id="fb063-171">-5</span></span>       | <span data-ttu-id="fb063-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="fb063-172">-458.33</span></span>     | <span data-ttu-id="fb063-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="fb063-173">-458.33</span></span>              |
| <span data-ttu-id="fb063-174">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-174">Transfer order</span></span> | <span data-ttu-id="fb063-175">1</span><span class="sxs-lookup"><span data-stu-id="fb063-175">1</span></span>    | <span data-ttu-id="fb063-176">12</span><span class="sxs-lookup"><span data-stu-id="fb063-176">12</span></span>        | <span data-ttu-id="fb063-177">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="fb063-177">Purchased</span></span> |       | <span data-ttu-id="fb063-178">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-178">May 2</span></span>         | <span data-ttu-id="fb063-179">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-179">May 2</span></span>          | <span data-ttu-id="fb063-180">5</span><span class="sxs-lookup"><span data-stu-id="fb063-180">5</span></span>        | <span data-ttu-id="fb063-181">458.33</span><span class="sxs-lookup"><span data-stu-id="fb063-181">458.33</span></span>      | <span data-ttu-id="fb063-182">458.33</span><span class="sxs-lookup"><span data-stu-id="fb063-182">458.33</span></span>               |
| <span data-ttu-id="fb063-183">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="fb063-183">Sales order</span></span>    | <span data-ttu-id="fb063-184">1</span><span class="sxs-lookup"><span data-stu-id="fb063-184">1</span></span>    | <span data-ttu-id="fb063-185">12</span><span class="sxs-lookup"><span data-stu-id="fb063-185">12</span></span>        |           | <span data-ttu-id="fb063-186">Parduota</span><span class="sxs-lookup"><span data-stu-id="fb063-186">Sold</span></span>  | <span data-ttu-id="fb063-187">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-187">May 3</span></span>         | <span data-ttu-id="fb063-188">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="fb063-188">May 3</span></span>          | <span data-ttu-id="fb063-189">-1</span><span class="sxs-lookup"><span data-stu-id="fb063-189">-1</span></span>       | <span data-ttu-id="fb063-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="fb063-190">-91.67</span></span>      | <span data-ttu-id="fb063-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="fb063-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="fb063-192">Kaip apskaičiuojami kiekvieno laikotarpio rinkinio kiekiai ir sumos</span><span class="sxs-lookup"><span data-stu-id="fb063-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="fb063-193">Naudodami ankstesniuose skyriuose aprašytus duomenų pavyzdžius, galite paleisti **Atsargų skirstymas pagal terminus** ataskaitą, nustatytą pagal šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="fb063-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="fb063-194">**Nuo datos:** *2020 m. gegužės 9 d.*</span><span class="sxs-lookup"><span data-stu-id="fb063-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="fb063-195">**Vieta:** *Rodinys*</span><span class="sxs-lookup"><span data-stu-id="fb063-195">**Site:** *View*</span></span>
- <span data-ttu-id="fb063-196">**Sandėlis:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="fb063-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="fb063-197">**Prekės numeris:** *Iš viso*</span><span class="sxs-lookup"><span data-stu-id="fb063-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="fb063-198">**Skirstymo pagal terminus laikotarpis:** nustatykite šį lauką, kad būtų generuojami mėnesio rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="fb063-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="fb063-199">Šiuo atveju sugeneruotos ataskaitos turinys bus panašus į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="fb063-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="fb063-200">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="fb063-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-201">Vieta</span><span class="sxs-lookup"><span data-stu-id="fb063-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-202">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-203">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-204">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-205">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-206">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="fb063-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-207">2020-05-01–2020-05-08 </span><span class="sxs-lookup"><span data-stu-id="fb063-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-208">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="fb063-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-209">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="fb063-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="fb063-210">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-211">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="fb063-212">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-213">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="fb063-214">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-215">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="fb063-216">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-216">1000</span></span></td>
    <td><span data-ttu-id="fb063-217">1</span><span class="sxs-lookup"><span data-stu-id="fb063-217">1</span></span></td>
    <td><span data-ttu-id="fb063-218">14</span><span class="sxs-lookup"><span data-stu-id="fb063-218">14</span></span></td>
    <td><span data-ttu-id="fb063-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="fb063-219">1,283.33</span></span></td>
    <td><span data-ttu-id="fb063-220">14</span><span class="sxs-lookup"><span data-stu-id="fb063-220">14</span></span></td>
    <td><span data-ttu-id="fb063-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="fb063-221">1,283.33</span></span></td>
    <td><span data-ttu-id="fb063-222">91.67</span><span class="sxs-lookup"><span data-stu-id="fb063-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-223">5.00</span><span class="sxs-lookup"><span data-stu-id="fb063-223">5.00</span></span></td>
    <td><span data-ttu-id="fb063-224">458.33</span><span class="sxs-lookup"><span data-stu-id="fb063-224">458.33</span></span></td>
    <td><span data-ttu-id="fb063-225">9.00</span><span class="sxs-lookup"><span data-stu-id="fb063-225">9.00</span></span></td>
    <td><span data-ttu-id="fb063-226">825.00</span><span class="sxs-lookup"><span data-stu-id="fb063-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="fb063-227">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-227">1000</span></span></td>
    <td><span data-ttu-id="fb063-228">2</span><span class="sxs-lookup"><span data-stu-id="fb063-228">2</span></span></td>
    <td><span data-ttu-id="fb063-229">10</span><span class="sxs-lookup"><span data-stu-id="fb063-229">10</span></span></td>
    <td><span data-ttu-id="fb063-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-230">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-231">10</span><span class="sxs-lookup"><span data-stu-id="fb063-231">10</span></span></td>
    <td><span data-ttu-id="fb063-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-232">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-233">200.00</span><span class="sxs-lookup"><span data-stu-id="fb063-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-234">10,00</span><span class="sxs-lookup"><span data-stu-id="fb063-234">10.00</span></span></td>
    <td><span data-ttu-id="fb063-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="fb063-236"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="fb063-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="fb063-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="fb063-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="fb063-243">Atkreipkite dėmesį į šią išsamią informaciją šio pavyzdžio ataskaitoje:</span><span class="sxs-lookup"><span data-stu-id="fb063-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="fb063-244">**Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** ataskaitoje rodomos vertės yra finansinių atsargų dimensijų ( šiuo atveju, **Vieta**) vertės.</span><span class="sxs-lookup"><span data-stu-id="fb063-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="fb063-245">Pavyzdžiui, 1-oje vietoje ataskaitoje pateikiama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="fb063-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="fb063-246">**Atsargų verčių kiekis** vertė yra *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="fb063-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="fb063-247">**Atsargų vertė** vertė yra *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="fb063-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="fb063-248">**Vidutinė vieneto savikaina** vertė yra *91,67*.</span><span class="sxs-lookup"><span data-stu-id="fb063-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="fb063-249">**Turima vertė** vertė ir **Suma** vertė kiekviename laikotarpio rinkinyje yra apskaičiuojama naudojant **Vidutinė vieneto savikaina** vertę.</span><span class="sxs-lookup"><span data-stu-id="fb063-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="fb063-250">Ši ataskaita apibrėžia turimą kiekvieno laikotarpio rinkinio kiekį apibendrindama bendrą gautų atsargų kiekį kiekvienam laikotarpio rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="fb063-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="fb063-251">Tada taikoma pirmas ateina, pirmas išeina (FIFO) principas norint atskaityti visą išduotą kiekį, neatsižvelgiant į atsargų modelį, kurį naudoja prekės.</span><span class="sxs-lookup"><span data-stu-id="fb063-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="fb063-252">Jei tą pačią ataskaitą paleidote iš naujo, šį kartą nustatykite tiek **Vieta**, tiek **Sandėlis** laukus į *Peržiūrėti*, kad nauja ataskaita būtų panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="fb063-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="fb063-253">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="fb063-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-254">Vieta</span><span class="sxs-lookup"><span data-stu-id="fb063-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-255">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="fb063-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-256">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-257">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-258">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-259">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-260">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="fb063-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-261">2020-05-01–2020-05-08 </span><span class="sxs-lookup"><span data-stu-id="fb063-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-262">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="fb063-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-263">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="fb063-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="fb063-264">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-265">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="fb063-266">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-267">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="fb063-268">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-269">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="fb063-270">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-270">1000</span></span></td>
    <td><span data-ttu-id="fb063-271">1</span><span class="sxs-lookup"><span data-stu-id="fb063-271">1</span></span></td>
    <td><span data-ttu-id="fb063-272">11</span><span class="sxs-lookup"><span data-stu-id="fb063-272">11</span></span></td>
    <td><span data-ttu-id="fb063-273">10</span><span class="sxs-lookup"><span data-stu-id="fb063-273">10</span></span></td>
    <td><span data-ttu-id="fb063-274">916.67</span><span class="sxs-lookup"><span data-stu-id="fb063-274">916.67</span></span></td>
    <td><span data-ttu-id="fb063-275">14</span><span class="sxs-lookup"><span data-stu-id="fb063-275">14</span></span></td>
    <td><span data-ttu-id="fb063-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="fb063-276">1,283.33</span></span></td>
    <td><span data-ttu-id="fb063-277">91.67</span><span class="sxs-lookup"><span data-stu-id="fb063-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-278">5.00</span><span class="sxs-lookup"><span data-stu-id="fb063-278">5.00</span></span></td>
    <td><span data-ttu-id="fb063-279">458.33</span><span class="sxs-lookup"><span data-stu-id="fb063-279">458.33</span></span></td>
    <td><span data-ttu-id="fb063-280">5.00</span><span class="sxs-lookup"><span data-stu-id="fb063-280">5.00</span></span></td>
    <td><span data-ttu-id="fb063-281">458.33</span><span class="sxs-lookup"><span data-stu-id="fb063-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="fb063-282">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-282">1000</span></span></td>
    <td><span data-ttu-id="fb063-283">1</span><span class="sxs-lookup"><span data-stu-id="fb063-283">1</span></span></td>
    <td><span data-ttu-id="fb063-284">12</span><span class="sxs-lookup"><span data-stu-id="fb063-284">12</span></span></td>
    <td><span data-ttu-id="fb063-285">4</span><span class="sxs-lookup"><span data-stu-id="fb063-285">4</span></span></td>
    <td><span data-ttu-id="fb063-286">366.67</span><span class="sxs-lookup"><span data-stu-id="fb063-286">366.67</span></span></td>
    <td><span data-ttu-id="fb063-287">14</span><span class="sxs-lookup"><span data-stu-id="fb063-287">14</span></span></td>
    <td><span data-ttu-id="fb063-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="fb063-288">1,283.33</span></span></td>
    <td><span data-ttu-id="fb063-289">91.67</span><span class="sxs-lookup"><span data-stu-id="fb063-289">91.67</span></span></td>
    <td><span data-ttu-id="fb063-290">4.00</span><span class="sxs-lookup"><span data-stu-id="fb063-290">4.00</span></span></td>
    <td><span data-ttu-id="fb063-291">366.67</span><span class="sxs-lookup"><span data-stu-id="fb063-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="fb063-292">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-292">1000</span></span></td>
    <td><span data-ttu-id="fb063-293">2</span><span class="sxs-lookup"><span data-stu-id="fb063-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="fb063-294">10</span><span class="sxs-lookup"><span data-stu-id="fb063-294">10</span></span></td>
    <td><span data-ttu-id="fb063-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-295">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-296">10</span><span class="sxs-lookup"><span data-stu-id="fb063-296">10</span></span></td>
    <td><span data-ttu-id="fb063-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-297">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-298">200.00</span><span class="sxs-lookup"><span data-stu-id="fb063-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-299">10,00</span><span class="sxs-lookup"><span data-stu-id="fb063-299">10.00</span></span></td>
    <td><span data-ttu-id="fb063-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="fb063-301"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="fb063-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="fb063-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="fb063-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="fb063-310">Šį kartą 1-a vieta yra padalinama į dvi eiles: vieną 11-am sandėliui ir vieną 12-am sandėliui.</span><span class="sxs-lookup"><span data-stu-id="fb063-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="fb063-311">Tačiau **Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės yra tos pačios, nes **Sandėlis** nėra finansinė atsargų dimensija.</span><span class="sxs-lookup"><span data-stu-id="fb063-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="fb063-312">Be to, atkreipkite dėmesį, kad 1-os vietos kiekio paskirstymas skiriasi.</span><span class="sxs-lookup"><span data-stu-id="fb063-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="fb063-313">Pirmoje jūsų paleistoje ataskaitoje sistema nepaisė perkėlimo užsakymo, įvykusio toje pačioje vietoje, ir išskaitė pardavimo sąskaitos faktūros kiekį iš **2020-03-01-2020-03-31** laikotarpio rinkinį 1-oje vietoje.</span><span class="sxs-lookup"><span data-stu-id="fb063-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="fb063-314">Tačiau naujoje ataskaitoje sistema išskaito pardavimo sąskaitos faktūros kiekį iš **2020-05-01–2020-05-08** laikotarpio rinkinio 12-ame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="fb063-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="fb063-315">Atsargų uždarymo pasekmės</span><span class="sxs-lookup"><span data-stu-id="fb063-315">Effects of inventory closing</span></span>

<span data-ttu-id="fb063-316">Jeigu įvykdėte atsargų uždarymą gegužės mėnesiui, o tada dar kartą paleidote ankstesnę ataskaitą, bet nustatėte **Nuo datos** lauką į *2020 m. gegužės 31 d.*, pastebėsite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="fb063-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="fb063-317">**Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės atnaujintos.</span><span class="sxs-lookup"><span data-stu-id="fb063-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="fb063-318">**Turima vertė** vertė ir visos **Suma** vertės kiekviename laikotarpio rinkinyje yra atitinkamai atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="fb063-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="fb063-319">Naujoji ataskaita bus panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="fb063-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="fb063-320">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="fb063-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-321">Vieta</span><span class="sxs-lookup"><span data-stu-id="fb063-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-322">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="fb063-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-323">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-324">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-325">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-326">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="fb063-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="fb063-327">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="fb063-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-328">2020-05-01–2020-05-31 </span><span class="sxs-lookup"><span data-stu-id="fb063-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-329">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="fb063-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="fb063-330">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="fb063-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="fb063-331">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-332">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="fb063-333">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-334">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="fb063-335">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="fb063-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="fb063-336">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="fb063-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="fb063-337">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-337">1000</span></span></td>
    <td><span data-ttu-id="fb063-338">1</span><span class="sxs-lookup"><span data-stu-id="fb063-338">1</span></span></td>
    <td><span data-ttu-id="fb063-339">11</span><span class="sxs-lookup"><span data-stu-id="fb063-339">11</span></span></td>
    <td><span data-ttu-id="fb063-340">10</span><span class="sxs-lookup"><span data-stu-id="fb063-340">10</span></span></td>
    <td><span data-ttu-id="fb063-341">910.70</span><span class="sxs-lookup"><span data-stu-id="fb063-341">910.70</span></span></td>
    <td><span data-ttu-id="fb063-342">14</span><span class="sxs-lookup"><span data-stu-id="fb063-342">14</span></span></td>
    <td><span data-ttu-id="fb063-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="fb063-343">1,275.00</span></span></td>
    <td><span data-ttu-id="fb063-344">91.07</span><span class="sxs-lookup"><span data-stu-id="fb063-344">91.07</span></span></td>
    <td><span data-ttu-id="fb063-345">0,00</span><span class="sxs-lookup"><span data-stu-id="fb063-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="fb063-346">5.00</span><span class="sxs-lookup"><span data-stu-id="fb063-346">5.00</span></span></td>
    <td><span data-ttu-id="fb063-347">455.36</span><span class="sxs-lookup"><span data-stu-id="fb063-347">455.36</span></span></td>
    <td><span data-ttu-id="fb063-348">5.00</span><span class="sxs-lookup"><span data-stu-id="fb063-348">5.00</span></span></td>
    <td><span data-ttu-id="fb063-349">455.36</span><span class="sxs-lookup"><span data-stu-id="fb063-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="fb063-350">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-350">1000</span></span></td>
    <td><span data-ttu-id="fb063-351">1</span><span class="sxs-lookup"><span data-stu-id="fb063-351">1</span></span></td>
    <td><span data-ttu-id="fb063-352">12</span><span class="sxs-lookup"><span data-stu-id="fb063-352">12</span></span></td>
    <td><span data-ttu-id="fb063-353">4</span><span class="sxs-lookup"><span data-stu-id="fb063-353">4</span></span></td>
    <td><span data-ttu-id="fb063-354">364.29</span><span class="sxs-lookup"><span data-stu-id="fb063-354">364.29</span></span></td>
    <td><span data-ttu-id="fb063-355">14</span><span class="sxs-lookup"><span data-stu-id="fb063-355">14</span></span></td>
    <td><span data-ttu-id="fb063-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="fb063-356">1,275.00</span></span></td>
    <td><span data-ttu-id="fb063-357">91.07</span><span class="sxs-lookup"><span data-stu-id="fb063-357">91.07</span></span></td>
    <td><span data-ttu-id="fb063-358">4.00</span><span class="sxs-lookup"><span data-stu-id="fb063-358">4.00</span></span></td>
    <td><span data-ttu-id="fb063-359">364.29</span><span class="sxs-lookup"><span data-stu-id="fb063-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="fb063-360">1000</span><span class="sxs-lookup"><span data-stu-id="fb063-360">1000</span></span></td>
    <td><span data-ttu-id="fb063-361">2</span><span class="sxs-lookup"><span data-stu-id="fb063-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="fb063-362">10</span><span class="sxs-lookup"><span data-stu-id="fb063-362">10</span></span></td>
    <td><span data-ttu-id="fb063-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-363">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-364">10</span><span class="sxs-lookup"><span data-stu-id="fb063-364">10</span></span></td>
    <td><span data-ttu-id="fb063-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-365">2,000.00</span></span></td>
    <td><span data-ttu-id="fb063-366">200.00</span><span class="sxs-lookup"><span data-stu-id="fb063-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-367">10,00</span><span class="sxs-lookup"><span data-stu-id="fb063-367">10.00</span></span></td>
    <td><span data-ttu-id="fb063-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="fb063-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="fb063-369"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="fb063-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="fb063-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="fb063-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="fb063-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="fb063-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="fb063-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
