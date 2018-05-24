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
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fbef7cb9a9fb18809dff96d4a44454d0dc6a31fc
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="97a60-103">Nusidėvėjimo poveikis su atšaukimais</span><span class="sxs-lookup"><span data-stu-id="97a60-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97a60-104">Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.</span><span class="sxs-lookup"><span data-stu-id="97a60-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="97a60-105">Galite atšaukti ilgalaikio turto operacijas ir su ilgalaikiu turtu susietas operacijas.</span><span class="sxs-lookup"><span data-stu-id="97a60-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="97a60-106">Atšauktą operaciją taip pat galite anuliuoti.</span><span class="sxs-lookup"><span data-stu-id="97a60-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="97a60-107">Atšaukite arba anuliuokite galite operaciją, kuri nebuvo paskutinė operacija, registruota turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="97a60-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="97a60-108">Pirmiausia turėtumėte nustatyti, ar po operacijos, kurią atšaukiate, buvo užregistruota kokių nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="97a60-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="97a60-109">Taip yra todėl, nes, atšaukiant operaciją, nusidėvėjimas neperskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="97a60-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="97a60-110">Todėl po atšaukimo nusidėvėjimas dažnai pervertinamas ar nuvertinamas, kaip parodyta pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="97a60-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="97a60-111">Kad užtikrintumėte, kad, atšaukiant operaciją, nusidėvėjimas teisingas, netęskite atšaukimo, jeigu gaunate pranešimą, kad nusidėvėjimas nebus skaičiuojamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="97a60-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="97a60-112">Geriau pirmiausia atšaukite nusidėvėjimo operaciją, kuri užregistruota po operacijos, kurią bandote atšaukti, tada tęskite atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="97a60-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="97a60-113">Nebūsite įspėti apie nusidėvėjimo perskaičiavimus ir galėsite tęsti atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="97a60-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="97a60-114">Toliau pateiktuose pavyzdžiuose rodomi skaičiavimai, kurie atliekami, jei tęsiate nepaisydami pranešimo ir pirmiausia neatšaukę nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="97a60-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="97a60-115"> 1 pavyzdys: nusidėvėjimas pervertintas</span><span class="sxs-lookup"><span data-stu-id="97a60-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="97a60-116">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="97a60-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="97a60-117">Šiame pavyzdyje nusidėvėjimas pervertintas.</span><span class="sxs-lookup"><span data-stu-id="97a60-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="97a60-118">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="97a60-118">Asset transaction history</span></span>

| <span data-ttu-id="97a60-119">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-119">Date</span></span>       | <span data-ttu-id="97a60-120">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-120">Transaction type</span></span>                                                          | <span data-ttu-id="97a60-121">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="97a60-122">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-122">January 1</span></span>  | <span data-ttu-id="97a60-123">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="97a60-123">Acquisition</span></span>                                                               | <span data-ttu-id="97a60-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-124">59,000.00</span></span>                                 |
| <span data-ttu-id="97a60-125">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-125">January 1</span></span>  | <span data-ttu-id="97a60-126">Įsigijimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="97a60-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="97a60-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-127">1,000.00</span></span>                                  |
| <span data-ttu-id="97a60-128">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="97a60-128">January 31</span></span> | <span data-ttu-id="97a60-129">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="97a60-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="97a60-130">1 000,00Skaičiavimas: balansinė vertė (59 000 + 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="97a60-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="97a60-131">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="97a60-131">Reversal action</span></span>

| <span data-ttu-id="97a60-132">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-132">Date</span></span>      | <span data-ttu-id="97a60-133">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-133">Transaction type</span></span>                | <span data-ttu-id="97a60-134">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="97a60-135">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-135">January 1</span></span> | <span data-ttu-id="97a60-136">Įsigijimo derinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97a60-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="97a60-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="97a60-138">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="97a60-138">Depreciation effect</span></span>

| <span data-ttu-id="97a60-139">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-139">Date</span></span>        | <span data-ttu-id="97a60-140">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-140">Transaction type</span></span>        | <span data-ttu-id="97a60-141">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97a60-142">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="97a60-142">February 28</span></span> | <span data-ttu-id="97a60-143">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="97a60-143">Depreciation (proposal)</span></span> | <span data-ttu-id="97a60-144">983,05Skaičiavimas: balansinė vertė (59 000 – 1 000 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="97a60-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="97a60-145">Nusidėvėjimas parvertintas 16,95 (1000–983,05).</span><span class="sxs-lookup"><span data-stu-id="97a60-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="97a60-146"> 2 pavyzdys: Nusidėvėjimas nuvertintas</span><span class="sxs-lookup"><span data-stu-id="97a60-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="97a60-147">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="97a60-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="97a60-148">Šiame pavyzdyje nusidėvėjimas nuvertintas.</span><span class="sxs-lookup"><span data-stu-id="97a60-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="97a60-149">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="97a60-149">Asset transaction history</span></span>

| <span data-ttu-id="97a60-150">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-150">Date</span></span>       | <span data-ttu-id="97a60-151">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-151">Transaction type</span></span>                                                          | <span data-ttu-id="97a60-152">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="97a60-153">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-153">January 1</span></span>  | <span data-ttu-id="97a60-154">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="97a60-154">Acquisition</span></span>                                                               | <span data-ttu-id="97a60-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-155">59,000.00</span></span>                                   |
| <span data-ttu-id="97a60-156">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-156">January 1</span></span>  | <span data-ttu-id="97a60-157">Vertės mažinimas</span><span class="sxs-lookup"><span data-stu-id="97a60-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="97a60-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-158">1,000.00</span></span>                                    |
| <span data-ttu-id="97a60-159">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="97a60-159">January 31</span></span> | <span data-ttu-id="97a60-160">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="97a60-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="97a60-161">966,67Skaičiavimas: balansinė vertė (59 000 – 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="97a60-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="97a60-162">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="97a60-162">Reversal action</span></span>

| <span data-ttu-id="97a60-163">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-163">Date</span></span>      | <span data-ttu-id="97a60-164">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-164">Transaction type</span></span>               | <span data-ttu-id="97a60-165">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="97a60-166">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="97a60-166">January 1</span></span> | <span data-ttu-id="97a60-167">Vertės mažinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97a60-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="97a60-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="97a60-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="97a60-169">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="97a60-169">Depreciation effect</span></span>

| <span data-ttu-id="97a60-170">Data</span><span class="sxs-lookup"><span data-stu-id="97a60-170">Date</span></span>        | <span data-ttu-id="97a60-171">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="97a60-171">Transaction type</span></span>        | <span data-ttu-id="97a60-172">Suma</span><span class="sxs-lookup"><span data-stu-id="97a60-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a60-173">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="97a60-173">February 28</span></span> | <span data-ttu-id="97a60-174">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="97a60-174">Depreciation (proposal)</span></span> | <span data-ttu-id="97a60-175">983,62Skaičiavimas: balansinė vertė (59 000 – 966,67 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="97a60-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="97a60-176">Nusidėvėjimas nuvertintas 16,95 (983,62–966,67).</span><span class="sxs-lookup"><span data-stu-id="97a60-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="97a60-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="97a60-177">Additional resources</span></span>
--------

[<span data-ttu-id="97a60-178">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="97a60-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)




