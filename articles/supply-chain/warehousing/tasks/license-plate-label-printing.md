--- 
title: "Įgalinti numerio lentelės žymės spausdinimą"
description: "Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 75b47e8e4a5643a6e582214c59cd32d74321a4da
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="bd1e1-103">Įgalinti numerio lentelės žymės spausdinimą</span><span class="sxs-lookup"><span data-stu-id="bd1e1-103">Enable license plate label printing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd1e1-104">Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="bd1e1-105">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="bd1e1-106">Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="bd1e1-107">Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="bd1e1-108">Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="bd1e1-109">Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="bd1e1-110">Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="bd1e1-111">Nustatyti GS1 įmonės prefiksą</span><span class="sxs-lookup"><span data-stu-id="bd1e1-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="bd1e1-112">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="bd1e1-113">Lauke GS1 įmonės prefiksas įveskite savo GS1 įmonės numerio 7 skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="bd1e1-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-114">Click Save.</span></span>
4. <span data-ttu-id="bd1e1-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="bd1e1-116">Nustatyti SSCC numerio lentelės numeraciją</span><span class="sxs-lookup"><span data-stu-id="bd1e1-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="bd1e1-117">Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="bd1e1-118">Lauke Sritis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="bd1e1-119">Lauke Nuoroda pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="bd1e1-120">Lauke Įmonė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="bd1e1-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bd1e1-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bd1e1-123">Išplėskite skyrių Segmentai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="bd1e1-124">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-124">Click Edit.</span></span>
9. <span data-ttu-id="bd1e1-125">Lentelėje Segmentai pasirinkite pirmąją eilutę</span><span class="sxs-lookup"><span data-stu-id="bd1e1-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="bd1e1-126">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-126">Click Remove.</span></span>
11. <span data-ttu-id="bd1e1-127">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-127">Click Remove.</span></span>
12. <span data-ttu-id="bd1e1-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-128">Click Save.</span></span>
13. <span data-ttu-id="bd1e1-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="bd1e1-130">Kurti dokumento maršruto maketą</span><span class="sxs-lookup"><span data-stu-id="bd1e1-130">Create the document route layout</span></span>
1. <span data-ttu-id="bd1e1-131">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="bd1e1-132">Įgalinti SSCC maketą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="bd1e1-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-133">Click New.</span></span>
3. <span data-ttu-id="bd1e1-134">Lauke Maketo ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="bd1e1-135">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bd1e1-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="bd1e1-137">Spustelėkite Įterpti teksto pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="bd1e1-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-138">Click Save.</span></span>
8. <span data-ttu-id="bd1e1-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="bd1e1-140">Nustatyti dokumentų maršruto planavimą</span><span class="sxs-lookup"><span data-stu-id="bd1e1-140">Set up the document routing</span></span>
1. <span data-ttu-id="bd1e1-141">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="bd1e1-142">Lauke Darbo užsakymo tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="bd1e1-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-143">Click New.</span></span>
4. <span data-ttu-id="bd1e1-144">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="bd1e1-145">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="bd1e1-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-146">Click New.</span></span>
7. <span data-ttu-id="bd1e1-147">Lauke Maketo ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="bd1e1-148">Lauke Pavadinimas įveskite spausdintuvo, kurį norite naudoti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="bd1e1-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-149">Click Save.</span></span>
10. <span data-ttu-id="bd1e1-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="bd1e1-151">Kurti mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="bd1e1-151">Create mobile device menu</span></span>
1. <span data-ttu-id="bd1e1-152">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="bd1e1-153">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-153">Click New.</span></span>
3. <span data-ttu-id="bd1e1-154">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="bd1e1-155">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="bd1e1-156">Lauke Režimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="bd1e1-157">Lauke Naudoti esamą darbą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="bd1e1-158">Lauke Generuoti numerio lentelę pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="bd1e1-159">Išplėskite skyrių Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="bd1e1-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-160">Click New.</span></span>
10. <span data-ttu-id="bd1e1-161">Lauke Darbo klasės ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="bd1e1-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-162">Click Save.</span></span>
12. <span data-ttu-id="bd1e1-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-163">Close the page.</span></span>
13. <span data-ttu-id="bd1e1-164">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="bd1e1-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="bd1e1-166">Medyje pasirinkite „Medyje pasirinkite meniu elementą, kurį sukūrėte anksčiau.‟.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="bd1e1-167">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-167">Click Edit.</span></span>
17. <span data-ttu-id="bd1e1-168">Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="bd1e1-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-169">Click Save.</span></span>
19. <span data-ttu-id="bd1e1-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="bd1e1-171">Naujinti darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="bd1e1-171">Update a work template</span></span>
1. <span data-ttu-id="bd1e1-172">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="bd1e1-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bd1e1-174">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-174">Click Edit.</span></span>
4. <span data-ttu-id="bd1e1-175">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-175">Click New.</span></span>
5. <span data-ttu-id="bd1e1-176">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bd1e1-177">Lauke Darbo tipas pasirinkite „Spausdinti‟.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="bd1e1-178">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="bd1e1-179">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bd1e1-180">Spustelėkite Perkelti aukštyn.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-180">Click Move up.</span></span>
10. <span data-ttu-id="bd1e1-181">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-181">Click Save.</span></span>
11. <span data-ttu-id="bd1e1-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd1e1-182">Close the page.</span></span>


