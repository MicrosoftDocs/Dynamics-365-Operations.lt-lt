---
title: Garantinio rašto operacija
description: Ši procedūra padeda apdoroti garantinius raštus.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 089515287fc5706983b10614f69b4b1cd90178c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834721"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="e3cd8-103">Garantinio rašto operacija</span><span class="sxs-lookup"><span data-stu-id="e3cd8-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3cd8-104">Ši procedūra padeda apdoroti garantinius raštus.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="e3cd8-105">Prieš baigdami šitą procedūrą, turite įvykdyti toliau nurodytas užduotis:</span><span class="sxs-lookup"><span data-stu-id="e3cd8-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="e3cd8-106">Nustatyti garantinio rašto banko priemones ir registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="e3cd8-107">Kurti garantinio rašto banko priemonės sutartį.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="e3cd8-108">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="e3cd8-109">Kurti pardavimo užsakymą su garantiniu raštu</span><span class="sxs-lookup"><span data-stu-id="e3cd8-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="e3cd8-110">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e3cd8-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-111">Click New.</span></span>
3. <span data-ttu-id="e3cd8-112">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="e3cd8-113">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-113">Expand the General section.</span></span>
5. <span data-ttu-id="e3cd8-114">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="e3cd8-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e3cd8-116">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="e3cd8-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e3cd8-118">Lauke Banko dokumento tipas pasirinkite „Garantinis raštas“.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="e3cd8-119">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-119">Click OK.</span></span>
11. <span data-ttu-id="e3cd8-120">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="e3cd8-121">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="e3cd8-122">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="e3cd8-123">Spustelėkite skirtuką Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="e3cd8-124">Pastaba: pristatymo datos valdymo pasirinkimas = nėra</span><span class="sxs-lookup"><span data-stu-id="e3cd8-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="e3cd8-125">Lauke Pageidaujama siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="e3cd8-126">Lauke Patvirtinta siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="e3cd8-127">Apdoroti garantinį raštą Užklausa</span><span class="sxs-lookup"><span data-stu-id="e3cd8-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="e3cd8-128">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="e3cd8-129">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="e3cd8-130">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="e3cd8-131">Spustelėdami Užklausa atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="e3cd8-132">Lauke Tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="e3cd8-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e3cd8-134">Lauke Vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="e3cd8-135">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="e3cd8-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-136">Click OK.</span></span>
10. <span data-ttu-id="e3cd8-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="e3cd8-138">Apdoroti garantinį raštą Pateikti bankui</span><span class="sxs-lookup"><span data-stu-id="e3cd8-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="e3cd8-139">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="e3cd8-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e3cd8-141">Spustelėdami Pateikti bankui atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="e3cd8-142">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="e3cd8-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e3cd8-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="e3cd8-145">Apdoroti garantinį raštą Gauti iš banko</span><span class="sxs-lookup"><span data-stu-id="e3cd8-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="e3cd8-146">Spustelėdami Gauti iš banko, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="e3cd8-147">Lauke Banko numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="e3cd8-148">Patikrinkite apskaičiuotų laukų Marža ir Išlaidos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="e3cd8-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-149">Click OK.</span></span>
4. <span data-ttu-id="e3cd8-150">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="e3cd8-151">Patikrinkite įrašą „Gauti iš banko“.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="e3cd8-152">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="e3cd8-153">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-153">Click Lines.</span></span>
    * <span data-ttu-id="e3cd8-154">Patikrinkite žurnalo įrašų registravimą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="e3cd8-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="e3cd8-156">Apdoroti garantinį raštą Duoti gavėjui</span><span class="sxs-lookup"><span data-stu-id="e3cd8-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="e3cd8-157">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e3cd8-158">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e3cd8-159">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e3cd8-160">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e3cd8-161">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e3cd8-162">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="e3cd8-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-163">Click OK.</span></span>
8. <span data-ttu-id="e3cd8-164">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="e3cd8-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e3cd8-166">Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="e3cd8-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-167">Click OK.</span></span>
12. <span data-ttu-id="e3cd8-168">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="e3cd8-169">Patikrinkite įrašą „Duoti gavėjui“.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="e3cd8-170">Apdoroti garantinį raštą Didinti vertę</span><span class="sxs-lookup"><span data-stu-id="e3cd8-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="e3cd8-171">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e3cd8-172">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e3cd8-173">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e3cd8-174">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e3cd8-175">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e3cd8-176">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="e3cd8-177">Lauke Įtrauktina vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="e3cd8-178">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-178">Click OK.</span></span>
9. <span data-ttu-id="e3cd8-179">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="e3cd8-180">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e3cd8-181">Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="e3cd8-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-182">Click OK.</span></span>
13. <span data-ttu-id="e3cd8-183">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="e3cd8-184">Patikrinkite įrašą „Didinti vertę“.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="e3cd8-185">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="e3cd8-186">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="e3cd8-187">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-187">Click Lines.</span></span>
    * <span data-ttu-id="e3cd8-188">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="e3cd8-189">Apdoroti garantinį raštą Likviduoti</span><span class="sxs-lookup"><span data-stu-id="e3cd8-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="e3cd8-190">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="e3cd8-191">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="e3cd8-192">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="e3cd8-193">Spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="e3cd8-194">Veiksmų srityje spustelėkite Garantinis raštas.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="e3cd8-195">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="e3cd8-196">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-196">Click OK.</span></span>
8. <span data-ttu-id="e3cd8-197">Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="e3cd8-198">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e3cd8-199">Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="e3cd8-200">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-200">Click OK.</span></span>
12. <span data-ttu-id="e3cd8-201">Išplėskite sekciją Veiksmai.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="e3cd8-202">Patikrinkite įrašą „Likviduoti“.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="e3cd8-203">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e3cd8-204">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="e3cd8-205">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-205">Click Lines.</span></span>
    * <span data-ttu-id="e3cd8-206">Patikrinkite užregistruotus žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="e3cd8-207">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e3cd8-207">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]