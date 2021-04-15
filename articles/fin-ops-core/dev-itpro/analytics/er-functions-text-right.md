---
title: RIGHT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama RIGHT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746128"
---
# <a name="right-er-function"></a><span data-ttu-id="14968-103">RIGHT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="14968-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14968-104">`RIGHT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pabaigos.</span><span class="sxs-lookup"><span data-stu-id="14968-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="14968-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="14968-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="14968-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="14968-106">Arguments</span></span>

<span data-ttu-id="14968-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="14968-107">`text`: *String*</span></span>

<span data-ttu-id="14968-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="14968-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="14968-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="14968-109">`number`: *Integer*</span></span>

<span data-ttu-id="14968-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pabaigos, skaičius.</span><span class="sxs-lookup"><span data-stu-id="14968-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="14968-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="14968-111">Return values</span></span>

<span data-ttu-id="14968-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="14968-112">*String*</span></span>

<span data-ttu-id="14968-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="14968-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="14968-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="14968-114">Example</span></span>

<span data-ttu-id="14968-115">`RIGHT ("Sample", 3)` grąžina **„dys“**.</span><span class="sxs-lookup"><span data-stu-id="14968-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14968-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="14968-116">Additional resources</span></span>

[<span data-ttu-id="14968-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="14968-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]