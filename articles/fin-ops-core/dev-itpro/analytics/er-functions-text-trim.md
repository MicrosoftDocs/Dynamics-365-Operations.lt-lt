---
title: TRIM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRIM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040830"
---
# <span data-ttu-id="809ae-103"><a name="TRIM">TRIM ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="809ae-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="809ae-104">`TRIM` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę, sutrumpinus priekinius ir galinius tarpus bei pašalinus perteklinius tarpus tarp žodžių.</span><span class="sxs-lookup"><span data-stu-id="809ae-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="809ae-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="809ae-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="809ae-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="809ae-106">Arguments</span></span>

<span data-ttu-id="809ae-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="809ae-107">`text`: *String*</span></span>

<span data-ttu-id="809ae-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="809ae-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="809ae-109">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="809ae-109">Return values</span></span>

<span data-ttu-id="809ae-110">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="809ae-110">*String*</span></span>

<span data-ttu-id="809ae-111">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="809ae-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="809ae-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="809ae-112">Example</span></span>

<span data-ttu-id="809ae-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` grąžina **„Teksto pavyzdys“**.</span><span class="sxs-lookup"><span data-stu-id="809ae-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="809ae-114">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="809ae-114">Additional resources</span></span>

[<span data-ttu-id="809ae-115">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="809ae-115">Text functions</span></span>](er-functions-category-text.md)
