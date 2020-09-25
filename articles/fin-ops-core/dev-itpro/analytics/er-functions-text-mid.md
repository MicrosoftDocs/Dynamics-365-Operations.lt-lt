---
title: MID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MID elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744724"
---
# <a name="mid-er-function"></a><span data-ttu-id="0e795-103">MID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="0e795-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e795-104">`MID` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradėdama nuo nurodytos vietos.</span><span class="sxs-lookup"><span data-stu-id="0e795-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e795-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="0e795-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="0e795-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="0e795-106">Arguments</span></span>

<span data-ttu-id="0e795-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="0e795-107">`text`: *String*</span></span>

<span data-ttu-id="0e795-108">*Eilutės* reikšmė, nurodanti tekstą, iš kurio grąžinami simboliai.</span><span class="sxs-lookup"><span data-stu-id="0e795-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="0e795-109">`starting position`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="0e795-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="0e795-110">*Sveikojo skaičiaus* reikšmė, nurodanti pirmojo simbolio, kuris turi būti grąžinamas iš nurodyto teksto, vietą.</span><span class="sxs-lookup"><span data-stu-id="0e795-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="0e795-111">`number of characters`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="0e795-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="0e795-112">*Sveikojo skaičiaus* reikšmė, nurodanti simbolių, kurie turi būti grąžinami pradedant nuo nurodytos pradžios vietos, skaičių.</span><span class="sxs-lookup"><span data-stu-id="0e795-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e795-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="0e795-113">Return values</span></span>

<span data-ttu-id="0e795-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="0e795-114">*String*</span></span>

<span data-ttu-id="0e795-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0e795-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0e795-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="0e795-116">Usage notes</span></span>

<span data-ttu-id="0e795-117">Jei argumento `starting position` reikšmė yra mažesnė už 0 (nulį), grąžinami simboliai skaičiuojami nuo pirmosios nurodytos eilutės vietos.</span><span class="sxs-lookup"><span data-stu-id="0e795-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="0e795-118">Jei argumento `starting position` reikšmė viršija nurodytos eilutės ilgį, grąžinama tuščia eilutė.</span><span class="sxs-lookup"><span data-stu-id="0e795-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="0e795-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0e795-119">Example</span></span>

<span data-ttu-id="0e795-120">`MID ("Sample", 2, 3)`grąžina **„amp“**.</span><span class="sxs-lookup"><span data-stu-id="0e795-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e795-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0e795-121">Additional resources</span></span>

[<span data-ttu-id="0e795-122">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="0e795-122">Text functions</span></span>](er-functions-category-text.md)
