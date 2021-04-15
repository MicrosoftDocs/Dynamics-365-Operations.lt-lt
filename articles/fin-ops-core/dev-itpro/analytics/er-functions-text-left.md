---
title: LEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama LEFT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746344"
---
# <a name="left-er-function"></a><span data-ttu-id="75885-103">LEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="75885-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75885-104">`LEFT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pradžios.</span><span class="sxs-lookup"><span data-stu-id="75885-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="75885-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="75885-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="75885-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="75885-106">Arguments</span></span>

<span data-ttu-id="75885-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="75885-107">`text`: *String*</span></span>

<span data-ttu-id="75885-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="75885-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="75885-109">`number`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="75885-109">`number`: *Integer*</span></span>

<span data-ttu-id="75885-110">Simbolių, kuriuos reikia grąžinti iš pradinio teksto pradžios, skaičius.</span><span class="sxs-lookup"><span data-stu-id="75885-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="75885-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="75885-111">Return values</span></span>

<span data-ttu-id="75885-112">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="75885-112">*String*</span></span>

<span data-ttu-id="75885-113">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="75885-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="75885-114">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="75885-114">Example</span></span>

<span data-ttu-id="75885-115">`LEFT ("Sample", 3)` grąžina **„Pavyz“**.</span><span class="sxs-lookup"><span data-stu-id="75885-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75885-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="75885-116">Additional resources</span></span>

[<span data-ttu-id="75885-117">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="75885-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]