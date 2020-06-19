---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (2 dalis – Modelio susiejimas)
description: Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: 3aabd622d15917d7e4549d0b0679aa20231c5815
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406525"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="ca902-103">ER naudoti finansines dimensijas kaip duomenų šaltinį (2 dalis – Modelio susiejimas)</span><span class="sxs-lookup"><span data-stu-id="ca902-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca902-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="ca902-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ca902-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="ca902-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ca902-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (1 dalis. Duomenų modelio kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="ca902-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="ca902-107">Būtinų duomenų šaltinių įtraukimas į modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="ca902-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="ca902-108">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ca902-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ca902-109">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ca902-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ca902-110">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="ca902-110">Click Designer.</span></span>
4. <span data-ttu-id="ca902-111">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="ca902-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="ca902-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca902-112">Click New.</span></span>
6. <span data-ttu-id="ca902-113">Lauke Apibrėžimas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="ca902-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="ca902-114">Lauke Pavadinimas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="ca902-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="ca902-115">Lauke Aprašas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="ca902-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="ca902-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca902-116">Click Save.</span></span>
10. <span data-ttu-id="ca902-117">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="ca902-117">Click Designer.</span></span>
11. <span data-ttu-id="ca902-118">Medyje pasirinkite Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="ca902-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="ca902-119">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="ca902-119">Click Add root.</span></span>
13. <span data-ttu-id="ca902-120">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="ca902-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="ca902-121">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="ca902-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="ca902-122">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="ca902-122">Click OK.</span></span>
16. <span data-ttu-id="ca902-123">Medyje pasirinkite Functions\Financial dimensions details.</span><span class="sxs-lookup"><span data-stu-id="ca902-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="ca902-124">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="ca902-124">Click Add root.</span></span>
    * <span data-ttu-id="ca902-125">Šis duomenų šaltinis nurodo, kaip bus apibrėžta kiekvienos ataskaitos, kurioje šis modelis bus naudojamas kaip duomenų šaltinis, finansinių dimensijų apimtis.</span><span class="sxs-lookup"><span data-stu-id="ca902-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="ca902-126">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca902-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="ca902-127">Lauke Prašyti dimensijų pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ca902-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="ca902-128">Pasirinkite Taip, jei norite leisti vartotojui vykdymo metu pasirinkti dimensijas formoje Vartotojo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="ca902-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="ca902-129">Jei pasirinksite NE, visos šio egzemplioriaus finansinės dimensijos bus naudojamas kaip numatytosios.</span><span class="sxs-lookup"><span data-stu-id="ca902-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="ca902-130">Lauke Finansinių dimensijų pasirinkimas pasirinkite Juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="ca902-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="ca902-131">Pasirinkite Visos, jei norite leisti vartotojui pasirinkti norimas dabartinio egzemplioriaus dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="ca902-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="ca902-132">Pasirinkite Juridinis subjektas, jei norite leisti vartotojui pasirinkti įmonės dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="ca902-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="ca902-133">Pasirinkite Dimensija, jei norite leisti vartotojui pasirinkti dimensijas naudojant vieną dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ca902-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="ca902-134">Lauke Prašyti pagrindinės sąskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ca902-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="ca902-135">Nustatykite parinktį „Prašyti pagrindinės sąskaitos“ į Taip, kad leistumėte vartotojams pasirinkti pagrindinę sąskaitą kaip dimensijų sąrašo dalį.</span><span class="sxs-lookup"><span data-stu-id="ca902-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="ca902-136">Jei pasirinksite Ne, pagrindinė sąskaita nebus įtraukta į dimensijų sąrašą ir parinktis „Ar pagrindinė sąskaita yra privaloma“ bus įjungta.</span><span class="sxs-lookup"><span data-stu-id="ca902-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="ca902-137">Jei parinktį „Ar pagrindinė sąskaita yra privaloma“ yra nustatyta į Taip, įtraukite pagrindinę sąskaitą į dimensijų sąrašą neatsižvelgdami į vartotojo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="ca902-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="ca902-138">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="ca902-138">Click OK.</span></span>
<span data-ttu-id="ca902-139">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="ca902-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="ca902-140">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="ca902-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="ca902-141">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="ca902-141">Click Add root.</span></span>
25. <span data-ttu-id="ca902-142">Lauke Pavadinimas įveskite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="ca902-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="ca902-143">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="ca902-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="ca902-144">Lauke Lentelė įveskite LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="ca902-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="ca902-145">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="ca902-145">Click OK.</span></span>
<span data-ttu-id="ca902-146">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="ca902-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="ca902-147">Duomenų modelio elementų susiejimas su įtrauktais duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="ca902-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="ca902-148">Medyje išplėskite dalį Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="ca902-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="ca902-149">Medyje išplėskite dalį Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="ca902-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="ca902-150">Medyje išplėskite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="ca902-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="ca902-151">Medyje išplėskite dalį Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="ca902-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="ca902-152">Medyje išplėskite dalį LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="ca902-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="ca902-153">Medyje išplėskite LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="ca902-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="ca902-154">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="ca902-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="ca902-155">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="ca902-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="ca902-156">Medyje pasirinkite Journal\Transaction\Voucher.</span><span class="sxs-lookup"><span data-stu-id="ca902-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="ca902-157">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-157">Click Bind.</span></span>
11. <span data-ttu-id="ca902-158">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="ca902-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="ca902-159">Atminkite, kad su bet kokia nuoroda į finansines dimensijas, nustatyta į, pavyzdžiui, LedgerDimension, galima naudoti atitinkamą duomenų šaltinio elementą (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="ca902-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="ca902-160">Šis duomenų šaltinio elementas pateikia finansines dimensijas, kurios nustatytos kaip įrašo sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ca902-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="ca902-161">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="ca902-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="ca902-162">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="ca902-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="ca902-163">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="ca902-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="ca902-164">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="ca902-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="ca902-165">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="ca902-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="ca902-166">Medyje pasirinkite Journal\Transaction\Dimensions data\Name.</span><span class="sxs-lookup"><span data-stu-id="ca902-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="ca902-167">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-167">Click Bind.</span></span>
19. <span data-ttu-id="ca902-168">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="ca902-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="ca902-169">Medyje pasirinkite Journal\Transaction\Dimensions data\Description.</span><span class="sxs-lookup"><span data-stu-id="ca902-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="ca902-170">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-170">Click Bind.</span></span>
22. <span data-ttu-id="ca902-171">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="ca902-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="ca902-172">Medyje pasirinkite Journal\Transaction\Dimensions data\Code.</span><span class="sxs-lookup"><span data-stu-id="ca902-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="ca902-173">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-173">Click Bind.</span></span>
25. <span data-ttu-id="ca902-174">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="ca902-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="ca902-175">Medyje pasirinkite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="ca902-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="ca902-176">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-176">Click Bind.</span></span>
<span data-ttu-id="ca902-177">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="ca902-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="ca902-178">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="ca902-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="ca902-179">Medyje pasirinkite Journal\Transaction\Debit.</span><span class="sxs-lookup"><span data-stu-id="ca902-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="ca902-180">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-180">Click Bind.</span></span>
31. <span data-ttu-id="ca902-181">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="ca902-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="ca902-182">Medyje pasirinkite Journal\Transaction\Date.</span><span class="sxs-lookup"><span data-stu-id="ca902-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="ca902-183">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-183">Click Bind.</span></span>
34. <span data-ttu-id="ca902-184">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="ca902-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="ca902-185">Medyje pasirinkite Journal\Transaction\Currency.</span><span class="sxs-lookup"><span data-stu-id="ca902-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="ca902-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-186">Click Bind.</span></span>
37. <span data-ttu-id="ca902-187">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="ca902-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="ca902-188">Medyje pasirinkite Journal\Transaction\Credit.</span><span class="sxs-lookup"><span data-stu-id="ca902-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="ca902-189">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-189">Click Bind.</span></span>
40. <span data-ttu-id="ca902-190">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="ca902-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="ca902-191">Medyje pasirinkite Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="ca902-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="ca902-192">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-192">Click Bind.</span></span>
43. <span data-ttu-id="ca902-193">Medyje pasirinkite LedgerJournal\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="ca902-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="ca902-194">Medyje pasirinkite Journal\Batch.</span><span class="sxs-lookup"><span data-stu-id="ca902-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="ca902-195">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-195">Click Bind.</span></span>
46. <span data-ttu-id="ca902-196">Medyje pasirinkite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="ca902-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="ca902-197">Medyje pasirinkite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="ca902-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="ca902-198">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-198">Click Bind.</span></span>
49. <span data-ttu-id="ca902-199">Medyje išplėskite dalį Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="ca902-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="ca902-200">Medyje išplėskite dalį Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="ca902-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="ca902-201">Medyje išplėskite dalį Dimensions\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="ca902-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="ca902-202">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="ca902-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="ca902-203">Medyje pasirinkite Dimensions setting\Code.</span><span class="sxs-lookup"><span data-stu-id="ca902-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="ca902-204">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-204">Click Bind.</span></span>
55. <span data-ttu-id="ca902-205">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Report column name.</span><span class="sxs-lookup"><span data-stu-id="ca902-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="ca902-206">Medyje pasirinkite Dimensions setting\Name.</span><span class="sxs-lookup"><span data-stu-id="ca902-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="ca902-207">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-207">Click Bind.</span></span>
58. <span data-ttu-id="ca902-208">Medyje pasirinkite Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="ca902-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="ca902-209">Medyje pasirinkite Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="ca902-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="ca902-210">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="ca902-210">Click Bind.</span></span>
61. <span data-ttu-id="ca902-211">Medyje pasirinkite Įmonė.</span><span class="sxs-lookup"><span data-stu-id="ca902-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="ca902-212">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ca902-212">Click Edit.</span></span>
63. <span data-ttu-id="ca902-213">Lauke expressionAsStringText įveskite Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="ca902-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="ca902-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="ca902-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="ca902-215">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca902-215">Click Save.</span></span>
<span data-ttu-id="ca902-216">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="ca902-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="ca902-217">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca902-217">Close the page.</span></span>
66. <span data-ttu-id="ca902-218">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca902-218">Click Save.</span></span>
67. <span data-ttu-id="ca902-219">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca902-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="ca902-220">Šio modelio versijos juodraščio užbaigimas</span><span class="sxs-lookup"><span data-stu-id="ca902-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="ca902-221">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca902-221">Close the page.</span></span>
2. <span data-ttu-id="ca902-222">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ca902-222">Close the page.</span></span>
3. <span data-ttu-id="ca902-223">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="ca902-223">Click Change status.</span></span>
4. <span data-ttu-id="ca902-224">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="ca902-224">Click Complete.</span></span>
5. <span data-ttu-id="ca902-225">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="ca902-225">Click OK.</span></span>
<span data-ttu-id="ca902-226">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="ca902-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
