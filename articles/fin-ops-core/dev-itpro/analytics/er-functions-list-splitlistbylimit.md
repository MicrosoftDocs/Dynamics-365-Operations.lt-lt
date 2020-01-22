---
title: SPLITLISTBYLIMIT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama SPLITLISTBYLIMIT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9b740b7d46fcfdf0d0b08d03411017cf909265d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916182"
---
# <span data-ttu-id="5d4a2-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="5d4a2-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d4a2-104">`SPLITLISTBYLIMIT` funkcija išskaido nurodytą sąrašą į naują antrinių sąrašų (paketų) sąrašą.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="5d4a2-105">Kiekvieno paketo įrašų skaičius yra dinamiškai apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="5d4a2-106">Tada funkcija grąžina rezultatą kaip naują *Įrašų sąrašo* reikšmę, kurią sudaro paketai.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4a2-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="5d4a2-107">Syntax</span></span>

```
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="5d4a2-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="5d4a2-108">Arguments</span></span>

<span data-ttu-id="5d4a2-109">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-109">`list`: *Record list*</span></span>

<span data-ttu-id="5d4a2-110">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="5d4a2-111">`limit value`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="5d4a2-112">Didžiausia ribos vertė, naudojama norint suskaidyti pradinį sąrašą į paketus.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="5d4a2-113">`limit source`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-113">`limit source`: *Field*</span></span>

<span data-ttu-id="5d4a2-114">Tinkamas *sveikojo skaičiaus* arba *realiojo skaičiaus* tipo lauko maršrutas nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="5d4a2-115">Šio lauko reikšmė apibrėžia veiksmą, kad bendroji suma padidinama.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d4a2-116">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="5d4a2-116">Return values</span></span>

<span data-ttu-id="5d4a2-117">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-117">*Record list*</span></span>

<span data-ttu-id="5d4a2-118">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5d4a2-119">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="5d4a2-119">Usage notes</span></span>

<span data-ttu-id="5d4a2-120">Grąžintame paketų sąraše yra šių elementų:</span><span class="sxs-lookup"><span data-stu-id="5d4a2-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="5d4a2-121">**Vertė**: *Sąrašas*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-121">**Value**: *List*</span></span>

    <span data-ttu-id="5d4a2-122">Įrašų, priklausančių dabartiniam paketui, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="5d4a2-123">**BatchNumber**: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="5d4a2-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="5d4a2-124">Grąžinto sąrašo dabartinio paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="5d4a2-125">Riba netaikoma vienam pradinio sąrašo elementui, jei ribos šaltinis viršija nustatytą ribą.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="5d4a2-126">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5d4a2-126">Example</span></span>

<span data-ttu-id="5d4a2-127">Tolesnėje iliustracijoje parodytas elektroninis ataskaitų (ER) formatas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="5d4a2-128">Tolesnėje iliustracijoje parodyti formatui naudojami duomenų šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="5d4a2-129">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas formatas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="5d4a2-130">Šiuo atveju išeiga yra standartinis prekių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="5d4a2-131">Toliau pateiktose iliustracijose rodomas tas pats formatas, pakoreguotas norint pateikti prekių sąrašą paketais, jei viename pakete turi būti prekės, o bendrasis svoris negali viršyti ribos 9.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="5d4a2-132">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas pakoreguotas formatas.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="5d4a2-133">Riba nėra taikoma paskutinei pradinio sąrašo prekei, nes ribos šaltinio (**svorio**) reikšmė (**11**) viršija nustatytą ribą (**9**).</span><span class="sxs-lookup"><span data-stu-id="5d4a2-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="5d4a2-134">Norėdami ignoruoti antrinius sąrašus generuojant ataskaitą, pagal poreikį naudokite funkciją `WHERE` arba atitinkamo formato elemento išraišką **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="5d4a2-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d4a2-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5d4a2-135">Additional resources</span></span>

[<span data-ttu-id="5d4a2-136">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="5d4a2-136">List functions</span></span>](er-functions-category-list.md)
