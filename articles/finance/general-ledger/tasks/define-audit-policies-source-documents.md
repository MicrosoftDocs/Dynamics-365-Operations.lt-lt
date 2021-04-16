---
title: Šaltinio dokumentų audito strategijų apibrėžimas
description: Šioje temoje aiškinama, kaip konfigūruoti ir vykdyti audito strategijų taisykles.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836966"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="c4057-103">Šaltinio dokumentų audito strategijų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="c4057-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4057-104">Šioje temoje aiškinama, kaip konfigūruoti ir vykdyti audito strategijų taisykles.</span><span class="sxs-lookup"><span data-stu-id="c4057-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="c4057-105">Pavyzdyje naudojamos viešbučio tipo išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="c4057-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="c4057-106">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="c4057-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="c4057-107">Kad būtų galima atlikti šias užduotis, auditoriaus vaidmenį sudaro tinkamos teisės.</span><span class="sxs-lookup"><span data-stu-id="c4057-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="c4057-108">Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Konfigūravimas > Strategijos taisyklės tipas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="c4057-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-109">Select **New**.</span></span>
3. <span data-ttu-id="c4057-110">Lauke **Taisyklės pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="c4057-111">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c4057-112">Lauke **Užklausos pavadinimas** pasirinkite **Išlaidų ataskaitos eilutė**</span><span class="sxs-lookup"><span data-stu-id="c4057-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="c4057-113">Lauke **Užklausos tipas** pasirinkite **Agregavimas**</span><span class="sxs-lookup"><span data-stu-id="c4057-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="c4057-114">Lauke **Juridinis subjektas** pasirinkite **Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="c4057-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="c4057-115">Lauke **Dokumento datos nuoroda** pasirinkite **Modifikavimo data ir laikas**</span><span class="sxs-lookup"><span data-stu-id="c4057-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="c4057-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-116">Select **Save**.</span></span>
10. <span data-ttu-id="c4057-117">Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Konfigūravimas > Audito strategijos**.</span><span class="sxs-lookup"><span data-stu-id="c4057-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="c4057-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-118">Select **New**.</span></span>
12. <span data-ttu-id="c4057-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="c4057-120">Išplėskite skyrių **Organizacijų strategijos**.</span><span class="sxs-lookup"><span data-stu-id="c4057-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="c4057-121">Medyje pasirinkite **„Contoso Entertainment System“, JAV**, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="c4057-122">Medyje pasirinkite **„Contoso Consulting“, JAV**, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="c4057-123">Medyje pasirinkite **„Contoso Retail“, JAV**, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="c4057-124">Sutraukite skyrių **Organizacijų strategijos**.</span><span class="sxs-lookup"><span data-stu-id="c4057-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="c4057-125">Išplėskite skyrių **Strategijų taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="c4057-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="c4057-126">Sąraše raskite ir pasirinkite anksčiau sukurtą strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="c4057-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="c4057-127">Pasirinkite **Kurti strategijos taisyklę**.</span><span class="sxs-lookup"><span data-stu-id="c4057-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="c4057-128">Lauke **Įsigaliojimo data** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c4057-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="c4057-129">Pasirinkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="c4057-129">Select **Filter**.</span></span>
23. <span data-ttu-id="c4057-130">Sąraše pasirinkite eilutę parinkčiai **Išlaidų kategorija** ir nustatykite išsamią informaciją į **Viešbutis**.</span><span class="sxs-lookup"><span data-stu-id="c4057-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="c4057-131">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="c4057-132">Pasirinkite skirtuką **Agregavimas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="c4057-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-133">Select **Add**.</span></span>
27. <span data-ttu-id="c4057-134">Sąraše pasirinkite parinkties **Operacijos suma** lauko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="c4057-135">Lauke **Laukas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="c4057-136">Lauke **AggregateFunction** pasirinkite **Suma**.</span><span class="sxs-lookup"><span data-stu-id="c4057-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="c4057-137">Pasirinkite skirtuką **Grupuoti pagal**.</span><span class="sxs-lookup"><span data-stu-id="c4057-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="c4057-138">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-138">Select **Add**.</span></span>
32. <span data-ttu-id="c4057-139">Sąraše pasirinkite reikšmę parinkčiai **Darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="c4057-140">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-140">Select **Add**.</span></span>
34. <span data-ttu-id="c4057-141">Sąraše pasirinkite reikšmę parinkčiai **Išlaidų kategorija**.</span><span class="sxs-lookup"><span data-stu-id="c4057-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="c4057-142">Lauke **Laukas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="c4057-143">Pažymėkite skirtuką **Having**.</span><span class="sxs-lookup"><span data-stu-id="c4057-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="c4057-144">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-144">Select **Add**.</span></span>
38. <span data-ttu-id="c4057-145">Pasirinkite **Operacijos suma**.</span><span class="sxs-lookup"><span data-stu-id="c4057-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="c4057-146">Lauke **Laukas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c4057-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="c4057-147">Lauke **AggregateFunction** pasirinkite **Suma**.</span><span class="sxs-lookup"><span data-stu-id="c4057-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="c4057-148">Lauke **Kriterijai** įveskite `>2000`.</span><span class="sxs-lookup"><span data-stu-id="c4057-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="c4057-149">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c4057-149">Select **OK**.</span></span>
43. <span data-ttu-id="c4057-150">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="c4057-150">Select **Test**.</span></span>
44. <span data-ttu-id="c4057-151">Lauke **Dokumento žymėjimo pradžios data** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c4057-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="c4057-152">Lauke **Dokumento žymėjimo pabaigos data** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c4057-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="c4057-153">Pasirinkite **Paleisti tikrinimą**.</span><span class="sxs-lookup"><span data-stu-id="c4057-153">Select **Run test**.</span></span>
47. <span data-ttu-id="c4057-154">Veiksmų srityje pasirinkite **Audito strategija**.</span><span class="sxs-lookup"><span data-stu-id="c4057-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="c4057-155">Pasirinkite **Papildomos parinktys**.</span><span class="sxs-lookup"><span data-stu-id="c4057-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="c4057-156">Lauke **Pradžios data** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c4057-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="c4057-157">Lauke **Pabaigos data** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c4057-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="c4057-158">Pasirinkite **Paketas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-158">Select **Batch**.</span></span>
52. <span data-ttu-id="c4057-159">Išplėskite skyrių **Vykdyti fone**.</span><span class="sxs-lookup"><span data-stu-id="c4057-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="c4057-160">Pasirinkite **Taip** lauke **Paketinis vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="c4057-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="c4057-161">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c4057-161">Select **OK**.</span></span>
55. <span data-ttu-id="c4057-162">Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Audito atvejai**.</span><span class="sxs-lookup"><span data-stu-id="c4057-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="c4057-163">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c4057-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="c4057-164">Išplėskite skyrių **Sąsajos**.</span><span class="sxs-lookup"><span data-stu-id="c4057-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="c4057-165">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c4057-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]