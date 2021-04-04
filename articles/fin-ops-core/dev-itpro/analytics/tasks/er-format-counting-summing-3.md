---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis – Skaičiavimų naudojimas išvesčiai kurti)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (3 dalis)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567121"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="4186e-104">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis – Skaičiavimų naudojimas išvesčiai kurti)</span><span class="sxs-lookup"><span data-stu-id="4186e-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4186e-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="4186e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="4186e-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="4186e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4186e-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (2 dalis. Skaičiavimų konfigūravimas)“.</span><span class="sxs-lookup"><span data-stu-id="4186e-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="4186e-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="4186e-109">Šios ataskaitos konfigūravimas, norint naudoti skaičiavimo ir sumavimo informaciją</span><span class="sxs-lookup"><span data-stu-id="4186e-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="4186e-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="4186e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4186e-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="4186e-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4186e-112">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="4186e-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="4186e-113">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="4186e-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="4186e-114">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="4186e-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="4186e-115">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="4186e-115">Click Designer.</span></span>
7. <span data-ttu-id="4186e-116">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="4186e-117">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="4186e-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="4186e-118">Įtraukite naują duomenų šaltinį, norėdami gauti išsaugotų blokų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4186e-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="4186e-119">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="4186e-120">Lauke Pavadinimas įveskite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="4186e-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="4186e-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="4186e-121">$BlocksList</span></span>  
11. <span data-ttu-id="4186e-122">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="4186e-122">Click Edit formula.</span></span>
12. <span data-ttu-id="4186e-123">Medyje pasirinkite Data collection functions\COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="4186e-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="4186e-124">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="4186e-124">Click Add function.</span></span>
14. <span data-ttu-id="4186e-125">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="4186e-125">Click Add data source.</span></span>
15. <span data-ttu-id="4186e-126">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="4186e-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="4186e-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4186e-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="4186e-128">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', "\*").</span><span class="sxs-lookup"><span data-stu-id="4186e-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="4186e-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="4186e-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="4186e-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-130">Click Save.</span></span>
    * <span data-ttu-id="4186e-131">Simbolis „\*“ nurodo, kad visi blokai bus įtraukti į šio įrašo sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4186e-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="4186e-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4186e-132">Close the page.</span></span>
19. <span data-ttu-id="4186e-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4186e-133">Click OK.</span></span>
20. <span data-ttu-id="4186e-134">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="4186e-134">Click the Format tab.</span></span>
21. <span data-ttu-id="4186e-135">Medyje pasirinkite Intrastat\Data.</span><span class="sxs-lookup"><span data-stu-id="4186e-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="4186e-136">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="4186e-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="4186e-137">Medyje pasirinkite Text\Sequence.</span><span class="sxs-lookup"><span data-stu-id="4186e-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="4186e-138">Lauke Pavadinimas, įveskite Bendrosios sumos pagal blokus.</span><span class="sxs-lookup"><span data-stu-id="4186e-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="4186e-139">Bendrosios sumos pagal blokus</span><span class="sxs-lookup"><span data-stu-id="4186e-139">Totals by blocks</span></span>  
25. <span data-ttu-id="4186e-140">Lauke Specialieji simboliai pasirinkite Nauja eilutė – „Windows“ (CR LF).</span><span class="sxs-lookup"><span data-stu-id="4186e-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="4186e-141">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="4186e-141">Click OK.</span></span>
27. <span data-ttu-id="4186e-142">Medyje pasirinkite Intrastat\Data\Totals by blocks.</span><span class="sxs-lookup"><span data-stu-id="4186e-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="4186e-143">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="4186e-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="4186e-144">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="4186e-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="4186e-145">Lauke Pavadinimas įveskite Bloko kodas.</span><span class="sxs-lookup"><span data-stu-id="4186e-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="4186e-146">Bloko kodas</span><span class="sxs-lookup"><span data-stu-id="4186e-146">Block code</span></span>  
31. <span data-ttu-id="4186e-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4186e-147">Click OK.</span></span>
32. <span data-ttu-id="4186e-148">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="4186e-148">Click Add String.</span></span>
33. <span data-ttu-id="4186e-149">Lauke Pavadinimas įveskite Eilučių skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="4186e-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="4186e-150">Eilučių skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="4186e-150">Lines counting</span></span>  
34. <span data-ttu-id="4186e-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4186e-151">Click OK.</span></span>
35. <span data-ttu-id="4186e-152">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="4186e-152">Click Add String.</span></span>
36. <span data-ttu-id="4186e-153">Lauke Pavadinimas įveskite Bendroji suma.</span><span class="sxs-lookup"><span data-stu-id="4186e-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="4186e-154">Bendra suma</span><span class="sxs-lookup"><span data-stu-id="4186e-154">Total amount</span></span>  
37. <span data-ttu-id="4186e-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4186e-155">Click OK.</span></span>
38. <span data-ttu-id="4186e-156">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="4186e-157">Medyje pasirinkite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="4186e-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="4186e-158">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="4186e-158">Click Bind.</span></span>
    * <span data-ttu-id="4186e-159">Kurkite kiekvieno išsaugoto bloko suvestinės eilutę.</span><span class="sxs-lookup"><span data-stu-id="4186e-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="4186e-160">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="4186e-160">Click the Format tab.</span></span>
42. <span data-ttu-id="4186e-161">Medyje pasirinkite Intrastat\Data\Totals by blocks\Block code.</span><span class="sxs-lookup"><span data-stu-id="4186e-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="4186e-162">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="4186e-163">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="4186e-163">Click Edit formula.</span></span>
45. <span data-ttu-id="4186e-164">Lauke Formulė įveskite '"Block id: " & '.</span><span class="sxs-lookup"><span data-stu-id="4186e-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="4186e-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="4186e-165">"Block id: " &</span></span>  
46. <span data-ttu-id="4186e-166">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="4186e-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="4186e-167">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="4186e-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="4186e-168">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="4186e-168">Click Add data source.</span></span>
49. <span data-ttu-id="4186e-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-169">Click Save.</span></span>
50. <span data-ttu-id="4186e-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4186e-170">Close the page.</span></span>
51. <span data-ttu-id="4186e-171">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="4186e-171">Click the Format tab.</span></span>
52. <span data-ttu-id="4186e-172">Medyje pasirinkite Intrastat\Data\Totals by blocks\Lines counting.</span><span class="sxs-lookup"><span data-stu-id="4186e-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="4186e-173">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="4186e-174">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="4186e-174">Click Edit formula.</span></span>
    * <span data-ttu-id="4186e-175">Kurkite kiekvieno šioje ataskaitoje pateikto bloko eilučių skaičiaus išvestį.</span><span class="sxs-lookup"><span data-stu-id="4186e-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="4186e-176">Lauke Formulė įveskite '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="4186e-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="4186e-177">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="4186e-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="4186e-178">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="4186e-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="4186e-179">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="4186e-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="4186e-180">Medyje pasirinkite Data collection functions\COUNTIFS.</span><span class="sxs-lookup"><span data-stu-id="4186e-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="4186e-181">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="4186e-181">Click Add function.</span></span>
59. <span data-ttu-id="4186e-182">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="4186e-182">Click Add data source.</span></span>
60. <span data-ttu-id="4186e-183">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="4186e-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="4186e-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="4186e-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="4186e-185">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="4186e-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="4186e-186">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="4186e-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="4186e-187">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="4186e-187">Click Add data source.</span></span>
64. <span data-ttu-id="4186e-188">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="4186e-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="4186e-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="4186e-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="4186e-190">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="4186e-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="4186e-191">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="4186e-191">Click Add data source.</span></span>
67. <span data-ttu-id="4186e-192">Lauke Formulė įveskite "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="4186e-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4186e-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4186e-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="4186e-194">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-194">Click Save.</span></span>
69. <span data-ttu-id="4186e-195">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4186e-195">Close the page.</span></span>
70. <span data-ttu-id="4186e-196">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="4186e-196">Click the Format tab.</span></span>
71. <span data-ttu-id="4186e-197">Medyje pasirinkite Intrastat\Data\Totals by blocks\Total amount.</span><span class="sxs-lookup"><span data-stu-id="4186e-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="4186e-198">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="4186e-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="4186e-199">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="4186e-199">Click Edit formula.</span></span>
    * <span data-ttu-id="4186e-200">Kurkite išvestį, kuri bus kiekvieno šioje ataskaitoje pateikto bloko bendroji SF suma.</span><span class="sxs-lookup"><span data-stu-id="4186e-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="4186e-201">Lauke Formulė įveskite "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="4186e-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="4186e-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="4186e-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="4186e-203">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-203">Click Save.</span></span>
76. <span data-ttu-id="4186e-204">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4186e-204">Close the page.</span></span>
77. <span data-ttu-id="4186e-205">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4186e-205">Click Save.</span></span>
78. <span data-ttu-id="4186e-206">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4186e-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]