---
title: PADLEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama PADLEFT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 86957808ca30db87e6f8202c2024d9929969fc3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562690"
---
# <a name="padleft-er-function"></a><span data-ttu-id="6bd28-103">PADLEFT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="6bd28-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bd28-104">`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.</span><span class="sxs-lookup"><span data-stu-id="6bd28-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd28-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6bd28-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="6bd28-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6bd28-106">Arguments</span></span>

<span data-ttu-id="6bd28-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6bd28-107">`text`: *String*</span></span>

<span data-ttu-id="6bd28-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="6bd28-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="6bd28-109">`length`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="6bd28-109">`length`: *Integer*</span></span>

<span data-ttu-id="6bd28-110">*Sveikojo skaičiaus* reikšmė, reiškianti galutinį simbolių skaičių, esantį užpildytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6bd28-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="6bd28-111">`padding chars`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6bd28-111">`padding chars`: *String*</span></span>

<span data-ttu-id="6bd28-112">Simboliai, naudojami užpildant.</span><span class="sxs-lookup"><span data-stu-id="6bd28-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="6bd28-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="6bd28-113">Return values</span></span>

<span data-ttu-id="6bd28-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6bd28-114">*String*</span></span>

<span data-ttu-id="6bd28-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6bd28-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="6bd28-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6bd28-116">Example</span></span>

<span data-ttu-id="6bd28-117">`PADLEFT ("1234", 10, "`&nbsp;`")` grąžina teksto eilutę **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234“**.</span><span class="sxs-lookup"><span data-stu-id="6bd28-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bd28-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6bd28-118">Additional resources</span></span>

[<span data-ttu-id="6bd28-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="6bd28-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]