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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "324036"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="910c9-103">Įgalinti numerio lentelės žymės spausdinimą</span><span class="sxs-lookup"><span data-stu-id="910c9-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="910c9-104">Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę.</span><span class="sxs-lookup"><span data-stu-id="910c9-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="910c9-105">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="910c9-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="910c9-106">Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="910c9-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="910c9-107">Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="910c9-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="910c9-108">Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="910c9-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="910c9-109">Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą.</span><span class="sxs-lookup"><span data-stu-id="910c9-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="910c9-110">Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.</span><span class="sxs-lookup"><span data-stu-id="910c9-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="910c9-111">Nustatyti GS1 įmonės prefiksą</span><span class="sxs-lookup"><span data-stu-id="910c9-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="910c9-112">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="910c9-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="910c9-113">Lauke GS1 įmonės prefiksas įveskite savo GS1 įmonės numerio 7 skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="910c9-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="910c9-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-114">Click Save.</span></span>
4. <span data-ttu-id="910c9-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="910c9-116">Nustatyti SSCC numerio lentelės numeraciją</span><span class="sxs-lookup"><span data-stu-id="910c9-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="910c9-117">Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="910c9-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="910c9-118">Lauke Sritis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="910c9-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="910c9-119">Lauke Nuoroda pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="910c9-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="910c9-120">Lauke Įmonė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="910c9-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="910c9-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="910c9-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="910c9-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="910c9-123">Išplėskite skyrių Segmentai.</span><span class="sxs-lookup"><span data-stu-id="910c9-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="910c9-124">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="910c9-124">Click Edit.</span></span>
9. <span data-ttu-id="910c9-125">Lentelėje Segmentai pasirinkite pirmąją eilutę</span><span class="sxs-lookup"><span data-stu-id="910c9-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="910c9-126">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="910c9-126">Click Remove.</span></span>
11. <span data-ttu-id="910c9-127">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="910c9-127">Click Remove.</span></span>
12. <span data-ttu-id="910c9-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-128">Click Save.</span></span>
13. <span data-ttu-id="910c9-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="910c9-130">Kurti dokumento maršruto maketą</span><span class="sxs-lookup"><span data-stu-id="910c9-130">Create the document route layout</span></span>
1. <span data-ttu-id="910c9-131">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai.</span><span class="sxs-lookup"><span data-stu-id="910c9-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="910c9-132">Įgalinti SSCC maketą.</span><span class="sxs-lookup"><span data-stu-id="910c9-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="910c9-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-133">Click New.</span></span>
3. <span data-ttu-id="910c9-134">Lauke Maketo ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="910c9-135">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="910c9-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="910c9-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="910c9-137">Spustelėkite Įterpti teksto pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="910c9-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="910c9-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-138">Click Save.</span></span>
8. <span data-ttu-id="910c9-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="910c9-140">Nustatyti dokumentų maršruto planavimą</span><span class="sxs-lookup"><span data-stu-id="910c9-140">Set up the document routing</span></span>
1. <span data-ttu-id="910c9-141">Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimas.</span><span class="sxs-lookup"><span data-stu-id="910c9-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="910c9-142">Lauke Darbo užsakymo tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="910c9-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="910c9-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-143">Click New.</span></span>
4. <span data-ttu-id="910c9-144">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="910c9-145">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="910c9-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-146">Click New.</span></span>
7. <span data-ttu-id="910c9-147">Lauke Maketo ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="910c9-148">Lauke Pavadinimas įveskite spausdintuvo, kurį norite naudoti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="910c9-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="910c9-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-149">Click Save.</span></span>
10. <span data-ttu-id="910c9-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="910c9-151">Kurti mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="910c9-151">Create mobile device menu</span></span>
1. <span data-ttu-id="910c9-152">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="910c9-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="910c9-153">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-153">Click New.</span></span>
3. <span data-ttu-id="910c9-154">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="910c9-155">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="910c9-156">Lauke Režimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="910c9-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="910c9-157">Lauke Naudoti esamą darbą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="910c9-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="910c9-158">Lauke Generuoti numerio lentelę pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="910c9-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="910c9-159">Išplėskite skyrių Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="910c9-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="910c9-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-160">Click New.</span></span>
10. <span data-ttu-id="910c9-161">Lauke Darbo klasės ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="910c9-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-162">Click Save.</span></span>
12. <span data-ttu-id="910c9-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-163">Close the page.</span></span>
13. <span data-ttu-id="910c9-164">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="910c9-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="910c9-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="910c9-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="910c9-166">Medyje pasirinkite „Medyje pasirinkite meniu elementą, kurį sukūrėte anksčiau.‟.</span><span class="sxs-lookup"><span data-stu-id="910c9-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="910c9-167">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="910c9-167">Click Edit.</span></span>
17. <span data-ttu-id="910c9-168">Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.</span><span class="sxs-lookup"><span data-stu-id="910c9-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="910c9-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-169">Click Save.</span></span>
19. <span data-ttu-id="910c9-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="910c9-171">Naujinti darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="910c9-171">Update a work template</span></span>
1. <span data-ttu-id="910c9-172">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="910c9-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="910c9-173">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="910c9-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="910c9-174">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="910c9-174">Click Edit.</span></span>
4. <span data-ttu-id="910c9-175">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="910c9-175">Click New.</span></span>
5. <span data-ttu-id="910c9-176">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="910c9-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="910c9-177">Lauke Darbo tipas pasirinkite „Spausdinti‟.</span><span class="sxs-lookup"><span data-stu-id="910c9-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="910c9-178">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="910c9-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="910c9-179">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="910c9-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="910c9-180">Spustelėkite Perkelti aukštyn.</span><span class="sxs-lookup"><span data-stu-id="910c9-180">Click Move up.</span></span>
10. <span data-ttu-id="910c9-181">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="910c9-181">Click Save.</span></span>
11. <span data-ttu-id="910c9-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="910c9-182">Close the page.</span></span>

