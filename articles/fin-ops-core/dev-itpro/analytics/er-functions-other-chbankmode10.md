---
title: CH_BANK_MOD_10 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CH_BANK_MOD_10 elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915883"
---
# <span data-ttu-id="1321f-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="1321f-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1321f-104">`CH_BANK_MOD_10` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD10 išraišką pagal nurodyto sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1321f-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1321f-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1321f-105">Syntax</span></span>

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="1321f-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1321f-106">Arguments</span></span>

<span data-ttu-id="1321f-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1321f-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="1321f-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1321f-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1321f-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="1321f-109">Return values</span></span>

<span data-ttu-id="1321f-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1321f-110">*String*</span></span>

<span data-ttu-id="1321f-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1321f-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1321f-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1321f-112">Example</span></span>

<span data-ttu-id="1321f-113">`CH_BANK_MOD_10 ("VEND-200002")` grąžina **3**.</span><span class="sxs-lookup"><span data-stu-id="1321f-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1321f-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1321f-114">Additional resources</span></span>

[<span data-ttu-id="1321f-115">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="1321f-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
