---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)
description: Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84f546b73eefe3ead78c6ab3fdbbc05d0db5fef5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "339515"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="1e298-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (1 dalis: duomenų modelio kūrimas)</span><span class="sxs-lookup"><span data-stu-id="1e298-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e298-104">Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1e298-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="1e298-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="1e298-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1e298-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="1e298-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="1e298-107">Naujo duomenų modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="1e298-107">Create a new data model</span></span>
1. <span data-ttu-id="1e298-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="1e298-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="1e298-109">Įsitikinkite, kad teikėjas „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="1e298-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="1e298-110">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="1e298-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="1e298-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="1e298-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1e298-112">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1e298-113">Lauke Pavadinimas įveskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1e298-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="1e298-114">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1e298-114">Click Create configuration.</span></span>
6. <span data-ttu-id="1e298-115">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="1e298-115">Click Designer.</span></span>
7. <span data-ttu-id="1e298-116">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="1e298-117">Lauke Pavadinimas įveskite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="1e298-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="1e298-118">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-118">Click Add.</span></span>
10. <span data-ttu-id="1e298-119">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="1e298-120">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="1e298-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="1e298-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-121">Click Add.</span></span>
    * <span data-ttu-id="1e298-122">Įtrauksime mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1e298-122">We will add to our model a new record list.</span></span> <span data-ttu-id="1e298-123">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų parametrai.</span><span class="sxs-lookup"><span data-stu-id="1e298-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="1e298-124">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukus, nurodančiais dimensijos parametrą.</span><span class="sxs-lookup"><span data-stu-id="1e298-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="1e298-125">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="1e298-126">Lauke Pavadinimas įveskite Dimensijos parametras.</span><span class="sxs-lookup"><span data-stu-id="1e298-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="1e298-127">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="1e298-128">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-128">Click Add.</span></span>
17. <span data-ttu-id="1e298-129">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="1e298-130">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="1e298-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="1e298-131">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1e298-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="1e298-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-132">Click Add.</span></span>
21. <span data-ttu-id="1e298-133">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="1e298-134">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="1e298-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-135">Click Add.</span></span>
24. <span data-ttu-id="1e298-136">Medyje pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="1e298-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="1e298-137">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="1e298-138">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="1e298-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="1e298-139">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="1e298-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-140">Click Add.</span></span>
29. <span data-ttu-id="1e298-141">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="1e298-142">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="1e298-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="1e298-143">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1e298-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="1e298-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-144">Click Add.</span></span>
33. <span data-ttu-id="1e298-145">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="1e298-146">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="1e298-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="1e298-147">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="1e298-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-148">Click Add.</span></span>
37. <span data-ttu-id="1e298-149">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="1e298-150">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="1e298-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="1e298-151">Lauke „Prekės tipas“ pasirinkite „Data“.</span><span class="sxs-lookup"><span data-stu-id="1e298-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="1e298-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-152">Click Add.</span></span>
41. <span data-ttu-id="1e298-153">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="1e298-154">Lauke Pavadinimas įveskite Debetas.</span><span class="sxs-lookup"><span data-stu-id="1e298-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="1e298-155">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="1e298-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="1e298-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-156">Click Add.</span></span>
45. <span data-ttu-id="1e298-157">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="1e298-158">Lauke Pavadinimas įveskite Kreditas.</span><span class="sxs-lookup"><span data-stu-id="1e298-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="1e298-159">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-159">Click Add.</span></span>
48. <span data-ttu-id="1e298-160">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="1e298-161">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="1e298-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="1e298-162">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1e298-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="1e298-163">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-163">Click Add.</span></span>
52. <span data-ttu-id="1e298-164">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="1e298-165">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="1e298-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="1e298-166">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-166">Click Add.</span></span>
55. <span data-ttu-id="1e298-167">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="1e298-168">Lauke Pavadinimas įveskite Dimensijų duomenys.</span><span class="sxs-lookup"><span data-stu-id="1e298-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="1e298-169">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="1e298-170">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-170">Click Add.</span></span>
    * <span data-ttu-id="1e298-171">Įtraukėme mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1e298-171">We added to our model a new record list.</span></span> <span data-ttu-id="1e298-172">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="1e298-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="1e298-173">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukus, nurodančiais dimensijos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="1e298-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="1e298-174">Dimensijos pavadinimas taip pat bus pateiktas šiame įraše yra laukas, kurį, jei reikia, galima naudoti norint pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="1e298-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="1e298-175">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="1e298-176">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="1e298-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="1e298-177">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="1e298-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="1e298-178">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-178">Click Add.</span></span>
63. <span data-ttu-id="1e298-179">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="1e298-180">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="1e298-181">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-181">Click Add.</span></span>
66. <span data-ttu-id="1e298-182">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1e298-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="1e298-183">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="1e298-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="1e298-184">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="1e298-184">Click Add.</span></span>
69. <span data-ttu-id="1e298-185">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1e298-185">Click Save.</span></span>
70. <span data-ttu-id="1e298-186">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1e298-186">Close the page.</span></span>

