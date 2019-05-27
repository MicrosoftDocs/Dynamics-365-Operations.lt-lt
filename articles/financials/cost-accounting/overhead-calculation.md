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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544060"
---
# <a name="overhead-calculation"></a><span data-ttu-id="db2f3-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db2f3-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="db2f3-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="db2f3-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="db2f3-105">Term definition</span></span>
---------------

<span data-ttu-id="db2f3-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="db2f3-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="db2f3-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="db2f3-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="db2f3-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="db2f3-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="db2f3-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="db2f3-109">Rent</span></span>
-   <span data-ttu-id="db2f3-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-110">Electricity</span></span>
-   <span data-ttu-id="db2f3-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="db2f3-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="db2f3-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="db2f3-112">Overhead calculation overview</span></span>
<span data-ttu-id="db2f3-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="db2f3-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="db2f3-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="db2f3-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="db2f3-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="db2f3-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="db2f3-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="db2f3-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="db2f3-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="db2f3-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="db2f3-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="db2f3-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="db2f3-119">Version type</span></span>
-   <span data-ttu-id="db2f3-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="db2f3-120">Date and time</span></span>
-   <span data-ttu-id="db2f3-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="db2f3-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="db2f3-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="db2f3-122">Fiscal year</span></span>
-   <span data-ttu-id="db2f3-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-123">Fiscal period</span></span>

<span data-ttu-id="db2f3-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="db2f3-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="db2f3-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="db2f3-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="db2f3-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="db2f3-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="db2f3-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="db2f3-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="db2f3-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="db2f3-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="db2f3-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="db2f3-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="db2f3-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="db2f3-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="db2f3-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="db2f3-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="db2f3-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="db2f3-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="db2f3-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="db2f3-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="db2f3-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="db2f3-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="db2f3-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="db2f3-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="db2f3-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="db2f3-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="db2f3-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="db2f3-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="db2f3-140">Main account</span></span></th>
<th><span data-ttu-id="db2f3-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="db2f3-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="db2f3-143">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-143">CC099</span></span></td>
<td><span data-ttu-id="db2f3-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-144">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-145">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-145">10001</span></span></td>
<td><span data-ttu-id="db2f3-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-146">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="db2f3-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="db2f3-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="db2f3-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="db2f3-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="db2f3-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="db2f3-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="db2f3-151">Define the cost behavior rule</span></span>

<span data-ttu-id="db2f3-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="db2f3-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="db2f3-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="db2f3-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="db2f3-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="db2f3-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="db2f3-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="db2f3-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="db2f3-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="db2f3-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="db2f3-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="db2f3-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="db2f3-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-160">Journal</span></span></th>
<th><span data-ttu-id="db2f3-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="db2f3-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="db2f3-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="db2f3-163">Versija</span><span class="sxs-lookup"><span data-stu-id="db2f3-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-164">00001</span><span class="sxs-lookup"><span data-stu-id="db2f3-164">00001</span></span></td>
<td><span data-ttu-id="db2f3-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="db2f3-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="db2f3-166">Fiscal</span></span></td>
<td><span data-ttu-id="db2f3-167">2017</span><span class="sxs-lookup"><span data-stu-id="db2f3-167">2017</span></span></td>
<td><span data-ttu-id="db2f3-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-168">Period 1</span></span></td>
<td><span data-ttu-id="db2f3-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="db2f3-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="db2f3-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-173">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-174">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-175">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="db2f3-177">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-177">CC099</span></span></td>
<td><span data-ttu-id="db2f3-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-178">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-179">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-179">10001</span></span></td>
<td><span data-ttu-id="db2f3-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-180">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="db2f3-181">Unclassified</span></span></td>
<td><span data-ttu-id="db2f3-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="db2f3-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="db2f3-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-185">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-186">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-187">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-187">Amount</span></span></th>
<th><span data-ttu-id="db2f3-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-189">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-189">CC099</span></span></td>
<td><span data-ttu-id="db2f3-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-190">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-191">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-191">10001</span></span></td>
<td><span data-ttu-id="db2f3-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-192">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="db2f3-193">Unclassified</span></span></td>
<td><span data-ttu-id="db2f3-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-194">10,000.00</span></span></td>
<td><span data-ttu-id="db2f3-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-196">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-196">CC099</span></span></td>
<td><span data-ttu-id="db2f3-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-197">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-198">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-198">10001</span></span></td>
<td><span data-ttu-id="db2f3-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-199">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="db2f3-200">Unclassified</span></span></td>
<td><span data-ttu-id="db2f3-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-201">-10,000.00</span></span></td>
<td><span data-ttu-id="db2f3-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-203">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-203">CC099</span></span></td>
<td><span data-ttu-id="db2f3-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-204">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-205">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-205">10001</span></span></td>
<td><span data-ttu-id="db2f3-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-206">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-207">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-208">1,000.00</span></span></td>
<td><span data-ttu-id="db2f3-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-210">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-210">CC099</span></span></td>
<td><span data-ttu-id="db2f3-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-211">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-212">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-212">10001</span></span></td>
<td><span data-ttu-id="db2f3-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-213">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-214">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-215">9,000.00</span></span></td>
<td><span data-ttu-id="db2f3-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="db2f3-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="db2f3-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="db2f3-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="db2f3-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="db2f3-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="db2f3-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="db2f3-221">Define the cost distribution rule</span></span>

<span data-ttu-id="db2f3-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="db2f3-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="db2f3-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="db2f3-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="db2f3-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="db2f3-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="db2f3-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="db2f3-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="db2f3-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="db2f3-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="db2f3-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="db2f3-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-228">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="db2f3-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-230">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-230">CC001</span></span></td>
<td><span data-ttu-id="db2f3-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-231">HR</span></span></td>
<td><span data-ttu-id="db2f3-232">1000</span><span class="sxs-lookup"><span data-stu-id="db2f3-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-233">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-233">CC002</span></span></td>
<td><span data-ttu-id="db2f3-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-234">Finance</span></span></td>
<td><span data-ttu-id="db2f3-235">6,000</span><span class="sxs-lookup"><span data-stu-id="db2f3-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-236">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-236">CC003</span></span></td>
<td><span data-ttu-id="db2f3-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-237">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-238">0</span><span class="sxs-lookup"><span data-stu-id="db2f3-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-240">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-241">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-242">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-243">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-244">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-244">CC001</span></span></td>
<td><span data-ttu-id="db2f3-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-245">HR</span></span></td>
<td><span data-ttu-id="db2f3-246">1000</span><span class="sxs-lookup"><span data-stu-id="db2f3-246">1,000</span></span></td>
<td><span data-ttu-id="db2f3-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="db2f3-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-249">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-249">CC002</span></span></td>
<td><span data-ttu-id="db2f3-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-250">Finance</span></span></td>
<td><span data-ttu-id="db2f3-251">6,000</span><span class="sxs-lookup"><span data-stu-id="db2f3-251">6,000</span></span></td>
<td><span data-ttu-id="db2f3-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="db2f3-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="db2f3-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-254">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-254">CC003</span></span></td>
<td><span data-ttu-id="db2f3-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-255">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-256">0</span><span class="sxs-lookup"><span data-stu-id="db2f3-256">0</span></span></td>
<td><span data-ttu-id="db2f3-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="db2f3-258">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="db2f3-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-261">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="db2f3-262">Formula</span></span></th>
<th><span data-ttu-id="db2f3-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-263">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-264">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-265">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-266">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-266">CC001</span></span></td>
<td><span data-ttu-id="db2f3-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-267">HR</span></span></td>
<td><span data-ttu-id="db2f3-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="db2f3-269">1</span><span class="sxs-lookup"><span data-stu-id="db2f3-269">1</span></span></td>
<td><span data-ttu-id="db2f3-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="db2f3-271">500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-272">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-272">CC002</span></span></td>
<td><span data-ttu-id="db2f3-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-273">Finance</span></span></td>
<td><span data-ttu-id="db2f3-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="db2f3-275">1</span><span class="sxs-lookup"><span data-stu-id="db2f3-275">1</span></span></td>
<td><span data-ttu-id="db2f3-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="db2f3-277">500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-278">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-278">CC003</span></span></td>
<td><span data-ttu-id="db2f3-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-279">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="db2f3-281">0</span><span class="sxs-lookup"><span data-stu-id="db2f3-281">0</span></span></td>
<td><span data-ttu-id="db2f3-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="db2f3-283">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="db2f3-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-285">Journal</span></span></th>
<th><span data-ttu-id="db2f3-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="db2f3-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="db2f3-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="db2f3-288">Versija</span><span class="sxs-lookup"><span data-stu-id="db2f3-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-289">00002</span><span class="sxs-lookup"><span data-stu-id="db2f3-289">00002</span></span></td>
<td><span data-ttu-id="db2f3-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="db2f3-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="db2f3-291">Fiscal</span></span></td>
<td><span data-ttu-id="db2f3-292">2017</span><span class="sxs-lookup"><span data-stu-id="db2f3-292">2017</span></span></td>
<td><span data-ttu-id="db2f3-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-293">Period 1</span></span></td>
<td><span data-ttu-id="db2f3-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="db2f3-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="db2f3-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-298">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-299">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-300">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-302">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-302">CC099</span></span></td>
<td><span data-ttu-id="db2f3-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-303">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-304">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-304">10001</span></span></td>
<td><span data-ttu-id="db2f3-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-305">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-306">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-309">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-309">CC099</span></span></td>
<td><span data-ttu-id="db2f3-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-310">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-311">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-311">10001</span></span></td>
<td><span data-ttu-id="db2f3-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-312">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-313">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="db2f3-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="db2f3-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-317">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-318">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-319">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-319">Amount</span></span></th>
<th><span data-ttu-id="db2f3-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-321">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-321">CC099</span></span></td>
<td><span data-ttu-id="db2f3-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-322">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-323">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-323">10001</span></span></td>
<td><span data-ttu-id="db2f3-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-324">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-325">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-326">-1,000.00</span></span></td>
<td><span data-ttu-id="db2f3-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-328">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-328">CC001</span></span></td>
<td><span data-ttu-id="db2f3-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-329">HR</span></span></td>
<td><span data-ttu-id="db2f3-330">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-330">10001</span></span></td>
<td><span data-ttu-id="db2f3-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-331">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-332">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-333">500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-333">500.00</span></span></td>
<td><span data-ttu-id="db2f3-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-335">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-335">CC002</span></span></td>
<td><span data-ttu-id="db2f3-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-336">Finance</span></span></td>
<td><span data-ttu-id="db2f3-337">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-337">10001</span></span></td>
<td><span data-ttu-id="db2f3-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-338">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-339">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-340">500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-340">500.00</span></span></td>
<td><span data-ttu-id="db2f3-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-342">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-342">CC099</span></span></td>
<td><span data-ttu-id="db2f3-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="db2f3-343">Default cost center</span></span></td>
<td><span data-ttu-id="db2f3-344">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-344">10001</span></span></td>
<td><span data-ttu-id="db2f3-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-345">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-346">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-347">-9,000.00</span></span></td>
<td><span data-ttu-id="db2f3-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-349">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-349">CC001</span></span></td>
<td><span data-ttu-id="db2f3-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-350">HR</span></span></td>
<td><span data-ttu-id="db2f3-351">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-351">10001</span></span></td>
<td><span data-ttu-id="db2f3-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-352">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-353">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-354">1,285.71</span></span></td>
<td><span data-ttu-id="db2f3-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-356">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-356">CC002</span></span></td>
<td><span data-ttu-id="db2f3-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-357">Finance</span></span></td>
<td><span data-ttu-id="db2f3-358">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-358">10001</span></span></td>
<td><span data-ttu-id="db2f3-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-359">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-360">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="db2f3-361">7,714.29</span></span></td>
<td><span data-ttu-id="db2f3-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="db2f3-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="db2f3-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="db2f3-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="db2f3-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="db2f3-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="db2f3-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="db2f3-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db2f3-367">Define the overhead rate</span></span>

<span data-ttu-id="db2f3-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="db2f3-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-370">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="db2f3-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-372">Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-373">Project 1</span></span></td>
<td><span data-ttu-id="db2f3-374">3</span><span class="sxs-lookup"><span data-stu-id="db2f3-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-375">Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-376">Project 2</span></span></td>
<td><span data-ttu-id="db2f3-377">1</span><span class="sxs-lookup"><span data-stu-id="db2f3-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="db2f3-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-379">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-380">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-381">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="db2f3-382">Units</span></span></th>
<th><span data-ttu-id="db2f3-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="db2f3-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-384">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-384">CC001</span></span></td>
<td><span data-ttu-id="db2f3-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-385">HR</span></span></td>
<td><span data-ttu-id="db2f3-386">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-386">10001</span></span></td>
<td><span data-ttu-id="db2f3-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-387">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-388">1</span><span class="sxs-lookup"><span data-stu-id="db2f3-388">1</span></span></td>
<td><span data-ttu-id="db2f3-389">10</span><span class="sxs-lookup"><span data-stu-id="db2f3-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-391">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-392">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-393">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-394">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-395">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-396">Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-397">Project 1</span></span></td>
<td><span data-ttu-id="db2f3-398">3</span><span class="sxs-lookup"><span data-stu-id="db2f3-398">3</span></span></td>
<td><span data-ttu-id="db2f3-399">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-399">10001</span></span></td>
<td><span data-ttu-id="db2f3-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="db2f3-401">30,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-402">Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-403">Project 2</span></span></td>
<td><span data-ttu-id="db2f3-404">1</span><span class="sxs-lookup"><span data-stu-id="db2f3-404">1</span></span></td>
<td><span data-ttu-id="db2f3-405">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-405">10001</span></span></td>
<td><span data-ttu-id="db2f3-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="db2f3-407">10,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="db2f3-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-409">Journal</span></span></th>
<th><span data-ttu-id="db2f3-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="db2f3-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="db2f3-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="db2f3-412">Versija</span><span class="sxs-lookup"><span data-stu-id="db2f3-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-413">00003</span><span class="sxs-lookup"><span data-stu-id="db2f3-413">00003</span></span></td>
<td><span data-ttu-id="db2f3-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="db2f3-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="db2f3-415">Fiscal</span></span></td>
<td><span data-ttu-id="db2f3-416">2017</span><span class="sxs-lookup"><span data-stu-id="db2f3-416">2017</span></span></td>
<td><span data-ttu-id="db2f3-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-417">Period 1</span></span></td>
<td><span data-ttu-id="db2f3-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="db2f3-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="db2f3-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-421">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-424">Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-426">3,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-428">Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-430">1,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="db2f3-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="db2f3-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-433">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-434">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-435">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-435">Amount</span></span></th>
<th><span data-ttu-id="db2f3-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="db2f3-437">CC0001</span></span></td>
<td><span data-ttu-id="db2f3-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-438">HR</span></span></td>
<td><span data-ttu-id="db2f3-439">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-439">10001</span></span></td>
<td><span data-ttu-id="db2f3-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-440">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-441">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-442">-30.00</span></span></td>
<td><span data-ttu-id="db2f3-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-444">Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="db2f3-446">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-446">10001</span></span></td>
<td><span data-ttu-id="db2f3-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-447">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-448">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-449">30,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-449">30.00</span></span></td>
<td><span data-ttu-id="db2f3-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-451">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-451">CC001</span></span></td>
<td><span data-ttu-id="db2f3-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-452">HR</span></span></td>
<td><span data-ttu-id="db2f3-453">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-453">10001</span></span></td>
<td><span data-ttu-id="db2f3-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-454">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-455">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-456">-10.00</span></span></td>
<td><span data-ttu-id="db2f3-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-458">Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="db2f3-460">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-460">10001</span></span></td>
<td><span data-ttu-id="db2f3-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-461">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-462">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-463">10,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-463">10.00</span></span></td>
<td><span data-ttu-id="db2f3-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="db2f3-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="db2f3-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="db2f3-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="db2f3-468">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="db2f3-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="db2f3-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="db2f3-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="db2f3-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="db2f3-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="db2f3-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="db2f3-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="db2f3-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="db2f3-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="db2f3-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="db2f3-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="db2f3-475">Define the cost allocation</span></span>

<span data-ttu-id="db2f3-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="db2f3-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="db2f3-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-479">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="db2f3-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-481">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-481">CC002</span></span></td>
<td><span data-ttu-id="db2f3-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-482">Finance</span></span></td>
<td><span data-ttu-id="db2f3-483">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-484">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-484">CC003</span></span></td>
<td><span data-ttu-id="db2f3-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-485">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-486">55</span><span class="sxs-lookup"><span data-stu-id="db2f3-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-487">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-487">CC004</span></span></td>
<td><span data-ttu-id="db2f3-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-488">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-489">10</span><span class="sxs-lookup"><span data-stu-id="db2f3-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="db2f3-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-492">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="db2f3-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-494">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-494">CC003</span></span></td>
<td><span data-ttu-id="db2f3-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-495">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-496">65</span><span class="sxs-lookup"><span data-stu-id="db2f3-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-497">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-497">CC004</span></span></td>
<td><span data-ttu-id="db2f3-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-498">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-499">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="db2f3-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-502">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="db2f3-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-504">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-505">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-506">60</span><span class="sxs-lookup"><span data-stu-id="db2f3-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-507">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-508">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-509">20</span><span class="sxs-lookup"><span data-stu-id="db2f3-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="db2f3-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db2f3-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-512">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="db2f3-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-514">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-515">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-516">80</span><span class="sxs-lookup"><span data-stu-id="db2f3-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-517">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-518">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-519">15</span><span class="sxs-lookup"><span data-stu-id="db2f3-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="db2f3-520">Programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="db2f3-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="db2f3-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="db2f3-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="db2f3-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-523">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-524">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-525">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-526">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-526">Amount</span></span></th>
<th><span data-ttu-id="db2f3-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-528">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-528">CC002</span></span></td>
<td><span data-ttu-id="db2f3-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-529">Finance</span></span></td>
<td><span data-ttu-id="db2f3-530">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-530">35</span></span></td>
<td><span data-ttu-id="db2f3-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="db2f3-532">175.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-532">175.00</span></span></td>
<td><span data-ttu-id="db2f3-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-534">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-534">CC003</span></span></td>
<td><span data-ttu-id="db2f3-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-535">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-536">55</span><span class="sxs-lookup"><span data-stu-id="db2f3-536">55</span></span></td>
<td><span data-ttu-id="db2f3-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="db2f3-538">275.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-538">275.00</span></span></td>
<td><span data-ttu-id="db2f3-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-540">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-540">CC004</span></span></td>
<td><span data-ttu-id="db2f3-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-541">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-542">10</span><span class="sxs-lookup"><span data-stu-id="db2f3-542">10</span></span></td>
<td><span data-ttu-id="db2f3-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="db2f3-544">50,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-544">50.00</span></span></td>
<td><span data-ttu-id="db2f3-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-546">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-546">CC002</span></span></td>
<td><span data-ttu-id="db2f3-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-547">Finance</span></span></td>
<td><span data-ttu-id="db2f3-548">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-548">35</span></span></td>
<td><span data-ttu-id="db2f3-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="db2f3-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="db2f3-550">436.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-550">436.00</span></span></td>
<td><span data-ttu-id="db2f3-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-552">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-552">CC003</span></span></td>
<td><span data-ttu-id="db2f3-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-553">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-554">55</span><span class="sxs-lookup"><span data-stu-id="db2f3-554">55</span></span></td>
<td><span data-ttu-id="db2f3-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="db2f3-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="db2f3-556">685.14</span><span class="sxs-lookup"><span data-stu-id="db2f3-556">685.14</span></span></td>
<td><span data-ttu-id="db2f3-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-558">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-558">CC004</span></span></td>
<td><span data-ttu-id="db2f3-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-559">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-560">10</span><span class="sxs-lookup"><span data-stu-id="db2f3-560">10</span></span></td>
<td><span data-ttu-id="db2f3-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="db2f3-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="db2f3-562">124.57</span><span class="sxs-lookup"><span data-stu-id="db2f3-562">124.57</span></span></td>
<td><span data-ttu-id="db2f3-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-565">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-566">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-567">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-568">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-568">Amount</span></span></th>
<th><span data-ttu-id="db2f3-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-570">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-570">CC003</span></span></td>
<td><span data-ttu-id="db2f3-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-571">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-572">65</span><span class="sxs-lookup"><span data-stu-id="db2f3-572">65</span></span></td>
<td><span data-ttu-id="db2f3-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="db2f3-574">438.75</span><span class="sxs-lookup"><span data-stu-id="db2f3-574">438.75</span></span></td>
<td><span data-ttu-id="db2f3-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-576">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-576">CC004</span></span></td>
<td><span data-ttu-id="db2f3-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-577">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-578">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-578">35</span></span></td>
<td><span data-ttu-id="db2f3-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="db2f3-580">236.25</span><span class="sxs-lookup"><span data-stu-id="db2f3-580">236.25</span></span></td>
<td><span data-ttu-id="db2f3-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-582">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-582">CC003</span></span></td>
<td><span data-ttu-id="db2f3-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-583">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-584">65</span><span class="sxs-lookup"><span data-stu-id="db2f3-584">65</span></span></td>
<td><span data-ttu-id="db2f3-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="db2f3-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="db2f3-586">5,297.69</span></span></td>
<td><span data-ttu-id="db2f3-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-588">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-588">CC004</span></span></td>
<td><span data-ttu-id="db2f3-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-589">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-590">35</span><span class="sxs-lookup"><span data-stu-id="db2f3-590">35</span></span></td>
<td><span data-ttu-id="db2f3-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="db2f3-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="db2f3-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="db2f3-592">2,852.60</span></span></td>
<td><span data-ttu-id="db2f3-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-595">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-596">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-597">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-598">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-598">Amount</span></span></th>
<th><span data-ttu-id="db2f3-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-600">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-601">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-602">60</span><span class="sxs-lookup"><span data-stu-id="db2f3-602">60</span></span></td>
<td><span data-ttu-id="db2f3-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="db2f3-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="db2f3-604">535.31</span><span class="sxs-lookup"><span data-stu-id="db2f3-604">535.31</span></span></td>
<td><span data-ttu-id="db2f3-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-606">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-607">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-608">20</span><span class="sxs-lookup"><span data-stu-id="db2f3-608">20</span></span></td>
<td><span data-ttu-id="db2f3-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="db2f3-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="db2f3-610">178.44</span><span class="sxs-lookup"><span data-stu-id="db2f3-610">178.44</span></span></td>
<td><span data-ttu-id="db2f3-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-612">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-613">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-614">60</span><span class="sxs-lookup"><span data-stu-id="db2f3-614">60</span></span></td>
<td><span data-ttu-id="db2f3-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="db2f3-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="db2f3-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="db2f3-616">4,487.12</span></span></td>
<td><span data-ttu-id="db2f3-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-618">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-619">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-620">20</span><span class="sxs-lookup"><span data-stu-id="db2f3-620">20</span></span></td>
<td><span data-ttu-id="db2f3-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="db2f3-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="db2f3-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-622">1,495.71</span></span></td>
<td><span data-ttu-id="db2f3-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="db2f3-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-625">Cost object</span></span></th>
<th><span data-ttu-id="db2f3-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="db2f3-626">Magnitude</span></span></th>
<th><span data-ttu-id="db2f3-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="db2f3-627">Allocation factor</span></span></th>
<th><span data-ttu-id="db2f3-628">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-628">Amount</span></span></th>
<th><span data-ttu-id="db2f3-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-630">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-631">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-632">80</span><span class="sxs-lookup"><span data-stu-id="db2f3-632">80</span></span></td>
<td><span data-ttu-id="db2f3-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="db2f3-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="db2f3-634">241.05</span><span class="sxs-lookup"><span data-stu-id="db2f3-634">241.05</span></span></td>
<td><span data-ttu-id="db2f3-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-636">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-637">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-638">15</span><span class="sxs-lookup"><span data-stu-id="db2f3-638">15</span></span></td>
<td><span data-ttu-id="db2f3-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="db2f3-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="db2f3-640">45.20</span><span class="sxs-lookup"><span data-stu-id="db2f3-640">45.20</span></span></td>
<td><span data-ttu-id="db2f3-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-642">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-643">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-644">80</span><span class="sxs-lookup"><span data-stu-id="db2f3-644">80</span></span></td>
<td><span data-ttu-id="db2f3-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="db2f3-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="db2f3-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="db2f3-646">2,507.09</span></span></td>
<td><span data-ttu-id="db2f3-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-648">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-649">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-650">15</span><span class="sxs-lookup"><span data-stu-id="db2f3-650">15</span></span></td>
<td><span data-ttu-id="db2f3-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="db2f3-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="db2f3-652">470.08</span><span class="sxs-lookup"><span data-stu-id="db2f3-652">470.08</span></span></td>
<td><span data-ttu-id="db2f3-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="db2f3-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="db2f3-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-655">Journal</span></span></th>
<th><span data-ttu-id="db2f3-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="db2f3-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="db2f3-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="db2f3-658">Versija</span><span class="sxs-lookup"><span data-stu-id="db2f3-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-659">00004</span><span class="sxs-lookup"><span data-stu-id="db2f3-659">00004</span></span></td>
<td><span data-ttu-id="db2f3-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="db2f3-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="db2f3-661">Fiscal</span></span></td>
<td><span data-ttu-id="db2f3-662">2017</span><span class="sxs-lookup"><span data-stu-id="db2f3-662">2017</span></span></td>
<td><span data-ttu-id="db2f3-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-663">Period 1</span></span></td>
<td><span data-ttu-id="db2f3-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="db2f3-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="db2f3-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="db2f3-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="db2f3-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-668">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-669">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-670">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-672">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-672">CC001</span></span></td>
<td><span data-ttu-id="db2f3-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-673">HR</span></span></td>
<td><span data-ttu-id="db2f3-674">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-674">10001</span></span></td>
<td><span data-ttu-id="db2f3-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-675">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-676">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-677">500,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-679">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-679">CC001</span></span></td>
<td><span data-ttu-id="db2f3-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-680">HR</span></span></td>
<td><span data-ttu-id="db2f3-681">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-681">10001</span></span></td>
<td><span data-ttu-id="db2f3-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-682">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-683">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-686">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-686">CC002</span></span></td>
<td><span data-ttu-id="db2f3-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-687">Finance</span></span></td>
<td><span data-ttu-id="db2f3-688">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-688">10001</span></span></td>
<td><span data-ttu-id="db2f3-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-689">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-690">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-691">675.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-693">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-693">CC002</span></span></td>
<td><span data-ttu-id="db2f3-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-694">Finance</span></span></td>
<td><span data-ttu-id="db2f3-695">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-695">10001</span></span></td>
<td><span data-ttu-id="db2f3-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-696">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-697">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="db2f3-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-700">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-700">CC003</span></span></td>
<td><span data-ttu-id="db2f3-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-701">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-702">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-702">10001</span></span></td>
<td><span data-ttu-id="db2f3-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-703">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-704">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-705">713.75</span><span class="sxs-lookup"><span data-stu-id="db2f3-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-707">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-707">CC003</span></span></td>
<td><span data-ttu-id="db2f3-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-708">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-709">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-709">10001</span></span></td>
<td><span data-ttu-id="db2f3-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-710">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-711">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="db2f3-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-714">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-714">CC003</span></span></td>
<td><span data-ttu-id="db2f3-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-715">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-716">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-716">10001</span></span></td>
<td><span data-ttu-id="db2f3-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-717">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-718">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-719">286.25</span><span class="sxs-lookup"><span data-stu-id="db2f3-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-721">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-721">CC003</span></span></td>
<td><span data-ttu-id="db2f3-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-722">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-723">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-723">10001</span></span></td>
<td><span data-ttu-id="db2f3-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-724">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-725">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="db2f3-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-728">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-729">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-730">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-730">10001</span></span></td>
<td><span data-ttu-id="db2f3-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-731">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-732">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-733">776.36</span><span class="sxs-lookup"><span data-stu-id="db2f3-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-735">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-736">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-737">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-737">10001</span></span></td>
<td><span data-ttu-id="db2f3-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-738">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-739">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="db2f3-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-742">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-743">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-744">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-744">10001</span></span></td>
<td><span data-ttu-id="db2f3-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-745">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-746">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-747">223.64</span><span class="sxs-lookup"><span data-stu-id="db2f3-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="db2f3-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-749">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-750">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-751">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-751">10001</span></span></td>
<td><span data-ttu-id="db2f3-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-752">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-753">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="db2f3-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="db2f3-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="db2f3-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="db2f3-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="db2f3-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-757">Cost element</span></span></th>
<th><span data-ttu-id="db2f3-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="db2f3-758">Cost behavior</span></span></th>
<th><span data-ttu-id="db2f3-759">Suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-759">Amount</span></span></th>
<th><span data-ttu-id="db2f3-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="db2f3-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="db2f3-761">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-761">CC001</span></span></td>
<td><span data-ttu-id="db2f3-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-762">HR</span></span></td>
<td><span data-ttu-id="db2f3-763">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-763">10001</span></span></td>
<td><span data-ttu-id="db2f3-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-764">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-765">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-766">-500.00</span></span></td>
<td><span data-ttu-id="db2f3-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-768">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-768">CC002</span></span></td>
<td><span data-ttu-id="db2f3-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-769">Finance</span></span></td>
<td><span data-ttu-id="db2f3-770">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-770">10001</span></span></td>
<td><span data-ttu-id="db2f3-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-771">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-772">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-773">175.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-773">175.00</span></span></td>
<td><span data-ttu-id="db2f3-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-775">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-775">CC003</span></span></td>
<td><span data-ttu-id="db2f3-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-776">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-777">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-777">10001</span></span></td>
<td><span data-ttu-id="db2f3-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-778">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-779">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-780">275.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-780">275.00</span></span></td>
<td><span data-ttu-id="db2f3-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-782">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-782">CC004</span></span></td>
<td><span data-ttu-id="db2f3-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-783">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-784">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-784">10001</span></span></td>
<td><span data-ttu-id="db2f3-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-785">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-786">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-787">50,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-787">50,00</span></span></td>
<td><span data-ttu-id="db2f3-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-789">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-789">CC001</span></span></td>
<td><span data-ttu-id="db2f3-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="db2f3-790">HR</span></span></td>
<td><span data-ttu-id="db2f3-791">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-791">10001</span></span></td>
<td><span data-ttu-id="db2f3-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-792">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-793">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-794">-1,245.71</span></span></td>
<td><span data-ttu-id="db2f3-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-796">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-796">CC002</span></span></td>
<td><span data-ttu-id="db2f3-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-797">Finance</span></span></td>
<td><span data-ttu-id="db2f3-798">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-798">10001</span></span></td>
<td><span data-ttu-id="db2f3-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-799">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-800">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-801">436.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-801">436.00</span></span></td>
<td><span data-ttu-id="db2f3-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-803">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-803">CC003</span></span></td>
<td><span data-ttu-id="db2f3-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-804">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-805">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-805">10001</span></span></td>
<td><span data-ttu-id="db2f3-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-806">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-807">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-808">685.14</span><span class="sxs-lookup"><span data-stu-id="db2f3-808">685.14</span></span></td>
<td><span data-ttu-id="db2f3-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-810">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-810">CC004</span></span></td>
<td><span data-ttu-id="db2f3-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-811">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-812">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-812">10001</span></span></td>
<td><span data-ttu-id="db2f3-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-813">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-814">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-815">124.57</span><span class="sxs-lookup"><span data-stu-id="db2f3-815">124.57</span></span></td>
<td><span data-ttu-id="db2f3-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-817">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-817">CC002</span></span></td>
<td><span data-ttu-id="db2f3-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-818">Finance</span></span></td>
<td><span data-ttu-id="db2f3-819">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-819">10001</span></span></td>
<td><span data-ttu-id="db2f3-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-820">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-821">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="db2f3-822">-675.00</span></span></td>
<td><span data-ttu-id="db2f3-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-824">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-824">CC003</span></span></td>
<td><span data-ttu-id="db2f3-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-825">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-826">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-826">10001</span></span></td>
<td><span data-ttu-id="db2f3-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-827">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-828">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-829">438.75</span><span class="sxs-lookup"><span data-stu-id="db2f3-829">438.75</span></span></td>
<td><span data-ttu-id="db2f3-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-831">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-831">CC004</span></span></td>
<td><span data-ttu-id="db2f3-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-832">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-833">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-833">10001</span></span></td>
<td><span data-ttu-id="db2f3-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-834">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-835">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-836">236.25</span><span class="sxs-lookup"><span data-stu-id="db2f3-836">236.25</span></span></td>
<td><span data-ttu-id="db2f3-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-838">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-838">CC002</span></span></td>
<td><span data-ttu-id="db2f3-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="db2f3-839">Finance</span></span></td>
<td><span data-ttu-id="db2f3-840">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-840">10001</span></span></td>
<td><span data-ttu-id="db2f3-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-841">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-842">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="db2f3-843">-8,150.29</span></span></td>
<td><span data-ttu-id="db2f3-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-845">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-845">CC003</span></span></td>
<td><span data-ttu-id="db2f3-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-846">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-847">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-847">10001</span></span></td>
<td><span data-ttu-id="db2f3-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-848">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-849">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="db2f3-850">5,297.69</span></span></td>
<td><span data-ttu-id="db2f3-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-852">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-852">CC004</span></span></td>
<td><span data-ttu-id="db2f3-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="db2f3-853">Packaging</span></span></td>
<td><span data-ttu-id="db2f3-854">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-854">10001</span></span></td>
<td><span data-ttu-id="db2f3-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-855">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-856">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="db2f3-857">2,852.60</span></span></td>
<td><span data-ttu-id="db2f3-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-859">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-859">CC003</span></span></td>
<td><span data-ttu-id="db2f3-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-860">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-861">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-861">10001</span></span></td>
<td><span data-ttu-id="db2f3-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-862">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-863">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="db2f3-864">-713.75</span></span></td>
<td><span data-ttu-id="db2f3-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-866">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-867">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-868">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-868">10001</span></span></td>
<td><span data-ttu-id="db2f3-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-869">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-870">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-871">535.31</span><span class="sxs-lookup"><span data-stu-id="db2f3-871">535.31</span></span></td>
<td><span data-ttu-id="db2f3-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-873">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-874">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-875">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-875">10001</span></span></td>
<td><span data-ttu-id="db2f3-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-876">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-877">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-878">178.44</span><span class="sxs-lookup"><span data-stu-id="db2f3-878">178.44</span></span></td>
<td><span data-ttu-id="db2f3-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-880">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-880">CC003</span></span></td>
<td><span data-ttu-id="db2f3-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-881">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-882">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-882">10001</span></span></td>
<td><span data-ttu-id="db2f3-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-883">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-884">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="db2f3-885">-5,982.83</span></span></td>
<td><span data-ttu-id="db2f3-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-887">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-888">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-889">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-889">10001</span></span></td>
<td><span data-ttu-id="db2f3-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-890">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-891">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="db2f3-892">4,487.12</span></span></td>
<td><span data-ttu-id="db2f3-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-894">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-895">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-896">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-896">10001</span></span></td>
<td><span data-ttu-id="db2f3-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-897">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-898">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="db2f3-899">1,495.71</span></span></td>
<td><span data-ttu-id="db2f3-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-901">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-901">CC003</span></span></td>
<td><span data-ttu-id="db2f3-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-902">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-903">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-903">10001</span></span></td>
<td><span data-ttu-id="db2f3-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-904">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-905">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="db2f3-906">-286.25</span></span></td>
<td><span data-ttu-id="db2f3-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-908">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-909">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-910">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-910">10001</span></span></td>
<td><span data-ttu-id="db2f3-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-911">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-912">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-913">241.05</span><span class="sxs-lookup"><span data-stu-id="db2f3-913">241.05</span></span></td>
<td><span data-ttu-id="db2f3-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-915">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-916">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-917">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-917">10001</span></span></td>
<td><span data-ttu-id="db2f3-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-918">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-919">Fixed cost</span></span></td>
<td><span data-ttu-id="db2f3-920">45.20</span><span class="sxs-lookup"><span data-stu-id="db2f3-920">45.20</span></span></td>
<td><span data-ttu-id="db2f3-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-922">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-922">CC003</span></span></td>
<td><span data-ttu-id="db2f3-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="db2f3-923">Assembly</span></span></td>
<td><span data-ttu-id="db2f3-924">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-924">10001</span></span></td>
<td><span data-ttu-id="db2f3-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-925">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-926">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="db2f3-927">-2,977.17</span></span></td>
<td><span data-ttu-id="db2f3-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-929">Prod 1</span></span></td>
<td><span data-ttu-id="db2f3-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-930">Product 1</span></span></td>
<td><span data-ttu-id="db2f3-931">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-931">10001</span></span></td>
<td><span data-ttu-id="db2f3-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-932">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-933">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="db2f3-934">2,507.09</span></span></td>
<td><span data-ttu-id="db2f3-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="db2f3-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-936">Prod 2</span></span></td>
<td><span data-ttu-id="db2f3-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="db2f3-937">Product 2</span></span></td>
<td><span data-ttu-id="db2f3-938">10001</span><span class="sxs-lookup"><span data-stu-id="db2f3-938">10001</span></span></td>
<td><span data-ttu-id="db2f3-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-939">Electricity</span></span></td>
<td><span data-ttu-id="db2f3-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-940">Variable cost</span></span></td>
<td><span data-ttu-id="db2f3-941">470.08</span><span class="sxs-lookup"><span data-stu-id="db2f3-941">470.08</span></span></td>
<td><span data-ttu-id="db2f3-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="db2f3-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="db2f3-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="db2f3-943">Conclusion</span></span>
<span data-ttu-id="db2f3-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="db2f3-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="db2f3-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="db2f3-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="db2f3-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="db2f3-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="db2f3-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="db2f3-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="db2f3-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="db2f3-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="db2f3-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="db2f3-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="db2f3-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="db2f3-951">CC099</span><span class="sxs-lookup"><span data-stu-id="db2f3-951">CC099</span></span></th>
<th><span data-ttu-id="db2f3-952">CC001</span><span class="sxs-lookup"><span data-stu-id="db2f3-952">CC001</span></span></th>
<th><span data-ttu-id="db2f3-953">CC002</span><span class="sxs-lookup"><span data-stu-id="db2f3-953">CC002</span></span></th>
<th><span data-ttu-id="db2f3-954">CC003</span><span class="sxs-lookup"><span data-stu-id="db2f3-954">CC003</span></span></th>
<th><span data-ttu-id="db2f3-955">CC004</span><span class="sxs-lookup"><span data-stu-id="db2f3-955">CC004</span></span></th>
<th><span data-ttu-id="db2f3-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-956">Proj 1</span></span></th>
<th><span data-ttu-id="db2f3-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="db2f3-957">Proj 2</span></span></th>
<th><span data-ttu-id="db2f3-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-958">Prod 1</span></span></th>
<th><span data-ttu-id="db2f3-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="db2f3-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="db2f3-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="db2f3-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="db2f3-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="db2f3-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-971">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="db2f3-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-973">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-974">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-975">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-976">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-977">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-978">776.36</span><span class="sxs-lookup"><span data-stu-id="db2f3-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-979">223.64</span><span class="sxs-lookup"><span data-stu-id="db2f3-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="db2f3-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="db2f3-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-982">000</span><span class="sxs-lookup"><span data-stu-id="db2f3-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-983">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-984">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-985">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-986">0,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-987">30,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-988">10,00</span><span class="sxs-lookup"><span data-stu-id="db2f3-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="db2f3-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="db2f3-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="db2f3-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="db2f3-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="db2f3-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="db2f3-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="db2f3-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="db2f3-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="db2f3-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="db2f3-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="db2f3-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="db2f3-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="db2f3-996">Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="db2f3-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



