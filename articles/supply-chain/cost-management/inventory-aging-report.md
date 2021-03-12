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
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983930"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="a6cb5-103">Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika</span><span class="sxs-lookup"><span data-stu-id="a6cb5-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6cb5-104">Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti **Atsargų skirstymas pagal terminus** ataskaitos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="a6cb5-105">Ši ataskaita sugrupuoja turimos pasirinktos prekės arba prekių grupės kiekį ir atsargų vertes į kelių laikotarpių rinkinius.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="a6cb5-106">Šioje temoje taip pat parodoma vidinė ataskaitos logika.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="a6cb5-107">Šioje temoje pateikiami rezultatai rodo rezultatus, kurie pateikiami standartinėje **Atsargų skirstymas pagal terminus** ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="a6cb5-108">Tačiau bendrai rekomenduojame naudoti [Atsargų skirstymo pagal terminus ataskaitos saugyklos](inventory-aging-report-storage.md) versiją, ypač jei turite daug prekių ir sandėlių, kuriuos reikia sutvarkyti.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="a6cb5-109">Atsargų skirstymo pagal terminus ataskaitos saugykla išsaugo kiekvieną jūsų sukurtą ataskaitą, parodo rezultatus kaip interaktyvų puslapį ir diagramą ir leidžia eksportuoti visas įrašytas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="a6cb5-110">Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a6cb5-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="a6cb5-111">Šios temos pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiu, aprašytu šioje dalyje.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="a6cb5-112">Saugyklos dimensijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-112">Storage dimension setup</span></span>

<span data-ttu-id="a6cb5-113">Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="a6cb5-114">Pavadinimas arba vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-114">Name</span></span>      | <span data-ttu-id="a6cb5-115">Aktyvi</span><span class="sxs-lookup"><span data-stu-id="a6cb5-115">Active</span></span> | <span data-ttu-id="a6cb5-116">Faktinės atsargos</span><span class="sxs-lookup"><span data-stu-id="a6cb5-116">Physical inventory</span></span> | <span data-ttu-id="a6cb5-117">Finansinės atsargos</span><span class="sxs-lookup"><span data-stu-id="a6cb5-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="a6cb5-118">Vieta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-118">Site</span></span>      | <span data-ttu-id="a6cb5-119">Taip</span><span class="sxs-lookup"><span data-stu-id="a6cb5-119">Yes</span></span>    | <span data-ttu-id="a6cb5-120">Taip</span><span class="sxs-lookup"><span data-stu-id="a6cb5-120">Yes</span></span>                | <span data-ttu-id="a6cb5-121">Taip</span><span class="sxs-lookup"><span data-stu-id="a6cb5-121">Yes</span></span>                 |
| <span data-ttu-id="a6cb5-122">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-122">Warehouse</span></span> | <span data-ttu-id="a6cb5-123">Taip</span><span class="sxs-lookup"><span data-stu-id="a6cb5-123">Yes</span></span>    | <span data-ttu-id="a6cb5-124">Taip</span><span class="sxs-lookup"><span data-stu-id="a6cb5-124">Yes</span></span>                | <span data-ttu-id="a6cb5-125">nr.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="a6cb5-126">Atsargų modelis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-126">Inventory model</span></span>

<span data-ttu-id="a6cb5-127">Pavyzdinėje sistemoje išleistų produktų atsargų modelis yra *FIFO*, o **Savikaina** atsargų modelio parametras yra *Apima faktinę vertę*.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="a6cb5-128">Atsargų operacijos</span><span class="sxs-lookup"><span data-stu-id="a6cb5-128">Inventory transactions</span></span>

<span data-ttu-id="a6cb5-129">Pavyzdžio sistemoje yra šios išleisto produkto atsargų operacijos, kurio prekės numeris *1000*.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="a6cb5-130">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="a6cb5-130">Reference</span></span>      | <span data-ttu-id="a6cb5-131">Vieta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-131">Site</span></span> | <span data-ttu-id="a6cb5-132">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-132">Warehouse</span></span> | <span data-ttu-id="a6cb5-133">Gavimas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-133">Receipt</span></span>   | <span data-ttu-id="a6cb5-134">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-134">Issue</span></span> | <span data-ttu-id="a6cb5-135">Faktinė data</span><span class="sxs-lookup"><span data-stu-id="a6cb5-135">Physical date</span></span> | <span data-ttu-id="a6cb5-136">Fin. data</span><span class="sxs-lookup"><span data-stu-id="a6cb5-136">Financial date</span></span> | <span data-ttu-id="a6cb5-137">Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-137">Quantity</span></span> | <span data-ttu-id="a6cb5-138">Išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-138">Cost amount</span></span> | <span data-ttu-id="a6cb5-139">Fakt. išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="a6cb5-140">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-140">Purchase order</span></span> | <span data-ttu-id="a6cb5-141">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-141">1</span></span>    | <span data-ttu-id="a6cb5-142">11</span><span class="sxs-lookup"><span data-stu-id="a6cb5-142">11</span></span>        | <span data-ttu-id="a6cb5-143">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-143">Purchased</span></span> |       | <span data-ttu-id="a6cb5-144">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-144">March 15</span></span>      | <span data-ttu-id="a6cb5-145">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-145">March 15</span></span>       | <span data-ttu-id="a6cb5-146">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-146">10</span></span>       | <span data-ttu-id="a6cb5-147">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-147">1,000</span></span>       | <span data-ttu-id="a6cb5-148">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-148">1,000</span></span>                |
| <span data-ttu-id="a6cb5-149">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-149">Purchase order</span></span> | <span data-ttu-id="a6cb5-150">2</span><span class="sxs-lookup"><span data-stu-id="a6cb5-150">2</span></span>    | <span data-ttu-id="a6cb5-151">21</span><span class="sxs-lookup"><span data-stu-id="a6cb5-151">21</span></span>        | <span data-ttu-id="a6cb5-152">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-152">Purchased</span></span> |       | <span data-ttu-id="a6cb5-153">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-153">March 15</span></span>      | <span data-ttu-id="a6cb5-154">15 m. kovo mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-154">March 15</span></span>       | <span data-ttu-id="a6cb5-155">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-155">10</span></span>       | <span data-ttu-id="a6cb5-156">2,000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-156">2,000</span></span>       | <span data-ttu-id="a6cb5-157">2,000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-157">2,000</span></span>                |
| <span data-ttu-id="a6cb5-158">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-158">Purchase order</span></span> | <span data-ttu-id="a6cb5-159">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-159">1</span></span>    | <span data-ttu-id="a6cb5-160">11</span><span class="sxs-lookup"><span data-stu-id="a6cb5-160">11</span></span>        | <span data-ttu-id="a6cb5-161">Gauta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-161">Received</span></span>  |       | <span data-ttu-id="a6cb5-162">15 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-162">April 15</span></span>      |                | <span data-ttu-id="a6cb5-163">5</span><span class="sxs-lookup"><span data-stu-id="a6cb5-163">5</span></span>        |             | <span data-ttu-id="a6cb5-164">375</span><span class="sxs-lookup"><span data-stu-id="a6cb5-164">375</span></span>                  |
| <span data-ttu-id="a6cb5-165">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-165">Transfer order</span></span> | <span data-ttu-id="a6cb5-166">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-166">1</span></span>    | <span data-ttu-id="a6cb5-167">11</span><span class="sxs-lookup"><span data-stu-id="a6cb5-167">11</span></span>        |           | <span data-ttu-id="a6cb5-168">Parduota</span><span class="sxs-lookup"><span data-stu-id="a6cb5-168">Sold</span></span>  | <span data-ttu-id="a6cb5-169">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-169">May 2</span></span>         | <span data-ttu-id="a6cb5-170">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-170">May 2</span></span>          | <span data-ttu-id="a6cb5-171">-5</span><span class="sxs-lookup"><span data-stu-id="a6cb5-171">-5</span></span>       | <span data-ttu-id="a6cb5-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-172">-458.33</span></span>     | <span data-ttu-id="a6cb5-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-173">-458.33</span></span>              |
| <span data-ttu-id="a6cb5-174">Perkėlimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-174">Transfer order</span></span> | <span data-ttu-id="a6cb5-175">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-175">1</span></span>    | <span data-ttu-id="a6cb5-176">12</span><span class="sxs-lookup"><span data-stu-id="a6cb5-176">12</span></span>        | <span data-ttu-id="a6cb5-177">Nupirkta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-177">Purchased</span></span> |       | <span data-ttu-id="a6cb5-178">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-178">May 2</span></span>         | <span data-ttu-id="a6cb5-179">2 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-179">May 2</span></span>          | <span data-ttu-id="a6cb5-180">5</span><span class="sxs-lookup"><span data-stu-id="a6cb5-180">5</span></span>        | <span data-ttu-id="a6cb5-181">458.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-181">458.33</span></span>      | <span data-ttu-id="a6cb5-182">458.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-182">458.33</span></span>               |
| <span data-ttu-id="a6cb5-183">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="a6cb5-183">Sales order</span></span>    | <span data-ttu-id="a6cb5-184">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-184">1</span></span>    | <span data-ttu-id="a6cb5-185">12</span><span class="sxs-lookup"><span data-stu-id="a6cb5-185">12</span></span>        |           | <span data-ttu-id="a6cb5-186">Parduota</span><span class="sxs-lookup"><span data-stu-id="a6cb5-186">Sold</span></span>  | <span data-ttu-id="a6cb5-187">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-187">May 3</span></span>         | <span data-ttu-id="a6cb5-188">3 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-188">May 3</span></span>          | <span data-ttu-id="a6cb5-189">-1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-189">-1</span></span>       | <span data-ttu-id="a6cb5-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-190">-91.67</span></span>      | <span data-ttu-id="a6cb5-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="a6cb5-192">Kaip apskaičiuojami kiekvieno laikotarpio rinkinio kiekiai ir sumos</span><span class="sxs-lookup"><span data-stu-id="a6cb5-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="a6cb5-193">Naudodami ankstesniuose skyriuose aprašytus duomenų pavyzdžius, galite paleisti **Atsargų skirstymas pagal terminus** ataskaitą, nustatytą pagal šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="a6cb5-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="a6cb5-194">**Nuo datos:** *2020 m. gegužės 9 d.*</span><span class="sxs-lookup"><span data-stu-id="a6cb5-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="a6cb5-195">**Vieta:** *Rodinys*</span><span class="sxs-lookup"><span data-stu-id="a6cb5-195">**Site:** *View*</span></span>
- <span data-ttu-id="a6cb5-196">**Sandėlis:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="a6cb5-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="a6cb5-197">**Prekės numeris:** *Iš viso*</span><span class="sxs-lookup"><span data-stu-id="a6cb5-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="a6cb5-198">**Skirstymo pagal terminus laikotarpis:** nustatykite šį lauką, kad būtų generuojami mėnesio rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="a6cb5-199">Šiuo atveju sugeneruotos ataskaitos turinys bus panašus į šį pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a6cb5-200">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-201">Vieta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-202">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-203">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-204">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-205">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-206">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="a6cb5-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-207">2020-05-01–2020-05-08</span><span class="sxs-lookup"><span data-stu-id="a6cb5-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-208">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="a6cb5-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-209">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="a6cb5-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a6cb5-210">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-211">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-212">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-213">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-214">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-215">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a6cb5-216">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-216">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-217">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-217">1</span></span></td>
    <td><span data-ttu-id="a6cb5-218">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-218">14</span></span></td>
    <td><span data-ttu-id="a6cb5-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-219">1,283.33</span></span></td>
    <td><span data-ttu-id="a6cb5-220">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-220">14</span></span></td>
    <td><span data-ttu-id="a6cb5-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-221">1,283.33</span></span></td>
    <td><span data-ttu-id="a6cb5-222">91.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-223">5.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-223">5.00</span></span></td>
    <td><span data-ttu-id="a6cb5-224">458.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-224">458.33</span></span></td>
    <td><span data-ttu-id="a6cb5-225">9.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-225">9.00</span></span></td>
    <td><span data-ttu-id="a6cb5-226">825.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a6cb5-227">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-227">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-228">2</span><span class="sxs-lookup"><span data-stu-id="a6cb5-228">2</span></span></td>
    <td><span data-ttu-id="a6cb5-229">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-229">10</span></span></td>
    <td><span data-ttu-id="a6cb5-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-230">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-231">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-231">10</span></span></td>
    <td><span data-ttu-id="a6cb5-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-232">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-233">200.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-234">10,00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-234">10.00</span></span></td>
    <td><span data-ttu-id="a6cb5-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a6cb5-236"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a6cb5-243">Atkreipkite dėmesį į šią išsamią informaciją šio pavyzdžio ataskaitoje:</span><span class="sxs-lookup"><span data-stu-id="a6cb5-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="a6cb5-244">**Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** ataskaitoje rodomos vertės yra finansinių atsargų dimensijų ( šiuo atveju, **Vieta**) vertės.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="a6cb5-245">Pavyzdžiui, 1-oje vietoje ataskaitoje pateikiama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="a6cb5-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="a6cb5-246">**Atsargų verčių kiekis** vertė yra *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="a6cb5-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="a6cb5-247">**Atsargų vertė** vertė yra *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="a6cb5-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="a6cb5-248">**Vidutinė vieneto savikaina** vertė yra *91,67*.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="a6cb5-249">**Turima vertė** vertė ir **Suma** vertė kiekviename laikotarpio rinkinyje yra apskaičiuojama naudojant **Vidutinė vieneto savikaina** vertę.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="a6cb5-250">Ši ataskaita apibrėžia turimą kiekvieno laikotarpio rinkinio kiekį apibendrindama bendrą gautų atsargų kiekį kiekvienam laikotarpio rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="a6cb5-251">Tada taikoma pirmas ateina, pirmas išeina (FIFO) principas norint atskaityti visą išduotą kiekį, neatsižvelgiant į atsargų modelį, kurį naudoja prekės.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="a6cb5-252">Jei tą pačią ataskaitą paleidote iš naujo, šį kartą nustatykite tiek **Vieta**, tiek **Sandėlis** laukus į *Peržiūrėti*, kad nauja ataskaita būtų panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a6cb5-253">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-254">Vieta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-255">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-256">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-257">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-258">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-259">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-260">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="a6cb5-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-261">2020-05-01–2020-05-08</span><span class="sxs-lookup"><span data-stu-id="a6cb5-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-262">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="a6cb5-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-263">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="a6cb5-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a6cb5-264">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-265">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-266">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-267">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-268">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-269">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a6cb5-270">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-270">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-271">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-271">1</span></span></td>
    <td><span data-ttu-id="a6cb5-272">11</span><span class="sxs-lookup"><span data-stu-id="a6cb5-272">11</span></span></td>
    <td><span data-ttu-id="a6cb5-273">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-273">10</span></span></td>
    <td><span data-ttu-id="a6cb5-274">916.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-274">916.67</span></span></td>
    <td><span data-ttu-id="a6cb5-275">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-275">14</span></span></td>
    <td><span data-ttu-id="a6cb5-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-276">1,283.33</span></span></td>
    <td><span data-ttu-id="a6cb5-277">91.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-278">5.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-278">5.00</span></span></td>
    <td><span data-ttu-id="a6cb5-279">458.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-279">458.33</span></span></td>
    <td><span data-ttu-id="a6cb5-280">5.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-280">5.00</span></span></td>
    <td><span data-ttu-id="a6cb5-281">458.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a6cb5-282">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-282">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-283">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-283">1</span></span></td>
    <td><span data-ttu-id="a6cb5-284">12</span><span class="sxs-lookup"><span data-stu-id="a6cb5-284">12</span></span></td>
    <td><span data-ttu-id="a6cb5-285">4</span><span class="sxs-lookup"><span data-stu-id="a6cb5-285">4</span></span></td>
    <td><span data-ttu-id="a6cb5-286">366.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-286">366.67</span></span></td>
    <td><span data-ttu-id="a6cb5-287">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-287">14</span></span></td>
    <td><span data-ttu-id="a6cb5-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a6cb5-288">1,283.33</span></span></td>
    <td><span data-ttu-id="a6cb5-289">91.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-289">91.67</span></span></td>
    <td><span data-ttu-id="a6cb5-290">4.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-290">4.00</span></span></td>
    <td><span data-ttu-id="a6cb5-291">366.67</span><span class="sxs-lookup"><span data-stu-id="a6cb5-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a6cb5-292">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-292">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-293">2</span><span class="sxs-lookup"><span data-stu-id="a6cb5-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-294">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-294">10</span></span></td>
    <td><span data-ttu-id="a6cb5-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-295">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-296">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-296">10</span></span></td>
    <td><span data-ttu-id="a6cb5-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-297">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-298">200.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-299">10,00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-299">10.00</span></span></td>
    <td><span data-ttu-id="a6cb5-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a6cb5-301"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a6cb5-310">Šį kartą 1-a vieta yra padalinama į dvi eiles: vieną 11-am sandėliui ir vieną 12-am sandėliui.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="a6cb5-311">Tačiau **Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės yra tos pačios, nes **Sandėlis** nėra finansinė atsargų dimensija.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="a6cb5-312">Be to, atkreipkite dėmesį, kad 1-os vietos kiekio paskirstymas skiriasi.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="a6cb5-313">Pirmoje jūsų paleistoje ataskaitoje sistema nepaisė perkėlimo užsakymo, įvykusio toje pačioje vietoje, ir išskaitė pardavimo sąskaitos faktūros kiekį iš **2020-03-01-2020-03-31** laikotarpio rinkinį 1-oje vietoje.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="a6cb5-314">Tačiau naujoje ataskaitoje sistema išskaito pardavimo sąskaitos faktūros kiekį iš **2020-05-01–2020-05-08** laikotarpio rinkinio 12-ame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="a6cb5-315">Atsargų uždarymo pasekmės</span><span class="sxs-lookup"><span data-stu-id="a6cb5-315">Effects of inventory closing</span></span>

<span data-ttu-id="a6cb5-316">Jeigu įvykdėte atsargų uždarymą gegužės mėnesiui, o tada dar kartą paleidote ankstesnę ataskaitą, bet nustatėte **Nuo datos** lauką į *2020 m. gegužės 31 d.*, pastebėsite šiuos rezultatus:</span><span class="sxs-lookup"><span data-stu-id="a6cb5-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="a6cb5-317">**Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės atnaujintos.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="a6cb5-318">**Turima vertė** vertė ir visos **Suma** vertės kiekviename laikotarpio rinkinyje yra atitinkamai atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="a6cb5-319">Naujoji ataskaita bus panaši į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a6cb5-320">Prekės Nr.</span><span class="sxs-lookup"><span data-stu-id="a6cb5-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-321">Vieta</span><span class="sxs-lookup"><span data-stu-id="a6cb5-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-322">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-323">Turimas kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-324">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-325">Atsargų vertės kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-326">Atsargų vertė</span><span class="sxs-lookup"><span data-stu-id="a6cb5-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a6cb5-327">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="a6cb5-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-328">2020-05-01–2020-05-31</span><span class="sxs-lookup"><span data-stu-id="a6cb5-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-329">2020-04-01–2020-04-30</span><span class="sxs-lookup"><span data-stu-id="a6cb5-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a6cb5-330">2020-03-01–2020-03-31</span><span class="sxs-lookup"><span data-stu-id="a6cb5-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a6cb5-331">P1:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-332">P1:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-333">P2:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-334">P2:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="a6cb5-335">P3:Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6cb5-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a6cb5-336">P3:Suma</span><span class="sxs-lookup"><span data-stu-id="a6cb5-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a6cb5-337">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-337">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-338">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-338">1</span></span></td>
    <td><span data-ttu-id="a6cb5-339">11</span><span class="sxs-lookup"><span data-stu-id="a6cb5-339">11</span></span></td>
    <td><span data-ttu-id="a6cb5-340">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-340">10</span></span></td>
    <td><span data-ttu-id="a6cb5-341">910.70</span><span class="sxs-lookup"><span data-stu-id="a6cb5-341">910.70</span></span></td>
    <td><span data-ttu-id="a6cb5-342">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-342">14</span></span></td>
    <td><span data-ttu-id="a6cb5-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-343">1,275.00</span></span></td>
    <td><span data-ttu-id="a6cb5-344">91.07</span><span class="sxs-lookup"><span data-stu-id="a6cb5-344">91.07</span></span></td>
    <td><span data-ttu-id="a6cb5-345">0,00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-346">5.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-346">5.00</span></span></td>
    <td><span data-ttu-id="a6cb5-347">455.36</span><span class="sxs-lookup"><span data-stu-id="a6cb5-347">455.36</span></span></td>
    <td><span data-ttu-id="a6cb5-348">5.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-348">5.00</span></span></td>
    <td><span data-ttu-id="a6cb5-349">455.36</span><span class="sxs-lookup"><span data-stu-id="a6cb5-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a6cb5-350">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-350">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-351">1</span><span class="sxs-lookup"><span data-stu-id="a6cb5-351">1</span></span></td>
    <td><span data-ttu-id="a6cb5-352">12</span><span class="sxs-lookup"><span data-stu-id="a6cb5-352">12</span></span></td>
    <td><span data-ttu-id="a6cb5-353">4</span><span class="sxs-lookup"><span data-stu-id="a6cb5-353">4</span></span></td>
    <td><span data-ttu-id="a6cb5-354">364.29</span><span class="sxs-lookup"><span data-stu-id="a6cb5-354">364.29</span></span></td>
    <td><span data-ttu-id="a6cb5-355">14</span><span class="sxs-lookup"><span data-stu-id="a6cb5-355">14</span></span></td>
    <td><span data-ttu-id="a6cb5-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-356">1,275.00</span></span></td>
    <td><span data-ttu-id="a6cb5-357">91.07</span><span class="sxs-lookup"><span data-stu-id="a6cb5-357">91.07</span></span></td>
    <td><span data-ttu-id="a6cb5-358">4.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-358">4.00</span></span></td>
    <td><span data-ttu-id="a6cb5-359">364.29</span><span class="sxs-lookup"><span data-stu-id="a6cb5-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a6cb5-360">1000</span><span class="sxs-lookup"><span data-stu-id="a6cb5-360">1000</span></span></td>
    <td><span data-ttu-id="a6cb5-361">2</span><span class="sxs-lookup"><span data-stu-id="a6cb5-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-362">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-362">10</span></span></td>
    <td><span data-ttu-id="a6cb5-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-363">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-364">10</span><span class="sxs-lookup"><span data-stu-id="a6cb5-364">10</span></span></td>
    <td><span data-ttu-id="a6cb5-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-365">2,000.00</span></span></td>
    <td><span data-ttu-id="a6cb5-366">200.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-367">10,00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-367">10.00</span></span></td>
    <td><span data-ttu-id="a6cb5-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a6cb5-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a6cb5-369"><strong>1000 bendros sumos</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a6cb5-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a6cb5-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="a6cb5-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
