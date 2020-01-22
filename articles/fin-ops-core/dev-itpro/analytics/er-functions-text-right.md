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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916734"
---
# <span data-ttu-id="668a7-103"><a name="RIGHT">RIGHT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="668a7-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="668a7-104">`RIGHT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pabaigos.</span><span class="sxs-lookup"><span data-stu-id="668a7-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="668a7-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="668a7-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="668a7-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="668a7-106">Arguments</span></span>

<span data-ttu-id="668a7-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="668a7-107">`text`: *String*</span></span>

<span data-ttu-id="668a7-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="668a7-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="668a7-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="668a7-109">`number`: *Integer*</span></span>

<span data-ttu-id="668a7-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pabaigos, skaičius.</span><span class="sxs-lookup"><span data-stu-id="668a7-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="668a7-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="668a7-111">Return values</span></span>

<span data-ttu-id="668a7-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="668a7-112">*String*</span></span>

<span data-ttu-id="668a7-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="668a7-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="668a7-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="668a7-114">Example</span></span>

<span data-ttu-id="668a7-115">`RIGHT ("Sample", 3)` grąžina **„dys“**.</span><span class="sxs-lookup"><span data-stu-id="668a7-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="668a7-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="668a7-116">Additional resources</span></span>

[<span data-ttu-id="668a7-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="668a7-117">Text functions</span></span>](er-functions-category-text.md)
