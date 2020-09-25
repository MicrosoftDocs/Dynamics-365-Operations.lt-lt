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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759477"
---
# <a name="overhead-calculation"></a><span data-ttu-id="76438-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="76438-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76438-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="76438-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="76438-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="76438-105">Term definition</span></span>
---------------

<span data-ttu-id="76438-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="76438-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="76438-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="76438-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="76438-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="76438-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="76438-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="76438-109">Rent</span></span>
-   <span data-ttu-id="76438-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-110">Electricity</span></span>
-   <span data-ttu-id="76438-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="76438-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="76438-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="76438-112">Overhead calculation overview</span></span>
<span data-ttu-id="76438-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="76438-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="76438-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="76438-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="76438-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="76438-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="76438-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="76438-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="76438-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="76438-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="76438-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="76438-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="76438-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="76438-119">Version type</span></span>
-   <span data-ttu-id="76438-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="76438-120">Date and time</span></span>
-   <span data-ttu-id="76438-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="76438-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="76438-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="76438-122">Fiscal year</span></span>
-   <span data-ttu-id="76438-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-123">Fiscal period</span></span>

<span data-ttu-id="76438-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="76438-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="76438-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="76438-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="76438-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="76438-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="76438-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="76438-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="76438-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="76438-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="76438-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="76438-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="76438-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="76438-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="76438-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="76438-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="76438-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="76438-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="76438-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="76438-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="76438-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="76438-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="76438-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="76438-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="76438-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="76438-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="76438-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="76438-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76438-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="76438-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="76438-140">Main account</span></span></th>
<th><span data-ttu-id="76438-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="76438-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="76438-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="76438-143">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-143">CC099</span></span></td>
<td><span data-ttu-id="76438-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-144">Default cost center</span></span></td>
<td><span data-ttu-id="76438-145">10001</span><span class="sxs-lookup"><span data-stu-id="76438-145">10001</span></span></td>
<td><span data-ttu-id="76438-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-146">Electricity</span></span></td>
<td><span data-ttu-id="76438-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76438-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="76438-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="76438-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="76438-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="76438-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="76438-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="76438-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="76438-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="76438-151">Define the cost behavior rule</span></span>

<span data-ttu-id="76438-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="76438-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="76438-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="76438-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="76438-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="76438-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="76438-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="76438-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="76438-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="76438-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="76438-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="76438-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="76438-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="76438-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-160">Journal</span></span></th>
<th><span data-ttu-id="76438-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="76438-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76438-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76438-163">Versija</span><span class="sxs-lookup"><span data-stu-id="76438-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-164">00001</span><span class="sxs-lookup"><span data-stu-id="76438-164">00001</span></span></td>
<td><span data-ttu-id="76438-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="76438-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="76438-166">Fiscal</span></span></td>
<td><span data-ttu-id="76438-167">2017</span><span class="sxs-lookup"><span data-stu-id="76438-167">2017</span></span></td>
<td><span data-ttu-id="76438-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-168">Period 1</span></span></td>
<td><span data-ttu-id="76438-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76438-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="76438-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76438-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-173">Cost element</span></span></th>
<th><span data-ttu-id="76438-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-174">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-175">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="76438-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="76438-177">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-177">CC099</span></span></td>
<td><span data-ttu-id="76438-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-178">Default cost center</span></span></td>
<td><span data-ttu-id="76438-179">10001</span><span class="sxs-lookup"><span data-stu-id="76438-179">10001</span></span></td>
<td><span data-ttu-id="76438-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-180">Electricity</span></span></td>
<td><span data-ttu-id="76438-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="76438-181">Unclassified</span></span></td>
<td><span data-ttu-id="76438-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76438-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76438-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="76438-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-185">Cost element</span></span></th>
<th><span data-ttu-id="76438-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-186">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-187">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-187">Amount</span></span></th>
<th><span data-ttu-id="76438-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-189">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-189">CC099</span></span></td>
<td><span data-ttu-id="76438-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-190">Default cost center</span></span></td>
<td><span data-ttu-id="76438-191">10001</span><span class="sxs-lookup"><span data-stu-id="76438-191">10001</span></span></td>
<td><span data-ttu-id="76438-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-192">Electricity</span></span></td>
<td><span data-ttu-id="76438-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="76438-193">Unclassified</span></span></td>
<td><span data-ttu-id="76438-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="76438-194">10,000.00</span></span></td>
<td><span data-ttu-id="76438-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="76438-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-196">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-196">CC099</span></span></td>
<td><span data-ttu-id="76438-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-197">Default cost center</span></span></td>
<td><span data-ttu-id="76438-198">10001</span><span class="sxs-lookup"><span data-stu-id="76438-198">10001</span></span></td>
<td><span data-ttu-id="76438-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-199">Electricity</span></span></td>
<td><span data-ttu-id="76438-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="76438-200">Unclassified</span></span></td>
<td><span data-ttu-id="76438-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="76438-201">-10,000.00</span></span></td>
<td><span data-ttu-id="76438-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-203">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-203">CC099</span></span></td>
<td><span data-ttu-id="76438-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-204">Default cost center</span></span></td>
<td><span data-ttu-id="76438-205">10001</span><span class="sxs-lookup"><span data-stu-id="76438-205">10001</span></span></td>
<td><span data-ttu-id="76438-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-206">Electricity</span></span></td>
<td><span data-ttu-id="76438-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-207">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="76438-208">1,000.00</span></span></td>
<td><span data-ttu-id="76438-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-210">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-210">CC099</span></span></td>
<td><span data-ttu-id="76438-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-211">Default cost center</span></span></td>
<td><span data-ttu-id="76438-212">10001</span><span class="sxs-lookup"><span data-stu-id="76438-212">10001</span></span></td>
<td><span data-ttu-id="76438-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-213">Electricity</span></span></td>
<td><span data-ttu-id="76438-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-214">Variable cost</span></span></td>
<td><span data-ttu-id="76438-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="76438-215">9,000.00</span></span></td>
<td><span data-ttu-id="76438-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="76438-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="76438-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="76438-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="76438-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="76438-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="76438-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="76438-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="76438-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="76438-221">Define the cost distribution rule</span></span>

<span data-ttu-id="76438-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="76438-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="76438-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="76438-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="76438-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="76438-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="76438-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="76438-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="76438-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="76438-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="76438-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="76438-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-228">Cost object</span></span></th>
<th><span data-ttu-id="76438-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="76438-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-230">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-230">CC001</span></span></td>
<td><span data-ttu-id="76438-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-231">HR</span></span></td>
<td><span data-ttu-id="76438-232">1000</span><span class="sxs-lookup"><span data-stu-id="76438-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-233">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-233">CC002</span></span></td>
<td><span data-ttu-id="76438-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-234">Finance</span></span></td>
<td><span data-ttu-id="76438-235">6,000</span><span class="sxs-lookup"><span data-stu-id="76438-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-236">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-236">CC003</span></span></td>
<td><span data-ttu-id="76438-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-237">Assembly</span></span></td>
<td><span data-ttu-id="76438-238">0</span><span class="sxs-lookup"><span data-stu-id="76438-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-240">Cost object</span></span></th>
<th><span data-ttu-id="76438-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-241">Magnitude</span></span></th>
<th><span data-ttu-id="76438-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-242">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-243">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-244">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-244">CC001</span></span></td>
<td><span data-ttu-id="76438-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-245">HR</span></span></td>
<td><span data-ttu-id="76438-246">1000</span><span class="sxs-lookup"><span data-stu-id="76438-246">1,000</span></span></td>
<td><span data-ttu-id="76438-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76438-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="76438-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-249">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-249">CC002</span></span></td>
<td><span data-ttu-id="76438-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-250">Finance</span></span></td>
<td><span data-ttu-id="76438-251">6,000</span><span class="sxs-lookup"><span data-stu-id="76438-251">6,000</span></span></td>
<td><span data-ttu-id="76438-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76438-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="76438-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-254">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-254">CC003</span></span></td>
<td><span data-ttu-id="76438-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-255">Assembly</span></span></td>
<td><span data-ttu-id="76438-256">0</span><span class="sxs-lookup"><span data-stu-id="76438-256">0</span></span></td>
<td><span data-ttu-id="76438-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="76438-258">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="76438-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="76438-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-261">Cost object</span></span></th>
<th><span data-ttu-id="76438-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="76438-262">Formula</span></span></th>
<th><span data-ttu-id="76438-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-263">Magnitude</span></span></th>
<th><span data-ttu-id="76438-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-264">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-265">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-266">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-266">CC001</span></span></td>
<td><span data-ttu-id="76438-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-267">HR</span></span></td>
<td><span data-ttu-id="76438-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76438-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76438-269">1</span><span class="sxs-lookup"><span data-stu-id="76438-269">1</span></span></td>
<td><span data-ttu-id="76438-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76438-271">500,00</span><span class="sxs-lookup"><span data-stu-id="76438-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-272">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-272">CC002</span></span></td>
<td><span data-ttu-id="76438-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-273">Finance</span></span></td>
<td><span data-ttu-id="76438-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76438-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76438-275">1</span><span class="sxs-lookup"><span data-stu-id="76438-275">1</span></span></td>
<td><span data-ttu-id="76438-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76438-277">500,00</span><span class="sxs-lookup"><span data-stu-id="76438-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-278">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-278">CC003</span></span></td>
<td><span data-ttu-id="76438-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-279">Assembly</span></span></td>
<td><span data-ttu-id="76438-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="76438-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="76438-281">0</span><span class="sxs-lookup"><span data-stu-id="76438-281">0</span></span></td>
<td><span data-ttu-id="76438-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="76438-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="76438-283">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="76438-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-285">Journal</span></span></th>
<th><span data-ttu-id="76438-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="76438-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76438-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76438-288">Versija</span><span class="sxs-lookup"><span data-stu-id="76438-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-289">00002</span><span class="sxs-lookup"><span data-stu-id="76438-289">00002</span></span></td>
<td><span data-ttu-id="76438-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="76438-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="76438-291">Fiscal</span></span></td>
<td><span data-ttu-id="76438-292">2017</span><span class="sxs-lookup"><span data-stu-id="76438-292">2017</span></span></td>
<td><span data-ttu-id="76438-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-293">Period 1</span></span></td>
<td><span data-ttu-id="76438-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76438-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="76438-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76438-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-298">Cost element</span></span></th>
<th><span data-ttu-id="76438-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-299">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-300">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-302">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-302">CC099</span></span></td>
<td><span data-ttu-id="76438-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-303">Default cost center</span></span></td>
<td><span data-ttu-id="76438-304">10001</span><span class="sxs-lookup"><span data-stu-id="76438-304">10001</span></span></td>
<td><span data-ttu-id="76438-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-305">Electricity</span></span></td>
<td><span data-ttu-id="76438-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-306">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="76438-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-309">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-309">CC099</span></span></td>
<td><span data-ttu-id="76438-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-310">Default cost center</span></span></td>
<td><span data-ttu-id="76438-311">10001</span><span class="sxs-lookup"><span data-stu-id="76438-311">10001</span></span></td>
<td><span data-ttu-id="76438-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-312">Electricity</span></span></td>
<td><span data-ttu-id="76438-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-313">Variable cost</span></span></td>
<td><span data-ttu-id="76438-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="76438-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76438-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="76438-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-317">Cost element</span></span></th>
<th><span data-ttu-id="76438-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-318">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-319">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-319">Amount</span></span></th>
<th><span data-ttu-id="76438-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-321">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-321">CC099</span></span></td>
<td><span data-ttu-id="76438-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-322">Default cost center</span></span></td>
<td><span data-ttu-id="76438-323">10001</span><span class="sxs-lookup"><span data-stu-id="76438-323">10001</span></span></td>
<td><span data-ttu-id="76438-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-324">Electricity</span></span></td>
<td><span data-ttu-id="76438-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-325">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="76438-326">-1,000.00</span></span></td>
<td><span data-ttu-id="76438-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-328">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-328">CC001</span></span></td>
<td><span data-ttu-id="76438-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-329">HR</span></span></td>
<td><span data-ttu-id="76438-330">10001</span><span class="sxs-lookup"><span data-stu-id="76438-330">10001</span></span></td>
<td><span data-ttu-id="76438-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-331">Electricity</span></span></td>
<td><span data-ttu-id="76438-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-332">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-333">500,00</span><span class="sxs-lookup"><span data-stu-id="76438-333">500.00</span></span></td>
<td><span data-ttu-id="76438-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-335">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-335">CC002</span></span></td>
<td><span data-ttu-id="76438-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-336">Finance</span></span></td>
<td><span data-ttu-id="76438-337">10001</span><span class="sxs-lookup"><span data-stu-id="76438-337">10001</span></span></td>
<td><span data-ttu-id="76438-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-338">Electricity</span></span></td>
<td><span data-ttu-id="76438-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-339">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-340">500,00</span><span class="sxs-lookup"><span data-stu-id="76438-340">500.00</span></span></td>
<td><span data-ttu-id="76438-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-342">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-342">CC099</span></span></td>
<td><span data-ttu-id="76438-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="76438-343">Default cost center</span></span></td>
<td><span data-ttu-id="76438-344">10001</span><span class="sxs-lookup"><span data-stu-id="76438-344">10001</span></span></td>
<td><span data-ttu-id="76438-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-345">Electricity</span></span></td>
<td><span data-ttu-id="76438-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-346">Variable cost</span></span></td>
<td><span data-ttu-id="76438-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="76438-347">-9,000.00</span></span></td>
<td><span data-ttu-id="76438-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-349">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-349">CC001</span></span></td>
<td><span data-ttu-id="76438-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-350">HR</span></span></td>
<td><span data-ttu-id="76438-351">10001</span><span class="sxs-lookup"><span data-stu-id="76438-351">10001</span></span></td>
<td><span data-ttu-id="76438-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-352">Electricity</span></span></td>
<td><span data-ttu-id="76438-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-353">Variable cost</span></span></td>
<td><span data-ttu-id="76438-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="76438-354">1,285.71</span></span></td>
<td><span data-ttu-id="76438-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-356">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-356">CC002</span></span></td>
<td><span data-ttu-id="76438-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-357">Finance</span></span></td>
<td><span data-ttu-id="76438-358">10001</span><span class="sxs-lookup"><span data-stu-id="76438-358">10001</span></span></td>
<td><span data-ttu-id="76438-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-359">Electricity</span></span></td>
<td><span data-ttu-id="76438-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-360">Variable cost</span></span></td>
<td><span data-ttu-id="76438-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="76438-361">7,714.29</span></span></td>
<td><span data-ttu-id="76438-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="76438-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="76438-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="76438-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="76438-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="76438-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="76438-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="76438-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="76438-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="76438-367">Define the overhead rate</span></span>

<span data-ttu-id="76438-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="76438-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="76438-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76438-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-370">Cost object</span></span></th>
<th><span data-ttu-id="76438-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="76438-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-372">Proj 1</span></span></td>
<td><span data-ttu-id="76438-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-373">Project 1</span></span></td>
<td><span data-ttu-id="76438-374">3</span><span class="sxs-lookup"><span data-stu-id="76438-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-375">Proj 2</span></span></td>
<td><span data-ttu-id="76438-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-376">Project 2</span></span></td>
<td><span data-ttu-id="76438-377">1</span><span class="sxs-lookup"><span data-stu-id="76438-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="76438-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-379">Cost object</span></span></th>
<th><span data-ttu-id="76438-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-380">Cost element</span></span></th>
<th><span data-ttu-id="76438-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-381">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="76438-382">Units</span></span></th>
<th><span data-ttu-id="76438-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="76438-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-384">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-384">CC001</span></span></td>
<td><span data-ttu-id="76438-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-385">HR</span></span></td>
<td><span data-ttu-id="76438-386">10001</span><span class="sxs-lookup"><span data-stu-id="76438-386">10001</span></span></td>
<td><span data-ttu-id="76438-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-387">Variable cost</span></span></td>
<td><span data-ttu-id="76438-388">1</span><span class="sxs-lookup"><span data-stu-id="76438-388">1</span></span></td>
<td><span data-ttu-id="76438-389">10</span><span class="sxs-lookup"><span data-stu-id="76438-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-391">Cost object</span></span></th>
<th><span data-ttu-id="76438-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-392">Magnitude</span></span></th>
<th><span data-ttu-id="76438-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-393">Cost element</span></span></th>
<th><span data-ttu-id="76438-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-394">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-395">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-396">Proj 1</span></span></td>
<td><span data-ttu-id="76438-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-397">Project 1</span></span></td>
<td><span data-ttu-id="76438-398">3</span><span class="sxs-lookup"><span data-stu-id="76438-398">3</span></span></td>
<td><span data-ttu-id="76438-399">10001</span><span class="sxs-lookup"><span data-stu-id="76438-399">10001</span></span></td>
<td><span data-ttu-id="76438-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="76438-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="76438-401">30,00</span><span class="sxs-lookup"><span data-stu-id="76438-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-402">Proj 2</span></span></td>
<td><span data-ttu-id="76438-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-403">Project 2</span></span></td>
<td><span data-ttu-id="76438-404">1</span><span class="sxs-lookup"><span data-stu-id="76438-404">1</span></span></td>
<td><span data-ttu-id="76438-405">10001</span><span class="sxs-lookup"><span data-stu-id="76438-405">10001</span></span></td>
<td><span data-ttu-id="76438-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="76438-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="76438-407">10,00</span><span class="sxs-lookup"><span data-stu-id="76438-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="76438-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-409">Journal</span></span></th>
<th><span data-ttu-id="76438-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="76438-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76438-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76438-412">Versija</span><span class="sxs-lookup"><span data-stu-id="76438-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-413">00003</span><span class="sxs-lookup"><span data-stu-id="76438-413">00003</span></span></td>
<td><span data-ttu-id="76438-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="76438-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="76438-415">Fiscal</span></span></td>
<td><span data-ttu-id="76438-416">2017</span><span class="sxs-lookup"><span data-stu-id="76438-416">2017</span></span></td>
<td><span data-ttu-id="76438-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-417">Period 1</span></span></td>
<td><span data-ttu-id="76438-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="76438-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="76438-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76438-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-421">Cost object</span></span></th>
<th><span data-ttu-id="76438-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-424">Proj 1</span></span></td>
<td><span data-ttu-id="76438-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="76438-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="76438-426">3,00</span><span class="sxs-lookup"><span data-stu-id="76438-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-428">Proj 2</span></span></td>
<td><span data-ttu-id="76438-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="76438-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="76438-430">1,00</span><span class="sxs-lookup"><span data-stu-id="76438-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76438-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="76438-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-433">Cost element</span></span></th>
<th><span data-ttu-id="76438-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-434">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-435">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-435">Amount</span></span></th>
<th><span data-ttu-id="76438-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="76438-437">CC0001</span></span></td>
<td><span data-ttu-id="76438-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-438">HR</span></span></td>
<td><span data-ttu-id="76438-439">10001</span><span class="sxs-lookup"><span data-stu-id="76438-439">10001</span></span></td>
<td><span data-ttu-id="76438-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-440">Electricity</span></span></td>
<td><span data-ttu-id="76438-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-441">Variable cost</span></span></td>
<td><span data-ttu-id="76438-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="76438-442">-30.00</span></span></td>
<td><span data-ttu-id="76438-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-444">Proj 1</span></span></td>
<td><span data-ttu-id="76438-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="76438-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="76438-446">10001</span><span class="sxs-lookup"><span data-stu-id="76438-446">10001</span></span></td>
<td><span data-ttu-id="76438-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-447">Electricity</span></span></td>
<td><span data-ttu-id="76438-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-448">Variable cost</span></span></td>
<td><span data-ttu-id="76438-449">30,00</span><span class="sxs-lookup"><span data-stu-id="76438-449">30.00</span></span></td>
<td><span data-ttu-id="76438-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-451">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-451">CC001</span></span></td>
<td><span data-ttu-id="76438-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-452">HR</span></span></td>
<td><span data-ttu-id="76438-453">10001</span><span class="sxs-lookup"><span data-stu-id="76438-453">10001</span></span></td>
<td><span data-ttu-id="76438-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-454">Electricity</span></span></td>
<td><span data-ttu-id="76438-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-455">Variable cost</span></span></td>
<td><span data-ttu-id="76438-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="76438-456">-10.00</span></span></td>
<td><span data-ttu-id="76438-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-458">Proj 2</span></span></td>
<td><span data-ttu-id="76438-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="76438-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="76438-460">10001</span><span class="sxs-lookup"><span data-stu-id="76438-460">10001</span></span></td>
<td><span data-ttu-id="76438-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-461">Electricity</span></span></td>
<td><span data-ttu-id="76438-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-462">Variable cost</span></span></td>
<td><span data-ttu-id="76438-463">10,00</span><span class="sxs-lookup"><span data-stu-id="76438-463">10.00</span></span></td>
<td><span data-ttu-id="76438-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="76438-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="76438-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="76438-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="76438-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="76438-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="76438-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="76438-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="76438-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="76438-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="76438-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="76438-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="76438-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="76438-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="76438-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="76438-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="76438-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="76438-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="76438-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="76438-475">Define the cost allocation</span></span>

<span data-ttu-id="76438-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="76438-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="76438-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="76438-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="76438-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76438-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-479">Cost object</span></span></th>
<th><span data-ttu-id="76438-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="76438-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-481">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-481">CC002</span></span></td>
<td><span data-ttu-id="76438-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-482">Finance</span></span></td>
<td><span data-ttu-id="76438-483">35</span><span class="sxs-lookup"><span data-stu-id="76438-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-484">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-484">CC003</span></span></td>
<td><span data-ttu-id="76438-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-485">Assembly</span></span></td>
<td><span data-ttu-id="76438-486">55</span><span class="sxs-lookup"><span data-stu-id="76438-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-487">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-487">CC004</span></span></td>
<td><span data-ttu-id="76438-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-488">Packaging</span></span></td>
<td><span data-ttu-id="76438-489">10</span><span class="sxs-lookup"><span data-stu-id="76438-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="76438-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="76438-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76438-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-492">Cost object</span></span></th>
<th><span data-ttu-id="76438-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="76438-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-494">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-494">CC003</span></span></td>
<td><span data-ttu-id="76438-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-495">Assembly</span></span></td>
<td><span data-ttu-id="76438-496">65</span><span class="sxs-lookup"><span data-stu-id="76438-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-497">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-497">CC004</span></span></td>
<td><span data-ttu-id="76438-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-498">Packaging</span></span></td>
<td><span data-ttu-id="76438-499">35</span><span class="sxs-lookup"><span data-stu-id="76438-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="76438-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="76438-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76438-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-502">Cost object</span></span></th>
<th><span data-ttu-id="76438-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="76438-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-504">Prod 1</span></span></td>
<td><span data-ttu-id="76438-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-505">Product 1</span></span></td>
<td><span data-ttu-id="76438-506">60</span><span class="sxs-lookup"><span data-stu-id="76438-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-507">Prod 2</span></span></td>
<td><span data-ttu-id="76438-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-508">Product 2</span></span></td>
<td><span data-ttu-id="76438-509">20</span><span class="sxs-lookup"><span data-stu-id="76438-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="76438-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="76438-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76438-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-512">Cost object</span></span></th>
<th><span data-ttu-id="76438-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="76438-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-514">Prod 1</span></span></td>
<td><span data-ttu-id="76438-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-515">Product 1</span></span></td>
<td><span data-ttu-id="76438-516">80</span><span class="sxs-lookup"><span data-stu-id="76438-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-517">Prod 2</span></span></td>
<td><span data-ttu-id="76438-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-518">Product 2</span></span></td>
<td><span data-ttu-id="76438-519">15</span><span class="sxs-lookup"><span data-stu-id="76438-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="76438-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="76438-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="76438-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="76438-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="76438-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-523">Cost object</span></span></th>
<th><span data-ttu-id="76438-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-524">Magnitude</span></span></th>
<th><span data-ttu-id="76438-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-525">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-526">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-526">Amount</span></span></th>
<th><span data-ttu-id="76438-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-528">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-528">CC002</span></span></td>
<td><span data-ttu-id="76438-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-529">Finance</span></span></td>
<td><span data-ttu-id="76438-530">35</span><span class="sxs-lookup"><span data-stu-id="76438-530">35</span></span></td>
<td><span data-ttu-id="76438-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76438-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76438-532">175.00</span><span class="sxs-lookup"><span data-stu-id="76438-532">175.00</span></span></td>
<td><span data-ttu-id="76438-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-534">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-534">CC003</span></span></td>
<td><span data-ttu-id="76438-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-535">Assembly</span></span></td>
<td><span data-ttu-id="76438-536">55</span><span class="sxs-lookup"><span data-stu-id="76438-536">55</span></span></td>
<td><span data-ttu-id="76438-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76438-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76438-538">275.00</span><span class="sxs-lookup"><span data-stu-id="76438-538">275.00</span></span></td>
<td><span data-ttu-id="76438-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-540">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-540">CC004</span></span></td>
<td><span data-ttu-id="76438-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-541">Packaging</span></span></td>
<td><span data-ttu-id="76438-542">10</span><span class="sxs-lookup"><span data-stu-id="76438-542">10</span></span></td>
<td><span data-ttu-id="76438-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="76438-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="76438-544">50,00</span><span class="sxs-lookup"><span data-stu-id="76438-544">50.00</span></span></td>
<td><span data-ttu-id="76438-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-546">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-546">CC002</span></span></td>
<td><span data-ttu-id="76438-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-547">Finance</span></span></td>
<td><span data-ttu-id="76438-548">35</span><span class="sxs-lookup"><span data-stu-id="76438-548">35</span></span></td>
<td><span data-ttu-id="76438-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="76438-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76438-550">436.00</span><span class="sxs-lookup"><span data-stu-id="76438-550">436.00</span></span></td>
<td><span data-ttu-id="76438-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-552">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-552">CC003</span></span></td>
<td><span data-ttu-id="76438-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-553">Assembly</span></span></td>
<td><span data-ttu-id="76438-554">55</span><span class="sxs-lookup"><span data-stu-id="76438-554">55</span></span></td>
<td><span data-ttu-id="76438-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="76438-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76438-556">685.14</span><span class="sxs-lookup"><span data-stu-id="76438-556">685.14</span></span></td>
<td><span data-ttu-id="76438-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-558">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-558">CC004</span></span></td>
<td><span data-ttu-id="76438-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-559">Packaging</span></span></td>
<td><span data-ttu-id="76438-560">10</span><span class="sxs-lookup"><span data-stu-id="76438-560">10</span></span></td>
<td><span data-ttu-id="76438-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="76438-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="76438-562">124.57</span><span class="sxs-lookup"><span data-stu-id="76438-562">124.57</span></span></td>
<td><span data-ttu-id="76438-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-565">Cost object</span></span></th>
<th><span data-ttu-id="76438-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-566">Magnitude</span></span></th>
<th><span data-ttu-id="76438-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-567">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-568">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-568">Amount</span></span></th>
<th><span data-ttu-id="76438-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-570">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-570">CC003</span></span></td>
<td><span data-ttu-id="76438-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-571">Assembly</span></span></td>
<td><span data-ttu-id="76438-572">65</span><span class="sxs-lookup"><span data-stu-id="76438-572">65</span></span></td>
<td><span data-ttu-id="76438-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="76438-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="76438-574">438.75</span><span class="sxs-lookup"><span data-stu-id="76438-574">438.75</span></span></td>
<td><span data-ttu-id="76438-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-576">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-576">CC004</span></span></td>
<td><span data-ttu-id="76438-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-577">Packaging</span></span></td>
<td><span data-ttu-id="76438-578">35</span><span class="sxs-lookup"><span data-stu-id="76438-578">35</span></span></td>
<td><span data-ttu-id="76438-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="76438-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="76438-580">236.25</span><span class="sxs-lookup"><span data-stu-id="76438-580">236.25</span></span></td>
<td><span data-ttu-id="76438-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-582">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-582">CC003</span></span></td>
<td><span data-ttu-id="76438-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-583">Assembly</span></span></td>
<td><span data-ttu-id="76438-584">65</span><span class="sxs-lookup"><span data-stu-id="76438-584">65</span></span></td>
<td><span data-ttu-id="76438-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="76438-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="76438-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="76438-586">5,297.69</span></span></td>
<td><span data-ttu-id="76438-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-588">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-588">CC004</span></span></td>
<td><span data-ttu-id="76438-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-589">Packaging</span></span></td>
<td><span data-ttu-id="76438-590">35</span><span class="sxs-lookup"><span data-stu-id="76438-590">35</span></span></td>
<td><span data-ttu-id="76438-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="76438-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="76438-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="76438-592">2,852.60</span></span></td>
<td><span data-ttu-id="76438-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-595">Cost object</span></span></th>
<th><span data-ttu-id="76438-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-596">Magnitude</span></span></th>
<th><span data-ttu-id="76438-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-597">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-598">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-598">Amount</span></span></th>
<th><span data-ttu-id="76438-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-600">Prod 1</span></span></td>
<td><span data-ttu-id="76438-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-601">Product 1</span></span></td>
<td><span data-ttu-id="76438-602">60</span><span class="sxs-lookup"><span data-stu-id="76438-602">60</span></span></td>
<td><span data-ttu-id="76438-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="76438-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="76438-604">535.31</span><span class="sxs-lookup"><span data-stu-id="76438-604">535.31</span></span></td>
<td><span data-ttu-id="76438-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-606">Prod 2</span></span></td>
<td><span data-ttu-id="76438-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-607">Product 2</span></span></td>
<td><span data-ttu-id="76438-608">20</span><span class="sxs-lookup"><span data-stu-id="76438-608">20</span></span></td>
<td><span data-ttu-id="76438-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="76438-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="76438-610">178.44</span><span class="sxs-lookup"><span data-stu-id="76438-610">178.44</span></span></td>
<td><span data-ttu-id="76438-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-612">Prod 1</span></span></td>
<td><span data-ttu-id="76438-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-613">Product 1</span></span></td>
<td><span data-ttu-id="76438-614">60</span><span class="sxs-lookup"><span data-stu-id="76438-614">60</span></span></td>
<td><span data-ttu-id="76438-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="76438-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="76438-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="76438-616">4,487.12</span></span></td>
<td><span data-ttu-id="76438-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-618">Prod 2</span></span></td>
<td><span data-ttu-id="76438-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-619">Product 2</span></span></td>
<td><span data-ttu-id="76438-620">20</span><span class="sxs-lookup"><span data-stu-id="76438-620">20</span></span></td>
<td><span data-ttu-id="76438-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="76438-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="76438-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="76438-622">1,495.71</span></span></td>
<td><span data-ttu-id="76438-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="76438-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76438-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-625">Cost object</span></span></th>
<th><span data-ttu-id="76438-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="76438-626">Magnitude</span></span></th>
<th><span data-ttu-id="76438-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="76438-627">Allocation factor</span></span></th>
<th><span data-ttu-id="76438-628">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-628">Amount</span></span></th>
<th><span data-ttu-id="76438-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-630">Prod 1</span></span></td>
<td><span data-ttu-id="76438-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-631">Product 1</span></span></td>
<td><span data-ttu-id="76438-632">80</span><span class="sxs-lookup"><span data-stu-id="76438-632">80</span></span></td>
<td><span data-ttu-id="76438-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="76438-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="76438-634">241.05</span><span class="sxs-lookup"><span data-stu-id="76438-634">241.05</span></span></td>
<td><span data-ttu-id="76438-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-636">Prod 2</span></span></td>
<td><span data-ttu-id="76438-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-637">Product 2</span></span></td>
<td><span data-ttu-id="76438-638">15</span><span class="sxs-lookup"><span data-stu-id="76438-638">15</span></span></td>
<td><span data-ttu-id="76438-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="76438-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="76438-640">45.20</span><span class="sxs-lookup"><span data-stu-id="76438-640">45.20</span></span></td>
<td><span data-ttu-id="76438-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-642">Prod 1</span></span></td>
<td><span data-ttu-id="76438-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-643">Product 1</span></span></td>
<td><span data-ttu-id="76438-644">80</span><span class="sxs-lookup"><span data-stu-id="76438-644">80</span></span></td>
<td><span data-ttu-id="76438-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="76438-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="76438-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="76438-646">2,507.09</span></span></td>
<td><span data-ttu-id="76438-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-648">Prod 2</span></span></td>
<td><span data-ttu-id="76438-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-649">Product 2</span></span></td>
<td><span data-ttu-id="76438-650">15</span><span class="sxs-lookup"><span data-stu-id="76438-650">15</span></span></td>
<td><span data-ttu-id="76438-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="76438-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="76438-652">470.08</span><span class="sxs-lookup"><span data-stu-id="76438-652">470.08</span></span></td>
<td><span data-ttu-id="76438-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="76438-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="76438-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-655">Journal</span></span></th>
<th><span data-ttu-id="76438-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="76438-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="76438-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="76438-658">Versija</span><span class="sxs-lookup"><span data-stu-id="76438-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-659">00004</span><span class="sxs-lookup"><span data-stu-id="76438-659">00004</span></span></td>
<td><span data-ttu-id="76438-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="76438-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="76438-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="76438-661">Fiscal</span></span></td>
<td><span data-ttu-id="76438-662">2017</span><span class="sxs-lookup"><span data-stu-id="76438-662">2017</span></span></td>
<td><span data-ttu-id="76438-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-663">Period 1</span></span></td>
<td><span data-ttu-id="76438-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="76438-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="76438-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="76438-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="76438-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="76438-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-668">Cost element</span></span></th>
<th><span data-ttu-id="76438-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-669">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-670">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-672">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-672">CC001</span></span></td>
<td><span data-ttu-id="76438-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-673">HR</span></span></td>
<td><span data-ttu-id="76438-674">10001</span><span class="sxs-lookup"><span data-stu-id="76438-674">10001</span></span></td>
<td><span data-ttu-id="76438-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-675">Electricity</span></span></td>
<td><span data-ttu-id="76438-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-676">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-677">500,00</span><span class="sxs-lookup"><span data-stu-id="76438-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-679">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-679">CC001</span></span></td>
<td><span data-ttu-id="76438-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-680">HR</span></span></td>
<td><span data-ttu-id="76438-681">10001</span><span class="sxs-lookup"><span data-stu-id="76438-681">10001</span></span></td>
<td><span data-ttu-id="76438-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-682">Electricity</span></span></td>
<td><span data-ttu-id="76438-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-683">Variable cost</span></span></td>
<td><span data-ttu-id="76438-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="76438-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-686">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-686">CC002</span></span></td>
<td><span data-ttu-id="76438-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-687">Finance</span></span></td>
<td><span data-ttu-id="76438-688">10001</span><span class="sxs-lookup"><span data-stu-id="76438-688">10001</span></span></td>
<td><span data-ttu-id="76438-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-689">Electricity</span></span></td>
<td><span data-ttu-id="76438-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-690">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-691">675.00</span><span class="sxs-lookup"><span data-stu-id="76438-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-693">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-693">CC002</span></span></td>
<td><span data-ttu-id="76438-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-694">Finance</span></span></td>
<td><span data-ttu-id="76438-695">10001</span><span class="sxs-lookup"><span data-stu-id="76438-695">10001</span></span></td>
<td><span data-ttu-id="76438-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-696">Electricity</span></span></td>
<td><span data-ttu-id="76438-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-697">Variable cost</span></span></td>
<td><span data-ttu-id="76438-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="76438-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-700">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-700">CC003</span></span></td>
<td><span data-ttu-id="76438-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-701">Assembly</span></span></td>
<td><span data-ttu-id="76438-702">10001</span><span class="sxs-lookup"><span data-stu-id="76438-702">10001</span></span></td>
<td><span data-ttu-id="76438-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-703">Electricity</span></span></td>
<td><span data-ttu-id="76438-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-704">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-705">713.75</span><span class="sxs-lookup"><span data-stu-id="76438-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-707">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-707">CC003</span></span></td>
<td><span data-ttu-id="76438-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-708">Assembly</span></span></td>
<td><span data-ttu-id="76438-709">10001</span><span class="sxs-lookup"><span data-stu-id="76438-709">10001</span></span></td>
<td><span data-ttu-id="76438-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-710">Electricity</span></span></td>
<td><span data-ttu-id="76438-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-711">Variable cost</span></span></td>
<td><span data-ttu-id="76438-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="76438-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-714">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-714">CC003</span></span></td>
<td><span data-ttu-id="76438-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-715">Packaging</span></span></td>
<td><span data-ttu-id="76438-716">10001</span><span class="sxs-lookup"><span data-stu-id="76438-716">10001</span></span></td>
<td><span data-ttu-id="76438-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-717">Electricity</span></span></td>
<td><span data-ttu-id="76438-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-718">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-719">286.25</span><span class="sxs-lookup"><span data-stu-id="76438-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-721">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-721">CC003</span></span></td>
<td><span data-ttu-id="76438-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-722">Packaging</span></span></td>
<td><span data-ttu-id="76438-723">10001</span><span class="sxs-lookup"><span data-stu-id="76438-723">10001</span></span></td>
<td><span data-ttu-id="76438-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-724">Electricity</span></span></td>
<td><span data-ttu-id="76438-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-725">Variable cost</span></span></td>
<td><span data-ttu-id="76438-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="76438-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-728">Prod 1</span></span></td>
<td><span data-ttu-id="76438-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-729">Product 1</span></span></td>
<td><span data-ttu-id="76438-730">10001</span><span class="sxs-lookup"><span data-stu-id="76438-730">10001</span></span></td>
<td><span data-ttu-id="76438-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-731">Electricity</span></span></td>
<td><span data-ttu-id="76438-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-732">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-733">776.36</span><span class="sxs-lookup"><span data-stu-id="76438-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-735">Prod 1</span></span></td>
<td><span data-ttu-id="76438-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-736">Product 1</span></span></td>
<td><span data-ttu-id="76438-737">10001</span><span class="sxs-lookup"><span data-stu-id="76438-737">10001</span></span></td>
<td><span data-ttu-id="76438-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-738">Electricity</span></span></td>
<td><span data-ttu-id="76438-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-739">Variable cost</span></span></td>
<td><span data-ttu-id="76438-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="76438-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-742">Prod 2</span></span></td>
<td><span data-ttu-id="76438-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-743">Product 1</span></span></td>
<td><span data-ttu-id="76438-744">10001</span><span class="sxs-lookup"><span data-stu-id="76438-744">10001</span></span></td>
<td><span data-ttu-id="76438-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-745">Electricity</span></span></td>
<td><span data-ttu-id="76438-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-746">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-747">223.64</span><span class="sxs-lookup"><span data-stu-id="76438-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="76438-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-749">Prod 2</span></span></td>
<td><span data-ttu-id="76438-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-750">Product 1</span></span></td>
<td><span data-ttu-id="76438-751">10001</span><span class="sxs-lookup"><span data-stu-id="76438-751">10001</span></span></td>
<td><span data-ttu-id="76438-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-752">Electricity</span></span></td>
<td><span data-ttu-id="76438-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-753">Variable cost</span></span></td>
<td><span data-ttu-id="76438-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="76438-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="76438-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="76438-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="76438-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="76438-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-757">Cost element</span></span></th>
<th><span data-ttu-id="76438-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="76438-758">Cost behavior</span></span></th>
<th><span data-ttu-id="76438-759">Suma</span><span class="sxs-lookup"><span data-stu-id="76438-759">Amount</span></span></th>
<th><span data-ttu-id="76438-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="76438-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="76438-761">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-761">CC001</span></span></td>
<td><span data-ttu-id="76438-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-762">HR</span></span></td>
<td><span data-ttu-id="76438-763">10001</span><span class="sxs-lookup"><span data-stu-id="76438-763">10001</span></span></td>
<td><span data-ttu-id="76438-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-764">Electricity</span></span></td>
<td><span data-ttu-id="76438-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-765">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="76438-766">-500.00</span></span></td>
<td><span data-ttu-id="76438-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-768">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-768">CC002</span></span></td>
<td><span data-ttu-id="76438-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-769">Finance</span></span></td>
<td><span data-ttu-id="76438-770">10001</span><span class="sxs-lookup"><span data-stu-id="76438-770">10001</span></span></td>
<td><span data-ttu-id="76438-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-771">Electricity</span></span></td>
<td><span data-ttu-id="76438-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-772">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-773">175.00</span><span class="sxs-lookup"><span data-stu-id="76438-773">175.00</span></span></td>
<td><span data-ttu-id="76438-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-775">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-775">CC003</span></span></td>
<td><span data-ttu-id="76438-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-776">Assembly</span></span></td>
<td><span data-ttu-id="76438-777">10001</span><span class="sxs-lookup"><span data-stu-id="76438-777">10001</span></span></td>
<td><span data-ttu-id="76438-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-778">Electricity</span></span></td>
<td><span data-ttu-id="76438-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-779">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-780">275.00</span><span class="sxs-lookup"><span data-stu-id="76438-780">275.00</span></span></td>
<td><span data-ttu-id="76438-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-782">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-782">CC004</span></span></td>
<td><span data-ttu-id="76438-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-783">Packaging</span></span></td>
<td><span data-ttu-id="76438-784">10001</span><span class="sxs-lookup"><span data-stu-id="76438-784">10001</span></span></td>
<td><span data-ttu-id="76438-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-785">Electricity</span></span></td>
<td><span data-ttu-id="76438-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-786">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-787">50,00</span><span class="sxs-lookup"><span data-stu-id="76438-787">50,00</span></span></td>
<td><span data-ttu-id="76438-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-789">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-789">CC001</span></span></td>
<td><span data-ttu-id="76438-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="76438-790">HR</span></span></td>
<td><span data-ttu-id="76438-791">10001</span><span class="sxs-lookup"><span data-stu-id="76438-791">10001</span></span></td>
<td><span data-ttu-id="76438-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-792">Electricity</span></span></td>
<td><span data-ttu-id="76438-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-793">Variable cost</span></span></td>
<td><span data-ttu-id="76438-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="76438-794">-1,245.71</span></span></td>
<td><span data-ttu-id="76438-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-796">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-796">CC002</span></span></td>
<td><span data-ttu-id="76438-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-797">Finance</span></span></td>
<td><span data-ttu-id="76438-798">10001</span><span class="sxs-lookup"><span data-stu-id="76438-798">10001</span></span></td>
<td><span data-ttu-id="76438-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-799">Electricity</span></span></td>
<td><span data-ttu-id="76438-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-800">Variable cost</span></span></td>
<td><span data-ttu-id="76438-801">436.00</span><span class="sxs-lookup"><span data-stu-id="76438-801">436.00</span></span></td>
<td><span data-ttu-id="76438-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-803">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-803">CC003</span></span></td>
<td><span data-ttu-id="76438-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-804">Assembly</span></span></td>
<td><span data-ttu-id="76438-805">10001</span><span class="sxs-lookup"><span data-stu-id="76438-805">10001</span></span></td>
<td><span data-ttu-id="76438-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-806">Electricity</span></span></td>
<td><span data-ttu-id="76438-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-807">Variable cost</span></span></td>
<td><span data-ttu-id="76438-808">685.14</span><span class="sxs-lookup"><span data-stu-id="76438-808">685.14</span></span></td>
<td><span data-ttu-id="76438-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-810">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-810">CC004</span></span></td>
<td><span data-ttu-id="76438-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-811">Packaging</span></span></td>
<td><span data-ttu-id="76438-812">10001</span><span class="sxs-lookup"><span data-stu-id="76438-812">10001</span></span></td>
<td><span data-ttu-id="76438-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-813">Electricity</span></span></td>
<td><span data-ttu-id="76438-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-814">Variable cost</span></span></td>
<td><span data-ttu-id="76438-815">124.57</span><span class="sxs-lookup"><span data-stu-id="76438-815">124.57</span></span></td>
<td><span data-ttu-id="76438-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-817">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-817">CC002</span></span></td>
<td><span data-ttu-id="76438-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-818">Finance</span></span></td>
<td><span data-ttu-id="76438-819">10001</span><span class="sxs-lookup"><span data-stu-id="76438-819">10001</span></span></td>
<td><span data-ttu-id="76438-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-820">Electricity</span></span></td>
<td><span data-ttu-id="76438-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-821">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="76438-822">-675.00</span></span></td>
<td><span data-ttu-id="76438-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-824">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-824">CC003</span></span></td>
<td><span data-ttu-id="76438-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-825">Assembly</span></span></td>
<td><span data-ttu-id="76438-826">10001</span><span class="sxs-lookup"><span data-stu-id="76438-826">10001</span></span></td>
<td><span data-ttu-id="76438-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-827">Electricity</span></span></td>
<td><span data-ttu-id="76438-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-828">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-829">438.75</span><span class="sxs-lookup"><span data-stu-id="76438-829">438.75</span></span></td>
<td><span data-ttu-id="76438-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-831">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-831">CC004</span></span></td>
<td><span data-ttu-id="76438-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-832">Packaging</span></span></td>
<td><span data-ttu-id="76438-833">10001</span><span class="sxs-lookup"><span data-stu-id="76438-833">10001</span></span></td>
<td><span data-ttu-id="76438-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-834">Electricity</span></span></td>
<td><span data-ttu-id="76438-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-835">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-836">236.25</span><span class="sxs-lookup"><span data-stu-id="76438-836">236.25</span></span></td>
<td><span data-ttu-id="76438-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-838">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-838">CC002</span></span></td>
<td><span data-ttu-id="76438-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="76438-839">Finance</span></span></td>
<td><span data-ttu-id="76438-840">10001</span><span class="sxs-lookup"><span data-stu-id="76438-840">10001</span></span></td>
<td><span data-ttu-id="76438-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-841">Electricity</span></span></td>
<td><span data-ttu-id="76438-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-842">Variable cost</span></span></td>
<td><span data-ttu-id="76438-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="76438-843">-8,150.29</span></span></td>
<td><span data-ttu-id="76438-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-845">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-845">CC003</span></span></td>
<td><span data-ttu-id="76438-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-846">Assembly</span></span></td>
<td><span data-ttu-id="76438-847">10001</span><span class="sxs-lookup"><span data-stu-id="76438-847">10001</span></span></td>
<td><span data-ttu-id="76438-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-848">Electricity</span></span></td>
<td><span data-ttu-id="76438-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-849">Variable cost</span></span></td>
<td><span data-ttu-id="76438-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="76438-850">5,297.69</span></span></td>
<td><span data-ttu-id="76438-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-852">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-852">CC004</span></span></td>
<td><span data-ttu-id="76438-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="76438-853">Packaging</span></span></td>
<td><span data-ttu-id="76438-854">10001</span><span class="sxs-lookup"><span data-stu-id="76438-854">10001</span></span></td>
<td><span data-ttu-id="76438-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-855">Electricity</span></span></td>
<td><span data-ttu-id="76438-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-856">Variable cost</span></span></td>
<td><span data-ttu-id="76438-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="76438-857">2,852.60</span></span></td>
<td><span data-ttu-id="76438-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-859">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-859">CC003</span></span></td>
<td><span data-ttu-id="76438-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-860">Assembly</span></span></td>
<td><span data-ttu-id="76438-861">10001</span><span class="sxs-lookup"><span data-stu-id="76438-861">10001</span></span></td>
<td><span data-ttu-id="76438-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-862">Electricity</span></span></td>
<td><span data-ttu-id="76438-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-863">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="76438-864">-713.75</span></span></td>
<td><span data-ttu-id="76438-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-866">Prod 1</span></span></td>
<td><span data-ttu-id="76438-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-867">Product 1</span></span></td>
<td><span data-ttu-id="76438-868">10001</span><span class="sxs-lookup"><span data-stu-id="76438-868">10001</span></span></td>
<td><span data-ttu-id="76438-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-869">Electricity</span></span></td>
<td><span data-ttu-id="76438-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-870">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-871">535.31</span><span class="sxs-lookup"><span data-stu-id="76438-871">535.31</span></span></td>
<td><span data-ttu-id="76438-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-873">Prod 2</span></span></td>
<td><span data-ttu-id="76438-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-874">Product 2</span></span></td>
<td><span data-ttu-id="76438-875">10001</span><span class="sxs-lookup"><span data-stu-id="76438-875">10001</span></span></td>
<td><span data-ttu-id="76438-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-876">Electricity</span></span></td>
<td><span data-ttu-id="76438-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-877">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-878">178.44</span><span class="sxs-lookup"><span data-stu-id="76438-878">178.44</span></span></td>
<td><span data-ttu-id="76438-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-880">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-880">CC003</span></span></td>
<td><span data-ttu-id="76438-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-881">Assembly</span></span></td>
<td><span data-ttu-id="76438-882">10001</span><span class="sxs-lookup"><span data-stu-id="76438-882">10001</span></span></td>
<td><span data-ttu-id="76438-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-883">Electricity</span></span></td>
<td><span data-ttu-id="76438-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-884">Variable cost</span></span></td>
<td><span data-ttu-id="76438-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="76438-885">-5,982.83</span></span></td>
<td><span data-ttu-id="76438-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-887">Prod 1</span></span></td>
<td><span data-ttu-id="76438-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-888">Product 1</span></span></td>
<td><span data-ttu-id="76438-889">10001</span><span class="sxs-lookup"><span data-stu-id="76438-889">10001</span></span></td>
<td><span data-ttu-id="76438-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-890">Electricity</span></span></td>
<td><span data-ttu-id="76438-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-891">Variable cost</span></span></td>
<td><span data-ttu-id="76438-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="76438-892">4,487.12</span></span></td>
<td><span data-ttu-id="76438-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-894">Prod 2</span></span></td>
<td><span data-ttu-id="76438-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-895">Product 2</span></span></td>
<td><span data-ttu-id="76438-896">10001</span><span class="sxs-lookup"><span data-stu-id="76438-896">10001</span></span></td>
<td><span data-ttu-id="76438-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-897">Electricity</span></span></td>
<td><span data-ttu-id="76438-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-898">Variable cost</span></span></td>
<td><span data-ttu-id="76438-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="76438-899">1,495.71</span></span></td>
<td><span data-ttu-id="76438-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-901">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-901">CC003</span></span></td>
<td><span data-ttu-id="76438-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-902">Assembly</span></span></td>
<td><span data-ttu-id="76438-903">10001</span><span class="sxs-lookup"><span data-stu-id="76438-903">10001</span></span></td>
<td><span data-ttu-id="76438-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-904">Electricity</span></span></td>
<td><span data-ttu-id="76438-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-905">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="76438-906">-286.25</span></span></td>
<td><span data-ttu-id="76438-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-908">Prod 1</span></span></td>
<td><span data-ttu-id="76438-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-909">Product 1</span></span></td>
<td><span data-ttu-id="76438-910">10001</span><span class="sxs-lookup"><span data-stu-id="76438-910">10001</span></span></td>
<td><span data-ttu-id="76438-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-911">Electricity</span></span></td>
<td><span data-ttu-id="76438-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-912">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-913">241.05</span><span class="sxs-lookup"><span data-stu-id="76438-913">241.05</span></span></td>
<td><span data-ttu-id="76438-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-915">Prod 2</span></span></td>
<td><span data-ttu-id="76438-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-916">Product 2</span></span></td>
<td><span data-ttu-id="76438-917">10001</span><span class="sxs-lookup"><span data-stu-id="76438-917">10001</span></span></td>
<td><span data-ttu-id="76438-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-918">Electricity</span></span></td>
<td><span data-ttu-id="76438-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-919">Fixed cost</span></span></td>
<td><span data-ttu-id="76438-920">45.20</span><span class="sxs-lookup"><span data-stu-id="76438-920">45.20</span></span></td>
<td><span data-ttu-id="76438-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-922">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-922">CC003</span></span></td>
<td><span data-ttu-id="76438-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="76438-923">Assembly</span></span></td>
<td><span data-ttu-id="76438-924">10001</span><span class="sxs-lookup"><span data-stu-id="76438-924">10001</span></span></td>
<td><span data-ttu-id="76438-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-925">Electricity</span></span></td>
<td><span data-ttu-id="76438-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-926">Variable cost</span></span></td>
<td><span data-ttu-id="76438-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="76438-927">-2,977.17</span></span></td>
<td><span data-ttu-id="76438-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-929">Prod 1</span></span></td>
<td><span data-ttu-id="76438-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-930">Product 1</span></span></td>
<td><span data-ttu-id="76438-931">10001</span><span class="sxs-lookup"><span data-stu-id="76438-931">10001</span></span></td>
<td><span data-ttu-id="76438-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-932">Electricity</span></span></td>
<td><span data-ttu-id="76438-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-933">Variable cost</span></span></td>
<td><span data-ttu-id="76438-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="76438-934">2,507.09</span></span></td>
<td><span data-ttu-id="76438-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="76438-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-936">Prod 2</span></span></td>
<td><span data-ttu-id="76438-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="76438-937">Product 2</span></span></td>
<td><span data-ttu-id="76438-938">10001</span><span class="sxs-lookup"><span data-stu-id="76438-938">10001</span></span></td>
<td><span data-ttu-id="76438-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-939">Electricity</span></span></td>
<td><span data-ttu-id="76438-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-940">Variable cost</span></span></td>
<td><span data-ttu-id="76438-941">470.08</span><span class="sxs-lookup"><span data-stu-id="76438-941">470.08</span></span></td>
<td><span data-ttu-id="76438-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="76438-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="76438-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="76438-943">Conclusion</span></span>
<span data-ttu-id="76438-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="76438-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="76438-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="76438-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="76438-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="76438-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="76438-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="76438-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="76438-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="76438-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="76438-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="76438-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="76438-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="76438-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="76438-951">CC099</span><span class="sxs-lookup"><span data-stu-id="76438-951">CC099</span></span></th>
<th><span data-ttu-id="76438-952">CC001</span><span class="sxs-lookup"><span data-stu-id="76438-952">CC001</span></span></th>
<th><span data-ttu-id="76438-953">CC002</span><span class="sxs-lookup"><span data-stu-id="76438-953">CC002</span></span></th>
<th><span data-ttu-id="76438-954">CC003</span><span class="sxs-lookup"><span data-stu-id="76438-954">CC003</span></span></th>
<th><span data-ttu-id="76438-955">CC004</span><span class="sxs-lookup"><span data-stu-id="76438-955">CC004</span></span></th>
<th><span data-ttu-id="76438-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-956">Proj 1</span></span></th>
<th><span data-ttu-id="76438-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="76438-957">Proj 2</span></span></th>
<th><span data-ttu-id="76438-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-958">Prod 1</span></span></th>
<th><span data-ttu-id="76438-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="76438-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="76438-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="76438-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="76438-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="76438-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="76438-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="76438-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="76438-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-971">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="76438-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-973">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-974">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-975">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-976">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-977">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="76438-978">776.36</span><span class="sxs-lookup"><span data-stu-id="76438-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-979">223.64</span><span class="sxs-lookup"><span data-stu-id="76438-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="76438-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="76438-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-982">000</span><span class="sxs-lookup"><span data-stu-id="76438-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-983">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-984">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-985">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-986">0,00</span><span class="sxs-lookup"><span data-stu-id="76438-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-987">30,00</span><span class="sxs-lookup"><span data-stu-id="76438-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-988">10,00</span><span class="sxs-lookup"><span data-stu-id="76438-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="76438-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="76438-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="76438-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="76438-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="76438-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="76438-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="76438-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="76438-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="76438-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="76438-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="76438-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="76438-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="76438-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="76438-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



