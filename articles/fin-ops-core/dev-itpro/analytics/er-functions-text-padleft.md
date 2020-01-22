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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916780"
---
# <span data-ttu-id="6a38c-103"><a name="PADLEFT">PADLEFT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="6a38c-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a38c-104">`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.</span><span class="sxs-lookup"><span data-stu-id="6a38c-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a38c-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6a38c-105">Syntax</span></span>

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="6a38c-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6a38c-106">Arguments</span></span>

<span data-ttu-id="6a38c-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6a38c-107">`text`: *String*</span></span>

<span data-ttu-id="6a38c-108">*Eilutės* reikšmė, nurodanti pradinį tekstą.</span><span class="sxs-lookup"><span data-stu-id="6a38c-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="6a38c-109">`length`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="6a38c-109">`length`: *Integer*</span></span>

<span data-ttu-id="6a38c-110">*Sveikojo skaičiaus* reikšmė, reiškianti galutinį simbolių skaičių, esantį užpildytoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6a38c-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="6a38c-111">`padding chars`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6a38c-111">`padding chars`: *String*</span></span>

<span data-ttu-id="6a38c-112">Simboliai, naudojami užpildant.</span><span class="sxs-lookup"><span data-stu-id="6a38c-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="6a38c-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="6a38c-113">Return values</span></span>

<span data-ttu-id="6a38c-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="6a38c-114">*String*</span></span>

<span data-ttu-id="6a38c-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6a38c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="6a38c-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6a38c-116">Example</span></span>

<span data-ttu-id="6a38c-117">`PADLEFT ("1234", 10, "`&nbsp;`")` grąžina teksto eilutę **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234“**.</span><span class="sxs-lookup"><span data-stu-id="6a38c-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a38c-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6a38c-118">Additional resources</span></span>

[<span data-ttu-id="6a38c-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="6a38c-119">Text functions</span></span>](er-functions-category-text.md)
