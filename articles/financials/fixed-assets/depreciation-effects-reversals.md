---
title: "Nusidėvėjimo poveikis su atšaukimais"
description: "Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7309cb3175f65bc6b806edb875ac9406a8faaf66
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="6416f-103">Nusidėvėjimo poveikis su atšaukimais</span><span class="sxs-lookup"><span data-stu-id="6416f-103">Depreciation effects with reversals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6416f-104">Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.</span><span class="sxs-lookup"><span data-stu-id="6416f-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="6416f-105">Galite atšaukti ilgalaikio turto operacijas ir su ilgalaikiu turtu susietas operacijas.</span><span class="sxs-lookup"><span data-stu-id="6416f-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="6416f-106">Atšauktą operaciją taip pat galite anuliuoti.</span><span class="sxs-lookup"><span data-stu-id="6416f-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="6416f-107">Atšaukite arba anuliuokite galite operaciją, kuri nebuvo paskutinė operacija, registruota turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="6416f-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="6416f-108">Pirmiausia turėtumėte nustatyti, ar po operacijos, kurią atšaukiate, buvo užregistruota kokių nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="6416f-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="6416f-109">Taip yra todėl, nes, atšaukiant operaciją, nusidėvėjimas neperskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="6416f-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="6416f-110">Todėl po atšaukimo nusidėvėjimas dažnai pervertinamas ar nuvertinamas, kaip parodyta pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="6416f-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="6416f-111">Kad užtikrintumėte, kad, atšaukiant operaciją, nusidėvėjimas teisingas, netęskite atšaukimo, jeigu gaunate pranešimą, kad nusidėvėjimas nebus skaičiuojamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="6416f-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="6416f-112">Geriau pirmiausia atšaukite nusidėvėjimo operaciją, kuri užregistruota po operacijos, kurią bandote atšaukti, tada tęskite atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="6416f-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="6416f-113">Nebūsite įspėti apie nusidėvėjimo perskaičiavimus ir galėsite tęsti atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="6416f-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="6416f-114">Toliau pateiktuose pavyzdžiuose rodomi skaičiavimai, kurie atliekami, jei tęsiate nepaisydami pranešimo ir pirmiausia neatšaukę nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="6416f-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="6416f-115"> 1 pavyzdys: nusidėvėjimas pervertintas</span><span class="sxs-lookup"><span data-stu-id="6416f-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="6416f-116">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="6416f-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6416f-117">Šiame pavyzdyje nusidėvėjimas pervertintas.</span><span class="sxs-lookup"><span data-stu-id="6416f-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6416f-118">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="6416f-118">Asset transaction history</span></span>

| <span data-ttu-id="6416f-119">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-119">Date</span></span>       | <span data-ttu-id="6416f-120">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-120">Transaction type</span></span>                                                          | <span data-ttu-id="6416f-121">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="6416f-122">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-122">January 1</span></span>  | <span data-ttu-id="6416f-123">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="6416f-123">Acquisition</span></span>                                                               | <span data-ttu-id="6416f-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-124">59,000.00</span></span>                                 |
| <span data-ttu-id="6416f-125">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-125">January 1</span></span>  | <span data-ttu-id="6416f-126">Įsigijimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="6416f-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="6416f-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-127">1,000.00</span></span>                                  |
| <span data-ttu-id="6416f-128">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="6416f-128">January 31</span></span> | <span data-ttu-id="6416f-129">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="6416f-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6416f-130">1 000,00Skaičiavimas: balansinė vertė (59 000 + 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="6416f-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6416f-131">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="6416f-131">Reversal action</span></span>

| <span data-ttu-id="6416f-132">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-132">Date</span></span>      | <span data-ttu-id="6416f-133">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-133">Transaction type</span></span>                | <span data-ttu-id="6416f-134">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="6416f-135">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-135">January 1</span></span> | <span data-ttu-id="6416f-136">Įsigijimo derinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="6416f-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="6416f-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6416f-138">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="6416f-138">Depreciation effect</span></span>

| <span data-ttu-id="6416f-139">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-139">Date</span></span>        | <span data-ttu-id="6416f-140">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-140">Transaction type</span></span>        | <span data-ttu-id="6416f-141">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6416f-142">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="6416f-142">February 28</span></span> | <span data-ttu-id="6416f-143">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="6416f-143">Depreciation (proposal)</span></span> | <span data-ttu-id="6416f-144">983,05Skaičiavimas: balansinė vertė (59 000 – 1 000 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="6416f-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6416f-145">Nusidėvėjimas parvertintas 16,95 (1000–983,05).</span><span class="sxs-lookup"><span data-stu-id="6416f-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="6416f-146"> 2 pavyzdys: Nusidėvėjimas nuvertintas</span><span class="sxs-lookup"><span data-stu-id="6416f-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="6416f-147">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="6416f-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="6416f-148">Šiame pavyzdyje nusidėvėjimas nuvertintas.</span><span class="sxs-lookup"><span data-stu-id="6416f-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="6416f-149">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="6416f-149">Asset transaction history</span></span>

| <span data-ttu-id="6416f-150">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-150">Date</span></span>       | <span data-ttu-id="6416f-151">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-151">Transaction type</span></span>                                                          | <span data-ttu-id="6416f-152">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="6416f-153">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-153">January 1</span></span>  | <span data-ttu-id="6416f-154">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="6416f-154">Acquisition</span></span>                                                               | <span data-ttu-id="6416f-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-155">59,000.00</span></span>                                   |
| <span data-ttu-id="6416f-156">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-156">January 1</span></span>  | <span data-ttu-id="6416f-157">Vertės mažinimas</span><span class="sxs-lookup"><span data-stu-id="6416f-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="6416f-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-158">1,000.00</span></span>                                    |
| <span data-ttu-id="6416f-159">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="6416f-159">January 31</span></span> | <span data-ttu-id="6416f-160">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="6416f-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="6416f-161">966,67Skaičiavimas: balansinė vertė (59 000 – 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="6416f-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="6416f-162">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="6416f-162">Reversal action</span></span>

| <span data-ttu-id="6416f-163">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-163">Date</span></span>      | <span data-ttu-id="6416f-164">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-164">Transaction type</span></span>               | <span data-ttu-id="6416f-165">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="6416f-166">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="6416f-166">January 1</span></span> | <span data-ttu-id="6416f-167">Vertės mažinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="6416f-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="6416f-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="6416f-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="6416f-169">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="6416f-169">Depreciation effect</span></span>

| <span data-ttu-id="6416f-170">Data</span><span class="sxs-lookup"><span data-stu-id="6416f-170">Date</span></span>        | <span data-ttu-id="6416f-171">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="6416f-171">Transaction type</span></span>        | <span data-ttu-id="6416f-172">Suma</span><span class="sxs-lookup"><span data-stu-id="6416f-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6416f-173">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="6416f-173">February 28</span></span> | <span data-ttu-id="6416f-174">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="6416f-174">Depreciation (proposal)</span></span> | <span data-ttu-id="6416f-175">983,62Skaičiavimas: balansinė vertė (59 000 – 966,67 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="6416f-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="6416f-176">Nusidėvėjimas nuvertintas 16,95 (983,62–966,67).</span><span class="sxs-lookup"><span data-stu-id="6416f-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="see-also"></a><span data-ttu-id="6416f-177">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6416f-177">See also</span></span>
--------

[<span data-ttu-id="6416f-178">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="6416f-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




