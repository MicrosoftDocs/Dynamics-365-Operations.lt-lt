---
title: CURCREDREF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CURCREDREF elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 5633541b1c7e25a0cfb837c4679691506806421b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917010"
---
# <span data-ttu-id="1aef3-103"><a name="CURCREDREF">CURCREDREF ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="1aef3-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1aef3-104">`CURCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą pagal nurodyto sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1aef3-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aef3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1aef3-105">Syntax</span></span>

```
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="1aef3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1aef3-106">Arguments</span></span>

<span data-ttu-id="1aef3-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1aef3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="1aef3-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1aef3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1aef3-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="1aef3-109">Return values</span></span>

<span data-ttu-id="1aef3-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1aef3-110">*String*</span></span>

<span data-ttu-id="1aef3-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1aef3-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1aef3-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1aef3-112">Example</span></span>

<span data-ttu-id="1aef3-113">`CURCredRef ("VEND-200002")` grąžina **„2200002“**.</span><span class="sxs-lookup"><span data-stu-id="1aef3-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1aef3-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1aef3-114">Additional resources</span></span>

[<span data-ttu-id="1aef3-115">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="1aef3-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
