---
title: ER INDEX funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INDEX funkcija.
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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042072"
---
# <span data-ttu-id="9994c-103"><a name="INDEX">ER INDEX funkcija</a></span><span class="sxs-lookup"><span data-stu-id="9994c-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9994c-104">`INDEX` funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą.</span><span class="sxs-lookup"><span data-stu-id="9994c-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="9994c-105">Jei indekse nėra nurodyto sąrašo įrašų intervalo, pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="9994c-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="9994c-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9994c-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="9994c-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9994c-107">Arguments</span></span>

<span data-ttu-id="9994c-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="9994c-108">`list`: *Record list*</span></span>

<span data-ttu-id="9994c-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="9994c-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="9994c-110">`index`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="9994c-110">`index`: *Integer*</span></span>

<span data-ttu-id="9994c-111">Skaitinis indeksas, nurodantis norimo įrašo vietą nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="9994c-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="9994c-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="9994c-112">Return values</span></span>

<span data-ttu-id="9994c-113">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="9994c-113">*Container (record)*</span></span>

<span data-ttu-id="9994c-114">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9994c-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9994c-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9994c-115">Example 1</span></span>

<span data-ttu-id="9994c-116">Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `DS.Value` pateikia šio įrašų sąrašo antrojo įrašo teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="9994c-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="9994c-117">Reiškinys `INDEX (SPLIT ("A|B|C", "|"), 2).Value` taip pat pateikia teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="9994c-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9994c-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9994c-118">Example 2</span></span>

<span data-ttu-id="9994c-119">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, vykdomas reiškinys `INDEX (SPLIT ("A|B|C", "|"), 4).Value` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="9994c-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9994c-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9994c-120">Additional resources</span></span>

[<span data-ttu-id="9994c-121">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="9994c-121">List functions</span></span>](er-functions-category-list.md)
