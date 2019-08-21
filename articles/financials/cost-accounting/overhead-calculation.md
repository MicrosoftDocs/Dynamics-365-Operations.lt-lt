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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841494"
---
# <a name="overhead-calculation"></a><span data-ttu-id="daaa7-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="daaa7-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="daaa7-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="daaa7-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="daaa7-105">Term definition</span></span>
---------------

<span data-ttu-id="daaa7-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="daaa7-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="daaa7-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="daaa7-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="daaa7-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="daaa7-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="daaa7-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="daaa7-109">Rent</span></span>
-   <span data-ttu-id="daaa7-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-110">Electricity</span></span>
-   <span data-ttu-id="daaa7-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="daaa7-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="daaa7-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="daaa7-112">Overhead calculation overview</span></span>
<span data-ttu-id="daaa7-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="daaa7-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="daaa7-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="daaa7-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="daaa7-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="daaa7-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="daaa7-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="daaa7-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="daaa7-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="daaa7-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="daaa7-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="daaa7-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="daaa7-119">Version type</span></span>
-   <span data-ttu-id="daaa7-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="daaa7-120">Date and time</span></span>
-   <span data-ttu-id="daaa7-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="daaa7-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="daaa7-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="daaa7-122">Fiscal year</span></span>
-   <span data-ttu-id="daaa7-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-123">Fiscal period</span></span>

<span data-ttu-id="daaa7-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="daaa7-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="daaa7-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="daaa7-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="daaa7-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="daaa7-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="daaa7-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="daaa7-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="daaa7-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="daaa7-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="daaa7-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="daaa7-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="daaa7-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="daaa7-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="daaa7-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="daaa7-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="daaa7-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="daaa7-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="daaa7-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="daaa7-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="daaa7-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="daaa7-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="daaa7-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="daaa7-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="daaa7-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="daaa7-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="daaa7-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="daaa7-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="daaa7-140">Main account</span></span></th>
<th><span data-ttu-id="daaa7-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="daaa7-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="daaa7-143">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-143">CC099</span></span></td>
<td><span data-ttu-id="daaa7-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-144">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-145">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-145">10001</span></span></td>
<td><span data-ttu-id="daaa7-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-146">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="daaa7-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="daaa7-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="daaa7-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="daaa7-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="daaa7-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="daaa7-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="daaa7-151">Define the cost behavior rule</span></span>

<span data-ttu-id="daaa7-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="daaa7-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="daaa7-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="daaa7-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="daaa7-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="daaa7-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="daaa7-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="daaa7-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="daaa7-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="daaa7-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="daaa7-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="daaa7-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="daaa7-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-160">Journal</span></span></th>
<th><span data-ttu-id="daaa7-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="daaa7-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="daaa7-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="daaa7-163">Versija</span><span class="sxs-lookup"><span data-stu-id="daaa7-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-164">00001</span><span class="sxs-lookup"><span data-stu-id="daaa7-164">00001</span></span></td>
<td><span data-ttu-id="daaa7-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="daaa7-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="daaa7-166">Fiscal</span></span></td>
<td><span data-ttu-id="daaa7-167">2017</span><span class="sxs-lookup"><span data-stu-id="daaa7-167">2017</span></span></td>
<td><span data-ttu-id="daaa7-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-168">Period 1</span></span></td>
<td><span data-ttu-id="daaa7-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="daaa7-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="daaa7-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-173">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-174">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-175">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="daaa7-177">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-177">CC099</span></span></td>
<td><span data-ttu-id="daaa7-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-178">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-179">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-179">10001</span></span></td>
<td><span data-ttu-id="daaa7-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-180">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="daaa7-181">Unclassified</span></span></td>
<td><span data-ttu-id="daaa7-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="daaa7-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="daaa7-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-185">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-186">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-187">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-187">Amount</span></span></th>
<th><span data-ttu-id="daaa7-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-189">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-189">CC099</span></span></td>
<td><span data-ttu-id="daaa7-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-190">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-191">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-191">10001</span></span></td>
<td><span data-ttu-id="daaa7-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-192">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="daaa7-193">Unclassified</span></span></td>
<td><span data-ttu-id="daaa7-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-194">10,000.00</span></span></td>
<td><span data-ttu-id="daaa7-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-196">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-196">CC099</span></span></td>
<td><span data-ttu-id="daaa7-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-197">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-198">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-198">10001</span></span></td>
<td><span data-ttu-id="daaa7-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-199">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="daaa7-200">Unclassified</span></span></td>
<td><span data-ttu-id="daaa7-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-201">-10,000.00</span></span></td>
<td><span data-ttu-id="daaa7-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-203">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-203">CC099</span></span></td>
<td><span data-ttu-id="daaa7-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-204">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-205">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-205">10001</span></span></td>
<td><span data-ttu-id="daaa7-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-206">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-207">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-208">1,000.00</span></span></td>
<td><span data-ttu-id="daaa7-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-210">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-210">CC099</span></span></td>
<td><span data-ttu-id="daaa7-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-211">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-212">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-212">10001</span></span></td>
<td><span data-ttu-id="daaa7-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-213">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-214">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-215">9,000.00</span></span></td>
<td><span data-ttu-id="daaa7-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="daaa7-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="daaa7-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="daaa7-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="daaa7-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="daaa7-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="daaa7-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="daaa7-221">Define the cost distribution rule</span></span>

<span data-ttu-id="daaa7-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="daaa7-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="daaa7-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="daaa7-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="daaa7-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="daaa7-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="daaa7-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="daaa7-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="daaa7-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="daaa7-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="daaa7-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="daaa7-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-228">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="daaa7-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-230">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-230">CC001</span></span></td>
<td><span data-ttu-id="daaa7-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-231">HR</span></span></td>
<td><span data-ttu-id="daaa7-232">1000</span><span class="sxs-lookup"><span data-stu-id="daaa7-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-233">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-233">CC002</span></span></td>
<td><span data-ttu-id="daaa7-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-234">Finance</span></span></td>
<td><span data-ttu-id="daaa7-235">6,000</span><span class="sxs-lookup"><span data-stu-id="daaa7-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-236">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-236">CC003</span></span></td>
<td><span data-ttu-id="daaa7-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-237">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-238">0</span><span class="sxs-lookup"><span data-stu-id="daaa7-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-240">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-241">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-242">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-243">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-244">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-244">CC001</span></span></td>
<td><span data-ttu-id="daaa7-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-245">HR</span></span></td>
<td><span data-ttu-id="daaa7-246">1000</span><span class="sxs-lookup"><span data-stu-id="daaa7-246">1,000</span></span></td>
<td><span data-ttu-id="daaa7-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="daaa7-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-249">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-249">CC002</span></span></td>
<td><span data-ttu-id="daaa7-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-250">Finance</span></span></td>
<td><span data-ttu-id="daaa7-251">6,000</span><span class="sxs-lookup"><span data-stu-id="daaa7-251">6,000</span></span></td>
<td><span data-ttu-id="daaa7-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="daaa7-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="daaa7-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-254">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-254">CC003</span></span></td>
<td><span data-ttu-id="daaa7-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-255">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-256">0</span><span class="sxs-lookup"><span data-stu-id="daaa7-256">0</span></span></td>
<td><span data-ttu-id="daaa7-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="daaa7-258">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="daaa7-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-261">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="daaa7-262">Formula</span></span></th>
<th><span data-ttu-id="daaa7-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-263">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-264">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-265">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-266">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-266">CC001</span></span></td>
<td><span data-ttu-id="daaa7-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-267">HR</span></span></td>
<td><span data-ttu-id="daaa7-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="daaa7-269">1</span><span class="sxs-lookup"><span data-stu-id="daaa7-269">1</span></span></td>
<td><span data-ttu-id="daaa7-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="daaa7-271">500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-272">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-272">CC002</span></span></td>
<td><span data-ttu-id="daaa7-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-273">Finance</span></span></td>
<td><span data-ttu-id="daaa7-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="daaa7-275">1</span><span class="sxs-lookup"><span data-stu-id="daaa7-275">1</span></span></td>
<td><span data-ttu-id="daaa7-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="daaa7-277">500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-278">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-278">CC003</span></span></td>
<td><span data-ttu-id="daaa7-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-279">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="daaa7-281">0</span><span class="sxs-lookup"><span data-stu-id="daaa7-281">0</span></span></td>
<td><span data-ttu-id="daaa7-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="daaa7-283">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="daaa7-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-285">Journal</span></span></th>
<th><span data-ttu-id="daaa7-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="daaa7-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="daaa7-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="daaa7-288">Versija</span><span class="sxs-lookup"><span data-stu-id="daaa7-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-289">00002</span><span class="sxs-lookup"><span data-stu-id="daaa7-289">00002</span></span></td>
<td><span data-ttu-id="daaa7-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="daaa7-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="daaa7-291">Fiscal</span></span></td>
<td><span data-ttu-id="daaa7-292">2017</span><span class="sxs-lookup"><span data-stu-id="daaa7-292">2017</span></span></td>
<td><span data-ttu-id="daaa7-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-293">Period 1</span></span></td>
<td><span data-ttu-id="daaa7-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="daaa7-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="daaa7-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-298">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-299">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-300">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-302">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-302">CC099</span></span></td>
<td><span data-ttu-id="daaa7-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-303">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-304">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-304">10001</span></span></td>
<td><span data-ttu-id="daaa7-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-305">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-306">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-309">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-309">CC099</span></span></td>
<td><span data-ttu-id="daaa7-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-310">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-311">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-311">10001</span></span></td>
<td><span data-ttu-id="daaa7-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-312">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-313">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="daaa7-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="daaa7-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-317">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-318">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-319">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-319">Amount</span></span></th>
<th><span data-ttu-id="daaa7-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-321">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-321">CC099</span></span></td>
<td><span data-ttu-id="daaa7-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-322">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-323">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-323">10001</span></span></td>
<td><span data-ttu-id="daaa7-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-324">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-325">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-326">-1,000.00</span></span></td>
<td><span data-ttu-id="daaa7-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-328">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-328">CC001</span></span></td>
<td><span data-ttu-id="daaa7-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-329">HR</span></span></td>
<td><span data-ttu-id="daaa7-330">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-330">10001</span></span></td>
<td><span data-ttu-id="daaa7-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-331">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-332">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-333">500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-333">500.00</span></span></td>
<td><span data-ttu-id="daaa7-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-335">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-335">CC002</span></span></td>
<td><span data-ttu-id="daaa7-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-336">Finance</span></span></td>
<td><span data-ttu-id="daaa7-337">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-337">10001</span></span></td>
<td><span data-ttu-id="daaa7-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-338">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-339">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-340">500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-340">500.00</span></span></td>
<td><span data-ttu-id="daaa7-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-342">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-342">CC099</span></span></td>
<td><span data-ttu-id="daaa7-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="daaa7-343">Default cost center</span></span></td>
<td><span data-ttu-id="daaa7-344">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-344">10001</span></span></td>
<td><span data-ttu-id="daaa7-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-345">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-346">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-347">-9,000.00</span></span></td>
<td><span data-ttu-id="daaa7-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-349">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-349">CC001</span></span></td>
<td><span data-ttu-id="daaa7-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-350">HR</span></span></td>
<td><span data-ttu-id="daaa7-351">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-351">10001</span></span></td>
<td><span data-ttu-id="daaa7-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-352">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-353">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-354">1,285.71</span></span></td>
<td><span data-ttu-id="daaa7-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-356">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-356">CC002</span></span></td>
<td><span data-ttu-id="daaa7-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-357">Finance</span></span></td>
<td><span data-ttu-id="daaa7-358">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-358">10001</span></span></td>
<td><span data-ttu-id="daaa7-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-359">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-360">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="daaa7-361">7,714.29</span></span></td>
<td><span data-ttu-id="daaa7-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="daaa7-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="daaa7-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="daaa7-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="daaa7-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="daaa7-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="daaa7-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="daaa7-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="daaa7-367">Define the overhead rate</span></span>

<span data-ttu-id="daaa7-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="daaa7-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-370">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="daaa7-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-372">Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-373">Project 1</span></span></td>
<td><span data-ttu-id="daaa7-374">3</span><span class="sxs-lookup"><span data-stu-id="daaa7-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-375">Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-376">Project 2</span></span></td>
<td><span data-ttu-id="daaa7-377">1</span><span class="sxs-lookup"><span data-stu-id="daaa7-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="daaa7-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-379">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-380">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-381">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="daaa7-382">Units</span></span></th>
<th><span data-ttu-id="daaa7-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="daaa7-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-384">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-384">CC001</span></span></td>
<td><span data-ttu-id="daaa7-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-385">HR</span></span></td>
<td><span data-ttu-id="daaa7-386">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-386">10001</span></span></td>
<td><span data-ttu-id="daaa7-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-387">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-388">1</span><span class="sxs-lookup"><span data-stu-id="daaa7-388">1</span></span></td>
<td><span data-ttu-id="daaa7-389">10</span><span class="sxs-lookup"><span data-stu-id="daaa7-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-391">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-392">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-393">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-394">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-395">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-396">Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-397">Project 1</span></span></td>
<td><span data-ttu-id="daaa7-398">3</span><span class="sxs-lookup"><span data-stu-id="daaa7-398">3</span></span></td>
<td><span data-ttu-id="daaa7-399">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-399">10001</span></span></td>
<td><span data-ttu-id="daaa7-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="daaa7-401">30,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-402">Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-403">Project 2</span></span></td>
<td><span data-ttu-id="daaa7-404">1</span><span class="sxs-lookup"><span data-stu-id="daaa7-404">1</span></span></td>
<td><span data-ttu-id="daaa7-405">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-405">10001</span></span></td>
<td><span data-ttu-id="daaa7-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="daaa7-407">10,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="daaa7-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-409">Journal</span></span></th>
<th><span data-ttu-id="daaa7-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="daaa7-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="daaa7-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="daaa7-412">Versija</span><span class="sxs-lookup"><span data-stu-id="daaa7-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-413">00003</span><span class="sxs-lookup"><span data-stu-id="daaa7-413">00003</span></span></td>
<td><span data-ttu-id="daaa7-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="daaa7-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="daaa7-415">Fiscal</span></span></td>
<td><span data-ttu-id="daaa7-416">2017</span><span class="sxs-lookup"><span data-stu-id="daaa7-416">2017</span></span></td>
<td><span data-ttu-id="daaa7-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-417">Period 1</span></span></td>
<td><span data-ttu-id="daaa7-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="daaa7-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="daaa7-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-421">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-424">Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-426">3,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-428">Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-430">1,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="daaa7-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="daaa7-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-433">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-434">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-435">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-435">Amount</span></span></th>
<th><span data-ttu-id="daaa7-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="daaa7-437">CC0001</span></span></td>
<td><span data-ttu-id="daaa7-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-438">HR</span></span></td>
<td><span data-ttu-id="daaa7-439">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-439">10001</span></span></td>
<td><span data-ttu-id="daaa7-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-440">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-441">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-442">-30.00</span></span></td>
<td><span data-ttu-id="daaa7-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-444">Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="daaa7-446">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-446">10001</span></span></td>
<td><span data-ttu-id="daaa7-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-447">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-448">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-449">30,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-449">30.00</span></span></td>
<td><span data-ttu-id="daaa7-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-451">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-451">CC001</span></span></td>
<td><span data-ttu-id="daaa7-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-452">HR</span></span></td>
<td><span data-ttu-id="daaa7-453">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-453">10001</span></span></td>
<td><span data-ttu-id="daaa7-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-454">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-455">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-456">-10.00</span></span></td>
<td><span data-ttu-id="daaa7-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-458">Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="daaa7-460">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-460">10001</span></span></td>
<td><span data-ttu-id="daaa7-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-461">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-462">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-463">10,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-463">10.00</span></span></td>
<td><span data-ttu-id="daaa7-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="daaa7-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="daaa7-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="daaa7-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="daaa7-468">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="daaa7-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="daaa7-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="daaa7-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="daaa7-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="daaa7-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="daaa7-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="daaa7-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="daaa7-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="daaa7-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="daaa7-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="daaa7-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="daaa7-475">Define the cost allocation</span></span>

<span data-ttu-id="daaa7-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="daaa7-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="daaa7-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-479">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="daaa7-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-481">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-481">CC002</span></span></td>
<td><span data-ttu-id="daaa7-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-482">Finance</span></span></td>
<td><span data-ttu-id="daaa7-483">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-484">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-484">CC003</span></span></td>
<td><span data-ttu-id="daaa7-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-485">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-486">55</span><span class="sxs-lookup"><span data-stu-id="daaa7-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-487">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-487">CC004</span></span></td>
<td><span data-ttu-id="daaa7-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-488">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-489">10</span><span class="sxs-lookup"><span data-stu-id="daaa7-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="daaa7-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-492">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="daaa7-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-494">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-494">CC003</span></span></td>
<td><span data-ttu-id="daaa7-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-495">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-496">65</span><span class="sxs-lookup"><span data-stu-id="daaa7-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-497">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-497">CC004</span></span></td>
<td><span data-ttu-id="daaa7-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-498">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-499">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="daaa7-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-502">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="daaa7-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-504">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-505">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-506">60</span><span class="sxs-lookup"><span data-stu-id="daaa7-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-507">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-508">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-509">20</span><span class="sxs-lookup"><span data-stu-id="daaa7-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="daaa7-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="daaa7-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-512">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="daaa7-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-514">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-515">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-516">80</span><span class="sxs-lookup"><span data-stu-id="daaa7-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-517">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-518">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-519">15</span><span class="sxs-lookup"><span data-stu-id="daaa7-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="daaa7-520">Programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="daaa7-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="daaa7-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="daaa7-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="daaa7-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-523">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-524">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-525">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-526">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-526">Amount</span></span></th>
<th><span data-ttu-id="daaa7-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-528">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-528">CC002</span></span></td>
<td><span data-ttu-id="daaa7-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-529">Finance</span></span></td>
<td><span data-ttu-id="daaa7-530">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-530">35</span></span></td>
<td><span data-ttu-id="daaa7-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="daaa7-532">175.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-532">175.00</span></span></td>
<td><span data-ttu-id="daaa7-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-534">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-534">CC003</span></span></td>
<td><span data-ttu-id="daaa7-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-535">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-536">55</span><span class="sxs-lookup"><span data-stu-id="daaa7-536">55</span></span></td>
<td><span data-ttu-id="daaa7-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="daaa7-538">275.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-538">275.00</span></span></td>
<td><span data-ttu-id="daaa7-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-540">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-540">CC004</span></span></td>
<td><span data-ttu-id="daaa7-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-541">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-542">10</span><span class="sxs-lookup"><span data-stu-id="daaa7-542">10</span></span></td>
<td><span data-ttu-id="daaa7-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="daaa7-544">50,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-544">50.00</span></span></td>
<td><span data-ttu-id="daaa7-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-546">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-546">CC002</span></span></td>
<td><span data-ttu-id="daaa7-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-547">Finance</span></span></td>
<td><span data-ttu-id="daaa7-548">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-548">35</span></span></td>
<td><span data-ttu-id="daaa7-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="daaa7-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="daaa7-550">436.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-550">436.00</span></span></td>
<td><span data-ttu-id="daaa7-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-552">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-552">CC003</span></span></td>
<td><span data-ttu-id="daaa7-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-553">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-554">55</span><span class="sxs-lookup"><span data-stu-id="daaa7-554">55</span></span></td>
<td><span data-ttu-id="daaa7-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="daaa7-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="daaa7-556">685.14</span><span class="sxs-lookup"><span data-stu-id="daaa7-556">685.14</span></span></td>
<td><span data-ttu-id="daaa7-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-558">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-558">CC004</span></span></td>
<td><span data-ttu-id="daaa7-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-559">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-560">10</span><span class="sxs-lookup"><span data-stu-id="daaa7-560">10</span></span></td>
<td><span data-ttu-id="daaa7-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="daaa7-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="daaa7-562">124.57</span><span class="sxs-lookup"><span data-stu-id="daaa7-562">124.57</span></span></td>
<td><span data-ttu-id="daaa7-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-565">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-566">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-567">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-568">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-568">Amount</span></span></th>
<th><span data-ttu-id="daaa7-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-570">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-570">CC003</span></span></td>
<td><span data-ttu-id="daaa7-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-571">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-572">65</span><span class="sxs-lookup"><span data-stu-id="daaa7-572">65</span></span></td>
<td><span data-ttu-id="daaa7-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="daaa7-574">438.75</span><span class="sxs-lookup"><span data-stu-id="daaa7-574">438.75</span></span></td>
<td><span data-ttu-id="daaa7-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-576">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-576">CC004</span></span></td>
<td><span data-ttu-id="daaa7-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-577">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-578">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-578">35</span></span></td>
<td><span data-ttu-id="daaa7-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="daaa7-580">236.25</span><span class="sxs-lookup"><span data-stu-id="daaa7-580">236.25</span></span></td>
<td><span data-ttu-id="daaa7-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-582">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-582">CC003</span></span></td>
<td><span data-ttu-id="daaa7-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-583">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-584">65</span><span class="sxs-lookup"><span data-stu-id="daaa7-584">65</span></span></td>
<td><span data-ttu-id="daaa7-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="daaa7-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="daaa7-586">5,297.69</span></span></td>
<td><span data-ttu-id="daaa7-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-588">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-588">CC004</span></span></td>
<td><span data-ttu-id="daaa7-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-589">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-590">35</span><span class="sxs-lookup"><span data-stu-id="daaa7-590">35</span></span></td>
<td><span data-ttu-id="daaa7-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="daaa7-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="daaa7-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="daaa7-592">2,852.60</span></span></td>
<td><span data-ttu-id="daaa7-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-595">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-596">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-597">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-598">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-598">Amount</span></span></th>
<th><span data-ttu-id="daaa7-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-600">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-601">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-602">60</span><span class="sxs-lookup"><span data-stu-id="daaa7-602">60</span></span></td>
<td><span data-ttu-id="daaa7-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="daaa7-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="daaa7-604">535.31</span><span class="sxs-lookup"><span data-stu-id="daaa7-604">535.31</span></span></td>
<td><span data-ttu-id="daaa7-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-606">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-607">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-608">20</span><span class="sxs-lookup"><span data-stu-id="daaa7-608">20</span></span></td>
<td><span data-ttu-id="daaa7-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="daaa7-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="daaa7-610">178.44</span><span class="sxs-lookup"><span data-stu-id="daaa7-610">178.44</span></span></td>
<td><span data-ttu-id="daaa7-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-612">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-613">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-614">60</span><span class="sxs-lookup"><span data-stu-id="daaa7-614">60</span></span></td>
<td><span data-ttu-id="daaa7-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="daaa7-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="daaa7-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="daaa7-616">4,487.12</span></span></td>
<td><span data-ttu-id="daaa7-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-618">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-619">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-620">20</span><span class="sxs-lookup"><span data-stu-id="daaa7-620">20</span></span></td>
<td><span data-ttu-id="daaa7-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="daaa7-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="daaa7-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-622">1,495.71</span></span></td>
<td><span data-ttu-id="daaa7-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="daaa7-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-625">Cost object</span></span></th>
<th><span data-ttu-id="daaa7-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="daaa7-626">Magnitude</span></span></th>
<th><span data-ttu-id="daaa7-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="daaa7-627">Allocation factor</span></span></th>
<th><span data-ttu-id="daaa7-628">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-628">Amount</span></span></th>
<th><span data-ttu-id="daaa7-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-630">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-631">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-632">80</span><span class="sxs-lookup"><span data-stu-id="daaa7-632">80</span></span></td>
<td><span data-ttu-id="daaa7-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="daaa7-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="daaa7-634">241.05</span><span class="sxs-lookup"><span data-stu-id="daaa7-634">241.05</span></span></td>
<td><span data-ttu-id="daaa7-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-636">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-637">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-638">15</span><span class="sxs-lookup"><span data-stu-id="daaa7-638">15</span></span></td>
<td><span data-ttu-id="daaa7-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="daaa7-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="daaa7-640">45.20</span><span class="sxs-lookup"><span data-stu-id="daaa7-640">45.20</span></span></td>
<td><span data-ttu-id="daaa7-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-642">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-643">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-644">80</span><span class="sxs-lookup"><span data-stu-id="daaa7-644">80</span></span></td>
<td><span data-ttu-id="daaa7-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="daaa7-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="daaa7-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="daaa7-646">2,507.09</span></span></td>
<td><span data-ttu-id="daaa7-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-648">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-649">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-650">15</span><span class="sxs-lookup"><span data-stu-id="daaa7-650">15</span></span></td>
<td><span data-ttu-id="daaa7-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="daaa7-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="daaa7-652">470.08</span><span class="sxs-lookup"><span data-stu-id="daaa7-652">470.08</span></span></td>
<td><span data-ttu-id="daaa7-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="daaa7-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="daaa7-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-655">Journal</span></span></th>
<th><span data-ttu-id="daaa7-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="daaa7-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="daaa7-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="daaa7-658">Versija</span><span class="sxs-lookup"><span data-stu-id="daaa7-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-659">00004</span><span class="sxs-lookup"><span data-stu-id="daaa7-659">00004</span></span></td>
<td><span data-ttu-id="daaa7-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="daaa7-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="daaa7-661">Fiscal</span></span></td>
<td><span data-ttu-id="daaa7-662">2017</span><span class="sxs-lookup"><span data-stu-id="daaa7-662">2017</span></span></td>
<td><span data-ttu-id="daaa7-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-663">Period 1</span></span></td>
<td><span data-ttu-id="daaa7-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="daaa7-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="daaa7-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="daaa7-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="daaa7-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-668">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-669">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-670">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-672">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-672">CC001</span></span></td>
<td><span data-ttu-id="daaa7-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-673">HR</span></span></td>
<td><span data-ttu-id="daaa7-674">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-674">10001</span></span></td>
<td><span data-ttu-id="daaa7-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-675">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-676">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-677">500,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-679">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-679">CC001</span></span></td>
<td><span data-ttu-id="daaa7-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-680">HR</span></span></td>
<td><span data-ttu-id="daaa7-681">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-681">10001</span></span></td>
<td><span data-ttu-id="daaa7-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-682">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-683">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-686">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-686">CC002</span></span></td>
<td><span data-ttu-id="daaa7-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-687">Finance</span></span></td>
<td><span data-ttu-id="daaa7-688">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-688">10001</span></span></td>
<td><span data-ttu-id="daaa7-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-689">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-690">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-691">675.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-693">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-693">CC002</span></span></td>
<td><span data-ttu-id="daaa7-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-694">Finance</span></span></td>
<td><span data-ttu-id="daaa7-695">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-695">10001</span></span></td>
<td><span data-ttu-id="daaa7-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-696">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-697">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="daaa7-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-700">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-700">CC003</span></span></td>
<td><span data-ttu-id="daaa7-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-701">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-702">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-702">10001</span></span></td>
<td><span data-ttu-id="daaa7-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-703">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-704">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-705">713.75</span><span class="sxs-lookup"><span data-stu-id="daaa7-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-707">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-707">CC003</span></span></td>
<td><span data-ttu-id="daaa7-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-708">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-709">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-709">10001</span></span></td>
<td><span data-ttu-id="daaa7-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-710">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-711">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="daaa7-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-714">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-714">CC003</span></span></td>
<td><span data-ttu-id="daaa7-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-715">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-716">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-716">10001</span></span></td>
<td><span data-ttu-id="daaa7-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-717">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-718">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-719">286.25</span><span class="sxs-lookup"><span data-stu-id="daaa7-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-721">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-721">CC003</span></span></td>
<td><span data-ttu-id="daaa7-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-722">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-723">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-723">10001</span></span></td>
<td><span data-ttu-id="daaa7-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-724">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-725">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="daaa7-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-728">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-729">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-730">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-730">10001</span></span></td>
<td><span data-ttu-id="daaa7-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-731">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-732">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-733">776.36</span><span class="sxs-lookup"><span data-stu-id="daaa7-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-735">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-736">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-737">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-737">10001</span></span></td>
<td><span data-ttu-id="daaa7-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-738">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-739">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="daaa7-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-742">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-743">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-744">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-744">10001</span></span></td>
<td><span data-ttu-id="daaa7-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-745">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-746">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-747">223.64</span><span class="sxs-lookup"><span data-stu-id="daaa7-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="daaa7-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-749">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-750">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-751">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-751">10001</span></span></td>
<td><span data-ttu-id="daaa7-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-752">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-753">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="daaa7-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="daaa7-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="daaa7-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="daaa7-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="daaa7-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-757">Cost element</span></span></th>
<th><span data-ttu-id="daaa7-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="daaa7-758">Cost behavior</span></span></th>
<th><span data-ttu-id="daaa7-759">Suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-759">Amount</span></span></th>
<th><span data-ttu-id="daaa7-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="daaa7-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="daaa7-761">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-761">CC001</span></span></td>
<td><span data-ttu-id="daaa7-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-762">HR</span></span></td>
<td><span data-ttu-id="daaa7-763">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-763">10001</span></span></td>
<td><span data-ttu-id="daaa7-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-764">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-765">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-766">-500.00</span></span></td>
<td><span data-ttu-id="daaa7-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-768">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-768">CC002</span></span></td>
<td><span data-ttu-id="daaa7-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-769">Finance</span></span></td>
<td><span data-ttu-id="daaa7-770">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-770">10001</span></span></td>
<td><span data-ttu-id="daaa7-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-771">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-772">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-773">175.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-773">175.00</span></span></td>
<td><span data-ttu-id="daaa7-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-775">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-775">CC003</span></span></td>
<td><span data-ttu-id="daaa7-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-776">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-777">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-777">10001</span></span></td>
<td><span data-ttu-id="daaa7-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-778">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-779">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-780">275.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-780">275.00</span></span></td>
<td><span data-ttu-id="daaa7-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-782">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-782">CC004</span></span></td>
<td><span data-ttu-id="daaa7-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-783">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-784">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-784">10001</span></span></td>
<td><span data-ttu-id="daaa7-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-785">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-786">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-787">50,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-787">50,00</span></span></td>
<td><span data-ttu-id="daaa7-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-789">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-789">CC001</span></span></td>
<td><span data-ttu-id="daaa7-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="daaa7-790">HR</span></span></td>
<td><span data-ttu-id="daaa7-791">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-791">10001</span></span></td>
<td><span data-ttu-id="daaa7-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-792">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-793">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-794">-1,245.71</span></span></td>
<td><span data-ttu-id="daaa7-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-796">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-796">CC002</span></span></td>
<td><span data-ttu-id="daaa7-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-797">Finance</span></span></td>
<td><span data-ttu-id="daaa7-798">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-798">10001</span></span></td>
<td><span data-ttu-id="daaa7-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-799">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-800">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-801">436.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-801">436.00</span></span></td>
<td><span data-ttu-id="daaa7-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-803">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-803">CC003</span></span></td>
<td><span data-ttu-id="daaa7-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-804">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-805">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-805">10001</span></span></td>
<td><span data-ttu-id="daaa7-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-806">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-807">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-808">685.14</span><span class="sxs-lookup"><span data-stu-id="daaa7-808">685.14</span></span></td>
<td><span data-ttu-id="daaa7-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-810">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-810">CC004</span></span></td>
<td><span data-ttu-id="daaa7-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-811">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-812">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-812">10001</span></span></td>
<td><span data-ttu-id="daaa7-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-813">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-814">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-815">124.57</span><span class="sxs-lookup"><span data-stu-id="daaa7-815">124.57</span></span></td>
<td><span data-ttu-id="daaa7-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-817">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-817">CC002</span></span></td>
<td><span data-ttu-id="daaa7-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-818">Finance</span></span></td>
<td><span data-ttu-id="daaa7-819">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-819">10001</span></span></td>
<td><span data-ttu-id="daaa7-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-820">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-821">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="daaa7-822">-675.00</span></span></td>
<td><span data-ttu-id="daaa7-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-824">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-824">CC003</span></span></td>
<td><span data-ttu-id="daaa7-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-825">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-826">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-826">10001</span></span></td>
<td><span data-ttu-id="daaa7-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-827">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-828">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-829">438.75</span><span class="sxs-lookup"><span data-stu-id="daaa7-829">438.75</span></span></td>
<td><span data-ttu-id="daaa7-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-831">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-831">CC004</span></span></td>
<td><span data-ttu-id="daaa7-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-832">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-833">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-833">10001</span></span></td>
<td><span data-ttu-id="daaa7-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-834">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-835">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-836">236.25</span><span class="sxs-lookup"><span data-stu-id="daaa7-836">236.25</span></span></td>
<td><span data-ttu-id="daaa7-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-838">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-838">CC002</span></span></td>
<td><span data-ttu-id="daaa7-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="daaa7-839">Finance</span></span></td>
<td><span data-ttu-id="daaa7-840">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-840">10001</span></span></td>
<td><span data-ttu-id="daaa7-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-841">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-842">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="daaa7-843">-8,150.29</span></span></td>
<td><span data-ttu-id="daaa7-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-845">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-845">CC003</span></span></td>
<td><span data-ttu-id="daaa7-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-846">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-847">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-847">10001</span></span></td>
<td><span data-ttu-id="daaa7-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-848">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-849">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="daaa7-850">5,297.69</span></span></td>
<td><span data-ttu-id="daaa7-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-852">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-852">CC004</span></span></td>
<td><span data-ttu-id="daaa7-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="daaa7-853">Packaging</span></span></td>
<td><span data-ttu-id="daaa7-854">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-854">10001</span></span></td>
<td><span data-ttu-id="daaa7-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-855">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-856">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="daaa7-857">2,852.60</span></span></td>
<td><span data-ttu-id="daaa7-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-859">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-859">CC003</span></span></td>
<td><span data-ttu-id="daaa7-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-860">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-861">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-861">10001</span></span></td>
<td><span data-ttu-id="daaa7-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-862">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-863">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="daaa7-864">-713.75</span></span></td>
<td><span data-ttu-id="daaa7-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-866">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-867">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-868">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-868">10001</span></span></td>
<td><span data-ttu-id="daaa7-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-869">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-870">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-871">535.31</span><span class="sxs-lookup"><span data-stu-id="daaa7-871">535.31</span></span></td>
<td><span data-ttu-id="daaa7-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-873">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-874">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-875">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-875">10001</span></span></td>
<td><span data-ttu-id="daaa7-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-876">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-877">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-878">178.44</span><span class="sxs-lookup"><span data-stu-id="daaa7-878">178.44</span></span></td>
<td><span data-ttu-id="daaa7-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-880">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-880">CC003</span></span></td>
<td><span data-ttu-id="daaa7-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-881">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-882">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-882">10001</span></span></td>
<td><span data-ttu-id="daaa7-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-883">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-884">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="daaa7-885">-5,982.83</span></span></td>
<td><span data-ttu-id="daaa7-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-887">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-888">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-889">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-889">10001</span></span></td>
<td><span data-ttu-id="daaa7-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-890">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-891">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="daaa7-892">4,487.12</span></span></td>
<td><span data-ttu-id="daaa7-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-894">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-895">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-896">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-896">10001</span></span></td>
<td><span data-ttu-id="daaa7-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-897">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-898">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="daaa7-899">1,495.71</span></span></td>
<td><span data-ttu-id="daaa7-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-901">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-901">CC003</span></span></td>
<td><span data-ttu-id="daaa7-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-902">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-903">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-903">10001</span></span></td>
<td><span data-ttu-id="daaa7-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-904">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-905">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="daaa7-906">-286.25</span></span></td>
<td><span data-ttu-id="daaa7-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-908">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-909">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-910">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-910">10001</span></span></td>
<td><span data-ttu-id="daaa7-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-911">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-912">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-913">241.05</span><span class="sxs-lookup"><span data-stu-id="daaa7-913">241.05</span></span></td>
<td><span data-ttu-id="daaa7-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-915">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-916">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-917">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-917">10001</span></span></td>
<td><span data-ttu-id="daaa7-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-918">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-919">Fixed cost</span></span></td>
<td><span data-ttu-id="daaa7-920">45.20</span><span class="sxs-lookup"><span data-stu-id="daaa7-920">45.20</span></span></td>
<td><span data-ttu-id="daaa7-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-922">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-922">CC003</span></span></td>
<td><span data-ttu-id="daaa7-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="daaa7-923">Assembly</span></span></td>
<td><span data-ttu-id="daaa7-924">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-924">10001</span></span></td>
<td><span data-ttu-id="daaa7-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-925">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-926">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="daaa7-927">-2,977.17</span></span></td>
<td><span data-ttu-id="daaa7-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-929">Prod 1</span></span></td>
<td><span data-ttu-id="daaa7-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-930">Product 1</span></span></td>
<td><span data-ttu-id="daaa7-931">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-931">10001</span></span></td>
<td><span data-ttu-id="daaa7-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-932">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-933">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="daaa7-934">2,507.09</span></span></td>
<td><span data-ttu-id="daaa7-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="daaa7-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-936">Prod 2</span></span></td>
<td><span data-ttu-id="daaa7-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="daaa7-937">Product 2</span></span></td>
<td><span data-ttu-id="daaa7-938">10001</span><span class="sxs-lookup"><span data-stu-id="daaa7-938">10001</span></span></td>
<td><span data-ttu-id="daaa7-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-939">Electricity</span></span></td>
<td><span data-ttu-id="daaa7-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-940">Variable cost</span></span></td>
<td><span data-ttu-id="daaa7-941">470.08</span><span class="sxs-lookup"><span data-stu-id="daaa7-941">470.08</span></span></td>
<td><span data-ttu-id="daaa7-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="daaa7-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="daaa7-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="daaa7-943">Conclusion</span></span>
<span data-ttu-id="daaa7-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="daaa7-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="daaa7-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="daaa7-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="daaa7-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="daaa7-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="daaa7-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="daaa7-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="daaa7-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="daaa7-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="daaa7-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="daaa7-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="daaa7-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="daaa7-951">CC099</span><span class="sxs-lookup"><span data-stu-id="daaa7-951">CC099</span></span></th>
<th><span data-ttu-id="daaa7-952">CC001</span><span class="sxs-lookup"><span data-stu-id="daaa7-952">CC001</span></span></th>
<th><span data-ttu-id="daaa7-953">CC002</span><span class="sxs-lookup"><span data-stu-id="daaa7-953">CC002</span></span></th>
<th><span data-ttu-id="daaa7-954">CC003</span><span class="sxs-lookup"><span data-stu-id="daaa7-954">CC003</span></span></th>
<th><span data-ttu-id="daaa7-955">CC004</span><span class="sxs-lookup"><span data-stu-id="daaa7-955">CC004</span></span></th>
<th><span data-ttu-id="daaa7-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-956">Proj 1</span></span></th>
<th><span data-ttu-id="daaa7-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="daaa7-957">Proj 2</span></span></th>
<th><span data-ttu-id="daaa7-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-958">Prod 1</span></span></th>
<th><span data-ttu-id="daaa7-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="daaa7-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="daaa7-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="daaa7-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="daaa7-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="daaa7-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-971">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="daaa7-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-973">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-974">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-975">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-976">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-977">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-978">776.36</span><span class="sxs-lookup"><span data-stu-id="daaa7-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-979">223.64</span><span class="sxs-lookup"><span data-stu-id="daaa7-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="daaa7-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="daaa7-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-982">000</span><span class="sxs-lookup"><span data-stu-id="daaa7-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-983">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-984">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-985">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-986">0,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-987">30,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-988">10,00</span><span class="sxs-lookup"><span data-stu-id="daaa7-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="daaa7-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="daaa7-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="daaa7-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="daaa7-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="daaa7-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="daaa7-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="daaa7-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="daaa7-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="daaa7-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="daaa7-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="daaa7-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="daaa7-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="daaa7-996">Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="daaa7-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



