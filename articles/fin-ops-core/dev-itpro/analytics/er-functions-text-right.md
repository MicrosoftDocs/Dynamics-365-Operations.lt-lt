---
title: RIGHT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama RIGHT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040876"
---
# <span data-ttu-id="09c36-103"><a name="RIGHT">RIGHT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="09c36-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09c36-104">`RIGHT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pabaigos.</span><span class="sxs-lookup"><span data-stu-id="09c36-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c36-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="09c36-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="09c36-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="09c36-106">Arguments</span></span>

<span data-ttu-id="09c36-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="09c36-107">`text`: *String*</span></span>

<span data-ttu-id="09c36-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="09c36-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="09c36-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="09c36-109">`number`: *Integer*</span></span>

<span data-ttu-id="09c36-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pabaigos, skaičius.</span><span class="sxs-lookup"><span data-stu-id="09c36-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="09c36-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="09c36-111">Return values</span></span>

<span data-ttu-id="09c36-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="09c36-112">*String*</span></span>

<span data-ttu-id="09c36-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="09c36-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="09c36-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="09c36-114">Example</span></span>

<span data-ttu-id="09c36-115">`RIGHT ("Sample", 3)` grąžina **„dys“**.</span><span class="sxs-lookup"><span data-stu-id="09c36-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09c36-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="09c36-116">Additional resources</span></span>

[<span data-ttu-id="09c36-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="09c36-117">Text functions</span></span>](er-functions-category-text.md)
