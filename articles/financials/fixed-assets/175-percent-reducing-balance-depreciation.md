---
title: "175 procentų mažėjančios vertės metodas"
description: "Šiame straipsnyje apžvelgtas 175 % nusidėvėjimo mažėjančios vertės metodas."
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
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 318e111f784157666c2853bcd6d5b3af2c9ffdc5
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="d8d59-103">175 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="d8d59-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d8d59-104">Šiame straipsnyje apžvelgtas 175 % nusidėvėjimo mažėjančios vertės metodas.</span><span class="sxs-lookup"><span data-stu-id="d8d59-104">This article gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="d8d59-105">Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **175 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="d8d59-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="d8d59-106">Norėdami nustatyti 175 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis.</span><span class="sxs-lookup"><span data-stu-id="d8d59-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d8d59-107">Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d8d59-108">Pasirinkite nusidėvėjimo metus.</span><span class="sxs-lookup"><span data-stu-id="d8d59-108">Select a depreciation year</span></span>
<span data-ttu-id="d8d59-109">Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d8d59-110">Numatytoji reikšmė yra **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="d8d59-111">Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="d8d59-112">Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.</span><span class="sxs-lookup"><span data-stu-id="d8d59-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="d8d59-113">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="d8d59-113">Calendar</span></span>

<span data-ttu-id="d8d59-114">**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="d8d59-115">Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="d8d59-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="d8d59-116">Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę.</span><span class="sxs-lookup"><span data-stu-id="d8d59-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="d8d59-117">Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="d8d59-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d8d59-118">Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="d8d59-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d8d59-119">Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d8d59-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="d8d59-120">Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="d8d59-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d8d59-121">Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="d8d59-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d8d59-122">Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="d8d59-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d8d59-123">Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="d8d59-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d8d59-124">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d8d59-124">Fiscal</span></span>

<span data-ttu-id="d8d59-125">Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 175 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="d8d59-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="d8d59-126">Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d8d59-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="d8d59-127">Daugiau informacijos žr. [Ataskaitiniai kalendoriai, ataskaitiniai metai ir laikotarpiai.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="d8d59-127">For more information, see [Fiscal calendars, fiscal years, and periods.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="d8d59-128">Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="d8d59-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d8d59-129">Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="d8d59-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d8d59-130">Kiekvieno laikotarpio nusidėvėjimas koreguojamas automatiškai, o kitų ataskaitinių metų trukmė nustatoma pagal puslapyje **Ataskaitiniai kalendoriai** nustatytus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="d8d59-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d8d59-131">Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="d8d59-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d8d59-132">Pasirinkus **Kasmet**, bendroji ataskaitinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę ataskaitinių metų dieną.</span><span class="sxs-lookup"><span data-stu-id="d8d59-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d8d59-133">**Ataskaitinis laikotarpis** apskaičiuoja bendrąją ataskaitinių metų nusidėvėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="d8d59-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="d8d59-134">Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d8d59-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="d8d59-135">175% mažėjančios vertės nusidėvėjimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d8d59-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="d8d59-136">Įsigijimo savikaina</span><span class="sxs-lookup"><span data-stu-id="d8d59-136">Acquisition cost</span></span>               | <span data-ttu-id="d8d59-137">11 000</span><span class="sxs-lookup"><span data-stu-id="d8d59-137">11,000</span></span> |
| <span data-ttu-id="d8d59-138">Likvidacinė vertė</span><span class="sxs-lookup"><span data-stu-id="d8d59-138">Salvage value</span></span>                  | <span data-ttu-id="d8d59-139">1000</span><span class="sxs-lookup"><span data-stu-id="d8d59-139">1,000</span></span>  |
| <span data-ttu-id="d8d59-140">Nusidėvėjimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="d8d59-140">Depreciation base</span></span>              | <span data-ttu-id="d8d59-141">10.000</span><span class="sxs-lookup"><span data-stu-id="d8d59-141">10,000</span></span> |
| <span data-ttu-id="d8d59-142">Aptarnavimo laikas metais</span><span class="sxs-lookup"><span data-stu-id="d8d59-142">Service life years</span></span>             | <span data-ttu-id="d8d59-143">5</span><span class="sxs-lookup"><span data-stu-id="d8d59-143">5</span></span>      |
| <span data-ttu-id="d8d59-144">Metinio nusidėvėjimo procentas</span><span class="sxs-lookup"><span data-stu-id="d8d59-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="d8d59-145">35 %</span><span class="sxs-lookup"><span data-stu-id="d8d59-145">35%</span></span>    |

<span data-ttu-id="d8d59-146">Naudojant 175 % mažėjančios vertės nusidėvėjimo metodą, 175 procentai padalijami iš dėvėjimo metų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="d8d59-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="d8d59-147">Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.</span><span class="sxs-lookup"><span data-stu-id="d8d59-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="d8d59-148">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d8d59-148">Period</span></span> | <span data-ttu-id="d8d59-149">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d8d59-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d8d59-150">Knygos vertė</span><span class="sxs-lookup"><span data-stu-id="d8d59-150">Book value</span></span>                  | <span data-ttu-id="d8d59-151">Balansinės vertė metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="d8d59-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="d8d59-152">1 metai</span><span class="sxs-lookup"><span data-stu-id="d8d59-152">Year 1</span></span> | <span data-ttu-id="d8d59-153">(11 000 – 1 000) × 35 % = 3 500</span><span class="sxs-lookup"><span data-stu-id="d8d59-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="d8d59-154">11 000 – 3 500 = 7 500</span><span class="sxs-lookup"><span data-stu-id="d8d59-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="d8d59-155">11 000 – 1 000 – 3 500 = 6 500</span><span class="sxs-lookup"><span data-stu-id="d8d59-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="d8d59-156">2 metai</span><span class="sxs-lookup"><span data-stu-id="d8d59-156">Year 2</span></span> | <span data-ttu-id="d8d59-157">6 500 × 35 % = 2 275</span><span class="sxs-lookup"><span data-stu-id="d8d59-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="d8d59-158">7 500 – 2 275 = 5 225</span><span class="sxs-lookup"><span data-stu-id="d8d59-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="d8d59-159">6 500 – 2 275 = 4 225</span><span class="sxs-lookup"><span data-stu-id="d8d59-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="d8d59-160">3 metai</span><span class="sxs-lookup"><span data-stu-id="d8d59-160">Year 3</span></span> | <span data-ttu-id="d8d59-161">4 225 × 35 % = 1 478,75</span><span class="sxs-lookup"><span data-stu-id="d8d59-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="d8d59-162">5 225 – 1 478,75 = 3 746,25</span><span class="sxs-lookup"><span data-stu-id="d8d59-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="d8d59-163">4 225 – 1 478,75 = 2 746,25</span><span class="sxs-lookup"><span data-stu-id="d8d59-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="d8d59-164">Paprastai, kai suma, kuri apskaičiuojama naudojant 175 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.</span><span class="sxs-lookup"><span data-stu-id="d8d59-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




