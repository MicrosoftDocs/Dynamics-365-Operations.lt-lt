---
title: "Pridėtinių išlaidų skaičiavimas"
description: "Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai."
author: YuyuScheller
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="d4d8e-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d4d8e-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="d4d8e-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-105">Term definition</span></span>
---------------

<span data-ttu-id="d4d8e-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="d4d8e-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="d4d8e-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="d4d8e-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-109">Rent</span></span>
-   <span data-ttu-id="d4d8e-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-110">Electricity</span></span>
-   <span data-ttu-id="d4d8e-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="d4d8e-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="d4d8e-112">Overhead calculation overview</span></span>
<span data-ttu-id="d4d8e-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="d4d8e-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="d4d8e-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="d4d8e-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="d4d8e-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="d4d8e-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="d4d8e-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-119">Version type</span></span>
-   <span data-ttu-id="d4d8e-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-120">Date and time</span></span>
-   <span data-ttu-id="d4d8e-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="d4d8e-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="d4d8e-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-122">Fiscal year</span></span>
-   <span data-ttu-id="d4d8e-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-123">Fiscal period</span></span>

<span data-ttu-id="d4d8e-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="d4d8e-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="d4d8e-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="d4d8e-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="d4d8e-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="d4d8e-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="d4d8e-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="d4d8e-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="d4d8e-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="d4d8e-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="d4d8e-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="d4d8e-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="d4d8e-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="d4d8e-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="d4d8e-140">Main account</span></span></th>
<th><span data-ttu-id="d4d8e-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="d4d8e-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-143">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-143">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-144">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-145">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-145">10001</span></span></td>
<td><span data-ttu-id="d4d8e-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-146">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="d4d8e-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="d4d8e-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="d4d8e-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="d4d8e-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-151">Define the cost behavior rule</span></span>

<span data-ttu-id="d4d8e-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="d4d8e-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="d4d8e-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="d4d8e-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="d4d8e-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="d4d8e-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="d4d8e-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="d4d8e-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="d4d8e-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="d4d8e-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-160">Journal</span></span></th>
<th><span data-ttu-id="d4d8e-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d4d8e-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d4d8e-163">Versija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-164">00001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-164">00001</span></span></td>
<td><span data-ttu-id="d4d8e-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="d4d8e-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-166">Fiscal</span></span></td>
<td><span data-ttu-id="d4d8e-167">2017</span><span class="sxs-lookup"><span data-stu-id="d4d8e-167">2017</span></span></td>
<td><span data-ttu-id="d4d8e-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-168">Period 1</span></span></td>
<td><span data-ttu-id="d4d8e-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d4d8e-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-173">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-174">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-175">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-177">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-177">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-178">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-179">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-179">10001</span></span></td>
<td><span data-ttu-id="d4d8e-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-180">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="d4d8e-181">Unclassified</span></span></td>
<td><span data-ttu-id="d4d8e-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d4d8e-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-185">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-186">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-187">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-187">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-189">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-189">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-190">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-191">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-191">10001</span></span></td>
<td><span data-ttu-id="d4d8e-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-192">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="d4d8e-193">Unclassified</span></span></td>
<td><span data-ttu-id="d4d8e-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-194">10,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-196">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-196">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-197">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-198">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-198">10001</span></span></td>
<td><span data-ttu-id="d4d8e-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-199">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="d4d8e-200">Unclassified</span></span></td>
<td><span data-ttu-id="d4d8e-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-201">-10,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-203">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-203">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-204">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-205">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-205">10001</span></span></td>
<td><span data-ttu-id="d4d8e-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-206">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-207">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-208">1,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-210">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-210">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-211">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-212">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-212">10001</span></span></td>
<td><span data-ttu-id="d4d8e-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-213">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-214">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-215">9,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-217">Išsamios informacijos apie išlaidų veikimo būdą žr. temoje Išlaidų veikimo būdo strategija.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="d4d8e-218">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="d4d8e-219">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="d4d8e-220">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="d4d8e-221">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="d4d8e-222">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-222">Define the cost distribution rule</span></span>

<span data-ttu-id="d4d8e-223">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="d4d8e-224">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="d4d8e-225">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="d4d8e-226">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="d4d8e-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="d4d8e-227">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="d4d8e-228">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-229">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-229">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="d4d8e-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-231">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-231">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-232">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-232">HR</span></span></td>
<td><span data-ttu-id="d4d8e-233">1000</span><span class="sxs-lookup"><span data-stu-id="d4d8e-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-234">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-234">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-235">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-235">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-236">6,000</span><span class="sxs-lookup"><span data-stu-id="d4d8e-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-237">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-237">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-238">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-238">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-239">0</span><span class="sxs-lookup"><span data-stu-id="d4d8e-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-240">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-241">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-241">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-242">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-242">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-243">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-243">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-244">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-245">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-245">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-246">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-246">HR</span></span></td>
<td><span data-ttu-id="d4d8e-247">1000</span><span class="sxs-lookup"><span data-stu-id="d4d8e-247">1,000</span></span></td>
<td><span data-ttu-id="d4d8e-248">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-250">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-250">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-251">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-251">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-252">6,000</span><span class="sxs-lookup"><span data-stu-id="d4d8e-252">6,000</span></span></td>
<td><span data-ttu-id="d4d8e-253">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d4d8e-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-255">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-255">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-256">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-256">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-257">0</span><span class="sxs-lookup"><span data-stu-id="d4d8e-257">0</span></span></td>
<td><span data-ttu-id="d4d8e-258">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-259">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-260">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="d4d8e-261">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-262">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-262">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-263">Formulė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-263">Formula</span></span></th>
<th><span data-ttu-id="d4d8e-264">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-264">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-265">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-265">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-266">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-267">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-267">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-268">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-268">HR</span></span></td>
<td><span data-ttu-id="d4d8e-269">{1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d4d8e-270">1</span><span class="sxs-lookup"><span data-stu-id="d4d8e-270">1</span></span></td>
<td><span data-ttu-id="d4d8e-271">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-272">500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-273">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-273">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-274">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-274">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-275">{6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d4d8e-276">1</span><span class="sxs-lookup"><span data-stu-id="d4d8e-276">1</span></span></td>
<td><span data-ttu-id="d4d8e-277">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-278">500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-279">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-279">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-280">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-280">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-281">{0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="d4d8e-282">0</span><span class="sxs-lookup"><span data-stu-id="d4d8e-282">0</span></span></td>
<td><span data-ttu-id="d4d8e-283">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-284">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d4d8e-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-286">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-286">Journal</span></span></th>
<th><span data-ttu-id="d4d8e-287">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d4d8e-288">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d4d8e-289">Versija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-290">00002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-290">00002</span></span></td>
<td><span data-ttu-id="d4d8e-291">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="d4d8e-292">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-292">Fiscal</span></span></td>
<td><span data-ttu-id="d4d8e-293">2017</span><span class="sxs-lookup"><span data-stu-id="d4d8e-293">2017</span></span></td>
<td><span data-ttu-id="d4d8e-294">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-294">Period 1</span></span></td>
<td><span data-ttu-id="d4d8e-295">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d4d8e-296">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-297">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-298">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-299">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-299">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-300">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-300">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-301">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-302">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-303">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-303">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-304">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-304">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-305">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-305">10001</span></span></td>
<td><span data-ttu-id="d4d8e-306">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-306">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-307">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-307">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-308">1000,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-309">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-310">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-310">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-311">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-311">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-312">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-312">10001</span></span></td>
<td><span data-ttu-id="d4d8e-313">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-313">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-314">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-314">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d4d8e-316">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-317">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-318">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-318">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-319">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-319">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-320">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-320">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-321">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-322">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-322">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-323">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-323">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-324">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-324">10001</span></span></td>
<td><span data-ttu-id="d4d8e-325">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-325">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-326">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-326">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-327">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-327">-1,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-328">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-329">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-329">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-330">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-330">HR</span></span></td>
<td><span data-ttu-id="d4d8e-331">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-331">10001</span></span></td>
<td><span data-ttu-id="d4d8e-332">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-332">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-333">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-333">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-334">500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-334">500.00</span></span></td>
<td><span data-ttu-id="d4d8e-335">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-336">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-336">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-337">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-337">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-338">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-338">10001</span></span></td>
<td><span data-ttu-id="d4d8e-339">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-339">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-340">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-340">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-341">500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-341">500.00</span></span></td>
<td><span data-ttu-id="d4d8e-342">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-343">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-343">CC099</span></span></td>
<td><span data-ttu-id="d4d8e-344">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="d4d8e-344">Default cost center</span></span></td>
<td><span data-ttu-id="d4d8e-345">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-345">10001</span></span></td>
<td><span data-ttu-id="d4d8e-346">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-346">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-347">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-347">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-348">-9,000.00</span></span></td>
<td><span data-ttu-id="d4d8e-349">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-350">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-350">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-351">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-351">HR</span></span></td>
<td><span data-ttu-id="d4d8e-352">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-352">10001</span></span></td>
<td><span data-ttu-id="d4d8e-353">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-353">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-354">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-354">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-355">1,285.71</span></span></td>
<td><span data-ttu-id="d4d8e-356">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-357">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-357">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-358">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-358">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-359">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-359">10001</span></span></td>
<td><span data-ttu-id="d4d8e-360">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-360">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-361">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-361">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="d4d8e-362">7,714.29</span></span></td>
<td><span data-ttu-id="d4d8e-363">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-364">Daugiau informacijos apie išlaidų paskirstymą ir paskirstymo pagrindus žr. temose Išlaidų paskirstymo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="d4d8e-365">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="d4d8e-366">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="d4d8e-367">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="d4d8e-368">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="d4d8e-369">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-369">Define the overhead rate</span></span>

<span data-ttu-id="d4d8e-370">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="d4d8e-371">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-372">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-372">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-373">Valandos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-374">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-374">Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-375">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-375">Project 1</span></span></td>
<td><span data-ttu-id="d4d8e-376">3</span><span class="sxs-lookup"><span data-stu-id="d4d8e-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-377">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-377">Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-378">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-378">Project 2</span></span></td>
<td><span data-ttu-id="d4d8e-379">1</span><span class="sxs-lookup"><span data-stu-id="d4d8e-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-380">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-381">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-381">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-382">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-382">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-383">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-383">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-384">Vienetai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-384">Units</span></span></th>
<th><span data-ttu-id="d4d8e-385">Tarifas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-386">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-386">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-387">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-387">HR</span></span></td>
<td><span data-ttu-id="d4d8e-388">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-388">10001</span></span></td>
<td><span data-ttu-id="d4d8e-389">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-389">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-390">1</span><span class="sxs-lookup"><span data-stu-id="d4d8e-390">1</span></span></td>
<td><span data-ttu-id="d4d8e-391">10</span><span class="sxs-lookup"><span data-stu-id="d4d8e-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-392">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-393">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-393">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-394">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-394">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-395">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-395">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-396">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-396">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-397">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-398">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-398">Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-399">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-399">Project 1</span></span></td>
<td><span data-ttu-id="d4d8e-400">3</span><span class="sxs-lookup"><span data-stu-id="d4d8e-400">3</span></span></td>
<td><span data-ttu-id="d4d8e-401">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-401">10001</span></span></td>
<td><span data-ttu-id="d4d8e-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d4d8e-403">30,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-404">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-404">Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-405">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-405">Project 2</span></span></td>
<td><span data-ttu-id="d4d8e-406">1</span><span class="sxs-lookup"><span data-stu-id="d4d8e-406">1</span></span></td>
<td><span data-ttu-id="d4d8e-407">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-407">10001</span></span></td>
<td><span data-ttu-id="d4d8e-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="d4d8e-409">10,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="d4d8e-410">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-411">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-411">Journal</span></span></th>
<th><span data-ttu-id="d4d8e-412">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d4d8e-413">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d4d8e-414">Versija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-415">00003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-415">00003</span></span></td>
<td><span data-ttu-id="d4d8e-416">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="d4d8e-417">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-417">Fiscal</span></span></td>
<td><span data-ttu-id="d4d8e-418">2017</span><span class="sxs-lookup"><span data-stu-id="d4d8e-418">2017</span></span></td>
<td><span data-ttu-id="d4d8e-419">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-419">Period 1</span></span></td>
<td><span data-ttu-id="d4d8e-420">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="d4d8e-421">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-422">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-423">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-423">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-424">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-425">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-426">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-426">Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-427">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-428">3,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-429">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-430">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-430">Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-431">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-432">1,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d4d8e-433">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-434">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-435">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-435">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-436">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-436">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-437">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-437">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-438">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-439">CC0001</span></span></td>
<td><span data-ttu-id="d4d8e-440">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-440">HR</span></span></td>
<td><span data-ttu-id="d4d8e-441">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-441">10001</span></span></td>
<td><span data-ttu-id="d4d8e-442">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-442">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-443">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-443">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-444">-30.00</span></span></td>
<td><span data-ttu-id="d4d8e-445">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-446">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-446">Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-447">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="d4d8e-448">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-448">10001</span></span></td>
<td><span data-ttu-id="d4d8e-449">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-449">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-450">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-450">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-451">30,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-451">30.00</span></span></td>
<td><span data-ttu-id="d4d8e-452">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-453">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-453">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-454">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-454">HR</span></span></td>
<td><span data-ttu-id="d4d8e-455">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-455">10001</span></span></td>
<td><span data-ttu-id="d4d8e-456">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-456">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-457">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-457">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-458">-10.00</span></span></td>
<td><span data-ttu-id="d4d8e-459">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-460">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-460">Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-461">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="d4d8e-462">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-462">10001</span></span></td>
<td><span data-ttu-id="d4d8e-463">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-463">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-464">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-464">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-465">10,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-465">10.00</span></span></td>
<td><span data-ttu-id="d4d8e-466">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-467">Išsamesnės informacijos apie pridėtinių išlaidų tarifo strategiją žr. temoje Pridėtinių išlaidų tarifo strategija ir Paskirstymo pagrindai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="d4d8e-468">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="d4d8e-469">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="d4d8e-470">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="d4d8e-471">„Finance and Operations” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="d4d8e-472">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="d4d8e-473">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="d4d8e-474">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="d4d8e-475">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="d4d8e-476">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="d4d8e-477">[![Abipusis metodas](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="d4d8e-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="d4d8e-478">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-478">Define the cost allocation</span></span>

<span data-ttu-id="d4d8e-479">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="d4d8e-480">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="d4d8e-481">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-482">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-482">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-483">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-484">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-484">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-485">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-485">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-486">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-487">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-487">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-488">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-488">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-489">55</span><span class="sxs-lookup"><span data-stu-id="d4d8e-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-490">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-490">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-491">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-491">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-492">10</span><span class="sxs-lookup"><span data-stu-id="d4d8e-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-493">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="d4d8e-494">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-495">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-495">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-496">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-497">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-497">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-498">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-498">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-499">65</span><span class="sxs-lookup"><span data-stu-id="d4d8e-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-500">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-500">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-501">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-501">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-502">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-503">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="d4d8e-504">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-505">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-505">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-506">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-507">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-507">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-508">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-508">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-509">60</span><span class="sxs-lookup"><span data-stu-id="d4d8e-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-510">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-510">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-511">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-511">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-512">20</span><span class="sxs-lookup"><span data-stu-id="d4d8e-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-513">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="d4d8e-514">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-515">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-515">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-516">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-517">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-517">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-518">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-518">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-519">80</span><span class="sxs-lookup"><span data-stu-id="d4d8e-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-520">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-520">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-521">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-521">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-522">15</span><span class="sxs-lookup"><span data-stu-id="d4d8e-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-523">**Pastaba:** programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="d4d8e-524">Išsamesnės informacijos apie statistinių priemonių teikimo įrankius žr. temoje Statistinės priemonės teikimo įrankio šablonas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="d4d8e-525">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.) Toliau pateikiamoje lentelėje rodoma, kas nutinka pritaikius personalo paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-526">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-526">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-527">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-527">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-528">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-528">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-529">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-529">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-530">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-531">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-531">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-532">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-532">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-533">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-533">35</span></span></td>
<td><span data-ttu-id="d4d8e-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d4d8e-535">175.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-535">175.00</span></span></td>
<td><span data-ttu-id="d4d8e-536">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-537">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-537">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-538">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-538">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-539">55</span><span class="sxs-lookup"><span data-stu-id="d4d8e-539">55</span></span></td>
<td><span data-ttu-id="d4d8e-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d4d8e-541">275.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-541">275.00</span></span></td>
<td><span data-ttu-id="d4d8e-542">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-543">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-543">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-544">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-544">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-545">10</span><span class="sxs-lookup"><span data-stu-id="d4d8e-545">10</span></span></td>
<td><span data-ttu-id="d4d8e-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="d4d8e-547">50,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-547">50.00</span></span></td>
<td><span data-ttu-id="d4d8e-548">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-549">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-549">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-550">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-550">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-551">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-551">35</span></span></td>
<td><span data-ttu-id="d4d8e-552">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d4d8e-553">436.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-553">436.00</span></span></td>
<td><span data-ttu-id="d4d8e-554">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-555">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-555">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-556">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-556">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-557">55</span><span class="sxs-lookup"><span data-stu-id="d4d8e-557">55</span></span></td>
<td><span data-ttu-id="d4d8e-558">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d4d8e-559">685.14</span><span class="sxs-lookup"><span data-stu-id="d4d8e-559">685.14</span></span></td>
<td><span data-ttu-id="d4d8e-560">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-561">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-561">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-562">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-562">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-563">10</span><span class="sxs-lookup"><span data-stu-id="d4d8e-563">10</span></span></td>
<td><span data-ttu-id="d4d8e-564">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="d4d8e-565">124.57</span><span class="sxs-lookup"><span data-stu-id="d4d8e-565">124.57</span></span></td>
<td><span data-ttu-id="d4d8e-566">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-567">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-568">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-568">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-569">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-569">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-570">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-570">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-571">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-571">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-572">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-573">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-573">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-574">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-574">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-575">65</span><span class="sxs-lookup"><span data-stu-id="d4d8e-575">65</span></span></td>
<td><span data-ttu-id="d4d8e-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d4d8e-577">438.75</span><span class="sxs-lookup"><span data-stu-id="d4d8e-577">438.75</span></span></td>
<td><span data-ttu-id="d4d8e-578">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-579">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-579">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-580">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-580">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-581">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-581">35</span></span></td>
<td><span data-ttu-id="d4d8e-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="d4d8e-583">236.25</span><span class="sxs-lookup"><span data-stu-id="d4d8e-583">236.25</span></span></td>
<td><span data-ttu-id="d4d8e-584">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-585">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-585">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-586">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-586">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-587">65</span><span class="sxs-lookup"><span data-stu-id="d4d8e-587">65</span></span></td>
<td><span data-ttu-id="d4d8e-588">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d4d8e-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d4d8e-589">5,297.69</span></span></td>
<td><span data-ttu-id="d4d8e-590">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-591">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-591">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-592">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-592">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-593">35</span><span class="sxs-lookup"><span data-stu-id="d4d8e-593">35</span></span></td>
<td><span data-ttu-id="d4d8e-594">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="d4d8e-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d4d8e-595">2,852.60</span></span></td>
<td><span data-ttu-id="d4d8e-596">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-597">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-598">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-598">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-599">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-599">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-600">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-600">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-601">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-601">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-602">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-603">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-603">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-604">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-604">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-605">60</span><span class="sxs-lookup"><span data-stu-id="d4d8e-605">60</span></span></td>
<td><span data-ttu-id="d4d8e-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d4d8e-607">535.31</span><span class="sxs-lookup"><span data-stu-id="d4d8e-607">535.31</span></span></td>
<td><span data-ttu-id="d4d8e-608">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-609">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-609">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-610">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-610">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-611">20</span><span class="sxs-lookup"><span data-stu-id="d4d8e-611">20</span></span></td>
<td><span data-ttu-id="d4d8e-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="d4d8e-613">178.44</span><span class="sxs-lookup"><span data-stu-id="d4d8e-613">178.44</span></span></td>
<td><span data-ttu-id="d4d8e-614">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-615">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-615">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-616">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-616">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-617">60</span><span class="sxs-lookup"><span data-stu-id="d4d8e-617">60</span></span></td>
<td><span data-ttu-id="d4d8e-618">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d4d8e-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d4d8e-619">4,487.12</span></span></td>
<td><span data-ttu-id="d4d8e-620">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-621">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-621">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-622">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-622">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-623">20</span><span class="sxs-lookup"><span data-stu-id="d4d8e-623">20</span></span></td>
<td><span data-ttu-id="d4d8e-624">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="d4d8e-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-625">1,495.71</span></span></td>
<td><span data-ttu-id="d4d8e-626">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4d8e-627">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-628">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-628">Cost object</span></span></th>
<th><span data-ttu-id="d4d8e-629">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="d4d8e-629">Magnitude</span></span></th>
<th><span data-ttu-id="d4d8e-630">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-630">Allocation factor</span></span></th>
<th><span data-ttu-id="d4d8e-631">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-631">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-632">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-633">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-633">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-634">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-634">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-635">80</span><span class="sxs-lookup"><span data-stu-id="d4d8e-635">80</span></span></td>
<td><span data-ttu-id="d4d8e-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d4d8e-637">241.05</span><span class="sxs-lookup"><span data-stu-id="d4d8e-637">241.05</span></span></td>
<td><span data-ttu-id="d4d8e-638">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-639">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-639">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-640">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-640">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-641">15</span><span class="sxs-lookup"><span data-stu-id="d4d8e-641">15</span></span></td>
<td><span data-ttu-id="d4d8e-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="d4d8e-643">45.20</span><span class="sxs-lookup"><span data-stu-id="d4d8e-643">45.20</span></span></td>
<td><span data-ttu-id="d4d8e-644">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-645">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-645">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-646">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-646">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-647">80</span><span class="sxs-lookup"><span data-stu-id="d4d8e-647">80</span></span></td>
<td><span data-ttu-id="d4d8e-648">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d4d8e-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d4d8e-649">2,507.09</span></span></td>
<td><span data-ttu-id="d4d8e-650">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-651">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-651">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-652">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-652">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-653">15</span><span class="sxs-lookup"><span data-stu-id="d4d8e-653">15</span></span></td>
<td><span data-ttu-id="d4d8e-654">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="d4d8e-655">470.08</span><span class="sxs-lookup"><span data-stu-id="d4d8e-655">470.08</span></span></td>
<td><span data-ttu-id="d4d8e-656">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="d4d8e-657">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-658">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-658">Journal</span></span></th>
<th><span data-ttu-id="d4d8e-659">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="d4d8e-660">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="d4d8e-661">Versija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-662">00004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-662">00004</span></span></td>
<td><span data-ttu-id="d4d8e-663">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="d4d8e-664">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-664">Fiscal</span></span></td>
<td><span data-ttu-id="d4d8e-665">2017</span><span class="sxs-lookup"><span data-stu-id="d4d8e-665">2017</span></span></td>
<td><span data-ttu-id="d4d8e-666">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-666">Period 1</span></span></td>
<td><span data-ttu-id="d4d8e-667">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="d4d8e-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="d4d8e-668">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4d8e-669">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-670">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-671">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-671">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-672">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-672">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-673">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-674">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-675">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-675">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-676">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-676">HR</span></span></td>
<td><span data-ttu-id="d4d8e-677">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-677">10001</span></span></td>
<td><span data-ttu-id="d4d8e-678">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-678">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-679">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-679">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-680">500,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-681">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-682">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-682">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-683">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-683">HR</span></span></td>
<td><span data-ttu-id="d4d8e-684">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-684">10001</span></span></td>
<td><span data-ttu-id="d4d8e-685">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-685">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-686">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-686">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-688">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-689">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-689">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-690">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-690">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-691">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-691">10001</span></span></td>
<td><span data-ttu-id="d4d8e-692">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-692">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-693">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-693">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-694">675.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-695">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-696">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-696">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-697">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-697">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-698">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-698">10001</span></span></td>
<td><span data-ttu-id="d4d8e-699">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-699">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-700">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-700">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="d4d8e-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-702">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-703">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-703">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-704">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-704">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-705">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-705">10001</span></span></td>
<td><span data-ttu-id="d4d8e-706">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-706">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-707">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-707">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-708">713.75</span><span class="sxs-lookup"><span data-stu-id="d4d8e-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-709">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-710">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-710">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-711">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-711">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-712">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-712">10001</span></span></td>
<td><span data-ttu-id="d4d8e-713">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-713">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-714">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-714">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="d4d8e-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-716">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-717">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-717">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-718">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-718">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-719">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-719">10001</span></span></td>
<td><span data-ttu-id="d4d8e-720">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-720">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-721">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-721">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-722">286.25</span><span class="sxs-lookup"><span data-stu-id="d4d8e-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-723">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-724">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-724">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-725">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-725">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-726">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-726">10001</span></span></td>
<td><span data-ttu-id="d4d8e-727">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-727">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-728">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-728">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="d4d8e-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-730">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-731">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-731">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-732">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-732">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-733">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-733">10001</span></span></td>
<td><span data-ttu-id="d4d8e-734">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-734">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-735">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-735">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-736">776.36</span><span class="sxs-lookup"><span data-stu-id="d4d8e-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-737">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-738">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-738">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-739">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-739">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-740">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-740">10001</span></span></td>
<td><span data-ttu-id="d4d8e-741">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-741">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-742">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-742">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d4d8e-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-744">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-745">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-745">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-746">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-746">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-747">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-747">10001</span></span></td>
<td><span data-ttu-id="d4d8e-748">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-748">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-749">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-749">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-750">223.64</span><span class="sxs-lookup"><span data-stu-id="d4d8e-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-751">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="d4d8e-752">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-752">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-753">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-753">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-754">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-754">10001</span></span></td>
<td><span data-ttu-id="d4d8e-755">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-755">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-756">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-756">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d4d8e-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="d4d8e-758">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="d4d8e-759">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="d4d8e-760">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-760">Cost element</span></span></th>
<th><span data-ttu-id="d4d8e-761">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-761">Cost behavior</span></span></th>
<th><span data-ttu-id="d4d8e-762">Suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-762">Amount</span></span></th>
<th><span data-ttu-id="d4d8e-763">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="d4d8e-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4d8e-764">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-764">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-765">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-765">HR</span></span></td>
<td><span data-ttu-id="d4d8e-766">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-766">10001</span></span></td>
<td><span data-ttu-id="d4d8e-767">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-767">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-768">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-768">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-769">-500.00</span></span></td>
<td><span data-ttu-id="d4d8e-770">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-771">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-771">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-772">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-772">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-773">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-773">10001</span></span></td>
<td><span data-ttu-id="d4d8e-774">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-774">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-775">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-775">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-776">175.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-776">175.00</span></span></td>
<td><span data-ttu-id="d4d8e-777">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-778">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-778">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-779">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-779">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-780">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-780">10001</span></span></td>
<td><span data-ttu-id="d4d8e-781">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-781">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-782">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-782">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-783">275.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-783">275.00</span></span></td>
<td><span data-ttu-id="d4d8e-784">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-785">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-785">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-786">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-786">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-787">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-787">10001</span></span></td>
<td><span data-ttu-id="d4d8e-788">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-788">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-789">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-789">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-790">50,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-790">50,00</span></span></td>
<td><span data-ttu-id="d4d8e-791">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-792">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-792">CC001</span></span></td>
<td><span data-ttu-id="d4d8e-793">Personalas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-793">HR</span></span></td>
<td><span data-ttu-id="d4d8e-794">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-794">10001</span></span></td>
<td><span data-ttu-id="d4d8e-795">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-795">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-796">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-796">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-797">-1,245.71</span></span></td>
<td><span data-ttu-id="d4d8e-798">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-799">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-799">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-800">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-800">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-801">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-801">10001</span></span></td>
<td><span data-ttu-id="d4d8e-802">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-802">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-803">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-803">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-804">436.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-804">436.00</span></span></td>
<td><span data-ttu-id="d4d8e-805">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-806">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-806">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-807">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-807">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-808">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-808">10001</span></span></td>
<td><span data-ttu-id="d4d8e-809">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-809">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-810">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-810">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-811">685.14</span><span class="sxs-lookup"><span data-stu-id="d4d8e-811">685.14</span></span></td>
<td><span data-ttu-id="d4d8e-812">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-813">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-813">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-814">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-814">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-815">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-815">10001</span></span></td>
<td><span data-ttu-id="d4d8e-816">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-816">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-817">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-817">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-818">124.57</span><span class="sxs-lookup"><span data-stu-id="d4d8e-818">124.57</span></span></td>
<td><span data-ttu-id="d4d8e-819">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-820">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-820">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-821">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-821">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-822">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-822">10001</span></span></td>
<td><span data-ttu-id="d4d8e-823">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-823">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-824">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-824">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-825">-675.00</span></span></td>
<td><span data-ttu-id="d4d8e-826">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-827">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-827">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-828">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-828">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-829">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-829">10001</span></span></td>
<td><span data-ttu-id="d4d8e-830">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-830">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-831">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-831">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-832">438.75</span><span class="sxs-lookup"><span data-stu-id="d4d8e-832">438.75</span></span></td>
<td><span data-ttu-id="d4d8e-833">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-834">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-834">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-835">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-835">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-836">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-836">10001</span></span></td>
<td><span data-ttu-id="d4d8e-837">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-837">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-838">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-838">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-839">236.25</span><span class="sxs-lookup"><span data-stu-id="d4d8e-839">236.25</span></span></td>
<td><span data-ttu-id="d4d8e-840">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-841">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-841">CC002</span></span></td>
<td><span data-ttu-id="d4d8e-842">Finansai</span><span class="sxs-lookup"><span data-stu-id="d4d8e-842">Finance</span></span></td>
<td><span data-ttu-id="d4d8e-843">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-843">10001</span></span></td>
<td><span data-ttu-id="d4d8e-844">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-844">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-845">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-845">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="d4d8e-846">-8,150.29</span></span></td>
<td><span data-ttu-id="d4d8e-847">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-848">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-848">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-849">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-849">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-850">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-850">10001</span></span></td>
<td><span data-ttu-id="d4d8e-851">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-851">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-852">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-852">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="d4d8e-853">5,297.69</span></span></td>
<td><span data-ttu-id="d4d8e-854">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-855">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-855">CC004</span></span></td>
<td><span data-ttu-id="d4d8e-856">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="d4d8e-856">Packaging</span></span></td>
<td><span data-ttu-id="d4d8e-857">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-857">10001</span></span></td>
<td><span data-ttu-id="d4d8e-858">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-858">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-859">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-859">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="d4d8e-860">2,852.60</span></span></td>
<td><span data-ttu-id="d4d8e-861">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-862">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-862">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-863">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-863">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-864">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-864">10001</span></span></td>
<td><span data-ttu-id="d4d8e-865">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-865">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-866">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-866">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="d4d8e-867">-713.75</span></span></td>
<td><span data-ttu-id="d4d8e-868">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-869">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-869">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-870">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-870">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-871">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-871">10001</span></span></td>
<td><span data-ttu-id="d4d8e-872">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-872">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-873">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-873">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-874">535.31</span><span class="sxs-lookup"><span data-stu-id="d4d8e-874">535.31</span></span></td>
<td><span data-ttu-id="d4d8e-875">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-876">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-876">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-877">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-877">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-878">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-878">10001</span></span></td>
<td><span data-ttu-id="d4d8e-879">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-879">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-880">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-880">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-881">178.44</span><span class="sxs-lookup"><span data-stu-id="d4d8e-881">178.44</span></span></td>
<td><span data-ttu-id="d4d8e-882">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-883">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-883">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-884">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-884">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-885">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-885">10001</span></span></td>
<td><span data-ttu-id="d4d8e-886">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-886">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-887">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-887">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="d4d8e-888">-5,982.83</span></span></td>
<td><span data-ttu-id="d4d8e-889">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-890">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-890">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-891">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-891">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-892">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-892">10001</span></span></td>
<td><span data-ttu-id="d4d8e-893">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-893">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-894">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-894">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="d4d8e-895">4,487.12</span></span></td>
<td><span data-ttu-id="d4d8e-896">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-897">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-897">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-898">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-898">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-899">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-899">10001</span></span></td>
<td><span data-ttu-id="d4d8e-900">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-900">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-901">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-901">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="d4d8e-902">1,495.71</span></span></td>
<td><span data-ttu-id="d4d8e-903">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-904">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-904">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-905">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-905">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-906">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-906">10001</span></span></td>
<td><span data-ttu-id="d4d8e-907">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-907">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-908">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-908">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="d4d8e-909">-286.25</span></span></td>
<td><span data-ttu-id="d4d8e-910">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-911">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-911">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-912">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-912">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-913">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-913">10001</span></span></td>
<td><span data-ttu-id="d4d8e-914">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-914">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-915">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-915">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-916">241.05</span><span class="sxs-lookup"><span data-stu-id="d4d8e-916">241.05</span></span></td>
<td><span data-ttu-id="d4d8e-917">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-918">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-918">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-919">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-919">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-920">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-920">10001</span></span></td>
<td><span data-ttu-id="d4d8e-921">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-921">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-922">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-922">Fixed cost</span></span></td>
<td><span data-ttu-id="d4d8e-923">45.20</span><span class="sxs-lookup"><span data-stu-id="d4d8e-923">45.20</span></span></td>
<td><span data-ttu-id="d4d8e-924">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-925">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-925">CC003</span></span></td>
<td><span data-ttu-id="d4d8e-926">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-926">Assembly</span></span></td>
<td><span data-ttu-id="d4d8e-927">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-927">10001</span></span></td>
<td><span data-ttu-id="d4d8e-928">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-928">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-929">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-929">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="d4d8e-930">-2,977.17</span></span></td>
<td><span data-ttu-id="d4d8e-931">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-932">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-932">Prod 1</span></span></td>
<td><span data-ttu-id="d4d8e-933">1 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-933">Product 1</span></span></td>
<td><span data-ttu-id="d4d8e-934">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-934">10001</span></span></td>
<td><span data-ttu-id="d4d8e-935">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-935">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-936">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-936">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="d4d8e-937">2,507.09</span></span></td>
<td><span data-ttu-id="d4d8e-938">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4d8e-939">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-939">Prod 2</span></span></td>
<td><span data-ttu-id="d4d8e-940">2 produktas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-940">Product 2</span></span></td>
<td><span data-ttu-id="d4d8e-941">10001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-941">10001</span></span></td>
<td><span data-ttu-id="d4d8e-942">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-942">Electricity</span></span></td>
<td><span data-ttu-id="d4d8e-943">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-943">Variable cost</span></span></td>
<td><span data-ttu-id="d4d8e-944">470.08</span><span class="sxs-lookup"><span data-stu-id="d4d8e-944">470.08</span></span></td>
<td><span data-ttu-id="d4d8e-945">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="d4d8e-946">Išvada</span><span class="sxs-lookup"><span data-stu-id="d4d8e-946">Conclusion</span></span>
<span data-ttu-id="d4d8e-947">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="d4d8e-948">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="d4d8e-949">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="d4d8e-950">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="d4d8e-951">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="d4d8e-952">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="d4d8e-953">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="d4d8e-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d4d8e-954">CC099</span><span class="sxs-lookup"><span data-stu-id="d4d8e-954">CC099</span></span></th>
<th><span data-ttu-id="d4d8e-955">CC001</span><span class="sxs-lookup"><span data-stu-id="d4d8e-955">CC001</span></span></th>
<th><span data-ttu-id="d4d8e-956">CC002</span><span class="sxs-lookup"><span data-stu-id="d4d8e-956">CC002</span></span></th>
<th><span data-ttu-id="d4d8e-957">CC003</span><span class="sxs-lookup"><span data-stu-id="d4d8e-957">CC003</span></span></th>
<th><span data-ttu-id="d4d8e-958">CC004</span><span class="sxs-lookup"><span data-stu-id="d4d8e-958">CC004</span></span></th>
<th><span data-ttu-id="d4d8e-959">1 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-959">Proj 1</span></span></th>
<th><span data-ttu-id="d4d8e-960">2 projektas</span><span class="sxs-lookup"><span data-stu-id="d4d8e-960">Proj 2</span></span></th>
<th><span data-ttu-id="d4d8e-961">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-961">Prod 1</span></span></th>
<th><span data-ttu-id="d4d8e-962">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="d4d8e-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="d4d8e-963">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="d4d8e-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="d4d8e-973">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="d4d8e-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-974">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="d4d8e-975">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-976">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-977">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-978">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-979">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-980">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-981">776.36</span><span class="sxs-lookup"><span data-stu-id="d4d8e-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-982">223.64</span><span class="sxs-lookup"><span data-stu-id="d4d8e-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="d4d8e-984">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="d4d8e-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-985">000</span><span class="sxs-lookup"><span data-stu-id="d4d8e-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-986">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-987">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-988">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-989">0,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-990">30,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-991">10,00</span><span class="sxs-lookup"><span data-stu-id="d4d8e-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="d4d8e-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="d4d8e-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="d4d8e-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="d4d8e-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d4d8e-995">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="d4d8e-996">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="d4d8e-997">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="d4d8e-998">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="d4d8e-999">Išsamesnės informacijos žr. temoje Išlaidų sumavimo strategija.</span><span class="sxs-lookup"><span data-stu-id="d4d8e-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="d4d8e-1000">(Atkreipkite dėmesį, kad ši tema nėra, bet bus greitai baigta.)</span><span class="sxs-lookup"><span data-stu-id="d4d8e-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




