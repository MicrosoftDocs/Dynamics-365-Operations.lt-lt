---
title: Numerio lentelės žymės spausdinimo įgalinimas
description: Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43dc913e84fa53179855d7ab8dbbf4d179e2cc63
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383049"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="e2f1c-103">Numerio lentelės žymės spausdinimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="e2f1c-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2f1c-104">Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="e2f1c-105">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="e2f1c-106">Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="e2f1c-107">Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="e2f1c-108">Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="e2f1c-109">Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-109">On the Action Pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="e2f1c-110">Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="e2f1c-111">Nustatyti GS1 įmonės prefiksą</span><span class="sxs-lookup"><span data-stu-id="e2f1c-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="e2f1c-112">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="e2f1c-113">Lauke **GS1 įmonės prefiksas** įveskite 7 savo GS1 įmonės kodo skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="e2f1c-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-114">Select **Save**.</span></span>
4. <span data-ttu-id="e2f1c-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="e2f1c-116">Nustatyti SSCC numerio lentelės numeraciją</span><span class="sxs-lookup"><span data-stu-id="e2f1c-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="e2f1c-117">Eikite į **naršymo sritį > Moduliai > Organizacijos administravimas > Numeracija > Numeracija**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="e2f1c-118">Lauke **Sritis** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="e2f1c-119">Lauke **Nuoroda** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="e2f1c-120">Lauke **Įmonė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="e2f1c-121">Išplėskite skyrių **Segmentai**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="e2f1c-122">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-122">Select **Edit**.</span></span>
7. <span data-ttu-id="e2f1c-123">Lentelėje **Segmentai** pasirinkite pirmą eilutę</span><span class="sxs-lookup"><span data-stu-id="e2f1c-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="e2f1c-124">Pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-124">Select **Remove**.</span></span>
9. <span data-ttu-id="e2f1c-125">Pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-125">Select **Remove**.</span></span>
10. <span data-ttu-id="e2f1c-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-126">Select **Save**.</span></span>
11. <span data-ttu-id="e2f1c-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="e2f1c-128">Kurti dokumento maršruto maketą</span><span class="sxs-lookup"><span data-stu-id="e2f1c-128">Create the document route layout</span></span>
1. <span data-ttu-id="e2f1c-129">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="e2f1c-130">Įgalinti SSCC maketą.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="e2f1c-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-131">Select **New**.</span></span>
3. <span data-ttu-id="e2f1c-132">Lauke **Maketo ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="e2f1c-133">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e2f1c-134">Pasirinkite **Įterpti teksto pabaigoje**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="e2f1c-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-135">Select **Save**.</span></span>
7. <span data-ttu-id="e2f1c-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="e2f1c-137">Nustatyti dokumentų maršruto planavimą</span><span class="sxs-lookup"><span data-stu-id="e2f1c-137">Set up the document routing</span></span>
1. <span data-ttu-id="e2f1c-138">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="e2f1c-139">Lauke **Darbo užsakymo tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="e2f1c-140">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-140">Select **New**.</span></span>
4. <span data-ttu-id="e2f1c-141">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="e2f1c-142">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="e2f1c-143">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-143">Select **New**.</span></span>
7. <span data-ttu-id="e2f1c-144">Lauke **Maketo ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="e2f1c-145">Lauke **Pavadinimas** įveskite norimą naudoti spausdintuvo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="e2f1c-146">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-146">Select **Save**.</span></span>
10. <span data-ttu-id="e2f1c-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="e2f1c-148">Kurti mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="e2f1c-148">Create mobile device menu</span></span>
1. <span data-ttu-id="e2f1c-149">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="e2f1c-150">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-150">Select **New**.</span></span>
3. <span data-ttu-id="e2f1c-151">Lauke **Meniu elemento pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="e2f1c-152">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="e2f1c-153">Lauke **Režimas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="e2f1c-154">Pasirinkite **Taip** lauke **Naudoti esamą darbą**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="e2f1c-155">Pasirinkite **Taip** lauke **Generuoti numerio lentelę**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="e2f1c-156">Išplėskite sekciją **Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="e2f1c-157">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-157">Select **New**.</span></span>
10. <span data-ttu-id="e2f1c-158">Lauke **Darbo klasės ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="e2f1c-159">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-159">Select **Save**.</span></span>
12. <span data-ttu-id="e2f1c-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-160">Close the page.</span></span>
13. <span data-ttu-id="e2f1c-161">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="e2f1c-162">Medyje pasirinkite anksčiau sukurtą meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="e2f1c-163">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-163">Select **Edit**.</span></span>
16. <span data-ttu-id="e2f1c-164">Pasirinkę rodyklę, įtraukite meniu elementą į meniu.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="e2f1c-165">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-165">Select **Save**.</span></span>
18. <span data-ttu-id="e2f1c-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="e2f1c-167">Naujinti darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="e2f1c-167">Update a work template</span></span>
1. <span data-ttu-id="e2f1c-168">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="e2f1c-169">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-169">Select **Edit**.</span></span>
3. <span data-ttu-id="e2f1c-170">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-170">Select **New**.</span></span>
4. <span data-ttu-id="e2f1c-171">Lauke **Darbo tipas** pasirinkite **Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="e2f1c-172">Lauke **Darbo klasės ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="e2f1c-173">Pasirinkite **Perkelti aukštyn**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-173">Select **Move up**.</span></span>
7. <span data-ttu-id="e2f1c-174">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-174">Select **Save**.</span></span>
8. <span data-ttu-id="e2f1c-175">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e2f1c-175">Close the page.</span></span>

