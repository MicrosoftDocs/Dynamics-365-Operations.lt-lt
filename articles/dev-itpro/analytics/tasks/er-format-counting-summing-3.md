---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis – Skaičiavimų naudojimas išvesčiai kurti)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544615"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="66d87-103">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis: skaičiavimų naudojimas išvesčiai kurti)</span><span class="sxs-lookup"><span data-stu-id="66d87-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66d87-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="66d87-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="66d87-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="66d87-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="66d87-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (2 dalis: skaičiavimų konfigūravimas)“.</span><span class="sxs-lookup"><span data-stu-id="66d87-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="66d87-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="66d87-108">Šios ataskaitos konfigūravimas, norint naudoti skaičiavimo ir sumavimo informaciją</span><span class="sxs-lookup"><span data-stu-id="66d87-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="66d87-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="66d87-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="66d87-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="66d87-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="66d87-111">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="66d87-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="66d87-112">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="66d87-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="66d87-113">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="66d87-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="66d87-114">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="66d87-114">Click Designer.</span></span>
7. <span data-ttu-id="66d87-115">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="66d87-116">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="66d87-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="66d87-117">Įtraukite naują duomenų šaltinį, norėdami gauti išsaugotų blokų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="66d87-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="66d87-118">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="66d87-119">Lauke Pavadinimas įveskite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="66d87-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="66d87-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="66d87-120">$BlocksList</span></span>  
11. <span data-ttu-id="66d87-121">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="66d87-121">Click Edit formula.</span></span>
12. <span data-ttu-id="66d87-122">Medyje pasirinkite Data collection functions\COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="66d87-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="66d87-123">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="66d87-123">Click Add function.</span></span>
14. <span data-ttu-id="66d87-124">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="66d87-124">Click Add data source.</span></span>
15. <span data-ttu-id="66d87-125">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="66d87-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="66d87-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="66d87-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="66d87-127">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', "\*").</span><span class="sxs-lookup"><span data-stu-id="66d87-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="66d87-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="66d87-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="66d87-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-129">Click Save.</span></span>
    * <span data-ttu-id="66d87-130">Simbolis \* nurodo, kad visi blokai bus įtraukti į šio įrašo sąrašą.</span><span class="sxs-lookup"><span data-stu-id="66d87-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="66d87-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66d87-131">Close the page.</span></span>
19. <span data-ttu-id="66d87-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="66d87-132">Click OK.</span></span>
20. <span data-ttu-id="66d87-133">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="66d87-133">Click the Format tab.</span></span>
21. <span data-ttu-id="66d87-134">Medyje pasirinkite Intrastat\Data.</span><span class="sxs-lookup"><span data-stu-id="66d87-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="66d87-135">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="66d87-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="66d87-136">Medyje pasirinkite Text\Sequence.</span><span class="sxs-lookup"><span data-stu-id="66d87-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="66d87-137">Lauke Pavadinimas, įveskite Bendrosios sumos pagal blokus.</span><span class="sxs-lookup"><span data-stu-id="66d87-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="66d87-138">Bendrosios sumos pagal blokus</span><span class="sxs-lookup"><span data-stu-id="66d87-138">Totals by blocks</span></span>  
25. <span data-ttu-id="66d87-139">Lauke Specialieji simboliai pasirinkite Nauja eilutė – „Windows“ (CR LF).</span><span class="sxs-lookup"><span data-stu-id="66d87-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="66d87-140">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="66d87-140">Click OK.</span></span>
27. <span data-ttu-id="66d87-141">Medyje pasirinkite Intrastat\Data\Totals by blocks.</span><span class="sxs-lookup"><span data-stu-id="66d87-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="66d87-142">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="66d87-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="66d87-143">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="66d87-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="66d87-144">Lauke Pavadinimas įveskite Bloko kodas.</span><span class="sxs-lookup"><span data-stu-id="66d87-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="66d87-145">Bloko kodas</span><span class="sxs-lookup"><span data-stu-id="66d87-145">Block code</span></span>  
31. <span data-ttu-id="66d87-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="66d87-146">Click OK.</span></span>
32. <span data-ttu-id="66d87-147">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="66d87-147">Click Add String.</span></span>
33. <span data-ttu-id="66d87-148">Lauke Pavadinimas įveskite Eilučių skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="66d87-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="66d87-149">Eilučių skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="66d87-149">Lines counting</span></span>  
34. <span data-ttu-id="66d87-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="66d87-150">Click OK.</span></span>
35. <span data-ttu-id="66d87-151">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="66d87-151">Click Add String.</span></span>
36. <span data-ttu-id="66d87-152">Lauke Pavadinimas įveskite Bendroji suma.</span><span class="sxs-lookup"><span data-stu-id="66d87-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="66d87-153">Bendra suma</span><span class="sxs-lookup"><span data-stu-id="66d87-153">Total amount</span></span>  
37. <span data-ttu-id="66d87-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="66d87-154">Click OK.</span></span>
38. <span data-ttu-id="66d87-155">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="66d87-156">Medyje pasirinkite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="66d87-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="66d87-157">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="66d87-157">Click Bind.</span></span>
    * <span data-ttu-id="66d87-158">Kurkite kiekvieno išsaugoto bloko suvestinės eilutę.</span><span class="sxs-lookup"><span data-stu-id="66d87-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="66d87-159">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="66d87-159">Click the Format tab.</span></span>
42. <span data-ttu-id="66d87-160">Medyje pasirinkite Intrastat\Data\Totals by blocks\Block code.</span><span class="sxs-lookup"><span data-stu-id="66d87-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="66d87-161">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="66d87-162">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="66d87-162">Click Edit formula.</span></span>
45. <span data-ttu-id="66d87-163">Lauke Formulė įveskite '"Block id: " & '.</span><span class="sxs-lookup"><span data-stu-id="66d87-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="66d87-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="66d87-164">"Block id: " &</span></span>  
46. <span data-ttu-id="66d87-165">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="66d87-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="66d87-166">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="66d87-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="66d87-167">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="66d87-167">Click Add data source.</span></span>
49. <span data-ttu-id="66d87-168">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-168">Click Save.</span></span>
50. <span data-ttu-id="66d87-169">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66d87-169">Close the page.</span></span>
51. <span data-ttu-id="66d87-170">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="66d87-170">Click the Format tab.</span></span>
52. <span data-ttu-id="66d87-171">Medyje pasirinkite Intrastat\Data\Totals by blocks\Lines counting.</span><span class="sxs-lookup"><span data-stu-id="66d87-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="66d87-172">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="66d87-173">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="66d87-173">Click Edit formula.</span></span>
    * <span data-ttu-id="66d87-174">Kurkite kiekvieno šioje ataskaitoje pateikto bloko eilučių skaičiaus išvestį.</span><span class="sxs-lookup"><span data-stu-id="66d87-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="66d87-175">Lauke Formulė įveskite '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="66d87-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="66d87-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="66d87-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="66d87-177">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="66d87-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="66d87-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="66d87-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="66d87-179">Medyje pasirinkite Data collection functions\COUNTIFS.</span><span class="sxs-lookup"><span data-stu-id="66d87-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="66d87-180">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="66d87-180">Click Add function.</span></span>
59. <span data-ttu-id="66d87-181">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="66d87-181">Click Add data source.</span></span>
60. <span data-ttu-id="66d87-182">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="66d87-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="66d87-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="66d87-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="66d87-184">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="66d87-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="66d87-185">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="66d87-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="66d87-186">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="66d87-186">Click Add data source.</span></span>
64. <span data-ttu-id="66d87-187">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="66d87-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="66d87-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="66d87-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="66d87-189">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="66d87-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="66d87-190">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="66d87-190">Click Add data source.</span></span>
67. <span data-ttu-id="66d87-191">Lauke Formulė įveskite "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="66d87-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="66d87-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="66d87-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="66d87-193">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-193">Click Save.</span></span>
69. <span data-ttu-id="66d87-194">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66d87-194">Close the page.</span></span>
70. <span data-ttu-id="66d87-195">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="66d87-195">Click the Format tab.</span></span>
71. <span data-ttu-id="66d87-196">Medyje pasirinkite Intrastat\Data\Totals by blocks\Total amount.</span><span class="sxs-lookup"><span data-stu-id="66d87-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="66d87-197">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="66d87-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="66d87-198">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="66d87-198">Click Edit formula.</span></span>
    * <span data-ttu-id="66d87-199">Kurkite išvestį, kuri bus kiekvieno šioje ataskaitoje pateikto bloko bendroji SF suma.</span><span class="sxs-lookup"><span data-stu-id="66d87-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="66d87-200">Lauke Formulė įveskite "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="66d87-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="66d87-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="66d87-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="66d87-202">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-202">Click Save.</span></span>
76. <span data-ttu-id="66d87-203">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66d87-203">Close the page.</span></span>
77. <span data-ttu-id="66d87-204">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="66d87-204">Click Save.</span></span>
78. <span data-ttu-id="66d87-205">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66d87-205">Close the page.</span></span>

