---
title: Nustatyti kokybės užsakymus
description: Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a073de7bdfd2ef597c09a8066ff2b6a7721ca62
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561322"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="f5c24-103">Nustatyti kokybės užsakymus</span><span class="sxs-lookup"><span data-stu-id="f5c24-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5c24-104">Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="f5c24-105">Procedūrą paprastai atlieka kokybės vadovas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="f5c24-106">Šis procesas apima kokybės grupės kūrimą apibrėžti prekėms, iš kurių bus imami pavyzdžiai, ir bandymo grupės kūrimą grupuoti bandymams, kuriuos reikia atlikti su prekėmis kokybės grupėje.</span><span class="sxs-lookup"><span data-stu-id="f5c24-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="f5c24-107">Šį vedlį galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="f5c24-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="f5c24-108">Kokybės valdymo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="f5c24-108">Enable quality management</span></span>
1. <span data-ttu-id="f5c24-109">Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="f5c24-110">Spustelėkite skirtuką Kokybės valdymas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="f5c24-111">Nustatykite parinkčiai Naudoti kokybės valdymą reikšmę Taip.</span><span class="sxs-lookup"><span data-stu-id="f5c24-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="f5c24-112">Spustelėkite Ataskaitų sąranka.</span><span class="sxs-lookup"><span data-stu-id="f5c24-112">Click Report setup.</span></span>
    * <span data-ttu-id="f5c24-113">USMF kokybės valdymo ataskaitos sąranka jau yra nurodyta.</span><span class="sxs-lookup"><span data-stu-id="f5c24-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="f5c24-114">Jei tai buvo atlikta, čia galite įtraukti naujas skirtingų ataskaitų tipų eilutes ir pasirinkti kiekvienos ataskaitos dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="f5c24-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-115">Close the page.</span></span>
6. <span data-ttu-id="f5c24-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="f5c24-117">Kurti bandymą</span><span class="sxs-lookup"><span data-stu-id="f5c24-117">Create a test</span></span>
1. <span data-ttu-id="f5c24-118">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="f5c24-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-119">Click New.</span></span>
3. <span data-ttu-id="f5c24-120">Lauke Bandymas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="f5c24-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5c24-122">Lauke Tipas pasirinkite „Parinktis‟.</span><span class="sxs-lookup"><span data-stu-id="f5c24-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="f5c24-123">Šiame pavyzdyje pasirinksime „Parinktis‟ – bus galima priskirti tikrinimo rezultatus pagal iš anksto apibrėžtas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f5c24-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="f5c24-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-124">Click Save.</span></span>
7. <span data-ttu-id="f5c24-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="f5c24-126">Kurti bandymų kintamuosius, kad būtų galima apibrėžti, kaip įrašomi bandymų rezultatai</span><span class="sxs-lookup"><span data-stu-id="f5c24-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="f5c24-127">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymo kintamieji.</span><span class="sxs-lookup"><span data-stu-id="f5c24-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="f5c24-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-128">Click New.</span></span>
3. <span data-ttu-id="f5c24-129">Lauke Kintamasis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="f5c24-130">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5c24-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-131">Click Save.</span></span>
6. <span data-ttu-id="f5c24-132">Spustelėkite Rezultatai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-132">Click Outcomes.</span></span>
7. <span data-ttu-id="f5c24-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-133">Click New.</span></span>
8. <span data-ttu-id="f5c24-134">Lauke Rezultatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="f5c24-135">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f5c24-136">Lauke Rezultato būsena pasirinkite „Sėkmingai‟.</span><span class="sxs-lookup"><span data-stu-id="f5c24-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="f5c24-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-137">Click Save.</span></span>
12. <span data-ttu-id="f5c24-138">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-138">Click New.</span></span>
13. <span data-ttu-id="f5c24-139">Lauke Rezultatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="f5c24-140">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="f5c24-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-141">Click Save.</span></span>
16. <span data-ttu-id="f5c24-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-142">Close the page.</span></span>
17. <span data-ttu-id="f5c24-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="f5c24-144">Nustatyti prekių pavyzdžių ėmimą</span><span class="sxs-lookup"><span data-stu-id="f5c24-144">Set up item sampling</span></span>
1. <span data-ttu-id="f5c24-145">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Prekių pavyzdžių ėmimas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="f5c24-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-146">Click New.</span></span>
3. <span data-ttu-id="f5c24-147">Lauke Prekių pavyzdžių ėmimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="f5c24-148">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5c24-149">Lauke Vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5c24-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="f5c24-150">Ši reikšmė susijusi su kiekio specifikacija, pasirinkta gretimame lauke.</span><span class="sxs-lookup"><span data-stu-id="f5c24-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="f5c24-151">Išplėskite arba sutraukite sekciją Procesas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="f5c24-152">Pažymėkite arba panaikinkite žymės langelio Visiškas blokavimas žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="f5c24-153">Jei pasirenkate šią parinktį ir jei tikrinti nepavyksta, užblokuojama visa partija ar užsakymo eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="f5c24-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="f5c24-154">Jei jos nepasirenkate, blokuojamos tik kokybės užsakymo prekės.</span><span class="sxs-lookup"><span data-stu-id="f5c24-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="f5c24-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-155">Click Save.</span></span>
9. <span data-ttu-id="f5c24-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="f5c24-157">Kurti kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="f5c24-157">Create a quality group</span></span>
1. <span data-ttu-id="f5c24-158">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės grupės.</span><span class="sxs-lookup"><span data-stu-id="f5c24-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="f5c24-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-159">Click New.</span></span>
3. <span data-ttu-id="f5c24-160">Lauke Kokybės grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="f5c24-161">Naudokite aprašomąjį pavadinimą, kad būtų lengviau identifikuoti, kokios rūšies prekės bus grupėje (pavyzdžių ėmimo kriterijai).</span><span class="sxs-lookup"><span data-stu-id="f5c24-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="f5c24-162">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5c24-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-163">Click Save.</span></span>
6. <span data-ttu-id="f5c24-164">Spustelėkite Įtraukti prekes.</span><span class="sxs-lookup"><span data-stu-id="f5c24-164">Click Add items.</span></span>
7. <span data-ttu-id="f5c24-165">Pasirinkti eilutę Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="f5c24-165">Select the Item number row</span></span>
    * <span data-ttu-id="f5c24-166">Šiame pavyzdyje filtravimas bus vykdomas pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="f5c24-167">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f5c24-168">Pavyzdžiui, įveskite T\*, kad filtruotumėte tuos prekių numerius, kurie prasideda T.</span><span class="sxs-lookup"><span data-stu-id="f5c24-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="f5c24-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f5c24-169">Click OK.</span></span>
10. <span data-ttu-id="f5c24-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f5c24-170">Click OK.</span></span>
11. <span data-ttu-id="f5c24-171">Spustelėkite Prekių kokybės grupės.</span><span class="sxs-lookup"><span data-stu-id="f5c24-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="f5c24-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-172">Close the page.</span></span>
13. <span data-ttu-id="f5c24-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="f5c24-174">Kurti bandymų grupę</span><span class="sxs-lookup"><span data-stu-id="f5c24-174">Create a test group</span></span>
1. <span data-ttu-id="f5c24-175">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymų grupės.</span><span class="sxs-lookup"><span data-stu-id="f5c24-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="f5c24-176">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-176">Click New.</span></span>
3. <span data-ttu-id="f5c24-177">Lauke Bandymų grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="f5c24-178">Suteikite bandymų grupei pavadinimą, kuris padės prisiminti, kokie bandymai vykdomi ir su kuria kokybės grupe ji turėtų būti susieta.</span><span class="sxs-lookup"><span data-stu-id="f5c24-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="f5c24-179">Pavyzdžiui, jei ji bus naudojama su kokybės grupe, kuri pasirenka prekes, prasidedančias „T‟, galite ją pavadinti „T prekių bandymai‟.</span><span class="sxs-lookup"><span data-stu-id="f5c24-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="f5c24-180">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f5c24-181">Lauke Prekių pavyzdžių ėmimas pasirinkite prekių pavyzdžių ėmimo eilutę, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="f5c24-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="f5c24-182">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5c24-183">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-183">Click Add.</span></span>
8. <span data-ttu-id="f5c24-184">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5c24-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="f5c24-185">Lauke Bandymas pasirinkite bandymą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="f5c24-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="f5c24-186">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f5c24-187">Spustelėkite skirtuką Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-187">Click the Test tab.</span></span>
12. <span data-ttu-id="f5c24-188">Lauke Kintamasis pasirinkite bandymo kintamąjį, kurį sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="f5c24-189">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="f5c24-190">Lauke Numatytasis rezultatas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f5c24-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f5c24-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f5c24-192">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-192">Click Save.</span></span>
17. <span data-ttu-id="f5c24-193">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="f5c24-194">Apibrėžti, kada bus kuriami kokybės užsakymai</span><span class="sxs-lookup"><span data-stu-id="f5c24-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="f5c24-195">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės susiejimai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="f5c24-196">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-196">Click New.</span></span>
3. <span data-ttu-id="f5c24-197">Lauke Nuorodos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="f5c24-198">Lauke Prekės kodas pasirinkite „Grupė‟.</span><span class="sxs-lookup"><span data-stu-id="f5c24-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="f5c24-199">Šiame pavyzdyje pasirinksime „Grupė‟ ir naudosime anksčiau savo sukurtą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="f5c24-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="f5c24-200">Taip pat galite nustatyti „Lentelė‟, kad prekes nurodytumėte rankiniu būdu, arba pasirinkti „Visi‟, kad visos prekės būtų pridėtos į kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="f5c24-201">Lauke Prekė pasirinkite kokybės grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="f5c24-202">Galimos parinktys lauke Prekė priklauso nuo to, ką nustatote lauke Prekės kodas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="f5c24-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5c24-204">Išplėskite arba sutraukite sekciją Procesas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="f5c24-205">Lauke Įvykio tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="f5c24-206">Tai yra įvykis, kuris suaktyvina bandymą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-206">This is the event that triggers the test.</span></span> <span data-ttu-id="f5c24-207">Čia galimos parinktys priklauso nuo to, kokį procesą pasirinkote lauke Nuorodos tipas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="f5c24-208">Lauke Vykdymas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="f5c24-209">Išplėskite arba sutraukite sekciją Kokybės užsakymo procesas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="f5c24-210">Lauke Įvykių blokavimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f5c24-211">Šiame lauke rodomas procesų, kuriuos galima blokuoti, jei kokybės užsakymas vis dar atidarytas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="f5c24-212">Parinktys priklauso nuo to, ką pasirinkote lauke Įvykio tipas.</span><span class="sxs-lookup"><span data-stu-id="f5c24-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="f5c24-213">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f5c24-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5c24-214">Tai priklausys nuo ankstesnių pasirinktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="f5c24-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="f5c24-215">Pasirinkite, are reikia blokuoti šiuos procesus, o atidarytus kokybės užsakymus susieti su šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="f5c24-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="f5c24-216">Išplėskite arba sutraukite sekciją Specifikacijos.</span><span class="sxs-lookup"><span data-stu-id="f5c24-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="f5c24-217">Lauke Bandymų grupė pasirinkite bandymų grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="f5c24-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="f5c24-218">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f5c24-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f5c24-219">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f5c24-219">Click Save.</span></span>
17. <span data-ttu-id="f5c24-220">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5c24-220">Close the page.</span></span>

