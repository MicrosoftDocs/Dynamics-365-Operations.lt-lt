---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (2 dalis – Modelio susiejimas)
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (2 dalis)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093242"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="9bafd-104">ER naudoti finansines dimensijas kaip duomenų šaltinį (2 dalis – Modelio susiejimas)</span><span class="sxs-lookup"><span data-stu-id="9bafd-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9bafd-105">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9bafd-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="9bafd-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="9bafd-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (1 dalis. Duomenų modelio kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="9bafd-108">Būtinų duomenų šaltinių įtraukimas į modelio susiejimą</span><span class="sxs-lookup"><span data-stu-id="9bafd-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="9bafd-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9bafd-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9bafd-110">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9bafd-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9bafd-111">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9bafd-111">Click Designer.</span></span>
4. <span data-ttu-id="9bafd-112">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="9bafd-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-113">Click New.</span></span>
6. <span data-ttu-id="9bafd-114">Lauke Apibrėžimas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="9bafd-115">Lauke Pavadinimas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="9bafd-116">Lauke Aprašas įveskite Dimensijų duomenų susiejimas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="9bafd-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-117">Click Save.</span></span>
10. <span data-ttu-id="9bafd-118">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9bafd-118">Click Designer.</span></span>
11. <span data-ttu-id="9bafd-119">Medyje pasirinkite Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="9bafd-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="9bafd-120">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-120">Click Add root.</span></span>
13. <span data-ttu-id="9bafd-121">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="9bafd-122">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="9bafd-123">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9bafd-123">Click OK.</span></span>
16. <span data-ttu-id="9bafd-124">Medyje pasirinkite Functions\Financial dimensions details.</span><span class="sxs-lookup"><span data-stu-id="9bafd-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="9bafd-125">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-125">Click Add root.</span></span>
    * <span data-ttu-id="9bafd-126">Šis duomenų šaltinis nurodo, kaip bus apibrėžta kiekvienos ataskaitos, kurioje šis modelis bus naudojamas kaip duomenų šaltinis, finansinių dimensijų apimtis.</span><span class="sxs-lookup"><span data-stu-id="9bafd-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="9bafd-127">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9bafd-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="9bafd-128">Lauke Prašyti dimensijų pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9bafd-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="9bafd-129">Pasirinkite Taip, jei norite leisti vartotojui vykdymo metu pasirinkti dimensijas formoje Vartotojo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="9bafd-130">Jei pasirinksite NE, visos šio egzemplioriaus finansinės dimensijos bus naudojamas kaip numatytosios.</span><span class="sxs-lookup"><span data-stu-id="9bafd-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="9bafd-131">Lauke Finansinių dimensijų pasirinkimas pasirinkite Juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="9bafd-132">Pasirinkite Visos, jei norite leisti vartotojui pasirinkti norimas dabartinio egzemplioriaus dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="9bafd-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="9bafd-133">Pasirinkite Juridinis subjektas, jei norite leisti vartotojui pasirinkti įmonės dimensijas lauke Peržvalga.</span><span class="sxs-lookup"><span data-stu-id="9bafd-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="9bafd-134">Pasirinkite Dimensija, jei norite leisti vartotojui pasirinkti dimensijas naudojant vieną dimensijų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="9bafd-135">Lauke Prašyti pagrindinės sąskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9bafd-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="9bafd-136">Nustatykite parinktį „Prašyti pagrindinės sąskaitos“ į Taip, kad leistumėte vartotojams pasirinkti pagrindinę sąskaitą kaip dimensijų sąrašo dalį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="9bafd-137">Jei pasirinksite Ne, pagrindinė sąskaita nebus įtraukta į dimensijų sąrašą ir parinktis „Ar pagrindinė sąskaita yra privaloma“ bus įjungta.</span><span class="sxs-lookup"><span data-stu-id="9bafd-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="9bafd-138">Jei parinktį „Ar pagrindinė sąskaita yra privaloma“ yra nustatyta į Taip, įtraukite pagrindinę sąskaitą į dimensijų sąrašą neatsižvelgdami į vartotojo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="9bafd-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="9bafd-139">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9bafd-139">Click OK.</span></span>
<span data-ttu-id="9bafd-140">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="9bafd-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="9bafd-141">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="9bafd-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="9bafd-142">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-142">Click Add root.</span></span>
25. <span data-ttu-id="9bafd-143">Lauke Pavadinimas įveskite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="9bafd-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="9bafd-144">Lauke „Prašyti užklausos“ pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="9bafd-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="9bafd-145">Lauke Lentelė įveskite LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="9bafd-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="9bafd-146">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9bafd-146">Click OK.</span></span>
<span data-ttu-id="9bafd-147">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="9bafd-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="9bafd-148">Duomenų modelio elementų susiejimas su įtrauktais duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="9bafd-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="9bafd-149">Medyje išplėskite dalį Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="9bafd-150">Medyje išplėskite dalį Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="9bafd-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="9bafd-151">Medyje išplėskite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="9bafd-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="9bafd-152">Medyje išplėskite dalį Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="9bafd-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="9bafd-153">Medyje išplėskite dalį LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="9bafd-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="9bafd-154">Medyje išplėskite LedgerJournal\<Relations.</span><span class="sxs-lookup"><span data-stu-id="9bafd-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="9bafd-155">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="9bafd-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="9bafd-156">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="9bafd-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="9bafd-157">Medyje pasirinkite Journal\Transaction\Voucher.</span><span class="sxs-lookup"><span data-stu-id="9bafd-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="9bafd-158">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-158">Click Bind.</span></span>
11. <span data-ttu-id="9bafd-159">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="9bafd-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="9bafd-160">Atminkite, kad su bet kokia nuoroda į finansines dimensijas, nustatyta į, pavyzdžiui, LedgerDimension, galima naudoti atitinkamą duomenų šaltinio elementą (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="9bafd-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="9bafd-161">Šis duomenų šaltinio elementas pateikia finansines dimensijas, kurios nustatytos kaip įrašo sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="9bafd-162">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="9bafd-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="9bafd-163">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="9bafd-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="9bafd-164">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="9bafd-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="9bafd-165">Medyje išplėskite dalį LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="9bafd-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="9bafd-166">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="9bafd-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="9bafd-167">Medyje pasirinkite Journal\Transaction\Dimensions data\Name.</span><span class="sxs-lookup"><span data-stu-id="9bafd-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="9bafd-168">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-168">Click Bind.</span></span>
19. <span data-ttu-id="9bafd-169">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="9bafd-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="9bafd-170">Medyje pasirinkite Journal\Transaction\Dimensions data\Description.</span><span class="sxs-lookup"><span data-stu-id="9bafd-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="9bafd-171">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-171">Click Bind.</span></span>
22. <span data-ttu-id="9bafd-172">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="9bafd-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="9bafd-173">Medyje pasirinkite Journal\Transaction\Dimensions data\Code.</span><span class="sxs-lookup"><span data-stu-id="9bafd-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="9bafd-174">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-174">Click Bind.</span></span>
25. <span data-ttu-id="9bafd-175">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="9bafd-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="9bafd-176">Medyje pasirinkite Journal\Transaction\Dimensions data.</span><span class="sxs-lookup"><span data-stu-id="9bafd-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="9bafd-177">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-177">Click Bind.</span></span>
<span data-ttu-id="9bafd-178">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="9bafd-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="9bafd-179">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="9bafd-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="9bafd-180">Medyje pasirinkite Journal\Transaction\Debit.</span><span class="sxs-lookup"><span data-stu-id="9bafd-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="9bafd-181">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-181">Click Bind.</span></span>
31. <span data-ttu-id="9bafd-182">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="9bafd-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="9bafd-183">Medyje pasirinkite Journal\Transaction\Date.</span><span class="sxs-lookup"><span data-stu-id="9bafd-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="9bafd-184">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-184">Click Bind.</span></span>
34. <span data-ttu-id="9bafd-185">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="9bafd-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="9bafd-186">Medyje pasirinkite Journal\Transaction\Currency.</span><span class="sxs-lookup"><span data-stu-id="9bafd-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="9bafd-187">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-187">Click Bind.</span></span>
37. <span data-ttu-id="9bafd-188">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="9bafd-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="9bafd-189">Medyje pasirinkite Journal\Transaction\Credit.</span><span class="sxs-lookup"><span data-stu-id="9bafd-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="9bafd-190">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-190">Click Bind.</span></span>
40. <span data-ttu-id="9bafd-191">Medyje pasirinkite LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="9bafd-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="9bafd-192">Medyje pasirinkite Journal\Transaction.</span><span class="sxs-lookup"><span data-stu-id="9bafd-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="9bafd-193">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-193">Click Bind.</span></span>
43. <span data-ttu-id="9bafd-194">Medyje pasirinkite LedgerJournal\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="9bafd-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="9bafd-195">Medyje pasirinkite Journal\Batch.</span><span class="sxs-lookup"><span data-stu-id="9bafd-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="9bafd-196">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-196">Click Bind.</span></span>
46. <span data-ttu-id="9bafd-197">Medyje pasirinkite LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="9bafd-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="9bafd-198">Medyje pasirinkite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="9bafd-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="9bafd-199">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-199">Click Bind.</span></span>
49. <span data-ttu-id="9bafd-200">Medyje išplėskite dalį Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="9bafd-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="9bafd-201">Medyje išplėskite dalį Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="9bafd-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="9bafd-202">Medyje išplėskite dalį Dimensions\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="9bafd-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="9bafd-203">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="9bafd-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="9bafd-204">Medyje pasirinkite Dimensions setting\Code.</span><span class="sxs-lookup"><span data-stu-id="9bafd-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="9bafd-205">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-205">Click Bind.</span></span>
55. <span data-ttu-id="9bafd-206">Medyje pasirinkite Dimensions\Main account and dimensions\Definition\Report column name.</span><span class="sxs-lookup"><span data-stu-id="9bafd-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="9bafd-207">Medyje pasirinkite Dimensions setting\Name.</span><span class="sxs-lookup"><span data-stu-id="9bafd-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="9bafd-208">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-208">Click Bind.</span></span>
58. <span data-ttu-id="9bafd-209">Medyje pasirinkite Dimensions\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="9bafd-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="9bafd-210">Medyje pasirinkite Dimensijų parametras.</span><span class="sxs-lookup"><span data-stu-id="9bafd-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="9bafd-211">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-211">Click Bind.</span></span>
61. <span data-ttu-id="9bafd-212">Medyje pasirinkite Įmonė.</span><span class="sxs-lookup"><span data-stu-id="9bafd-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="9bafd-213">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-213">Click Edit.</span></span>
63. <span data-ttu-id="9bafd-214">Lauke expressionAsStringText įveskite Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="9bafd-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="9bafd-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="9bafd-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="9bafd-216">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-216">Click Save.</span></span>
<span data-ttu-id="9bafd-217">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="9bafd-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="9bafd-218">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-218">Close the page.</span></span>
66. <span data-ttu-id="9bafd-219">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-219">Click Save.</span></span>
67. <span data-ttu-id="9bafd-220">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="9bafd-221">Šio modelio versijos juodraščio užbaigimas</span><span class="sxs-lookup"><span data-stu-id="9bafd-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="9bafd-222">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-222">Close the page.</span></span>
2. <span data-ttu-id="9bafd-223">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9bafd-223">Close the page.</span></span>
3. <span data-ttu-id="9bafd-224">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9bafd-224">Click Change status.</span></span>
4. <span data-ttu-id="9bafd-225">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9bafd-225">Click Complete.</span></span>
5. <span data-ttu-id="9bafd-226">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9bafd-226">Click OK.</span></span>
<span data-ttu-id="9bafd-227">![ER modelio susiejimo dizaino įrankio puslapis](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="9bafd-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
