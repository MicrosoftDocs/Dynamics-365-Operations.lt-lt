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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cef61787e50561eaac4fd52741ab5f90d9c4171d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406502"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="f512d-103">ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis – Ataskaitos kūrimas)</span><span class="sxs-lookup"><span data-stu-id="f512d-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f512d-104">Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="f512d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f512d-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="f512d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f512d-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis. Modelio susiejimas)“.</span><span class="sxs-lookup"><span data-stu-id="f512d-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="f512d-107">Ataskaitos kūrimas finansinėms dimensijoms pateikti</span><span class="sxs-lookup"><span data-stu-id="f512d-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="f512d-108">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f512d-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f512d-109">Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f512d-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f512d-110">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f512d-111">Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f512d-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="f512d-112">Naudokite modelį, kuris buvo iš anksto sukurtas kaip naujos ataskaitos duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="f512d-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="f512d-113">Lauke Pavadinimas, įveskite DK žurnalo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="f512d-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="f512d-114">Lauke Duomenų modelio aprašas pasirinkite Įrašas.</span><span class="sxs-lookup"><span data-stu-id="f512d-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="f512d-115">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="f512d-115">Click Create configuration.</span></span>
8. <span data-ttu-id="f512d-116">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f512d-116">Click Designer.</span></span>
9. <span data-ttu-id="f512d-117">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="f512d-118">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="f512d-119">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="f512d-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="f512d-120">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-120">Click OK.</span></span>
13. <span data-ttu-id="f512d-121">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="f512d-122">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="f512d-123">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="f512d-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="f512d-124">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-124">Click OK.</span></span>
17. <span data-ttu-id="f512d-125">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="f512d-126">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="f512d-127">Lauke Pavadinimas įveskite Žurnalas.</span><span class="sxs-lookup"><span data-stu-id="f512d-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="f512d-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-128">Click OK.</span></span>
21. <span data-ttu-id="f512d-129">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="f512d-130">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="f512d-131">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="f512d-132">Lauke Pavadinimas įveskite Paketas.</span><span class="sxs-lookup"><span data-stu-id="f512d-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="f512d-133">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-133">Click OK.</span></span>
26. <span data-ttu-id="f512d-134">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="f512d-135">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="f512d-136">Lauke Pavadinimas įveskite Operacija.</span><span class="sxs-lookup"><span data-stu-id="f512d-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="f512d-137">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-137">Click OK.</span></span>
30. <span data-ttu-id="f512d-138">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="f512d-139">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="f512d-140">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="f512d-141">Lauke Pavadinimas įveskite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="f512d-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="f512d-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-142">Click OK.</span></span>
35. <span data-ttu-id="f512d-143">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="f512d-144">Lauke Pavadinimas įveskite Data.</span><span class="sxs-lookup"><span data-stu-id="f512d-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="f512d-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-145">Click OK.</span></span>
38. <span data-ttu-id="f512d-146">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="f512d-147">Lauke „Pavadinimas“ suveskite „Valiuta“.</span><span class="sxs-lookup"><span data-stu-id="f512d-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="f512d-148">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-148">Click OK.</span></span>
41. <span data-ttu-id="f512d-149">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="f512d-150">Lauke Pavadinimas Dt.</span><span class="sxs-lookup"><span data-stu-id="f512d-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="f512d-151">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-151">Click OK.</span></span>
44. <span data-ttu-id="f512d-152">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="f512d-153">Lauke Pavadinimas įveskite Ct.</span><span class="sxs-lookup"><span data-stu-id="f512d-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="f512d-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-154">Click OK.</span></span>
47. <span data-ttu-id="f512d-155">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="f512d-156">Medyje pasirinkite „XML \ Elementas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="f512d-157">Lauke Pavadinimas įveskite Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="f512d-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="f512d-158">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-158">Click OK.</span></span>
51. <span data-ttu-id="f512d-159">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="f512d-160">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f512d-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="f512d-161">Medyje pasirinkite „XML \ Atributas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="f512d-162">Lauke Pavadinimas įveskite Kodas.</span><span class="sxs-lookup"><span data-stu-id="f512d-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="f512d-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-163">Click OK.</span></span>
56. <span data-ttu-id="f512d-164">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="f512d-165">Lauke Pavadinimas įveskite Reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f512d-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="f512d-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f512d-166">Click OK.</span></span>
59. <span data-ttu-id="f512d-167">Spustelėkite Įtraukti atributą.</span><span class="sxs-lookup"><span data-stu-id="f512d-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="f512d-168">Lauke Pavadinimas įveskite Aprašas.</span><span class="sxs-lookup"><span data-stu-id="f512d-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="f512d-169">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f512d-169">Click OK.</span></span>
<span data-ttu-id="f512d-170">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="f512d-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="f512d-171">Ataskaitos elementų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="f512d-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="f512d-172">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="f512d-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f512d-173">Medyje išplėskite dalį model: Data model Financial dimensions sample model.</span><span class="sxs-lookup"><span data-stu-id="f512d-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f512d-174">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="f512d-175">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="f512d-176">Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="f512d-177">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="f512d-178">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="f512d-179">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-179">Click Bind.</span></span>
9. <span data-ttu-id="f512d-180">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="f512d-181">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="f512d-182">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-182">Click Bind.</span></span>
12. <span data-ttu-id="f512d-183">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="f512d-184">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="f512d-185">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-185">Click Bind.</span></span>
15. <span data-ttu-id="f512d-186">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="f512d-187">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="f512d-188">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-188">Click Bind.</span></span>
18. <span data-ttu-id="f512d-189">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="f512d-190">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.</span><span class="sxs-lookup"><span data-stu-id="f512d-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="f512d-191">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-191">Click Bind.</span></span>
21. <span data-ttu-id="f512d-192">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="f512d-193">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.</span><span class="sxs-lookup"><span data-stu-id="f512d-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="f512d-194">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-194">Click Bind.</span></span>
24. <span data-ttu-id="f512d-195">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="f512d-196">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="f512d-197">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-197">Click Bind.</span></span>
27. <span data-ttu-id="f512d-198">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="f512d-199">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.</span><span class="sxs-lookup"><span data-stu-id="f512d-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="f512d-200">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-200">Click Bind.</span></span>
30. <span data-ttu-id="f512d-201">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="f512d-202">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="f512d-203">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-203">Click Bind.</span></span>
33. <span data-ttu-id="f512d-204">Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="f512d-205">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="f512d-206">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-206">Click Bind.</span></span>
36. <span data-ttu-id="f512d-207">Medyje pasirinkite Root: XML Element\Journal: XML Element\Batch: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="f512d-208">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="f512d-209">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-209">Click Bind.</span></span>
39. <span data-ttu-id="f512d-210">Medyje pasirinkite Root: XML Element\Journal: XML Element.</span><span class="sxs-lookup"><span data-stu-id="f512d-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="f512d-211">Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.</span><span class="sxs-lookup"><span data-stu-id="f512d-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="f512d-212">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-212">Click Bind.</span></span>
42. <span data-ttu-id="f512d-213">Medyje pasirinkite Root: XML Element\Company: XML Attribute.</span><span class="sxs-lookup"><span data-stu-id="f512d-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="f512d-214">Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.</span><span class="sxs-lookup"><span data-stu-id="f512d-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="f512d-215">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="f512d-215">Click Bind.</span></span>
45. <span data-ttu-id="f512d-216">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f512d-216">Click Save.</span></span>
46. <span data-ttu-id="f512d-217">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f512d-217">Close the page.</span></span>
<span data-ttu-id="f512d-218">![ER operacijų dizaino įrankio puslapis](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="f512d-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

