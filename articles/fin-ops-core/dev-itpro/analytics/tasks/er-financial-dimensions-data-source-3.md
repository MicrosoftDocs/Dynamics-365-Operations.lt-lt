---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis – Ataskaitos kūrimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (3 dalis)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092305"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="a7849-104">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis – Ataskaitos kūrimas)</span><span class="sxs-lookup"><span data-stu-id="a7849-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7849-105">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="a7849-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a7849-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="a7849-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a7849-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis. Modelio susiejimas)“.</span><span class="sxs-lookup"><span data-stu-id="a7849-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a7849-108">Ataskaitos kūrimas finansinėms dimensijoms pateikti</span><span class="sxs-lookup"><span data-stu-id="a7849-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a7849-109">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a7849-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a7849-110">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a7849-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a7849-111">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a7849-112">Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a7849-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a7849-113">Naudokite modelį, kuris buvo iš anksto sukurtas kaip naujos ataskaitos duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="a7849-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a7849-114">Lauke Pavadinimas, įveskite DK žurnalo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="a7849-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a7849-115">Lauke Duomenų modelio aprašas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="a7849-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a7849-116">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="a7849-116">Click Create configuration.</span></span>
8. <span data-ttu-id="a7849-117">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="a7849-117">Click Designer.</span></span>
9. <span data-ttu-id="a7849-118">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a7849-119">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a7849-120">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="a7849-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a7849-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-121">Click OK.</span></span>
13. <span data-ttu-id="a7849-122">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a7849-123">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a7849-124">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="a7849-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a7849-125">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-125">Click OK.</span></span>
17. <span data-ttu-id="a7849-126">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a7849-127">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a7849-128">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="a7849-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a7849-129">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-129">Click OK.</span></span>
21. <span data-ttu-id="a7849-130">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a7849-131">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a7849-132">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a7849-133">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="a7849-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a7849-134">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-134">Click OK.</span></span>
26. <span data-ttu-id="a7849-135">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a7849-136">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a7849-137">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="a7849-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a7849-138">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-138">Click OK.</span></span>
30. <span data-ttu-id="a7849-139">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a7849-140">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a7849-141">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a7849-142">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="a7849-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a7849-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-143">Click OK.</span></span>
35. <span data-ttu-id="a7849-144">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="a7849-145">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="a7849-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a7849-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-146">Click OK.</span></span>
38. <span data-ttu-id="a7849-147">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="a7849-148">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="a7849-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a7849-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-149">Click OK.</span></span>
41. <span data-ttu-id="a7849-150">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="a7849-151">Lauke Pavadinimas Dt.</span><span class="sxs-lookup"><span data-stu-id="a7849-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a7849-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-152">Click OK.</span></span>
44. <span data-ttu-id="a7849-153">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="a7849-154">Lauke Pavadinimas įveskite Ct.</span><span class="sxs-lookup"><span data-stu-id="a7849-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a7849-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-155">Click OK.</span></span>
47. <span data-ttu-id="a7849-156">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a7849-157">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a7849-158">Lauke Pavadinimas įveskite Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="a7849-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a7849-159">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-159">Click OK.</span></span>
51. <span data-ttu-id="a7849-160">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a7849-161">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a7849-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a7849-162">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a7849-163">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="a7849-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a7849-164">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-164">Click OK.</span></span>
56. <span data-ttu-id="a7849-165">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="a7849-166">Lauke Pavadinimas įveskite Reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a7849-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a7849-167">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a7849-167">Click OK.</span></span>
59. <span data-ttu-id="a7849-168">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="a7849-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="a7849-169">Lauke Pavadinimas įveskite Aprašas.</span><span class="sxs-lookup"><span data-stu-id="a7849-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a7849-170">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a7849-170">Click OK.</span></span>
<span data-ttu-id="a7849-171">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="a7849-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a7849-172">Ataskaitos elementų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="a7849-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="a7849-173">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="a7849-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a7849-174">Medyje išplėskite dalį model: Data model Financial dimensions sample model.</span><span class="sxs-lookup"><span data-stu-id="a7849-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a7849-175">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a7849-176">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a7849-177">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a7849-178">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a7849-179">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a7849-180">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-180">Click Bind.</span></span>
9. <span data-ttu-id="a7849-181">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a7849-182">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a7849-183">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-183">Click Bind.</span></span>
12. <span data-ttu-id="a7849-184">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a7849-185">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a7849-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-186">Click Bind.</span></span>
15. <span data-ttu-id="a7849-187">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a7849-188">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a7849-189">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-189">Click Bind.</span></span>
18. <span data-ttu-id="a7849-190">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a7849-191">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.</span><span class="sxs-lookup"><span data-stu-id="a7849-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a7849-192">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-192">Click Bind.</span></span>
21. <span data-ttu-id="a7849-193">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a7849-194">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.</span><span class="sxs-lookup"><span data-stu-id="a7849-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a7849-195">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-195">Click Bind.</span></span>
24. <span data-ttu-id="a7849-196">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a7849-197">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a7849-198">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-198">Click Bind.</span></span>
27. <span data-ttu-id="a7849-199">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a7849-200">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.</span><span class="sxs-lookup"><span data-stu-id="a7849-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a7849-201">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-201">Click Bind.</span></span>
30. <span data-ttu-id="a7849-202">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a7849-203">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a7849-204">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-204">Click Bind.</span></span>
33. <span data-ttu-id="a7849-205">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a7849-206">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a7849-207">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-207">Click Bind.</span></span>
36. <span data-ttu-id="a7849-208">Medyje pasirinkite Root: XML Element\Journal: XML Element\Batch: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a7849-209">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a7849-210">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-210">Click Bind.</span></span>
39. <span data-ttu-id="a7849-211">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="a7849-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a7849-212">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="a7849-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a7849-213">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-213">Click Bind.</span></span>
42. <span data-ttu-id="a7849-214">Medyje pasirinkite Root: XML Element\Company: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="a7849-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a7849-215">Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.</span><span class="sxs-lookup"><span data-stu-id="a7849-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a7849-216">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="a7849-216">Click Bind.</span></span>
45. <span data-ttu-id="a7849-217">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a7849-217">Click Save.</span></span>
46. <span data-ttu-id="a7849-218">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a7849-218">Close the page.</span></span>
<span data-ttu-id="a7849-219">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="a7849-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

