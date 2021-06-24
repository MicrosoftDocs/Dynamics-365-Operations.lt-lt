---
title: Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms
description: Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF. Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 513066a597620450f0b482e98e36d31c6f2c980a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189098"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="37450-104">Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms</span><span class="sxs-lookup"><span data-stu-id="37450-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37450-105">Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="37450-106">Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="37450-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

## <a name="accounting-distributions"></a><span data-ttu-id="37450-107">Apskaitos paskirstymai</span><span class="sxs-lookup"><span data-stu-id="37450-107">Accounting distributions</span></span> 

<span data-ttu-id="37450-108">Puslapyje Tiekėjo SF naudodami toliau nurodytus mygtukus galite peržiūrėti ir galbūt modifikuoti kiekvienos tiekėjo SF nurodytos sumos apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="37450-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="37450-109">**Paskirstyti sumas** – peržiūrėkite ir modifikuokite apskaitos paskirstymus konkrečioje eilutėje ir visose antrinėse eilutėse, pvz., mokesčių ar rinkliavų.</span><span class="sxs-lookup"><span data-stu-id="37450-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="37450-110">Antrinės eilutės apskaitos paskirstymus taip pat galite peržiūrėti ir keisti tiesiogiai iš PVM operacijų puslapio arba Išlaidų operacijų puslapio.</span><span class="sxs-lookup"><span data-stu-id="37450-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="37450-111">Modifikuokite tiekėjo SF antraštės sumas, pvz., rinkliavas arba valiutos sumos apvalinimą.</span><span class="sxs-lookup"><span data-stu-id="37450-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="37450-112">Modifikuokite tiekėjo SF eilučių sumas.</span><span class="sxs-lookup"><span data-stu-id="37450-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="37450-113">**Peržiūrėti paskirstymus** – peržiūrėkite visų dokumentų eilučių apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="37450-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="37450-114">Negalite modifikuoti apskaitos paskirstymų iš šio rodinio.</span><span class="sxs-lookup"><span data-stu-id="37450-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="37450-115">Peržiūrėkite antraštės ir eilutės sumas.</span><span class="sxs-lookup"><span data-stu-id="37450-115">View header and line amounts.</span></span>

<span data-ttu-id="37450-116">Jei tiekėjo SF nurodomas pirkimo užsakymas, galite skaidyti ir modifikuoti apskaitos paskirstymus eilutėse, kuriose nurodomos nelaikomos prekės.</span><span class="sxs-lookup"><span data-stu-id="37450-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="37450-117">Panaikinti apskaitos paskirstymą taip pat galite, jei tiekėjo SF eilutėje nenurodyta pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="37450-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="37450-118">Negalite skaidyti arba naikinti išlaidų, mokesčių ir eilutės nuolaidų eilučių.</span><span class="sxs-lookup"><span data-stu-id="37450-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="37450-119">Galite modifikuoti DK sąskaitą, bet negalite keisti sumų arba procentinių dydžių.</span><span class="sxs-lookup"><span data-stu-id="37450-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="37450-120">Jei pirminėje eilutėje yra nelaikoma prekė, o apskaitos paskirstymai padalyti, antrinė eilutė bus automatiškai padalyta, kad atitiktų pirminės eilutės finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="37450-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="37450-121">Antrinės eilutės apskaitos paskirstymų negalima dalyti papildomai arba naikinti, bet, priklausomai nuo antrinės eilutės nustatymo, galbūt galite modifikuoti antrinės eilutės apskaitos paskirstymų DK sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="37450-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="37450-122">Sumų paskirstymas</span><span class="sxs-lookup"><span data-stu-id="37450-122">Distributing amounts</span></span>
<span data-ttu-id="37450-123">Kai įvedate tiekėjo SF, kiekviena suma bus paskirstyta kaip aprašyta toliau.</span><span class="sxs-lookup"><span data-stu-id="37450-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37450-124">Tiekėjo SF eilutės tipas</span><span class="sxs-lookup"><span data-stu-id="37450-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="37450-125">Pirmenybės tvarka, kuri lemia, iš kur rodoma pagrindinė sąskaita</span><span class="sxs-lookup"><span data-stu-id="37450-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="37450-126">Pirmenybės tvarka, kuri lemia, kuri numatytoji finansinė dimensija rodoma</span><span class="sxs-lookup"><span data-stu-id="37450-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="37450-127">Laikomas produktas</span><span class="sxs-lookup"><span data-stu-id="37450-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-128">Pirkimo užsakymo eilutės apskaitos paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="37450-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-129">Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Produkto pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="37450-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-130">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-131">Naudokite numatytąsias finansines dimensijos reikšmes tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-132">Įsigijimo kategorija arba nelaikomas produktas</span><span class="sxs-lookup"><span data-stu-id="37450-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-133">Pirkimo užsakymo eilutės apskaitos paskirstymas, jei tiekėjo SF eilutėje nurodoma pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="37450-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-134">Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Išlaidų pirkimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="37450-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-135">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-136">Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="37450-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="37450-137">Naudokite numatytąsias finansines dimensijos reikšmes tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="37450-138">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-139">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37450-140">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="37450-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-141">Pirkimo užsakymo eilutės apskaitos paskirstymas, jei tiekėjo SF eilutėje nurodoma pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="37450-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-142">Formos Tiekėjo SF lauke Operacijos tipas pasirinkus Įsigijimas, laukas Pagrindinė sąskaita, kai puslapyje Ilgalaikio turto registravimo šablonai pasirinkta Įsigijimas.</span><span class="sxs-lookup"><span data-stu-id="37450-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="37450-143">Lauke Operacijos tipas pasirinkus Įsigijimo koregavimas, laukas Pagrindinė sąskaita, kai puslapyje Ilgalaikio turto registravimo šablonai pasirinkta Įsigijimo koregavimas.</span><span class="sxs-lookup"><span data-stu-id="37450-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-144">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-145">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-146">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-147">Tiekėjo SF eilutėje nurodytas projektas</span><span class="sxs-lookup"><span data-stu-id="37450-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-148">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-149">Puslapio Projektų grupės lauke Registruoti išlaidas – Prekė pasirinkus Balansas, laukas Pagrindinė sąskaita, kai puslapyje Registravimo DK nustatymai pasirinkus Išlaidos.</span><span class="sxs-lookup"><span data-stu-id="37450-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="37450-150">Puslapio Projektų grupės lauke Registruoti išlaidas – Prekė pasirinkus Pelnas ir nuostolis, laukas Pagrindinė sąskaita, kai puslapyje Registravimo DK nustatymai pasirinkus Išlaidos – Prekė.</span><span class="sxs-lookup"><span data-stu-id="37450-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-151">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37450-152">Eilutės nuolaida</span><span class="sxs-lookup"><span data-stu-id="37450-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-153">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-154">Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Nuolaida.</span><span class="sxs-lookup"><span data-stu-id="37450-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="37450-155">Jei registravimo šablone neapibrėžta nuolaidos pagrindinė sąskaita, išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-156">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-157">Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-158">Naudokite tiekėjo SF eilutės finansinės dimensijos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="37450-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-159">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-160">Pirkimo mokestis, įvestas pirkimo užsakymo eilutės skirtuke Kaina ir nuolaida</span><span class="sxs-lookup"><span data-stu-id="37450-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-161">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-162">Išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-163">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-164">Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37450-165">Eilutės mokestis</span><span class="sxs-lookup"><span data-stu-id="37450-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-166">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-167">Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta DK sąskaita, puslapio Išlaidų kodas laukas Debeto sąskaita.</span><span class="sxs-lookup"><span data-stu-id="37450-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="37450-168">Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Prekė, išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-169">Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Klientas/tiekėjas, puslapio Išlaidų kodas laukas Kredito sąskaita.</span><span class="sxs-lookup"><span data-stu-id="37450-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-170">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-171">Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-172">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-173">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-174">Mokestis su šia sąlyga:</span><span class="sxs-lookup"><span data-stu-id="37450-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="37450-175">DK parametrų puslapyje pasirinkta pasirinktis taikyti JAV apmokestinimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="37450-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="37450-176">Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="37450-177">Išplėstinės kainos arba mokesčio apskaitos paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="37450-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-178">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-179">Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-180">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37450-181">Mokestis su šiomis sąlygomis:</span><span class="sxs-lookup"><span data-stu-id="37450-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="37450-182">DK parametrų puslapyje išvalyta pasirinktis taikyti JAV apmokestinimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="37450-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="37450-183">PVM grupės laukas Naudojimo mokestis išvalomas puslapyje PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="37450-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="37450-184">Jei mokesčio sumą galima susigrąžinti, puslapio DK registravimo grupės laukas Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="37450-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="37450-185">Jei susigrąžinti mokesčio sumos negalima, išplėstinė kaina arba mokesčio apskaitos paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="37450-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-186">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-187">Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-188">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-189">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-190">Mokestis su šiomis sąlygomis:</span><span class="sxs-lookup"><span data-stu-id="37450-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="37450-191">DK parametrų puslapyje išvalyta pasirinktis taikyti JAV apmokestinimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="37450-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="37450-192">PVM grupės laukas Naudojimo mokestis pasirenkamas puslapyje PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="37450-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="37450-193">Jei mokesčio sumą galima susigrąžinti, puslapio DK registravimo grupės laukas Gautinas PVM.</span><span class="sxs-lookup"><span data-stu-id="37450-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="37450-194">Jei mokesčio sumos negalima susigrąžinti, puslapio DK registravimo grupės laukas Naudojimo mokesčio išlaidos.</span><span class="sxs-lookup"><span data-stu-id="37450-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-195">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-196">Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-197">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-198">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="37450-199">Antraštės lygmenyje pateikiamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="37450-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-200">Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta DK sąskaita, puslapio Išlaidų kodas laukas Debeto sąskaita.</span><span class="sxs-lookup"><span data-stu-id="37450-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="37450-201">Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Klientas/tiekėjas, puslapio Išlaidų kodas laukas Kredito sąskaita.</span><span class="sxs-lookup"><span data-stu-id="37450-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-202">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-203">Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="37450-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="37450-204">Naudokite finansinės dimensijos numatytojo šablono reikšmes iš tiekėjo SF antraštės.</span><span class="sxs-lookup"><span data-stu-id="37450-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="37450-205">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-206">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="37450-207">Antraštės nuolaida</span><span class="sxs-lookup"><span data-stu-id="37450-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="37450-208">Puslapio Automatinių operacijų sąskaitos registravimo tipo Tiekėjo SF nuolaida laukas Pagrindinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="37450-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="37450-209">Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37450-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="37450-210">Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</span><span class="sxs-lookup"><span data-stu-id="37450-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-211">Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="37450-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="37450-212">Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</span><span class="sxs-lookup"><span data-stu-id="37450-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a><span data-ttu-id="37450-213">Mokesčių paskirstymas</span><span class="sxs-lookup"><span data-stu-id="37450-213">Distributing taxes</span></span>

<span data-ttu-id="37450-214">Mokesčių apskaitos paskirstymus galima kurti tik apskaičiavus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="37450-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="37450-215">Norėdami skaičiuoti PVM, turite atlikti vieną iš toliau nurodytų užduočių puslapyje Tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="37450-216">Peržiūrėkite SF bendrąją sumą.</span><span class="sxs-lookup"><span data-stu-id="37450-216">View the invoice total.</span></span>
-   <span data-ttu-id="37450-217">Peržiūrėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="37450-217">View the sales tax.</span></span>
-   <span data-ttu-id="37450-218">Peržiūrėkite papildomos knygos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="37450-218">View the subledger journal.</span></span>
-   <span data-ttu-id="37450-219">Peržiūrėkite visos tiekėjo SF apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="37450-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="37450-220">Sulaikykite tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="37450-221">Registruokite tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="37450-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="37450-222">Tiekėjo SF papildomos knygos žurnalai</span><span class="sxs-lookup"><span data-stu-id="37450-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="37450-223">Prieš registruodami tiekėjo SF galite peržiūrėti visą sąskaitos faktūros apskaitos įrašą, kuris apima debetus ir kreditus, kad patikrintumėte, ar sąskaita faktūra registruojama tinkamose sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="37450-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="37450-224">Šis viso apskaitos įrašo rodinys vadinamas papildomos knygos žurnalu.</span><span class="sxs-lookup"><span data-stu-id="37450-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="37450-225">Jei papildomos knygos žurnalo įrašas neteisingas, kai peržiūrite jį prieš įtraukdami tiekėjo SF į žurnalą, negalite modifikuoti papildomos knygos žurnalo įrašo.</span><span class="sxs-lookup"><span data-stu-id="37450-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="37450-226">Bet galite modifikuoti apskaitos paskirstymus arba registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="37450-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="37450-227">Apskaitos paskirstymai naudojami norint nustatyti vieną apskaitos įrašo pusę, debetą arba kreditą.</span><span class="sxs-lookup"><span data-stu-id="37450-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="37450-228">Balansavimo papildomos knygos žurnalo sąskaitos įrašas sukuriamas naudojant registravimo profilius, pvz., iš tiekėjo sąskaitos arba mokesčio.</span><span class="sxs-lookup"><span data-stu-id="37450-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]