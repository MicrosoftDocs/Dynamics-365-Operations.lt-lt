---
title: TRIM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRIM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746054"
---
# <a name="trim-er-function"></a><span data-ttu-id="9d03b-103">TRIM ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9d03b-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d03b-104">`TRIM` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę, sutrumpinus priekinius ir galinius tarpus bei pašalinus perteklinius tarpus tarp žodžių.</span><span class="sxs-lookup"><span data-stu-id="9d03b-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d03b-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9d03b-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="9d03b-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9d03b-106">Arguments</span></span>

<span data-ttu-id="9d03b-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9d03b-107">`text`: *String*</span></span>

<span data-ttu-id="9d03b-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="9d03b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d03b-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="9d03b-109">Return values</span></span>

<span data-ttu-id="9d03b-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9d03b-110">*String*</span></span>

<span data-ttu-id="9d03b-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9d03b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9d03b-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9d03b-112">Example</span></span>

<span data-ttu-id="9d03b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` grąžina **„Teksto pavyzdys“**.</span><span class="sxs-lookup"><span data-stu-id="9d03b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d03b-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9d03b-114">Additional resources</span></span>

[<span data-ttu-id="9d03b-115">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="9d03b-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]