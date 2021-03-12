---
title: Neautomatinis nusidėvėjimas
description: Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 228e6c94042942a26793eb0bebc1186dd4767e7f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969034"
---
# <a name="manual-depreciation"></a><span data-ttu-id="c1611-103">Neautomatinis nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="c1611-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1611-104">Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas.</span><span class="sxs-lookup"><span data-stu-id="c1611-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="c1611-105">Kai nustatote ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo profiliai** lauke **Metodas** pasirenkate **Rankinis**, ilgalaikio turto, priskirto nusidėvėjimo šablonui, nusidėvėjimas nustatomas pagal kiekviename kalendorinių metų intervale įvestą procentinį dydį.</span><span class="sxs-lookup"><span data-stu-id="c1611-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="c1611-106">Intervalai, kurių procentinius dydžius nustatote, registruojami atsižvelgiant į reikšmę, kurią pasirenkate **Laikotarpio dažnio** lauke, esančiame „FastTab‟ **Bendra**, **Nusidėvėjimo profilių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c1611-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="c1611-107">Čia nurodytos reikšmės, kurias galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="c1611-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="c1611-108">Kasmet</span><span class="sxs-lookup"><span data-stu-id="c1611-108">Yearly</span></span>
-   <span data-ttu-id="c1611-109">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="c1611-109">Monthly</span></span>
-   <span data-ttu-id="c1611-110">Kas ketvirtį</span><span class="sxs-lookup"><span data-stu-id="c1611-110">Quarterly</span></span>
-   <span data-ttu-id="c1611-111">Kas pusę metų</span><span class="sxs-lookup"><span data-stu-id="c1611-111">Half-Yearly</span></span>
-   <span data-ttu-id="c1611-112">Kasdien</span><span class="sxs-lookup"><span data-stu-id="c1611-112">Daily</span></span>

<span data-ttu-id="c1611-113">Pasirinkę laikotarpio dažnį, spustelėkite **Rankiniu būdu sudaryti grafikai** ir nustatykite kiekvieno registravimo intervalo procentinius dydžius.</span><span class="sxs-lookup"><span data-stu-id="c1611-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="c1611-114">Veikdami kartu, rankiniu būdu sudarytas grafikas ir registravimo intervalas apibrėžia nusidėvėjimo sumą, kaip parodyta vėliau šiame straipsnyje pateikiamuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="c1611-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="c1611-115">Rankinis nusidėvėjimas visuomet skaičiuojamas kaip įsigijimo kainos procentinis dydis.</span><span class="sxs-lookup"><span data-stu-id="c1611-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="c1611-116">Procentiniai dydžiai, kuriuos įvedate rankiniu būdu nustatomo nusidėvėjimo intervaluose, neprivalo sudaryti 100 procentų.</span><span class="sxs-lookup"><span data-stu-id="c1611-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="c1611-117">Rankinis nusidėvėjimas yra lankstus nusidėvėjimo metodas, kuris dažnai naudojamas norint puslapyje **Knygos** nurodyti visiško nusidėvėjimo šabloną, pavyzdžiui, specialiais tikslais (pavyzdžiui, mokesčių) nustatyti neperiodinį nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="c1611-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="c1611-118">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="c1611-118">Examples</span></span>
<span data-ttu-id="c1611-119">Įsigijimo kaina: 11 000,00 Numatyta nurašymo vertė: 1 000,00 Toliau pateikiamoje lentelėje rodomi intervalai ir procentiniai dydžiai, kuriuos nustatote **Ilgalaikio turto nusidėvėjimo profilių grafikų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c1611-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="c1611-120">Intervalo numeris</span><span class="sxs-lookup"><span data-stu-id="c1611-120">Interval number</span></span> | <span data-ttu-id="c1611-121">Procentai</span><span class="sxs-lookup"><span data-stu-id="c1611-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="c1611-122">1</span><span class="sxs-lookup"><span data-stu-id="c1611-122">1</span></span>               | <span data-ttu-id="c1611-123">10,00</span><span class="sxs-lookup"><span data-stu-id="c1611-123">10.00</span></span>      |
| <span data-ttu-id="c1611-124">2</span><span class="sxs-lookup"><span data-stu-id="c1611-124">2</span></span>               | <span data-ttu-id="c1611-125">50,00</span><span class="sxs-lookup"><span data-stu-id="c1611-125">50.00</span></span>      |
| <span data-ttu-id="c1611-126">3</span><span class="sxs-lookup"><span data-stu-id="c1611-126">3</span></span>               | <span data-ttu-id="c1611-127">8,00</span><span class="sxs-lookup"><span data-stu-id="c1611-127">8.00</span></span>       |

<span data-ttu-id="c1611-128">Toliau pateikiamoje lentelėje rodoma, kaip skaičiuojamas kiekvieno intervalo nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="c1611-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="c1611-129">Intervalo numeris</span><span class="sxs-lookup"><span data-stu-id="c1611-129">Interval number</span></span> | <span data-ttu-id="c1611-130">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="c1611-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="c1611-131">Balansinė vertė intervalo pabaigoje</span><span class="sxs-lookup"><span data-stu-id="c1611-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="c1611-132">1</span><span class="sxs-lookup"><span data-stu-id="c1611-132">1</span></span>                | <span data-ttu-id="c1611-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="c1611-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="c1611-134">10 000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="c1611-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="c1611-135">2</span><span class="sxs-lookup"><span data-stu-id="c1611-135">2</span></span>                | <span data-ttu-id="c1611-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="c1611-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="c1611-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="c1611-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="c1611-138">3</span><span class="sxs-lookup"><span data-stu-id="c1611-138">3</span></span>                | <span data-ttu-id="c1611-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="c1611-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="c1611-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="c1611-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="c1611-141">Jeigu lauke **Laikotarpio dažnis** pasirenkate **Kas mėnesį**, nustatote 12 rankinių grafikų intervalų.</span><span class="sxs-lookup"><span data-stu-id="c1611-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="c1611-142">Toliau pateikiamoje lentelėje rodomos pirmųjų dviejų intervalų nusidėvėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="c1611-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="c1611-143">Intervalas</span><span class="sxs-lookup"><span data-stu-id="c1611-143">Interval</span></span> | <span data-ttu-id="c1611-144">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="c1611-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="c1611-145">sausio</span><span class="sxs-lookup"><span data-stu-id="c1611-145">January</span></span>  | <span data-ttu-id="c1611-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="c1611-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="c1611-147">Vasaris</span><span class="sxs-lookup"><span data-stu-id="c1611-147">February</span></span> | <span data-ttu-id="c1611-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="c1611-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="c1611-149">Jeigu *lauke <strong><em>Laikotarpio dažnis</em>*</strong> pasirenkate <strong>Kas pusmetį</strong>, nustatote du rankinių grafikų intervalus.</span><span class="sxs-lookup"><span data-stu-id="c1611-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="c1611-150">Toliau pateikiamoje lentelėje rodomos tų dviejų intervalų nusidėvėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="c1611-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="c1611-151">Intervalas</span><span class="sxs-lookup"><span data-stu-id="c1611-151">Interval</span></span>    | <span data-ttu-id="c1611-152">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="c1611-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="c1611-153">Birželio 30 d.</span><span class="sxs-lookup"><span data-stu-id="c1611-153">June 30</span></span>     | <span data-ttu-id="c1611-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="c1611-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="c1611-155">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="c1611-155">December 31</span></span> | <span data-ttu-id="c1611-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="c1611-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="c1611-157">Bendra procentinių dydžių suma neturi būti 100.</span><span class="sxs-lookup"><span data-stu-id="c1611-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="c1611-158">Tačiau, jei reikšmė lauke **Sukaupti procentai**, esančiame puslapyje **Ilgalaikio turto nusidėvėjimo profilių grafikų**, nėra **100**, gaunate pranešimą.</span><span class="sxs-lookup"><span data-stu-id="c1611-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



