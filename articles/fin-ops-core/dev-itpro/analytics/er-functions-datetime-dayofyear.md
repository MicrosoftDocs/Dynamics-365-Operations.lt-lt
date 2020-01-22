---
title: ER DAYOFYEAR funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYOFYEAR funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916343"
---
# <span data-ttu-id="bbf53-103"><a name="DAYOFYEAR">ER DAYOFYEAR funkcija</a></span><span class="sxs-lookup"><span data-stu-id="bbf53-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbf53-104">`DAYOFYEAR` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="bbf53-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbf53-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="bbf53-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="bbf53-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="bbf53-106">Arguments</span></span>

<span data-ttu-id="bbf53-107">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="bbf53-107">`date`: *Date*</span></span>

<span data-ttu-id="bbf53-108">Datos reikšmė, nurodanti datą, naudotiną dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="bbf53-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbf53-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="bbf53-109">Return values</span></span>

<span data-ttu-id="bbf53-110">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="bbf53-110">*Integer*</span></span>

<span data-ttu-id="bbf53-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="bbf53-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="bbf53-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bbf53-112">Example 1</span></span>

<span data-ttu-id="bbf53-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` pateikia **61**.</span><span class="sxs-lookup"><span data-stu-id="bbf53-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bbf53-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bbf53-114">Example 2</span></span>

<span data-ttu-id="bbf53-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` pateikia **1**.</span><span class="sxs-lookup"><span data-stu-id="bbf53-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbf53-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bbf53-116">Additional resources</span></span>

[<span data-ttu-id="bbf53-117">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="bbf53-117">Date and time functions</span></span>](er-functions-category-datetime.md)
