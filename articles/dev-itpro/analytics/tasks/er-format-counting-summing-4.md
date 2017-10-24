--- 
title: "Formato paleidimas skaičiavimo ir sumavimo veiksmams elektroninėse ataskaitose (ER) atlikti"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="f1c0c-103">Formato paleidimas skaičiavimo ir sumavimo veiksmams elektroninėse ataskaitose (ER) atlikti</span><span class="sxs-lookup"><span data-stu-id="f1c0c-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1c0c-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f1c0c-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f1c0c-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (3 dalis: konfigūracijų naudojimas, norit kurti išvestį)“.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="f1c0c-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="f1c0c-108">Patikrinkite šią „Intrastat“ ataskaitų generavimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="f1c0c-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="f1c0c-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f1c0c-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f1c0c-111">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="f1c0c-112">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="f1c0c-113">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="f1c0c-114">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="f1c0c-115">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-115">Click User parameters.</span></span>
8. <span data-ttu-id="f1c0c-116">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="f1c0c-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-117">Click OK.</span></span>
10. <span data-ttu-id="f1c0c-118">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-118">Click Edit.</span></span>
11. <span data-ttu-id="f1c0c-119">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="f1c0c-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-120">Click Save.</span></span>
13. <span data-ttu-id="f1c0c-121">Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="f1c0c-122">Išplėskite skyrių Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="f1c0c-123">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="f1c0c-124">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="f1c0c-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-125">Click Save.</span></span>
18. <span data-ttu-id="f1c0c-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-126">Close the page.</span></span>
19. <span data-ttu-id="f1c0c-127">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="f1c0c-128">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-128">Click Output.</span></span>
21. <span data-ttu-id="f1c0c-129">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-129">Click Report.</span></span>
    * <span data-ttu-id="f1c0c-130">Paleiskite „Intrastat“ ataskaitos generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="f1c0c-131">Lauke Pradžios data nustatykite datą „2000-01-01“.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="f1c0c-132">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="f1c0c-133">Lauke Pabaigos data nustatykite datą „2022-12-31“.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="f1c0c-134">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="f1c0c-135">Lauke Kryptis pasirinkite Gavimai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="f1c0c-136">Lauke Generuoti failą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="f1c0c-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-137">Click OK.</span></span>
    * <span data-ttu-id="f1c0c-138">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="f1c0c-139">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-139">Click New.</span></span>
28. <span data-ttu-id="f1c0c-140">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="f1c0c-141">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="f1c0c-142">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="f1c0c-143">Lauke Prekė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="f1c0c-144">Lauke Svoris nustatykite reikšmę 10.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="f1c0c-145">Lauke SF suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="f1c0c-146">Lauke Statistinė suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="f1c0c-147">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-147">Click Output.</span></span>
36. <span data-ttu-id="f1c0c-148">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-148">Click Report.</span></span>
37. <span data-ttu-id="f1c0c-149">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="f1c0c-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-150">Click OK.</span></span>
    * <span data-ttu-id="f1c0c-151">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="f1c0c-152">Atkreipkite dėmesį, kad ji buvo pakeista, lyginant su pirmuoju paleidimu.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="f1c0c-153">Paleiskite šią konfigūraciją derinimo režimu, norėdami peržiūrėti surinktus skaičiavimo ir sumavimo duomenis</span><span class="sxs-lookup"><span data-stu-id="f1c0c-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="f1c0c-154">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f1c0c-155">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="f1c0c-156">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="f1c0c-157">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="f1c0c-158">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="f1c0c-159">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-159">Click User parameters.</span></span>
7. <span data-ttu-id="f1c0c-160">Lauke Vykdyti derinimo režimu pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="f1c0c-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-161">Click OK.</span></span>
9. <span data-ttu-id="f1c0c-162">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-162">Close the page.</span></span>
10. <span data-ttu-id="f1c0c-163">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="f1c0c-164">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-164">Click Output.</span></span>
12. <span data-ttu-id="f1c0c-165">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-165">Click Report.</span></span>
13. <span data-ttu-id="f1c0c-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-166">Click OK.</span></span>
14. <span data-ttu-id="f1c0c-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-167">Close the page.</span></span>
15. <span data-ttu-id="f1c0c-168">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="f1c0c-169">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="f1c0c-170">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f1c0c-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="f1c0c-171">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="f1c0c-172">Spustelėkite Derinimo žurnalai.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-172">Click Debug logs.</span></span>
    * <span data-ttu-id="f1c0c-173">Atkreipkite dėmesį, kad sukurtas pasirinktos konfigūracijos vykdymo proceso derinimo žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="f1c0c-174">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-174">Click Attach.</span></span>
21. <span data-ttu-id="f1c0c-175">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-175">Click Open.</span></span>
    * <span data-ttu-id="f1c0c-176">Peržiūrėkite sukurtą XML failą, kuriame yra skaičiavimo ir sumavimo informacija, surinkta vykdant pasirinktą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="f1c0c-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


