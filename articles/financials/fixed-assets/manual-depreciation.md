---
title: "Neautomatinis nusidėvėjimas"
description: "Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d7a672b80a0da7ab05acf5b5efe041f0f89c0042
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="32d75-103">Neautomatinis nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="32d75-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="32d75-104">Šiame straipsnyje apžvelgtas rankinis nusidėvėjimo metodas.</span><span class="sxs-lookup"><span data-stu-id="32d75-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="32d75-105">Kai nustatote ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo profiliai** lauke **Metodas** pasirenkate **Rankinis**, ilgalaikio turto, priskirto nusidėvėjimo šablonui, nusidėvėjimas nustatomas pagal kiekviename kalendorinių metų intervale įvestą procentinį dydį.</span><span class="sxs-lookup"><span data-stu-id="32d75-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="32d75-106">Intervalai, kurių procentinius dydžius nustatote, registruojami atsižvelgiant į reikšmę, kurią pasirenkate **Laikotarpio dažnio** lauke, esančiame „FastTab‟ **Bendra**, **Nusidėvėjimo profilių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="32d75-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="32d75-107">Čia nurodytos reikšmės, kurias galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="32d75-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="32d75-108">Kasmet</span><span class="sxs-lookup"><span data-stu-id="32d75-108">Yearly</span></span>
-   <span data-ttu-id="32d75-109">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="32d75-109">Monthly</span></span>
-   <span data-ttu-id="32d75-110">Kas ketvirtį</span><span class="sxs-lookup"><span data-stu-id="32d75-110">Quarterly</span></span>
-   <span data-ttu-id="32d75-111">Kas pusę metų</span><span class="sxs-lookup"><span data-stu-id="32d75-111">Half-Yearly</span></span>
-   <span data-ttu-id="32d75-112">Kasdien</span><span class="sxs-lookup"><span data-stu-id="32d75-112">Daily</span></span>

<span data-ttu-id="32d75-113">Pasirinkę laikotarpio dažnį, spustelėkite **Rankiniu būdu sudaryti grafikai** ir nustatykite kiekvieno registravimo intervalo procentinius dydžius.</span><span class="sxs-lookup"><span data-stu-id="32d75-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="32d75-114">Veikdami kartu, rankiniu būdu sudarytas grafikas ir registravimo intervalas apibrėžia nusidėvėjimo sumą, kaip parodyta vėliau šiame straipsnyje pateikiamuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="32d75-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="32d75-115">Rankinis nusidėvėjimas visuomet skaičiuojamas kaip įsigijimo kainos procentinis dydis.</span><span class="sxs-lookup"><span data-stu-id="32d75-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="32d75-116">Procentiniai dydžiai, kuriuos įvedate rankiniu būdu nustatomo nusidėvėjimo intervaluose, neprivalo sudaryti 100 procentų.</span><span class="sxs-lookup"><span data-stu-id="32d75-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="32d75-117">Rankinis nusidėvėjimas yra lankstus nusidėvėjimo metodas, kuris dažnai naudojamas norint puslapyje **Knygos** nurodyti visiško nusidėvėjimo šabloną, pavyzdžiui, specialiais tikslais (pavyzdžiui, mokesčių) nustatyti neperiodinį nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="32d75-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="32d75-118">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="32d75-118">Examples</span></span>
<span data-ttu-id="32d75-119">Įsigijimo kaina: 11 000,00 Numatyta nurašymo vertė: 1 000,00 Toliau pateikiamoje lentelėje rodomi intervalai ir procentiniai dydžiai, kuriuos nustatote **Ilgalaikio turto nusidėvėjimo profilių grafikų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="32d75-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="32d75-120">Intervalo numeris</span><span class="sxs-lookup"><span data-stu-id="32d75-120">Interval number</span></span> | <span data-ttu-id="32d75-121">Procentai</span><span class="sxs-lookup"><span data-stu-id="32d75-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="32d75-122">1</span><span class="sxs-lookup"><span data-stu-id="32d75-122">1</span></span>               | <span data-ttu-id="32d75-123">10,00</span><span class="sxs-lookup"><span data-stu-id="32d75-123">10.00</span></span>      |
| <span data-ttu-id="32d75-124">2</span><span class="sxs-lookup"><span data-stu-id="32d75-124">2</span></span>               | <span data-ttu-id="32d75-125">50,00</span><span class="sxs-lookup"><span data-stu-id="32d75-125">50.00</span></span>      |
| <span data-ttu-id="32d75-126">3</span><span class="sxs-lookup"><span data-stu-id="32d75-126">3</span></span>               | <span data-ttu-id="32d75-127">8,00</span><span class="sxs-lookup"><span data-stu-id="32d75-127">8.00</span></span>       |

<span data-ttu-id="32d75-128">Toliau pateikiamoje lentelėje rodoma, kaip skaičiuojamas kiekvieno intervalo nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="32d75-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="32d75-129">Intervalo numeris</span><span class="sxs-lookup"><span data-stu-id="32d75-129">Interval number</span></span> | <span data-ttu-id="32d75-130">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="32d75-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="32d75-131">Balansinė vertė intervalo pabaigoje</span><span class="sxs-lookup"><span data-stu-id="32d75-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="32d75-132">1</span><span class="sxs-lookup"><span data-stu-id="32d75-132">1</span></span>                | <span data-ttu-id="32d75-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="32d75-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="32d75-134">10 000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="32d75-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="32d75-135">2</span><span class="sxs-lookup"><span data-stu-id="32d75-135">2</span></span>                | <span data-ttu-id="32d75-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="32d75-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="32d75-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="32d75-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="32d75-138">3</span><span class="sxs-lookup"><span data-stu-id="32d75-138">3</span></span>                | <span data-ttu-id="32d75-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="32d75-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="32d75-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="32d75-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="32d75-141">Jeigu lauke **Laikotarpio dažnis** pasirenkate **Kas mėnesį**, nustatote 12 rankinių grafikų intervalų.</span><span class="sxs-lookup"><span data-stu-id="32d75-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="32d75-142">Toliau pateikiamoje lentelėje rodomos pirmųjų dviejų intervalų nusidėvėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="32d75-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="32d75-143">Intervalas</span><span class="sxs-lookup"><span data-stu-id="32d75-143">Interval</span></span> | <span data-ttu-id="32d75-144">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="32d75-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="32d75-145">sausio</span><span class="sxs-lookup"><span data-stu-id="32d75-145">January</span></span>  | <span data-ttu-id="32d75-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="32d75-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="32d75-147">Vasaris</span><span class="sxs-lookup"><span data-stu-id="32d75-147">February</span></span> | <span data-ttu-id="32d75-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="32d75-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="32d75-149">Jeigu lauke ****Laikotarpio dažnis**** pasirenkate **Kas pusmetį**, nustatote du rankinių grafikų intervalus.</span><span class="sxs-lookup"><span data-stu-id="32d75-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="32d75-150">Toliau pateikiamoje lentelėje rodomos tų dviejų intervalų nusidėvėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="32d75-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="32d75-151">Intervalas</span><span class="sxs-lookup"><span data-stu-id="32d75-151">Interval</span></span>    | <span data-ttu-id="32d75-152">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="32d75-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="32d75-153">Birželio 30 d.</span><span class="sxs-lookup"><span data-stu-id="32d75-153">June 30</span></span>     | <span data-ttu-id="32d75-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="32d75-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="32d75-155">Gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="32d75-155">December 31</span></span> | <span data-ttu-id="32d75-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="32d75-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="32d75-157">Bendra procentinių dydžių suma neturi būti 100.</span><span class="sxs-lookup"><span data-stu-id="32d75-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="32d75-158">Tačiau, jei reikšmė lauke **Sukaupti procentai**, esančiame puslapyje **Ilgalaikio turto nusidėvėjimo profilių grafikų**, nėra **100**, gaunate pranešimą.</span><span class="sxs-lookup"><span data-stu-id="32d75-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




