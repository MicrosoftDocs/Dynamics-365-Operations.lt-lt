--- 
title: "Skaičiavimų naudojimas skaičiavimo ir sumavimo veiksmų išvestims pateikti elektroninėse ataskaitose (ER)"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 143856f65eaf1d6d667f4f7dfb229807da6f4ad8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="807a9-103">Skaičiavimų naudojimas skaičiavimo ir sumavimo veiksmų išvestims pateikti elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="807a9-103">Use computations to make the output for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="807a9-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="807a9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="807a9-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="807a9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="807a9-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (2 dalis: skaičiavimų konfigūravimas)“.</span><span class="sxs-lookup"><span data-stu-id="807a9-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="807a9-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="807a9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="807a9-108">Šios ataskaitos konfigūravimas, norint naudoti skaičiavimo ir sumavimo informaciją</span><span class="sxs-lookup"><span data-stu-id="807a9-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="807a9-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="807a9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="807a9-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="807a9-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="807a9-111">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="807a9-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="807a9-112">Medyje išplėskite dalį Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="807a9-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="807a9-113">Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="807a9-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="807a9-114">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="807a9-114">Click Designer.</span></span>
7. <span data-ttu-id="807a9-115">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="807a9-116">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="807a9-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="807a9-117">Įtraukite naują duomenų šaltinį, norėdami gauti išsaugotų blokų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="807a9-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="807a9-118">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="807a9-119">Lauke Pavadinimas įveskite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="807a9-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="807a9-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="807a9-120">$BlocksList</span></span>  
11. <span data-ttu-id="807a9-121">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="807a9-121">Click Edit formula.</span></span>
12. <span data-ttu-id="807a9-122">Medyje pasirinkite Data collection functions\COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="807a9-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="807a9-123">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="807a9-123">Click Add function.</span></span>
14. <span data-ttu-id="807a9-124">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="807a9-124">Click Add data source.</span></span>
15. <span data-ttu-id="807a9-125">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="807a9-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="807a9-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="807a9-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="807a9-127">Lauke Formulė įveskite COLLECTEDLIST('$BlockName', "*").</span><span class="sxs-lookup"><span data-stu-id="807a9-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "*")'.</span></span>
    * <span data-ttu-id="807a9-128">COLLECTEDLIST('$BlockName', "*")</span><span class="sxs-lookup"><span data-stu-id="807a9-128">COLLECTEDLIST('$BlockName', "*")</span></span>  
17. <span data-ttu-id="807a9-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="807a9-129">Click Save.</span></span>
    * <span data-ttu-id="807a9-130">Simbolis * nurodo, kad visi blokai bus įtraukti į šio įrašo sąrašą.</span><span class="sxs-lookup"><span data-stu-id="807a9-130">The pattern “*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="807a9-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="807a9-131">Close the page.</span></span>
19. <span data-ttu-id="807a9-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="807a9-132">Click OK.</span></span>
20. <span data-ttu-id="807a9-133">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="807a9-133">Click the Format tab.</span></span>
21. <span data-ttu-id="807a9-134">Medyje pasirinkite Intrastat\Data.</span><span class="sxs-lookup"><span data-stu-id="807a9-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="807a9-135">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="807a9-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="807a9-136">Medyje pasirinkite Text\Sequence.</span><span class="sxs-lookup"><span data-stu-id="807a9-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="807a9-137">Lauke Pavadinimas, įveskite Bendrosios sumos pagal blokus.</span><span class="sxs-lookup"><span data-stu-id="807a9-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="807a9-138">Bendrosios sumos pagal blokus</span><span class="sxs-lookup"><span data-stu-id="807a9-138">Totals by blocks</span></span>  
25. <span data-ttu-id="807a9-139">Lauke Specialieji simboliai pasirinkite Nauja eilutė – „Windows“ (CR LF).</span><span class="sxs-lookup"><span data-stu-id="807a9-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="807a9-140">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="807a9-140">Click OK.</span></span>
27. <span data-ttu-id="807a9-141">Medyje pasirinkite Intrastat\Data\Totals by blocks.</span><span class="sxs-lookup"><span data-stu-id="807a9-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="807a9-142">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="807a9-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="807a9-143">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="807a9-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="807a9-144">Lauke Pavadinimas įveskite Bloko kodas.</span><span class="sxs-lookup"><span data-stu-id="807a9-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="807a9-145">Bloko kodas</span><span class="sxs-lookup"><span data-stu-id="807a9-145">Block code</span></span>  
31. <span data-ttu-id="807a9-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="807a9-146">Click OK.</span></span>
32. <span data-ttu-id="807a9-147">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="807a9-147">Click Add String.</span></span>
33. <span data-ttu-id="807a9-148">Lauke Pavadinimas įveskite Eilučių skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="807a9-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="807a9-149">Eilučių skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="807a9-149">Lines counting</span></span>  
34. <span data-ttu-id="807a9-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="807a9-150">Click OK.</span></span>
35. <span data-ttu-id="807a9-151">Spustelėkite Įtraukti eilutę.</span><span class="sxs-lookup"><span data-stu-id="807a9-151">Click Add String.</span></span>
36. <span data-ttu-id="807a9-152">Lauke Pavadinimas įveskite Bendroji suma.</span><span class="sxs-lookup"><span data-stu-id="807a9-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="807a9-153">Bendra suma</span><span class="sxs-lookup"><span data-stu-id="807a9-153">Total amount</span></span>  
37. <span data-ttu-id="807a9-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="807a9-154">Click OK.</span></span>
38. <span data-ttu-id="807a9-155">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="807a9-156">Medyje pasirinkite $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="807a9-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="807a9-157">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="807a9-157">Click Bind.</span></span>
    * <span data-ttu-id="807a9-158">Kurkite kiekvieno išsaugoto bloko suvestinės eilutę.</span><span class="sxs-lookup"><span data-stu-id="807a9-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="807a9-159">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="807a9-159">Click the Format tab.</span></span>
42. <span data-ttu-id="807a9-160">Medyje pasirinkite Intrastat\Data\Totals by blocks\Block code.</span><span class="sxs-lookup"><span data-stu-id="807a9-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="807a9-161">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="807a9-162">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="807a9-162">Click Edit formula.</span></span>
45. <span data-ttu-id="807a9-163">Lauke Formulė įveskite '"Block id:: " & '.</span><span class="sxs-lookup"><span data-stu-id="807a9-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="807a9-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="807a9-164">"Block id: " &</span></span>  
46. <span data-ttu-id="807a9-165">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="807a9-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="807a9-166">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="807a9-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="807a9-167">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="807a9-167">Click Add data source.</span></span>
49. <span data-ttu-id="807a9-168">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="807a9-168">Click Save.</span></span>
50. <span data-ttu-id="807a9-169">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="807a9-169">Close the page.</span></span>
51. <span data-ttu-id="807a9-170">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="807a9-170">Click the Format tab.</span></span>
52. <span data-ttu-id="807a9-171">Medyje pasirinkite Intrastat\Data\Totals by blocks\Lines counting.</span><span class="sxs-lookup"><span data-stu-id="807a9-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="807a9-172">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="807a9-173">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="807a9-173">Click Edit formula.</span></span>
    * <span data-ttu-id="807a9-174">Kurkite kiekvieno šioje ataskaitoje pateikto bloko eilučių skaičiaus išvestį.</span><span class="sxs-lookup"><span data-stu-id="807a9-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="807a9-175">Lauke Formulė įveskite '"Number of lines in this block: " & '.</span><span class="sxs-lookup"><span data-stu-id="807a9-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="807a9-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="807a9-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="807a9-177">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="807a9-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="807a9-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="807a9-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="807a9-179">Medyje pasirinkite Data collection functions\COUNTIFS.</span><span class="sxs-lookup"><span data-stu-id="807a9-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="807a9-180">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="807a9-180">Click Add function.</span></span>
59. <span data-ttu-id="807a9-181">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="807a9-181">Click Add data source.</span></span>
60. <span data-ttu-id="807a9-182">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="807a9-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="807a9-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="807a9-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="807a9-184">Medyje išplėskite dalį $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="807a9-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="807a9-185">Medyje pasirinkite $BlocksList\Value.</span><span class="sxs-lookup"><span data-stu-id="807a9-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="807a9-186">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="807a9-186">Click Add data source.</span></span>
64. <span data-ttu-id="807a9-187">Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="807a9-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="807a9-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="807a9-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="807a9-189">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="807a9-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="807a9-190">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="807a9-190">Click Add data source.</span></span>
67. <span data-ttu-id="807a9-191">Lauke Formulė įveskite "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="807a9-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="807a9-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="807a9-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
68. <span data-ttu-id="807a9-193">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="807a9-193">Click Save.</span></span>
69. <span data-ttu-id="807a9-194">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="807a9-194">Close the page.</span></span>
70. <span data-ttu-id="807a9-195">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="807a9-195">Click the Format tab.</span></span>
71. <span data-ttu-id="807a9-196">Medyje pasirinkite Intrastat\Data\Totals by blocks\Total amount.</span><span class="sxs-lookup"><span data-stu-id="807a9-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="807a9-197">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="807a9-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="807a9-198">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="807a9-198">Click Edit formula.</span></span>
    * <span data-ttu-id="807a9-199">Kurkite išvestį, kuri bus kiekvieno šioje ataskaitoje pateikto bloko bendroji SF suma.</span><span class="sxs-lookup"><span data-stu-id="807a9-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="807a9-200">Lauke Formulė įveskite "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="807a9-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="807a9-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="807a9-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
75. <span data-ttu-id="807a9-202">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="807a9-202">Click Save.</span></span>
76. <span data-ttu-id="807a9-203">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="807a9-203">Close the page.</span></span>
77. <span data-ttu-id="807a9-204">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="807a9-204">Click Save.</span></span>
78. <span data-ttu-id="807a9-205">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="807a9-205">Close the page.</span></span>


