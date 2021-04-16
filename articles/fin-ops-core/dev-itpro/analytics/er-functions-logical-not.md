---
title: NOT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NOT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751724"
---
# <a name="not-er-function"></a><span data-ttu-id="1bb73-103">NOT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1bb73-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bb73-104">`NOT` funkcija grąžina nurodytos sąlygos atvirkštinės reikšmės loginę reikšmę kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1bb73-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb73-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1bb73-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="1bb73-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1bb73-106">Arguments</span></span>

<span data-ttu-id="1bb73-107">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="1bb73-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="1bb73-108">Tinkama sąlyginė išraiška, kuri turi būti atvirkščiai perdaryta.</span><span class="sxs-lookup"><span data-stu-id="1bb73-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="1bb73-109">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="1bb73-109">Return values</span></span>

<span data-ttu-id="1bb73-110">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="1bb73-110">*Boolean*</span></span>

<span data-ttu-id="1bb73-111">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1bb73-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="1bb73-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1bb73-112">Example</span></span>

<span data-ttu-id="1bb73-113">`NOT (TRUE)` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="1bb73-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bb73-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1bb73-114">Additional resources</span></span>

[<span data-ttu-id="1bb73-115">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="1bb73-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]