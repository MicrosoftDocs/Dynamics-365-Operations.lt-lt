---
title: Mažėjančio balanso nusidėvėjimas
description: Šiame straipsnyje apžvelgtas nusidėvėjimo Mažėjančios vertės metodas.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd4a8726ca194de2e5d95128659f3b212eaace5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179011"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="d17bf-103">Mažėjančio balanso nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="d17bf-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d17bf-104">Šiame straipsnyje apžvelgtas nusidėvėjimo Mažėjančios vertės metodas.</span><span class="sxs-lookup"><span data-stu-id="d17bf-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="d17bf-105">Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio Nusidėvėjimo šablonai lauke Metodas pasirinkus Mažėjantis balansas, šiam nusidėvėjimo šablonui priskirto turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="d17bf-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="d17bf-106">Norėdami nustatyti mažėjančio balanso nusidėvėjimą, turite pasirinkti ir puslapio Nusidėvėjimo šablonai „FastTab“ skirtuko Bendra laukuose.</span><span class="sxs-lookup"><span data-stu-id="d17bf-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="d17bf-107">Pirmiausia lauke Nusidėvėjimo metai pasirinkite metus.</span><span class="sxs-lookup"><span data-stu-id="d17bf-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="d17bf-108">Priklausomai nuo jūsų pasirinkimo, lauke Laikotarpio dažnis atsiranda kitos pasirinktys, kaip paaiškinta kituose skyriuose.</span><span class="sxs-lookup"><span data-stu-id="d17bf-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="d17bf-109">Taip pat turite įvesti nusidėvėjimo profilio lauko Procentas reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d17bf-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="d17bf-110">Pasirinkus pasirinktį Visiškas nusidėvėjimas, likęs nusidėvėjimo pagrindas paimamas iš paskutinio nusidėvėjimo laikotarpio ir gali sudaryti didelę sumą.</span><span class="sxs-lookup"><span data-stu-id="d17bf-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="d17bf-111">Kai kurios šalys / regionai nenaudoja perjungimo į tiesią eilutę metodo.</span><span class="sxs-lookup"><span data-stu-id="d17bf-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="d17bf-112">Perjungimas įvyksta, kai alternatyvaus nusidėvėjimo metodo suma didesnė arba lygi pirminio nusidėvėjimo šablono sumai ir nusidėvėjimo suma yra alternatyvaus metodo suma.</span><span class="sxs-lookup"><span data-stu-id="d17bf-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="d17bf-113">Kadangi turtas, remiantis procentinės išraiškos apskaičiavimais, niekada visiškai nenusidėvės, norėdami, kad būtų įvykdytas visiškas turto nusidėvėjimas, turite pasirinkti pasirinktį Visiškas nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="d17bf-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d17bf-114">Pasirinkti nusidėvėjimo metus.</span><span class="sxs-lookup"><span data-stu-id="d17bf-114">Select a depreciation year</span></span>
<span data-ttu-id="d17bf-115">Puslapio Nusidėvėjimo šablonai lauke Nusidėvėjimo metai galite pasirinkti Kalendorius arba Finansiniai metai.</span><span class="sxs-lookup"><span data-stu-id="d17bf-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="d17bf-116">Nuo jūsų pasirinkimo priklausys, kokios pasirinktys bus galimos lauke Laikotarpio dažnis.</span><span class="sxs-lookup"><span data-stu-id="d17bf-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="d17bf-117">Numatytoji pasirinktis yra Kalendorius.</span><span class="sxs-lookup"><span data-stu-id="d17bf-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="d17bf-118">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="d17bf-118">Calendar</span></span>

<span data-ttu-id="d17bf-119">Pasirinktis Kalendorius kasmet sausio 1 d. atnaujina nusidėvėjimo pagrindą (paprastai tai būna suma, gauta iš balansinės vertės atėmus likvidacinę vertę).</span><span class="sxs-lookup"><span data-stu-id="d17bf-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="d17bf-120">Toliau šioje temoje pateiktame mažėjančio balanso nusidėvėjimo pavyzdyje nusidėvėjimo pagrindas yra stulpelyje Skaičiavimas nurodytas pirmos skaičiavimo išraiškos skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="d17bf-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d17bf-121">Jei pasirinksite Kalendorius, lauke Laikotarpio dažnis galimos toliau nurodytos pasirinktys, nurodančios kalendorinių metų faktines nusidėvėjimo registravimo datas ir sumas.</span><span class="sxs-lookup"><span data-stu-id="d17bf-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="d17bf-122">Kasmet registruojama gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d17bf-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="d17bf-123">Kas mėnesį mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="d17bf-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d17bf-124">Kas ketvirtį ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="d17bf-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d17bf-125">Kas pusmetį pusmečio suma yra registruojama kiekvieno kalendorinio pusmečio pabaigoje (birželio 30 d. ir gruodžio 31 d.).</span><span class="sxs-lookup"><span data-stu-id="d17bf-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d17bf-126">Kasdien registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.</span><span class="sxs-lookup"><span data-stu-id="d17bf-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="d17bf-127">Pavyzdžiui, jei pasirenkate Kasmet, metinis nusidėvėjimas registruojamas tik vieną kartą, kiekvienų metų gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d17bf-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="d17bf-128">Jei pasirenkate Kas mėnesį, mėnesisnis nusidėvėjimas registruojamas kiekvieną mėnesį kaip 1/12 metinio nusidėvėjimo sumos dalis.</span><span class="sxs-lookup"><span data-stu-id="d17bf-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d17bf-129">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d17bf-129">Fiscal</span></span>

<span data-ttu-id="d17bf-130">Lauke Nusidėvėjimo metai pasirinkus Finansiniai metai, naudojamas tiesios eilutės nusidėvėjimo metodas.</span><span class="sxs-lookup"><span data-stu-id="d17bf-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="d17bf-131">Jis apskaičiuojamas remiantis finansiniais metais, kurie nustatomi puslapyje Didžioji knyga pasirinkto finansinio kalendoriaus puslapyje Finansinių metų kalendoriai.</span><span class="sxs-lookup"><span data-stu-id="d17bf-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="d17bf-132">Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="d17bf-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d17bf-133">Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių.</span><span class="sxs-lookup"><span data-stu-id="d17bf-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d17bf-134">Koreguojamas kiekvieno ataskaitinio laikotarpio nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="d17bf-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="d17bf-135">Kitų finansinių metų ilgis priklauso nuo ataskaitinių laikotarpių, kuriuos nustatote, kai puslapyje Finansiniai kalendoriai kuriate naujus finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="d17bf-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="d17bf-136">Pasirinkus Finansiniai metai, lauke Laikotarpio dažnis galimos šios pasirinktys:</span><span class="sxs-lookup"><span data-stu-id="d17bf-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="d17bf-137">Kasmet bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.</span><span class="sxs-lookup"><span data-stu-id="d17bf-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d17bf-138">Ataskaitinis laikotarpis – registruojama bendroji finansinių metų nusidėvėjimo suma, paskirstyta į ataskaitinius laikotarpius, kurie nurodomi pagal puslapyje Didžioji knyga pasirinktą finansinį kalendorių arba pagal pasirinktą ilgalaikio turto knygos kalendorių.</span><span class="sxs-lookup"><span data-stu-id="d17bf-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="d17bf-139">Mažėjančios vertės nusidėvėjimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d17bf-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="d17bf-140">Tarkime, kad ilgalaikio turto įsigijimo kaina yra 11 000, likvidacinė vertė yra 1000, o nusidėvėjimo procento koeficientas yra 30.</span><span class="sxs-lookup"><span data-stu-id="d17bf-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="d17bf-141">Naudojant metodą Mažėjanti vertė, 30 procentų nusidėvėjimo pagrindo (iš balansinės vertės atėmus likvidacinę vertę) yra apskaičiuojami ankstesnio nusidėvėjimo laikotarpio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="d17bf-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="d17bf-142">Pirmų trijų metų nusidėvėjimas rodomas toliau pateikiamoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d17bf-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="d17bf-143">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d17bf-143">Period</span></span> | <span data-ttu-id="d17bf-144">Metinio nusidėvėjimo sumos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d17bf-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="d17bf-145">Balansinės vertė metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="d17bf-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="d17bf-146">1 metai</span><span class="sxs-lookup"><span data-stu-id="d17bf-146">Year 1</span></span> | <span data-ttu-id="d17bf-147">(11 000 - 1 000) \* 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="d17bf-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="d17bf-148">(11 000 - 1000) - 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="d17bf-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="d17bf-149">2 metai</span><span class="sxs-lookup"><span data-stu-id="d17bf-149">Year 2</span></span> | <span data-ttu-id="d17bf-150">(7000 - 1000) \* 30% = 1800</span><span class="sxs-lookup"><span data-stu-id="d17bf-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="d17bf-151">(7000 -1800) = 5200</span><span class="sxs-lookup"><span data-stu-id="d17bf-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="d17bf-152">3 metai</span><span class="sxs-lookup"><span data-stu-id="d17bf-152">Year 3</span></span> | <span data-ttu-id="d17bf-153">(5200 - 1000) \* 30% = 1260</span><span class="sxs-lookup"><span data-stu-id="d17bf-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="d17bf-154">(5200 - 1260) = 3940</span><span class="sxs-lookup"><span data-stu-id="d17bf-154">(5,200 - 1,260) = 3,940</span></span>               |


-





