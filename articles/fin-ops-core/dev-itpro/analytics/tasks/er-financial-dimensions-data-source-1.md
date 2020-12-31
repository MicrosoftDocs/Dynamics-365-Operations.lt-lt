---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)
description: Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35c4a05fb15a7e3166c6d075569debcf9cbc3cc3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681714"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="9ed93-103">ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)</span><span class="sxs-lookup"><span data-stu-id="9ed93-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9ed93-104">Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="9ed93-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9ed93-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="9ed93-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9ed93-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="9ed93-107">Naujo duomenų modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="9ed93-107">Create a new data model</span></span>
1. <span data-ttu-id="9ed93-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="9ed93-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9ed93-109">Įsitikinkite, kad „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="9ed93-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="9ed93-110">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="9ed93-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="9ed93-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="9ed93-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9ed93-112">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="9ed93-113">Lauke Pavadinimas įveskite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9ed93-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="9ed93-114">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9ed93-114">Click Create configuration.</span></span>
6. <span data-ttu-id="9ed93-115">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="9ed93-115">Click Designer.</span></span>
7. <span data-ttu-id="9ed93-116">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9ed93-117">Lauke Pavadinimas įveskite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="9ed93-118">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-118">Click Add.</span></span>
10. <span data-ttu-id="9ed93-119">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="9ed93-120">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="9ed93-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-121">Click Add.</span></span>
    * <span data-ttu-id="9ed93-122">Įtrauksime mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-122">We will add to our model a new record list.</span></span> <span data-ttu-id="9ed93-123">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų parametrai.</span><span class="sxs-lookup"><span data-stu-id="9ed93-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="9ed93-124">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos parametrą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="9ed93-125">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="9ed93-126">Lauke Pavadinimas įveskite Dimensijos parametras.</span><span class="sxs-lookup"><span data-stu-id="9ed93-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="9ed93-127">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="9ed93-128">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-128">Click Add.</span></span>
17. <span data-ttu-id="9ed93-129">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="9ed93-130">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="9ed93-131">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="9ed93-132">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-132">Click Add.</span></span>
21. <span data-ttu-id="9ed93-133">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9ed93-134">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="9ed93-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-135">Click Add.</span></span>
24. <span data-ttu-id="9ed93-136">Medyje pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="9ed93-137">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="9ed93-138">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="9ed93-139">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="9ed93-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-140">Click Add.</span></span>
29. <span data-ttu-id="9ed93-141">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="9ed93-142">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="9ed93-143">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="9ed93-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-144">Click Add.</span></span>
33. <span data-ttu-id="9ed93-145">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="9ed93-146">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="9ed93-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="9ed93-147">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="9ed93-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-148">Click Add.</span></span>
37. <span data-ttu-id="9ed93-149">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="9ed93-150">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="9ed93-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="9ed93-151">Lauke „Prekės tipas“ pasirinkite „Data“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="9ed93-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-152">Click Add.</span></span>
41. <span data-ttu-id="9ed93-153">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="9ed93-154">Lauke Pavadinimas įveskite Debetas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="9ed93-155">Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="9ed93-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-156">Click Add.</span></span>
45. <span data-ttu-id="9ed93-157">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="9ed93-158">Lauke Pavadinimas įveskite Kreditas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="9ed93-159">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-159">Click Add.</span></span>
48. <span data-ttu-id="9ed93-160">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="9ed93-161">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="9ed93-162">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="9ed93-163">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-163">Click Add.</span></span>
52. <span data-ttu-id="9ed93-164">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="9ed93-165">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="9ed93-166">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-166">Click Add.</span></span>
55. <span data-ttu-id="9ed93-167">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="9ed93-168">Lauke Pavadinimas įveskite Dimensijų duomenys.</span><span class="sxs-lookup"><span data-stu-id="9ed93-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="9ed93-169">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="9ed93-170">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-170">Click Add.</span></span>
    * <span data-ttu-id="9ed93-171">Įtraukėme mūsų modelį į naują įrašų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-171">We added to our model a new record list.</span></span> <span data-ttu-id="9ed93-172">Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų reikšmės.</span><span class="sxs-lookup"><span data-stu-id="9ed93-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="9ed93-173">Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9ed93-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="9ed93-174">Dimensijos pavadinimas taip pat bus pateiktas šiame įraše yra laukas, kurį, jei reikia, galima naudoti norint pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="9ed93-175">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="9ed93-176">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="9ed93-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="9ed93-177">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="9ed93-178">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-178">Click Add.</span></span>
63. <span data-ttu-id="9ed93-179">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="9ed93-180">Lauke „Pavadinimas“, įveskite „Aprašas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="9ed93-181">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-181">Click Add.</span></span>
66. <span data-ttu-id="9ed93-182">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9ed93-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="9ed93-183">Lauke „Pavadinimas“ įveskite „Agentas“.</span><span class="sxs-lookup"><span data-stu-id="9ed93-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="9ed93-184">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-184">Click Add.</span></span>
69. <span data-ttu-id="9ed93-185">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-185">Click Save.</span></span>
70. <span data-ttu-id="9ed93-186">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9ed93-186">Close the page.</span></span>

![ER duomenų modelio dizaino įrankio puslapis](../media/er-financial-dimensions-guides-data-model.png)

