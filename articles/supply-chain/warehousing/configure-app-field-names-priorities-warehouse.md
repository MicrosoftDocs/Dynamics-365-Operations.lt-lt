---
title: Programos laukų pavadinimų konfigūravimas sandėliavimo programoje
description: Šioje temoje aprašoma, kaip nurodyti ir konfigūruoti sandėlio programos laukų pavadinimus ir prioritetus programoje „Dynamics 365 Supply Chain Management“.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 4c22a4314c36ba7112456ef264df500af98996f3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232964"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a><span data-ttu-id="93206-103">Programos laukų pavadinimų konfigūravimas sandėliavimo programoje</span><span class="sxs-lookup"><span data-stu-id="93206-103">Configure app field names in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93206-104">Šioje temoje aprašoma, kaip nurodyti ir konfigūruoti sandėlio programos laukų pavadinimus ir prioritetus programoje „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="93206-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="93206-105">Ši tema taikoma sandėlio valdymo funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="93206-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="93206-106">Ji netaikoma atsargų valdymo funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="93206-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="93206-107">„Warehousing” yra programa, kurią galite naudoti sandėlio užduotims atlikti.</span><span class="sxs-lookup"><span data-stu-id="93206-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="93206-108">Galite nurodyti ir konfigūruoti programoje naudojamų laukų pavadinimus, taip pat galite konfigūruoti prioritetą, kuriam laukų pavadinimai turėtų būti priskirti.</span><span class="sxs-lookup"><span data-stu-id="93206-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="93206-109">Šioje temoje paaiškinama, kaip nurodyti ir konfigūruoti šiuos sandėlio programos laukų pavadinimus bei prioritetus ir kaip jie naudojami „Warehousing“.</span><span class="sxs-lookup"><span data-stu-id="93206-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="93206-110">Daugiau informacijos apie prisijungimo prie Fsandėliavimo konfigūravimą, žr. mokymo programoje [Sandėliavimo programos diegimo ir konfigūravimo apžvalga](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="93206-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the warehouse app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="93206-111">Sandėlio programos laukų pavadinimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="93206-111">Configure warehouse app field names</span></span>

<span data-ttu-id="93206-112">Naudodami „Warehousing“ savo mobiliajame įrenginyje galite konfigūruoti, kaip metaduomenys turėtų būti rodomi puslapyje **Sandėlio programos laukų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="93206-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="93206-113">Naujoje įmonėje pasirinkite **Kurti numatytąją sąranką**, kad sugeneruotumėte visų laukų pavadinimus, kurie bus naudojami sandėlio mobiliųjų įrenginių darbo eigose, ir tada jiems priskirkite pageidaujamą įvesties režimą ir įvesties tipą.</span><span class="sxs-lookup"><span data-stu-id="93206-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="93206-114">Sugeneravę visų laukų pavadinimus, galite pasirinkti toliau nurodytas įvesties parinktis.</span><span class="sxs-lookup"><span data-stu-id="93206-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93206-115">Parinktis</span><span class="sxs-lookup"><span data-stu-id="93206-115">Option</span></span></th>
<th><span data-ttu-id="93206-116">aprašymas</span><span class="sxs-lookup"><span data-stu-id="93206-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93206-117">Pageidaujamas įvesties režimas</span><span class="sxs-lookup"><span data-stu-id="93206-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="93206-118">Ši parinktis nurodo, ar pasirinktam lauko pavadinimui turi būti priskirtas ir rodomas nuskaitymo laukas, ar neautomatinės įvesties laukas.</span><span class="sxs-lookup"><span data-stu-id="93206-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="93206-119">Tai naudinga norint laukus atskirti pagal tai, ar juose naudojami brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="93206-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="93206-120"><strong>Pastaba.</strong> Kai pageidaujamas laukų pavadinimų įvesties režimas nustatytas į parinktį <strong>Nuskaitymas</strong>, galite įvesti informaciją neautomatiškai, jei brūkšninis kodas yra neįskaitomas arba pažeistas.</span><span class="sxs-lookup"><span data-stu-id="93206-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93206-121">Įvedimo tipas</span><span class="sxs-lookup"><span data-stu-id="93206-121">Input type</span></span></td>
<td><span data-ttu-id="93206-122">Ši parinktis nurodo, koks įvesties tipas turėtų būti priskirtas pasirinktam lauko pavadinimui.</span><span class="sxs-lookup"><span data-stu-id="93206-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="93206-123">Galima pasirinkti iš keturių toliau pateiktų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="93206-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="93206-124"><strong>Pasirinkimas</strong> - pateiktas parinkčių, kurias galima pasirinkti, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="93206-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="93206-125">Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="93206-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="93206-126"><strong>Data</strong> - laukų pavadinimuose, kurie nurodyti kaip data, bus rodomas datos formatas su žyma.</span><span class="sxs-lookup"><span data-stu-id="93206-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="93206-127">Tokiu būdu sandėlio darbuotojai gali matyti, kokiu formatu įvesti datą.</span><span class="sxs-lookup"><span data-stu-id="93206-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="93206-128">Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="93206-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="93206-129"><strong>Raidinis</strong> - jei pasirinkta ši parinktis, programoje įvedant informaciją neautomatiškai bus naudojama įrenginio klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="93206-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="93206-130">Klaviatūros patirtį galima keisti, atsižvelgiant į naudojamą įrenginį.</span><span class="sxs-lookup"><span data-stu-id="93206-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="93206-131"><strong>Skaitinis</strong> - jei laukų pavadinimuose nustatyta tik skaitinių duomenų įvestis, galite pasirinkti šią parinktį, kad būtų rodoma pasirinktinė skaitinė klaviatūra su įvesties lauku, o ne įrenginio klaviatūra.</span><span class="sxs-lookup"><span data-stu-id="93206-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="93206-132">Sandėlio programos laukų prioriteto konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="93206-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="93206-133">Puslapyje **Sandėlio programos laukų prioritetas** laukų pavadinimus galite suskirstyti į skirtingas prioritetų grupes.</span><span class="sxs-lookup"><span data-stu-id="93206-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="93206-134">Tokiu būdu galima pasirinkti, kokia informacija turėtų būti rodomas pagrindiniame užduočių puslapyje, kai sandėlio darbuotojai atlieka užduotis naudodami programą.</span><span class="sxs-lookup"><span data-stu-id="93206-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="93206-135">Jei spustelėsite **Kurti numatytąją sąranką**, bus sugeneruotas numatytasis prioritetų grupių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="93206-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="93206-136">Galima kurti tiek prioritetų grupių, kiek norima, bet užduočių puslapyje bus rodomos tik trys prioritetų grupės.</span><span class="sxs-lookup"><span data-stu-id="93206-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="93206-137">Kai sistema siunčia metaduomenis į programą, kiekvienam laukui ji priskirs santykinį prioritetą, atsižvelgiant į lauko prioriteto grupę, o programos užduočių puslapyje bus rodomos pirmosios trys prioritetų grupės, esančios metaduomenyse.</span><span class="sxs-lookup"><span data-stu-id="93206-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="93206-138">Kiti perviršio metaduomenys bus rodomi antriniame informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="93206-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="93206-139">Tolesnėje lentelėje pateikiamas penkių prioritetų grupių pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="93206-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93206-140">Prioritetų grupė</span><span class="sxs-lookup"><span data-stu-id="93206-140">Priority group</span></span></th>
<th><span data-ttu-id="93206-141">Priskirti laukai</span><span class="sxs-lookup"><span data-stu-id="93206-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="93206-142">10 prioritetas</span><span class="sxs-lookup"><span data-stu-id="93206-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="93206-143">Produktas</span><span class="sxs-lookup"><span data-stu-id="93206-143">Item</span></span></li>
<li><span data-ttu-id="93206-144">Kiekis</span><span class="sxs-lookup"><span data-stu-id="93206-144">Quantity</span></span></li>
<li><span data-ttu-id="93206-145">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="93206-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="93206-146">20 prioritetas</span><span class="sxs-lookup"><span data-stu-id="93206-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="93206-147">Klasterio pareigos</span><span class="sxs-lookup"><span data-stu-id="93206-147">Cluster position</span></span></li>
<li><span data-ttu-id="93206-148">Klasteris</span><span class="sxs-lookup"><span data-stu-id="93206-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="93206-149">30 prioritetas</span><span class="sxs-lookup"><span data-stu-id="93206-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="93206-150">Prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="93206-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="93206-151">40 prioritetas</span><span class="sxs-lookup"><span data-stu-id="93206-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="93206-152">Konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="93206-152">Configuration</span></span></li>
<li><span data-ttu-id="93206-153">Spalva</span><span class="sxs-lookup"><span data-stu-id="93206-153">Color</span></span></li>
<li><span data-ttu-id="93206-154">Dydis</span><span class="sxs-lookup"><span data-stu-id="93206-154">Size</span></span></li>
<li><span data-ttu-id="93206-155">Stilius</span><span class="sxs-lookup"><span data-stu-id="93206-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="93206-156">50 prioritetas</span><span class="sxs-lookup"><span data-stu-id="93206-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="93206-157">Buvimo vieta</span><span class="sxs-lookup"><span data-stu-id="93206-157">Location</span></span></li>
<li><span data-ttu-id="93206-158">Numerio lentelė</span><span class="sxs-lookup"><span data-stu-id="93206-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="93206-159">Pvz., kai sandėlio darbuotojas atlieka užduotį mobiliajame įrenginyje, jei metaduomenys, kurie bus rodomi programoje, apima toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="93206-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="93206-160">Produktas</span><span class="sxs-lookup"><span data-stu-id="93206-160">Item</span></span>
-   <span data-ttu-id="93206-161">Kiekis</span><span class="sxs-lookup"><span data-stu-id="93206-161">Quantity</span></span>
-   <span data-ttu-id="93206-162">Matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="93206-162">Unit of measure</span></span>
-   <span data-ttu-id="93206-163">Prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="93206-163">Item description</span></span>
-   <span data-ttu-id="93206-164">Dydis ir vieta</span><span class="sxs-lookup"><span data-stu-id="93206-164">Size and Location</span></span>

<span data-ttu-id="93206-165">Atsižvelgiant į sandėlio programos laukų prioriteto nustatymą ankstesnėje lentelėje, užduočių puslapyje bus rodomos 3 toliau pateiktos informacijos eilutės.</span><span class="sxs-lookup"><span data-stu-id="93206-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="93206-166">1 eilutė: prekė, kiekis, matavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="93206-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="93206-167">2 eilutė: prekės aprašas</span><span class="sxs-lookup"><span data-stu-id="93206-167">Row 2: Item description</span></span>
-   <span data-ttu-id="93206-168">3 eilutė: dydis</span><span class="sxs-lookup"><span data-stu-id="93206-168">Row 3: Size</span></span>

<span data-ttu-id="93206-169">Likę metaduomenys, pvz., vieta, užduočių puslapyje rodomi nebus, bet bus rodomi informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="93206-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="93206-170">Norėdami sužinoti daugiau ir pamatyti vartotojo sąsajos pavyzdžių žr. tinklaraščio įrašą [Pranešimas apie „Finance and Operations“ – versiją „Warehousing“](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="93206-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="93206-171">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="93206-171">Additional resources</span></span>
--------

[<span data-ttu-id="93206-172">Sandėliavimo programos diegimo ir konfigūravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="93206-172">Install and configure the warehouse app overview</span></span>](install-configure-warehousing-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]