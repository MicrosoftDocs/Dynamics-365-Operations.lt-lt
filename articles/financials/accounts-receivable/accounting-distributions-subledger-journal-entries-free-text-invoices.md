---
title: Apskaitos paskirstymai ir papildomos knygos žurnalo įrašai, skirti laisvos formos SF
description: Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF. Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d1546e8537110daec5d6655f68d3328a58ca1cb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "334869"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="a4021-104">Apskaitos paskirstymai ir papildomos knygos žurnalo įrašai, skirti laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="a4021-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4021-105">Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="a4021-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="a4021-106">Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="a4021-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="a4021-107">Apskaitos paskirstymai</span><span class="sxs-lookup"><span data-stu-id="a4021-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="a4021-108">Laisvos formos SF puslapyje naudodami toliau nurodytus mygtukus galite peržiūrėti ir, galbūt, keisti kiekvienos laisvos formos SF nurodytos sumos apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="a4021-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="a4021-109">**Paskirstyti sumas** –peržiūrėkite ir keiskite apskaitos paskirstymus konkrečioje eilutėje ir visose antrinėse eilutėse, pvz., mokesčių ar rinkliavų.</span><span class="sxs-lookup"><span data-stu-id="a4021-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="a4021-110">Antrinės eilutės apskaitos paskirstymus taip pat galite peržiūrėti ir keisti tiesiogiai iš PVM operacijų puslapio arba Išlaidų operacijų puslapio.</span><span class="sxs-lookup"><span data-stu-id="a4021-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="a4021-111">Keiskite laisvos formos SF antraštės sumas, pvz., rinkliavas arba valiutos sumos apvalinimą.</span><span class="sxs-lookup"><span data-stu-id="a4021-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="a4021-112">Keiskite laisvos formos SF eilutės sumas.</span><span class="sxs-lookup"><span data-stu-id="a4021-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="a4021-113">**Peržiūrėti paskirstymus** – peržiūrėkite visų dokumentų eilučių apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="a4021-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="a4021-114">Negalite keisti apskaitos paskirstymų iš šio rodinio.</span><span class="sxs-lookup"><span data-stu-id="a4021-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="a4021-115">Peržiūrėkite antraštės ir eilutės sumas.</span><span class="sxs-lookup"><span data-stu-id="a4021-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="a4021-116">Sumų paskirstymas</span><span class="sxs-lookup"><span data-stu-id="a4021-116">Distributing amounts</span></span>
<span data-ttu-id="a4021-117">Kai įvedate laisvos formos SF, kiekviena suma bus paskirstyta kaip aprašyta toliau.</span><span class="sxs-lookup"><span data-stu-id="a4021-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4021-118">Piniginės sumos tipas</span><span class="sxs-lookup"><span data-stu-id="a4021-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="a4021-119">Iš kur rodoma pagrindinė sąskaita</span><span class="sxs-lookup"><span data-stu-id="a4021-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="a4021-120">Pirmenybės tvarka, kuri lemia, kuri numatytoji finansinė dimensija rodoma</span><span class="sxs-lookup"><span data-stu-id="a4021-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4021-121">Laisvos formos SF eilutė</span><span class="sxs-lookup"><span data-stu-id="a4021-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="a4021-122">Laisvos formos SF eilutės DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="a4021-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="a4021-123">Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="a4021-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="a4021-124">Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4021-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-125">Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4021-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-126">Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4021-127">Ilgalaikio turto numerio ir vertinimo modelio derinio laisvos formos SF eilutė</span><span class="sxs-lookup"><span data-stu-id="a4021-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a4021-128"><strong>Pastaba. </strong></span><span class="sxs-lookup"><span data-stu-id="a4021-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4021-129">Laisvos formos SF eilutėje pagrindinė sąskaita bus ilgalaikio turto likvidavimo sąskaita.</span><span class="sxs-lookup"><span data-stu-id="a4021-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="a4021-130">Laisvos formos SF eilutės DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="a4021-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="a4021-131">Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4021-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-132">Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4021-133">Laisvos formos SF nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="a4021-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="a4021-134">Puslapio Mokėjimo nuolaidos laukas Pagrindinė sąskaita, skirta kliento nuolaidoms.</span><span class="sxs-lookup"><span data-stu-id="a4021-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="a4021-135">Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="a4021-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="a4021-136">Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4021-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-137">Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4021-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-138">Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4021-139">Laisvos formos SF PVM suma</span><span class="sxs-lookup"><span data-stu-id="a4021-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="a4021-140">Mokėtino PVM laukas DK registravimo grupių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="a4021-141">Naudokite finansines dimensijas, apibrėžtas laisvos formos SF eilutės sumoje, arba paskirstymus išlaidų eilutės sumoje.</span><span class="sxs-lookup"><span data-stu-id="a4021-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="a4021-142">Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4021-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-143">Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4021-144">Laisvos formos SF išlaidų eilutės suma</span><span class="sxs-lookup"><span data-stu-id="a4021-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="a4021-145">Kredito sąskaitos laukas Išlaidų kodo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="a4021-146">Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="a4021-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="a4021-147">Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4021-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-148">Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a4021-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="a4021-149">Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a4021-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="a4021-150">Mokesčių paskirstymas</span><span class="sxs-lookup"><span data-stu-id="a4021-150">Distributing taxes</span></span>
<span data-ttu-id="a4021-151">Mokesčių apskaitos paskirstymus galima kurti tik apskaičiavus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="a4021-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="a4021-152">Norėdami skaičiuoti PVM, turite atlikti vieną iš toliau pateiktų užduočių formoje Laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="a4021-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="a4021-153">Peržiūrėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="a4021-153">View the sales tax.</span></span>
-   <span data-ttu-id="a4021-154">Peržiūrėkite SF bendrąją sumą.</span><span class="sxs-lookup"><span data-stu-id="a4021-154">View the invoice total.</span></span>
-   <span data-ttu-id="a4021-155">Peržiūrėkite grynųjų pinigų srautą.</span><span class="sxs-lookup"><span data-stu-id="a4021-155">View the cash flow.</span></span>
-   <span data-ttu-id="a4021-156">Peržiūrėkite visos laisvos formos SF apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="a4021-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="a4021-157">Peržiūrėkite papildomos knygos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="a4021-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="a4021-158"> Laisvos formos SF papildomos knygos žurnalai</span><span class="sxs-lookup"><span data-stu-id="a4021-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="a4021-159">Prieš registruodami laisvos formos SF galite peržiūrėti visą sąskaitos faktūros apskaitos įrašą, kuris apima debetus ir kreditus, kad patikrintumėte, ar sąskaita faktūra registruojama tinkamose sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="a4021-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="a4021-160">Šis viso apskaitos įrašo rodinys vadinamas papildomos knygos žurnalu.</span><span class="sxs-lookup"><span data-stu-id="a4021-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="a4021-161">Jei papildomos knygos žurnalo įrašas neteisingas, kai peržiūrite jį prieš įtraukdami laisvos formos SF į žurnalą, negalite keisti papildomos knygos žurnalo įrašo.</span><span class="sxs-lookup"><span data-stu-id="a4021-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="a4021-162">Bet galite keisti apskaitos paskirstymus arba registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="a4021-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="a4021-163">Apskaitos paskirstymai naudojami norint nustatyti vieną apskaitos įrašo pusę, debetą arba kreditą.</span><span class="sxs-lookup"><span data-stu-id="a4021-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="a4021-164">Balansavimo papildomos knygos žurnalo sąskaitos įrašas sukuriamas iš registravimo profilių, pvz., iš kliento sąskaitos arba mokesčio.</span><span class="sxs-lookup"><span data-stu-id="a4021-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



