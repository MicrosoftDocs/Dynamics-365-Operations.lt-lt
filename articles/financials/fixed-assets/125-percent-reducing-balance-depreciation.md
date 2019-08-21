---
title: 125 procentų mažėjančios vertės metodas
description: Šiame straipsnyje apžvelgtas 125 % nusidėvėjimo mažėjančios vertės metodas.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5af050fb6099b583be4e9c60ba56dacf38d31c08
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840870"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="7f9c1-103">125 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="7f9c1-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f9c1-104">Šiame straipsnyje apžvelgtas 125 % nusidėvėjimo mažėjančios vertės metodas.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="7f9c1-105">Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **125 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="7f9c1-106">Šis procentas apskaičiuojamas remiantis ilgalaikio turto dėvėjimo laiku.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="7f9c1-107">Pavyzdžiui, jei turto dėvėjimo laikas yra penkeri metai, apskaičiuotas procentas yra 25 procentai (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="7f9c1-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="7f9c1-108">Norėdami nustatyti 125 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="7f9c1-109">Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="7f9c1-110">Pasirinkite nusidėvėjimo metus.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-110">Select a depreciation year</span></span>
<span data-ttu-id="7f9c1-111">Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="7f9c1-112">Numatytoji reikšmė yra **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="7f9c1-113">Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="7f9c1-114">Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="7f9c1-115">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="7f9c1-115">Calendar</span></span>

<span data-ttu-id="7f9c1-116">**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="7f9c1-117">Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="7f9c1-118">Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="7f9c1-119">Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="7f9c1-120">Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="7f9c1-121">Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="7f9c1-122">Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="7f9c1-123">Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="7f9c1-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="7f9c1-124">Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="7f9c1-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="7f9c1-125">Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="7f9c1-126">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="7f9c1-126">Fiscal</span></span>

<span data-ttu-id="7f9c1-127">Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 125 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="7f9c1-128">Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="7f9c1-129">Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="7f9c1-130">Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="7f9c1-131">Kiekvieno laikotarpio nusidėvėjimas koreguojamas automatiškai, o kitų ataskaitinių metų trukmė nustatoma pagal puslapyje **Ataskaitiniai kalendoriai** nustatytus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="7f9c1-132">Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="7f9c1-133">**Kasmet** apskaičiuota bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="7f9c1-134">Pasirinkus **Ataskaitinis laikotarpis**, rodoma apskaičiuota bendroji ataskaitinių metų nusidėvėjimo suma.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="7f9c1-135">Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="7f9c1-136">125% mažėjančios vertės nusidėvėjimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7f9c1-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="7f9c1-137">Įsigijimo savikaina</span><span class="sxs-lookup"><span data-stu-id="7f9c1-137">Acquisition cost</span></span>               | <span data-ttu-id="7f9c1-138">11 000</span><span class="sxs-lookup"><span data-stu-id="7f9c1-138">11,000</span></span> |
| <span data-ttu-id="7f9c1-139">Likvidacinė vertė</span><span class="sxs-lookup"><span data-stu-id="7f9c1-139">Salvage value</span></span>                  | <span data-ttu-id="7f9c1-140">1000</span><span class="sxs-lookup"><span data-stu-id="7f9c1-140">1,000</span></span>  |
| <span data-ttu-id="7f9c1-141">Nusidėvėjimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="7f9c1-141">Depreciation base</span></span>              | <span data-ttu-id="7f9c1-142">10.000</span><span class="sxs-lookup"><span data-stu-id="7f9c1-142">10,000</span></span> |
| <span data-ttu-id="7f9c1-143">Aptarnavimo laikas metais</span><span class="sxs-lookup"><span data-stu-id="7f9c1-143">Service life years</span></span>             | <span data-ttu-id="7f9c1-144">5</span><span class="sxs-lookup"><span data-stu-id="7f9c1-144">5</span></span>      |
| <span data-ttu-id="7f9c1-145">Metinio nusidėvėjimo procentas</span><span class="sxs-lookup"><span data-stu-id="7f9c1-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="7f9c1-146">25 %</span><span class="sxs-lookup"><span data-stu-id="7f9c1-146">25%</span></span>    |

<span data-ttu-id="7f9c1-147">Naudojant 125 % mažėjančios vertės metodą, 125 procentai padalijami iš dėvėjimo metų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="7f9c1-148">Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="7f9c1-149">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="7f9c1-149">Period</span></span> | <span data-ttu-id="7f9c1-150">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="7f9c1-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="7f9c1-151">Knygos vertė</span><span class="sxs-lookup"><span data-stu-id="7f9c1-151">Book value</span></span>                    | <span data-ttu-id="7f9c1-152">Balansinės vertė metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="7f9c1-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="7f9c1-153">1 metai</span><span class="sxs-lookup"><span data-stu-id="7f9c1-153">Year 1</span></span> | <span data-ttu-id="7f9c1-154">(11 000 – 1 000) × 25 % = 2 500</span><span class="sxs-lookup"><span data-stu-id="7f9c1-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="7f9c1-155">(11 000 – 2 500) = 8 500</span><span class="sxs-lookup"><span data-stu-id="7f9c1-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="7f9c1-156">(11 000 – 1 000 – 2 500) = 7 500</span><span class="sxs-lookup"><span data-stu-id="7f9c1-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="7f9c1-157">2 metai</span><span class="sxs-lookup"><span data-stu-id="7f9c1-157">Year 2</span></span> | <span data-ttu-id="7f9c1-158">7 500 × 25 % = 1 875</span><span class="sxs-lookup"><span data-stu-id="7f9c1-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="7f9c1-159">(8 500 – 1 875) = 6 625</span><span class="sxs-lookup"><span data-stu-id="7f9c1-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="7f9c1-160">(7 500 – 1 875) = 5 625</span><span class="sxs-lookup"><span data-stu-id="7f9c1-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="7f9c1-161">3 metai</span><span class="sxs-lookup"><span data-stu-id="7f9c1-161">Year 3</span></span> | <span data-ttu-id="7f9c1-162">5 625 × 25 % = 1 406,25</span><span class="sxs-lookup"><span data-stu-id="7f9c1-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="7f9c1-163">(6 625 – 1 406,25) = 5 218,75</span><span class="sxs-lookup"><span data-stu-id="7f9c1-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="7f9c1-164">(5 625 – 1 406,25) = 4 218,75</span><span class="sxs-lookup"><span data-stu-id="7f9c1-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="7f9c1-165">Paprastai, kai suma, kuri apskaičiuojama naudojant 125 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



