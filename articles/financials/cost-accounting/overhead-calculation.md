---
title: "Pridėtinių išlaidų skaičiavimas"
description: "Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f56feac74dfe78b740342688a908d001614cffd0
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="693fa-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="693fa-103">Overhead calculation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="693fa-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="693fa-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="693fa-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="693fa-105">Term definition</span></span>
---------------

<span data-ttu-id="693fa-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="693fa-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="693fa-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="693fa-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="693fa-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="693fa-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="693fa-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="693fa-109">Rent</span></span>
-   <span data-ttu-id="693fa-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-110">Electricity</span></span>
-   <span data-ttu-id="693fa-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="693fa-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="693fa-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="693fa-112">Overhead calculation overview</span></span>
<span data-ttu-id="693fa-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="693fa-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="693fa-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="693fa-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="693fa-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="693fa-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="693fa-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="693fa-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="693fa-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="693fa-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="693fa-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="693fa-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="693fa-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="693fa-119">Version type</span></span>
-   <span data-ttu-id="693fa-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="693fa-120">Date and time</span></span>
-   <span data-ttu-id="693fa-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="693fa-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="693fa-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="693fa-122">Fiscal year</span></span>
-   <span data-ttu-id="693fa-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-123">Fiscal period</span></span>

<span data-ttu-id="693fa-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="693fa-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="693fa-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="693fa-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="693fa-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="693fa-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="693fa-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="693fa-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="693fa-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="693fa-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="693fa-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="693fa-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="693fa-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="693fa-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="693fa-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="693fa-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="693fa-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="693fa-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="693fa-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="693fa-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="693fa-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="693fa-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="693fa-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="693fa-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="693fa-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="693fa-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="693fa-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="693fa-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="693fa-140">Main account</span></span></th>
<th><span data-ttu-id="693fa-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="693fa-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="693fa-143">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-143">CC099</span></span></td>
<td><span data-ttu-id="693fa-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-144">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-145">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-145">10001</span></span></td>
<td><span data-ttu-id="693fa-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-146">Electricity</span></span></td>
<td><span data-ttu-id="693fa-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="693fa-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="693fa-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="693fa-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="693fa-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="693fa-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="693fa-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="693fa-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="693fa-151">Define the cost behavior rule</span></span>

<span data-ttu-id="693fa-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="693fa-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="693fa-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="693fa-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="693fa-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="693fa-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="693fa-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="693fa-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="693fa-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="693fa-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="693fa-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="693fa-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="693fa-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="693fa-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-160">Journal</span></span></th>
<th><span data-ttu-id="693fa-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="693fa-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="693fa-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="693fa-163">Versija</span><span class="sxs-lookup"><span data-stu-id="693fa-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-164">00001</span><span class="sxs-lookup"><span data-stu-id="693fa-164">00001</span></span></td>
<td><span data-ttu-id="693fa-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="693fa-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="693fa-166">Fiscal</span></span></td>
<td><span data-ttu-id="693fa-167">2017</span><span class="sxs-lookup"><span data-stu-id="693fa-167">2017</span></span></td>
<td><span data-ttu-id="693fa-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-168">Period 1</span></span></td>
<td><span data-ttu-id="693fa-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="693fa-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="693fa-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-173">Cost element</span></span></th>
<th><span data-ttu-id="693fa-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-174">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-175">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="693fa-177">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-177">CC099</span></span></td>
<td><span data-ttu-id="693fa-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-178">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-179">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-179">10001</span></span></td>
<td><span data-ttu-id="693fa-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-180">Electricity</span></span></td>
<td><span data-ttu-id="693fa-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="693fa-181">Unclassified</span></span></td>
<td><span data-ttu-id="693fa-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="693fa-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="693fa-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-185">Cost element</span></span></th>
<th><span data-ttu-id="693fa-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-186">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-187">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-187">Amount</span></span></th>
<th><span data-ttu-id="693fa-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-189">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-189">CC099</span></span></td>
<td><span data-ttu-id="693fa-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-190">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-191">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-191">10001</span></span></td>
<td><span data-ttu-id="693fa-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-192">Electricity</span></span></td>
<td><span data-ttu-id="693fa-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="693fa-193">Unclassified</span></span></td>
<td><span data-ttu-id="693fa-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-194">10,000.00</span></span></td>
<td><span data-ttu-id="693fa-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-196">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-196">CC099</span></span></td>
<td><span data-ttu-id="693fa-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-197">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-198">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-198">10001</span></span></td>
<td><span data-ttu-id="693fa-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-199">Electricity</span></span></td>
<td><span data-ttu-id="693fa-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="693fa-200">Unclassified</span></span></td>
<td><span data-ttu-id="693fa-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="693fa-201">-10,000.00</span></span></td>
<td><span data-ttu-id="693fa-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-203">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-203">CC099</span></span></td>
<td><span data-ttu-id="693fa-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-204">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-205">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-205">10001</span></span></td>
<td><span data-ttu-id="693fa-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-206">Electricity</span></span></td>
<td><span data-ttu-id="693fa-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-207">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-208">1,000.00</span></span></td>
<td><span data-ttu-id="693fa-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-210">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-210">CC099</span></span></td>
<td><span data-ttu-id="693fa-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-211">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-212">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-212">10001</span></span></td>
<td><span data-ttu-id="693fa-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-213">Electricity</span></span></td>
<td><span data-ttu-id="693fa-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-214">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="693fa-215">9,000.00</span></span></td>
<td><span data-ttu-id="693fa-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-217">Išsamios informacijos apie išlaidų veikimo būdą žr. temoje Išlaidų veikimo būdo strategija.</span><span class="sxs-lookup"><span data-stu-id="693fa-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="693fa-218">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="693fa-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="693fa-219">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="693fa-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="693fa-220">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="693fa-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="693fa-221">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="693fa-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="693fa-222">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="693fa-222">Define the cost distribution rule</span></span>

<span data-ttu-id="693fa-223">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="693fa-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="693fa-224">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="693fa-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="693fa-225">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="693fa-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="693fa-226">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="693fa-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="693fa-227">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="693fa-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="693fa-228">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="693fa-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-229">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-229">Cost object</span></span></th>
<th><span data-ttu-id="693fa-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="693fa-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-231">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-231">CC001</span></span></td>
<td><span data-ttu-id="693fa-232">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-232">HR</span></span></td>
<td><span data-ttu-id="693fa-233">1000</span><span class="sxs-lookup"><span data-stu-id="693fa-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-234">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-234">CC002</span></span></td>
<td><span data-ttu-id="693fa-235">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-235">Finance</span></span></td>
<td><span data-ttu-id="693fa-236">6,000</span><span class="sxs-lookup"><span data-stu-id="693fa-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-237">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-237">CC003</span></span></td>
<td><span data-ttu-id="693fa-238">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-238">Assembly</span></span></td>
<td><span data-ttu-id="693fa-239">0</span><span class="sxs-lookup"><span data-stu-id="693fa-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-240">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-241">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-241">Cost object</span></span></th>
<th><span data-ttu-id="693fa-242">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-242">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-243">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-243">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-244">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-245">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-245">CC001</span></span></td>
<td><span data-ttu-id="693fa-246">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-246">HR</span></span></td>
<td><span data-ttu-id="693fa-247">1000</span><span class="sxs-lookup"><span data-stu-id="693fa-247">1,000</span></span></td>
<td><span data-ttu-id="693fa-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="693fa-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="693fa-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-250">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-250">CC002</span></span></td>
<td><span data-ttu-id="693fa-251">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-251">Finance</span></span></td>
<td><span data-ttu-id="693fa-252">6,000</span><span class="sxs-lookup"><span data-stu-id="693fa-252">6,000</span></span></td>
<td><span data-ttu-id="693fa-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="693fa-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="693fa-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-255">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-255">CC003</span></span></td>
<td><span data-ttu-id="693fa-256">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-256">Assembly</span></span></td>
<td><span data-ttu-id="693fa-257">0</span><span class="sxs-lookup"><span data-stu-id="693fa-257">0</span></span></td>
<td><span data-ttu-id="693fa-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="693fa-259">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-260">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="693fa-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="693fa-261">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-262">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-262">Cost object</span></span></th>
<th><span data-ttu-id="693fa-263">Formulė</span><span class="sxs-lookup"><span data-stu-id="693fa-263">Formula</span></span></th>
<th><span data-ttu-id="693fa-264">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-264">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-265">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-265">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-266">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-267">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-267">CC001</span></span></td>
<td><span data-ttu-id="693fa-268">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-268">HR</span></span></td>
<td><span data-ttu-id="693fa-269">{1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="693fa-270">1</span><span class="sxs-lookup"><span data-stu-id="693fa-270">1</span></span></td>
<td><span data-ttu-id="693fa-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="693fa-272">500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-273">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-273">CC002</span></span></td>
<td><span data-ttu-id="693fa-274">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-274">Finance</span></span></td>
<td><span data-ttu-id="693fa-275">{6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="693fa-276">1</span><span class="sxs-lookup"><span data-stu-id="693fa-276">1</span></span></td>
<td><span data-ttu-id="693fa-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="693fa-278">500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-279">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-279">CC003</span></span></td>
<td><span data-ttu-id="693fa-280">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-280">Assembly</span></span></td>
<td><span data-ttu-id="693fa-281">{0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="693fa-282">0</span><span class="sxs-lookup"><span data-stu-id="693fa-282">0</span></span></td>
<td><span data-ttu-id="693fa-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="693fa-284">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="693fa-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-286">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-286">Journal</span></span></th>
<th><span data-ttu-id="693fa-287">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="693fa-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="693fa-288">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="693fa-289">Versija</span><span class="sxs-lookup"><span data-stu-id="693fa-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-290">00002</span><span class="sxs-lookup"><span data-stu-id="693fa-290">00002</span></span></td>
<td><span data-ttu-id="693fa-291">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="693fa-292">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="693fa-292">Fiscal</span></span></td>
<td><span data-ttu-id="693fa-293">2017</span><span class="sxs-lookup"><span data-stu-id="693fa-293">2017</span></span></td>
<td><span data-ttu-id="693fa-294">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-294">Period 1</span></span></td>
<td><span data-ttu-id="693fa-295">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="693fa-296">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="693fa-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-297">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-298">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-299">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-299">Cost element</span></span></th>
<th><span data-ttu-id="693fa-300">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-300">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-301">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-302">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-303">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-303">CC099</span></span></td>
<td><span data-ttu-id="693fa-304">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-304">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-305">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-305">10001</span></span></td>
<td><span data-ttu-id="693fa-306">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-306">Electricity</span></span></td>
<td><span data-ttu-id="693fa-307">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-307">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="693fa-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-309">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-310">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-310">CC099</span></span></td>
<td><span data-ttu-id="693fa-311">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-311">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-312">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-312">10001</span></span></td>
<td><span data-ttu-id="693fa-313">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-313">Electricity</span></span></td>
<td><span data-ttu-id="693fa-314">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-314">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="693fa-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="693fa-316">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="693fa-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-317">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-318">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-318">Cost element</span></span></th>
<th><span data-ttu-id="693fa-319">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-319">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-320">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-320">Amount</span></span></th>
<th><span data-ttu-id="693fa-321">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-322">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-322">CC099</span></span></td>
<td><span data-ttu-id="693fa-323">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-323">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-324">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-324">10001</span></span></td>
<td><span data-ttu-id="693fa-325">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-325">Electricity</span></span></td>
<td><span data-ttu-id="693fa-326">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-326">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-327">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="693fa-327">-1,000.00</span></span></td>
<td><span data-ttu-id="693fa-328">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-329">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-329">CC001</span></span></td>
<td><span data-ttu-id="693fa-330">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-330">HR</span></span></td>
<td><span data-ttu-id="693fa-331">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-331">10001</span></span></td>
<td><span data-ttu-id="693fa-332">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-332">Electricity</span></span></td>
<td><span data-ttu-id="693fa-333">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-333">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-334">500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-334">500.00</span></span></td>
<td><span data-ttu-id="693fa-335">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-336">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-336">CC002</span></span></td>
<td><span data-ttu-id="693fa-337">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-337">Finance</span></span></td>
<td><span data-ttu-id="693fa-338">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-338">10001</span></span></td>
<td><span data-ttu-id="693fa-339">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-339">Electricity</span></span></td>
<td><span data-ttu-id="693fa-340">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-340">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-341">500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-341">500.00</span></span></td>
<td><span data-ttu-id="693fa-342">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-343">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-343">CC099</span></span></td>
<td><span data-ttu-id="693fa-344">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="693fa-344">Default cost center</span></span></td>
<td><span data-ttu-id="693fa-345">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-345">10001</span></span></td>
<td><span data-ttu-id="693fa-346">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-346">Electricity</span></span></td>
<td><span data-ttu-id="693fa-347">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-347">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="693fa-348">-9,000.00</span></span></td>
<td><span data-ttu-id="693fa-349">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-350">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-350">CC001</span></span></td>
<td><span data-ttu-id="693fa-351">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-351">HR</span></span></td>
<td><span data-ttu-id="693fa-352">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-352">10001</span></span></td>
<td><span data-ttu-id="693fa-353">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-353">Electricity</span></span></td>
<td><span data-ttu-id="693fa-354">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-354">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="693fa-355">1,285.71</span></span></td>
<td><span data-ttu-id="693fa-356">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-357">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-357">CC002</span></span></td>
<td><span data-ttu-id="693fa-358">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-358">Finance</span></span></td>
<td><span data-ttu-id="693fa-359">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-359">10001</span></span></td>
<td><span data-ttu-id="693fa-360">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-360">Electricity</span></span></td>
<td><span data-ttu-id="693fa-361">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-361">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="693fa-362">7,714.29</span></span></td>
<td><span data-ttu-id="693fa-363">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-364">Daugiau informacijos apie išlaidų paskirstymą ir paskirstymo pagrindus žr. temose Išlaidų paskirstymo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="693fa-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="693fa-365">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="693fa-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="693fa-366">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="693fa-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="693fa-367">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="693fa-368">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="693fa-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="693fa-369">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="693fa-369">Define the overhead rate</span></span>

<span data-ttu-id="693fa-370">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="693fa-371">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="693fa-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-372">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-372">Cost object</span></span></th>
<th><span data-ttu-id="693fa-373">Valandos</span><span class="sxs-lookup"><span data-stu-id="693fa-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-374">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-374">Proj 1</span></span></td>
<td><span data-ttu-id="693fa-375">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-375">Project 1</span></span></td>
<td><span data-ttu-id="693fa-376">3</span><span class="sxs-lookup"><span data-stu-id="693fa-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-377">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-377">Proj 2</span></span></td>
<td><span data-ttu-id="693fa-378">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-378">Project 2</span></span></td>
<td><span data-ttu-id="693fa-379">1</span><span class="sxs-lookup"><span data-stu-id="693fa-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-380">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="693fa-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-381">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-381">Cost object</span></span></th>
<th><span data-ttu-id="693fa-382">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-382">Cost element</span></span></th>
<th><span data-ttu-id="693fa-383">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-383">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-384">Vienetai</span><span class="sxs-lookup"><span data-stu-id="693fa-384">Units</span></span></th>
<th><span data-ttu-id="693fa-385">Tarifas</span><span class="sxs-lookup"><span data-stu-id="693fa-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-386">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-386">CC001</span></span></td>
<td><span data-ttu-id="693fa-387">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-387">HR</span></span></td>
<td><span data-ttu-id="693fa-388">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-388">10001</span></span></td>
<td><span data-ttu-id="693fa-389">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-389">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-390">1</span><span class="sxs-lookup"><span data-stu-id="693fa-390">1</span></span></td>
<td><span data-ttu-id="693fa-391">10</span><span class="sxs-lookup"><span data-stu-id="693fa-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-392">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-393">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-393">Cost object</span></span></th>
<th><span data-ttu-id="693fa-394">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-394">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-395">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-395">Cost element</span></span></th>
<th><span data-ttu-id="693fa-396">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-396">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-397">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-398">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-398">Proj 1</span></span></td>
<td><span data-ttu-id="693fa-399">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-399">Project 1</span></span></td>
<td><span data-ttu-id="693fa-400">3</span><span class="sxs-lookup"><span data-stu-id="693fa-400">3</span></span></td>
<td><span data-ttu-id="693fa-401">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-401">10001</span></span></td>
<td><span data-ttu-id="693fa-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="693fa-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="693fa-403">30,00</span><span class="sxs-lookup"><span data-stu-id="693fa-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-404">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-404">Proj 2</span></span></td>
<td><span data-ttu-id="693fa-405">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-405">Project 2</span></span></td>
<td><span data-ttu-id="693fa-406">1</span><span class="sxs-lookup"><span data-stu-id="693fa-406">1</span></span></td>
<td><span data-ttu-id="693fa-407">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-407">10001</span></span></td>
<td><span data-ttu-id="693fa-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="693fa-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="693fa-409">10,00</span><span class="sxs-lookup"><span data-stu-id="693fa-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="693fa-410">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-411">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-411">Journal</span></span></th>
<th><span data-ttu-id="693fa-412">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="693fa-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="693fa-413">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="693fa-414">Versija</span><span class="sxs-lookup"><span data-stu-id="693fa-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-415">00003</span><span class="sxs-lookup"><span data-stu-id="693fa-415">00003</span></span></td>
<td><span data-ttu-id="693fa-416">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="693fa-417">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="693fa-417">Fiscal</span></span></td>
<td><span data-ttu-id="693fa-418">2017</span><span class="sxs-lookup"><span data-stu-id="693fa-418">2017</span></span></td>
<td><span data-ttu-id="693fa-419">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-419">Period 1</span></span></td>
<td><span data-ttu-id="693fa-420">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="693fa-421">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="693fa-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-422">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-423">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-423">Cost object</span></span></th>
<th><span data-ttu-id="693fa-424">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-425">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-426">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-426">Proj 1</span></span></td>
<td><span data-ttu-id="693fa-427">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="693fa-428">3,00</span><span class="sxs-lookup"><span data-stu-id="693fa-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-429">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-430">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-430">Proj 2</span></span></td>
<td><span data-ttu-id="693fa-431">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="693fa-432">1,00</span><span class="sxs-lookup"><span data-stu-id="693fa-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="693fa-433">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="693fa-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-434">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-435">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-435">Cost element</span></span></th>
<th><span data-ttu-id="693fa-436">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-436">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-437">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-437">Amount</span></span></th>
<th><span data-ttu-id="693fa-438">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="693fa-439">CC0001</span></span></td>
<td><span data-ttu-id="693fa-440">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-440">HR</span></span></td>
<td><span data-ttu-id="693fa-441">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-441">10001</span></span></td>
<td><span data-ttu-id="693fa-442">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-442">Electricity</span></span></td>
<td><span data-ttu-id="693fa-443">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-443">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="693fa-444">-30.00</span></span></td>
<td><span data-ttu-id="693fa-445">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-446">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-446">Proj 1</span></span></td>
<td><span data-ttu-id="693fa-447">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="693fa-448">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-448">10001</span></span></td>
<td><span data-ttu-id="693fa-449">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-449">Electricity</span></span></td>
<td><span data-ttu-id="693fa-450">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-450">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-451">30,00</span><span class="sxs-lookup"><span data-stu-id="693fa-451">30.00</span></span></td>
<td><span data-ttu-id="693fa-452">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-453">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-453">CC001</span></span></td>
<td><span data-ttu-id="693fa-454">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-454">HR</span></span></td>
<td><span data-ttu-id="693fa-455">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-455">10001</span></span></td>
<td><span data-ttu-id="693fa-456">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-456">Electricity</span></span></td>
<td><span data-ttu-id="693fa-457">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-457">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="693fa-458">-10.00</span></span></td>
<td><span data-ttu-id="693fa-459">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-460">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-460">Proj 2</span></span></td>
<td><span data-ttu-id="693fa-461">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="693fa-462">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-462">10001</span></span></td>
<td><span data-ttu-id="693fa-463">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-463">Electricity</span></span></td>
<td><span data-ttu-id="693fa-464">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-464">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-465">10,00</span><span class="sxs-lookup"><span data-stu-id="693fa-465">10.00</span></span></td>
<td><span data-ttu-id="693fa-466">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-467">Išsamesnės informacijos apie pridėtinių išlaidų tarifo strategiją žr. temoje Pridėtinių išlaidų tarifo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="693fa-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="693fa-468">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="693fa-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="693fa-469">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="693fa-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="693fa-470">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="693fa-471">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="693fa-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="693fa-472">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="693fa-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="693fa-473">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="693fa-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="693fa-474">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="693fa-475">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="693fa-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="693fa-476">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="693fa-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="693fa-477">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="693fa-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="693fa-478">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="693fa-478">Define the cost allocation</span></span>

<span data-ttu-id="693fa-479">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="693fa-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="693fa-480">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="693fa-481">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="693fa-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-482">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-482">Cost object</span></span></th>
<th><span data-ttu-id="693fa-483">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="693fa-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-484">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-484">CC002</span></span></td>
<td><span data-ttu-id="693fa-485">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-485">Finance</span></span></td>
<td><span data-ttu-id="693fa-486">35</span><span class="sxs-lookup"><span data-stu-id="693fa-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-487">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-487">CC003</span></span></td>
<td><span data-ttu-id="693fa-488">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-488">Assembly</span></span></td>
<td><span data-ttu-id="693fa-489">55</span><span class="sxs-lookup"><span data-stu-id="693fa-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-490">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-490">CC004</span></span></td>
<td><span data-ttu-id="693fa-491">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-491">Packaging</span></span></td>
<td><span data-ttu-id="693fa-492">10</span><span class="sxs-lookup"><span data-stu-id="693fa-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-493">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="693fa-494">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="693fa-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-495">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-495">Cost object</span></span></th>
<th><span data-ttu-id="693fa-496">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="693fa-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-497">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-497">CC003</span></span></td>
<td><span data-ttu-id="693fa-498">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-498">Assembly</span></span></td>
<td><span data-ttu-id="693fa-499">65</span><span class="sxs-lookup"><span data-stu-id="693fa-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-500">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-500">CC004</span></span></td>
<td><span data-ttu-id="693fa-501">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-501">Packaging</span></span></td>
<td><span data-ttu-id="693fa-502">35</span><span class="sxs-lookup"><span data-stu-id="693fa-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-503">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="693fa-504">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="693fa-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-505">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-505">Cost object</span></span></th>
<th><span data-ttu-id="693fa-506">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="693fa-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-507">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-507">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-508">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-508">Product 1</span></span></td>
<td><span data-ttu-id="693fa-509">60</span><span class="sxs-lookup"><span data-stu-id="693fa-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-510">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-510">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-511">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-511">Product 2</span></span></td>
<td><span data-ttu-id="693fa-512">20</span><span class="sxs-lookup"><span data-stu-id="693fa-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-513">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="693fa-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="693fa-514">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="693fa-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-515">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-515">Cost object</span></span></th>
<th><span data-ttu-id="693fa-516">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="693fa-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-517">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-517">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-518">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-518">Product 1</span></span></td>
<td><span data-ttu-id="693fa-519">80</span><span class="sxs-lookup"><span data-stu-id="693fa-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-520">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-520">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-521">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-521">Product 2</span></span></td>
<td><span data-ttu-id="693fa-522">15</span><span class="sxs-lookup"><span data-stu-id="693fa-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-523">**Pastaba:** programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="693fa-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="693fa-524">Išsamesnės informacijos apie statistinių priemonių teikimo įrankius žr. temoje Statistinės priemonės teikimo įrankio šablonas.</span><span class="sxs-lookup"><span data-stu-id="693fa-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="693fa-525">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.) Toliau pateikiamoje lentelėje rodoma, kas nutinka pritaikius personalo paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-526">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-526">Cost object</span></span></th>
<th><span data-ttu-id="693fa-527">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-527">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-528">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-528">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-529">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-529">Amount</span></span></th>
<th><span data-ttu-id="693fa-530">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-531">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-531">CC002</span></span></td>
<td><span data-ttu-id="693fa-532">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-532">Finance</span></span></td>
<td><span data-ttu-id="693fa-533">35</span><span class="sxs-lookup"><span data-stu-id="693fa-533">35</span></span></td>
<td><span data-ttu-id="693fa-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="693fa-535">175.00</span><span class="sxs-lookup"><span data-stu-id="693fa-535">175.00</span></span></td>
<td><span data-ttu-id="693fa-536">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-537">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-537">CC003</span></span></td>
<td><span data-ttu-id="693fa-538">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-538">Assembly</span></span></td>
<td><span data-ttu-id="693fa-539">55</span><span class="sxs-lookup"><span data-stu-id="693fa-539">55</span></span></td>
<td><span data-ttu-id="693fa-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="693fa-541">275.00</span><span class="sxs-lookup"><span data-stu-id="693fa-541">275.00</span></span></td>
<td><span data-ttu-id="693fa-542">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-543">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-543">CC004</span></span></td>
<td><span data-ttu-id="693fa-544">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-544">Packaging</span></span></td>
<td><span data-ttu-id="693fa-545">10</span><span class="sxs-lookup"><span data-stu-id="693fa-545">10</span></span></td>
<td><span data-ttu-id="693fa-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="693fa-547">50,00</span><span class="sxs-lookup"><span data-stu-id="693fa-547">50.00</span></span></td>
<td><span data-ttu-id="693fa-548">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-549">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-549">CC002</span></span></td>
<td><span data-ttu-id="693fa-550">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-550">Finance</span></span></td>
<td><span data-ttu-id="693fa-551">35</span><span class="sxs-lookup"><span data-stu-id="693fa-551">35</span></span></td>
<td><span data-ttu-id="693fa-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="693fa-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="693fa-553">436.00</span><span class="sxs-lookup"><span data-stu-id="693fa-553">436.00</span></span></td>
<td><span data-ttu-id="693fa-554">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-555">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-555">CC003</span></span></td>
<td><span data-ttu-id="693fa-556">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-556">Assembly</span></span></td>
<td><span data-ttu-id="693fa-557">55</span><span class="sxs-lookup"><span data-stu-id="693fa-557">55</span></span></td>
<td><span data-ttu-id="693fa-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="693fa-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="693fa-559">685.14</span><span class="sxs-lookup"><span data-stu-id="693fa-559">685.14</span></span></td>
<td><span data-ttu-id="693fa-560">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-561">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-561">CC004</span></span></td>
<td><span data-ttu-id="693fa-562">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-562">Packaging</span></span></td>
<td><span data-ttu-id="693fa-563">10</span><span class="sxs-lookup"><span data-stu-id="693fa-563">10</span></span></td>
<td><span data-ttu-id="693fa-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="693fa-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="693fa-565">124.57</span><span class="sxs-lookup"><span data-stu-id="693fa-565">124.57</span></span></td>
<td><span data-ttu-id="693fa-566">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-567">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-568">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-568">Cost object</span></span></th>
<th><span data-ttu-id="693fa-569">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-569">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-570">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-570">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-571">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-571">Amount</span></span></th>
<th><span data-ttu-id="693fa-572">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-573">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-573">CC003</span></span></td>
<td><span data-ttu-id="693fa-574">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-574">Assembly</span></span></td>
<td><span data-ttu-id="693fa-575">65</span><span class="sxs-lookup"><span data-stu-id="693fa-575">65</span></span></td>
<td><span data-ttu-id="693fa-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="693fa-577">438.75</span><span class="sxs-lookup"><span data-stu-id="693fa-577">438.75</span></span></td>
<td><span data-ttu-id="693fa-578">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-579">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-579">CC004</span></span></td>
<td><span data-ttu-id="693fa-580">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-580">Packaging</span></span></td>
<td><span data-ttu-id="693fa-581">35</span><span class="sxs-lookup"><span data-stu-id="693fa-581">35</span></span></td>
<td><span data-ttu-id="693fa-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="693fa-583">236.25</span><span class="sxs-lookup"><span data-stu-id="693fa-583">236.25</span></span></td>
<td><span data-ttu-id="693fa-584">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-585">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-585">CC003</span></span></td>
<td><span data-ttu-id="693fa-586">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-586">Assembly</span></span></td>
<td><span data-ttu-id="693fa-587">65</span><span class="sxs-lookup"><span data-stu-id="693fa-587">65</span></span></td>
<td><span data-ttu-id="693fa-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="693fa-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="693fa-589">5,297.69</span></span></td>
<td><span data-ttu-id="693fa-590">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-591">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-591">CC004</span></span></td>
<td><span data-ttu-id="693fa-592">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-592">Packaging</span></span></td>
<td><span data-ttu-id="693fa-593">35</span><span class="sxs-lookup"><span data-stu-id="693fa-593">35</span></span></td>
<td><span data-ttu-id="693fa-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="693fa-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="693fa-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="693fa-595">2,852.60</span></span></td>
<td><span data-ttu-id="693fa-596">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-597">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-598">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-598">Cost object</span></span></th>
<th><span data-ttu-id="693fa-599">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-599">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-600">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-600">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-601">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-601">Amount</span></span></th>
<th><span data-ttu-id="693fa-602">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-603">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-603">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-604">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-604">Product 1</span></span></td>
<td><span data-ttu-id="693fa-605">60</span><span class="sxs-lookup"><span data-stu-id="693fa-605">60</span></span></td>
<td><span data-ttu-id="693fa-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="693fa-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="693fa-607">535.31</span><span class="sxs-lookup"><span data-stu-id="693fa-607">535.31</span></span></td>
<td><span data-ttu-id="693fa-608">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-609">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-609">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-610">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-610">Product 2</span></span></td>
<td><span data-ttu-id="693fa-611">20</span><span class="sxs-lookup"><span data-stu-id="693fa-611">20</span></span></td>
<td><span data-ttu-id="693fa-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="693fa-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="693fa-613">178.44</span><span class="sxs-lookup"><span data-stu-id="693fa-613">178.44</span></span></td>
<td><span data-ttu-id="693fa-614">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-615">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-615">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-616">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-616">Product 1</span></span></td>
<td><span data-ttu-id="693fa-617">60</span><span class="sxs-lookup"><span data-stu-id="693fa-617">60</span></span></td>
<td><span data-ttu-id="693fa-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="693fa-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="693fa-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="693fa-619">4,487.12</span></span></td>
<td><span data-ttu-id="693fa-620">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-621">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-621">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-622">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-622">Product 2</span></span></td>
<td><span data-ttu-id="693fa-623">20</span><span class="sxs-lookup"><span data-stu-id="693fa-623">20</span></span></td>
<td><span data-ttu-id="693fa-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="693fa-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="693fa-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="693fa-625">1,495.71</span></span></td>
<td><span data-ttu-id="693fa-626">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="693fa-627">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="693fa-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-628">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-628">Cost object</span></span></th>
<th><span data-ttu-id="693fa-629">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="693fa-629">Magnitude</span></span></th>
<th><span data-ttu-id="693fa-630">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="693fa-630">Allocation factor</span></span></th>
<th><span data-ttu-id="693fa-631">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-631">Amount</span></span></th>
<th><span data-ttu-id="693fa-632">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-633">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-633">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-634">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-634">Product 1</span></span></td>
<td><span data-ttu-id="693fa-635">80</span><span class="sxs-lookup"><span data-stu-id="693fa-635">80</span></span></td>
<td><span data-ttu-id="693fa-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="693fa-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="693fa-637">241.05</span><span class="sxs-lookup"><span data-stu-id="693fa-637">241.05</span></span></td>
<td><span data-ttu-id="693fa-638">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-639">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-639">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-640">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-640">Product 2</span></span></td>
<td><span data-ttu-id="693fa-641">15</span><span class="sxs-lookup"><span data-stu-id="693fa-641">15</span></span></td>
<td><span data-ttu-id="693fa-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="693fa-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="693fa-643">45.20</span><span class="sxs-lookup"><span data-stu-id="693fa-643">45.20</span></span></td>
<td><span data-ttu-id="693fa-644">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-645">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-645">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-646">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-646">Product 1</span></span></td>
<td><span data-ttu-id="693fa-647">80</span><span class="sxs-lookup"><span data-stu-id="693fa-647">80</span></span></td>
<td><span data-ttu-id="693fa-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="693fa-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="693fa-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="693fa-649">2,507.09</span></span></td>
<td><span data-ttu-id="693fa-650">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-651">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-651">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-652">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-652">Product 2</span></span></td>
<td><span data-ttu-id="693fa-653">15</span><span class="sxs-lookup"><span data-stu-id="693fa-653">15</span></span></td>
<td><span data-ttu-id="693fa-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="693fa-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="693fa-655">470.08</span><span class="sxs-lookup"><span data-stu-id="693fa-655">470.08</span></span></td>
<td><span data-ttu-id="693fa-656">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="693fa-657">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="693fa-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-658">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-658">Journal</span></span></th>
<th><span data-ttu-id="693fa-659">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="693fa-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="693fa-660">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="693fa-661">Versija</span><span class="sxs-lookup"><span data-stu-id="693fa-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-662">00004</span><span class="sxs-lookup"><span data-stu-id="693fa-662">00004</span></span></td>
<td><span data-ttu-id="693fa-663">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="693fa-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="693fa-664">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="693fa-664">Fiscal</span></span></td>
<td><span data-ttu-id="693fa-665">2017</span><span class="sxs-lookup"><span data-stu-id="693fa-665">2017</span></span></td>
<td><span data-ttu-id="693fa-666">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-666">Period 1</span></span></td>
<td><span data-ttu-id="693fa-667">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="693fa-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="693fa-668">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="693fa-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="693fa-669">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-670">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-671">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-671">Cost element</span></span></th>
<th><span data-ttu-id="693fa-672">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-672">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-673">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-674">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-675">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-675">CC001</span></span></td>
<td><span data-ttu-id="693fa-676">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-676">HR</span></span></td>
<td><span data-ttu-id="693fa-677">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-677">10001</span></span></td>
<td><span data-ttu-id="693fa-678">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-678">Electricity</span></span></td>
<td><span data-ttu-id="693fa-679">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-679">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-680">500,00</span><span class="sxs-lookup"><span data-stu-id="693fa-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-681">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-682">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-682">CC001</span></span></td>
<td><span data-ttu-id="693fa-683">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-683">HR</span></span></td>
<td><span data-ttu-id="693fa-684">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-684">10001</span></span></td>
<td><span data-ttu-id="693fa-685">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-685">Electricity</span></span></td>
<td><span data-ttu-id="693fa-686">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-686">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="693fa-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-688">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-689">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-689">CC002</span></span></td>
<td><span data-ttu-id="693fa-690">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-690">Finance</span></span></td>
<td><span data-ttu-id="693fa-691">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-691">10001</span></span></td>
<td><span data-ttu-id="693fa-692">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-692">Electricity</span></span></td>
<td><span data-ttu-id="693fa-693">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-693">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-694">675.00</span><span class="sxs-lookup"><span data-stu-id="693fa-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-695">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-696">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-696">CC002</span></span></td>
<td><span data-ttu-id="693fa-697">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-697">Finance</span></span></td>
<td><span data-ttu-id="693fa-698">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-698">10001</span></span></td>
<td><span data-ttu-id="693fa-699">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-699">Electricity</span></span></td>
<td><span data-ttu-id="693fa-700">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-700">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="693fa-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-702">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-703">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-703">CC003</span></span></td>
<td><span data-ttu-id="693fa-704">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-704">Assembly</span></span></td>
<td><span data-ttu-id="693fa-705">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-705">10001</span></span></td>
<td><span data-ttu-id="693fa-706">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-706">Electricity</span></span></td>
<td><span data-ttu-id="693fa-707">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-707">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-708">713.75</span><span class="sxs-lookup"><span data-stu-id="693fa-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-709">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-710">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-710">CC003</span></span></td>
<td><span data-ttu-id="693fa-711">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-711">Assembly</span></span></td>
<td><span data-ttu-id="693fa-712">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-712">10001</span></span></td>
<td><span data-ttu-id="693fa-713">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-713">Electricity</span></span></td>
<td><span data-ttu-id="693fa-714">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-714">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="693fa-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-716">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-717">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-717">CC003</span></span></td>
<td><span data-ttu-id="693fa-718">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-718">Packaging</span></span></td>
<td><span data-ttu-id="693fa-719">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-719">10001</span></span></td>
<td><span data-ttu-id="693fa-720">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-720">Electricity</span></span></td>
<td><span data-ttu-id="693fa-721">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-721">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-722">286.25</span><span class="sxs-lookup"><span data-stu-id="693fa-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-723">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-724">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-724">CC003</span></span></td>
<td><span data-ttu-id="693fa-725">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-725">Packaging</span></span></td>
<td><span data-ttu-id="693fa-726">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-726">10001</span></span></td>
<td><span data-ttu-id="693fa-727">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-727">Electricity</span></span></td>
<td><span data-ttu-id="693fa-728">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-728">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="693fa-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-730">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-731">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-731">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-732">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-732">Product 1</span></span></td>
<td><span data-ttu-id="693fa-733">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-733">10001</span></span></td>
<td><span data-ttu-id="693fa-734">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-734">Electricity</span></span></td>
<td><span data-ttu-id="693fa-735">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-735">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-736">776.36</span><span class="sxs-lookup"><span data-stu-id="693fa-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-737">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-738">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-738">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-739">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-739">Product 1</span></span></td>
<td><span data-ttu-id="693fa-740">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-740">10001</span></span></td>
<td><span data-ttu-id="693fa-741">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-741">Electricity</span></span></td>
<td><span data-ttu-id="693fa-742">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-742">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="693fa-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-744">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-745">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-745">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-746">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-746">Product 1</span></span></td>
<td><span data-ttu-id="693fa-747">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-747">10001</span></span></td>
<td><span data-ttu-id="693fa-748">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-748">Electricity</span></span></td>
<td><span data-ttu-id="693fa-749">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-749">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-750">223.64</span><span class="sxs-lookup"><span data-stu-id="693fa-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-751">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="693fa-752">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-752">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-753">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-753">Product 1</span></span></td>
<td><span data-ttu-id="693fa-754">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-754">10001</span></span></td>
<td><span data-ttu-id="693fa-755">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-755">Electricity</span></span></td>
<td><span data-ttu-id="693fa-756">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-756">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="693fa-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="693fa-758">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="693fa-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="693fa-759">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="693fa-760">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-760">Cost element</span></span></th>
<th><span data-ttu-id="693fa-761">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="693fa-761">Cost behavior</span></span></th>
<th><span data-ttu-id="693fa-762">Suma</span><span class="sxs-lookup"><span data-stu-id="693fa-762">Amount</span></span></th>
<th><span data-ttu-id="693fa-763">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="693fa-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="693fa-764">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-764">CC001</span></span></td>
<td><span data-ttu-id="693fa-765">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-765">HR</span></span></td>
<td><span data-ttu-id="693fa-766">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-766">10001</span></span></td>
<td><span data-ttu-id="693fa-767">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-767">Electricity</span></span></td>
<td><span data-ttu-id="693fa-768">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-768">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="693fa-769">-500.00</span></span></td>
<td><span data-ttu-id="693fa-770">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-771">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-771">CC002</span></span></td>
<td><span data-ttu-id="693fa-772">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-772">Finance</span></span></td>
<td><span data-ttu-id="693fa-773">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-773">10001</span></span></td>
<td><span data-ttu-id="693fa-774">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-774">Electricity</span></span></td>
<td><span data-ttu-id="693fa-775">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-775">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-776">175.00</span><span class="sxs-lookup"><span data-stu-id="693fa-776">175.00</span></span></td>
<td><span data-ttu-id="693fa-777">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-778">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-778">CC003</span></span></td>
<td><span data-ttu-id="693fa-779">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-779">Assembly</span></span></td>
<td><span data-ttu-id="693fa-780">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-780">10001</span></span></td>
<td><span data-ttu-id="693fa-781">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-781">Electricity</span></span></td>
<td><span data-ttu-id="693fa-782">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-782">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-783">275.00</span><span class="sxs-lookup"><span data-stu-id="693fa-783">275.00</span></span></td>
<td><span data-ttu-id="693fa-784">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-785">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-785">CC004</span></span></td>
<td><span data-ttu-id="693fa-786">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-786">Packaging</span></span></td>
<td><span data-ttu-id="693fa-787">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-787">10001</span></span></td>
<td><span data-ttu-id="693fa-788">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-788">Electricity</span></span></td>
<td><span data-ttu-id="693fa-789">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-789">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-790">50,00</span><span class="sxs-lookup"><span data-stu-id="693fa-790">50,00</span></span></td>
<td><span data-ttu-id="693fa-791">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-792">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-792">CC001</span></span></td>
<td><span data-ttu-id="693fa-793">Personalas</span><span class="sxs-lookup"><span data-stu-id="693fa-793">HR</span></span></td>
<td><span data-ttu-id="693fa-794">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-794">10001</span></span></td>
<td><span data-ttu-id="693fa-795">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-795">Electricity</span></span></td>
<td><span data-ttu-id="693fa-796">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-796">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="693fa-797">-1,245.71</span></span></td>
<td><span data-ttu-id="693fa-798">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-799">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-799">CC002</span></span></td>
<td><span data-ttu-id="693fa-800">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-800">Finance</span></span></td>
<td><span data-ttu-id="693fa-801">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-801">10001</span></span></td>
<td><span data-ttu-id="693fa-802">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-802">Electricity</span></span></td>
<td><span data-ttu-id="693fa-803">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-803">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-804">436.00</span><span class="sxs-lookup"><span data-stu-id="693fa-804">436.00</span></span></td>
<td><span data-ttu-id="693fa-805">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-806">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-806">CC003</span></span></td>
<td><span data-ttu-id="693fa-807">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-807">Assembly</span></span></td>
<td><span data-ttu-id="693fa-808">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-808">10001</span></span></td>
<td><span data-ttu-id="693fa-809">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-809">Electricity</span></span></td>
<td><span data-ttu-id="693fa-810">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-810">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-811">685.14</span><span class="sxs-lookup"><span data-stu-id="693fa-811">685.14</span></span></td>
<td><span data-ttu-id="693fa-812">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-813">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-813">CC004</span></span></td>
<td><span data-ttu-id="693fa-814">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-814">Packaging</span></span></td>
<td><span data-ttu-id="693fa-815">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-815">10001</span></span></td>
<td><span data-ttu-id="693fa-816">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-816">Electricity</span></span></td>
<td><span data-ttu-id="693fa-817">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-817">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-818">124.57</span><span class="sxs-lookup"><span data-stu-id="693fa-818">124.57</span></span></td>
<td><span data-ttu-id="693fa-819">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-820">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-820">CC002</span></span></td>
<td><span data-ttu-id="693fa-821">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-821">Finance</span></span></td>
<td><span data-ttu-id="693fa-822">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-822">10001</span></span></td>
<td><span data-ttu-id="693fa-823">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-823">Electricity</span></span></td>
<td><span data-ttu-id="693fa-824">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-824">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="693fa-825">-675.00</span></span></td>
<td><span data-ttu-id="693fa-826">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-827">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-827">CC003</span></span></td>
<td><span data-ttu-id="693fa-828">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-828">Assembly</span></span></td>
<td><span data-ttu-id="693fa-829">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-829">10001</span></span></td>
<td><span data-ttu-id="693fa-830">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-830">Electricity</span></span></td>
<td><span data-ttu-id="693fa-831">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-831">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-832">438.75</span><span class="sxs-lookup"><span data-stu-id="693fa-832">438.75</span></span></td>
<td><span data-ttu-id="693fa-833">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-834">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-834">CC004</span></span></td>
<td><span data-ttu-id="693fa-835">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-835">Packaging</span></span></td>
<td><span data-ttu-id="693fa-836">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-836">10001</span></span></td>
<td><span data-ttu-id="693fa-837">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-837">Electricity</span></span></td>
<td><span data-ttu-id="693fa-838">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-838">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-839">236.25</span><span class="sxs-lookup"><span data-stu-id="693fa-839">236.25</span></span></td>
<td><span data-ttu-id="693fa-840">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-841">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-841">CC002</span></span></td>
<td><span data-ttu-id="693fa-842">Finansai</span><span class="sxs-lookup"><span data-stu-id="693fa-842">Finance</span></span></td>
<td><span data-ttu-id="693fa-843">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-843">10001</span></span></td>
<td><span data-ttu-id="693fa-844">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-844">Electricity</span></span></td>
<td><span data-ttu-id="693fa-845">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-845">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="693fa-846">-8,150.29</span></span></td>
<td><span data-ttu-id="693fa-847">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-848">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-848">CC003</span></span></td>
<td><span data-ttu-id="693fa-849">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-849">Assembly</span></span></td>
<td><span data-ttu-id="693fa-850">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-850">10001</span></span></td>
<td><span data-ttu-id="693fa-851">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-851">Electricity</span></span></td>
<td><span data-ttu-id="693fa-852">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-852">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="693fa-853">5,297.69</span></span></td>
<td><span data-ttu-id="693fa-854">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-855">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-855">CC004</span></span></td>
<td><span data-ttu-id="693fa-856">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="693fa-856">Packaging</span></span></td>
<td><span data-ttu-id="693fa-857">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-857">10001</span></span></td>
<td><span data-ttu-id="693fa-858">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-858">Electricity</span></span></td>
<td><span data-ttu-id="693fa-859">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-859">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="693fa-860">2,852.60</span></span></td>
<td><span data-ttu-id="693fa-861">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-862">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-862">CC003</span></span></td>
<td><span data-ttu-id="693fa-863">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-863">Assembly</span></span></td>
<td><span data-ttu-id="693fa-864">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-864">10001</span></span></td>
<td><span data-ttu-id="693fa-865">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-865">Electricity</span></span></td>
<td><span data-ttu-id="693fa-866">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-866">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="693fa-867">-713.75</span></span></td>
<td><span data-ttu-id="693fa-868">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-869">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-869">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-870">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-870">Product 1</span></span></td>
<td><span data-ttu-id="693fa-871">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-871">10001</span></span></td>
<td><span data-ttu-id="693fa-872">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-872">Electricity</span></span></td>
<td><span data-ttu-id="693fa-873">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-873">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-874">535.31</span><span class="sxs-lookup"><span data-stu-id="693fa-874">535.31</span></span></td>
<td><span data-ttu-id="693fa-875">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-876">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-876">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-877">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-877">Product 2</span></span></td>
<td><span data-ttu-id="693fa-878">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-878">10001</span></span></td>
<td><span data-ttu-id="693fa-879">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-879">Electricity</span></span></td>
<td><span data-ttu-id="693fa-880">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-880">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-881">178.44</span><span class="sxs-lookup"><span data-stu-id="693fa-881">178.44</span></span></td>
<td><span data-ttu-id="693fa-882">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-883">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-883">CC003</span></span></td>
<td><span data-ttu-id="693fa-884">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-884">Assembly</span></span></td>
<td><span data-ttu-id="693fa-885">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-885">10001</span></span></td>
<td><span data-ttu-id="693fa-886">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-886">Electricity</span></span></td>
<td><span data-ttu-id="693fa-887">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-887">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="693fa-888">-5,982.83</span></span></td>
<td><span data-ttu-id="693fa-889">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-890">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-890">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-891">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-891">Product 1</span></span></td>
<td><span data-ttu-id="693fa-892">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-892">10001</span></span></td>
<td><span data-ttu-id="693fa-893">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-893">Electricity</span></span></td>
<td><span data-ttu-id="693fa-894">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-894">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="693fa-895">4,487.12</span></span></td>
<td><span data-ttu-id="693fa-896">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-897">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-897">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-898">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-898">Product 2</span></span></td>
<td><span data-ttu-id="693fa-899">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-899">10001</span></span></td>
<td><span data-ttu-id="693fa-900">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-900">Electricity</span></span></td>
<td><span data-ttu-id="693fa-901">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-901">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="693fa-902">1,495.71</span></span></td>
<td><span data-ttu-id="693fa-903">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-904">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-904">CC003</span></span></td>
<td><span data-ttu-id="693fa-905">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-905">Assembly</span></span></td>
<td><span data-ttu-id="693fa-906">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-906">10001</span></span></td>
<td><span data-ttu-id="693fa-907">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-907">Electricity</span></span></td>
<td><span data-ttu-id="693fa-908">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-908">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="693fa-909">-286.25</span></span></td>
<td><span data-ttu-id="693fa-910">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-911">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-911">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-912">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-912">Product 1</span></span></td>
<td><span data-ttu-id="693fa-913">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-913">10001</span></span></td>
<td><span data-ttu-id="693fa-914">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-914">Electricity</span></span></td>
<td><span data-ttu-id="693fa-915">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-915">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-916">241.05</span><span class="sxs-lookup"><span data-stu-id="693fa-916">241.05</span></span></td>
<td><span data-ttu-id="693fa-917">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-918">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-918">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-919">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-919">Product 2</span></span></td>
<td><span data-ttu-id="693fa-920">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-920">10001</span></span></td>
<td><span data-ttu-id="693fa-921">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-921">Electricity</span></span></td>
<td><span data-ttu-id="693fa-922">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-922">Fixed cost</span></span></td>
<td><span data-ttu-id="693fa-923">45.20</span><span class="sxs-lookup"><span data-stu-id="693fa-923">45.20</span></span></td>
<td><span data-ttu-id="693fa-924">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-925">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-925">CC003</span></span></td>
<td><span data-ttu-id="693fa-926">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="693fa-926">Assembly</span></span></td>
<td><span data-ttu-id="693fa-927">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-927">10001</span></span></td>
<td><span data-ttu-id="693fa-928">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-928">Electricity</span></span></td>
<td><span data-ttu-id="693fa-929">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-929">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="693fa-930">-2,977.17</span></span></td>
<td><span data-ttu-id="693fa-931">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-932">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-932">Prod 1</span></span></td>
<td><span data-ttu-id="693fa-933">1 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-933">Product 1</span></span></td>
<td><span data-ttu-id="693fa-934">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-934">10001</span></span></td>
<td><span data-ttu-id="693fa-935">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-935">Electricity</span></span></td>
<td><span data-ttu-id="693fa-936">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-936">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="693fa-937">2,507.09</span></span></td>
<td><span data-ttu-id="693fa-938">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="693fa-939">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-939">Prod 2</span></span></td>
<td><span data-ttu-id="693fa-940">2 produktas</span><span class="sxs-lookup"><span data-stu-id="693fa-940">Product 2</span></span></td>
<td><span data-ttu-id="693fa-941">10001</span><span class="sxs-lookup"><span data-stu-id="693fa-941">10001</span></span></td>
<td><span data-ttu-id="693fa-942">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-942">Electricity</span></span></td>
<td><span data-ttu-id="693fa-943">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-943">Variable cost</span></span></td>
<td><span data-ttu-id="693fa-944">470.08</span><span class="sxs-lookup"><span data-stu-id="693fa-944">470.08</span></span></td>
<td><span data-ttu-id="693fa-945">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="693fa-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="693fa-946">Išvada</span><span class="sxs-lookup"><span data-stu-id="693fa-946">Conclusion</span></span>
<span data-ttu-id="693fa-947">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="693fa-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="693fa-948">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="693fa-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="693fa-949">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="693fa-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="693fa-950">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="693fa-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="693fa-951">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="693fa-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="693fa-952">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="693fa-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="693fa-953">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="693fa-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="693fa-954">CC099</span><span class="sxs-lookup"><span data-stu-id="693fa-954">CC099</span></span></th>
<th><span data-ttu-id="693fa-955">CC001</span><span class="sxs-lookup"><span data-stu-id="693fa-955">CC001</span></span></th>
<th><span data-ttu-id="693fa-956">CC002</span><span class="sxs-lookup"><span data-stu-id="693fa-956">CC002</span></span></th>
<th><span data-ttu-id="693fa-957">CC003</span><span class="sxs-lookup"><span data-stu-id="693fa-957">CC003</span></span></th>
<th><span data-ttu-id="693fa-958">CC004</span><span class="sxs-lookup"><span data-stu-id="693fa-958">CC004</span></span></th>
<th><span data-ttu-id="693fa-959">1 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-959">Proj 1</span></span></th>
<th><span data-ttu-id="693fa-960">2 projektas</span><span class="sxs-lookup"><span data-stu-id="693fa-960">Proj 2</span></span></th>
<th><span data-ttu-id="693fa-961">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-961">Prod 1</span></span></th>
<th><span data-ttu-id="693fa-962">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="693fa-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="693fa-963">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="693fa-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="693fa-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="693fa-973">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="693fa-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-974">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="693fa-975">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-976">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-977">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-978">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-979">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-980">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="693fa-981">776.36</span><span class="sxs-lookup"><span data-stu-id="693fa-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-982">223.64</span><span class="sxs-lookup"><span data-stu-id="693fa-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="693fa-984">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="693fa-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-985">000</span><span class="sxs-lookup"><span data-stu-id="693fa-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-986">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-987">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-988">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-989">0,00</span><span class="sxs-lookup"><span data-stu-id="693fa-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-990">30,00</span><span class="sxs-lookup"><span data-stu-id="693fa-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-991">10,00</span><span class="sxs-lookup"><span data-stu-id="693fa-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="693fa-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="693fa-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="693fa-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="693fa-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="693fa-995">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="693fa-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="693fa-996">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="693fa-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="693fa-997">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="693fa-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="693fa-998">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="693fa-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="693fa-999">Išsamesnės informacijos žr. temoje Išlaidų sumavimo strategija.</span><span class="sxs-lookup"><span data-stu-id="693fa-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="693fa-1000">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="693fa-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




