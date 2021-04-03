---
title: POWER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama POWER elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9c45e7f9b47a3f0ff4445b1dd160def0ada3a56e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570427"
---
# <a name="power-er-function"></a><span data-ttu-id="16df7-103">POWER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="16df7-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16df7-104">`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="16df7-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="16df7-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="16df7-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="16df7-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="16df7-106">Arguments</span></span>

<span data-ttu-id="16df7-107">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="16df7-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="16df7-108">Skaitinė reikšmė, kurią reikia pakelti nurodytu laipsniu.</span><span class="sxs-lookup"><span data-stu-id="16df7-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="16df7-109">`power`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="16df7-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="16df7-110">Skaitinė reikšmė, nurodanti konkretų laipsnį.</span><span class="sxs-lookup"><span data-stu-id="16df7-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="16df7-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="16df7-111">Return values</span></span>

<span data-ttu-id="16df7-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="16df7-112">*Real*</span></span>

<span data-ttu-id="16df7-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="16df7-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="16df7-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="16df7-114">Example 1</span></span>

<span data-ttu-id="16df7-115">`POWER (10, 2)` grąžina **100**.</span><span class="sxs-lookup"><span data-stu-id="16df7-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="16df7-116">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="16df7-116">Example 2</span></span>

<span data-ttu-id="16df7-117">`POWER (4, 0.5)` grąžina **2**.</span><span class="sxs-lookup"><span data-stu-id="16df7-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16df7-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="16df7-118">Additional resources</span></span>

[<span data-ttu-id="16df7-119">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="16df7-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]