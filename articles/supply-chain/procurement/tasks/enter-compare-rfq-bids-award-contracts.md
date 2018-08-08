--- 
title: "RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas"
description: "Šia procedūra rodoma, kaip į RFQ įvesti atsakymų, vertinti bei lyginti kainos pasiūlymus ir tada pasirinkti vieno iš tiekėjo kainos pasiūlymą."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e2b07323fc7c66e2e551f3eabb8e4965b85e92f4
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="643e6-103">RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="643e6-103">Enter and compare RFQ bids and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="643e6-104">Šia procedūra rodoma, kaip į RFQ įvesti atsakymų, vertinti bei lyginti kainos pasiūlymus ir tada pasirinkti vieno iš tiekėjo kainos pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="643e6-105">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="643e6-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="643e6-106">Prieš pradedant reikia turėti RFQ su dviem eilutėmis, išsiųstą bent dviem tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="643e6-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="643e6-107">Norėdami tokį sukurti, kaip būtinąjį komponentą galite vykdyti procedūrą „Pasiūlymo patvirtinimo kūrimas“.</span><span class="sxs-lookup"><span data-stu-id="643e6-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="643e6-108">Šios procedūros vykdyti negalėsite tol, kol nenustatysite vertinimo kriterijų.</span><span class="sxs-lookup"><span data-stu-id="643e6-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="643e6-109">Atsakymo iš tiekėjo įvedimas</span><span class="sxs-lookup"><span data-stu-id="643e6-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="643e6-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="643e6-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="643e6-111">Pasirinkite RFQ, kurio būsena yra Išsiųstas ir spustelėkite saitą ant pasiūlymo patvirtinimo atvejo numerio.</span><span class="sxs-lookup"><span data-stu-id="643e6-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="643e6-112">RFQ turėjo būti išsiųstas bent 2 tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="643e6-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="643e6-113">Spustelėdami antraštę, pereikite į tiekėjų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="643e6-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="643e6-114">Pasirinkite tiekėją, kuriam RFQ dokumente norite įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="643e6-115">Spustelėkite Įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-115">Click Enter reply.</span></span>
6. <span data-ttu-id="643e6-116">Veiksmų srityje spustelėkite Atsakymas.</span><span class="sxs-lookup"><span data-stu-id="643e6-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="643e6-117">Spustelėkite Kopijuoti duomenis į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="643e6-118">Šiuo veiksmu bus kopijuojami pasirinkti duomenys, pvz., kiekis iš RFQ atvejo į RFQ atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="643e6-119">Taip pat šį veiksmą galite praleisti ir visus atsakymo laukus užpildyti rankiniu būdu, redaguodami atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="643e6-120">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="643e6-120">Click Edit.</span></span>
9. <span data-ttu-id="643e6-121">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="643e6-122">Pasirinkite kitą pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="643e6-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="643e6-123">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="643e6-124">Kainos pasiūlymo vertinimas</span><span class="sxs-lookup"><span data-stu-id="643e6-124">Score the bid</span></span>
1. <span data-ttu-id="643e6-125">Spustelėdami antraštę, pereikite prie kainos pasiūlymo vertinimo.</span><span class="sxs-lookup"><span data-stu-id="643e6-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="643e6-126">Išplėskite dalį Kainos pasiūlymo vertinimas.</span><span class="sxs-lookup"><span data-stu-id="643e6-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="643e6-127">Lauke Rezultatas įveskite vieno iš vertinimo kriterijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="643e6-128">Jei ant vieno iš vertinimo kriterijų užvedate pele, patariama, kokiame intervale turi būti jūsų rezultatas.</span><span class="sxs-lookup"><span data-stu-id="643e6-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="643e6-129">Šioje demonstracijoje į bet kurį iš kriterijų galite įtraukti skaičių nuo 1 iki 5.</span><span class="sxs-lookup"><span data-stu-id="643e6-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="643e6-130">Pasirinkite kitą vertinimo kriterijų.</span><span class="sxs-lookup"><span data-stu-id="643e6-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="643e6-131">Lauke Rezultatas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="643e6-132">Išplėskite dalį Klausimynai.</span><span class="sxs-lookup"><span data-stu-id="643e6-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="643e6-133">Jei RFQ atvejyje yra tiekėjams išsiųstas klausimynas, jų atsakymus galite įvesti klausimyno skyriuje.</span><span class="sxs-lookup"><span data-stu-id="643e6-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="643e6-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="643e6-135">Kito tiekėjo atsakymo įvedimas</span><span class="sxs-lookup"><span data-stu-id="643e6-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="643e6-136">Pasirinkite kitą tiekėją – išvalykite tiekėją, kuriam ką tik įvedėte atsakymą ir pasirinkite kito tiekėjo eilutę.</span><span class="sxs-lookup"><span data-stu-id="643e6-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="643e6-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="643e6-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="643e6-138">Spustelėkite Įvesti atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-138">Click Enter reply.</span></span>
4. <span data-ttu-id="643e6-139">Spustelėkite Kopijuoti duomenis į atsakymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="643e6-140">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="643e6-140">Click Edit.</span></span>
6. <span data-ttu-id="643e6-141">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="643e6-142">Pasirinkite kitą pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="643e6-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="643e6-143">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="643e6-144">Antro kainos pasiūlymo vertinimas</span><span class="sxs-lookup"><span data-stu-id="643e6-144">Score the second bid</span></span>
1. <span data-ttu-id="643e6-145">Spustelėdami antraštę, pereikite prie kainos pasiūlymo vertinimo.</span><span class="sxs-lookup"><span data-stu-id="643e6-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="643e6-146">Lauke Rezultatas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="643e6-147">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="643e6-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="643e6-148">Lauke Rezultatas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="643e6-149">Atsakymų palyginimas</span><span class="sxs-lookup"><span data-stu-id="643e6-149">Compare the replies</span></span>
1. <span data-ttu-id="643e6-150">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="643e6-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="643e6-151">Spustelėkite Palyginti atsakymus.</span><span class="sxs-lookup"><span data-stu-id="643e6-151">Click Compare replies.</span></span>
3. <span data-ttu-id="643e6-152">Lauke Reitingas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="643e6-153">Šiame puslapyje rodomi kainų pasiūlymai su antrašte ir eilutėmis bei bendras rezultatas antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="643e6-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="643e6-154">Eilutes galite palyginti jas rūšiuodami tinklelyje, kad palyginamos eilutės būtų viena šalia kitos.</span><span class="sxs-lookup"><span data-stu-id="643e6-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="643e6-155">Taip pat pateikiama tolesnė informacija. Kiekis: tiekėjo pasiūlytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="643e6-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="643e6-156">Jis gali skirtis nuo RFQ nurodyto kiekio.</span><span class="sxs-lookup"><span data-stu-id="643e6-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="643e6-157">Grynoji suma – atėmus visas nuolaidas tiekėjo siūloma kaina už eilutėje nurodytas prekes.</span><span class="sxs-lookup"><span data-stu-id="643e6-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="643e6-158">Nuokrypis: dienų skaičius, kuriuo kainos pasiūlymo antraštėje arba eilutėje nurodyta pristatymo data skiriasi nuo pageidaujamos RFQ antraštėje arba RFQ eilutėje nurodytos pristatymo datos.</span><span class="sxs-lookup"><span data-stu-id="643e6-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="643e6-159">Galite įvesti kiekvieno kainos pasiūlymo reitingą.</span><span class="sxs-lookup"><span data-stu-id="643e6-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="643e6-160">Pasirinkite kito norimo reitinguoti kainos pasiūlymo antraštės eilutę.</span><span class="sxs-lookup"><span data-stu-id="643e6-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="643e6-161">Lauke Reitingas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="643e6-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="643e6-162">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="643e6-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="643e6-163">Kainos pasiūlymo atmetimas</span><span class="sxs-lookup"><span data-stu-id="643e6-163">Reject a bid</span></span>
1. <span data-ttu-id="643e6-164">Pasirinkite norimo atmesti kainos pasiūlymo antraštės eilutę.</span><span class="sxs-lookup"><span data-stu-id="643e6-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="643e6-165">Vienu metu vieną kainos pasiūlymą ar vieno kainos pasiūlymo eilutes galite tik priimti, atmesti arba grąžinti.</span><span class="sxs-lookup"><span data-stu-id="643e6-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="643e6-166">Pažymėkite žymės langelį Žymėti.</span><span class="sxs-lookup"><span data-stu-id="643e6-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="643e6-167">Jei kainos pasiūlymo antraštėje pažymėsite žymės langelį Žymėti, taip pat bus pažymėtos visos eilutės.</span><span class="sxs-lookup"><span data-stu-id="643e6-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="643e6-168">Taip pat galite pasirinkti pažymėti kainos pasiūlymo eilučių subrinkinį ir taip jas atmesti arba priimti.</span><span class="sxs-lookup"><span data-stu-id="643e6-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="643e6-169">Galima dėl kai kurių RFQ eilučių priimti vieno tiekėjo kainos pasiūlymą, o kitas RFQ eilutes paskirti kitam tiekėjui, tačiau tai atlikti reikia 2 veiksmais, vienu metu dirbant su vienu kainos pasiūlymu.</span><span class="sxs-lookup"><span data-stu-id="643e6-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="643e6-170">Jei yra pakaitinių eilučių, galite priimti tik pradinę pasiūlymo eilutę arba jos pakaitą, bet ne abu.</span><span class="sxs-lookup"><span data-stu-id="643e6-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="643e6-171">Spustelėkite Atmesti.</span><span class="sxs-lookup"><span data-stu-id="643e6-171">Click Reject.</span></span>
4. <span data-ttu-id="643e6-172">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="643e6-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="643e6-173">Lauke Atmetimo priežastis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="643e6-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="643e6-174">Atmetimo priežastis bus išsaugota atsakyme.</span><span class="sxs-lookup"><span data-stu-id="643e6-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="643e6-175">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="643e6-175">Click OK.</span></span>
7. <span data-ttu-id="643e6-176">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="643e6-176">Click OK.</span></span>
8. <span data-ttu-id="643e6-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-177">Close the page.</span></span>
9. <span data-ttu-id="643e6-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-178">Close the page.</span></span>
10. <span data-ttu-id="643e6-179">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="643e6-180">Kainos pasiūlymo priėmimas</span><span class="sxs-lookup"><span data-stu-id="643e6-180">Accept a bid</span></span>
1. <span data-ttu-id="643e6-181">Pasirinkite pasiūlymą, kurį norite priimti ir spustelėkite lauke Pasiūlymo patvirtinimas esantį saitą.</span><span class="sxs-lookup"><span data-stu-id="643e6-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="643e6-182">Veiksmų srityje spustelėkite Atsakymas.</span><span class="sxs-lookup"><span data-stu-id="643e6-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="643e6-183">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="643e6-183">Click Accept.</span></span>
    * <span data-ttu-id="643e6-184">Jei pažymėjote konkrečias eilutes, į priėmimo veiksmą bus įtrauktos tik pažymėtos eilutės.</span><span class="sxs-lookup"><span data-stu-id="643e6-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="643e6-185">Jei norite priimti visas kainos pasiūlymo eilutes, tada eilučių žymėti nereikia.</span><span class="sxs-lookup"><span data-stu-id="643e6-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="643e6-186">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="643e6-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="643e6-187">Taip galite įrašyti kainos pasiūlymo priėmimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="643e6-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="643e6-188">Priežastis bus išsaugota kainos pasiūlyme.</span><span class="sxs-lookup"><span data-stu-id="643e6-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="643e6-189">Lauke Priėmimo priežastis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="643e6-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="643e6-190">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="643e6-190">Click OK.</span></span>
7. <span data-ttu-id="643e6-191">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="643e6-191">Click OK.</span></span>
    * <span data-ttu-id="643e6-192">Spustelėjus Gerai, pagal eilutes, įtrauktas į RFQ priėmimą, sugeneruojamas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="643e6-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="643e6-193">Jei yra kitų neapdorotų (priimtų, atmestų ar grąžintų) kainos pasiūlymų, sistema jus paragins likusius kainos pasiūlymus atmesti.</span><span class="sxs-lookup"><span data-stu-id="643e6-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="643e6-194">Sugeneruoto pirkimo užsakymo peržiūra</span><span class="sxs-lookup"><span data-stu-id="643e6-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="643e6-195">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="643e6-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="643e6-196">Spustelėkite Pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="643e6-196">Click Purchase order.</span></span>
    * <span data-ttu-id="643e6-197">Čia galite peržiūrėti pirkimo užsakymą, kuris buvo sugeneruotas, kai priėmėte kainos pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="643e6-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="643e6-198">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-198">Close the page.</span></span>
4. <span data-ttu-id="643e6-199">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-199">Close the page.</span></span>
5. <span data-ttu-id="643e6-200">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-200">Close the page.</span></span>
6. <span data-ttu-id="643e6-201">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="643e6-201">Close the page.</span></span>


