---
title: Numerio lentelės žymės spausdinimo įgalinimas
description: Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų.
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: 545f1c15888bcd0b46e1028f58cbe3a274846c92
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146036"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="f5d21-103">Numerio lentelės žymės spausdinimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="f5d21-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5d21-104">Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų.</span><span class="sxs-lookup"><span data-stu-id="f5d21-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="f5d21-105">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="f5d21-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="f5d21-106">Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="f5d21-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="f5d21-107">Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="f5d21-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="f5d21-108">Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="f5d21-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="f5d21-109">Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą.</span><span class="sxs-lookup"><span data-stu-id="f5d21-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="f5d21-110">Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.</span><span class="sxs-lookup"><span data-stu-id="f5d21-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="f5d21-111">Nustatyti GS1 įmonės prefiksą</span><span class="sxs-lookup"><span data-stu-id="f5d21-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="f5d21-112">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="f5d21-113">Lauke **GS1 įmonės prefiksas** įveskite 7 savo GS1 įmonės kodo skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="f5d21-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="f5d21-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-114">Select **Save**.</span></span>
4. <span data-ttu-id="f5d21-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="f5d21-116">Nustatyti SSCC numerio lentelės numeraciją</span><span class="sxs-lookup"><span data-stu-id="f5d21-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="f5d21-117">Eikite į **naršymo sritį > Moduliai > Organizacijos administravimas > Numeracija > Numeracija**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="f5d21-118">Lauke **Sritis** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="f5d21-119">Lauke **Nuoroda** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="f5d21-120">Lauke **Įmonė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="f5d21-121">Išplėskite skyrių **Segmentai**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="f5d21-122">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-122">Select **Edit**.</span></span>
7. <span data-ttu-id="f5d21-123">Lentelėje **Segmentai** pasirinkite pirmą eilutę</span><span class="sxs-lookup"><span data-stu-id="f5d21-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="f5d21-124">Pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-124">Select **Remove**.</span></span>
9. <span data-ttu-id="f5d21-125">Pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-125">Select **Remove**.</span></span>
10. <span data-ttu-id="f5d21-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-126">Select **Save**.</span></span>
11. <span data-ttu-id="f5d21-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="f5d21-128">Kurti dokumento maršruto maketą</span><span class="sxs-lookup"><span data-stu-id="f5d21-128">Create the document route layout</span></span>
1. <span data-ttu-id="f5d21-129">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="f5d21-130">Įgalinti SSCC maketą.</span><span class="sxs-lookup"><span data-stu-id="f5d21-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="f5d21-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-131">Select **New**.</span></span>
3. <span data-ttu-id="f5d21-132">Lauke **Maketo ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="f5d21-133">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f5d21-134">Pasirinkite **Įterpti teksto pabaigoje**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="f5d21-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-135">Select **Save**.</span></span>
7. <span data-ttu-id="f5d21-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="f5d21-137">Nustatyti dokumentų maršruto planavimą</span><span class="sxs-lookup"><span data-stu-id="f5d21-137">Set up the document routing</span></span>
1. <span data-ttu-id="f5d21-138">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="f5d21-139">Lauke **Darbo užsakymo tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="f5d21-140">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-140">Select **New**.</span></span>
4. <span data-ttu-id="f5d21-141">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="f5d21-142">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="f5d21-143">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-143">Select **New**.</span></span>
7. <span data-ttu-id="f5d21-144">Lauke **Maketo ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="f5d21-145">Lauke **Pavadinimas** įveskite norimą naudoti spausdintuvo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f5d21-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="f5d21-146">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-146">Select **Save**.</span></span>
10. <span data-ttu-id="f5d21-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="f5d21-148">Kurti mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="f5d21-148">Create mobile device menu</span></span>
1. <span data-ttu-id="f5d21-149">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="f5d21-150">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-150">Select **New**.</span></span>
3. <span data-ttu-id="f5d21-151">Lauke **Meniu elemento pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="f5d21-152">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="f5d21-153">Lauke **Režimas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="f5d21-154">Pasirinkite **Taip** lauke **Naudoti esamą darbą**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="f5d21-155">Pasirinkite **Taip** lauke **Generuoti numerio lentelę**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="f5d21-156">Išplėskite sekciją **Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="f5d21-157">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-157">Select **New**.</span></span>
10. <span data-ttu-id="f5d21-158">Lauke **Darbo klasės ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="f5d21-159">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-159">Select **Save**.</span></span>
12. <span data-ttu-id="f5d21-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-160">Close the page.</span></span>
13. <span data-ttu-id="f5d21-161">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="f5d21-162">Medyje pasirinkite anksčiau sukurtą meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="f5d21-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="f5d21-163">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-163">Select **Edit**.</span></span>
16. <span data-ttu-id="f5d21-164">Pasirinkę rodyklę, įtraukite meniu elementą į meniu.</span><span class="sxs-lookup"><span data-stu-id="f5d21-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="f5d21-165">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-165">Select **Save**.</span></span>
18. <span data-ttu-id="f5d21-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="f5d21-167">Naujinti darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="f5d21-167">Update a work template</span></span>
1. <span data-ttu-id="f5d21-168">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="f5d21-169">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-169">Select **Edit**.</span></span>
3. <span data-ttu-id="f5d21-170">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-170">Select **New**.</span></span>
4. <span data-ttu-id="f5d21-171">Lauke **Darbo tipas** pasirinkite **Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="f5d21-172">Lauke **Darbo klasės ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5d21-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="f5d21-173">Pasirinkite **Perkelti aukštyn**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-173">Select **Move up**.</span></span>
7. <span data-ttu-id="f5d21-174">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f5d21-174">Select **Save**.</span></span>
8. <span data-ttu-id="f5d21-175">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f5d21-175">Close the page.</span></span>

