---
title: ER NOW funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NOW funkcija.
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
ms.openlocfilehash: e8c411e1ce9656ffa35986f1ceef712c9def1e6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743524"
---
# <a name="now-er-function"></a><span data-ttu-id="3a27c-103">ER NOW funkcija</span><span class="sxs-lookup"><span data-stu-id="3a27c-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a27c-104">`NOW` funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos serverio datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="3a27c-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a27c-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="3a27c-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="3a27c-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="3a27c-106">Return values</span></span>

<span data-ttu-id="3a27c-107">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="3a27c-107">*DateTime*</span></span>

<span data-ttu-id="3a27c-108">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="3a27c-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="3a27c-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3a27c-109">Example</span></span>

<span data-ttu-id="3a27c-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="3a27c-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a27c-111">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3a27c-111">Additional resources</span></span>

[<span data-ttu-id="3a27c-112">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="3a27c-112">Date and time functions</span></span>](er-functions-category-datetime.md)
