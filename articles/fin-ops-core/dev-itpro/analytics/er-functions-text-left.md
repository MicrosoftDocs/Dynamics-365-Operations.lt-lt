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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743788"
---
# <a name="left-er-function"></a><span data-ttu-id="39a23-103">LEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="39a23-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39a23-104">`LEFT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pradžios.</span><span class="sxs-lookup"><span data-stu-id="39a23-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a23-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="39a23-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="39a23-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="39a23-106">Arguments</span></span>

<span data-ttu-id="39a23-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="39a23-107">`text`: *String*</span></span>

<span data-ttu-id="39a23-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="39a23-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="39a23-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="39a23-109">`number`: *Integer*</span></span>

<span data-ttu-id="39a23-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pradžios, skaičius.</span><span class="sxs-lookup"><span data-stu-id="39a23-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="39a23-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="39a23-111">Return values</span></span>

<span data-ttu-id="39a23-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="39a23-112">*String*</span></span>

<span data-ttu-id="39a23-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="39a23-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="39a23-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="39a23-114">Example</span></span>

<span data-ttu-id="39a23-115">`LEFT ("Sample", 3)` grąžina **„Pavyz“**.</span><span class="sxs-lookup"><span data-stu-id="39a23-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39a23-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="39a23-116">Additional resources</span></span>

[<span data-ttu-id="39a23-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="39a23-117">Text functions</span></span>](er-functions-category-text.md)
