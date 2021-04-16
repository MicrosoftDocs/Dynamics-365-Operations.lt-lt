---
title: Priminimo laiškų apdorojimo pavyzdys
description: Šioje temoje pateikiamas pavyzdys, kuriame parodomas priminimo laiškų kūrimo, spausdinimo ir registravimo procesas.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826352"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="99e63-103">Priminimo laiškų apdorojimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="99e63-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99e63-104">Šioje temoje pateikiamas pavyzdys, kuriame parodomas priminimo laiškų kūrimo, spausdinimo ir registravimo procesas.</span><span class="sxs-lookup"><span data-stu-id="99e63-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="99e63-105">Pavyzdys yra pagrįstas **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant priminimo laiško kodą** parinktis Kredite ir priminimuose.</span><span class="sxs-lookup"><span data-stu-id="99e63-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="99e63-106">Ji naudoja duomenis USMF demonstracinėje įmonėje ir naują klientą, JAV-045.</span><span class="sxs-lookup"><span data-stu-id="99e63-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="99e63-107">Norėdami pradėti, eikite į **Gautinos sąskaitos \> Klientai \> Visi klientai**, pasirinkite **Nauja** ir tada įveskite būtiną informaciją, kad sukurtumėte klientą JAV-045.</span><span class="sxs-lookup"><span data-stu-id="99e63-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="99e63-108">Pabaigus atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99e63-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="99e63-109">Eikite į **Kreditas ir priminimai \> Priminimo laiškas \> Nustatyti priminimo laiško eiliškumą** ir nustatykite priminimo laiško eiliškumą, kaip parodyta žemiau pateiktoje lentelėje, kuri paskirta kliento registravimo profilyje.</span><span class="sxs-lookup"><span data-stu-id="99e63-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="99e63-110">Priminimo laiško kodas</span><span class="sxs-lookup"><span data-stu-id="99e63-110">Collection   letter code</span></span>      |     <span data-ttu-id="99e63-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="99e63-111">Description</span></span>                           |     <span data-ttu-id="99e63-112">Valiuta</span><span class="sxs-lookup"><span data-stu-id="99e63-112">Currency</span></span>      |     <span data-ttu-id="99e63-113">Pagrindinė sąskaita</span><span class="sxs-lookup"><span data-stu-id="99e63-113">Main   account</span></span>        |     <span data-ttu-id="99e63-114">Mokestis valiuta</span><span class="sxs-lookup"><span data-stu-id="99e63-114">Fee   in currency</span></span>     |     <span data-ttu-id="99e63-115">Mažiausiai virš</span><span class="sxs-lookup"><span data-stu-id="99e63-115">Minimum   over</span></span>        |     <span data-ttu-id="99e63-116">Dienos blokuoti</span><span class="sxs-lookup"><span data-stu-id="99e63-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="99e63-117">1 priminimo laiškas</span><span class="sxs-lookup"><span data-stu-id="99e63-117">Collection   letter 1</span></span>         |     <span data-ttu-id="99e63-118">Antras pranešimas su mokesčiu</span><span class="sxs-lookup"><span data-stu-id="99e63-118">Second   notification with fee</span></span>        |     <span data-ttu-id="99e63-119">USD</span><span class="sxs-lookup"><span data-stu-id="99e63-119">USD</span></span>           |                           |     <span data-ttu-id="99e63-120">0,00</span><span class="sxs-lookup"><span data-stu-id="99e63-120">0.00</span></span>                  |     <span data-ttu-id="99e63-121">0,00</span><span class="sxs-lookup"><span data-stu-id="99e63-121">0.00</span></span>                  |     <span data-ttu-id="99e63-122">2</span><span class="sxs-lookup"><span data-stu-id="99e63-122">2</span></span>                 |
|     <span data-ttu-id="99e63-123">2 priminimo laiškas</span><span class="sxs-lookup"><span data-stu-id="99e63-123">Collection   letter 2</span></span>         |     <span data-ttu-id="99e63-124">Antras pranešimas su mokesčiu</span><span class="sxs-lookup"><span data-stu-id="99e63-124">Second   notification with fee</span></span>        |     <span data-ttu-id="99e63-125">USC</span><span class="sxs-lookup"><span data-stu-id="99e63-125">USC</span></span>           |     <span data-ttu-id="99e63-126">403150</span><span class="sxs-lookup"><span data-stu-id="99e63-126">403150</span></span>                |     <span data-ttu-id="99e63-127">20.00</span><span class="sxs-lookup"><span data-stu-id="99e63-127">20.00</span></span>                 |     <span data-ttu-id="99e63-128">10,00</span><span class="sxs-lookup"><span data-stu-id="99e63-128">10.00</span></span>                 |     <span data-ttu-id="99e63-129">3</span><span class="sxs-lookup"><span data-stu-id="99e63-129">3</span></span>                 |
|     <span data-ttu-id="99e63-130">Rinkimas</span><span class="sxs-lookup"><span data-stu-id="99e63-130">Collection</span></span>                    |     <span data-ttu-id="99e63-131">Paskutinis pranešimas su mokesčiu</span><span class="sxs-lookup"><span data-stu-id="99e63-131">Final   notification with fee</span></span>         |     <span data-ttu-id="99e63-132">USD</span><span class="sxs-lookup"><span data-stu-id="99e63-132">USD</span></span>           |     <span data-ttu-id="99e63-133">403150</span><span class="sxs-lookup"><span data-stu-id="99e63-133">403150</span></span>                |     <span data-ttu-id="99e63-134">50.00</span><span class="sxs-lookup"><span data-stu-id="99e63-134">50.00</span></span>                 |     <span data-ttu-id="99e63-135">100.00</span><span class="sxs-lookup"><span data-stu-id="99e63-135">100.00</span></span>                |     <span data-ttu-id="99e63-136">15</span><span class="sxs-lookup"><span data-stu-id="99e63-136">15</span></span>                |

<span data-ttu-id="99e63-137">Toliau pateikiamoje iliustracijoje rodoma informacija, kuri yra lentelėje tokia, kaip ji bus pateikta **Priminimo laiškai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="99e63-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="99e63-138">[![Priminimo laiško sekos nustatymas](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="99e63-139">Dabar turite nustatyti du šiam pavyzdžiui būtinus parametrus.</span><span class="sxs-lookup"><span data-stu-id="99e63-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="99e63-140">Eikite į **Kreditai ir priminimai \> Sąranka \> Gautinų sąskaitų parametrai** ir atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-141">**Priminimai** skirtuke nustatykite **Nepaisyti mokėjimų ir kreditų pažymų skaičiuojant priminimo laiško kodą** parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99e63-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="99e63-142">Įsitikinkite, kad lauke **Kurti priminimo laišką** nustatytas į **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="99e63-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="99e63-143">[![Gautinų sąskaitų parametrų Kredito priminimams nustatymas](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="99e63-144">Eikite į **Gautinos sąskaitos  \> Sąskaitos faktūros \> Visi laisvos formos teksto sąskaitos faktūros** ir tada pasirinkite **Nauja**, ir tada atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="99e63-145">Lauke **Kliento sąskaita** pasirinkite **JAV-045**.</span><span class="sxs-lookup"><span data-stu-id="99e63-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="99e63-146">Lauke **Sąskaitos faktūros data** įveskite **2021-01-15**.</span><span class="sxs-lookup"><span data-stu-id="99e63-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="99e63-147">Lauke **Termino pabaigos data** įveskite **2021-01-16**.</span><span class="sxs-lookup"><span data-stu-id="99e63-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="99e63-148">„FastTab”  **Sąskaitos faktūros eilutės** skirtuke **Pagrindinė sąskaita** įveskite **401100**.</span><span class="sxs-lookup"><span data-stu-id="99e63-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="99e63-149">Lauke **Vieneto kaina** įveskite **500.00**.</span><span class="sxs-lookup"><span data-stu-id="99e63-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="99e63-150">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="99e63-150">Select **Post**.</span></span>

    <span data-ttu-id="99e63-151">Dabar turite įvesti dvi kliento kredito pažymas.</span><span class="sxs-lookup"><span data-stu-id="99e63-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="99e63-152">Pasirinkite **Nauja** ir atlikite tolesnius veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="99e63-153">Lauke **Kliento kodas** pasirinkite **„US-045”**.</span><span class="sxs-lookup"><span data-stu-id="99e63-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="99e63-154">Lauke **Sąskaitos faktūros data** įveskite **2021-01-15**.</span><span class="sxs-lookup"><span data-stu-id="99e63-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="99e63-155">Lauke **Termino pabaigos data** įveskite **2021-01-16**.</span><span class="sxs-lookup"><span data-stu-id="99e63-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="99e63-156">„FastTab”  **Sąskaitos faktūros eilutės** skirtuke **Pagrindinė sąskaita** įveskite **401100**.</span><span class="sxs-lookup"><span data-stu-id="99e63-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="99e63-157">Lauke **Vieneto kaina** įveskite **-100,00**.</span><span class="sxs-lookup"><span data-stu-id="99e63-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="99e63-158">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="99e63-158">Select **Post**.</span></span>

5. <span data-ttu-id="99e63-159">Pakartokite 4-ą veiksmą, bet įveskite **-200,00** **Vieneto kaina** lauke.</span><span class="sxs-lookup"><span data-stu-id="99e63-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="99e63-160">Eikite į **Gautinos sąskaitos  \> Klientai \> Visi klientai** ir pasirinkite klientą **JAV-045**.</span><span class="sxs-lookup"><span data-stu-id="99e63-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="99e63-161">Tada Veiksmų srityje pasirinkite **Operacijos \> Operacijos**, kad peržiūrėtumėte anksčiau paskelbtas kliento operacijas.</span><span class="sxs-lookup"><span data-stu-id="99e63-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="99e63-162">[![Paskelbtų kliento operacijų peržiūra](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="99e63-163">Dabar privalote sukurti priminimo laiškus klientui JAV-045.</span><span class="sxs-lookup"><span data-stu-id="99e63-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="99e63-164">Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-165">Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99e63-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="99e63-166">Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.</span><span class="sxs-lookup"><span data-stu-id="99e63-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="99e63-167">Lauke **Priminimo laiško data** įveskite **2021-01-19**.</span><span class="sxs-lookup"><span data-stu-id="99e63-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="99e63-168">„FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.</span><span class="sxs-lookup"><span data-stu-id="99e63-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="99e63-169">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="99e63-169">Select **OK**.</span></span>
    5. <span data-ttu-id="99e63-170">Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="99e63-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="99e63-171">Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \>Peržiūrėti ir apdoroti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-172">Atkreipkite dėmesį, kad priminimo laiško kodas antraštėje ir operacijų eilutėse yra **Priminimo laiškas Nr. 1**, nes šis priminimo laiškas yra pirmas priminimo laiškas pagal eiliškumą.</span><span class="sxs-lookup"><span data-stu-id="99e63-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="99e63-173">(Norėdami peržiūrėti operacijos eilutes, jums gali tekti pasirinkti **Operacijos** „FastTab” skirtuke.)</span><span class="sxs-lookup"><span data-stu-id="99e63-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="99e63-174">[![Patikrinimas, ar antraštėje ir eilutėse rodomas toks pats priminimo laiško kodas](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="99e63-175">Veiksmų srityje pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="99e63-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="99e63-176">Lauke **Registravimo data** įveskite **2021-01-19**.</span><span class="sxs-lookup"><span data-stu-id="99e63-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="99e63-177">Dabar privalote vėl sukurti priminimo laiškus klientui JAV-045.</span><span class="sxs-lookup"><span data-stu-id="99e63-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="99e63-178">Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-179">Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99e63-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="99e63-180">Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.</span><span class="sxs-lookup"><span data-stu-id="99e63-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="99e63-181">Lauke **Priminimo laiško data** įveskite **2021-01-23**.</span><span class="sxs-lookup"><span data-stu-id="99e63-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="99e63-182">„FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.</span><span class="sxs-lookup"><span data-stu-id="99e63-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="99e63-183">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="99e63-183">Select **OK**.</span></span>
    5. <span data-ttu-id="99e63-184">Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="99e63-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="99e63-185">Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \>Peržiūrėti ir apdoroti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-186">Atkreipkite dėmesį, kad priminimo laiško kodas antraštėje yra **Priminimo laiškas Nr. 1**.</span><span class="sxs-lookup"><span data-stu-id="99e63-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="99e63-187">Tačiau operacijos eilučių kodas yra **Priminimo laiškas Nr. 2**.</span><span class="sxs-lookup"><span data-stu-id="99e63-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="99e63-188">[![Patikrina, ar antraštėje ir eilutėse rodomi skirtingi priminimo laiško kodai](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="99e63-189">Kodai skiriasi, nes **Ignoruoti mokėjimus ir kredito pažymas skaičiuojant priminimo laiškų kodą** parinktis nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99e63-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="99e63-190">Neregistruokite šio priminimo laiško.</span><span class="sxs-lookup"><span data-stu-id="99e63-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="99e63-191">Eikite į **Kreditas ir priminimai \> Sąranka \> Gautinų sąskaitų parametrai** ir tada **Priminimai** skirtuke nustatykite **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant laiško kodą** parinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="99e63-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="99e63-192">[![Nustatykite parinktį „Nepaisyti mokėjimų ir kredito pažymų apskaičiuojant priminimo laiško kodą” į Ne](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="99e63-193">Dabar privalote vėl sukurti priminimo laiškus klientui JAV-045.</span><span class="sxs-lookup"><span data-stu-id="99e63-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="99e63-194">Eikite į **Kreditai ir priminimai  \> Priminimo laiškas \> Sukurti priminimo laiškus** ir atlikite žemiau pateiktus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="99e63-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="99e63-195">Nustatykite **Sąskaita faktūra** ir **Kredito pažyma** parinktis į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99e63-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="99e63-196">Pagal numatytuosius nustatymus, lauke **Priminimo laiškas** turėtų būti nustatytas į **Kliento priminimas**.</span><span class="sxs-lookup"><span data-stu-id="99e63-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="99e63-197">Lauke **Priminimo laiško data** įveskite **2021-01-23**.</span><span class="sxs-lookup"><span data-stu-id="99e63-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="99e63-198">„FastTab” skirtuke **Įrašai, kuriuose reikia įtraukti** pasirinkite **Filtruoti** ir tada lauke **Kliento paskyra** pridėkite kliento **JAV-045**.</span><span class="sxs-lookup"><span data-stu-id="99e63-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="99e63-199">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="99e63-199">Select **OK**.</span></span>
    5. <span data-ttu-id="99e63-200">Pasirinkite **Gerai**, kad sukurtumėte priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="99e63-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="99e63-201">Eikite į **Kreditas ir priminimai \> Priminimo laiškas \> Peržiūrėti ir apdoroti priminimų laiškus** ir atkreipkite dėmesį, ar priminimo laiško kodas antraštėje ir operacijų eilutėse yra **Priminimo laiško Nr. 2**.</span><span class="sxs-lookup"><span data-stu-id="99e63-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="99e63-202">[![Tokio paties priminimo laiško kodo antraštėje ir eilutėse pakartotinis rodymas](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="99e63-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="99e63-203">Toks pat kodas atsiras abiejose vietose, nes **Nepaisyti mokėjimų ir kredito pažymų skaičiuojant priminimo laiško kodą** parinktis dabar nustatyta į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="99e63-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
