---
title: MID ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MID elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562738"
---
# <a name="mid-er-function"></a><span data-ttu-id="40fa7-103">MID ER funkcija</span><span class="sxs-lookup"><span data-stu-id="40fa7-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40fa7-104">`MID` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės, pradėdama nuo nurodytos vietos.</span><span class="sxs-lookup"><span data-stu-id="40fa7-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="40fa7-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="40fa7-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="40fa7-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="40fa7-106">Arguments</span></span>

<span data-ttu-id="40fa7-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="40fa7-107">`text`: *String*</span></span>

<span data-ttu-id="40fa7-108">*Eilutės* reikšmė, nurodanti tekstą, iš kurio grąžinami simboliai.</span><span class="sxs-lookup"><span data-stu-id="40fa7-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="40fa7-109">`starting position`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="40fa7-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="40fa7-110">*Sveikojo skaičiaus* reikšmė, nurodanti pirmojo simbolio, kuris turi būti grąžinamas iš nurodyto teksto, vietą.</span><span class="sxs-lookup"><span data-stu-id="40fa7-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="40fa7-111">`number of characters`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="40fa7-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="40fa7-112">*Sveikojo skaičiaus* reikšmė, nurodanti simbolių, kurie turi būti grąžinami pradedant nuo nurodytos pradžios vietos, skaičių.</span><span class="sxs-lookup"><span data-stu-id="40fa7-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="40fa7-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="40fa7-113">Return values</span></span>

<span data-ttu-id="40fa7-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="40fa7-114">*String*</span></span>

<span data-ttu-id="40fa7-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="40fa7-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="40fa7-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="40fa7-116">Usage notes</span></span>

<span data-ttu-id="40fa7-117">Jei argumento `starting position` reikšmė yra mažesnė už 0 (nulį), grąžinami simboliai skaičiuojami nuo pirmosios nurodytos eilutės vietos.</span><span class="sxs-lookup"><span data-stu-id="40fa7-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="40fa7-118">Jei argumento `starting position` reikšmė viršija nurodytos eilutės ilgį, grąžinama tuščia eilutė.</span><span class="sxs-lookup"><span data-stu-id="40fa7-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="40fa7-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="40fa7-119">Example</span></span>

<span data-ttu-id="40fa7-120">`MID ("Sample", 2, 3)`grąžina **„amp“**.</span><span class="sxs-lookup"><span data-stu-id="40fa7-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40fa7-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="40fa7-121">Additional resources</span></span>

[<span data-ttu-id="40fa7-122">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="40fa7-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]