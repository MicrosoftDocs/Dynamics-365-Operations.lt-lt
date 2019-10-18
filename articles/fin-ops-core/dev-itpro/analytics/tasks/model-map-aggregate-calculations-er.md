---
title: Modelio susiejimo konfigūracijų naudojimas agreguotiems skaičiavimams duomenų bazės lygiu
description: Naudojant šią procedūrą pateikiama informacija apie tai, kaip sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3084882dd4b51f067793b3a7999ce89cda1257d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184605"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="7f6b2-103">Modelio susiejimo konfigūracijų naudojimas agreguotiems skaičiavimams duomenų bazės lygiu</span><span class="sxs-lookup"><span data-stu-id="7f6b2-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f6b2-104">Naudojant šią procedūrą pateikiama informacija apie tai, kaip sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="7f6b2-105">Šioje procedūroje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="7f6b2-106">Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="7f6b2-107">Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="7f6b2-108">Norėdami atlikti šiuos veiksmus, turite užbaigti procedūros „ER pagerina sujungtų skaičiavimų efektyvumą juos atliekant duomenų bazės lygmeniu (1 dalis: Konfigūracijų parengimas)“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="7f6b2-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7f6b2-110">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="7f6b2-111">Medyje pasirinkite „Intrastat model\Intrastat sample mapping“ (Intrastat modelis\Intrastat pavyzdinis susiejimas).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="7f6b2-112">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-112">Click Designer.</span></span>
5. <span data-ttu-id="7f6b2-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-113">Click Designer.</span></span>
6. <span data-ttu-id="7f6b2-114">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="7f6b2-115">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-115">Click Add root.</span></span>
    * <span data-ttu-id="7f6b2-116">Įtraukite naują duomenų šaltinį, apimantį norimus grupuoti įrašus.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="7f6b2-117">Lauke „Pavadinimas“, įveskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="7f6b2-118">Operacijos</span><span class="sxs-lookup"><span data-stu-id="7f6b2-118">Transactions</span></span>  
9. <span data-ttu-id="7f6b2-119">Lauke Lentelė, įveskite „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="7f6b2-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="7f6b2-120">Intrastat</span></span>  
10. <span data-ttu-id="7f6b2-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-121">Click OK.</span></span>
11. <span data-ttu-id="7f6b2-122">Medyje pasirinkite Funkcijos\Grupuoti pagal.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="7f6b2-123">Šis duomenų šaltinio tipas naudojamas norint vykdymo metu į grupės įrašus įtraukti naują duomenų šaltinį ir apskaičiuoti reikiamus telkimus.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="7f6b2-124">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-124">Click Add root.</span></span>
13. <span data-ttu-id="7f6b2-125">Lauke Pavadinimas įveskite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="7f6b2-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="7f6b2-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="7f6b2-127">Spustelėkite Redaguoti grupę pagal.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-127">Click Edit group by.</span></span>
15. <span data-ttu-id="7f6b2-128">Medyje pasirinkite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="7f6b2-129">Pasirinkite norimus grupuoti įrašus apimantį tipo „Įrašų sąrašas“ įtrauktą dumenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="7f6b2-130">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-130">Click Add field to.</span></span>
17. <span data-ttu-id="7f6b2-131">Spustelėkite Ką grupuoti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-131">Click What to group.</span></span>
18. <span data-ttu-id="7f6b2-132">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="7f6b2-133">Medyje pasirinkite „Operacijos\Kryptis“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="7f6b2-134">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-134">Click Add field to.</span></span>
21. <span data-ttu-id="7f6b2-135">Spustelėkite Sugrupuoti laukai.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="7f6b2-136">Pasirinkę lauką nurodykite grupavimo lygį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="7f6b2-137">Pagal šią pasirinktį, duomenų šaltinis vykdymo metu grąžina tiek operacijų grupių, kiek yra Intrastat lentelėje sutinkamų krypčių kodų.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="7f6b2-138">Medyje pasirinkite „Operacijos\SF suma(MSTSuma)“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="7f6b2-139">Pasirinkite lauką, kad galėtumėte nurodyti telkimo skaičiavimo šaltinį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="7f6b2-140">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-140">Click Add field to.</span></span>
24. <span data-ttu-id="7f6b2-141">Spustelėkite Telkimo laukai.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="7f6b2-142">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="7f6b2-143">Lauke Metodas pasirinkite „Sum“ (suma).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="7f6b2-144">Pasirinkite telkimo tipą.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="7f6b2-145">Lauke Pavadinimas įveskite „SumOfAmountMST“ (bendroji MST suma).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="7f6b2-146">Nurodykite šio telkimo pavadinimą sukonfigūruotame duomenų šaltinyje.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="7f6b2-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-147">Click Save.</span></span>
    * <span data-ttu-id="7f6b2-148">Atkreipkite dėmesį į tai, kad lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo metu SQL duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="7f6b2-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-149">Close the page.</span></span>
30. <span data-ttu-id="7f6b2-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-150">Click OK.</span></span>
31. <span data-ttu-id="7f6b2-151">Medyje išplėskite „Totals“ (bendrosios sumos).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="7f6b2-152">Medyje išplėskite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="7f6b2-153">Medyje išplėskite „OperacijųGrupės\susietos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="7f6b2-154">Medyje pasirinkite „OperacijųGrupės\susietos\BendrojiMSTsuma“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="7f6b2-155">Medyje pasirinkite „Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="7f6b2-156">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-156">Click Bind.</span></span>
    * <span data-ttu-id="7f6b2-157">Pagal šį parametrą šis duomenų šaltinis skaičiuos kiekvienos operacijų grupės lauko „AmountMST“ verčių sumą.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="7f6b2-158">Šis telkimo skaičiavimas bus pasiekiamas kaip elementas TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="7f6b2-159">Medyje išplėskite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="7f6b2-160">Medyje pasirinkite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="7f6b2-161">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-161">Click Edit.</span></span>
40. <span data-ttu-id="7f6b2-162">Spustelėkite Redaguoti grupę pagal.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-162">Click Edit group by.</span></span>
41. <span data-ttu-id="7f6b2-163">Medyje išplėskite „Operacijos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="7f6b2-164">Medyje pasirinkite „Operacijos\SF suma(MSTSuma)“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="7f6b2-165">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-165">Click Add field to.</span></span>
44. <span data-ttu-id="7f6b2-166">Spustelėkite Telkimo laukai.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="7f6b2-167">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="7f6b2-168">Lauke Metodas pasirinkite „Max“ (maksimalus).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="7f6b2-169">Lauke Pavadinimas įveskite „MaxOfAmountMST“ (maksimali MST suma).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="7f6b2-170">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-170">Click Save.</span></span>
    * <span data-ttu-id="7f6b2-171">Šiuo metu GROUPBY duomenų šaltinių vykdymas gali būti konvertuotas į SQL duomenų bazės lygį taikant tam tikrus apribojimus.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="7f6b2-172">Galima atlikti tipo „Įrašų sąrašas“ duomenų šaltinių arba kaip išraiška pateikiamų duomenų šaltinių konvertavimą naudojant funkciją FILTER (filtras).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="7f6b2-173">Tai taip pat galima atlikti, kai sukonfigūruotas tik vienas vieno grupavimo įrašų lauko telkimas.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="7f6b2-174">Atkreipkite dėmesį į tai, kad, nors sukonfigūruotas daugiau nei vienas lauko AmountMST telkimas, lauke „Vykdymas“ vis tiek nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku SQL duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="7f6b2-175">Taip yra todėl, kad su duomenų modelio elementu susietas tik vienas telkimas, kuris bus naudojamas vykdymo laiku norint ištraukti duomenis iš šio duomenų šaltinio.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="7f6b2-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-176">Close the page.</span></span>
50. <span data-ttu-id="7f6b2-177">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-177">Click OK.</span></span>
51. <span data-ttu-id="7f6b2-178">Medyje išplėskite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="7f6b2-179">Medyje išplėskite „OperacijųGrupės\susietos“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="7f6b2-180">Medyje pasirinkite „TransactionsGroups\aggregated\MaxOfAmountMST“ (operacijų grupės\susietos\maksimali MST suma).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="7f6b2-181">Medyje pasirinkite „Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="7f6b2-182">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-182">Click Bind.</span></span>
56. <span data-ttu-id="7f6b2-183">Medyje išplėskite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="7f6b2-184">Medyje pasirinkite „TransactionsGroups“ (operacijų grupės).</span><span class="sxs-lookup"><span data-stu-id="7f6b2-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="7f6b2-185">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-185">Click Edit.</span></span>
59. <span data-ttu-id="7f6b2-186">Spustelėkite Redaguoti grupę pagal.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-186">Click Edit group by.</span></span>
    * <span data-ttu-id="7f6b2-187">Atkreipkite dėmesį į tai, lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku atmintyje, nes abu to paties lauko telkimai susieti su duomenų modelio elementais.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="7f6b2-188">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="7f6b2-189">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-189">Click Delete.</span></span>
62. <span data-ttu-id="7f6b2-190">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-190">Click Yes.</span></span>
63. <span data-ttu-id="7f6b2-191">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-191">Click Delete.</span></span>
64. <span data-ttu-id="7f6b2-192">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-192">Click Yes.</span></span>
65. <span data-ttu-id="7f6b2-193">Spustelėkite Įtraukti lauką į.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-193">Click Add field to.</span></span>
66. <span data-ttu-id="7f6b2-194">Spustelėkite Ką grupuoti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-194">Click What to group.</span></span>
67. <span data-ttu-id="7f6b2-195">Medyje išplėskite „Commodity record(Intrastat)“.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="7f6b2-196">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-196">Click Save.</span></span>
    * <span data-ttu-id="7f6b2-197">Atkreipkite dėmesį į tai, kad lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku atmintyje, nors nėra nurodytų telkimų, o pasirinktas tipo „Lentelės įrašai“ duomenų šaltinis paremtas ta pačia „Intrastat“ lentele.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="7f6b2-198">Taip yra todėl, kad duomenų šaltinyje yra keletas apskaičiuotų laukų, kurie dar negali būti konvertuoti į SQL duomenų bazės lygį.</span><span class="sxs-lookup"><span data-stu-id="7f6b2-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

