---
title: MOD_97 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MOD_97 elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 1054407addaf6f7c2a7d2f72bf1479e9dc374389
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749170"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="1a9dd-103">MOD_97 ER funkcija</span><span class="sxs-lookup"><span data-stu-id="1a9dd-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a9dd-104">`MOD_97` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1a9dd-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9dd-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="1a9dd-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="1a9dd-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="1a9dd-106">Arguments</span></span>

<span data-ttu-id="1a9dd-107">`invoice number digits`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1a9dd-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="1a9dd-108">Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="1a9dd-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a9dd-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="1a9dd-109">Return values</span></span>

<span data-ttu-id="1a9dd-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="1a9dd-110">*String*</span></span>

<span data-ttu-id="1a9dd-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1a9dd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1a9dd-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1a9dd-112">Example</span></span>

<span data-ttu-id="1a9dd-113">`MOD_97 ("VEND-200002")` grąžina **„20000285“**.</span><span class="sxs-lookup"><span data-stu-id="1a9dd-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a9dd-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1a9dd-114">Additional resources</span></span>

[<span data-ttu-id="1a9dd-115">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="1a9dd-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]