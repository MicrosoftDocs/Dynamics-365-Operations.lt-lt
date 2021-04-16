---
title: ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais
description: Šioje temoje aprašoma, kaip susieti elektroninės ataskaitos (ER) duomenų modelį su pasirinktais „Microsoft Dynamics 365 Finance” duomenų šaltiniais.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0eb7f48a50e32637003c1488d80899a704709068
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751491"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="33879-103">ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="33879-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33879-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali susieti elektroninių ataskaitų (ER) duomenų modelį su pasirinktais duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="33879-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="33879-105">Vėliau šis modelio susiejimas bus naudojamas kaip duomenų šaltinis formato konfigūracijoje, kuri bus naudojama elektroninio mokėjimo dokumentams valdyti.</span><span class="sxs-lookup"><span data-stu-id="33879-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="33879-106">Šiame pavyzdyje susiesite pavyzdinės įmonės „Litware, Inc“ duomenų modelį su duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="33879-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="33879-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Pasirinkti modelio susiejimo duomenų šaltinius“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="33879-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="33879-108">Atidaryti ER konfigūracijos medį</span><span class="sxs-lookup"><span data-stu-id="33879-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="33879-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="33879-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="33879-110">Spustelėkite „Konfigūracijos“.</span><span class="sxs-lookup"><span data-stu-id="33879-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="33879-111">Pasirinkti sukurto modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="33879-111">Select created model mapping</span></span>
1. <span data-ttu-id="33879-112">Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.</span><span class="sxs-lookup"><span data-stu-id="33879-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="33879-113">Įsitikinkite, kad modelio konfigūracija „Mokėjimai (supaprastintas modelis)“ buvo sukurta iš anksto.</span><span class="sxs-lookup"><span data-stu-id="33879-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="33879-114">Priešingu atveju tuoj pat sustabdykite ir grįžkite užbaigę užduočių vadovą „Naujos konfigūracijos naudojant pasirinkto domeno duomenų modelį kūrimas”.</span><span class="sxs-lookup"><span data-stu-id="33879-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="33879-115">Spustelėkite „Modelių kūrimo įrankis“.</span><span class="sxs-lookup"><span data-stu-id="33879-115">Click Model designer.</span></span>
3. <span data-ttu-id="33879-116">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="33879-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="33879-117">Pasirinkite įrašą „Kredito pervedimo susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="33879-118">Kreditų pervedimų susiejimas</span><span class="sxs-lookup"><span data-stu-id="33879-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="33879-119">Susieti sukurtus duomenų šaltinius su duomenų modelio elementais</span><span class="sxs-lookup"><span data-stu-id="33879-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="33879-120">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="33879-120">Click Designer.</span></span>
2. <span data-ttu-id="33879-121">Medyje pasirinkite „Apdorojimo data ir laikas (ProcessingDateTime)“.</span><span class="sxs-lookup"><span data-stu-id="33879-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="33879-122">Medyje pasirinkite „Apdorojimo data (ProcessingDateTime)“.</span><span class="sxs-lookup"><span data-stu-id="33879-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="33879-123">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-123">Click Bind.</span></span>
5. <span data-ttu-id="33879-124">Medyje pasirinkite „Mokėjimo pranešimo identifikacija (MessageIdentification)“.</span><span class="sxs-lookup"><span data-stu-id="33879-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="33879-125">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="33879-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="33879-126">Medyje pasirinkite „Operacijos \ Žurnalo numeris (JournalNum)“.</span><span class="sxs-lookup"><span data-stu-id="33879-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="33879-127">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-127">Click Bind.</span></span>
9. <span data-ttu-id="33879-128">Medyje pasirinkite „Mokėjimai“.</span><span class="sxs-lookup"><span data-stu-id="33879-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="33879-129">Medyje pasirinkite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="33879-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="33879-130">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-130">Click Bind.</span></span>
12. <span data-ttu-id="33879-131">Medyje išplėskite „Mokėjimai = Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="33879-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="33879-132">Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius‟.</span><span class="sxs-lookup"><span data-stu-id="33879-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="33879-133">Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="33879-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="33879-134">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ Valiutos kodas (Valiuta)“.</span><span class="sxs-lookup"><span data-stu-id="33879-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="33879-135">Medyje išplėskite „Operacijos \ vendBankAccountInTransactionCompany()“.</span><span class="sxs-lookup"><span data-stu-id="33879-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="33879-136">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Valiuta (CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="33879-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="33879-137">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-137">Click Bind.</span></span>
19. <span data-ttu-id="33879-138">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ IBAN kodas (IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="33879-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="33879-139">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ IBAN (BankIBAN)“.</span><span class="sxs-lookup"><span data-stu-id="33879-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="33879-140">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-140">Click Bind.</span></span>
22. <span data-ttu-id="33879-141">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ Numeris“.</span><span class="sxs-lookup"><span data-stu-id="33879-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="33879-142">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Banko sąskaitos numeris (AccountNum).</span><span class="sxs-lookup"><span data-stu-id="33879-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="33879-143">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-143">Click Bind.</span></span>
25. <span data-ttu-id="33879-144">Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius \ Agentas“.</span><span class="sxs-lookup"><span data-stu-id="33879-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="33879-145">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="33879-146">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="33879-147">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-147">Click Bind.</span></span>
29. <span data-ttu-id="33879-148">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ Banko numeris (RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="33879-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="33879-149">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Banko numeris (RegistrationNum)“.</span><span class="sxs-lookup"><span data-stu-id="33879-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="33879-150">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-150">Click Bind.</span></span>
32. <span data-ttu-id="33879-151">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ SWIFT kodas (SWIFT)“.</span><span class="sxs-lookup"><span data-stu-id="33879-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="33879-152">Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ SWIFT kodas (SWIFTNo)“.</span><span class="sxs-lookup"><span data-stu-id="33879-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="33879-153">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-153">Click Bind.</span></span>
35. <span data-ttu-id="33879-154">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="33879-155">Medyje išplėskite „Operacijos \ findVendTable()“.</span><span class="sxs-lookup"><span data-stu-id="33879-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="33879-156">Medyje pasirinkite „Operacijos \ findVendTable()\name()“.</span><span class="sxs-lookup"><span data-stu-id="33879-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="33879-157">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-157">Click Bind.</span></span>
39. <span data-ttu-id="33879-158">Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Valiutos kodas (Valiuta)“.</span><span class="sxs-lookup"><span data-stu-id="33879-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="33879-159">Medyje išplėskite Transactions\>Relations.</span><span class="sxs-lookup"><span data-stu-id="33879-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="33879-160">Medyje išplėskite Transactions\>Relations\Currency table(Currency).</span><span class="sxs-lookup"><span data-stu-id="33879-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="33879-161">Medyje pasirinkite Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).</span><span class="sxs-lookup"><span data-stu-id="33879-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="33879-162">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-162">Click Bind.</span></span>
44. <span data-ttu-id="33879-163">Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas“.</span><span class="sxs-lookup"><span data-stu-id="33879-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="33879-164">Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="33879-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="33879-165">Medyje pasirinkite „Mokėjimai = Operacijos \ Debitorius \ Sąskaita \ Valiutos kodas (Valiuta)“.</span><span class="sxs-lookup"><span data-stu-id="33879-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="33879-166">Medyje pasirinkite „Banko sąskaita (BankAccount)“.</span><span class="sxs-lookup"><span data-stu-id="33879-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="33879-167">Medyje išplėskite „Banko sąskaita (BankAccount)“.</span><span class="sxs-lookup"><span data-stu-id="33879-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="33879-168">Medyje pasirinkite „Banko sąskaita (BankAccount) \ Valiuta (CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="33879-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="33879-169">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-169">Click Bind.</span></span>
51. <span data-ttu-id="33879-170">Medyje pasirinkite „Banko sąskaita (BankAccount) \ IBAN“.</span><span class="sxs-lookup"><span data-stu-id="33879-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="33879-171">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita \ IBAN kodas (IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="33879-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="33879-172">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-172">Click Bind.</span></span>
54. <span data-ttu-id="33879-173">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita \ Numeris“.</span><span class="sxs-lookup"><span data-stu-id="33879-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="33879-174">Medyje pasirinkite „Banko sąskaitą (BankAccount) \ Bank sąskaitos numeris (AccountNum)“.</span><span class="sxs-lookup"><span data-stu-id="33879-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="33879-175">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-175">Click Bind.</span></span>
57. <span data-ttu-id="33879-176">Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas \ Agentas‟.</span><span class="sxs-lookup"><span data-stu-id="33879-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="33879-177">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="33879-178">Medyje pasirinkite „Banko sąskaita (BankAccount) \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="33879-179">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-179">Click Bind.</span></span>
61. <span data-ttu-id="33879-180">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ Banko numeris (RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="33879-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="33879-181">Medyje pasirinkite „Banko sąskaitą (BankAccount) \ Bank numeris (RegistrationNum)“.</span><span class="sxs-lookup"><span data-stu-id="33879-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="33879-182">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-182">Click Bind.</span></span>
64. <span data-ttu-id="33879-183">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ SWIFT kodas (SWIFT)“.</span><span class="sxs-lookup"><span data-stu-id="33879-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="33879-184">Medyje pasirinkite „Banko sąskaita (BankAccount) \ SWIFT kodas (SWIFTNo)“.</span><span class="sxs-lookup"><span data-stu-id="33879-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="33879-185">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-185">Click Bind.</span></span>
67. <span data-ttu-id="33879-186">Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="33879-187">Medyje pasirinkite „Įmonės informacija (Įmonė)“.</span><span class="sxs-lookup"><span data-stu-id="33879-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="33879-188">Medyje išplėskite „Įmonės informacija (Įmonė)“.</span><span class="sxs-lookup"><span data-stu-id="33879-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="33879-189">Medyje pasirinkite „Įmonės informacija (Įmonė) \ Pavadinimas“.</span><span class="sxs-lookup"><span data-stu-id="33879-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="33879-190">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-190">Click Bind.</span></span>
72. <span data-ttu-id="33879-191">Medyje pasirinkite „Mokėjimai = Operacijos \ Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="33879-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="33879-192">Medyje pasirinkite „Operacijos \ Aprašas (Txt)“.</span><span class="sxs-lookup"><span data-stu-id="33879-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="33879-193">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-193">Click Bind.</span></span>
75. <span data-ttu-id="33879-194">Medyje pasirinkite „Mokėjimai = Operacijos \ Tiesioginės identifikacijos kodas (End2EndID)“.</span><span class="sxs-lookup"><span data-stu-id="33879-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="33879-195">Medyje pasirinkite Transactions\$EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="33879-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="33879-196">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-196">Click Bind.</span></span>
78. <span data-ttu-id="33879-197">Medyje pasirinkite „Mokėjimai = Operacijos \ Nurodyta suma (InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="33879-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="33879-198">Medyje pasirinkite „Transactions\$Amount“.</span><span class="sxs-lookup"><span data-stu-id="33879-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="33879-199">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-199">Click Bind.</span></span>
81. <span data-ttu-id="33879-200">Medyje pasirinkite „Mokėjimai = Operacijos \ Operacijos data (TransactionDate)“.</span><span class="sxs-lookup"><span data-stu-id="33879-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="33879-201">Medyje pasirinkite „Operacijos \ Data (TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="33879-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="33879-202">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="33879-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="33879-203">Tikrinti sukurtą susiejimą</span><span class="sxs-lookup"><span data-stu-id="33879-203">Validate created mapping</span></span>
1. <span data-ttu-id="33879-204">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="33879-204">Click Validate.</span></span>
    * <span data-ttu-id="33879-205">Norėdami įsitikinti, kad visi susiejimai veikia gerai, patikrinkite naują susiejimą.</span><span class="sxs-lookup"><span data-stu-id="33879-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="33879-206">Spustelėdami rodyklę išplėskite arba sutraukite sekciją Klaidų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="33879-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="33879-207">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="33879-207">Click Save.</span></span>
4. <span data-ttu-id="33879-208">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="33879-208">Close the page.</span></span>
5. <span data-ttu-id="33879-209">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="33879-209">Close the page.</span></span>
6. <span data-ttu-id="33879-210">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="33879-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="33879-211">Pakeisti esamos modelio konfigūracijos versijos būseną</span><span class="sxs-lookup"><span data-stu-id="33879-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="33879-212">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="33879-212">Click Change status.</span></span>
    * <span data-ttu-id="33879-213">Pakeiskite sukurtos modelio konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti kuriant mokėjimo formatus.</span><span class="sxs-lookup"><span data-stu-id="33879-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="33879-214">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="33879-214">Click Complete.</span></span>
    * <span data-ttu-id="33879-215">Pasirinkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="33879-215">Select Complete.</span></span>  
3. <span data-ttu-id="33879-216">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="33879-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="33879-217">Pavyzdžiui, „1 versija“.</span><span class="sxs-lookup"><span data-stu-id="33879-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="33879-218">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="33879-218">Click OK.</span></span>
5. <span data-ttu-id="33879-219">Pasirinkite baigtą esamos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="33879-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="33879-220">Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.</span><span class="sxs-lookup"><span data-stu-id="33879-220">Note that the created configuration is saved as completed version 1.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]