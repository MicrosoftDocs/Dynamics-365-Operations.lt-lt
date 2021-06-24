---
title: Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas
description: Šioje temoje aprašoma, kaip apibrėžti ir konfigūruoti laukų, rodomų sandėlio valdymo mobiliųjų įrenginių programėlėje, pavadinimus ir prioritetus.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc224d3fd6cf5b111f61066202090f10ba4a7e8a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189255"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="3eac4-103">Sandėlio valdymo mobiliųjų įrenginių programėlės laukų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3eac4-104">Šioje temoje aprašoma, kaip apibrėžti ir konfigūruoti laukų, rodomų sandėlio valdymo mobiliųjų įrenginių programėlėje, pavadinimus ir prioritetus.</span><span class="sxs-lookup"><span data-stu-id="3eac4-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="3eac4-105">Ši tema taikoma sandėlio valdymo funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="3eac4-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="3eac4-106">Ji netaikoma atsargų valdymo funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="3eac4-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="3eac4-107">Sandėlio valdymo mobiliųjų įrenginių programėlė yra programa, kurią galite naudoti sandėlio užduotims atlikti.</span><span class="sxs-lookup"><span data-stu-id="3eac4-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="3eac4-108">Galite nurodyti ir konfigūruoti programoje naudojamų laukų pavadinimus, taip pat galite konfigūruoti prioritetą, kuriam laukų pavadinimai turėtų būti priskirti.</span><span class="sxs-lookup"><span data-stu-id="3eac4-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="3eac4-109">Šioje temoje paaiškinama, kaip nurodyti ir konfigūruoti šiuos sandėlio valdymo mobiliųjų įrenginių programėlės laukų pavadinimus bei prioritetus ir, kaip jie naudojami.</span><span class="sxs-lookup"><span data-stu-id="3eac4-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="3eac4-110">Sandėlio programos laukų pavadinimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-110">Configure warehouse app field names</span></span>

<span data-ttu-id="3eac4-111">Naudodami „Warehousing“ savo mobiliajame įrenginyje galite konfigūruoti, kaip metaduomenys turėtų būti rodomi puslapyje **Sandėlio programos laukų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="3eac4-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="3eac4-112">Naujoje įmonėje pasirinkite **Kurti numatytąją sąranką**, kad sugeneruotumėte visų laukų pavadinimus, kurie bus naudojami sandėlio mobiliųjų įrenginių darbo eigose, ir tada jiems priskirkite pageidaujamą įvesties režimą ir įvesties tipą.</span><span class="sxs-lookup"><span data-stu-id="3eac4-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="3eac4-113">Sugeneravę visų laukų pavadinimus, galite pasirinkti toliau nurodytas įvesties parinktis.</span><span class="sxs-lookup"><span data-stu-id="3eac4-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3eac4-114">Parinktis</span><span class="sxs-lookup"><span data-stu-id="3eac4-114">Option</span></span></th>
<th><span data-ttu-id="3eac4-115">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3eac4-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3eac4-116">Pageidaujamas įvesties režimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="3eac4-117">Ši parinktis nurodo, ar pasirinktam lauko pavadinimui turi būti priskirtas ir rodomas nuskaitymo laukas, ar neautomatinės įvesties laukas.</span><span class="sxs-lookup"><span data-stu-id="3eac4-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="3eac4-118">Tai naudinga norint laukus atskirti pagal tai, ar juose naudojami brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="3eac4-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="3eac4-119"><strong>Pastaba.</strong> Kai pageidaujamas laukų pavadinimų įvesties režimas nustatytas į parinktį <strong>Nuskaitymas</strong>, galite įvesti informaciją neautomatiškai, jei brūkšninis kodas yra neįskaitomas arba pažeistas.</span><span class="sxs-lookup"><span data-stu-id="3eac4-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3eac4-120">Įvedimo tipas</span><span class="sxs-lookup"><span data-stu-id="3eac4-120">Input type</span></span></td>
<td><span data-ttu-id="3eac4-121">Ši parinktis nurodo, koks įvesties tipas turėtų būti priskirtas pasirinktam lauko pavadinimui.</span><span class="sxs-lookup"><span data-stu-id="3eac4-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="3eac4-122">Galima pasirinkti iš keturių toliau pateiktų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="3eac4-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="3eac4-123"><strong>Pasirinkimas</strong> - pateiktas parinkčių, kurias galima pasirinkti, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3eac4-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="3eac4-124">Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="3eac4-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3eac4-125"><strong>Data</strong> - laukų pavadinimuose, kurie nurodyti kaip data, bus rodomas datos formatas su žyma.</span><span class="sxs-lookup"><span data-stu-id="3eac4-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="3eac4-126">Tokiu būdu sandėlio darbuotojai gali matyti, kokiu formatu įvesti datą.</span><span class="sxs-lookup"><span data-stu-id="3eac4-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="3eac4-127">Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="3eac4-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="3eac4-128"><strong>Raidinis</strong> - jei pasirinkta ši parinktis, programoje įvedant informaciją neautomatiškai bus naudojama įrenginio klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="3eac4-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="3eac4-129">Klaviatūros patirtį galima keisti, atsižvelgiant į naudojamą įrenginį.</span><span class="sxs-lookup"><span data-stu-id="3eac4-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="3eac4-130"><strong>Skaitinis</strong> - jei laukų pavadinimuose nustatyta tik skaitinių duomenų įvestis, galite pasirinkti šią parinktį, kad būtų rodoma pasirinktinė skaitinė klaviatūra su įvesties lauku, o ne įrenginio klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="3eac4-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="3eac4-131">Sandėlio programos laukų prioriteto konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="3eac4-132">Puslapyje **Sandėlio programos laukų prioritetas** laukų pavadinimus galite suskirstyti į skirtingas prioritetų grupes.</span><span class="sxs-lookup"><span data-stu-id="3eac4-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="3eac4-133">Tokiu būdu galima pasirinkti, kokia informacija turėtų būti rodomas pagrindiniame užduočių puslapyje, kai sandėlio darbuotojai atlieka užduotis naudodami programą.</span><span class="sxs-lookup"><span data-stu-id="3eac4-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="3eac4-134">Jei spustelėsite **Kurti numatytąją sąranką**, bus sugeneruotas numatytasis prioritetų grupių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3eac4-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="3eac4-135">Galima kurti tiek prioritetų grupių, kiek norima, bet užduočių puslapyje bus rodomos tik trys prioritetų grupės.</span><span class="sxs-lookup"><span data-stu-id="3eac4-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="3eac4-136">Kai sistema siunčia metaduomenis į programą, kiekvienam laukui ji priskirs santykinį prioritetą, atsižvelgiant į lauko prioriteto grupę, o programos užduočių puslapyje bus rodomos pirmosios trys prioritetų grupės, esančios metaduomenyse.</span><span class="sxs-lookup"><span data-stu-id="3eac4-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="3eac4-137">Kiti perviršio metaduomenys bus rodomi antriniame informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3eac4-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="3eac4-138">Tolesnėje lentelėje pateikiamas penkių prioritetų grupių pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3eac4-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3eac4-139">Prioritetų grupė</span><span class="sxs-lookup"><span data-stu-id="3eac4-139">Priority group</span></span></th>
<th><span data-ttu-id="3eac4-140">Priskirti laukai</span><span class="sxs-lookup"><span data-stu-id="3eac4-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="3eac4-141">10 prioritetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="3eac4-142">Produktas</span><span class="sxs-lookup"><span data-stu-id="3eac4-142">Item</span></span></li>
<li><span data-ttu-id="3eac4-143">Kiekis</span><span class="sxs-lookup"><span data-stu-id="3eac4-143">Quantity</span></span></li>
<li><span data-ttu-id="3eac4-144">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3eac4-145">20 prioritetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="3eac4-146">Klasterio pareigos</span><span class="sxs-lookup"><span data-stu-id="3eac4-146">Cluster position</span></span></li>
<li><span data-ttu-id="3eac4-147">Klasteris</span><span class="sxs-lookup"><span data-stu-id="3eac4-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3eac4-148">30 prioritetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="3eac4-149">Prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="3eac4-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="3eac4-150">40 prioritetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="3eac4-151">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-151">Configuration</span></span></li>
<li><span data-ttu-id="3eac4-152">Spalva</span><span class="sxs-lookup"><span data-stu-id="3eac4-152">Color</span></span></li>
<li><span data-ttu-id="3eac4-153">Dydis</span><span class="sxs-lookup"><span data-stu-id="3eac4-153">Size</span></span></li>
<li><span data-ttu-id="3eac4-154">Stilius</span><span class="sxs-lookup"><span data-stu-id="3eac4-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="3eac4-155">50 prioritetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="3eac4-156">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="3eac4-156">Location</span></span></li>
<li><span data-ttu-id="3eac4-157">Numerio lentelė</span><span class="sxs-lookup"><span data-stu-id="3eac4-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3eac4-158">Pvz., kai sandėlio darbuotojas atlieka užduotį mobiliajame įrenginyje, jei metaduomenys, kurie bus rodomi programoje, apima toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="3eac4-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="3eac4-159">Produktas</span><span class="sxs-lookup"><span data-stu-id="3eac4-159">Item</span></span>
-   <span data-ttu-id="3eac4-160">Kiekis</span><span class="sxs-lookup"><span data-stu-id="3eac4-160">Quantity</span></span>
-   <span data-ttu-id="3eac4-161">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-161">Unit of measure</span></span>
-   <span data-ttu-id="3eac4-162">Prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="3eac4-162">Item description</span></span>
-   <span data-ttu-id="3eac4-163">Dydis ir vieta</span><span class="sxs-lookup"><span data-stu-id="3eac4-163">Size and Location</span></span>

<span data-ttu-id="3eac4-164">Atsižvelgiant į sandėlio programos laukų prioriteto nustatymą ankstesnėje lentelėje, užduočių puslapyje bus rodomos 3 toliau pateiktos informacijos eilutės.</span><span class="sxs-lookup"><span data-stu-id="3eac4-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="3eac4-165">1 eilutė: prekė, kiekis, matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="3eac4-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="3eac4-166">2 eilutė: prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="3eac4-166">Row 2: Item description</span></span>
-   <span data-ttu-id="3eac4-167">3 eilutė: dydis</span><span class="sxs-lookup"><span data-stu-id="3eac4-167">Row 3: Size</span></span>

<span data-ttu-id="3eac4-168">Likę metaduomenys, pvz., vieta, užduočių puslapyje rodomi nebus, bet bus rodomi informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3eac4-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="3eac4-169">Norėdami sužinoti daugiau ir pamatyti vartotojo sąsajos pavyzdžių žr. tinklaraščio įrašą [Pranešimas apie „Finance and Operations“ – versiją „Warehousing“](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="3eac4-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3eac4-170">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3eac4-170">Additional resources</span></span>

[<span data-ttu-id="3eac4-171">Sandėli valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas</span><span class="sxs-lookup"><span data-stu-id="3eac4-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]