---
title: NOT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NOT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 9b55b3d8930ece7e2f2925579821ca88749801f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565885"
---
# <a name="not-er-function"></a><span data-ttu-id="85099-103">NOT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="85099-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85099-104">`NOT` funkcija grąžina nurodytos sąlygos atvirkštinės reikšmės loginę reikšmę kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85099-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="85099-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="85099-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="85099-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="85099-106">Arguments</span></span>

<span data-ttu-id="85099-107">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="85099-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="85099-108">Tinkama sąlyginė išraiška, kuri turi būti atvirkščiai perdaryta.</span><span class="sxs-lookup"><span data-stu-id="85099-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="85099-109">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="85099-109">Return values</span></span>

<span data-ttu-id="85099-110">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="85099-110">*Boolean*</span></span>

<span data-ttu-id="85099-111">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="85099-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="85099-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="85099-112">Example</span></span>

<span data-ttu-id="85099-113">`NOT (TRUE)` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="85099-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85099-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="85099-114">Additional resources</span></span>

[<span data-ttu-id="85099-115">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="85099-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]