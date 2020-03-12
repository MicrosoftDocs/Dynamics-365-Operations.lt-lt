---
title: MOD_97 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MOD_97 elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070534"
---
# <span data-ttu-id="d7ee6-103"><a name="MOD_97">MOD_97 ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="d7ee6-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7ee6-104">`MOD_97` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ee6-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="d7ee6-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d7ee6-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d7ee6-106">Arguments</span></span>

<span data-ttu-id="d7ee6-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d7ee6-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d7ee6-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7ee6-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="d7ee6-109">Return values</span></span>

<span data-ttu-id="d7ee6-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d7ee6-110">*String*</span></span>

<span data-ttu-id="d7ee6-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d7ee6-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d7ee6-112">Example</span></span>

<span data-ttu-id="d7ee6-113">`MOD_97 ("VEND-200002")` grąžina **„20000285“**.</span><span class="sxs-lookup"><span data-stu-id="d7ee6-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7ee6-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d7ee6-114">Additional resources</span></span>

[<span data-ttu-id="d7ee6-115">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="d7ee6-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
