---
title: Garantinio rašto operacija
description: Ši procedūra padeda apdoroti garantinius raštus.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "333650"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="0fa80-103">Garantinio rašto operacija</span><span class="sxs-lookup"><span data-stu-id="0fa80-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0fa80-104">Ši procedūra padeda apdoroti garantinius raštus.</span><span class="sxs-lookup"><span data-stu-id="0fa80-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="0fa80-105">Prieš baigdami šitą procedūrą, turite įvykdyti toliau nurodytas užduotis:</span><span class="sxs-lookup"><span data-stu-id="0fa80-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="0fa80-106">Nustatyti garantinio rašto banko priemones ir registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="0fa80-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="0fa80-107">Kurti garantinio rašto banko priemonės sutartį.</span><span class="sxs-lookup"><span data-stu-id="0fa80-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="0fa80-108">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="0fa80-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="0fa80-109">Kurti pardavimo užsakymą su garantiniu raštu</span><span class="sxs-lookup"><span data-stu-id="0fa80-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="0fa80-110">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0fa80-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-111">Click New.</span></span>
3. <span data-ttu-id="0fa80-112">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="0fa80-113">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="0fa80-113">Expand the General section.</span></span>
5. <span data-ttu-id="0fa80-114">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0fa80-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0fa80-116">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="0fa80-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0fa80-118">Lauke Banko dokumento tipas pasirinkite „Garantinis raštas“.</span><span class="sxs-lookup"><span data-stu-id="0fa80-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="0fa80-119">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-119">Click OK.</span></span>
11. <span data-ttu-id="0fa80-120">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="0fa80-121">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0fa80-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="0fa80-122">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="0fa80-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="0fa80-123">Spustelėkite skirtuką Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="0fa80-124">Pastaba: pristatymo datos valdymo pasirinkimas = nėra</span><span class="sxs-lookup"><span data-stu-id="0fa80-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="0fa80-125">Lauke Pageidaujama siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="0fa80-126">Lauke Patvirtinta siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="0fa80-127">Apdoroti garantinį raštą Užklausa</span><span class="sxs-lookup"><span data-stu-id="0fa80-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="0fa80-128">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="0fa80-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="0fa80-129">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="0fa80-130">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="0fa80-131">Spustelėdami Užklausa atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="0fa80-132">Lauke Tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="0fa80-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0fa80-134">Lauke Vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0fa80-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="0fa80-135">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="0fa80-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="0fa80-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-136">Click OK.</span></span>
10. <span data-ttu-id="0fa80-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0fa80-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="0fa80-138">Apdoroti garantinį raštą Pateikti bankui</span><span class="sxs-lookup"><span data-stu-id="0fa80-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="0fa80-139">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="0fa80-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0fa80-141">Spustelėdami Pateikti bankui atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="0fa80-142">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="0fa80-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0fa80-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="0fa80-145">Apdoroti garantinį raštą Gauti iš banko</span><span class="sxs-lookup"><span data-stu-id="0fa80-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="0fa80-146">Spustelėdami Gauti iš banko, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="0fa80-147">Lauke Banko numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa80-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="0fa80-148">Patikrinkite apskaičiuotų laukų Marža ir Išlaidos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0fa80-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="0fa80-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-149">Click OK.</span></span>
4. <span data-ttu-id="0fa80-150">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="0fa80-151">Patikrinkite įrašą „Gauti iš banko“.</span><span class="sxs-lookup"><span data-stu-id="0fa80-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="0fa80-152">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="0fa80-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="0fa80-153">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="0fa80-153">Click Lines.</span></span>
    * <span data-ttu-id="0fa80-154">Patikrinkite žurnalo įrašų registravimą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="0fa80-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0fa80-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="0fa80-156">Apdoroti garantinį raštą Duoti gavėjui</span><span class="sxs-lookup"><span data-stu-id="0fa80-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="0fa80-157">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0fa80-158">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0fa80-159">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="0fa80-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0fa80-160">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0fa80-161">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0fa80-162">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="0fa80-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-163">Click OK.</span></span>
8. <span data-ttu-id="0fa80-164">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="0fa80-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0fa80-166">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="0fa80-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-167">Click OK.</span></span>
12. <span data-ttu-id="0fa80-168">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="0fa80-169">Patikrinkite įrašą „Duoti gavėjui“.</span><span class="sxs-lookup"><span data-stu-id="0fa80-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="0fa80-170">Apdoroti garantinį raštą Didinti vertę</span><span class="sxs-lookup"><span data-stu-id="0fa80-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="0fa80-171">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0fa80-172">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0fa80-173">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="0fa80-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0fa80-174">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0fa80-175">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0fa80-176">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="0fa80-177">Lauke Įtrauktina vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0fa80-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="0fa80-178">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-178">Click OK.</span></span>
9. <span data-ttu-id="0fa80-179">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="0fa80-180">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="0fa80-181">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="0fa80-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-182">Click OK.</span></span>
13. <span data-ttu-id="0fa80-183">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="0fa80-184">Patikrinkite įrašą „Didinti vertę“.</span><span class="sxs-lookup"><span data-stu-id="0fa80-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="0fa80-185">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="0fa80-186">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="0fa80-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="0fa80-187">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="0fa80-187">Click Lines.</span></span>
    * <span data-ttu-id="0fa80-188">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="0fa80-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="0fa80-189">Apdoroti garantinį raštą Likviduoti</span><span class="sxs-lookup"><span data-stu-id="0fa80-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="0fa80-190">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0fa80-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0fa80-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0fa80-192">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="0fa80-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="0fa80-193">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="0fa80-194">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="0fa80-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="0fa80-195">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="0fa80-196">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-196">Click OK.</span></span>
8. <span data-ttu-id="0fa80-197">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="0fa80-198">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0fa80-199">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="0fa80-200">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0fa80-200">Click OK.</span></span>
12. <span data-ttu-id="0fa80-201">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0fa80-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="0fa80-202">Patikrinkite įrašą „Likviduoti“.</span><span class="sxs-lookup"><span data-stu-id="0fa80-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="0fa80-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0fa80-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="0fa80-204">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="0fa80-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="0fa80-205">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="0fa80-205">Click Lines.</span></span>
    * <span data-ttu-id="0fa80-206">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="0fa80-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="0fa80-207">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0fa80-207">Close the page.</span></span>

