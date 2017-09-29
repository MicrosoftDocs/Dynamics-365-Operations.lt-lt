---
title: "Mažinimo raktai"
description: "Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą. Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus. Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 30634b0af343ad171c385a95c4ba0934180f70cf
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="f6c63-105">Mažinimo raktai</span><span class="sxs-lookup"><span data-stu-id="f6c63-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f6c63-106">Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą.</span><span class="sxs-lookup"><span data-stu-id="f6c63-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="f6c63-107">Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="f6c63-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="f6c63-108">Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius.</span><span class="sxs-lookup"><span data-stu-id="f6c63-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="f6c63-109">1 pavyzdys: procentas – mažinimo rakto prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="f6c63-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="f6c63-110">Šiame pavyzdyje parodoma, kaip mažinimo raktas sumažina poreikio prognozės poreikius pagal procentines dalis ir laikotarpius, kuriuos nurodo mažinimo raktas.</span><span class="sxs-lookup"><span data-stu-id="f6c63-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="f6c63-111">Puslapyje **Mažinimo raktai** nustatykite toliau nurodytas eilutes.</span><span class="sxs-lookup"><span data-stu-id="f6c63-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="f6c63-112">Grąža</span><span class="sxs-lookup"><span data-stu-id="f6c63-112">Change</span></span> | <span data-ttu-id="f6c63-113">Vienetas</span><span class="sxs-lookup"><span data-stu-id="f6c63-113">Unit</span></span>  | <span data-ttu-id="f6c63-114">Procentas</span><span class="sxs-lookup"><span data-stu-id="f6c63-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="f6c63-115">1</span><span class="sxs-lookup"><span data-stu-id="f6c63-115">1</span></span>      | <span data-ttu-id="f6c63-116">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-116">Month</span></span> | <span data-ttu-id="f6c63-117">100</span><span class="sxs-lookup"><span data-stu-id="f6c63-117">100</span></span>     |
    | <span data-ttu-id="f6c63-118">2</span><span class="sxs-lookup"><span data-stu-id="f6c63-118">2</span></span>      | <span data-ttu-id="f6c63-119">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-119">Month</span></span> | <span data-ttu-id="f6c63-120">75</span><span class="sxs-lookup"><span data-stu-id="f6c63-120">75</span></span>      |
    | <span data-ttu-id="f6c63-121">3</span><span class="sxs-lookup"><span data-stu-id="f6c63-121">3</span></span>      | <span data-ttu-id="f6c63-122">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-122">Month</span></span> | <span data-ttu-id="f6c63-123">50</span><span class="sxs-lookup"><span data-stu-id="f6c63-123">50</span></span>      |
    | <span data-ttu-id="f6c63-124">4</span><span class="sxs-lookup"><span data-stu-id="f6c63-124">4</span></span>      | <span data-ttu-id="f6c63-125">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-125">Month</span></span> | <span data-ttu-id="f6c63-126">25</span><span class="sxs-lookup"><span data-stu-id="f6c63-126">25</span></span>      |

2.  <span data-ttu-id="f6c63-127">Susiekite mažinimo raktą su prekės draudimo grupe.</span><span class="sxs-lookup"><span data-stu-id="f6c63-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="f6c63-128">Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Procentas – mažinimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="f6c63-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="f6c63-129">Sukurkite 1 000 vienetų per mėnesį poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="f6c63-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="f6c63-130">Jei prognozės planavimą paleisite sausio 1 d., poreikio prognozės poreikiai bus naudojami atsižvelgiant į procentus, nustatytus puslapyje **Mažinimo raktai**.</span><span class="sxs-lookup"><span data-stu-id="f6c63-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="f6c63-131">Toliau nurodyti poreikio kiekiai perkeliami į bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="f6c63-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="f6c63-132">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-132">Month</span></span>                | <span data-ttu-id="f6c63-133">Reikalingas vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="f6c63-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="f6c63-134">sausio</span><span class="sxs-lookup"><span data-stu-id="f6c63-134">January</span></span>              | <span data-ttu-id="f6c63-135">0</span><span class="sxs-lookup"><span data-stu-id="f6c63-135">0</span></span>                         |
| <span data-ttu-id="f6c63-136">Vasaris</span><span class="sxs-lookup"><span data-stu-id="f6c63-136">February</span></span>             | <span data-ttu-id="f6c63-137">250</span><span class="sxs-lookup"><span data-stu-id="f6c63-137">250</span></span>                       |
| <span data-ttu-id="f6c63-138">Kovas</span><span class="sxs-lookup"><span data-stu-id="f6c63-138">March</span></span>                | <span data-ttu-id="f6c63-139">500</span><span class="sxs-lookup"><span data-stu-id="f6c63-139">500</span></span>                       |
| <span data-ttu-id="f6c63-140">Balandžio</span><span class="sxs-lookup"><span data-stu-id="f6c63-140">April</span></span>                | <span data-ttu-id="f6c63-141">750</span><span class="sxs-lookup"><span data-stu-id="f6c63-141">750</span></span>                       |
| <span data-ttu-id="f6c63-142">Gegužė–gruodis</span><span class="sxs-lookup"><span data-stu-id="f6c63-142">May through December</span></span> | <span data-ttu-id="f6c63-143">1000</span><span class="sxs-lookup"><span data-stu-id="f6c63-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="f6c63-144">2 pavyzdys: operacijų mažinimo rakto prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="f6c63-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="f6c63-145">Šiame pavyzdyje parodoma, kaip faktiniai užsakymai, vykdomi per laikotarpius, kuriuos nurodo mažinimo raktas, sumažina poreikio prognozės poreikius.</span><span class="sxs-lookup"><span data-stu-id="f6c63-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="f6c63-146">Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Operacijos – mažinimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="f6c63-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="f6c63-147">Sausio 1 d. yra toliau nurodyti pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="f6c63-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="f6c63-148">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-148">Month</span></span>    | <span data-ttu-id="f6c63-149">Užsakytų vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="f6c63-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="f6c63-150">sausio</span><span class="sxs-lookup"><span data-stu-id="f6c63-150">January</span></span>  | <span data-ttu-id="f6c63-151">956</span><span class="sxs-lookup"><span data-stu-id="f6c63-151">956</span></span>                      |
| <span data-ttu-id="f6c63-152">Vasaris</span><span class="sxs-lookup"><span data-stu-id="f6c63-152">February</span></span> | <span data-ttu-id="f6c63-153">1 176</span><span class="sxs-lookup"><span data-stu-id="f6c63-153">1,176</span></span>                    |
| <span data-ttu-id="f6c63-154">Kovas</span><span class="sxs-lookup"><span data-stu-id="f6c63-154">March</span></span>    | <span data-ttu-id="f6c63-155">451</span><span class="sxs-lookup"><span data-stu-id="f6c63-155">451</span></span>                      |
| <span data-ttu-id="f6c63-156">Balandis</span><span class="sxs-lookup"><span data-stu-id="f6c63-156">April</span></span>    | <span data-ttu-id="f6c63-157">119</span><span class="sxs-lookup"><span data-stu-id="f6c63-157">119</span></span>                      |

<span data-ttu-id="f6c63-158">Jei naudojate tą pačią 1 000 vienetų per mėnesį poreikio prognozę, į bendrąjį planą perkeliami toliau nurodyti poreikio kiekiai.</span><span class="sxs-lookup"><span data-stu-id="f6c63-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="f6c63-159">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="f6c63-159">Month</span></span>                | <span data-ttu-id="f6c63-160">Reikalingas vienetų kiekis</span><span class="sxs-lookup"><span data-stu-id="f6c63-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="f6c63-161">sausio</span><span class="sxs-lookup"><span data-stu-id="f6c63-161">January</span></span>              | <span data-ttu-id="f6c63-162">44</span><span class="sxs-lookup"><span data-stu-id="f6c63-162">44</span></span>                        |
| <span data-ttu-id="f6c63-163">Vasaris</span><span class="sxs-lookup"><span data-stu-id="f6c63-163">February</span></span>             | <span data-ttu-id="f6c63-164">0</span><span class="sxs-lookup"><span data-stu-id="f6c63-164">0</span></span>                         |
| <span data-ttu-id="f6c63-165">Kovas</span><span class="sxs-lookup"><span data-stu-id="f6c63-165">March</span></span>                | <span data-ttu-id="f6c63-166">549</span><span class="sxs-lookup"><span data-stu-id="f6c63-166">549</span></span>                       |
| <span data-ttu-id="f6c63-167">Balandžio</span><span class="sxs-lookup"><span data-stu-id="f6c63-167">April</span></span>                | <span data-ttu-id="f6c63-168">881</span><span class="sxs-lookup"><span data-stu-id="f6c63-168">881</span></span>                       |
| <span data-ttu-id="f6c63-169">Gegužė–gruodis</span><span class="sxs-lookup"><span data-stu-id="f6c63-169">May through December</span></span> | <span data-ttu-id="f6c63-170">1000</span><span class="sxs-lookup"><span data-stu-id="f6c63-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="f6c63-171">3 pavyzdys: operacijų dinaminio laikotarpio prognozės mažinimo principas</span><span class="sxs-lookup"><span data-stu-id="f6c63-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="f6c63-172">Dažniausiai sistemos yra nustatomos taip, kad operacijos sumažintų poreikio prognozę per tam tikrus prognozės laikotarpius: savaites, mėnesius ir t. t.</span><span class="sxs-lookup"><span data-stu-id="f6c63-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="f6c63-173">Šie laikotarpiai yra nustatomi mažinimo rakte.</span><span class="sxs-lookup"><span data-stu-id="f6c63-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="f6c63-174">Tačiau laiko tarpas tarp dviejų poreikio prognozės eilučių taip pat gali *nurodyti* laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="f6c63-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="f6c63-175">Kurkite toliau nurodytų datų ir kiekių poreikio prognozę.</span><span class="sxs-lookup"><span data-stu-id="f6c63-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="f6c63-176">Data</span><span class="sxs-lookup"><span data-stu-id="f6c63-176">Date</span></span>       | <span data-ttu-id="f6c63-177">Poreikio prognozė</span><span class="sxs-lookup"><span data-stu-id="f6c63-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="f6c63-178">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="f6c63-178">January 1</span></span>  | <span data-ttu-id="f6c63-179">1000</span><span class="sxs-lookup"><span data-stu-id="f6c63-179">1,000</span></span>           |
    | <span data-ttu-id="f6c63-180">Sausio 5 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-180">January 5</span></span>  | <span data-ttu-id="f6c63-181">500</span><span class="sxs-lookup"><span data-stu-id="f6c63-181">500</span></span>             |
    | <span data-ttu-id="f6c63-182">Sausio 12 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-182">January 12</span></span> | <span data-ttu-id="f6c63-183">1000</span><span class="sxs-lookup"><span data-stu-id="f6c63-183">1,000</span></span>           |

    <span data-ttu-id="f6c63-184">Šioje prognozėje nėra aiškaus laikotarpio tarp prognozės datų: tarp pirmosios ir antrosios datų yra keturių dienų laikotarpis, o tarp antrosios ir trečiosios datų yra septynių dienų laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="f6c63-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="f6c63-185">Šie įvairūs laikotarpiai yra dinaminiai laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="f6c63-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="f6c63-186">Kurkite pardavimo užsakymo eilutes, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="f6c63-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="f6c63-187">Data</span><span class="sxs-lookup"><span data-stu-id="f6c63-187">Date</span></span>                             | <span data-ttu-id="f6c63-188">Pardavimo užsakymo kiekis</span><span class="sxs-lookup"><span data-stu-id="f6c63-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="f6c63-189">Ankstesnių metų gruodžio 15 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-189">December 15 in the previous year</span></span> | <span data-ttu-id="f6c63-190">500</span><span class="sxs-lookup"><span data-stu-id="f6c63-190">500</span></span>                  |
    | <span data-ttu-id="f6c63-191">Sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-191">January 3</span></span>                        | <span data-ttu-id="f6c63-192">100</span><span class="sxs-lookup"><span data-stu-id="f6c63-192">100</span></span>                  |
    | <span data-ttu-id="f6c63-193">Sausio 10 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-193">January 10</span></span>                       | <span data-ttu-id="f6c63-194">200</span><span class="sxs-lookup"><span data-stu-id="f6c63-194">200</span></span>                  |

<span data-ttu-id="f6c63-195">Prognozė bus sumažinama, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="f6c63-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="f6c63-196">Pirmasis pardavimo užsakymas nepatenka į jokį laikotarpį, todėl jis nesumažins jokios prognozės.</span><span class="sxs-lookup"><span data-stu-id="f6c63-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="f6c63-197">Antrasis pardavimo užsakymas yra tarp sausio 1 d. ir sausio 5 d., todėl jis sumažins sausio 1 d. prognozę 100.</span><span class="sxs-lookup"><span data-stu-id="f6c63-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="f6c63-198">Trečiasis pardavimo užsakymas yra tarp sausio 5 d. ir sausio 12 d., todėl jis sumažins sausio 5 d. prognozę 200.</span><span class="sxs-lookup"><span data-stu-id="f6c63-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="f6c63-199">Prognozei įvykdyti bus sukurtas toliau nurodytas suplanuotas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f6c63-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="f6c63-200">Poreikio prognozės data</span><span class="sxs-lookup"><span data-stu-id="f6c63-200">Demand forecast date</span></span> | <span data-ttu-id="f6c63-201">Sumažintas kiekis</span><span class="sxs-lookup"><span data-stu-id="f6c63-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="f6c63-202">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="f6c63-202">January 1</span></span>            | <span data-ttu-id="f6c63-203">900</span><span class="sxs-lookup"><span data-stu-id="f6c63-203">900</span></span>              |
| <span data-ttu-id="f6c63-204">Sausio 5 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-204">January 5</span></span>            | <span data-ttu-id="f6c63-205">300</span><span class="sxs-lookup"><span data-stu-id="f6c63-205">300</span></span>              |
| <span data-ttu-id="f6c63-206">Sausio 12 d.</span><span class="sxs-lookup"><span data-stu-id="f6c63-206">January 12</span></span>           | <span data-ttu-id="f6c63-207">1000</span><span class="sxs-lookup"><span data-stu-id="f6c63-207">1,000</span></span>            |

<span data-ttu-id="f6c63-208">Toliau pateikiama sumažinimo **Operacijos – dinaminis laikotarpis** suvestinė.</span><span class="sxs-lookup"><span data-stu-id="f6c63-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="f6c63-209">Prognozės poreikius sumažina faktinės užsakymo operacijos, vykdomos dinaminio laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="f6c63-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="f6c63-210">Dinaminis laikotarpis apima dabartinės prognozės datas ir baigiasi, kai prasideda kita prognozė.</span><span class="sxs-lookup"><span data-stu-id="f6c63-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="f6c63-211">Naudojant šį metodą mažinimo raktas nėra reikalingas.</span><span class="sxs-lookup"><span data-stu-id="f6c63-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="f6c63-212">Naudojant šią parinktį, įvyksta toliau pateikti scenarijai.</span><span class="sxs-lookup"><span data-stu-id="f6c63-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="f6c63-213">Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="f6c63-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="f6c63-214">Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.</span><span class="sxs-lookup"><span data-stu-id="f6c63-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="f6c63-215">Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.</span><span class="sxs-lookup"><span data-stu-id="f6c63-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="f6c63-216">Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.</span><span class="sxs-lookup"><span data-stu-id="f6c63-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="f6c63-217">Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="f6c63-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="f6c63-218">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f6c63-218">See also</span></span>
--------

[<span data-ttu-id="f6c63-219">Bendrieji planai</span><span class="sxs-lookup"><span data-stu-id="f6c63-219">Master plans</span></span>](master-plans.md)




