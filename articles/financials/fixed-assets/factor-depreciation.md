---
title: Nusidėvėjimo faktorius
description: Šiame straipsnyje apžvelgiamas nusidėvėjimo pagal koeficientą metodas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa8bc4566def9dd770a97facb459e6b977bfaffb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "338802"
---
# <a name="factor-depreciation"></a><span data-ttu-id="2a83a-103">Nusidėvėjimo faktorius</span><span class="sxs-lookup"><span data-stu-id="2a83a-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a83a-104">Šiame straipsnyje apžvelgiamas nusidėvėjimo pagal koeficientą metodas.</span><span class="sxs-lookup"><span data-stu-id="2a83a-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="2a83a-105">Koeficientai yra turto nusidėvėjimo procentai.</span><span class="sxs-lookup"><span data-stu-id="2a83a-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="2a83a-106">Kai nustatote ilgalaikio turto nusidėvėjimo profilį ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirenkate vertę  **Koeficientas**, galite nustatyti progresyvinį, regresyvinį arba tiesiogiai proporcingą nusidėvėjimą:</span><span class="sxs-lookup"><span data-stu-id="2a83a-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="2a83a-107">Pasirinkus progresyvinį nusidėvėjimą, nusidėvėjimo suma didės kiekvieną nusidėvėjimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="2a83a-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="2a83a-108">Pasirinkus regresyvinį nusidėvėjimą, laikotarpio nusidėvėjimo suma mažės laikui bėgant.</span><span class="sxs-lookup"><span data-stu-id="2a83a-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="2a83a-109">Pasirinkus tiesiogiai proporcingą nusidėvėjimą, kiekvieną laikotarpį nusidėvėjimas bus toks pat.</span><span class="sxs-lookup"><span data-stu-id="2a83a-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="2a83a-110">Toliau pateiktos taisyklės ir pavyzdžiai nurodo, kaip nustatyti kiekvieno nusidėvėjimo tipo koeficientus.</span><span class="sxs-lookup"><span data-stu-id="2a83a-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="2a83a-111">Kai lauke **Metodas** pasirinksite **Koeficientas**, bus rodomi laukai **Koeficientas** ir **Intervalas**.</span><span class="sxs-lookup"><span data-stu-id="2a83a-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="2a83a-112">Progresyvinis nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="2a83a-112">Progressive depreciation</span></span>
<span data-ttu-id="2a83a-113">Lauko **Koeficientas** vertė – daugiau negu **50**.</span><span class="sxs-lookup"><span data-stu-id="2a83a-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2a83a-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2a83a-114">Example</span></span>

<span data-ttu-id="2a83a-115">Įsigijimo kaina yra 100 000, koeficientas yra 70, dėvėjimo laikas yra 10 metų, o nusidėvėjimas pradėtas sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2a83a-116">Rodomos tik pirmųjų šešių dėvėjimo metų nusidėvėjimo ir balansinės vertės sumos.</span><span class="sxs-lookup"><span data-stu-id="2a83a-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2a83a-117">Metai</span><span class="sxs-lookup"><span data-stu-id="2a83a-117">Year</span></span> | <span data-ttu-id="2a83a-118">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="2a83a-118">Period</span></span>      | <span data-ttu-id="2a83a-119">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="2a83a-119">Depreciation amount</span></span> | <span data-ttu-id="2a83a-120">Balansinės vertės suma</span><span class="sxs-lookup"><span data-stu-id="2a83a-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2a83a-121">1</span><span class="sxs-lookup"><span data-stu-id="2a83a-121">1</span></span>    | <span data-ttu-id="2a83a-122">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-122">December 31</span></span> | <span data-ttu-id="2a83a-123">307,69</span><span class="sxs-lookup"><span data-stu-id="2a83a-123">307.69</span></span>              | <span data-ttu-id="2a83a-124">99 692,31</span><span class="sxs-lookup"><span data-stu-id="2a83a-124">99,692.31</span></span>             |
| <span data-ttu-id="2a83a-125">2</span><span class="sxs-lookup"><span data-stu-id="2a83a-125">2</span></span>    | <span data-ttu-id="2a83a-126">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-126">December 31</span></span> | <span data-ttu-id="2a83a-127">1447,21</span><span class="sxs-lookup"><span data-stu-id="2a83a-127">1,447.21</span></span>            | <span data-ttu-id="2a83a-128">98 245,10</span><span class="sxs-lookup"><span data-stu-id="2a83a-128">98,245.10</span></span>             |
| <span data-ttu-id="2a83a-129">3</span><span class="sxs-lookup"><span data-stu-id="2a83a-129">3</span></span>    | <span data-ttu-id="2a83a-130">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-130">December 31</span></span> | <span data-ttu-id="2a83a-131">3104,50</span><span class="sxs-lookup"><span data-stu-id="2a83a-131">3,104.50</span></span>            | <span data-ttu-id="2a83a-132">95 140,60</span><span class="sxs-lookup"><span data-stu-id="2a83a-132">95,140.60</span></span>             |
| <span data-ttu-id="2a83a-133">4</span><span class="sxs-lookup"><span data-stu-id="2a83a-133">4</span></span>    | <span data-ttu-id="2a83a-134">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-134">December 31</span></span> | <span data-ttu-id="2a83a-135">5150,21</span><span class="sxs-lookup"><span data-stu-id="2a83a-135">5,150.21</span></span>            | <span data-ttu-id="2a83a-136">89 990,39</span><span class="sxs-lookup"><span data-stu-id="2a83a-136">89,990.39</span></span>             |
| <span data-ttu-id="2a83a-137">5</span><span class="sxs-lookup"><span data-stu-id="2a83a-137">5</span></span>    | <span data-ttu-id="2a83a-138">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-138">December 31</span></span> | <span data-ttu-id="2a83a-139">7522,95</span><span class="sxs-lookup"><span data-stu-id="2a83a-139">7,522.95</span></span>            | <span data-ttu-id="2a83a-140">82 467,44</span><span class="sxs-lookup"><span data-stu-id="2a83a-140">82,467.44</span></span>             |
| <span data-ttu-id="2a83a-141">6</span><span class="sxs-lookup"><span data-stu-id="2a83a-141">6</span></span>    | <span data-ttu-id="2a83a-142">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-142">December 31</span></span> | <span data-ttu-id="2a83a-143">10 184,06</span><span class="sxs-lookup"><span data-stu-id="2a83a-143">10,184.06</span></span>           | <span data-ttu-id="2a83a-144">72 283,38</span><span class="sxs-lookup"><span data-stu-id="2a83a-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="2a83a-145">Regresyvinis nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="2a83a-145">Digressive depreciation</span></span>
<span data-ttu-id="2a83a-146">Lauko **Koeficientas** vertė – mažiau negu **50**.</span><span class="sxs-lookup"><span data-stu-id="2a83a-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="2a83a-147">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2a83a-147">Example</span></span>

<span data-ttu-id="2a83a-148">Įsigijimo kaina yra 100 000, koeficientas yra 20, dėvėjimo laikas yra 10 metų, o nusidėvėjimas pradėtas sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="2a83a-149">Rodomos tik pirmųjų šešių dėvėjimo metų nusidėvėjimo ir balansinės vertės sumos.</span><span class="sxs-lookup"><span data-stu-id="2a83a-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="2a83a-150">Metai</span><span class="sxs-lookup"><span data-stu-id="2a83a-150">Year</span></span> | <span data-ttu-id="2a83a-151">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="2a83a-151">Period</span></span>      | <span data-ttu-id="2a83a-152">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="2a83a-152">Depreciation amount</span></span> | <span data-ttu-id="2a83a-153">Balansinės vertės suma</span><span class="sxs-lookup"><span data-stu-id="2a83a-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="2a83a-154">1</span><span class="sxs-lookup"><span data-stu-id="2a83a-154">1</span></span>    | <span data-ttu-id="2a83a-155">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-155">December 31</span></span> | <span data-ttu-id="2a83a-156">56 080,43</span><span class="sxs-lookup"><span data-stu-id="2a83a-156">56,080.43</span></span>           | <span data-ttu-id="2a83a-157">43 919,57</span><span class="sxs-lookup"><span data-stu-id="2a83a-157">43,919.57</span></span>             |
| <span data-ttu-id="2a83a-158">2</span><span class="sxs-lookup"><span data-stu-id="2a83a-158">2</span></span>    | <span data-ttu-id="2a83a-159">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-159">December 31</span></span> | <span data-ttu-id="2a83a-160">10 665,70</span><span class="sxs-lookup"><span data-stu-id="2a83a-160">10,665.70</span></span>           | <span data-ttu-id="2a83a-161">33 253,87</span><span class="sxs-lookup"><span data-stu-id="2a83a-161">33,253.87</span></span>             |
| <span data-ttu-id="2a83a-162">3</span><span class="sxs-lookup"><span data-stu-id="2a83a-162">3</span></span>    | <span data-ttu-id="2a83a-163">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-163">December 31</span></span> | <span data-ttu-id="2a83a-164">7156,22</span><span class="sxs-lookup"><span data-stu-id="2a83a-164">7,156.22</span></span>            | <span data-ttu-id="2a83a-165">26 097,65</span><span class="sxs-lookup"><span data-stu-id="2a83a-165">26,097.65</span></span>             |
| <span data-ttu-id="2a83a-166">4</span><span class="sxs-lookup"><span data-stu-id="2a83a-166">4</span></span>    | <span data-ttu-id="2a83a-167">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-167">December 31</span></span> | <span data-ttu-id="2a83a-168">5538,06</span><span class="sxs-lookup"><span data-stu-id="2a83a-168">5,538.06</span></span>            | <span data-ttu-id="2a83a-169">20 559,59</span><span class="sxs-lookup"><span data-stu-id="2a83a-169">20,559.59</span></span>             |
| <span data-ttu-id="2a83a-170">5</span><span class="sxs-lookup"><span data-stu-id="2a83a-170">5</span></span>    | <span data-ttu-id="2a83a-171">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-171">December 31</span></span> | <span data-ttu-id="2a83a-172">4579,89</span><span class="sxs-lookup"><span data-stu-id="2a83a-172">4,579.89</span></span>            | <span data-ttu-id="2a83a-173">15 979,70</span><span class="sxs-lookup"><span data-stu-id="2a83a-173">15,979.70</span></span>             |
| <span data-ttu-id="2a83a-174">6</span><span class="sxs-lookup"><span data-stu-id="2a83a-174">6</span></span>    | <span data-ttu-id="2a83a-175">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="2a83a-175">December 31</span></span> | <span data-ttu-id="2a83a-176">3937,36</span><span class="sxs-lookup"><span data-stu-id="2a83a-176">3,937.36</span></span>            | <span data-ttu-id="2a83a-177">12 042,34</span><span class="sxs-lookup"><span data-stu-id="2a83a-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="2a83a-178">Tiesiogiai proporcingas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="2a83a-178">Straight line depreciation</span></span>
<span data-ttu-id="2a83a-179">Lauko **Koeficientas** vertė lygi **50**.</span><span class="sxs-lookup"><span data-stu-id="2a83a-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="2a83a-180">Šiuo atveju kiekvieno laikotarpio nusidėvėjimas vienodas, reikia atsižvelgti į kituose laukuose nurodytas, kaip aprašyta straipsnyje [Tiesiogiai proporcingas nusidėvėjimas](straight-line-service-life-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="2a83a-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



