---
title: ER modelio susiejimų nustatymas ir jų duomenų šaltinių pasirinkimas
description: Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjas gali pažymėti elektroninių ataskaitų duomenų modelio duomenų šaltinius.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b5f291372bc459bc1979dca4a95cfafb39e2ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567299"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="b15d0-103">ER modelio susiejimų nustatymas ir jų duomenų šaltinių pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="b15d0-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b15d0-104">Tolesniais veiksmais paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali pažymėti elektroninių ataskaitų (ER) duomenų modelio duomenų šaltinius.</span><span class="sxs-lookup"><span data-stu-id="b15d0-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="b15d0-105">Duomenų šaltiniai bus susieti su atskirais pasirinkto duomenų modelio komponentais kūrimo metu ir automatiškai įves verslo duomenis į tą duomenų modelį vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="b15d0-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="b15d0-106">Šiame pavyzdyje pasirinksite esamo duomenų modelio, sukurto pavyzdinei įmonei „Litware, Inc.“, duomenų šaltinius. Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Kurti naują duomenų modelį“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b15d0-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="b15d0-107">Atidaryti elektroninių ataskaitų konfigūracijų medį</span><span class="sxs-lookup"><span data-stu-id="b15d0-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="b15d0-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="b15d0-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b15d0-109">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="b15d0-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="b15d0-110">Įterpti naują modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="b15d0-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="b15d0-111">Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="b15d0-112">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="b15d0-112">Click Designer.</span></span>
3. <span data-ttu-id="b15d0-113">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="b15d0-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b15d0-114">Click New.</span></span>
    * <span data-ttu-id="b15d0-115">Taip sukursite naują įrašą, kuris susies duomenų modelį su duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="b15d0-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="b15d0-116">Šiame pavyzdyje susiesite duomenų modelį su norimo mokėjimo tipo (kredito pervedimas) duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="b15d0-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="b15d0-117">Galima sukurti daugiau nei vieną konkretaus duomenų modelio susiejimą.</span><span class="sxs-lookup"><span data-stu-id="b15d0-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="b15d0-118">Pvz., galite sukurti skirtingų tipų mokėjimų, pvz., tiesioginio debeto arba kredito pervedimų, susiejimą.</span><span class="sxs-lookup"><span data-stu-id="b15d0-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="b15d0-119">Šiame pavyzdyje sukursite kredito pervedimų susiejimą.</span><span class="sxs-lookup"><span data-stu-id="b15d0-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="b15d0-120">Lauke „Pavadinimas“ įveskite „CT susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="b15d0-121">Kreditų pervedimų susiejimas</span><span class="sxs-lookup"><span data-stu-id="b15d0-121">CT mapping</span></span>  
6. <span data-ttu-id="b15d0-122">Lauke „Aprašas“ įveskite „Mokėjimo modelio CT susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="b15d0-123">Kreditų pervedimų mokėjimo modelio susiejimas</span><span class="sxs-lookup"><span data-stu-id="b15d0-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="b15d0-124">Lauke „Aprašas“ įveskite „CustomerCreditTransferInitiation“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b15d0-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="b15d0-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="b15d0-126">ResolveChanges – aprašas.</span><span class="sxs-lookup"><span data-stu-id="b15d0-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="b15d0-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="b15d0-128">Nurodyti reikiamus esamo modelio susiejimo duomenų šaltinius</span><span class="sxs-lookup"><span data-stu-id="b15d0-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="b15d0-129">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="b15d0-129">Click Designer.</span></span>
2. <span data-ttu-id="b15d0-130">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="b15d0-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="b15d0-131">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-131">Click Add root.</span></span>
    * <span data-ttu-id="b15d0-132">Įveskite šį duomenų šaltinį, kad pasiektumėte mokėjimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="b15d0-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="b15d0-133">Lauke „Pavadinimas“, įveskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b15d0-134">Operacijos</span><span class="sxs-lookup"><span data-stu-id="b15d0-134">Transactions</span></span>  
5. <span data-ttu-id="b15d0-135">Lauke „Žyma“ įveskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="b15d0-136">Operacijos</span><span class="sxs-lookup"><span data-stu-id="b15d0-136">Transactions</span></span>  
6. <span data-ttu-id="b15d0-137">Lauke „Žinynas“ įveskite „Didžiosios knygos žurnalo eilutės“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="b15d0-138">Didžiosios knygos žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="b15d0-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="b15d0-139">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b15d0-140">Pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-140">Select Yes.</span></span>  
8. <span data-ttu-id="b15d0-141">Lauke „Lentelė“, įveskite „LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="b15d0-142">LedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="b15d0-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="b15d0-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-143">Click OK.</span></span>
    * <span data-ttu-id="b15d0-144">Pasirinkite lentelę „LedgerJournalTrans“ kaip esamo duomenų modelio duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="b15d0-145">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b15d0-146">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-146">Click Add.</span></span>
    * <span data-ttu-id="b15d0-147">Spustelėkite „Įtraukti“, kad įtrauktumėte naują apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="b15d0-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="b15d0-148">Lauke „Pavadinimas“ įveskite „$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="b15d0-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="b15d0-149">$EndToEndID</span></span>  
13. <span data-ttu-id="b15d0-150">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-150">Click Edit formula.</span></span>
14. <span data-ttu-id="b15d0-151">Medyje pasirinkite „Eilutė \ SUJUNGTI“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="b15d0-152">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-152">Click Add function.</span></span>
16. <span data-ttu-id="b15d0-153">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="b15d0-154">Medyje pasirinkite „Operacijos \ Kvitas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="b15d0-155">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-155">Click Add data source.</span></span>
19. <span data-ttu-id="b15d0-156">Lauke „Formulė“ įveskite „CONCATENATE(Transactions.Voucher, "-", “.</span><span class="sxs-lookup"><span data-stu-id="b15d0-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="b15d0-157">Įveskite [, "–",] formulės pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="b15d0-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="b15d0-158">Medyje pasirinkite „Eilutė \ TEKSTAS“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="b15d0-159">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-159">Click Add function.</span></span>
22. <span data-ttu-id="b15d0-160">Medyje pasirinkite „Operacijos \ Įrašo ID (RecId)“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="b15d0-161">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-161">Click Add data source.</span></span>
24. <span data-ttu-id="b15d0-162">Lauke „Formulė“ įveskite „CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="b15d0-163">Įveskite [))] formulės pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="b15d0-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="b15d0-164">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-164">Click Save.</span></span>
    * <span data-ttu-id="b15d0-165">Įsitikinkite, ar neaptikta sukurtos formulės klaidų.</span><span class="sxs-lookup"><span data-stu-id="b15d0-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="b15d0-166">Peržiūrėkite skirtuką KLAIDOS, esantį po formulės redaktorius valdikliu.</span><span class="sxs-lookup"><span data-stu-id="b15d0-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="b15d0-167">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-167">Close the page.</span></span>
27. <span data-ttu-id="b15d0-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-168">Click OK.</span></span>
    * <span data-ttu-id="b15d0-169">Įtraukite apskaičiuotą lauką į šį duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="b15d0-170">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-170">Click Add.</span></span>
    * <span data-ttu-id="b15d0-171">Spustelėkite „Įtraukti“, kad įtrauktumėte naują apskaičiuotą lauką.</span><span class="sxs-lookup"><span data-stu-id="b15d0-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="b15d0-172">Lauke „Pavadinimas“ įveskite „$Suma“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="b15d0-173">$Suma</span><span class="sxs-lookup"><span data-stu-id="b15d0-173">$Amount</span></span>  
30. <span data-ttu-id="b15d0-174">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-174">Click Edit formula.</span></span>
31. <span data-ttu-id="b15d0-175">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="b15d0-176">Medyje pasirinkite „Operacijos \ Debetas (AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="b15d0-177">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-177">Click Add data source.</span></span>
34. <span data-ttu-id="b15d0-178">Lauke „Formulė“ įveskite „Transactions.AmountCurDebit - ”.</span><span class="sxs-lookup"><span data-stu-id="b15d0-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="b15d0-179">Įveskite [ - ] formulės pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="b15d0-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="b15d0-180">Medyje pasirinkite „Operacijos \ Kreditas (AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="b15d0-181">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-181">Click Add data source.</span></span>
37. <span data-ttu-id="b15d0-182">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-182">Click Save.</span></span>
38. <span data-ttu-id="b15d0-183">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-183">Close the page.</span></span>
39. <span data-ttu-id="b15d0-184">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-184">Click OK.</span></span>
    * <span data-ttu-id="b15d0-185">Tai įtrauks apskaičiuotą lauką „$Suma“ į pasirinktą esamo duomenų modelio duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="b15d0-186">Medyje pasirinkite „Transactions\$Amount“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="b15d0-187">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b15d0-188">Medyje išplėskite arba sutraukite „Transactions\$Amount”.</span><span class="sxs-lookup"><span data-stu-id="b15d0-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="b15d0-189">Medyje išplėskite arba sutraukite „Operacijos”.</span><span class="sxs-lookup"><span data-stu-id="b15d0-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="b15d0-190">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="b15d0-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="b15d0-191">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-191">Click Add root.</span></span>
    * <span data-ttu-id="b15d0-192">Įveskite šį duomenų šaltinį, kad pasiektumėte įmonės banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="b15d0-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="b15d0-193">Lauke „Pavadinimas“ įveskite „BankAccount“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="b15d0-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="b15d0-194">BankAccount</span></span>  
47. <span data-ttu-id="b15d0-195">Lauke „Žyma“ įveskite „Banko sąskaita“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b15d0-196">Banko kodas</span><span class="sxs-lookup"><span data-stu-id="b15d0-196">Bank Account</span></span>  
48. <span data-ttu-id="b15d0-197">Lauke „Žinynas“ įveskite „Banko sąskaita“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b15d0-198">Banko kodas</span><span class="sxs-lookup"><span data-stu-id="b15d0-198">Bank Account</span></span>  
49. <span data-ttu-id="b15d0-199">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b15d0-200">Pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-200">Select Yes.</span></span>  
50. <span data-ttu-id="b15d0-201">Lauke „Lentelė“, įveskite „BankAccountTable“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="b15d0-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="b15d0-202">BankAccountTable</span></span>  
51. <span data-ttu-id="b15d0-203">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-203">Click OK.</span></span>
    * <span data-ttu-id="b15d0-204">Pasirinkite lentelę „BankAccountTable“ kaip esamo duomenų modelio duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="b15d0-205">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-205">Click Add root.</span></span>
    * <span data-ttu-id="b15d0-206">Įveskite šį duomenų šaltinį, kad pasiektumėte įmonės rekvizitus.</span><span class="sxs-lookup"><span data-stu-id="b15d0-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="b15d0-207">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="b15d0-208">Įmonė</span><span class="sxs-lookup"><span data-stu-id="b15d0-208">Company</span></span>  
54. <span data-ttu-id="b15d0-209">Lauke „Žyma“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b15d0-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="b15d0-210">Informacija apie įmonę</span><span class="sxs-lookup"><span data-stu-id="b15d0-210">Company information</span></span>  
55. <span data-ttu-id="b15d0-211">Lauke „Žinynas“ įveskite „Įmonės informacija“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="b15d0-212">Informacija apie įmonę</span><span class="sxs-lookup"><span data-stu-id="b15d0-212">Company information</span></span>  
56. <span data-ttu-id="b15d0-213">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b15d0-214">Pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-214">Select Yes.</span></span>  
57. <span data-ttu-id="b15d0-215">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="b15d0-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="b15d0-216">CompanyInfo</span></span>  
58. <span data-ttu-id="b15d0-217">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-217">Click OK.</span></span>
    * <span data-ttu-id="b15d0-218">Pasirinkite lentelę „CompanyInfo“ kaip esamo duomenų modelio duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="b15d0-219">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="b15d0-220">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-220">Click Add root.</span></span>
    * <span data-ttu-id="b15d0-221">Įtraukite apskaičiuotą lauką kaip naują duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="b15d0-222">Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="b15d0-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="b15d0-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="b15d0-224">Lauke Žyma įveskite „Apdorojimo data ir laikas“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="b15d0-225">Apdorojimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="b15d0-225">Processing date & time</span></span>  
63. <span data-ttu-id="b15d0-226">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-226">Click Edit formula.</span></span>
64. <span data-ttu-id="b15d0-227">Medyje pasirinkite „Data / laikas \ SESSIONNOW”.</span><span class="sxs-lookup"><span data-stu-id="b15d0-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="b15d0-228">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="b15d0-228">Click Add function.</span></span>
66. <span data-ttu-id="b15d0-229">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-229">Click Save.</span></span>
67. <span data-ttu-id="b15d0-230">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-230">Close the page.</span></span>
68. <span data-ttu-id="b15d0-231">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b15d0-231">Click OK.</span></span>
    * <span data-ttu-id="b15d0-232">Įtraukite apskaičiuotą lauką „ProcessingDateTime“ kaip esamo duomenų modelio duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="b15d0-233">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b15d0-233">Click Save.</span></span>
70. <span data-ttu-id="b15d0-234">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-234">Close the page.</span></span>
71. <span data-ttu-id="b15d0-235">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-235">Close the page.</span></span>
72. <span data-ttu-id="b15d0-236">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b15d0-236">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]