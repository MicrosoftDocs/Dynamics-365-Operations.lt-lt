---
title: ER DAYOFYEAR funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYOFYEAR funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563539"
---
# <a name="dayofyear-er-function"></a><span data-ttu-id="c0198-103">ER DAYOFYEAR funkcija</span><span class="sxs-lookup"><span data-stu-id="c0198-103">DAYOFYEAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0198-104">`DAYOFYEAR` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="c0198-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0198-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="c0198-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="c0198-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="c0198-106">Arguments</span></span>

<span data-ttu-id="c0198-107">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="c0198-107">`date`: *Date*</span></span>

<span data-ttu-id="c0198-108">Datos reikšmė, nurodanti datą, naudotiną dienų skaičiui skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="c0198-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0198-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="c0198-109">Return values</span></span>

<span data-ttu-id="c0198-110">*Sveikasis skaičius*</span><span class="sxs-lookup"><span data-stu-id="c0198-110">*Integer*</span></span>

<span data-ttu-id="c0198-111">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c0198-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0198-112">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c0198-112">Example 1</span></span>

<span data-ttu-id="c0198-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` pateikia **61**.</span><span class="sxs-lookup"><span data-stu-id="c0198-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0198-114">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c0198-114">Example 2</span></span>

<span data-ttu-id="c0198-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` pateikia **1**.</span><span class="sxs-lookup"><span data-stu-id="c0198-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0198-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c0198-116">Additional resources</span></span>

[<span data-ttu-id="c0198-117">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="c0198-117">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]