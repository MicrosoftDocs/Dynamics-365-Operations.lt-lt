---
title: "Pridėtinių išlaidų skaičiavimas"
description: "Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="86ac2-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86ac2-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="86ac2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="86ac2-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="86ac2-105">Term definition</span></span>
---------------

<span data-ttu-id="86ac2-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="86ac2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="86ac2-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="86ac2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="86ac2-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="86ac2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="86ac2-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="86ac2-109">Rent</span></span>
-   <span data-ttu-id="86ac2-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-110">Electricity</span></span>
-   <span data-ttu-id="86ac2-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="86ac2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="86ac2-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="86ac2-112">Overhead calculation overview</span></span>
<span data-ttu-id="86ac2-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="86ac2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="86ac2-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="86ac2-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="86ac2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="86ac2-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="86ac2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="86ac2-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="86ac2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="86ac2-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="86ac2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="86ac2-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="86ac2-119">Version type</span></span>
-   <span data-ttu-id="86ac2-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="86ac2-120">Date and time</span></span>
-   <span data-ttu-id="86ac2-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="86ac2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="86ac2-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="86ac2-122">Fiscal year</span></span>
-   <span data-ttu-id="86ac2-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-123">Fiscal period</span></span>

<span data-ttu-id="86ac2-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="86ac2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="86ac2-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="86ac2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="86ac2-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="86ac2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="86ac2-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="86ac2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="86ac2-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="86ac2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="86ac2-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="86ac2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="86ac2-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="86ac2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="86ac2-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="86ac2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="86ac2-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="86ac2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="86ac2-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="86ac2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="86ac2-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="86ac2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="86ac2-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="86ac2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="86ac2-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="86ac2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="86ac2-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="86ac2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="86ac2-140">Main account</span></span></th>
<th><span data-ttu-id="86ac2-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="86ac2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="86ac2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-143">CC099</span></span></td>
<td><span data-ttu-id="86ac2-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-144">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-145">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-145">10001</span></span></td>
<td><span data-ttu-id="86ac2-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-146">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="86ac2-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="86ac2-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="86ac2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="86ac2-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="86ac2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="86ac2-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="86ac2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="86ac2-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="86ac2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="86ac2-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="86ac2-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="86ac2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="86ac2-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="86ac2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="86ac2-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="86ac2-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="86ac2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="86ac2-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="86ac2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="86ac2-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-160">Journal</span></span></th>
<th><span data-ttu-id="86ac2-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="86ac2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="86ac2-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="86ac2-163">Versija</span><span class="sxs-lookup"><span data-stu-id="86ac2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-164">00001</span><span class="sxs-lookup"><span data-stu-id="86ac2-164">00001</span></span></td>
<td><span data-ttu-id="86ac2-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="86ac2-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="86ac2-166">Fiscal</span></span></td>
<td><span data-ttu-id="86ac2-167">2017</span><span class="sxs-lookup"><span data-stu-id="86ac2-167">2017</span></span></td>
<td><span data-ttu-id="86ac2-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-168">Period 1</span></span></td>
<td><span data-ttu-id="86ac2-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="86ac2-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="86ac2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-173">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-175">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="86ac2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-177">CC099</span></span></td>
<td><span data-ttu-id="86ac2-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-178">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-179">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-179">10001</span></span></td>
<td><span data-ttu-id="86ac2-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-180">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="86ac2-181">Unclassified</span></span></td>
<td><span data-ttu-id="86ac2-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="86ac2-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="86ac2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-185">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-187">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-187">Amount</span></span></th>
<th><span data-ttu-id="86ac2-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-189">CC099</span></span></td>
<td><span data-ttu-id="86ac2-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-190">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-191">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-191">10001</span></span></td>
<td><span data-ttu-id="86ac2-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-192">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="86ac2-193">Unclassified</span></span></td>
<td><span data-ttu-id="86ac2-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-194">10,000.00</span></span></td>
<td><span data-ttu-id="86ac2-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-196">CC099</span></span></td>
<td><span data-ttu-id="86ac2-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-197">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-198">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-198">10001</span></span></td>
<td><span data-ttu-id="86ac2-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-199">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="86ac2-200">Unclassified</span></span></td>
<td><span data-ttu-id="86ac2-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="86ac2-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-203">CC099</span></span></td>
<td><span data-ttu-id="86ac2-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-204">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-205">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-205">10001</span></span></td>
<td><span data-ttu-id="86ac2-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-206">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-208">1,000.00</span></span></td>
<td><span data-ttu-id="86ac2-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-210">CC099</span></span></td>
<td><span data-ttu-id="86ac2-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-211">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-212">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-212">10001</span></span></td>
<td><span data-ttu-id="86ac2-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-213">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-214">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-215">9,000.00</span></span></td>
<td><span data-ttu-id="86ac2-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="86ac2-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="86ac2-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="86ac2-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="86ac2-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="86ac2-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="86ac2-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="86ac2-221">Define the cost distribution rule</span></span>

<span data-ttu-id="86ac2-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="86ac2-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="86ac2-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="86ac2-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="86ac2-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="86ac2-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="86ac2-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="86ac2-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="86ac2-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="86ac2-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="86ac2-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="86ac2-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-228">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="86ac2-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-230">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-230">CC001</span></span></td>
<td><span data-ttu-id="86ac2-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-231">HR</span></span></td>
<td><span data-ttu-id="86ac2-232">1000</span><span class="sxs-lookup"><span data-stu-id="86ac2-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-233">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-233">CC002</span></span></td>
<td><span data-ttu-id="86ac2-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-234">Finance</span></span></td>
<td><span data-ttu-id="86ac2-235">6,000</span><span class="sxs-lookup"><span data-stu-id="86ac2-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-236">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-236">CC003</span></span></td>
<td><span data-ttu-id="86ac2-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-237">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-238">0</span><span class="sxs-lookup"><span data-stu-id="86ac2-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-240">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-241">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-242">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-243">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-244">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-244">CC001</span></span></td>
<td><span data-ttu-id="86ac2-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-245">HR</span></span></td>
<td><span data-ttu-id="86ac2-246">1000</span><span class="sxs-lookup"><span data-stu-id="86ac2-246">1,000</span></span></td>
<td><span data-ttu-id="86ac2-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="86ac2-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-249">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-249">CC002</span></span></td>
<td><span data-ttu-id="86ac2-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-250">Finance</span></span></td>
<td><span data-ttu-id="86ac2-251">6,000</span><span class="sxs-lookup"><span data-stu-id="86ac2-251">6,000</span></span></td>
<td><span data-ttu-id="86ac2-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="86ac2-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="86ac2-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-254">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-254">CC003</span></span></td>
<td><span data-ttu-id="86ac2-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-255">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-256">0</span><span class="sxs-lookup"><span data-stu-id="86ac2-256">0</span></span></td>
<td><span data-ttu-id="86ac2-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="86ac2-258">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="86ac2-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-261">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="86ac2-262">Formula</span></span></th>
<th><span data-ttu-id="86ac2-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-263">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-264">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-265">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-266">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-266">CC001</span></span></td>
<td><span data-ttu-id="86ac2-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-267">HR</span></span></td>
<td><span data-ttu-id="86ac2-268">{1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="86ac2-269">1</span><span class="sxs-lookup"><span data-stu-id="86ac2-269">1</span></span></td>
<td><span data-ttu-id="86ac2-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="86ac2-271">500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-272">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-272">CC002</span></span></td>
<td><span data-ttu-id="86ac2-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-273">Finance</span></span></td>
<td><span data-ttu-id="86ac2-274">{6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="86ac2-275">1</span><span class="sxs-lookup"><span data-stu-id="86ac2-275">1</span></span></td>
<td><span data-ttu-id="86ac2-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="86ac2-277">500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-278">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-278">CC003</span></span></td>
<td><span data-ttu-id="86ac2-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-279">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-280">{0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="86ac2-281">0</span><span class="sxs-lookup"><span data-stu-id="86ac2-281">0</span></span></td>
<td><span data-ttu-id="86ac2-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="86ac2-283">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="86ac2-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-285">Journal</span></span></th>
<th><span data-ttu-id="86ac2-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="86ac2-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="86ac2-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="86ac2-288">Versija</span><span class="sxs-lookup"><span data-stu-id="86ac2-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-289">00002</span><span class="sxs-lookup"><span data-stu-id="86ac2-289">00002</span></span></td>
<td><span data-ttu-id="86ac2-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="86ac2-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="86ac2-291">Fiscal</span></span></td>
<td><span data-ttu-id="86ac2-292">2017</span><span class="sxs-lookup"><span data-stu-id="86ac2-292">2017</span></span></td>
<td><span data-ttu-id="86ac2-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-293">Period 1</span></span></td>
<td><span data-ttu-id="86ac2-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="86ac2-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="86ac2-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-298">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-299">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-300">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-302">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-302">CC099</span></span></td>
<td><span data-ttu-id="86ac2-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-303">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-304">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-304">10001</span></span></td>
<td><span data-ttu-id="86ac2-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-305">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-306">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-309">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-309">CC099</span></span></td>
<td><span data-ttu-id="86ac2-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-310">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-311">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-311">10001</span></span></td>
<td><span data-ttu-id="86ac2-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-312">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-313">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="86ac2-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="86ac2-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-317">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-318">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-319">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-319">Amount</span></span></th>
<th><span data-ttu-id="86ac2-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-321">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-321">CC099</span></span></td>
<td><span data-ttu-id="86ac2-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-322">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-323">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-323">10001</span></span></td>
<td><span data-ttu-id="86ac2-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-324">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-325">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-326">-1,000.00</span></span></td>
<td><span data-ttu-id="86ac2-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-328">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-328">CC001</span></span></td>
<td><span data-ttu-id="86ac2-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-329">HR</span></span></td>
<td><span data-ttu-id="86ac2-330">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-330">10001</span></span></td>
<td><span data-ttu-id="86ac2-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-331">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-332">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-333">500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-333">500.00</span></span></td>
<td><span data-ttu-id="86ac2-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-335">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-335">CC002</span></span></td>
<td><span data-ttu-id="86ac2-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-336">Finance</span></span></td>
<td><span data-ttu-id="86ac2-337">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-337">10001</span></span></td>
<td><span data-ttu-id="86ac2-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-338">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-339">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-340">500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-340">500.00</span></span></td>
<td><span data-ttu-id="86ac2-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-342">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-342">CC099</span></span></td>
<td><span data-ttu-id="86ac2-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="86ac2-343">Default cost center</span></span></td>
<td><span data-ttu-id="86ac2-344">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-344">10001</span></span></td>
<td><span data-ttu-id="86ac2-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-345">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-346">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-347">-9,000.00</span></span></td>
<td><span data-ttu-id="86ac2-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-349">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-349">CC001</span></span></td>
<td><span data-ttu-id="86ac2-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-350">HR</span></span></td>
<td><span data-ttu-id="86ac2-351">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-351">10001</span></span></td>
<td><span data-ttu-id="86ac2-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-352">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-353">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-354">1,285.71</span></span></td>
<td><span data-ttu-id="86ac2-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-356">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-356">CC002</span></span></td>
<td><span data-ttu-id="86ac2-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-357">Finance</span></span></td>
<td><span data-ttu-id="86ac2-358">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-358">10001</span></span></td>
<td><span data-ttu-id="86ac2-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-359">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-360">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="86ac2-361">7,714.29</span></span></td>
<td><span data-ttu-id="86ac2-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="86ac2-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="86ac2-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="86ac2-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="86ac2-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="86ac2-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="86ac2-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="86ac2-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="86ac2-367">Define the overhead rate</span></span>

<span data-ttu-id="86ac2-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="86ac2-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-370">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="86ac2-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-372">Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-373">Project 1</span></span></td>
<td><span data-ttu-id="86ac2-374">3</span><span class="sxs-lookup"><span data-stu-id="86ac2-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-375">Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-376">Project 2</span></span></td>
<td><span data-ttu-id="86ac2-377">1</span><span class="sxs-lookup"><span data-stu-id="86ac2-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="86ac2-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-379">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-380">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-381">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="86ac2-382">Units</span></span></th>
<th><span data-ttu-id="86ac2-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="86ac2-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-384">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-384">CC001</span></span></td>
<td><span data-ttu-id="86ac2-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-385">HR</span></span></td>
<td><span data-ttu-id="86ac2-386">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-386">10001</span></span></td>
<td><span data-ttu-id="86ac2-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-387">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-388">1</span><span class="sxs-lookup"><span data-stu-id="86ac2-388">1</span></span></td>
<td><span data-ttu-id="86ac2-389">10</span><span class="sxs-lookup"><span data-stu-id="86ac2-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-391">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-392">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-393">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-394">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-395">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-396">Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-397">Project 1</span></span></td>
<td><span data-ttu-id="86ac2-398">3</span><span class="sxs-lookup"><span data-stu-id="86ac2-398">3</span></span></td>
<td><span data-ttu-id="86ac2-399">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-399">10001</span></span></td>
<td><span data-ttu-id="86ac2-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="86ac2-401">30,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-402">Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-403">Project 2</span></span></td>
<td><span data-ttu-id="86ac2-404">1</span><span class="sxs-lookup"><span data-stu-id="86ac2-404">1</span></span></td>
<td><span data-ttu-id="86ac2-405">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-405">10001</span></span></td>
<td><span data-ttu-id="86ac2-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="86ac2-407">10,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="86ac2-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-409">Journal</span></span></th>
<th><span data-ttu-id="86ac2-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="86ac2-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="86ac2-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="86ac2-412">Versija</span><span class="sxs-lookup"><span data-stu-id="86ac2-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-413">00003</span><span class="sxs-lookup"><span data-stu-id="86ac2-413">00003</span></span></td>
<td><span data-ttu-id="86ac2-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="86ac2-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="86ac2-415">Fiscal</span></span></td>
<td><span data-ttu-id="86ac2-416">2017</span><span class="sxs-lookup"><span data-stu-id="86ac2-416">2017</span></span></td>
<td><span data-ttu-id="86ac2-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-417">Period 1</span></span></td>
<td><span data-ttu-id="86ac2-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="86ac2-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="86ac2-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-421">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-424">Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-426">3,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-428">Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-430">1,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="86ac2-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="86ac2-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-433">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-434">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-435">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-435">Amount</span></span></th>
<th><span data-ttu-id="86ac2-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="86ac2-437">CC0001</span></span></td>
<td><span data-ttu-id="86ac2-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-438">HR</span></span></td>
<td><span data-ttu-id="86ac2-439">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-439">10001</span></span></td>
<td><span data-ttu-id="86ac2-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-440">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-441">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-442">-30.00</span></span></td>
<td><span data-ttu-id="86ac2-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-444">Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="86ac2-446">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-446">10001</span></span></td>
<td><span data-ttu-id="86ac2-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-447">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-448">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-449">30,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-449">30.00</span></span></td>
<td><span data-ttu-id="86ac2-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-451">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-451">CC001</span></span></td>
<td><span data-ttu-id="86ac2-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-452">HR</span></span></td>
<td><span data-ttu-id="86ac2-453">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-453">10001</span></span></td>
<td><span data-ttu-id="86ac2-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-454">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-455">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-456">-10.00</span></span></td>
<td><span data-ttu-id="86ac2-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-458">Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="86ac2-460">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-460">10001</span></span></td>
<td><span data-ttu-id="86ac2-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-461">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-462">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-463">10,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-463">10.00</span></span></td>
<td><span data-ttu-id="86ac2-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="86ac2-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="86ac2-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="86ac2-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="86ac2-468">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="86ac2-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="86ac2-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="86ac2-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="86ac2-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="86ac2-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="86ac2-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="86ac2-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="86ac2-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="86ac2-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="86ac2-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="86ac2-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="86ac2-475">Define the cost allocation</span></span>

<span data-ttu-id="86ac2-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="86ac2-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="86ac2-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-479">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="86ac2-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-481">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-481">CC002</span></span></td>
<td><span data-ttu-id="86ac2-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-482">Finance</span></span></td>
<td><span data-ttu-id="86ac2-483">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-484">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-484">CC003</span></span></td>
<td><span data-ttu-id="86ac2-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-485">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-486">55</span><span class="sxs-lookup"><span data-stu-id="86ac2-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-487">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-487">CC004</span></span></td>
<td><span data-ttu-id="86ac2-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-488">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-489">10</span><span class="sxs-lookup"><span data-stu-id="86ac2-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="86ac2-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-492">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="86ac2-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-494">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-494">CC003</span></span></td>
<td><span data-ttu-id="86ac2-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-495">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-496">65</span><span class="sxs-lookup"><span data-stu-id="86ac2-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-497">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-497">CC004</span></span></td>
<td><span data-ttu-id="86ac2-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-498">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-499">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="86ac2-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-502">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="86ac2-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-504">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-505">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-506">60</span><span class="sxs-lookup"><span data-stu-id="86ac2-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-507">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-508">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-509">20</span><span class="sxs-lookup"><span data-stu-id="86ac2-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="86ac2-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="86ac2-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-512">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="86ac2-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-514">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-515">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-516">80</span><span class="sxs-lookup"><span data-stu-id="86ac2-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-517">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-518">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-519">15</span><span class="sxs-lookup"><span data-stu-id="86ac2-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="86ac2-520">Programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="86ac2-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="86ac2-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="86ac2-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="86ac2-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-523">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-524">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-525">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-526">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-526">Amount</span></span></th>
<th><span data-ttu-id="86ac2-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-528">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-528">CC002</span></span></td>
<td><span data-ttu-id="86ac2-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-529">Finance</span></span></td>
<td><span data-ttu-id="86ac2-530">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-530">35</span></span></td>
<td><span data-ttu-id="86ac2-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="86ac2-532">175.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-532">175.00</span></span></td>
<td><span data-ttu-id="86ac2-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-534">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-534">CC003</span></span></td>
<td><span data-ttu-id="86ac2-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-535">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-536">55</span><span class="sxs-lookup"><span data-stu-id="86ac2-536">55</span></span></td>
<td><span data-ttu-id="86ac2-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="86ac2-538">275.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-538">275.00</span></span></td>
<td><span data-ttu-id="86ac2-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-540">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-540">CC004</span></span></td>
<td><span data-ttu-id="86ac2-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-541">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-542">10</span><span class="sxs-lookup"><span data-stu-id="86ac2-542">10</span></span></td>
<td><span data-ttu-id="86ac2-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="86ac2-544">50,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-544">50.00</span></span></td>
<td><span data-ttu-id="86ac2-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-546">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-546">CC002</span></span></td>
<td><span data-ttu-id="86ac2-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-547">Finance</span></span></td>
<td><span data-ttu-id="86ac2-548">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-548">35</span></span></td>
<td><span data-ttu-id="86ac2-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="86ac2-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="86ac2-550">436.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-550">436.00</span></span></td>
<td><span data-ttu-id="86ac2-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-552">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-552">CC003</span></span></td>
<td><span data-ttu-id="86ac2-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-553">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-554">55</span><span class="sxs-lookup"><span data-stu-id="86ac2-554">55</span></span></td>
<td><span data-ttu-id="86ac2-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="86ac2-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="86ac2-556">685.14</span><span class="sxs-lookup"><span data-stu-id="86ac2-556">685.14</span></span></td>
<td><span data-ttu-id="86ac2-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-558">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-558">CC004</span></span></td>
<td><span data-ttu-id="86ac2-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-559">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-560">10</span><span class="sxs-lookup"><span data-stu-id="86ac2-560">10</span></span></td>
<td><span data-ttu-id="86ac2-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="86ac2-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="86ac2-562">124.57</span><span class="sxs-lookup"><span data-stu-id="86ac2-562">124.57</span></span></td>
<td><span data-ttu-id="86ac2-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-565">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-566">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-567">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-568">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-568">Amount</span></span></th>
<th><span data-ttu-id="86ac2-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-570">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-570">CC003</span></span></td>
<td><span data-ttu-id="86ac2-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-571">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-572">65</span><span class="sxs-lookup"><span data-stu-id="86ac2-572">65</span></span></td>
<td><span data-ttu-id="86ac2-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="86ac2-574">438.75</span><span class="sxs-lookup"><span data-stu-id="86ac2-574">438.75</span></span></td>
<td><span data-ttu-id="86ac2-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-576">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-576">CC004</span></span></td>
<td><span data-ttu-id="86ac2-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-577">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-578">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-578">35</span></span></td>
<td><span data-ttu-id="86ac2-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="86ac2-580">236.25</span><span class="sxs-lookup"><span data-stu-id="86ac2-580">236.25</span></span></td>
<td><span data-ttu-id="86ac2-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-582">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-582">CC003</span></span></td>
<td><span data-ttu-id="86ac2-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-583">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-584">65</span><span class="sxs-lookup"><span data-stu-id="86ac2-584">65</span></span></td>
<td><span data-ttu-id="86ac2-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="86ac2-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="86ac2-586">5,297.69</span></span></td>
<td><span data-ttu-id="86ac2-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-588">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-588">CC004</span></span></td>
<td><span data-ttu-id="86ac2-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-589">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-590">35</span><span class="sxs-lookup"><span data-stu-id="86ac2-590">35</span></span></td>
<td><span data-ttu-id="86ac2-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="86ac2-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="86ac2-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="86ac2-592">2,852.60</span></span></td>
<td><span data-ttu-id="86ac2-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-595">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-596">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-597">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-598">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-598">Amount</span></span></th>
<th><span data-ttu-id="86ac2-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-600">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-601">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-602">60</span><span class="sxs-lookup"><span data-stu-id="86ac2-602">60</span></span></td>
<td><span data-ttu-id="86ac2-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="86ac2-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="86ac2-604">535.31</span><span class="sxs-lookup"><span data-stu-id="86ac2-604">535.31</span></span></td>
<td><span data-ttu-id="86ac2-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-606">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-607">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-608">20</span><span class="sxs-lookup"><span data-stu-id="86ac2-608">20</span></span></td>
<td><span data-ttu-id="86ac2-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="86ac2-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="86ac2-610">178.44</span><span class="sxs-lookup"><span data-stu-id="86ac2-610">178.44</span></span></td>
<td><span data-ttu-id="86ac2-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-612">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-613">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-614">60</span><span class="sxs-lookup"><span data-stu-id="86ac2-614">60</span></span></td>
<td><span data-ttu-id="86ac2-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="86ac2-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="86ac2-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="86ac2-616">4,487.12</span></span></td>
<td><span data-ttu-id="86ac2-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-618">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-619">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-620">20</span><span class="sxs-lookup"><span data-stu-id="86ac2-620">20</span></span></td>
<td><span data-ttu-id="86ac2-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="86ac2-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="86ac2-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-622">1,495.71</span></span></td>
<td><span data-ttu-id="86ac2-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="86ac2-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-625">Cost object</span></span></th>
<th><span data-ttu-id="86ac2-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="86ac2-626">Magnitude</span></span></th>
<th><span data-ttu-id="86ac2-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="86ac2-627">Allocation factor</span></span></th>
<th><span data-ttu-id="86ac2-628">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-628">Amount</span></span></th>
<th><span data-ttu-id="86ac2-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-630">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-631">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-632">80</span><span class="sxs-lookup"><span data-stu-id="86ac2-632">80</span></span></td>
<td><span data-ttu-id="86ac2-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="86ac2-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="86ac2-634">241.05</span><span class="sxs-lookup"><span data-stu-id="86ac2-634">241.05</span></span></td>
<td><span data-ttu-id="86ac2-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-636">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-637">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-638">15</span><span class="sxs-lookup"><span data-stu-id="86ac2-638">15</span></span></td>
<td><span data-ttu-id="86ac2-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="86ac2-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="86ac2-640">45.20</span><span class="sxs-lookup"><span data-stu-id="86ac2-640">45.20</span></span></td>
<td><span data-ttu-id="86ac2-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-642">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-643">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-644">80</span><span class="sxs-lookup"><span data-stu-id="86ac2-644">80</span></span></td>
<td><span data-ttu-id="86ac2-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="86ac2-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="86ac2-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="86ac2-646">2,507.09</span></span></td>
<td><span data-ttu-id="86ac2-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-648">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-649">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-650">15</span><span class="sxs-lookup"><span data-stu-id="86ac2-650">15</span></span></td>
<td><span data-ttu-id="86ac2-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="86ac2-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="86ac2-652">470.08</span><span class="sxs-lookup"><span data-stu-id="86ac2-652">470.08</span></span></td>
<td><span data-ttu-id="86ac2-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="86ac2-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="86ac2-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-655">Journal</span></span></th>
<th><span data-ttu-id="86ac2-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="86ac2-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="86ac2-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="86ac2-658">Versija</span><span class="sxs-lookup"><span data-stu-id="86ac2-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-659">00004</span><span class="sxs-lookup"><span data-stu-id="86ac2-659">00004</span></span></td>
<td><span data-ttu-id="86ac2-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="86ac2-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="86ac2-661">Fiscal</span></span></td>
<td><span data-ttu-id="86ac2-662">2017</span><span class="sxs-lookup"><span data-stu-id="86ac2-662">2017</span></span></td>
<td><span data-ttu-id="86ac2-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-663">Period 1</span></span></td>
<td><span data-ttu-id="86ac2-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="86ac2-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="86ac2-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="86ac2-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86ac2-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-668">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-669">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-670">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-672">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-672">CC001</span></span></td>
<td><span data-ttu-id="86ac2-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-673">HR</span></span></td>
<td><span data-ttu-id="86ac2-674">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-674">10001</span></span></td>
<td><span data-ttu-id="86ac2-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-675">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-676">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-677">500,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-679">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-679">CC001</span></span></td>
<td><span data-ttu-id="86ac2-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-680">HR</span></span></td>
<td><span data-ttu-id="86ac2-681">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-681">10001</span></span></td>
<td><span data-ttu-id="86ac2-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-682">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-683">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-686">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-686">CC002</span></span></td>
<td><span data-ttu-id="86ac2-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-687">Finance</span></span></td>
<td><span data-ttu-id="86ac2-688">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-688">10001</span></span></td>
<td><span data-ttu-id="86ac2-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-689">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-690">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-691">675.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-693">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-693">CC002</span></span></td>
<td><span data-ttu-id="86ac2-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-694">Finance</span></span></td>
<td><span data-ttu-id="86ac2-695">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-695">10001</span></span></td>
<td><span data-ttu-id="86ac2-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-696">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-697">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="86ac2-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-700">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-700">CC003</span></span></td>
<td><span data-ttu-id="86ac2-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-701">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-702">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-702">10001</span></span></td>
<td><span data-ttu-id="86ac2-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-703">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-704">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-705">713.75</span><span class="sxs-lookup"><span data-stu-id="86ac2-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-707">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-707">CC003</span></span></td>
<td><span data-ttu-id="86ac2-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-708">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-709">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-709">10001</span></span></td>
<td><span data-ttu-id="86ac2-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-710">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-711">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="86ac2-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-714">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-714">CC003</span></span></td>
<td><span data-ttu-id="86ac2-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-715">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-716">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-716">10001</span></span></td>
<td><span data-ttu-id="86ac2-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-717">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-718">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-719">286.25</span><span class="sxs-lookup"><span data-stu-id="86ac2-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-721">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-721">CC003</span></span></td>
<td><span data-ttu-id="86ac2-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-722">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-723">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-723">10001</span></span></td>
<td><span data-ttu-id="86ac2-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-724">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-725">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="86ac2-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-728">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-729">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-730">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-730">10001</span></span></td>
<td><span data-ttu-id="86ac2-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-731">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-732">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-733">776.36</span><span class="sxs-lookup"><span data-stu-id="86ac2-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-735">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-736">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-737">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-737">10001</span></span></td>
<td><span data-ttu-id="86ac2-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-738">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-739">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="86ac2-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-742">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-743">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-744">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-744">10001</span></span></td>
<td><span data-ttu-id="86ac2-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-745">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-746">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-747">223.64</span><span class="sxs-lookup"><span data-stu-id="86ac2-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="86ac2-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-749">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-750">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-751">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-751">10001</span></span></td>
<td><span data-ttu-id="86ac2-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-752">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-753">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="86ac2-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="86ac2-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="86ac2-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="86ac2-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="86ac2-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-757">Cost element</span></span></th>
<th><span data-ttu-id="86ac2-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="86ac2-758">Cost behavior</span></span></th>
<th><span data-ttu-id="86ac2-759">Suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-759">Amount</span></span></th>
<th><span data-ttu-id="86ac2-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="86ac2-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86ac2-761">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-761">CC001</span></span></td>
<td><span data-ttu-id="86ac2-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-762">HR</span></span></td>
<td><span data-ttu-id="86ac2-763">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-763">10001</span></span></td>
<td><span data-ttu-id="86ac2-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-764">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-765">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-766">-500.00</span></span></td>
<td><span data-ttu-id="86ac2-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-768">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-768">CC002</span></span></td>
<td><span data-ttu-id="86ac2-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-769">Finance</span></span></td>
<td><span data-ttu-id="86ac2-770">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-770">10001</span></span></td>
<td><span data-ttu-id="86ac2-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-771">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-772">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-773">175.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-773">175.00</span></span></td>
<td><span data-ttu-id="86ac2-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-775">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-775">CC003</span></span></td>
<td><span data-ttu-id="86ac2-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-776">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-777">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-777">10001</span></span></td>
<td><span data-ttu-id="86ac2-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-778">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-779">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-780">275.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-780">275.00</span></span></td>
<td><span data-ttu-id="86ac2-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-782">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-782">CC004</span></span></td>
<td><span data-ttu-id="86ac2-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-783">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-784">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-784">10001</span></span></td>
<td><span data-ttu-id="86ac2-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-785">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-786">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-787">50,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-787">50,00</span></span></td>
<td><span data-ttu-id="86ac2-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-789">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-789">CC001</span></span></td>
<td><span data-ttu-id="86ac2-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="86ac2-790">HR</span></span></td>
<td><span data-ttu-id="86ac2-791">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-791">10001</span></span></td>
<td><span data-ttu-id="86ac2-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-792">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-793">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-794">-1,245.71</span></span></td>
<td><span data-ttu-id="86ac2-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-796">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-796">CC002</span></span></td>
<td><span data-ttu-id="86ac2-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-797">Finance</span></span></td>
<td><span data-ttu-id="86ac2-798">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-798">10001</span></span></td>
<td><span data-ttu-id="86ac2-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-799">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-800">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-801">436.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-801">436.00</span></span></td>
<td><span data-ttu-id="86ac2-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-803">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-803">CC003</span></span></td>
<td><span data-ttu-id="86ac2-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-804">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-805">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-805">10001</span></span></td>
<td><span data-ttu-id="86ac2-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-806">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-807">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-808">685.14</span><span class="sxs-lookup"><span data-stu-id="86ac2-808">685.14</span></span></td>
<td><span data-ttu-id="86ac2-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-810">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-810">CC004</span></span></td>
<td><span data-ttu-id="86ac2-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-811">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-812">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-812">10001</span></span></td>
<td><span data-ttu-id="86ac2-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-813">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-814">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-815">124.57</span><span class="sxs-lookup"><span data-stu-id="86ac2-815">124.57</span></span></td>
<td><span data-ttu-id="86ac2-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-817">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-817">CC002</span></span></td>
<td><span data-ttu-id="86ac2-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-818">Finance</span></span></td>
<td><span data-ttu-id="86ac2-819">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-819">10001</span></span></td>
<td><span data-ttu-id="86ac2-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-820">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-821">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="86ac2-822">-675.00</span></span></td>
<td><span data-ttu-id="86ac2-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-824">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-824">CC003</span></span></td>
<td><span data-ttu-id="86ac2-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-825">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-826">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-826">10001</span></span></td>
<td><span data-ttu-id="86ac2-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-827">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-828">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-829">438.75</span><span class="sxs-lookup"><span data-stu-id="86ac2-829">438.75</span></span></td>
<td><span data-ttu-id="86ac2-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-831">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-831">CC004</span></span></td>
<td><span data-ttu-id="86ac2-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-832">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-833">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-833">10001</span></span></td>
<td><span data-ttu-id="86ac2-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-834">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-835">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-836">236.25</span><span class="sxs-lookup"><span data-stu-id="86ac2-836">236.25</span></span></td>
<td><span data-ttu-id="86ac2-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-838">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-838">CC002</span></span></td>
<td><span data-ttu-id="86ac2-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="86ac2-839">Finance</span></span></td>
<td><span data-ttu-id="86ac2-840">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-840">10001</span></span></td>
<td><span data-ttu-id="86ac2-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-841">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-842">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="86ac2-843">-8,150.29</span></span></td>
<td><span data-ttu-id="86ac2-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-845">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-845">CC003</span></span></td>
<td><span data-ttu-id="86ac2-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-846">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-847">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-847">10001</span></span></td>
<td><span data-ttu-id="86ac2-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-848">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-849">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="86ac2-850">5,297.69</span></span></td>
<td><span data-ttu-id="86ac2-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-852">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-852">CC004</span></span></td>
<td><span data-ttu-id="86ac2-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="86ac2-853">Packaging</span></span></td>
<td><span data-ttu-id="86ac2-854">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-854">10001</span></span></td>
<td><span data-ttu-id="86ac2-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-855">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-856">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="86ac2-857">2,852.60</span></span></td>
<td><span data-ttu-id="86ac2-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-859">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-859">CC003</span></span></td>
<td><span data-ttu-id="86ac2-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-860">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-861">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-861">10001</span></span></td>
<td><span data-ttu-id="86ac2-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-862">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-863">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="86ac2-864">-713.75</span></span></td>
<td><span data-ttu-id="86ac2-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-866">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-867">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-868">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-868">10001</span></span></td>
<td><span data-ttu-id="86ac2-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-869">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-870">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-871">535.31</span><span class="sxs-lookup"><span data-stu-id="86ac2-871">535.31</span></span></td>
<td><span data-ttu-id="86ac2-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-873">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-874">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-875">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-875">10001</span></span></td>
<td><span data-ttu-id="86ac2-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-876">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-877">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-878">178.44</span><span class="sxs-lookup"><span data-stu-id="86ac2-878">178.44</span></span></td>
<td><span data-ttu-id="86ac2-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-880">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-880">CC003</span></span></td>
<td><span data-ttu-id="86ac2-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-881">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-882">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-882">10001</span></span></td>
<td><span data-ttu-id="86ac2-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-883">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-884">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="86ac2-885">-5,982.83</span></span></td>
<td><span data-ttu-id="86ac2-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-887">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-888">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-889">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-889">10001</span></span></td>
<td><span data-ttu-id="86ac2-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-890">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-891">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="86ac2-892">4,487.12</span></span></td>
<td><span data-ttu-id="86ac2-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-894">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-895">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-896">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-896">10001</span></span></td>
<td><span data-ttu-id="86ac2-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-897">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-898">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="86ac2-899">1,495.71</span></span></td>
<td><span data-ttu-id="86ac2-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-901">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-901">CC003</span></span></td>
<td><span data-ttu-id="86ac2-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-902">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-903">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-903">10001</span></span></td>
<td><span data-ttu-id="86ac2-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-904">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-905">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="86ac2-906">-286.25</span></span></td>
<td><span data-ttu-id="86ac2-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-908">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-909">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-910">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-910">10001</span></span></td>
<td><span data-ttu-id="86ac2-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-911">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-912">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-913">241.05</span><span class="sxs-lookup"><span data-stu-id="86ac2-913">241.05</span></span></td>
<td><span data-ttu-id="86ac2-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-915">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-916">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-917">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-917">10001</span></span></td>
<td><span data-ttu-id="86ac2-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-918">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-919">Fixed cost</span></span></td>
<td><span data-ttu-id="86ac2-920">45.20</span><span class="sxs-lookup"><span data-stu-id="86ac2-920">45.20</span></span></td>
<td><span data-ttu-id="86ac2-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-922">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-922">CC003</span></span></td>
<td><span data-ttu-id="86ac2-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="86ac2-923">Assembly</span></span></td>
<td><span data-ttu-id="86ac2-924">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-924">10001</span></span></td>
<td><span data-ttu-id="86ac2-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-925">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-926">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="86ac2-927">-2,977.17</span></span></td>
<td><span data-ttu-id="86ac2-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-929">Prod 1</span></span></td>
<td><span data-ttu-id="86ac2-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-930">Product 1</span></span></td>
<td><span data-ttu-id="86ac2-931">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-931">10001</span></span></td>
<td><span data-ttu-id="86ac2-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-932">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-933">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="86ac2-934">2,507.09</span></span></td>
<td><span data-ttu-id="86ac2-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86ac2-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-936">Prod 2</span></span></td>
<td><span data-ttu-id="86ac2-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="86ac2-937">Product 2</span></span></td>
<td><span data-ttu-id="86ac2-938">10001</span><span class="sxs-lookup"><span data-stu-id="86ac2-938">10001</span></span></td>
<td><span data-ttu-id="86ac2-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-939">Electricity</span></span></td>
<td><span data-ttu-id="86ac2-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-940">Variable cost</span></span></td>
<td><span data-ttu-id="86ac2-941">470.08</span><span class="sxs-lookup"><span data-stu-id="86ac2-941">470.08</span></span></td>
<td><span data-ttu-id="86ac2-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="86ac2-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="86ac2-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="86ac2-943">Conclusion</span></span>
<span data-ttu-id="86ac2-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="86ac2-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="86ac2-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="86ac2-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="86ac2-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="86ac2-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="86ac2-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="86ac2-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="86ac2-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="86ac2-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="86ac2-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="86ac2-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="86ac2-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="86ac2-951">CC099</span><span class="sxs-lookup"><span data-stu-id="86ac2-951">CC099</span></span></th>
<th><span data-ttu-id="86ac2-952">CC001</span><span class="sxs-lookup"><span data-stu-id="86ac2-952">CC001</span></span></th>
<th><span data-ttu-id="86ac2-953">CC002</span><span class="sxs-lookup"><span data-stu-id="86ac2-953">CC002</span></span></th>
<th><span data-ttu-id="86ac2-954">CC003</span><span class="sxs-lookup"><span data-stu-id="86ac2-954">CC003</span></span></th>
<th><span data-ttu-id="86ac2-955">CC004</span><span class="sxs-lookup"><span data-stu-id="86ac2-955">CC004</span></span></th>
<th><span data-ttu-id="86ac2-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-956">Proj 1</span></span></th>
<th><span data-ttu-id="86ac2-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="86ac2-957">Proj 2</span></span></th>
<th><span data-ttu-id="86ac2-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-958">Prod 1</span></span></th>
<th><span data-ttu-id="86ac2-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="86ac2-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="86ac2-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="86ac2-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="86ac2-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="86ac2-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-971">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="86ac2-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-973">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-974">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-975">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-976">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-977">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-978">776.36</span><span class="sxs-lookup"><span data-stu-id="86ac2-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-979">223.64</span><span class="sxs-lookup"><span data-stu-id="86ac2-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="86ac2-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="86ac2-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-982">000</span><span class="sxs-lookup"><span data-stu-id="86ac2-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-983">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-984">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-985">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-986">0,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-987">30,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-988">10,00</span><span class="sxs-lookup"><span data-stu-id="86ac2-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="86ac2-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="86ac2-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="86ac2-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="86ac2-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="86ac2-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="86ac2-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="86ac2-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="86ac2-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="86ac2-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="86ac2-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="86ac2-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="86ac2-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="86ac2-996">Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="86ac2-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




