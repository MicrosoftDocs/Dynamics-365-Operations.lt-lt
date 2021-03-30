---
title: Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika
description: Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti atsargų skirstymo pagal terminus ataskaitos rezultatus.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214423"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="46186-103">Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika</span><span class="sxs-lookup"><span data-stu-id="46186-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46186-104">Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti **Atsargų skirstymas pagal terminus** ataskaitos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="46186-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="46186-105">Ši ataskaita sugrupuoja turimos pasirinktos prekės arba prekių grupės kiekį ir atsargų vertes į kelių laikotarpių rinkinius.</span><span class="sxs-lookup"><span data-stu-id="46186-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="46186-106">Šioje temoje taip pat parodoma vidinė ataskaitos logika.</span><span class="sxs-lookup"><span data-stu-id="46186-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="46186-107">Šioje temoje pateikiami rezultatai rodo rezultatus, kurie pateikiami standartinėje **Atsargų skirstymas pagal terminus** ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="46186-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="46186-108">Tačiau bendrai rekomenduojame naudoti [Atsargų skirstymo pagal terminus ataskaitos saugyklos](inventory-aging-report-storage.md) versiją, ypač jei turite daug prekių ir sandėlių, kuriuos reikia sutvarkyti.</span><span class="sxs-lookup"><span data-stu-id="46186-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="46186-109">Atsargų skirstymo pagal terminus ataskaitos saugykla išsaugo kiekvieną jūsų sukurtą ataskaitą, parodo rezultatus kaip interaktyvų puslapį ir diagramą ir leidžia eksportuoti visas įrašytas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="46186-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="46186-110">Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys</span><span class="sxs-lookup"><span data-stu-id="46186-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="46186-111">Šios temos pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiu, aprašytu šioje dalyje.</span><span class="sxs-lookup"><span data-stu-id="46186-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="46186-112">Saugyklos dimensijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="46186-112">Storage dimension setup</span></span>

<span data-ttu-id="46186-113">Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.</span><span class="sxs-lookup"><span data-stu-id="46186-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="46186-114">Pavadinimas arba vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="46186-114">Name</span></span>      | <span data-ttu-id="46186-115">Aktyvi</span><span class="sxs-lookup"><span data-stu-id="46186-115">Active</span></span> | <span data-ttu-id="46186-116">Faktinės atsargos</span><span class="sxs-lookup"><span data-stu-id="46186-116">Physical inventory</span></span> | <span data-ttu-id="46186-117">Finansinės atsargos</span><span class="sxs-lookup"><span data-stu-id="46186-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="46186-118">Vieta</span><span class="sxs-lookup"><span data-stu-id="46186-118">Site</span></span>      | <span data-ttu-id="46186-119">Taip</span><span class="sxs-lookup"><span data-stu-id="46186-119">Yes</span></span>    | <span data-ttu-id="46186-120">Taip</span><span class="sxs-lookup"><span data-stu-id="46186-120">Yes</span></span>                | <span data-ttu-id="46186-121">Taip</span><span class="sxs-lookup"><span data-stu-id="46186-121">Yes</span></span>                 |
| <span data-ttu-id="46186-122">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="46186-122">Warehouse</span></span> | <span data-ttu-id="46186-123">Taip</span><span class="sxs-lookup"><span data-stu-id="46186-123">Yes</span></span>    | <span data-ttu-id="46186-124">Taip</span><span class="sxs-lookup"><span data-stu-id="46186-124">Yes</span></span>                | <span data-ttu-id="46186-125">nr.</span><span class="sxs-lookup"><span data-stu-id="46186-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="46186-126">Atsargų modelis</span><span class="sxs-lookup"><span data-stu-id="46186-126">Inventory model</span></span>

<span data-ttu-id="46186-127">Pavyzdinėje sistemoje išleistų produktų atsargų modelis yra *FIFO*, o **Savikaina** atsargų modelio parametras yra *Apima faktinę vertę*.</span><span class="sxs-lookup"><span data-stu-id="46186-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="46186-128">Atsargų operacijos</span><span class="sxs-lookup"><span data-stu-id="46186-128">Inventory transactions</span></span>

<span data-ttu-id="46186-129">Pavyzdžio sistemoje yra šios išleisto produkto atsargų operacijos, kurio prekės numeris *1000*.</span><span class="sxs-lookup"><span data-stu-id="46186-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="46186-130">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="46186-130">Reference</span></span>      | <span data-ttu-id="46186-131">Vieta</span><span class="sxs-lookup"><span data-stu-id="46186-131">Site</span></span> | <span data-ttu-id="46186-132">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="46186-132">Warehouse</span></span> | <span data-ttu-id="46186-133">Gavimas</span><span class="sxs-lookup"><span data-stu-id="46186-133">Receipt</span></span>   | <span data-ttu-id="46186-134">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="46186-134">Issue</span></span> | <span data-ttu-id="46186-135">Faktinė data</span><span class="sxs-lookup"><span data-stu-id="46186-135">Physical date</span></span> | <span data-ttu-id="46186-136">Fin. data</span><span class="sxs-lookup"><span data-stu-id="46186-136">Financial date</span></span> | <span data-ttu-id="46186-137">Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-137">Quantity</span></span> | <span data-ttu-id="46186-138">Išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="46186-138">Cost amount</span></span> | <span data-ttu-id="46186-139">Fakt. išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="46186-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="46186-140">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-140">Purchase order</span></span> | <span data-ttu-id="46186-141">1</span><span class="sxs-lookup"><span data-stu-id="46186-141">1</span></span>    | <span data-ttu-id="46186-142">11</span><span class="sxs-lookup"><span data-stu-id="46186-142">11</span></span>        | <span data-ttu-id="46186-143">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="46186-143">Purchased</span></span> |       | <span data-ttu-id="46186-144">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-144">March 15</span></span>      | <span data-ttu-id="46186-145">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-145">March 15</span></span>       | <span data-ttu-id="46186-146">10</span><span class="sxs-lookup"><span data-stu-id="46186-146">10</span></span>       | <span data-ttu-id="46186-147">1000</span><span class="sxs-lookup"><span data-stu-id="46186-147">1,000</span></span>       | <span data-ttu-id="46186-148">1000</span><span class="sxs-lookup"><span data-stu-id="46186-148">1,000</span></span>                |
| <span data-ttu-id="46186-149">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-149">Purchase order</span></span> | <span data-ttu-id="46186-150">2</span><span class="sxs-lookup"><span data-stu-id="46186-150">2</span></span>    | <span data-ttu-id="46186-151">21</span><span class="sxs-lookup"><span data-stu-id="46186-151">21</span></span>        | <span data-ttu-id="46186-152">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="46186-152">Purchased</span></span> |       | <span data-ttu-id="46186-153">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-153">March 15</span></span>      | <span data-ttu-id="46186-154">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-154">March 15</span></span>       | <span data-ttu-id="46186-155">10</span><span class="sxs-lookup"><span data-stu-id="46186-155">10</span></span>       | <span data-ttu-id="46186-156">2,000</span><span class="sxs-lookup"><span data-stu-id="46186-156">2,000</span></span>       | <span data-ttu-id="46186-157">2,000</span><span class="sxs-lookup"><span data-stu-id="46186-157">2,000</span></span>                |
| <span data-ttu-id="46186-158">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-158">Purchase order</span></span> | <span data-ttu-id="46186-159">1</span><span class="sxs-lookup"><span data-stu-id="46186-159">1</span></span>    | <span data-ttu-id="46186-160">11</span><span class="sxs-lookup"><span data-stu-id="46186-160">11</span></span>        | <span data-ttu-id="46186-161">Gauta</span><span class="sxs-lookup"><span data-stu-id="46186-161">Received</span></span>  |       | <span data-ttu-id="46186-162">15 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-162">April 15</span></span>      |                | <span data-ttu-id="46186-163">5</span><span class="sxs-lookup"><span data-stu-id="46186-163">5</span></span>        |             | <span data-ttu-id="46186-164">375</span><span class="sxs-lookup"><span data-stu-id="46186-164">375</span></span>                  |
| <span data-ttu-id="46186-165">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-165">Transfer order</span></span> | <span data-ttu-id="46186-166">1</span><span class="sxs-lookup"><span data-stu-id="46186-166">1</span></span>    | <span data-ttu-id="46186-167">11</span><span class="sxs-lookup"><span data-stu-id="46186-167">11</span></span>        |           | <span data-ttu-id="46186-168">Parduota</span><span class="sxs-lookup"><span data-stu-id="46186-168">Sold</span></span>  | <span data-ttu-id="46186-169">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-169">May 2</span></span>         | <span data-ttu-id="46186-170">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-170">May 2</span></span>          | <span data-ttu-id="46186-171">-5</span><span class="sxs-lookup"><span data-stu-id="46186-171">-5</span></span>       | <span data-ttu-id="46186-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="46186-172">-458.33</span></span>     | <span data-ttu-id="46186-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="46186-173">-458.33</span></span>              |
| <span data-ttu-id="46186-174">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-174">Transfer order</span></span> | <span data-ttu-id="46186-175">1</span><span class="sxs-lookup"><span data-stu-id="46186-175">1</span></span>    | <span data-ttu-id="46186-176">12</span><span class="sxs-lookup"><span data-stu-id="46186-176">12</span></span>        | <span data-ttu-id="46186-177">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="46186-177">Purchased</span></span> |       | <span data-ttu-id="46186-178">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-178">May 2</span></span>         | <span data-ttu-id="46186-179">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-179">May 2</span></span>          | <span data-ttu-id="46186-180">5</span><span class="sxs-lookup"><span data-stu-id="46186-180">5</span></span>        | <span data-ttu-id="46186-181">458.33</span><span class="sxs-lookup"><span data-stu-id="46186-181">458.33</span></span>      | <span data-ttu-id="46186-182">458.33</span><span class="sxs-lookup"><span data-stu-id="46186-182">458.33</span></span>               |
| <span data-ttu-id="46186-183">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="46186-183">Sales order</span></span>    | <span data-ttu-id="46186-184">1</span><span class="sxs-lookup"><span data-stu-id="46186-184">1</span></span>    | <span data-ttu-id="46186-185">12</span><span class="sxs-lookup"><span data-stu-id="46186-185">12</span></span>        |           | <span data-ttu-id="46186-186">Parduota</span><span class="sxs-lookup"><span data-stu-id="46186-186">Sold</span></span>  | <span data-ttu-id="46186-187">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-187">May 3</span></span>         | <span data-ttu-id="46186-188">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="46186-188">May 3</span></span>          | <span data-ttu-id="46186-189">-1</span><span class="sxs-lookup"><span data-stu-id="46186-189">-1</span></span>       | <span data-ttu-id="46186-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="46186-190">-91.67</span></span>      | <span data-ttu-id="46186-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="46186-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="46186-192">Kaip apskaičiuojami kiekvieno laikotarpio rinkinio kiekiai ir sumos</span><span class="sxs-lookup"><span data-stu-id="46186-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="46186-193">Naudodami ankstesniuose skyriuose aprašytus duomenų pavyzdžius, galite paleisti **Atsargų skirstymas pagal terminus** ataskaitą, nustatytą pagal šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="46186-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="46186-194">**Nuo datos:** *2020 m. gegužės 9 d.*</span><span class="sxs-lookup"><span data-stu-id="46186-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="46186-195">**Vieta:** *Rodinys*</span><span class="sxs-lookup"><span data-stu-id="46186-195">**Site:** *View*</span></span>
- <span data-ttu-id="46186-196">**Sandėlis:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="46186-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="46186-197">**Prekės numeris:** *Iš viso*</span><span class="sxs-lookup"><span data-stu-id="46186-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="46186-198">**Skirstymo pagal terminus laikotarpis:** nustatykite šį lauką, kad būtų generuojami mėnesio rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="46186-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="46186-199">Šiuo atveju sugeneruotos ataskaitos turinys bus panašus į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="46186-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="46186-200">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="46186-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-201">Vieta</span><span class="sxs-lookup"><span data-stu-id="46186-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-202">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-203">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="46186-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-204">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-205">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="46186-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-206">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="46186-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-207">2020-05-01–2020-05-08</span><span class="sxs-lookup"><span data-stu-id="46186-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-208">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="46186-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-209">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="46186-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="46186-210">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="46186-211">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="46186-212">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="46186-213">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="46186-214">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="46186-215">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="46186-216">1000</span><span class="sxs-lookup"><span data-stu-id="46186-216">1000</span></span></td>
    <td><span data-ttu-id="46186-217">1</span><span class="sxs-lookup"><span data-stu-id="46186-217">1</span></span></td>
    <td><span data-ttu-id="46186-218">14</span><span class="sxs-lookup"><span data-stu-id="46186-218">14</span></span></td>
    <td><span data-ttu-id="46186-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="46186-219">1,283.33</span></span></td>
    <td><span data-ttu-id="46186-220">14</span><span class="sxs-lookup"><span data-stu-id="46186-220">14</span></span></td>
    <td><span data-ttu-id="46186-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="46186-221">1,283.33</span></span></td>
    <td><span data-ttu-id="46186-222">91.67</span><span class="sxs-lookup"><span data-stu-id="46186-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-223">5.00</span><span class="sxs-lookup"><span data-stu-id="46186-223">5.00</span></span></td>
    <td><span data-ttu-id="46186-224">458.33</span><span class="sxs-lookup"><span data-stu-id="46186-224">458.33</span></span></td>
    <td><span data-ttu-id="46186-225">9.00</span><span class="sxs-lookup"><span data-stu-id="46186-225">9.00</span></span></td>
    <td><span data-ttu-id="46186-226">825.00</span><span class="sxs-lookup"><span data-stu-id="46186-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="46186-227">1000</span><span class="sxs-lookup"><span data-stu-id="46186-227">1000</span></span></td>
    <td><span data-ttu-id="46186-228">2</span><span class="sxs-lookup"><span data-stu-id="46186-228">2</span></span></td>
    <td><span data-ttu-id="46186-229">10</span><span class="sxs-lookup"><span data-stu-id="46186-229">10</span></span></td>
    <td><span data-ttu-id="46186-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-230">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-231">10</span><span class="sxs-lookup"><span data-stu-id="46186-231">10</span></span></td>
    <td><span data-ttu-id="46186-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-232">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-233">200.00</span><span class="sxs-lookup"><span data-stu-id="46186-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-234">10,00</span><span class="sxs-lookup"><span data-stu-id="46186-234">10.00</span></span></td>
    <td><span data-ttu-id="46186-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="46186-236"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="46186-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="46186-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="46186-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="46186-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="46186-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="46186-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="46186-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="46186-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="46186-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="46186-243">Atkreipkite dėmesį į šią išsamią informaciją šio pavyzdžio ataskaitoje:</span><span class="sxs-lookup"><span data-stu-id="46186-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="46186-244">**Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** ataskaitoje rodomos vertės yra finansinių atsargų dimensijų ( šiuo atveju, **Vieta**) vertės.</span><span class="sxs-lookup"><span data-stu-id="46186-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="46186-245">Pavyzdžiui, 1-oje vietoje ataskaitoje pateikiama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="46186-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="46186-246">**Atsargų verčių kiekis** vertė yra *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="46186-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="46186-247">**Atsargų vertė** vertė yra *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="46186-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="46186-248">**Vidutinė vieneto savikaina** vertė yra *91,67*.</span><span class="sxs-lookup"><span data-stu-id="46186-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="46186-249">**Turima vertė** vertė ir **Suma** vertė kiekviename laikotarpio rinkinyje yra apskaičiuojama naudojant **Vidutinė vieneto savikaina** vertę.</span><span class="sxs-lookup"><span data-stu-id="46186-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="46186-250">Ši ataskaita apibrėžia turimą kiekvieno laikotarpio rinkinio kiekį apibendrindama bendrą gautų atsargų kiekį kiekvienam laikotarpio rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="46186-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="46186-251">Tada taikoma pirmas ateina, pirmas išeina (FIFO) principas norint atskaityti visą išduotą kiekį, neatsižvelgiant į atsargų modelį, kurį naudoja prekės.</span><span class="sxs-lookup"><span data-stu-id="46186-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="46186-252">Jei tą pačią ataskaitą paleidote iš naujo, šį kartą nustatykite tiek **Vieta**, tiek **Sandėlis** laukus į *Peržiūrėti*, kad nauja ataskaita būtų panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="46186-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="46186-253">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="46186-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-254">Vieta</span><span class="sxs-lookup"><span data-stu-id="46186-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-255">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="46186-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-256">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-257">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="46186-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-258">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-259">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="46186-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-260">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="46186-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-261">2020-05-01–2020-05-08</span><span class="sxs-lookup"><span data-stu-id="46186-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-262">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="46186-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-263">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="46186-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="46186-264">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="46186-265">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="46186-266">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="46186-267">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="46186-268">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="46186-269">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="46186-270">1000</span><span class="sxs-lookup"><span data-stu-id="46186-270">1000</span></span></td>
    <td><span data-ttu-id="46186-271">1</span><span class="sxs-lookup"><span data-stu-id="46186-271">1</span></span></td>
    <td><span data-ttu-id="46186-272">11</span><span class="sxs-lookup"><span data-stu-id="46186-272">11</span></span></td>
    <td><span data-ttu-id="46186-273">10</span><span class="sxs-lookup"><span data-stu-id="46186-273">10</span></span></td>
    <td><span data-ttu-id="46186-274">916.67</span><span class="sxs-lookup"><span data-stu-id="46186-274">916.67</span></span></td>
    <td><span data-ttu-id="46186-275">14</span><span class="sxs-lookup"><span data-stu-id="46186-275">14</span></span></td>
    <td><span data-ttu-id="46186-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="46186-276">1,283.33</span></span></td>
    <td><span data-ttu-id="46186-277">91.67</span><span class="sxs-lookup"><span data-stu-id="46186-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-278">5.00</span><span class="sxs-lookup"><span data-stu-id="46186-278">5.00</span></span></td>
    <td><span data-ttu-id="46186-279">458.33</span><span class="sxs-lookup"><span data-stu-id="46186-279">458.33</span></span></td>
    <td><span data-ttu-id="46186-280">5.00</span><span class="sxs-lookup"><span data-stu-id="46186-280">5.00</span></span></td>
    <td><span data-ttu-id="46186-281">458.33</span><span class="sxs-lookup"><span data-stu-id="46186-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="46186-282">1000</span><span class="sxs-lookup"><span data-stu-id="46186-282">1000</span></span></td>
    <td><span data-ttu-id="46186-283">1</span><span class="sxs-lookup"><span data-stu-id="46186-283">1</span></span></td>
    <td><span data-ttu-id="46186-284">12</span><span class="sxs-lookup"><span data-stu-id="46186-284">12</span></span></td>
    <td><span data-ttu-id="46186-285">4</span><span class="sxs-lookup"><span data-stu-id="46186-285">4</span></span></td>
    <td><span data-ttu-id="46186-286">366.67</span><span class="sxs-lookup"><span data-stu-id="46186-286">366.67</span></span></td>
    <td><span data-ttu-id="46186-287">14</span><span class="sxs-lookup"><span data-stu-id="46186-287">14</span></span></td>
    <td><span data-ttu-id="46186-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="46186-288">1,283.33</span></span></td>
    <td><span data-ttu-id="46186-289">91.67</span><span class="sxs-lookup"><span data-stu-id="46186-289">91.67</span></span></td>
    <td><span data-ttu-id="46186-290">4.00</span><span class="sxs-lookup"><span data-stu-id="46186-290">4.00</span></span></td>
    <td><span data-ttu-id="46186-291">366.67</span><span class="sxs-lookup"><span data-stu-id="46186-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="46186-292">1000</span><span class="sxs-lookup"><span data-stu-id="46186-292">1000</span></span></td>
    <td><span data-ttu-id="46186-293">2</span><span class="sxs-lookup"><span data-stu-id="46186-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="46186-294">10</span><span class="sxs-lookup"><span data-stu-id="46186-294">10</span></span></td>
    <td><span data-ttu-id="46186-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-295">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-296">10</span><span class="sxs-lookup"><span data-stu-id="46186-296">10</span></span></td>
    <td><span data-ttu-id="46186-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-297">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-298">200.00</span><span class="sxs-lookup"><span data-stu-id="46186-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-299">10,00</span><span class="sxs-lookup"><span data-stu-id="46186-299">10.00</span></span></td>
    <td><span data-ttu-id="46186-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="46186-301"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="46186-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="46186-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="46186-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="46186-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="46186-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="46186-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="46186-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="46186-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="46186-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="46186-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="46186-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="46186-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="46186-310">Šį kartą 1-a vieta yra padalinama į dvi eiles: vieną 11-am sandėliui ir vieną 12-am sandėliui.</span><span class="sxs-lookup"><span data-stu-id="46186-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="46186-311">Tačiau **Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės yra tos pačios, nes **Sandėlis** nėra finansinė atsargų dimensija.</span><span class="sxs-lookup"><span data-stu-id="46186-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="46186-312">Be to, atkreipkite dėmesį, kad 1-os vietos kiekio paskirstymas skiriasi.</span><span class="sxs-lookup"><span data-stu-id="46186-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="46186-313">Pirmoje jūsų paleistoje ataskaitoje sistema nepaisė perkėlimo užsakymo, įvykusio toje pačioje vietoje, ir išskaitė pardavimo sąskaitos faktūros kiekį iš **2020-03-01-2020-03-31** laikotarpio rinkinį 1-oje vietoje.</span><span class="sxs-lookup"><span data-stu-id="46186-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="46186-314">Tačiau naujoje ataskaitoje sistema išskaito pardavimo sąskaitos faktūros kiekį iš **2020-05-01–2020-05-08** laikotarpio rinkinio 12-ame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="46186-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="46186-315">Atsargų uždarymo pasekmės</span><span class="sxs-lookup"><span data-stu-id="46186-315">Effects of inventory closing</span></span>

<span data-ttu-id="46186-316">Jeigu įvykdėte atsargų uždarymą gegužės mėnesiui, o tada dar kartą paleidote ankstesnę ataskaitą, bet nustatėte **Nuo datos** lauką į *2020 m. gegužės 31 d.*, pastebėsite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="46186-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="46186-317">**Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės atnaujintos.</span><span class="sxs-lookup"><span data-stu-id="46186-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="46186-318">**Turima vertė** vertė ir visos **Suma** vertės kiekviename laikotarpio rinkinyje yra atitinkamai atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="46186-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="46186-319">Naujoji ataskaita bus panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="46186-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="46186-320">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="46186-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-321">Vieta</span><span class="sxs-lookup"><span data-stu-id="46186-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-322">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="46186-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-323">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-324">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="46186-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-325">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-326">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="46186-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="46186-327">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="46186-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-328">2020-05-01–2020-05-31</span><span class="sxs-lookup"><span data-stu-id="46186-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-329">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="46186-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="46186-330">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="46186-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="46186-331">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="46186-332">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="46186-333">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="46186-334">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="46186-335">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="46186-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="46186-336">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="46186-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="46186-337">1000</span><span class="sxs-lookup"><span data-stu-id="46186-337">1000</span></span></td>
    <td><span data-ttu-id="46186-338">1</span><span class="sxs-lookup"><span data-stu-id="46186-338">1</span></span></td>
    <td><span data-ttu-id="46186-339">11</span><span class="sxs-lookup"><span data-stu-id="46186-339">11</span></span></td>
    <td><span data-ttu-id="46186-340">10</span><span class="sxs-lookup"><span data-stu-id="46186-340">10</span></span></td>
    <td><span data-ttu-id="46186-341">910.70</span><span class="sxs-lookup"><span data-stu-id="46186-341">910.70</span></span></td>
    <td><span data-ttu-id="46186-342">14</span><span class="sxs-lookup"><span data-stu-id="46186-342">14</span></span></td>
    <td><span data-ttu-id="46186-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="46186-343">1,275.00</span></span></td>
    <td><span data-ttu-id="46186-344">91.07</span><span class="sxs-lookup"><span data-stu-id="46186-344">91.07</span></span></td>
    <td><span data-ttu-id="46186-345">0,00</span><span class="sxs-lookup"><span data-stu-id="46186-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="46186-346">5.00</span><span class="sxs-lookup"><span data-stu-id="46186-346">5.00</span></span></td>
    <td><span data-ttu-id="46186-347">455.36</span><span class="sxs-lookup"><span data-stu-id="46186-347">455.36</span></span></td>
    <td><span data-ttu-id="46186-348">5.00</span><span class="sxs-lookup"><span data-stu-id="46186-348">5.00</span></span></td>
    <td><span data-ttu-id="46186-349">455.36</span><span class="sxs-lookup"><span data-stu-id="46186-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="46186-350">1000</span><span class="sxs-lookup"><span data-stu-id="46186-350">1000</span></span></td>
    <td><span data-ttu-id="46186-351">1</span><span class="sxs-lookup"><span data-stu-id="46186-351">1</span></span></td>
    <td><span data-ttu-id="46186-352">12</span><span class="sxs-lookup"><span data-stu-id="46186-352">12</span></span></td>
    <td><span data-ttu-id="46186-353">4</span><span class="sxs-lookup"><span data-stu-id="46186-353">4</span></span></td>
    <td><span data-ttu-id="46186-354">364.29</span><span class="sxs-lookup"><span data-stu-id="46186-354">364.29</span></span></td>
    <td><span data-ttu-id="46186-355">14</span><span class="sxs-lookup"><span data-stu-id="46186-355">14</span></span></td>
    <td><span data-ttu-id="46186-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="46186-356">1,275.00</span></span></td>
    <td><span data-ttu-id="46186-357">91.07</span><span class="sxs-lookup"><span data-stu-id="46186-357">91.07</span></span></td>
    <td><span data-ttu-id="46186-358">4.00</span><span class="sxs-lookup"><span data-stu-id="46186-358">4.00</span></span></td>
    <td><span data-ttu-id="46186-359">364.29</span><span class="sxs-lookup"><span data-stu-id="46186-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="46186-360">1000</span><span class="sxs-lookup"><span data-stu-id="46186-360">1000</span></span></td>
    <td><span data-ttu-id="46186-361">2</span><span class="sxs-lookup"><span data-stu-id="46186-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="46186-362">10</span><span class="sxs-lookup"><span data-stu-id="46186-362">10</span></span></td>
    <td><span data-ttu-id="46186-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-363">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-364">10</span><span class="sxs-lookup"><span data-stu-id="46186-364">10</span></span></td>
    <td><span data-ttu-id="46186-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-365">2,000.00</span></span></td>
    <td><span data-ttu-id="46186-366">200.00</span><span class="sxs-lookup"><span data-stu-id="46186-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-367">10,00</span><span class="sxs-lookup"><span data-stu-id="46186-367">10.00</span></span></td>
    <td><span data-ttu-id="46186-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="46186-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="46186-369"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="46186-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="46186-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="46186-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="46186-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="46186-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="46186-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="46186-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="46186-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="46186-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="46186-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="46186-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="46186-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="46186-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]