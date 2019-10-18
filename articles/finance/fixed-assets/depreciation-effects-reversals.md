---
title: Nusidėvėjimo poveikis su atšaukimais
description: Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187365"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="15cc9-103">Nusidėvėjimo poveikis su atšaukimais</span><span class="sxs-lookup"><span data-stu-id="15cc9-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15cc9-104">Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.</span><span class="sxs-lookup"><span data-stu-id="15cc9-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="15cc9-105">Galite atšaukti ilgalaikio turto operacijas ir su ilgalaikiu turtu susietas operacijas.</span><span class="sxs-lookup"><span data-stu-id="15cc9-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="15cc9-106">Atšauktą operaciją taip pat galite anuliuoti.</span><span class="sxs-lookup"><span data-stu-id="15cc9-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="15cc9-107">Atšaukite arba anuliuokite galite operaciją, kuri nebuvo paskutinė operacija, registruota turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="15cc9-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="15cc9-108">Pirmiausia turėtumėte nustatyti, ar po operacijos, kurią atšaukiate, buvo užregistruota kokių nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="15cc9-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="15cc9-109">Taip yra todėl, nes, atšaukiant operaciją, nusidėvėjimas neperskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="15cc9-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="15cc9-110">Todėl po atšaukimo nusidėvėjimas dažnai pervertinamas ar nuvertinamas, kaip parodyta pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="15cc9-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="15cc9-111">Kad užtikrintumėte, kad, atšaukiant operaciją, nusidėvėjimas teisingas, netęskite atšaukimo, jeigu gaunate pranešimą, kad nusidėvėjimas nebus skaičiuojamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="15cc9-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="15cc9-112">Geriau pirmiausia atšaukite nusidėvėjimo operaciją, kuri užregistruota po operacijos, kurią bandote atšaukti, tada tęskite atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="15cc9-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="15cc9-113">Nebūsite įspėti apie nusidėvėjimo perskaičiavimus ir galėsite tęsti atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="15cc9-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="15cc9-114">Toliau pateiktuose pavyzdžiuose rodomi skaičiavimai, kurie atliekami, jei tęsiate nepaisydami pranešimo ir pirmiausia neatšaukę nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="15cc9-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="15cc9-115"> 1 pavyzdys: nusidėvėjimas pervertintas</span><span class="sxs-lookup"><span data-stu-id="15cc9-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="15cc9-116">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="15cc9-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="15cc9-117">Šiame pavyzdyje nusidėvėjimas pervertintas.</span><span class="sxs-lookup"><span data-stu-id="15cc9-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="15cc9-118">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="15cc9-118">Asset transaction history</span></span>

| <span data-ttu-id="15cc9-119">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-119">Date</span></span>       | <span data-ttu-id="15cc9-120">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-120">Transaction type</span></span>                                                          | <span data-ttu-id="15cc9-121">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="15cc9-122">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-122">January 1</span></span>  | <span data-ttu-id="15cc9-123">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-123">Acquisition</span></span>                                                               | <span data-ttu-id="15cc9-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-124">59,000.00</span></span>                                 |
| <span data-ttu-id="15cc9-125">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-125">January 1</span></span>  | <span data-ttu-id="15cc9-126">Įsigijimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="15cc9-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-127">1,000.00</span></span>                                  |
| <span data-ttu-id="15cc9-128">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="15cc9-128">January 31</span></span> | <span data-ttu-id="15cc9-129">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="15cc9-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="15cc9-130">1 000,00Skaičiavimas: balansinė vertė (59 000 + 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="15cc9-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="15cc9-131">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="15cc9-131">Reversal action</span></span>

| <span data-ttu-id="15cc9-132">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-132">Date</span></span>      | <span data-ttu-id="15cc9-133">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-133">Transaction type</span></span>                | <span data-ttu-id="15cc9-134">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="15cc9-135">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-135">January 1</span></span> | <span data-ttu-id="15cc9-136">Įsigijimo derinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="15cc9-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="15cc9-138">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="15cc9-138">Depreciation effect</span></span>

| <span data-ttu-id="15cc9-139">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-139">Date</span></span>        | <span data-ttu-id="15cc9-140">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-140">Transaction type</span></span>        | <span data-ttu-id="15cc9-141">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15cc9-142">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="15cc9-142">February 28</span></span> | <span data-ttu-id="15cc9-143">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="15cc9-143">Depreciation (proposal)</span></span> | <span data-ttu-id="15cc9-144">983,05Skaičiavimas: balansinė vertė (59 000 – 1 000 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="15cc9-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="15cc9-145">Nusidėvėjimas parvertintas 16,95 (1000–983,05).</span><span class="sxs-lookup"><span data-stu-id="15cc9-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="15cc9-146"> 2 pavyzdys: Nusidėvėjimas nuvertintas</span><span class="sxs-lookup"><span data-stu-id="15cc9-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="15cc9-147">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="15cc9-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="15cc9-148">Šiame pavyzdyje nusidėvėjimas nuvertintas.</span><span class="sxs-lookup"><span data-stu-id="15cc9-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="15cc9-149">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="15cc9-149">Asset transaction history</span></span>

| <span data-ttu-id="15cc9-150">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-150">Date</span></span>       | <span data-ttu-id="15cc9-151">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-151">Transaction type</span></span>                                                          | <span data-ttu-id="15cc9-152">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="15cc9-153">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-153">January 1</span></span>  | <span data-ttu-id="15cc9-154">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-154">Acquisition</span></span>                                                               | <span data-ttu-id="15cc9-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-155">59,000.00</span></span>                                   |
| <span data-ttu-id="15cc9-156">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-156">January 1</span></span>  | <span data-ttu-id="15cc9-157">Vertės mažinimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="15cc9-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-158">1,000.00</span></span>                                    |
| <span data-ttu-id="15cc9-159">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="15cc9-159">January 31</span></span> | <span data-ttu-id="15cc9-160">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="15cc9-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="15cc9-161">966,67Skaičiavimas: balansinė vertė (59 000 – 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="15cc9-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="15cc9-162">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="15cc9-162">Reversal action</span></span>

| <span data-ttu-id="15cc9-163">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-163">Date</span></span>      | <span data-ttu-id="15cc9-164">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-164">Transaction type</span></span>               | <span data-ttu-id="15cc9-165">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="15cc9-166">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="15cc9-166">January 1</span></span> | <span data-ttu-id="15cc9-167">Vertės mažinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="15cc9-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="15cc9-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="15cc9-169">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="15cc9-169">Depreciation effect</span></span>

| <span data-ttu-id="15cc9-170">Data</span><span class="sxs-lookup"><span data-stu-id="15cc9-170">Date</span></span>        | <span data-ttu-id="15cc9-171">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="15cc9-171">Transaction type</span></span>        | <span data-ttu-id="15cc9-172">Suma</span><span class="sxs-lookup"><span data-stu-id="15cc9-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15cc9-173">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="15cc9-173">February 28</span></span> | <span data-ttu-id="15cc9-174">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="15cc9-174">Depreciation (proposal)</span></span> | <span data-ttu-id="15cc9-175">983,62Skaičiavimas: balansinė vertė (59 000 – 966,67 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="15cc9-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="15cc9-176">Nusidėvėjimas nuvertintas 16,95 (983,62–966,67).</span><span class="sxs-lookup"><span data-stu-id="15cc9-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="15cc9-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="15cc9-177">Additional resources</span></span>
--------

[<span data-ttu-id="15cc9-178">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="15cc9-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



