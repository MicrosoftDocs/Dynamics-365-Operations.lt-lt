--- 
title: "Eksportuoti akredityvą"
description: "Ši procedūra padeda eksportuoti akredityvą."
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="export-letter-of-credit"></a><span data-ttu-id="f4fea-103">Eksportuoti akredityvą</span><span class="sxs-lookup"><span data-stu-id="f4fea-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4fea-104">Ši procedūra padeda eksportuoti akredityvą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="f4fea-105">Akredityvas yra banko išduota sutartis, pagal kurią bankas sutinka užtikrinti mokėjimą pirkėjo vardu, jei sutarties tarp pirkėjo ir pardavėjo sąlygos yra patenkinamos.</span><span class="sxs-lookup"><span data-stu-id="f4fea-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="f4fea-106">Prieš šią procedūrą atlikite procedūras „Banko priemonių ir registravimo šablonų nustatymas“ ir „Akredityvo banko priemonės sutarties kūrimas“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="f4fea-107">Reikia pasirinkti demonstracinę įmonę USMF, kad būtų galima sėkmingai atlikti šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="f4fea-108">Kurti eksporto akredityvo pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="f4fea-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="f4fea-109">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="f4fea-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f4fea-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-110">Click New.</span></span>
3. <span data-ttu-id="f4fea-111">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f4fea-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f4fea-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4fea-114">Išplėskite arba sutraukite dalį Bendra.</span><span class="sxs-lookup"><span data-stu-id="f4fea-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="f4fea-115">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4fea-116">Pasirinkite teritoriją, kurioje saugoma išduotina prekė.</span><span class="sxs-lookup"><span data-stu-id="f4fea-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="f4fea-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f4fea-118">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4fea-119">Pasirinkite sandėlį, kuriame saugoma išduotina prekė.</span><span class="sxs-lookup"><span data-stu-id="f4fea-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="f4fea-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4fea-121">Pastaba: turi būti pasirinkta lauko Banko dokumento tipas reikšmė „Akredityvas“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="f4fea-122">Lauke Banko dokumento tipas pasirinkite „Akredityvas“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="f4fea-123">Išplėskite arba sutraukite sekciją Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="f4fea-124">Pasirinkite Pristatymo datos valdymas = Nėra.</span><span class="sxs-lookup"><span data-stu-id="f4fea-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="f4fea-125">Lauke Pageidaujama gavimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="f4fea-126">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-126">Click OK.</span></span>
15. <span data-ttu-id="f4fea-127">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f4fea-128">Pasirinkite prekę, kurią reikia išduoti / parduoti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="f4fea-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f4fea-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f4fea-131">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f4fea-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="f4fea-132">Išplėskite arba sutraukite dalį Išsami eilučių informacija.</span><span class="sxs-lookup"><span data-stu-id="f4fea-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="f4fea-133">Spustelėkite skirtuką Pristatymas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="f4fea-134">Lauke Pageidaujama siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="f4fea-135">Lauke Patvirtinta siuntimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="f4fea-136">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="f4fea-137">Spustelėkite Akredityvas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="f4fea-138">Lauke Banko dokumento numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f4fea-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="f4fea-139">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="f4fea-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="f4fea-140">Išplėskite arba sutraukite sekciją Banko informacija.</span><span class="sxs-lookup"><span data-stu-id="f4fea-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="f4fea-141">Lauke Išduodantis bankas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="f4fea-142">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="f4fea-143">Lauke Konsultavimo bankas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="f4fea-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="f4fea-145">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="f4fea-146">Spustelėkite Surasti pardavimo užsakymo siuntas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="f4fea-147">Spustelėkite Išduodančio banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="f4fea-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="f4fea-149">Registruoti važtaraštį</span><span class="sxs-lookup"><span data-stu-id="f4fea-149">Post Packing slip</span></span>
1. <span data-ttu-id="f4fea-150">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="f4fea-151">Spustelėkite Registruoti važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="f4fea-152">Išplėskite arba sutraukite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="f4fea-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="f4fea-153">Lauke Kiekis pasirinkite „Visi‟.</span><span class="sxs-lookup"><span data-stu-id="f4fea-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="f4fea-154">Išplėskite arba sutraukite sekciją Sąranka.</span><span class="sxs-lookup"><span data-stu-id="f4fea-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="f4fea-155">Lauke Važtaraščio data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="f4fea-156">Pasirinkite siuntos numerį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="f4fea-157">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f4fea-158">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-158">Click OK.</span></span>
10. <span data-ttu-id="f4fea-159">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="f4fea-160">Registruoti pardavimo SF</span><span class="sxs-lookup"><span data-stu-id="f4fea-160">Post sales invoice</span></span>
1. <span data-ttu-id="f4fea-161">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="f4fea-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f4fea-162">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="f4fea-162">Click Invoice.</span></span>
3. <span data-ttu-id="f4fea-163">Išplėskite arba sutraukite sekciją Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="f4fea-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="f4fea-164">Pasirinkite siuntos numerį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="f4fea-165">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4fea-166">Išplėskite arba sutraukite sekciją Sąranka.</span><span class="sxs-lookup"><span data-stu-id="f4fea-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="f4fea-167">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="f4fea-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="f4fea-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-168">Click OK.</span></span>
9. <span data-ttu-id="f4fea-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="f4fea-170">Pateikto siuntos dokumento būsena</span><span class="sxs-lookup"><span data-stu-id="f4fea-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="f4fea-171">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="f4fea-172">Spustelėkite Akredityvas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="f4fea-173">Išplėskite arba sutraukite sekciją Eilutės.</span><span class="sxs-lookup"><span data-stu-id="f4fea-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="f4fea-174">Pastaba: lauko „Dokumentas pateiktas“ reikšmė turi būti nustatyta kaip „Taip“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="f4fea-175">Tikrinti eksporto akredityvą</span><span class="sxs-lookup"><span data-stu-id="f4fea-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="f4fea-176">Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Eksportuoti akredityvą ir importuoti rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="f4fea-177">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f4fea-178">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4fea-179">Patikrinkite, ar eksporto akredityvo siuntos būsena yra „SF išrašyta“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="f4fea-180">Kliento mokėjimas</span><span class="sxs-lookup"><span data-stu-id="f4fea-180">Customer payment</span></span>
1. <span data-ttu-id="f4fea-181">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f4fea-182">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-182">Click New.</span></span>
3. <span data-ttu-id="f4fea-183">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f4fea-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f4fea-184">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f4fea-185">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f4fea-186">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="f4fea-186">Click Lines.</span></span>
7. <span data-ttu-id="f4fea-187">Lauke Data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="f4fea-188">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f4fea-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="f4fea-189">Spustelėkite Atsiskaitymas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-189">Click Settlement.</span></span>
10. <span data-ttu-id="f4fea-190">Antraštėje Bendrosios sumos pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="f4fea-191">Pastaba: nustatykite lauko Rodyti reikšmę kaip „Akredityvas“.</span><span class="sxs-lookup"><span data-stu-id="f4fea-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="f4fea-192">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f4fea-193">Pažymėkite arba išvalykite žymės langelį Žymėti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="f4fea-194">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f4fea-194">Click OK.</span></span>
14. <span data-ttu-id="f4fea-195">Spustelėkite skirtuką Mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="f4fea-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="f4fea-196">Tikrinti banko dokumento numerio ir siuntos numerio informaciją</span><span class="sxs-lookup"><span data-stu-id="f4fea-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="f4fea-197">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="f4fea-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="f4fea-198">Tikrinti eksporto akredityvą po apmokėjimo</span><span class="sxs-lookup"><span data-stu-id="f4fea-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="f4fea-199">Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Eksportuoti akredityvą ir importuoti rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f4fea-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="f4fea-200">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f4fea-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f4fea-201">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f4fea-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4fea-202">Patikrinkite, ar siuntos būsena = mokėjimas gautas, o balanso suma = 0,00.</span><span class="sxs-lookup"><span data-stu-id="f4fea-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


