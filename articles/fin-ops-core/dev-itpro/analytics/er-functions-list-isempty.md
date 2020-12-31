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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684888"
---
# <a name="isempty-er-function"></a><span data-ttu-id="b4282-103">ER ISEMPTY funkcija</span><span class="sxs-lookup"><span data-stu-id="b4282-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4282-104">Jei nurodytame sąraše nėra įrašų, `ISEMPTY` funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b4282-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="b4282-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b4282-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4282-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="b4282-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="b4282-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="b4282-107">Arguments</span></span>

<span data-ttu-id="b4282-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="b4282-108">`list`: *Record list*</span></span>

<span data-ttu-id="b4282-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="b4282-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b4282-110">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b4282-110">Return values</span></span>

<span data-ttu-id="b4282-111">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="b4282-111">*Boolean*</span></span>

<span data-ttu-id="b4282-112">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="b4282-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b4282-113">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b4282-113">Example 1</span></span>

<span data-ttu-id="b4282-114">Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `ISEMPTY(DS)` pateikia **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b4282-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b4282-115">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="b4282-115">Example 2</span></span>

<span data-ttu-id="b4282-116">Reiškinys `ISEMPTY (SPLIT ("",1))` pateikia **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b4282-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4282-117">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b4282-117">Additional resources</span></span>

[<span data-ttu-id="b4282-118">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="b4282-118">List functions</span></span>](er-functions-category-list.md)
