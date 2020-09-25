---
title: ER INTVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INTVALUE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743644"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="e409d-103">ER INTVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="e409d-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e409d-104">`INTVALUE` funkcija pateikia *Int* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="e409d-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e409d-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="e409d-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="e409d-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="e409d-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="e409d-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="e409d-107">Arguments</span></span>

<span data-ttu-id="e409d-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e409d-108">`text`: *String*</span></span>

<span data-ttu-id="e409d-109">Teksto reikšmė, kurią reikia konvertuoti į *Int* skaičių.</span><span class="sxs-lookup"><span data-stu-id="e409d-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="e409d-110">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="e409d-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="e409d-111">Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int* skaičių.</span><span class="sxs-lookup"><span data-stu-id="e409d-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e409d-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="e409d-112">Return values</span></span>

<span data-ttu-id="e409d-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="e409d-113">*Int*</span></span>

<span data-ttu-id="e409d-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e409d-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e409d-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="e409d-115">Usage notes</span></span>

<span data-ttu-id="e409d-116">Visi skaičiai po kablelio pašalinami.</span><span class="sxs-lookup"><span data-stu-id="e409d-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="e409d-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e409d-117">Example 1</span></span>

<span data-ttu-id="e409d-118">`INTVALUE ("100.77")` pateikia *Int* reikšmę **100**.</span><span class="sxs-lookup"><span data-stu-id="e409d-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e409d-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e409d-119">Example 2</span></span>

<span data-ttu-id="e409d-120">`INTVALUE (-100.77)` pateikia *Int* reikšmę **–100**.</span><span class="sxs-lookup"><span data-stu-id="e409d-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e409d-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e409d-121">Additional resources</span></span>

[<span data-ttu-id="e409d-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="e409d-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
