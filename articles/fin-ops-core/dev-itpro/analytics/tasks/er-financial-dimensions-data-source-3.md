---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis – Ataskaitos kūrimas)'
description: Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.
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
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684792"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="5af23-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis – Ataskaitos kūrimas)</span><span class="sxs-lookup"><span data-stu-id="5af23-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5af23-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="5af23-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="5af23-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="5af23-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5af23-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis. Modelio susiejimas)“.</span><span class="sxs-lookup"><span data-stu-id="5af23-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="5af23-107">Ataskaitos kūrimas finansinėms dimensijoms pateikti</span><span class="sxs-lookup"><span data-stu-id="5af23-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="5af23-108">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="5af23-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="5af23-109">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5af23-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5af23-110">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="5af23-111">Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5af23-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="5af23-112">Naudokite modelį, kuris buvo iš anksto sukurtas kaip naujos ataskaitos duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="5af23-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="5af23-113">Lauke Pavadinimas, įveskite DK žurnalo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="5af23-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="5af23-114">Lauke Duomenų modelio aprašas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="5af23-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="5af23-115">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="5af23-115">Click Create configuration.</span></span>
8. <span data-ttu-id="5af23-116">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="5af23-116">Click Designer.</span></span>
9. <span data-ttu-id="5af23-117">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="5af23-118">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="5af23-119">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="5af23-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="5af23-120">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-120">Click OK.</span></span>
13. <span data-ttu-id="5af23-121">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="5af23-122">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="5af23-123">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="5af23-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="5af23-124">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-124">Click OK.</span></span>
17. <span data-ttu-id="5af23-125">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="5af23-126">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="5af23-127">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="5af23-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="5af23-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-128">Click OK.</span></span>
21. <span data-ttu-id="5af23-129">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="5af23-130">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="5af23-131">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="5af23-132">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="5af23-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="5af23-133">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-133">Click OK.</span></span>
26. <span data-ttu-id="5af23-134">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="5af23-135">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="5af23-136">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="5af23-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="5af23-137">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-137">Click OK.</span></span>
30. <span data-ttu-id="5af23-138">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="5af23-139">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="5af23-140">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="5af23-141">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="5af23-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="5af23-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-142">Click OK.</span></span>
35. <span data-ttu-id="5af23-143">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="5af23-144">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="5af23-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="5af23-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-145">Click OK.</span></span>
38. <span data-ttu-id="5af23-146">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="5af23-147">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="5af23-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="5af23-148">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-148">Click OK.</span></span>
41. <span data-ttu-id="5af23-149">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="5af23-150">Lauke Pavadinimas Dt.</span><span class="sxs-lookup"><span data-stu-id="5af23-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="5af23-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-151">Click OK.</span></span>
44. <span data-ttu-id="5af23-152">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="5af23-153">Lauke Pavadinimas įveskite Ct.</span><span class="sxs-lookup"><span data-stu-id="5af23-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="5af23-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-154">Click OK.</span></span>
47. <span data-ttu-id="5af23-155">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="5af23-156">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="5af23-157">Lauke Pavadinimas įveskite Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="5af23-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="5af23-158">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-158">Click OK.</span></span>
51. <span data-ttu-id="5af23-159">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="5af23-160">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5af23-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="5af23-161">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="5af23-162">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="5af23-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="5af23-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-163">Click OK.</span></span>
56. <span data-ttu-id="5af23-164">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="5af23-165">Lauke Pavadinimas įveskite Reikšmė.</span><span class="sxs-lookup"><span data-stu-id="5af23-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="5af23-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5af23-166">Click OK.</span></span>
59. <span data-ttu-id="5af23-167">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="5af23-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="5af23-168">Lauke Pavadinimas įveskite Aprašas.</span><span class="sxs-lookup"><span data-stu-id="5af23-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="5af23-169">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5af23-169">Click OK.</span></span>
<span data-ttu-id="5af23-170">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="5af23-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="5af23-171">Ataskaitos elementų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="5af23-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="5af23-172">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="5af23-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="5af23-173">Medyje išplėskite dalį model: Data model Financial dimensions sample model.</span><span class="sxs-lookup"><span data-stu-id="5af23-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="5af23-174">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="5af23-175">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="5af23-176">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="5af23-177">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="5af23-178">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="5af23-179">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-179">Click Bind.</span></span>
9. <span data-ttu-id="5af23-180">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="5af23-181">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="5af23-182">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-182">Click Bind.</span></span>
12. <span data-ttu-id="5af23-183">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="5af23-184">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="5af23-185">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-185">Click Bind.</span></span>
15. <span data-ttu-id="5af23-186">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="5af23-187">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="5af23-188">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-188">Click Bind.</span></span>
18. <span data-ttu-id="5af23-189">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="5af23-190">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.</span><span class="sxs-lookup"><span data-stu-id="5af23-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="5af23-191">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-191">Click Bind.</span></span>
21. <span data-ttu-id="5af23-192">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="5af23-193">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.</span><span class="sxs-lookup"><span data-stu-id="5af23-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="5af23-194">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-194">Click Bind.</span></span>
24. <span data-ttu-id="5af23-195">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="5af23-196">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="5af23-197">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-197">Click Bind.</span></span>
27. <span data-ttu-id="5af23-198">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="5af23-199">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.</span><span class="sxs-lookup"><span data-stu-id="5af23-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="5af23-200">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-200">Click Bind.</span></span>
30. <span data-ttu-id="5af23-201">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="5af23-202">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="5af23-203">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-203">Click Bind.</span></span>
33. <span data-ttu-id="5af23-204">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="5af23-205">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="5af23-206">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-206">Click Bind.</span></span>
36. <span data-ttu-id="5af23-207">Medyje pasirinkite Root: XML Element\Journal: XML Element\Batch: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="5af23-208">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="5af23-209">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-209">Click Bind.</span></span>
39. <span data-ttu-id="5af23-210">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="5af23-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="5af23-211">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="5af23-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="5af23-212">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-212">Click Bind.</span></span>
42. <span data-ttu-id="5af23-213">Medyje pasirinkite Root: XML Element\Company: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="5af23-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="5af23-214">Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.</span><span class="sxs-lookup"><span data-stu-id="5af23-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="5af23-215">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="5af23-215">Click Bind.</span></span>
45. <span data-ttu-id="5af23-216">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5af23-216">Click Save.</span></span>
46. <span data-ttu-id="5af23-217">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5af23-217">Close the page.</span></span>
<span data-ttu-id="5af23-218">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="5af23-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

