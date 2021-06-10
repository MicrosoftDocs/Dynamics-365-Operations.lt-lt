---
title: ER INDEX funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INDEX funkcija.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087756"
---
# <a name="index-er-function"></a><span data-ttu-id="cb681-103">ER INDEX funkcija</span><span class="sxs-lookup"><span data-stu-id="cb681-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb681-104">`INDEX` funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą.</span><span class="sxs-lookup"><span data-stu-id="cb681-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="cb681-105">Jei indekse nėra nurodyto sąrašo įrašų intervalo, pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="cb681-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb681-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="cb681-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="cb681-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="cb681-107">Arguments</span></span>

<span data-ttu-id="cb681-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="cb681-108">`list`: *Record list*</span></span>

<span data-ttu-id="cb681-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="cb681-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="cb681-110">`index`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="cb681-110">`index`: *Integer*</span></span>

<span data-ttu-id="cb681-111">Skaitinis indeksas, nurodantis norimo įrašo vietą nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="cb681-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="cb681-112">Kadangi šiai funkcijai naudojamas vienas numeravimas, nurodykite vertę **„1”**, kad būtų grąžinamas pirmas nurodyto sąrašo įrašas.</span><span class="sxs-lookup"><span data-stu-id="cb681-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb681-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="cb681-113">Return values</span></span>

<span data-ttu-id="cb681-114">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="cb681-114">*Container (record)*</span></span>

<span data-ttu-id="cb681-115">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cb681-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb681-116">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cb681-116">Example 1</span></span>

<span data-ttu-id="cb681-117">Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `DS.Value` pateikia šio įrašų sąrašo antrojo įrašo teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="cb681-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="cb681-118">Reiškinys `INDEX (SPLIT ("A|B|C", "|"), 2).Value` taip pat pateikia teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="cb681-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb681-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cb681-119">Example 2</span></span>

<span data-ttu-id="cb681-120">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, vykdomas reiškinys `INDEX (SPLIT ("A|B|C", "|"), 4).Value` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="cb681-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb681-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cb681-121">Additional resources</span></span>

[<span data-ttu-id="cb681-122">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="cb681-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
