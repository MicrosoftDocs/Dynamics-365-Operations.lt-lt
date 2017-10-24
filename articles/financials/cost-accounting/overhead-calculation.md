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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0ea6f7428cd5c7618d2d69f1fb66fd9539ad1073
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="a4920-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a4920-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a4920-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="a4920-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a4920-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="a4920-105">Term definition</span></span>
---------------

<span data-ttu-id="a4920-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="a4920-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a4920-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="a4920-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a4920-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="a4920-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a4920-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="a4920-109">Rent</span></span>
-   <span data-ttu-id="a4920-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-110">Electricity</span></span>
-   <span data-ttu-id="a4920-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="a4920-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a4920-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="a4920-112">Overhead calculation overview</span></span>
<span data-ttu-id="a4920-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="a4920-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a4920-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a4920-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a4920-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="a4920-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a4920-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="a4920-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a4920-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="a4920-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a4920-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="a4920-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a4920-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="a4920-119">Version type</span></span>
-   <span data-ttu-id="a4920-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="a4920-120">Date and time</span></span>
-   <span data-ttu-id="a4920-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="a4920-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a4920-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="a4920-122">Fiscal year</span></span>
-   <span data-ttu-id="a4920-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-123">Fiscal period</span></span>

<span data-ttu-id="a4920-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="a4920-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a4920-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="a4920-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a4920-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="a4920-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a4920-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="a4920-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a4920-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="a4920-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a4920-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="a4920-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a4920-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="a4920-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a4920-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a4920-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a4920-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="a4920-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a4920-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="a4920-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a4920-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="a4920-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a4920-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="a4920-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a4920-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="a4920-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a4920-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="a4920-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="a4920-140">Main account</span></span></th>
<th><span data-ttu-id="a4920-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="a4920-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a4920-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-143">CC099</span></span></td>
<td><span data-ttu-id="a4920-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-144">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-145">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-145">10001</span></span></td>
<td><span data-ttu-id="a4920-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-146">Electricity</span></span></td>
<td><span data-ttu-id="a4920-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a4920-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="a4920-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a4920-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="a4920-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a4920-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="a4920-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a4920-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="a4920-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a4920-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="a4920-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a4920-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="a4920-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a4920-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a4920-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a4920-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="a4920-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a4920-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a4920-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="a4920-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a4920-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="a4920-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a4920-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-160">Journal</span></span></th>
<th><span data-ttu-id="a4920-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="a4920-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a4920-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a4920-163">Versija</span><span class="sxs-lookup"><span data-stu-id="a4920-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-164">00001</span><span class="sxs-lookup"><span data-stu-id="a4920-164">00001</span></span></td>
<td><span data-ttu-id="a4920-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a4920-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="a4920-166">Fiscal</span></span></td>
<td><span data-ttu-id="a4920-167">2017</span><span class="sxs-lookup"><span data-stu-id="a4920-167">2017</span></span></td>
<td><span data-ttu-id="a4920-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-168">Period 1</span></span></td>
<td><span data-ttu-id="a4920-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a4920-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="a4920-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-173">Cost element</span></span></th>
<th><span data-ttu-id="a4920-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-175">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a4920-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-177">CC099</span></span></td>
<td><span data-ttu-id="a4920-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-178">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-179">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-179">10001</span></span></td>
<td><span data-ttu-id="a4920-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-180">Electricity</span></span></td>
<td><span data-ttu-id="a4920-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="a4920-181">Unclassified</span></span></td>
<td><span data-ttu-id="a4920-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a4920-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="a4920-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-185">Cost element</span></span></th>
<th><span data-ttu-id="a4920-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-187">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-187">Amount</span></span></th>
<th><span data-ttu-id="a4920-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-189">CC099</span></span></td>
<td><span data-ttu-id="a4920-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-190">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-191">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-191">10001</span></span></td>
<td><span data-ttu-id="a4920-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-192">Electricity</span></span></td>
<td><span data-ttu-id="a4920-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="a4920-193">Unclassified</span></span></td>
<td><span data-ttu-id="a4920-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-194">10,000.00</span></span></td>
<td><span data-ttu-id="a4920-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-196">CC099</span></span></td>
<td><span data-ttu-id="a4920-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-197">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-198">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-198">10001</span></span></td>
<td><span data-ttu-id="a4920-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-199">Electricity</span></span></td>
<td><span data-ttu-id="a4920-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="a4920-200">Unclassified</span></span></td>
<td><span data-ttu-id="a4920-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="a4920-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a4920-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-203">CC099</span></span></td>
<td><span data-ttu-id="a4920-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-204">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-205">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-205">10001</span></span></td>
<td><span data-ttu-id="a4920-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-206">Electricity</span></span></td>
<td><span data-ttu-id="a4920-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-208">1,000.00</span></span></td>
<td><span data-ttu-id="a4920-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-210">CC099</span></span></td>
<td><span data-ttu-id="a4920-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-211">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-212">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-212">10001</span></span></td>
<td><span data-ttu-id="a4920-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-213">Electricity</span></span></td>
<td><span data-ttu-id="a4920-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-214">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a4920-215">9,000.00</span></span></td>
<td><span data-ttu-id="a4920-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-217">Išsamios informacijos apie išlaidų veikimo būdą žr. temoje Išlaidų veikimo būdo strategija.</span><span class="sxs-lookup"><span data-stu-id="a4920-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="a4920-218">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="a4920-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a4920-219">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="a4920-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a4920-220">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="a4920-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a4920-221">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="a4920-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a4920-222">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="a4920-222">Define the cost distribution rule</span></span>

<span data-ttu-id="a4920-223">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="a4920-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a4920-224">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="a4920-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a4920-225">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="a4920-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a4920-226">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="a4920-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a4920-227">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="a4920-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a4920-228">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="a4920-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-229">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-229">Cost object</span></span></th>
<th><span data-ttu-id="a4920-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="a4920-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-231">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-231">CC001</span></span></td>
<td><span data-ttu-id="a4920-232">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-232">HR</span></span></td>
<td><span data-ttu-id="a4920-233">1000</span><span class="sxs-lookup"><span data-stu-id="a4920-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-234">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-234">CC002</span></span></td>
<td><span data-ttu-id="a4920-235">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-235">Finance</span></span></td>
<td><span data-ttu-id="a4920-236">6,000</span><span class="sxs-lookup"><span data-stu-id="a4920-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-237">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-237">CC003</span></span></td>
<td><span data-ttu-id="a4920-238">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-238">Assembly</span></span></td>
<td><span data-ttu-id="a4920-239">0</span><span class="sxs-lookup"><span data-stu-id="a4920-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-240">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-241">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-241">Cost object</span></span></th>
<th><span data-ttu-id="a4920-242">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-242">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-243">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-243">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-244">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-245">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-245">CC001</span></span></td>
<td><span data-ttu-id="a4920-246">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-246">HR</span></span></td>
<td><span data-ttu-id="a4920-247">1000</span><span class="sxs-lookup"><span data-stu-id="a4920-247">1,000</span></span></td>
<td><span data-ttu-id="a4920-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a4920-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a4920-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-250">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-250">CC002</span></span></td>
<td><span data-ttu-id="a4920-251">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-251">Finance</span></span></td>
<td><span data-ttu-id="a4920-252">6,000</span><span class="sxs-lookup"><span data-stu-id="a4920-252">6,000</span></span></td>
<td><span data-ttu-id="a4920-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a4920-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a4920-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-255">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-255">CC003</span></span></td>
<td><span data-ttu-id="a4920-256">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-256">Assembly</span></span></td>
<td><span data-ttu-id="a4920-257">0</span><span class="sxs-lookup"><span data-stu-id="a4920-257">0</span></span></td>
<td><span data-ttu-id="a4920-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a4920-259">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-260">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="a4920-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a4920-261">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-262">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-262">Cost object</span></span></th>
<th><span data-ttu-id="a4920-263">Formulė</span><span class="sxs-lookup"><span data-stu-id="a4920-263">Formula</span></span></th>
<th><span data-ttu-id="a4920-264">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-264">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-265">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-265">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-266">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-267">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-267">CC001</span></span></td>
<td><span data-ttu-id="a4920-268">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-268">HR</span></span></td>
<td><span data-ttu-id="a4920-269">{1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a4920-270">1</span><span class="sxs-lookup"><span data-stu-id="a4920-270">1</span></span></td>
<td><span data-ttu-id="a4920-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a4920-272">500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-273">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-273">CC002</span></span></td>
<td><span data-ttu-id="a4920-274">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-274">Finance</span></span></td>
<td><span data-ttu-id="a4920-275">{6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a4920-276">1</span><span class="sxs-lookup"><span data-stu-id="a4920-276">1</span></span></td>
<td><span data-ttu-id="a4920-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a4920-278">500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-279">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-279">CC003</span></span></td>
<td><span data-ttu-id="a4920-280">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-280">Assembly</span></span></td>
<td><span data-ttu-id="a4920-281">{0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a4920-282">0</span><span class="sxs-lookup"><span data-stu-id="a4920-282">0</span></span></td>
<td><span data-ttu-id="a4920-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a4920-284">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a4920-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-286">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-286">Journal</span></span></th>
<th><span data-ttu-id="a4920-287">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="a4920-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a4920-288">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a4920-289">Versija</span><span class="sxs-lookup"><span data-stu-id="a4920-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-290">00002</span><span class="sxs-lookup"><span data-stu-id="a4920-290">00002</span></span></td>
<td><span data-ttu-id="a4920-291">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a4920-292">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="a4920-292">Fiscal</span></span></td>
<td><span data-ttu-id="a4920-293">2017</span><span class="sxs-lookup"><span data-stu-id="a4920-293">2017</span></span></td>
<td><span data-ttu-id="a4920-294">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-294">Period 1</span></span></td>
<td><span data-ttu-id="a4920-295">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a4920-296">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="a4920-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-297">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-298">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-299">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-299">Cost element</span></span></th>
<th><span data-ttu-id="a4920-300">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-300">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-301">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-302">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-303">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-303">CC099</span></span></td>
<td><span data-ttu-id="a4920-304">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-304">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-305">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-305">10001</span></span></td>
<td><span data-ttu-id="a4920-306">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-306">Electricity</span></span></td>
<td><span data-ttu-id="a4920-307">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-307">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="a4920-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-309">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-310">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-310">CC099</span></span></td>
<td><span data-ttu-id="a4920-311">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-311">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-312">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-312">10001</span></span></td>
<td><span data-ttu-id="a4920-313">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-313">Electricity</span></span></td>
<td><span data-ttu-id="a4920-314">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-314">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a4920-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a4920-316">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="a4920-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-317">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-318">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-318">Cost element</span></span></th>
<th><span data-ttu-id="a4920-319">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-319">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-320">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-320">Amount</span></span></th>
<th><span data-ttu-id="a4920-321">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-322">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-322">CC099</span></span></td>
<td><span data-ttu-id="a4920-323">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-323">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-324">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-324">10001</span></span></td>
<td><span data-ttu-id="a4920-325">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-325">Electricity</span></span></td>
<td><span data-ttu-id="a4920-326">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-326">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-327">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="a4920-327">-1,000.00</span></span></td>
<td><span data-ttu-id="a4920-328">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-329">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-329">CC001</span></span></td>
<td><span data-ttu-id="a4920-330">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-330">HR</span></span></td>
<td><span data-ttu-id="a4920-331">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-331">10001</span></span></td>
<td><span data-ttu-id="a4920-332">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-332">Electricity</span></span></td>
<td><span data-ttu-id="a4920-333">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-333">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-334">500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-334">500.00</span></span></td>
<td><span data-ttu-id="a4920-335">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-336">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-336">CC002</span></span></td>
<td><span data-ttu-id="a4920-337">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-337">Finance</span></span></td>
<td><span data-ttu-id="a4920-338">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-338">10001</span></span></td>
<td><span data-ttu-id="a4920-339">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-339">Electricity</span></span></td>
<td><span data-ttu-id="a4920-340">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-340">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-341">500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-341">500.00</span></span></td>
<td><span data-ttu-id="a4920-342">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-343">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-343">CC099</span></span></td>
<td><span data-ttu-id="a4920-344">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="a4920-344">Default cost center</span></span></td>
<td><span data-ttu-id="a4920-345">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-345">10001</span></span></td>
<td><span data-ttu-id="a4920-346">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-346">Electricity</span></span></td>
<td><span data-ttu-id="a4920-347">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-347">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="a4920-348">-9,000.00</span></span></td>
<td><span data-ttu-id="a4920-349">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-350">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-350">CC001</span></span></td>
<td><span data-ttu-id="a4920-351">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-351">HR</span></span></td>
<td><span data-ttu-id="a4920-352">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-352">10001</span></span></td>
<td><span data-ttu-id="a4920-353">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-353">Electricity</span></span></td>
<td><span data-ttu-id="a4920-354">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-354">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a4920-355">1,285.71</span></span></td>
<td><span data-ttu-id="a4920-356">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-357">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-357">CC002</span></span></td>
<td><span data-ttu-id="a4920-358">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-358">Finance</span></span></td>
<td><span data-ttu-id="a4920-359">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-359">10001</span></span></td>
<td><span data-ttu-id="a4920-360">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-360">Electricity</span></span></td>
<td><span data-ttu-id="a4920-361">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-361">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a4920-362">7,714.29</span></span></td>
<td><span data-ttu-id="a4920-363">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-364">Daugiau informacijos apie išlaidų paskirstymą ir paskirstymo pagrindus žr. temose Išlaidų paskirstymo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="a4920-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="a4920-365">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="a4920-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a4920-366">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="a4920-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a4920-367">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a4920-368">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="a4920-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a4920-369">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a4920-369">Define the overhead rate</span></span>

<span data-ttu-id="a4920-370">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a4920-371">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4920-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-372">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-372">Cost object</span></span></th>
<th><span data-ttu-id="a4920-373">Valandos</span><span class="sxs-lookup"><span data-stu-id="a4920-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-374">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-374">Proj 1</span></span></td>
<td><span data-ttu-id="a4920-375">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-375">Project 1</span></span></td>
<td><span data-ttu-id="a4920-376">3</span><span class="sxs-lookup"><span data-stu-id="a4920-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-377">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-377">Proj 2</span></span></td>
<td><span data-ttu-id="a4920-378">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-378">Project 2</span></span></td>
<td><span data-ttu-id="a4920-379">1</span><span class="sxs-lookup"><span data-stu-id="a4920-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-380">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="a4920-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-381">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-381">Cost object</span></span></th>
<th><span data-ttu-id="a4920-382">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-382">Cost element</span></span></th>
<th><span data-ttu-id="a4920-383">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-383">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-384">Vienetai</span><span class="sxs-lookup"><span data-stu-id="a4920-384">Units</span></span></th>
<th><span data-ttu-id="a4920-385">Tarifas</span><span class="sxs-lookup"><span data-stu-id="a4920-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-386">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-386">CC001</span></span></td>
<td><span data-ttu-id="a4920-387">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-387">HR</span></span></td>
<td><span data-ttu-id="a4920-388">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-388">10001</span></span></td>
<td><span data-ttu-id="a4920-389">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-389">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-390">1</span><span class="sxs-lookup"><span data-stu-id="a4920-390">1</span></span></td>
<td><span data-ttu-id="a4920-391">10</span><span class="sxs-lookup"><span data-stu-id="a4920-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-392">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-393">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-393">Cost object</span></span></th>
<th><span data-ttu-id="a4920-394">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-394">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-395">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-395">Cost element</span></span></th>
<th><span data-ttu-id="a4920-396">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-396">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-397">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-398">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-398">Proj 1</span></span></td>
<td><span data-ttu-id="a4920-399">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-399">Project 1</span></span></td>
<td><span data-ttu-id="a4920-400">3</span><span class="sxs-lookup"><span data-stu-id="a4920-400">3</span></span></td>
<td><span data-ttu-id="a4920-401">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-401">10001</span></span></td>
<td><span data-ttu-id="a4920-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a4920-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a4920-403">30,00</span><span class="sxs-lookup"><span data-stu-id="a4920-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-404">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-404">Proj 2</span></span></td>
<td><span data-ttu-id="a4920-405">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-405">Project 2</span></span></td>
<td><span data-ttu-id="a4920-406">1</span><span class="sxs-lookup"><span data-stu-id="a4920-406">1</span></span></td>
<td><span data-ttu-id="a4920-407">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-407">10001</span></span></td>
<td><span data-ttu-id="a4920-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a4920-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a4920-409">10,00</span><span class="sxs-lookup"><span data-stu-id="a4920-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a4920-410">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-411">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-411">Journal</span></span></th>
<th><span data-ttu-id="a4920-412">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="a4920-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a4920-413">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a4920-414">Versija</span><span class="sxs-lookup"><span data-stu-id="a4920-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-415">00003</span><span class="sxs-lookup"><span data-stu-id="a4920-415">00003</span></span></td>
<td><span data-ttu-id="a4920-416">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a4920-417">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="a4920-417">Fiscal</span></span></td>
<td><span data-ttu-id="a4920-418">2017</span><span class="sxs-lookup"><span data-stu-id="a4920-418">2017</span></span></td>
<td><span data-ttu-id="a4920-419">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-419">Period 1</span></span></td>
<td><span data-ttu-id="a4920-420">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a4920-421">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="a4920-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-422">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-423">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-423">Cost object</span></span></th>
<th><span data-ttu-id="a4920-424">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-425">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-426">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-426">Proj 1</span></span></td>
<td><span data-ttu-id="a4920-427">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a4920-428">3,00</span><span class="sxs-lookup"><span data-stu-id="a4920-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-429">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-430">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-430">Proj 2</span></span></td>
<td><span data-ttu-id="a4920-431">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a4920-432">1,00</span><span class="sxs-lookup"><span data-stu-id="a4920-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a4920-433">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="a4920-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-434">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-435">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-435">Cost element</span></span></th>
<th><span data-ttu-id="a4920-436">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-436">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-437">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-437">Amount</span></span></th>
<th><span data-ttu-id="a4920-438">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="a4920-439">CC0001</span></span></td>
<td><span data-ttu-id="a4920-440">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-440">HR</span></span></td>
<td><span data-ttu-id="a4920-441">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-441">10001</span></span></td>
<td><span data-ttu-id="a4920-442">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-442">Electricity</span></span></td>
<td><span data-ttu-id="a4920-443">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-443">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="a4920-444">-30.00</span></span></td>
<td><span data-ttu-id="a4920-445">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-446">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-446">Proj 1</span></span></td>
<td><span data-ttu-id="a4920-447">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a4920-448">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-448">10001</span></span></td>
<td><span data-ttu-id="a4920-449">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-449">Electricity</span></span></td>
<td><span data-ttu-id="a4920-450">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-450">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-451">30,00</span><span class="sxs-lookup"><span data-stu-id="a4920-451">30.00</span></span></td>
<td><span data-ttu-id="a4920-452">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-453">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-453">CC001</span></span></td>
<td><span data-ttu-id="a4920-454">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-454">HR</span></span></td>
<td><span data-ttu-id="a4920-455">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-455">10001</span></span></td>
<td><span data-ttu-id="a4920-456">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-456">Electricity</span></span></td>
<td><span data-ttu-id="a4920-457">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-457">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="a4920-458">-10.00</span></span></td>
<td><span data-ttu-id="a4920-459">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-460">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-460">Proj 2</span></span></td>
<td><span data-ttu-id="a4920-461">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a4920-462">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-462">10001</span></span></td>
<td><span data-ttu-id="a4920-463">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-463">Electricity</span></span></td>
<td><span data-ttu-id="a4920-464">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-464">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-465">10,00</span><span class="sxs-lookup"><span data-stu-id="a4920-465">10.00</span></span></td>
<td><span data-ttu-id="a4920-466">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-467">Išsamesnės informacijos apie pridėtinių išlaidų tarifo strategiją žr. temoje Pridėtinių išlaidų tarifo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="a4920-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="a4920-468">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="a4920-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a4920-469">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="a4920-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a4920-470">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a4920-471">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="a4920-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="a4920-472">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="a4920-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a4920-473">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="a4920-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a4920-474">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a4920-475">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="a4920-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a4920-476">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="a4920-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a4920-477">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a4920-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a4920-478">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a4920-478">Define the cost allocation</span></span>

<span data-ttu-id="a4920-479">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="a4920-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a4920-480">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a4920-481">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4920-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-482">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-482">Cost object</span></span></th>
<th><span data-ttu-id="a4920-483">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="a4920-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-484">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-484">CC002</span></span></td>
<td><span data-ttu-id="a4920-485">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-485">Finance</span></span></td>
<td><span data-ttu-id="a4920-486">35</span><span class="sxs-lookup"><span data-stu-id="a4920-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-487">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-487">CC003</span></span></td>
<td><span data-ttu-id="a4920-488">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-488">Assembly</span></span></td>
<td><span data-ttu-id="a4920-489">55</span><span class="sxs-lookup"><span data-stu-id="a4920-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-490">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-490">CC004</span></span></td>
<td><span data-ttu-id="a4920-491">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-491">Packaging</span></span></td>
<td><span data-ttu-id="a4920-492">10</span><span class="sxs-lookup"><span data-stu-id="a4920-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-493">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a4920-494">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4920-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-495">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-495">Cost object</span></span></th>
<th><span data-ttu-id="a4920-496">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="a4920-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-497">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-497">CC003</span></span></td>
<td><span data-ttu-id="a4920-498">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-498">Assembly</span></span></td>
<td><span data-ttu-id="a4920-499">65</span><span class="sxs-lookup"><span data-stu-id="a4920-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-500">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-500">CC004</span></span></td>
<td><span data-ttu-id="a4920-501">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-501">Packaging</span></span></td>
<td><span data-ttu-id="a4920-502">35</span><span class="sxs-lookup"><span data-stu-id="a4920-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-503">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a4920-504">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4920-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-505">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-505">Cost object</span></span></th>
<th><span data-ttu-id="a4920-506">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="a4920-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-507">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-507">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-508">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-508">Product 1</span></span></td>
<td><span data-ttu-id="a4920-509">60</span><span class="sxs-lookup"><span data-stu-id="a4920-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-510">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-510">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-511">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-511">Product 2</span></span></td>
<td><span data-ttu-id="a4920-512">20</span><span class="sxs-lookup"><span data-stu-id="a4920-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-513">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="a4920-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a4920-514">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4920-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-515">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-515">Cost object</span></span></th>
<th><span data-ttu-id="a4920-516">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="a4920-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-517">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-517">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-518">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-518">Product 1</span></span></td>
<td><span data-ttu-id="a4920-519">80</span><span class="sxs-lookup"><span data-stu-id="a4920-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-520">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-520">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-521">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-521">Product 2</span></span></td>
<td><span data-ttu-id="a4920-522">15</span><span class="sxs-lookup"><span data-stu-id="a4920-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-523">**Pastaba:** programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="a4920-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a4920-524">Išsamesnės informacijos apie statistinių priemonių teikimo įrankius žr. temoje Statistinės priemonės teikimo įrankio šablonas.</span><span class="sxs-lookup"><span data-stu-id="a4920-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="a4920-525">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.) Toliau pateikiamoje lentelėje rodoma, kas nutinka pritaikius personalo paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-526">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-526">Cost object</span></span></th>
<th><span data-ttu-id="a4920-527">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-527">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-528">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-528">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-529">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-529">Amount</span></span></th>
<th><span data-ttu-id="a4920-530">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-531">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-531">CC002</span></span></td>
<td><span data-ttu-id="a4920-532">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-532">Finance</span></span></td>
<td><span data-ttu-id="a4920-533">35</span><span class="sxs-lookup"><span data-stu-id="a4920-533">35</span></span></td>
<td><span data-ttu-id="a4920-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a4920-535">175.00</span><span class="sxs-lookup"><span data-stu-id="a4920-535">175.00</span></span></td>
<td><span data-ttu-id="a4920-536">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-537">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-537">CC003</span></span></td>
<td><span data-ttu-id="a4920-538">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-538">Assembly</span></span></td>
<td><span data-ttu-id="a4920-539">55</span><span class="sxs-lookup"><span data-stu-id="a4920-539">55</span></span></td>
<td><span data-ttu-id="a4920-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a4920-541">275.00</span><span class="sxs-lookup"><span data-stu-id="a4920-541">275.00</span></span></td>
<td><span data-ttu-id="a4920-542">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-543">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-543">CC004</span></span></td>
<td><span data-ttu-id="a4920-544">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-544">Packaging</span></span></td>
<td><span data-ttu-id="a4920-545">10</span><span class="sxs-lookup"><span data-stu-id="a4920-545">10</span></span></td>
<td><span data-ttu-id="a4920-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a4920-547">50,00</span><span class="sxs-lookup"><span data-stu-id="a4920-547">50.00</span></span></td>
<td><span data-ttu-id="a4920-548">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-549">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-549">CC002</span></span></td>
<td><span data-ttu-id="a4920-550">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-550">Finance</span></span></td>
<td><span data-ttu-id="a4920-551">35</span><span class="sxs-lookup"><span data-stu-id="a4920-551">35</span></span></td>
<td><span data-ttu-id="a4920-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="a4920-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a4920-553">436.00</span><span class="sxs-lookup"><span data-stu-id="a4920-553">436.00</span></span></td>
<td><span data-ttu-id="a4920-554">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-555">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-555">CC003</span></span></td>
<td><span data-ttu-id="a4920-556">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-556">Assembly</span></span></td>
<td><span data-ttu-id="a4920-557">55</span><span class="sxs-lookup"><span data-stu-id="a4920-557">55</span></span></td>
<td><span data-ttu-id="a4920-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="a4920-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a4920-559">685.14</span><span class="sxs-lookup"><span data-stu-id="a4920-559">685.14</span></span></td>
<td><span data-ttu-id="a4920-560">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-561">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-561">CC004</span></span></td>
<td><span data-ttu-id="a4920-562">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-562">Packaging</span></span></td>
<td><span data-ttu-id="a4920-563">10</span><span class="sxs-lookup"><span data-stu-id="a4920-563">10</span></span></td>
<td><span data-ttu-id="a4920-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="a4920-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a4920-565">124.57</span><span class="sxs-lookup"><span data-stu-id="a4920-565">124.57</span></span></td>
<td><span data-ttu-id="a4920-566">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-567">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-568">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-568">Cost object</span></span></th>
<th><span data-ttu-id="a4920-569">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-569">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-570">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-570">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-571">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-571">Amount</span></span></th>
<th><span data-ttu-id="a4920-572">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-573">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-573">CC003</span></span></td>
<td><span data-ttu-id="a4920-574">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-574">Assembly</span></span></td>
<td><span data-ttu-id="a4920-575">65</span><span class="sxs-lookup"><span data-stu-id="a4920-575">65</span></span></td>
<td><span data-ttu-id="a4920-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a4920-577">438.75</span><span class="sxs-lookup"><span data-stu-id="a4920-577">438.75</span></span></td>
<td><span data-ttu-id="a4920-578">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-579">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-579">CC004</span></span></td>
<td><span data-ttu-id="a4920-580">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-580">Packaging</span></span></td>
<td><span data-ttu-id="a4920-581">35</span><span class="sxs-lookup"><span data-stu-id="a4920-581">35</span></span></td>
<td><span data-ttu-id="a4920-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a4920-583">236.25</span><span class="sxs-lookup"><span data-stu-id="a4920-583">236.25</span></span></td>
<td><span data-ttu-id="a4920-584">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-585">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-585">CC003</span></span></td>
<td><span data-ttu-id="a4920-586">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-586">Assembly</span></span></td>
<td><span data-ttu-id="a4920-587">65</span><span class="sxs-lookup"><span data-stu-id="a4920-587">65</span></span></td>
<td><span data-ttu-id="a4920-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a4920-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a4920-589">5,297.69</span></span></td>
<td><span data-ttu-id="a4920-590">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-591">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-591">CC004</span></span></td>
<td><span data-ttu-id="a4920-592">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-592">Packaging</span></span></td>
<td><span data-ttu-id="a4920-593">35</span><span class="sxs-lookup"><span data-stu-id="a4920-593">35</span></span></td>
<td><span data-ttu-id="a4920-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a4920-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a4920-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a4920-595">2,852.60</span></span></td>
<td><span data-ttu-id="a4920-596">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-597">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-598">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-598">Cost object</span></span></th>
<th><span data-ttu-id="a4920-599">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-599">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-600">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-600">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-601">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-601">Amount</span></span></th>
<th><span data-ttu-id="a4920-602">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-603">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-603">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-604">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-604">Product 1</span></span></td>
<td><span data-ttu-id="a4920-605">60</span><span class="sxs-lookup"><span data-stu-id="a4920-605">60</span></span></td>
<td><span data-ttu-id="a4920-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a4920-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a4920-607">535.31</span><span class="sxs-lookup"><span data-stu-id="a4920-607">535.31</span></span></td>
<td><span data-ttu-id="a4920-608">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-609">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-609">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-610">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-610">Product 2</span></span></td>
<td><span data-ttu-id="a4920-611">20</span><span class="sxs-lookup"><span data-stu-id="a4920-611">20</span></span></td>
<td><span data-ttu-id="a4920-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a4920-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a4920-613">178.44</span><span class="sxs-lookup"><span data-stu-id="a4920-613">178.44</span></span></td>
<td><span data-ttu-id="a4920-614">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-615">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-615">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-616">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-616">Product 1</span></span></td>
<td><span data-ttu-id="a4920-617">60</span><span class="sxs-lookup"><span data-stu-id="a4920-617">60</span></span></td>
<td><span data-ttu-id="a4920-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a4920-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a4920-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a4920-619">4,487.12</span></span></td>
<td><span data-ttu-id="a4920-620">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-621">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-621">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-622">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-622">Product 2</span></span></td>
<td><span data-ttu-id="a4920-623">20</span><span class="sxs-lookup"><span data-stu-id="a4920-623">20</span></span></td>
<td><span data-ttu-id="a4920-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a4920-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a4920-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a4920-625">1,495.71</span></span></td>
<td><span data-ttu-id="a4920-626">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4920-627">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="a4920-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-628">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-628">Cost object</span></span></th>
<th><span data-ttu-id="a4920-629">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="a4920-629">Magnitude</span></span></th>
<th><span data-ttu-id="a4920-630">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="a4920-630">Allocation factor</span></span></th>
<th><span data-ttu-id="a4920-631">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-631">Amount</span></span></th>
<th><span data-ttu-id="a4920-632">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-633">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-633">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-634">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-634">Product 1</span></span></td>
<td><span data-ttu-id="a4920-635">80</span><span class="sxs-lookup"><span data-stu-id="a4920-635">80</span></span></td>
<td><span data-ttu-id="a4920-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a4920-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a4920-637">241.05</span><span class="sxs-lookup"><span data-stu-id="a4920-637">241.05</span></span></td>
<td><span data-ttu-id="a4920-638">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-639">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-639">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-640">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-640">Product 2</span></span></td>
<td><span data-ttu-id="a4920-641">15</span><span class="sxs-lookup"><span data-stu-id="a4920-641">15</span></span></td>
<td><span data-ttu-id="a4920-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a4920-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a4920-643">45.20</span><span class="sxs-lookup"><span data-stu-id="a4920-643">45.20</span></span></td>
<td><span data-ttu-id="a4920-644">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-645">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-645">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-646">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-646">Product 1</span></span></td>
<td><span data-ttu-id="a4920-647">80</span><span class="sxs-lookup"><span data-stu-id="a4920-647">80</span></span></td>
<td><span data-ttu-id="a4920-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a4920-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a4920-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a4920-649">2,507.09</span></span></td>
<td><span data-ttu-id="a4920-650">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-651">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-651">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-652">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-652">Product 2</span></span></td>
<td><span data-ttu-id="a4920-653">15</span><span class="sxs-lookup"><span data-stu-id="a4920-653">15</span></span></td>
<td><span data-ttu-id="a4920-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a4920-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a4920-655">470.08</span><span class="sxs-lookup"><span data-stu-id="a4920-655">470.08</span></span></td>
<td><span data-ttu-id="a4920-656">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a4920-657">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="a4920-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-658">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-658">Journal</span></span></th>
<th><span data-ttu-id="a4920-659">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="a4920-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a4920-660">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a4920-661">Versija</span><span class="sxs-lookup"><span data-stu-id="a4920-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-662">00004</span><span class="sxs-lookup"><span data-stu-id="a4920-662">00004</span></span></td>
<td><span data-ttu-id="a4920-663">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="a4920-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a4920-664">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="a4920-664">Fiscal</span></span></td>
<td><span data-ttu-id="a4920-665">2017</span><span class="sxs-lookup"><span data-stu-id="a4920-665">2017</span></span></td>
<td><span data-ttu-id="a4920-666">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-666">Period 1</span></span></td>
<td><span data-ttu-id="a4920-667">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="a4920-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a4920-668">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="a4920-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a4920-669">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-670">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-671">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-671">Cost element</span></span></th>
<th><span data-ttu-id="a4920-672">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-672">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-673">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-674">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-675">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-675">CC001</span></span></td>
<td><span data-ttu-id="a4920-676">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-676">HR</span></span></td>
<td><span data-ttu-id="a4920-677">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-677">10001</span></span></td>
<td><span data-ttu-id="a4920-678">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-678">Electricity</span></span></td>
<td><span data-ttu-id="a4920-679">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-679">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-680">500,00</span><span class="sxs-lookup"><span data-stu-id="a4920-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-681">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-682">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-682">CC001</span></span></td>
<td><span data-ttu-id="a4920-683">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-683">HR</span></span></td>
<td><span data-ttu-id="a4920-684">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-684">10001</span></span></td>
<td><span data-ttu-id="a4920-685">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-685">Electricity</span></span></td>
<td><span data-ttu-id="a4920-686">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-686">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a4920-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-688">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-689">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-689">CC002</span></span></td>
<td><span data-ttu-id="a4920-690">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-690">Finance</span></span></td>
<td><span data-ttu-id="a4920-691">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-691">10001</span></span></td>
<td><span data-ttu-id="a4920-692">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-692">Electricity</span></span></td>
<td><span data-ttu-id="a4920-693">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-693">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-694">675.00</span><span class="sxs-lookup"><span data-stu-id="a4920-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-695">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-696">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-696">CC002</span></span></td>
<td><span data-ttu-id="a4920-697">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-697">Finance</span></span></td>
<td><span data-ttu-id="a4920-698">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-698">10001</span></span></td>
<td><span data-ttu-id="a4920-699">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-699">Electricity</span></span></td>
<td><span data-ttu-id="a4920-700">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-700">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a4920-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-702">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-703">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-703">CC003</span></span></td>
<td><span data-ttu-id="a4920-704">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-704">Assembly</span></span></td>
<td><span data-ttu-id="a4920-705">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-705">10001</span></span></td>
<td><span data-ttu-id="a4920-706">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-706">Electricity</span></span></td>
<td><span data-ttu-id="a4920-707">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-707">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-708">713.75</span><span class="sxs-lookup"><span data-stu-id="a4920-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-709">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-710">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-710">CC003</span></span></td>
<td><span data-ttu-id="a4920-711">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-711">Assembly</span></span></td>
<td><span data-ttu-id="a4920-712">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-712">10001</span></span></td>
<td><span data-ttu-id="a4920-713">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-713">Electricity</span></span></td>
<td><span data-ttu-id="a4920-714">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-714">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a4920-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-716">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-717">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-717">CC003</span></span></td>
<td><span data-ttu-id="a4920-718">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-718">Packaging</span></span></td>
<td><span data-ttu-id="a4920-719">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-719">10001</span></span></td>
<td><span data-ttu-id="a4920-720">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-720">Electricity</span></span></td>
<td><span data-ttu-id="a4920-721">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-721">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-722">286.25</span><span class="sxs-lookup"><span data-stu-id="a4920-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-723">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-724">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-724">CC003</span></span></td>
<td><span data-ttu-id="a4920-725">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-725">Packaging</span></span></td>
<td><span data-ttu-id="a4920-726">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-726">10001</span></span></td>
<td><span data-ttu-id="a4920-727">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-727">Electricity</span></span></td>
<td><span data-ttu-id="a4920-728">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-728">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a4920-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-730">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-731">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-731">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-732">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-732">Product 1</span></span></td>
<td><span data-ttu-id="a4920-733">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-733">10001</span></span></td>
<td><span data-ttu-id="a4920-734">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-734">Electricity</span></span></td>
<td><span data-ttu-id="a4920-735">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-735">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-736">776.36</span><span class="sxs-lookup"><span data-stu-id="a4920-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-737">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-738">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-738">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-739">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-739">Product 1</span></span></td>
<td><span data-ttu-id="a4920-740">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-740">10001</span></span></td>
<td><span data-ttu-id="a4920-741">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-741">Electricity</span></span></td>
<td><span data-ttu-id="a4920-742">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-742">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a4920-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-744">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-745">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-745">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-746">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-746">Product 1</span></span></td>
<td><span data-ttu-id="a4920-747">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-747">10001</span></span></td>
<td><span data-ttu-id="a4920-748">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-748">Electricity</span></span></td>
<td><span data-ttu-id="a4920-749">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-749">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-750">223.64</span><span class="sxs-lookup"><span data-stu-id="a4920-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-751">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="a4920-752">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-752">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-753">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-753">Product 1</span></span></td>
<td><span data-ttu-id="a4920-754">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-754">10001</span></span></td>
<td><span data-ttu-id="a4920-755">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-755">Electricity</span></span></td>
<td><span data-ttu-id="a4920-756">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-756">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a4920-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a4920-758">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="a4920-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a4920-759">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a4920-760">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-760">Cost element</span></span></th>
<th><span data-ttu-id="a4920-761">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="a4920-761">Cost behavior</span></span></th>
<th><span data-ttu-id="a4920-762">Suma</span><span class="sxs-lookup"><span data-stu-id="a4920-762">Amount</span></span></th>
<th><span data-ttu-id="a4920-763">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="a4920-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a4920-764">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-764">CC001</span></span></td>
<td><span data-ttu-id="a4920-765">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-765">HR</span></span></td>
<td><span data-ttu-id="a4920-766">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-766">10001</span></span></td>
<td><span data-ttu-id="a4920-767">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-767">Electricity</span></span></td>
<td><span data-ttu-id="a4920-768">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-768">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="a4920-769">-500.00</span></span></td>
<td><span data-ttu-id="a4920-770">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-771">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-771">CC002</span></span></td>
<td><span data-ttu-id="a4920-772">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-772">Finance</span></span></td>
<td><span data-ttu-id="a4920-773">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-773">10001</span></span></td>
<td><span data-ttu-id="a4920-774">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-774">Electricity</span></span></td>
<td><span data-ttu-id="a4920-775">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-775">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-776">175.00</span><span class="sxs-lookup"><span data-stu-id="a4920-776">175.00</span></span></td>
<td><span data-ttu-id="a4920-777">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-778">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-778">CC003</span></span></td>
<td><span data-ttu-id="a4920-779">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-779">Assembly</span></span></td>
<td><span data-ttu-id="a4920-780">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-780">10001</span></span></td>
<td><span data-ttu-id="a4920-781">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-781">Electricity</span></span></td>
<td><span data-ttu-id="a4920-782">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-782">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-783">275.00</span><span class="sxs-lookup"><span data-stu-id="a4920-783">275.00</span></span></td>
<td><span data-ttu-id="a4920-784">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-785">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-785">CC004</span></span></td>
<td><span data-ttu-id="a4920-786">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-786">Packaging</span></span></td>
<td><span data-ttu-id="a4920-787">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-787">10001</span></span></td>
<td><span data-ttu-id="a4920-788">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-788">Electricity</span></span></td>
<td><span data-ttu-id="a4920-789">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-789">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-790">50,00</span><span class="sxs-lookup"><span data-stu-id="a4920-790">50,00</span></span></td>
<td><span data-ttu-id="a4920-791">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-792">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-792">CC001</span></span></td>
<td><span data-ttu-id="a4920-793">Personalas</span><span class="sxs-lookup"><span data-stu-id="a4920-793">HR</span></span></td>
<td><span data-ttu-id="a4920-794">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-794">10001</span></span></td>
<td><span data-ttu-id="a4920-795">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-795">Electricity</span></span></td>
<td><span data-ttu-id="a4920-796">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-796">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="a4920-797">-1,245.71</span></span></td>
<td><span data-ttu-id="a4920-798">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-799">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-799">CC002</span></span></td>
<td><span data-ttu-id="a4920-800">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-800">Finance</span></span></td>
<td><span data-ttu-id="a4920-801">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-801">10001</span></span></td>
<td><span data-ttu-id="a4920-802">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-802">Electricity</span></span></td>
<td><span data-ttu-id="a4920-803">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-803">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-804">436.00</span><span class="sxs-lookup"><span data-stu-id="a4920-804">436.00</span></span></td>
<td><span data-ttu-id="a4920-805">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-806">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-806">CC003</span></span></td>
<td><span data-ttu-id="a4920-807">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-807">Assembly</span></span></td>
<td><span data-ttu-id="a4920-808">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-808">10001</span></span></td>
<td><span data-ttu-id="a4920-809">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-809">Electricity</span></span></td>
<td><span data-ttu-id="a4920-810">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-810">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-811">685.14</span><span class="sxs-lookup"><span data-stu-id="a4920-811">685.14</span></span></td>
<td><span data-ttu-id="a4920-812">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-813">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-813">CC004</span></span></td>
<td><span data-ttu-id="a4920-814">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-814">Packaging</span></span></td>
<td><span data-ttu-id="a4920-815">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-815">10001</span></span></td>
<td><span data-ttu-id="a4920-816">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-816">Electricity</span></span></td>
<td><span data-ttu-id="a4920-817">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-817">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-818">124.57</span><span class="sxs-lookup"><span data-stu-id="a4920-818">124.57</span></span></td>
<td><span data-ttu-id="a4920-819">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-820">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-820">CC002</span></span></td>
<td><span data-ttu-id="a4920-821">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-821">Finance</span></span></td>
<td><span data-ttu-id="a4920-822">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-822">10001</span></span></td>
<td><span data-ttu-id="a4920-823">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-823">Electricity</span></span></td>
<td><span data-ttu-id="a4920-824">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-824">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="a4920-825">-675.00</span></span></td>
<td><span data-ttu-id="a4920-826">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-827">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-827">CC003</span></span></td>
<td><span data-ttu-id="a4920-828">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-828">Assembly</span></span></td>
<td><span data-ttu-id="a4920-829">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-829">10001</span></span></td>
<td><span data-ttu-id="a4920-830">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-830">Electricity</span></span></td>
<td><span data-ttu-id="a4920-831">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-831">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-832">438.75</span><span class="sxs-lookup"><span data-stu-id="a4920-832">438.75</span></span></td>
<td><span data-ttu-id="a4920-833">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-834">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-834">CC004</span></span></td>
<td><span data-ttu-id="a4920-835">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-835">Packaging</span></span></td>
<td><span data-ttu-id="a4920-836">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-836">10001</span></span></td>
<td><span data-ttu-id="a4920-837">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-837">Electricity</span></span></td>
<td><span data-ttu-id="a4920-838">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-838">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-839">236.25</span><span class="sxs-lookup"><span data-stu-id="a4920-839">236.25</span></span></td>
<td><span data-ttu-id="a4920-840">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-841">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-841">CC002</span></span></td>
<td><span data-ttu-id="a4920-842">Finansai</span><span class="sxs-lookup"><span data-stu-id="a4920-842">Finance</span></span></td>
<td><span data-ttu-id="a4920-843">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-843">10001</span></span></td>
<td><span data-ttu-id="a4920-844">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-844">Electricity</span></span></td>
<td><span data-ttu-id="a4920-845">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-845">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="a4920-846">-8,150.29</span></span></td>
<td><span data-ttu-id="a4920-847">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-848">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-848">CC003</span></span></td>
<td><span data-ttu-id="a4920-849">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-849">Assembly</span></span></td>
<td><span data-ttu-id="a4920-850">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-850">10001</span></span></td>
<td><span data-ttu-id="a4920-851">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-851">Electricity</span></span></td>
<td><span data-ttu-id="a4920-852">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-852">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a4920-853">5,297.69</span></span></td>
<td><span data-ttu-id="a4920-854">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-855">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-855">CC004</span></span></td>
<td><span data-ttu-id="a4920-856">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="a4920-856">Packaging</span></span></td>
<td><span data-ttu-id="a4920-857">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-857">10001</span></span></td>
<td><span data-ttu-id="a4920-858">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-858">Electricity</span></span></td>
<td><span data-ttu-id="a4920-859">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-859">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a4920-860">2,852.60</span></span></td>
<td><span data-ttu-id="a4920-861">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-862">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-862">CC003</span></span></td>
<td><span data-ttu-id="a4920-863">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-863">Assembly</span></span></td>
<td><span data-ttu-id="a4920-864">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-864">10001</span></span></td>
<td><span data-ttu-id="a4920-865">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-865">Electricity</span></span></td>
<td><span data-ttu-id="a4920-866">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-866">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="a4920-867">-713.75</span></span></td>
<td><span data-ttu-id="a4920-868">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-869">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-869">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-870">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-870">Product 1</span></span></td>
<td><span data-ttu-id="a4920-871">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-871">10001</span></span></td>
<td><span data-ttu-id="a4920-872">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-872">Electricity</span></span></td>
<td><span data-ttu-id="a4920-873">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-873">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-874">535.31</span><span class="sxs-lookup"><span data-stu-id="a4920-874">535.31</span></span></td>
<td><span data-ttu-id="a4920-875">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-876">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-876">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-877">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-877">Product 2</span></span></td>
<td><span data-ttu-id="a4920-878">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-878">10001</span></span></td>
<td><span data-ttu-id="a4920-879">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-879">Electricity</span></span></td>
<td><span data-ttu-id="a4920-880">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-880">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-881">178.44</span><span class="sxs-lookup"><span data-stu-id="a4920-881">178.44</span></span></td>
<td><span data-ttu-id="a4920-882">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-883">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-883">CC003</span></span></td>
<td><span data-ttu-id="a4920-884">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-884">Assembly</span></span></td>
<td><span data-ttu-id="a4920-885">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-885">10001</span></span></td>
<td><span data-ttu-id="a4920-886">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-886">Electricity</span></span></td>
<td><span data-ttu-id="a4920-887">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-887">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="a4920-888">-5,982.83</span></span></td>
<td><span data-ttu-id="a4920-889">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-890">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-890">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-891">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-891">Product 1</span></span></td>
<td><span data-ttu-id="a4920-892">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-892">10001</span></span></td>
<td><span data-ttu-id="a4920-893">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-893">Electricity</span></span></td>
<td><span data-ttu-id="a4920-894">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-894">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a4920-895">4,487.12</span></span></td>
<td><span data-ttu-id="a4920-896">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-897">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-897">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-898">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-898">Product 2</span></span></td>
<td><span data-ttu-id="a4920-899">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-899">10001</span></span></td>
<td><span data-ttu-id="a4920-900">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-900">Electricity</span></span></td>
<td><span data-ttu-id="a4920-901">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-901">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a4920-902">1,495.71</span></span></td>
<td><span data-ttu-id="a4920-903">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-904">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-904">CC003</span></span></td>
<td><span data-ttu-id="a4920-905">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-905">Assembly</span></span></td>
<td><span data-ttu-id="a4920-906">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-906">10001</span></span></td>
<td><span data-ttu-id="a4920-907">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-907">Electricity</span></span></td>
<td><span data-ttu-id="a4920-908">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-908">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="a4920-909">-286.25</span></span></td>
<td><span data-ttu-id="a4920-910">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-911">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-911">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-912">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-912">Product 1</span></span></td>
<td><span data-ttu-id="a4920-913">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-913">10001</span></span></td>
<td><span data-ttu-id="a4920-914">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-914">Electricity</span></span></td>
<td><span data-ttu-id="a4920-915">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-915">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-916">241.05</span><span class="sxs-lookup"><span data-stu-id="a4920-916">241.05</span></span></td>
<td><span data-ttu-id="a4920-917">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-918">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-918">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-919">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-919">Product 2</span></span></td>
<td><span data-ttu-id="a4920-920">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-920">10001</span></span></td>
<td><span data-ttu-id="a4920-921">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-921">Electricity</span></span></td>
<td><span data-ttu-id="a4920-922">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-922">Fixed cost</span></span></td>
<td><span data-ttu-id="a4920-923">45.20</span><span class="sxs-lookup"><span data-stu-id="a4920-923">45.20</span></span></td>
<td><span data-ttu-id="a4920-924">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-925">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-925">CC003</span></span></td>
<td><span data-ttu-id="a4920-926">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="a4920-926">Assembly</span></span></td>
<td><span data-ttu-id="a4920-927">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-927">10001</span></span></td>
<td><span data-ttu-id="a4920-928">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-928">Electricity</span></span></td>
<td><span data-ttu-id="a4920-929">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-929">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="a4920-930">-2,977.17</span></span></td>
<td><span data-ttu-id="a4920-931">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-932">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-932">Prod 1</span></span></td>
<td><span data-ttu-id="a4920-933">1 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-933">Product 1</span></span></td>
<td><span data-ttu-id="a4920-934">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-934">10001</span></span></td>
<td><span data-ttu-id="a4920-935">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-935">Electricity</span></span></td>
<td><span data-ttu-id="a4920-936">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-936">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a4920-937">2,507.09</span></span></td>
<td><span data-ttu-id="a4920-938">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a4920-939">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-939">Prod 2</span></span></td>
<td><span data-ttu-id="a4920-940">2 produktas</span><span class="sxs-lookup"><span data-stu-id="a4920-940">Product 2</span></span></td>
<td><span data-ttu-id="a4920-941">10001</span><span class="sxs-lookup"><span data-stu-id="a4920-941">10001</span></span></td>
<td><span data-ttu-id="a4920-942">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-942">Electricity</span></span></td>
<td><span data-ttu-id="a4920-943">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-943">Variable cost</span></span></td>
<td><span data-ttu-id="a4920-944">470.08</span><span class="sxs-lookup"><span data-stu-id="a4920-944">470.08</span></span></td>
<td><span data-ttu-id="a4920-945">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a4920-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a4920-946">Išvada</span><span class="sxs-lookup"><span data-stu-id="a4920-946">Conclusion</span></span>
<span data-ttu-id="a4920-947">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="a4920-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a4920-948">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="a4920-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a4920-949">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="a4920-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a4920-950">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="a4920-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a4920-951">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="a4920-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a4920-952">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="a4920-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a4920-953">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="a4920-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a4920-954">CC099</span><span class="sxs-lookup"><span data-stu-id="a4920-954">CC099</span></span></th>
<th><span data-ttu-id="a4920-955">CC001</span><span class="sxs-lookup"><span data-stu-id="a4920-955">CC001</span></span></th>
<th><span data-ttu-id="a4920-956">CC002</span><span class="sxs-lookup"><span data-stu-id="a4920-956">CC002</span></span></th>
<th><span data-ttu-id="a4920-957">CC003</span><span class="sxs-lookup"><span data-stu-id="a4920-957">CC003</span></span></th>
<th><span data-ttu-id="a4920-958">CC004</span><span class="sxs-lookup"><span data-stu-id="a4920-958">CC004</span></span></th>
<th><span data-ttu-id="a4920-959">1 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-959">Proj 1</span></span></th>
<th><span data-ttu-id="a4920-960">2 projektas</span><span class="sxs-lookup"><span data-stu-id="a4920-960">Proj 2</span></span></th>
<th><span data-ttu-id="a4920-961">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-961">Prod 1</span></span></th>
<th><span data-ttu-id="a4920-962">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="a4920-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a4920-963">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="a4920-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a4920-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a4920-973">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="a4920-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-974">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a4920-975">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-976">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-977">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-978">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-979">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-980">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a4920-981">776.36</span><span class="sxs-lookup"><span data-stu-id="a4920-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-982">223.64</span><span class="sxs-lookup"><span data-stu-id="a4920-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a4920-984">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="a4920-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-985">000</span><span class="sxs-lookup"><span data-stu-id="a4920-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-986">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-987">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-988">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-989">0,00</span><span class="sxs-lookup"><span data-stu-id="a4920-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-990">30,00</span><span class="sxs-lookup"><span data-stu-id="a4920-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-991">10,00</span><span class="sxs-lookup"><span data-stu-id="a4920-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a4920-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a4920-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a4920-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="a4920-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a4920-995">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="a4920-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a4920-996">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="a4920-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a4920-997">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="a4920-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a4920-998">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="a4920-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a4920-999">Išsamesnės informacijos žr. temoje Išlaidų sumavimo strategija.</span><span class="sxs-lookup"><span data-stu-id="a4920-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="a4920-1000">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="a4920-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




