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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745518"
---
# <a name="value-er-function"></a><span data-ttu-id="ead72-103">ER VALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="ead72-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ead72-104">`VALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos eilutės.</span><span class="sxs-lookup"><span data-stu-id="ead72-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead72-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="ead72-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="ead72-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="ead72-106">Arguments</span></span>

<span data-ttu-id="ead72-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ead72-107">`text`: *String*</span></span>

<span data-ttu-id="ead72-108">Eilutės reikšmė, kurią reikia konvertuoti į skaitinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ead72-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="ead72-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ead72-109">Return values</span></span>

<span data-ttu-id="ead72-110">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="ead72-110">*Real*</span></span>

<span data-ttu-id="ead72-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ead72-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ead72-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="ead72-112">Usage notes</span></span>

<span data-ttu-id="ead72-113">Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas.</span><span class="sxs-lookup"><span data-stu-id="ead72-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="ead72-114">Jei nurodytoje eilutėje yra kitų neskaitinių simbolių, vykdant pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="ead72-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="ead72-115">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ead72-115">Example 1</span></span>

<span data-ttu-id="ead72-116">`VALUE ("1 234,56")` pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="ead72-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="ead72-117">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ead72-117">Example 2</span></span>

<span data-ttu-id="ead72-118">`VALUE ("1234,56")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="ead72-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ead72-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ead72-119">Additional resources</span></span>

[<span data-ttu-id="ead72-120">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="ead72-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
