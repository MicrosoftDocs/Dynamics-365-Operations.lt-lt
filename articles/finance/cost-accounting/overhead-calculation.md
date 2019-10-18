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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179045"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4afd6-103">Pridėtinių išlaidų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4afd6-104">Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.</span><span class="sxs-lookup"><span data-stu-id="4afd6-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4afd6-105">Termino aprašas</span><span class="sxs-lookup"><span data-stu-id="4afd6-105">Term definition</span></span>
---------------

<span data-ttu-id="4afd6-106">Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai.</span><span class="sxs-lookup"><span data-stu-id="4afd6-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4afd6-107">Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas.</span><span class="sxs-lookup"><span data-stu-id="4afd6-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4afd6-108">Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.</span><span class="sxs-lookup"><span data-stu-id="4afd6-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4afd6-109">Nuoma</span><span class="sxs-lookup"><span data-stu-id="4afd6-109">Rent</span></span>
-   <span data-ttu-id="4afd6-110">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-110">Electricity</span></span>
-   <span data-ttu-id="4afd6-111">Administravimo atlyginimai</span><span class="sxs-lookup"><span data-stu-id="4afd6-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4afd6-112">Pridėtinių išlaidų skaičiavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="4afd6-112">Overhead calculation overview</span></span>
<span data-ttu-id="4afd6-113">Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka.</span><span class="sxs-lookup"><span data-stu-id="4afd6-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4afd6-114">Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4afd6-115">Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="4afd6-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4afd6-116">Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data.</span><span class="sxs-lookup"><span data-stu-id="4afd6-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4afd6-117">Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="4afd6-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4afd6-118">Unikalų versijos ID sudaro toliau nurodyti elementai.</span><span class="sxs-lookup"><span data-stu-id="4afd6-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4afd6-119">Versijos tipas</span><span class="sxs-lookup"><span data-stu-id="4afd6-119">Version type</span></span>
-   <span data-ttu-id="4afd6-120">Data ir laikas</span><span class="sxs-lookup"><span data-stu-id="4afd6-120">Date and time</span></span>
-   <span data-ttu-id="4afd6-121">Savikainos apskaitos didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="4afd6-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4afd6-122">Finansiniai metai</span><span class="sxs-lookup"><span data-stu-id="4afd6-122">Fiscal year</span></span>
-   <span data-ttu-id="4afd6-123">Ataskaitinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-123">Fiscal period</span></span>

<span data-ttu-id="4afd6-124">Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos.</span><span class="sxs-lookup"><span data-stu-id="4afd6-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4afd6-125">Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją.</span><span class="sxs-lookup"><span data-stu-id="4afd6-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4afd6-126">Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="4afd6-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4afd6-127">Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais.</span><span class="sxs-lookup"><span data-stu-id="4afd6-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4afd6-128">Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys.</span><span class="sxs-lookup"><span data-stu-id="4afd6-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4afd6-129">Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga.</span><span class="sxs-lookup"><span data-stu-id="4afd6-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4afd6-130">Todėl visada galite atsekti visą informaciją.</span><span class="sxs-lookup"><span data-stu-id="4afd6-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4afd6-131">[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4afd6-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4afd6-132">Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="4afd6-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4afd6-133">Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="4afd6-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4afd6-134">Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos.</span><span class="sxs-lookup"><span data-stu-id="4afd6-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4afd6-135">Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus.</span><span class="sxs-lookup"><span data-stu-id="4afd6-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4afd6-136">Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="4afd6-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4afd6-137">DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="4afd6-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-138">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-139">Išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-140">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="4afd6-140">Main account</span></span></th>
<th><span data-ttu-id="4afd6-141">Suma apskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="4afd6-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-142">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4afd6-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-143">CC099</span></span></td>
<td><span data-ttu-id="4afd6-144">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-144">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-145">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-145">10001</span></span></td>
<td><span data-ttu-id="4afd6-146">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-146">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4afd6-148">1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4afd6-149">Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**.</span><span class="sxs-lookup"><span data-stu-id="4afd6-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4afd6-150">Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.</span><span class="sxs-lookup"><span data-stu-id="4afd6-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4afd6-151">Išlaidų veikimo būdo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="4afd6-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4afd6-152">Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="4afd6-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4afd6-153">Sąskaitos už elektrą dažnai atitinka šį apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4afd6-154">Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4afd6-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4afd6-155">Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="4afd6-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4afd6-156">Fiksuota suma 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4afd6-157">0 &lt;= 1 000,00 = fiksuota</span><span class="sxs-lookup"><span data-stu-id="4afd6-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4afd6-158">1 000,01 &lt; N = kintamasis</span><span class="sxs-lookup"><span data-stu-id="4afd6-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4afd6-159">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-160">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-160">Journal</span></span></th>
<th><span data-ttu-id="4afd6-161">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="4afd6-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4afd6-162">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4afd6-163">Versija</span><span class="sxs-lookup"><span data-stu-id="4afd6-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-164">00001</span><span class="sxs-lookup"><span data-stu-id="4afd6-164">00001</span></span></td>
<td><span data-ttu-id="4afd6-165">Savikainos veikimo būdo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4afd6-166">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="4afd6-166">Fiscal</span></span></td>
<td><span data-ttu-id="4afd6-167">2017</span><span class="sxs-lookup"><span data-stu-id="4afd6-167">2017</span></span></td>
<td><span data-ttu-id="4afd6-168">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-168">Period 1</span></span></td>
<td><span data-ttu-id="4afd6-169">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4afd6-170">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="4afd6-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-171">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-172">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-173">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-173">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-174">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-175">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-176">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4afd6-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-177">CC099</span></span></td>
<td><span data-ttu-id="4afd6-178">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-178">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-179">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-179">10001</span></span></td>
<td><span data-ttu-id="4afd6-180">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-180">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-181">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="4afd6-181">Unclassified</span></span></td>
<td><span data-ttu-id="4afd6-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4afd6-183">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="4afd6-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-184">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-185">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-185">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-186">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-187">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-187">Amount</span></span></th>
<th><span data-ttu-id="4afd6-188">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-189">CC099</span></span></td>
<td><span data-ttu-id="4afd6-190">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-190">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-191">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-191">10001</span></span></td>
<td><span data-ttu-id="4afd6-192">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-192">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-193">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="4afd6-193">Unclassified</span></span></td>
<td><span data-ttu-id="4afd6-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-194">10,000.00</span></span></td>
<td><span data-ttu-id="4afd6-195">2017 m. sausio 3 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-196">CC099</span></span></td>
<td><span data-ttu-id="4afd6-197">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-197">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-198">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-198">10001</span></span></td>
<td><span data-ttu-id="4afd6-199">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-199">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-200">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="4afd6-200">Unclassified</span></span></td>
<td><span data-ttu-id="4afd6-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4afd6-202">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-203">CC099</span></span></td>
<td><span data-ttu-id="4afd6-204">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-204">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-205">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-205">10001</span></span></td>
<td><span data-ttu-id="4afd6-206">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-206">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-207">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-208">1000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-208">1,000.00</span></span></td>
<td><span data-ttu-id="4afd6-209">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-210">CC099</span></span></td>
<td><span data-ttu-id="4afd6-211">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-211">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-212">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-212">10001</span></span></td>
<td><span data-ttu-id="4afd6-213">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-213">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-214">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-214">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-215">9,000.00</span></span></td>
<td><span data-ttu-id="4afd6-216">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-217">Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="4afd6-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4afd6-218">2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4afd6-219">Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4afd6-220">Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.</span><span class="sxs-lookup"><span data-stu-id="4afd6-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4afd6-221">Išlaidų paskirstymo taisyklės nustatymas</span><span class="sxs-lookup"><span data-stu-id="4afd6-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4afd6-222">Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="4afd6-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4afd6-223">Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas.</span><span class="sxs-lookup"><span data-stu-id="4afd6-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4afd6-224">Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu.</span><span class="sxs-lookup"><span data-stu-id="4afd6-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4afd6-225">Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh).</span><span class="sxs-lookup"><span data-stu-id="4afd6-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4afd6-226">Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="4afd6-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4afd6-227">Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.</span><span class="sxs-lookup"><span data-stu-id="4afd6-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-228">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-228">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4afd6-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-230">CC001</span></span></td>
<td><span data-ttu-id="4afd6-231">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-231">HR</span></span></td>
<td><span data-ttu-id="4afd6-232">1000</span><span class="sxs-lookup"><span data-stu-id="4afd6-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-233">CC002</span></span></td>
<td><span data-ttu-id="4afd6-234">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-234">Finance</span></span></td>
<td><span data-ttu-id="4afd6-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4afd6-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-236">CC003</span></span></td>
<td><span data-ttu-id="4afd6-237">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-237">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-238">0</span><span class="sxs-lookup"><span data-stu-id="4afd6-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-239">Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-240">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-240">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-241">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-241">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-242">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-243">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-244">CC001</span></span></td>
<td><span data-ttu-id="4afd6-245">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-245">HR</span></span></td>
<td><span data-ttu-id="4afd6-246">1000</span><span class="sxs-lookup"><span data-stu-id="4afd6-246">1,000</span></span></td>
<td><span data-ttu-id="4afd6-247">(1 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4afd6-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-249">CC002</span></span></td>
<td><span data-ttu-id="4afd6-250">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-250">Finance</span></span></td>
<td><span data-ttu-id="4afd6-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4afd6-251">6,000</span></span></td>
<td><span data-ttu-id="4afd6-252">(6 000 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4afd6-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4afd6-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-254">CC003</span></span></td>
<td><span data-ttu-id="4afd6-255">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-255">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-256">0</span><span class="sxs-lookup"><span data-stu-id="4afd6-256">0</span></span></td>
<td><span data-ttu-id="4afd6-257">(0 ÷ 7 000) × 9 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4afd6-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-259">Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4afd6-260">Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-261">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-261">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-262">Formulė</span><span class="sxs-lookup"><span data-stu-id="4afd6-262">Formula</span></span></th>
<th><span data-ttu-id="4afd6-263">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-263">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-264">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-265">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-266">CC001</span></span></td>
<td><span data-ttu-id="4afd6-267">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-267">HR</span></span></td>
<td><span data-ttu-id="4afd6-268">(1 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4afd6-269">1</span><span class="sxs-lookup"><span data-stu-id="4afd6-269">1</span></span></td>
<td><span data-ttu-id="4afd6-270">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4afd6-271">500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-272">CC002</span></span></td>
<td><span data-ttu-id="4afd6-273">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-273">Finance</span></span></td>
<td><span data-ttu-id="4afd6-274">(6 000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4afd6-275">1</span><span class="sxs-lookup"><span data-stu-id="4afd6-275">1</span></span></td>
<td><span data-ttu-id="4afd6-276">(1 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4afd6-277">500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-278">CC003</span></span></td>
<td><span data-ttu-id="4afd6-279">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-279">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4afd6-281">0</span><span class="sxs-lookup"><span data-stu-id="4afd6-281">0</span></span></td>
<td><span data-ttu-id="4afd6-282">(0 ÷ 2) × 1 000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4afd6-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4afd6-284">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-285">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-285">Journal</span></span></th>
<th><span data-ttu-id="4afd6-286">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="4afd6-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4afd6-287">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4afd6-288">Versija</span><span class="sxs-lookup"><span data-stu-id="4afd6-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-289">00002</span><span class="sxs-lookup"><span data-stu-id="4afd6-289">00002</span></span></td>
<td><span data-ttu-id="4afd6-290">Išlaidų paskirstymo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4afd6-291">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="4afd6-291">Fiscal</span></span></td>
<td><span data-ttu-id="4afd6-292">2017</span><span class="sxs-lookup"><span data-stu-id="4afd6-292">2017</span></span></td>
<td><span data-ttu-id="4afd6-293">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-293">Period 1</span></span></td>
<td><span data-ttu-id="4afd6-294">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4afd6-295">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="4afd6-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-296">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-297">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-298">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-298">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-299">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-300">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-301">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-302">CC099</span></span></td>
<td><span data-ttu-id="4afd6-303">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-303">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-304">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-304">10001</span></span></td>
<td><span data-ttu-id="4afd6-305">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-305">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-306">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-307">1000,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-308">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-309">CC099</span></span></td>
<td><span data-ttu-id="4afd6-310">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-310">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-311">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-311">10001</span></span></td>
<td><span data-ttu-id="4afd6-312">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-312">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-313">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-313">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4afd6-315">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="4afd6-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-316">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-317">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-317">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-318">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-319">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-319">Amount</span></span></th>
<th><span data-ttu-id="4afd6-320">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-321">CC099</span></span></td>
<td><span data-ttu-id="4afd6-322">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-322">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-323">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-323">10001</span></span></td>
<td><span data-ttu-id="4afd6-324">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-324">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-325">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4afd6-327">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-328">CC001</span></span></td>
<td><span data-ttu-id="4afd6-329">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-329">HR</span></span></td>
<td><span data-ttu-id="4afd6-330">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-330">10001</span></span></td>
<td><span data-ttu-id="4afd6-331">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-331">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-332">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-333">500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-333">500.00</span></span></td>
<td><span data-ttu-id="4afd6-334">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-335">CC002</span></span></td>
<td><span data-ttu-id="4afd6-336">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-336">Finance</span></span></td>
<td><span data-ttu-id="4afd6-337">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-337">10001</span></span></td>
<td><span data-ttu-id="4afd6-338">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-338">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-339">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-340">500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-340">500.00</span></span></td>
<td><span data-ttu-id="4afd6-341">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-342">CC099</span></span></td>
<td><span data-ttu-id="4afd6-343">Numatytasis išlaidų centras</span><span class="sxs-lookup"><span data-stu-id="4afd6-343">Default cost center</span></span></td>
<td><span data-ttu-id="4afd6-344">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-344">10001</span></span></td>
<td><span data-ttu-id="4afd6-345">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-345">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-346">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-346">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4afd6-348">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-349">CC001</span></span></td>
<td><span data-ttu-id="4afd6-350">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-350">HR</span></span></td>
<td><span data-ttu-id="4afd6-351">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-351">10001</span></span></td>
<td><span data-ttu-id="4afd6-352">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-352">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-353">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-353">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-354">1,285.71</span></span></td>
<td><span data-ttu-id="4afd6-355">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-356">CC002</span></span></td>
<td><span data-ttu-id="4afd6-357">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-357">Finance</span></span></td>
<td><span data-ttu-id="4afd6-358">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-358">10001</span></span></td>
<td><span data-ttu-id="4afd6-359">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-359">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-360">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-360">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4afd6-361">7,714.29</span></span></td>
<td><span data-ttu-id="4afd6-362">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-363">Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)</span><span class="sxs-lookup"><span data-stu-id="4afd6-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4afd6-364">3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas</span><span class="sxs-lookup"><span data-stu-id="4afd6-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4afd6-365">Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4afd6-366">Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo.</span><span class="sxs-lookup"><span data-stu-id="4afd6-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4afd6-367">Pridėtinių išlaidų tarifo nustatymas</span><span class="sxs-lookup"><span data-stu-id="4afd6-367">Define the overhead rate</span></span>

<span data-ttu-id="4afd6-368">Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4afd6-369">Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-370">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-370">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-371">Valandos</span><span class="sxs-lookup"><span data-stu-id="4afd6-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-372">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-372">Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-373">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-373">Project 1</span></span></td>
<td><span data-ttu-id="4afd6-374">3</span><span class="sxs-lookup"><span data-stu-id="4afd6-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-375">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-375">Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-376">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-376">Project 2</span></span></td>
<td><span data-ttu-id="4afd6-377">1</span><span class="sxs-lookup"><span data-stu-id="4afd6-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-378">Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="4afd6-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-379">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-379">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-380">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-380">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-381">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-382">Vienetai</span><span class="sxs-lookup"><span data-stu-id="4afd6-382">Units</span></span></th>
<th><span data-ttu-id="4afd6-383">Tarifas</span><span class="sxs-lookup"><span data-stu-id="4afd6-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-384">CC001</span></span></td>
<td><span data-ttu-id="4afd6-385">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-385">HR</span></span></td>
<td><span data-ttu-id="4afd6-386">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-386">10001</span></span></td>
<td><span data-ttu-id="4afd6-387">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-387">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-388">1</span><span class="sxs-lookup"><span data-stu-id="4afd6-388">1</span></span></td>
<td><span data-ttu-id="4afd6-389">10</span><span class="sxs-lookup"><span data-stu-id="4afd6-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-390">Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-391">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-391">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-392">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-392">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-393">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-393">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-394">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-395">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-396">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-396">Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-397">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-397">Project 1</span></span></td>
<td><span data-ttu-id="4afd6-398">3</span><span class="sxs-lookup"><span data-stu-id="4afd6-398">3</span></span></td>
<td><span data-ttu-id="4afd6-399">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-399">10001</span></span></td>
<td><span data-ttu-id="4afd6-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4afd6-401">30,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-402">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-402">Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-403">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-403">Project 2</span></span></td>
<td><span data-ttu-id="4afd6-404">1</span><span class="sxs-lookup"><span data-stu-id="4afd6-404">1</span></span></td>
<td><span data-ttu-id="4afd6-405">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-405">10001</span></span></td>
<td><span data-ttu-id="4afd6-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4afd6-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4afd6-408">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-409">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-409">Journal</span></span></th>
<th><span data-ttu-id="4afd6-410">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="4afd6-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4afd6-411">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4afd6-412">Versija</span><span class="sxs-lookup"><span data-stu-id="4afd6-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-413">00003</span><span class="sxs-lookup"><span data-stu-id="4afd6-413">00003</span></span></td>
<td><span data-ttu-id="4afd6-414">Pridėtinių išlaidų tarifo skaičiavimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4afd6-415">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="4afd6-415">Fiscal</span></span></td>
<td><span data-ttu-id="4afd6-416">2017</span><span class="sxs-lookup"><span data-stu-id="4afd6-416">2017</span></span></td>
<td><span data-ttu-id="4afd6-417">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-417">Period 1</span></span></td>
<td><span data-ttu-id="4afd6-418">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4afd6-419">Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="4afd6-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-420">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-421">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-421">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-422">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-423">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-424">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-424">Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-425">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-427">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-428">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-428">Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-429">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-430">1,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4afd6-431">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="4afd6-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-432">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-433">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-433">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-434">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-435">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-435">Amount</span></span></th>
<th><span data-ttu-id="4afd6-436">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4afd6-437">CC0001</span></span></td>
<td><span data-ttu-id="4afd6-438">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-438">HR</span></span></td>
<td><span data-ttu-id="4afd6-439">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-439">10001</span></span></td>
<td><span data-ttu-id="4afd6-440">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-440">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-441">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-441">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-442">-30.00</span></span></td>
<td><span data-ttu-id="4afd6-443">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-444">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-444">Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-445">1 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4afd6-446">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-446">10001</span></span></td>
<td><span data-ttu-id="4afd6-447">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-447">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-448">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-448">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-449">30,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-449">30.00</span></span></td>
<td><span data-ttu-id="4afd6-450">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-451">CC001</span></span></td>
<td><span data-ttu-id="4afd6-452">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-452">HR</span></span></td>
<td><span data-ttu-id="4afd6-453">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-453">10001</span></span></td>
<td><span data-ttu-id="4afd6-454">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-454">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-455">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-455">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-456">-10.00</span></span></td>
<td><span data-ttu-id="4afd6-457">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-458">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-458">Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-459">2 vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4afd6-460">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-460">10001</span></span></td>
<td><span data-ttu-id="4afd6-461">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-461">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-462">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-462">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-463">10,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-463">10.00</span></span></td>
<td><span data-ttu-id="4afd6-464">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-465">Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..</span><span class="sxs-lookup"><span data-stu-id="4afd6-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4afd6-466">4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4afd6-467">Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4afd6-468">„Finance” palaiko abipusio paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4afd6-469">Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos.</span><span class="sxs-lookup"><span data-stu-id="4afd6-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4afd6-470">Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4afd6-471">Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4afd6-472">Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams.</span><span class="sxs-lookup"><span data-stu-id="4afd6-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4afd6-473">Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso.</span><span class="sxs-lookup"><span data-stu-id="4afd6-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4afd6-474">[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4afd6-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4afd6-475">Išlaidų paskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="4afd6-475">Define the cost allocation</span></span>

<span data-ttu-id="4afd6-476">Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4afd6-477">Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4afd6-478">Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-479">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-479">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-480">Personalo paslaugos</span><span class="sxs-lookup"><span data-stu-id="4afd6-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-481">CC002</span></span></td>
<td><span data-ttu-id="4afd6-482">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-482">Finance</span></span></td>
<td><span data-ttu-id="4afd6-483">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-484">CC003</span></span></td>
<td><span data-ttu-id="4afd6-485">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-485">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-486">55</span><span class="sxs-lookup"><span data-stu-id="4afd6-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-487">CC004</span></span></td>
<td><span data-ttu-id="4afd6-488">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-488">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-489">10</span><span class="sxs-lookup"><span data-stu-id="4afd6-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-490">Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4afd6-491">Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-492">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-492">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-493">Finansų padalinio paslaugos</span><span class="sxs-lookup"><span data-stu-id="4afd6-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-494">CC003</span></span></td>
<td><span data-ttu-id="4afd6-495">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-495">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-496">65</span><span class="sxs-lookup"><span data-stu-id="4afd6-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-497">CC004</span></span></td>
<td><span data-ttu-id="4afd6-498">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-498">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-499">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-500">Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4afd6-501">Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-502">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-502">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-503">Surinkimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="4afd6-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-504">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-504">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-505">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-505">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-506">60</span><span class="sxs-lookup"><span data-stu-id="4afd6-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-507">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-507">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-508">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-508">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-509">20</span><span class="sxs-lookup"><span data-stu-id="4afd6-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-510">Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4afd6-511">Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4afd6-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-512">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-512">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-513">Pakavimo padalinio paslaugos (valandomis)</span><span class="sxs-lookup"><span data-stu-id="4afd6-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-514">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-514">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-515">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-515">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-516">80</span><span class="sxs-lookup"><span data-stu-id="4afd6-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-517">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-517">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-518">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-518">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-519">15</span><span class="sxs-lookup"><span data-stu-id="4afd6-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4afd6-520">Statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų.</span><span class="sxs-lookup"><span data-stu-id="4afd6-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4afd6-521">Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="4afd6-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4afd6-522">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-523">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-523">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-524">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-524">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-525">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-526">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-526">Amount</span></span></th>
<th><span data-ttu-id="4afd6-527">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-528">CC002</span></span></td>
<td><span data-ttu-id="4afd6-529">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-529">Finance</span></span></td>
<td><span data-ttu-id="4afd6-530">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-530">35</span></span></td>
<td><span data-ttu-id="4afd6-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4afd6-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-532">175.00</span></span></td>
<td><span data-ttu-id="4afd6-533">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-534">CC003</span></span></td>
<td><span data-ttu-id="4afd6-535">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-535">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-536">55</span><span class="sxs-lookup"><span data-stu-id="4afd6-536">55</span></span></td>
<td><span data-ttu-id="4afd6-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4afd6-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-538">275.00</span></span></td>
<td><span data-ttu-id="4afd6-539">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-540">CC004</span></span></td>
<td><span data-ttu-id="4afd6-541">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-541">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-542">10</span><span class="sxs-lookup"><span data-stu-id="4afd6-542">10</span></span></td>
<td><span data-ttu-id="4afd6-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4afd6-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-544">50.00</span></span></td>
<td><span data-ttu-id="4afd6-545">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-546">CC002</span></span></td>
<td><span data-ttu-id="4afd6-547">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-547">Finance</span></span></td>
<td><span data-ttu-id="4afd6-548">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-548">35</span></span></td>
<td><span data-ttu-id="4afd6-549">(35 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4afd6-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4afd6-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-550">436.00</span></span></td>
<td><span data-ttu-id="4afd6-551">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-552">CC003</span></span></td>
<td><span data-ttu-id="4afd6-553">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-553">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-554">55</span><span class="sxs-lookup"><span data-stu-id="4afd6-554">55</span></span></td>
<td><span data-ttu-id="4afd6-555">(55 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4afd6-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4afd6-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4afd6-556">685.14</span></span></td>
<td><span data-ttu-id="4afd6-557">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-558">CC004</span></span></td>
<td><span data-ttu-id="4afd6-559">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-559">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-560">10</span><span class="sxs-lookup"><span data-stu-id="4afd6-560">10</span></span></td>
<td><span data-ttu-id="4afd6-561">(10 ÷ 100) × 1 245,71</span><span class="sxs-lookup"><span data-stu-id="4afd6-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4afd6-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4afd6-562">124.57</span></span></td>
<td><span data-ttu-id="4afd6-563">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-564">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-565">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-565">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-566">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-566">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-567">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-568">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-568">Amount</span></span></th>
<th><span data-ttu-id="4afd6-569">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-570">CC003</span></span></td>
<td><span data-ttu-id="4afd6-571">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-571">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-572">65</span><span class="sxs-lookup"><span data-stu-id="4afd6-572">65</span></span></td>
<td><span data-ttu-id="4afd6-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4afd6-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4afd6-574">438.75</span></span></td>
<td><span data-ttu-id="4afd6-575">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-576">CC004</span></span></td>
<td><span data-ttu-id="4afd6-577">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-577">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-578">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-578">35</span></span></td>
<td><span data-ttu-id="4afd6-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4afd6-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4afd6-580">236.25</span></span></td>
<td><span data-ttu-id="4afd6-581">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-582">CC003</span></span></td>
<td><span data-ttu-id="4afd6-583">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-583">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-584">65</span><span class="sxs-lookup"><span data-stu-id="4afd6-584">65</span></span></td>
<td><span data-ttu-id="4afd6-585">(65 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4afd6-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4afd6-586">5,297.69</span></span></td>
<td><span data-ttu-id="4afd6-587">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-588">CC004</span></span></td>
<td><span data-ttu-id="4afd6-589">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-589">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-590">35</span><span class="sxs-lookup"><span data-stu-id="4afd6-590">35</span></span></td>
<td><span data-ttu-id="4afd6-591">(35 ÷ 100) × (7 714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4afd6-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4afd6-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4afd6-592">2,852.60</span></span></td>
<td><span data-ttu-id="4afd6-593">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-594">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-595">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-595">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-596">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-596">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-597">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-598">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-598">Amount</span></span></th>
<th><span data-ttu-id="4afd6-599">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-600">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-600">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-601">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-601">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-602">60</span><span class="sxs-lookup"><span data-stu-id="4afd6-602">60</span></span></td>
<td><span data-ttu-id="4afd6-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4afd6-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4afd6-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4afd6-604">535.31</span></span></td>
<td><span data-ttu-id="4afd6-605">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-606">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-606">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-607">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-607">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-608">20</span><span class="sxs-lookup"><span data-stu-id="4afd6-608">20</span></span></td>
<td><span data-ttu-id="4afd6-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4afd6-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4afd6-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4afd6-610">178.44</span></span></td>
<td><span data-ttu-id="4afd6-611">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-612">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-612">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-613">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-613">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-614">60</span><span class="sxs-lookup"><span data-stu-id="4afd6-614">60</span></span></td>
<td><span data-ttu-id="4afd6-615">(60 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4afd6-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4afd6-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4afd6-616">4,487.12</span></span></td>
<td><span data-ttu-id="4afd6-617">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-618">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-618">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-619">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-619">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-620">20</span><span class="sxs-lookup"><span data-stu-id="4afd6-620">20</span></span></td>
<td><span data-ttu-id="4afd6-621">(20 ÷ 80) × (5 297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4afd6-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4afd6-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-622">1,495.71</span></span></td>
<td><span data-ttu-id="4afd6-623">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4afd6-624">Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-625">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-625">Cost object</span></span></th>
<th><span data-ttu-id="4afd6-626">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4afd6-626">Magnitude</span></span></th>
<th><span data-ttu-id="4afd6-627">Paskirstymo koeficientas</span><span class="sxs-lookup"><span data-stu-id="4afd6-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4afd6-628">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-628">Amount</span></span></th>
<th><span data-ttu-id="4afd6-629">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-630">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-630">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-631">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-631">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-632">80</span><span class="sxs-lookup"><span data-stu-id="4afd6-632">80</span></span></td>
<td><span data-ttu-id="4afd6-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4afd6-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4afd6-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4afd6-634">241.05</span></span></td>
<td><span data-ttu-id="4afd6-635">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-636">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-636">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-637">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-637">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-638">15</span><span class="sxs-lookup"><span data-stu-id="4afd6-638">15</span></span></td>
<td><span data-ttu-id="4afd6-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4afd6-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4afd6-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4afd6-640">45.20</span></span></td>
<td><span data-ttu-id="4afd6-641">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-642">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-642">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-643">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-643">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-644">80</span><span class="sxs-lookup"><span data-stu-id="4afd6-644">80</span></span></td>
<td><span data-ttu-id="4afd6-645">(80 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4afd6-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4afd6-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4afd6-646">2,507.09</span></span></td>
<td><span data-ttu-id="4afd6-647">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-648">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-648">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-649">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-649">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-650">15</span><span class="sxs-lookup"><span data-stu-id="4afd6-650">15</span></span></td>
<td><span data-ttu-id="4afd6-651">(15 ÷ 95) × (2 852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4afd6-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4afd6-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4afd6-652">470.08</span></span></td>
<td><span data-ttu-id="4afd6-653">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4afd6-654">Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)</span><span class="sxs-lookup"><span data-stu-id="4afd6-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-655">Žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-655">Journal</span></span></th>
<th><span data-ttu-id="4afd6-656">Žurnalo tipas</span><span class="sxs-lookup"><span data-stu-id="4afd6-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4afd6-657">Ataskaitinis kalendorinis laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4afd6-658">Versija</span><span class="sxs-lookup"><span data-stu-id="4afd6-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-659">00004</span><span class="sxs-lookup"><span data-stu-id="4afd6-659">00004</span></span></td>
<td><span data-ttu-id="4afd6-660">Savikainos paskirstymo žurnalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4afd6-661">Finansiniai</span><span class="sxs-lookup"><span data-stu-id="4afd6-661">Fiscal</span></span></td>
<td><span data-ttu-id="4afd6-662">2017</span><span class="sxs-lookup"><span data-stu-id="4afd6-662">2017</span></span></td>
<td><span data-ttu-id="4afd6-663">1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-663">Period 1</span></span></td>
<td><span data-ttu-id="4afd6-664">Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</span><span class="sxs-lookup"><span data-stu-id="4afd6-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4afd6-665">Žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="4afd6-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4afd6-666">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-667">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-668">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-668">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-669">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-670">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-671">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-672">CC001</span></span></td>
<td><span data-ttu-id="4afd6-673">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-673">HR</span></span></td>
<td><span data-ttu-id="4afd6-674">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-674">10001</span></span></td>
<td><span data-ttu-id="4afd6-675">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-675">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-676">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-677">500,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-678">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-679">CC001</span></span></td>
<td><span data-ttu-id="4afd6-680">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-680">HR</span></span></td>
<td><span data-ttu-id="4afd6-681">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-681">10001</span></span></td>
<td><span data-ttu-id="4afd6-682">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-682">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-683">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-683">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-685">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-686">CC002</span></span></td>
<td><span data-ttu-id="4afd6-687">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-687">Finance</span></span></td>
<td><span data-ttu-id="4afd6-688">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-688">10001</span></span></td>
<td><span data-ttu-id="4afd6-689">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-689">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-690">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-692">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-693">CC002</span></span></td>
<td><span data-ttu-id="4afd6-694">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-694">Finance</span></span></td>
<td><span data-ttu-id="4afd6-695">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-695">10001</span></span></td>
<td><span data-ttu-id="4afd6-696">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-696">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-697">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-697">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4afd6-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-699">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-700">CC003</span></span></td>
<td><span data-ttu-id="4afd6-701">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-701">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-702">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-702">10001</span></span></td>
<td><span data-ttu-id="4afd6-703">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-703">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-704">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4afd6-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-706">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-707">CC003</span></span></td>
<td><span data-ttu-id="4afd6-708">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-708">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-709">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-709">10001</span></span></td>
<td><span data-ttu-id="4afd6-710">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-710">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-711">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-711">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4afd6-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-713">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-714">CC003</span></span></td>
<td><span data-ttu-id="4afd6-715">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-715">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-716">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-716">10001</span></span></td>
<td><span data-ttu-id="4afd6-717">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-717">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-718">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4afd6-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-720">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-721">CC003</span></span></td>
<td><span data-ttu-id="4afd6-722">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-722">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-723">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-723">10001</span></span></td>
<td><span data-ttu-id="4afd6-724">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-724">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-725">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-725">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4afd6-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-727">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-728">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-728">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-729">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-729">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-730">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-730">10001</span></span></td>
<td><span data-ttu-id="4afd6-731">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-731">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-732">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4afd6-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-734">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-735">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-735">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-736">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-736">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-737">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-737">10001</span></span></td>
<td><span data-ttu-id="4afd6-738">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-738">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-739">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-739">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4afd6-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-741">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-742">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-742">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-743">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-743">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-744">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-744">10001</span></span></td>
<td><span data-ttu-id="4afd6-745">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-745">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-746">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4afd6-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-748">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4afd6-749">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-749">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-750">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-750">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-751">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-751">10001</span></span></td>
<td><span data-ttu-id="4afd6-752">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-752">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-753">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-753">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4afd6-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4afd6-755">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="4afd6-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4afd6-756">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4afd6-757">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-757">Cost element</span></span></th>
<th><span data-ttu-id="4afd6-758">Savikainos veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="4afd6-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4afd6-759">Suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-759">Amount</span></span></th>
<th><span data-ttu-id="4afd6-760">Ataskaitinė data</span><span class="sxs-lookup"><span data-stu-id="4afd6-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4afd6-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-761">CC001</span></span></td>
<td><span data-ttu-id="4afd6-762">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-762">HR</span></span></td>
<td><span data-ttu-id="4afd6-763">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-763">10001</span></span></td>
<td><span data-ttu-id="4afd6-764">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-764">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-765">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-766">-500.00</span></span></td>
<td><span data-ttu-id="4afd6-767">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-768">CC002</span></span></td>
<td><span data-ttu-id="4afd6-769">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-769">Finance</span></span></td>
<td><span data-ttu-id="4afd6-770">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-770">10001</span></span></td>
<td><span data-ttu-id="4afd6-771">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-771">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-772">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-773">175.00</span></span></td>
<td><span data-ttu-id="4afd6-774">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-775">CC003</span></span></td>
<td><span data-ttu-id="4afd6-776">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-776">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-777">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-777">10001</span></span></td>
<td><span data-ttu-id="4afd6-778">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-778">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-779">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-780">275.00</span></span></td>
<td><span data-ttu-id="4afd6-781">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-782">CC004</span></span></td>
<td><span data-ttu-id="4afd6-783">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-783">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-784">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-784">10001</span></span></td>
<td><span data-ttu-id="4afd6-785">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-785">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-786">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-787">50,00</span></span></td>
<td><span data-ttu-id="4afd6-788">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-789">CC001</span></span></td>
<td><span data-ttu-id="4afd6-790">Personalas</span><span class="sxs-lookup"><span data-stu-id="4afd6-790">HR</span></span></td>
<td><span data-ttu-id="4afd6-791">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-791">10001</span></span></td>
<td><span data-ttu-id="4afd6-792">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-792">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-793">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-793">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4afd6-795">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-796">CC002</span></span></td>
<td><span data-ttu-id="4afd6-797">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-797">Finance</span></span></td>
<td><span data-ttu-id="4afd6-798">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-798">10001</span></span></td>
<td><span data-ttu-id="4afd6-799">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-799">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-800">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-800">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-801">436.00</span></span></td>
<td><span data-ttu-id="4afd6-802">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-803">CC003</span></span></td>
<td><span data-ttu-id="4afd6-804">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-804">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-805">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-805">10001</span></span></td>
<td><span data-ttu-id="4afd6-806">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-806">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-807">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-807">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4afd6-808">685.14</span></span></td>
<td><span data-ttu-id="4afd6-809">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-810">CC004</span></span></td>
<td><span data-ttu-id="4afd6-811">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-811">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-812">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-812">10001</span></span></td>
<td><span data-ttu-id="4afd6-813">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-813">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-814">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-814">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4afd6-815">124.57</span></span></td>
<td><span data-ttu-id="4afd6-816">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-817">CC002</span></span></td>
<td><span data-ttu-id="4afd6-818">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-818">Finance</span></span></td>
<td><span data-ttu-id="4afd6-819">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-819">10001</span></span></td>
<td><span data-ttu-id="4afd6-820">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-820">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-821">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="4afd6-822">-675.00</span></span></td>
<td><span data-ttu-id="4afd6-823">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-824">CC003</span></span></td>
<td><span data-ttu-id="4afd6-825">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-825">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-826">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-826">10001</span></span></td>
<td><span data-ttu-id="4afd6-827">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-827">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-828">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4afd6-829">438.75</span></span></td>
<td><span data-ttu-id="4afd6-830">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-831">CC004</span></span></td>
<td><span data-ttu-id="4afd6-832">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-832">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-833">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-833">10001</span></span></td>
<td><span data-ttu-id="4afd6-834">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-834">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-835">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4afd6-836">236.25</span></span></td>
<td><span data-ttu-id="4afd6-837">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-838">CC002</span></span></td>
<td><span data-ttu-id="4afd6-839">Finansai</span><span class="sxs-lookup"><span data-stu-id="4afd6-839">Finance</span></span></td>
<td><span data-ttu-id="4afd6-840">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-840">10001</span></span></td>
<td><span data-ttu-id="4afd6-841">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-841">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-842">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-842">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="4afd6-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4afd6-844">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-845">CC003</span></span></td>
<td><span data-ttu-id="4afd6-846">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-846">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-847">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-847">10001</span></span></td>
<td><span data-ttu-id="4afd6-848">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-848">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-849">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-849">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4afd6-850">5,297.69</span></span></td>
<td><span data-ttu-id="4afd6-851">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-852">CC004</span></span></td>
<td><span data-ttu-id="4afd6-853">Pakuotės</span><span class="sxs-lookup"><span data-stu-id="4afd6-853">Packaging</span></span></td>
<td><span data-ttu-id="4afd6-854">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-854">10001</span></span></td>
<td><span data-ttu-id="4afd6-855">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-855">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-856">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-856">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4afd6-857">2,852.60</span></span></td>
<td><span data-ttu-id="4afd6-858">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-859">CC003</span></span></td>
<td><span data-ttu-id="4afd6-860">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-860">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-861">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-861">10001</span></span></td>
<td><span data-ttu-id="4afd6-862">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-862">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-863">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4afd6-864">-713.75</span></span></td>
<td><span data-ttu-id="4afd6-865">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-866">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-866">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-867">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-867">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-868">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-868">10001</span></span></td>
<td><span data-ttu-id="4afd6-869">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-869">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-870">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4afd6-871">535.31</span></span></td>
<td><span data-ttu-id="4afd6-872">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-873">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-873">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-874">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-874">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-875">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-875">10001</span></span></td>
<td><span data-ttu-id="4afd6-876">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-876">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-877">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4afd6-878">178.44</span></span></td>
<td><span data-ttu-id="4afd6-879">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-880">CC003</span></span></td>
<td><span data-ttu-id="4afd6-881">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-881">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-882">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-882">10001</span></span></td>
<td><span data-ttu-id="4afd6-883">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-883">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-884">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-884">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="4afd6-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4afd6-886">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-887">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-887">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-888">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-888">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-889">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-889">10001</span></span></td>
<td><span data-ttu-id="4afd6-890">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-890">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-891">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-891">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4afd6-892">4,487.12</span></span></td>
<td><span data-ttu-id="4afd6-893">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-894">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-894">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-895">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-895">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-896">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-896">10001</span></span></td>
<td><span data-ttu-id="4afd6-897">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-897">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-898">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-898">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4afd6-899">1,495.71</span></span></td>
<td><span data-ttu-id="4afd6-900">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-901">CC003</span></span></td>
<td><span data-ttu-id="4afd6-902">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-902">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-903">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-903">10001</span></span></td>
<td><span data-ttu-id="4afd6-904">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-904">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-905">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="4afd6-906">-286.25</span></span></td>
<td><span data-ttu-id="4afd6-907">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-908">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-908">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-909">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-909">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-910">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-910">10001</span></span></td>
<td><span data-ttu-id="4afd6-911">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-911">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-912">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4afd6-913">241.05</span></span></td>
<td><span data-ttu-id="4afd6-914">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-915">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-915">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-916">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-916">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-917">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-917">10001</span></span></td>
<td><span data-ttu-id="4afd6-918">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-918">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-919">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4afd6-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4afd6-920">45.20</span></span></td>
<td><span data-ttu-id="4afd6-921">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-922">CC003</span></span></td>
<td><span data-ttu-id="4afd6-923">Surinkimas</span><span class="sxs-lookup"><span data-stu-id="4afd6-923">Assembly</span></span></td>
<td><span data-ttu-id="4afd6-924">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-924">10001</span></span></td>
<td><span data-ttu-id="4afd6-925">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-925">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-926">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-926">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="4afd6-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4afd6-928">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-929">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-929">Prod 1</span></span></td>
<td><span data-ttu-id="4afd6-930">1 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-930">Product 1</span></span></td>
<td><span data-ttu-id="4afd6-931">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-931">10001</span></span></td>
<td><span data-ttu-id="4afd6-932">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-932">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-933">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-933">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4afd6-934">2,507.09</span></span></td>
<td><span data-ttu-id="4afd6-935">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4afd6-936">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-936">Prod 2</span></span></td>
<td><span data-ttu-id="4afd6-937">2 produktas</span><span class="sxs-lookup"><span data-stu-id="4afd6-937">Product 2</span></span></td>
<td><span data-ttu-id="4afd6-938">10001</span><span class="sxs-lookup"><span data-stu-id="4afd6-938">10001</span></span></td>
<td><span data-ttu-id="4afd6-939">Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-939">Electricity</span></span></td>
<td><span data-ttu-id="4afd6-940">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-940">Variable cost</span></span></td>
<td><span data-ttu-id="4afd6-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4afd6-941">470.08</span></span></td>
<td><span data-ttu-id="4afd6-942">2017 m. sausio 31 d.</span><span class="sxs-lookup"><span data-stu-id="4afd6-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4afd6-943">Išvada</span><span class="sxs-lookup"><span data-stu-id="4afd6-943">Conclusion</span></span>
<span data-ttu-id="4afd6-944">Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID.</span><span class="sxs-lookup"><span data-stu-id="4afd6-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4afd6-945">Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="4afd6-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4afd6-946">Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles.</span><span class="sxs-lookup"><span data-stu-id="4afd6-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4afd6-947">Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="4afd6-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4afd6-948">Savikainos elementas</span><span class="sxs-lookup"><span data-stu-id="4afd6-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4afd6-949">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4afd6-950">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="4afd6-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4afd6-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4afd6-951">CC099</span></span></th>
<th><span data-ttu-id="4afd6-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4afd6-952">CC001</span></span></th>
<th><span data-ttu-id="4afd6-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4afd6-953">CC002</span></span></th>
<th><span data-ttu-id="4afd6-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4afd6-954">CC003</span></span></th>
<th><span data-ttu-id="4afd6-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4afd6-955">CC004</span></span></th>
<th><span data-ttu-id="4afd6-956">1 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-956">Proj 1</span></span></th>
<th><span data-ttu-id="4afd6-957">2 projektas</span><span class="sxs-lookup"><span data-stu-id="4afd6-957">Proj 2</span></span></th>
<th><span data-ttu-id="4afd6-958">1 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-958">Prod 1</span></span></th>
<th><span data-ttu-id="4afd6-959">2 gamyba</span><span class="sxs-lookup"><span data-stu-id="4afd6-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4afd6-960">10001 Elektros energija</span><span class="sxs-lookup"><span data-stu-id="4afd6-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4afd6-970">Nesuklasifikuota</span><span class="sxs-lookup"><span data-stu-id="4afd6-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4afd6-972">Fiksuotos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4afd6-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4afd6-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4afd6-981">Kintamos išlaidos</span><span class="sxs-lookup"><span data-stu-id="4afd6-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-982">000</span><span class="sxs-lookup"><span data-stu-id="4afd6-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-987">30,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4afd6-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4afd6-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4afd6-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4afd6-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="4afd6-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4afd6-992">Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus.</span><span class="sxs-lookup"><span data-stu-id="4afd6-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4afd6-993">Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="4afd6-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4afd6-994">Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="4afd6-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4afd6-995">Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą.</span><span class="sxs-lookup"><span data-stu-id="4afd6-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4afd6-996">Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="4afd6-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



