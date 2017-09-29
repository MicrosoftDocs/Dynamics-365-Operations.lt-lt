---
title: "Nustatyti kokybės užsakymus"
description: "Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="3aee5-103">Nustatyti kokybės užsakymus</span><span class="sxs-lookup"><span data-stu-id="3aee5-103">Set up quality orders</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aee5-104">Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.</span><span class="sxs-lookup"><span data-stu-id="3aee5-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="3aee5-105">Procedūrą paprastai atlieka kokybės vadovas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="3aee5-106">Šis procesas apima kokybės grupės kūrimą apibrėžti prekėms, iš kurių bus imami pavyzdžiai, ir bandymo grupės kūrimą grupuoti bandymams, kuriuos reikia atlikti su prekėmis kokybės grupėje.</span><span class="sxs-lookup"><span data-stu-id="3aee5-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="3aee5-107">Šį vedlį galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="3aee5-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="3aee5-108">Kokybės valdymo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="3aee5-108">Enable quality management</span></span>
1. <span data-ttu-id="3aee5-109">Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="3aee5-110">Spustelėkite skirtuką Kokybės valdymas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="3aee5-111">Nustatykite parinkčiai Naudoti kokybės valdymą reikšmę Taip.</span><span class="sxs-lookup"><span data-stu-id="3aee5-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="3aee5-112">Spustelėkite Ataskaitų sąranka.</span><span class="sxs-lookup"><span data-stu-id="3aee5-112">Click Report setup.</span></span>
    * <span data-ttu-id="3aee5-113">USMF kokybės valdymo ataskaitos sąranka jau yra nurodyta.</span><span class="sxs-lookup"><span data-stu-id="3aee5-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="3aee5-114">Jei tai buvo atlikta, čia galite įtraukti naujas skirtingų ataskaitų tipų eilutes ir pasirinkti kiekvienos ataskaitos dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="3aee5-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-115">Close the page.</span></span>
6. <span data-ttu-id="3aee5-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="3aee5-117">Kurti bandymą</span><span class="sxs-lookup"><span data-stu-id="3aee5-117">Create a test</span></span>
1. <span data-ttu-id="3aee5-118">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="3aee5-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-119">Click New.</span></span>
3. <span data-ttu-id="3aee5-120">Lauke Bandymas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="3aee5-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3aee5-122">Lauke Tipas pasirinkite „Parinktis‟.</span><span class="sxs-lookup"><span data-stu-id="3aee5-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="3aee5-123">Šiame pavyzdyje pasirinksime „Parinktis‟ – bus galima priskirti tikrinimo rezultatus pagal iš anksto apibrėžtas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="3aee5-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="3aee5-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-124">Click Save.</span></span>
7. <span data-ttu-id="3aee5-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="3aee5-126">Kurti bandymų kintamuosius, kad būtų galima apibrėžti, kaip įrašomi bandymų rezultatai</span><span class="sxs-lookup"><span data-stu-id="3aee5-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="3aee5-127">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymo kintamieji.</span><span class="sxs-lookup"><span data-stu-id="3aee5-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="3aee5-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-128">Click New.</span></span>
3. <span data-ttu-id="3aee5-129">Lauke Kintamasis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="3aee5-130">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3aee5-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-131">Click Save.</span></span>
6. <span data-ttu-id="3aee5-132">Spustelėkite Rezultatai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-132">Click Outcomes.</span></span>
7. <span data-ttu-id="3aee5-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-133">Click New.</span></span>
8. <span data-ttu-id="3aee5-134">Lauke Rezultatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="3aee5-135">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="3aee5-136">Lauke Rezultato būsena pasirinkite „Sėkmingai‟.</span><span class="sxs-lookup"><span data-stu-id="3aee5-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="3aee5-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-137">Click Save.</span></span>
12. <span data-ttu-id="3aee5-138">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-138">Click New.</span></span>
13. <span data-ttu-id="3aee5-139">Lauke Rezultatas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="3aee5-140">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="3aee5-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-141">Click Save.</span></span>
16. <span data-ttu-id="3aee5-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-142">Close the page.</span></span>
17. <span data-ttu-id="3aee5-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="3aee5-144">Nustatyti prekių pavyzdžių ėmimą</span><span class="sxs-lookup"><span data-stu-id="3aee5-144">Set up item sampling</span></span>
1. <span data-ttu-id="3aee5-145">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Prekių pavyzdžių ėmimas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="3aee5-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-146">Click New.</span></span>
3. <span data-ttu-id="3aee5-147">Lauke Prekių pavyzdžių ėmimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="3aee5-148">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3aee5-149">Lauke Vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3aee5-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="3aee5-150">Ši reikšmė susijusi su kiekio specifikacija, pasirinkta gretimame lauke.</span><span class="sxs-lookup"><span data-stu-id="3aee5-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="3aee5-151">Išplėskite arba sutraukite sekciją Procesas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="3aee5-152">Pažymėkite arba panaikinkite žymės langelio Visiškas blokavimas žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="3aee5-153">Jei pasirenkate šią parinktį ir jei tikrinti nepavyksta, užblokuojama visa partija ar užsakymo eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="3aee5-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="3aee5-154">Jei jos nepasirenkate, blokuojamos tik kokybės užsakymo prekės.</span><span class="sxs-lookup"><span data-stu-id="3aee5-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="3aee5-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-155">Click Save.</span></span>
9. <span data-ttu-id="3aee5-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="3aee5-157">Kurti kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="3aee5-157">Create a quality group</span></span>
1. <span data-ttu-id="3aee5-158">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės grupės.</span><span class="sxs-lookup"><span data-stu-id="3aee5-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="3aee5-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-159">Click New.</span></span>
3. <span data-ttu-id="3aee5-160">Lauke Kokybės grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="3aee5-161">Naudokite aprašomąjį pavadinimą, kad būtų lengviau identifikuoti, kokios rūšies prekės bus grupėje (pavyzdžių ėmimo kriterijai).</span><span class="sxs-lookup"><span data-stu-id="3aee5-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="3aee5-162">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3aee5-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-163">Click Save.</span></span>
6. <span data-ttu-id="3aee5-164">Spustelėkite Įtraukti prekes.</span><span class="sxs-lookup"><span data-stu-id="3aee5-164">Click Add items.</span></span>
7. <span data-ttu-id="3aee5-165">Pasirinkti eilutę Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="3aee5-165">Select the Item number row</span></span>
    * <span data-ttu-id="3aee5-166">Šiame pavyzdyje filtravimas bus vykdomas pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="3aee5-167">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3aee5-168">Pavyzdžiui, įveskite T*, kad filtruotumėte tuos prekių numerius, kurie prasideda T.</span><span class="sxs-lookup"><span data-stu-id="3aee5-168">For example, type T* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="3aee5-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3aee5-169">Click OK.</span></span>
10. <span data-ttu-id="3aee5-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3aee5-170">Click OK.</span></span>
11. <span data-ttu-id="3aee5-171">Spustelėkite Prekių kokybės grupės.</span><span class="sxs-lookup"><span data-stu-id="3aee5-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="3aee5-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-172">Close the page.</span></span>
13. <span data-ttu-id="3aee5-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="3aee5-174">Kurti bandymų grupę</span><span class="sxs-lookup"><span data-stu-id="3aee5-174">Create a test group</span></span>
1. <span data-ttu-id="3aee5-175">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymų grupės.</span><span class="sxs-lookup"><span data-stu-id="3aee5-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="3aee5-176">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-176">Click New.</span></span>
3. <span data-ttu-id="3aee5-177">Lauke Bandymų grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="3aee5-178">Suteikite bandymų grupei pavadinimą, kuris padės prisiminti, kokie bandymai vykdomi ir su kuria kokybės grupe ji turėtų būti susieta.</span><span class="sxs-lookup"><span data-stu-id="3aee5-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="3aee5-179">Pavyzdžiui, jei ji bus naudojama su kokybės grupe, kuri pasirenka prekes, prasidedančias „T‟, galite ją pavadinti „T prekių bandymai‟.</span><span class="sxs-lookup"><span data-stu-id="3aee5-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="3aee5-180">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3aee5-181">Lauke Prekių pavyzdžių ėmimas pasirinkite prekių pavyzdžių ėmimo eilutę, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="3aee5-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="3aee5-182">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3aee5-183">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-183">Click Add.</span></span>
8. <span data-ttu-id="3aee5-184">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3aee5-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="3aee5-185">Lauke Bandymas pasirinkite bandymą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="3aee5-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="3aee5-186">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="3aee5-187">Spustelėkite skirtuką Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-187">Click the Test tab.</span></span>
12. <span data-ttu-id="3aee5-188">Lauke Kintamasis pasirinkite bandymo kintamąjį, kurį sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="3aee5-189">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="3aee5-190">Lauke Numatytasis rezultatas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3aee5-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3aee5-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3aee5-192">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-192">Click Save.</span></span>
17. <span data-ttu-id="3aee5-193">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="3aee5-194">Apibrėžti, kada bus kuriami kokybės užsakymai</span><span class="sxs-lookup"><span data-stu-id="3aee5-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="3aee5-195">Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės susiejimai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="3aee5-196">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-196">Click New.</span></span>
3. <span data-ttu-id="3aee5-197">Lauke Nuorodos tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="3aee5-198">Lauke Prekės kodas pasirinkite „Grupė‟.</span><span class="sxs-lookup"><span data-stu-id="3aee5-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="3aee5-199">Šiame pavyzdyje pasirinksime „Grupė‟ ir naudosime anksčiau savo sukurtą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="3aee5-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="3aee5-200">Taip pat galite nustatyti „Lentelė‟, kad prekes nurodytumėte rankiniu būdu, arba pasirinkti „Visi‟, kad visos prekės būtų pridėtos į kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="3aee5-201">Lauke Prekė pasirinkite kokybės grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="3aee5-202">Galimos parinktys lauke Prekė priklauso nuo to, ką nustatote lauke Prekės kodas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="3aee5-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3aee5-204">Išplėskite arba sutraukite sekciją Procesas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="3aee5-205">Lauke Įvykio tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="3aee5-206">Tai yra įvykis, kuris suaktyvina bandymą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-206">This is the event that triggers the test.</span></span> <span data-ttu-id="3aee5-207">Čia galimos parinktys priklauso nuo to, kokį procesą pasirinkote lauke Nuorodos tipas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="3aee5-208">Lauke Vykdymas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="3aee5-209">Išplėskite arba sutraukite sekciją Kokybės užsakymo procesas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="3aee5-210">Lauke Įvykių blokavimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3aee5-211">Šiame lauke rodomas procesų, kuriuos galima blokuoti, jei kokybės užsakymas vis dar atidarytas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="3aee5-212">Parinktys priklauso nuo to, ką pasirinkote lauke Įvykio tipas.</span><span class="sxs-lookup"><span data-stu-id="3aee5-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="3aee5-213">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3aee5-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3aee5-214">Tai priklausys nuo ankstesnių pasirinktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="3aee5-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="3aee5-215">Pasirinkite, are reikia blokuoti šiuos procesus, o atidarytus kokybės užsakymus susieti su šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="3aee5-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="3aee5-216">Išplėskite arba sutraukite sekciją Specifikacijos.</span><span class="sxs-lookup"><span data-stu-id="3aee5-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="3aee5-217">Lauke Bandymų grupė pasirinkite bandymų grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="3aee5-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="3aee5-218">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3aee5-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="3aee5-219">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3aee5-219">Click Save.</span></span>
17. <span data-ttu-id="3aee5-220">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3aee5-220">Close the page.</span></span>
