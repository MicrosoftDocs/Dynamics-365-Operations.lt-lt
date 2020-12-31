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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685888"
---
# <a name="left-er-function"></a><span data-ttu-id="62f52-103">LEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="62f52-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62f52-104">`LEFT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pradžios.</span><span class="sxs-lookup"><span data-stu-id="62f52-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f52-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="62f52-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="62f52-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="62f52-106">Arguments</span></span>

<span data-ttu-id="62f52-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="62f52-107">`text`: *String*</span></span>

<span data-ttu-id="62f52-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="62f52-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="62f52-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="62f52-109">`number`: *Integer*</span></span>

<span data-ttu-id="62f52-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pradžios, skaičius.</span><span class="sxs-lookup"><span data-stu-id="62f52-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="62f52-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="62f52-111">Return values</span></span>

<span data-ttu-id="62f52-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="62f52-112">*String*</span></span>

<span data-ttu-id="62f52-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="62f52-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="62f52-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="62f52-114">Example</span></span>

<span data-ttu-id="62f52-115">`LEFT ("Sample", 3)` grąžina **„Pavyz“**.</span><span class="sxs-lookup"><span data-stu-id="62f52-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62f52-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="62f52-116">Additional resources</span></span>

[<span data-ttu-id="62f52-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="62f52-117">Text functions</span></span>](er-functions-category-text.md)
