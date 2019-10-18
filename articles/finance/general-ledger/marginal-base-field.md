---
title: PVM tarifai pagal bazinę ribą ir skaičiavimo metodus
description: Šioje temoje aiškinama, kaip naudojant vertes laukuose Bazinės ribos ir Skaičiavimo metodas nustatomas (-i) pardavimo ir pirkimo operacijų mokesčių tarifas (-ai).
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178983"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="c00bc-103">PVM tarifai pagal bazinę ribą ir skaičiavimo metodus</span><span class="sxs-lookup"><span data-stu-id="c00bc-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c00bc-104">Šioje temoje aiškinama, kaip naudojant vertes laukuose Bazinės ribos ir Skaičiavimo metodas nustatomas (-i) pardavimo ir pirkimo operacijų mokesčių tarifas (-ai).</span><span class="sxs-lookup"><span data-stu-id="c00bc-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="c00bc-105">Puslapio PVM kodai Skaičiavimo „FastTab‟ Bazinės ribos laukas nustato, kuri suma naudojama parinkti tinkamam mokesčio tarifui (-ams) iš tarifų PVM kodų reikšmių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c00bc-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="c00bc-106">Sumos tipas lauke Bazinė riba kartu su lauko Skaičiavimo metodas metodu nustato logiką, kuria ieškoma tinkamo operacijos mokesčio tarifo (-ų).</span><span class="sxs-lookup"><span data-stu-id="c00bc-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="c00bc-107">Kaip pateikta toliau esančiuose pavyzdžiuose, šiuose laukuose naudojant įvairias verčių kombinacijas, gaunami labai skirtingi PVM skaičiavimų rezultatai.</span><span class="sxs-lookup"><span data-stu-id="c00bc-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="c00bc-108">Pavyzdžiuose naudojamos tos pačios mokesčių intervalo reikšmės, puslapyje PVM kodų reikšmės nustatytos kiekvienam mokesčio kodui.</span><span class="sxs-lookup"><span data-stu-id="c00bc-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="c00bc-109">Norėdami atidaryti šį puslapį, puslapyje PVM kodai spustelėkite PVM kodas &gt; Reikšmės.</span><span class="sxs-lookup"><span data-stu-id="c00bc-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="c00bc-110">Jei vieno ar kelių jūsų PVM kodų Bazinė riba paremta eilučių sumomis ar vienetais, lauko Skaičiavimo metodas, esančio DK parametrų puslapyje, reikšmė, turi būti nustatyta į Eilutė.</span><span class="sxs-lookup"><span data-stu-id="c00bc-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="c00bc-111"> Grynoji kiekvienos eilutės suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-111">Net amount per line</span></span>
<span data-ttu-id="c00bc-112">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal SF eilučių grynąją sumą, išskyrus bet kokius kitus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-113">Example</span></span>

<span data-ttu-id="c00bc-114">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-115">Sumos intervalas</span><span class="sxs-lookup"><span data-stu-id="c00bc-115">Amount interval</span></span>    | <span data-ttu-id="c00bc-116">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="c00bc-117">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-117">0 - 50</span></span>             | <span data-ttu-id="c00bc-118">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-118">30%</span></span>      |
| <span data-ttu-id="c00bc-119">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-119">50 - 100</span></span>           | <span data-ttu-id="c00bc-120">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-120">20%</span></span>      |
| <span data-ttu-id="c00bc-121">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-122">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="c00bc-123">Viršutinė paskutinio intervalo riba nulis (0) reiškia, kad į intervalą įtraukiamos visos sumos, viršijančios 100.</span><span class="sxs-lookup"><span data-stu-id="c00bc-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="c00bc-124">Bazinė riba: **Grynoji kiekvienos eilutės suma**</span><span class="sxs-lookup"><span data-stu-id="c00bc-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="c00bc-125">Skaičiavimo metodas: **Intervalas**</span><span class="sxs-lookup"><span data-stu-id="c00bc-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="c00bc-126">Perkate 8 lempas, kurių kiekviena kainuoja 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="c00bc-127">Grynoji SF eilutės suma yra 200,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="c00bc-128">Mokestis apskaičiuojamas taip:</span><span class="sxs-lookup"><span data-stu-id="c00bc-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="c00bc-129">Bendra PVM suma = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="c00bc-130">Bendra SF suma = 200,00 + 35,00 = 235,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="c00bc-131">**Nuokrypis**</span><span class="sxs-lookup"><span data-stu-id="c00bc-131">**Variation**</span></span> 

<span data-ttu-id="c00bc-132">Jei SF yra dvi eilutės, kurių kiekvienoje – keturios prekės, kiekvienos eilutės grynoji suma yra 100,00, o PVM apskaičiuojamas taip:</span><span class="sxs-lookup"><span data-stu-id="c00bc-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="c00bc-133">1 PVM eilutė = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="c00bc-134">2 PVM eilutė = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="c00bc-135">Bendras PVM = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="c00bc-136">Bendra SF suma = 200,00 + 50,00 = 250,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="c00bc-137"> Grynoji kiekvieno vieneto suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-137">Net amount per unit</span></span>
<span data-ttu-id="c00bc-138">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal kiekvieno vieneto vertę, išskyrus bet kokius kitus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="c00bc-139">Kai pasirenkama vienetu paremta Bazinė riba, taip pat turi būti nurodytas PVM kodo Vienetas.</span><span class="sxs-lookup"><span data-stu-id="c00bc-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-140">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-140">Example</span></span>

<span data-ttu-id="c00bc-141">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-142">Suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-142">Amount</span></span>             | <span data-ttu-id="c00bc-143">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="c00bc-144">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-144">0 - 50</span></span>             | <span data-ttu-id="c00bc-145">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-145">30%</span></span>      |
| <span data-ttu-id="c00bc-146">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-146">50 - 100</span></span>           | <span data-ttu-id="c00bc-147">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-147">20%</span></span>      |
| <span data-ttu-id="c00bc-148">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-149">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-149">10%</span></span>      |

<span data-ttu-id="c00bc-150">Bazinė riba: **Grynoji kiekvieno vieneto suma**</span><span class="sxs-lookup"><span data-stu-id="c00bc-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="c00bc-151">Skaičiavimo metodas: **Visa suma**</span><span class="sxs-lookup"><span data-stu-id="c00bc-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="c00bc-152">Perkate 8 lempas, kurių kiekviena kainuoja 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="c00bc-153">Grynoji SF eilutės suma yra 200,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="c00bc-154">Mokestis apskaičiuojamas taip: Vieneto PVM = 25,00 x 30 % = 7,50 Bendras PVM = 7,50 x 8 vienetai = 60,00 Bendroji SF suma = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="c00bc-155"> Grynoji SF balanso suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-155">Net amount of invoice balance</span></span>

<span data-ttu-id="c00bc-156">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal visą SF vertę, išskyrus bet kokius kitus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-157">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-157">Example</span></span>

<span data-ttu-id="c00bc-158">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-159">Suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-159">Amount</span></span>            | <span data-ttu-id="c00bc-160">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="c00bc-161">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-161">0 - 50</span></span>            | <span data-ttu-id="c00bc-162">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-162">30%</span></span>      |
| <span data-ttu-id="c00bc-163">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-163">50 - 100</span></span>          | <span data-ttu-id="c00bc-164">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-164">20%</span></span>      |
| <span data-ttu-id="c00bc-165">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-166">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-166">10%</span></span>      |

<span data-ttu-id="c00bc-167">Bazinė riba: **Grynoji SF balanso suma**</span><span class="sxs-lookup"><span data-stu-id="c00bc-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="c00bc-168">Skaičiavimo metodas: **Intervalas** Pardavimo SF yra 2 eilutės, kurių kiekvienoje – 4 lempos po 25,00 už vienetą.</span><span class="sxs-lookup"><span data-stu-id="c00bc-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="c00bc-169">Grynoji SF balanso suma yra 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="c00bc-170">Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Bendra SF suma = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="c00bc-171"> Bendra suma pagal eilutę</span><span class="sxs-lookup"><span data-stu-id="c00bc-171">Gross amount per line</span></span>

<span data-ttu-id="c00bc-172">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal eilutės vertę, įtraukiant visus kitus tos eilutės mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="c00bc-173">PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba.</span><span class="sxs-lookup"><span data-stu-id="c00bc-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-174">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-174">Example</span></span>

<span data-ttu-id="c00bc-175">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-176">Suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-176">Amount</span></span>             | <span data-ttu-id="c00bc-177">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="c00bc-178">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-178">0 - 50</span></span>             | <span data-ttu-id="c00bc-179">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-179">30%</span></span>      |
| <span data-ttu-id="c00bc-180">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-180">50 - 100</span></span>           | <span data-ttu-id="c00bc-181">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-181">20%</span></span>      |
| <span data-ttu-id="c00bc-182">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-183">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-183">10%</span></span>      |

<span data-ttu-id="c00bc-184">Bazinė riba: **Bendra suma pagal eilutę** Skaičiavimo metodas: **Intervalas** Dar yra apskaičiuotas kitas mokesčio kodas už specialų muitą – 5,00 už kiekvieną lempą.</span><span class="sxs-lookup"><span data-stu-id="c00bc-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="c00bc-185">Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos.</span><span class="sxs-lookup"><span data-stu-id="c00bc-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="c00bc-186">Perkate 8 lempas, kurių kiekviena kainuoja 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="c00bc-187">Grynoji SF eilutės suma yra 200,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="c00bc-188">Bendra SF eilutės suma yra 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="c00bc-189">Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="c00bc-190">**Nuokrypis**</span><span class="sxs-lookup"><span data-stu-id="c00bc-190">**Variation**</span></span> 

<span data-ttu-id="c00bc-191">Jei SF sudaro 2 eilutės, kurių kiekvienoje – 4 prekės, grynoji SF eilutės suma yra 100,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="c00bc-192">Bendra SF eilutės suma (įskaitant muitą: 4 x 5,00) būtų 120,00, o PVM sukuriamas taip: 1 PVM SF eilutė = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 2 PVM SF eilutė = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Bendras PVM = 27,00 + 27,00 = 54,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 54,00 + 40,00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="c00bc-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="c00bc-193"> Bendra suma pagal vnt.</span><span class="sxs-lookup"><span data-stu-id="c00bc-193">Gross amount per unit</span></span>

<span data-ttu-id="c00bc-194">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal vieneto vertę, įskaitant visus kitus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="c00bc-195">PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba.</span><span class="sxs-lookup"><span data-stu-id="c00bc-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-196">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-196">Example</span></span>

<span data-ttu-id="c00bc-197">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-198">Suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-198">Amount</span></span>             | <span data-ttu-id="c00bc-199">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="c00bc-200">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-200">0 - 50</span></span>             | <span data-ttu-id="c00bc-201">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-201">30%</span></span>      |
| <span data-ttu-id="c00bc-202">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-202">50 - 100</span></span>           | <span data-ttu-id="c00bc-203">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-203">20%</span></span>      |
| <span data-ttu-id="c00bc-204">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-205">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-205">10%</span></span>      |

<span data-ttu-id="c00bc-206">Bazinė riba: **Bendra suma pagal vnt.** Kiekvienai lempai taikomas specialus 5,00 muito mokestis.</span><span class="sxs-lookup"><span data-stu-id="c00bc-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="c00bc-207">Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos.</span><span class="sxs-lookup"><span data-stu-id="c00bc-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="c00bc-208">Perkate 8 lempas, kurių kiekviena kainuoja 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="c00bc-209">Bendra vieneto suma yra 30,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="c00bc-210">Mokestis apskaičiuojamas taip: PVM pagal vnt. = 30 x 30 % = 9,00 Bendras PVM = 9,00 x 8 = 72,00 Bendras muito mokestis = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="c00bc-211"> SF suma, įskaitant kitas PVM sumas</span><span class="sxs-lookup"><span data-stu-id="c00bc-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="c00bc-212">Pasirinkite šią parinktį, kad PVM tarifus nustatytumėte pagal visą SF vertę, įskaitant visus kitus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="c00bc-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="c00bc-213">PVM grupėje gali būti tik vienas PVM kodas su šiuo pasirinkimu, atliktu lauke Bazinė riba</span><span class="sxs-lookup"><span data-stu-id="c00bc-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="c00bc-214">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c00bc-214">Example</span></span>

<span data-ttu-id="c00bc-215">PVM tarifai yra nustatomi toliau nurodytais intervalais.</span><span class="sxs-lookup"><span data-stu-id="c00bc-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="c00bc-216">Suma</span><span class="sxs-lookup"><span data-stu-id="c00bc-216">Amount</span></span>             | <span data-ttu-id="c00bc-217">Mokesčio tarifas</span><span class="sxs-lookup"><span data-stu-id="c00bc-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="c00bc-218">0 – 50</span><span class="sxs-lookup"><span data-stu-id="c00bc-218">0 - 50</span></span>             | <span data-ttu-id="c00bc-219">30 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-219">30%</span></span>      |
| <span data-ttu-id="c00bc-220">50 – 100</span><span class="sxs-lookup"><span data-stu-id="c00bc-220">50 - 100</span></span>           | <span data-ttu-id="c00bc-221">20 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-221">20%</span></span>      |
| <span data-ttu-id="c00bc-222">100 – 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="c00bc-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="c00bc-223">10 %</span><span class="sxs-lookup"><span data-stu-id="c00bc-223">10%</span></span>      |

<span data-ttu-id="c00bc-224">Bazinė riba: **SF suma, įskaitant kitas PVM sumas** Skaičiavimo metodas: **Intervalas** </span><span class="sxs-lookup"><span data-stu-id="c00bc-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="c00bc-225">Kiekvienai lempai taikomas specialus 5,00 muito mokestis.</span><span class="sxs-lookup"><span data-stu-id="c00bc-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="c00bc-226">Prieš skaičiuojant PVM, šis muito mokestis pridedamas prie grynosios sumos.</span><span class="sxs-lookup"><span data-stu-id="c00bc-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="c00bc-227">Perkate 8 lempas, kurių kiekviena kainuoja 25,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="c00bc-228">Grynoji SF suma yra 200,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="c00bc-229">Bendra SF suma yra 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="c00bc-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="c00bc-230">Mokestis apskaičiuojamas taip: Bendras PVM = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Bendra muito mokesčio suma = 5,00 x 8 = 40,00 Bendra SF suma = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="c00bc-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="c00bc-231">Daugiau informacijos žr. temose [Visa suma ir PVM kodų intervalo skaičiavimo pasirinktys](whole-amount-interval-options-sales-tax-codes.md) ir [PVM skaičiavimo metodai lauke Kilmė](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="c00bc-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



