--- 
title: "Skaičiavimų konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d41ce101c0b038627e2baf6b5eac2410095af7ce
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="configure-computations-to-do-counting-and-summing"></a><span data-ttu-id="c83dc-103">Skaičiavimų konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti</span><span class="sxs-lookup"><span data-stu-id="c83dc-103">Configure computations to do counting and summing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c83dc-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="c83dc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="c83dc-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="c83dc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c83dc-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (1 dalis: formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="c83dc-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="c83dc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="c83dc-108">Formato konfigūracijos kūrimas, norint įtraukti skaičiavimo ir sumavimo informaciją</span><span class="sxs-lookup"><span data-stu-id="c83dc-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="c83dc-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c83dc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c83dc-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="c83dc-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c83dc-111">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="c83dc-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="c83dc-112">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="c83dc-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="c83dc-113">Tarkime, kad norite tinkinti formatą, kurį teikia „Microsoft“, „Intrastat“ ataskaitos gale įtraukdami eilutes su suvestinės informacija.</span><span class="sxs-lookup"><span data-stu-id="c83dc-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="c83dc-114">Tai galite atlikti, savo „Intrastat“ konfigūracijos egzempliorių išvesdami iš „Microsoft“ egzemplioriaus, kad galėtumėte atlikti keitimus.</span><span class="sxs-lookup"><span data-stu-id="c83dc-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="c83dc-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="c83dc-116">Lauke Naujas įveskite Kildinti iš pavadinimo: „Intrastat“ (DE), „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="c83dc-117">Lauke Pavadinimas įveskite Intrastat (DE) be skaičiavimo ir sumavimo.</span><span class="sxs-lookup"><span data-stu-id="c83dc-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="c83dc-118">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c83dc-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="c83dc-119">Šios ataskaitos konfigūravimas, norint skaičiavimo ir sumavimo veiksmus atlikti pagal išvesties informaciją</span><span class="sxs-lookup"><span data-stu-id="c83dc-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="c83dc-120">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="c83dc-120">Click Designer.</span></span>
2. <span data-ttu-id="c83dc-121">Lauke Rinkti išeigos informaciją pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c83dc-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="c83dc-122">Pažymėjus šią žymą, vykdymo metu bus suaktyvintas „Intrastat“ failo generavimo išvesties informacijos rinkimo procesas.</span><span class="sxs-lookup"><span data-stu-id="c83dc-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="c83dc-123">Turite atlikti skirtingų „Intrastat“ krypčių skaičiavimus, todėl skirtąjį modelių išvardijimą turite įtraukti į šios formato konfigūracijos duomenų šaltinių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="c83dc-124">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="c83dc-125">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="c83dc-126">Medyje pasirinkite Data model\Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c83dc-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="c83dc-127">Lauke Pavadinimas įveskite Kryptis.</span><span class="sxs-lookup"><span data-stu-id="c83dc-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="c83dc-128">Lauke Modelių išvardijimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c83dc-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="c83dc-129">Pasirinkite reikšmę Kryptis.</span><span class="sxs-lookup"><span data-stu-id="c83dc-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="c83dc-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c83dc-130">Click OK.</span></span>
9. <span data-ttu-id="c83dc-131">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="c83dc-132">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="c83dc-133">Lauke Pavadinimas įveskite $BlockName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="c83dc-134">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-134">Click Edit formula.</span></span>
13. <span data-ttu-id="c83dc-135">Lauke Formulė įveskite blokas.</span><span class="sxs-lookup"><span data-stu-id="c83dc-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="c83dc-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-136">Click Save.</span></span>
15. <span data-ttu-id="c83dc-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-137">Close the page.</span></span>
16. <span data-ttu-id="c83dc-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c83dc-138">Click OK.</span></span>
17. <span data-ttu-id="c83dc-139">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="c83dc-140">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="c83dc-141">Lauke Pavadinimas įveskite $RecName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="c83dc-142">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-142">Click Edit formula.</span></span>
21. <span data-ttu-id="c83dc-143">Lauke Formulė įveskite įrašas.</span><span class="sxs-lookup"><span data-stu-id="c83dc-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="c83dc-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-144">Click Save.</span></span>
23. <span data-ttu-id="c83dc-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-145">Close the page.</span></span>
24. <span data-ttu-id="c83dc-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c83dc-146">Click OK.</span></span>
25. <span data-ttu-id="c83dc-147">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c83dc-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="c83dc-148">Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="c83dc-149">Lauke Pavadinimas įveskite $InvName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="c83dc-150">Spustelėkite „Redaguoti formulę“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-150">Click Edit formula.</span></span>
29. <span data-ttu-id="c83dc-151">Lauke Formulė įveskite InvoicedAmountEUR.</span><span class="sxs-lookup"><span data-stu-id="c83dc-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="c83dc-152">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-152">Click Save.</span></span>
31. <span data-ttu-id="c83dc-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-153">Close the page.</span></span>
32. <span data-ttu-id="c83dc-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c83dc-154">Click OK.</span></span>
33. <span data-ttu-id="c83dc-155">Medyje pasirinkite Intrastat\Data.</span><span class="sxs-lookup"><span data-stu-id="c83dc-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="c83dc-156">Spustelėkite lauko Surinktų duomenų rakto pavadinimas mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="c83dc-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="c83dc-157">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-157">Click Add data source.</span></span>
    * <span data-ttu-id="c83dc-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="c83dc-158">$BlockName</span></span>  
36. <span data-ttu-id="c83dc-159">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-159">Click Save.</span></span>
37. <span data-ttu-id="c83dc-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-160">Close the page.</span></span>
38. <span data-ttu-id="c83dc-161">Spustelėkite lauko Surinktų duomenų rakto reikšmė mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="c83dc-162">Lauke Formulė įveskite IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").</span><span class="sxs-lookup"><span data-stu-id="c83dc-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="c83dc-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="c83dc-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="c83dc-164">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-164">Click Save.</span></span>
41. <span data-ttu-id="c83dc-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-165">Close the page.</span></span>
    * <span data-ttu-id="c83dc-166">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="c83dc-166">Count the lines of this sequence.</span></span> <span data-ttu-id="c83dc-167">Rezultatai, pavadinimu „blokas“, bus atskirai naudojami skirtingoms kryptims.</span><span class="sxs-lookup"><span data-stu-id="c83dc-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="c83dc-168">Reikšmė Importuoti bus naudojama visoms „Intrastat“ gavimų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="c83dc-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="c83dc-169">Reikšmė Eksportuoti bus naudojama visoms „Intrastat“ išsiuntimų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="c83dc-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="c83dc-170">Tai gali būti laikoma virtualia „Excel“ skaičiuokle.</span><span class="sxs-lookup"><span data-stu-id="c83dc-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="c83dc-171">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis, pavadinimu „blokas“, bus užpildytas atitinkamomis reikšmėmis Importuoti ir Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="c83dc-172">Medyje išplėskite dalį Intrastat\Data: Sequence.</span><span class="sxs-lookup"><span data-stu-id="c83dc-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="c83dc-173">Medyje pasirinkite Intrastat\Data: Sequence\Arrivals?.</span><span class="sxs-lookup"><span data-stu-id="c83dc-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="c83dc-174">Spustelėkite lauko Surinktų duomenų rakto pavadinimas mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="c83dc-175">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="c83dc-175">Count the lines of this sequence.</span></span> <span data-ttu-id="c83dc-176">Rezultatai bus išsaugoti naudojant pavadinimą „įrašas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="c83dc-177">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="c83dc-178">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-178">Click Add data source.</span></span>
47. <span data-ttu-id="c83dc-179">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-179">Click Save.</span></span>
48. <span data-ttu-id="c83dc-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-180">Close the page.</span></span>
49. <span data-ttu-id="c83dc-181">Spustelėkite lauko Surinktų duomenų rakto reikšmė mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="c83dc-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="c83dc-182">Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="c83dc-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="c83dc-183">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-183">Click Save.</span></span>
52. <span data-ttu-id="c83dc-184">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-184">Close the page.</span></span>
    * <span data-ttu-id="c83dc-185">Suskaičiuokite šios sekos eilutes.</span><span class="sxs-lookup"><span data-stu-id="c83dc-185">Count the lines of this sequence.</span></span> <span data-ttu-id="c83dc-186">Rezultatai, pavadinimu „įrašas“, bus atskirai naudojami skirtingiems prekių kodams.</span><span class="sxs-lookup"><span data-stu-id="c83dc-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="c83dc-187">Tai gali būti laikoma virtualia „Excel“ skaičiuokle.</span><span class="sxs-lookup"><span data-stu-id="c83dc-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="c83dc-188">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis, pavadinimu „blokas“, užpildytas atitinkamomis reikšmėmis Importuoti ir Eksportuoti, o antrasis blokas, pavadinimu „įrašas“, užpildytas prekės kodo reikšme.</span><span class="sxs-lookup"><span data-stu-id="c83dc-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="c83dc-189">Medyje pasirinkite Intrastat\Data: Sequence\Dispatches?.</span><span class="sxs-lookup"><span data-stu-id="c83dc-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="c83dc-190">Spustelėkite lauko Surinktų duomenų rakto pavadinimas mygtuką Redaguoti</span><span class="sxs-lookup"><span data-stu-id="c83dc-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="c83dc-191">Medyje pasirinkite $RecName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="c83dc-192">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-192">Click Add data source.</span></span>
57. <span data-ttu-id="c83dc-193">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-193">Click Save.</span></span>
58. <span data-ttu-id="c83dc-194">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-194">Close the page.</span></span>
59. <span data-ttu-id="c83dc-195">Spustelėkite lauko Surinktų duomenų rakto reikšmė mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="c83dc-196">Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="c83dc-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="c83dc-197">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-197">Click Save.</span></span>
62. <span data-ttu-id="c83dc-198">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-198">Close the page.</span></span>
63. <span data-ttu-id="c83dc-199">Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?.</span><span class="sxs-lookup"><span data-stu-id="c83dc-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="c83dc-200">Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="c83dc-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="c83dc-201">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="c83dc-201">Click the Format tab.</span></span>
66. <span data-ttu-id="c83dc-202">Medyje pasirinkite Intrastat\Data\Dispatches\Record\Invoice amount EUR.</span><span class="sxs-lookup"><span data-stu-id="c83dc-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="c83dc-203">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="c83dc-204">Spustelėkite lauko Surinktų duomenų rakto pavadinimas mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="c83dc-205">Medyje pasirinkite $InvName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="c83dc-206">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-206">Click Add data source.</span></span>
71. <span data-ttu-id="c83dc-207">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-207">Click Save.</span></span>
72. <span data-ttu-id="c83dc-208">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-208">Close the page.</span></span>
    * <span data-ttu-id="c83dc-209">Susumuokite šios sekos eilučių SF sumos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c83dc-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="c83dc-210">Rezultatai, pavadinimu „InvoicedAmountEUR“, bus naudojami skirtingoms „Intrastat“ kryptims ir prekių kodams.</span><span class="sxs-lookup"><span data-stu-id="c83dc-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="c83dc-211">Tai gali būti laikoma virtualiai sukurtu elementu „Excel“ skaičiuoklėje.</span><span class="sxs-lookup"><span data-stu-id="c83dc-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="c83dc-212">Kiekvienos operacijos eilutė, kurios pirmasis stulpelis, pavadinimu „blokas“, bus užpildytas atitinkamomis reikšmėmis Importuoti ir Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="c83dc-213">Antrasis blokas, pavadinimu „įrašas“, užpildomas prekės kodo reikšme, o trečiasis stulpelis, pavadinimu „InvoicedAmountEUR“, užpildomas SF sumos reikšme.</span><span class="sxs-lookup"><span data-stu-id="c83dc-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="c83dc-214">Medyje išplėskite dalį Intrastat\Data\Arrivals?.</span><span class="sxs-lookup"><span data-stu-id="c83dc-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="c83dc-215">Medyje išplėskite dalį Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="c83dc-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="c83dc-216">Spustelėkite skirtuką Formatas.</span><span class="sxs-lookup"><span data-stu-id="c83dc-216">Click the Format tab.</span></span>
76. <span data-ttu-id="c83dc-217">Medyje pasirinkite Intrastat\Data\Arrivals\Record\Invoice amount EUR.</span><span class="sxs-lookup"><span data-stu-id="c83dc-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="c83dc-218">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="c83dc-219">Spustelėkite lauko Surinktų duomenų rakto pavadinimas mygtuką Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="c83dc-220">Medyje pasirinkite $InvName.</span><span class="sxs-lookup"><span data-stu-id="c83dc-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="c83dc-221">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="c83dc-221">Click Add data source.</span></span>
81. <span data-ttu-id="c83dc-222">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-222">Click Save.</span></span>
82. <span data-ttu-id="c83dc-223">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-223">Close the page.</span></span>
83. <span data-ttu-id="c83dc-224">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c83dc-224">Click Save.</span></span>
84. <span data-ttu-id="c83dc-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c83dc-225">Close the page.</span></span>


