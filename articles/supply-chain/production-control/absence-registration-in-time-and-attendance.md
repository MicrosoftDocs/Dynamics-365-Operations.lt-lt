---
title: "Neatvykimų registravimas modulyje Laikas ir buvimas darbe"
description: "Šioje temoje aiškinama, kaip tvarkyti neatvykimų registracijas srityje Laikas ir buvimas darbe."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7ef244d5abf762bcaab426cf1cefb232383a8109
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="28eb0-103">Neatvykimų registravimas modulyje Laikas ir buvimas darbe</span><span class="sxs-lookup"><span data-stu-id="28eb0-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28eb0-104">Šioje temoje aprašomos neatvykimo sąvokos ir paaiškinama, kaip tvarkyti neatvykimą srityje Laikas ir buvimas darbe.</span><span class="sxs-lookup"><span data-stu-id="28eb0-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="28eb0-105">Įprastomis darbo valandomis pagrįstas neatvykimas</span><span class="sxs-lookup"><span data-stu-id="28eb0-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="28eb0-106">Darbuotojai, nedirbantys įprastų darbo valandų metu, laikomi neatvykusiais į darbą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="28eb0-107">Įprastos darbo valandos apibrėžtos darbuotojo standartinio laiko profilyje.</span><span class="sxs-lookup"><span data-stu-id="28eb0-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="28eb0-108">Pavyzdžiui, darbuotojas dirba dienos profiliu, kai atėjimas į darbą registruojamas 7.00 val., o išėjimas iš darbo – 15.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="28eb0-109">Jei darbuotojas atėjimą į darbą užregistruoja 9.00 val., laikoma, kad tą dieną jis nuo 7.00 iki 9.00 val. nebuvo darbe.</span><span class="sxs-lookup"><span data-stu-id="28eb0-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="28eb0-110">Tokiu atveju darbuotojai raginami įvesti neatvykimo į darbą priežastį.</span><span class="sxs-lookup"><span data-stu-id="28eb0-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="28eb0-111">Jie nurodyti priežastį gali pasirinkdami neatvykimų kodą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="28eb0-112">Neatvykimų kodai</span><span class="sxs-lookup"><span data-stu-id="28eb0-112">Absence codes</span></span>

<span data-ttu-id="28eb0-113">Neatvykimų kodais apibrėžiami įvairių tipų neatvykimai.</span><span class="sxs-lookup"><span data-stu-id="28eb0-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="28eb0-114">Neatvykimo kodus apibrėžia įmonė.</span><span class="sxs-lookup"><span data-stu-id="28eb0-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="28eb0-115">Neatvykimo kodams gali būti taikomos įvairios taisyklės.</span><span class="sxs-lookup"><span data-stu-id="28eb0-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="28eb0-116">Pavyzdžiui, neatvykimo kodą galima sukonfigūruoti taip, kad jį pritaikius būtų atskaitomi arba paskiriami mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="28eb0-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="28eb0-117">Pavyzdžiui, įmonė darbuotojai neatvykimo kodą **Vėluoja** naudotų tada, jei jie į darbą ateina vėlai be pateisinamos priežasties.</span><span class="sxs-lookup"><span data-stu-id="28eb0-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="28eb0-118">Įmonė taip pat apibrėžia **Vidinių kursų** neatvykimo kodą, kurį darbuotojai vidiniuose kursuose praleistam laikui žymėti.</span><span class="sxs-lookup"><span data-stu-id="28eb0-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="28eb0-119">Šiuos neatvykimo kodus galima nustatyti taip, kad nurodžius kodą **Vėluoja** iš darbo užmokesčio atskaitomi pinigai, bet nurodžius kodą **Vidiniai kursai** pinigai iš darbuotojo darbo užmokesčio neatskaitomi.</span><span class="sxs-lookup"><span data-stu-id="28eb0-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="28eb0-120">Galite nustatyti automatinius neatvykimo kodus.</span><span class="sxs-lookup"><span data-stu-id="28eb0-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="28eb0-121">Šiuos neatvykimo kodus galima panaudoti darbuotojo laikui, kai neatvykimas neregistruojamas, apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="28eb0-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="28eb0-122">Darbuotojo darbo laiko profilyje nustatoma, ar neatvykimo laikas bus naudojamas standartiniam ar nukrypimo laikui.</span><span class="sxs-lookup"><span data-stu-id="28eb0-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="28eb0-123">Standartinio ir nukrypimo laiko nustatymas</span><span class="sxs-lookup"><span data-stu-id="28eb0-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="28eb0-124">Sukonfigūruokite standartinio ir nukrypimo laiko parametrus naudodami parinktis **Automatinis neatvykimo įvedimas** ir **Automatinis nukrypimo įvedimas -**, pateikiamus puslapyje **Laiko ir buvimo darbe parametrai**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="28eb0-125">Neatvykimų grupės</span><span class="sxs-lookup"><span data-stu-id="28eb0-125">Absence groups</span></span>

<span data-ttu-id="28eb0-126">Neatvykimų kodai sugrupuojanti į neatvykimų grupes.</span><span class="sxs-lookup"><span data-stu-id="28eb0-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="28eb0-127">Neatvykimų grupėse sugrupuojami vienodų charakteristikų neatvykimų kodai.</span><span class="sxs-lookup"><span data-stu-id="28eb0-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="28eb0-128">Pavyzdžiai: leistino neatvykimo kodai arba neatvykimo į darbą dėl apsilankymo pas gydytoją, dalyvavimo komisijoje ar sergančio vaiko kodai.</span><span class="sxs-lookup"><span data-stu-id="28eb0-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="28eb0-129">Suplanuotas neatvykimas</span><span class="sxs-lookup"><span data-stu-id="28eb0-129">Planned absence</span></span>

<span data-ttu-id="28eb0-130">Jei žinote, kad darbuotojo tam tikrą laikotarpį nebus darbe, pvz., dėl būsimų atostogų, galite naudoti suplanuotus neatvykimus.</span><span class="sxs-lookup"><span data-stu-id="28eb0-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="28eb0-131">Suplanuotą neatvykimą galite nustatyti tam tikru būdu sukonfigūruodami neatvykimo kodą, kad į jį būtų įtraukta suplanuoto neatvykimo tikimybė.</span><span class="sxs-lookup"><span data-stu-id="28eb0-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="28eb0-132">Nustatydami suplanuotą neatvykimą, neatvykimo laikotarpiu, kai skaičiuojamos vartotojo laiko registracijos, nesate raginami pateikti neatvykimo kodą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="28eb0-133">Galima apibrėžti vieno darbuotojo suplanuotą neatvykimą arba paketinę užduotį, kad informacija apie darbuotojų neatvykimus būtų atnaujinama masiškai.</span><span class="sxs-lookup"><span data-stu-id="28eb0-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="28eb0-134">Suplanuotų neatvykimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="28eb0-134">Set up planned absence</span></span>

1. <span data-ttu-id="28eb0-135">Pasirinkite **Personalas** &gt; **Darbininkai** &gt; **Darbuotojai** ir pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="28eb0-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="28eb0-136">Pasirinkite **Laikas** &gt; **Laiko priskyrimas** &gt; **Neatvykimų laiko registracija** ir nustatykite suplanuotą neatvykimą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="28eb0-137">Nutraukiamas suplanuotas neatvykimas</span><span class="sxs-lookup"><span data-stu-id="28eb0-137">Interrupted planned absence</span></span>

<span data-ttu-id="28eb0-138">Jei nustatydami suplanuotą neatvykimą taikysite parinktį **Nutraukti**, darbuotojui užsiregistravus suplanuoto laikotarpio metu, suplanuotas neatvykimas bus nutrauktas.</span><span class="sxs-lookup"><span data-stu-id="28eb0-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="28eb0-139">Suplanuotas neatvykimas bus pažymėtas kaip **Nutraukta** ir neturės įtakos būsimiems skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="28eb0-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="28eb0-140">Suplanuoto neatvykimo nutraukimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="28eb0-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="28eb0-141">Atidarykite puslapį **Neatvykimo laiko registracija**, kaip aprašyta suplanuoto neatvykimo nustatymo procedūroje.</span><span class="sxs-lookup"><span data-stu-id="28eb0-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="28eb0-142">Pasirinkite **Nutraukti**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-142">Select **Interrupt**.</span></span>

<span data-ttu-id="28eb0-143">Parinktis **Nutraukti** taikoma, kai laikas registruojamas naudojant darbo laiko terminalą arba darbo laiko įrenginį.</span><span class="sxs-lookup"><span data-stu-id="28eb0-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="28eb0-144">Parinktis netaikoma, jei registracijos įvedamos skaičiavimo ir patvirtinimo puslapiuose arba puslapyje **Elektroninė laiko kortelė**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="28eb0-145">Neatvykimų naudojimų pavyzdžiai nukrypimų profilyje</span><span class="sxs-lookup"><span data-stu-id="28eb0-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="28eb0-146">Toliau pateiktuose trijuose šablonuose rodoma, kaip apskaičiuojamas neatvykimas profilyje su nukrypimo laikotarpiais.</span><span class="sxs-lookup"><span data-stu-id="28eb0-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="28eb0-147">Šiuose pavyzdžiuose naudojamas toliau nurodytas profilis.</span><span class="sxs-lookup"><span data-stu-id="28eb0-147">The examples use the following profile.</span></span>

| <span data-ttu-id="28eb0-148">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="28eb0-148">Clock-in</span></span> | <span data-ttu-id="28eb0-149">Standartinis laikas</span><span class="sxs-lookup"><span data-stu-id="28eb0-149">Standard time</span></span>    | <span data-ttu-id="28eb0-150">Pertrauka</span><span class="sxs-lookup"><span data-stu-id="28eb0-150">Break</span></span>             | <span data-ttu-id="28eb0-151">Standartinis laikas</span><span class="sxs-lookup"><span data-stu-id="28eb0-151">Standard time</span></span> | <span data-ttu-id="28eb0-152">Nukrypimas-</span><span class="sxs-lookup"><span data-stu-id="28eb0-152">Flex-</span></span>        | <span data-ttu-id="28eb0-153">Išėjimas iš darbo</span><span class="sxs-lookup"><span data-stu-id="28eb0-153">Clock-out</span></span> | <span data-ttu-id="28eb0-154">Nukrypimas+</span><span class="sxs-lookup"><span data-stu-id="28eb0-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="28eb0-155">8.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-155">8 AM</span></span>     | <span data-ttu-id="28eb0-156">Nuo 9.00 iki 11.30 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="28eb0-157">Nuo 11.30 iki 12.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="28eb0-158">Nuo 12.00 iki 15.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-158">12 PM to 3 PM</span></span> | <span data-ttu-id="28eb0-159">Nuo 15.00 iki 16.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-159">3 PM to 4 PM</span></span> | <span data-ttu-id="28eb0-160">16.00</span><span class="sxs-lookup"><span data-stu-id="28eb0-160">4 PM</span></span>      | <span data-ttu-id="28eb0-161">Nuo 16.00 iki 18.00 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="28eb0-162">1 pavyzdys: išsiregistravimas iš darbo nukrypimo- laikotarpiu</span><span class="sxs-lookup"><span data-stu-id="28eb0-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="28eb0-163">Darbuotojas atėjimą į darbą užregistruoja 8.00 val., o išsiregistruoja 15.30 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="28eb0-164">Tokiu atveju neatvykimas neskaičiuojamas, nes darbuotojas iš darbo išsiregistruoja nukrypimo- laikotarpiu ir iš darbuotojo nukrypimų balansų atskaičiuojamas pusvalandis.</span><span class="sxs-lookup"><span data-stu-id="28eb0-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="28eb0-165">2 pavyzdys: išsiregistravimas iš darbo standartinio laiko laikotarpiu</span><span class="sxs-lookup"><span data-stu-id="28eb0-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="28eb0-166">Darbuotojas atėjimą į darbą užregistruoja 8.00 val., o išėjimą išregistruoja 15.30 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="28eb0-167">Tokiu atveju neatvykimas skaičiuojamas nuo 14.30 iki 16.00 val., nes darbuotojas iš darbo išsiregistruoja standartinio laiko laikotarpiu ir registruojamas 1,5 valandos neatvykimo laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="28eb0-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="28eb0-168">Šiam laikotarpiui reikia priskirti neatvykimo kodą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="28eb0-169">3 pavyzdys: išsiregistravimas iš darbo nukrypimo+ laikotarpiu</span><span class="sxs-lookup"><span data-stu-id="28eb0-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="28eb0-170">Darbuotojas atėjimą į darbą užregistruoja 8.00 val., o išsiregistruoja 15.30 val.</span><span class="sxs-lookup"><span data-stu-id="28eb0-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="28eb0-171">Tokiu atveju neatvykimas neskaičiuojamas, nes darbuotojas iš darbo išsiregistruoja nukrypimo+ laikotarpiu ir prie darbuotojo nukrypimų balansų pridedamas pusvalandis.</span><span class="sxs-lookup"><span data-stu-id="28eb0-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="28eb0-172">Neatvykimas skaičiavimo ir patvirtinimo procese</span><span class="sxs-lookup"><span data-stu-id="28eb0-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="28eb0-173">Darbuotojo laiko registracijos turi būti apskaičiuojamas ir patvirtinamos prieš jas perkeliant į algalapio sistemą kaip mokėjimo elementus.</span><span class="sxs-lookup"><span data-stu-id="28eb0-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="28eb0-174">Tvirtintojas gali keisti darbuotojo darbo laiko registracijas.</span><span class="sxs-lookup"><span data-stu-id="28eb0-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="28eb0-175">Tvirtintojas gali keisti netgi bet kokį darbuotojo užregistruotą neatvykimą.</span><span class="sxs-lookup"><span data-stu-id="28eb0-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="28eb0-176">Jei tvirtintojas rankiniu būdu įveda laikotarpį, kuriam priskirtas neatvykimo kodas, tam laikotarpiui skirtas neatvykimas kodas nėra perrašomas Laiko ir buvimo darbe parametruose įvestu numatytuoju neatvykimo kodu.</span><span class="sxs-lookup"><span data-stu-id="28eb0-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="28eb0-177">Pavyzdžiui, darbuotoja atėjimą į darbą užregistruoja 10.00 val. ir pasirenka neatvykimo kodą, kuriuo žymimas vėlavimas.</span><span class="sxs-lookup"><span data-stu-id="28eb0-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="28eb0-178">Vėliau darbuotoja informuoja savo prižiūrėtoją, kad ji nuo 8.00 iki 10.00 val. lankėsi pas gydytoją.</span><span class="sxs-lookup"><span data-stu-id="28eb0-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="28eb0-179">Dėl apsilankymo pas gydytoją iš darbuotojo atlyginimo pinigai neturi būti atskaitomi.</span><span class="sxs-lookup"><span data-stu-id="28eb0-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="28eb0-180">Todėl tokiu atveju prižiūrėtojas dviejų valandų neatvykimą nuo 8.00 iki 10.00 val. gali koreguoti rankiniu būdu įvesdamas neatvykimo kodą, kuriuo žymima, kad darbuotojas tas dvi valandas sirgo.</span><span class="sxs-lookup"><span data-stu-id="28eb0-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="28eb0-181">Neatvykimo apskaičiavimas ir patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="28eb0-181">Calculate and approve absence</span></span>

- <span data-ttu-id="28eb0-182">Pasirinkite **Laikas ir buvimas darbe** &gt; **Peržiūrėti ir patvirtinti** &gt; **Patvirtinti arba skaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="28eb0-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>

