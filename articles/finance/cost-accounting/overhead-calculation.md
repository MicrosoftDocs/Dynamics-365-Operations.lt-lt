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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822908"
---
# <a name="overhead-calculation"></a><span data-ttu-id="75132-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="75132-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75132-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="75132-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="75132-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="75132-105">Term definition</span></span>
---------------

<span data-ttu-id="75132-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="75132-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="75132-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="75132-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="75132-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="75132-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="75132-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="75132-109">Rent</span></span>
-   <span data-ttu-id="75132-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-110">Electricity</span></span>
-   <span data-ttu-id="75132-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="75132-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="75132-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="75132-112">Overhead calculation overview</span></span>
<span data-ttu-id="75132-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="75132-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="75132-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="75132-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="75132-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="75132-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="75132-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="75132-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="75132-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="75132-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="75132-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="75132-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="75132-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="75132-119">Version type</span></span>
-   <span data-ttu-id="75132-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="75132-120">Date and time</span></span>
-   <span data-ttu-id="75132-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="75132-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="75132-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="75132-122">Fiscal year</span></span>
-   <span data-ttu-id="75132-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-123">Fiscal period</span></span>

<span data-ttu-id="75132-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="75132-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="75132-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="75132-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="75132-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="75132-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="75132-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="75132-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="75132-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="75132-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="75132-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="75132-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="75132-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="75132-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="75132-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="75132-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="75132-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="75132-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="75132-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="75132-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="75132-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="75132-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="75132-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="75132-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="75132-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="75132-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="75132-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="75132-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75132-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="75132-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="75132-140">Main account</span></span></th>
<th><span data-ttu-id="75132-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="75132-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="75132-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="75132-143">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-143">CC099</span></span></td>
<td><span data-ttu-id="75132-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-144">Default cost center</span></span></td>
<td><span data-ttu-id="75132-145">10001</span><span class="sxs-lookup"><span data-stu-id="75132-145">10001</span></span></td>
<td><span data-ttu-id="75132-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-146">Electricity</span></span></td>
<td><span data-ttu-id="75132-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="75132-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="75132-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="75132-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="75132-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="75132-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="75132-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="75132-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="75132-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="75132-151">Define the cost behavior rule</span></span>

<span data-ttu-id="75132-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="75132-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="75132-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="75132-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="75132-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="75132-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="75132-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="75132-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="75132-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="75132-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="75132-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="75132-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="75132-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="75132-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-160">Journal</span></span></th>
<th><span data-ttu-id="75132-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="75132-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75132-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75132-163">Versija</span><span class="sxs-lookup"><span data-stu-id="75132-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-164">00001</span><span class="sxs-lookup"><span data-stu-id="75132-164">00001</span></span></td>
<td><span data-ttu-id="75132-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="75132-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="75132-166">Fiscal</span></span></td>
<td><span data-ttu-id="75132-167">2017</span><span class="sxs-lookup"><span data-stu-id="75132-167">2017</span></span></td>
<td><span data-ttu-id="75132-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-168">Period 1</span></span></td>
<td><span data-ttu-id="75132-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75132-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="75132-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75132-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-173">Cost element</span></span></th>
<th><span data-ttu-id="75132-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-174">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-175">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="75132-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="75132-177">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-177">CC099</span></span></td>
<td><span data-ttu-id="75132-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-178">Default cost center</span></span></td>
<td><span data-ttu-id="75132-179">10001</span><span class="sxs-lookup"><span data-stu-id="75132-179">10001</span></span></td>
<td><span data-ttu-id="75132-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-180">Electricity</span></span></td>
<td><span data-ttu-id="75132-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="75132-181">Unclassified</span></span></td>
<td><span data-ttu-id="75132-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="75132-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75132-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="75132-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-185">Cost element</span></span></th>
<th><span data-ttu-id="75132-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-186">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-187">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-187">Amount</span></span></th>
<th><span data-ttu-id="75132-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-189">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-189">CC099</span></span></td>
<td><span data-ttu-id="75132-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-190">Default cost center</span></span></td>
<td><span data-ttu-id="75132-191">10001</span><span class="sxs-lookup"><span data-stu-id="75132-191">10001</span></span></td>
<td><span data-ttu-id="75132-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-192">Electricity</span></span></td>
<td><span data-ttu-id="75132-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="75132-193">Unclassified</span></span></td>
<td><span data-ttu-id="75132-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="75132-194">10,000.00</span></span></td>
<td><span data-ttu-id="75132-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="75132-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-196">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-196">CC099</span></span></td>
<td><span data-ttu-id="75132-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-197">Default cost center</span></span></td>
<td><span data-ttu-id="75132-198">10001</span><span class="sxs-lookup"><span data-stu-id="75132-198">10001</span></span></td>
<td><span data-ttu-id="75132-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-199">Electricity</span></span></td>
<td><span data-ttu-id="75132-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="75132-200">Unclassified</span></span></td>
<td><span data-ttu-id="75132-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="75132-201">-10,000.00</span></span></td>
<td><span data-ttu-id="75132-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-203">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-203">CC099</span></span></td>
<td><span data-ttu-id="75132-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-204">Default cost center</span></span></td>
<td><span data-ttu-id="75132-205">10001</span><span class="sxs-lookup"><span data-stu-id="75132-205">10001</span></span></td>
<td><span data-ttu-id="75132-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-206">Electricity</span></span></td>
<td><span data-ttu-id="75132-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-207">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="75132-208">1,000.00</span></span></td>
<td><span data-ttu-id="75132-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-210">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-210">CC099</span></span></td>
<td><span data-ttu-id="75132-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-211">Default cost center</span></span></td>
<td><span data-ttu-id="75132-212">10001</span><span class="sxs-lookup"><span data-stu-id="75132-212">10001</span></span></td>
<td><span data-ttu-id="75132-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-213">Electricity</span></span></td>
<td><span data-ttu-id="75132-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-214">Variable cost</span></span></td>
<td><span data-ttu-id="75132-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="75132-215">9,000.00</span></span></td>
<td><span data-ttu-id="75132-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="75132-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="75132-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="75132-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="75132-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="75132-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="75132-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="75132-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="75132-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="75132-221">Define the cost distribution rule</span></span>

<span data-ttu-id="75132-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="75132-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="75132-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="75132-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="75132-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="75132-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="75132-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="75132-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="75132-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="75132-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="75132-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="75132-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-228">Cost object</span></span></th>
<th><span data-ttu-id="75132-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="75132-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-230">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-230">CC001</span></span></td>
<td><span data-ttu-id="75132-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-231">HR</span></span></td>
<td><span data-ttu-id="75132-232">1000</span><span class="sxs-lookup"><span data-stu-id="75132-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-233">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-233">CC002</span></span></td>
<td><span data-ttu-id="75132-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-234">Finance</span></span></td>
<td><span data-ttu-id="75132-235">6,000</span><span class="sxs-lookup"><span data-stu-id="75132-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-236">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-236">CC003</span></span></td>
<td><span data-ttu-id="75132-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-237">Assembly</span></span></td>
<td><span data-ttu-id="75132-238">0</span><span class="sxs-lookup"><span data-stu-id="75132-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-240">Cost object</span></span></th>
<th><span data-ttu-id="75132-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-241">Magnitude</span></span></th>
<th><span data-ttu-id="75132-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-242">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-243">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-244">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-244">CC001</span></span></td>
<td><span data-ttu-id="75132-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-245">HR</span></span></td>
<td><span data-ttu-id="75132-246">1000</span><span class="sxs-lookup"><span data-stu-id="75132-246">1,000</span></span></td>
<td><span data-ttu-id="75132-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75132-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="75132-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-249">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-249">CC002</span></span></td>
<td><span data-ttu-id="75132-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-250">Finance</span></span></td>
<td><span data-ttu-id="75132-251">6,000</span><span class="sxs-lookup"><span data-stu-id="75132-251">6,000</span></span></td>
<td><span data-ttu-id="75132-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75132-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="75132-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-254">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-254">CC003</span></span></td>
<td><span data-ttu-id="75132-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-255">Assembly</span></span></td>
<td><span data-ttu-id="75132-256">0</span><span class="sxs-lookup"><span data-stu-id="75132-256">0</span></span></td>
<td><span data-ttu-id="75132-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="75132-258">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="75132-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="75132-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-261">Cost object</span></span></th>
<th><span data-ttu-id="75132-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="75132-262">Formula</span></span></th>
<th><span data-ttu-id="75132-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-263">Magnitude</span></span></th>
<th><span data-ttu-id="75132-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-264">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-265">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-266">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-266">CC001</span></span></td>
<td><span data-ttu-id="75132-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-267">HR</span></span></td>
<td><span data-ttu-id="75132-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75132-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75132-269">1</span><span class="sxs-lookup"><span data-stu-id="75132-269">1</span></span></td>
<td><span data-ttu-id="75132-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75132-271">500,00</span><span class="sxs-lookup"><span data-stu-id="75132-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-272">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-272">CC002</span></span></td>
<td><span data-ttu-id="75132-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-273">Finance</span></span></td>
<td><span data-ttu-id="75132-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75132-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75132-275">1</span><span class="sxs-lookup"><span data-stu-id="75132-275">1</span></span></td>
<td><span data-ttu-id="75132-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75132-277">500,00</span><span class="sxs-lookup"><span data-stu-id="75132-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-278">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-278">CC003</span></span></td>
<td><span data-ttu-id="75132-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-279">Assembly</span></span></td>
<td><span data-ttu-id="75132-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="75132-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="75132-281">0</span><span class="sxs-lookup"><span data-stu-id="75132-281">0</span></span></td>
<td><span data-ttu-id="75132-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="75132-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="75132-283">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="75132-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-285">Journal</span></span></th>
<th><span data-ttu-id="75132-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="75132-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75132-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75132-288">Versija</span><span class="sxs-lookup"><span data-stu-id="75132-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-289">00002</span><span class="sxs-lookup"><span data-stu-id="75132-289">00002</span></span></td>
<td><span data-ttu-id="75132-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="75132-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="75132-291">Fiscal</span></span></td>
<td><span data-ttu-id="75132-292">2017</span><span class="sxs-lookup"><span data-stu-id="75132-292">2017</span></span></td>
<td><span data-ttu-id="75132-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-293">Period 1</span></span></td>
<td><span data-ttu-id="75132-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75132-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="75132-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75132-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-298">Cost element</span></span></th>
<th><span data-ttu-id="75132-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-299">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-300">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-302">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-302">CC099</span></span></td>
<td><span data-ttu-id="75132-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-303">Default cost center</span></span></td>
<td><span data-ttu-id="75132-304">10001</span><span class="sxs-lookup"><span data-stu-id="75132-304">10001</span></span></td>
<td><span data-ttu-id="75132-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-305">Electricity</span></span></td>
<td><span data-ttu-id="75132-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-306">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="75132-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-309">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-309">CC099</span></span></td>
<td><span data-ttu-id="75132-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-310">Default cost center</span></span></td>
<td><span data-ttu-id="75132-311">10001</span><span class="sxs-lookup"><span data-stu-id="75132-311">10001</span></span></td>
<td><span data-ttu-id="75132-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-312">Electricity</span></span></td>
<td><span data-ttu-id="75132-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-313">Variable cost</span></span></td>
<td><span data-ttu-id="75132-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="75132-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75132-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="75132-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-317">Cost element</span></span></th>
<th><span data-ttu-id="75132-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-318">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-319">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-319">Amount</span></span></th>
<th><span data-ttu-id="75132-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-321">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-321">CC099</span></span></td>
<td><span data-ttu-id="75132-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-322">Default cost center</span></span></td>
<td><span data-ttu-id="75132-323">10001</span><span class="sxs-lookup"><span data-stu-id="75132-323">10001</span></span></td>
<td><span data-ttu-id="75132-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-324">Electricity</span></span></td>
<td><span data-ttu-id="75132-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-325">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="75132-326">-1,000.00</span></span></td>
<td><span data-ttu-id="75132-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-328">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-328">CC001</span></span></td>
<td><span data-ttu-id="75132-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-329">HR</span></span></td>
<td><span data-ttu-id="75132-330">10001</span><span class="sxs-lookup"><span data-stu-id="75132-330">10001</span></span></td>
<td><span data-ttu-id="75132-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-331">Electricity</span></span></td>
<td><span data-ttu-id="75132-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-332">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-333">500,00</span><span class="sxs-lookup"><span data-stu-id="75132-333">500.00</span></span></td>
<td><span data-ttu-id="75132-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-335">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-335">CC002</span></span></td>
<td><span data-ttu-id="75132-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-336">Finance</span></span></td>
<td><span data-ttu-id="75132-337">10001</span><span class="sxs-lookup"><span data-stu-id="75132-337">10001</span></span></td>
<td><span data-ttu-id="75132-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-338">Electricity</span></span></td>
<td><span data-ttu-id="75132-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-339">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-340">500,00</span><span class="sxs-lookup"><span data-stu-id="75132-340">500.00</span></span></td>
<td><span data-ttu-id="75132-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-342">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-342">CC099</span></span></td>
<td><span data-ttu-id="75132-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="75132-343">Default cost center</span></span></td>
<td><span data-ttu-id="75132-344">10001</span><span class="sxs-lookup"><span data-stu-id="75132-344">10001</span></span></td>
<td><span data-ttu-id="75132-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-345">Electricity</span></span></td>
<td><span data-ttu-id="75132-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-346">Variable cost</span></span></td>
<td><span data-ttu-id="75132-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="75132-347">-9,000.00</span></span></td>
<td><span data-ttu-id="75132-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-349">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-349">CC001</span></span></td>
<td><span data-ttu-id="75132-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-350">HR</span></span></td>
<td><span data-ttu-id="75132-351">10001</span><span class="sxs-lookup"><span data-stu-id="75132-351">10001</span></span></td>
<td><span data-ttu-id="75132-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-352">Electricity</span></span></td>
<td><span data-ttu-id="75132-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-353">Variable cost</span></span></td>
<td><span data-ttu-id="75132-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="75132-354">1,285.71</span></span></td>
<td><span data-ttu-id="75132-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-356">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-356">CC002</span></span></td>
<td><span data-ttu-id="75132-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-357">Finance</span></span></td>
<td><span data-ttu-id="75132-358">10001</span><span class="sxs-lookup"><span data-stu-id="75132-358">10001</span></span></td>
<td><span data-ttu-id="75132-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-359">Electricity</span></span></td>
<td><span data-ttu-id="75132-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-360">Variable cost</span></span></td>
<td><span data-ttu-id="75132-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="75132-361">7,714.29</span></span></td>
<td><span data-ttu-id="75132-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="75132-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="75132-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="75132-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="75132-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="75132-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="75132-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="75132-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="75132-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="75132-367">Define the overhead rate</span></span>

<span data-ttu-id="75132-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="75132-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="75132-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="75132-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-370">Cost object</span></span></th>
<th><span data-ttu-id="75132-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="75132-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-372">Proj 1</span></span></td>
<td><span data-ttu-id="75132-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-373">Project 1</span></span></td>
<td><span data-ttu-id="75132-374">3</span><span class="sxs-lookup"><span data-stu-id="75132-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-375">Proj 2</span></span></td>
<td><span data-ttu-id="75132-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-376">Project 2</span></span></td>
<td><span data-ttu-id="75132-377">1</span><span class="sxs-lookup"><span data-stu-id="75132-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="75132-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-379">Cost object</span></span></th>
<th><span data-ttu-id="75132-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-380">Cost element</span></span></th>
<th><span data-ttu-id="75132-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-381">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="75132-382">Units</span></span></th>
<th><span data-ttu-id="75132-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="75132-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-384">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-384">CC001</span></span></td>
<td><span data-ttu-id="75132-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-385">HR</span></span></td>
<td><span data-ttu-id="75132-386">10001</span><span class="sxs-lookup"><span data-stu-id="75132-386">10001</span></span></td>
<td><span data-ttu-id="75132-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-387">Variable cost</span></span></td>
<td><span data-ttu-id="75132-388">1</span><span class="sxs-lookup"><span data-stu-id="75132-388">1</span></span></td>
<td><span data-ttu-id="75132-389">10</span><span class="sxs-lookup"><span data-stu-id="75132-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-391">Cost object</span></span></th>
<th><span data-ttu-id="75132-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-392">Magnitude</span></span></th>
<th><span data-ttu-id="75132-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-393">Cost element</span></span></th>
<th><span data-ttu-id="75132-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-394">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-395">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-396">Proj 1</span></span></td>
<td><span data-ttu-id="75132-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-397">Project 1</span></span></td>
<td><span data-ttu-id="75132-398">3</span><span class="sxs-lookup"><span data-stu-id="75132-398">3</span></span></td>
<td><span data-ttu-id="75132-399">10001</span><span class="sxs-lookup"><span data-stu-id="75132-399">10001</span></span></td>
<td><span data-ttu-id="75132-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="75132-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="75132-401">30,00</span><span class="sxs-lookup"><span data-stu-id="75132-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-402">Proj 2</span></span></td>
<td><span data-ttu-id="75132-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-403">Project 2</span></span></td>
<td><span data-ttu-id="75132-404">1</span><span class="sxs-lookup"><span data-stu-id="75132-404">1</span></span></td>
<td><span data-ttu-id="75132-405">10001</span><span class="sxs-lookup"><span data-stu-id="75132-405">10001</span></span></td>
<td><span data-ttu-id="75132-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="75132-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="75132-407">10,00</span><span class="sxs-lookup"><span data-stu-id="75132-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="75132-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-409">Journal</span></span></th>
<th><span data-ttu-id="75132-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="75132-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75132-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75132-412">Versija</span><span class="sxs-lookup"><span data-stu-id="75132-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-413">00003</span><span class="sxs-lookup"><span data-stu-id="75132-413">00003</span></span></td>
<td><span data-ttu-id="75132-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="75132-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="75132-415">Fiscal</span></span></td>
<td><span data-ttu-id="75132-416">2017</span><span class="sxs-lookup"><span data-stu-id="75132-416">2017</span></span></td>
<td><span data-ttu-id="75132-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-417">Period 1</span></span></td>
<td><span data-ttu-id="75132-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="75132-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="75132-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75132-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-421">Cost object</span></span></th>
<th><span data-ttu-id="75132-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-424">Proj 1</span></span></td>
<td><span data-ttu-id="75132-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="75132-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="75132-426">3,00</span><span class="sxs-lookup"><span data-stu-id="75132-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-428">Proj 2</span></span></td>
<td><span data-ttu-id="75132-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="75132-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="75132-430">1,00</span><span class="sxs-lookup"><span data-stu-id="75132-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75132-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="75132-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-433">Cost element</span></span></th>
<th><span data-ttu-id="75132-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-434">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-435">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-435">Amount</span></span></th>
<th><span data-ttu-id="75132-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="75132-437">CC0001</span></span></td>
<td><span data-ttu-id="75132-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-438">HR</span></span></td>
<td><span data-ttu-id="75132-439">10001</span><span class="sxs-lookup"><span data-stu-id="75132-439">10001</span></span></td>
<td><span data-ttu-id="75132-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-440">Electricity</span></span></td>
<td><span data-ttu-id="75132-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-441">Variable cost</span></span></td>
<td><span data-ttu-id="75132-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="75132-442">-30.00</span></span></td>
<td><span data-ttu-id="75132-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-444">Proj 1</span></span></td>
<td><span data-ttu-id="75132-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="75132-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="75132-446">10001</span><span class="sxs-lookup"><span data-stu-id="75132-446">10001</span></span></td>
<td><span data-ttu-id="75132-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-447">Electricity</span></span></td>
<td><span data-ttu-id="75132-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-448">Variable cost</span></span></td>
<td><span data-ttu-id="75132-449">30,00</span><span class="sxs-lookup"><span data-stu-id="75132-449">30.00</span></span></td>
<td><span data-ttu-id="75132-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-451">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-451">CC001</span></span></td>
<td><span data-ttu-id="75132-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-452">HR</span></span></td>
<td><span data-ttu-id="75132-453">10001</span><span class="sxs-lookup"><span data-stu-id="75132-453">10001</span></span></td>
<td><span data-ttu-id="75132-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-454">Electricity</span></span></td>
<td><span data-ttu-id="75132-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-455">Variable cost</span></span></td>
<td><span data-ttu-id="75132-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="75132-456">-10.00</span></span></td>
<td><span data-ttu-id="75132-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-458">Proj 2</span></span></td>
<td><span data-ttu-id="75132-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="75132-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="75132-460">10001</span><span class="sxs-lookup"><span data-stu-id="75132-460">10001</span></span></td>
<td><span data-ttu-id="75132-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-461">Electricity</span></span></td>
<td><span data-ttu-id="75132-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-462">Variable cost</span></span></td>
<td><span data-ttu-id="75132-463">10,00</span><span class="sxs-lookup"><span data-stu-id="75132-463">10.00</span></span></td>
<td><span data-ttu-id="75132-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="75132-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="75132-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="75132-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="75132-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="75132-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="75132-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="75132-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="75132-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="75132-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="75132-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="75132-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="75132-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="75132-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="75132-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="75132-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="75132-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="75132-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="75132-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="75132-475">Define the cost allocation</span></span>

<span data-ttu-id="75132-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="75132-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="75132-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="75132-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="75132-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="75132-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-479">Cost object</span></span></th>
<th><span data-ttu-id="75132-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="75132-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-481">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-481">CC002</span></span></td>
<td><span data-ttu-id="75132-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-482">Finance</span></span></td>
<td><span data-ttu-id="75132-483">35</span><span class="sxs-lookup"><span data-stu-id="75132-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-484">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-484">CC003</span></span></td>
<td><span data-ttu-id="75132-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-485">Assembly</span></span></td>
<td><span data-ttu-id="75132-486">55</span><span class="sxs-lookup"><span data-stu-id="75132-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-487">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-487">CC004</span></span></td>
<td><span data-ttu-id="75132-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-488">Packaging</span></span></td>
<td><span data-ttu-id="75132-489">10</span><span class="sxs-lookup"><span data-stu-id="75132-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="75132-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="75132-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="75132-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-492">Cost object</span></span></th>
<th><span data-ttu-id="75132-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="75132-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-494">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-494">CC003</span></span></td>
<td><span data-ttu-id="75132-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-495">Assembly</span></span></td>
<td><span data-ttu-id="75132-496">65</span><span class="sxs-lookup"><span data-stu-id="75132-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-497">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-497">CC004</span></span></td>
<td><span data-ttu-id="75132-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-498">Packaging</span></span></td>
<td><span data-ttu-id="75132-499">35</span><span class="sxs-lookup"><span data-stu-id="75132-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="75132-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="75132-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="75132-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-502">Cost object</span></span></th>
<th><span data-ttu-id="75132-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="75132-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-504">Prod 1</span></span></td>
<td><span data-ttu-id="75132-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-505">Product 1</span></span></td>
<td><span data-ttu-id="75132-506">60</span><span class="sxs-lookup"><span data-stu-id="75132-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-507">Prod 2</span></span></td>
<td><span data-ttu-id="75132-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-508">Product 2</span></span></td>
<td><span data-ttu-id="75132-509">20</span><span class="sxs-lookup"><span data-stu-id="75132-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="75132-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="75132-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="75132-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-512">Cost object</span></span></th>
<th><span data-ttu-id="75132-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="75132-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-514">Prod 1</span></span></td>
<td><span data-ttu-id="75132-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-515">Product 1</span></span></td>
<td><span data-ttu-id="75132-516">80</span><span class="sxs-lookup"><span data-stu-id="75132-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-517">Prod 2</span></span></td>
<td><span data-ttu-id="75132-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-518">Product 2</span></span></td>
<td><span data-ttu-id="75132-519">15</span><span class="sxs-lookup"><span data-stu-id="75132-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="75132-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="75132-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="75132-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="75132-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="75132-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-523">Cost object</span></span></th>
<th><span data-ttu-id="75132-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-524">Magnitude</span></span></th>
<th><span data-ttu-id="75132-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-525">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-526">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-526">Amount</span></span></th>
<th><span data-ttu-id="75132-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-528">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-528">CC002</span></span></td>
<td><span data-ttu-id="75132-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-529">Finance</span></span></td>
<td><span data-ttu-id="75132-530">35</span><span class="sxs-lookup"><span data-stu-id="75132-530">35</span></span></td>
<td><span data-ttu-id="75132-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75132-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75132-532">175.00</span><span class="sxs-lookup"><span data-stu-id="75132-532">175.00</span></span></td>
<td><span data-ttu-id="75132-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-534">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-534">CC003</span></span></td>
<td><span data-ttu-id="75132-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-535">Assembly</span></span></td>
<td><span data-ttu-id="75132-536">55</span><span class="sxs-lookup"><span data-stu-id="75132-536">55</span></span></td>
<td><span data-ttu-id="75132-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75132-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75132-538">275.00</span><span class="sxs-lookup"><span data-stu-id="75132-538">275.00</span></span></td>
<td><span data-ttu-id="75132-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-540">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-540">CC004</span></span></td>
<td><span data-ttu-id="75132-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-541">Packaging</span></span></td>
<td><span data-ttu-id="75132-542">10</span><span class="sxs-lookup"><span data-stu-id="75132-542">10</span></span></td>
<td><span data-ttu-id="75132-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="75132-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="75132-544">50,00</span><span class="sxs-lookup"><span data-stu-id="75132-544">50.00</span></span></td>
<td><span data-ttu-id="75132-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-546">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-546">CC002</span></span></td>
<td><span data-ttu-id="75132-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-547">Finance</span></span></td>
<td><span data-ttu-id="75132-548">35</span><span class="sxs-lookup"><span data-stu-id="75132-548">35</span></span></td>
<td><span data-ttu-id="75132-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75132-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75132-550">436.00</span><span class="sxs-lookup"><span data-stu-id="75132-550">436.00</span></span></td>
<td><span data-ttu-id="75132-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-552">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-552">CC003</span></span></td>
<td><span data-ttu-id="75132-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-553">Assembly</span></span></td>
<td><span data-ttu-id="75132-554">55</span><span class="sxs-lookup"><span data-stu-id="75132-554">55</span></span></td>
<td><span data-ttu-id="75132-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75132-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75132-556">685.14</span><span class="sxs-lookup"><span data-stu-id="75132-556">685.14</span></span></td>
<td><span data-ttu-id="75132-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-558">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-558">CC004</span></span></td>
<td><span data-ttu-id="75132-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-559">Packaging</span></span></td>
<td><span data-ttu-id="75132-560">10</span><span class="sxs-lookup"><span data-stu-id="75132-560">10</span></span></td>
<td><span data-ttu-id="75132-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="75132-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="75132-562">124.57</span><span class="sxs-lookup"><span data-stu-id="75132-562">124.57</span></span></td>
<td><span data-ttu-id="75132-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-565">Cost object</span></span></th>
<th><span data-ttu-id="75132-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-566">Magnitude</span></span></th>
<th><span data-ttu-id="75132-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-567">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-568">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-568">Amount</span></span></th>
<th><span data-ttu-id="75132-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-570">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-570">CC003</span></span></td>
<td><span data-ttu-id="75132-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-571">Assembly</span></span></td>
<td><span data-ttu-id="75132-572">65</span><span class="sxs-lookup"><span data-stu-id="75132-572">65</span></span></td>
<td><span data-ttu-id="75132-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="75132-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="75132-574">438.75</span><span class="sxs-lookup"><span data-stu-id="75132-574">438.75</span></span></td>
<td><span data-ttu-id="75132-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-576">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-576">CC004</span></span></td>
<td><span data-ttu-id="75132-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-577">Packaging</span></span></td>
<td><span data-ttu-id="75132-578">35</span><span class="sxs-lookup"><span data-stu-id="75132-578">35</span></span></td>
<td><span data-ttu-id="75132-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="75132-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="75132-580">236.25</span><span class="sxs-lookup"><span data-stu-id="75132-580">236.25</span></span></td>
<td><span data-ttu-id="75132-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-582">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-582">CC003</span></span></td>
<td><span data-ttu-id="75132-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-583">Assembly</span></span></td>
<td><span data-ttu-id="75132-584">65</span><span class="sxs-lookup"><span data-stu-id="75132-584">65</span></span></td>
<td><span data-ttu-id="75132-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="75132-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="75132-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="75132-586">5,297.69</span></span></td>
<td><span data-ttu-id="75132-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-588">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-588">CC004</span></span></td>
<td><span data-ttu-id="75132-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-589">Packaging</span></span></td>
<td><span data-ttu-id="75132-590">35</span><span class="sxs-lookup"><span data-stu-id="75132-590">35</span></span></td>
<td><span data-ttu-id="75132-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="75132-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="75132-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="75132-592">2,852.60</span></span></td>
<td><span data-ttu-id="75132-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-595">Cost object</span></span></th>
<th><span data-ttu-id="75132-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-596">Magnitude</span></span></th>
<th><span data-ttu-id="75132-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-597">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-598">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-598">Amount</span></span></th>
<th><span data-ttu-id="75132-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-600">Prod 1</span></span></td>
<td><span data-ttu-id="75132-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-601">Product 1</span></span></td>
<td><span data-ttu-id="75132-602">60</span><span class="sxs-lookup"><span data-stu-id="75132-602">60</span></span></td>
<td><span data-ttu-id="75132-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="75132-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="75132-604">535.31</span><span class="sxs-lookup"><span data-stu-id="75132-604">535.31</span></span></td>
<td><span data-ttu-id="75132-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-606">Prod 2</span></span></td>
<td><span data-ttu-id="75132-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-607">Product 2</span></span></td>
<td><span data-ttu-id="75132-608">20</span><span class="sxs-lookup"><span data-stu-id="75132-608">20</span></span></td>
<td><span data-ttu-id="75132-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="75132-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="75132-610">178.44</span><span class="sxs-lookup"><span data-stu-id="75132-610">178.44</span></span></td>
<td><span data-ttu-id="75132-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-612">Prod 1</span></span></td>
<td><span data-ttu-id="75132-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-613">Product 1</span></span></td>
<td><span data-ttu-id="75132-614">60</span><span class="sxs-lookup"><span data-stu-id="75132-614">60</span></span></td>
<td><span data-ttu-id="75132-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="75132-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="75132-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="75132-616">4,487.12</span></span></td>
<td><span data-ttu-id="75132-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-618">Prod 2</span></span></td>
<td><span data-ttu-id="75132-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-619">Product 2</span></span></td>
<td><span data-ttu-id="75132-620">20</span><span class="sxs-lookup"><span data-stu-id="75132-620">20</span></span></td>
<td><span data-ttu-id="75132-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="75132-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="75132-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="75132-622">1,495.71</span></span></td>
<td><span data-ttu-id="75132-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="75132-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="75132-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-625">Cost object</span></span></th>
<th><span data-ttu-id="75132-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="75132-626">Magnitude</span></span></th>
<th><span data-ttu-id="75132-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="75132-627">Allocation factor</span></span></th>
<th><span data-ttu-id="75132-628">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-628">Amount</span></span></th>
<th><span data-ttu-id="75132-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-630">Prod 1</span></span></td>
<td><span data-ttu-id="75132-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-631">Product 1</span></span></td>
<td><span data-ttu-id="75132-632">80</span><span class="sxs-lookup"><span data-stu-id="75132-632">80</span></span></td>
<td><span data-ttu-id="75132-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="75132-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="75132-634">241.05</span><span class="sxs-lookup"><span data-stu-id="75132-634">241.05</span></span></td>
<td><span data-ttu-id="75132-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-636">Prod 2</span></span></td>
<td><span data-ttu-id="75132-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-637">Product 2</span></span></td>
<td><span data-ttu-id="75132-638">15</span><span class="sxs-lookup"><span data-stu-id="75132-638">15</span></span></td>
<td><span data-ttu-id="75132-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="75132-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="75132-640">45.20</span><span class="sxs-lookup"><span data-stu-id="75132-640">45.20</span></span></td>
<td><span data-ttu-id="75132-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-642">Prod 1</span></span></td>
<td><span data-ttu-id="75132-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-643">Product 1</span></span></td>
<td><span data-ttu-id="75132-644">80</span><span class="sxs-lookup"><span data-stu-id="75132-644">80</span></span></td>
<td><span data-ttu-id="75132-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="75132-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="75132-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="75132-646">2,507.09</span></span></td>
<td><span data-ttu-id="75132-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-648">Prod 2</span></span></td>
<td><span data-ttu-id="75132-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-649">Product 2</span></span></td>
<td><span data-ttu-id="75132-650">15</span><span class="sxs-lookup"><span data-stu-id="75132-650">15</span></span></td>
<td><span data-ttu-id="75132-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="75132-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="75132-652">470.08</span><span class="sxs-lookup"><span data-stu-id="75132-652">470.08</span></span></td>
<td><span data-ttu-id="75132-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="75132-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="75132-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-655">Journal</span></span></th>
<th><span data-ttu-id="75132-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="75132-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="75132-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="75132-658">Versija</span><span class="sxs-lookup"><span data-stu-id="75132-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-659">00004</span><span class="sxs-lookup"><span data-stu-id="75132-659">00004</span></span></td>
<td><span data-ttu-id="75132-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="75132-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="75132-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="75132-661">Fiscal</span></span></td>
<td><span data-ttu-id="75132-662">2017</span><span class="sxs-lookup"><span data-stu-id="75132-662">2017</span></span></td>
<td><span data-ttu-id="75132-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-663">Period 1</span></span></td>
<td><span data-ttu-id="75132-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="75132-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="75132-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="75132-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="75132-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="75132-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-668">Cost element</span></span></th>
<th><span data-ttu-id="75132-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-669">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-670">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-672">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-672">CC001</span></span></td>
<td><span data-ttu-id="75132-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-673">HR</span></span></td>
<td><span data-ttu-id="75132-674">10001</span><span class="sxs-lookup"><span data-stu-id="75132-674">10001</span></span></td>
<td><span data-ttu-id="75132-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-675">Electricity</span></span></td>
<td><span data-ttu-id="75132-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-676">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-677">500,00</span><span class="sxs-lookup"><span data-stu-id="75132-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-679">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-679">CC001</span></span></td>
<td><span data-ttu-id="75132-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-680">HR</span></span></td>
<td><span data-ttu-id="75132-681">10001</span><span class="sxs-lookup"><span data-stu-id="75132-681">10001</span></span></td>
<td><span data-ttu-id="75132-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-682">Electricity</span></span></td>
<td><span data-ttu-id="75132-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-683">Variable cost</span></span></td>
<td><span data-ttu-id="75132-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="75132-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-686">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-686">CC002</span></span></td>
<td><span data-ttu-id="75132-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-687">Finance</span></span></td>
<td><span data-ttu-id="75132-688">10001</span><span class="sxs-lookup"><span data-stu-id="75132-688">10001</span></span></td>
<td><span data-ttu-id="75132-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-689">Electricity</span></span></td>
<td><span data-ttu-id="75132-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-690">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-691">675.00</span><span class="sxs-lookup"><span data-stu-id="75132-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-693">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-693">CC002</span></span></td>
<td><span data-ttu-id="75132-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-694">Finance</span></span></td>
<td><span data-ttu-id="75132-695">10001</span><span class="sxs-lookup"><span data-stu-id="75132-695">10001</span></span></td>
<td><span data-ttu-id="75132-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-696">Electricity</span></span></td>
<td><span data-ttu-id="75132-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-697">Variable cost</span></span></td>
<td><span data-ttu-id="75132-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="75132-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-700">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-700">CC003</span></span></td>
<td><span data-ttu-id="75132-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-701">Assembly</span></span></td>
<td><span data-ttu-id="75132-702">10001</span><span class="sxs-lookup"><span data-stu-id="75132-702">10001</span></span></td>
<td><span data-ttu-id="75132-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-703">Electricity</span></span></td>
<td><span data-ttu-id="75132-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-704">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-705">713.75</span><span class="sxs-lookup"><span data-stu-id="75132-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-707">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-707">CC003</span></span></td>
<td><span data-ttu-id="75132-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-708">Assembly</span></span></td>
<td><span data-ttu-id="75132-709">10001</span><span class="sxs-lookup"><span data-stu-id="75132-709">10001</span></span></td>
<td><span data-ttu-id="75132-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-710">Electricity</span></span></td>
<td><span data-ttu-id="75132-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-711">Variable cost</span></span></td>
<td><span data-ttu-id="75132-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="75132-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-714">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-714">CC003</span></span></td>
<td><span data-ttu-id="75132-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-715">Packaging</span></span></td>
<td><span data-ttu-id="75132-716">10001</span><span class="sxs-lookup"><span data-stu-id="75132-716">10001</span></span></td>
<td><span data-ttu-id="75132-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-717">Electricity</span></span></td>
<td><span data-ttu-id="75132-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-718">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-719">286.25</span><span class="sxs-lookup"><span data-stu-id="75132-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-721">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-721">CC003</span></span></td>
<td><span data-ttu-id="75132-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-722">Packaging</span></span></td>
<td><span data-ttu-id="75132-723">10001</span><span class="sxs-lookup"><span data-stu-id="75132-723">10001</span></span></td>
<td><span data-ttu-id="75132-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-724">Electricity</span></span></td>
<td><span data-ttu-id="75132-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-725">Variable cost</span></span></td>
<td><span data-ttu-id="75132-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="75132-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-728">Prod 1</span></span></td>
<td><span data-ttu-id="75132-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-729">Product 1</span></span></td>
<td><span data-ttu-id="75132-730">10001</span><span class="sxs-lookup"><span data-stu-id="75132-730">10001</span></span></td>
<td><span data-ttu-id="75132-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-731">Electricity</span></span></td>
<td><span data-ttu-id="75132-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-732">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-733">776.36</span><span class="sxs-lookup"><span data-stu-id="75132-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-735">Prod 1</span></span></td>
<td><span data-ttu-id="75132-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-736">Product 1</span></span></td>
<td><span data-ttu-id="75132-737">10001</span><span class="sxs-lookup"><span data-stu-id="75132-737">10001</span></span></td>
<td><span data-ttu-id="75132-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-738">Electricity</span></span></td>
<td><span data-ttu-id="75132-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-739">Variable cost</span></span></td>
<td><span data-ttu-id="75132-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="75132-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-742">Prod 2</span></span></td>
<td><span data-ttu-id="75132-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-743">Product 1</span></span></td>
<td><span data-ttu-id="75132-744">10001</span><span class="sxs-lookup"><span data-stu-id="75132-744">10001</span></span></td>
<td><span data-ttu-id="75132-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-745">Electricity</span></span></td>
<td><span data-ttu-id="75132-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-746">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-747">223.64</span><span class="sxs-lookup"><span data-stu-id="75132-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="75132-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-749">Prod 2</span></span></td>
<td><span data-ttu-id="75132-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-750">Product 1</span></span></td>
<td><span data-ttu-id="75132-751">10001</span><span class="sxs-lookup"><span data-stu-id="75132-751">10001</span></span></td>
<td><span data-ttu-id="75132-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-752">Electricity</span></span></td>
<td><span data-ttu-id="75132-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-753">Variable cost</span></span></td>
<td><span data-ttu-id="75132-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="75132-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="75132-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="75132-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="75132-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="75132-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-757">Cost element</span></span></th>
<th><span data-ttu-id="75132-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="75132-758">Cost behavior</span></span></th>
<th><span data-ttu-id="75132-759">Suma</span><span class="sxs-lookup"><span data-stu-id="75132-759">Amount</span></span></th>
<th><span data-ttu-id="75132-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="75132-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="75132-761">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-761">CC001</span></span></td>
<td><span data-ttu-id="75132-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-762">HR</span></span></td>
<td><span data-ttu-id="75132-763">10001</span><span class="sxs-lookup"><span data-stu-id="75132-763">10001</span></span></td>
<td><span data-ttu-id="75132-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-764">Electricity</span></span></td>
<td><span data-ttu-id="75132-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-765">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="75132-766">-500.00</span></span></td>
<td><span data-ttu-id="75132-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-768">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-768">CC002</span></span></td>
<td><span data-ttu-id="75132-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-769">Finance</span></span></td>
<td><span data-ttu-id="75132-770">10001</span><span class="sxs-lookup"><span data-stu-id="75132-770">10001</span></span></td>
<td><span data-ttu-id="75132-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-771">Electricity</span></span></td>
<td><span data-ttu-id="75132-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-772">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-773">175.00</span><span class="sxs-lookup"><span data-stu-id="75132-773">175.00</span></span></td>
<td><span data-ttu-id="75132-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-775">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-775">CC003</span></span></td>
<td><span data-ttu-id="75132-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-776">Assembly</span></span></td>
<td><span data-ttu-id="75132-777">10001</span><span class="sxs-lookup"><span data-stu-id="75132-777">10001</span></span></td>
<td><span data-ttu-id="75132-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-778">Electricity</span></span></td>
<td><span data-ttu-id="75132-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-779">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-780">275.00</span><span class="sxs-lookup"><span data-stu-id="75132-780">275.00</span></span></td>
<td><span data-ttu-id="75132-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-782">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-782">CC004</span></span></td>
<td><span data-ttu-id="75132-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-783">Packaging</span></span></td>
<td><span data-ttu-id="75132-784">10001</span><span class="sxs-lookup"><span data-stu-id="75132-784">10001</span></span></td>
<td><span data-ttu-id="75132-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-785">Electricity</span></span></td>
<td><span data-ttu-id="75132-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-786">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-787">50,00</span><span class="sxs-lookup"><span data-stu-id="75132-787">50,00</span></span></td>
<td><span data-ttu-id="75132-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-789">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-789">CC001</span></span></td>
<td><span data-ttu-id="75132-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="75132-790">HR</span></span></td>
<td><span data-ttu-id="75132-791">10001</span><span class="sxs-lookup"><span data-stu-id="75132-791">10001</span></span></td>
<td><span data-ttu-id="75132-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-792">Electricity</span></span></td>
<td><span data-ttu-id="75132-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-793">Variable cost</span></span></td>
<td><span data-ttu-id="75132-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="75132-794">-1,245.71</span></span></td>
<td><span data-ttu-id="75132-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-796">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-796">CC002</span></span></td>
<td><span data-ttu-id="75132-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-797">Finance</span></span></td>
<td><span data-ttu-id="75132-798">10001</span><span class="sxs-lookup"><span data-stu-id="75132-798">10001</span></span></td>
<td><span data-ttu-id="75132-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-799">Electricity</span></span></td>
<td><span data-ttu-id="75132-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-800">Variable cost</span></span></td>
<td><span data-ttu-id="75132-801">436.00</span><span class="sxs-lookup"><span data-stu-id="75132-801">436.00</span></span></td>
<td><span data-ttu-id="75132-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-803">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-803">CC003</span></span></td>
<td><span data-ttu-id="75132-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-804">Assembly</span></span></td>
<td><span data-ttu-id="75132-805">10001</span><span class="sxs-lookup"><span data-stu-id="75132-805">10001</span></span></td>
<td><span data-ttu-id="75132-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-806">Electricity</span></span></td>
<td><span data-ttu-id="75132-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-807">Variable cost</span></span></td>
<td><span data-ttu-id="75132-808">685.14</span><span class="sxs-lookup"><span data-stu-id="75132-808">685.14</span></span></td>
<td><span data-ttu-id="75132-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-810">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-810">CC004</span></span></td>
<td><span data-ttu-id="75132-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-811">Packaging</span></span></td>
<td><span data-ttu-id="75132-812">10001</span><span class="sxs-lookup"><span data-stu-id="75132-812">10001</span></span></td>
<td><span data-ttu-id="75132-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-813">Electricity</span></span></td>
<td><span data-ttu-id="75132-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-814">Variable cost</span></span></td>
<td><span data-ttu-id="75132-815">124.57</span><span class="sxs-lookup"><span data-stu-id="75132-815">124.57</span></span></td>
<td><span data-ttu-id="75132-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-817">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-817">CC002</span></span></td>
<td><span data-ttu-id="75132-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-818">Finance</span></span></td>
<td><span data-ttu-id="75132-819">10001</span><span class="sxs-lookup"><span data-stu-id="75132-819">10001</span></span></td>
<td><span data-ttu-id="75132-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-820">Electricity</span></span></td>
<td><span data-ttu-id="75132-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-821">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="75132-822">-675.00</span></span></td>
<td><span data-ttu-id="75132-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-824">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-824">CC003</span></span></td>
<td><span data-ttu-id="75132-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-825">Assembly</span></span></td>
<td><span data-ttu-id="75132-826">10001</span><span class="sxs-lookup"><span data-stu-id="75132-826">10001</span></span></td>
<td><span data-ttu-id="75132-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-827">Electricity</span></span></td>
<td><span data-ttu-id="75132-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-828">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-829">438.75</span><span class="sxs-lookup"><span data-stu-id="75132-829">438.75</span></span></td>
<td><span data-ttu-id="75132-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-831">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-831">CC004</span></span></td>
<td><span data-ttu-id="75132-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-832">Packaging</span></span></td>
<td><span data-ttu-id="75132-833">10001</span><span class="sxs-lookup"><span data-stu-id="75132-833">10001</span></span></td>
<td><span data-ttu-id="75132-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-834">Electricity</span></span></td>
<td><span data-ttu-id="75132-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-835">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-836">236.25</span><span class="sxs-lookup"><span data-stu-id="75132-836">236.25</span></span></td>
<td><span data-ttu-id="75132-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-838">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-838">CC002</span></span></td>
<td><span data-ttu-id="75132-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="75132-839">Finance</span></span></td>
<td><span data-ttu-id="75132-840">10001</span><span class="sxs-lookup"><span data-stu-id="75132-840">10001</span></span></td>
<td><span data-ttu-id="75132-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-841">Electricity</span></span></td>
<td><span data-ttu-id="75132-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-842">Variable cost</span></span></td>
<td><span data-ttu-id="75132-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="75132-843">-8,150.29</span></span></td>
<td><span data-ttu-id="75132-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-845">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-845">CC003</span></span></td>
<td><span data-ttu-id="75132-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-846">Assembly</span></span></td>
<td><span data-ttu-id="75132-847">10001</span><span class="sxs-lookup"><span data-stu-id="75132-847">10001</span></span></td>
<td><span data-ttu-id="75132-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-848">Electricity</span></span></td>
<td><span data-ttu-id="75132-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-849">Variable cost</span></span></td>
<td><span data-ttu-id="75132-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="75132-850">5,297.69</span></span></td>
<td><span data-ttu-id="75132-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-852">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-852">CC004</span></span></td>
<td><span data-ttu-id="75132-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="75132-853">Packaging</span></span></td>
<td><span data-ttu-id="75132-854">10001</span><span class="sxs-lookup"><span data-stu-id="75132-854">10001</span></span></td>
<td><span data-ttu-id="75132-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-855">Electricity</span></span></td>
<td><span data-ttu-id="75132-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-856">Variable cost</span></span></td>
<td><span data-ttu-id="75132-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="75132-857">2,852.60</span></span></td>
<td><span data-ttu-id="75132-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-859">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-859">CC003</span></span></td>
<td><span data-ttu-id="75132-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-860">Assembly</span></span></td>
<td><span data-ttu-id="75132-861">10001</span><span class="sxs-lookup"><span data-stu-id="75132-861">10001</span></span></td>
<td><span data-ttu-id="75132-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-862">Electricity</span></span></td>
<td><span data-ttu-id="75132-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-863">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="75132-864">-713.75</span></span></td>
<td><span data-ttu-id="75132-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-866">Prod 1</span></span></td>
<td><span data-ttu-id="75132-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-867">Product 1</span></span></td>
<td><span data-ttu-id="75132-868">10001</span><span class="sxs-lookup"><span data-stu-id="75132-868">10001</span></span></td>
<td><span data-ttu-id="75132-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-869">Electricity</span></span></td>
<td><span data-ttu-id="75132-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-870">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-871">535.31</span><span class="sxs-lookup"><span data-stu-id="75132-871">535.31</span></span></td>
<td><span data-ttu-id="75132-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-873">Prod 2</span></span></td>
<td><span data-ttu-id="75132-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-874">Product 2</span></span></td>
<td><span data-ttu-id="75132-875">10001</span><span class="sxs-lookup"><span data-stu-id="75132-875">10001</span></span></td>
<td><span data-ttu-id="75132-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-876">Electricity</span></span></td>
<td><span data-ttu-id="75132-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-877">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-878">178.44</span><span class="sxs-lookup"><span data-stu-id="75132-878">178.44</span></span></td>
<td><span data-ttu-id="75132-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-880">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-880">CC003</span></span></td>
<td><span data-ttu-id="75132-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-881">Assembly</span></span></td>
<td><span data-ttu-id="75132-882">10001</span><span class="sxs-lookup"><span data-stu-id="75132-882">10001</span></span></td>
<td><span data-ttu-id="75132-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-883">Electricity</span></span></td>
<td><span data-ttu-id="75132-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-884">Variable cost</span></span></td>
<td><span data-ttu-id="75132-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="75132-885">-5,982.83</span></span></td>
<td><span data-ttu-id="75132-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-887">Prod 1</span></span></td>
<td><span data-ttu-id="75132-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-888">Product 1</span></span></td>
<td><span data-ttu-id="75132-889">10001</span><span class="sxs-lookup"><span data-stu-id="75132-889">10001</span></span></td>
<td><span data-ttu-id="75132-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-890">Electricity</span></span></td>
<td><span data-ttu-id="75132-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-891">Variable cost</span></span></td>
<td><span data-ttu-id="75132-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="75132-892">4,487.12</span></span></td>
<td><span data-ttu-id="75132-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-894">Prod 2</span></span></td>
<td><span data-ttu-id="75132-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-895">Product 2</span></span></td>
<td><span data-ttu-id="75132-896">10001</span><span class="sxs-lookup"><span data-stu-id="75132-896">10001</span></span></td>
<td><span data-ttu-id="75132-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-897">Electricity</span></span></td>
<td><span data-ttu-id="75132-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-898">Variable cost</span></span></td>
<td><span data-ttu-id="75132-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="75132-899">1,495.71</span></span></td>
<td><span data-ttu-id="75132-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-901">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-901">CC003</span></span></td>
<td><span data-ttu-id="75132-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-902">Assembly</span></span></td>
<td><span data-ttu-id="75132-903">10001</span><span class="sxs-lookup"><span data-stu-id="75132-903">10001</span></span></td>
<td><span data-ttu-id="75132-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-904">Electricity</span></span></td>
<td><span data-ttu-id="75132-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-905">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="75132-906">-286.25</span></span></td>
<td><span data-ttu-id="75132-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-908">Prod 1</span></span></td>
<td><span data-ttu-id="75132-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-909">Product 1</span></span></td>
<td><span data-ttu-id="75132-910">10001</span><span class="sxs-lookup"><span data-stu-id="75132-910">10001</span></span></td>
<td><span data-ttu-id="75132-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-911">Electricity</span></span></td>
<td><span data-ttu-id="75132-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-912">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-913">241.05</span><span class="sxs-lookup"><span data-stu-id="75132-913">241.05</span></span></td>
<td><span data-ttu-id="75132-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-915">Prod 2</span></span></td>
<td><span data-ttu-id="75132-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-916">Product 2</span></span></td>
<td><span data-ttu-id="75132-917">10001</span><span class="sxs-lookup"><span data-stu-id="75132-917">10001</span></span></td>
<td><span data-ttu-id="75132-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-918">Electricity</span></span></td>
<td><span data-ttu-id="75132-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-919">Fixed cost</span></span></td>
<td><span data-ttu-id="75132-920">45.20</span><span class="sxs-lookup"><span data-stu-id="75132-920">45.20</span></span></td>
<td><span data-ttu-id="75132-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-922">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-922">CC003</span></span></td>
<td><span data-ttu-id="75132-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="75132-923">Assembly</span></span></td>
<td><span data-ttu-id="75132-924">10001</span><span class="sxs-lookup"><span data-stu-id="75132-924">10001</span></span></td>
<td><span data-ttu-id="75132-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-925">Electricity</span></span></td>
<td><span data-ttu-id="75132-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-926">Variable cost</span></span></td>
<td><span data-ttu-id="75132-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="75132-927">-2,977.17</span></span></td>
<td><span data-ttu-id="75132-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-929">Prod 1</span></span></td>
<td><span data-ttu-id="75132-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-930">Product 1</span></span></td>
<td><span data-ttu-id="75132-931">10001</span><span class="sxs-lookup"><span data-stu-id="75132-931">10001</span></span></td>
<td><span data-ttu-id="75132-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-932">Electricity</span></span></td>
<td><span data-ttu-id="75132-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-933">Variable cost</span></span></td>
<td><span data-ttu-id="75132-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="75132-934">2,507.09</span></span></td>
<td><span data-ttu-id="75132-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="75132-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-936">Prod 2</span></span></td>
<td><span data-ttu-id="75132-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="75132-937">Product 2</span></span></td>
<td><span data-ttu-id="75132-938">10001</span><span class="sxs-lookup"><span data-stu-id="75132-938">10001</span></span></td>
<td><span data-ttu-id="75132-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-939">Electricity</span></span></td>
<td><span data-ttu-id="75132-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-940">Variable cost</span></span></td>
<td><span data-ttu-id="75132-941">470.08</span><span class="sxs-lookup"><span data-stu-id="75132-941">470.08</span></span></td>
<td><span data-ttu-id="75132-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="75132-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="75132-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="75132-943">Conclusion</span></span>
<span data-ttu-id="75132-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="75132-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="75132-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="75132-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="75132-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="75132-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="75132-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="75132-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="75132-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="75132-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="75132-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="75132-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="75132-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="75132-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="75132-951">CC099</span><span class="sxs-lookup"><span data-stu-id="75132-951">CC099</span></span></th>
<th><span data-ttu-id="75132-952">CC001</span><span class="sxs-lookup"><span data-stu-id="75132-952">CC001</span></span></th>
<th><span data-ttu-id="75132-953">CC002</span><span class="sxs-lookup"><span data-stu-id="75132-953">CC002</span></span></th>
<th><span data-ttu-id="75132-954">CC003</span><span class="sxs-lookup"><span data-stu-id="75132-954">CC003</span></span></th>
<th><span data-ttu-id="75132-955">CC004</span><span class="sxs-lookup"><span data-stu-id="75132-955">CC004</span></span></th>
<th><span data-ttu-id="75132-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-956">Proj 1</span></span></th>
<th><span data-ttu-id="75132-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="75132-957">Proj 2</span></span></th>
<th><span data-ttu-id="75132-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-958">Prod 1</span></span></th>
<th><span data-ttu-id="75132-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="75132-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="75132-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="75132-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="75132-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="75132-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="75132-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="75132-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="75132-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-971">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="75132-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-973">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-974">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-975">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-976">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-977">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="75132-978">776.36</span><span class="sxs-lookup"><span data-stu-id="75132-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-979">223.64</span><span class="sxs-lookup"><span data-stu-id="75132-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="75132-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="75132-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-982">000</span><span class="sxs-lookup"><span data-stu-id="75132-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-983">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-984">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-985">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-986">0,00</span><span class="sxs-lookup"><span data-stu-id="75132-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-987">30,00</span><span class="sxs-lookup"><span data-stu-id="75132-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-988">10,00</span><span class="sxs-lookup"><span data-stu-id="75132-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="75132-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="75132-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="75132-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="75132-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="75132-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="75132-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="75132-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="75132-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="75132-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="75132-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="75132-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="75132-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="75132-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="75132-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]