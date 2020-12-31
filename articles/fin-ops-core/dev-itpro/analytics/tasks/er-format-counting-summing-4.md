---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (4 dalis – Formato paleidimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f37fc3c611e9c5328f4d99be8c7c63ab59b2f08
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684648"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="17806-103">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (4 dalis – Formato paleidimas)</span><span class="sxs-lookup"><span data-stu-id="17806-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17806-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="17806-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="17806-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="17806-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="17806-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (3 dalis: konfigūracijų naudojimas, norit kurti išvestį)“.</span><span class="sxs-lookup"><span data-stu-id="17806-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="17806-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="17806-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="17806-108">Patikrinkite šią „Intrastat“ ataskaitų generavimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="17806-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="17806-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="17806-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="17806-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="17806-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="17806-111">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="17806-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="17806-112">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="17806-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="17806-113">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="17806-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="17806-114">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="17806-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="17806-115">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="17806-115">Click User parameters.</span></span>
8. <span data-ttu-id="17806-116">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="17806-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="17806-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17806-117">Click OK.</span></span>
10. <span data-ttu-id="17806-118">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="17806-118">Click Edit.</span></span>
11. <span data-ttu-id="17806-119">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="17806-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="17806-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="17806-120">Click Save.</span></span>
13. <span data-ttu-id="17806-121">Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="17806-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="17806-122">Išplėskite skyrių Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="17806-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="17806-123">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="17806-123">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="17806-124">Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.</span><span class="sxs-lookup"><span data-stu-id="17806-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="17806-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="17806-125">Click Save.</span></span>
18. <span data-ttu-id="17806-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17806-126">Close the page.</span></span>
19. <span data-ttu-id="17806-127">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="17806-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="17806-128">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="17806-128">Click Output.</span></span>
21. <span data-ttu-id="17806-129">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="17806-129">Click Report.</span></span>
    * <span data-ttu-id="17806-130">Paleiskite „Intrastat“ ataskaitos generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="17806-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="17806-131">Lauke Pradžios data nustatykite datą „2000-01-01“.</span><span class="sxs-lookup"><span data-stu-id="17806-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="17806-132">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="17806-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="17806-133">Lauke Pabaigos data nustatykite datą „2022-12-31“.</span><span class="sxs-lookup"><span data-stu-id="17806-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="17806-134">Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="17806-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="17806-135">Lauke Kryptis pasirinkite Gavimai.</span><span class="sxs-lookup"><span data-stu-id="17806-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="17806-136">Lauke Generuoti failą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="17806-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="17806-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17806-137">Click OK.</span></span>
    * <span data-ttu-id="17806-138">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="17806-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="17806-139">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="17806-139">Click New.</span></span>
28. <span data-ttu-id="17806-140">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="17806-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="17806-141">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="17806-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="17806-142">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17806-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="17806-143">Lauke Prekė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17806-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="17806-144">Lauke Svoris nustatykite reikšmę 10.</span><span class="sxs-lookup"><span data-stu-id="17806-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="17806-145">Lauke SF suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="17806-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="17806-146">Lauke Statistinė suma nustatykite reikšmę 10000.</span><span class="sxs-lookup"><span data-stu-id="17806-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="17806-147">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="17806-147">Click Output.</span></span>
36. <span data-ttu-id="17806-148">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="17806-148">Click Report.</span></span>
37. <span data-ttu-id="17806-149">Lauke Kryptis pasirinkite Išsiuntimai.</span><span class="sxs-lookup"><span data-stu-id="17806-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="17806-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17806-150">Click OK.</span></span>
    * <span data-ttu-id="17806-151">Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.</span><span class="sxs-lookup"><span data-stu-id="17806-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="17806-152">Atkreipkite dėmesį, kad ji buvo pakeista, lyginant su pirmuoju paleidimu.</span><span class="sxs-lookup"><span data-stu-id="17806-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="17806-153">Paleiskite šią konfigūraciją derinimo režimu, norėdami peržiūrėti surinktus skaičiavimo ir sumavimo duomenis</span><span class="sxs-lookup"><span data-stu-id="17806-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="17806-154">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="17806-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="17806-155">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="17806-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="17806-156">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="17806-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="17806-157">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="17806-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="17806-158">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="17806-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="17806-159">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="17806-159">Click User parameters.</span></span>
7. <span data-ttu-id="17806-160">Lauke Vykdyti derinimo režimu pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="17806-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="17806-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17806-161">Click OK.</span></span>
9. <span data-ttu-id="17806-162">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17806-162">Close the page.</span></span>
10. <span data-ttu-id="17806-163">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="17806-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="17806-164">Spustelėkite Išvestis.</span><span class="sxs-lookup"><span data-stu-id="17806-164">Click Output.</span></span>
12. <span data-ttu-id="17806-165">Spustelėkite Ataskaita.</span><span class="sxs-lookup"><span data-stu-id="17806-165">Click Report.</span></span>
13. <span data-ttu-id="17806-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17806-166">Click OK.</span></span>
14. <span data-ttu-id="17806-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17806-167">Close the page.</span></span>
15. <span data-ttu-id="17806-168">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="17806-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="17806-169">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="17806-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="17806-170">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="17806-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="17806-171">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="17806-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="17806-172">Spustelėkite Derinimo žurnalai.</span><span class="sxs-lookup"><span data-stu-id="17806-172">Click Debug logs.</span></span>
    * <span data-ttu-id="17806-173">Atkreipkite dėmesį, kad sukurtas pasirinktos konfigūracijos vykdymo proceso derinimo žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="17806-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="17806-174">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="17806-174">Click Attach.</span></span>
21. <span data-ttu-id="17806-175">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="17806-175">Click Open.</span></span>
    * <span data-ttu-id="17806-176">Peržiūrėkite sukurtą XML failą, kuriame yra skaičiavimo ir sumavimo informacija, surinkta vykdant pasirinktą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="17806-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

