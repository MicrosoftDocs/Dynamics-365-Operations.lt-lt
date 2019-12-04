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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770809"
---
# <a name="overhead-calculation"></a><span data-ttu-id="05c76-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="05c76-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05c76-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="05c76-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="05c76-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="05c76-105">Term definition</span></span>
---------------

<span data-ttu-id="05c76-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="05c76-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="05c76-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="05c76-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="05c76-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="05c76-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="05c76-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="05c76-109">Rent</span></span>
-   <span data-ttu-id="05c76-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-110">Electricity</span></span>
-   <span data-ttu-id="05c76-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="05c76-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="05c76-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="05c76-112">Overhead calculation overview</span></span>
<span data-ttu-id="05c76-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="05c76-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="05c76-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="05c76-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="05c76-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="05c76-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="05c76-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="05c76-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="05c76-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="05c76-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="05c76-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="05c76-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="05c76-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="05c76-119">Version type</span></span>
-   <span data-ttu-id="05c76-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="05c76-120">Date and time</span></span>
-   <span data-ttu-id="05c76-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="05c76-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="05c76-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="05c76-122">Fiscal year</span></span>
-   <span data-ttu-id="05c76-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-123">Fiscal period</span></span>

<span data-ttu-id="05c76-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="05c76-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="05c76-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="05c76-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="05c76-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="05c76-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="05c76-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="05c76-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="05c76-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="05c76-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="05c76-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="05c76-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="05c76-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="05c76-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="05c76-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="05c76-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="05c76-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="05c76-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="05c76-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="05c76-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="05c76-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="05c76-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="05c76-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="05c76-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="05c76-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="05c76-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="05c76-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="05c76-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="05c76-140">Main account</span></span></th>
<th><span data-ttu-id="05c76-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="05c76-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="05c76-143">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-143">CC099</span></span></td>
<td><span data-ttu-id="05c76-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-144">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-145">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-145">10001</span></span></td>
<td><span data-ttu-id="05c76-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-146">Electricity</span></span></td>
<td><span data-ttu-id="05c76-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="05c76-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="05c76-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="05c76-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="05c76-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="05c76-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="05c76-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="05c76-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="05c76-151">Define the cost behavior rule</span></span>

<span data-ttu-id="05c76-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="05c76-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="05c76-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="05c76-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="05c76-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="05c76-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="05c76-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="05c76-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="05c76-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="05c76-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="05c76-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="05c76-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="05c76-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="05c76-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-160">Journal</span></span></th>
<th><span data-ttu-id="05c76-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="05c76-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="05c76-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="05c76-163">Versija</span><span class="sxs-lookup"><span data-stu-id="05c76-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-164">00001</span><span class="sxs-lookup"><span data-stu-id="05c76-164">00001</span></span></td>
<td><span data-ttu-id="05c76-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="05c76-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="05c76-166">Fiscal</span></span></td>
<td><span data-ttu-id="05c76-167">2017</span><span class="sxs-lookup"><span data-stu-id="05c76-167">2017</span></span></td>
<td><span data-ttu-id="05c76-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-168">Period 1</span></span></td>
<td><span data-ttu-id="05c76-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="05c76-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="05c76-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-173">Cost element</span></span></th>
<th><span data-ttu-id="05c76-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-174">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-175">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="05c76-177">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-177">CC099</span></span></td>
<td><span data-ttu-id="05c76-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-178">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-179">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-179">10001</span></span></td>
<td><span data-ttu-id="05c76-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-180">Electricity</span></span></td>
<td><span data-ttu-id="05c76-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="05c76-181">Unclassified</span></span></td>
<td><span data-ttu-id="05c76-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="05c76-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="05c76-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-185">Cost element</span></span></th>
<th><span data-ttu-id="05c76-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-186">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-187">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-187">Amount</span></span></th>
<th><span data-ttu-id="05c76-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-189">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-189">CC099</span></span></td>
<td><span data-ttu-id="05c76-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-190">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-191">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-191">10001</span></span></td>
<td><span data-ttu-id="05c76-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-192">Electricity</span></span></td>
<td><span data-ttu-id="05c76-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="05c76-193">Unclassified</span></span></td>
<td><span data-ttu-id="05c76-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-194">10,000.00</span></span></td>
<td><span data-ttu-id="05c76-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-196">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-196">CC099</span></span></td>
<td><span data-ttu-id="05c76-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-197">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-198">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-198">10001</span></span></td>
<td><span data-ttu-id="05c76-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-199">Electricity</span></span></td>
<td><span data-ttu-id="05c76-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="05c76-200">Unclassified</span></span></td>
<td><span data-ttu-id="05c76-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="05c76-201">-10,000.00</span></span></td>
<td><span data-ttu-id="05c76-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-203">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-203">CC099</span></span></td>
<td><span data-ttu-id="05c76-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-204">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-205">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-205">10001</span></span></td>
<td><span data-ttu-id="05c76-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-206">Electricity</span></span></td>
<td><span data-ttu-id="05c76-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-207">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-208">1,000.00</span></span></td>
<td><span data-ttu-id="05c76-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-210">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-210">CC099</span></span></td>
<td><span data-ttu-id="05c76-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-211">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-212">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-212">10001</span></span></td>
<td><span data-ttu-id="05c76-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-213">Electricity</span></span></td>
<td><span data-ttu-id="05c76-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-214">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="05c76-215">9,000.00</span></span></td>
<td><span data-ttu-id="05c76-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="05c76-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="05c76-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="05c76-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="05c76-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="05c76-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="05c76-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="05c76-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="05c76-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="05c76-221">Define the cost distribution rule</span></span>

<span data-ttu-id="05c76-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="05c76-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="05c76-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="05c76-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="05c76-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="05c76-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="05c76-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="05c76-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="05c76-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="05c76-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="05c76-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="05c76-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-228">Cost object</span></span></th>
<th><span data-ttu-id="05c76-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="05c76-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-230">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-230">CC001</span></span></td>
<td><span data-ttu-id="05c76-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-231">HR</span></span></td>
<td><span data-ttu-id="05c76-232">1000</span><span class="sxs-lookup"><span data-stu-id="05c76-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-233">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-233">CC002</span></span></td>
<td><span data-ttu-id="05c76-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-234">Finance</span></span></td>
<td><span data-ttu-id="05c76-235">6,000</span><span class="sxs-lookup"><span data-stu-id="05c76-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-236">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-236">CC003</span></span></td>
<td><span data-ttu-id="05c76-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-237">Assembly</span></span></td>
<td><span data-ttu-id="05c76-238">0</span><span class="sxs-lookup"><span data-stu-id="05c76-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-240">Cost object</span></span></th>
<th><span data-ttu-id="05c76-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-241">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-242">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-243">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-244">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-244">CC001</span></span></td>
<td><span data-ttu-id="05c76-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-245">HR</span></span></td>
<td><span data-ttu-id="05c76-246">1000</span><span class="sxs-lookup"><span data-stu-id="05c76-246">1,000</span></span></td>
<td><span data-ttu-id="05c76-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="05c76-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="05c76-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-249">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-249">CC002</span></span></td>
<td><span data-ttu-id="05c76-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-250">Finance</span></span></td>
<td><span data-ttu-id="05c76-251">6,000</span><span class="sxs-lookup"><span data-stu-id="05c76-251">6,000</span></span></td>
<td><span data-ttu-id="05c76-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="05c76-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="05c76-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-254">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-254">CC003</span></span></td>
<td><span data-ttu-id="05c76-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-255">Assembly</span></span></td>
<td><span data-ttu-id="05c76-256">0</span><span class="sxs-lookup"><span data-stu-id="05c76-256">0</span></span></td>
<td><span data-ttu-id="05c76-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="05c76-258">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="05c76-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="05c76-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-261">Cost object</span></span></th>
<th><span data-ttu-id="05c76-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="05c76-262">Formula</span></span></th>
<th><span data-ttu-id="05c76-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-263">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-264">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-265">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-266">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-266">CC001</span></span></td>
<td><span data-ttu-id="05c76-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-267">HR</span></span></td>
<td><span data-ttu-id="05c76-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="05c76-269">1</span><span class="sxs-lookup"><span data-stu-id="05c76-269">1</span></span></td>
<td><span data-ttu-id="05c76-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="05c76-271">500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-272">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-272">CC002</span></span></td>
<td><span data-ttu-id="05c76-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-273">Finance</span></span></td>
<td><span data-ttu-id="05c76-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="05c76-275">1</span><span class="sxs-lookup"><span data-stu-id="05c76-275">1</span></span></td>
<td><span data-ttu-id="05c76-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="05c76-277">500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-278">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-278">CC003</span></span></td>
<td><span data-ttu-id="05c76-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-279">Assembly</span></span></td>
<td><span data-ttu-id="05c76-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="05c76-281">0</span><span class="sxs-lookup"><span data-stu-id="05c76-281">0</span></span></td>
<td><span data-ttu-id="05c76-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="05c76-283">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="05c76-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-285">Journal</span></span></th>
<th><span data-ttu-id="05c76-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="05c76-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="05c76-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="05c76-288">Versija</span><span class="sxs-lookup"><span data-stu-id="05c76-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-289">00002</span><span class="sxs-lookup"><span data-stu-id="05c76-289">00002</span></span></td>
<td><span data-ttu-id="05c76-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="05c76-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="05c76-291">Fiscal</span></span></td>
<td><span data-ttu-id="05c76-292">2017</span><span class="sxs-lookup"><span data-stu-id="05c76-292">2017</span></span></td>
<td><span data-ttu-id="05c76-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-293">Period 1</span></span></td>
<td><span data-ttu-id="05c76-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="05c76-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="05c76-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-298">Cost element</span></span></th>
<th><span data-ttu-id="05c76-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-299">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-300">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-302">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-302">CC099</span></span></td>
<td><span data-ttu-id="05c76-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-303">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-304">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-304">10001</span></span></td>
<td><span data-ttu-id="05c76-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-305">Electricity</span></span></td>
<td><span data-ttu-id="05c76-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-306">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="05c76-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-309">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-309">CC099</span></span></td>
<td><span data-ttu-id="05c76-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-310">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-311">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-311">10001</span></span></td>
<td><span data-ttu-id="05c76-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-312">Electricity</span></span></td>
<td><span data-ttu-id="05c76-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-313">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="05c76-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="05c76-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="05c76-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-317">Cost element</span></span></th>
<th><span data-ttu-id="05c76-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-318">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-319">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-319">Amount</span></span></th>
<th><span data-ttu-id="05c76-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-321">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-321">CC099</span></span></td>
<td><span data-ttu-id="05c76-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-322">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-323">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-323">10001</span></span></td>
<td><span data-ttu-id="05c76-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-324">Electricity</span></span></td>
<td><span data-ttu-id="05c76-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-325">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="05c76-326">-1,000.00</span></span></td>
<td><span data-ttu-id="05c76-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-328">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-328">CC001</span></span></td>
<td><span data-ttu-id="05c76-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-329">HR</span></span></td>
<td><span data-ttu-id="05c76-330">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-330">10001</span></span></td>
<td><span data-ttu-id="05c76-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-331">Electricity</span></span></td>
<td><span data-ttu-id="05c76-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-332">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-333">500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-333">500.00</span></span></td>
<td><span data-ttu-id="05c76-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-335">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-335">CC002</span></span></td>
<td><span data-ttu-id="05c76-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-336">Finance</span></span></td>
<td><span data-ttu-id="05c76-337">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-337">10001</span></span></td>
<td><span data-ttu-id="05c76-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-338">Electricity</span></span></td>
<td><span data-ttu-id="05c76-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-339">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-340">500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-340">500.00</span></span></td>
<td><span data-ttu-id="05c76-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-342">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-342">CC099</span></span></td>
<td><span data-ttu-id="05c76-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="05c76-343">Default cost center</span></span></td>
<td><span data-ttu-id="05c76-344">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-344">10001</span></span></td>
<td><span data-ttu-id="05c76-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-345">Electricity</span></span></td>
<td><span data-ttu-id="05c76-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-346">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="05c76-347">-9,000.00</span></span></td>
<td><span data-ttu-id="05c76-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-349">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-349">CC001</span></span></td>
<td><span data-ttu-id="05c76-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-350">HR</span></span></td>
<td><span data-ttu-id="05c76-351">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-351">10001</span></span></td>
<td><span data-ttu-id="05c76-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-352">Electricity</span></span></td>
<td><span data-ttu-id="05c76-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-353">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="05c76-354">1,285.71</span></span></td>
<td><span data-ttu-id="05c76-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-356">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-356">CC002</span></span></td>
<td><span data-ttu-id="05c76-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-357">Finance</span></span></td>
<td><span data-ttu-id="05c76-358">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-358">10001</span></span></td>
<td><span data-ttu-id="05c76-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-359">Electricity</span></span></td>
<td><span data-ttu-id="05c76-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-360">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="05c76-361">7,714.29</span></span></td>
<td><span data-ttu-id="05c76-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="05c76-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="05c76-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="05c76-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="05c76-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="05c76-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="05c76-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="05c76-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05c76-367">Define the overhead rate</span></span>

<span data-ttu-id="05c76-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="05c76-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05c76-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-370">Cost object</span></span></th>
<th><span data-ttu-id="05c76-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="05c76-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-372">Proj 1</span></span></td>
<td><span data-ttu-id="05c76-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-373">Project 1</span></span></td>
<td><span data-ttu-id="05c76-374">3</span><span class="sxs-lookup"><span data-stu-id="05c76-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-375">Proj 2</span></span></td>
<td><span data-ttu-id="05c76-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-376">Project 2</span></span></td>
<td><span data-ttu-id="05c76-377">1</span><span class="sxs-lookup"><span data-stu-id="05c76-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="05c76-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-379">Cost object</span></span></th>
<th><span data-ttu-id="05c76-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-380">Cost element</span></span></th>
<th><span data-ttu-id="05c76-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-381">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="05c76-382">Units</span></span></th>
<th><span data-ttu-id="05c76-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="05c76-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-384">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-384">CC001</span></span></td>
<td><span data-ttu-id="05c76-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-385">HR</span></span></td>
<td><span data-ttu-id="05c76-386">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-386">10001</span></span></td>
<td><span data-ttu-id="05c76-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-387">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-388">1</span><span class="sxs-lookup"><span data-stu-id="05c76-388">1</span></span></td>
<td><span data-ttu-id="05c76-389">10</span><span class="sxs-lookup"><span data-stu-id="05c76-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-391">Cost object</span></span></th>
<th><span data-ttu-id="05c76-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-392">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-393">Cost element</span></span></th>
<th><span data-ttu-id="05c76-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-394">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-395">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-396">Proj 1</span></span></td>
<td><span data-ttu-id="05c76-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-397">Project 1</span></span></td>
<td><span data-ttu-id="05c76-398">3</span><span class="sxs-lookup"><span data-stu-id="05c76-398">3</span></span></td>
<td><span data-ttu-id="05c76-399">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-399">10001</span></span></td>
<td><span data-ttu-id="05c76-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="05c76-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="05c76-401">30,00</span><span class="sxs-lookup"><span data-stu-id="05c76-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-402">Proj 2</span></span></td>
<td><span data-ttu-id="05c76-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-403">Project 2</span></span></td>
<td><span data-ttu-id="05c76-404">1</span><span class="sxs-lookup"><span data-stu-id="05c76-404">1</span></span></td>
<td><span data-ttu-id="05c76-405">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-405">10001</span></span></td>
<td><span data-ttu-id="05c76-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="05c76-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="05c76-407">10,00</span><span class="sxs-lookup"><span data-stu-id="05c76-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="05c76-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-409">Journal</span></span></th>
<th><span data-ttu-id="05c76-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="05c76-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="05c76-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="05c76-412">Versija</span><span class="sxs-lookup"><span data-stu-id="05c76-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-413">00003</span><span class="sxs-lookup"><span data-stu-id="05c76-413">00003</span></span></td>
<td><span data-ttu-id="05c76-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="05c76-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="05c76-415">Fiscal</span></span></td>
<td><span data-ttu-id="05c76-416">2017</span><span class="sxs-lookup"><span data-stu-id="05c76-416">2017</span></span></td>
<td><span data-ttu-id="05c76-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-417">Period 1</span></span></td>
<td><span data-ttu-id="05c76-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="05c76-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="05c76-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-421">Cost object</span></span></th>
<th><span data-ttu-id="05c76-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-424">Proj 1</span></span></td>
<td><span data-ttu-id="05c76-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="05c76-426">3,00</span><span class="sxs-lookup"><span data-stu-id="05c76-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-428">Proj 2</span></span></td>
<td><span data-ttu-id="05c76-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="05c76-430">1,00</span><span class="sxs-lookup"><span data-stu-id="05c76-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="05c76-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="05c76-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-433">Cost element</span></span></th>
<th><span data-ttu-id="05c76-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-434">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-435">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-435">Amount</span></span></th>
<th><span data-ttu-id="05c76-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="05c76-437">CC0001</span></span></td>
<td><span data-ttu-id="05c76-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-438">HR</span></span></td>
<td><span data-ttu-id="05c76-439">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-439">10001</span></span></td>
<td><span data-ttu-id="05c76-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-440">Electricity</span></span></td>
<td><span data-ttu-id="05c76-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-441">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="05c76-442">-30.00</span></span></td>
<td><span data-ttu-id="05c76-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-444">Proj 1</span></span></td>
<td><span data-ttu-id="05c76-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="05c76-446">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-446">10001</span></span></td>
<td><span data-ttu-id="05c76-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-447">Electricity</span></span></td>
<td><span data-ttu-id="05c76-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-448">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-449">30,00</span><span class="sxs-lookup"><span data-stu-id="05c76-449">30.00</span></span></td>
<td><span data-ttu-id="05c76-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-451">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-451">CC001</span></span></td>
<td><span data-ttu-id="05c76-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-452">HR</span></span></td>
<td><span data-ttu-id="05c76-453">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-453">10001</span></span></td>
<td><span data-ttu-id="05c76-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-454">Electricity</span></span></td>
<td><span data-ttu-id="05c76-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-455">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="05c76-456">-10.00</span></span></td>
<td><span data-ttu-id="05c76-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-458">Proj 2</span></span></td>
<td><span data-ttu-id="05c76-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="05c76-460">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-460">10001</span></span></td>
<td><span data-ttu-id="05c76-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-461">Electricity</span></span></td>
<td><span data-ttu-id="05c76-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-462">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-463">10,00</span><span class="sxs-lookup"><span data-stu-id="05c76-463">10.00</span></span></td>
<td><span data-ttu-id="05c76-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="05c76-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="05c76-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="05c76-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="05c76-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="05c76-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="05c76-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="05c76-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="05c76-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="05c76-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="05c76-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="05c76-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="05c76-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="05c76-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="05c76-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="05c76-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="05c76-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="05c76-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="05c76-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="05c76-475">Define the cost allocation</span></span>

<span data-ttu-id="05c76-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="05c76-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="05c76-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="05c76-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05c76-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-479">Cost object</span></span></th>
<th><span data-ttu-id="05c76-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="05c76-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-481">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-481">CC002</span></span></td>
<td><span data-ttu-id="05c76-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-482">Finance</span></span></td>
<td><span data-ttu-id="05c76-483">35</span><span class="sxs-lookup"><span data-stu-id="05c76-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-484">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-484">CC003</span></span></td>
<td><span data-ttu-id="05c76-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-485">Assembly</span></span></td>
<td><span data-ttu-id="05c76-486">55</span><span class="sxs-lookup"><span data-stu-id="05c76-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-487">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-487">CC004</span></span></td>
<td><span data-ttu-id="05c76-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-488">Packaging</span></span></td>
<td><span data-ttu-id="05c76-489">10</span><span class="sxs-lookup"><span data-stu-id="05c76-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="05c76-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05c76-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-492">Cost object</span></span></th>
<th><span data-ttu-id="05c76-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="05c76-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-494">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-494">CC003</span></span></td>
<td><span data-ttu-id="05c76-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-495">Assembly</span></span></td>
<td><span data-ttu-id="05c76-496">65</span><span class="sxs-lookup"><span data-stu-id="05c76-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-497">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-497">CC004</span></span></td>
<td><span data-ttu-id="05c76-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-498">Packaging</span></span></td>
<td><span data-ttu-id="05c76-499">35</span><span class="sxs-lookup"><span data-stu-id="05c76-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="05c76-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05c76-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-502">Cost object</span></span></th>
<th><span data-ttu-id="05c76-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="05c76-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-504">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-505">Product 1</span></span></td>
<td><span data-ttu-id="05c76-506">60</span><span class="sxs-lookup"><span data-stu-id="05c76-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-507">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-508">Product 2</span></span></td>
<td><span data-ttu-id="05c76-509">20</span><span class="sxs-lookup"><span data-stu-id="05c76-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="05c76-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="05c76-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05c76-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-512">Cost object</span></span></th>
<th><span data-ttu-id="05c76-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="05c76-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-514">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-515">Product 1</span></span></td>
<td><span data-ttu-id="05c76-516">80</span><span class="sxs-lookup"><span data-stu-id="05c76-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-517">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-518">Product 2</span></span></td>
<td><span data-ttu-id="05c76-519">15</span><span class="sxs-lookup"><span data-stu-id="05c76-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="05c76-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="05c76-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="05c76-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="05c76-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="05c76-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-523">Cost object</span></span></th>
<th><span data-ttu-id="05c76-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-524">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-525">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-526">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-526">Amount</span></span></th>
<th><span data-ttu-id="05c76-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-528">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-528">CC002</span></span></td>
<td><span data-ttu-id="05c76-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-529">Finance</span></span></td>
<td><span data-ttu-id="05c76-530">35</span><span class="sxs-lookup"><span data-stu-id="05c76-530">35</span></span></td>
<td><span data-ttu-id="05c76-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="05c76-532">175.00</span><span class="sxs-lookup"><span data-stu-id="05c76-532">175.00</span></span></td>
<td><span data-ttu-id="05c76-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-534">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-534">CC003</span></span></td>
<td><span data-ttu-id="05c76-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-535">Assembly</span></span></td>
<td><span data-ttu-id="05c76-536">55</span><span class="sxs-lookup"><span data-stu-id="05c76-536">55</span></span></td>
<td><span data-ttu-id="05c76-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="05c76-538">275.00</span><span class="sxs-lookup"><span data-stu-id="05c76-538">275.00</span></span></td>
<td><span data-ttu-id="05c76-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-540">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-540">CC004</span></span></td>
<td><span data-ttu-id="05c76-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-541">Packaging</span></span></td>
<td><span data-ttu-id="05c76-542">10</span><span class="sxs-lookup"><span data-stu-id="05c76-542">10</span></span></td>
<td><span data-ttu-id="05c76-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="05c76-544">50,00</span><span class="sxs-lookup"><span data-stu-id="05c76-544">50.00</span></span></td>
<td><span data-ttu-id="05c76-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-546">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-546">CC002</span></span></td>
<td><span data-ttu-id="05c76-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-547">Finance</span></span></td>
<td><span data-ttu-id="05c76-548">35</span><span class="sxs-lookup"><span data-stu-id="05c76-548">35</span></span></td>
<td><span data-ttu-id="05c76-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="05c76-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="05c76-550">436.00</span><span class="sxs-lookup"><span data-stu-id="05c76-550">436.00</span></span></td>
<td><span data-ttu-id="05c76-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-552">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-552">CC003</span></span></td>
<td><span data-ttu-id="05c76-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-553">Assembly</span></span></td>
<td><span data-ttu-id="05c76-554">55</span><span class="sxs-lookup"><span data-stu-id="05c76-554">55</span></span></td>
<td><span data-ttu-id="05c76-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="05c76-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="05c76-556">685.14</span><span class="sxs-lookup"><span data-stu-id="05c76-556">685.14</span></span></td>
<td><span data-ttu-id="05c76-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-558">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-558">CC004</span></span></td>
<td><span data-ttu-id="05c76-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-559">Packaging</span></span></td>
<td><span data-ttu-id="05c76-560">10</span><span class="sxs-lookup"><span data-stu-id="05c76-560">10</span></span></td>
<td><span data-ttu-id="05c76-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="05c76-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="05c76-562">124.57</span><span class="sxs-lookup"><span data-stu-id="05c76-562">124.57</span></span></td>
<td><span data-ttu-id="05c76-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-565">Cost object</span></span></th>
<th><span data-ttu-id="05c76-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-566">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-567">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-568">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-568">Amount</span></span></th>
<th><span data-ttu-id="05c76-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-570">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-570">CC003</span></span></td>
<td><span data-ttu-id="05c76-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-571">Assembly</span></span></td>
<td><span data-ttu-id="05c76-572">65</span><span class="sxs-lookup"><span data-stu-id="05c76-572">65</span></span></td>
<td><span data-ttu-id="05c76-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="05c76-574">438.75</span><span class="sxs-lookup"><span data-stu-id="05c76-574">438.75</span></span></td>
<td><span data-ttu-id="05c76-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-576">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-576">CC004</span></span></td>
<td><span data-ttu-id="05c76-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-577">Packaging</span></span></td>
<td><span data-ttu-id="05c76-578">35</span><span class="sxs-lookup"><span data-stu-id="05c76-578">35</span></span></td>
<td><span data-ttu-id="05c76-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="05c76-580">236.25</span><span class="sxs-lookup"><span data-stu-id="05c76-580">236.25</span></span></td>
<td><span data-ttu-id="05c76-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-582">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-582">CC003</span></span></td>
<td><span data-ttu-id="05c76-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-583">Assembly</span></span></td>
<td><span data-ttu-id="05c76-584">65</span><span class="sxs-lookup"><span data-stu-id="05c76-584">65</span></span></td>
<td><span data-ttu-id="05c76-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="05c76-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="05c76-586">5,297.69</span></span></td>
<td><span data-ttu-id="05c76-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-588">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-588">CC004</span></span></td>
<td><span data-ttu-id="05c76-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-589">Packaging</span></span></td>
<td><span data-ttu-id="05c76-590">35</span><span class="sxs-lookup"><span data-stu-id="05c76-590">35</span></span></td>
<td><span data-ttu-id="05c76-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="05c76-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="05c76-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="05c76-592">2,852.60</span></span></td>
<td><span data-ttu-id="05c76-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-595">Cost object</span></span></th>
<th><span data-ttu-id="05c76-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-596">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-597">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-598">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-598">Amount</span></span></th>
<th><span data-ttu-id="05c76-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-600">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-601">Product 1</span></span></td>
<td><span data-ttu-id="05c76-602">60</span><span class="sxs-lookup"><span data-stu-id="05c76-602">60</span></span></td>
<td><span data-ttu-id="05c76-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="05c76-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="05c76-604">535.31</span><span class="sxs-lookup"><span data-stu-id="05c76-604">535.31</span></span></td>
<td><span data-ttu-id="05c76-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-606">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-607">Product 2</span></span></td>
<td><span data-ttu-id="05c76-608">20</span><span class="sxs-lookup"><span data-stu-id="05c76-608">20</span></span></td>
<td><span data-ttu-id="05c76-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="05c76-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="05c76-610">178.44</span><span class="sxs-lookup"><span data-stu-id="05c76-610">178.44</span></span></td>
<td><span data-ttu-id="05c76-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-612">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-613">Product 1</span></span></td>
<td><span data-ttu-id="05c76-614">60</span><span class="sxs-lookup"><span data-stu-id="05c76-614">60</span></span></td>
<td><span data-ttu-id="05c76-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="05c76-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="05c76-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="05c76-616">4,487.12</span></span></td>
<td><span data-ttu-id="05c76-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-618">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-619">Product 2</span></span></td>
<td><span data-ttu-id="05c76-620">20</span><span class="sxs-lookup"><span data-stu-id="05c76-620">20</span></span></td>
<td><span data-ttu-id="05c76-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="05c76-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="05c76-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="05c76-622">1,495.71</span></span></td>
<td><span data-ttu-id="05c76-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="05c76-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="05c76-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-625">Cost object</span></span></th>
<th><span data-ttu-id="05c76-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="05c76-626">Magnitude</span></span></th>
<th><span data-ttu-id="05c76-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="05c76-627">Allocation factor</span></span></th>
<th><span data-ttu-id="05c76-628">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-628">Amount</span></span></th>
<th><span data-ttu-id="05c76-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-630">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-631">Product 1</span></span></td>
<td><span data-ttu-id="05c76-632">80</span><span class="sxs-lookup"><span data-stu-id="05c76-632">80</span></span></td>
<td><span data-ttu-id="05c76-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="05c76-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="05c76-634">241.05</span><span class="sxs-lookup"><span data-stu-id="05c76-634">241.05</span></span></td>
<td><span data-ttu-id="05c76-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-636">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-637">Product 2</span></span></td>
<td><span data-ttu-id="05c76-638">15</span><span class="sxs-lookup"><span data-stu-id="05c76-638">15</span></span></td>
<td><span data-ttu-id="05c76-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="05c76-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="05c76-640">45.20</span><span class="sxs-lookup"><span data-stu-id="05c76-640">45.20</span></span></td>
<td><span data-ttu-id="05c76-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-642">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-643">Product 1</span></span></td>
<td><span data-ttu-id="05c76-644">80</span><span class="sxs-lookup"><span data-stu-id="05c76-644">80</span></span></td>
<td><span data-ttu-id="05c76-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="05c76-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="05c76-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="05c76-646">2,507.09</span></span></td>
<td><span data-ttu-id="05c76-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-648">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-649">Product 2</span></span></td>
<td><span data-ttu-id="05c76-650">15</span><span class="sxs-lookup"><span data-stu-id="05c76-650">15</span></span></td>
<td><span data-ttu-id="05c76-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="05c76-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="05c76-652">470.08</span><span class="sxs-lookup"><span data-stu-id="05c76-652">470.08</span></span></td>
<td><span data-ttu-id="05c76-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="05c76-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="05c76-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-655">Journal</span></span></th>
<th><span data-ttu-id="05c76-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="05c76-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="05c76-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="05c76-658">Versija</span><span class="sxs-lookup"><span data-stu-id="05c76-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-659">00004</span><span class="sxs-lookup"><span data-stu-id="05c76-659">00004</span></span></td>
<td><span data-ttu-id="05c76-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="05c76-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="05c76-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="05c76-661">Fiscal</span></span></td>
<td><span data-ttu-id="05c76-662">2017</span><span class="sxs-lookup"><span data-stu-id="05c76-662">2017</span></span></td>
<td><span data-ttu-id="05c76-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-663">Period 1</span></span></td>
<td><span data-ttu-id="05c76-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="05c76-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="05c76-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="05c76-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="05c76-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-668">Cost element</span></span></th>
<th><span data-ttu-id="05c76-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-669">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-670">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-672">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-672">CC001</span></span></td>
<td><span data-ttu-id="05c76-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-673">HR</span></span></td>
<td><span data-ttu-id="05c76-674">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-674">10001</span></span></td>
<td><span data-ttu-id="05c76-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-675">Electricity</span></span></td>
<td><span data-ttu-id="05c76-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-676">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-677">500,00</span><span class="sxs-lookup"><span data-stu-id="05c76-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-679">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-679">CC001</span></span></td>
<td><span data-ttu-id="05c76-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-680">HR</span></span></td>
<td><span data-ttu-id="05c76-681">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-681">10001</span></span></td>
<td><span data-ttu-id="05c76-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-682">Electricity</span></span></td>
<td><span data-ttu-id="05c76-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-683">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="05c76-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-686">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-686">CC002</span></span></td>
<td><span data-ttu-id="05c76-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-687">Finance</span></span></td>
<td><span data-ttu-id="05c76-688">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-688">10001</span></span></td>
<td><span data-ttu-id="05c76-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-689">Electricity</span></span></td>
<td><span data-ttu-id="05c76-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-690">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-691">675.00</span><span class="sxs-lookup"><span data-stu-id="05c76-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-693">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-693">CC002</span></span></td>
<td><span data-ttu-id="05c76-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-694">Finance</span></span></td>
<td><span data-ttu-id="05c76-695">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-695">10001</span></span></td>
<td><span data-ttu-id="05c76-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-696">Electricity</span></span></td>
<td><span data-ttu-id="05c76-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-697">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="05c76-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-700">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-700">CC003</span></span></td>
<td><span data-ttu-id="05c76-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-701">Assembly</span></span></td>
<td><span data-ttu-id="05c76-702">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-702">10001</span></span></td>
<td><span data-ttu-id="05c76-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-703">Electricity</span></span></td>
<td><span data-ttu-id="05c76-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-704">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-705">713.75</span><span class="sxs-lookup"><span data-stu-id="05c76-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-707">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-707">CC003</span></span></td>
<td><span data-ttu-id="05c76-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-708">Assembly</span></span></td>
<td><span data-ttu-id="05c76-709">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-709">10001</span></span></td>
<td><span data-ttu-id="05c76-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-710">Electricity</span></span></td>
<td><span data-ttu-id="05c76-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-711">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="05c76-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-714">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-714">CC003</span></span></td>
<td><span data-ttu-id="05c76-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-715">Packaging</span></span></td>
<td><span data-ttu-id="05c76-716">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-716">10001</span></span></td>
<td><span data-ttu-id="05c76-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-717">Electricity</span></span></td>
<td><span data-ttu-id="05c76-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-718">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-719">286.25</span><span class="sxs-lookup"><span data-stu-id="05c76-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-721">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-721">CC003</span></span></td>
<td><span data-ttu-id="05c76-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-722">Packaging</span></span></td>
<td><span data-ttu-id="05c76-723">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-723">10001</span></span></td>
<td><span data-ttu-id="05c76-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-724">Electricity</span></span></td>
<td><span data-ttu-id="05c76-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-725">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="05c76-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-728">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-729">Product 1</span></span></td>
<td><span data-ttu-id="05c76-730">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-730">10001</span></span></td>
<td><span data-ttu-id="05c76-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-731">Electricity</span></span></td>
<td><span data-ttu-id="05c76-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-732">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-733">776.36</span><span class="sxs-lookup"><span data-stu-id="05c76-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-735">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-736">Product 1</span></span></td>
<td><span data-ttu-id="05c76-737">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-737">10001</span></span></td>
<td><span data-ttu-id="05c76-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-738">Electricity</span></span></td>
<td><span data-ttu-id="05c76-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-739">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="05c76-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-742">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-743">Product 1</span></span></td>
<td><span data-ttu-id="05c76-744">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-744">10001</span></span></td>
<td><span data-ttu-id="05c76-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-745">Electricity</span></span></td>
<td><span data-ttu-id="05c76-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-746">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-747">223.64</span><span class="sxs-lookup"><span data-stu-id="05c76-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="05c76-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-749">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-750">Product 1</span></span></td>
<td><span data-ttu-id="05c76-751">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-751">10001</span></span></td>
<td><span data-ttu-id="05c76-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-752">Electricity</span></span></td>
<td><span data-ttu-id="05c76-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-753">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="05c76-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="05c76-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="05c76-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="05c76-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="05c76-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-757">Cost element</span></span></th>
<th><span data-ttu-id="05c76-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05c76-758">Cost behavior</span></span></th>
<th><span data-ttu-id="05c76-759">Suma</span><span class="sxs-lookup"><span data-stu-id="05c76-759">Amount</span></span></th>
<th><span data-ttu-id="05c76-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="05c76-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="05c76-761">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-761">CC001</span></span></td>
<td><span data-ttu-id="05c76-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-762">HR</span></span></td>
<td><span data-ttu-id="05c76-763">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-763">10001</span></span></td>
<td><span data-ttu-id="05c76-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-764">Electricity</span></span></td>
<td><span data-ttu-id="05c76-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-765">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="05c76-766">-500.00</span></span></td>
<td><span data-ttu-id="05c76-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-768">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-768">CC002</span></span></td>
<td><span data-ttu-id="05c76-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-769">Finance</span></span></td>
<td><span data-ttu-id="05c76-770">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-770">10001</span></span></td>
<td><span data-ttu-id="05c76-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-771">Electricity</span></span></td>
<td><span data-ttu-id="05c76-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-772">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-773">175.00</span><span class="sxs-lookup"><span data-stu-id="05c76-773">175.00</span></span></td>
<td><span data-ttu-id="05c76-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-775">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-775">CC003</span></span></td>
<td><span data-ttu-id="05c76-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-776">Assembly</span></span></td>
<td><span data-ttu-id="05c76-777">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-777">10001</span></span></td>
<td><span data-ttu-id="05c76-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-778">Electricity</span></span></td>
<td><span data-ttu-id="05c76-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-779">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-780">275.00</span><span class="sxs-lookup"><span data-stu-id="05c76-780">275.00</span></span></td>
<td><span data-ttu-id="05c76-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-782">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-782">CC004</span></span></td>
<td><span data-ttu-id="05c76-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-783">Packaging</span></span></td>
<td><span data-ttu-id="05c76-784">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-784">10001</span></span></td>
<td><span data-ttu-id="05c76-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-785">Electricity</span></span></td>
<td><span data-ttu-id="05c76-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-786">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-787">50,00</span><span class="sxs-lookup"><span data-stu-id="05c76-787">50,00</span></span></td>
<td><span data-ttu-id="05c76-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-789">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-789">CC001</span></span></td>
<td><span data-ttu-id="05c76-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="05c76-790">HR</span></span></td>
<td><span data-ttu-id="05c76-791">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-791">10001</span></span></td>
<td><span data-ttu-id="05c76-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-792">Electricity</span></span></td>
<td><span data-ttu-id="05c76-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-793">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="05c76-794">-1,245.71</span></span></td>
<td><span data-ttu-id="05c76-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-796">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-796">CC002</span></span></td>
<td><span data-ttu-id="05c76-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-797">Finance</span></span></td>
<td><span data-ttu-id="05c76-798">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-798">10001</span></span></td>
<td><span data-ttu-id="05c76-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-799">Electricity</span></span></td>
<td><span data-ttu-id="05c76-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-800">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-801">436.00</span><span class="sxs-lookup"><span data-stu-id="05c76-801">436.00</span></span></td>
<td><span data-ttu-id="05c76-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-803">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-803">CC003</span></span></td>
<td><span data-ttu-id="05c76-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-804">Assembly</span></span></td>
<td><span data-ttu-id="05c76-805">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-805">10001</span></span></td>
<td><span data-ttu-id="05c76-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-806">Electricity</span></span></td>
<td><span data-ttu-id="05c76-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-807">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-808">685.14</span><span class="sxs-lookup"><span data-stu-id="05c76-808">685.14</span></span></td>
<td><span data-ttu-id="05c76-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-810">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-810">CC004</span></span></td>
<td><span data-ttu-id="05c76-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-811">Packaging</span></span></td>
<td><span data-ttu-id="05c76-812">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-812">10001</span></span></td>
<td><span data-ttu-id="05c76-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-813">Electricity</span></span></td>
<td><span data-ttu-id="05c76-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-814">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-815">124.57</span><span class="sxs-lookup"><span data-stu-id="05c76-815">124.57</span></span></td>
<td><span data-ttu-id="05c76-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-817">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-817">CC002</span></span></td>
<td><span data-ttu-id="05c76-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-818">Finance</span></span></td>
<td><span data-ttu-id="05c76-819">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-819">10001</span></span></td>
<td><span data-ttu-id="05c76-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-820">Electricity</span></span></td>
<td><span data-ttu-id="05c76-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-821">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="05c76-822">-675.00</span></span></td>
<td><span data-ttu-id="05c76-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-824">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-824">CC003</span></span></td>
<td><span data-ttu-id="05c76-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-825">Assembly</span></span></td>
<td><span data-ttu-id="05c76-826">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-826">10001</span></span></td>
<td><span data-ttu-id="05c76-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-827">Electricity</span></span></td>
<td><span data-ttu-id="05c76-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-828">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-829">438.75</span><span class="sxs-lookup"><span data-stu-id="05c76-829">438.75</span></span></td>
<td><span data-ttu-id="05c76-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-831">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-831">CC004</span></span></td>
<td><span data-ttu-id="05c76-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-832">Packaging</span></span></td>
<td><span data-ttu-id="05c76-833">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-833">10001</span></span></td>
<td><span data-ttu-id="05c76-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-834">Electricity</span></span></td>
<td><span data-ttu-id="05c76-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-835">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-836">236.25</span><span class="sxs-lookup"><span data-stu-id="05c76-836">236.25</span></span></td>
<td><span data-ttu-id="05c76-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-838">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-838">CC002</span></span></td>
<td><span data-ttu-id="05c76-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="05c76-839">Finance</span></span></td>
<td><span data-ttu-id="05c76-840">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-840">10001</span></span></td>
<td><span data-ttu-id="05c76-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-841">Electricity</span></span></td>
<td><span data-ttu-id="05c76-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-842">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="05c76-843">-8,150.29</span></span></td>
<td><span data-ttu-id="05c76-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-845">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-845">CC003</span></span></td>
<td><span data-ttu-id="05c76-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-846">Assembly</span></span></td>
<td><span data-ttu-id="05c76-847">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-847">10001</span></span></td>
<td><span data-ttu-id="05c76-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-848">Electricity</span></span></td>
<td><span data-ttu-id="05c76-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-849">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="05c76-850">5,297.69</span></span></td>
<td><span data-ttu-id="05c76-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-852">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-852">CC004</span></span></td>
<td><span data-ttu-id="05c76-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="05c76-853">Packaging</span></span></td>
<td><span data-ttu-id="05c76-854">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-854">10001</span></span></td>
<td><span data-ttu-id="05c76-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-855">Electricity</span></span></td>
<td><span data-ttu-id="05c76-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-856">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="05c76-857">2,852.60</span></span></td>
<td><span data-ttu-id="05c76-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-859">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-859">CC003</span></span></td>
<td><span data-ttu-id="05c76-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-860">Assembly</span></span></td>
<td><span data-ttu-id="05c76-861">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-861">10001</span></span></td>
<td><span data-ttu-id="05c76-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-862">Electricity</span></span></td>
<td><span data-ttu-id="05c76-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-863">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="05c76-864">-713.75</span></span></td>
<td><span data-ttu-id="05c76-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-866">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-867">Product 1</span></span></td>
<td><span data-ttu-id="05c76-868">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-868">10001</span></span></td>
<td><span data-ttu-id="05c76-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-869">Electricity</span></span></td>
<td><span data-ttu-id="05c76-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-870">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-871">535.31</span><span class="sxs-lookup"><span data-stu-id="05c76-871">535.31</span></span></td>
<td><span data-ttu-id="05c76-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-873">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-874">Product 2</span></span></td>
<td><span data-ttu-id="05c76-875">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-875">10001</span></span></td>
<td><span data-ttu-id="05c76-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-876">Electricity</span></span></td>
<td><span data-ttu-id="05c76-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-877">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-878">178.44</span><span class="sxs-lookup"><span data-stu-id="05c76-878">178.44</span></span></td>
<td><span data-ttu-id="05c76-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-880">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-880">CC003</span></span></td>
<td><span data-ttu-id="05c76-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-881">Assembly</span></span></td>
<td><span data-ttu-id="05c76-882">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-882">10001</span></span></td>
<td><span data-ttu-id="05c76-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-883">Electricity</span></span></td>
<td><span data-ttu-id="05c76-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-884">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="05c76-885">-5,982.83</span></span></td>
<td><span data-ttu-id="05c76-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-887">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-888">Product 1</span></span></td>
<td><span data-ttu-id="05c76-889">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-889">10001</span></span></td>
<td><span data-ttu-id="05c76-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-890">Electricity</span></span></td>
<td><span data-ttu-id="05c76-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-891">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="05c76-892">4,487.12</span></span></td>
<td><span data-ttu-id="05c76-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-894">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-895">Product 2</span></span></td>
<td><span data-ttu-id="05c76-896">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-896">10001</span></span></td>
<td><span data-ttu-id="05c76-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-897">Electricity</span></span></td>
<td><span data-ttu-id="05c76-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-898">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="05c76-899">1,495.71</span></span></td>
<td><span data-ttu-id="05c76-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-901">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-901">CC003</span></span></td>
<td><span data-ttu-id="05c76-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-902">Assembly</span></span></td>
<td><span data-ttu-id="05c76-903">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-903">10001</span></span></td>
<td><span data-ttu-id="05c76-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-904">Electricity</span></span></td>
<td><span data-ttu-id="05c76-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-905">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="05c76-906">-286.25</span></span></td>
<td><span data-ttu-id="05c76-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-908">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-909">Product 1</span></span></td>
<td><span data-ttu-id="05c76-910">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-910">10001</span></span></td>
<td><span data-ttu-id="05c76-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-911">Electricity</span></span></td>
<td><span data-ttu-id="05c76-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-912">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-913">241.05</span><span class="sxs-lookup"><span data-stu-id="05c76-913">241.05</span></span></td>
<td><span data-ttu-id="05c76-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-915">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-916">Product 2</span></span></td>
<td><span data-ttu-id="05c76-917">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-917">10001</span></span></td>
<td><span data-ttu-id="05c76-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-918">Electricity</span></span></td>
<td><span data-ttu-id="05c76-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-919">Fixed cost</span></span></td>
<td><span data-ttu-id="05c76-920">45.20</span><span class="sxs-lookup"><span data-stu-id="05c76-920">45.20</span></span></td>
<td><span data-ttu-id="05c76-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-922">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-922">CC003</span></span></td>
<td><span data-ttu-id="05c76-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="05c76-923">Assembly</span></span></td>
<td><span data-ttu-id="05c76-924">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-924">10001</span></span></td>
<td><span data-ttu-id="05c76-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-925">Electricity</span></span></td>
<td><span data-ttu-id="05c76-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-926">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="05c76-927">-2,977.17</span></span></td>
<td><span data-ttu-id="05c76-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-929">Prod 1</span></span></td>
<td><span data-ttu-id="05c76-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-930">Product 1</span></span></td>
<td><span data-ttu-id="05c76-931">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-931">10001</span></span></td>
<td><span data-ttu-id="05c76-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-932">Electricity</span></span></td>
<td><span data-ttu-id="05c76-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-933">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="05c76-934">2,507.09</span></span></td>
<td><span data-ttu-id="05c76-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="05c76-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-936">Prod 2</span></span></td>
<td><span data-ttu-id="05c76-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="05c76-937">Product 2</span></span></td>
<td><span data-ttu-id="05c76-938">10001</span><span class="sxs-lookup"><span data-stu-id="05c76-938">10001</span></span></td>
<td><span data-ttu-id="05c76-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-939">Electricity</span></span></td>
<td><span data-ttu-id="05c76-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-940">Variable cost</span></span></td>
<td><span data-ttu-id="05c76-941">470.08</span><span class="sxs-lookup"><span data-stu-id="05c76-941">470.08</span></span></td>
<td><span data-ttu-id="05c76-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="05c76-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="05c76-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="05c76-943">Conclusion</span></span>
<span data-ttu-id="05c76-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="05c76-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="05c76-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="05c76-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="05c76-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="05c76-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="05c76-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="05c76-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="05c76-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="05c76-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="05c76-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="05c76-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="05c76-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="05c76-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="05c76-951">CC099</span><span class="sxs-lookup"><span data-stu-id="05c76-951">CC099</span></span></th>
<th><span data-ttu-id="05c76-952">CC001</span><span class="sxs-lookup"><span data-stu-id="05c76-952">CC001</span></span></th>
<th><span data-ttu-id="05c76-953">CC002</span><span class="sxs-lookup"><span data-stu-id="05c76-953">CC002</span></span></th>
<th><span data-ttu-id="05c76-954">CC003</span><span class="sxs-lookup"><span data-stu-id="05c76-954">CC003</span></span></th>
<th><span data-ttu-id="05c76-955">CC004</span><span class="sxs-lookup"><span data-stu-id="05c76-955">CC004</span></span></th>
<th><span data-ttu-id="05c76-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-956">Proj 1</span></span></th>
<th><span data-ttu-id="05c76-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="05c76-957">Proj 2</span></span></th>
<th><span data-ttu-id="05c76-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-958">Prod 1</span></span></th>
<th><span data-ttu-id="05c76-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="05c76-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="05c76-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="05c76-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="05c76-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="05c76-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="05c76-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-971">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="05c76-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-973">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-974">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-975">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-976">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-977">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="05c76-978">776.36</span><span class="sxs-lookup"><span data-stu-id="05c76-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-979">223.64</span><span class="sxs-lookup"><span data-stu-id="05c76-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="05c76-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="05c76-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-982">000</span><span class="sxs-lookup"><span data-stu-id="05c76-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-983">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-984">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-985">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-986">0,00</span><span class="sxs-lookup"><span data-stu-id="05c76-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-987">30,00</span><span class="sxs-lookup"><span data-stu-id="05c76-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-988">10,00</span><span class="sxs-lookup"><span data-stu-id="05c76-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="05c76-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="05c76-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="05c76-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="05c76-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="05c76-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="05c76-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="05c76-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="05c76-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="05c76-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="05c76-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="05c76-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="05c76-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="05c76-996">Daugiau informacijos žr. [avikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="05c76-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



