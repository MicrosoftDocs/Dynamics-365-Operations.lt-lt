---
title: SPLITLIST ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama SPLITLIST elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559143"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="03898-103">SPLITLIST ER funkcija</span><span class="sxs-lookup"><span data-stu-id="03898-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03898-104">`SPLITLIST` funkcija skaido nurodytą sąrašą į antrinius sąrašus (arba į paketus), iš kurių kiekviename būtų nurodytas įrašų skaičius.</span><span class="sxs-lookup"><span data-stu-id="03898-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="03898-105">Tada grąžinamas rezultatas kaip nauja *Įrašų sąrašo* reikšmė, kurią sudaro paketai.</span><span class="sxs-lookup"><span data-stu-id="03898-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="03898-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="03898-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="03898-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="03898-107">Arguments</span></span>

<span data-ttu-id="03898-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="03898-108">`list`: *Record list*</span></span>

<span data-ttu-id="03898-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="03898-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="03898-110">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="03898-110">`number`: *Integer*</span></span>

<span data-ttu-id="03898-111">Didžiausias įrašų skaičius vienam paketui.</span><span class="sxs-lookup"><span data-stu-id="03898-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="03898-112">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="03898-112">Return values</span></span>

<span data-ttu-id="03898-113">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="03898-113">*Record list*</span></span>

<span data-ttu-id="03898-114">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="03898-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="03898-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="03898-115">Usage notes</span></span>

<span data-ttu-id="03898-116">Grąžintame paketų sąraše yra šių elementų:</span><span class="sxs-lookup"><span data-stu-id="03898-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="03898-117">**Vertė:** *Sąrašas*</span><span class="sxs-lookup"><span data-stu-id="03898-117">**Value:** *List*</span></span>

    <span data-ttu-id="03898-118">Įrašų, priklausančių dabartiniam paketui, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="03898-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="03898-119">**BatchNumber:** *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="03898-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="03898-120">Grąžinto sąrašo dabartinio paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="03898-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="03898-121">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="03898-121">Example</span></span>

<span data-ttu-id="03898-122">Tolesnėje iliustracijoje duomenų šaltinis **Eilutės** sukurtas kaip įrašų sąrašas, turintis tris įrašus.</span><span class="sxs-lookup"><span data-stu-id="03898-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="03898-123">Šis sąrašas suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų.</span><span class="sxs-lookup"><span data-stu-id="03898-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="03898-124">Tolesnėje iliustracijoje parodytas sukurtas formato maketas.</span><span class="sxs-lookup"><span data-stu-id="03898-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="03898-125">Šiame formato makete sukuriami susiejimai su duomenų šaltiniu **Eilutės**, siekiant generuoti išeigą XML formatu.</span><span class="sxs-lookup"><span data-stu-id="03898-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="03898-126">Ši išeiga pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus.</span><span class="sxs-lookup"><span data-stu-id="03898-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="03898-127">Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</span><span class="sxs-lookup"><span data-stu-id="03898-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="03898-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="03898-128">Additional resources</span></span>

[<span data-ttu-id="03898-129">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="03898-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]