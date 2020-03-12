---
title: NOT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NOT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041727"
---
# <span data-ttu-id="6746d-103"><a name="NOT">NOT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="6746d-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6746d-104">`NOT` funkcija grąžina nurodytos sąlygos atvirkštinės reikšmės loginę reikšmę kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6746d-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6746d-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6746d-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="6746d-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6746d-106">Arguments</span></span>

<span data-ttu-id="6746d-107">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="6746d-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="6746d-108">Tinkama sąlyginė išraiška, kuri turi būti atvirkščiai perdaryta.</span><span class="sxs-lookup"><span data-stu-id="6746d-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="6746d-109">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="6746d-109">Return values</span></span>

<span data-ttu-id="6746d-110">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="6746d-110">*Boolean*</span></span>

<span data-ttu-id="6746d-111">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6746d-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="6746d-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6746d-112">Example</span></span>

<span data-ttu-id="6746d-113">`NOT (TRUE)` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="6746d-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6746d-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6746d-114">Additional resources</span></span>

[<span data-ttu-id="6746d-115">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="6746d-115">Logical functions</span></span>](er-functions-category-logical.md)
