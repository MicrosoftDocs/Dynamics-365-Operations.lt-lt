---
title: Pridėtinių išlaidų skaičiavimas
description: Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188002"
---
# <a name="overhead-calculation"></a><span data-ttu-id="09ad8-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09ad8-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="09ad8-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="09ad8-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="09ad8-105">Term definition</span></span>

<span data-ttu-id="09ad8-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="09ad8-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="09ad8-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="09ad8-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="09ad8-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="09ad8-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="09ad8-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="09ad8-109">Rent</span></span>
-   <span data-ttu-id="09ad8-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-110">Electricity</span></span>
-   <span data-ttu-id="09ad8-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="09ad8-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="09ad8-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="09ad8-112">Overhead calculation overview</span></span>
<span data-ttu-id="09ad8-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="09ad8-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="09ad8-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="09ad8-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="09ad8-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="09ad8-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="09ad8-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="09ad8-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="09ad8-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="09ad8-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="09ad8-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="09ad8-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="09ad8-119">Version type</span></span>
-   <span data-ttu-id="09ad8-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="09ad8-120">Date and time</span></span>
-   <span data-ttu-id="09ad8-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="09ad8-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="09ad8-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="09ad8-122">Fiscal year</span></span>
-   <span data-ttu-id="09ad8-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-123">Fiscal period</span></span>

<span data-ttu-id="09ad8-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="09ad8-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="09ad8-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="09ad8-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="09ad8-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="09ad8-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="09ad8-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="09ad8-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="09ad8-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="09ad8-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="09ad8-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="09ad8-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="09ad8-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="09ad8-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="09ad8-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="09ad8-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="09ad8-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="09ad8-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="09ad8-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="09ad8-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="09ad8-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="09ad8-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="09ad8-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="09ad8-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="09ad8-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="09ad8-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="09ad8-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="09ad8-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="09ad8-140">Main account</span></span></th>
<th><span data-ttu-id="09ad8-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="09ad8-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="09ad8-143">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-143">CC099</span></span></td>
<td><span data-ttu-id="09ad8-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-144">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-145">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-145">10001</span></span></td>
<td><span data-ttu-id="09ad8-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-146">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="09ad8-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="09ad8-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="09ad8-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="09ad8-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="09ad8-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="09ad8-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="09ad8-151">Define the cost behavior rule</span></span>

<span data-ttu-id="09ad8-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="09ad8-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="09ad8-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="09ad8-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="09ad8-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="09ad8-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="09ad8-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="09ad8-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="09ad8-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="09ad8-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="09ad8-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="09ad8-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="09ad8-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-160">Journal</span></span></th>
<th><span data-ttu-id="09ad8-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="09ad8-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="09ad8-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="09ad8-163">Versija</span><span class="sxs-lookup"><span data-stu-id="09ad8-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-164">00001</span><span class="sxs-lookup"><span data-stu-id="09ad8-164">00001</span></span></td>
<td><span data-ttu-id="09ad8-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="09ad8-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="09ad8-166">Fiscal</span></span></td>
<td><span data-ttu-id="09ad8-167">2017</span><span class="sxs-lookup"><span data-stu-id="09ad8-167">2017</span></span></td>
<td><span data-ttu-id="09ad8-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-168">Period 1</span></span></td>
<td><span data-ttu-id="09ad8-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="09ad8-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="09ad8-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-173">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-174">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-175">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="09ad8-177">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-177">CC099</span></span></td>
<td><span data-ttu-id="09ad8-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-178">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-179">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-179">10001</span></span></td>
<td><span data-ttu-id="09ad8-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-180">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="09ad8-181">Unclassified</span></span></td>
<td><span data-ttu-id="09ad8-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="09ad8-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="09ad8-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-185">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-186">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-187">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-187">Amount</span></span></th>
<th><span data-ttu-id="09ad8-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-189">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-189">CC099</span></span></td>
<td><span data-ttu-id="09ad8-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-190">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-191">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-191">10001</span></span></td>
<td><span data-ttu-id="09ad8-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-192">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="09ad8-193">Unclassified</span></span></td>
<td><span data-ttu-id="09ad8-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-194">10,000.00</span></span></td>
<td><span data-ttu-id="09ad8-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-196">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-196">CC099</span></span></td>
<td><span data-ttu-id="09ad8-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-197">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-198">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-198">10001</span></span></td>
<td><span data-ttu-id="09ad8-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-199">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="09ad8-200">Unclassified</span></span></td>
<td><span data-ttu-id="09ad8-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-201">-10,000.00</span></span></td>
<td><span data-ttu-id="09ad8-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-203">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-203">CC099</span></span></td>
<td><span data-ttu-id="09ad8-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-204">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-205">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-205">10001</span></span></td>
<td><span data-ttu-id="09ad8-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-206">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-207">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-208">1,000.00</span></span></td>
<td><span data-ttu-id="09ad8-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-210">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-210">CC099</span></span></td>
<td><span data-ttu-id="09ad8-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-211">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-212">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-212">10001</span></span></td>
<td><span data-ttu-id="09ad8-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-213">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-214">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-215">9,000.00</span></span></td>
<td><span data-ttu-id="09ad8-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="09ad8-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="09ad8-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="09ad8-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="09ad8-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="09ad8-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="09ad8-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="09ad8-221">Define the cost distribution rule</span></span>

<span data-ttu-id="09ad8-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="09ad8-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="09ad8-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="09ad8-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="09ad8-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="09ad8-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="09ad8-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="09ad8-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="09ad8-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="09ad8-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="09ad8-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="09ad8-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-228">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="09ad8-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-230">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-230">CC001</span></span></td>
<td><span data-ttu-id="09ad8-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-231">HR</span></span></td>
<td><span data-ttu-id="09ad8-232">1000</span><span class="sxs-lookup"><span data-stu-id="09ad8-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-233">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-233">CC002</span></span></td>
<td><span data-ttu-id="09ad8-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-234">Finance</span></span></td>
<td><span data-ttu-id="09ad8-235">6,000</span><span class="sxs-lookup"><span data-stu-id="09ad8-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-236">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-236">CC003</span></span></td>
<td><span data-ttu-id="09ad8-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-237">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-238">0</span><span class="sxs-lookup"><span data-stu-id="09ad8-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-240">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-241">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-242">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-243">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-244">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-244">CC001</span></span></td>
<td><span data-ttu-id="09ad8-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-245">HR</span></span></td>
<td><span data-ttu-id="09ad8-246">1000</span><span class="sxs-lookup"><span data-stu-id="09ad8-246">1,000</span></span></td>
<td><span data-ttu-id="09ad8-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="09ad8-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-249">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-249">CC002</span></span></td>
<td><span data-ttu-id="09ad8-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-250">Finance</span></span></td>
<td><span data-ttu-id="09ad8-251">6,000</span><span class="sxs-lookup"><span data-stu-id="09ad8-251">6,000</span></span></td>
<td><span data-ttu-id="09ad8-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="09ad8-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="09ad8-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-254">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-254">CC003</span></span></td>
<td><span data-ttu-id="09ad8-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-255">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-256">0</span><span class="sxs-lookup"><span data-stu-id="09ad8-256">0</span></span></td>
<td><span data-ttu-id="09ad8-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="09ad8-258">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="09ad8-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-261">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="09ad8-262">Formula</span></span></th>
<th><span data-ttu-id="09ad8-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-263">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-264">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-265">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-266">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-266">CC001</span></span></td>
<td><span data-ttu-id="09ad8-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-267">HR</span></span></td>
<td><span data-ttu-id="09ad8-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="09ad8-269">1</span><span class="sxs-lookup"><span data-stu-id="09ad8-269">1</span></span></td>
<td><span data-ttu-id="09ad8-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="09ad8-271">500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-272">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-272">CC002</span></span></td>
<td><span data-ttu-id="09ad8-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-273">Finance</span></span></td>
<td><span data-ttu-id="09ad8-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="09ad8-275">1</span><span class="sxs-lookup"><span data-stu-id="09ad8-275">1</span></span></td>
<td><span data-ttu-id="09ad8-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="09ad8-277">500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-278">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-278">CC003</span></span></td>
<td><span data-ttu-id="09ad8-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-279">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="09ad8-281">0</span><span class="sxs-lookup"><span data-stu-id="09ad8-281">0</span></span></td>
<td><span data-ttu-id="09ad8-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="09ad8-283">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="09ad8-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-285">Journal</span></span></th>
<th><span data-ttu-id="09ad8-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="09ad8-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="09ad8-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="09ad8-288">Versija</span><span class="sxs-lookup"><span data-stu-id="09ad8-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-289">00002</span><span class="sxs-lookup"><span data-stu-id="09ad8-289">00002</span></span></td>
<td><span data-ttu-id="09ad8-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="09ad8-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="09ad8-291">Fiscal</span></span></td>
<td><span data-ttu-id="09ad8-292">2017</span><span class="sxs-lookup"><span data-stu-id="09ad8-292">2017</span></span></td>
<td><span data-ttu-id="09ad8-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-293">Period 1</span></span></td>
<td><span data-ttu-id="09ad8-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="09ad8-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="09ad8-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-298">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-299">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-300">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-302">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-302">CC099</span></span></td>
<td><span data-ttu-id="09ad8-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-303">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-304">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-304">10001</span></span></td>
<td><span data-ttu-id="09ad8-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-305">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-306">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-309">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-309">CC099</span></span></td>
<td><span data-ttu-id="09ad8-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-310">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-311">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-311">10001</span></span></td>
<td><span data-ttu-id="09ad8-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-312">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-313">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="09ad8-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="09ad8-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-317">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-318">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-319">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-319">Amount</span></span></th>
<th><span data-ttu-id="09ad8-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-321">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-321">CC099</span></span></td>
<td><span data-ttu-id="09ad8-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-322">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-323">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-323">10001</span></span></td>
<td><span data-ttu-id="09ad8-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-324">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-325">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-326">-1,000.00</span></span></td>
<td><span data-ttu-id="09ad8-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-328">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-328">CC001</span></span></td>
<td><span data-ttu-id="09ad8-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-329">HR</span></span></td>
<td><span data-ttu-id="09ad8-330">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-330">10001</span></span></td>
<td><span data-ttu-id="09ad8-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-331">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-332">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-333">500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-333">500.00</span></span></td>
<td><span data-ttu-id="09ad8-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-335">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-335">CC002</span></span></td>
<td><span data-ttu-id="09ad8-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-336">Finance</span></span></td>
<td><span data-ttu-id="09ad8-337">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-337">10001</span></span></td>
<td><span data-ttu-id="09ad8-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-338">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-339">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-340">500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-340">500.00</span></span></td>
<td><span data-ttu-id="09ad8-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-342">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-342">CC099</span></span></td>
<td><span data-ttu-id="09ad8-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="09ad8-343">Default cost center</span></span></td>
<td><span data-ttu-id="09ad8-344">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-344">10001</span></span></td>
<td><span data-ttu-id="09ad8-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-345">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-346">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-347">-9,000.00</span></span></td>
<td><span data-ttu-id="09ad8-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-349">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-349">CC001</span></span></td>
<td><span data-ttu-id="09ad8-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-350">HR</span></span></td>
<td><span data-ttu-id="09ad8-351">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-351">10001</span></span></td>
<td><span data-ttu-id="09ad8-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-352">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-353">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-354">1,285.71</span></span></td>
<td><span data-ttu-id="09ad8-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-356">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-356">CC002</span></span></td>
<td><span data-ttu-id="09ad8-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-357">Finance</span></span></td>
<td><span data-ttu-id="09ad8-358">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-358">10001</span></span></td>
<td><span data-ttu-id="09ad8-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-359">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-360">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="09ad8-361">7,714.29</span></span></td>
<td><span data-ttu-id="09ad8-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="09ad8-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="09ad8-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="09ad8-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="09ad8-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="09ad8-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="09ad8-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="09ad8-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="09ad8-367">Define the overhead rate</span></span>

<span data-ttu-id="09ad8-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="09ad8-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-370">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="09ad8-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-372">Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-373">Project 1</span></span></td>
<td><span data-ttu-id="09ad8-374">3</span><span class="sxs-lookup"><span data-stu-id="09ad8-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-375">Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-376">Project 2</span></span></td>
<td><span data-ttu-id="09ad8-377">1</span><span class="sxs-lookup"><span data-stu-id="09ad8-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="09ad8-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-379">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-380">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-381">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="09ad8-382">Units</span></span></th>
<th><span data-ttu-id="09ad8-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="09ad8-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-384">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-384">CC001</span></span></td>
<td><span data-ttu-id="09ad8-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-385">HR</span></span></td>
<td><span data-ttu-id="09ad8-386">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-386">10001</span></span></td>
<td><span data-ttu-id="09ad8-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-387">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-388">1</span><span class="sxs-lookup"><span data-stu-id="09ad8-388">1</span></span></td>
<td><span data-ttu-id="09ad8-389">10</span><span class="sxs-lookup"><span data-stu-id="09ad8-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-391">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-392">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-393">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-394">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-395">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-396">Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-397">Project 1</span></span></td>
<td><span data-ttu-id="09ad8-398">3</span><span class="sxs-lookup"><span data-stu-id="09ad8-398">3</span></span></td>
<td><span data-ttu-id="09ad8-399">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-399">10001</span></span></td>
<td><span data-ttu-id="09ad8-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="09ad8-401">30,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-402">Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-403">Project 2</span></span></td>
<td><span data-ttu-id="09ad8-404">1</span><span class="sxs-lookup"><span data-stu-id="09ad8-404">1</span></span></td>
<td><span data-ttu-id="09ad8-405">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-405">10001</span></span></td>
<td><span data-ttu-id="09ad8-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="09ad8-407">10,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="09ad8-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-409">Journal</span></span></th>
<th><span data-ttu-id="09ad8-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="09ad8-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="09ad8-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="09ad8-412">Versija</span><span class="sxs-lookup"><span data-stu-id="09ad8-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-413">00003</span><span class="sxs-lookup"><span data-stu-id="09ad8-413">00003</span></span></td>
<td><span data-ttu-id="09ad8-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="09ad8-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="09ad8-415">Fiscal</span></span></td>
<td><span data-ttu-id="09ad8-416">2017</span><span class="sxs-lookup"><span data-stu-id="09ad8-416">2017</span></span></td>
<td><span data-ttu-id="09ad8-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-417">Period 1</span></span></td>
<td><span data-ttu-id="09ad8-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="09ad8-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="09ad8-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-421">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-424">Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-426">3,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-428">Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-430">1,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="09ad8-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="09ad8-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-433">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-434">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-435">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-435">Amount</span></span></th>
<th><span data-ttu-id="09ad8-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="09ad8-437">CC0001</span></span></td>
<td><span data-ttu-id="09ad8-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-438">HR</span></span></td>
<td><span data-ttu-id="09ad8-439">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-439">10001</span></span></td>
<td><span data-ttu-id="09ad8-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-440">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-441">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-442">-30.00</span></span></td>
<td><span data-ttu-id="09ad8-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-444">Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="09ad8-446">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-446">10001</span></span></td>
<td><span data-ttu-id="09ad8-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-447">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-448">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-449">30,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-449">30.00</span></span></td>
<td><span data-ttu-id="09ad8-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-451">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-451">CC001</span></span></td>
<td><span data-ttu-id="09ad8-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-452">HR</span></span></td>
<td><span data-ttu-id="09ad8-453">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-453">10001</span></span></td>
<td><span data-ttu-id="09ad8-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-454">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-455">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-456">-10.00</span></span></td>
<td><span data-ttu-id="09ad8-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-458">Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="09ad8-460">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-460">10001</span></span></td>
<td><span data-ttu-id="09ad8-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-461">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-462">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-463">10,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-463">10.00</span></span></td>
<td><span data-ttu-id="09ad8-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="09ad8-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="09ad8-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="09ad8-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="09ad8-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="09ad8-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="09ad8-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="09ad8-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="09ad8-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="09ad8-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="09ad8-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="09ad8-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="09ad8-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="09ad8-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="09ad8-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="09ad8-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="09ad8-475">Define the cost allocation</span></span>

<span data-ttu-id="09ad8-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="09ad8-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="09ad8-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-479">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="09ad8-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-481">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-481">CC002</span></span></td>
<td><span data-ttu-id="09ad8-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-482">Finance</span></span></td>
<td><span data-ttu-id="09ad8-483">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-484">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-484">CC003</span></span></td>
<td><span data-ttu-id="09ad8-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-485">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-486">55</span><span class="sxs-lookup"><span data-stu-id="09ad8-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-487">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-487">CC004</span></span></td>
<td><span data-ttu-id="09ad8-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-488">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-489">10</span><span class="sxs-lookup"><span data-stu-id="09ad8-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="09ad8-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-492">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="09ad8-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-494">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-494">CC003</span></span></td>
<td><span data-ttu-id="09ad8-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-495">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-496">65</span><span class="sxs-lookup"><span data-stu-id="09ad8-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-497">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-497">CC004</span></span></td>
<td><span data-ttu-id="09ad8-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-498">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-499">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="09ad8-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-502">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="09ad8-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-504">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-505">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-506">60</span><span class="sxs-lookup"><span data-stu-id="09ad8-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-507">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-508">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-509">20</span><span class="sxs-lookup"><span data-stu-id="09ad8-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="09ad8-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09ad8-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-512">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="09ad8-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-514">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-515">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-516">80</span><span class="sxs-lookup"><span data-stu-id="09ad8-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-517">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-518">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-519">15</span><span class="sxs-lookup"><span data-stu-id="09ad8-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="09ad8-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="09ad8-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="09ad8-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="09ad8-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="09ad8-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-523">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-524">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-525">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-526">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-526">Amount</span></span></th>
<th><span data-ttu-id="09ad8-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-528">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-528">CC002</span></span></td>
<td><span data-ttu-id="09ad8-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-529">Finance</span></span></td>
<td><span data-ttu-id="09ad8-530">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-530">35</span></span></td>
<td><span data-ttu-id="09ad8-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="09ad8-532">175.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-532">175.00</span></span></td>
<td><span data-ttu-id="09ad8-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-534">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-534">CC003</span></span></td>
<td><span data-ttu-id="09ad8-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-535">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-536">55</span><span class="sxs-lookup"><span data-stu-id="09ad8-536">55</span></span></td>
<td><span data-ttu-id="09ad8-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="09ad8-538">275.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-538">275.00</span></span></td>
<td><span data-ttu-id="09ad8-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-540">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-540">CC004</span></span></td>
<td><span data-ttu-id="09ad8-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-541">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-542">10</span><span class="sxs-lookup"><span data-stu-id="09ad8-542">10</span></span></td>
<td><span data-ttu-id="09ad8-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="09ad8-544">50,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-544">50.00</span></span></td>
<td><span data-ttu-id="09ad8-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-546">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-546">CC002</span></span></td>
<td><span data-ttu-id="09ad8-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-547">Finance</span></span></td>
<td><span data-ttu-id="09ad8-548">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-548">35</span></span></td>
<td><span data-ttu-id="09ad8-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="09ad8-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="09ad8-550">436.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-550">436.00</span></span></td>
<td><span data-ttu-id="09ad8-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-552">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-552">CC003</span></span></td>
<td><span data-ttu-id="09ad8-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-553">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-554">55</span><span class="sxs-lookup"><span data-stu-id="09ad8-554">55</span></span></td>
<td><span data-ttu-id="09ad8-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="09ad8-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="09ad8-556">685.14</span><span class="sxs-lookup"><span data-stu-id="09ad8-556">685.14</span></span></td>
<td><span data-ttu-id="09ad8-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-558">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-558">CC004</span></span></td>
<td><span data-ttu-id="09ad8-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-559">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-560">10</span><span class="sxs-lookup"><span data-stu-id="09ad8-560">10</span></span></td>
<td><span data-ttu-id="09ad8-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="09ad8-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="09ad8-562">124.57</span><span class="sxs-lookup"><span data-stu-id="09ad8-562">124.57</span></span></td>
<td><span data-ttu-id="09ad8-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-565">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-566">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-567">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-568">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-568">Amount</span></span></th>
<th><span data-ttu-id="09ad8-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-570">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-570">CC003</span></span></td>
<td><span data-ttu-id="09ad8-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-571">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-572">65</span><span class="sxs-lookup"><span data-stu-id="09ad8-572">65</span></span></td>
<td><span data-ttu-id="09ad8-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="09ad8-574">438.75</span><span class="sxs-lookup"><span data-stu-id="09ad8-574">438.75</span></span></td>
<td><span data-ttu-id="09ad8-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-576">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-576">CC004</span></span></td>
<td><span data-ttu-id="09ad8-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-577">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-578">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-578">35</span></span></td>
<td><span data-ttu-id="09ad8-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="09ad8-580">236.25</span><span class="sxs-lookup"><span data-stu-id="09ad8-580">236.25</span></span></td>
<td><span data-ttu-id="09ad8-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-582">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-582">CC003</span></span></td>
<td><span data-ttu-id="09ad8-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-583">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-584">65</span><span class="sxs-lookup"><span data-stu-id="09ad8-584">65</span></span></td>
<td><span data-ttu-id="09ad8-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="09ad8-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="09ad8-586">5,297.69</span></span></td>
<td><span data-ttu-id="09ad8-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-588">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-588">CC004</span></span></td>
<td><span data-ttu-id="09ad8-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-589">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-590">35</span><span class="sxs-lookup"><span data-stu-id="09ad8-590">35</span></span></td>
<td><span data-ttu-id="09ad8-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="09ad8-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="09ad8-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="09ad8-592">2,852.60</span></span></td>
<td><span data-ttu-id="09ad8-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-595">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-596">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-597">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-598">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-598">Amount</span></span></th>
<th><span data-ttu-id="09ad8-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-600">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-601">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-602">60</span><span class="sxs-lookup"><span data-stu-id="09ad8-602">60</span></span></td>
<td><span data-ttu-id="09ad8-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="09ad8-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="09ad8-604">535.31</span><span class="sxs-lookup"><span data-stu-id="09ad8-604">535.31</span></span></td>
<td><span data-ttu-id="09ad8-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-606">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-607">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-608">20</span><span class="sxs-lookup"><span data-stu-id="09ad8-608">20</span></span></td>
<td><span data-ttu-id="09ad8-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="09ad8-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="09ad8-610">178.44</span><span class="sxs-lookup"><span data-stu-id="09ad8-610">178.44</span></span></td>
<td><span data-ttu-id="09ad8-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-612">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-613">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-614">60</span><span class="sxs-lookup"><span data-stu-id="09ad8-614">60</span></span></td>
<td><span data-ttu-id="09ad8-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="09ad8-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="09ad8-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="09ad8-616">4,487.12</span></span></td>
<td><span data-ttu-id="09ad8-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-618">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-619">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-620">20</span><span class="sxs-lookup"><span data-stu-id="09ad8-620">20</span></span></td>
<td><span data-ttu-id="09ad8-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="09ad8-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="09ad8-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-622">1,495.71</span></span></td>
<td><span data-ttu-id="09ad8-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09ad8-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-625">Cost object</span></span></th>
<th><span data-ttu-id="09ad8-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="09ad8-626">Magnitude</span></span></th>
<th><span data-ttu-id="09ad8-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="09ad8-627">Allocation factor</span></span></th>
<th><span data-ttu-id="09ad8-628">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-628">Amount</span></span></th>
<th><span data-ttu-id="09ad8-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-630">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-631">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-632">80</span><span class="sxs-lookup"><span data-stu-id="09ad8-632">80</span></span></td>
<td><span data-ttu-id="09ad8-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="09ad8-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="09ad8-634">241.05</span><span class="sxs-lookup"><span data-stu-id="09ad8-634">241.05</span></span></td>
<td><span data-ttu-id="09ad8-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-636">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-637">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-638">15</span><span class="sxs-lookup"><span data-stu-id="09ad8-638">15</span></span></td>
<td><span data-ttu-id="09ad8-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="09ad8-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="09ad8-640">45.20</span><span class="sxs-lookup"><span data-stu-id="09ad8-640">45.20</span></span></td>
<td><span data-ttu-id="09ad8-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-642">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-643">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-644">80</span><span class="sxs-lookup"><span data-stu-id="09ad8-644">80</span></span></td>
<td><span data-ttu-id="09ad8-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="09ad8-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="09ad8-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="09ad8-646">2,507.09</span></span></td>
<td><span data-ttu-id="09ad8-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-648">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-649">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-650">15</span><span class="sxs-lookup"><span data-stu-id="09ad8-650">15</span></span></td>
<td><span data-ttu-id="09ad8-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="09ad8-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="09ad8-652">470.08</span><span class="sxs-lookup"><span data-stu-id="09ad8-652">470.08</span></span></td>
<td><span data-ttu-id="09ad8-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="09ad8-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="09ad8-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-655">Journal</span></span></th>
<th><span data-ttu-id="09ad8-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="09ad8-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="09ad8-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="09ad8-658">Versija</span><span class="sxs-lookup"><span data-stu-id="09ad8-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-659">00004</span><span class="sxs-lookup"><span data-stu-id="09ad8-659">00004</span></span></td>
<td><span data-ttu-id="09ad8-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="09ad8-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="09ad8-661">Fiscal</span></span></td>
<td><span data-ttu-id="09ad8-662">2017</span><span class="sxs-lookup"><span data-stu-id="09ad8-662">2017</span></span></td>
<td><span data-ttu-id="09ad8-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-663">Period 1</span></span></td>
<td><span data-ttu-id="09ad8-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="09ad8-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="09ad8-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="09ad8-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="09ad8-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-668">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-669">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-670">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-672">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-672">CC001</span></span></td>
<td><span data-ttu-id="09ad8-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-673">HR</span></span></td>
<td><span data-ttu-id="09ad8-674">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-674">10001</span></span></td>
<td><span data-ttu-id="09ad8-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-675">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-676">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-677">500,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-679">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-679">CC001</span></span></td>
<td><span data-ttu-id="09ad8-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-680">HR</span></span></td>
<td><span data-ttu-id="09ad8-681">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-681">10001</span></span></td>
<td><span data-ttu-id="09ad8-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-682">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-683">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-686">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-686">CC002</span></span></td>
<td><span data-ttu-id="09ad8-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-687">Finance</span></span></td>
<td><span data-ttu-id="09ad8-688">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-688">10001</span></span></td>
<td><span data-ttu-id="09ad8-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-689">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-690">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-691">675.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-693">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-693">CC002</span></span></td>
<td><span data-ttu-id="09ad8-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-694">Finance</span></span></td>
<td><span data-ttu-id="09ad8-695">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-695">10001</span></span></td>
<td><span data-ttu-id="09ad8-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-696">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-697">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="09ad8-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-700">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-700">CC003</span></span></td>
<td><span data-ttu-id="09ad8-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-701">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-702">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-702">10001</span></span></td>
<td><span data-ttu-id="09ad8-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-703">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-704">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-705">713.75</span><span class="sxs-lookup"><span data-stu-id="09ad8-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-707">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-707">CC003</span></span></td>
<td><span data-ttu-id="09ad8-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-708">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-709">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-709">10001</span></span></td>
<td><span data-ttu-id="09ad8-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-710">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-711">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="09ad8-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-714">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-714">CC003</span></span></td>
<td><span data-ttu-id="09ad8-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-715">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-716">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-716">10001</span></span></td>
<td><span data-ttu-id="09ad8-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-717">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-718">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-719">286.25</span><span class="sxs-lookup"><span data-stu-id="09ad8-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-721">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-721">CC003</span></span></td>
<td><span data-ttu-id="09ad8-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-722">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-723">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-723">10001</span></span></td>
<td><span data-ttu-id="09ad8-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-724">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-725">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="09ad8-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-728">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-729">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-730">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-730">10001</span></span></td>
<td><span data-ttu-id="09ad8-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-731">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-732">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-733">776.36</span><span class="sxs-lookup"><span data-stu-id="09ad8-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-735">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-736">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-737">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-737">10001</span></span></td>
<td><span data-ttu-id="09ad8-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-738">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-739">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="09ad8-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-742">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-743">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-744">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-744">10001</span></span></td>
<td><span data-ttu-id="09ad8-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-745">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-746">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-747">223.64</span><span class="sxs-lookup"><span data-stu-id="09ad8-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="09ad8-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-749">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-750">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-751">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-751">10001</span></span></td>
<td><span data-ttu-id="09ad8-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-752">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-753">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="09ad8-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="09ad8-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="09ad8-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="09ad8-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="09ad8-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-757">Cost element</span></span></th>
<th><span data-ttu-id="09ad8-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="09ad8-758">Cost behavior</span></span></th>
<th><span data-ttu-id="09ad8-759">Suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-759">Amount</span></span></th>
<th><span data-ttu-id="09ad8-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="09ad8-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="09ad8-761">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-761">CC001</span></span></td>
<td><span data-ttu-id="09ad8-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-762">HR</span></span></td>
<td><span data-ttu-id="09ad8-763">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-763">10001</span></span></td>
<td><span data-ttu-id="09ad8-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-764">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-765">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-766">-500.00</span></span></td>
<td><span data-ttu-id="09ad8-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-768">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-768">CC002</span></span></td>
<td><span data-ttu-id="09ad8-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-769">Finance</span></span></td>
<td><span data-ttu-id="09ad8-770">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-770">10001</span></span></td>
<td><span data-ttu-id="09ad8-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-771">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-772">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-773">175.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-773">175.00</span></span></td>
<td><span data-ttu-id="09ad8-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-775">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-775">CC003</span></span></td>
<td><span data-ttu-id="09ad8-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-776">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-777">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-777">10001</span></span></td>
<td><span data-ttu-id="09ad8-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-778">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-779">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-780">275.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-780">275.00</span></span></td>
<td><span data-ttu-id="09ad8-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-782">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-782">CC004</span></span></td>
<td><span data-ttu-id="09ad8-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-783">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-784">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-784">10001</span></span></td>
<td><span data-ttu-id="09ad8-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-785">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-786">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-787">50,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-787">50,00</span></span></td>
<td><span data-ttu-id="09ad8-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-789">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-789">CC001</span></span></td>
<td><span data-ttu-id="09ad8-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="09ad8-790">HR</span></span></td>
<td><span data-ttu-id="09ad8-791">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-791">10001</span></span></td>
<td><span data-ttu-id="09ad8-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-792">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-793">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-794">-1,245.71</span></span></td>
<td><span data-ttu-id="09ad8-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-796">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-796">CC002</span></span></td>
<td><span data-ttu-id="09ad8-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-797">Finance</span></span></td>
<td><span data-ttu-id="09ad8-798">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-798">10001</span></span></td>
<td><span data-ttu-id="09ad8-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-799">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-800">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-801">436.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-801">436.00</span></span></td>
<td><span data-ttu-id="09ad8-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-803">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-803">CC003</span></span></td>
<td><span data-ttu-id="09ad8-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-804">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-805">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-805">10001</span></span></td>
<td><span data-ttu-id="09ad8-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-806">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-807">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-808">685.14</span><span class="sxs-lookup"><span data-stu-id="09ad8-808">685.14</span></span></td>
<td><span data-ttu-id="09ad8-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-810">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-810">CC004</span></span></td>
<td><span data-ttu-id="09ad8-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-811">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-812">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-812">10001</span></span></td>
<td><span data-ttu-id="09ad8-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-813">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-814">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-815">124.57</span><span class="sxs-lookup"><span data-stu-id="09ad8-815">124.57</span></span></td>
<td><span data-ttu-id="09ad8-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-817">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-817">CC002</span></span></td>
<td><span data-ttu-id="09ad8-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-818">Finance</span></span></td>
<td><span data-ttu-id="09ad8-819">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-819">10001</span></span></td>
<td><span data-ttu-id="09ad8-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-820">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-821">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="09ad8-822">-675.00</span></span></td>
<td><span data-ttu-id="09ad8-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-824">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-824">CC003</span></span></td>
<td><span data-ttu-id="09ad8-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-825">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-826">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-826">10001</span></span></td>
<td><span data-ttu-id="09ad8-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-827">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-828">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-829">438.75</span><span class="sxs-lookup"><span data-stu-id="09ad8-829">438.75</span></span></td>
<td><span data-ttu-id="09ad8-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-831">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-831">CC004</span></span></td>
<td><span data-ttu-id="09ad8-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-832">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-833">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-833">10001</span></span></td>
<td><span data-ttu-id="09ad8-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-834">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-835">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-836">236.25</span><span class="sxs-lookup"><span data-stu-id="09ad8-836">236.25</span></span></td>
<td><span data-ttu-id="09ad8-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-838">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-838">CC002</span></span></td>
<td><span data-ttu-id="09ad8-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="09ad8-839">Finance</span></span></td>
<td><span data-ttu-id="09ad8-840">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-840">10001</span></span></td>
<td><span data-ttu-id="09ad8-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-841">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-842">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="09ad8-843">-8,150.29</span></span></td>
<td><span data-ttu-id="09ad8-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-845">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-845">CC003</span></span></td>
<td><span data-ttu-id="09ad8-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-846">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-847">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-847">10001</span></span></td>
<td><span data-ttu-id="09ad8-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-848">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-849">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="09ad8-850">5,297.69</span></span></td>
<td><span data-ttu-id="09ad8-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-852">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-852">CC004</span></span></td>
<td><span data-ttu-id="09ad8-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="09ad8-853">Packaging</span></span></td>
<td><span data-ttu-id="09ad8-854">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-854">10001</span></span></td>
<td><span data-ttu-id="09ad8-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-855">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-856">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="09ad8-857">2,852.60</span></span></td>
<td><span data-ttu-id="09ad8-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-859">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-859">CC003</span></span></td>
<td><span data-ttu-id="09ad8-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-860">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-861">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-861">10001</span></span></td>
<td><span data-ttu-id="09ad8-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-862">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-863">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="09ad8-864">-713.75</span></span></td>
<td><span data-ttu-id="09ad8-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-866">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-867">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-868">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-868">10001</span></span></td>
<td><span data-ttu-id="09ad8-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-869">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-870">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-871">535.31</span><span class="sxs-lookup"><span data-stu-id="09ad8-871">535.31</span></span></td>
<td><span data-ttu-id="09ad8-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-873">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-874">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-875">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-875">10001</span></span></td>
<td><span data-ttu-id="09ad8-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-876">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-877">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-878">178.44</span><span class="sxs-lookup"><span data-stu-id="09ad8-878">178.44</span></span></td>
<td><span data-ttu-id="09ad8-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-880">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-880">CC003</span></span></td>
<td><span data-ttu-id="09ad8-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-881">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-882">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-882">10001</span></span></td>
<td><span data-ttu-id="09ad8-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-883">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-884">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="09ad8-885">-5,982.83</span></span></td>
<td><span data-ttu-id="09ad8-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-887">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-888">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-889">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-889">10001</span></span></td>
<td><span data-ttu-id="09ad8-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-890">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-891">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="09ad8-892">4,487.12</span></span></td>
<td><span data-ttu-id="09ad8-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-894">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-895">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-896">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-896">10001</span></span></td>
<td><span data-ttu-id="09ad8-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-897">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-898">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="09ad8-899">1,495.71</span></span></td>
<td><span data-ttu-id="09ad8-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-901">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-901">CC003</span></span></td>
<td><span data-ttu-id="09ad8-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-902">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-903">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-903">10001</span></span></td>
<td><span data-ttu-id="09ad8-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-904">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-905">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="09ad8-906">-286.25</span></span></td>
<td><span data-ttu-id="09ad8-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-908">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-909">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-910">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-910">10001</span></span></td>
<td><span data-ttu-id="09ad8-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-911">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-912">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-913">241.05</span><span class="sxs-lookup"><span data-stu-id="09ad8-913">241.05</span></span></td>
<td><span data-ttu-id="09ad8-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-915">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-916">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-917">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-917">10001</span></span></td>
<td><span data-ttu-id="09ad8-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-918">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-919">Fixed cost</span></span></td>
<td><span data-ttu-id="09ad8-920">45.20</span><span class="sxs-lookup"><span data-stu-id="09ad8-920">45.20</span></span></td>
<td><span data-ttu-id="09ad8-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-922">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-922">CC003</span></span></td>
<td><span data-ttu-id="09ad8-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="09ad8-923">Assembly</span></span></td>
<td><span data-ttu-id="09ad8-924">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-924">10001</span></span></td>
<td><span data-ttu-id="09ad8-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-925">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-926">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="09ad8-927">-2,977.17</span></span></td>
<td><span data-ttu-id="09ad8-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-929">Prod 1</span></span></td>
<td><span data-ttu-id="09ad8-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-930">Product 1</span></span></td>
<td><span data-ttu-id="09ad8-931">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-931">10001</span></span></td>
<td><span data-ttu-id="09ad8-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-932">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-933">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="09ad8-934">2,507.09</span></span></td>
<td><span data-ttu-id="09ad8-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="09ad8-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-936">Prod 2</span></span></td>
<td><span data-ttu-id="09ad8-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="09ad8-937">Product 2</span></span></td>
<td><span data-ttu-id="09ad8-938">10001</span><span class="sxs-lookup"><span data-stu-id="09ad8-938">10001</span></span></td>
<td><span data-ttu-id="09ad8-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-939">Electricity</span></span></td>
<td><span data-ttu-id="09ad8-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-940">Variable cost</span></span></td>
<td><span data-ttu-id="09ad8-941">470.08</span><span class="sxs-lookup"><span data-stu-id="09ad8-941">470.08</span></span></td>
<td><span data-ttu-id="09ad8-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="09ad8-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="09ad8-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="09ad8-943">Conclusion</span></span>
<span data-ttu-id="09ad8-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="09ad8-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="09ad8-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="09ad8-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="09ad8-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="09ad8-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="09ad8-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="09ad8-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="09ad8-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="09ad8-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="09ad8-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="09ad8-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="09ad8-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="09ad8-951">CC099</span><span class="sxs-lookup"><span data-stu-id="09ad8-951">CC099</span></span></th>
<th><span data-ttu-id="09ad8-952">CC001</span><span class="sxs-lookup"><span data-stu-id="09ad8-952">CC001</span></span></th>
<th><span data-ttu-id="09ad8-953">CC002</span><span class="sxs-lookup"><span data-stu-id="09ad8-953">CC002</span></span></th>
<th><span data-ttu-id="09ad8-954">CC003</span><span class="sxs-lookup"><span data-stu-id="09ad8-954">CC003</span></span></th>
<th><span data-ttu-id="09ad8-955">CC004</span><span class="sxs-lookup"><span data-stu-id="09ad8-955">CC004</span></span></th>
<th><span data-ttu-id="09ad8-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-956">Proj 1</span></span></th>
<th><span data-ttu-id="09ad8-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="09ad8-957">Proj 2</span></span></th>
<th><span data-ttu-id="09ad8-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-958">Prod 1</span></span></th>
<th><span data-ttu-id="09ad8-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="09ad8-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="09ad8-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="09ad8-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="09ad8-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="09ad8-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-971">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="09ad8-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-973">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-974">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-975">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-976">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-977">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-978">776.36</span><span class="sxs-lookup"><span data-stu-id="09ad8-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-979">223.64</span><span class="sxs-lookup"><span data-stu-id="09ad8-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="09ad8-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="09ad8-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-982">000</span><span class="sxs-lookup"><span data-stu-id="09ad8-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-983">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-984">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-985">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-986">0,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-987">30,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-988">10,00</span><span class="sxs-lookup"><span data-stu-id="09ad8-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="09ad8-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="09ad8-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="09ad8-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="09ad8-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="09ad8-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="09ad8-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="09ad8-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="09ad8-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="09ad8-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="09ad8-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="09ad8-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="09ad8-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="09ad8-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="09ad8-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]