---
title: Įveskite sąskaitų ir dimensijų kombinacijas (segmentuoto įrašo valdiklis)
description: Šiame straipsnyje aprašyta, kaip įvesti sąskaitos ir dimensijų kombinacijas arba DK sąskaitas. Įvedimo patirtis dažnai vadinama segmentuotu įrašų valdikliu.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445881"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="36ae5-104">Įveskite sąskaitų ir dimensijų kombinacijas (segmentuoto įrašo valdiklis)</span><span class="sxs-lookup"><span data-stu-id="36ae5-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36ae5-105">Šiame straipsnyje aprašyta, kaip įvesti sąskaitos ir dimensijų kombinacijas arba DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="36ae5-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="36ae5-106">Įvedimo patirtis dažnai vadinama segmentuotu įrašų valdikliu.</span><span class="sxs-lookup"><span data-stu-id="36ae5-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="36ae5-107">Vartotojai įveda sąskaitų ir dimensijų kombinacijas įvairiuose puslapiuose, pvz., bendrųjų žurnalų, biudžeto sudarymo ir registravimo aprašų puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="36ae5-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="36ae5-108">Galiojančios sąskaitų ir dimensijų kombinacijos priklauso nuo sąskaitų struktūrų, kurios priskirtus DK, ir išplėstinių taisyklių, kurios priskirtos sąskaitų struktūroms.</span><span class="sxs-lookup"><span data-stu-id="36ae5-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="36ae5-109">Kai vartotojai įveda kombinaciją, jie gali įvesti reikšmes rankiniu būdu arba pasinaudoti išsamia peržvalgos patirtimi.</span><span class="sxs-lookup"><span data-stu-id="36ae5-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="36ae5-110">Kai lauke nustatyta įvesties vieta, galite pradėti įvesti tekstą ir bus ieškoma reikšmės bei aprašo.</span><span class="sxs-lookup"><span data-stu-id="36ae5-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="36ae5-111">Pvz., jei įvesite 180, bus ieškoma bet kokios reikšmės, prasidedančios šia skaitmenų kombinacija.</span><span class="sxs-lookup"><span data-stu-id="36ae5-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="36ae5-112">Arba, jei įvesite Grynieji pinigai, bus ieškoma bet kokios reikšmės, kurios aprašas prasideda fraze Grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="36ae5-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="36ae5-113">Taip pat ieškodami galite naudoti pakaitos simbolį, pvz., \*Grynieji pinigai arba \*180, jei reikšmėje arba apraše yra ieškos kriterijų.</span><span class="sxs-lookup"><span data-stu-id="36ae5-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="36ae5-114">Toliau pateikiamoje lentelėje aprašomi spartieji klavišai, kuriuos galima naudoti, kai peržvalga uždaryta.</span><span class="sxs-lookup"><span data-stu-id="36ae5-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36ae5-115">Spartieji klavišai</span><span class="sxs-lookup"><span data-stu-id="36ae5-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="36ae5-116">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="36ae5-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36ae5-117">Alt + rodyklė žemyn</span><span class="sxs-lookup"><span data-stu-id="36ae5-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="36ae5-118">Atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="36ae5-118">Open the lookup.</span></span> <span data-ttu-id="36ae5-119">Jei paspausite Alt + rodyklę žemyn antrą kartą, dėmesys sutelkiamas į iškeliamojo objekto segmentus.</span><span class="sxs-lookup"><span data-stu-id="36ae5-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="36ae5-120">Enter ir Shift + Enter</span><span class="sxs-lookup"><span data-stu-id="36ae5-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="36ae5-121">Sąskaitų plano skyriklis</span><span class="sxs-lookup"><span data-stu-id="36ae5-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="36ae5-122">Rodyklė dešinėn ir rodyklė kairėn</span><span class="sxs-lookup"><span data-stu-id="36ae5-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="36ae5-123">Pereiti į kitą ar ankstesnį segmentą.</span><span class="sxs-lookup"><span data-stu-id="36ae5-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ae5-124">Tabuliavimo ženklas</span><span class="sxs-lookup"><span data-stu-id="36ae5-124">Tab</span></span></td>
<td><span data-ttu-id="36ae5-125">Pereiti prie kito lauko tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="36ae5-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="36ae5-126">Toliau pateikiamoje lentelėje aprašomi spartieji klavišai, kuriuos galima naudoti, kai peržvalga atidaryta.</span><span class="sxs-lookup"><span data-stu-id="36ae5-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="36ae5-127">Spartieji klavišai</span><span class="sxs-lookup"><span data-stu-id="36ae5-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="36ae5-128">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="36ae5-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="36ae5-129">Esc</span><span class="sxs-lookup"><span data-stu-id="36ae5-129">Esc</span></span></td>
<td><span data-ttu-id="36ae5-130">Uždarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="36ae5-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="36ae5-131">Rodyklė aukštyn ir rodyklė žemyn</span><span class="sxs-lookup"><span data-stu-id="36ae5-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="36ae5-132">Page Up ir Page Down</span><span class="sxs-lookup"><span data-stu-id="36ae5-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="36ae5-133">Home ir End</span><span class="sxs-lookup"><span data-stu-id="36ae5-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="36ae5-134">Pereiti prie ankstesnės arba kitos reikšmės sąrašuose, prie ankstesnių arba kitų reikšmių grupių, arba prie pirmo arba paskutinio elemento peržvalgoje.</span><span class="sxs-lookup"><span data-stu-id="36ae5-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="36ae5-135">Sąskaitų plano skyriklis</span><span class="sxs-lookup"><span data-stu-id="36ae5-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="36ae5-136">Rodyklė dešinėn ir rodyklė kairėn</span><span class="sxs-lookup"><span data-stu-id="36ae5-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="36ae5-137">Pereiti į kitą ar ankstesnį segmentą.</span><span class="sxs-lookup"><span data-stu-id="36ae5-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="36ae5-138">Skirtukas</span><span class="sxs-lookup"><span data-stu-id="36ae5-138">Tab</span></span></td>
<td><span data-ttu-id="36ae5-139">Pereiti prie kito lauko tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="36ae5-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="36ae5-140">ALT + W</span><span class="sxs-lookup"><span data-stu-id="36ae5-140">Alt+W</span></span></td>
<td><span data-ttu-id="36ae5-141">Perjungti tarp <strong>Rodyti viską</strong> ir <strong>Rodyti tinkamą</strong>.</span><span class="sxs-lookup"><span data-stu-id="36ae5-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





