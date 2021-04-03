---
title: RIGHT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama RIGHT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570245"
---
# <a name="right-er-function"></a><span data-ttu-id="89084-103">RIGHT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="89084-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89084-104">`RIGHT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pabaigos.</span><span class="sxs-lookup"><span data-stu-id="89084-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="89084-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="89084-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="89084-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="89084-106">Arguments</span></span>

<span data-ttu-id="89084-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="89084-107">`text`: *String*</span></span>

<span data-ttu-id="89084-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="89084-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="89084-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="89084-109">`number`: *Integer*</span></span>

<span data-ttu-id="89084-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pabaigos, skaičius.</span><span class="sxs-lookup"><span data-stu-id="89084-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="89084-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="89084-111">Return values</span></span>

<span data-ttu-id="89084-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="89084-112">*String*</span></span>

<span data-ttu-id="89084-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="89084-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="89084-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="89084-114">Example</span></span>

<span data-ttu-id="89084-115">`RIGHT ("Sample", 3)` grąžina **„dys“**.</span><span class="sxs-lookup"><span data-stu-id="89084-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89084-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="89084-116">Additional resources</span></span>

[<span data-ttu-id="89084-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="89084-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]