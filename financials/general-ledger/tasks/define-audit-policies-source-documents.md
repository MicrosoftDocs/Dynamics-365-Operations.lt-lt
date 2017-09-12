--- 
title: "Apibrėžti šaltinio dokumento audito strategijas"
description: "Ši procedūra parodo, kaip nustatyti ir vykdyti audito strategijos taisykles."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="7b7c5-103">Apibrėžti šaltinio dokumento audito strategijas</span><span class="sxs-lookup"><span data-stu-id="7b7c5-103">Define audit policies for source documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b7c5-104">Ši procedūra parodo, kaip nustatyti ir vykdyti audito strategijos taisykles.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="7b7c5-105">Pavyzdyje naudojamos viešbučio tipo išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="7b7c5-106">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="7b7c5-107">Kad būtų galima atlikti šias užduotis, auditoriaus vaidmenį sudaro tinkamos teisės.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="7b7c5-108">Eikite į dalį Audito darbo sritis > Nustatymas > Strategijos taisyklės tipas.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="7b7c5-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-109">Click New.</span></span>
3. <span data-ttu-id="7b7c5-110">Lauke Taisyklės pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="7b7c5-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b7c5-112">Lauke Užklausos pavadinimas pasirinkite Išlaidų ataskaitos eilutė</span><span class="sxs-lookup"><span data-stu-id="7b7c5-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="7b7c5-113">Užklausos tipo lauke pasirinkite Sudėtinė.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="7b7c5-114">Lauke Juridinis subjektas pasirinkite juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="7b7c5-115">Lauke Dokumento datos nuoroda pasirinkite Modifikavimo data ir laikas</span><span class="sxs-lookup"><span data-stu-id="7b7c5-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="7b7c5-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-116">Click Save.</span></span>
10. <span data-ttu-id="7b7c5-117">Eikite į dalį Audito darbo sritis > Nustatymas > Audito strategijos.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="7b7c5-118">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-118">Click New.</span></span>
12. <span data-ttu-id="7b7c5-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="7b7c5-120">Išplėskite dalį Strategijos organizacijos.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="7b7c5-121">Medyje pasirinkite „Contoso Entertainment System USA‟.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="7b7c5-122">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-122">Click Add.</span></span>
16. <span data-ttu-id="7b7c5-123">Medyje pasirinkite „Contoso Consulting USA‟.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="7b7c5-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-124">Click Add.</span></span>
18. <span data-ttu-id="7b7c5-125">Medyje pasirinkite „Contoso Retail USA‟.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="7b7c5-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-126">Click Add.</span></span>
20. <span data-ttu-id="7b7c5-127">Sutraukite dalį Strategijos organizacijos.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="7b7c5-128">Išplėskite dalį Strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="7b7c5-129">Sąraše raskite ir pasirinkite anksčiau sukurtą strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="7b7c5-130">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="7b7c5-131">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="7b7c5-132">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-132">Click Filter.</span></span>
26. <span data-ttu-id="7b7c5-133">Sąraše pasirinkite eilutę Išlaidų kategorija ir informaciją nustatykite į Viešbutis</span><span class="sxs-lookup"><span data-stu-id="7b7c5-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="7b7c5-134">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="7b7c5-135">Spustelėkite skirtuką Sudėtin.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="7b7c5-136">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-136">Click Add.</span></span>
30. <span data-ttu-id="7b7c5-137">Sąraše pasirinkite lauko reikšmę Operacijos suma</span><span class="sxs-lookup"><span data-stu-id="7b7c5-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="7b7c5-138">Lauke Laukas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="7b7c5-139">Lauke Sudėtinė funkcija pasirinkite „Suma‟.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="7b7c5-140">Spustelėkite skirtuką Grupuoti pagal.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="7b7c5-141">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-141">Click Add.</span></span>
35. <span data-ttu-id="7b7c5-142">Sąraše pasirinkite darbuotojo reikšmę </span><span class="sxs-lookup"><span data-stu-id="7b7c5-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="7b7c5-143">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-143">Click Add.</span></span>
37. <span data-ttu-id="7b7c5-144">Sąraše pasirinkite išlaidų kategorijos reikšmę</span><span class="sxs-lookup"><span data-stu-id="7b7c5-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="7b7c5-145">Lauke Laukas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="7b7c5-146">Spustelėkite skirtuką Turi.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-146">Click the Having tab.</span></span>
40. <span data-ttu-id="7b7c5-147">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-147">Click Add.</span></span>
41. <span data-ttu-id="7b7c5-148">Pasirinkite Operacijos suma</span><span class="sxs-lookup"><span data-stu-id="7b7c5-148">Select Transaction amount</span></span>
42. <span data-ttu-id="7b7c5-149">Lauke Laukas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="7b7c5-150">Lauke Sudėtinė funkcija pasirinkite „Suma‟.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="7b7c5-151">Lauke Kriterijai įveskite „>2000“.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="7b7c5-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-152">Click OK.</span></span>
46. <span data-ttu-id="7b7c5-153">Spustelėkite Išbandyti.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-153">Click Test.</span></span>
47. <span data-ttu-id="7b7c5-154">Lauke Dokumentų pasirinkimo pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="7b7c5-155">Lauke Dokumentų pasirinkimo pabaigos data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="7b7c5-156">Spustelėkite Vykdyti testą.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-156">Click Run test.</span></span>
50. <span data-ttu-id="7b7c5-157">Veiksmų srityje spustelėkite Audito strategija.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="7b7c5-158">Spustelėkite Papildomos parinktys.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-158">Click Additional options.</span></span>
52. <span data-ttu-id="7b7c5-159">Lauke Pradžios data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="7b7c5-160">Lauke Pabaigos data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="7b7c5-161">Spustelėkite Paketas.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-161">Click Batch.</span></span>
55. <span data-ttu-id="7b7c5-162">Išplėskite dalį Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="7b7c5-163">Lauke Paketinis vykdymas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="7b7c5-164">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-164">Click OK.</span></span>
58. <span data-ttu-id="7b7c5-165">Eikite į dalį Audito darbo sritis > Audito atvejai.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="7b7c5-166">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="7b7c5-167">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="7b7c5-168">Išplėskite dalį Susiejimai.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="7b7c5-169">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="7b7c5-170">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7b7c5-170">In the list, click the link in the selected row.</span></span>


