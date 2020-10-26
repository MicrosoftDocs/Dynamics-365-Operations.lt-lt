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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976480"
---
# <a name="overhead-calculation"></a><span data-ttu-id="54db1-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="54db1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54db1-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="54db1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="54db1-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="54db1-105">Term definition</span></span>
---------------

<span data-ttu-id="54db1-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="54db1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="54db1-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="54db1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="54db1-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="54db1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="54db1-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="54db1-109">Rent</span></span>
-   <span data-ttu-id="54db1-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-110">Electricity</span></span>
-   <span data-ttu-id="54db1-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="54db1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="54db1-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="54db1-112">Overhead calculation overview</span></span>
<span data-ttu-id="54db1-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="54db1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="54db1-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="54db1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="54db1-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="54db1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="54db1-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="54db1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="54db1-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="54db1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="54db1-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="54db1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="54db1-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="54db1-119">Version type</span></span>
-   <span data-ttu-id="54db1-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="54db1-120">Date and time</span></span>
-   <span data-ttu-id="54db1-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="54db1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="54db1-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="54db1-122">Fiscal year</span></span>
-   <span data-ttu-id="54db1-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-123">Fiscal period</span></span>

<span data-ttu-id="54db1-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="54db1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="54db1-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="54db1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="54db1-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="54db1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="54db1-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="54db1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="54db1-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="54db1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="54db1-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="54db1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="54db1-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="54db1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="54db1-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="54db1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="54db1-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="54db1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="54db1-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="54db1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="54db1-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="54db1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="54db1-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="54db1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="54db1-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="54db1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="54db1-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="54db1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="54db1-140">Main account</span></span></th>
<th><span data-ttu-id="54db1-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="54db1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="54db1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-143">CC099</span></span></td>
<td><span data-ttu-id="54db1-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-144">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-145">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-145">10001</span></span></td>
<td><span data-ttu-id="54db1-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-146">Electricity</span></span></td>
<td><span data-ttu-id="54db1-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="54db1-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="54db1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="54db1-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="54db1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="54db1-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="54db1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="54db1-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="54db1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="54db1-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="54db1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="54db1-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="54db1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="54db1-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="54db1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="54db1-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="54db1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="54db1-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="54db1-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="54db1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="54db1-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="54db1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="54db1-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-160">Journal</span></span></th>
<th><span data-ttu-id="54db1-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="54db1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="54db1-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="54db1-163">Versija</span><span class="sxs-lookup"><span data-stu-id="54db1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-164">00001</span><span class="sxs-lookup"><span data-stu-id="54db1-164">00001</span></span></td>
<td><span data-ttu-id="54db1-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="54db1-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="54db1-166">Fiscal</span></span></td>
<td><span data-ttu-id="54db1-167">2017</span><span class="sxs-lookup"><span data-stu-id="54db1-167">2017</span></span></td>
<td><span data-ttu-id="54db1-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-168">Period 1</span></span></td>
<td><span data-ttu-id="54db1-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="54db1-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="54db1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-173">Cost element</span></span></th>
<th><span data-ttu-id="54db1-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-175">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="54db1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-177">CC099</span></span></td>
<td><span data-ttu-id="54db1-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-178">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-179">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-179">10001</span></span></td>
<td><span data-ttu-id="54db1-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-180">Electricity</span></span></td>
<td><span data-ttu-id="54db1-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="54db1-181">Unclassified</span></span></td>
<td><span data-ttu-id="54db1-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="54db1-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="54db1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-185">Cost element</span></span></th>
<th><span data-ttu-id="54db1-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-187">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-187">Amount</span></span></th>
<th><span data-ttu-id="54db1-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-189">CC099</span></span></td>
<td><span data-ttu-id="54db1-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-190">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-191">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-191">10001</span></span></td>
<td><span data-ttu-id="54db1-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-192">Electricity</span></span></td>
<td><span data-ttu-id="54db1-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="54db1-193">Unclassified</span></span></td>
<td><span data-ttu-id="54db1-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-194">10,000.00</span></span></td>
<td><span data-ttu-id="54db1-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-196">CC099</span></span></td>
<td><span data-ttu-id="54db1-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-197">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-198">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-198">10001</span></span></td>
<td><span data-ttu-id="54db1-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-199">Electricity</span></span></td>
<td><span data-ttu-id="54db1-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="54db1-200">Unclassified</span></span></td>
<td><span data-ttu-id="54db1-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="54db1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="54db1-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-203">CC099</span></span></td>
<td><span data-ttu-id="54db1-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-204">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-205">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-205">10001</span></span></td>
<td><span data-ttu-id="54db1-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-206">Electricity</span></span></td>
<td><span data-ttu-id="54db1-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-208">1,000.00</span></span></td>
<td><span data-ttu-id="54db1-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-210">CC099</span></span></td>
<td><span data-ttu-id="54db1-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-211">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-212">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-212">10001</span></span></td>
<td><span data-ttu-id="54db1-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-213">Electricity</span></span></td>
<td><span data-ttu-id="54db1-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-214">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="54db1-215">9,000.00</span></span></td>
<td><span data-ttu-id="54db1-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="54db1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="54db1-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="54db1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="54db1-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="54db1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="54db1-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="54db1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="54db1-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="54db1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="54db1-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="54db1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="54db1-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="54db1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="54db1-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="54db1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="54db1-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="54db1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="54db1-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="54db1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="54db1-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="54db1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-228">Cost object</span></span></th>
<th><span data-ttu-id="54db1-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="54db1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-230">CC001</span></span></td>
<td><span data-ttu-id="54db1-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-231">HR</span></span></td>
<td><span data-ttu-id="54db1-232">1000</span><span class="sxs-lookup"><span data-stu-id="54db1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-233">CC002</span></span></td>
<td><span data-ttu-id="54db1-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-234">Finance</span></span></td>
<td><span data-ttu-id="54db1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="54db1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-236">CC003</span></span></td>
<td><span data-ttu-id="54db1-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-237">Assembly</span></span></td>
<td><span data-ttu-id="54db1-238">0</span><span class="sxs-lookup"><span data-stu-id="54db1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-240">Cost object</span></span></th>
<th><span data-ttu-id="54db1-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-241">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-243">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-244">CC001</span></span></td>
<td><span data-ttu-id="54db1-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-245">HR</span></span></td>
<td><span data-ttu-id="54db1-246">1000</span><span class="sxs-lookup"><span data-stu-id="54db1-246">1,000</span></span></td>
<td><span data-ttu-id="54db1-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="54db1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="54db1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-249">CC002</span></span></td>
<td><span data-ttu-id="54db1-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-250">Finance</span></span></td>
<td><span data-ttu-id="54db1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="54db1-251">6,000</span></span></td>
<td><span data-ttu-id="54db1-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="54db1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="54db1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-254">CC003</span></span></td>
<td><span data-ttu-id="54db1-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-255">Assembly</span></span></td>
<td><span data-ttu-id="54db1-256">0</span><span class="sxs-lookup"><span data-stu-id="54db1-256">0</span></span></td>
<td><span data-ttu-id="54db1-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="54db1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="54db1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="54db1-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-261">Cost object</span></span></th>
<th><span data-ttu-id="54db1-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="54db1-262">Formula</span></span></th>
<th><span data-ttu-id="54db1-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-263">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-265">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-266">CC001</span></span></td>
<td><span data-ttu-id="54db1-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-267">HR</span></span></td>
<td><span data-ttu-id="54db1-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="54db1-269">1</span><span class="sxs-lookup"><span data-stu-id="54db1-269">1</span></span></td>
<td><span data-ttu-id="54db1-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="54db1-271">500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-272">CC002</span></span></td>
<td><span data-ttu-id="54db1-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-273">Finance</span></span></td>
<td><span data-ttu-id="54db1-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="54db1-275">1</span><span class="sxs-lookup"><span data-stu-id="54db1-275">1</span></span></td>
<td><span data-ttu-id="54db1-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="54db1-277">500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-278">CC003</span></span></td>
<td><span data-ttu-id="54db1-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-279">Assembly</span></span></td>
<td><span data-ttu-id="54db1-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="54db1-281">0</span><span class="sxs-lookup"><span data-stu-id="54db1-281">0</span></span></td>
<td><span data-ttu-id="54db1-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="54db1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="54db1-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-285">Journal</span></span></th>
<th><span data-ttu-id="54db1-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="54db1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="54db1-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="54db1-288">Versija</span><span class="sxs-lookup"><span data-stu-id="54db1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-289">00002</span><span class="sxs-lookup"><span data-stu-id="54db1-289">00002</span></span></td>
<td><span data-ttu-id="54db1-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="54db1-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="54db1-291">Fiscal</span></span></td>
<td><span data-ttu-id="54db1-292">2017</span><span class="sxs-lookup"><span data-stu-id="54db1-292">2017</span></span></td>
<td><span data-ttu-id="54db1-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-293">Period 1</span></span></td>
<td><span data-ttu-id="54db1-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="54db1-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="54db1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-298">Cost element</span></span></th>
<th><span data-ttu-id="54db1-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-300">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-302">CC099</span></span></td>
<td><span data-ttu-id="54db1-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-303">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-304">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-304">10001</span></span></td>
<td><span data-ttu-id="54db1-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-305">Electricity</span></span></td>
<td><span data-ttu-id="54db1-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="54db1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-309">CC099</span></span></td>
<td><span data-ttu-id="54db1-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-310">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-311">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-311">10001</span></span></td>
<td><span data-ttu-id="54db1-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-312">Electricity</span></span></td>
<td><span data-ttu-id="54db1-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-313">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="54db1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="54db1-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="54db1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-317">Cost element</span></span></th>
<th><span data-ttu-id="54db1-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-319">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-319">Amount</span></span></th>
<th><span data-ttu-id="54db1-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-321">CC099</span></span></td>
<td><span data-ttu-id="54db1-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-322">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-323">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-323">10001</span></span></td>
<td><span data-ttu-id="54db1-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-324">Electricity</span></span></td>
<td><span data-ttu-id="54db1-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="54db1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="54db1-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-328">CC001</span></span></td>
<td><span data-ttu-id="54db1-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-329">HR</span></span></td>
<td><span data-ttu-id="54db1-330">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-330">10001</span></span></td>
<td><span data-ttu-id="54db1-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-331">Electricity</span></span></td>
<td><span data-ttu-id="54db1-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-333">500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-333">500.00</span></span></td>
<td><span data-ttu-id="54db1-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-335">CC002</span></span></td>
<td><span data-ttu-id="54db1-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-336">Finance</span></span></td>
<td><span data-ttu-id="54db1-337">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-337">10001</span></span></td>
<td><span data-ttu-id="54db1-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-338">Electricity</span></span></td>
<td><span data-ttu-id="54db1-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-340">500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-340">500.00</span></span></td>
<td><span data-ttu-id="54db1-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-342">CC099</span></span></td>
<td><span data-ttu-id="54db1-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="54db1-343">Default cost center</span></span></td>
<td><span data-ttu-id="54db1-344">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-344">10001</span></span></td>
<td><span data-ttu-id="54db1-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-345">Electricity</span></span></td>
<td><span data-ttu-id="54db1-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-346">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="54db1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="54db1-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-349">CC001</span></span></td>
<td><span data-ttu-id="54db1-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-350">HR</span></span></td>
<td><span data-ttu-id="54db1-351">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-351">10001</span></span></td>
<td><span data-ttu-id="54db1-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-352">Electricity</span></span></td>
<td><span data-ttu-id="54db1-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-353">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="54db1-354">1,285.71</span></span></td>
<td><span data-ttu-id="54db1-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-356">CC002</span></span></td>
<td><span data-ttu-id="54db1-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-357">Finance</span></span></td>
<td><span data-ttu-id="54db1-358">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-358">10001</span></span></td>
<td><span data-ttu-id="54db1-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-359">Electricity</span></span></td>
<td><span data-ttu-id="54db1-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-360">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="54db1-361">7,714.29</span></span></td>
<td><span data-ttu-id="54db1-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="54db1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="54db1-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="54db1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="54db1-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="54db1-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="54db1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="54db1-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="54db1-367">Define the overhead rate</span></span>

<span data-ttu-id="54db1-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="54db1-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54db1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-370">Cost object</span></span></th>
<th><span data-ttu-id="54db1-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="54db1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-372">Proj 1</span></span></td>
<td><span data-ttu-id="54db1-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-373">Project 1</span></span></td>
<td><span data-ttu-id="54db1-374">3</span><span class="sxs-lookup"><span data-stu-id="54db1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-375">Proj 2</span></span></td>
<td><span data-ttu-id="54db1-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-376">Project 2</span></span></td>
<td><span data-ttu-id="54db1-377">1</span><span class="sxs-lookup"><span data-stu-id="54db1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="54db1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-379">Cost object</span></span></th>
<th><span data-ttu-id="54db1-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-380">Cost element</span></span></th>
<th><span data-ttu-id="54db1-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="54db1-382">Units</span></span></th>
<th><span data-ttu-id="54db1-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="54db1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-384">CC001</span></span></td>
<td><span data-ttu-id="54db1-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-385">HR</span></span></td>
<td><span data-ttu-id="54db1-386">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-386">10001</span></span></td>
<td><span data-ttu-id="54db1-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-387">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-388">1</span><span class="sxs-lookup"><span data-stu-id="54db1-388">1</span></span></td>
<td><span data-ttu-id="54db1-389">10</span><span class="sxs-lookup"><span data-stu-id="54db1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-391">Cost object</span></span></th>
<th><span data-ttu-id="54db1-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-392">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-393">Cost element</span></span></th>
<th><span data-ttu-id="54db1-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-395">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-396">Proj 1</span></span></td>
<td><span data-ttu-id="54db1-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-397">Project 1</span></span></td>
<td><span data-ttu-id="54db1-398">3</span><span class="sxs-lookup"><span data-stu-id="54db1-398">3</span></span></td>
<td><span data-ttu-id="54db1-399">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-399">10001</span></span></td>
<td><span data-ttu-id="54db1-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="54db1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="54db1-401">30,00</span><span class="sxs-lookup"><span data-stu-id="54db1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-402">Proj 2</span></span></td>
<td><span data-ttu-id="54db1-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-403">Project 2</span></span></td>
<td><span data-ttu-id="54db1-404">1</span><span class="sxs-lookup"><span data-stu-id="54db1-404">1</span></span></td>
<td><span data-ttu-id="54db1-405">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-405">10001</span></span></td>
<td><span data-ttu-id="54db1-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="54db1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="54db1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="54db1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="54db1-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-409">Journal</span></span></th>
<th><span data-ttu-id="54db1-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="54db1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="54db1-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="54db1-412">Versija</span><span class="sxs-lookup"><span data-stu-id="54db1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-413">00003</span><span class="sxs-lookup"><span data-stu-id="54db1-413">00003</span></span></td>
<td><span data-ttu-id="54db1-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="54db1-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="54db1-415">Fiscal</span></span></td>
<td><span data-ttu-id="54db1-416">2017</span><span class="sxs-lookup"><span data-stu-id="54db1-416">2017</span></span></td>
<td><span data-ttu-id="54db1-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-417">Period 1</span></span></td>
<td><span data-ttu-id="54db1-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="54db1-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="54db1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-421">Cost object</span></span></th>
<th><span data-ttu-id="54db1-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-424">Proj 1</span></span></td>
<td><span data-ttu-id="54db1-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="54db1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="54db1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-428">Proj 2</span></span></td>
<td><span data-ttu-id="54db1-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="54db1-430">1,00</span><span class="sxs-lookup"><span data-stu-id="54db1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="54db1-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="54db1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-433">Cost element</span></span></th>
<th><span data-ttu-id="54db1-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-435">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-435">Amount</span></span></th>
<th><span data-ttu-id="54db1-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="54db1-437">CC0001</span></span></td>
<td><span data-ttu-id="54db1-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-438">HR</span></span></td>
<td><span data-ttu-id="54db1-439">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-439">10001</span></span></td>
<td><span data-ttu-id="54db1-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-440">Electricity</span></span></td>
<td><span data-ttu-id="54db1-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-441">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="54db1-442">-30.00</span></span></td>
<td><span data-ttu-id="54db1-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-444">Proj 1</span></span></td>
<td><span data-ttu-id="54db1-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="54db1-446">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-446">10001</span></span></td>
<td><span data-ttu-id="54db1-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-447">Electricity</span></span></td>
<td><span data-ttu-id="54db1-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-448">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-449">30,00</span><span class="sxs-lookup"><span data-stu-id="54db1-449">30.00</span></span></td>
<td><span data-ttu-id="54db1-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-451">CC001</span></span></td>
<td><span data-ttu-id="54db1-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-452">HR</span></span></td>
<td><span data-ttu-id="54db1-453">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-453">10001</span></span></td>
<td><span data-ttu-id="54db1-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-454">Electricity</span></span></td>
<td><span data-ttu-id="54db1-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-455">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="54db1-456">-10.00</span></span></td>
<td><span data-ttu-id="54db1-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-458">Proj 2</span></span></td>
<td><span data-ttu-id="54db1-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="54db1-460">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-460">10001</span></span></td>
<td><span data-ttu-id="54db1-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-461">Electricity</span></span></td>
<td><span data-ttu-id="54db1-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-462">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-463">10,00</span><span class="sxs-lookup"><span data-stu-id="54db1-463">10.00</span></span></td>
<td><span data-ttu-id="54db1-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="54db1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="54db1-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="54db1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="54db1-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="54db1-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="54db1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="54db1-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="54db1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="54db1-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="54db1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="54db1-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="54db1-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="54db1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="54db1-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="54db1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="54db1-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="54db1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="54db1-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="54db1-475">Define the cost allocation</span></span>

<span data-ttu-id="54db1-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="54db1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="54db1-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="54db1-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54db1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-479">Cost object</span></span></th>
<th><span data-ttu-id="54db1-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="54db1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-481">CC002</span></span></td>
<td><span data-ttu-id="54db1-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-482">Finance</span></span></td>
<td><span data-ttu-id="54db1-483">35</span><span class="sxs-lookup"><span data-stu-id="54db1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-484">CC003</span></span></td>
<td><span data-ttu-id="54db1-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-485">Assembly</span></span></td>
<td><span data-ttu-id="54db1-486">55</span><span class="sxs-lookup"><span data-stu-id="54db1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-487">CC004</span></span></td>
<td><span data-ttu-id="54db1-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-488">Packaging</span></span></td>
<td><span data-ttu-id="54db1-489">10</span><span class="sxs-lookup"><span data-stu-id="54db1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="54db1-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54db1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-492">Cost object</span></span></th>
<th><span data-ttu-id="54db1-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="54db1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-494">CC003</span></span></td>
<td><span data-ttu-id="54db1-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-495">Assembly</span></span></td>
<td><span data-ttu-id="54db1-496">65</span><span class="sxs-lookup"><span data-stu-id="54db1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-497">CC004</span></span></td>
<td><span data-ttu-id="54db1-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-498">Packaging</span></span></td>
<td><span data-ttu-id="54db1-499">35</span><span class="sxs-lookup"><span data-stu-id="54db1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="54db1-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54db1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-502">Cost object</span></span></th>
<th><span data-ttu-id="54db1-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="54db1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-504">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-505">Product 1</span></span></td>
<td><span data-ttu-id="54db1-506">60</span><span class="sxs-lookup"><span data-stu-id="54db1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-507">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-508">Product 2</span></span></td>
<td><span data-ttu-id="54db1-509">20</span><span class="sxs-lookup"><span data-stu-id="54db1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="54db1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="54db1-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="54db1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-512">Cost object</span></span></th>
<th><span data-ttu-id="54db1-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="54db1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-514">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-515">Product 1</span></span></td>
<td><span data-ttu-id="54db1-516">80</span><span class="sxs-lookup"><span data-stu-id="54db1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-517">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-518">Product 2</span></span></td>
<td><span data-ttu-id="54db1-519">15</span><span class="sxs-lookup"><span data-stu-id="54db1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="54db1-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="54db1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="54db1-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="54db1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="54db1-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-523">Cost object</span></span></th>
<th><span data-ttu-id="54db1-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-524">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-526">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-526">Amount</span></span></th>
<th><span data-ttu-id="54db1-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-528">CC002</span></span></td>
<td><span data-ttu-id="54db1-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-529">Finance</span></span></td>
<td><span data-ttu-id="54db1-530">35</span><span class="sxs-lookup"><span data-stu-id="54db1-530">35</span></span></td>
<td><span data-ttu-id="54db1-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="54db1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="54db1-532">175.00</span></span></td>
<td><span data-ttu-id="54db1-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-534">CC003</span></span></td>
<td><span data-ttu-id="54db1-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-535">Assembly</span></span></td>
<td><span data-ttu-id="54db1-536">55</span><span class="sxs-lookup"><span data-stu-id="54db1-536">55</span></span></td>
<td><span data-ttu-id="54db1-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="54db1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="54db1-538">275.00</span></span></td>
<td><span data-ttu-id="54db1-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-540">CC004</span></span></td>
<td><span data-ttu-id="54db1-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-541">Packaging</span></span></td>
<td><span data-ttu-id="54db1-542">10</span><span class="sxs-lookup"><span data-stu-id="54db1-542">10</span></span></td>
<td><span data-ttu-id="54db1-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="54db1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="54db1-544">50.00</span></span></td>
<td><span data-ttu-id="54db1-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-546">CC002</span></span></td>
<td><span data-ttu-id="54db1-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-547">Finance</span></span></td>
<td><span data-ttu-id="54db1-548">35</span><span class="sxs-lookup"><span data-stu-id="54db1-548">35</span></span></td>
<td><span data-ttu-id="54db1-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="54db1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="54db1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="54db1-550">436.00</span></span></td>
<td><span data-ttu-id="54db1-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-552">CC003</span></span></td>
<td><span data-ttu-id="54db1-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-553">Assembly</span></span></td>
<td><span data-ttu-id="54db1-554">55</span><span class="sxs-lookup"><span data-stu-id="54db1-554">55</span></span></td>
<td><span data-ttu-id="54db1-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="54db1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="54db1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="54db1-556">685.14</span></span></td>
<td><span data-ttu-id="54db1-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-558">CC004</span></span></td>
<td><span data-ttu-id="54db1-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-559">Packaging</span></span></td>
<td><span data-ttu-id="54db1-560">10</span><span class="sxs-lookup"><span data-stu-id="54db1-560">10</span></span></td>
<td><span data-ttu-id="54db1-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="54db1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="54db1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="54db1-562">124.57</span></span></td>
<td><span data-ttu-id="54db1-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-565">Cost object</span></span></th>
<th><span data-ttu-id="54db1-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-566">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-568">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-568">Amount</span></span></th>
<th><span data-ttu-id="54db1-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-570">CC003</span></span></td>
<td><span data-ttu-id="54db1-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-571">Assembly</span></span></td>
<td><span data-ttu-id="54db1-572">65</span><span class="sxs-lookup"><span data-stu-id="54db1-572">65</span></span></td>
<td><span data-ttu-id="54db1-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="54db1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="54db1-574">438.75</span></span></td>
<td><span data-ttu-id="54db1-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-576">CC004</span></span></td>
<td><span data-ttu-id="54db1-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-577">Packaging</span></span></td>
<td><span data-ttu-id="54db1-578">35</span><span class="sxs-lookup"><span data-stu-id="54db1-578">35</span></span></td>
<td><span data-ttu-id="54db1-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="54db1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="54db1-580">236.25</span></span></td>
<td><span data-ttu-id="54db1-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-582">CC003</span></span></td>
<td><span data-ttu-id="54db1-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-583">Assembly</span></span></td>
<td><span data-ttu-id="54db1-584">65</span><span class="sxs-lookup"><span data-stu-id="54db1-584">65</span></span></td>
<td><span data-ttu-id="54db1-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="54db1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="54db1-586">5,297.69</span></span></td>
<td><span data-ttu-id="54db1-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-588">CC004</span></span></td>
<td><span data-ttu-id="54db1-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-589">Packaging</span></span></td>
<td><span data-ttu-id="54db1-590">35</span><span class="sxs-lookup"><span data-stu-id="54db1-590">35</span></span></td>
<td><span data-ttu-id="54db1-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="54db1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="54db1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="54db1-592">2,852.60</span></span></td>
<td><span data-ttu-id="54db1-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-595">Cost object</span></span></th>
<th><span data-ttu-id="54db1-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-596">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-598">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-598">Amount</span></span></th>
<th><span data-ttu-id="54db1-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-600">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-601">Product 1</span></span></td>
<td><span data-ttu-id="54db1-602">60</span><span class="sxs-lookup"><span data-stu-id="54db1-602">60</span></span></td>
<td><span data-ttu-id="54db1-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="54db1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="54db1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="54db1-604">535.31</span></span></td>
<td><span data-ttu-id="54db1-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-606">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-607">Product 2</span></span></td>
<td><span data-ttu-id="54db1-608">20</span><span class="sxs-lookup"><span data-stu-id="54db1-608">20</span></span></td>
<td><span data-ttu-id="54db1-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="54db1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="54db1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="54db1-610">178.44</span></span></td>
<td><span data-ttu-id="54db1-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-612">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-613">Product 1</span></span></td>
<td><span data-ttu-id="54db1-614">60</span><span class="sxs-lookup"><span data-stu-id="54db1-614">60</span></span></td>
<td><span data-ttu-id="54db1-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="54db1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="54db1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="54db1-616">4,487.12</span></span></td>
<td><span data-ttu-id="54db1-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-618">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-619">Product 2</span></span></td>
<td><span data-ttu-id="54db1-620">20</span><span class="sxs-lookup"><span data-stu-id="54db1-620">20</span></span></td>
<td><span data-ttu-id="54db1-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="54db1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="54db1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="54db1-622">1,495.71</span></span></td>
<td><span data-ttu-id="54db1-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="54db1-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="54db1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-625">Cost object</span></span></th>
<th><span data-ttu-id="54db1-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="54db1-626">Magnitude</span></span></th>
<th><span data-ttu-id="54db1-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="54db1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="54db1-628">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-628">Amount</span></span></th>
<th><span data-ttu-id="54db1-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-630">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-631">Product 1</span></span></td>
<td><span data-ttu-id="54db1-632">80</span><span class="sxs-lookup"><span data-stu-id="54db1-632">80</span></span></td>
<td><span data-ttu-id="54db1-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="54db1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="54db1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="54db1-634">241.05</span></span></td>
<td><span data-ttu-id="54db1-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-636">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-637">Product 2</span></span></td>
<td><span data-ttu-id="54db1-638">15</span><span class="sxs-lookup"><span data-stu-id="54db1-638">15</span></span></td>
<td><span data-ttu-id="54db1-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="54db1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="54db1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="54db1-640">45.20</span></span></td>
<td><span data-ttu-id="54db1-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-642">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-643">Product 1</span></span></td>
<td><span data-ttu-id="54db1-644">80</span><span class="sxs-lookup"><span data-stu-id="54db1-644">80</span></span></td>
<td><span data-ttu-id="54db1-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="54db1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="54db1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="54db1-646">2,507.09</span></span></td>
<td><span data-ttu-id="54db1-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-648">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-649">Product 2</span></span></td>
<td><span data-ttu-id="54db1-650">15</span><span class="sxs-lookup"><span data-stu-id="54db1-650">15</span></span></td>
<td><span data-ttu-id="54db1-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="54db1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="54db1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="54db1-652">470.08</span></span></td>
<td><span data-ttu-id="54db1-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="54db1-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="54db1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-655">Journal</span></span></th>
<th><span data-ttu-id="54db1-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="54db1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="54db1-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="54db1-658">Versija</span><span class="sxs-lookup"><span data-stu-id="54db1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-659">00004</span><span class="sxs-lookup"><span data-stu-id="54db1-659">00004</span></span></td>
<td><span data-ttu-id="54db1-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="54db1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="54db1-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="54db1-661">Fiscal</span></span></td>
<td><span data-ttu-id="54db1-662">2017</span><span class="sxs-lookup"><span data-stu-id="54db1-662">2017</span></span></td>
<td><span data-ttu-id="54db1-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-663">Period 1</span></span></td>
<td><span data-ttu-id="54db1-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="54db1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="54db1-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="54db1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="54db1-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-668">Cost element</span></span></th>
<th><span data-ttu-id="54db1-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-670">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-672">CC001</span></span></td>
<td><span data-ttu-id="54db1-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-673">HR</span></span></td>
<td><span data-ttu-id="54db1-674">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-674">10001</span></span></td>
<td><span data-ttu-id="54db1-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-675">Electricity</span></span></td>
<td><span data-ttu-id="54db1-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-677">500,00</span><span class="sxs-lookup"><span data-stu-id="54db1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-679">CC001</span></span></td>
<td><span data-ttu-id="54db1-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-680">HR</span></span></td>
<td><span data-ttu-id="54db1-681">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-681">10001</span></span></td>
<td><span data-ttu-id="54db1-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-682">Electricity</span></span></td>
<td><span data-ttu-id="54db1-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-683">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="54db1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-686">CC002</span></span></td>
<td><span data-ttu-id="54db1-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-687">Finance</span></span></td>
<td><span data-ttu-id="54db1-688">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-688">10001</span></span></td>
<td><span data-ttu-id="54db1-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-689">Electricity</span></span></td>
<td><span data-ttu-id="54db1-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="54db1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-693">CC002</span></span></td>
<td><span data-ttu-id="54db1-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-694">Finance</span></span></td>
<td><span data-ttu-id="54db1-695">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-695">10001</span></span></td>
<td><span data-ttu-id="54db1-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-696">Electricity</span></span></td>
<td><span data-ttu-id="54db1-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-697">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="54db1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-700">CC003</span></span></td>
<td><span data-ttu-id="54db1-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-701">Assembly</span></span></td>
<td><span data-ttu-id="54db1-702">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-702">10001</span></span></td>
<td><span data-ttu-id="54db1-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-703">Electricity</span></span></td>
<td><span data-ttu-id="54db1-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="54db1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-707">CC003</span></span></td>
<td><span data-ttu-id="54db1-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-708">Assembly</span></span></td>
<td><span data-ttu-id="54db1-709">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-709">10001</span></span></td>
<td><span data-ttu-id="54db1-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-710">Electricity</span></span></td>
<td><span data-ttu-id="54db1-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-711">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="54db1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-714">CC003</span></span></td>
<td><span data-ttu-id="54db1-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-715">Packaging</span></span></td>
<td><span data-ttu-id="54db1-716">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-716">10001</span></span></td>
<td><span data-ttu-id="54db1-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-717">Electricity</span></span></td>
<td><span data-ttu-id="54db1-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="54db1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-721">CC003</span></span></td>
<td><span data-ttu-id="54db1-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-722">Packaging</span></span></td>
<td><span data-ttu-id="54db1-723">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-723">10001</span></span></td>
<td><span data-ttu-id="54db1-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-724">Electricity</span></span></td>
<td><span data-ttu-id="54db1-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-725">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="54db1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-728">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-729">Product 1</span></span></td>
<td><span data-ttu-id="54db1-730">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-730">10001</span></span></td>
<td><span data-ttu-id="54db1-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-731">Electricity</span></span></td>
<td><span data-ttu-id="54db1-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="54db1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-735">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-736">Product 1</span></span></td>
<td><span data-ttu-id="54db1-737">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-737">10001</span></span></td>
<td><span data-ttu-id="54db1-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-738">Electricity</span></span></td>
<td><span data-ttu-id="54db1-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-739">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="54db1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-742">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-743">Product 1</span></span></td>
<td><span data-ttu-id="54db1-744">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-744">10001</span></span></td>
<td><span data-ttu-id="54db1-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-745">Electricity</span></span></td>
<td><span data-ttu-id="54db1-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="54db1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="54db1-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-749">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-750">Product 1</span></span></td>
<td><span data-ttu-id="54db1-751">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-751">10001</span></span></td>
<td><span data-ttu-id="54db1-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-752">Electricity</span></span></td>
<td><span data-ttu-id="54db1-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-753">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="54db1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="54db1-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="54db1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="54db1-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="54db1-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-757">Cost element</span></span></th>
<th><span data-ttu-id="54db1-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="54db1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="54db1-759">Suma</span><span class="sxs-lookup"><span data-stu-id="54db1-759">Amount</span></span></th>
<th><span data-ttu-id="54db1-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="54db1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="54db1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-761">CC001</span></span></td>
<td><span data-ttu-id="54db1-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-762">HR</span></span></td>
<td><span data-ttu-id="54db1-763">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-763">10001</span></span></td>
<td><span data-ttu-id="54db1-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-764">Electricity</span></span></td>
<td><span data-ttu-id="54db1-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="54db1-766">-500.00</span></span></td>
<td><span data-ttu-id="54db1-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-768">CC002</span></span></td>
<td><span data-ttu-id="54db1-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-769">Finance</span></span></td>
<td><span data-ttu-id="54db1-770">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-770">10001</span></span></td>
<td><span data-ttu-id="54db1-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-771">Electricity</span></span></td>
<td><span data-ttu-id="54db1-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="54db1-773">175.00</span></span></td>
<td><span data-ttu-id="54db1-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-775">CC003</span></span></td>
<td><span data-ttu-id="54db1-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-776">Assembly</span></span></td>
<td><span data-ttu-id="54db1-777">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-777">10001</span></span></td>
<td><span data-ttu-id="54db1-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-778">Electricity</span></span></td>
<td><span data-ttu-id="54db1-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="54db1-780">275.00</span></span></td>
<td><span data-ttu-id="54db1-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-782">CC004</span></span></td>
<td><span data-ttu-id="54db1-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-783">Packaging</span></span></td>
<td><span data-ttu-id="54db1-784">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-784">10001</span></span></td>
<td><span data-ttu-id="54db1-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-785">Electricity</span></span></td>
<td><span data-ttu-id="54db1-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="54db1-787">50,00</span></span></td>
<td><span data-ttu-id="54db1-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-789">CC001</span></span></td>
<td><span data-ttu-id="54db1-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="54db1-790">HR</span></span></td>
<td><span data-ttu-id="54db1-791">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-791">10001</span></span></td>
<td><span data-ttu-id="54db1-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-792">Electricity</span></span></td>
<td><span data-ttu-id="54db1-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-793">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="54db1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="54db1-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-796">CC002</span></span></td>
<td><span data-ttu-id="54db1-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-797">Finance</span></span></td>
<td><span data-ttu-id="54db1-798">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-798">10001</span></span></td>
<td><span data-ttu-id="54db1-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-799">Electricity</span></span></td>
<td><span data-ttu-id="54db1-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-800">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="54db1-801">436.00</span></span></td>
<td><span data-ttu-id="54db1-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-803">CC003</span></span></td>
<td><span data-ttu-id="54db1-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-804">Assembly</span></span></td>
<td><span data-ttu-id="54db1-805">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-805">10001</span></span></td>
<td><span data-ttu-id="54db1-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-806">Electricity</span></span></td>
<td><span data-ttu-id="54db1-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-807">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="54db1-808">685.14</span></span></td>
<td><span data-ttu-id="54db1-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-810">CC004</span></span></td>
<td><span data-ttu-id="54db1-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-811">Packaging</span></span></td>
<td><span data-ttu-id="54db1-812">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-812">10001</span></span></td>
<td><span data-ttu-id="54db1-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-813">Electricity</span></span></td>
<td><span data-ttu-id="54db1-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-814">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="54db1-815">124.57</span></span></td>
<td><span data-ttu-id="54db1-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-817">CC002</span></span></td>
<td><span data-ttu-id="54db1-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-818">Finance</span></span></td>
<td><span data-ttu-id="54db1-819">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-819">10001</span></span></td>
<td><span data-ttu-id="54db1-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-820">Electricity</span></span></td>
<td><span data-ttu-id="54db1-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="54db1-822">-675.00</span></span></td>
<td><span data-ttu-id="54db1-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-824">CC003</span></span></td>
<td><span data-ttu-id="54db1-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-825">Assembly</span></span></td>
<td><span data-ttu-id="54db1-826">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-826">10001</span></span></td>
<td><span data-ttu-id="54db1-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-827">Electricity</span></span></td>
<td><span data-ttu-id="54db1-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="54db1-829">438.75</span></span></td>
<td><span data-ttu-id="54db1-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-831">CC004</span></span></td>
<td><span data-ttu-id="54db1-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-832">Packaging</span></span></td>
<td><span data-ttu-id="54db1-833">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-833">10001</span></span></td>
<td><span data-ttu-id="54db1-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-834">Electricity</span></span></td>
<td><span data-ttu-id="54db1-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="54db1-836">236.25</span></span></td>
<td><span data-ttu-id="54db1-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-838">CC002</span></span></td>
<td><span data-ttu-id="54db1-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="54db1-839">Finance</span></span></td>
<td><span data-ttu-id="54db1-840">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-840">10001</span></span></td>
<td><span data-ttu-id="54db1-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-841">Electricity</span></span></td>
<td><span data-ttu-id="54db1-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-842">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="54db1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="54db1-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-845">CC003</span></span></td>
<td><span data-ttu-id="54db1-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-846">Assembly</span></span></td>
<td><span data-ttu-id="54db1-847">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-847">10001</span></span></td>
<td><span data-ttu-id="54db1-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-848">Electricity</span></span></td>
<td><span data-ttu-id="54db1-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-849">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="54db1-850">5,297.69</span></span></td>
<td><span data-ttu-id="54db1-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-852">CC004</span></span></td>
<td><span data-ttu-id="54db1-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="54db1-853">Packaging</span></span></td>
<td><span data-ttu-id="54db1-854">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-854">10001</span></span></td>
<td><span data-ttu-id="54db1-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-855">Electricity</span></span></td>
<td><span data-ttu-id="54db1-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-856">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="54db1-857">2,852.60</span></span></td>
<td><span data-ttu-id="54db1-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-859">CC003</span></span></td>
<td><span data-ttu-id="54db1-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-860">Assembly</span></span></td>
<td><span data-ttu-id="54db1-861">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-861">10001</span></span></td>
<td><span data-ttu-id="54db1-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-862">Electricity</span></span></td>
<td><span data-ttu-id="54db1-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="54db1-864">-713.75</span></span></td>
<td><span data-ttu-id="54db1-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-866">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-867">Product 1</span></span></td>
<td><span data-ttu-id="54db1-868">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-868">10001</span></span></td>
<td><span data-ttu-id="54db1-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-869">Electricity</span></span></td>
<td><span data-ttu-id="54db1-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="54db1-871">535.31</span></span></td>
<td><span data-ttu-id="54db1-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-873">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-874">Product 2</span></span></td>
<td><span data-ttu-id="54db1-875">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-875">10001</span></span></td>
<td><span data-ttu-id="54db1-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-876">Electricity</span></span></td>
<td><span data-ttu-id="54db1-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="54db1-878">178.44</span></span></td>
<td><span data-ttu-id="54db1-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-880">CC003</span></span></td>
<td><span data-ttu-id="54db1-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-881">Assembly</span></span></td>
<td><span data-ttu-id="54db1-882">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-882">10001</span></span></td>
<td><span data-ttu-id="54db1-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-883">Electricity</span></span></td>
<td><span data-ttu-id="54db1-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-884">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="54db1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="54db1-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-887">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-888">Product 1</span></span></td>
<td><span data-ttu-id="54db1-889">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-889">10001</span></span></td>
<td><span data-ttu-id="54db1-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-890">Electricity</span></span></td>
<td><span data-ttu-id="54db1-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-891">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="54db1-892">4,487.12</span></span></td>
<td><span data-ttu-id="54db1-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-894">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-895">Product 2</span></span></td>
<td><span data-ttu-id="54db1-896">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-896">10001</span></span></td>
<td><span data-ttu-id="54db1-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-897">Electricity</span></span></td>
<td><span data-ttu-id="54db1-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-898">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="54db1-899">1,495.71</span></span></td>
<td><span data-ttu-id="54db1-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-901">CC003</span></span></td>
<td><span data-ttu-id="54db1-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-902">Assembly</span></span></td>
<td><span data-ttu-id="54db1-903">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-903">10001</span></span></td>
<td><span data-ttu-id="54db1-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-904">Electricity</span></span></td>
<td><span data-ttu-id="54db1-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="54db1-906">-286.25</span></span></td>
<td><span data-ttu-id="54db1-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-908">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-909">Product 1</span></span></td>
<td><span data-ttu-id="54db1-910">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-910">10001</span></span></td>
<td><span data-ttu-id="54db1-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-911">Electricity</span></span></td>
<td><span data-ttu-id="54db1-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="54db1-913">241.05</span></span></td>
<td><span data-ttu-id="54db1-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-915">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-916">Product 2</span></span></td>
<td><span data-ttu-id="54db1-917">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-917">10001</span></span></td>
<td><span data-ttu-id="54db1-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-918">Electricity</span></span></td>
<td><span data-ttu-id="54db1-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="54db1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="54db1-920">45.20</span></span></td>
<td><span data-ttu-id="54db1-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-922">CC003</span></span></td>
<td><span data-ttu-id="54db1-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="54db1-923">Assembly</span></span></td>
<td><span data-ttu-id="54db1-924">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-924">10001</span></span></td>
<td><span data-ttu-id="54db1-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-925">Electricity</span></span></td>
<td><span data-ttu-id="54db1-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-926">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="54db1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="54db1-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-929">Prod 1</span></span></td>
<td><span data-ttu-id="54db1-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-930">Product 1</span></span></td>
<td><span data-ttu-id="54db1-931">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-931">10001</span></span></td>
<td><span data-ttu-id="54db1-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-932">Electricity</span></span></td>
<td><span data-ttu-id="54db1-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-933">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="54db1-934">2,507.09</span></span></td>
<td><span data-ttu-id="54db1-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="54db1-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-936">Prod 2</span></span></td>
<td><span data-ttu-id="54db1-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="54db1-937">Product 2</span></span></td>
<td><span data-ttu-id="54db1-938">10001</span><span class="sxs-lookup"><span data-stu-id="54db1-938">10001</span></span></td>
<td><span data-ttu-id="54db1-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-939">Electricity</span></span></td>
<td><span data-ttu-id="54db1-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-940">Variable cost</span></span></td>
<td><span data-ttu-id="54db1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="54db1-941">470.08</span></span></td>
<td><span data-ttu-id="54db1-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="54db1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="54db1-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="54db1-943">Conclusion</span></span>
<span data-ttu-id="54db1-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="54db1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="54db1-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="54db1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="54db1-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="54db1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="54db1-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="54db1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="54db1-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="54db1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="54db1-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="54db1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="54db1-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="54db1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="54db1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="54db1-951">CC099</span></span></th>
<th><span data-ttu-id="54db1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="54db1-952">CC001</span></span></th>
<th><span data-ttu-id="54db1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="54db1-953">CC002</span></span></th>
<th><span data-ttu-id="54db1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="54db1-954">CC003</span></span></th>
<th><span data-ttu-id="54db1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="54db1-955">CC004</span></span></th>
<th><span data-ttu-id="54db1-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-956">Proj 1</span></span></th>
<th><span data-ttu-id="54db1-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="54db1-957">Proj 2</span></span></th>
<th><span data-ttu-id="54db1-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-958">Prod 1</span></span></th>
<th><span data-ttu-id="54db1-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="54db1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="54db1-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="54db1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="54db1-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="54db1-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="54db1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="54db1-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="54db1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="54db1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="54db1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="54db1-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="54db1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-982">000</span><span class="sxs-lookup"><span data-stu-id="54db1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="54db1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-987">30,00</span><span class="sxs-lookup"><span data-stu-id="54db1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="54db1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="54db1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="54db1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="54db1-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="54db1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="54db1-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="54db1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="54db1-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="54db1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="54db1-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="54db1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="54db1-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="54db1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="54db1-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="54db1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



