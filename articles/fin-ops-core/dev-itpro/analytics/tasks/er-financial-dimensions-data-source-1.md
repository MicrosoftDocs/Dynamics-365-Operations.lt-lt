---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (1 dalis)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570197"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="761ad-104">ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)</span><span class="sxs-lookup"><span data-stu-id="761ad-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="761ad-105">Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="761ad-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="761ad-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="761ad-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="761ad-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="761ad-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="761ad-108">Naujo duomenų modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="761ad-108">Create a new data model</span></span>
1. <span data-ttu-id="761ad-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="761ad-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="761ad-110">Įsitikinkite, kad „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="761ad-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="761ad-111">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="761ad-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="761ad-112">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="761ad-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="761ad-113">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="761ad-114">Lauke Pavadinimas įveskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="761ad-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="761ad-115">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="761ad-115">Click Create configuration.</span></span>
6. <span data-ttu-id="761ad-116">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="761ad-116">Click Designer.</span></span>
7. <span data-ttu-id="761ad-117">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="761ad-118">Lauke Pavadinimas įveskite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="761ad-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="761ad-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-119">Click Add.</span></span>
10. <span data-ttu-id="761ad-120">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="761ad-121">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="761ad-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="761ad-122">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-122">Click Add.</span></span>
    * <span data-ttu-id="761ad-123">Įtrauksime mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="761ad-123">We will add to our model a new record list.</span></span> <span data-ttu-id="761ad-124">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų parametrai.</span><span class="sxs-lookup"><span data-stu-id="761ad-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="761ad-125">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos parametrą.</span><span class="sxs-lookup"><span data-stu-id="761ad-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="761ad-126">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="761ad-127">Lauke Pavadinimas įveskite Dimensijos parametras.</span><span class="sxs-lookup"><span data-stu-id="761ad-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="761ad-128">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="761ad-129">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-129">Click Add.</span></span>
17. <span data-ttu-id="761ad-130">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="761ad-131">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="761ad-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="761ad-132">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="761ad-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="761ad-133">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-133">Click Add.</span></span>
21. <span data-ttu-id="761ad-134">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="761ad-135">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="761ad-136">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-136">Click Add.</span></span>
24. <span data-ttu-id="761ad-137">Medyje pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="761ad-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="761ad-138">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="761ad-139">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="761ad-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="761ad-140">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="761ad-141">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-141">Click Add.</span></span>
29. <span data-ttu-id="761ad-142">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="761ad-143">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="761ad-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="761ad-144">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="761ad-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="761ad-145">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-145">Click Add.</span></span>
33. <span data-ttu-id="761ad-146">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="761ad-147">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="761ad-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="761ad-148">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="761ad-149">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-149">Click Add.</span></span>
37. <span data-ttu-id="761ad-150">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="761ad-151">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="761ad-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="761ad-152">Lauke „Prekės tipas“ pasirinkite „Data“.</span><span class="sxs-lookup"><span data-stu-id="761ad-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="761ad-153">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-153">Click Add.</span></span>
41. <span data-ttu-id="761ad-154">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="761ad-155">Lauke Pavadinimas įveskite Debetas.</span><span class="sxs-lookup"><span data-stu-id="761ad-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="761ad-156">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="761ad-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="761ad-157">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-157">Click Add.</span></span>
45. <span data-ttu-id="761ad-158">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="761ad-159">Lauke Pavadinimas įveskite Kreditas.</span><span class="sxs-lookup"><span data-stu-id="761ad-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="761ad-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-160">Click Add.</span></span>
48. <span data-ttu-id="761ad-161">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="761ad-162">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="761ad-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="761ad-163">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="761ad-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="761ad-164">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-164">Click Add.</span></span>
52. <span data-ttu-id="761ad-165">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="761ad-166">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="761ad-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="761ad-167">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-167">Click Add.</span></span>
55. <span data-ttu-id="761ad-168">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="761ad-169">Lauke Pavadinimas įveskite Dimensijų duomenys.</span><span class="sxs-lookup"><span data-stu-id="761ad-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="761ad-170">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="761ad-171">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-171">Click Add.</span></span>
    * <span data-ttu-id="761ad-172">Įtraukėme mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="761ad-172">We added to our model a new record list.</span></span> <span data-ttu-id="761ad-173">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="761ad-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="761ad-174">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="761ad-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="761ad-175">Dimensijos pavadinimas taip pat bus pateiktas šiame įraše yra laukas, kurį, jei reikia, galima naudoti norint pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="761ad-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="761ad-176">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="761ad-177">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="761ad-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="761ad-178">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="761ad-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="761ad-179">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-179">Click Add.</span></span>
63. <span data-ttu-id="761ad-180">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="761ad-181">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="761ad-182">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-182">Click Add.</span></span>
66. <span data-ttu-id="761ad-183">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="761ad-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="761ad-184">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="761ad-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="761ad-185">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="761ad-185">Click Add.</span></span>
69. <span data-ttu-id="761ad-186">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="761ad-186">Click Save.</span></span>
70. <span data-ttu-id="761ad-187">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="761ad-187">Close the page.</span></span>

![ER duomenų modelio dizaino įrankio puslapis](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]