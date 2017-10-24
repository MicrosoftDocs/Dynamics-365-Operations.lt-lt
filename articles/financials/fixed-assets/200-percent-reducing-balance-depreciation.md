---
title: "200 procentų mažėjančios vertės metodas"
description: "Šiame straipsnyje apžvelgiamas 200 % nusidėvėjimo mažėjančios vertės metodas."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 46afd002a370a43c9e1d2fb7cc5e61ece9033be9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="3782c-103">200 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="3782c-103">200 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3782c-104">Šiame straipsnyje apžvelgiamas 200 % nusidėvėjimo mažėjančios vertės metodas.</span><span class="sxs-lookup"><span data-stu-id="3782c-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="3782c-105">Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **200 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="3782c-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="3782c-106">Procentas apskaičiuojamas remiantis ilgalaikio turto dėvėjimo laiku.</span><span class="sxs-lookup"><span data-stu-id="3782c-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="3782c-107">Pavyzdžiui, jei turto dėvėjimo laikas yra penkeri metai, apskaičiuotas procentas yra 40 procentai (200 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="3782c-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="3782c-108">Šis metodas dar vadinamas dvigubos mažėjančios vertės metodu.</span><span class="sxs-lookup"><span data-stu-id="3782c-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="3782c-109">Norėdami nustatyti 200 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis.</span><span class="sxs-lookup"><span data-stu-id="3782c-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3782c-110">Pasirinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į vertę, pasirinktą lauke **Nusidėvėjimo metai**.</span><span class="sxs-lookup"><span data-stu-id="3782c-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="3782c-111">Pasirinkite nusidėvėjimo metus.</span><span class="sxs-lookup"><span data-stu-id="3782c-111">Select a depreciation year</span></span>
<span data-ttu-id="3782c-112">Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**.</span><span class="sxs-lookup"><span data-stu-id="3782c-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3782c-113">Numatytoji reikšmė yra **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="3782c-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="3782c-114">Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**.</span><span class="sxs-lookup"><span data-stu-id="3782c-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="3782c-115">Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.</span><span class="sxs-lookup"><span data-stu-id="3782c-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="3782c-116">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="3782c-116">Calendar</span></span>

<span data-ttu-id="3782c-117">**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="3782c-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="3782c-118">Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="3782c-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="3782c-119">Paprastai nusidėvėjimas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę.</span><span class="sxs-lookup"><span data-stu-id="3782c-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="3782c-120">Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="3782c-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="3782c-121">Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="3782c-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3782c-122">Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3782c-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="3782c-123">Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="3782c-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="3782c-124">Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="3782c-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="3782c-125">Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="3782c-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="3782c-126">Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="3782c-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="3782c-127">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="3782c-127">Fiscal</span></span>

<span data-ttu-id="3782c-128">Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 200 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="3782c-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="3782c-129">Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3782c-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="3782c-130">Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="3782c-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="3782c-131">Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="3782c-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="3782c-132">Koreguojamas kiekvieno laikotarpio nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="3782c-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="3782c-133">Kitų ataskaitinių metų trukmė nustatoma pagal laikotarpių sąranką puslapyje **Ataskaitiniai kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="3782c-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="3782c-134">Kai kaip nusidėvėjimo metai pasirinkta **Finansiniai**, galimos šios lauko **Laikotarpio dažnis** parinktys:</span><span class="sxs-lookup"><span data-stu-id="3782c-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3782c-135">**Kasmet** apskaičiuota bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.</span><span class="sxs-lookup"><span data-stu-id="3782c-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="3782c-136">Pasirinkus **Ataskaitinis laikotarpis**, rodoma apskaičiuota bendroji ataskaitinių metų nusidėvėjimo suma.</span><span class="sxs-lookup"><span data-stu-id="3782c-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="3782c-137">Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3782c-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="3782c-138">200% mažėjančios vertės nusidėvėjimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3782c-138">Example of 200% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="3782c-139">Įsigijimo savikaina</span><span class="sxs-lookup"><span data-stu-id="3782c-139">Acquisition cost</span></span>               | <span data-ttu-id="3782c-140">11 000</span><span class="sxs-lookup"><span data-stu-id="3782c-140">11,000</span></span> |
| <span data-ttu-id="3782c-141">Likvidacinė vertė</span><span class="sxs-lookup"><span data-stu-id="3782c-141">Salvage value</span></span>                  | <span data-ttu-id="3782c-142">1000</span><span class="sxs-lookup"><span data-stu-id="3782c-142">1, 000</span></span> |
| <span data-ttu-id="3782c-143">Nusidėvėjimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="3782c-143">Depreciation base</span></span>              | <span data-ttu-id="3782c-144">10.000</span><span class="sxs-lookup"><span data-stu-id="3782c-144">10,000</span></span> |
| <span data-ttu-id="3782c-145">Aptarnavimo laikas metais</span><span class="sxs-lookup"><span data-stu-id="3782c-145">Service life years</span></span>             | <span data-ttu-id="3782c-146">5</span><span class="sxs-lookup"><span data-stu-id="3782c-146">5</span></span>      |
| <span data-ttu-id="3782c-147">Metinio nusidėvėjimo procentas</span><span class="sxs-lookup"><span data-stu-id="3782c-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="3782c-148">40 %</span><span class="sxs-lookup"><span data-stu-id="3782c-148">40%</span></span>    |

<span data-ttu-id="3782c-149">Naudojant 200 % mažėjančios vertės metodą, 200 procentų padalijami iš dėvėjimo metų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="3782c-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="3782c-150">Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.</span><span class="sxs-lookup"><span data-stu-id="3782c-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="3782c-151">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3782c-151">Period</span></span> | <span data-ttu-id="3782c-152">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="3782c-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="3782c-153">Knygos vertė</span><span class="sxs-lookup"><span data-stu-id="3782c-153">Book value</span></span>             | <span data-ttu-id="3782c-154">Balansinės vertė metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="3782c-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="3782c-155">1 metai</span><span class="sxs-lookup"><span data-stu-id="3782c-155">Year 1</span></span> | <span data-ttu-id="3782c-156">(11 000 – 1000) × 40 % = 4000</span><span class="sxs-lookup"><span data-stu-id="3782c-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="3782c-157">11 000 – 4000 = 7000</span><span class="sxs-lookup"><span data-stu-id="3782c-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="3782c-158">11 000 – 1000 – 4000 = 6000</span><span class="sxs-lookup"><span data-stu-id="3782c-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="3782c-159">2 metai</span><span class="sxs-lookup"><span data-stu-id="3782c-159">Year 2</span></span> | <span data-ttu-id="3782c-160">6000 × 40 % = 2400</span><span class="sxs-lookup"><span data-stu-id="3782c-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="3782c-161">7000 – 2400 = 4600</span><span class="sxs-lookup"><span data-stu-id="3782c-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="3782c-162">6000 – 2400 = 3600</span><span class="sxs-lookup"><span data-stu-id="3782c-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="3782c-163">3 metai</span><span class="sxs-lookup"><span data-stu-id="3782c-163">Year 3</span></span> | <span data-ttu-id="3782c-164">3600 × 40 % = 1440</span><span class="sxs-lookup"><span data-stu-id="3782c-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="3782c-165">4600 – 1440 = 3160</span><span class="sxs-lookup"><span data-stu-id="3782c-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="3782c-166">3600 – 1440 = 2160</span><span class="sxs-lookup"><span data-stu-id="3782c-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="3782c-167">Paprastai, kai suma, kuri apskaičiuojama naudojant 200 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.</span><span class="sxs-lookup"><span data-stu-id="3782c-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




