---
title: Įgalinti numerio lentelės žymės spausdinimą
description: Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed74806e5e037570f3ed7f59725eed494c829d34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847277"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="2ca28-103">Įgalinti numerio lentelės žymės spausdinimą</span><span class="sxs-lookup"><span data-stu-id="2ca28-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ca28-104">Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="2ca28-105">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="2ca28-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="2ca28-106">Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="2ca28-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="2ca28-107">Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="2ca28-108">Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="2ca28-109">Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="2ca28-110">Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.</span><span class="sxs-lookup"><span data-stu-id="2ca28-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="2ca28-111">Nustatyti GS1 įmonės prefiksą</span><span class="sxs-lookup"><span data-stu-id="2ca28-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="2ca28-112">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="2ca28-113">Lauke GS1 įmonės prefiksas įveskite savo GS1 įmonės numerio 7 skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="2ca28-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="2ca28-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-114">Click Save.</span></span>
4. <span data-ttu-id="2ca28-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="2ca28-116">Nustatyti SSCC numerio lentelės numeraciją</span><span class="sxs-lookup"><span data-stu-id="2ca28-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="2ca28-117">Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="2ca28-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="2ca28-118">Lauke Sritis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="2ca28-119">Lauke Nuoroda pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="2ca28-120">Lauke Įmonė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="2ca28-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2ca28-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2ca28-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2ca28-123">Išplėskite skyrių Segmentai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="2ca28-124">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-124">Click Edit.</span></span>
9. <span data-ttu-id="2ca28-125">Lentelėje Segmentai pasirinkite pirmąją eilutę</span><span class="sxs-lookup"><span data-stu-id="2ca28-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="2ca28-126">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-126">Click Remove.</span></span>
11. <span data-ttu-id="2ca28-127">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-127">Click Remove.</span></span>
12. <span data-ttu-id="2ca28-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-128">Click Save.</span></span>
13. <span data-ttu-id="2ca28-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="2ca28-130">Kurti dokumento maršruto maketą</span><span class="sxs-lookup"><span data-stu-id="2ca28-130">Create the document route layout</span></span>
1. <span data-ttu-id="2ca28-131">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="2ca28-132">Įgalinti SSCC maketą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="2ca28-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-133">Click New.</span></span>
3. <span data-ttu-id="2ca28-134">Lauke Maketo ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="2ca28-135">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2ca28-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2ca28-137">Spustelėkite Įterpti teksto pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="2ca28-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="2ca28-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-138">Click Save.</span></span>
8. <span data-ttu-id="2ca28-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="2ca28-140">Nustatyti dokumentų maršruto planavimą</span><span class="sxs-lookup"><span data-stu-id="2ca28-140">Set up the document routing</span></span>
1. <span data-ttu-id="2ca28-141">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="2ca28-142">Lauke Darbo užsakymo tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="2ca28-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-143">Click New.</span></span>
4. <span data-ttu-id="2ca28-144">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="2ca28-145">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2ca28-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-146">Click New.</span></span>
7. <span data-ttu-id="2ca28-147">Lauke Maketo ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="2ca28-148">Lauke Pavadinimas įveskite spausdintuvo, kurį norite naudoti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="2ca28-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-149">Click Save.</span></span>
10. <span data-ttu-id="2ca28-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="2ca28-151">Kurti mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="2ca28-151">Create mobile device menu</span></span>
1. <span data-ttu-id="2ca28-152">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2ca28-153">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-153">Click New.</span></span>
3. <span data-ttu-id="2ca28-154">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="2ca28-155">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="2ca28-156">Lauke Režimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="2ca28-157">Lauke Naudoti esamą darbą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2ca28-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="2ca28-158">Lauke Generuoti numerio lentelę pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2ca28-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="2ca28-159">Išplėskite skyrių Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="2ca28-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="2ca28-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-160">Click New.</span></span>
10. <span data-ttu-id="2ca28-161">Lauke Darbo klasės ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="2ca28-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-162">Click Save.</span></span>
12. <span data-ttu-id="2ca28-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-163">Close the page.</span></span>
13. <span data-ttu-id="2ca28-164">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="2ca28-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="2ca28-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2ca28-166">Medyje pasirinkite „Medyje pasirinkite meniu elementą, kurį sukūrėte anksčiau.‟.</span><span class="sxs-lookup"><span data-stu-id="2ca28-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="2ca28-167">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-167">Click Edit.</span></span>
17. <span data-ttu-id="2ca28-168">Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="2ca28-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-169">Click Save.</span></span>
19. <span data-ttu-id="2ca28-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="2ca28-171">Naujinti darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="2ca28-171">Update a work template</span></span>
1. <span data-ttu-id="2ca28-172">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="2ca28-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="2ca28-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2ca28-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2ca28-174">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-174">Click Edit.</span></span>
4. <span data-ttu-id="2ca28-175">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2ca28-175">Click New.</span></span>
5. <span data-ttu-id="2ca28-176">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2ca28-177">Lauke Darbo tipas pasirinkite „Spausdinti‟.</span><span class="sxs-lookup"><span data-stu-id="2ca28-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="2ca28-178">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ca28-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="2ca28-179">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2ca28-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2ca28-180">Spustelėkite Perkelti aukštyn.</span><span class="sxs-lookup"><span data-stu-id="2ca28-180">Click Move up.</span></span>
10. <span data-ttu-id="2ca28-181">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2ca28-181">Click Save.</span></span>
11. <span data-ttu-id="2ca28-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ca28-182">Close the page.</span></span>

