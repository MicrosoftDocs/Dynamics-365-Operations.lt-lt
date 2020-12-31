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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3923126060963122634d90c2ba8a380f534e9178
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686767"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="2dfa1-103">CURCREDREF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="2dfa1-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dfa1-104">`CURCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą pagal nurodyto sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="2dfa1-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dfa1-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2dfa1-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="2dfa1-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2dfa1-106">Arguments</span></span>

<span data-ttu-id="2dfa1-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="2dfa1-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="2dfa1-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="2dfa1-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2dfa1-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="2dfa1-109">Return values</span></span>

<span data-ttu-id="2dfa1-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="2dfa1-110">*String*</span></span>

<span data-ttu-id="2dfa1-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2dfa1-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2dfa1-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2dfa1-112">Example</span></span>

<span data-ttu-id="2dfa1-113">`CURCredRef ("VEND-200002")` grąžina **„2200002“**.</span><span class="sxs-lookup"><span data-stu-id="2dfa1-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dfa1-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2dfa1-114">Additional resources</span></span>

[<span data-ttu-id="2dfa1-115">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="2dfa1-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
