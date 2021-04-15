---
title: ER INDEX funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INDEX funkcija.
author: NickSelin
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
ms.openlocfilehash: 14f10359a3f20fb9d23639babce764b9ef64243d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750465"
---
# <a name="index-er-function"></a><span data-ttu-id="b5976-103">ER INDEX funkcija</span><span class="sxs-lookup"><span data-stu-id="b5976-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5976-104">`INDEX` funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą.</span><span class="sxs-lookup"><span data-stu-id="b5976-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="b5976-105">Jei indekse nėra nurodyto sąrašo įrašų intervalo, pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="b5976-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5976-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b5976-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="b5976-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b5976-107">Arguments</span></span>

<span data-ttu-id="b5976-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b5976-108">`list`: *Record list*</span></span>

<span data-ttu-id="b5976-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="b5976-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b5976-110">`index`: *Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="b5976-110">`index`: *Integer*</span></span>

<span data-ttu-id="b5976-111">Skaitinis indeksas, nurodantis norimo įrašo vietą nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="b5976-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="b5976-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b5976-112">Return values</span></span>

<span data-ttu-id="b5976-113">*Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="b5976-113">*Container (record)*</span></span>

<span data-ttu-id="b5976-114">Gauta įrašo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b5976-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b5976-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b5976-115">Example 1</span></span>

<span data-ttu-id="b5976-116">Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `DS.Value` pateikia šio įrašų sąrašo antrojo įrašo teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="b5976-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="b5976-117">Reiškinys `INDEX (SPLIT ("A|B|C", "|"), 2).Value` taip pat pateikia teksto reikšmę **„B“**.</span><span class="sxs-lookup"><span data-stu-id="b5976-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b5976-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b5976-118">Example 2</span></span>

<span data-ttu-id="b5976-119">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, vykdomas reiškinys `INDEX (SPLIT ("A|B|C", "|"), 4).Value` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="b5976-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5976-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b5976-120">Additional resources</span></span>

[<span data-ttu-id="b5976-121">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="b5976-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]