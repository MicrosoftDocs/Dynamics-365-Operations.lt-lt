---
title: ABS ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ABS elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917102"
---
# <span data-ttu-id="84e8b-103"><a name="ABS">ABS ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="84e8b-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84e8b-104">`ABS` funkcija grąžina nurodyto skaičiaus absoliučiąją reikšmę (modulį) kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="84e8b-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="84e8b-105">Kitaip tariant, grąžinamas skaičius be grotelių.</span><span class="sxs-lookup"><span data-stu-id="84e8b-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="84e8b-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="84e8b-106">Syntax</span></span>

```
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="84e8b-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="84e8b-107">Arguments</span></span>

<span data-ttu-id="84e8b-108">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="84e8b-108">`number`: *Real*</span></span>

<span data-ttu-id="84e8b-109">Skaitinė reikšmė, kurios modulį norite gauti.</span><span class="sxs-lookup"><span data-stu-id="84e8b-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="84e8b-110">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="84e8b-110">Return values</span></span>

<span data-ttu-id="84e8b-111">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="84e8b-111">*Real*</span></span>

<span data-ttu-id="84e8b-112">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="84e8b-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="84e8b-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="84e8b-113">Example</span></span>

<span data-ttu-id="84e8b-114">`ABS (-1)` grąžina **1**.</span><span class="sxs-lookup"><span data-stu-id="84e8b-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84e8b-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="84e8b-115">Additional resources</span></span>

[<span data-ttu-id="84e8b-116">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="84e8b-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
