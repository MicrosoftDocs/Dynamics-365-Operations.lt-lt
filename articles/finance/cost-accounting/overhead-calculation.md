---
title: Pridėtinių išlaidų skaičiavimas
description: Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446103"
---
# <a name="overhead-calculation"></a><span data-ttu-id="41e44-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="41e44-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41e44-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="41e44-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="41e44-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="41e44-105">Term definition</span></span>
---------------

<span data-ttu-id="41e44-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="41e44-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="41e44-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="41e44-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="41e44-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="41e44-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="41e44-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="41e44-109">Rent</span></span>
-   <span data-ttu-id="41e44-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-110">Electricity</span></span>
-   <span data-ttu-id="41e44-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="41e44-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="41e44-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="41e44-112">Overhead calculation overview</span></span>
<span data-ttu-id="41e44-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="41e44-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="41e44-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="41e44-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="41e44-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="41e44-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="41e44-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="41e44-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="41e44-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="41e44-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="41e44-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="41e44-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="41e44-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="41e44-119">Version type</span></span>
-   <span data-ttu-id="41e44-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="41e44-120">Date and time</span></span>
-   <span data-ttu-id="41e44-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="41e44-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="41e44-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="41e44-122">Fiscal year</span></span>
-   <span data-ttu-id="41e44-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-123">Fiscal period</span></span>

<span data-ttu-id="41e44-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="41e44-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="41e44-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="41e44-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="41e44-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="41e44-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="41e44-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="41e44-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="41e44-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="41e44-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="41e44-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="41e44-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="41e44-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="41e44-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="41e44-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="41e44-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="41e44-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="41e44-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="41e44-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="41e44-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="41e44-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="41e44-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="41e44-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="41e44-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="41e44-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="41e44-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="41e44-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="41e44-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="41e44-140">Main account</span></span></th>
<th><span data-ttu-id="41e44-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="41e44-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="41e44-143">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-143">CC099</span></span></td>
<td><span data-ttu-id="41e44-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-144">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-145">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-145">10001</span></span></td>
<td><span data-ttu-id="41e44-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-146">Electricity</span></span></td>
<td><span data-ttu-id="41e44-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="41e44-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="41e44-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="41e44-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="41e44-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="41e44-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="41e44-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="41e44-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="41e44-151">Define the cost behavior rule</span></span>

<span data-ttu-id="41e44-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="41e44-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="41e44-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="41e44-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="41e44-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="41e44-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="41e44-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="41e44-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="41e44-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="41e44-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="41e44-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="41e44-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="41e44-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="41e44-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-160">Journal</span></span></th>
<th><span data-ttu-id="41e44-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="41e44-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="41e44-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="41e44-163">Versija</span><span class="sxs-lookup"><span data-stu-id="41e44-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-164">00001</span><span class="sxs-lookup"><span data-stu-id="41e44-164">00001</span></span></td>
<td><span data-ttu-id="41e44-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="41e44-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="41e44-166">Fiscal</span></span></td>
<td><span data-ttu-id="41e44-167">2017</span><span class="sxs-lookup"><span data-stu-id="41e44-167">2017</span></span></td>
<td><span data-ttu-id="41e44-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-168">Period 1</span></span></td>
<td><span data-ttu-id="41e44-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="41e44-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="41e44-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-173">Cost element</span></span></th>
<th><span data-ttu-id="41e44-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-174">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-175">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="41e44-177">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-177">CC099</span></span></td>
<td><span data-ttu-id="41e44-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-178">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-179">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-179">10001</span></span></td>
<td><span data-ttu-id="41e44-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-180">Electricity</span></span></td>
<td><span data-ttu-id="41e44-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="41e44-181">Unclassified</span></span></td>
<td><span data-ttu-id="41e44-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="41e44-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="41e44-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-185">Cost element</span></span></th>
<th><span data-ttu-id="41e44-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-186">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-187">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-187">Amount</span></span></th>
<th><span data-ttu-id="41e44-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-189">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-189">CC099</span></span></td>
<td><span data-ttu-id="41e44-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-190">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-191">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-191">10001</span></span></td>
<td><span data-ttu-id="41e44-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-192">Electricity</span></span></td>
<td><span data-ttu-id="41e44-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="41e44-193">Unclassified</span></span></td>
<td><span data-ttu-id="41e44-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-194">10,000.00</span></span></td>
<td><span data-ttu-id="41e44-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-196">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-196">CC099</span></span></td>
<td><span data-ttu-id="41e44-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-197">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-198">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-198">10001</span></span></td>
<td><span data-ttu-id="41e44-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-199">Electricity</span></span></td>
<td><span data-ttu-id="41e44-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="41e44-200">Unclassified</span></span></td>
<td><span data-ttu-id="41e44-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="41e44-201">-10,000.00</span></span></td>
<td><span data-ttu-id="41e44-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-203">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-203">CC099</span></span></td>
<td><span data-ttu-id="41e44-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-204">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-205">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-205">10001</span></span></td>
<td><span data-ttu-id="41e44-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-206">Electricity</span></span></td>
<td><span data-ttu-id="41e44-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-207">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-208">1,000.00</span></span></td>
<td><span data-ttu-id="41e44-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-210">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-210">CC099</span></span></td>
<td><span data-ttu-id="41e44-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-211">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-212">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-212">10001</span></span></td>
<td><span data-ttu-id="41e44-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-213">Electricity</span></span></td>
<td><span data-ttu-id="41e44-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-214">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="41e44-215">9,000.00</span></span></td>
<td><span data-ttu-id="41e44-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="41e44-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="41e44-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="41e44-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="41e44-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="41e44-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="41e44-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="41e44-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="41e44-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="41e44-221">Define the cost distribution rule</span></span>

<span data-ttu-id="41e44-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="41e44-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="41e44-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="41e44-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="41e44-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="41e44-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="41e44-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="41e44-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="41e44-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="41e44-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="41e44-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="41e44-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-228">Cost object</span></span></th>
<th><span data-ttu-id="41e44-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="41e44-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-230">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-230">CC001</span></span></td>
<td><span data-ttu-id="41e44-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-231">HR</span></span></td>
<td><span data-ttu-id="41e44-232">1000</span><span class="sxs-lookup"><span data-stu-id="41e44-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-233">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-233">CC002</span></span></td>
<td><span data-ttu-id="41e44-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-234">Finance</span></span></td>
<td><span data-ttu-id="41e44-235">6,000</span><span class="sxs-lookup"><span data-stu-id="41e44-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-236">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-236">CC003</span></span></td>
<td><span data-ttu-id="41e44-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-237">Assembly</span></span></td>
<td><span data-ttu-id="41e44-238">0</span><span class="sxs-lookup"><span data-stu-id="41e44-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-240">Cost object</span></span></th>
<th><span data-ttu-id="41e44-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-241">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-242">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-243">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-244">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-244">CC001</span></span></td>
<td><span data-ttu-id="41e44-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-245">HR</span></span></td>
<td><span data-ttu-id="41e44-246">1000</span><span class="sxs-lookup"><span data-stu-id="41e44-246">1,000</span></span></td>
<td><span data-ttu-id="41e44-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="41e44-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="41e44-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-249">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-249">CC002</span></span></td>
<td><span data-ttu-id="41e44-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-250">Finance</span></span></td>
<td><span data-ttu-id="41e44-251">6,000</span><span class="sxs-lookup"><span data-stu-id="41e44-251">6,000</span></span></td>
<td><span data-ttu-id="41e44-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="41e44-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="41e44-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-254">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-254">CC003</span></span></td>
<td><span data-ttu-id="41e44-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-255">Assembly</span></span></td>
<td><span data-ttu-id="41e44-256">0</span><span class="sxs-lookup"><span data-stu-id="41e44-256">0</span></span></td>
<td><span data-ttu-id="41e44-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="41e44-258">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="41e44-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="41e44-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-261">Cost object</span></span></th>
<th><span data-ttu-id="41e44-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="41e44-262">Formula</span></span></th>
<th><span data-ttu-id="41e44-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-263">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-264">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-265">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-266">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-266">CC001</span></span></td>
<td><span data-ttu-id="41e44-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-267">HR</span></span></td>
<td><span data-ttu-id="41e44-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="41e44-269">1</span><span class="sxs-lookup"><span data-stu-id="41e44-269">1</span></span></td>
<td><span data-ttu-id="41e44-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="41e44-271">500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-272">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-272">CC002</span></span></td>
<td><span data-ttu-id="41e44-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-273">Finance</span></span></td>
<td><span data-ttu-id="41e44-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="41e44-275">1</span><span class="sxs-lookup"><span data-stu-id="41e44-275">1</span></span></td>
<td><span data-ttu-id="41e44-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="41e44-277">500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-278">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-278">CC003</span></span></td>
<td><span data-ttu-id="41e44-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-279">Assembly</span></span></td>
<td><span data-ttu-id="41e44-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="41e44-281">0</span><span class="sxs-lookup"><span data-stu-id="41e44-281">0</span></span></td>
<td><span data-ttu-id="41e44-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="41e44-283">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="41e44-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-285">Journal</span></span></th>
<th><span data-ttu-id="41e44-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="41e44-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="41e44-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="41e44-288">Versija</span><span class="sxs-lookup"><span data-stu-id="41e44-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-289">00002</span><span class="sxs-lookup"><span data-stu-id="41e44-289">00002</span></span></td>
<td><span data-ttu-id="41e44-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="41e44-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="41e44-291">Fiscal</span></span></td>
<td><span data-ttu-id="41e44-292">2017</span><span class="sxs-lookup"><span data-stu-id="41e44-292">2017</span></span></td>
<td><span data-ttu-id="41e44-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-293">Period 1</span></span></td>
<td><span data-ttu-id="41e44-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="41e44-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="41e44-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-298">Cost element</span></span></th>
<th><span data-ttu-id="41e44-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-299">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-300">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-302">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-302">CC099</span></span></td>
<td><span data-ttu-id="41e44-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-303">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-304">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-304">10001</span></span></td>
<td><span data-ttu-id="41e44-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-305">Electricity</span></span></td>
<td><span data-ttu-id="41e44-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-306">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="41e44-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-309">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-309">CC099</span></span></td>
<td><span data-ttu-id="41e44-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-310">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-311">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-311">10001</span></span></td>
<td><span data-ttu-id="41e44-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-312">Electricity</span></span></td>
<td><span data-ttu-id="41e44-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-313">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="41e44-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="41e44-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="41e44-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-317">Cost element</span></span></th>
<th><span data-ttu-id="41e44-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-318">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-319">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-319">Amount</span></span></th>
<th><span data-ttu-id="41e44-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-321">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-321">CC099</span></span></td>
<td><span data-ttu-id="41e44-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-322">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-323">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-323">10001</span></span></td>
<td><span data-ttu-id="41e44-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-324">Electricity</span></span></td>
<td><span data-ttu-id="41e44-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-325">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="41e44-326">-1,000.00</span></span></td>
<td><span data-ttu-id="41e44-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-328">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-328">CC001</span></span></td>
<td><span data-ttu-id="41e44-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-329">HR</span></span></td>
<td><span data-ttu-id="41e44-330">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-330">10001</span></span></td>
<td><span data-ttu-id="41e44-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-331">Electricity</span></span></td>
<td><span data-ttu-id="41e44-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-332">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-333">500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-333">500.00</span></span></td>
<td><span data-ttu-id="41e44-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-335">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-335">CC002</span></span></td>
<td><span data-ttu-id="41e44-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-336">Finance</span></span></td>
<td><span data-ttu-id="41e44-337">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-337">10001</span></span></td>
<td><span data-ttu-id="41e44-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-338">Electricity</span></span></td>
<td><span data-ttu-id="41e44-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-339">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-340">500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-340">500.00</span></span></td>
<td><span data-ttu-id="41e44-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-342">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-342">CC099</span></span></td>
<td><span data-ttu-id="41e44-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="41e44-343">Default cost center</span></span></td>
<td><span data-ttu-id="41e44-344">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-344">10001</span></span></td>
<td><span data-ttu-id="41e44-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-345">Electricity</span></span></td>
<td><span data-ttu-id="41e44-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-346">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="41e44-347">-9,000.00</span></span></td>
<td><span data-ttu-id="41e44-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-349">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-349">CC001</span></span></td>
<td><span data-ttu-id="41e44-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-350">HR</span></span></td>
<td><span data-ttu-id="41e44-351">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-351">10001</span></span></td>
<td><span data-ttu-id="41e44-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-352">Electricity</span></span></td>
<td><span data-ttu-id="41e44-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-353">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="41e44-354">1,285.71</span></span></td>
<td><span data-ttu-id="41e44-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-356">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-356">CC002</span></span></td>
<td><span data-ttu-id="41e44-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-357">Finance</span></span></td>
<td><span data-ttu-id="41e44-358">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-358">10001</span></span></td>
<td><span data-ttu-id="41e44-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-359">Electricity</span></span></td>
<td><span data-ttu-id="41e44-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-360">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="41e44-361">7,714.29</span></span></td>
<td><span data-ttu-id="41e44-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="41e44-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="41e44-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="41e44-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="41e44-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="41e44-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="41e44-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="41e44-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="41e44-367">Define the overhead rate</span></span>

<span data-ttu-id="41e44-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="41e44-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="41e44-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-370">Cost object</span></span></th>
<th><span data-ttu-id="41e44-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="41e44-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-372">Proj 1</span></span></td>
<td><span data-ttu-id="41e44-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-373">Project 1</span></span></td>
<td><span data-ttu-id="41e44-374">3</span><span class="sxs-lookup"><span data-stu-id="41e44-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-375">Proj 2</span></span></td>
<td><span data-ttu-id="41e44-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-376">Project 2</span></span></td>
<td><span data-ttu-id="41e44-377">1</span><span class="sxs-lookup"><span data-stu-id="41e44-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="41e44-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-379">Cost object</span></span></th>
<th><span data-ttu-id="41e44-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-380">Cost element</span></span></th>
<th><span data-ttu-id="41e44-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-381">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="41e44-382">Units</span></span></th>
<th><span data-ttu-id="41e44-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="41e44-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-384">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-384">CC001</span></span></td>
<td><span data-ttu-id="41e44-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-385">HR</span></span></td>
<td><span data-ttu-id="41e44-386">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-386">10001</span></span></td>
<td><span data-ttu-id="41e44-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-387">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-388">1</span><span class="sxs-lookup"><span data-stu-id="41e44-388">1</span></span></td>
<td><span data-ttu-id="41e44-389">10</span><span class="sxs-lookup"><span data-stu-id="41e44-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-391">Cost object</span></span></th>
<th><span data-ttu-id="41e44-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-392">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-393">Cost element</span></span></th>
<th><span data-ttu-id="41e44-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-394">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-395">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-396">Proj 1</span></span></td>
<td><span data-ttu-id="41e44-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-397">Project 1</span></span></td>
<td><span data-ttu-id="41e44-398">3</span><span class="sxs-lookup"><span data-stu-id="41e44-398">3</span></span></td>
<td><span data-ttu-id="41e44-399">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-399">10001</span></span></td>
<td><span data-ttu-id="41e44-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="41e44-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="41e44-401">30,00</span><span class="sxs-lookup"><span data-stu-id="41e44-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-402">Proj 2</span></span></td>
<td><span data-ttu-id="41e44-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-403">Project 2</span></span></td>
<td><span data-ttu-id="41e44-404">1</span><span class="sxs-lookup"><span data-stu-id="41e44-404">1</span></span></td>
<td><span data-ttu-id="41e44-405">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-405">10001</span></span></td>
<td><span data-ttu-id="41e44-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="41e44-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="41e44-407">10,00</span><span class="sxs-lookup"><span data-stu-id="41e44-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="41e44-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-409">Journal</span></span></th>
<th><span data-ttu-id="41e44-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="41e44-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="41e44-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="41e44-412">Versija</span><span class="sxs-lookup"><span data-stu-id="41e44-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-413">00003</span><span class="sxs-lookup"><span data-stu-id="41e44-413">00003</span></span></td>
<td><span data-ttu-id="41e44-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="41e44-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="41e44-415">Fiscal</span></span></td>
<td><span data-ttu-id="41e44-416">2017</span><span class="sxs-lookup"><span data-stu-id="41e44-416">2017</span></span></td>
<td><span data-ttu-id="41e44-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-417">Period 1</span></span></td>
<td><span data-ttu-id="41e44-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="41e44-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="41e44-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-421">Cost object</span></span></th>
<th><span data-ttu-id="41e44-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-424">Proj 1</span></span></td>
<td><span data-ttu-id="41e44-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="41e44-426">3,00</span><span class="sxs-lookup"><span data-stu-id="41e44-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-428">Proj 2</span></span></td>
<td><span data-ttu-id="41e44-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="41e44-430">1,00</span><span class="sxs-lookup"><span data-stu-id="41e44-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="41e44-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="41e44-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-433">Cost element</span></span></th>
<th><span data-ttu-id="41e44-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-434">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-435">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-435">Amount</span></span></th>
<th><span data-ttu-id="41e44-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="41e44-437">CC0001</span></span></td>
<td><span data-ttu-id="41e44-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-438">HR</span></span></td>
<td><span data-ttu-id="41e44-439">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-439">10001</span></span></td>
<td><span data-ttu-id="41e44-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-440">Electricity</span></span></td>
<td><span data-ttu-id="41e44-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-441">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="41e44-442">-30.00</span></span></td>
<td><span data-ttu-id="41e44-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-444">Proj 1</span></span></td>
<td><span data-ttu-id="41e44-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="41e44-446">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-446">10001</span></span></td>
<td><span data-ttu-id="41e44-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-447">Electricity</span></span></td>
<td><span data-ttu-id="41e44-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-448">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-449">30,00</span><span class="sxs-lookup"><span data-stu-id="41e44-449">30.00</span></span></td>
<td><span data-ttu-id="41e44-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-451">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-451">CC001</span></span></td>
<td><span data-ttu-id="41e44-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-452">HR</span></span></td>
<td><span data-ttu-id="41e44-453">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-453">10001</span></span></td>
<td><span data-ttu-id="41e44-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-454">Electricity</span></span></td>
<td><span data-ttu-id="41e44-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-455">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="41e44-456">-10.00</span></span></td>
<td><span data-ttu-id="41e44-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-458">Proj 2</span></span></td>
<td><span data-ttu-id="41e44-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="41e44-460">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-460">10001</span></span></td>
<td><span data-ttu-id="41e44-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-461">Electricity</span></span></td>
<td><span data-ttu-id="41e44-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-462">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-463">10,00</span><span class="sxs-lookup"><span data-stu-id="41e44-463">10.00</span></span></td>
<td><span data-ttu-id="41e44-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="41e44-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="41e44-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="41e44-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="41e44-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="41e44-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="41e44-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="41e44-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="41e44-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="41e44-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="41e44-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="41e44-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="41e44-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="41e44-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="41e44-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="41e44-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="41e44-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="41e44-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="41e44-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="41e44-475">Define the cost allocation</span></span>

<span data-ttu-id="41e44-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="41e44-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="41e44-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="41e44-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="41e44-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-479">Cost object</span></span></th>
<th><span data-ttu-id="41e44-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="41e44-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-481">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-481">CC002</span></span></td>
<td><span data-ttu-id="41e44-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-482">Finance</span></span></td>
<td><span data-ttu-id="41e44-483">35</span><span class="sxs-lookup"><span data-stu-id="41e44-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-484">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-484">CC003</span></span></td>
<td><span data-ttu-id="41e44-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-485">Assembly</span></span></td>
<td><span data-ttu-id="41e44-486">55</span><span class="sxs-lookup"><span data-stu-id="41e44-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-487">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-487">CC004</span></span></td>
<td><span data-ttu-id="41e44-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-488">Packaging</span></span></td>
<td><span data-ttu-id="41e44-489">10</span><span class="sxs-lookup"><span data-stu-id="41e44-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="41e44-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="41e44-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-492">Cost object</span></span></th>
<th><span data-ttu-id="41e44-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="41e44-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-494">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-494">CC003</span></span></td>
<td><span data-ttu-id="41e44-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-495">Assembly</span></span></td>
<td><span data-ttu-id="41e44-496">65</span><span class="sxs-lookup"><span data-stu-id="41e44-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-497">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-497">CC004</span></span></td>
<td><span data-ttu-id="41e44-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-498">Packaging</span></span></td>
<td><span data-ttu-id="41e44-499">35</span><span class="sxs-lookup"><span data-stu-id="41e44-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="41e44-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="41e44-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-502">Cost object</span></span></th>
<th><span data-ttu-id="41e44-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="41e44-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-504">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-505">Product 1</span></span></td>
<td><span data-ttu-id="41e44-506">60</span><span class="sxs-lookup"><span data-stu-id="41e44-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-507">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-508">Product 2</span></span></td>
<td><span data-ttu-id="41e44-509">20</span><span class="sxs-lookup"><span data-stu-id="41e44-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="41e44-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="41e44-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="41e44-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-512">Cost object</span></span></th>
<th><span data-ttu-id="41e44-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="41e44-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-514">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-515">Product 1</span></span></td>
<td><span data-ttu-id="41e44-516">80</span><span class="sxs-lookup"><span data-stu-id="41e44-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-517">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-518">Product 2</span></span></td>
<td><span data-ttu-id="41e44-519">15</span><span class="sxs-lookup"><span data-stu-id="41e44-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="41e44-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="41e44-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="41e44-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="41e44-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="41e44-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-523">Cost object</span></span></th>
<th><span data-ttu-id="41e44-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-524">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-525">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-526">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-526">Amount</span></span></th>
<th><span data-ttu-id="41e44-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-528">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-528">CC002</span></span></td>
<td><span data-ttu-id="41e44-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-529">Finance</span></span></td>
<td><span data-ttu-id="41e44-530">35</span><span class="sxs-lookup"><span data-stu-id="41e44-530">35</span></span></td>
<td><span data-ttu-id="41e44-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="41e44-532">175.00</span><span class="sxs-lookup"><span data-stu-id="41e44-532">175.00</span></span></td>
<td><span data-ttu-id="41e44-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-534">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-534">CC003</span></span></td>
<td><span data-ttu-id="41e44-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-535">Assembly</span></span></td>
<td><span data-ttu-id="41e44-536">55</span><span class="sxs-lookup"><span data-stu-id="41e44-536">55</span></span></td>
<td><span data-ttu-id="41e44-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="41e44-538">275.00</span><span class="sxs-lookup"><span data-stu-id="41e44-538">275.00</span></span></td>
<td><span data-ttu-id="41e44-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-540">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-540">CC004</span></span></td>
<td><span data-ttu-id="41e44-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-541">Packaging</span></span></td>
<td><span data-ttu-id="41e44-542">10</span><span class="sxs-lookup"><span data-stu-id="41e44-542">10</span></span></td>
<td><span data-ttu-id="41e44-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="41e44-544">50,00</span><span class="sxs-lookup"><span data-stu-id="41e44-544">50.00</span></span></td>
<td><span data-ttu-id="41e44-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-546">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-546">CC002</span></span></td>
<td><span data-ttu-id="41e44-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-547">Finance</span></span></td>
<td><span data-ttu-id="41e44-548">35</span><span class="sxs-lookup"><span data-stu-id="41e44-548">35</span></span></td>
<td><span data-ttu-id="41e44-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="41e44-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="41e44-550">436.00</span><span class="sxs-lookup"><span data-stu-id="41e44-550">436.00</span></span></td>
<td><span data-ttu-id="41e44-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-552">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-552">CC003</span></span></td>
<td><span data-ttu-id="41e44-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-553">Assembly</span></span></td>
<td><span data-ttu-id="41e44-554">55</span><span class="sxs-lookup"><span data-stu-id="41e44-554">55</span></span></td>
<td><span data-ttu-id="41e44-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="41e44-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="41e44-556">685.14</span><span class="sxs-lookup"><span data-stu-id="41e44-556">685.14</span></span></td>
<td><span data-ttu-id="41e44-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-558">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-558">CC004</span></span></td>
<td><span data-ttu-id="41e44-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-559">Packaging</span></span></td>
<td><span data-ttu-id="41e44-560">10</span><span class="sxs-lookup"><span data-stu-id="41e44-560">10</span></span></td>
<td><span data-ttu-id="41e44-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="41e44-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="41e44-562">124.57</span><span class="sxs-lookup"><span data-stu-id="41e44-562">124.57</span></span></td>
<td><span data-ttu-id="41e44-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-565">Cost object</span></span></th>
<th><span data-ttu-id="41e44-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-566">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-567">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-568">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-568">Amount</span></span></th>
<th><span data-ttu-id="41e44-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-570">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-570">CC003</span></span></td>
<td><span data-ttu-id="41e44-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-571">Assembly</span></span></td>
<td><span data-ttu-id="41e44-572">65</span><span class="sxs-lookup"><span data-stu-id="41e44-572">65</span></span></td>
<td><span data-ttu-id="41e44-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="41e44-574">438.75</span><span class="sxs-lookup"><span data-stu-id="41e44-574">438.75</span></span></td>
<td><span data-ttu-id="41e44-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-576">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-576">CC004</span></span></td>
<td><span data-ttu-id="41e44-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-577">Packaging</span></span></td>
<td><span data-ttu-id="41e44-578">35</span><span class="sxs-lookup"><span data-stu-id="41e44-578">35</span></span></td>
<td><span data-ttu-id="41e44-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="41e44-580">236.25</span><span class="sxs-lookup"><span data-stu-id="41e44-580">236.25</span></span></td>
<td><span data-ttu-id="41e44-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-582">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-582">CC003</span></span></td>
<td><span data-ttu-id="41e44-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-583">Assembly</span></span></td>
<td><span data-ttu-id="41e44-584">65</span><span class="sxs-lookup"><span data-stu-id="41e44-584">65</span></span></td>
<td><span data-ttu-id="41e44-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="41e44-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="41e44-586">5,297.69</span></span></td>
<td><span data-ttu-id="41e44-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-588">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-588">CC004</span></span></td>
<td><span data-ttu-id="41e44-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-589">Packaging</span></span></td>
<td><span data-ttu-id="41e44-590">35</span><span class="sxs-lookup"><span data-stu-id="41e44-590">35</span></span></td>
<td><span data-ttu-id="41e44-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="41e44-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="41e44-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="41e44-592">2,852.60</span></span></td>
<td><span data-ttu-id="41e44-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-595">Cost object</span></span></th>
<th><span data-ttu-id="41e44-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-596">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-597">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-598">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-598">Amount</span></span></th>
<th><span data-ttu-id="41e44-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-600">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-601">Product 1</span></span></td>
<td><span data-ttu-id="41e44-602">60</span><span class="sxs-lookup"><span data-stu-id="41e44-602">60</span></span></td>
<td><span data-ttu-id="41e44-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="41e44-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="41e44-604">535.31</span><span class="sxs-lookup"><span data-stu-id="41e44-604">535.31</span></span></td>
<td><span data-ttu-id="41e44-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-606">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-607">Product 2</span></span></td>
<td><span data-ttu-id="41e44-608">20</span><span class="sxs-lookup"><span data-stu-id="41e44-608">20</span></span></td>
<td><span data-ttu-id="41e44-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="41e44-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="41e44-610">178.44</span><span class="sxs-lookup"><span data-stu-id="41e44-610">178.44</span></span></td>
<td><span data-ttu-id="41e44-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-612">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-613">Product 1</span></span></td>
<td><span data-ttu-id="41e44-614">60</span><span class="sxs-lookup"><span data-stu-id="41e44-614">60</span></span></td>
<td><span data-ttu-id="41e44-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="41e44-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="41e44-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="41e44-616">4,487.12</span></span></td>
<td><span data-ttu-id="41e44-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-618">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-619">Product 2</span></span></td>
<td><span data-ttu-id="41e44-620">20</span><span class="sxs-lookup"><span data-stu-id="41e44-620">20</span></span></td>
<td><span data-ttu-id="41e44-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="41e44-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="41e44-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="41e44-622">1,495.71</span></span></td>
<td><span data-ttu-id="41e44-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="41e44-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="41e44-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-625">Cost object</span></span></th>
<th><span data-ttu-id="41e44-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="41e44-626">Magnitude</span></span></th>
<th><span data-ttu-id="41e44-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="41e44-627">Allocation factor</span></span></th>
<th><span data-ttu-id="41e44-628">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-628">Amount</span></span></th>
<th><span data-ttu-id="41e44-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-630">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-631">Product 1</span></span></td>
<td><span data-ttu-id="41e44-632">80</span><span class="sxs-lookup"><span data-stu-id="41e44-632">80</span></span></td>
<td><span data-ttu-id="41e44-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="41e44-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="41e44-634">241.05</span><span class="sxs-lookup"><span data-stu-id="41e44-634">241.05</span></span></td>
<td><span data-ttu-id="41e44-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-636">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-637">Product 2</span></span></td>
<td><span data-ttu-id="41e44-638">15</span><span class="sxs-lookup"><span data-stu-id="41e44-638">15</span></span></td>
<td><span data-ttu-id="41e44-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="41e44-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="41e44-640">45.20</span><span class="sxs-lookup"><span data-stu-id="41e44-640">45.20</span></span></td>
<td><span data-ttu-id="41e44-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-642">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-643">Product 1</span></span></td>
<td><span data-ttu-id="41e44-644">80</span><span class="sxs-lookup"><span data-stu-id="41e44-644">80</span></span></td>
<td><span data-ttu-id="41e44-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="41e44-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="41e44-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="41e44-646">2,507.09</span></span></td>
<td><span data-ttu-id="41e44-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-648">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-649">Product 2</span></span></td>
<td><span data-ttu-id="41e44-650">15</span><span class="sxs-lookup"><span data-stu-id="41e44-650">15</span></span></td>
<td><span data-ttu-id="41e44-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="41e44-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="41e44-652">470.08</span><span class="sxs-lookup"><span data-stu-id="41e44-652">470.08</span></span></td>
<td><span data-ttu-id="41e44-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="41e44-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="41e44-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-655">Journal</span></span></th>
<th><span data-ttu-id="41e44-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="41e44-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="41e44-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="41e44-658">Versija</span><span class="sxs-lookup"><span data-stu-id="41e44-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-659">00004</span><span class="sxs-lookup"><span data-stu-id="41e44-659">00004</span></span></td>
<td><span data-ttu-id="41e44-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="41e44-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="41e44-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="41e44-661">Fiscal</span></span></td>
<td><span data-ttu-id="41e44-662">2017</span><span class="sxs-lookup"><span data-stu-id="41e44-662">2017</span></span></td>
<td><span data-ttu-id="41e44-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-663">Period 1</span></span></td>
<td><span data-ttu-id="41e44-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="41e44-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="41e44-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="41e44-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="41e44-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-668">Cost element</span></span></th>
<th><span data-ttu-id="41e44-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-669">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-670">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-672">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-672">CC001</span></span></td>
<td><span data-ttu-id="41e44-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-673">HR</span></span></td>
<td><span data-ttu-id="41e44-674">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-674">10001</span></span></td>
<td><span data-ttu-id="41e44-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-675">Electricity</span></span></td>
<td><span data-ttu-id="41e44-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-676">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-677">500,00</span><span class="sxs-lookup"><span data-stu-id="41e44-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-679">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-679">CC001</span></span></td>
<td><span data-ttu-id="41e44-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-680">HR</span></span></td>
<td><span data-ttu-id="41e44-681">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-681">10001</span></span></td>
<td><span data-ttu-id="41e44-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-682">Electricity</span></span></td>
<td><span data-ttu-id="41e44-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-683">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="41e44-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-686">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-686">CC002</span></span></td>
<td><span data-ttu-id="41e44-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-687">Finance</span></span></td>
<td><span data-ttu-id="41e44-688">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-688">10001</span></span></td>
<td><span data-ttu-id="41e44-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-689">Electricity</span></span></td>
<td><span data-ttu-id="41e44-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-690">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-691">675.00</span><span class="sxs-lookup"><span data-stu-id="41e44-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-693">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-693">CC002</span></span></td>
<td><span data-ttu-id="41e44-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-694">Finance</span></span></td>
<td><span data-ttu-id="41e44-695">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-695">10001</span></span></td>
<td><span data-ttu-id="41e44-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-696">Electricity</span></span></td>
<td><span data-ttu-id="41e44-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-697">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="41e44-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-700">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-700">CC003</span></span></td>
<td><span data-ttu-id="41e44-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-701">Assembly</span></span></td>
<td><span data-ttu-id="41e44-702">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-702">10001</span></span></td>
<td><span data-ttu-id="41e44-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-703">Electricity</span></span></td>
<td><span data-ttu-id="41e44-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-704">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-705">713.75</span><span class="sxs-lookup"><span data-stu-id="41e44-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-707">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-707">CC003</span></span></td>
<td><span data-ttu-id="41e44-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-708">Assembly</span></span></td>
<td><span data-ttu-id="41e44-709">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-709">10001</span></span></td>
<td><span data-ttu-id="41e44-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-710">Electricity</span></span></td>
<td><span data-ttu-id="41e44-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-711">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="41e44-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-714">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-714">CC003</span></span></td>
<td><span data-ttu-id="41e44-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-715">Packaging</span></span></td>
<td><span data-ttu-id="41e44-716">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-716">10001</span></span></td>
<td><span data-ttu-id="41e44-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-717">Electricity</span></span></td>
<td><span data-ttu-id="41e44-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-718">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-719">286.25</span><span class="sxs-lookup"><span data-stu-id="41e44-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-721">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-721">CC003</span></span></td>
<td><span data-ttu-id="41e44-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-722">Packaging</span></span></td>
<td><span data-ttu-id="41e44-723">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-723">10001</span></span></td>
<td><span data-ttu-id="41e44-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-724">Electricity</span></span></td>
<td><span data-ttu-id="41e44-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-725">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="41e44-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-728">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-729">Product 1</span></span></td>
<td><span data-ttu-id="41e44-730">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-730">10001</span></span></td>
<td><span data-ttu-id="41e44-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-731">Electricity</span></span></td>
<td><span data-ttu-id="41e44-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-732">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-733">776.36</span><span class="sxs-lookup"><span data-stu-id="41e44-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-735">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-736">Product 1</span></span></td>
<td><span data-ttu-id="41e44-737">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-737">10001</span></span></td>
<td><span data-ttu-id="41e44-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-738">Electricity</span></span></td>
<td><span data-ttu-id="41e44-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-739">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="41e44-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-742">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-743">Product 1</span></span></td>
<td><span data-ttu-id="41e44-744">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-744">10001</span></span></td>
<td><span data-ttu-id="41e44-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-745">Electricity</span></span></td>
<td><span data-ttu-id="41e44-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-746">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-747">223.64</span><span class="sxs-lookup"><span data-stu-id="41e44-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="41e44-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-749">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-750">Product 1</span></span></td>
<td><span data-ttu-id="41e44-751">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-751">10001</span></span></td>
<td><span data-ttu-id="41e44-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-752">Electricity</span></span></td>
<td><span data-ttu-id="41e44-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-753">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="41e44-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="41e44-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="41e44-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="41e44-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="41e44-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-757">Cost element</span></span></th>
<th><span data-ttu-id="41e44-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="41e44-758">Cost behavior</span></span></th>
<th><span data-ttu-id="41e44-759">Suma</span><span class="sxs-lookup"><span data-stu-id="41e44-759">Amount</span></span></th>
<th><span data-ttu-id="41e44-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="41e44-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="41e44-761">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-761">CC001</span></span></td>
<td><span data-ttu-id="41e44-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-762">HR</span></span></td>
<td><span data-ttu-id="41e44-763">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-763">10001</span></span></td>
<td><span data-ttu-id="41e44-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-764">Electricity</span></span></td>
<td><span data-ttu-id="41e44-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-765">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="41e44-766">-500.00</span></span></td>
<td><span data-ttu-id="41e44-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-768">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-768">CC002</span></span></td>
<td><span data-ttu-id="41e44-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-769">Finance</span></span></td>
<td><span data-ttu-id="41e44-770">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-770">10001</span></span></td>
<td><span data-ttu-id="41e44-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-771">Electricity</span></span></td>
<td><span data-ttu-id="41e44-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-772">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-773">175.00</span><span class="sxs-lookup"><span data-stu-id="41e44-773">175.00</span></span></td>
<td><span data-ttu-id="41e44-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-775">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-775">CC003</span></span></td>
<td><span data-ttu-id="41e44-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-776">Assembly</span></span></td>
<td><span data-ttu-id="41e44-777">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-777">10001</span></span></td>
<td><span data-ttu-id="41e44-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-778">Electricity</span></span></td>
<td><span data-ttu-id="41e44-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-779">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-780">275.00</span><span class="sxs-lookup"><span data-stu-id="41e44-780">275.00</span></span></td>
<td><span data-ttu-id="41e44-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-782">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-782">CC004</span></span></td>
<td><span data-ttu-id="41e44-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-783">Packaging</span></span></td>
<td><span data-ttu-id="41e44-784">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-784">10001</span></span></td>
<td><span data-ttu-id="41e44-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-785">Electricity</span></span></td>
<td><span data-ttu-id="41e44-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-786">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-787">50,00</span><span class="sxs-lookup"><span data-stu-id="41e44-787">50,00</span></span></td>
<td><span data-ttu-id="41e44-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-789">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-789">CC001</span></span></td>
<td><span data-ttu-id="41e44-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="41e44-790">HR</span></span></td>
<td><span data-ttu-id="41e44-791">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-791">10001</span></span></td>
<td><span data-ttu-id="41e44-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-792">Electricity</span></span></td>
<td><span data-ttu-id="41e44-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-793">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="41e44-794">-1,245.71</span></span></td>
<td><span data-ttu-id="41e44-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-796">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-796">CC002</span></span></td>
<td><span data-ttu-id="41e44-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-797">Finance</span></span></td>
<td><span data-ttu-id="41e44-798">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-798">10001</span></span></td>
<td><span data-ttu-id="41e44-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-799">Electricity</span></span></td>
<td><span data-ttu-id="41e44-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-800">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-801">436.00</span><span class="sxs-lookup"><span data-stu-id="41e44-801">436.00</span></span></td>
<td><span data-ttu-id="41e44-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-803">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-803">CC003</span></span></td>
<td><span data-ttu-id="41e44-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-804">Assembly</span></span></td>
<td><span data-ttu-id="41e44-805">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-805">10001</span></span></td>
<td><span data-ttu-id="41e44-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-806">Electricity</span></span></td>
<td><span data-ttu-id="41e44-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-807">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-808">685.14</span><span class="sxs-lookup"><span data-stu-id="41e44-808">685.14</span></span></td>
<td><span data-ttu-id="41e44-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-810">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-810">CC004</span></span></td>
<td><span data-ttu-id="41e44-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-811">Packaging</span></span></td>
<td><span data-ttu-id="41e44-812">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-812">10001</span></span></td>
<td><span data-ttu-id="41e44-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-813">Electricity</span></span></td>
<td><span data-ttu-id="41e44-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-814">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-815">124.57</span><span class="sxs-lookup"><span data-stu-id="41e44-815">124.57</span></span></td>
<td><span data-ttu-id="41e44-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-817">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-817">CC002</span></span></td>
<td><span data-ttu-id="41e44-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-818">Finance</span></span></td>
<td><span data-ttu-id="41e44-819">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-819">10001</span></span></td>
<td><span data-ttu-id="41e44-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-820">Electricity</span></span></td>
<td><span data-ttu-id="41e44-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-821">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="41e44-822">-675.00</span></span></td>
<td><span data-ttu-id="41e44-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-824">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-824">CC003</span></span></td>
<td><span data-ttu-id="41e44-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-825">Assembly</span></span></td>
<td><span data-ttu-id="41e44-826">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-826">10001</span></span></td>
<td><span data-ttu-id="41e44-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-827">Electricity</span></span></td>
<td><span data-ttu-id="41e44-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-828">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-829">438.75</span><span class="sxs-lookup"><span data-stu-id="41e44-829">438.75</span></span></td>
<td><span data-ttu-id="41e44-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-831">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-831">CC004</span></span></td>
<td><span data-ttu-id="41e44-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-832">Packaging</span></span></td>
<td><span data-ttu-id="41e44-833">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-833">10001</span></span></td>
<td><span data-ttu-id="41e44-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-834">Electricity</span></span></td>
<td><span data-ttu-id="41e44-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-835">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-836">236.25</span><span class="sxs-lookup"><span data-stu-id="41e44-836">236.25</span></span></td>
<td><span data-ttu-id="41e44-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-838">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-838">CC002</span></span></td>
<td><span data-ttu-id="41e44-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="41e44-839">Finance</span></span></td>
<td><span data-ttu-id="41e44-840">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-840">10001</span></span></td>
<td><span data-ttu-id="41e44-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-841">Electricity</span></span></td>
<td><span data-ttu-id="41e44-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-842">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="41e44-843">-8,150.29</span></span></td>
<td><span data-ttu-id="41e44-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-845">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-845">CC003</span></span></td>
<td><span data-ttu-id="41e44-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-846">Assembly</span></span></td>
<td><span data-ttu-id="41e44-847">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-847">10001</span></span></td>
<td><span data-ttu-id="41e44-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-848">Electricity</span></span></td>
<td><span data-ttu-id="41e44-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-849">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="41e44-850">5,297.69</span></span></td>
<td><span data-ttu-id="41e44-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-852">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-852">CC004</span></span></td>
<td><span data-ttu-id="41e44-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="41e44-853">Packaging</span></span></td>
<td><span data-ttu-id="41e44-854">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-854">10001</span></span></td>
<td><span data-ttu-id="41e44-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-855">Electricity</span></span></td>
<td><span data-ttu-id="41e44-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-856">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="41e44-857">2,852.60</span></span></td>
<td><span data-ttu-id="41e44-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-859">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-859">CC003</span></span></td>
<td><span data-ttu-id="41e44-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-860">Assembly</span></span></td>
<td><span data-ttu-id="41e44-861">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-861">10001</span></span></td>
<td><span data-ttu-id="41e44-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-862">Electricity</span></span></td>
<td><span data-ttu-id="41e44-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-863">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="41e44-864">-713.75</span></span></td>
<td><span data-ttu-id="41e44-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-866">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-867">Product 1</span></span></td>
<td><span data-ttu-id="41e44-868">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-868">10001</span></span></td>
<td><span data-ttu-id="41e44-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-869">Electricity</span></span></td>
<td><span data-ttu-id="41e44-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-870">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-871">535.31</span><span class="sxs-lookup"><span data-stu-id="41e44-871">535.31</span></span></td>
<td><span data-ttu-id="41e44-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-873">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-874">Product 2</span></span></td>
<td><span data-ttu-id="41e44-875">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-875">10001</span></span></td>
<td><span data-ttu-id="41e44-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-876">Electricity</span></span></td>
<td><span data-ttu-id="41e44-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-877">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-878">178.44</span><span class="sxs-lookup"><span data-stu-id="41e44-878">178.44</span></span></td>
<td><span data-ttu-id="41e44-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-880">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-880">CC003</span></span></td>
<td><span data-ttu-id="41e44-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-881">Assembly</span></span></td>
<td><span data-ttu-id="41e44-882">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-882">10001</span></span></td>
<td><span data-ttu-id="41e44-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-883">Electricity</span></span></td>
<td><span data-ttu-id="41e44-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-884">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="41e44-885">-5,982.83</span></span></td>
<td><span data-ttu-id="41e44-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-887">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-888">Product 1</span></span></td>
<td><span data-ttu-id="41e44-889">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-889">10001</span></span></td>
<td><span data-ttu-id="41e44-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-890">Electricity</span></span></td>
<td><span data-ttu-id="41e44-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-891">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="41e44-892">4,487.12</span></span></td>
<td><span data-ttu-id="41e44-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-894">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-895">Product 2</span></span></td>
<td><span data-ttu-id="41e44-896">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-896">10001</span></span></td>
<td><span data-ttu-id="41e44-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-897">Electricity</span></span></td>
<td><span data-ttu-id="41e44-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-898">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="41e44-899">1,495.71</span></span></td>
<td><span data-ttu-id="41e44-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-901">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-901">CC003</span></span></td>
<td><span data-ttu-id="41e44-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-902">Assembly</span></span></td>
<td><span data-ttu-id="41e44-903">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-903">10001</span></span></td>
<td><span data-ttu-id="41e44-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-904">Electricity</span></span></td>
<td><span data-ttu-id="41e44-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-905">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="41e44-906">-286.25</span></span></td>
<td><span data-ttu-id="41e44-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-908">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-909">Product 1</span></span></td>
<td><span data-ttu-id="41e44-910">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-910">10001</span></span></td>
<td><span data-ttu-id="41e44-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-911">Electricity</span></span></td>
<td><span data-ttu-id="41e44-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-912">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-913">241.05</span><span class="sxs-lookup"><span data-stu-id="41e44-913">241.05</span></span></td>
<td><span data-ttu-id="41e44-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-915">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-916">Product 2</span></span></td>
<td><span data-ttu-id="41e44-917">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-917">10001</span></span></td>
<td><span data-ttu-id="41e44-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-918">Electricity</span></span></td>
<td><span data-ttu-id="41e44-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-919">Fixed cost</span></span></td>
<td><span data-ttu-id="41e44-920">45.20</span><span class="sxs-lookup"><span data-stu-id="41e44-920">45.20</span></span></td>
<td><span data-ttu-id="41e44-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-922">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-922">CC003</span></span></td>
<td><span data-ttu-id="41e44-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="41e44-923">Assembly</span></span></td>
<td><span data-ttu-id="41e44-924">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-924">10001</span></span></td>
<td><span data-ttu-id="41e44-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-925">Electricity</span></span></td>
<td><span data-ttu-id="41e44-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-926">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="41e44-927">-2,977.17</span></span></td>
<td><span data-ttu-id="41e44-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-929">Prod 1</span></span></td>
<td><span data-ttu-id="41e44-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-930">Product 1</span></span></td>
<td><span data-ttu-id="41e44-931">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-931">10001</span></span></td>
<td><span data-ttu-id="41e44-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-932">Electricity</span></span></td>
<td><span data-ttu-id="41e44-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-933">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="41e44-934">2,507.09</span></span></td>
<td><span data-ttu-id="41e44-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="41e44-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-936">Prod 2</span></span></td>
<td><span data-ttu-id="41e44-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="41e44-937">Product 2</span></span></td>
<td><span data-ttu-id="41e44-938">10001</span><span class="sxs-lookup"><span data-stu-id="41e44-938">10001</span></span></td>
<td><span data-ttu-id="41e44-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-939">Electricity</span></span></td>
<td><span data-ttu-id="41e44-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-940">Variable cost</span></span></td>
<td><span data-ttu-id="41e44-941">470.08</span><span class="sxs-lookup"><span data-stu-id="41e44-941">470.08</span></span></td>
<td><span data-ttu-id="41e44-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="41e44-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="41e44-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="41e44-943">Conclusion</span></span>
<span data-ttu-id="41e44-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="41e44-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="41e44-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="41e44-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="41e44-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="41e44-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="41e44-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="41e44-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="41e44-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="41e44-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="41e44-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="41e44-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="41e44-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="41e44-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="41e44-951">CC099</span><span class="sxs-lookup"><span data-stu-id="41e44-951">CC099</span></span></th>
<th><span data-ttu-id="41e44-952">CC001</span><span class="sxs-lookup"><span data-stu-id="41e44-952">CC001</span></span></th>
<th><span data-ttu-id="41e44-953">CC002</span><span class="sxs-lookup"><span data-stu-id="41e44-953">CC002</span></span></th>
<th><span data-ttu-id="41e44-954">CC003</span><span class="sxs-lookup"><span data-stu-id="41e44-954">CC003</span></span></th>
<th><span data-ttu-id="41e44-955">CC004</span><span class="sxs-lookup"><span data-stu-id="41e44-955">CC004</span></span></th>
<th><span data-ttu-id="41e44-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-956">Proj 1</span></span></th>
<th><span data-ttu-id="41e44-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="41e44-957">Proj 2</span></span></th>
<th><span data-ttu-id="41e44-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-958">Prod 1</span></span></th>
<th><span data-ttu-id="41e44-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="41e44-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="41e44-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="41e44-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="41e44-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="41e44-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="41e44-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-971">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="41e44-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-973">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-974">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-975">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-976">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-977">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="41e44-978">776.36</span><span class="sxs-lookup"><span data-stu-id="41e44-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-979">223.64</span><span class="sxs-lookup"><span data-stu-id="41e44-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="41e44-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="41e44-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-982">000</span><span class="sxs-lookup"><span data-stu-id="41e44-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-983">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-984">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-985">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-986">0,00</span><span class="sxs-lookup"><span data-stu-id="41e44-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-987">30,00</span><span class="sxs-lookup"><span data-stu-id="41e44-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-988">10,00</span><span class="sxs-lookup"><span data-stu-id="41e44-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="41e44-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="41e44-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="41e44-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="41e44-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="41e44-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="41e44-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="41e44-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="41e44-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="41e44-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="41e44-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="41e44-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="41e44-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="41e44-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="41e44-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



