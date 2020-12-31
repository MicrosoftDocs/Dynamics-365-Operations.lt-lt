---
title: ER VALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip modulio Elektroninės ataskaitos (ER) VALUE funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681213"
---
# <a name="value-er-function"></a><span data-ttu-id="56e56-103">ER VALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="56e56-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56e56-104">`VALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="56e56-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e56-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="56e56-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="56e56-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="56e56-106">Arguments</span></span>

<span data-ttu-id="56e56-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="56e56-107">`text`: *String*</span></span>

<span data-ttu-id="56e56-108">Eilutės reikšmė, kurią reikia konvertuoti į skaitinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56e56-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="56e56-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="56e56-109">Return values</span></span>

<span data-ttu-id="56e56-110">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="56e56-110">*Real*</span></span>

<span data-ttu-id="56e56-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="56e56-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="56e56-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="56e56-112">Usage notes</span></span>

<span data-ttu-id="56e56-113">Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas.</span><span class="sxs-lookup"><span data-stu-id="56e56-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="56e56-114">Jei nurodytoje eilutėje yra kitų neskaitinių simbolių, vykdant pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="56e56-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="56e56-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="56e56-115">Example 1</span></span>

<span data-ttu-id="56e56-116">`VALUE ("1 234,56")` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="56e56-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="56e56-117">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="56e56-117">Example 2</span></span>

<span data-ttu-id="56e56-118">`VALUE ("1234,56")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="56e56-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56e56-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="56e56-119">Additional resources</span></span>

[<span data-ttu-id="56e56-120">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="56e56-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
