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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745494"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="2bc2b-103">ER DAYOFYEAR funkcija</span><span class="sxs-lookup"><span data-stu-id="2bc2b-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bc2b-104">`DAYOFYEAR` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc2b-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="2bc2b-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="2bc2b-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="2bc2b-106">Arguments</span></span>

<span data-ttu-id="2bc2b-107">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="2bc2b-107">`date`: *Date*</span></span>

<span data-ttu-id="2bc2b-108">Datos reikšmė, nurodanti datą, naudotiną dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="2bc2b-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="2bc2b-109">Return values</span></span>

<span data-ttu-id="2bc2b-110">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="2bc2b-110">*Integer*</span></span>

<span data-ttu-id="2bc2b-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2bc2b-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2bc2b-112">Example 1</span></span>

<span data-ttu-id="2bc2b-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` pateikia **61**.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2bc2b-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="2bc2b-114">Example 2</span></span>

<span data-ttu-id="2bc2b-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` pateikia **1**.</span><span class="sxs-lookup"><span data-stu-id="2bc2b-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bc2b-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2bc2b-116">Additional resources</span></span>

[<span data-ttu-id="2bc2b-117">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="2bc2b-117">Date and time functions</span></span>](er-functions-category-datetime.md)
