---
title: Nustatyti kokybės užsakymus
description: Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0119ae07e490f048dbb021983e25889cb1cb42b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845359"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="1f0f1-103">Nustatyti kokybės užsakymus</span><span class="sxs-lookup"><span data-stu-id="1f0f1-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f0f1-104">Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="1f0f1-105">Procedūrą paprastai atlieka kokybės vadovas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="1f0f1-106">Šis procesas apima kokybės grupės kūrimą apibrėžti prekėms, iš kurių bus imami pavyzdžiai, ir bandymo grupės kūrimą grupuoti bandymams, kuriuos reikia atlikti su prekėmis kokybės grupėje.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="1f0f1-107">Šį vedlį galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="1f0f1-108">Kokybės valdymo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="1f0f1-108">Enable quality management</span></span>
1. <span data-ttu-id="1f0f1-109">Eikite į **Valdymo skiltį > Moduliai > Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="1f0f1-110">Spustelėkite skirtuką **Quality management** tab.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="1f0f1-111">Nustatykite **Use quality management option** reikšmę Taip.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="1f0f1-112">Spustelėkit **Report setup**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-112">Click **Report setup**.</span></span> <span data-ttu-id="1f0f1-113">USMF kokybės valdymo ataskaitos sąranka jau yra nurodyta.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="1f0f1-114">Jei tai buvo atlikta, čia galite įtraukti naujas skirtingų ataskaitų tipų eilutes ir pasirinkti kiekvienos ataskaitos dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="1f0f1-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-115">Close the page.</span></span>
6. <span data-ttu-id="1f0f1-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="1f0f1-117">Kurti bandymą</span><span class="sxs-lookup"><span data-stu-id="1f0f1-117">Create a test</span></span>
1. <span data-ttu-id="1f0f1-118">Pasirinkite **Inventory management > Setup > Quality control > Tests**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="1f0f1-119">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-119">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-120">Lauke **Test** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="1f0f1-121">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f0f1-122">Lauke **Type** pasirinkite „Parinktis‟.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="1f0f1-123">Šiame pavyzdyje pasirinksime „Parinktis‟ – bus galima priskirti tikrinimo rezultatus pagal iš anksto apibrėžtas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="1f0f1-124">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-124">Click **Save**.</span></span>
7. <span data-ttu-id="1f0f1-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="1f0f1-126">Kurti bandymų kintamuosius, kad būtų galima apibrėžti, kaip įrašomi bandymų rezultatai</span><span class="sxs-lookup"><span data-stu-id="1f0f1-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="1f0f1-127">Pasirinkit **Inventory management > Setup > Quality control > Test variables**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="1f0f1-128">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-128">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-129">Lauke **Variable** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="1f0f1-130">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f0f1-131">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-131">Click **Save**.</span></span>
6. <span data-ttu-id="1f0f1-132">Spustelėkite **Outcomes**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="1f0f1-133">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-133">Click **New**.</span></span>
8. <span data-ttu-id="1f0f1-134">Lauke **Outcome** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="1f0f1-135">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="1f0f1-136">Lauke **Outcome status** pasirinkite „Sėkmingai‟.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="1f0f1-137">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-137">Click **Save**.</span></span>
12. <span data-ttu-id="1f0f1-138">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-138">Click **New**.</span></span>
13. <span data-ttu-id="1f0f1-139">Lauke **Outcome** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="1f0f1-140">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="1f0f1-141">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-141">Click **Save**.</span></span>
16. <span data-ttu-id="1f0f1-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-142">Close the page.</span></span>
17. <span data-ttu-id="1f0f1-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="1f0f1-144">Nustatyti prekių pavyzdžių ėmimą</span><span class="sxs-lookup"><span data-stu-id="1f0f1-144">Set up item sampling</span></span>
1. <span data-ttu-id="1f0f1-145">Pasirinkit **Inventory management > Setup > Quality control > Item sampling**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="1f0f1-146">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-146">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-147">Lauke **Item sampling**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="1f0f1-148">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f0f1-149">Lauke **Value** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="1f0f1-150">Ši reikšmė susijusi su kiekio specifikacija, pasirinkta gretimame lauke.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="1f0f1-151">Išplėskite arba sutraukite sekciją **Process** section.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="1f0f1-152">Pažymėkite arba panaikinkite žymės langelio **Full blocking** žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="1f0f1-153">Jei pasirenkate šią parinktį ir jei tikrinti nepavyksta, užblokuojama visa partija ar užsakymo eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="1f0f1-154">Jei jos nepasirenkate, blokuojamos tik kokybės užsakymo prekės.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="1f0f1-155">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-155">Click **Save**.</span></span>
9. <span data-ttu-id="1f0f1-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="1f0f1-157">Kurti kokybės grupę</span><span class="sxs-lookup"><span data-stu-id="1f0f1-157">Create a quality group</span></span>
1. <span data-ttu-id="1f0f1-158">Pasirinkit **Inventory management > Setup > Quality control > Quality groups**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="1f0f1-159">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-159">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-160">Lauke **Quality group** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="1f0f1-161">Naudokite aprašomąjį pavadinimą, kad būtų lengviau identifikuoti, kokios rūšies prekės bus grupėje (pavyzdžių ėmimo kriterijai).</span><span class="sxs-lookup"><span data-stu-id="1f0f1-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="1f0f1-162">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f0f1-163">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-163">Click **Save**.</span></span>
6. <span data-ttu-id="1f0f1-164">Spustelėkite **Įtraukti prekes**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-164">Click **Add items**.</span></span>
7. <span data-ttu-id="1f0f1-165">Pasirinkti eilutę **Item number**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-165">Select the **Item number** row.</span></span> <span data-ttu-id="1f0f1-166">Šiame pavyzdyje filtravimas bus vykdomas pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="1f0f1-167">Lauke **Criteria**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="1f0f1-168">Pavyzdžiui, įveskite T\*, kad filtruotumėte tuos prekių numerius, kurie prasideda T.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="1f0f1-169">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-169">Click **OK**.</span></span>
10. <span data-ttu-id="1f0f1-170">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-170">Click **OK**.</span></span>
11. <span data-ttu-id="1f0f1-171">Spustelėkit **Item quality groups**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="1f0f1-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-172">Close the page.</span></span>
13. <span data-ttu-id="1f0f1-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="1f0f1-174">Kurti bandymų grupę</span><span class="sxs-lookup"><span data-stu-id="1f0f1-174">Create a test group</span></span>
1. <span data-ttu-id="1f0f1-175">Pasirinkite **Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymų grupės**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="1f0f1-176">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-176">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-177">Lauke **Test group** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="1f0f1-178">Suteikite **Test group** pavadinimą, kuris padės prisiminti, kokie bandymai vykdomi ir su kuria kokybės grupe ji turėtų būti susieta.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="1f0f1-179">Pavyzdžiui, jei ji bus naudojama su kokybės grupe, kuri pasirenka prekes, prasidedančias „T‟, galite ją pavadinti „T prekių bandymai‟.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="1f0f1-180">Lauke **Description field**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1f0f1-181">Lauke **Item sampling** pasirinkite prekių pavyzdžių ėmimo eilutę, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="1f0f1-182">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="1f0f1-183">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-183">Click **Add**.</span></span>
8. <span data-ttu-id="1f0f1-184">Lauke **Sequence number**įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="1f0f1-185">Lauke **Test** pasirinkite bandymą, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="1f0f1-186">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="1f0f1-187">Spustelėkite skirtuką **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="1f0f1-188">Lauke **Variable** pasirinkite bandymo kintamąjį, kurį sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="1f0f1-189">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="1f0f1-190">Lauke **Default outcome** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="1f0f1-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="1f0f1-192">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-192">Click **Save**.</span></span>
17. <span data-ttu-id="1f0f1-193">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="1f0f1-194">Apibrėžti, kada bus kuriami kokybės užsakymai</span><span class="sxs-lookup"><span data-stu-id="1f0f1-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="1f0f1-195">Pasirinkit **Inventory management > Setup > Quality control > Quality associations**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="1f0f1-196">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-196">Click **New**.</span></span>
3. <span data-ttu-id="1f0f1-197">Lauke **Reference type**pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="1f0f1-198">Lauke **Item code** pasirinkite „Grupė‟.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="1f0f1-199">Šiame pavyzdyje pasirinksime „Grupė‟ ir naudosime anksčiau savo sukurtą kokybės grupę.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="1f0f1-200">Taip pat galite nustatyti „Lentelė‟, kad prekes nurodytumėte rankiniu būdu, arba pasirinkti „Visi‟, kad visos prekės būtų pridėtos į kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="1f0f1-201">Lauke **Item** pasirinkite kokybės grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="1f0f1-202">Galimos parinktys lauke Prekė priklauso nuo to, ką nustatote lauke Prekės kodas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="1f0f1-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="1f0f1-204">Išplėskite arba sutraukite sekciją Procesas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="1f0f1-205">Lauke **Event type** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="1f0f1-206">Tai yra įvykis, kuris suaktyvina bandymą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-206">This is the event that triggers the test.</span></span> <span data-ttu-id="1f0f1-207">Čia galimos parinktys priklauso nuo to, kokį procesą pasirinkote lauke Nuorodos tipas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="1f0f1-208">Lauke **Execution**pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="1f0f1-209">Išplėskite arba sutraukite **Quality order process** sekcijąf</span><span class="sxs-lookup"><span data-stu-id="1f0f1-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="1f0f1-210">Lauke **Event blocking** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="1f0f1-211">Šiame lauke rodomas procesų, kuriuos galima blokuoti, jei kokybės užsakymas vis dar atidarytas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="1f0f1-212">Parinktys priklauso nuo to, ką pasirinkote lauke Įvykio tipas.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="1f0f1-213">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="1f0f1-214">Tai priklausys nuo ankstesnių pasirinktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="1f0f1-215">Pasirinkite, are reikia blokuoti šiuos procesus, o atidarytus kokybės užsakymus susieti su šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="1f0f1-216">Išplėskite arba sutraukite sekciją **Specifications**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="1f0f1-217">Lauke **Test group** pasirinkite bandymų grupę, kurią sukūrėte prieš tai.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="1f0f1-218">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="1f0f1-219">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-219">Click **Save**.</span></span>
17. <span data-ttu-id="1f0f1-220">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-220">Close the page.</span></span>

