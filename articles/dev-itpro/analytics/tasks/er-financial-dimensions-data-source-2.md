---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (2 dalis – Modelio susiejimas)
description: Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92efd6a0b36471286c292a80542b81cd14a8eff3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551350"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="14f87-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis: modelio susiejimas)</span><span class="sxs-lookup"><span data-stu-id="14f87-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14f87-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="14f87-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="14f87-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="14f87-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="14f87-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (1 dalis: duomenų modelio kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="14f87-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="14f87-107">Būtinų duomenų šaltinių įtraukimas į modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="14f87-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="14f87-108">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="14f87-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="14f87-109">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="14f87-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="14f87-110">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="14f87-110">Click Designer.</span></span>
4. <span data-ttu-id="14f87-111">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="14f87-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="14f87-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="14f87-112">Click New.</span></span>
6. <span data-ttu-id="14f87-113">Lauke Apibrėžimas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="14f87-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="14f87-114">Lauke Pavadinimas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="14f87-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="14f87-115">Lauke Aprašas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="14f87-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="14f87-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="14f87-116">Click Save.</span></span>
10. <span data-ttu-id="14f87-117">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="14f87-117">Click Designer.</span></span>
11. <span data-ttu-id="14f87-118">Medyje pasirinkite Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="14f87-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="14f87-119">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="14f87-119">Click Add root.</span></span>
13. <span data-ttu-id="14f87-120">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="14f87-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="14f87-121">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="14f87-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="14f87-122">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="14f87-122">Click OK.</span></span>
16. <span data-ttu-id="14f87-123">Medyje pasirinkite Functions\Financial dimensions details.</span><span class="sxs-lookup"><span data-stu-id="14f87-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="14f87-124">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="14f87-124">Click Add root.</span></span>
    * <span data-ttu-id="14f87-125">Šis duomenų šaltinis nurodo, kaip bus apibrėžta kiekvienos ataskaitos, kurioje šis modelis bus naudojamas kaip duomenų šaltinis, finansinių dimensijų apimtis.</span><span class="sxs-lookup"><span data-stu-id="14f87-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="14f87-126">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="14f87-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="14f87-127">Lauke Prašyti dimensijų pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="14f87-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="14f87-128">Pasirinkite Taip, jei norite leisti vartotojui vykdymo metu pasirinkti dimensijas formoje Vartotojo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="14f87-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="14f87-129">Jei pasirinksite NE, visos šio egzemplioriaus finansinės dimensijos bus naudojamas kaip numatytosios.</span><span class="sxs-lookup"><span data-stu-id="14f87-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="14f87-130">Lauke Finansinių dimensijų pasirinkimas pasirinkite Juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="14f87-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="14f87-131">Pasirinkite Visos, jei norite leisti vartotojui pasirinkti norimas dabartinio egzemplioriaus dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="14f87-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="14f87-132">Pasirinkite Juridinis subjektas, jei norite leisti vartotojui pasirinkti įmonės dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="14f87-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="14f87-133">Pasirinkite Dimensija, jei norite leisti vartotojui pasirinkti dimensijas naudojant vieną dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="14f87-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="14f87-134">Lauke Prašyti pagrindinės sąskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="14f87-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="14f87-135">Nustatykite parinktį Prašyti pagrindinės sąskaitos į Taip, kad jei norite leisti vartotojams pasirinkti pagrindinę sąskaitą kaip dimensijų sąrašo dalį.</span><span class="sxs-lookup"><span data-stu-id="14f87-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="14f87-136">Jei pasirinksite Ne, pagrindinė sąskaita nebus įtraukta į dimensijų sąrašą ir parinktis Pagrindinė sąskaita yra privaloma bus įjungta.</span><span class="sxs-lookup"><span data-stu-id="14f87-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="14f87-137">Jei parinktį Pagrindinė sąskaita yra privaloma nustatysite į Taip, įtraukite pagrindinę sąskaitą į dimensijų sąrašą neatsižvelgdami į vartotojo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="14f87-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="14f87-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="14f87-138">Click OK.</span></span>
23. <span data-ttu-id="14f87-139">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="14f87-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="14f87-140">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="14f87-140">Click Add root.</span></span>
25. <span data-ttu-id="14f87-141">Lauke Pavadinimas įveskite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="14f87-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="14f87-142">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="14f87-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="14f87-143">Lauke Lentelė įveskite LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="14f87-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="14f87-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="14f87-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="14f87-145">Duomenų modelio elementų susiejimas su įtrauktais duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="14f87-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="14f87-146">Medyje išplėskite dalį Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="14f87-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="14f87-147">Medyje išplėskite dalį Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="14f87-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="14f87-148">Medyje išplėskite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="14f87-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="14f87-149">Medyje išplėskite dalį Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="14f87-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="14f87-150">Medyje išplėskite dalį LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="14f87-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="14f87-151">Medyje išplėskite LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="14f87-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="14f87-152">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="14f87-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="14f87-153">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="14f87-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="14f87-154">Medyje pasirinkite Journal\Transaction\Voucher.</span><span class="sxs-lookup"><span data-stu-id="14f87-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="14f87-155">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-155">Click Bind.</span></span>
11. <span data-ttu-id="14f87-156">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="14f87-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="14f87-157">Atminkite, kad su bet kokia nuoroda į finansines dimensijas, nustatyta į, pavyzdžiui, LedgerDimension, galima naudoti atitinkamą duomenų šaltinio elementą (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="14f87-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="14f87-158">Šis duomenų šaltinio elementas pateikia finansines dimensijas, kurios nustatytos kaip įrašo sąrašas.</span><span class="sxs-lookup"><span data-stu-id="14f87-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="14f87-159">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="14f87-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="14f87-160">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="14f87-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="14f87-161">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="14f87-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="14f87-162">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="14f87-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="14f87-163">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="14f87-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="14f87-164">Medyje pasirinkite Journal\Transaction\Dimensions data\Name.</span><span class="sxs-lookup"><span data-stu-id="14f87-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="14f87-165">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-165">Click Bind.</span></span>
19. <span data-ttu-id="14f87-166">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="14f87-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="14f87-167">Medyje pasirinkite Journal\Transaction\Dimensions data\Description.</span><span class="sxs-lookup"><span data-stu-id="14f87-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="14f87-168">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-168">Click Bind.</span></span>
22. <span data-ttu-id="14f87-169">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="14f87-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="14f87-170">Medyje pasirinkite Journal\Transaction\Dimensions data\Code.</span><span class="sxs-lookup"><span data-stu-id="14f87-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="14f87-171">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-171">Click Bind.</span></span>
25. <span data-ttu-id="14f87-172">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="14f87-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="14f87-173">Medyje pasirinkite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="14f87-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="14f87-174">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-174">Click Bind.</span></span>
28. <span data-ttu-id="14f87-175">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="14f87-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="14f87-176">Medyje pasirinkite Journal\Transaction\Debit.</span><span class="sxs-lookup"><span data-stu-id="14f87-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="14f87-177">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-177">Click Bind.</span></span>
31. <span data-ttu-id="14f87-178">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="14f87-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="14f87-179">Medyje pasirinkite Journal\Transaction\Date.</span><span class="sxs-lookup"><span data-stu-id="14f87-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="14f87-180">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-180">Click Bind.</span></span>
34. <span data-ttu-id="14f87-181">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="14f87-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="14f87-182">Medyje pasirinkite Journal\Transaction\Currency.</span><span class="sxs-lookup"><span data-stu-id="14f87-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="14f87-183">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-183">Click Bind.</span></span>
37. <span data-ttu-id="14f87-184">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="14f87-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="14f87-185">Medyje pasirinkite Journal\Transaction\Credit.</span><span class="sxs-lookup"><span data-stu-id="14f87-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="14f87-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-186">Click Bind.</span></span>
40. <span data-ttu-id="14f87-187">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="14f87-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="14f87-188">Medyje pasirinkite Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="14f87-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="14f87-189">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-189">Click Bind.</span></span>
43. <span data-ttu-id="14f87-190">Medyje pasirinkite LedgerJournal\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="14f87-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="14f87-191">Medyje pasirinkite Journal\Batch.</span><span class="sxs-lookup"><span data-stu-id="14f87-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="14f87-192">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-192">Click Bind.</span></span>
46. <span data-ttu-id="14f87-193">Medyje pasirinkite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="14f87-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="14f87-194">Medyje pasirinkite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="14f87-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="14f87-195">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-195">Click Bind.</span></span>
49. <span data-ttu-id="14f87-196">Medyje išplėskite dalį Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="14f87-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="14f87-197">Medyje išplėskite dalį Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="14f87-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="14f87-198">Medyje išplėskite dalį Dimensions\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="14f87-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="14f87-199">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="14f87-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="14f87-200">Medyje pasirinkite Dimensions setting\Code.</span><span class="sxs-lookup"><span data-stu-id="14f87-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="14f87-201">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-201">Click Bind.</span></span>
55. <span data-ttu-id="14f87-202">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Report column name.</span><span class="sxs-lookup"><span data-stu-id="14f87-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="14f87-203">Medyje pasirinkite Dimensions setting\Name.</span><span class="sxs-lookup"><span data-stu-id="14f87-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="14f87-204">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-204">Click Bind.</span></span>
58. <span data-ttu-id="14f87-205">Medyje pasirinkite Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="14f87-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="14f87-206">Medyje pasirinkite Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="14f87-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="14f87-207">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="14f87-207">Click Bind.</span></span>
61. <span data-ttu-id="14f87-208">Medyje pasirinkite Įmonė.</span><span class="sxs-lookup"><span data-stu-id="14f87-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="14f87-209">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="14f87-209">Click Edit.</span></span>
63. <span data-ttu-id="14f87-210">Lauke expressionAsStringText įveskite Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="14f87-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="14f87-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="14f87-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="14f87-212">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="14f87-212">Click Save.</span></span>
65. <span data-ttu-id="14f87-213">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="14f87-213">Close the page.</span></span>
66. <span data-ttu-id="14f87-214">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="14f87-214">Click Save.</span></span>
67. <span data-ttu-id="14f87-215">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="14f87-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="14f87-216">Šio modelio versijos juodraščio užbaigimas</span><span class="sxs-lookup"><span data-stu-id="14f87-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="14f87-217">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="14f87-217">Close the page.</span></span>
2. <span data-ttu-id="14f87-218">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="14f87-218">Close the page.</span></span>
3. <span data-ttu-id="14f87-219">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="14f87-219">Click Change status.</span></span>
4. <span data-ttu-id="14f87-220">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="14f87-220">Click Complete.</span></span>
5. <span data-ttu-id="14f87-221">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="14f87-221">Click OK.</span></span>

