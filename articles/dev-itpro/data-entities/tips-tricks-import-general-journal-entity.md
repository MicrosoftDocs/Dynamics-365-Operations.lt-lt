---
title: "Geriausios kvitų importavimo naudojant objektą Bendrasis žurnalas praktikos"
description: "Šioje temoje pateikiama patarimų, kaip į bendrąjį žurnalą importuoti duomenų naudojant objektą Bendrasis žurnalas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a45a75d23c77af86b55866f99a97343a210ec777
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a><span data-ttu-id="6d00d-103">Geriausios kvitų importavimo naudojant objektą Bendrasis žurnalas praktikos</span><span class="sxs-lookup"><span data-stu-id="6d00d-103">Best practices for importing vouchers using the General journal entity</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6d00d-104">Šioje temoje pateikiama patarimų, kaip į bendrąjį žurnalą importuoti duomenų naudojant objektą Bendrasis žurnalas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-104">This topic provides tips for importing data into the General journal by using the General journal entity.</span></span>  

<span data-ttu-id="6d00d-105">Naudodami objektą Bendrasis žurnalas galite importuoti kvitus, kurių sąskaitos ar korespondentinės sąskaitos tipas yra **Didžioji knyga, Klientas, Tiekėjas arba Bankas**.</span><span class="sxs-lookup"><span data-stu-id="6d00d-105">You can use the General journal entity to import vouchers that have an account or offset account type of **Ledger, Customer, Vendor, or Bank**.</span></span> <span data-ttu-id="6d00d-106">Kvito duomenis galima įvesti vienoje eilutėje naudojant laukus **Sąskaita** ir **Korespondentinė sąskaita** arba keliose eilutėse, kuriose naudojamas tik laukas **Sąskaita**, o kiekvienoje eilutėje laukas **Korespondentinė sąskaita** paliekamas tuščias.</span><span class="sxs-lookup"><span data-stu-id="6d00d-106">The voucher can be entered as one line, using both the **Account** field and the **Offset account** field, or as a multi-line voucher, where only the **Account** field is used (and the **Offset account** is left blank on each line).</span></span> <span data-ttu-id="6d00d-107">Objekte Bendrasis žurnalas nepalaikomi visi sąskaitos tipai.</span><span class="sxs-lookup"><span data-stu-id="6d00d-107">The General journal entity doesn't support every account type.</span></span> <span data-ttu-id="6d00d-108">Jeigu reikalingi skirtingi sąskaitų tipų deriniai, geriau naudoti kitus objektus.</span><span class="sxs-lookup"><span data-stu-id="6d00d-108">Instead, other entities exist for scenarios where different combinations of account types are required.</span></span> <span data-ttu-id="6d00d-109">Pavyzdžiui, naudokite objektą Projekto išlaidų žurnalas projekto operacijai importuoti.</span><span class="sxs-lookup"><span data-stu-id="6d00d-109">For example, to import a project transaction, use the Project expense journal entity.</span></span> <span data-ttu-id="6d00d-110">Kiekvienas objektas sukurtas konkretiems scenarijams palaikyti, todėl papildomi laukai gali būti pasiekiami konkrečiuose objektuose naudojant tam tikrus scenarijus, tačiau papildomų laukų nebus konkrečiuose objektuose naudojant kitus scenarijus.</span><span class="sxs-lookup"><span data-stu-id="6d00d-110">Each entity is designed to support specific scenarios, which means additional fields may be available in entities for those scenarios but not in entities for a different scenario.</span></span>

## <a name="setup"></a><span data-ttu-id="6d00d-111">Sąranka</span><span class="sxs-lookup"><span data-stu-id="6d00d-111">Setup</span></span>
<span data-ttu-id="6d00d-112">Kol dar neimportavote naudodami objektą Bendrasis žurnalas, patikrinkite toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="6d00d-112">Before you import by using the General journal entity, validate the following setup:</span></span>

-   <span data-ttu-id="6d00d-113">**Žurnalo paketo numerio numeracijos sąranka** – pagal numatytuosius parametrus importuojant ir naudojant objektą Bendrasis žurnalas, žurnalo paketo numeryje naudojama numeracija, nurodyta DK parametruose.</span><span class="sxs-lookup"><span data-stu-id="6d00d-113">**Number sequence setup for the journal batch number** - By default, when you import by using the General journal entity, the journal batch number uses the number sequence that is defined in the General ledger parameters.</span></span> <span data-ttu-id="6d00d-114">Jei nustatysite žurnalo paketo numerio numeracijos parinktį **Neautomatinis**, numatytasis numeris nebus taikomas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-114">If you set the number sequence for the journal batch number to **Manual**, a default number isn't applied.</span></span> <span data-ttu-id="6d00d-115">Šis nustatymas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-115">This setup isn't supported.</span></span>
-   <span data-ttu-id="6d00d-116">**Finansinių dimensijų konfigūracija** – kiekviena organizacija turi nurodyti finansinių dimensijų tvarką, skirtą operacijoms importuoti naudojant objektus.</span><span class="sxs-lookup"><span data-stu-id="6d00d-116">**Financial dimension configuration** - Every organization must define the order of financial dimensions when entities are used to import transactions.</span></span> <span data-ttu-id="6d00d-117">Formato **DK dimensijų integracija** tvarka nustatoma dalyje **DK** &gt; **Sąskaitų planas** &gt; **Dimensijos** &gt; **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas** &gt; **Pasirinkti duomenų objektus**.</span><span class="sxs-lookup"><span data-stu-id="6d00d-117">The order is defined for the **Ledger dimensions integration** format, at **General ledger** &gt; **Chart of accounts** &gt; **Dimensions** &gt; **Financial dimension configuration for integrating applications** &gt; **Select data entities**.</span></span> <span data-ttu-id="6d00d-118">Importuojamos DK sąskaitos segmentų tvarka turi būti ta tokia pati.</span><span class="sxs-lookup"><span data-stu-id="6d00d-118">The segments of the ledger account that is imported must have the same order.</span></span> <span data-ttu-id="6d00d-119">Kitaip importavimo metu įvyks klaida.</span><span class="sxs-lookup"><span data-stu-id="6d00d-119">Otherwise, an error will occur during import.</span></span>

## <a name="general-journal-entity-setup"></a><span data-ttu-id="6d00d-120">Objekto Bendrasis žurnalas nustatymas</span><span class="sxs-lookup"><span data-stu-id="6d00d-120">General journal entity setup</span></span>
<span data-ttu-id="6d00d-121">Du toliau pateikti duomenų valdymo parametrai nulemia numatytojo žurnalo paketo numerio arba kvito numerio pritaikymo pobūdį.</span><span class="sxs-lookup"><span data-stu-id="6d00d-121">Two settings in Data management affect how the default journal batch number or voucher number is applied:</span></span>

-   <span data-ttu-id="6d00d-122">**Apdorojimas pagal rinkinį** (duomenų objekte)</span><span class="sxs-lookup"><span data-stu-id="6d00d-122">**Set-based processing** (on the data entity)</span></span>
-   <span data-ttu-id="6d00d-123">**Automatiškai sugeneruotas** (laukų susiejime)</span><span class="sxs-lookup"><span data-stu-id="6d00d-123">**Auto-generated** (on the field mapping)</span></span>

<span data-ttu-id="6d00d-124">Tolesniuose skyriuose apibūdinama, kaip šie parametrai veikia, ir paaiškinama, kaip generuojami žurnalo paketo numeriai ir kvitų numeriai.</span><span class="sxs-lookup"><span data-stu-id="6d00d-124">The following sections describe the effect of these settings, and also explain how journal batch numbers and voucher numbers are generated.</span></span>

### <a name="journal-batch-number"></a><span data-ttu-id="6d00d-125">Žurnalų paketo numeris</span><span class="sxs-lookup"><span data-stu-id="6d00d-125">Journal batch number</span></span>

-   <span data-ttu-id="6d00d-126">Objekto Bendrasis žurnalas nustatymas **Rinkiniu pagrįstas apdorojimas** generuojant žurnalo paketo numerius įtakos neturi.</span><span class="sxs-lookup"><span data-stu-id="6d00d-126">The **Set-based processing** setting on the General journal entity doesn't affect the way that journal batch numbers are generated.</span></span>
-   <span data-ttu-id="6d00d-127">Jei laukas **Žurnalo paketo numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, sukuriamas naujas kiekvienos importuojamos eilutės žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="6d00d-127">If the **Journal batch number** field is set to **Auto-generated**, a new journal batch number is created for every line that is imported.</span></span> <span data-ttu-id="6d00d-128">Taip daryti nerekomenduojama.</span><span class="sxs-lookup"><span data-stu-id="6d00d-128">This behavior isn't recommended.</span></span> <span data-ttu-id="6d00d-129">Nustatymą **Automatiškai sugeneruotas** galima rasti importavimo projekto dalie **Peržiūrėti schemą** skirtuke **Susiejimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="6d00d-129">The **Auto-generated** setting is found on the import project, under **View map**, on the **Mapping details** tab.</span></span>
-   <span data-ttu-id="6d00d-130">Jei laukas **Žurnalo paketo numeris** nėra nustatytas į parinktį **Automatiškai sugeneruotas**, žurnalo paketo numeris, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="6d00d-130">If the **Journal batch number** field isn't set to **Auto-generated**, the journal batch number is created as follows:</span></span>
    -   <span data-ttu-id="6d00d-131">Jei importuoto failo žurnalo paketo numeris atitinka esamą neregistruoto kasdieninio žurnalo numerį, į esamą žurnalą importuojamos visos eilutės, kurių žurnalo paketo numeris atitinka.</span><span class="sxs-lookup"><span data-stu-id="6d00d-131">If the journal batch number that is defined in the imported file matches an existing, unposted daily journal, all lines that have a matching journal batch number are imported into the existing journal.</span></span> <span data-ttu-id="6d00d-132">Eilutės niekada neimportuojamos į užregistruotą žurnalo paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="6d00d-132">Lines are never imported into a posted journal batch number.</span></span> <span data-ttu-id="6d00d-133">Vietoj to sukuriamas naujas numeris.</span><span class="sxs-lookup"><span data-stu-id="6d00d-133">Instead, a new number is created.</span></span>
    -   <span data-ttu-id="6d00d-134">Jei importuoto failo žurnalo paketo numeris neatitinka esamo neregistruoto kasdieninio žurnalo numerio, visos eilutės, kurių žurnalo paketo numeris toks pat, įtraukiamos į naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="6d00d-134">If the journal batch number that is defined in the imported file doesn't match an existing, unposted daily journal, all lines that have the same journal batch number are grouped under a new journal.</span></span> <span data-ttu-id="6d00d-135">Pvz., visos eilutės, kurių žurnalo paketo numeris yra 1, importuojamos į naują žurnalą, o visos eilutės, kurių žurnalo paketo numeris yra 2, importuojamos į antrą naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="6d00d-135">For example, all lines that have a journal batch number of 1 are imported into a new journal, and all lines that have a journal batch number of 2 are imported into a second new journal.</span></span> <span data-ttu-id="6d00d-136">Žurnalo paketo numeris sukuriamas naudojant numeraciją, kuri nurodyta DK parametruose.</span><span class="sxs-lookup"><span data-stu-id="6d00d-136">The journal batch number is created by using the number sequence that is defined in the General ledger parameters.</span></span>

### <a name="voucher-number"></a><span data-ttu-id="6d00d-137">Kvito numeris</span><span class="sxs-lookup"><span data-stu-id="6d00d-137">Voucher number</span></span>

-   <span data-ttu-id="6d00d-138">Kai naudojate objekto Bendrasis žurnalas nustatymą **Rinkiniu pagrįstas apdorojimas**, kvito numeris turi būti nurodytas importuojamame faile.</span><span class="sxs-lookup"><span data-stu-id="6d00d-138">When you use the **Set-based processing** setting on the General journal entity, the voucher number must be provided in the imported file.</span></span> <span data-ttu-id="6d00d-139">Kiekvienai bendrojo žurnalo operacijai priskiriamas kvito numeris, nurodytas importuojamame faile, net jei kvitas nėra subalansuotas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-139">Every transaction in the General journal is assigned the voucher number that is provided in the imported file, even if the voucher isn’t balanced.</span></span> <span data-ttu-id="6d00d-140">Jei norite naudoti apdorojimo pagal rinkinį parametrą bei nustatytą kvitų numerių numeraciją, 2016 m. vasario mėn. leidime pateikiamos karštosios pataisos.</span><span class="sxs-lookup"><span data-stu-id="6d00d-140">If you want to use set-based processing, but you also want to use the number sequence that is defined for voucher numbers, a hotfix has been provided for the February 2016 release.</span></span> <span data-ttu-id="6d00d-141">Karštosios pataisos numeris yra 3170316 ir ją galima atsisiųsti iš „Lifecycle services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="6d00d-141">The hotfix number is 3170316 and available for download from Lifecycle services (LCS).</span></span> <span data-ttu-id="6d00d-142">Daugiau informacijos žr. [Karštųjų pataisų atsisiuntimas iš „Lifecycle services“](..\migration-upgrade\download-hotfix-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="6d00d-142">For more information, see [Download hotfixes from Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).</span></span>
    -   <span data-ttu-id="6d00d-143">Norėdami įgalinti šią funkciją, žurnalo pavadinime, kuris naudojamas importavimo operacijoms atlikti, nustatykite parinktį **Numerių paskirstymas registruojant** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6d00d-143">To enable this functionality, on the journal name that is used for imports, set **Number allocation at posting** to **Yes**.</span></span>
    -   <span data-ttu-id="6d00d-144">Kvito numeris vis tiek turi būti nurodytas importuojamame faile.</span><span class="sxs-lookup"><span data-stu-id="6d00d-144">A voucher number must still be defined in the imported file.</span></span> <span data-ttu-id="6d00d-145">Tačiau šis numeris yra laikinas ir registruojant žurnalą jis bus perrašytas naudojant kvito numerį.</span><span class="sxs-lookup"><span data-stu-id="6d00d-145">However, this number is temporary and is overwritten by the voucher number when the journal is posted.</span></span> <span data-ttu-id="6d00d-146">Įsitikinkite, kad visos žurnalo eilutės yra tinkamai sugrupuotos pagal laikiną kvito numerį.</span><span class="sxs-lookup"><span data-stu-id="6d00d-146">You must make sure that the lines of the journal are grouped correctly by temporary voucher number.</span></span> <span data-ttu-id="6d00d-147">Pavyzdžiui, registruojant surandamos trys eilutės, kurių laikinas kvito numeris – 1.</span><span class="sxs-lookup"><span data-stu-id="6d00d-147">For example, during posting, three lines are found that have a temporary voucher number of 1.</span></span> <span data-ttu-id="6d00d-148">Laikinas visų trijų eilučių kvito numeris perrašomas naudojant paskesnį numeracijos numerį.</span><span class="sxs-lookup"><span data-stu-id="6d00d-148">The temporary voucher number of all three lines is overwritten by the next number in the number sequence.</span></span> <span data-ttu-id="6d00d-149">Jei šios trys eilutės nėra subalansuotas įrašas, kvitas nėra registruojamas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-149">If those three lines aren’t a balanced entry, the voucher isn't posted.</span></span> <span data-ttu-id="6d00d-150">Tada, jei rasta eilučių, kurių laikino kvito numeris yra 2, šis numeris yra perrašomas naudojant paskesnį numeracijos kvito numerį, ir t. t.</span><span class="sxs-lookup"><span data-stu-id="6d00d-150">Next, if lines are found that have a temporary voucher number of 2, this number is overwritten by the next voucher number in the number sequence, and so on.</span></span>

<!-- -->

-   <span data-ttu-id="6d00d-151">Kai parametro **Apdorojimas pagal rinkinį** nenaudojate, importuojamame faile neturite pateikti kvito numerio.</span><span class="sxs-lookup"><span data-stu-id="6d00d-151">When you don't use the **Set-based processing** setting, you do not need to provide a voucher number in the imported file.</span></span> <span data-ttu-id="6d00d-152">Kvitų numeriai sukuriami importavimo metu pagal žurnalo pavadinimo nustatymą (**Tik vienas kvitas**, **Pagal balansą**, ir t. t.).</span><span class="sxs-lookup"><span data-stu-id="6d00d-152">The voucher numbers are created during import, based on the setup of the journal name (**One voucher only**, **In connection of balance**, and so on).</span></span> <span data-ttu-id="6d00d-153">Pavyzdžiui, jei žurnalo pavadinimo nustatymas yra **Pagal balansą**, pirmai eilutei priskiriamas naujas numatytasis kvito numeris.</span><span class="sxs-lookup"><span data-stu-id="6d00d-153">For example, if the journal name is defined as **In connection of balance**, the first line receives a new default voucher number.</span></span> <span data-ttu-id="6d00d-154">Tada sistema vertina eilutę, siekdama nustatyti, ar debeto sumos lygios kredito sumoms.</span><span class="sxs-lookup"><span data-stu-id="6d00d-154">The system then evaluates the line to determine whether the debits equal the credits.</span></span> <span data-ttu-id="6d00d-155">Jei eilutėje nurodyta korespondentinė sąskaita, kitai importuojamai eilutei priskiriamas naujas kvito numeris.</span><span class="sxs-lookup"><span data-stu-id="6d00d-155">If an offset account exists on the line, the next line that is imported receives a new voucher number.</span></span> <span data-ttu-id="6d00d-156">Jei korespondentinė sąskaita nenurodyta, sistema įvertina, ar debeto sumos lygios kredito sumoms, kai importuojama kiekviena nauja eilutė.</span><span class="sxs-lookup"><span data-stu-id="6d00d-156">If no offset account exists, the system evaluates whether the debits equal the credits as each new line is imported.</span></span>
-   <span data-ttu-id="6d00d-157">Jei laukas **Kvito numeris** nustatytas į parinktį **Automatiškai sugeneruotas**, importuoti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="6d00d-157">If the **Voucher number** field is set to **Auto-generated**, the import won't succeed.</span></span> <span data-ttu-id="6d00d-158">Lauko **Kvito numeris** nustatymas **Automatiškai sugeneruotas** nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="6d00d-158">The **Auto-generated** setting for the **Voucher number** field isn't supported.</span></span>

<span data-ttu-id="6d00d-159">Pagal numatytuosius parametrus objektas Bendrasis žurnalas naudoja rinkiniu pagrįstą apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="6d00d-159">By default, the General journal entity uses set-based processing.</span></span> <span data-ttu-id="6d00d-160">Įvertinę savo organizacijos verslo poreikius, nustatymą **Rinkiniu pagrįstas apdorojimas** galite pakeisti, darbo srityje **Duomenų valdymas** spustelėdami **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="6d00d-160">After you evaluate the business requirements for your organization, you can change the **Set-based processing** setting by clicking **Data entities** in the **Data management** workspace.</span></span> <span data-ttu-id="6d00d-161">Rinkiniu pagrįstas apdorojimas yra naudojamas importavimo procesui pagreitinti.</span><span class="sxs-lookup"><span data-stu-id="6d00d-161">Set-based processing is used to speed up the import process.</span></span> <span data-ttu-id="6d00d-162">Jeigu naudojate rinkiniu pagrįsto apdorojimo, importavimo procesas naudojant objektą Bendrasis žurnalas bus lėtesnis.</span><span class="sxs-lookup"><span data-stu-id="6d00d-162">If you don't use set-based processing, import of the General journal entity import will be slower.</span></span>



