---
title: "Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje"
description: "Sukūrus kūrimo blokus ir sugeneravus ataskaitas, patartina šiuos objektus sutvarkyti, kad vartotojai galėtų juos lengviau rasti. Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="f559e-104">Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje</span><span class="sxs-lookup"><span data-stu-id="f559e-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f559e-105">Sukūrus kūrimo blokus ir sugeneravus ataskaitas, patartina šiuos objektus sutvarkyti, kad vartotojai galėtų juos lengviau rasti.</span><span class="sxs-lookup"><span data-stu-id="f559e-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="f559e-106">Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus.</span><span class="sxs-lookup"><span data-stu-id="f559e-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="f559e-107">Galite pervardyti aplankus, ataskaitas, kūrimo blokus ir kitus objektus ataskaitų dizaino įrankyje, kad būtų lengviau sutvarkyti failus.</span><span class="sxs-lookup"><span data-stu-id="f559e-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="f559e-108">Atsižvelgiant į pervardijamo objekto tipą, gali reikėti atnaujinti susiejimus su šiuo objektu.</span><span class="sxs-lookup"><span data-stu-id="f559e-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="f559e-109">Aplanko arba kūrimo bloko pervardijimas ataskaitų konstruktoriuje</span><span class="sxs-lookup"><span data-stu-id="f559e-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="f559e-110">Ataskaitų konstruktoriuje galite pervardyti aplankus, ataskaitų aprašus, eilučių aprašus, stulpelių aprašus ir ataskaitų medžio aprašus.</span><span class="sxs-lookup"><span data-stu-id="f559e-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="f559e-111">**Pastaba.** Pervardiję kūrimo bloką, turite atnaujinti visus ataskaitų aprašus, naudojančius tą kūrimo bloką.</span><span class="sxs-lookup"><span data-stu-id="f559e-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="f559e-112">Kitaip nauja ataskaita negalės būti sėkmingai sugeneruota.</span><span class="sxs-lookup"><span data-stu-id="f559e-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="f559e-113">Aplanko arba kūrimo bloko pervardijimas ataskaitų konstruktoriuje</span><span class="sxs-lookup"><span data-stu-id="f559e-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="f559e-114">Ataskaitų konstruktoriuje raskite aplanką arba objektą, kurį norite pervardyti, naudodami naršymo sritį.</span><span class="sxs-lookup"><span data-stu-id="f559e-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="f559e-115">Dešiniuoju pelės klavišu spustelėkite aplanką arba objektą ir tada spustelėkite **Pervardyti**.</span><span class="sxs-lookup"><span data-stu-id="f559e-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="f559e-116">Naršymo srities laukas **Pavadinimas** tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="f559e-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="f559e-117">Įveskite naują pavadinimą ir tada paspauskite Įvesti.</span><span class="sxs-lookup"><span data-stu-id="f559e-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="f559e-118">Jei kūrimo blokas yra eilutės aprašas, stulpelio aprašas arba ataskaitų medžio aprašas, turite atnaujinti kitus kūrimo blokus, susietus su šiuo kūrimo bloku.</span><span class="sxs-lookup"><span data-stu-id="f559e-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="f559e-119">Dešiniuoju pelės klavišu spustelėkite kūrimo bloką, pervardytą atliekant 3 veiksmą, pasirinkite **Susiejimai** ir tada pasirinkite sąrašo elementą, kad jį atnaujintumėte.</span><span class="sxs-lookup"><span data-stu-id="f559e-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="f559e-120">Kartokite 4 veiksmą, kol visi susieti elementai bus atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="f559e-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="f559e-121">Ataskaitų grupių kūrimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="f559e-121">Create and manage report groups</span></span>
<span data-ttu-id="f559e-122">Galite grupuoti ataskaitų aprašus, kad sukurtumėte kelias ataskaitas tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="f559e-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="f559e-123">Kad galėtumėte kurti, modifikuoti, naikinti ir generuoti ataskaitų grupes, turite turėti dizainerio arba administratoriaus vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="f559e-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="f559e-124">Vartotojai, turintys generatorius vaidmenį, gali generuoti ataskaitų grupes ir taip pat modifikuoti ataskaitų grupių vartotojo ataskaitų aprašų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="f559e-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="f559e-125">Ataskaitų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="f559e-125">Create a report group</span></span>

1.  <span data-ttu-id="f559e-126">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.</span><span class="sxs-lookup"><span data-stu-id="f559e-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="f559e-127">Meniu **Failas** spustelėkite **Naujas** &gt; **Ataskaitų grupės aprašas**, kad atidarytumėte naują ataskaitų grupę peržiūros programos lange.</span><span class="sxs-lookup"><span data-stu-id="f559e-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="f559e-128">Arba įrankių juostoje spustelėkite mygtuką **Ataskaitų grupė** ![Ataskaitų grupė](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Ataskaitų grupė").</span><span class="sxs-lookup"><span data-stu-id="f559e-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="f559e-129">Spustelėkite skirtuką **Ataskaitų grupė**.</span><span class="sxs-lookup"><span data-stu-id="f559e-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="f559e-130">Norėdami perrašyti atskirų ataskaitų aprašų informaciją, kad galėtumėte generuoti šią ataskaitą, pažymėkite žymės langelį **Perrašyti atskirų ataskaitų aprašų įmonės, išsamios informacijos ir datos parametrus**.</span><span class="sxs-lookup"><span data-stu-id="f559e-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="f559e-131">Įmonės pavadinimo, išsamumo lygio, laikinojo parametro ir datos informacija įvedama automatiškai, bet jūs galite ją naujinti.</span><span class="sxs-lookup"><span data-stu-id="f559e-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="f559e-132">Pažymėkite žymės langelį **Įtraukti visas ataskaitų valiutas**, jei norite sugeneruoti kelias ataskaitas, kuriose rodomos tos ataskaitų valiutos.</span><span class="sxs-lookup"><span data-stu-id="f559e-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="f559e-133">Tada, peržiūrint ataskaitą, žiniatinklio peržiūros programoje spustelėjus mygtuką **Valiuta** bus rodomi keli rodiniai.</span><span class="sxs-lookup"><span data-stu-id="f559e-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="f559e-134">Lauke **Grupės ataskaitos** spustelėkite **Įtraukti** ir pasirinkite ataskaitas, kurias norite įtraukti į ataskaitų grupę.</span><span class="sxs-lookup"><span data-stu-id="f559e-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="f559e-135">Norėdami dialogo lange **Įtraukti** pasirinkti kelias ataskaitas, pažymėkite ataskaitas laikydami nuspaudę klavišą CTRL.</span><span class="sxs-lookup"><span data-stu-id="f559e-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="f559e-136">Pasirinkę ataskaitas, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f559e-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="f559e-137">Spustelėkite **Failas** &gt; **Įrašyti**, kad įrašytumėte naują ataskaitų grupę.</span><span class="sxs-lookup"><span data-stu-id="f559e-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="f559e-138">Ataskaitų grupės modifikavimas</span><span class="sxs-lookup"><span data-stu-id="f559e-138">Modify a report group</span></span>

1.  <span data-ttu-id="f559e-139">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.</span><span class="sxs-lookup"><span data-stu-id="f559e-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="f559e-140">Dukart spustelėkite ataskaitų grupę, kurią norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="f559e-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="f559e-141">Skirtuke **Ataskaitų grupė** atlikite norimus keitimus.</span><span class="sxs-lookup"><span data-stu-id="f559e-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="f559e-142">Meniu **Failas** spustelėkite **Įrašyti**, kad įrašytumėte modifikuotą ataskaitų grupę. Arba įrankių juostoje spustelėkite mygtuką **Įrašyti** ![Įrašyti](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Įrašyti").</span><span class="sxs-lookup"><span data-stu-id="f559e-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="f559e-143">**Pastaba.** Jei suplanavote ataskaitas generuoti tam tikrais intervalais, galite nepaisyti šių parametrų ir generuoti ataskaitą iš karto.</span><span class="sxs-lookup"><span data-stu-id="f559e-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="f559e-144">Ataskaitų grupės ataskaitos generavimas</span><span class="sxs-lookup"><span data-stu-id="f559e-144">Generate a report group report</span></span>

1.  <span data-ttu-id="f559e-145">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.</span><span class="sxs-lookup"><span data-stu-id="f559e-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="f559e-146">Atidarykite ataskaitų grupę, kurią norite generuoti.</span><span class="sxs-lookup"><span data-stu-id="f559e-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="f559e-147">Norėdami generuoti ataskaitas, spustelėkite mygtuką **Generuoti ataskaitą** ![Generuoti ataskaitą](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generuoti ataskaitą").</span><span class="sxs-lookup"><span data-stu-id="f559e-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="f559e-148">Ataskaitų grupės panaikinimas</span><span class="sxs-lookup"><span data-stu-id="f559e-148">Delete a report group</span></span>

1.  <span data-ttu-id="f559e-149">Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.</span><span class="sxs-lookup"><span data-stu-id="f559e-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="f559e-150">Dešiniuoju pelės klavišu spustelėkite ataskaitos grupę, kurią norite naikinti, ir tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="f559e-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="f559e-151">Kai pasirodo patvirtinimo pranešimas, spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f559e-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="f559e-152">Ataskaitų grupės skirtuko valdikliai</span><span class="sxs-lookup"><span data-stu-id="f559e-152">Report Group tab controls</span></span>
<span data-ttu-id="f559e-153">Toliau pateikiamoje lentelėje aprašomi skirtuko **Ataskaitų grupė** valdikliai.</span><span class="sxs-lookup"><span data-stu-id="f559e-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f559e-154">Valdiklis</span><span class="sxs-lookup"><span data-stu-id="f559e-154">Control</span></span></th>
<th><span data-ttu-id="f559e-155">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f559e-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f559e-156">Nepaisyti įmonės, išsamios informacijos ir datos parametrų iš atskirų ataskaitų aprašų</span><span class="sxs-lookup"><span data-stu-id="f559e-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="f559e-157">Pažymėkite šį žymės langelį norėdami nepaisyti atskirų šios ataskaitų grupės ataskaitų aprašų generuojant tik šias ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="f559e-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f559e-158">Įmonės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f559e-158">Company name</span></span></td>
<td><span data-ttu-id="f559e-159">Pasirinkite įmonę, kuri bus naudojama ataskaitoms generuoti.</span><span class="sxs-lookup"><span data-stu-id="f559e-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f559e-160">Detalumo lygis</span><span class="sxs-lookup"><span data-stu-id="f559e-160">Detail level</span></span></td>
<td><span data-ttu-id="f559e-161">Nurodykite ataskaitų informacijos išsamumo lygį.</span><span class="sxs-lookup"><span data-stu-id="f559e-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="f559e-162"><strong>Finansinė</strong>− aukšto lygio bendroji suvestinė ataskaita.</span><span class="sxs-lookup"><span data-stu-id="f559e-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="f559e-163">Negalima detalizuoti iki sąskaitų ir dimensijų, išskyrus tas sąskaitas ir dimensijas, kurios įtrauktos naudojant ataskaitų medį.</span><span class="sxs-lookup"><span data-stu-id="f559e-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="f559e-164"><strong>Finansinė &amp; sąskaitos</strong> − ataskaita, kurioje yra aukšto lygio suvestinė ir išsami sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="f559e-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="f559e-165"><strong>Finansinė, sąskaitos &amp; operacijų</strong> − ataskaita, kurioje yra aukšto lygio suvestinė ir išsami operacijų informacija.</span><span class="sxs-lookup"><span data-stu-id="f559e-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f559e-166">Laikinoji</span><span class="sxs-lookup"><span data-stu-id="f559e-166">Provisional</span></span></td>
<td><span data-ttu-id="f559e-167">Nurodykite ataskaitų veiklų tipus.</span><span class="sxs-lookup"><span data-stu-id="f559e-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="f559e-168"><strong>Tik užregistruota veikla</strong>− apima tik operacijas ir balansus, kurie yra užregistruoti kaip jūsų finansiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="f559e-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="f559e-169"><strong>Užregistruota ir neužregistruota veikla</strong>− apima visas operacijas ir balansus, kurie yra įvesti ir užregistruoti kaip jūsų finansiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="f559e-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="f559e-170"><strong>Tik neužregistruota veikla</strong>− apima tik operacijas, kurios yra įvestos, bet dar neužregistruotos kaip jūsų finansiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="f559e-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f559e-171">Apima visas ataskaitų valiutas</span><span class="sxs-lookup"><span data-stu-id="f559e-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="f559e-172">Jei jūsų „Microsoft Dynamics“ ERP sistemoje yra papildomų sukonfigūruotų ataskaitų valiutų, jos pateikiamos čia.</span><span class="sxs-lookup"><span data-stu-id="f559e-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="f559e-173">Pažymėkite šį žymės langelį, jei norite, kad papildomos ataskaitos būtų generuojamos nurodyta valiuta.</span><span class="sxs-lookup"><span data-stu-id="f559e-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="f559e-174">Norėdami šias ataskaitas peržiūrėti žiniatinklio peržiūros programoje, spustelėkite mygtuką <strong>Valiuta</strong> ir tada pasirinkite valiutą.</span><span class="sxs-lookup"><span data-stu-id="f559e-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f559e-175">Ataskaitos aprašo datos informacija neįrašyta</span><span class="sxs-lookup"><span data-stu-id="f559e-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="f559e-176">Pagrindinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="f559e-176">Base period</span></span></li>
<li><span data-ttu-id="f559e-177">Pagrindiniai metai</span><span class="sxs-lookup"><span data-stu-id="f559e-177">Base year</span></span></li>
<li><span data-ttu-id="f559e-178">Įtrauktas laikotarpis</span><span class="sxs-lookup"><span data-stu-id="f559e-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="f559e-179">Su ataskaitos aprašu įrašomi tik numatytieji pagrindinio laikotarpio parametrai.</span><span class="sxs-lookup"><span data-stu-id="f559e-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f559e-180">Ataskaitos aprašo datos informacija įrašyta</span><span class="sxs-lookup"><span data-stu-id="f559e-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="f559e-181">Ataskaitos data</span><span class="sxs-lookup"><span data-stu-id="f559e-181">Report date</span></span></li>
<li><span data-ttu-id="f559e-182">Numatytasis pagrindinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="f559e-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f559e-183">Grupės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="f559e-183">Reports in group</span></span></td>
<td><span data-ttu-id="f559e-184">Įtraukite, pašalinkite ir pertvarkykite ataskaitų grupės ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="f559e-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="f559e-185">Norėdami įtraukti į ataskaitų grupę ataskaitų, dukart spustelėkite ataskaitų grupę, kad ją atidarytumėte, ir tada spustelėkite <strong>Įtraukti</strong>.</span><span class="sxs-lookup"><span data-stu-id="f559e-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="f559e-186">Pažymėkite ataskaitas, kurias norite įtraukti į ataskaitos grupę, ir tada spustelėkite <strong>Gerai</strong>.</span><span class="sxs-lookup"><span data-stu-id="f559e-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="f559e-187">Norėdami pašalinti ataskaitą iš ataskaitos grupės, pažymėkite ją ir tada spustelėkite <strong>Pašalinti</strong>.</span><span class="sxs-lookup"><span data-stu-id="f559e-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="f559e-188">Norėdami modifikuoti, kokia tvarka ataskaitos bus generuojamos, sąraše pasirinkite ataskaitą ir tada spustelėkite <strong>Perkelti aukštyn</strong> arba <strong>Perkelti žemyn</strong>.</span><span class="sxs-lookup"><span data-stu-id="f559e-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="f559e-189">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="f559e-189">See also</span></span>
--------

[<span data-ttu-id="f559e-190">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="f559e-190">Financial reporting</span></span>](financial-reporting-intro.md)




