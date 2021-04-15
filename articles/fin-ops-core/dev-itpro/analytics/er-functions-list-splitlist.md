---
title: SPLITLIST ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama SPLITLIST elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 03/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745574"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="9515e-103">SPLITLIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9515e-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9515e-104">`SPLITLIST` funkcija skaido nurodytą sąrašą į antrinius sąrašus (arba į paketus), iš kurių kiekviename būtų nurodytas įrašų skaičius.</span><span class="sxs-lookup"><span data-stu-id="9515e-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="9515e-105">Tada grąžinamas rezultatas kaip nauja *Įrašų sąrašo* reikšmė, kurią sudaro paketai.</span><span class="sxs-lookup"><span data-stu-id="9515e-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9515e-106">Sintaksė 1</span><span class="sxs-lookup"><span data-stu-id="9515e-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="9515e-107">Sintaksė 2</span><span class="sxs-lookup"><span data-stu-id="9515e-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="9515e-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9515e-108">Arguments</span></span>

<span data-ttu-id="9515e-109">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9515e-109">`list`: *Record list*</span></span>

<span data-ttu-id="9515e-110">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="9515e-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9515e-111">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="9515e-111">`number`: *Integer*</span></span>

<span data-ttu-id="9515e-112">Didžiausias įrašų skaičius vienam paketui.</span><span class="sxs-lookup"><span data-stu-id="9515e-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="9515e-113">`on-demand reading flag`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="9515e-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="9515e-114">*Boolean* logikos reikšmė, nurodanti, ar subsaplankių elementai turi būti generuojami pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="9515e-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="9515e-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="9515e-115">Return values</span></span>

<span data-ttu-id="9515e-116">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9515e-116">*Record list*</span></span>

<span data-ttu-id="9515e-117">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9515e-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9515e-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9515e-118">Usage notes</span></span>

<span data-ttu-id="9515e-119">Grąžintame paketų sąraše yra šių elementų:</span><span class="sxs-lookup"><span data-stu-id="9515e-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="9515e-120">**Vertė:** *Sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9515e-120">**Value:** *List*</span></span>

    <span data-ttu-id="9515e-121">Įrašų, priklausančių dabartiniam paketui, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9515e-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="9515e-122">**BatchNumber:** *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="9515e-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="9515e-123">Grąžinto sąrašo dabartinio paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="9515e-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="9515e-124">Kai nustatyta skaitymo pagal poreikį žymė Teisinga, paantraštiniai sąrašai generuojami pagal užklausą, kuri leidžia sumažinti atminties suvartojimą, bet gali padidinti našumą, jei elementai nenaudojami **nuosekliai**.</span><span class="sxs-lookup"><span data-stu-id="9515e-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="9515e-125">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9515e-125">Example</span></span>

<span data-ttu-id="9515e-126">Tolesnėje iliustracijoje duomenų šaltinis **Eilutės** sukurtas kaip įrašų sąrašas, turintis tris įrašus.</span><span class="sxs-lookup"><span data-stu-id="9515e-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="9515e-127">Šis sąrašas suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų.</span><span class="sxs-lookup"><span data-stu-id="9515e-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="9515e-128">Tolesnėje iliustracijoje parodytas sukurtas formato maketas.</span><span class="sxs-lookup"><span data-stu-id="9515e-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="9515e-129">Šiame formato makete sukuriami susiejimai su duomenų šaltiniu **Eilutės**, siekiant generuoti išeigą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="9515e-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="9515e-130">Ši išeiga pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus.</span><span class="sxs-lookup"><span data-stu-id="9515e-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="9515e-131">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="9515e-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="9515e-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9515e-132">Additional resources</span></span>

[<span data-ttu-id="9515e-133">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9515e-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
