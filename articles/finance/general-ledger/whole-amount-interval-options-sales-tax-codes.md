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
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0414f835b7797d2ed554f8d9dbd95b2ad47bba43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234122"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="65efa-103">Visa suma ir PVM kodų intervalo skaičiavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="65efa-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65efa-104">Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.</span><span class="sxs-lookup"><span data-stu-id="65efa-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="65efa-105">Galite nustatyti, kad PVM kodas būtų skaičiuojamas pagal visą sumą arba intervalo sumą.</span><span class="sxs-lookup"><span data-stu-id="65efa-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="65efa-106">PVM kodų puslapyje „FastTab“ skirtuko Skaičiavimas lauke Skaičiavimo metodas pasirinkite, kaip skaičiuoti PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="65efa-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="65efa-107">Visa suma – mokesčio tarifas taikomas visai apmokestinamai sumai.</span><span class="sxs-lookup"><span data-stu-id="65efa-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="65efa-108">Intervalas – apmokestinama suma skirstoma į dalis, kiekviena iš jų patenka į intervalą, kuris turi tam tikrą PVM tarifą.</span><span class="sxs-lookup"><span data-stu-id="65efa-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="65efa-109">Sumos dalis, kuri patenka į tam tikrą intervalą, apmokestinama pagal to intervalo mokesčių tarifą.</span><span class="sxs-lookup"><span data-stu-id="65efa-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="65efa-110">PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.</span><span class="sxs-lookup"><span data-stu-id="65efa-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="65efa-111">Parinktis Intervalas galima tik puslapio DK parametrai srities PVM lauke Skaičiavimo metodas pasirinkus Eilutė.</span><span class="sxs-lookup"><span data-stu-id="65efa-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="65efa-112">Intervalai nustatomi puslapyje PVM kodo reikšmės įvedant mokesčio tarifo žemiausią ir aukščiausią ribines sumas.</span><span class="sxs-lookup"><span data-stu-id="65efa-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="65efa-113">Siekiant apskaičiuoti visų apmokestinamų sumų mokesčius (nepaisant to, koks pasirinktas skaičiavimo metodas) intervalai turi atitikti šiuos reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="65efa-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="65efa-114">Mažiausia primojo intervalo turi būti riba – nulis.</span><span class="sxs-lookup"><span data-stu-id="65efa-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="65efa-115">Paskutinio intervalo aukščiausia riba turi būti nulis, tai reiškia begalybę.</span><span class="sxs-lookup"><span data-stu-id="65efa-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="65efa-116">Aukščiausia intervalo riba turi būti žemiausia kito intervalo riba.</span><span class="sxs-lookup"><span data-stu-id="65efa-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="65efa-117">Jei suma yra aukščiausia ankstesnio intervalo riba ir žemiausia kito intervalo riba, tai sumai bus taikomas pirmojo intervalo PVM tarifas.</span><span class="sxs-lookup"><span data-stu-id="65efa-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="65efa-118">Jei suma nepatenka į intervalus, kuriuos nustato apatinės ir viršutinės ribos, taikomas PVM tarifas yra nulis.</span><span class="sxs-lookup"><span data-stu-id="65efa-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="65efa-119">Pavyzdys: bendros sumos skaičiavimo metodas</span><span class="sxs-lookup"><span data-stu-id="65efa-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="65efa-120">Puslapyje PVM kodų vertės PVM tarifai nustatomi šiais intervalais:</span><span class="sxs-lookup"><span data-stu-id="65efa-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="65efa-121">**Minimali riba**</span><span class="sxs-lookup"><span data-stu-id="65efa-121">**Minimum limit**</span></span> | <span data-ttu-id="65efa-122">**Aukščiausia riba**</span><span class="sxs-lookup"><span data-stu-id="65efa-122">**Maximum limit**</span></span> | <span data-ttu-id="65efa-123">**Mokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="65efa-123">**Tax rate**</span></span> |
| <span data-ttu-id="65efa-124">0,00</span><span class="sxs-lookup"><span data-stu-id="65efa-124">0.00</span></span>              | <span data-ttu-id="65efa-125">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-125">50.00</span></span>             | <span data-ttu-id="65efa-126">30 %</span><span class="sxs-lookup"><span data-stu-id="65efa-126">30%</span></span>          |
| <span data-ttu-id="65efa-127">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-127">50.00</span></span>             | <span data-ttu-id="65efa-128">100,00</span><span class="sxs-lookup"><span data-stu-id="65efa-128">100.00</span></span>            | <span data-ttu-id="65efa-129">20 %</span><span class="sxs-lookup"><span data-stu-id="65efa-129">20%</span></span>          |
| <span data-ttu-id="65efa-130">100,00</span><span class="sxs-lookup"><span data-stu-id="65efa-130">100.00</span></span>            | <span data-ttu-id="65efa-131">0,00</span><span class="sxs-lookup"><span data-stu-id="65efa-131">0.00</span></span>              | <span data-ttu-id="65efa-132">10 %</span><span class="sxs-lookup"><span data-stu-id="65efa-132">10%</span></span>          |

<span data-ttu-id="65efa-133">PVM skaičiuojamas visai apmokestinamai sumai.</span><span class="sxs-lookup"><span data-stu-id="65efa-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="65efa-134">Apmokestinama suma (kaina)</span><span class="sxs-lookup"><span data-stu-id="65efa-134">Taxable amount (price)</span></span> | <span data-ttu-id="65efa-135">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="65efa-135">Calculation</span></span>    | <span data-ttu-id="65efa-136">PVM</span><span class="sxs-lookup"><span data-stu-id="65efa-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="65efa-137">35,00</span><span class="sxs-lookup"><span data-stu-id="65efa-137">35.00</span></span>                  | <span data-ttu-id="65efa-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="65efa-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="65efa-139">10,50</span><span class="sxs-lookup"><span data-stu-id="65efa-139">10.50</span></span>     |
| <span data-ttu-id="65efa-140">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-140">50.00</span></span>                  | <span data-ttu-id="65efa-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="65efa-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="65efa-142">15,00</span><span class="sxs-lookup"><span data-stu-id="65efa-142">15.00</span></span>     |
| <span data-ttu-id="65efa-143">85,00</span><span class="sxs-lookup"><span data-stu-id="65efa-143">85.00</span></span>                  | <span data-ttu-id="65efa-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="65efa-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="65efa-145">17,00</span><span class="sxs-lookup"><span data-stu-id="65efa-145">17.00</span></span>     |
| <span data-ttu-id="65efa-146">305,00</span><span class="sxs-lookup"><span data-stu-id="65efa-146">305.00</span></span>                 | <span data-ttu-id="65efa-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="65efa-147">305.00 \* 0.10</span></span> | <span data-ttu-id="65efa-148">30,50</span><span class="sxs-lookup"><span data-stu-id="65efa-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="65efa-149"> Pavyzdys: intervalinis skaičiavimo metodas</span><span class="sxs-lookup"><span data-stu-id="65efa-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="65efa-150">Puslapyje Reikšmės PVM tarifai yra nustatomi šiais intervalais:</span><span class="sxs-lookup"><span data-stu-id="65efa-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="65efa-151">**Minimali riba**</span><span class="sxs-lookup"><span data-stu-id="65efa-151">**Minimum limit**</span></span> | <span data-ttu-id="65efa-152">**Aukščiausia riba**</span><span class="sxs-lookup"><span data-stu-id="65efa-152">**Maximum limit**</span></span> | <span data-ttu-id="65efa-153">**Mokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="65efa-153">**Tax rate**</span></span> |
| <span data-ttu-id="65efa-154">0,00</span><span class="sxs-lookup"><span data-stu-id="65efa-154">0.00</span></span>              | <span data-ttu-id="65efa-155">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-155">50.00</span></span>             | <span data-ttu-id="65efa-156">30 %</span><span class="sxs-lookup"><span data-stu-id="65efa-156">30%</span></span>          |
| <span data-ttu-id="65efa-157">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-157">50.00</span></span>             | <span data-ttu-id="65efa-158">100,00</span><span class="sxs-lookup"><span data-stu-id="65efa-158">100.00</span></span>            | <span data-ttu-id="65efa-159">20 %</span><span class="sxs-lookup"><span data-stu-id="65efa-159">20%</span></span>          |
| <span data-ttu-id="65efa-160">100,00</span><span class="sxs-lookup"><span data-stu-id="65efa-160">100.00</span></span>            | <span data-ttu-id="65efa-161">0,00</span><span class="sxs-lookup"><span data-stu-id="65efa-161">0.00</span></span>              | <span data-ttu-id="65efa-162">10 %</span><span class="sxs-lookup"><span data-stu-id="65efa-162">10%</span></span>          |

<span data-ttu-id="65efa-163">PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.</span><span class="sxs-lookup"><span data-stu-id="65efa-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="65efa-164">Apmokestinama suma (kaina)</span><span class="sxs-lookup"><span data-stu-id="65efa-164">Taxable amount (price)</span></span> | <span data-ttu-id="65efa-165">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="65efa-165">Calculation</span></span>                                                               | <span data-ttu-id="65efa-166">PVM</span><span class="sxs-lookup"><span data-stu-id="65efa-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="65efa-167">35,00</span><span class="sxs-lookup"><span data-stu-id="65efa-167">35.00</span></span>                  | <span data-ttu-id="65efa-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="65efa-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="65efa-169">10,50</span><span class="sxs-lookup"><span data-stu-id="65efa-169">10.50</span></span>     |
| <span data-ttu-id="65efa-170">50,00</span><span class="sxs-lookup"><span data-stu-id="65efa-170">50.00</span></span>                  | <span data-ttu-id="65efa-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="65efa-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="65efa-172">15,00</span><span class="sxs-lookup"><span data-stu-id="65efa-172">15.00</span></span>     |
| <span data-ttu-id="65efa-173">85,00</span><span class="sxs-lookup"><span data-stu-id="65efa-173">85.00</span></span>                  | <span data-ttu-id="65efa-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="65efa-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="65efa-175">22,00</span><span class="sxs-lookup"><span data-stu-id="65efa-175">22.00</span></span>     |
| <span data-ttu-id="65efa-176">305,00</span><span class="sxs-lookup"><span data-stu-id="65efa-176">305.00</span></span>                 | <span data-ttu-id="65efa-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="65efa-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="65efa-178">45.50</span><span class="sxs-lookup"><span data-stu-id="65efa-178">45.50</span></span>     |



<span data-ttu-id="65efa-179">Daugiau informacijos žr. [PVM tarifų nustatymas pagal bazinės ribos ir skaičiavimo metodus](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="65efa-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]