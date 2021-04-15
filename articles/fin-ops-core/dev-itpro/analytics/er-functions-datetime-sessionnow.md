---
title: ER SESSIONNOW funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SESSIONNOW funkcija.
author: NickSelin
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
ms.openlocfilehash: 47b88a1ca0ea9fd09c2a82963901d9ace78891bb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746800"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="8ce75-103">ER SESSIONNOW funkcija</span><span class="sxs-lookup"><span data-stu-id="8ce75-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ce75-104">`SESSIONNOW` funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos seanso datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8ce75-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ce75-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="8ce75-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="8ce75-106">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="8ce75-106">Return values</span></span>

<span data-ttu-id="8ce75-107">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="8ce75-107">*DateTime*</span></span>

<span data-ttu-id="8ce75-108">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8ce75-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="8ce75-109">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8ce75-109">Example</span></span>

<span data-ttu-id="8ce75-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.</span><span class="sxs-lookup"><span data-stu-id="8ce75-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ce75-111">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8ce75-111">Additional resources</span></span>

[<span data-ttu-id="8ce75-112">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="8ce75-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]