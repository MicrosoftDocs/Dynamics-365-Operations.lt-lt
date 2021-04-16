---
title: ER VALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip modulio Elektroninės ataskaitos (ER) VALUE funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752585"
---
# <a name="value-er-function"></a><span data-ttu-id="dc41e-103">ER VALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="dc41e-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc41e-104">`VALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="dc41e-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc41e-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="dc41e-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="dc41e-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="dc41e-106">Arguments</span></span>

<span data-ttu-id="dc41e-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="dc41e-107">`text`: *String*</span></span>

<span data-ttu-id="dc41e-108">Eilutės reikšmė, kurią reikia konvertuoti į skaitinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dc41e-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc41e-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="dc41e-109">Return values</span></span>

<span data-ttu-id="dc41e-110">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="dc41e-110">*Real*</span></span>

<span data-ttu-id="dc41e-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="dc41e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dc41e-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="dc41e-112">Usage notes</span></span>

<span data-ttu-id="dc41e-113">Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas.</span><span class="sxs-lookup"><span data-stu-id="dc41e-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="dc41e-114">Jei nurodytoje eilutėje yra kitų neskaitinių simbolių, vykdant pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="dc41e-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="dc41e-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="dc41e-115">Example 1</span></span>

<span data-ttu-id="dc41e-116">`VALUE ("1 234,56")` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="dc41e-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="dc41e-117">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="dc41e-117">Example 2</span></span>

<span data-ttu-id="dc41e-118">`VALUE ("1234,56")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="dc41e-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc41e-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dc41e-119">Additional resources</span></span>

[<span data-ttu-id="dc41e-120">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="dc41e-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]