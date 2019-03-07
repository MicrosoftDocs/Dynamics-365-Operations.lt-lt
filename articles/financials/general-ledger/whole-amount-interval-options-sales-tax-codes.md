---
title: Visa suma ir PVM kodų intervalo skaičiavimo parinktys
description: Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ea19a6d3cfea325281f301e0502bb051381d9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344069"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="08d47-103">Visa suma ir PVM kodų intervalo skaičiavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="08d47-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="08d47-104">Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.</span><span class="sxs-lookup"><span data-stu-id="08d47-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="08d47-105">Galite nustatyti, kad PVM kodas būtų skaičiuojamas pagal visą sumą arba intervalo sumą.</span><span class="sxs-lookup"><span data-stu-id="08d47-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="08d47-106">PVM kodų puslapyje „FastTab“ skirtuko Skaičiavimas lauke Skaičiavimo metodas pasirinkite, kaip skaičiuoti PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="08d47-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="08d47-107">Visa suma – mokesčio tarifas taikomas visai apmokestinamai sumai.</span><span class="sxs-lookup"><span data-stu-id="08d47-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="08d47-108">Intervalas – apmokestinama suma skirstoma į dalis, kiekviena iš jų patenka į intervalą, kuris turi tam tikrą PVM tarifą.</span><span class="sxs-lookup"><span data-stu-id="08d47-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="08d47-109">Sumos dalis, kuri patenka į tam tikrą intervalą, apmokestinama pagal to intervalo mokesčių tarifą.</span><span class="sxs-lookup"><span data-stu-id="08d47-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="08d47-110">PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.</span><span class="sxs-lookup"><span data-stu-id="08d47-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="08d47-111">Parinktis Intervalas galima tik puslapio DK parametrai srities PVM lauke Skaičiavimo metodas pasirinkus Eilutė.</span><span class="sxs-lookup"><span data-stu-id="08d47-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="08d47-112">Intervalai nustatomi puslapyje PVM kodo reikšmės įvedant mokesčio tarifo žemiausią ir aukščiausią ribines sumas.</span><span class="sxs-lookup"><span data-stu-id="08d47-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="08d47-113">Siekiant apskaičiuoti visų apmokestinamų sumų mokesčius (nepaisant to, koks pasirinktas skaičiavimo metodas) intervalai turi atitikti šiuos reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="08d47-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="08d47-114">Mažiausia primojo intervalo turi būti riba – nulis.</span><span class="sxs-lookup"><span data-stu-id="08d47-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="08d47-115">Paskutinio intervalo aukščiausia riba turi būti nulis, tai reiškia begalybę.</span><span class="sxs-lookup"><span data-stu-id="08d47-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="08d47-116">Aukščiausia intervalo riba turi būti žemiausia kito intervalo riba.</span><span class="sxs-lookup"><span data-stu-id="08d47-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="08d47-117">Jei suma yra aukščiausia ankstesnio intervalo riba ir žemiausia kito intervalo riba, tai sumai bus taikomas pirmojo intervalo PVM tarifas.</span><span class="sxs-lookup"><span data-stu-id="08d47-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="08d47-118">Jei suma nepatenka į intervalus, kuriuos nustato apatinės ir viršutinės ribos, taikomas PVM tarifas yra nulis.</span><span class="sxs-lookup"><span data-stu-id="08d47-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="08d47-119">Pavyzdys: bendros sumos skaičiavimo metodas</span><span class="sxs-lookup"><span data-stu-id="08d47-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="08d47-120">Puslapyje PVM kodų vertės PVM tarifai nustatomi šiais intervalais:</span><span class="sxs-lookup"><span data-stu-id="08d47-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="08d47-121">**Minimali riba**</span><span class="sxs-lookup"><span data-stu-id="08d47-121">**Minimum limit**</span></span> | <span data-ttu-id="08d47-122">**Aukščiausia riba**</span><span class="sxs-lookup"><span data-stu-id="08d47-122">**Maximum limit**</span></span> | <span data-ttu-id="08d47-123">**Mokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="08d47-123">**Tax rate**</span></span> |
| <span data-ttu-id="08d47-124">0,00</span><span class="sxs-lookup"><span data-stu-id="08d47-124">0.00</span></span>              | <span data-ttu-id="08d47-125">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-125">50.00</span></span>             | <span data-ttu-id="08d47-126">30 %</span><span class="sxs-lookup"><span data-stu-id="08d47-126">30%</span></span>          |
| <span data-ttu-id="08d47-127">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-127">50.00</span></span>             | <span data-ttu-id="08d47-128">100,00</span><span class="sxs-lookup"><span data-stu-id="08d47-128">100.00</span></span>            | <span data-ttu-id="08d47-129">20 %</span><span class="sxs-lookup"><span data-stu-id="08d47-129">20%</span></span>          |
| <span data-ttu-id="08d47-130">100,00</span><span class="sxs-lookup"><span data-stu-id="08d47-130">100.00</span></span>            | <span data-ttu-id="08d47-131">0,00</span><span class="sxs-lookup"><span data-stu-id="08d47-131">0.00</span></span>              | <span data-ttu-id="08d47-132">10 %</span><span class="sxs-lookup"><span data-stu-id="08d47-132">10%</span></span>          |

<span data-ttu-id="08d47-133">PVM skaičiuojamas visai apmokestinamai sumai.</span><span class="sxs-lookup"><span data-stu-id="08d47-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="08d47-134">Apmokestinama suma (kaina)</span><span class="sxs-lookup"><span data-stu-id="08d47-134">Taxable amount (price)</span></span> | <span data-ttu-id="08d47-135">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="08d47-135">Calculation</span></span>    | <span data-ttu-id="08d47-136">PVM</span><span class="sxs-lookup"><span data-stu-id="08d47-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="08d47-137">35,00</span><span class="sxs-lookup"><span data-stu-id="08d47-137">35.00</span></span>                  | <span data-ttu-id="08d47-138">{35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08d47-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="08d47-139">10,50</span><span class="sxs-lookup"><span data-stu-id="08d47-139">10.50</span></span>     |
| <span data-ttu-id="08d47-140">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-140">50.00</span></span>                  | <span data-ttu-id="08d47-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08d47-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="08d47-142">15,00</span><span class="sxs-lookup"><span data-stu-id="08d47-142">15.00</span></span>     |
| <span data-ttu-id="08d47-143">85,00</span><span class="sxs-lookup"><span data-stu-id="08d47-143">85.00</span></span>                  | <span data-ttu-id="08d47-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="08d47-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="08d47-145">17,00</span><span class="sxs-lookup"><span data-stu-id="08d47-145">17.00</span></span>     |
| <span data-ttu-id="08d47-146">305,00</span><span class="sxs-lookup"><span data-stu-id="08d47-146">305.00</span></span>                 | <span data-ttu-id="08d47-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="08d47-147">305.00 \* 0.10</span></span> | <span data-ttu-id="08d47-148">30,50</span><span class="sxs-lookup"><span data-stu-id="08d47-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="08d47-149"> Pavyzdys: intervalinis skaičiavimo metodas</span><span class="sxs-lookup"><span data-stu-id="08d47-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="08d47-150">Puslapyje Reikšmės PVM tarifai yra nustatomi šiais intervalais:</span><span class="sxs-lookup"><span data-stu-id="08d47-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="08d47-151">**Minimali riba**</span><span class="sxs-lookup"><span data-stu-id="08d47-151">**Minimum limit**</span></span> | <span data-ttu-id="08d47-152">**Aukščiausia riba**</span><span class="sxs-lookup"><span data-stu-id="08d47-152">**Maximum limit**</span></span> | <span data-ttu-id="08d47-153">**Mokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="08d47-153">**Tax rate**</span></span> |
| <span data-ttu-id="08d47-154">0,00</span><span class="sxs-lookup"><span data-stu-id="08d47-154">0.00</span></span>              | <span data-ttu-id="08d47-155">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-155">50.00</span></span>             | <span data-ttu-id="08d47-156">30 %</span><span class="sxs-lookup"><span data-stu-id="08d47-156">30%</span></span>          |
| <span data-ttu-id="08d47-157">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-157">50.00</span></span>             | <span data-ttu-id="08d47-158">100,00</span><span class="sxs-lookup"><span data-stu-id="08d47-158">100.00</span></span>            | <span data-ttu-id="08d47-159">20 %</span><span class="sxs-lookup"><span data-stu-id="08d47-159">20%</span></span>          |
| <span data-ttu-id="08d47-160">100,00</span><span class="sxs-lookup"><span data-stu-id="08d47-160">100.00</span></span>            | <span data-ttu-id="08d47-161">0,00</span><span class="sxs-lookup"><span data-stu-id="08d47-161">0.00</span></span>              | <span data-ttu-id="08d47-162">10 %</span><span class="sxs-lookup"><span data-stu-id="08d47-162">10%</span></span>          |

<span data-ttu-id="08d47-163">PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.</span><span class="sxs-lookup"><span data-stu-id="08d47-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="08d47-164">Apmokestinama suma (kaina)</span><span class="sxs-lookup"><span data-stu-id="08d47-164">Taxable amount (price)</span></span> | <span data-ttu-id="08d47-165">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="08d47-165">Calculation</span></span>                                                               | <span data-ttu-id="08d47-166">PVM</span><span class="sxs-lookup"><span data-stu-id="08d47-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="08d47-167">35,00</span><span class="sxs-lookup"><span data-stu-id="08d47-167">35.00</span></span>                  | <span data-ttu-id="08d47-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08d47-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="08d47-169">10,50</span><span class="sxs-lookup"><span data-stu-id="08d47-169">10.50</span></span>     |
| <span data-ttu-id="08d47-170">50,00</span><span class="sxs-lookup"><span data-stu-id="08d47-170">50.00</span></span>                  | <span data-ttu-id="08d47-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="08d47-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="08d47-172">15,00</span><span class="sxs-lookup"><span data-stu-id="08d47-172">15.00</span></span>     |
| <span data-ttu-id="08d47-173">85,00</span><span class="sxs-lookup"><span data-stu-id="08d47-173">85.00</span></span>                  | <span data-ttu-id="08d47-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="08d47-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="08d47-175">22,00</span><span class="sxs-lookup"><span data-stu-id="08d47-175">22.00</span></span>     |
| <span data-ttu-id="08d47-176">305,00</span><span class="sxs-lookup"><span data-stu-id="08d47-176">305.00</span></span>                 | <span data-ttu-id="08d47-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="08d47-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="08d47-178">45,50</span><span class="sxs-lookup"><span data-stu-id="08d47-178">45.50</span></span>     |



<span data-ttu-id="08d47-179">Daugiau informacijos žr. [PVM tarifų nustatymas pagal Bazinės ribos ir Skaičiavimo metodo laukus](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="08d47-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





