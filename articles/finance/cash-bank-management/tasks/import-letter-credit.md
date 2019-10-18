---
title: Importuoti akredityvą
description: Ši procedūra padeda importuoti akredityvą.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72a50b2cdda5d66e8aa4660f914e6f5e51531b5f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188147"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="b0b02-103">Importuoti akredityvą</span><span class="sxs-lookup"><span data-stu-id="b0b02-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0b02-104">Ši procedūra padeda importuoti akredityvą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="b0b02-105">Prieš atliekant šią procedūrą reikia nustatyti: banko priemones, registravimo šablonus, banko priemonės sutartį ir tiekėjo banko informaciją.</span><span class="sxs-lookup"><span data-stu-id="b0b02-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="b0b02-106">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="b0b02-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="b0b02-107">Kurti pirkimo užsakymą su akredityvu</span><span class="sxs-lookup"><span data-stu-id="b0b02-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="b0b02-108">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b0b02-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b0b02-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-109">Click New.</span></span>
3. <span data-ttu-id="b0b02-110">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="b0b02-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b0b02-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b0b02-113">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="b0b02-113">Expand the General section.</span></span>
7. <span data-ttu-id="b0b02-114">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="b0b02-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b0b02-116">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="b0b02-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b0b02-118">Lauke „Apskaitos data“ įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="b0b02-119">Lauke Pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="b0b02-120">Pastaba: turi būti pasirinkta lauko „Banko dokumento tipas“ reikšmė „Akredityvas“.</span><span class="sxs-lookup"><span data-stu-id="b0b02-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="b0b02-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-121">Click OK.</span></span>
14. <span data-ttu-id="b0b02-122">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="b0b02-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b0b02-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b0b02-125">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="b0b02-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="b0b02-126">Spustelėkite skirtuką Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="b0b02-127">Lauke Pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="b0b02-128">Lauke Patvirtinta pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="b0b02-129">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b0b02-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="b0b02-130">Nurodykite akredityvo informaciją.</span><span class="sxs-lookup"><span data-stu-id="b0b02-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="b0b02-131">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="b0b02-132">Spustelėkite Akredityvo / importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="b0b02-133">Lauke Prašymo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="b0b02-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="b0b02-134">Patikrinkite, ar lauko „Banko sąskaita“ reikšmė yra numatytoji aktyvi banko sąskaita, pagrįsta taikymo data.</span><span class="sxs-lookup"><span data-stu-id="b0b02-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="b0b02-135">Lauke Banko dokumento numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="b0b02-136">Lauke Gavimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="b0b02-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="b0b02-137">Išplėskite skyrių Banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="b0b02-138">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="b0b02-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="b0b02-139">Išplėskite sekciją Banko informacija.</span><span class="sxs-lookup"><span data-stu-id="b0b02-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="b0b02-140">Lauke Konsultavimo bankas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="b0b02-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="b0b02-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-142">Click Save.</span></span>
33. <span data-ttu-id="b0b02-143">Spustelėkite Surasti pirkimo užsakymo siuntas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="b0b02-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-144">Close the page.</span></span>
35. <span data-ttu-id="b0b02-145">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="b0b02-146">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-146">Click Confirm.</span></span>
37. <span data-ttu-id="b0b02-147">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="b0b02-148">Spustelėkite Akredityvo / importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="b0b02-149">Spustelėkite „Apdoroti“.</span><span class="sxs-lookup"><span data-stu-id="b0b02-149">Click Process.</span></span>
40. <span data-ttu-id="b0b02-150">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-150">Click Confirm.</span></span>
    * <span data-ttu-id="b0b02-151">Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="b0b02-152">Šiame pavyzdyje pirkimo suma = 500,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="b0b02-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="b0b02-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-153">Close the page.</span></span>
42. <span data-ttu-id="b0b02-154">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b0b02-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="b0b02-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-155">Click Save.</span></span>
44. <span data-ttu-id="b0b02-156">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="b0b02-157">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-157">Click Confirm.</span></span>
    * <span data-ttu-id="b0b02-158">Keiskite akredityvą dėl pakeistos vieneto kainos.</span><span class="sxs-lookup"><span data-stu-id="b0b02-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="b0b02-159">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="b0b02-160">Spustelėkite Akredityvo / importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="b0b02-161">Keiskite akredityvą dėl pakeistos pirkimo vieneto kainos.</span><span class="sxs-lookup"><span data-stu-id="b0b02-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="b0b02-162">Spustelėkite „Apdoroti“.</span><span class="sxs-lookup"><span data-stu-id="b0b02-162">Click Process.</span></span>
49. <span data-ttu-id="b0b02-163">Spustelėkite Keisti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-163">Click Amend.</span></span>
50. <span data-ttu-id="b0b02-164">Spustelėkite Šalinti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-164">Click Remove.</span></span>
51. <span data-ttu-id="b0b02-165">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b0b02-165">Click Yes.</span></span>
52. <span data-ttu-id="b0b02-166">Spustelėkite Surasti pirkimo užsakymo siuntas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="b0b02-167">Spustelėkite „Apdoroti“.</span><span class="sxs-lookup"><span data-stu-id="b0b02-167">Click Process.</span></span>
54. <span data-ttu-id="b0b02-168">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-168">Click Confirm.</span></span>
    * <span data-ttu-id="b0b02-169">Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="b0b02-170">Šiame pavyzdyje pakeista pirkimo suma = 600,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="b0b02-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="b0b02-171">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="b0b02-172">Registruoti važtaraštį</span><span class="sxs-lookup"><span data-stu-id="b0b02-172">Post Packing slip</span></span>
1. <span data-ttu-id="b0b02-173">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="b0b02-174">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-174">Click Product receipt.</span></span>
3. <span data-ttu-id="b0b02-175">Lauke „PurchParmTable_Num“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="b0b02-176">Pasirinkite siuntos numerį, sukurtą remiantis akredityvu.</span><span class="sxs-lookup"><span data-stu-id="b0b02-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="b0b02-177">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b0b02-178">Lauke Produkto gavimo kvito data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="b0b02-179">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-179">Click OK.</span></span>
7. <span data-ttu-id="b0b02-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-180">Close the page.</span></span>
8. <span data-ttu-id="b0b02-181">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="b0b02-182">Tikrinti importo akredityvo būseną</span><span class="sxs-lookup"><span data-stu-id="b0b02-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="b0b02-183">Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="b0b02-184">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0b02-185">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0b02-186">Patikrinkite importo akredityvo būseną.</span><span class="sxs-lookup"><span data-stu-id="b0b02-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="b0b02-187">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-187">Close the page.</span></span>
5. <span data-ttu-id="b0b02-188">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="b0b02-189">Registruoti pirkimo SF</span><span class="sxs-lookup"><span data-stu-id="b0b02-189">Post purchase invoice</span></span>
1. <span data-ttu-id="b0b02-190">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b0b02-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="b0b02-191">Pasirinkite pirkimo užsakymą, sukurtą naudojant akredityvą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="b0b02-192">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0b02-193">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b0b02-194">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="b0b02-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="b0b02-195">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="b0b02-195">Click Invoice.</span></span>
6. <span data-ttu-id="b0b02-196">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="b0b02-197">Lauke Siuntos numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="b0b02-198">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b0b02-199">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="b0b02-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="b0b02-200">Spustelėkite Naujinti gretinimo būseną.</span><span class="sxs-lookup"><span data-stu-id="b0b02-200">Click Update match status.</span></span>
11. <span data-ttu-id="b0b02-201">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-201">Click Post.</span></span>
12. <span data-ttu-id="b0b02-202">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-202">Close the page.</span></span>
13. <span data-ttu-id="b0b02-203">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="b0b02-204">Tikrinti importo akredityvo būseną</span><span class="sxs-lookup"><span data-stu-id="b0b02-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="b0b02-205">Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="b0b02-206">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0b02-207">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0b02-208">Patikrinkite 2 importo akredityvą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="b0b02-209">Tikrinti: siuntos būsena = banko paslaugos, kurių SF išrašytos, informacija</span><span class="sxs-lookup"><span data-stu-id="b0b02-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="b0b02-210">Spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-210">Click View.</span></span>
5. <span data-ttu-id="b0b02-211">Spustelėkite Spausdinti prašymą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-211">Click Print application.</span></span>
6. <span data-ttu-id="b0b02-212">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-212">Click OK.</span></span>
    * <span data-ttu-id="b0b02-213">Patikrinkite, ar spausdinamas akredityvo prašymas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="b0b02-214">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-214">Close the page.</span></span>
8. <span data-ttu-id="b0b02-215">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-215">Close the page.</span></span>
9. <span data-ttu-id="b0b02-216">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="b0b02-217">Registruoti sukurtos pirkimo SF su akredityvu tiekėjo mokėjimų žurnalą</span><span class="sxs-lookup"><span data-stu-id="b0b02-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="b0b02-218">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b0b02-219">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-219">Click New.</span></span>
3. <span data-ttu-id="b0b02-220">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="b0b02-221">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b0b02-222">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="b0b02-222">Click Lines.</span></span>
6. <span data-ttu-id="b0b02-223">Lauke Data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="b0b02-224">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b0b02-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="b0b02-225">Spustelėkite „Sudengti operacijas“.</span><span class="sxs-lookup"><span data-stu-id="b0b02-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="b0b02-226">Išplėskite sekciją Bendrosios sumos.</span><span class="sxs-lookup"><span data-stu-id="b0b02-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="b0b02-227">Lauke Rodyti pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="b0b02-228">Patikrinkite, ar atnaujinti laukai Banko dokumento numeris ir Siuntos numeris.</span><span class="sxs-lookup"><span data-stu-id="b0b02-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="b0b02-229">Pažymėkite žymės langelį Žymėti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="b0b02-230">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-230">Click OK.</span></span>
13. <span data-ttu-id="b0b02-231">Spustelėkite skirtuką Mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="b0b02-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="b0b02-232">Patikrinkite, ar atnaujinti laukai Banko dokumento numeris ir Siuntos numeris.</span><span class="sxs-lookup"><span data-stu-id="b0b02-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="b0b02-233">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="b0b02-233">Click Post.</span></span>
15. <span data-ttu-id="b0b02-234">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-234">Close the page.</span></span>
16. <span data-ttu-id="b0b02-235">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="b0b02-236">Tikrinti importo akredityvo būseną po SF apmokėjimo</span><span class="sxs-lookup"><span data-stu-id="b0b02-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="b0b02-237">Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b0b02-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="b0b02-238">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0b02-239">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0b02-240">Patikrinkite importo akredityvo būseną.</span><span class="sxs-lookup"><span data-stu-id="b0b02-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="b0b02-241">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="b0b02-242">Tikrinti banko priemonės limito ir naudojimo ataskaitą</span><span class="sxs-lookup"><span data-stu-id="b0b02-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="b0b02-243">Eikite į Grynųjų pinigų ir banko valdymas > Užklausos ir ataskaitos > Akredityvai arba garantiniai raštai > Banko priemonių ir naudojimo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="b0b02-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="b0b02-244">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="b0b02-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="b0b02-245">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="b0b02-245">Click Filter.</span></span>
    * <span data-ttu-id="b0b02-246">Lauke Kriterijai nurodykite reikiamą banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="b0b02-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="b0b02-247">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0b02-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="b0b02-248">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0b02-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b0b02-249">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-249">Click OK.</span></span>
7. <span data-ttu-id="b0b02-250">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b0b02-250">Click OK.</span></span>
    * <span data-ttu-id="b0b02-251">Patikrinkite ataskaitą, kurioje išvardytos operacijos.</span><span class="sxs-lookup"><span data-stu-id="b0b02-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="b0b02-252">Patikrinkite, ar ataskaitoje išvardijamos operacijos su banko dokumento numeriu, priemonės limitu, panaudota suma ir priemonės balanso suma.</span><span class="sxs-lookup"><span data-stu-id="b0b02-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="b0b02-253">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0b02-253">Close the page.</span></span>

