---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (4 dalis – Formato paleidimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (4 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5792505de78aad458bd8745630915cf58f05f73f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748978"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="ee7ac-104">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (4 dalis – Formato paleidimas)</span><span class="sxs-lookup"><span data-stu-id="ee7ac-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee7ac-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ee7ac-106">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ee7ac-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (3 dalis: konfigūracijų naudojimas, norit kurti išvestį)“.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="ee7ac-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="ee7ac-109">Patikrinkite šią „Intrastat“ ataskaitų generavimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="ee7ac-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="ee7ac-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ee7ac-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ee7ac-112">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ee7ac-113">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ee7ac-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ee7ac-114">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ee7ac-115">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="ee7ac-116">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-116">Click User parameters.</span></span>
8. <span data-ttu-id="ee7ac-117">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="ee7ac-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-118">Click OK.</span></span>
10. <span data-ttu-id="ee7ac-119">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-119">Click Edit.</span></span>
11. <span data-ttu-id="ee7ac-120">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="ee7ac-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-121">Click Save.</span></span>
13. <span data-ttu-id="ee7ac-122">Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="ee7ac-123">Išplėskite skyrių Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="ee7ac-124">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="ee7ac-125">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="ee7ac-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-126">Click Save.</span></span>
18. <span data-ttu-id="ee7ac-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-127">Close the page.</span></span>
19. <span data-ttu-id="ee7ac-128">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="ee7ac-129">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-129">Click Output.</span></span>
21. <span data-ttu-id="ee7ac-130">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-130">Click Report.</span></span>
    * <span data-ttu-id="ee7ac-131">Paleiskite „Intrastat“ ataskaitos generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="ee7ac-132">Lauke Pradžios data nustatykite datą „2000-01-01“.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="ee7ac-133">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="ee7ac-134">Lauke Pabaigos data nustatykite datą „2022-12-31“.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="ee7ac-135">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="ee7ac-136">Lauke Kryptis pasirinkite Gavimai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="ee7ac-137">Lauke Generuoti failą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="ee7ac-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-138">Click OK.</span></span>
    * <span data-ttu-id="ee7ac-139">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="ee7ac-140">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-140">Click New.</span></span>
28. <span data-ttu-id="ee7ac-141">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="ee7ac-142">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="ee7ac-143">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="ee7ac-144">Lauke Prekė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="ee7ac-145">Lauke Svoris nustatykite reikšmę 10.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="ee7ac-146">Lauke SF suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="ee7ac-147">Lauke Statistinė suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="ee7ac-148">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-148">Click Output.</span></span>
36. <span data-ttu-id="ee7ac-149">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-149">Click Report.</span></span>
37. <span data-ttu-id="ee7ac-150">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="ee7ac-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-151">Click OK.</span></span>
    * <span data-ttu-id="ee7ac-152">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="ee7ac-153">Atkreipkite dėmesį, kad ji buvo pakeista, lyginant su pirmuoju paleidimu.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="ee7ac-154">Paleiskite šią konfigūraciją derinimo režimu, norėdami peržiūrėti surinktus skaičiavimo ir sumavimo duomenis</span><span class="sxs-lookup"><span data-stu-id="ee7ac-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="ee7ac-155">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ee7ac-156">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="ee7ac-157">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ee7ac-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="ee7ac-158">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="ee7ac-159">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="ee7ac-160">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-160">Click User parameters.</span></span>
7. <span data-ttu-id="ee7ac-161">Lauke Vykdyti derinimo režimu pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="ee7ac-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-162">Click OK.</span></span>
9. <span data-ttu-id="ee7ac-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-163">Close the page.</span></span>
10. <span data-ttu-id="ee7ac-164">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="ee7ac-165">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-165">Click Output.</span></span>
12. <span data-ttu-id="ee7ac-166">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-166">Click Report.</span></span>
13. <span data-ttu-id="ee7ac-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-167">Click OK.</span></span>
14. <span data-ttu-id="ee7ac-168">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-168">Close the page.</span></span>
15. <span data-ttu-id="ee7ac-169">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="ee7ac-170">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="ee7ac-171">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ee7ac-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="ee7ac-172">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="ee7ac-173">Spustelėkite Derinimo žurnalai.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-173">Click Debug logs.</span></span>
    * <span data-ttu-id="ee7ac-174">Atkreipkite dėmesį, kad sukurtas pasirinktos konfigūracijos vykdymo proceso derinimo žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="ee7ac-175">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-175">Click Attach.</span></span>
21. <span data-ttu-id="ee7ac-176">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-176">Click Open.</span></span>
    * <span data-ttu-id="ee7ac-177">Peržiūrėkite sukurtą XML failą, kuriame yra skaičiavimo ir sumavimo informacija, surinkta vykdant pasirinktą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="ee7ac-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]