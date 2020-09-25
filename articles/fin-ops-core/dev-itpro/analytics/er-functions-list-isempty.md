---
title: ER ISEMPTY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ISEMPTY funkcija.
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745134"
---
# <a name="isempty-er-function"></a><span data-ttu-id="a403f-103">ER ISEMPTY funkcija</span><span class="sxs-lookup"><span data-stu-id="a403f-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a403f-104">Jei nurodytame sąraše nėra įrašų, `ISEMPTY` funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a403f-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="a403f-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a403f-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a403f-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="a403f-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="a403f-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="a403f-107">Arguments</span></span>

<span data-ttu-id="a403f-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="a403f-108">`list`: *Record list*</span></span>

<span data-ttu-id="a403f-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="a403f-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a403f-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="a403f-110">Return values</span></span>

<span data-ttu-id="a403f-111">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="a403f-111">*Boolean*</span></span>

<span data-ttu-id="a403f-112">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a403f-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a403f-113">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a403f-113">Example 1</span></span>

<span data-ttu-id="a403f-114">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `ISEMPTY(DS)` pateikia **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a403f-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a403f-115">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a403f-115">Example 2</span></span>

<span data-ttu-id="a403f-116">Reiškinys `ISEMPTY (SPLIT ("",1))` pateikia **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a403f-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a403f-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a403f-117">Additional resources</span></span>

[<span data-ttu-id="a403f-118">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="a403f-118">List functions</span></span>](er-functions-category-list.md)
