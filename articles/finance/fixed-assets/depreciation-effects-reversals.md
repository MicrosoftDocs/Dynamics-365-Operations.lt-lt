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
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4952f94d635a9c9cdc7892e6cc142cfe4d526e44
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241215"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="1fa38-103">Nusidėvėjimo poveikis su atšaukimais</span><span class="sxs-lookup"><span data-stu-id="1fa38-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fa38-104">Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.</span><span class="sxs-lookup"><span data-stu-id="1fa38-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="1fa38-105">Galite atšaukti ilgalaikio turto operacijas ir su ilgalaikiu turtu susietas operacijas.</span><span class="sxs-lookup"><span data-stu-id="1fa38-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="1fa38-106">Atšauktą operaciją taip pat galite anuliuoti.</span><span class="sxs-lookup"><span data-stu-id="1fa38-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="1fa38-107">Atšaukite arba anuliuokite galite operaciją, kuri nebuvo paskutinė operacija, registruota turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="1fa38-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="1fa38-108">Pirmiausia turėtumėte nustatyti, ar po operacijos, kurią atšaukiate, buvo užregistruota kokių nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="1fa38-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="1fa38-109">Taip yra todėl, nes, atšaukiant operaciją, nusidėvėjimas neperskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="1fa38-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="1fa38-110">Todėl po atšaukimo nusidėvėjimas dažnai pervertinamas ar nuvertinamas, kaip parodyta pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="1fa38-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="1fa38-111">Kad užtikrintumėte, kad, atšaukiant operaciją, nusidėvėjimas teisingas, netęskite atšaukimo, jeigu gaunate pranešimą, kad nusidėvėjimas nebus skaičiuojamas iš naujo.</span><span class="sxs-lookup"><span data-stu-id="1fa38-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="1fa38-112">Geriau pirmiausia atšaukite nusidėvėjimo operaciją, kuri užregistruota po operacijos, kurią bandote atšaukti, tada tęskite atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="1fa38-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="1fa38-113">Nebūsite įspėti apie nusidėvėjimo perskaičiavimus ir galėsite tęsti atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="1fa38-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="1fa38-114">Toliau pateiktuose pavyzdžiuose rodomi skaičiavimai, kurie atliekami, jei tęsiate nepaisydami pranešimo ir pirmiausia neatšaukę nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="1fa38-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="1fa38-115"> 1 pavyzdys: nusidėvėjimas pervertintas</span><span class="sxs-lookup"><span data-stu-id="1fa38-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="1fa38-116">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="1fa38-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="1fa38-117">Šiame pavyzdyje nusidėvėjimas pervertintas.</span><span class="sxs-lookup"><span data-stu-id="1fa38-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="1fa38-118">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="1fa38-118">Asset transaction history</span></span>

| <span data-ttu-id="1fa38-119">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-119">Date</span></span>       | <span data-ttu-id="1fa38-120">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-120">Transaction type</span></span>                                                          | <span data-ttu-id="1fa38-121">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="1fa38-122">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-122">January 1</span></span>  | <span data-ttu-id="1fa38-123">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-123">Acquisition</span></span>                                                               | <span data-ttu-id="1fa38-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-124">59,000.00</span></span>                                 |
| <span data-ttu-id="1fa38-125">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-125">January 1</span></span>  | <span data-ttu-id="1fa38-126">Įsigijimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="1fa38-127">1000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-127">1,000.00</span></span>                                  |
| <span data-ttu-id="1fa38-128">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="1fa38-128">January 31</span></span> | <span data-ttu-id="1fa38-129">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="1fa38-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="1fa38-130">1 000,00Skaičiavimas: balansinė vertė (59 000 + 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="1fa38-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="1fa38-131">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="1fa38-131">Reversal action</span></span>

| <span data-ttu-id="1fa38-132">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-132">Date</span></span>      | <span data-ttu-id="1fa38-133">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-133">Transaction type</span></span>                | <span data-ttu-id="1fa38-134">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="1fa38-135">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-135">January 1</span></span> | <span data-ttu-id="1fa38-136">Įsigijimo derinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="1fa38-137">-1000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="1fa38-138">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="1fa38-138">Depreciation effect</span></span>

| <span data-ttu-id="1fa38-139">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-139">Date</span></span>        | <span data-ttu-id="1fa38-140">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-140">Transaction type</span></span>        | <span data-ttu-id="1fa38-141">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa38-142">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="1fa38-142">February 28</span></span> | <span data-ttu-id="1fa38-143">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="1fa38-143">Depreciation (proposal)</span></span> | <span data-ttu-id="1fa38-144">983,05Skaičiavimas: balansinė vertė (59 000 – 1 000 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="1fa38-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="1fa38-145">Nusidėvėjimas parvertintas 16,95 (1000–983,05).</span><span class="sxs-lookup"><span data-stu-id="1fa38-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="1fa38-146"> 2 pavyzdys: Nusidėvėjimas nuvertintas</span><span class="sxs-lookup"><span data-stu-id="1fa38-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="1fa38-147">Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių).</span><span class="sxs-lookup"><span data-stu-id="1fa38-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="1fa38-148">Šiame pavyzdyje nusidėvėjimas nuvertintas.</span><span class="sxs-lookup"><span data-stu-id="1fa38-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="1fa38-149">Turto operacijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="1fa38-149">Asset transaction history</span></span>

| <span data-ttu-id="1fa38-150">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-150">Date</span></span>       | <span data-ttu-id="1fa38-151">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-151">Transaction type</span></span>                                                          | <span data-ttu-id="1fa38-152">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="1fa38-153">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-153">January 1</span></span>  | <span data-ttu-id="1fa38-154">Įsigijimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-154">Acquisition</span></span>                                                               | <span data-ttu-id="1fa38-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-155">59,000.00</span></span>                                   |
| <span data-ttu-id="1fa38-156">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-156">January 1</span></span>  | <span data-ttu-id="1fa38-157">Vertės mažinimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="1fa38-158">1000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-158">1,000.00</span></span>                                    |
| <span data-ttu-id="1fa38-159">Sausio 31</span><span class="sxs-lookup"><span data-stu-id="1fa38-159">January 31</span></span> | <span data-ttu-id="1fa38-160">Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui)</span><span class="sxs-lookup"><span data-stu-id="1fa38-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="1fa38-161">966,67Skaičiavimas: balansinė vertė (59 000 – 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60)</span><span class="sxs-lookup"><span data-stu-id="1fa38-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="1fa38-162">Atšaukimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="1fa38-162">Reversal action</span></span>

| <span data-ttu-id="1fa38-163">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-163">Date</span></span>      | <span data-ttu-id="1fa38-164">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-164">Transaction type</span></span>               | <span data-ttu-id="1fa38-165">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="1fa38-166">Sausio 1</span><span class="sxs-lookup"><span data-stu-id="1fa38-166">January 1</span></span> | <span data-ttu-id="1fa38-167">Vertės mažinimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="1fa38-168">-1000,00</span><span class="sxs-lookup"><span data-stu-id="1fa38-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="1fa38-169">Nusidėvėjimo efektas</span><span class="sxs-lookup"><span data-stu-id="1fa38-169">Depreciation effect</span></span>

| <span data-ttu-id="1fa38-170">Data</span><span class="sxs-lookup"><span data-stu-id="1fa38-170">Date</span></span>        | <span data-ttu-id="1fa38-171">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="1fa38-171">Transaction type</span></span>        | <span data-ttu-id="1fa38-172">Suma</span><span class="sxs-lookup"><span data-stu-id="1fa38-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa38-173">Vasario 28</span><span class="sxs-lookup"><span data-stu-id="1fa38-173">February 28</span></span> | <span data-ttu-id="1fa38-174">Nusidėvėjimas (pasiūlymas)</span><span class="sxs-lookup"><span data-stu-id="1fa38-174">Depreciation (proposal)</span></span> | <span data-ttu-id="1fa38-175">983,62Skaičiavimas: balansinė vertė (59 000 – 966,67 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59)</span><span class="sxs-lookup"><span data-stu-id="1fa38-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="1fa38-176">Nusidėvėjimas nuvertintas 16,95 (983,62–966,67).</span><span class="sxs-lookup"><span data-stu-id="1fa38-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="1fa38-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1fa38-177">Additional resources</span></span>
--------

[<span data-ttu-id="1fa38-178">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="1fa38-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]