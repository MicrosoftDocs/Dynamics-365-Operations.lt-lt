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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745183"
---
# <a name="index-er-function"></a><span data-ttu-id="0af39-103">ER INDEX funkcija</span><span class="sxs-lookup"><span data-stu-id="0af39-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0af39-104">`INDEX` funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą.</span><span class="sxs-lookup"><span data-stu-id="0af39-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="0af39-105">Jei indekse nėra nurodyto sąrašo įrašų intervalo, pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="0af39-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af39-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="0af39-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="0af39-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="0af39-107">Arguments</span></span>

<span data-ttu-id="0af39-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="0af39-108">`list`: *Record list*</span></span>

<span data-ttu-id="0af39-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="0af39-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0af39-110">`index`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="0af39-110">`index`: *Integer*</span></span>

<span data-ttu-id="0af39-111">Skaitinis indeksas, nurodantis norimo įrašo vietą nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="0af39-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="0af39-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="0af39-112">Return values</span></span>

<span data-ttu-id="0af39-113">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="0af39-113">*Container (record)*</span></span>

<span data-ttu-id="0af39-114">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0af39-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0af39-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0af39-115">Example 1</span></span>

<span data-ttu-id="0af39-116">Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `DS.Value` pateikia šio įrašų sąrašo antrojo įrašo teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="0af39-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="0af39-117">Reiškinys `INDEX (SPLIT ("A|B|C", "|"), 2).Value` taip pat pateikia teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="0af39-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0af39-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0af39-118">Example 2</span></span>

<span data-ttu-id="0af39-119">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, vykdomas reiškinys `INDEX (SPLIT ("A|B|C", "|"), 4).Value` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="0af39-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0af39-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0af39-120">Additional resources</span></span>

[<span data-ttu-id="0af39-121">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="0af39-121">List functions</span></span>](er-functions-category-list.md)
