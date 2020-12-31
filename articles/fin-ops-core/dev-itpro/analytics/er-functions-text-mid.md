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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d8a7d2e9beb0fc8724d26de0acaf1d61e3834c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680295"
---
# <a name="mid-er-function"></a><span data-ttu-id="db496-103">MID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="db496-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db496-104">`MID` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradėdama nuo nurodytos vietos.</span><span class="sxs-lookup"><span data-stu-id="db496-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="db496-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="db496-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="db496-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="db496-106">Arguments</span></span>

<span data-ttu-id="db496-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="db496-107">`text`: *String*</span></span>

<span data-ttu-id="db496-108">*Eilutės* reikšmė, nurodanti tekstą, iš kurio grąžinami simboliai.</span><span class="sxs-lookup"><span data-stu-id="db496-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="db496-109">`starting position`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="db496-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="db496-110">*Sveikojo skaičiaus* reikšmė, nurodanti pirmojo simbolio, kuris turi būti grąžinamas iš nurodyto teksto, vietą.</span><span class="sxs-lookup"><span data-stu-id="db496-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="db496-111">`number of characters`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="db496-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="db496-112">*Sveikojo skaičiaus* reikšmė, nurodanti simbolių, kurie turi būti grąžinami pradedant nuo nurodytos pradžios vietos, skaičių.</span><span class="sxs-lookup"><span data-stu-id="db496-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="db496-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="db496-113">Return values</span></span>

<span data-ttu-id="db496-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="db496-114">*String*</span></span>

<span data-ttu-id="db496-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="db496-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="db496-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="db496-116">Usage notes</span></span>

<span data-ttu-id="db496-117">Jei argumento `starting position` reikšmė yra mažesnė už 0 (nulį), grąžinami simboliai skaičiuojami nuo pirmosios nurodytos eilutės vietos.</span><span class="sxs-lookup"><span data-stu-id="db496-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="db496-118">Jei argumento `starting position` reikšmė viršija nurodytos eilutės ilgį, grąžinama tuščia eilutė.</span><span class="sxs-lookup"><span data-stu-id="db496-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="db496-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="db496-119">Example</span></span>

<span data-ttu-id="db496-120">`MID ("Sample", 2, 3)`grąžina **„amp“**.</span><span class="sxs-lookup"><span data-stu-id="db496-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db496-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="db496-121">Additional resources</span></span>

[<span data-ttu-id="db496-122">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="db496-122">Text functions</span></span>](er-functions-category-text.md)
