---
title: "Pašalinimo taisyklės"
description: "Šioje temoje pateikta informacija apie pašalinimo taisykles ir įvairias pašalinimo ataskaitų pasirinktis."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 882b8f21be94b8cbb0c162c965ffc129b47d7edf
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="elimination-rules"></a><span data-ttu-id="3e291-103">Pašalinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="3e291-103">Elimination rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3e291-104">Šioje temoje pateikta informacija apie pašalinimo taisykles ir įvairias pašalinimo ataskaitų pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="3e291-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="3e291-105">Šalinimo operacijų reikalaujama, kai pirminis juridinis subjektas bendradarbiauja su vienu ar daugiau filialo juridinių subjektų ir naudoja konsoliduotas finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="3e291-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="3e291-106">Konsoliduotose finansinėse ataskaitose turi būti nurodytos tik tos operacijos, kurios vyksta tarp konsoliduotos organizacijos ir kitų ne tos organizacijos objektų.</span><span class="sxs-lookup"><span data-stu-id="3e291-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="3e291-107">Todėl tos pačios organizacijos juridinių subjektų operacijos turi būti pašalintos iš DK, kad nebūtų rodomos finansinėse ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="3e291-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="3e291-108">Skelbti apie pašalinimus galima keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="3e291-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="3e291-109">Konsolidavimo ar pašalinimo įmonėje galima sukurti ir apdoroti pašalinimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="3e291-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="3e291-110">Galima naudoti finansines ataskaitas ir konkrečioje eilutėje arba stulpelyje rodyti pašalinimų sąskaitas ir dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3e291-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="3e291-111">Galima naudoti atskirą juridinį subjektą ir rankiniu būdu registruoti operacijų įrašus siekiant sekti pašalinimus.</span><span class="sxs-lookup"><span data-stu-id="3e291-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="3e291-112">Šioje temoje dėmesys skiriamas pašalinimo taisyklėms, kurios apdorojamos konsolidavimo arba pašalinimo įmonėje.</span><span class="sxs-lookup"><span data-stu-id="3e291-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="3e291-113">Galite nustatyti šalinimo taisykles, kad sukurtumėte šalinimo operacijas juridiniame subjekte, kuris nurodytas kaip šalinimo paskirties juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="3e291-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="3e291-114">Šis paskirties juridinis subjektas vadinamas šalinimo juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="3e291-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="3e291-115">Šalinimo žurnalus galima generuoti konsolidavimo proceso metu arba naudojant šalinimo žurnalo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="3e291-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="3e291-116">Prieš nustatydami pašalinimo taisykles, turite susipažinti su šiomis sąlygomis:</span><span class="sxs-lookup"><span data-stu-id="3e291-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="3e291-117">**Šaltinio juridinis subjektas** – juridinis subjektas, kur užregistruotos šalinimo sumos.</span><span class="sxs-lookup"><span data-stu-id="3e291-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="3e291-118">**Paskirties juridinis subjektas** – juridinis subjektas, kur užregistruotos šalinimo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="3e291-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="3e291-119">**Šalinimo juridinis subjektas** – juridinis subjektas, nurodytas kaip šalinimo paskirties juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="3e291-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="3e291-120">**Konsoliduotas juridinis subjektas** – juridinis subjektas, sukurtas norint pranešti juridinių subjektų grupės finansinius rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3e291-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="3e291-121">Juridinių subjektų finansiniai duomenys konsoliduojami šiame juridiniame subjekte, tada naudojant sujungtus duomenis sukuriama finansinė ataskaita.</span><span class="sxs-lookup"><span data-stu-id="3e291-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="3e291-122">Pateiktoje lentelėje parodyti operacijų, kurias gali reikėti pašalinti, tipai.</span><span class="sxs-lookup"><span data-stu-id="3e291-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e291-123">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="3e291-123">Transaction type</span></span></th>
<th><span data-ttu-id="3e291-124">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3e291-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e291-125">Pardavimo užsakymo įrašas ir SF išrašymas (centralizuotas vykdymas)</span><span class="sxs-lookup"><span data-stu-id="3e291-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="3e291-126">Galite parduoti produktą klientui kito jūsų organizacijos juridinio subjekto vardu.</span><span class="sxs-lookup"><span data-stu-id="3e291-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-127">Pardavimo užsakymo įrašas (vidinės įmonės / tarp įmonių) ir SF išrašymas</span><span class="sxs-lookup"><span data-stu-id="3e291-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="3e291-128">Galima parduoti produktų tarp savo organizacijos juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="3e291-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e291-129">Pirkimo užsakymai (centralizuotas vykdymas)</span><span class="sxs-lookup"><span data-stu-id="3e291-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="3e291-130">Atsargos, reikmenys, paslaugos, ilgalaikis turtas ir kiti produktai perkami iš tiekėjo kito jūsų organizacijos juridinio subjekto vardu.</span><span class="sxs-lookup"><span data-stu-id="3e291-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-131">Atsargų valdymas (įmonės viduje / tarp įmonių)</span><span class="sxs-lookup"><span data-stu-id="3e291-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="3e291-132">Vieno juridinio subjekto atsargas galite perkelti į kito savo organizacijos juridinio subjekto ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="3e291-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="3e291-133">Vieno juridinio subjekto atsargas galite perkelti į kito savo organizacijos juridinio subjekto atsargas.</span><span class="sxs-lookup"><span data-stu-id="3e291-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e291-134">Tranzitinis atsargų sekimas</span><span class="sxs-lookup"><span data-stu-id="3e291-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="3e291-135">Galite perkelti prekes tarp to paties juridinio subjekto sandėlių skirtingose geografinėse vietovėse.</span><span class="sxs-lookup"><span data-stu-id="3e291-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-136">Centralizuotas mokėtinų sumų SF vykdymas</span><span class="sxs-lookup"><span data-stu-id="3e291-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="3e291-137">SF galite įrašyti kito savo organizacijos juridinio subjekto vardu.</span><span class="sxs-lookup"><span data-stu-id="3e291-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e291-138">Centralizuotas mokėtinų sumų mokėjimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="3e291-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="3e291-139">SF galite apmokėti kito savo organizacijos juridinio subjekto vardu.</span><span class="sxs-lookup"><span data-stu-id="3e291-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-140">Grynųjų pinigų valdymas ir iždas (centralizuotas apdorojimas)</span><span class="sxs-lookup"><span data-stu-id="3e291-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="3e291-141">Galite apdoroti mokesčių mokėjimą, mokesčių grąžinimą, palūkanų išlaidas, panaudą, avansą, dividendų mokėjimą ir iš anksto sumokėtus naudojimosi turtu mokesčius arba komisinius.</span><span class="sxs-lookup"><span data-stu-id="3e291-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="3e291-142">Galite sumokėti kito savo organizacijos juridinio subjekto vardu.</span><span class="sxs-lookup"><span data-stu-id="3e291-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="3e291-143">SF įvedama paskirties juridinio subjekto knygose, o jūs turite sudengti tarp juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="3e291-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="3e291-144">Pavyzdžiui, vienas juridinis subjektas apmoka darbuotojo išlaidų ataskaitą kitame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="3e291-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="3e291-145">Šiuo atveju darbuotojo išlaidų ataskaitoje yra išlaidų, susijusių su kitu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="3e291-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="3e291-146">Savo organizacijoje galite perkelti grynuosius pinigus iš vieno juridinio subjekto į kitą.</span><span class="sxs-lookup"><span data-stu-id="3e291-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e291-147">Gautinos sumos (centralizuotas vykdymas)</span><span class="sxs-lookup"><span data-stu-id="3e291-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="3e291-148">Galite gauti grynųjų pinigų pagal kito juridinio subjekto kliento SF ir deponuoti čekį to juridinio subjekto banko sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="3e291-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-149">Algalapis (centralizuotas vykdymas, vidinėje įmonėje / tarp įmonių)</span><span class="sxs-lookup"><span data-stu-id="3e291-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="3e291-150">Galite mokėti kito juridinio subjekto atlyginimą.</span><span class="sxs-lookup"><span data-stu-id="3e291-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="3e291-151">Pvz., juridinis subjektas gali mokėti savo darbuotojams atlyginimą, bet atskaityti už darbą, kurį darbuotojas atliko kitam juridiniam subjektui, apdorodamas algalapius.</span><span class="sxs-lookup"><span data-stu-id="3e291-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="3e291-152">Arba darbuotojas pusę dienos dirbo juridiniame subjekte A, o kitą pusę – juridiniame subjekte B ir išmokos priklauso visam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="3e291-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="3e291-153">Tokiais atvejais darbuotojo užmokestis apima mokėjimą iš abiejų juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="3e291-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="3e291-154">Užregistruojami ne tik atlyginimai, bet ir mokesčiai, išmokos, atskaitymai ir atlyginimų kaupimas.</span><span class="sxs-lookup"><span data-stu-id="3e291-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="3e291-155">Galite perkelti darbą iš vieno padalinio į kitą.</span><span class="sxs-lookup"><span data-stu-id="3e291-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e291-156">Ilgalaikis turtas (vidinės įmonės / tarp įmonių)</span><span class="sxs-lookup"><span data-stu-id="3e291-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="3e291-157">Galite perkelti ilgalaikį turtą į kito juridinio subjekto ilgalaikį turtą ar atsargas.</span><span class="sxs-lookup"><span data-stu-id="3e291-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e291-158">Paskirstymai (vidinės įmonės / tarp įmonių)</span><span class="sxs-lookup"><span data-stu-id="3e291-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="3e291-159">Galite apdoroti įmonės paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="3e291-159">You process corporate allocations.</span></span> <span data-ttu-id="3e291-160">Paskirstymas yra bet kurios paskirstomos sąskaitos veikla nepaisant parengimo modulio.</span><span class="sxs-lookup"><span data-stu-id="3e291-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="3e291-161">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3e291-161">Example</span></span>
<span data-ttu-id="3e291-162">Jūsų juridinis subjektas (juridinis subjektas A) parduoda daiktus kitam jūsų organizacijos juridiniam subjektui (juridinis subjektas B). Pateiktame pavyzdyje parodyta, kaip gali tekti pašalinti dviejų juridinių subjektų atliekamas operacijas:</span><span class="sxs-lookup"><span data-stu-id="3e291-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="3e291-163">Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 10,00.</span><span class="sxs-lookup"><span data-stu-id="3e291-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="3e291-164">Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 10,00 bei apmoka faktines siuntimo išlaidas (2,00).</span><span class="sxs-lookup"><span data-stu-id="3e291-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="3e291-165">Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 15,00 ir pripažįsta šio pardavimo maržą.</span><span class="sxs-lookup"><span data-stu-id="3e291-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="3e291-166">Juridinis subjektas A parduoda daiktą, kuris kainuoja 10,00, juridiniam subjektui B už 15,00 ir pripažįsta pusę šio pardavimo maržos.</span><span class="sxs-lookup"><span data-stu-id="3e291-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="3e291-167">Juridinis subjektas B pripažįsta kitą šio pardavimo maržos pusę.</span><span class="sxs-lookup"><span data-stu-id="3e291-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="3e291-168">Todėl įplaukos išskaidomos.</span><span class="sxs-lookup"><span data-stu-id="3e291-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="3e291-169">Įplaukų išskaidymas suteikia stimulą užsakyti iš kito organizacijos juridinio subjekto, o ne išorinės organizacijos.</span><span class="sxs-lookup"><span data-stu-id="3e291-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="3e291-170">Visos šios operacijos sukuria vidinės įmonės operacijas, kurios užregistruojamos sąskaitose iki ir nuo.</span><span class="sxs-lookup"><span data-stu-id="3e291-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="3e291-171">Be to, šios operacijos gali apimti antkainio ir kainos sumažinimo sumas, kai vidinės įmonės pardavimo suma nėra lygi parduotų prekių išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="3e291-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="3e291-172">Nustatyti pašalinimo taisykles</span><span class="sxs-lookup"><span data-stu-id="3e291-172">Set up elimination rules</span></span>
<span data-ttu-id="3e291-173">Nustatant pašalinimo taisykles programoje „Microsoft Dynamics 365 for Finance and Operations“ rekomenduojame sukurti finansinę dimensija, skirtą tik šalinimo veiksmams atlikti.</span><span class="sxs-lookup"><span data-stu-id="3e291-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="3e291-174">Dauguma klientų pavadina ją Prekybos partneris arba panašiai</span><span class="sxs-lookup"><span data-stu-id="3e291-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="3e291-175">Jei nuspręsite nenaudoti finansinės dimensijos, būtinai turėkite dvi pagrindines sąskaitas, skirtas tik vidinės įmonės operacijoms.</span><span class="sxs-lookup"><span data-stu-id="3e291-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="3e291-176">Pašalinimo sąranką galima rasti modulio Konsolidavimas srityje Sąranka.</span><span class="sxs-lookup"><span data-stu-id="3e291-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="3e291-177">Įvedę taisyklės aprašą, turite pasirinkti įmonę, kurioje pašalinimo žurnalas bus registruojamas.</span><span class="sxs-lookup"><span data-stu-id="3e291-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="3e291-178">Tai turi būti įmonė, kurios juridinio subjekto sąrankoje pažymėta parinktis **Naudoti finansinio pašalinimo procese**.</span><span class="sxs-lookup"><span data-stu-id="3e291-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="3e291-179">Jei reikia, galite nustatyti pašalinimo taisyklės galiojimo pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="3e291-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="3e291-180">Turite nustatyti parinkties **Aktyvus** reikšmę **Taip**, jei norite, kad ją būtų galima naudoti pašalinimo pasiūlymo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="3e291-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="3e291-181">Pasirinkite žurnalo, kurio žurnalo tipas **Pašalinimas**, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3e291-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="3e291-182">Nurodę pagrindinę informaciją, galite nustatyti pačias apdorojimo taisykles, spustelėdami **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="3e291-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="3e291-183">Galimos dvi šalinimo parinktys: grynojo pokyčio sumos pašalinimas arba fiksuotos sumos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="3e291-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="3e291-184">Pasirinkite šaltinio sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3e291-184">Select your source account.</span></span> <span data-ttu-id="3e291-185">Žvaigždutę (\*) galite naudoti kaip universalųjį simbolį.</span><span class="sxs-lookup"><span data-stu-id="3e291-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="3e291-186">Pvz., nurodžius 1\*, kaip paskirstymo duomenų šaltinis būtų pasirinktos visos sąskaitos, kurios prasideda 1.</span><span class="sxs-lookup"><span data-stu-id="3e291-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="3e291-187">Pasirinkus šaltinio sąskaitas, **Sąskaitos specifikacija** nustato naudojamą paskirties įmonės sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3e291-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="3e291-188">Pasirinkite **Šaltinis**, jei norite naudoti tą pačią pagrindinę sąskaitą, nurodytą sąskaitoje **Šaltinis**.</span><span class="sxs-lookup"><span data-stu-id="3e291-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="3e291-189">Jei pasirinksite **Nurodyta vartotojo**, turite nurodyti paskirties sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3e291-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="3e291-190">Dimensijos specifikacijos funkcija tokia pati.</span><span class="sxs-lookup"><span data-stu-id="3e291-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="3e291-191">Jei pasirinkite **Šaltinis**, ji naudos tas pačias paskirties įmonės dimensijas, kurios naudojamos šaltinio įmonėje.</span><span class="sxs-lookup"><span data-stu-id="3e291-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="3e291-192">Jei pasirinksite **Nurodyta vartotojo**, turėsite nurodyti paskirties įmonės dimensijas, spustelėdami meniu elementą **Paskirties dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="3e291-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="3e291-193">Pasirinkite šaltinio dimensijas ir finansines dimensijas bei vertes, kurios naudojamos kaip pašalinimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="3e291-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="3e291-194">Apdoroti pašalinimo operacijas</span><span class="sxs-lookup"><span data-stu-id="3e291-194">Process elimination transactions</span></span>
<span data-ttu-id="3e291-195">Pašalinimo operacijas galima apdoroti dviem būdais: vykdant konsolidavimo tinkle procesą arba sukuriant pašalinimo žurnalą ir paleidžiant pašalinimo pasiūlymo procesą.</span><span class="sxs-lookup"><span data-stu-id="3e291-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="3e291-196">Šio skyriaus tikslas yra sukurti žurnalą ir paleisti pašalinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="3e291-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="3e291-197">Įmonėje, kuri nurodyta kaip pašalinimo įmonė, modulyje Konsolidavimas pasirinkite **Pašalinimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="3e291-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="3e291-198">Pasirinkę žurnalo pavadinimą spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="3e291-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="3e291-199">Pasiūlymą galite paleisti pasirinkę meniu **Pasiūlymai** ir tada pasirinkę **Pašalinimo pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="3e291-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="3e291-200">Pasirinktie įmonę, kuri yra konsoliduotų duomenų šaltinis, o tada pasirinktie taisyklę, kurią norite apdoroti.</span><span class="sxs-lookup"><span data-stu-id="3e291-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="3e291-201">Įveskite pradžios datą, kad pradėtumėte ieškoti pašalinimo sumų, ir įveskite pabaigos datą, kad pabaigtumėte pašalinimo sumų iešką.</span><span class="sxs-lookup"><span data-stu-id="3e291-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="3e291-202">Lauke **DK registravimo data** nurodyta data naudojama registruojant žurnalą DK.</span><span class="sxs-lookup"><span data-stu-id="3e291-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="3e291-203">Spustelėję **Gerai** galite peržiūrėti sumas ir registruoti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="3e291-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




