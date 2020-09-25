---
title: PADLEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama PADLEFT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744364"
---
# <a name="padleft-er-function"></a><span data-ttu-id="441f3-103">PADLEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="441f3-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="441f3-104">`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.</span><span class="sxs-lookup"><span data-stu-id="441f3-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="441f3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="441f3-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="441f3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="441f3-106">Arguments</span></span>

<span data-ttu-id="441f3-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="441f3-107">`text`: *String*</span></span>

<span data-ttu-id="441f3-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="441f3-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="441f3-109">`length`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="441f3-109">`length`: *Integer*</span></span>

<span data-ttu-id="441f3-110">*Sveikojo skaičiaus* reikšmė, reiškianti galutinį simbolių skaičių, esantį užpildytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="441f3-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="441f3-111">`padding chars`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="441f3-111">`padding chars`: *String*</span></span>

<span data-ttu-id="441f3-112">Simboliai, naudojami užpildant.</span><span class="sxs-lookup"><span data-stu-id="441f3-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="441f3-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="441f3-113">Return values</span></span>

<span data-ttu-id="441f3-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="441f3-114">*String*</span></span>

<span data-ttu-id="441f3-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="441f3-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="441f3-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="441f3-116">Example</span></span>

<span data-ttu-id="441f3-117">`PADLEFT ("1234", 10, "`&nbsp;`")` grąžina teksto eilutę **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234“**.</span><span class="sxs-lookup"><span data-stu-id="441f3-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="441f3-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="441f3-118">Additional resources</span></span>

[<span data-ttu-id="441f3-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="441f3-119">Text functions</span></span>](er-functions-category-text.md)
