---
title: 150 procentų mažėjančios vertės metodas
description: Šiame straipsnyje apžvelgtas 150 % nusidėvėjimo mažėjančios vertės metodas.
author: saraschi2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1c6b7e92ea8b20123c0b1c1747c49847b0e2420
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827175"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="dc598-103">150 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="dc598-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc598-104">Šiame straipsnyje apžvelgtas 150 % nusidėvėjimo mažėjančios vertės metodas.</span><span class="sxs-lookup"><span data-stu-id="dc598-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="dc598-105">Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **150 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="dc598-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="dc598-106">Šis procentas apskaičiuojamas remiantis ilgalaikio turto dėvėjimo laiku.</span><span class="sxs-lookup"><span data-stu-id="dc598-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="dc598-107">Pavyzdžiui, jei turto dėvėjimo laikas yra penkeri metai, apskaičiuotas procentas yra 30 procentų (150 %÷5).</span><span class="sxs-lookup"><span data-stu-id="dc598-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="dc598-108">Norėdami nustatyti 150 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis.</span><span class="sxs-lookup"><span data-stu-id="dc598-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="dc598-109">Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.</span><span class="sxs-lookup"><span data-stu-id="dc598-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="dc598-110">Nusidėvėjimo metų pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="dc598-110">Selection of depreciation year</span></span>
<span data-ttu-id="dc598-111">Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**.</span><span class="sxs-lookup"><span data-stu-id="dc598-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="dc598-112">Numatytoji reikšmė yra **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="dc598-112">The default value is **Calendar**.</span></span> <span data-ttu-id="dc598-113">Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**.</span><span class="sxs-lookup"><span data-stu-id="dc598-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="dc598-114">Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.</span><span class="sxs-lookup"><span data-stu-id="dc598-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="dc598-115">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="dc598-115">Calendar</span></span>

<span data-ttu-id="dc598-116">**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**.</span><span class="sxs-lookup"><span data-stu-id="dc598-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="dc598-117">Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d.</span><span class="sxs-lookup"><span data-stu-id="dc598-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="dc598-118">Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę.</span><span class="sxs-lookup"><span data-stu-id="dc598-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="dc598-119">Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="dc598-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="dc598-120">Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="dc598-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="dc598-121">Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="dc598-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="dc598-122">Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="dc598-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="dc598-123">Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="dc598-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="dc598-124">Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="dc598-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="dc598-125">Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="dc598-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="dc598-126">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="dc598-126">Fiscal</span></span>

<span data-ttu-id="dc598-127">Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 150 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="dc598-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="dc598-128">Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dc598-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="dc598-129">Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="dc598-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="dc598-130">Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="dc598-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="dc598-131">Koreguojamas kiekvieno laikotarpio nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="dc598-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="dc598-132">Kitų ataskaitinių metų trukmė nustatoma pagal laikotarpių sąranką puslapyje **Ataskaitiniai kalendoriai**.</span><span class="sxs-lookup"><span data-stu-id="dc598-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="dc598-133">Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.</span><span class="sxs-lookup"><span data-stu-id="dc598-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="dc598-134">Pasirinkus **Kasmet**, bendroji ataskaitinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę ataskaitinių metų dieną.</span><span class="sxs-lookup"><span data-stu-id="dc598-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="dc598-135">Pasirinkus **Ataskaitinis laikotarpis**, rodoma apskaičiuota bendroji ataskaitinių metų nusidėvėjimo suma.</span><span class="sxs-lookup"><span data-stu-id="dc598-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="dc598-136">Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dc598-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="dc598-137">150% mažėjančios vertės nusidėvėjimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="dc598-137">Example of 150% reducing balance depreciation</span></span>

| &nbsp;                         | &nbsp; |
|--------------------------------|--------|
| <span data-ttu-id="dc598-138">Įsigijimo savikaina</span><span class="sxs-lookup"><span data-stu-id="dc598-138">Acquisition cost</span></span>               | <span data-ttu-id="dc598-139">11 000</span><span class="sxs-lookup"><span data-stu-id="dc598-139">11,000</span></span> |
| <span data-ttu-id="dc598-140">Likvidacinė vertė</span><span class="sxs-lookup"><span data-stu-id="dc598-140">Salvage value</span></span>                  | <span data-ttu-id="dc598-141">1000</span><span class="sxs-lookup"><span data-stu-id="dc598-141">1,000</span></span>  |
| <span data-ttu-id="dc598-142">Nusidėvėjimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="dc598-142">Depreciation base</span></span>              | <span data-ttu-id="dc598-143">10.000</span><span class="sxs-lookup"><span data-stu-id="dc598-143">10,000</span></span> |
| <span data-ttu-id="dc598-144">Aptarnavimo laikas metais</span><span class="sxs-lookup"><span data-stu-id="dc598-144">Service life years</span></span>             | <span data-ttu-id="dc598-145">5</span><span class="sxs-lookup"><span data-stu-id="dc598-145">5</span></span>      |
| <span data-ttu-id="dc598-146">Metinio nusidėvėjimo procentas</span><span class="sxs-lookup"><span data-stu-id="dc598-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="dc598-147">30 %</span><span class="sxs-lookup"><span data-stu-id="dc598-147">30%</span></span>    |

<span data-ttu-id="dc598-148">150 % mažinančio balanso metodas padalija 150 procentų iš paslaugų gyvavimo metų.</span><span class="sxs-lookup"><span data-stu-id="dc598-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="dc598-149">Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.</span><span class="sxs-lookup"><span data-stu-id="dc598-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="dc598-150">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="dc598-150">Period</span></span> | <span data-ttu-id="dc598-151">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="dc598-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="dc598-152">Knygos vertė</span><span class="sxs-lookup"><span data-stu-id="dc598-152">Book value</span></span>             | <span data-ttu-id="dc598-153">Balansinės vertė metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="dc598-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="dc598-154">1 metai</span><span class="sxs-lookup"><span data-stu-id="dc598-154">Year 1</span></span> | <span data-ttu-id="dc598-155">(11 000 – 1 000) × 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="dc598-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="dc598-156">11 000 – 3 000 = 8 000</span><span class="sxs-lookup"><span data-stu-id="dc598-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="dc598-157">11 000 – 1 000 – 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="dc598-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="dc598-158">2 metai</span><span class="sxs-lookup"><span data-stu-id="dc598-158">Year 2</span></span> | <span data-ttu-id="dc598-159">7 000 × 30 % = 2 100</span><span class="sxs-lookup"><span data-stu-id="dc598-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="dc598-160">8 000 – 2 100 = 5 900</span><span class="sxs-lookup"><span data-stu-id="dc598-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="dc598-161">7 000 – 2 100 = 4 900</span><span class="sxs-lookup"><span data-stu-id="dc598-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="dc598-162">3 metai</span><span class="sxs-lookup"><span data-stu-id="dc598-162">Year 3</span></span> | <span data-ttu-id="dc598-163">4 900 × 30 % = 1 470</span><span class="sxs-lookup"><span data-stu-id="dc598-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="dc598-164">5 900 – 1 470 = 4 430</span><span class="sxs-lookup"><span data-stu-id="dc598-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="dc598-165">4 900 – 1 470 = 3 430</span><span class="sxs-lookup"><span data-stu-id="dc598-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="dc598-166">Paprastai, kai suma, kuri apskaičiuojama naudojant 150 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.</span><span class="sxs-lookup"><span data-stu-id="dc598-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]