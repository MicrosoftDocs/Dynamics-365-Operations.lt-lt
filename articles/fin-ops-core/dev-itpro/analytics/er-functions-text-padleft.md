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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040968"
---
# <span data-ttu-id="90d3e-103"><a name="PADLEFT">PADLEFT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="90d3e-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d3e-104">`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.</span><span class="sxs-lookup"><span data-stu-id="90d3e-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d3e-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="90d3e-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="90d3e-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="90d3e-106">Arguments</span></span>

<span data-ttu-id="90d3e-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="90d3e-107">`text`: *String*</span></span>

<span data-ttu-id="90d3e-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="90d3e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="90d3e-109">`length`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="90d3e-109">`length`: *Integer*</span></span>

<span data-ttu-id="90d3e-110">*Sveikojo skaičiaus* reikšmė, reiškianti galutinį simbolių skaičių, esantį užpildytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="90d3e-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="90d3e-111">`padding chars`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="90d3e-111">`padding chars`: *String*</span></span>

<span data-ttu-id="90d3e-112">Simboliai, naudojami užpildant.</span><span class="sxs-lookup"><span data-stu-id="90d3e-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="90d3e-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="90d3e-113">Return values</span></span>

<span data-ttu-id="90d3e-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="90d3e-114">*String*</span></span>

<span data-ttu-id="90d3e-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="90d3e-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="90d3e-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="90d3e-116">Example</span></span>

<span data-ttu-id="90d3e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` grąžina teksto eilutę **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234“**.</span><span class="sxs-lookup"><span data-stu-id="90d3e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90d3e-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="90d3e-118">Additional resources</span></span>

[<span data-ttu-id="90d3e-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="90d3e-119">Text functions</span></span>](er-functions-category-text.md)
