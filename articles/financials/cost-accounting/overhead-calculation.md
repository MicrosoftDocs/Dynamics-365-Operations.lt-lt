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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "335122"
---
# <a name="overhead-calculation"></a><span data-ttu-id="73298-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="73298-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73298-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="73298-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="73298-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="73298-105">Term definition</span></span>
---------------

<span data-ttu-id="73298-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="73298-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="73298-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="73298-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="73298-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="73298-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="73298-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="73298-109">Rent</span></span>
-   <span data-ttu-id="73298-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-110">Electricity</span></span>
-   <span data-ttu-id="73298-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="73298-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="73298-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="73298-112">Overhead calculation overview</span></span>
<span data-ttu-id="73298-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="73298-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="73298-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="73298-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="73298-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="73298-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="73298-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="73298-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="73298-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="73298-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="73298-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="73298-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="73298-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="73298-119">Version type</span></span>
-   <span data-ttu-id="73298-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="73298-120">Date and time</span></span>
-   <span data-ttu-id="73298-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="73298-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="73298-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="73298-122">Fiscal year</span></span>
-   <span data-ttu-id="73298-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-123">Fiscal period</span></span>

<span data-ttu-id="73298-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="73298-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="73298-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="73298-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="73298-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="73298-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="73298-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="73298-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="73298-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="73298-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="73298-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="73298-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="73298-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="73298-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="73298-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="73298-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="73298-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="73298-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="73298-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="73298-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="73298-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="73298-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="73298-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="73298-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="73298-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="73298-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="73298-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="73298-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73298-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="73298-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="73298-140">Main account</span></span></th>
<th><span data-ttu-id="73298-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="73298-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="73298-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="73298-143">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-143">CC099</span></span></td>
<td><span data-ttu-id="73298-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-144">Default cost center</span></span></td>
<td><span data-ttu-id="73298-145">10001</span><span class="sxs-lookup"><span data-stu-id="73298-145">10001</span></span></td>
<td><span data-ttu-id="73298-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-146">Electricity</span></span></td>
<td><span data-ttu-id="73298-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="73298-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="73298-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="73298-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="73298-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="73298-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="73298-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="73298-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="73298-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="73298-151">Define the cost behavior rule</span></span>

<span data-ttu-id="73298-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="73298-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="73298-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="73298-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="73298-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="73298-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="73298-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="73298-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="73298-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="73298-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="73298-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="73298-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="73298-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="73298-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-160">Journal</span></span></th>
<th><span data-ttu-id="73298-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="73298-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73298-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73298-163">Versija</span><span class="sxs-lookup"><span data-stu-id="73298-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-164">00001</span><span class="sxs-lookup"><span data-stu-id="73298-164">00001</span></span></td>
<td><span data-ttu-id="73298-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="73298-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="73298-166">Fiscal</span></span></td>
<td><span data-ttu-id="73298-167">2017</span><span class="sxs-lookup"><span data-stu-id="73298-167">2017</span></span></td>
<td><span data-ttu-id="73298-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-168">Period 1</span></span></td>
<td><span data-ttu-id="73298-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73298-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="73298-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73298-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-173">Cost element</span></span></th>
<th><span data-ttu-id="73298-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-174">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-175">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="73298-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="73298-177">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-177">CC099</span></span></td>
<td><span data-ttu-id="73298-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-178">Default cost center</span></span></td>
<td><span data-ttu-id="73298-179">10001</span><span class="sxs-lookup"><span data-stu-id="73298-179">10001</span></span></td>
<td><span data-ttu-id="73298-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-180">Electricity</span></span></td>
<td><span data-ttu-id="73298-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="73298-181">Unclassified</span></span></td>
<td><span data-ttu-id="73298-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="73298-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73298-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="73298-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-185">Cost element</span></span></th>
<th><span data-ttu-id="73298-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-186">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-187">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-187">Amount</span></span></th>
<th><span data-ttu-id="73298-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-189">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-189">CC099</span></span></td>
<td><span data-ttu-id="73298-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-190">Default cost center</span></span></td>
<td><span data-ttu-id="73298-191">10001</span><span class="sxs-lookup"><span data-stu-id="73298-191">10001</span></span></td>
<td><span data-ttu-id="73298-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-192">Electricity</span></span></td>
<td><span data-ttu-id="73298-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="73298-193">Unclassified</span></span></td>
<td><span data-ttu-id="73298-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="73298-194">10,000.00</span></span></td>
<td><span data-ttu-id="73298-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="73298-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-196">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-196">CC099</span></span></td>
<td><span data-ttu-id="73298-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-197">Default cost center</span></span></td>
<td><span data-ttu-id="73298-198">10001</span><span class="sxs-lookup"><span data-stu-id="73298-198">10001</span></span></td>
<td><span data-ttu-id="73298-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-199">Electricity</span></span></td>
<td><span data-ttu-id="73298-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="73298-200">Unclassified</span></span></td>
<td><span data-ttu-id="73298-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="73298-201">-10,000.00</span></span></td>
<td><span data-ttu-id="73298-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-203">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-203">CC099</span></span></td>
<td><span data-ttu-id="73298-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-204">Default cost center</span></span></td>
<td><span data-ttu-id="73298-205">10001</span><span class="sxs-lookup"><span data-stu-id="73298-205">10001</span></span></td>
<td><span data-ttu-id="73298-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-206">Electricity</span></span></td>
<td><span data-ttu-id="73298-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-207">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="73298-208">1,000.00</span></span></td>
<td><span data-ttu-id="73298-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-210">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-210">CC099</span></span></td>
<td><span data-ttu-id="73298-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-211">Default cost center</span></span></td>
<td><span data-ttu-id="73298-212">10001</span><span class="sxs-lookup"><span data-stu-id="73298-212">10001</span></span></td>
<td><span data-ttu-id="73298-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-213">Electricity</span></span></td>
<td><span data-ttu-id="73298-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-214">Variable cost</span></span></td>
<td><span data-ttu-id="73298-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="73298-215">9,000.00</span></span></td>
<td><span data-ttu-id="73298-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="73298-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="73298-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="73298-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="73298-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="73298-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="73298-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="73298-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="73298-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="73298-221">Define the cost distribution rule</span></span>

<span data-ttu-id="73298-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="73298-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="73298-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="73298-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="73298-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="73298-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="73298-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="73298-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="73298-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="73298-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="73298-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="73298-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-228">Cost object</span></span></th>
<th><span data-ttu-id="73298-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="73298-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-230">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-230">CC001</span></span></td>
<td><span data-ttu-id="73298-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-231">HR</span></span></td>
<td><span data-ttu-id="73298-232">1000</span><span class="sxs-lookup"><span data-stu-id="73298-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-233">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-233">CC002</span></span></td>
<td><span data-ttu-id="73298-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-234">Finance</span></span></td>
<td><span data-ttu-id="73298-235">6,000</span><span class="sxs-lookup"><span data-stu-id="73298-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-236">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-236">CC003</span></span></td>
<td><span data-ttu-id="73298-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-237">Assembly</span></span></td>
<td><span data-ttu-id="73298-238">0</span><span class="sxs-lookup"><span data-stu-id="73298-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-240">Cost object</span></span></th>
<th><span data-ttu-id="73298-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-241">Magnitude</span></span></th>
<th><span data-ttu-id="73298-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-242">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-243">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-244">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-244">CC001</span></span></td>
<td><span data-ttu-id="73298-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-245">HR</span></span></td>
<td><span data-ttu-id="73298-246">1000</span><span class="sxs-lookup"><span data-stu-id="73298-246">1,000</span></span></td>
<td><span data-ttu-id="73298-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73298-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="73298-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-249">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-249">CC002</span></span></td>
<td><span data-ttu-id="73298-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-250">Finance</span></span></td>
<td><span data-ttu-id="73298-251">6,000</span><span class="sxs-lookup"><span data-stu-id="73298-251">6,000</span></span></td>
<td><span data-ttu-id="73298-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73298-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="73298-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-254">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-254">CC003</span></span></td>
<td><span data-ttu-id="73298-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-255">Assembly</span></span></td>
<td><span data-ttu-id="73298-256">0</span><span class="sxs-lookup"><span data-stu-id="73298-256">0</span></span></td>
<td><span data-ttu-id="73298-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="73298-258">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="73298-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="73298-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-261">Cost object</span></span></th>
<th><span data-ttu-id="73298-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="73298-262">Formula</span></span></th>
<th><span data-ttu-id="73298-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-263">Magnitude</span></span></th>
<th><span data-ttu-id="73298-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-264">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-265">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-266">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-266">CC001</span></span></td>
<td><span data-ttu-id="73298-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-267">HR</span></span></td>
<td><span data-ttu-id="73298-268">{1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73298-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73298-269">1</span><span class="sxs-lookup"><span data-stu-id="73298-269">1</span></span></td>
<td><span data-ttu-id="73298-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73298-271">500,00</span><span class="sxs-lookup"><span data-stu-id="73298-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-272">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-272">CC002</span></span></td>
<td><span data-ttu-id="73298-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-273">Finance</span></span></td>
<td><span data-ttu-id="73298-274">{6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73298-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73298-275">1</span><span class="sxs-lookup"><span data-stu-id="73298-275">1</span></span></td>
<td><span data-ttu-id="73298-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73298-277">500,00</span><span class="sxs-lookup"><span data-stu-id="73298-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-278">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-278">CC003</span></span></td>
<td><span data-ttu-id="73298-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-279">Assembly</span></span></td>
<td><span data-ttu-id="73298-280">{0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="73298-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="73298-281">0</span><span class="sxs-lookup"><span data-stu-id="73298-281">0</span></span></td>
<td><span data-ttu-id="73298-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="73298-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="73298-283">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="73298-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-285">Journal</span></span></th>
<th><span data-ttu-id="73298-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="73298-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73298-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73298-288">Versija</span><span class="sxs-lookup"><span data-stu-id="73298-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-289">00002</span><span class="sxs-lookup"><span data-stu-id="73298-289">00002</span></span></td>
<td><span data-ttu-id="73298-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="73298-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="73298-291">Fiscal</span></span></td>
<td><span data-ttu-id="73298-292">2017</span><span class="sxs-lookup"><span data-stu-id="73298-292">2017</span></span></td>
<td><span data-ttu-id="73298-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-293">Period 1</span></span></td>
<td><span data-ttu-id="73298-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73298-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="73298-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73298-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-298">Cost element</span></span></th>
<th><span data-ttu-id="73298-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-299">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-300">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-302">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-302">CC099</span></span></td>
<td><span data-ttu-id="73298-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-303">Default cost center</span></span></td>
<td><span data-ttu-id="73298-304">10001</span><span class="sxs-lookup"><span data-stu-id="73298-304">10001</span></span></td>
<td><span data-ttu-id="73298-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-305">Electricity</span></span></td>
<td><span data-ttu-id="73298-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-306">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="73298-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-309">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-309">CC099</span></span></td>
<td><span data-ttu-id="73298-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-310">Default cost center</span></span></td>
<td><span data-ttu-id="73298-311">10001</span><span class="sxs-lookup"><span data-stu-id="73298-311">10001</span></span></td>
<td><span data-ttu-id="73298-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-312">Electricity</span></span></td>
<td><span data-ttu-id="73298-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-313">Variable cost</span></span></td>
<td><span data-ttu-id="73298-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="73298-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73298-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="73298-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-317">Cost element</span></span></th>
<th><span data-ttu-id="73298-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-318">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-319">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-319">Amount</span></span></th>
<th><span data-ttu-id="73298-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-321">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-321">CC099</span></span></td>
<td><span data-ttu-id="73298-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-322">Default cost center</span></span></td>
<td><span data-ttu-id="73298-323">10001</span><span class="sxs-lookup"><span data-stu-id="73298-323">10001</span></span></td>
<td><span data-ttu-id="73298-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-324">Electricity</span></span></td>
<td><span data-ttu-id="73298-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-325">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="73298-326">-1,000.00</span></span></td>
<td><span data-ttu-id="73298-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-328">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-328">CC001</span></span></td>
<td><span data-ttu-id="73298-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-329">HR</span></span></td>
<td><span data-ttu-id="73298-330">10001</span><span class="sxs-lookup"><span data-stu-id="73298-330">10001</span></span></td>
<td><span data-ttu-id="73298-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-331">Electricity</span></span></td>
<td><span data-ttu-id="73298-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-332">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-333">500,00</span><span class="sxs-lookup"><span data-stu-id="73298-333">500.00</span></span></td>
<td><span data-ttu-id="73298-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-335">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-335">CC002</span></span></td>
<td><span data-ttu-id="73298-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-336">Finance</span></span></td>
<td><span data-ttu-id="73298-337">10001</span><span class="sxs-lookup"><span data-stu-id="73298-337">10001</span></span></td>
<td><span data-ttu-id="73298-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-338">Electricity</span></span></td>
<td><span data-ttu-id="73298-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-339">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-340">500,00</span><span class="sxs-lookup"><span data-stu-id="73298-340">500.00</span></span></td>
<td><span data-ttu-id="73298-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-342">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-342">CC099</span></span></td>
<td><span data-ttu-id="73298-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="73298-343">Default cost center</span></span></td>
<td><span data-ttu-id="73298-344">10001</span><span class="sxs-lookup"><span data-stu-id="73298-344">10001</span></span></td>
<td><span data-ttu-id="73298-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-345">Electricity</span></span></td>
<td><span data-ttu-id="73298-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-346">Variable cost</span></span></td>
<td><span data-ttu-id="73298-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="73298-347">-9,000.00</span></span></td>
<td><span data-ttu-id="73298-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-349">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-349">CC001</span></span></td>
<td><span data-ttu-id="73298-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-350">HR</span></span></td>
<td><span data-ttu-id="73298-351">10001</span><span class="sxs-lookup"><span data-stu-id="73298-351">10001</span></span></td>
<td><span data-ttu-id="73298-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-352">Electricity</span></span></td>
<td><span data-ttu-id="73298-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-353">Variable cost</span></span></td>
<td><span data-ttu-id="73298-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="73298-354">1,285.71</span></span></td>
<td><span data-ttu-id="73298-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-356">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-356">CC002</span></span></td>
<td><span data-ttu-id="73298-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-357">Finance</span></span></td>
<td><span data-ttu-id="73298-358">10001</span><span class="sxs-lookup"><span data-stu-id="73298-358">10001</span></span></td>
<td><span data-ttu-id="73298-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-359">Electricity</span></span></td>
<td><span data-ttu-id="73298-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-360">Variable cost</span></span></td>
<td><span data-ttu-id="73298-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="73298-361">7,714.29</span></span></td>
<td><span data-ttu-id="73298-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="73298-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="73298-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="73298-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="73298-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="73298-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="73298-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="73298-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="73298-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="73298-367">Define the overhead rate</span></span>

<span data-ttu-id="73298-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="73298-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="73298-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="73298-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-370">Cost object</span></span></th>
<th><span data-ttu-id="73298-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="73298-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-372">Proj 1</span></span></td>
<td><span data-ttu-id="73298-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-373">Project 1</span></span></td>
<td><span data-ttu-id="73298-374">3</span><span class="sxs-lookup"><span data-stu-id="73298-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-375">Proj 2</span></span></td>
<td><span data-ttu-id="73298-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-376">Project 2</span></span></td>
<td><span data-ttu-id="73298-377">1</span><span class="sxs-lookup"><span data-stu-id="73298-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="73298-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-379">Cost object</span></span></th>
<th><span data-ttu-id="73298-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-380">Cost element</span></span></th>
<th><span data-ttu-id="73298-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-381">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="73298-382">Units</span></span></th>
<th><span data-ttu-id="73298-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="73298-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-384">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-384">CC001</span></span></td>
<td><span data-ttu-id="73298-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-385">HR</span></span></td>
<td><span data-ttu-id="73298-386">10001</span><span class="sxs-lookup"><span data-stu-id="73298-386">10001</span></span></td>
<td><span data-ttu-id="73298-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-387">Variable cost</span></span></td>
<td><span data-ttu-id="73298-388">1</span><span class="sxs-lookup"><span data-stu-id="73298-388">1</span></span></td>
<td><span data-ttu-id="73298-389">10</span><span class="sxs-lookup"><span data-stu-id="73298-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-391">Cost object</span></span></th>
<th><span data-ttu-id="73298-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-392">Magnitude</span></span></th>
<th><span data-ttu-id="73298-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-393">Cost element</span></span></th>
<th><span data-ttu-id="73298-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-394">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-395">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-396">Proj 1</span></span></td>
<td><span data-ttu-id="73298-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-397">Project 1</span></span></td>
<td><span data-ttu-id="73298-398">3</span><span class="sxs-lookup"><span data-stu-id="73298-398">3</span></span></td>
<td><span data-ttu-id="73298-399">10001</span><span class="sxs-lookup"><span data-stu-id="73298-399">10001</span></span></td>
<td><span data-ttu-id="73298-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="73298-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="73298-401">30,00</span><span class="sxs-lookup"><span data-stu-id="73298-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-402">Proj 2</span></span></td>
<td><span data-ttu-id="73298-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-403">Project 2</span></span></td>
<td><span data-ttu-id="73298-404">1</span><span class="sxs-lookup"><span data-stu-id="73298-404">1</span></span></td>
<td><span data-ttu-id="73298-405">10001</span><span class="sxs-lookup"><span data-stu-id="73298-405">10001</span></span></td>
<td><span data-ttu-id="73298-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="73298-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="73298-407">10,00</span><span class="sxs-lookup"><span data-stu-id="73298-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="73298-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-409">Journal</span></span></th>
<th><span data-ttu-id="73298-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="73298-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73298-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73298-412">Versija</span><span class="sxs-lookup"><span data-stu-id="73298-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-413">00003</span><span class="sxs-lookup"><span data-stu-id="73298-413">00003</span></span></td>
<td><span data-ttu-id="73298-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="73298-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="73298-415">Fiscal</span></span></td>
<td><span data-ttu-id="73298-416">2017</span><span class="sxs-lookup"><span data-stu-id="73298-416">2017</span></span></td>
<td><span data-ttu-id="73298-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-417">Period 1</span></span></td>
<td><span data-ttu-id="73298-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="73298-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="73298-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73298-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-421">Cost object</span></span></th>
<th><span data-ttu-id="73298-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-424">Proj 1</span></span></td>
<td><span data-ttu-id="73298-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="73298-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="73298-426">3,00</span><span class="sxs-lookup"><span data-stu-id="73298-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-428">Proj 2</span></span></td>
<td><span data-ttu-id="73298-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="73298-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="73298-430">1,00</span><span class="sxs-lookup"><span data-stu-id="73298-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73298-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="73298-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-433">Cost element</span></span></th>
<th><span data-ttu-id="73298-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-434">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-435">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-435">Amount</span></span></th>
<th><span data-ttu-id="73298-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="73298-437">CC0001</span></span></td>
<td><span data-ttu-id="73298-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-438">HR</span></span></td>
<td><span data-ttu-id="73298-439">10001</span><span class="sxs-lookup"><span data-stu-id="73298-439">10001</span></span></td>
<td><span data-ttu-id="73298-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-440">Electricity</span></span></td>
<td><span data-ttu-id="73298-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-441">Variable cost</span></span></td>
<td><span data-ttu-id="73298-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="73298-442">-30.00</span></span></td>
<td><span data-ttu-id="73298-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-444">Proj 1</span></span></td>
<td><span data-ttu-id="73298-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="73298-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="73298-446">10001</span><span class="sxs-lookup"><span data-stu-id="73298-446">10001</span></span></td>
<td><span data-ttu-id="73298-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-447">Electricity</span></span></td>
<td><span data-ttu-id="73298-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-448">Variable cost</span></span></td>
<td><span data-ttu-id="73298-449">30,00</span><span class="sxs-lookup"><span data-stu-id="73298-449">30.00</span></span></td>
<td><span data-ttu-id="73298-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-451">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-451">CC001</span></span></td>
<td><span data-ttu-id="73298-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-452">HR</span></span></td>
<td><span data-ttu-id="73298-453">10001</span><span class="sxs-lookup"><span data-stu-id="73298-453">10001</span></span></td>
<td><span data-ttu-id="73298-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-454">Electricity</span></span></td>
<td><span data-ttu-id="73298-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-455">Variable cost</span></span></td>
<td><span data-ttu-id="73298-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="73298-456">-10.00</span></span></td>
<td><span data-ttu-id="73298-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-458">Proj 2</span></span></td>
<td><span data-ttu-id="73298-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="73298-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="73298-460">10001</span><span class="sxs-lookup"><span data-stu-id="73298-460">10001</span></span></td>
<td><span data-ttu-id="73298-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-461">Electricity</span></span></td>
<td><span data-ttu-id="73298-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-462">Variable cost</span></span></td>
<td><span data-ttu-id="73298-463">10,00</span><span class="sxs-lookup"><span data-stu-id="73298-463">10.00</span></span></td>
<td><span data-ttu-id="73298-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="73298-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="73298-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="73298-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="73298-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="73298-468">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="73298-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="73298-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="73298-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="73298-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="73298-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="73298-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="73298-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="73298-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="73298-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="73298-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="73298-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="73298-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="73298-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="73298-475">Define the cost allocation</span></span>

<span data-ttu-id="73298-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="73298-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="73298-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="73298-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="73298-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="73298-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-479">Cost object</span></span></th>
<th><span data-ttu-id="73298-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="73298-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-481">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-481">CC002</span></span></td>
<td><span data-ttu-id="73298-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-482">Finance</span></span></td>
<td><span data-ttu-id="73298-483">35</span><span class="sxs-lookup"><span data-stu-id="73298-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-484">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-484">CC003</span></span></td>
<td><span data-ttu-id="73298-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-485">Assembly</span></span></td>
<td><span data-ttu-id="73298-486">55</span><span class="sxs-lookup"><span data-stu-id="73298-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-487">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-487">CC004</span></span></td>
<td><span data-ttu-id="73298-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-488">Packaging</span></span></td>
<td><span data-ttu-id="73298-489">10</span><span class="sxs-lookup"><span data-stu-id="73298-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="73298-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="73298-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="73298-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-492">Cost object</span></span></th>
<th><span data-ttu-id="73298-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="73298-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-494">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-494">CC003</span></span></td>
<td><span data-ttu-id="73298-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-495">Assembly</span></span></td>
<td><span data-ttu-id="73298-496">65</span><span class="sxs-lookup"><span data-stu-id="73298-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-497">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-497">CC004</span></span></td>
<td><span data-ttu-id="73298-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-498">Packaging</span></span></td>
<td><span data-ttu-id="73298-499">35</span><span class="sxs-lookup"><span data-stu-id="73298-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="73298-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="73298-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="73298-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-502">Cost object</span></span></th>
<th><span data-ttu-id="73298-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="73298-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-504">Prod 1</span></span></td>
<td><span data-ttu-id="73298-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-505">Product 1</span></span></td>
<td><span data-ttu-id="73298-506">60</span><span class="sxs-lookup"><span data-stu-id="73298-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-507">Prod 2</span></span></td>
<td><span data-ttu-id="73298-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-508">Product 2</span></span></td>
<td><span data-ttu-id="73298-509">20</span><span class="sxs-lookup"><span data-stu-id="73298-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="73298-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="73298-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="73298-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-512">Cost object</span></span></th>
<th><span data-ttu-id="73298-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="73298-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-514">Prod 1</span></span></td>
<td><span data-ttu-id="73298-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-515">Product 1</span></span></td>
<td><span data-ttu-id="73298-516">80</span><span class="sxs-lookup"><span data-stu-id="73298-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-517">Prod 2</span></span></td>
<td><span data-ttu-id="73298-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-518">Product 2</span></span></td>
<td><span data-ttu-id="73298-519">15</span><span class="sxs-lookup"><span data-stu-id="73298-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="73298-520">Programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="73298-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="73298-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="73298-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="73298-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-523">Cost object</span></span></th>
<th><span data-ttu-id="73298-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-524">Magnitude</span></span></th>
<th><span data-ttu-id="73298-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-525">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-526">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-526">Amount</span></span></th>
<th><span data-ttu-id="73298-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-528">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-528">CC002</span></span></td>
<td><span data-ttu-id="73298-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-529">Finance</span></span></td>
<td><span data-ttu-id="73298-530">35</span><span class="sxs-lookup"><span data-stu-id="73298-530">35</span></span></td>
<td><span data-ttu-id="73298-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73298-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73298-532">175.00</span><span class="sxs-lookup"><span data-stu-id="73298-532">175.00</span></span></td>
<td><span data-ttu-id="73298-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-534">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-534">CC003</span></span></td>
<td><span data-ttu-id="73298-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-535">Assembly</span></span></td>
<td><span data-ttu-id="73298-536">55</span><span class="sxs-lookup"><span data-stu-id="73298-536">55</span></span></td>
<td><span data-ttu-id="73298-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73298-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73298-538">275.00</span><span class="sxs-lookup"><span data-stu-id="73298-538">275.00</span></span></td>
<td><span data-ttu-id="73298-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-540">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-540">CC004</span></span></td>
<td><span data-ttu-id="73298-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-541">Packaging</span></span></td>
<td><span data-ttu-id="73298-542">10</span><span class="sxs-lookup"><span data-stu-id="73298-542">10</span></span></td>
<td><span data-ttu-id="73298-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="73298-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="73298-544">50,00</span><span class="sxs-lookup"><span data-stu-id="73298-544">50.00</span></span></td>
<td><span data-ttu-id="73298-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-546">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-546">CC002</span></span></td>
<td><span data-ttu-id="73298-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-547">Finance</span></span></td>
<td><span data-ttu-id="73298-548">35</span><span class="sxs-lookup"><span data-stu-id="73298-548">35</span></span></td>
<td><span data-ttu-id="73298-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73298-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73298-550">436.00</span><span class="sxs-lookup"><span data-stu-id="73298-550">436.00</span></span></td>
<td><span data-ttu-id="73298-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-552">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-552">CC003</span></span></td>
<td><span data-ttu-id="73298-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-553">Assembly</span></span></td>
<td><span data-ttu-id="73298-554">55</span><span class="sxs-lookup"><span data-stu-id="73298-554">55</span></span></td>
<td><span data-ttu-id="73298-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73298-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73298-556">685.14</span><span class="sxs-lookup"><span data-stu-id="73298-556">685.14</span></span></td>
<td><span data-ttu-id="73298-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-558">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-558">CC004</span></span></td>
<td><span data-ttu-id="73298-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-559">Packaging</span></span></td>
<td><span data-ttu-id="73298-560">10</span><span class="sxs-lookup"><span data-stu-id="73298-560">10</span></span></td>
<td><span data-ttu-id="73298-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="73298-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="73298-562">124.57</span><span class="sxs-lookup"><span data-stu-id="73298-562">124.57</span></span></td>
<td><span data-ttu-id="73298-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-565">Cost object</span></span></th>
<th><span data-ttu-id="73298-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-566">Magnitude</span></span></th>
<th><span data-ttu-id="73298-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-567">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-568">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-568">Amount</span></span></th>
<th><span data-ttu-id="73298-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-570">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-570">CC003</span></span></td>
<td><span data-ttu-id="73298-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-571">Assembly</span></span></td>
<td><span data-ttu-id="73298-572">65</span><span class="sxs-lookup"><span data-stu-id="73298-572">65</span></span></td>
<td><span data-ttu-id="73298-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="73298-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="73298-574">438.75</span><span class="sxs-lookup"><span data-stu-id="73298-574">438.75</span></span></td>
<td><span data-ttu-id="73298-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-576">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-576">CC004</span></span></td>
<td><span data-ttu-id="73298-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-577">Packaging</span></span></td>
<td><span data-ttu-id="73298-578">35</span><span class="sxs-lookup"><span data-stu-id="73298-578">35</span></span></td>
<td><span data-ttu-id="73298-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="73298-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="73298-580">236.25</span><span class="sxs-lookup"><span data-stu-id="73298-580">236.25</span></span></td>
<td><span data-ttu-id="73298-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-582">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-582">CC003</span></span></td>
<td><span data-ttu-id="73298-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-583">Assembly</span></span></td>
<td><span data-ttu-id="73298-584">65</span><span class="sxs-lookup"><span data-stu-id="73298-584">65</span></span></td>
<td><span data-ttu-id="73298-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="73298-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="73298-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="73298-586">5,297.69</span></span></td>
<td><span data-ttu-id="73298-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-588">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-588">CC004</span></span></td>
<td><span data-ttu-id="73298-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-589">Packaging</span></span></td>
<td><span data-ttu-id="73298-590">35</span><span class="sxs-lookup"><span data-stu-id="73298-590">35</span></span></td>
<td><span data-ttu-id="73298-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="73298-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="73298-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="73298-592">2,852.60</span></span></td>
<td><span data-ttu-id="73298-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-595">Cost object</span></span></th>
<th><span data-ttu-id="73298-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-596">Magnitude</span></span></th>
<th><span data-ttu-id="73298-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-597">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-598">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-598">Amount</span></span></th>
<th><span data-ttu-id="73298-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-600">Prod 1</span></span></td>
<td><span data-ttu-id="73298-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-601">Product 1</span></span></td>
<td><span data-ttu-id="73298-602">60</span><span class="sxs-lookup"><span data-stu-id="73298-602">60</span></span></td>
<td><span data-ttu-id="73298-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="73298-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="73298-604">535.31</span><span class="sxs-lookup"><span data-stu-id="73298-604">535.31</span></span></td>
<td><span data-ttu-id="73298-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-606">Prod 2</span></span></td>
<td><span data-ttu-id="73298-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-607">Product 2</span></span></td>
<td><span data-ttu-id="73298-608">20</span><span class="sxs-lookup"><span data-stu-id="73298-608">20</span></span></td>
<td><span data-ttu-id="73298-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="73298-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="73298-610">178.44</span><span class="sxs-lookup"><span data-stu-id="73298-610">178.44</span></span></td>
<td><span data-ttu-id="73298-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-612">Prod 1</span></span></td>
<td><span data-ttu-id="73298-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-613">Product 1</span></span></td>
<td><span data-ttu-id="73298-614">60</span><span class="sxs-lookup"><span data-stu-id="73298-614">60</span></span></td>
<td><span data-ttu-id="73298-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="73298-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="73298-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="73298-616">4,487.12</span></span></td>
<td><span data-ttu-id="73298-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-618">Prod 2</span></span></td>
<td><span data-ttu-id="73298-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-619">Product 2</span></span></td>
<td><span data-ttu-id="73298-620">20</span><span class="sxs-lookup"><span data-stu-id="73298-620">20</span></span></td>
<td><span data-ttu-id="73298-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="73298-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="73298-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="73298-622">1,495.71</span></span></td>
<td><span data-ttu-id="73298-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="73298-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="73298-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-625">Cost object</span></span></th>
<th><span data-ttu-id="73298-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="73298-626">Magnitude</span></span></th>
<th><span data-ttu-id="73298-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="73298-627">Allocation factor</span></span></th>
<th><span data-ttu-id="73298-628">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-628">Amount</span></span></th>
<th><span data-ttu-id="73298-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-630">Prod 1</span></span></td>
<td><span data-ttu-id="73298-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-631">Product 1</span></span></td>
<td><span data-ttu-id="73298-632">80</span><span class="sxs-lookup"><span data-stu-id="73298-632">80</span></span></td>
<td><span data-ttu-id="73298-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="73298-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="73298-634">241.05</span><span class="sxs-lookup"><span data-stu-id="73298-634">241.05</span></span></td>
<td><span data-ttu-id="73298-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-636">Prod 2</span></span></td>
<td><span data-ttu-id="73298-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-637">Product 2</span></span></td>
<td><span data-ttu-id="73298-638">15</span><span class="sxs-lookup"><span data-stu-id="73298-638">15</span></span></td>
<td><span data-ttu-id="73298-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="73298-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="73298-640">45.20</span><span class="sxs-lookup"><span data-stu-id="73298-640">45.20</span></span></td>
<td><span data-ttu-id="73298-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-642">Prod 1</span></span></td>
<td><span data-ttu-id="73298-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-643">Product 1</span></span></td>
<td><span data-ttu-id="73298-644">80</span><span class="sxs-lookup"><span data-stu-id="73298-644">80</span></span></td>
<td><span data-ttu-id="73298-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="73298-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="73298-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="73298-646">2,507.09</span></span></td>
<td><span data-ttu-id="73298-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-648">Prod 2</span></span></td>
<td><span data-ttu-id="73298-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-649">Product 2</span></span></td>
<td><span data-ttu-id="73298-650">15</span><span class="sxs-lookup"><span data-stu-id="73298-650">15</span></span></td>
<td><span data-ttu-id="73298-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="73298-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="73298-652">470.08</span><span class="sxs-lookup"><span data-stu-id="73298-652">470.08</span></span></td>
<td><span data-ttu-id="73298-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="73298-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="73298-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-655">Journal</span></span></th>
<th><span data-ttu-id="73298-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="73298-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="73298-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="73298-658">Versija</span><span class="sxs-lookup"><span data-stu-id="73298-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-659">00004</span><span class="sxs-lookup"><span data-stu-id="73298-659">00004</span></span></td>
<td><span data-ttu-id="73298-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="73298-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="73298-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="73298-661">Fiscal</span></span></td>
<td><span data-ttu-id="73298-662">2017</span><span class="sxs-lookup"><span data-stu-id="73298-662">2017</span></span></td>
<td><span data-ttu-id="73298-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-663">Period 1</span></span></td>
<td><span data-ttu-id="73298-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="73298-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="73298-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="73298-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="73298-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="73298-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-668">Cost element</span></span></th>
<th><span data-ttu-id="73298-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-669">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-670">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-672">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-672">CC001</span></span></td>
<td><span data-ttu-id="73298-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-673">HR</span></span></td>
<td><span data-ttu-id="73298-674">10001</span><span class="sxs-lookup"><span data-stu-id="73298-674">10001</span></span></td>
<td><span data-ttu-id="73298-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-675">Electricity</span></span></td>
<td><span data-ttu-id="73298-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-676">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-677">500,00</span><span class="sxs-lookup"><span data-stu-id="73298-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-679">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-679">CC001</span></span></td>
<td><span data-ttu-id="73298-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-680">HR</span></span></td>
<td><span data-ttu-id="73298-681">10001</span><span class="sxs-lookup"><span data-stu-id="73298-681">10001</span></span></td>
<td><span data-ttu-id="73298-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-682">Electricity</span></span></td>
<td><span data-ttu-id="73298-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-683">Variable cost</span></span></td>
<td><span data-ttu-id="73298-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="73298-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-686">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-686">CC002</span></span></td>
<td><span data-ttu-id="73298-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-687">Finance</span></span></td>
<td><span data-ttu-id="73298-688">10001</span><span class="sxs-lookup"><span data-stu-id="73298-688">10001</span></span></td>
<td><span data-ttu-id="73298-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-689">Electricity</span></span></td>
<td><span data-ttu-id="73298-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-690">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-691">675.00</span><span class="sxs-lookup"><span data-stu-id="73298-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-693">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-693">CC002</span></span></td>
<td><span data-ttu-id="73298-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-694">Finance</span></span></td>
<td><span data-ttu-id="73298-695">10001</span><span class="sxs-lookup"><span data-stu-id="73298-695">10001</span></span></td>
<td><span data-ttu-id="73298-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-696">Electricity</span></span></td>
<td><span data-ttu-id="73298-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-697">Variable cost</span></span></td>
<td><span data-ttu-id="73298-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="73298-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-700">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-700">CC003</span></span></td>
<td><span data-ttu-id="73298-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-701">Assembly</span></span></td>
<td><span data-ttu-id="73298-702">10001</span><span class="sxs-lookup"><span data-stu-id="73298-702">10001</span></span></td>
<td><span data-ttu-id="73298-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-703">Electricity</span></span></td>
<td><span data-ttu-id="73298-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-704">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-705">713.75</span><span class="sxs-lookup"><span data-stu-id="73298-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-707">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-707">CC003</span></span></td>
<td><span data-ttu-id="73298-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-708">Assembly</span></span></td>
<td><span data-ttu-id="73298-709">10001</span><span class="sxs-lookup"><span data-stu-id="73298-709">10001</span></span></td>
<td><span data-ttu-id="73298-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-710">Electricity</span></span></td>
<td><span data-ttu-id="73298-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-711">Variable cost</span></span></td>
<td><span data-ttu-id="73298-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="73298-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-714">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-714">CC003</span></span></td>
<td><span data-ttu-id="73298-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-715">Packaging</span></span></td>
<td><span data-ttu-id="73298-716">10001</span><span class="sxs-lookup"><span data-stu-id="73298-716">10001</span></span></td>
<td><span data-ttu-id="73298-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-717">Electricity</span></span></td>
<td><span data-ttu-id="73298-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-718">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-719">286.25</span><span class="sxs-lookup"><span data-stu-id="73298-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-721">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-721">CC003</span></span></td>
<td><span data-ttu-id="73298-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-722">Packaging</span></span></td>
<td><span data-ttu-id="73298-723">10001</span><span class="sxs-lookup"><span data-stu-id="73298-723">10001</span></span></td>
<td><span data-ttu-id="73298-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-724">Electricity</span></span></td>
<td><span data-ttu-id="73298-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-725">Variable cost</span></span></td>
<td><span data-ttu-id="73298-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="73298-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-728">Prod 1</span></span></td>
<td><span data-ttu-id="73298-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-729">Product 1</span></span></td>
<td><span data-ttu-id="73298-730">10001</span><span class="sxs-lookup"><span data-stu-id="73298-730">10001</span></span></td>
<td><span data-ttu-id="73298-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-731">Electricity</span></span></td>
<td><span data-ttu-id="73298-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-732">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-733">776.36</span><span class="sxs-lookup"><span data-stu-id="73298-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-735">Prod 1</span></span></td>
<td><span data-ttu-id="73298-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-736">Product 1</span></span></td>
<td><span data-ttu-id="73298-737">10001</span><span class="sxs-lookup"><span data-stu-id="73298-737">10001</span></span></td>
<td><span data-ttu-id="73298-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-738">Electricity</span></span></td>
<td><span data-ttu-id="73298-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-739">Variable cost</span></span></td>
<td><span data-ttu-id="73298-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="73298-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-742">Prod 2</span></span></td>
<td><span data-ttu-id="73298-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-743">Product 1</span></span></td>
<td><span data-ttu-id="73298-744">10001</span><span class="sxs-lookup"><span data-stu-id="73298-744">10001</span></span></td>
<td><span data-ttu-id="73298-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-745">Electricity</span></span></td>
<td><span data-ttu-id="73298-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-746">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-747">223.64</span><span class="sxs-lookup"><span data-stu-id="73298-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="73298-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-749">Prod 2</span></span></td>
<td><span data-ttu-id="73298-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-750">Product 1</span></span></td>
<td><span data-ttu-id="73298-751">10001</span><span class="sxs-lookup"><span data-stu-id="73298-751">10001</span></span></td>
<td><span data-ttu-id="73298-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-752">Electricity</span></span></td>
<td><span data-ttu-id="73298-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-753">Variable cost</span></span></td>
<td><span data-ttu-id="73298-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="73298-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="73298-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="73298-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="73298-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="73298-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-757">Cost element</span></span></th>
<th><span data-ttu-id="73298-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="73298-758">Cost behavior</span></span></th>
<th><span data-ttu-id="73298-759">Suma</span><span class="sxs-lookup"><span data-stu-id="73298-759">Amount</span></span></th>
<th><span data-ttu-id="73298-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="73298-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73298-761">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-761">CC001</span></span></td>
<td><span data-ttu-id="73298-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-762">HR</span></span></td>
<td><span data-ttu-id="73298-763">10001</span><span class="sxs-lookup"><span data-stu-id="73298-763">10001</span></span></td>
<td><span data-ttu-id="73298-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-764">Electricity</span></span></td>
<td><span data-ttu-id="73298-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-765">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="73298-766">-500.00</span></span></td>
<td><span data-ttu-id="73298-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-768">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-768">CC002</span></span></td>
<td><span data-ttu-id="73298-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-769">Finance</span></span></td>
<td><span data-ttu-id="73298-770">10001</span><span class="sxs-lookup"><span data-stu-id="73298-770">10001</span></span></td>
<td><span data-ttu-id="73298-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-771">Electricity</span></span></td>
<td><span data-ttu-id="73298-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-772">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-773">175.00</span><span class="sxs-lookup"><span data-stu-id="73298-773">175.00</span></span></td>
<td><span data-ttu-id="73298-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-775">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-775">CC003</span></span></td>
<td><span data-ttu-id="73298-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-776">Assembly</span></span></td>
<td><span data-ttu-id="73298-777">10001</span><span class="sxs-lookup"><span data-stu-id="73298-777">10001</span></span></td>
<td><span data-ttu-id="73298-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-778">Electricity</span></span></td>
<td><span data-ttu-id="73298-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-779">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-780">275.00</span><span class="sxs-lookup"><span data-stu-id="73298-780">275.00</span></span></td>
<td><span data-ttu-id="73298-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-782">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-782">CC004</span></span></td>
<td><span data-ttu-id="73298-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-783">Packaging</span></span></td>
<td><span data-ttu-id="73298-784">10001</span><span class="sxs-lookup"><span data-stu-id="73298-784">10001</span></span></td>
<td><span data-ttu-id="73298-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-785">Electricity</span></span></td>
<td><span data-ttu-id="73298-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-786">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-787">50,00</span><span class="sxs-lookup"><span data-stu-id="73298-787">50,00</span></span></td>
<td><span data-ttu-id="73298-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-789">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-789">CC001</span></span></td>
<td><span data-ttu-id="73298-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="73298-790">HR</span></span></td>
<td><span data-ttu-id="73298-791">10001</span><span class="sxs-lookup"><span data-stu-id="73298-791">10001</span></span></td>
<td><span data-ttu-id="73298-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-792">Electricity</span></span></td>
<td><span data-ttu-id="73298-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-793">Variable cost</span></span></td>
<td><span data-ttu-id="73298-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="73298-794">-1,245.71</span></span></td>
<td><span data-ttu-id="73298-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-796">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-796">CC002</span></span></td>
<td><span data-ttu-id="73298-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-797">Finance</span></span></td>
<td><span data-ttu-id="73298-798">10001</span><span class="sxs-lookup"><span data-stu-id="73298-798">10001</span></span></td>
<td><span data-ttu-id="73298-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-799">Electricity</span></span></td>
<td><span data-ttu-id="73298-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-800">Variable cost</span></span></td>
<td><span data-ttu-id="73298-801">436.00</span><span class="sxs-lookup"><span data-stu-id="73298-801">436.00</span></span></td>
<td><span data-ttu-id="73298-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-803">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-803">CC003</span></span></td>
<td><span data-ttu-id="73298-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-804">Assembly</span></span></td>
<td><span data-ttu-id="73298-805">10001</span><span class="sxs-lookup"><span data-stu-id="73298-805">10001</span></span></td>
<td><span data-ttu-id="73298-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-806">Electricity</span></span></td>
<td><span data-ttu-id="73298-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-807">Variable cost</span></span></td>
<td><span data-ttu-id="73298-808">685.14</span><span class="sxs-lookup"><span data-stu-id="73298-808">685.14</span></span></td>
<td><span data-ttu-id="73298-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-810">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-810">CC004</span></span></td>
<td><span data-ttu-id="73298-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-811">Packaging</span></span></td>
<td><span data-ttu-id="73298-812">10001</span><span class="sxs-lookup"><span data-stu-id="73298-812">10001</span></span></td>
<td><span data-ttu-id="73298-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-813">Electricity</span></span></td>
<td><span data-ttu-id="73298-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-814">Variable cost</span></span></td>
<td><span data-ttu-id="73298-815">124.57</span><span class="sxs-lookup"><span data-stu-id="73298-815">124.57</span></span></td>
<td><span data-ttu-id="73298-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-817">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-817">CC002</span></span></td>
<td><span data-ttu-id="73298-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-818">Finance</span></span></td>
<td><span data-ttu-id="73298-819">10001</span><span class="sxs-lookup"><span data-stu-id="73298-819">10001</span></span></td>
<td><span data-ttu-id="73298-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-820">Electricity</span></span></td>
<td><span data-ttu-id="73298-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-821">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="73298-822">-675.00</span></span></td>
<td><span data-ttu-id="73298-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-824">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-824">CC003</span></span></td>
<td><span data-ttu-id="73298-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-825">Assembly</span></span></td>
<td><span data-ttu-id="73298-826">10001</span><span class="sxs-lookup"><span data-stu-id="73298-826">10001</span></span></td>
<td><span data-ttu-id="73298-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-827">Electricity</span></span></td>
<td><span data-ttu-id="73298-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-828">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-829">438.75</span><span class="sxs-lookup"><span data-stu-id="73298-829">438.75</span></span></td>
<td><span data-ttu-id="73298-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-831">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-831">CC004</span></span></td>
<td><span data-ttu-id="73298-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-832">Packaging</span></span></td>
<td><span data-ttu-id="73298-833">10001</span><span class="sxs-lookup"><span data-stu-id="73298-833">10001</span></span></td>
<td><span data-ttu-id="73298-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-834">Electricity</span></span></td>
<td><span data-ttu-id="73298-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-835">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-836">236.25</span><span class="sxs-lookup"><span data-stu-id="73298-836">236.25</span></span></td>
<td><span data-ttu-id="73298-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-838">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-838">CC002</span></span></td>
<td><span data-ttu-id="73298-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="73298-839">Finance</span></span></td>
<td><span data-ttu-id="73298-840">10001</span><span class="sxs-lookup"><span data-stu-id="73298-840">10001</span></span></td>
<td><span data-ttu-id="73298-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-841">Electricity</span></span></td>
<td><span data-ttu-id="73298-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-842">Variable cost</span></span></td>
<td><span data-ttu-id="73298-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="73298-843">-8,150.29</span></span></td>
<td><span data-ttu-id="73298-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-845">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-845">CC003</span></span></td>
<td><span data-ttu-id="73298-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-846">Assembly</span></span></td>
<td><span data-ttu-id="73298-847">10001</span><span class="sxs-lookup"><span data-stu-id="73298-847">10001</span></span></td>
<td><span data-ttu-id="73298-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-848">Electricity</span></span></td>
<td><span data-ttu-id="73298-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-849">Variable cost</span></span></td>
<td><span data-ttu-id="73298-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="73298-850">5,297.69</span></span></td>
<td><span data-ttu-id="73298-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-852">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-852">CC004</span></span></td>
<td><span data-ttu-id="73298-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="73298-853">Packaging</span></span></td>
<td><span data-ttu-id="73298-854">10001</span><span class="sxs-lookup"><span data-stu-id="73298-854">10001</span></span></td>
<td><span data-ttu-id="73298-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-855">Electricity</span></span></td>
<td><span data-ttu-id="73298-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-856">Variable cost</span></span></td>
<td><span data-ttu-id="73298-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="73298-857">2,852.60</span></span></td>
<td><span data-ttu-id="73298-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-859">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-859">CC003</span></span></td>
<td><span data-ttu-id="73298-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-860">Assembly</span></span></td>
<td><span data-ttu-id="73298-861">10001</span><span class="sxs-lookup"><span data-stu-id="73298-861">10001</span></span></td>
<td><span data-ttu-id="73298-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-862">Electricity</span></span></td>
<td><span data-ttu-id="73298-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-863">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="73298-864">-713.75</span></span></td>
<td><span data-ttu-id="73298-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-866">Prod 1</span></span></td>
<td><span data-ttu-id="73298-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-867">Product 1</span></span></td>
<td><span data-ttu-id="73298-868">10001</span><span class="sxs-lookup"><span data-stu-id="73298-868">10001</span></span></td>
<td><span data-ttu-id="73298-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-869">Electricity</span></span></td>
<td><span data-ttu-id="73298-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-870">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-871">535.31</span><span class="sxs-lookup"><span data-stu-id="73298-871">535.31</span></span></td>
<td><span data-ttu-id="73298-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-873">Prod 2</span></span></td>
<td><span data-ttu-id="73298-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-874">Product 2</span></span></td>
<td><span data-ttu-id="73298-875">10001</span><span class="sxs-lookup"><span data-stu-id="73298-875">10001</span></span></td>
<td><span data-ttu-id="73298-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-876">Electricity</span></span></td>
<td><span data-ttu-id="73298-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-877">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-878">178.44</span><span class="sxs-lookup"><span data-stu-id="73298-878">178.44</span></span></td>
<td><span data-ttu-id="73298-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-880">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-880">CC003</span></span></td>
<td><span data-ttu-id="73298-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-881">Assembly</span></span></td>
<td><span data-ttu-id="73298-882">10001</span><span class="sxs-lookup"><span data-stu-id="73298-882">10001</span></span></td>
<td><span data-ttu-id="73298-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-883">Electricity</span></span></td>
<td><span data-ttu-id="73298-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-884">Variable cost</span></span></td>
<td><span data-ttu-id="73298-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="73298-885">-5,982.83</span></span></td>
<td><span data-ttu-id="73298-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-887">Prod 1</span></span></td>
<td><span data-ttu-id="73298-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-888">Product 1</span></span></td>
<td><span data-ttu-id="73298-889">10001</span><span class="sxs-lookup"><span data-stu-id="73298-889">10001</span></span></td>
<td><span data-ttu-id="73298-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-890">Electricity</span></span></td>
<td><span data-ttu-id="73298-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-891">Variable cost</span></span></td>
<td><span data-ttu-id="73298-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="73298-892">4,487.12</span></span></td>
<td><span data-ttu-id="73298-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-894">Prod 2</span></span></td>
<td><span data-ttu-id="73298-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-895">Product 2</span></span></td>
<td><span data-ttu-id="73298-896">10001</span><span class="sxs-lookup"><span data-stu-id="73298-896">10001</span></span></td>
<td><span data-ttu-id="73298-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-897">Electricity</span></span></td>
<td><span data-ttu-id="73298-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-898">Variable cost</span></span></td>
<td><span data-ttu-id="73298-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="73298-899">1,495.71</span></span></td>
<td><span data-ttu-id="73298-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-901">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-901">CC003</span></span></td>
<td><span data-ttu-id="73298-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-902">Assembly</span></span></td>
<td><span data-ttu-id="73298-903">10001</span><span class="sxs-lookup"><span data-stu-id="73298-903">10001</span></span></td>
<td><span data-ttu-id="73298-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-904">Electricity</span></span></td>
<td><span data-ttu-id="73298-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-905">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="73298-906">-286.25</span></span></td>
<td><span data-ttu-id="73298-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-908">Prod 1</span></span></td>
<td><span data-ttu-id="73298-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-909">Product 1</span></span></td>
<td><span data-ttu-id="73298-910">10001</span><span class="sxs-lookup"><span data-stu-id="73298-910">10001</span></span></td>
<td><span data-ttu-id="73298-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-911">Electricity</span></span></td>
<td><span data-ttu-id="73298-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-912">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-913">241.05</span><span class="sxs-lookup"><span data-stu-id="73298-913">241.05</span></span></td>
<td><span data-ttu-id="73298-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-915">Prod 2</span></span></td>
<td><span data-ttu-id="73298-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-916">Product 2</span></span></td>
<td><span data-ttu-id="73298-917">10001</span><span class="sxs-lookup"><span data-stu-id="73298-917">10001</span></span></td>
<td><span data-ttu-id="73298-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-918">Electricity</span></span></td>
<td><span data-ttu-id="73298-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-919">Fixed cost</span></span></td>
<td><span data-ttu-id="73298-920">45.20</span><span class="sxs-lookup"><span data-stu-id="73298-920">45.20</span></span></td>
<td><span data-ttu-id="73298-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-922">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-922">CC003</span></span></td>
<td><span data-ttu-id="73298-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="73298-923">Assembly</span></span></td>
<td><span data-ttu-id="73298-924">10001</span><span class="sxs-lookup"><span data-stu-id="73298-924">10001</span></span></td>
<td><span data-ttu-id="73298-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-925">Electricity</span></span></td>
<td><span data-ttu-id="73298-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-926">Variable cost</span></span></td>
<td><span data-ttu-id="73298-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="73298-927">-2,977.17</span></span></td>
<td><span data-ttu-id="73298-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-929">Prod 1</span></span></td>
<td><span data-ttu-id="73298-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-930">Product 1</span></span></td>
<td><span data-ttu-id="73298-931">10001</span><span class="sxs-lookup"><span data-stu-id="73298-931">10001</span></span></td>
<td><span data-ttu-id="73298-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-932">Electricity</span></span></td>
<td><span data-ttu-id="73298-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-933">Variable cost</span></span></td>
<td><span data-ttu-id="73298-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="73298-934">2,507.09</span></span></td>
<td><span data-ttu-id="73298-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73298-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-936">Prod 2</span></span></td>
<td><span data-ttu-id="73298-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="73298-937">Product 2</span></span></td>
<td><span data-ttu-id="73298-938">10001</span><span class="sxs-lookup"><span data-stu-id="73298-938">10001</span></span></td>
<td><span data-ttu-id="73298-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-939">Electricity</span></span></td>
<td><span data-ttu-id="73298-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-940">Variable cost</span></span></td>
<td><span data-ttu-id="73298-941">470.08</span><span class="sxs-lookup"><span data-stu-id="73298-941">470.08</span></span></td>
<td><span data-ttu-id="73298-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="73298-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="73298-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="73298-943">Conclusion</span></span>
<span data-ttu-id="73298-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="73298-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="73298-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="73298-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="73298-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="73298-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="73298-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="73298-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="73298-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="73298-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="73298-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="73298-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="73298-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="73298-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73298-951">CC099</span><span class="sxs-lookup"><span data-stu-id="73298-951">CC099</span></span></th>
<th><span data-ttu-id="73298-952">CC001</span><span class="sxs-lookup"><span data-stu-id="73298-952">CC001</span></span></th>
<th><span data-ttu-id="73298-953">CC002</span><span class="sxs-lookup"><span data-stu-id="73298-953">CC002</span></span></th>
<th><span data-ttu-id="73298-954">CC003</span><span class="sxs-lookup"><span data-stu-id="73298-954">CC003</span></span></th>
<th><span data-ttu-id="73298-955">CC004</span><span class="sxs-lookup"><span data-stu-id="73298-955">CC004</span></span></th>
<th><span data-ttu-id="73298-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-956">Proj 1</span></span></th>
<th><span data-ttu-id="73298-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="73298-957">Proj 2</span></span></th>
<th><span data-ttu-id="73298-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-958">Prod 1</span></span></th>
<th><span data-ttu-id="73298-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="73298-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="73298-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="73298-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="73298-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="73298-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="73298-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="73298-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="73298-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-971">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="73298-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-973">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-974">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-975">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-976">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-977">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="73298-978">776.36</span><span class="sxs-lookup"><span data-stu-id="73298-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-979">223.64</span><span class="sxs-lookup"><span data-stu-id="73298-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="73298-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="73298-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-982">000</span><span class="sxs-lookup"><span data-stu-id="73298-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-983">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-984">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-985">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-986">0,00</span><span class="sxs-lookup"><span data-stu-id="73298-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-987">30,00</span><span class="sxs-lookup"><span data-stu-id="73298-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-988">10,00</span><span class="sxs-lookup"><span data-stu-id="73298-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="73298-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="73298-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="73298-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="73298-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="73298-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="73298-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="73298-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="73298-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="73298-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="73298-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="73298-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="73298-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="73298-996">Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="73298-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



