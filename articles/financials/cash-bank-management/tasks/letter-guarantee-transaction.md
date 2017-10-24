--- 
title: "Garantinio rašto operacija"
description: "Ši procedūra padeda apdoroti garantinius raštus."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="869d5-103">Garantinio rašto operacija</span><span class="sxs-lookup"><span data-stu-id="869d5-103">Letter of guarantee transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="869d5-104">Ši procedūra padeda apdoroti garantinius raštus.</span><span class="sxs-lookup"><span data-stu-id="869d5-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="869d5-105">Prieš baigdami šitą procedūrą, turite įvykdyti toliau nurodytas užduotis:</span><span class="sxs-lookup"><span data-stu-id="869d5-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="869d5-106">Nustatyti garantinio rašto banko priemones ir registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="869d5-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="869d5-107">Kurti garantinio rašto banko priemonės sutartį.</span><span class="sxs-lookup"><span data-stu-id="869d5-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="869d5-108">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="869d5-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="869d5-109">Kurti pardavimo užsakymą su garantiniu raštu</span><span class="sxs-lookup"><span data-stu-id="869d5-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="869d5-110">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="869d5-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="869d5-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="869d5-111">Click New.</span></span>
3. <span data-ttu-id="869d5-112">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="869d5-113">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="869d5-113">Expand the General section.</span></span>
5. <span data-ttu-id="869d5-114">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="869d5-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="869d5-116">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="869d5-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="869d5-118">Lauke Banko dokumento tipas pasirinkite „Garantinis raštas“.</span><span class="sxs-lookup"><span data-stu-id="869d5-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="869d5-119">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="869d5-119">Click OK.</span></span>
11. <span data-ttu-id="869d5-120">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="869d5-121">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="869d5-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="869d5-122">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="869d5-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="869d5-123">Spustelėkite skirtuką Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="869d5-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="869d5-124">Pastaba: pristatymo datos valdymo pasirinkimas = nėra</span><span class="sxs-lookup"><span data-stu-id="869d5-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="869d5-125">Lauke Pageidaujama siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="869d5-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="869d5-126">Lauke Patvirtinta siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="869d5-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="869d5-127">Apdoroti garantinį raštą Užklausa</span><span class="sxs-lookup"><span data-stu-id="869d5-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="869d5-128">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="869d5-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="869d5-129">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="869d5-130">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="869d5-131">Spustelėdami Užklausa atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="869d5-132">Lauke Tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="869d5-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="869d5-134">Lauke Vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="869d5-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="869d5-135">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="869d5-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="869d5-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-136">Click OK.</span></span>
10. <span data-ttu-id="869d5-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="869d5-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="869d5-138">Apdoroti garantinį raštą Pateikti bankui</span><span class="sxs-lookup"><span data-stu-id="869d5-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="869d5-139">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="869d5-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="869d5-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="869d5-141">Spustelėdami Pateikti bankui atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="869d5-142">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="869d5-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="869d5-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="869d5-145">Apdoroti garantinį raštą Gauti iš banko</span><span class="sxs-lookup"><span data-stu-id="869d5-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="869d5-146">Spustelėdami Gauti iš banko, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="869d5-147">Lauke Banko numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="869d5-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="869d5-148">Patikrinkite apskaičiuotų laukų Marža ir Išlaidos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="869d5-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="869d5-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-149">Click OK.</span></span>
4. <span data-ttu-id="869d5-150">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="869d5-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="869d5-151">Patikrinkite įrašą „Gauti iš banko“.</span><span class="sxs-lookup"><span data-stu-id="869d5-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="869d5-152">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="869d5-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="869d5-153">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="869d5-153">Click Lines.</span></span>
    * <span data-ttu-id="869d5-154">Patikrinkite žurnalo įrašų registravimą.</span><span class="sxs-lookup"><span data-stu-id="869d5-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="869d5-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="869d5-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="869d5-156">Apdoroti garantinį raštą Duoti gavėjui</span><span class="sxs-lookup"><span data-stu-id="869d5-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="869d5-157">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="869d5-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="869d5-158">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="869d5-159">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="869d5-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="869d5-160">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="869d5-161">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="869d5-162">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="869d5-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-163">Click OK.</span></span>
8. <span data-ttu-id="869d5-164">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="869d5-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="869d5-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="869d5-166">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="869d5-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-167">Click OK.</span></span>
12. <span data-ttu-id="869d5-168">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="869d5-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="869d5-169">Patikrinkite įrašą „Duoti gavėjui“.</span><span class="sxs-lookup"><span data-stu-id="869d5-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="869d5-170">Apdoroti garantinį raštą Didinti vertę</span><span class="sxs-lookup"><span data-stu-id="869d5-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="869d5-171">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="869d5-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="869d5-172">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="869d5-173">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="869d5-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="869d5-174">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="869d5-175">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="869d5-176">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="869d5-177">Lauke Įtrauktina vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="869d5-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="869d5-178">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-178">Click OK.</span></span>
9. <span data-ttu-id="869d5-179">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="869d5-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="869d5-180">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="869d5-181">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="869d5-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-182">Click OK.</span></span>
13. <span data-ttu-id="869d5-183">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="869d5-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="869d5-184">Patikrinkite įrašą „Didinti vertę“.</span><span class="sxs-lookup"><span data-stu-id="869d5-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="869d5-185">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="869d5-186">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="869d5-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="869d5-187">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="869d5-187">Click Lines.</span></span>
    * <span data-ttu-id="869d5-188">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="869d5-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="869d5-189">Apdoroti garantinį raštą Likviduoti</span><span class="sxs-lookup"><span data-stu-id="869d5-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="869d5-190">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="869d5-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="869d5-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="869d5-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="869d5-192">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="869d5-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="869d5-193">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="869d5-194">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="869d5-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="869d5-195">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="869d5-196">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-196">Click OK.</span></span>
8. <span data-ttu-id="869d5-197">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="869d5-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="869d5-198">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="869d5-199">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="869d5-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="869d5-200">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="869d5-200">Click OK.</span></span>
12. <span data-ttu-id="869d5-201">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="869d5-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="869d5-202">Patikrinkite įrašą „Likviduoti“.</span><span class="sxs-lookup"><span data-stu-id="869d5-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="869d5-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="869d5-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="869d5-204">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="869d5-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="869d5-205">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="869d5-205">Click Lines.</span></span>
    * <span data-ttu-id="869d5-206">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="869d5-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="869d5-207">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="869d5-207">Close the page.</span></span>


