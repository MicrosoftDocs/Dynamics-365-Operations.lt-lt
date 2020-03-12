---
title: LEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama LEFT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041129"
---
# <span data-ttu-id="e2d12-103"><a name="LEFT">LEFT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="e2d12-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2d12-104">`LEFT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pradžios.</span><span class="sxs-lookup"><span data-stu-id="e2d12-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d12-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="e2d12-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="e2d12-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="e2d12-106">Arguments</span></span>

<span data-ttu-id="e2d12-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e2d12-107">`text`: *String*</span></span>

<span data-ttu-id="e2d12-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="e2d12-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="e2d12-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="e2d12-109">`number`: *Integer*</span></span>

<span data-ttu-id="e2d12-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pradžios, skaičius.</span><span class="sxs-lookup"><span data-stu-id="e2d12-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2d12-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="e2d12-111">Return values</span></span>

<span data-ttu-id="e2d12-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="e2d12-112">*String*</span></span>

<span data-ttu-id="e2d12-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e2d12-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e2d12-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e2d12-114">Example</span></span>

<span data-ttu-id="e2d12-115">`LEFT ("Sample", 3)` grąžina **„Pavyz“**.</span><span class="sxs-lookup"><span data-stu-id="e2d12-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2d12-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e2d12-116">Additional resources</span></span>

[<span data-ttu-id="e2d12-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="e2d12-117">Text functions</span></span>](er-functions-category-text.md)
