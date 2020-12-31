---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISVALIDCHARACTERISO7064 elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680667"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="bf2bf-103">ISVALIDCHARACTERISO7064 ER funkcija</span><span class="sxs-lookup"><span data-stu-id="bf2bf-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf2bf-104">`ISVALIDCHARACTERISO7064` funkcija grąžina *Bulio logikos* reikšmę **TRUE**, jei nurodyta eilutė rodo tinkamą tarptautinį banko sąskaitos numerį (IBAN).</span><span class="sxs-lookup"><span data-stu-id="bf2bf-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="bf2bf-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bf2bf-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2bf-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="bf2bf-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="bf2bf-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="bf2bf-107">Arguments</span></span>

<span data-ttu-id="bf2bf-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="bf2bf-108">`text`: *String*</span></span>

<span data-ttu-id="bf2bf-109">Tekstinė reikšmė, kuri nurodo IBAN.</span><span class="sxs-lookup"><span data-stu-id="bf2bf-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="bf2bf-110">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="bf2bf-110">Return values</span></span>

<span data-ttu-id="bf2bf-111">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="bf2bf-111">*String*</span></span>

<span data-ttu-id="bf2bf-112">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="bf2bf-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bf2bf-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="bf2bf-113">Example</span></span>

<span data-ttu-id="bf2bf-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="bf2bf-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="bf2bf-115">`ISVALIDCHARACTERISO7064 ("AT61")` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="bf2bf-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf2bf-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bf2bf-116">Additional resources</span></span>

[<span data-ttu-id="bf2bf-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="bf2bf-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
