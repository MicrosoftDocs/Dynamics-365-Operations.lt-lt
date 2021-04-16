---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (2 dalis – Skaičiavimų konfigūravimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (2 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a14fe079515b176cbcda74852ae2ad456dd6434a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749026"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="03075-104">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (2 dalis – Skaičiavimų konfigūravimas)</span><span class="sxs-lookup"><span data-stu-id="03075-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03075-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="03075-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="03075-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="03075-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="03075-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (1 dalis. Formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="03075-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="03075-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="03075-109">Formato konfigūracijos kūrimas, norint įtraukti skaičiavimo ir sumavimo informaciją</span><span class="sxs-lookup"><span data-stu-id="03075-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="03075-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="03075-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="03075-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="03075-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="03075-112">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="03075-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="03075-113">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="03075-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="03075-114">Tarkime, kad norite tinkinti formatą, kurį teikia „Microsoft“, „Intrastat“ ataskaitos gale įtraukdami eilutes su suvestinės informacija.</span><span class="sxs-lookup"><span data-stu-id="03075-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="03075-115">Tai galite atlikti, savo „Intrastat“ konfigūracijos egzempliorių išvesdami iš „Microsoft“ egzemplioriaus, kad galėtumėte atlikti keitimus.</span><span class="sxs-lookup"><span data-stu-id="03075-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="03075-116">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="03075-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="03075-117">Lauke Naujas įveskite Kildinti iš pavadinimo: „Intrastat“ (DE), „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="03075-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="03075-118">Lauke Pavadinimas įveskite Intrastat (DE) be skaičiavimo ir sumavimo.</span><span class="sxs-lookup"><span data-stu-id="03075-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="03075-119">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="03075-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="03075-120">Šios ataskaitos konfigūravimas, norint skaičiavimo ir sumavimo veiksmus atlikti pagal išvesties informaciją</span><span class="sxs-lookup"><span data-stu-id="03075-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="03075-121">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="03075-121">Click Designer.</span></span>
2. <span data-ttu-id="03075-122">Lauke Rinkti išeigos informaciją pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="03075-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="03075-123">Pažymėjus šią žymą, vykdymo metu bus suaktyvintas „Intrastat“ failo generavimo išvesties informacijos rinkimo procesas.</span><span class="sxs-lookup"><span data-stu-id="03075-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="03075-124">Turite atlikti skirtingų „Intrastat“ krypčių skaičiavimus, todėl skirtąjį modelių išvardijimą turite įtraukti į šios formato konfigūracijos duomenų šaltinių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="03075-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="03075-125">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="03075-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="03075-126">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="03075-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="03075-127">Medyje pasirinkite Data model\Enumeration.</span><span class="sxs-lookup"><span data-stu-id="03075-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="03075-128">Lauke Pavadinimas įveskite Kryptis.</span><span class="sxs-lookup"><span data-stu-id="03075-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="03075-129">Lauke Modelių išvardijimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03075-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="03075-130">Pasirinkite reikšmę Kryptis.</span><span class="sxs-lookup"><span data-stu-id="03075-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="03075-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03075-131">Click OK.</span></span>
9. <span data-ttu-id="03075-132">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="03075-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="03075-133">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="03075-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="03075-134">Lauke Pavadinimas įveskite $BlockName.</span><span class="sxs-lookup"><span data-stu-id="03075-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="03075-135">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="03075-135">Click Edit formula.</span></span>
13. <span data-ttu-id="03075-136">Lauke Formulė įveskite blokas.</span><span class="sxs-lookup"><span data-stu-id="03075-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="03075-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-137">Click Save.</span></span>
15. <span data-ttu-id="03075-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-138">Close the page.</span></span>
16. <span data-ttu-id="03075-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03075-139">Click OK.</span></span>
17. <span data-ttu-id="03075-140">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="03075-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="03075-141">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="03075-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="03075-142">Lauke Pavadinimas įveskite $RecName.</span><span class="sxs-lookup"><span data-stu-id="03075-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="03075-143">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="03075-143">Click Edit formula.</span></span>
21. <span data-ttu-id="03075-144">Lauke Formulė įveskite įrašas.</span><span class="sxs-lookup"><span data-stu-id="03075-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="03075-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-145">Click Save.</span></span>
23. <span data-ttu-id="03075-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-146">Close the page.</span></span>
24. <span data-ttu-id="03075-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03075-147">Click OK.</span></span>
25. <span data-ttu-id="03075-148">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="03075-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="03075-149">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="03075-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="03075-150">Lauke Pavadinimas įveskite $InvName.</span><span class="sxs-lookup"><span data-stu-id="03075-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="03075-151">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="03075-151">Click Edit formula.</span></span>
29. <span data-ttu-id="03075-152">Lauke Formulė įveskite InvoicedAmountEUR.</span><span class="sxs-lookup"><span data-stu-id="03075-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="03075-153">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-153">Click Save.</span></span>
31. <span data-ttu-id="03075-154">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-154">Close the page.</span></span>
32. <span data-ttu-id="03075-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03075-155">Click OK.</span></span>
33. <span data-ttu-id="03075-156">Medyje pasirinkite Intrastat\Data.</span><span class="sxs-lookup"><span data-stu-id="03075-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="03075-157">Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="03075-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="03075-158">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="03075-158">Click Add data source.</span></span>
    * <span data-ttu-id="03075-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="03075-159">$BlockName</span></span>  
36. <span data-ttu-id="03075-160">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-160">Click Save.</span></span>
37. <span data-ttu-id="03075-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-161">Close the page.</span></span>
38. <span data-ttu-id="03075-162">Spustelėkite lauko Surinktų duomenų rakto reikšmė mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03075-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="03075-163">Lauke Formulė įveskite IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").</span><span class="sxs-lookup"><span data-stu-id="03075-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="03075-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="03075-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="03075-165">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-165">Click Save.</span></span>
41. <span data-ttu-id="03075-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-166">Close the page.</span></span>
    * <span data-ttu-id="03075-167">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="03075-167">Count the lines of this sequence.</span></span> <span data-ttu-id="03075-168">Rezultatai, pavadinimu „blokas“, bus atskirai naudojami skirtingoms kryptims.</span><span class="sxs-lookup"><span data-stu-id="03075-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="03075-169">Reikšmė „Importuoti“ bus naudojama visoms „Intrastat“ gavimų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="03075-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="03075-170">Reikšmė „Eksportuoti“ bus naudojama visoms „Intrastat“ išsiuntimų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="03075-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="03075-171">Tai gali būti laikoma virtualia „Excel“ skaičiuokle.</span><span class="sxs-lookup"><span data-stu-id="03075-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="03075-172">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“.</span><span class="sxs-lookup"><span data-stu-id="03075-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="03075-173">Medyje išplėskite dalį Intrastat\Data: Sequence.</span><span class="sxs-lookup"><span data-stu-id="03075-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="03075-174">Medyje pasirinkite Intrastat\Data: Sequence\Arrivals?.</span><span class="sxs-lookup"><span data-stu-id="03075-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="03075-175">Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03075-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="03075-176">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="03075-176">Count the lines of this sequence.</span></span> <span data-ttu-id="03075-177">Rezultatai bus išsaugoti naudojant pavadinimą „įrašas“.</span><span class="sxs-lookup"><span data-stu-id="03075-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="03075-178">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="03075-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="03075-179">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="03075-179">Click Add data source.</span></span>
47. <span data-ttu-id="03075-180">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-180">Click Save.</span></span>
48. <span data-ttu-id="03075-181">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-181">Close the page.</span></span>
49. <span data-ttu-id="03075-182">Spustelėkite lauko „Surinktų duomenų rakto reikšmė“ mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="03075-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="03075-183">Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="03075-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="03075-184">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-184">Click Save.</span></span>
52. <span data-ttu-id="03075-185">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-185">Close the page.</span></span>
    * <span data-ttu-id="03075-186">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="03075-186">Count the lines of this sequence.</span></span> <span data-ttu-id="03075-187">Rezultatai, pavadinimu „įrašas“, bus atskirai naudojami skirtingiems prekių kodams.</span><span class="sxs-lookup"><span data-stu-id="03075-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="03075-188">Tai gali būti laikoma virtualia „Excel“ skaičiuokle.</span><span class="sxs-lookup"><span data-stu-id="03075-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="03075-189">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“, o antrasis blokas, pavadinimu „įrašas“, užpildytas prekės kodo reikšme.</span><span class="sxs-lookup"><span data-stu-id="03075-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="03075-190">Medyje pasirinkite Intrastat\Data: Sequence\Dispatches?.</span><span class="sxs-lookup"><span data-stu-id="03075-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="03075-191">Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="03075-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="03075-192">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="03075-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="03075-193">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="03075-193">Click Add data source.</span></span>
57. <span data-ttu-id="03075-194">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-194">Click Save.</span></span>
58. <span data-ttu-id="03075-195">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-195">Close the page.</span></span>
59. <span data-ttu-id="03075-196">Spustelėkite lauko „Surinktų duomenų rakto reikšmė“ mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03075-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="03075-197">Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="03075-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="03075-198">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-198">Click Save.</span></span>
62. <span data-ttu-id="03075-199">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-199">Close the page.</span></span>
63. <span data-ttu-id="03075-200">Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?.</span><span class="sxs-lookup"><span data-stu-id="03075-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="03075-201">Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="03075-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="03075-202">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="03075-202">Click the Format tab.</span></span>
66. <span data-ttu-id="03075-203">Medyje pasirinkite Intrastat\Data\Dispatches\Record\Invoice amount EUR.</span><span class="sxs-lookup"><span data-stu-id="03075-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="03075-204">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="03075-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="03075-205">Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03075-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="03075-206">Medyje pasirinkite $InvName.</span><span class="sxs-lookup"><span data-stu-id="03075-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="03075-207">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="03075-207">Click Add data source.</span></span>
71. <span data-ttu-id="03075-208">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-208">Click Save.</span></span>
72. <span data-ttu-id="03075-209">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-209">Close the page.</span></span>
    * <span data-ttu-id="03075-210">Susumuokite šios sekos eilučių SF sumos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="03075-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="03075-211">Rezultatai, pavadinimu „InvoicedAmountEUR“, bus naudojami skirtingoms „Intrastat“ kryptims ir prekių kodams.</span><span class="sxs-lookup"><span data-stu-id="03075-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="03075-212">Tai gali būti laikoma virtualiai sukurtu elementu „Excel“ skaičiuoklėje.</span><span class="sxs-lookup"><span data-stu-id="03075-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="03075-213">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“.</span><span class="sxs-lookup"><span data-stu-id="03075-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="03075-214">Antrasis blokas, pavadinimu „įrašas“, užpildomas prekės kodo reikšme, o trečiasis stulpelis, pavadinimu „InvoicedAmountEUR“, užpildomas SF sumos reikšme.</span><span class="sxs-lookup"><span data-stu-id="03075-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="03075-215">Medyje išplėskite dalį Intrastat\Data\Arrivals?.</span><span class="sxs-lookup"><span data-stu-id="03075-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="03075-216">Medyje išplėskite dalį Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="03075-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="03075-217">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="03075-217">Click the Format tab.</span></span>
76. <span data-ttu-id="03075-218">Medyje pasirinkite Intrastat\Data\Arrivals\Record\Invoice amount EUR.</span><span class="sxs-lookup"><span data-stu-id="03075-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="03075-219">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="03075-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="03075-220">Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="03075-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="03075-221">Medyje pasirinkite $InvName.</span><span class="sxs-lookup"><span data-stu-id="03075-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="03075-222">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="03075-222">Click Add data source.</span></span>
81. <span data-ttu-id="03075-223">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-223">Click Save.</span></span>
82. <span data-ttu-id="03075-224">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-224">Close the page.</span></span>
83. <span data-ttu-id="03075-225">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03075-225">Click Save.</span></span>
84. <span data-ttu-id="03075-226">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03075-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]