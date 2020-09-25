---
title: UPPER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama UPPER elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744340"
---
# <a name="upper-er-function"></a><span data-ttu-id="095d6-103">UPPER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="095d6-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="095d6-104">`UPPER` funkcija pateikia nurodytą teksto eilutę kaip *Eilutės* reikšmę, kai ji buvo konvertuota į didžiąsias raides.</span><span class="sxs-lookup"><span data-stu-id="095d6-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="095d6-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="095d6-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="095d6-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="095d6-106">Arguments</span></span>

<span data-ttu-id="095d6-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="095d6-107">`text`: *String*</span></span>

<span data-ttu-id="095d6-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="095d6-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="095d6-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="095d6-109">Return values</span></span>

<span data-ttu-id="095d6-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="095d6-110">*String*</span></span>

<span data-ttu-id="095d6-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="095d6-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="095d6-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="095d6-112">Example</span></span>

<span data-ttu-id="095d6-113">`UPPER ("Sample")` grąžina **„PAVYZDYS“**.</span><span class="sxs-lookup"><span data-stu-id="095d6-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="095d6-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="095d6-114">Additional resources</span></span>

[<span data-ttu-id="095d6-115">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="095d6-115">Text functions</span></span>](er-functions-category-text.md)
