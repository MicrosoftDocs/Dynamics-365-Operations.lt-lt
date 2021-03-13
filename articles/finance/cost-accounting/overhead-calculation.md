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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009523"
---
# <a name="overhead-calculation"></a><span data-ttu-id="3345f-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="3345f-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3345f-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="3345f-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="3345f-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="3345f-105">Term definition</span></span>
---------------

<span data-ttu-id="3345f-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="3345f-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="3345f-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="3345f-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="3345f-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="3345f-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="3345f-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="3345f-109">Rent</span></span>
-   <span data-ttu-id="3345f-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-110">Electricity</span></span>
-   <span data-ttu-id="3345f-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="3345f-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="3345f-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="3345f-112">Overhead calculation overview</span></span>
<span data-ttu-id="3345f-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="3345f-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="3345f-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="3345f-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="3345f-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="3345f-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="3345f-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="3345f-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="3345f-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="3345f-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="3345f-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="3345f-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="3345f-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="3345f-119">Version type</span></span>
-   <span data-ttu-id="3345f-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="3345f-120">Date and time</span></span>
-   <span data-ttu-id="3345f-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="3345f-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="3345f-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="3345f-122">Fiscal year</span></span>
-   <span data-ttu-id="3345f-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-123">Fiscal period</span></span>

<span data-ttu-id="3345f-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="3345f-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="3345f-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="3345f-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="3345f-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="3345f-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="3345f-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="3345f-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="3345f-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="3345f-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="3345f-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="3345f-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="3345f-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="3345f-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="3345f-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="3345f-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="3345f-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="3345f-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="3345f-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="3345f-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="3345f-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="3345f-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="3345f-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="3345f-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="3345f-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="3345f-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="3345f-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="3345f-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="3345f-140">Main account</span></span></th>
<th><span data-ttu-id="3345f-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="3345f-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="3345f-143">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-143">CC099</span></span></td>
<td><span data-ttu-id="3345f-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-144">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-145">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-145">10001</span></span></td>
<td><span data-ttu-id="3345f-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-146">Electricity</span></span></td>
<td><span data-ttu-id="3345f-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="3345f-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3345f-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="3345f-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="3345f-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="3345f-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="3345f-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="3345f-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="3345f-151">Define the cost behavior rule</span></span>

<span data-ttu-id="3345f-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="3345f-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="3345f-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="3345f-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="3345f-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="3345f-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="3345f-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="3345f-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="3345f-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="3345f-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="3345f-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="3345f-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="3345f-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="3345f-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-160">Journal</span></span></th>
<th><span data-ttu-id="3345f-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="3345f-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3345f-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3345f-163">Versija</span><span class="sxs-lookup"><span data-stu-id="3345f-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-164">00001</span><span class="sxs-lookup"><span data-stu-id="3345f-164">00001</span></span></td>
<td><span data-ttu-id="3345f-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="3345f-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="3345f-166">Fiscal</span></span></td>
<td><span data-ttu-id="3345f-167">2017</span><span class="sxs-lookup"><span data-stu-id="3345f-167">2017</span></span></td>
<td><span data-ttu-id="3345f-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-168">Period 1</span></span></td>
<td><span data-ttu-id="3345f-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3345f-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="3345f-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-173">Cost element</span></span></th>
<th><span data-ttu-id="3345f-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-174">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-175">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="3345f-177">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-177">CC099</span></span></td>
<td><span data-ttu-id="3345f-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-178">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-179">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-179">10001</span></span></td>
<td><span data-ttu-id="3345f-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-180">Electricity</span></span></td>
<td><span data-ttu-id="3345f-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="3345f-181">Unclassified</span></span></td>
<td><span data-ttu-id="3345f-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3345f-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="3345f-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-185">Cost element</span></span></th>
<th><span data-ttu-id="3345f-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-186">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-187">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-187">Amount</span></span></th>
<th><span data-ttu-id="3345f-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-189">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-189">CC099</span></span></td>
<td><span data-ttu-id="3345f-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-190">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-191">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-191">10001</span></span></td>
<td><span data-ttu-id="3345f-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-192">Electricity</span></span></td>
<td><span data-ttu-id="3345f-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="3345f-193">Unclassified</span></span></td>
<td><span data-ttu-id="3345f-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-194">10,000.00</span></span></td>
<td><span data-ttu-id="3345f-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-196">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-196">CC099</span></span></td>
<td><span data-ttu-id="3345f-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-197">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-198">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-198">10001</span></span></td>
<td><span data-ttu-id="3345f-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-199">Electricity</span></span></td>
<td><span data-ttu-id="3345f-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="3345f-200">Unclassified</span></span></td>
<td><span data-ttu-id="3345f-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="3345f-201">-10,000.00</span></span></td>
<td><span data-ttu-id="3345f-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-203">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-203">CC099</span></span></td>
<td><span data-ttu-id="3345f-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-204">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-205">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-205">10001</span></span></td>
<td><span data-ttu-id="3345f-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-206">Electricity</span></span></td>
<td><span data-ttu-id="3345f-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-207">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-208">1,000.00</span></span></td>
<td><span data-ttu-id="3345f-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-210">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-210">CC099</span></span></td>
<td><span data-ttu-id="3345f-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-211">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-212">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-212">10001</span></span></td>
<td><span data-ttu-id="3345f-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-213">Electricity</span></span></td>
<td><span data-ttu-id="3345f-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-214">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3345f-215">9,000.00</span></span></td>
<td><span data-ttu-id="3345f-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="3345f-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="3345f-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3345f-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="3345f-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="3345f-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="3345f-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="3345f-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="3345f-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="3345f-221">Define the cost distribution rule</span></span>

<span data-ttu-id="3345f-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="3345f-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="3345f-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="3345f-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="3345f-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="3345f-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="3345f-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="3345f-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="3345f-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="3345f-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="3345f-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="3345f-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-228">Cost object</span></span></th>
<th><span data-ttu-id="3345f-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="3345f-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-230">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-230">CC001</span></span></td>
<td><span data-ttu-id="3345f-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-231">HR</span></span></td>
<td><span data-ttu-id="3345f-232">1000</span><span class="sxs-lookup"><span data-stu-id="3345f-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-233">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-233">CC002</span></span></td>
<td><span data-ttu-id="3345f-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-234">Finance</span></span></td>
<td><span data-ttu-id="3345f-235">6,000</span><span class="sxs-lookup"><span data-stu-id="3345f-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-236">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-236">CC003</span></span></td>
<td><span data-ttu-id="3345f-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-237">Assembly</span></span></td>
<td><span data-ttu-id="3345f-238">0</span><span class="sxs-lookup"><span data-stu-id="3345f-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-240">Cost object</span></span></th>
<th><span data-ttu-id="3345f-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-241">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-242">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-243">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-244">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-244">CC001</span></span></td>
<td><span data-ttu-id="3345f-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-245">HR</span></span></td>
<td><span data-ttu-id="3345f-246">1000</span><span class="sxs-lookup"><span data-stu-id="3345f-246">1,000</span></span></td>
<td><span data-ttu-id="3345f-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3345f-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3345f-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-249">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-249">CC002</span></span></td>
<td><span data-ttu-id="3345f-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-250">Finance</span></span></td>
<td><span data-ttu-id="3345f-251">6,000</span><span class="sxs-lookup"><span data-stu-id="3345f-251">6,000</span></span></td>
<td><span data-ttu-id="3345f-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3345f-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3345f-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-254">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-254">CC003</span></span></td>
<td><span data-ttu-id="3345f-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-255">Assembly</span></span></td>
<td><span data-ttu-id="3345f-256">0</span><span class="sxs-lookup"><span data-stu-id="3345f-256">0</span></span></td>
<td><span data-ttu-id="3345f-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3345f-258">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="3345f-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="3345f-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-261">Cost object</span></span></th>
<th><span data-ttu-id="3345f-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="3345f-262">Formula</span></span></th>
<th><span data-ttu-id="3345f-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-263">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-264">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-265">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-266">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-266">CC001</span></span></td>
<td><span data-ttu-id="3345f-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-267">HR</span></span></td>
<td><span data-ttu-id="3345f-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3345f-269">1</span><span class="sxs-lookup"><span data-stu-id="3345f-269">1</span></span></td>
<td><span data-ttu-id="3345f-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3345f-271">500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-272">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-272">CC002</span></span></td>
<td><span data-ttu-id="3345f-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-273">Finance</span></span></td>
<td><span data-ttu-id="3345f-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3345f-275">1</span><span class="sxs-lookup"><span data-stu-id="3345f-275">1</span></span></td>
<td><span data-ttu-id="3345f-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3345f-277">500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-278">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-278">CC003</span></span></td>
<td><span data-ttu-id="3345f-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-279">Assembly</span></span></td>
<td><span data-ttu-id="3345f-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3345f-281">0</span><span class="sxs-lookup"><span data-stu-id="3345f-281">0</span></span></td>
<td><span data-ttu-id="3345f-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3345f-283">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3345f-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-285">Journal</span></span></th>
<th><span data-ttu-id="3345f-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="3345f-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3345f-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3345f-288">Versija</span><span class="sxs-lookup"><span data-stu-id="3345f-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-289">00002</span><span class="sxs-lookup"><span data-stu-id="3345f-289">00002</span></span></td>
<td><span data-ttu-id="3345f-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="3345f-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="3345f-291">Fiscal</span></span></td>
<td><span data-ttu-id="3345f-292">2017</span><span class="sxs-lookup"><span data-stu-id="3345f-292">2017</span></span></td>
<td><span data-ttu-id="3345f-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-293">Period 1</span></span></td>
<td><span data-ttu-id="3345f-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3345f-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="3345f-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-298">Cost element</span></span></th>
<th><span data-ttu-id="3345f-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-299">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-300">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-302">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-302">CC099</span></span></td>
<td><span data-ttu-id="3345f-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-303">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-304">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-304">10001</span></span></td>
<td><span data-ttu-id="3345f-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-305">Electricity</span></span></td>
<td><span data-ttu-id="3345f-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-306">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="3345f-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-309">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-309">CC099</span></span></td>
<td><span data-ttu-id="3345f-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-310">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-311">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-311">10001</span></span></td>
<td><span data-ttu-id="3345f-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-312">Electricity</span></span></td>
<td><span data-ttu-id="3345f-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-313">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3345f-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3345f-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="3345f-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-317">Cost element</span></span></th>
<th><span data-ttu-id="3345f-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-318">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-319">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-319">Amount</span></span></th>
<th><span data-ttu-id="3345f-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-321">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-321">CC099</span></span></td>
<td><span data-ttu-id="3345f-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-322">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-323">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-323">10001</span></span></td>
<td><span data-ttu-id="3345f-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-324">Electricity</span></span></td>
<td><span data-ttu-id="3345f-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-325">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="3345f-326">-1,000.00</span></span></td>
<td><span data-ttu-id="3345f-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-328">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-328">CC001</span></span></td>
<td><span data-ttu-id="3345f-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-329">HR</span></span></td>
<td><span data-ttu-id="3345f-330">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-330">10001</span></span></td>
<td><span data-ttu-id="3345f-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-331">Electricity</span></span></td>
<td><span data-ttu-id="3345f-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-332">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-333">500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-333">500.00</span></span></td>
<td><span data-ttu-id="3345f-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-335">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-335">CC002</span></span></td>
<td><span data-ttu-id="3345f-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-336">Finance</span></span></td>
<td><span data-ttu-id="3345f-337">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-337">10001</span></span></td>
<td><span data-ttu-id="3345f-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-338">Electricity</span></span></td>
<td><span data-ttu-id="3345f-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-339">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-340">500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-340">500.00</span></span></td>
<td><span data-ttu-id="3345f-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-342">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-342">CC099</span></span></td>
<td><span data-ttu-id="3345f-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="3345f-343">Default cost center</span></span></td>
<td><span data-ttu-id="3345f-344">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-344">10001</span></span></td>
<td><span data-ttu-id="3345f-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-345">Electricity</span></span></td>
<td><span data-ttu-id="3345f-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-346">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="3345f-347">-9,000.00</span></span></td>
<td><span data-ttu-id="3345f-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-349">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-349">CC001</span></span></td>
<td><span data-ttu-id="3345f-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-350">HR</span></span></td>
<td><span data-ttu-id="3345f-351">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-351">10001</span></span></td>
<td><span data-ttu-id="3345f-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-352">Electricity</span></span></td>
<td><span data-ttu-id="3345f-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-353">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3345f-354">1,285.71</span></span></td>
<td><span data-ttu-id="3345f-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-356">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-356">CC002</span></span></td>
<td><span data-ttu-id="3345f-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-357">Finance</span></span></td>
<td><span data-ttu-id="3345f-358">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-358">10001</span></span></td>
<td><span data-ttu-id="3345f-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-359">Electricity</span></span></td>
<td><span data-ttu-id="3345f-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-360">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3345f-361">7,714.29</span></span></td>
<td><span data-ttu-id="3345f-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="3345f-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="3345f-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="3345f-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="3345f-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="3345f-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="3345f-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="3345f-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3345f-367">Define the overhead rate</span></span>

<span data-ttu-id="3345f-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="3345f-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3345f-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-370">Cost object</span></span></th>
<th><span data-ttu-id="3345f-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="3345f-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-372">Proj 1</span></span></td>
<td><span data-ttu-id="3345f-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-373">Project 1</span></span></td>
<td><span data-ttu-id="3345f-374">3</span><span class="sxs-lookup"><span data-stu-id="3345f-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-375">Proj 2</span></span></td>
<td><span data-ttu-id="3345f-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-376">Project 2</span></span></td>
<td><span data-ttu-id="3345f-377">1</span><span class="sxs-lookup"><span data-stu-id="3345f-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="3345f-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-379">Cost object</span></span></th>
<th><span data-ttu-id="3345f-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-380">Cost element</span></span></th>
<th><span data-ttu-id="3345f-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-381">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="3345f-382">Units</span></span></th>
<th><span data-ttu-id="3345f-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="3345f-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-384">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-384">CC001</span></span></td>
<td><span data-ttu-id="3345f-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-385">HR</span></span></td>
<td><span data-ttu-id="3345f-386">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-386">10001</span></span></td>
<td><span data-ttu-id="3345f-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-387">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-388">1</span><span class="sxs-lookup"><span data-stu-id="3345f-388">1</span></span></td>
<td><span data-ttu-id="3345f-389">10</span><span class="sxs-lookup"><span data-stu-id="3345f-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-391">Cost object</span></span></th>
<th><span data-ttu-id="3345f-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-392">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-393">Cost element</span></span></th>
<th><span data-ttu-id="3345f-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-394">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-395">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-396">Proj 1</span></span></td>
<td><span data-ttu-id="3345f-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-397">Project 1</span></span></td>
<td><span data-ttu-id="3345f-398">3</span><span class="sxs-lookup"><span data-stu-id="3345f-398">3</span></span></td>
<td><span data-ttu-id="3345f-399">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-399">10001</span></span></td>
<td><span data-ttu-id="3345f-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="3345f-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3345f-401">30,00</span><span class="sxs-lookup"><span data-stu-id="3345f-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-402">Proj 2</span></span></td>
<td><span data-ttu-id="3345f-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-403">Project 2</span></span></td>
<td><span data-ttu-id="3345f-404">1</span><span class="sxs-lookup"><span data-stu-id="3345f-404">1</span></span></td>
<td><span data-ttu-id="3345f-405">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-405">10001</span></span></td>
<td><span data-ttu-id="3345f-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="3345f-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3345f-407">10,00</span><span class="sxs-lookup"><span data-stu-id="3345f-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3345f-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-409">Journal</span></span></th>
<th><span data-ttu-id="3345f-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="3345f-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3345f-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3345f-412">Versija</span><span class="sxs-lookup"><span data-stu-id="3345f-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-413">00003</span><span class="sxs-lookup"><span data-stu-id="3345f-413">00003</span></span></td>
<td><span data-ttu-id="3345f-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="3345f-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="3345f-415">Fiscal</span></span></td>
<td><span data-ttu-id="3345f-416">2017</span><span class="sxs-lookup"><span data-stu-id="3345f-416">2017</span></span></td>
<td><span data-ttu-id="3345f-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-417">Period 1</span></span></td>
<td><span data-ttu-id="3345f-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="3345f-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="3345f-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-421">Cost object</span></span></th>
<th><span data-ttu-id="3345f-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-424">Proj 1</span></span></td>
<td><span data-ttu-id="3345f-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3345f-426">3,00</span><span class="sxs-lookup"><span data-stu-id="3345f-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-428">Proj 2</span></span></td>
<td><span data-ttu-id="3345f-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3345f-430">1,00</span><span class="sxs-lookup"><span data-stu-id="3345f-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3345f-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="3345f-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-433">Cost element</span></span></th>
<th><span data-ttu-id="3345f-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-434">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-435">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-435">Amount</span></span></th>
<th><span data-ttu-id="3345f-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="3345f-437">CC0001</span></span></td>
<td><span data-ttu-id="3345f-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-438">HR</span></span></td>
<td><span data-ttu-id="3345f-439">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-439">10001</span></span></td>
<td><span data-ttu-id="3345f-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-440">Electricity</span></span></td>
<td><span data-ttu-id="3345f-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-441">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="3345f-442">-30.00</span></span></td>
<td><span data-ttu-id="3345f-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-444">Proj 1</span></span></td>
<td><span data-ttu-id="3345f-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3345f-446">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-446">10001</span></span></td>
<td><span data-ttu-id="3345f-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-447">Electricity</span></span></td>
<td><span data-ttu-id="3345f-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-448">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-449">30,00</span><span class="sxs-lookup"><span data-stu-id="3345f-449">30.00</span></span></td>
<td><span data-ttu-id="3345f-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-451">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-451">CC001</span></span></td>
<td><span data-ttu-id="3345f-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-452">HR</span></span></td>
<td><span data-ttu-id="3345f-453">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-453">10001</span></span></td>
<td><span data-ttu-id="3345f-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-454">Electricity</span></span></td>
<td><span data-ttu-id="3345f-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-455">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="3345f-456">-10.00</span></span></td>
<td><span data-ttu-id="3345f-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-458">Proj 2</span></span></td>
<td><span data-ttu-id="3345f-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3345f-460">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-460">10001</span></span></td>
<td><span data-ttu-id="3345f-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-461">Electricity</span></span></td>
<td><span data-ttu-id="3345f-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-462">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-463">10,00</span><span class="sxs-lookup"><span data-stu-id="3345f-463">10.00</span></span></td>
<td><span data-ttu-id="3345f-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="3345f-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="3345f-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3345f-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="3345f-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="3345f-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="3345f-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="3345f-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="3345f-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="3345f-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="3345f-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="3345f-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="3345f-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="3345f-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="3345f-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="3345f-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="3345f-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="3345f-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="3345f-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3345f-475">Define the cost allocation</span></span>

<span data-ttu-id="3345f-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="3345f-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="3345f-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="3345f-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3345f-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-479">Cost object</span></span></th>
<th><span data-ttu-id="3345f-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="3345f-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-481">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-481">CC002</span></span></td>
<td><span data-ttu-id="3345f-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-482">Finance</span></span></td>
<td><span data-ttu-id="3345f-483">35</span><span class="sxs-lookup"><span data-stu-id="3345f-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-484">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-484">CC003</span></span></td>
<td><span data-ttu-id="3345f-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-485">Assembly</span></span></td>
<td><span data-ttu-id="3345f-486">55</span><span class="sxs-lookup"><span data-stu-id="3345f-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-487">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-487">CC004</span></span></td>
<td><span data-ttu-id="3345f-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-488">Packaging</span></span></td>
<td><span data-ttu-id="3345f-489">10</span><span class="sxs-lookup"><span data-stu-id="3345f-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="3345f-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3345f-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-492">Cost object</span></span></th>
<th><span data-ttu-id="3345f-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="3345f-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-494">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-494">CC003</span></span></td>
<td><span data-ttu-id="3345f-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-495">Assembly</span></span></td>
<td><span data-ttu-id="3345f-496">65</span><span class="sxs-lookup"><span data-stu-id="3345f-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-497">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-497">CC004</span></span></td>
<td><span data-ttu-id="3345f-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-498">Packaging</span></span></td>
<td><span data-ttu-id="3345f-499">35</span><span class="sxs-lookup"><span data-stu-id="3345f-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="3345f-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3345f-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-502">Cost object</span></span></th>
<th><span data-ttu-id="3345f-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="3345f-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-504">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-505">Product 1</span></span></td>
<td><span data-ttu-id="3345f-506">60</span><span class="sxs-lookup"><span data-stu-id="3345f-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-507">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-508">Product 2</span></span></td>
<td><span data-ttu-id="3345f-509">20</span><span class="sxs-lookup"><span data-stu-id="3345f-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="3345f-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="3345f-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3345f-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-512">Cost object</span></span></th>
<th><span data-ttu-id="3345f-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="3345f-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-514">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-515">Product 1</span></span></td>
<td><span data-ttu-id="3345f-516">80</span><span class="sxs-lookup"><span data-stu-id="3345f-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-517">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-518">Product 2</span></span></td>
<td><span data-ttu-id="3345f-519">15</span><span class="sxs-lookup"><span data-stu-id="3345f-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3345f-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="3345f-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="3345f-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="3345f-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="3345f-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-523">Cost object</span></span></th>
<th><span data-ttu-id="3345f-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-524">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-525">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-526">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-526">Amount</span></span></th>
<th><span data-ttu-id="3345f-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-528">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-528">CC002</span></span></td>
<td><span data-ttu-id="3345f-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-529">Finance</span></span></td>
<td><span data-ttu-id="3345f-530">35</span><span class="sxs-lookup"><span data-stu-id="3345f-530">35</span></span></td>
<td><span data-ttu-id="3345f-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3345f-532">175.00</span><span class="sxs-lookup"><span data-stu-id="3345f-532">175.00</span></span></td>
<td><span data-ttu-id="3345f-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-534">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-534">CC003</span></span></td>
<td><span data-ttu-id="3345f-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-535">Assembly</span></span></td>
<td><span data-ttu-id="3345f-536">55</span><span class="sxs-lookup"><span data-stu-id="3345f-536">55</span></span></td>
<td><span data-ttu-id="3345f-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3345f-538">275.00</span><span class="sxs-lookup"><span data-stu-id="3345f-538">275.00</span></span></td>
<td><span data-ttu-id="3345f-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-540">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-540">CC004</span></span></td>
<td><span data-ttu-id="3345f-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-541">Packaging</span></span></td>
<td><span data-ttu-id="3345f-542">10</span><span class="sxs-lookup"><span data-stu-id="3345f-542">10</span></span></td>
<td><span data-ttu-id="3345f-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3345f-544">50,00</span><span class="sxs-lookup"><span data-stu-id="3345f-544">50.00</span></span></td>
<td><span data-ttu-id="3345f-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-546">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-546">CC002</span></span></td>
<td><span data-ttu-id="3345f-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-547">Finance</span></span></td>
<td><span data-ttu-id="3345f-548">35</span><span class="sxs-lookup"><span data-stu-id="3345f-548">35</span></span></td>
<td><span data-ttu-id="3345f-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="3345f-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3345f-550">436.00</span><span class="sxs-lookup"><span data-stu-id="3345f-550">436.00</span></span></td>
<td><span data-ttu-id="3345f-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-552">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-552">CC003</span></span></td>
<td><span data-ttu-id="3345f-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-553">Assembly</span></span></td>
<td><span data-ttu-id="3345f-554">55</span><span class="sxs-lookup"><span data-stu-id="3345f-554">55</span></span></td>
<td><span data-ttu-id="3345f-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="3345f-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3345f-556">685.14</span><span class="sxs-lookup"><span data-stu-id="3345f-556">685.14</span></span></td>
<td><span data-ttu-id="3345f-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-558">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-558">CC004</span></span></td>
<td><span data-ttu-id="3345f-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-559">Packaging</span></span></td>
<td><span data-ttu-id="3345f-560">10</span><span class="sxs-lookup"><span data-stu-id="3345f-560">10</span></span></td>
<td><span data-ttu-id="3345f-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="3345f-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3345f-562">124.57</span><span class="sxs-lookup"><span data-stu-id="3345f-562">124.57</span></span></td>
<td><span data-ttu-id="3345f-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-565">Cost object</span></span></th>
<th><span data-ttu-id="3345f-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-566">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-567">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-568">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-568">Amount</span></span></th>
<th><span data-ttu-id="3345f-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-570">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-570">CC003</span></span></td>
<td><span data-ttu-id="3345f-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-571">Assembly</span></span></td>
<td><span data-ttu-id="3345f-572">65</span><span class="sxs-lookup"><span data-stu-id="3345f-572">65</span></span></td>
<td><span data-ttu-id="3345f-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3345f-574">438.75</span><span class="sxs-lookup"><span data-stu-id="3345f-574">438.75</span></span></td>
<td><span data-ttu-id="3345f-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-576">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-576">CC004</span></span></td>
<td><span data-ttu-id="3345f-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-577">Packaging</span></span></td>
<td><span data-ttu-id="3345f-578">35</span><span class="sxs-lookup"><span data-stu-id="3345f-578">35</span></span></td>
<td><span data-ttu-id="3345f-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3345f-580">236.25</span><span class="sxs-lookup"><span data-stu-id="3345f-580">236.25</span></span></td>
<td><span data-ttu-id="3345f-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-582">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-582">CC003</span></span></td>
<td><span data-ttu-id="3345f-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-583">Assembly</span></span></td>
<td><span data-ttu-id="3345f-584">65</span><span class="sxs-lookup"><span data-stu-id="3345f-584">65</span></span></td>
<td><span data-ttu-id="3345f-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3345f-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3345f-586">5,297.69</span></span></td>
<td><span data-ttu-id="3345f-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-588">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-588">CC004</span></span></td>
<td><span data-ttu-id="3345f-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-589">Packaging</span></span></td>
<td><span data-ttu-id="3345f-590">35</span><span class="sxs-lookup"><span data-stu-id="3345f-590">35</span></span></td>
<td><span data-ttu-id="3345f-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="3345f-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3345f-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3345f-592">2,852.60</span></span></td>
<td><span data-ttu-id="3345f-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-595">Cost object</span></span></th>
<th><span data-ttu-id="3345f-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-596">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-597">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-598">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-598">Amount</span></span></th>
<th><span data-ttu-id="3345f-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-600">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-601">Product 1</span></span></td>
<td><span data-ttu-id="3345f-602">60</span><span class="sxs-lookup"><span data-stu-id="3345f-602">60</span></span></td>
<td><span data-ttu-id="3345f-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="3345f-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3345f-604">535.31</span><span class="sxs-lookup"><span data-stu-id="3345f-604">535.31</span></span></td>
<td><span data-ttu-id="3345f-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-606">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-607">Product 2</span></span></td>
<td><span data-ttu-id="3345f-608">20</span><span class="sxs-lookup"><span data-stu-id="3345f-608">20</span></span></td>
<td><span data-ttu-id="3345f-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="3345f-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3345f-610">178.44</span><span class="sxs-lookup"><span data-stu-id="3345f-610">178.44</span></span></td>
<td><span data-ttu-id="3345f-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-612">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-613">Product 1</span></span></td>
<td><span data-ttu-id="3345f-614">60</span><span class="sxs-lookup"><span data-stu-id="3345f-614">60</span></span></td>
<td><span data-ttu-id="3345f-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="3345f-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3345f-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3345f-616">4,487.12</span></span></td>
<td><span data-ttu-id="3345f-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-618">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-619">Product 2</span></span></td>
<td><span data-ttu-id="3345f-620">20</span><span class="sxs-lookup"><span data-stu-id="3345f-620">20</span></span></td>
<td><span data-ttu-id="3345f-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="3345f-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3345f-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3345f-622">1,495.71</span></span></td>
<td><span data-ttu-id="3345f-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3345f-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="3345f-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-625">Cost object</span></span></th>
<th><span data-ttu-id="3345f-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="3345f-626">Magnitude</span></span></th>
<th><span data-ttu-id="3345f-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="3345f-627">Allocation factor</span></span></th>
<th><span data-ttu-id="3345f-628">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-628">Amount</span></span></th>
<th><span data-ttu-id="3345f-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-630">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-631">Product 1</span></span></td>
<td><span data-ttu-id="3345f-632">80</span><span class="sxs-lookup"><span data-stu-id="3345f-632">80</span></span></td>
<td><span data-ttu-id="3345f-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="3345f-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3345f-634">241.05</span><span class="sxs-lookup"><span data-stu-id="3345f-634">241.05</span></span></td>
<td><span data-ttu-id="3345f-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-636">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-637">Product 2</span></span></td>
<td><span data-ttu-id="3345f-638">15</span><span class="sxs-lookup"><span data-stu-id="3345f-638">15</span></span></td>
<td><span data-ttu-id="3345f-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="3345f-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3345f-640">45.20</span><span class="sxs-lookup"><span data-stu-id="3345f-640">45.20</span></span></td>
<td><span data-ttu-id="3345f-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-642">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-643">Product 1</span></span></td>
<td><span data-ttu-id="3345f-644">80</span><span class="sxs-lookup"><span data-stu-id="3345f-644">80</span></span></td>
<td><span data-ttu-id="3345f-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="3345f-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3345f-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3345f-646">2,507.09</span></span></td>
<td><span data-ttu-id="3345f-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-648">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-649">Product 2</span></span></td>
<td><span data-ttu-id="3345f-650">15</span><span class="sxs-lookup"><span data-stu-id="3345f-650">15</span></span></td>
<td><span data-ttu-id="3345f-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="3345f-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3345f-652">470.08</span><span class="sxs-lookup"><span data-stu-id="3345f-652">470.08</span></span></td>
<td><span data-ttu-id="3345f-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3345f-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="3345f-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-655">Journal</span></span></th>
<th><span data-ttu-id="3345f-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="3345f-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3345f-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3345f-658">Versija</span><span class="sxs-lookup"><span data-stu-id="3345f-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-659">00004</span><span class="sxs-lookup"><span data-stu-id="3345f-659">00004</span></span></td>
<td><span data-ttu-id="3345f-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="3345f-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="3345f-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="3345f-661">Fiscal</span></span></td>
<td><span data-ttu-id="3345f-662">2017</span><span class="sxs-lookup"><span data-stu-id="3345f-662">2017</span></span></td>
<td><span data-ttu-id="3345f-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-663">Period 1</span></span></td>
<td><span data-ttu-id="3345f-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3345f-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="3345f-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="3345f-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3345f-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-668">Cost element</span></span></th>
<th><span data-ttu-id="3345f-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-669">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-670">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-672">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-672">CC001</span></span></td>
<td><span data-ttu-id="3345f-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-673">HR</span></span></td>
<td><span data-ttu-id="3345f-674">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-674">10001</span></span></td>
<td><span data-ttu-id="3345f-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-675">Electricity</span></span></td>
<td><span data-ttu-id="3345f-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-676">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-677">500,00</span><span class="sxs-lookup"><span data-stu-id="3345f-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-679">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-679">CC001</span></span></td>
<td><span data-ttu-id="3345f-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-680">HR</span></span></td>
<td><span data-ttu-id="3345f-681">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-681">10001</span></span></td>
<td><span data-ttu-id="3345f-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-682">Electricity</span></span></td>
<td><span data-ttu-id="3345f-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-683">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="3345f-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-686">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-686">CC002</span></span></td>
<td><span data-ttu-id="3345f-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-687">Finance</span></span></td>
<td><span data-ttu-id="3345f-688">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-688">10001</span></span></td>
<td><span data-ttu-id="3345f-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-689">Electricity</span></span></td>
<td><span data-ttu-id="3345f-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-690">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-691">675.00</span><span class="sxs-lookup"><span data-stu-id="3345f-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-693">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-693">CC002</span></span></td>
<td><span data-ttu-id="3345f-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-694">Finance</span></span></td>
<td><span data-ttu-id="3345f-695">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-695">10001</span></span></td>
<td><span data-ttu-id="3345f-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-696">Electricity</span></span></td>
<td><span data-ttu-id="3345f-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-697">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="3345f-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-700">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-700">CC003</span></span></td>
<td><span data-ttu-id="3345f-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-701">Assembly</span></span></td>
<td><span data-ttu-id="3345f-702">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-702">10001</span></span></td>
<td><span data-ttu-id="3345f-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-703">Electricity</span></span></td>
<td><span data-ttu-id="3345f-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-704">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-705">713.75</span><span class="sxs-lookup"><span data-stu-id="3345f-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-707">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-707">CC003</span></span></td>
<td><span data-ttu-id="3345f-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-708">Assembly</span></span></td>
<td><span data-ttu-id="3345f-709">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-709">10001</span></span></td>
<td><span data-ttu-id="3345f-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-710">Electricity</span></span></td>
<td><span data-ttu-id="3345f-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-711">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="3345f-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-714">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-714">CC003</span></span></td>
<td><span data-ttu-id="3345f-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-715">Packaging</span></span></td>
<td><span data-ttu-id="3345f-716">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-716">10001</span></span></td>
<td><span data-ttu-id="3345f-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-717">Electricity</span></span></td>
<td><span data-ttu-id="3345f-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-718">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-719">286.25</span><span class="sxs-lookup"><span data-stu-id="3345f-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-721">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-721">CC003</span></span></td>
<td><span data-ttu-id="3345f-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-722">Packaging</span></span></td>
<td><span data-ttu-id="3345f-723">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-723">10001</span></span></td>
<td><span data-ttu-id="3345f-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-724">Electricity</span></span></td>
<td><span data-ttu-id="3345f-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-725">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="3345f-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-728">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-729">Product 1</span></span></td>
<td><span data-ttu-id="3345f-730">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-730">10001</span></span></td>
<td><span data-ttu-id="3345f-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-731">Electricity</span></span></td>
<td><span data-ttu-id="3345f-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-732">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-733">776.36</span><span class="sxs-lookup"><span data-stu-id="3345f-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-735">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-736">Product 1</span></span></td>
<td><span data-ttu-id="3345f-737">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-737">10001</span></span></td>
<td><span data-ttu-id="3345f-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-738">Electricity</span></span></td>
<td><span data-ttu-id="3345f-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-739">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3345f-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-742">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-743">Product 1</span></span></td>
<td><span data-ttu-id="3345f-744">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-744">10001</span></span></td>
<td><span data-ttu-id="3345f-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-745">Electricity</span></span></td>
<td><span data-ttu-id="3345f-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-746">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-747">223.64</span><span class="sxs-lookup"><span data-stu-id="3345f-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="3345f-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-749">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-750">Product 1</span></span></td>
<td><span data-ttu-id="3345f-751">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-751">10001</span></span></td>
<td><span data-ttu-id="3345f-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-752">Electricity</span></span></td>
<td><span data-ttu-id="3345f-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-753">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3345f-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3345f-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="3345f-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3345f-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3345f-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-757">Cost element</span></span></th>
<th><span data-ttu-id="3345f-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="3345f-758">Cost behavior</span></span></th>
<th><span data-ttu-id="3345f-759">Suma</span><span class="sxs-lookup"><span data-stu-id="3345f-759">Amount</span></span></th>
<th><span data-ttu-id="3345f-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="3345f-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3345f-761">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-761">CC001</span></span></td>
<td><span data-ttu-id="3345f-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-762">HR</span></span></td>
<td><span data-ttu-id="3345f-763">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-763">10001</span></span></td>
<td><span data-ttu-id="3345f-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-764">Electricity</span></span></td>
<td><span data-ttu-id="3345f-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-765">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="3345f-766">-500.00</span></span></td>
<td><span data-ttu-id="3345f-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-768">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-768">CC002</span></span></td>
<td><span data-ttu-id="3345f-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-769">Finance</span></span></td>
<td><span data-ttu-id="3345f-770">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-770">10001</span></span></td>
<td><span data-ttu-id="3345f-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-771">Electricity</span></span></td>
<td><span data-ttu-id="3345f-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-772">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-773">175.00</span><span class="sxs-lookup"><span data-stu-id="3345f-773">175.00</span></span></td>
<td><span data-ttu-id="3345f-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-775">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-775">CC003</span></span></td>
<td><span data-ttu-id="3345f-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-776">Assembly</span></span></td>
<td><span data-ttu-id="3345f-777">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-777">10001</span></span></td>
<td><span data-ttu-id="3345f-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-778">Electricity</span></span></td>
<td><span data-ttu-id="3345f-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-779">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-780">275.00</span><span class="sxs-lookup"><span data-stu-id="3345f-780">275.00</span></span></td>
<td><span data-ttu-id="3345f-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-782">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-782">CC004</span></span></td>
<td><span data-ttu-id="3345f-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-783">Packaging</span></span></td>
<td><span data-ttu-id="3345f-784">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-784">10001</span></span></td>
<td><span data-ttu-id="3345f-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-785">Electricity</span></span></td>
<td><span data-ttu-id="3345f-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-786">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-787">50,00</span><span class="sxs-lookup"><span data-stu-id="3345f-787">50,00</span></span></td>
<td><span data-ttu-id="3345f-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-789">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-789">CC001</span></span></td>
<td><span data-ttu-id="3345f-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="3345f-790">HR</span></span></td>
<td><span data-ttu-id="3345f-791">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-791">10001</span></span></td>
<td><span data-ttu-id="3345f-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-792">Electricity</span></span></td>
<td><span data-ttu-id="3345f-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-793">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="3345f-794">-1,245.71</span></span></td>
<td><span data-ttu-id="3345f-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-796">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-796">CC002</span></span></td>
<td><span data-ttu-id="3345f-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-797">Finance</span></span></td>
<td><span data-ttu-id="3345f-798">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-798">10001</span></span></td>
<td><span data-ttu-id="3345f-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-799">Electricity</span></span></td>
<td><span data-ttu-id="3345f-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-800">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-801">436.00</span><span class="sxs-lookup"><span data-stu-id="3345f-801">436.00</span></span></td>
<td><span data-ttu-id="3345f-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-803">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-803">CC003</span></span></td>
<td><span data-ttu-id="3345f-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-804">Assembly</span></span></td>
<td><span data-ttu-id="3345f-805">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-805">10001</span></span></td>
<td><span data-ttu-id="3345f-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-806">Electricity</span></span></td>
<td><span data-ttu-id="3345f-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-807">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-808">685.14</span><span class="sxs-lookup"><span data-stu-id="3345f-808">685.14</span></span></td>
<td><span data-ttu-id="3345f-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-810">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-810">CC004</span></span></td>
<td><span data-ttu-id="3345f-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-811">Packaging</span></span></td>
<td><span data-ttu-id="3345f-812">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-812">10001</span></span></td>
<td><span data-ttu-id="3345f-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-813">Electricity</span></span></td>
<td><span data-ttu-id="3345f-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-814">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-815">124.57</span><span class="sxs-lookup"><span data-stu-id="3345f-815">124.57</span></span></td>
<td><span data-ttu-id="3345f-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-817">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-817">CC002</span></span></td>
<td><span data-ttu-id="3345f-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-818">Finance</span></span></td>
<td><span data-ttu-id="3345f-819">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-819">10001</span></span></td>
<td><span data-ttu-id="3345f-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-820">Electricity</span></span></td>
<td><span data-ttu-id="3345f-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-821">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="3345f-822">-675.00</span></span></td>
<td><span data-ttu-id="3345f-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-824">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-824">CC003</span></span></td>
<td><span data-ttu-id="3345f-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-825">Assembly</span></span></td>
<td><span data-ttu-id="3345f-826">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-826">10001</span></span></td>
<td><span data-ttu-id="3345f-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-827">Electricity</span></span></td>
<td><span data-ttu-id="3345f-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-828">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-829">438.75</span><span class="sxs-lookup"><span data-stu-id="3345f-829">438.75</span></span></td>
<td><span data-ttu-id="3345f-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-831">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-831">CC004</span></span></td>
<td><span data-ttu-id="3345f-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-832">Packaging</span></span></td>
<td><span data-ttu-id="3345f-833">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-833">10001</span></span></td>
<td><span data-ttu-id="3345f-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-834">Electricity</span></span></td>
<td><span data-ttu-id="3345f-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-835">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-836">236.25</span><span class="sxs-lookup"><span data-stu-id="3345f-836">236.25</span></span></td>
<td><span data-ttu-id="3345f-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-838">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-838">CC002</span></span></td>
<td><span data-ttu-id="3345f-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="3345f-839">Finance</span></span></td>
<td><span data-ttu-id="3345f-840">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-840">10001</span></span></td>
<td><span data-ttu-id="3345f-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-841">Electricity</span></span></td>
<td><span data-ttu-id="3345f-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-842">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="3345f-843">-8,150.29</span></span></td>
<td><span data-ttu-id="3345f-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-845">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-845">CC003</span></span></td>
<td><span data-ttu-id="3345f-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-846">Assembly</span></span></td>
<td><span data-ttu-id="3345f-847">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-847">10001</span></span></td>
<td><span data-ttu-id="3345f-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-848">Electricity</span></span></td>
<td><span data-ttu-id="3345f-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-849">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3345f-850">5,297.69</span></span></td>
<td><span data-ttu-id="3345f-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-852">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-852">CC004</span></span></td>
<td><span data-ttu-id="3345f-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="3345f-853">Packaging</span></span></td>
<td><span data-ttu-id="3345f-854">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-854">10001</span></span></td>
<td><span data-ttu-id="3345f-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-855">Electricity</span></span></td>
<td><span data-ttu-id="3345f-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-856">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3345f-857">2,852.60</span></span></td>
<td><span data-ttu-id="3345f-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-859">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-859">CC003</span></span></td>
<td><span data-ttu-id="3345f-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-860">Assembly</span></span></td>
<td><span data-ttu-id="3345f-861">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-861">10001</span></span></td>
<td><span data-ttu-id="3345f-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-862">Electricity</span></span></td>
<td><span data-ttu-id="3345f-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-863">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="3345f-864">-713.75</span></span></td>
<td><span data-ttu-id="3345f-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-866">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-867">Product 1</span></span></td>
<td><span data-ttu-id="3345f-868">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-868">10001</span></span></td>
<td><span data-ttu-id="3345f-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-869">Electricity</span></span></td>
<td><span data-ttu-id="3345f-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-870">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-871">535.31</span><span class="sxs-lookup"><span data-stu-id="3345f-871">535.31</span></span></td>
<td><span data-ttu-id="3345f-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-873">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-874">Product 2</span></span></td>
<td><span data-ttu-id="3345f-875">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-875">10001</span></span></td>
<td><span data-ttu-id="3345f-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-876">Electricity</span></span></td>
<td><span data-ttu-id="3345f-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-877">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-878">178.44</span><span class="sxs-lookup"><span data-stu-id="3345f-878">178.44</span></span></td>
<td><span data-ttu-id="3345f-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-880">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-880">CC003</span></span></td>
<td><span data-ttu-id="3345f-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-881">Assembly</span></span></td>
<td><span data-ttu-id="3345f-882">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-882">10001</span></span></td>
<td><span data-ttu-id="3345f-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-883">Electricity</span></span></td>
<td><span data-ttu-id="3345f-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-884">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="3345f-885">-5,982.83</span></span></td>
<td><span data-ttu-id="3345f-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-887">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-888">Product 1</span></span></td>
<td><span data-ttu-id="3345f-889">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-889">10001</span></span></td>
<td><span data-ttu-id="3345f-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-890">Electricity</span></span></td>
<td><span data-ttu-id="3345f-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-891">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3345f-892">4,487.12</span></span></td>
<td><span data-ttu-id="3345f-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-894">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-895">Product 2</span></span></td>
<td><span data-ttu-id="3345f-896">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-896">10001</span></span></td>
<td><span data-ttu-id="3345f-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-897">Electricity</span></span></td>
<td><span data-ttu-id="3345f-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-898">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3345f-899">1,495.71</span></span></td>
<td><span data-ttu-id="3345f-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-901">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-901">CC003</span></span></td>
<td><span data-ttu-id="3345f-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-902">Assembly</span></span></td>
<td><span data-ttu-id="3345f-903">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-903">10001</span></span></td>
<td><span data-ttu-id="3345f-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-904">Electricity</span></span></td>
<td><span data-ttu-id="3345f-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-905">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="3345f-906">-286.25</span></span></td>
<td><span data-ttu-id="3345f-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-908">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-909">Product 1</span></span></td>
<td><span data-ttu-id="3345f-910">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-910">10001</span></span></td>
<td><span data-ttu-id="3345f-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-911">Electricity</span></span></td>
<td><span data-ttu-id="3345f-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-912">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-913">241.05</span><span class="sxs-lookup"><span data-stu-id="3345f-913">241.05</span></span></td>
<td><span data-ttu-id="3345f-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-915">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-916">Product 2</span></span></td>
<td><span data-ttu-id="3345f-917">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-917">10001</span></span></td>
<td><span data-ttu-id="3345f-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-918">Electricity</span></span></td>
<td><span data-ttu-id="3345f-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-919">Fixed cost</span></span></td>
<td><span data-ttu-id="3345f-920">45.20</span><span class="sxs-lookup"><span data-stu-id="3345f-920">45.20</span></span></td>
<td><span data-ttu-id="3345f-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-922">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-922">CC003</span></span></td>
<td><span data-ttu-id="3345f-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="3345f-923">Assembly</span></span></td>
<td><span data-ttu-id="3345f-924">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-924">10001</span></span></td>
<td><span data-ttu-id="3345f-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-925">Electricity</span></span></td>
<td><span data-ttu-id="3345f-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-926">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="3345f-927">-2,977.17</span></span></td>
<td><span data-ttu-id="3345f-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-929">Prod 1</span></span></td>
<td><span data-ttu-id="3345f-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-930">Product 1</span></span></td>
<td><span data-ttu-id="3345f-931">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-931">10001</span></span></td>
<td><span data-ttu-id="3345f-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-932">Electricity</span></span></td>
<td><span data-ttu-id="3345f-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-933">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3345f-934">2,507.09</span></span></td>
<td><span data-ttu-id="3345f-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3345f-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-936">Prod 2</span></span></td>
<td><span data-ttu-id="3345f-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="3345f-937">Product 2</span></span></td>
<td><span data-ttu-id="3345f-938">10001</span><span class="sxs-lookup"><span data-stu-id="3345f-938">10001</span></span></td>
<td><span data-ttu-id="3345f-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-939">Electricity</span></span></td>
<td><span data-ttu-id="3345f-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-940">Variable cost</span></span></td>
<td><span data-ttu-id="3345f-941">470.08</span><span class="sxs-lookup"><span data-stu-id="3345f-941">470.08</span></span></td>
<td><span data-ttu-id="3345f-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="3345f-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="3345f-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="3345f-943">Conclusion</span></span>
<span data-ttu-id="3345f-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="3345f-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="3345f-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="3345f-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="3345f-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="3345f-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="3345f-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="3345f-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="3345f-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="3345f-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="3345f-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="3345f-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="3345f-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="3345f-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3345f-951">CC099</span><span class="sxs-lookup"><span data-stu-id="3345f-951">CC099</span></span></th>
<th><span data-ttu-id="3345f-952">CC001</span><span class="sxs-lookup"><span data-stu-id="3345f-952">CC001</span></span></th>
<th><span data-ttu-id="3345f-953">CC002</span><span class="sxs-lookup"><span data-stu-id="3345f-953">CC002</span></span></th>
<th><span data-ttu-id="3345f-954">CC003</span><span class="sxs-lookup"><span data-stu-id="3345f-954">CC003</span></span></th>
<th><span data-ttu-id="3345f-955">CC004</span><span class="sxs-lookup"><span data-stu-id="3345f-955">CC004</span></span></th>
<th><span data-ttu-id="3345f-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-956">Proj 1</span></span></th>
<th><span data-ttu-id="3345f-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="3345f-957">Proj 2</span></span></th>
<th><span data-ttu-id="3345f-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-958">Prod 1</span></span></th>
<th><span data-ttu-id="3345f-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="3345f-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="3345f-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="3345f-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3345f-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="3345f-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="3345f-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-971">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="3345f-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-973">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-974">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-975">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-976">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-977">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3345f-978">776.36</span><span class="sxs-lookup"><span data-stu-id="3345f-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-979">223.64</span><span class="sxs-lookup"><span data-stu-id="3345f-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3345f-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3345f-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-982">000</span><span class="sxs-lookup"><span data-stu-id="3345f-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-983">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-984">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-985">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-986">0,00</span><span class="sxs-lookup"><span data-stu-id="3345f-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-987">30,00</span><span class="sxs-lookup"><span data-stu-id="3345f-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-988">10,00</span><span class="sxs-lookup"><span data-stu-id="3345f-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3345f-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3345f-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3345f-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="3345f-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3345f-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="3345f-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="3345f-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="3345f-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="3345f-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="3345f-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="3345f-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="3345f-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="3345f-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="3345f-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



