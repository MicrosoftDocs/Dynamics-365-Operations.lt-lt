---
title: Mažinimo raktai
description: Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą. Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus. Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e62431a1fdbeb81dda68297f034ee00adece079
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "364815"
---
# <a name="reduction-keys"></a><span data-ttu-id="abb70-105">Mažinimo raktai</span><span class="sxs-lookup"><span data-stu-id="abb70-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abb70-106">Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą.</span><span class="sxs-lookup"><span data-stu-id="abb70-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="abb70-107">Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="abb70-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="abb70-108">Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius.</span><span class="sxs-lookup"><span data-stu-id="abb70-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="abb70-109">1 pavyzdys: procentas – mažinimo rakto prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="abb70-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="abb70-110">Šiame pavyzdyje parodoma, kaip mažinimo raktas sumažina poreikio prognozės poreikius pagal procentines dalis ir laikotarpius, kuriuos nurodo mažinimo raktas.</span><span class="sxs-lookup"><span data-stu-id="abb70-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="abb70-111">Puslapyje **Mažinimo raktai** nustatykite toliau nurodytas eilutes.</span><span class="sxs-lookup"><span data-stu-id="abb70-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="abb70-112">Grąža</span><span class="sxs-lookup"><span data-stu-id="abb70-112">Change</span></span> | <span data-ttu-id="abb70-113">Vienetas</span><span class="sxs-lookup"><span data-stu-id="abb70-113">Unit</span></span>  | <span data-ttu-id="abb70-114">Procentas</span><span class="sxs-lookup"><span data-stu-id="abb70-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="abb70-115">1</span><span class="sxs-lookup"><span data-stu-id="abb70-115">1</span></span>    | <span data-ttu-id="abb70-116">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-116">Month</span></span> |   <span data-ttu-id="abb70-117">100</span><span class="sxs-lookup"><span data-stu-id="abb70-117">100</span></span>   |
   |   <span data-ttu-id="abb70-118">2</span><span class="sxs-lookup"><span data-stu-id="abb70-118">2</span></span>    | <span data-ttu-id="abb70-119">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-119">Month</span></span> |   <span data-ttu-id="abb70-120">75</span><span class="sxs-lookup"><span data-stu-id="abb70-120">75</span></span>    |
   |   <span data-ttu-id="abb70-121">3</span><span class="sxs-lookup"><span data-stu-id="abb70-121">3</span></span>    | <span data-ttu-id="abb70-122">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-122">Month</span></span> |   <span data-ttu-id="abb70-123">50</span><span class="sxs-lookup"><span data-stu-id="abb70-123">50</span></span>    |
   |   <span data-ttu-id="abb70-124">4</span><span class="sxs-lookup"><span data-stu-id="abb70-124">4</span></span>    | <span data-ttu-id="abb70-125">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-125">Month</span></span> |   <span data-ttu-id="abb70-126">25</span><span class="sxs-lookup"><span data-stu-id="abb70-126">25</span></span>    |


2. <span data-ttu-id="abb70-127">Susiekite mažinimo raktą su prekės draudimo grupe.</span><span class="sxs-lookup"><span data-stu-id="abb70-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="abb70-128">Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Procentas – mažinimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="abb70-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="abb70-129">Sukurkite 1 000 vienetų per mėnesį poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="abb70-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="abb70-130">Jei prognozės planavimą paleisite sausio 1 d., poreikio prognozės poreikiai bus naudojami atsižvelgiant į procentus, nustatytus puslapyje **Mažinimo raktai**.</span><span class="sxs-lookup"><span data-stu-id="abb70-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="abb70-131">Toliau nurodyti poreikio kiekiai perkeliami į bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="abb70-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="abb70-132">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-132">Month</span></span>                | <span data-ttu-id="abb70-133">Reikalingas vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="abb70-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="abb70-134">sausio</span><span class="sxs-lookup"><span data-stu-id="abb70-134">January</span></span>              | <span data-ttu-id="abb70-135">0</span><span class="sxs-lookup"><span data-stu-id="abb70-135">0</span></span>                         |
| <span data-ttu-id="abb70-136">Vasaris</span><span class="sxs-lookup"><span data-stu-id="abb70-136">February</span></span>             | <span data-ttu-id="abb70-137">250</span><span class="sxs-lookup"><span data-stu-id="abb70-137">250</span></span>                       |
| <span data-ttu-id="abb70-138">Kovas</span><span class="sxs-lookup"><span data-stu-id="abb70-138">March</span></span>                | <span data-ttu-id="abb70-139">500</span><span class="sxs-lookup"><span data-stu-id="abb70-139">500</span></span>                       |
| <span data-ttu-id="abb70-140">Balandžio</span><span class="sxs-lookup"><span data-stu-id="abb70-140">April</span></span>                | <span data-ttu-id="abb70-141">750</span><span class="sxs-lookup"><span data-stu-id="abb70-141">750</span></span>                       |
| <span data-ttu-id="abb70-142">Gegužė–gruodis</span><span class="sxs-lookup"><span data-stu-id="abb70-142">May through December</span></span> | <span data-ttu-id="abb70-143">1000</span><span class="sxs-lookup"><span data-stu-id="abb70-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="abb70-144">2 pavyzdys: operacijų mažinimo rakto prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="abb70-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="abb70-145">Šiame pavyzdyje parodoma, kaip faktiniai užsakymai, vykdomi per laikotarpius, kuriuos nurodo mažinimo raktas, sumažina poreikio prognozės poreikius.</span><span class="sxs-lookup"><span data-stu-id="abb70-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="abb70-146">Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Operacijos – mažinimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="abb70-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="abb70-147">Sausio 1 d. yra toliau nurodyti pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="abb70-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="abb70-148">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-148">Month</span></span>    | <span data-ttu-id="abb70-149">Užsakytų vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="abb70-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="abb70-150">sausio</span><span class="sxs-lookup"><span data-stu-id="abb70-150">January</span></span>  | <span data-ttu-id="abb70-151">956</span><span class="sxs-lookup"><span data-stu-id="abb70-151">956</span></span>                      |
| <span data-ttu-id="abb70-152">Vasaris</span><span class="sxs-lookup"><span data-stu-id="abb70-152">February</span></span> | <span data-ttu-id="abb70-153">1 176</span><span class="sxs-lookup"><span data-stu-id="abb70-153">1,176</span></span>                    |
| <span data-ttu-id="abb70-154">Kovas</span><span class="sxs-lookup"><span data-stu-id="abb70-154">March</span></span>    | <span data-ttu-id="abb70-155">451</span><span class="sxs-lookup"><span data-stu-id="abb70-155">451</span></span>                      |
| <span data-ttu-id="abb70-156">Balandis</span><span class="sxs-lookup"><span data-stu-id="abb70-156">April</span></span>    | <span data-ttu-id="abb70-157">119</span><span class="sxs-lookup"><span data-stu-id="abb70-157">119</span></span>                      |

<span data-ttu-id="abb70-158">Jei naudojate tą pačią 1 000 vienetų per mėnesį poreikio prognozę, į bendrąjį planą perkeliami toliau nurodyti poreikio kiekiai.</span><span class="sxs-lookup"><span data-stu-id="abb70-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="abb70-159">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="abb70-159">Month</span></span>                | <span data-ttu-id="abb70-160">Reikalingas vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="abb70-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="abb70-161">sausio</span><span class="sxs-lookup"><span data-stu-id="abb70-161">January</span></span>              | <span data-ttu-id="abb70-162">44</span><span class="sxs-lookup"><span data-stu-id="abb70-162">44</span></span>                        |
| <span data-ttu-id="abb70-163">Vasaris</span><span class="sxs-lookup"><span data-stu-id="abb70-163">February</span></span>             | <span data-ttu-id="abb70-164">0</span><span class="sxs-lookup"><span data-stu-id="abb70-164">0</span></span>                         |
| <span data-ttu-id="abb70-165">Kovas</span><span class="sxs-lookup"><span data-stu-id="abb70-165">March</span></span>                | <span data-ttu-id="abb70-166">549</span><span class="sxs-lookup"><span data-stu-id="abb70-166">549</span></span>                       |
| <span data-ttu-id="abb70-167">Balandžio</span><span class="sxs-lookup"><span data-stu-id="abb70-167">April</span></span>                | <span data-ttu-id="abb70-168">881</span><span class="sxs-lookup"><span data-stu-id="abb70-168">881</span></span>                       |
| <span data-ttu-id="abb70-169">Gegužė–gruodis</span><span class="sxs-lookup"><span data-stu-id="abb70-169">May through December</span></span> | <span data-ttu-id="abb70-170">1000</span><span class="sxs-lookup"><span data-stu-id="abb70-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="abb70-171">3 pavyzdys: operacijų dinaminio laikotarpio prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="abb70-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="abb70-172">Dažniausiai sistemos yra nustatomos taip, kad operacijos sumažintų poreikio prognozę per tam tikrus prognozės laikotarpius: savaites, mėnesius ir t. t.</span><span class="sxs-lookup"><span data-stu-id="abb70-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="abb70-173">Šie laikotarpiai yra nustatomi mažinimo rakte.</span><span class="sxs-lookup"><span data-stu-id="abb70-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="abb70-174">Tačiau laiko tarpas tarp dviejų poreikio prognozės eilučių taip pat gali *nurodyti* laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="abb70-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="abb70-175">Kurkite toliau nurodytų datų ir kiekių poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="abb70-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="abb70-176">Data</span><span class="sxs-lookup"><span data-stu-id="abb70-176">Date</span></span>       | <span data-ttu-id="abb70-177">Poreikio prognozė</span><span class="sxs-lookup"><span data-stu-id="abb70-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="abb70-178">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="abb70-178">January 1</span></span>  | <span data-ttu-id="abb70-179">1000</span><span class="sxs-lookup"><span data-stu-id="abb70-179">1,000</span></span>           |
   | <span data-ttu-id="abb70-180">Sausio 5 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-180">January 5</span></span>  | <span data-ttu-id="abb70-181">500</span><span class="sxs-lookup"><span data-stu-id="abb70-181">500</span></span>             |
   | <span data-ttu-id="abb70-182">Sausio 12 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-182">January 12</span></span> | <span data-ttu-id="abb70-183">1000</span><span class="sxs-lookup"><span data-stu-id="abb70-183">1,000</span></span>           |

   <span data-ttu-id="abb70-184">Šioje prognozėje nėra aiškaus laikotarpio tarp prognozės datų: tarp pirmosios ir antrosios datų yra keturių dienų laikotarpis, o tarp antrosios ir trečiosios datų yra septynių dienų laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="abb70-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="abb70-185">Šie įvairūs laikotarpiai yra dinaminiai laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="abb70-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="abb70-186">Kurkite pardavimo užsakymo eilutes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="abb70-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="abb70-187">Data</span><span class="sxs-lookup"><span data-stu-id="abb70-187">Date</span></span>                             | <span data-ttu-id="abb70-188">Pardavimo užsakymo kiekis</span><span class="sxs-lookup"><span data-stu-id="abb70-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="abb70-189">Ankstesnių metų gruodžio 15 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-189">December 15 in the previous year</span></span> | <span data-ttu-id="abb70-190">500</span><span class="sxs-lookup"><span data-stu-id="abb70-190">500</span></span>                  |
   | <span data-ttu-id="abb70-191">Sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-191">January 3</span></span>                        | <span data-ttu-id="abb70-192">100</span><span class="sxs-lookup"><span data-stu-id="abb70-192">100</span></span>                  |
   | <span data-ttu-id="abb70-193">Sausio 10 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-193">January 10</span></span>                       | <span data-ttu-id="abb70-194">200</span><span class="sxs-lookup"><span data-stu-id="abb70-194">200</span></span>                  |

<span data-ttu-id="abb70-195">Prognozė bus sumažinama, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="abb70-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="abb70-196">Pirmasis pardavimo užsakymas nepatenka į jokį laikotarpį, todėl jis nesumažins jokios prognozės.</span><span class="sxs-lookup"><span data-stu-id="abb70-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="abb70-197">Antrasis pardavimo užsakymas yra tarp sausio 1 d. ir sausio 5 d., todėl jis sumažins sausio 1 d. prognozę 100.</span><span class="sxs-lookup"><span data-stu-id="abb70-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="abb70-198">Trečiasis pardavimo užsakymas yra tarp sausio 5 d. ir sausio 12 d., todėl jis sumažins sausio 5 d. prognozę 200.</span><span class="sxs-lookup"><span data-stu-id="abb70-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="abb70-199">Prognozei įvykdyti bus sukurtas toliau nurodytas suplanuotas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abb70-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="abb70-200">Poreikio prognozės data</span><span class="sxs-lookup"><span data-stu-id="abb70-200">Demand forecast date</span></span> | <span data-ttu-id="abb70-201">Sumažintas kiekis</span><span class="sxs-lookup"><span data-stu-id="abb70-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="abb70-202">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="abb70-202">January 1</span></span>            | <span data-ttu-id="abb70-203">900</span><span class="sxs-lookup"><span data-stu-id="abb70-203">900</span></span>              |
| <span data-ttu-id="abb70-204">Sausio 5 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-204">January 5</span></span>            | <span data-ttu-id="abb70-205">300</span><span class="sxs-lookup"><span data-stu-id="abb70-205">300</span></span>              |
| <span data-ttu-id="abb70-206">Sausio 12 d.</span><span class="sxs-lookup"><span data-stu-id="abb70-206">January 12</span></span>           | <span data-ttu-id="abb70-207">1000</span><span class="sxs-lookup"><span data-stu-id="abb70-207">1,000</span></span>            |

<span data-ttu-id="abb70-208">Toliau pateikiama sumažinimo **Operacijos – dinaminis laikotarpis** suvestinė.</span><span class="sxs-lookup"><span data-stu-id="abb70-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="abb70-209">Prognozės poreikius sumažina faktinės užsakymo operacijos, vykdomos dinaminio laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="abb70-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="abb70-210">Dinaminis laikotarpis apima dabartinės prognozės datas ir baigiasi, kai prasideda kita prognozė.</span><span class="sxs-lookup"><span data-stu-id="abb70-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="abb70-211">Naudojant šį metodą mažinimo raktas nėra reikalingas.</span><span class="sxs-lookup"><span data-stu-id="abb70-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="abb70-212">Naudojant šią parinktį, įvyksta toliau pateikti scenarijai.</span><span class="sxs-lookup"><span data-stu-id="abb70-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="abb70-213">Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="abb70-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="abb70-214">Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.</span><span class="sxs-lookup"><span data-stu-id="abb70-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="abb70-215">Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.</span><span class="sxs-lookup"><span data-stu-id="abb70-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="abb70-216">Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.</span><span class="sxs-lookup"><span data-stu-id="abb70-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="abb70-217">Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="abb70-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="abb70-218">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="abb70-218">Additional resources</span></span>
--------

[<span data-ttu-id="abb70-219">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="abb70-219">Master plans</span></span>](master-plans.md)



