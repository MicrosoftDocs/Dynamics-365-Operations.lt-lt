---
title: Finansinis konsolidavimas tinkle
description: "Šioje temoje aprašomas finansinis konsolidavimas Didžiojoje knygoje."
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2a9ceb774a8f205e39abe6a12a0deb69dd4cb69b
ms.openlocfilehash: fd29dc5f932c9cd274a42923e1ff659dd5d8e9d6
ms.contentlocale: lt-lt
ms.lasthandoff: 08/20/2018

---

# <a name="consolidate-online"></a><span data-ttu-id="51fbc-103">Konsoliduoti tinkle</span><span class="sxs-lookup"><span data-stu-id="51fbc-103">Consolidate online</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51fbc-104">Šioje temoje aprašomas finansinis konsolidavimas Didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="51fbc-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="51fbc-105">Prieš skaitydami šią temą, būtinai perskaitykite temą [Finansinio konsolidavimo ir valiutos konvertavimas](financial-consolidations-currency-translation.md).</span><span class="sxs-lookup"><span data-stu-id="51fbc-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="51fbc-106">Atlikę sąranką įveskite konsolidavimo informaciją puslapyje **Konsolidavimas [tinkle]**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="51fbc-107">Baigę galite spustelėti **Gerai** arba **Paketas**, kad apdorotumėte konsolidavimą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="51fbc-108">Kriterijai</span><span class="sxs-lookup"><span data-stu-id="51fbc-108">Criteria</span></span>
<span data-ttu-id="51fbc-109">Puslapio **Konsolidavimas [tinkle]** skirtuke **Kriterijai** galite nustatyti konsolidavimo sąskaitas, laikotarpius ir duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="51fbc-110">![Skirtukas Kriterijai](./media/criteria-consolidate-online.png "Skirtukas Kriterijai")</span><span class="sxs-lookup"><span data-stu-id="51fbc-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="51fbc-111">Čia pateikiamas šiame skirtuke esančių įvairių laukų paaiškinimas.</span><span class="sxs-lookup"><span data-stu-id="51fbc-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="51fbc-112">**Aprašas** – įveskite tikslų konsoliduojamo laikotarpio aprašą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="51fbc-113">**Pagrindinė sąskaita** – naudokite laukus šioje skiltyje, kad nustatytumėte pagrindines sąskaitas, kurios bus apdorojamos.</span><span class="sxs-lookup"><span data-stu-id="51fbc-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="51fbc-114">**Nuo** ir **Iki** – nurodykite apdorojamų sąskaitų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="51fbc-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="51fbc-115">Jei šie laukai paliekami tuščias, visos visų įmonių sąskaitos bus perkeltos į konsoliduotą įmonę.</span><span class="sxs-lookup"><span data-stu-id="51fbc-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="51fbc-116">Todėl, jei konsoliduojate keturias įmones, o kiekviena įmonė turi skirtingą sąskaitų planą, visos visų keturių įmonių sąskaitos bus sukurtos konsoliduotoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="51fbc-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="51fbc-117">**Naudoti konsolidavimo sąskaitą** – jei šią pasirinktį nustatote į **Taip**, galima naudoti lauką **Pasirinkti konsolidavimo sąskaitą iš**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="51fbc-118">Šiame lauke pasirinkite, ar visos sąskaitos turi būti konsoliduotos konsolidavimo sąskaitoje, kuri yra nustatyta puslapyje **Pagrindinės sąskaitos**, ar norite pasirinkti sąskaitą iš vienos iš konsolidavimo sąskaitų grupių.</span><span class="sxs-lookup"><span data-stu-id="51fbc-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="51fbc-119">**Konsolidavimo sąskaitų grupės** – pasirinkite grupę, kurią naudosite susiedami konsolidavimo pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="51fbc-120">**Konsolidavimo laikotarpis** – naudokite laukus šioje skiltyje, kad nurodytumėte konsolidavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="51fbc-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="51fbc-121">**Nuo** ir **Iki** – nurodykite konsolidavimo datų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="51fbc-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="51fbc-122">Jei šis laukas paliekamas tuščias, konsolidavimas bus taikomas visiems laikotarpiams, kurie apibrėžti įmonės DK kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="51fbc-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="51fbc-123">Nerekomenduojama palikti šiuos laukus tuščius.</span><span class="sxs-lookup"><span data-stu-id="51fbc-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="51fbc-124">**Įtraukti faktines sumas** – nustatykite šią parinktį į **Taip**, konsoliduotumėte savo faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="51fbc-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="51fbc-125">**Įtraukti biudžeto sumas** – nustatykite šią parinktį į **Taip**, kad konsoliduotumėte duomenis iš biudžeto registro.</span><span class="sxs-lookup"><span data-stu-id="51fbc-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="51fbc-126">**Perkurti balansus vykdant konsolidavimą** – nerekomenduojame nustatyti šią parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="51fbc-127">Vietoje to atkurkite balansus kaip atskirą paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="51fbc-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="51fbc-128">**Biudžeto modeliai** – jei pasirinkote konsoliduoti biudžeto duomenis, naudokite laukus šioje skiltyje, kad nustatytumėte biudžeto modelius.</span><span class="sxs-lookup"><span data-stu-id="51fbc-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="51fbc-129">**Nuo** ir **Iki** – nurodykite naudotinų modelių diapazoną.</span><span class="sxs-lookup"><span data-stu-id="51fbc-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="51fbc-130">**Biudžeto kurso tipas** – pasirinkite biudžeto kurso tipą, kuris bus naudojamas konvertuojant biudžeto duomenų valiutą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="51fbc-131">Finansinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="51fbc-131">Financial dimensions</span></span>
<span data-ttu-id="51fbc-132">Skirtuke **Finansinės dimensijos** galite nustatyti dimensijas, kurios turi būti įtrauktos į konsoliduotą įmonę.</span><span class="sxs-lookup"><span data-stu-id="51fbc-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="51fbc-133">Norėdami pasirinkti dimensiją, nustatyti lauką **Specifikacija** į parinktį **Dimensijos**, o tada nurodykite dimensijų tvarką konsoliduotoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="51fbc-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="51fbc-134">![Skirtukas Finansinės dimensijos](./media/financial-dimensions-cons.png "Skirtukas Finansinės dimensijos")</span><span class="sxs-lookup"><span data-stu-id="51fbc-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="51fbc-135">Nepaisant nurodytos tvarkos, **Pagrindinės sąskaita** visada bus pirmajame segmente.</span><span class="sxs-lookup"><span data-stu-id="51fbc-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="51fbc-136">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="51fbc-136">Legal entities</span></span>
<span data-ttu-id="51fbc-137">Skirtuke **Juridiniai subjektai** galite nustatyti įmones, kurios turi būti įtrauktos į konsoliduotą įmonę.</span><span class="sxs-lookup"><span data-stu-id="51fbc-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="51fbc-138">Taip pat galite nustatyti tų įmonių nuosavybės procentą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="51fbc-139">Jei nurodysite mažiau nei 100 procentų nuosavybės, nurodytas procentas bus sumuojamas konsoliduotoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="51fbc-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="51fbc-140">Jei yra konvertavimo skirtumų, laukas **Skirtumų konvertavimo sąskaitos tipas** naudojamas norint pasirinkti pagrindinę sąskaitą iš sąrankos puslapyje **Automatinių operacijų sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="51fbc-141">![Skirtukas Juridiniai subjektai](./media/legal-entities-cons.png "Skirtukas Juridiniai subjektai")</span><span class="sxs-lookup"><span data-stu-id="51fbc-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="51fbc-142">![Puslapis Automatinių operacijų sąskaitos](./media/accounts%20for%20automatic%20(cons).png "Puslapis Automatinių operacijų sąskaitos")</span><span class="sxs-lookup"><span data-stu-id="51fbc-142">![Accounts for automatic transactions page](./media/accounts%20for%20automatic%20(cons).png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="51fbc-143">Pašalinimas</span><span class="sxs-lookup"><span data-stu-id="51fbc-143">Elimination</span></span>
<span data-ttu-id="51fbc-144">Skirtuke **Pašalinimas** galite rinktis iš trijų toliau nurodytų apdorojimo pašalinimo parinkčių.</span><span class="sxs-lookup"><span data-stu-id="51fbc-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="51fbc-145">Pasirinkite pašalinimo taisyklę, tada lauke **Pasiūlymo pasirinktys** pasirinkite **Tik pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="51fbc-146">Pasirinkus šią parinktį pašalinimas bus apdorotas konsolidavimo proceso metu, tačiau viskas nebus registruojama vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="51fbc-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="51fbc-147">Žurnalą galima užregistruoti vėliau.</span><span class="sxs-lookup"><span data-stu-id="51fbc-147">You can post the journal later.</span></span>
- <span data-ttu-id="51fbc-148">Pasirinkite pašalinimo taisyklę, tada lauke **Pasiūlymo pasirinktys** pasirinkite **Tik registravimas**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="51fbc-149">Pasirinkus šią parinktį pašalinimas bus apdorotas konsolidavimo proceso metu ir viskas bus registruojama vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="51fbc-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="51fbc-150">Pašalinimo procesą vykdykite atskirai nuo konsolidavimo proceso naudodami pašalinimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="51fbc-151">![Skirtukas Pašalinimas](./media/elimination-cons-onl.png "Skirtukas Pašalinimas")</span><span class="sxs-lookup"><span data-stu-id="51fbc-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="51fbc-152">Daugiau informacijos apie pašalinimą žr. [Pašalinimo taisyklės](./elimination-rules.md).</span><span class="sxs-lookup"><span data-stu-id="51fbc-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="51fbc-153">Valiutos konvertavimas</span><span class="sxs-lookup"><span data-stu-id="51fbc-153">Currency translation</span></span>
<span data-ttu-id="51fbc-154">Skirtuke **Valiutos konvertavimas** galite nurodyti juridinį subjektą, sąskaitą ir valiutos kurso tipą bei kursą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="51fbc-155">Galima rinktis iš trijų parinkčių lauke **Taikyti valiutos kursą iš**.</span><span class="sxs-lookup"><span data-stu-id="51fbc-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="51fbc-156">**Konsolidavimo data** – konsolidavimo data bus naudojama valiutos kursui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="51fbc-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="51fbc-157">Šis kursas yra lygus vietos ar mėnesio pabaigos kursui.</span><span class="sxs-lookup"><span data-stu-id="51fbc-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="51fbc-158">Matysite kurso peržiūrą, tačiau negalėsite jo redaguoti.</span><span class="sxs-lookup"><span data-stu-id="51fbc-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="51fbc-159">**Operacijos data** – kiekvienos operacijos data bus naudojama pasirenkant valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="51fbc-160">Ši parinktis dažniausiai taikoma ilgalaikiam turtui ir dažnai vadinama retrospektyviniu kursu.</span><span class="sxs-lookup"><span data-stu-id="51fbc-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="51fbc-161">Negalite matyti kurso peržiūros, nes sąskaitų diapazone bus pateikta daug įvairių operacijų kursų.</span><span class="sxs-lookup"><span data-stu-id="51fbc-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="51fbc-162">**Vartotojo nurodytas kursas** – pasirinkę šią parinktį, galite įvesti norimą valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="51fbc-163">Ši parinktis gali būti naudinga taikant vidutinius valiutos keitimo kursus arba konsoliduojant pagal fiksuotą valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="51fbc-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="51fbc-164">![Skirtukas Valiutos konvertavimas](./media/currency-translation-cons-online.png "Skirtukas Valiutos konvertavimas")</span><span class="sxs-lookup"><span data-stu-id="51fbc-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51fbc-165">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="51fbc-165">Additional resources</span></span>

<span data-ttu-id="51fbc-166">Daugiau informacijos apie konsolidavimą ir valiutos konvertavimą žr. pirminę šios potemės temą: [Finansinis konsolidavimas ir valiutos konvertavimas](./financial-consolidations-currency-translation.md).</span><span class="sxs-lookup"><span data-stu-id="51fbc-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="51fbc-167">Informacijos apie scenarijus, kuriais galite generuoti konsoliduotas finansines ataskaitas, žr. [Konsoliduotų finansinių ataskaitų generavimas](./generating-consolidated-financial-statements.md).</span><span class="sxs-lookup"><span data-stu-id="51fbc-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>
