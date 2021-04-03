---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISVALIDCHARACTERISO7064 elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563371"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="77401-103">ISVALIDCHARACTERISO7064 ER funkcija</span><span class="sxs-lookup"><span data-stu-id="77401-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77401-104">`ISVALIDCHARACTERISO7064` funkcija grąžina *Bulio logikos* reikšmę **TRUE**, jei nurodyta eilutė rodo tinkamą tarptautinį banko sąskaitos numerį (IBAN).</span><span class="sxs-lookup"><span data-stu-id="77401-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="77401-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="77401-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="77401-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="77401-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="77401-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="77401-107">Arguments</span></span>

<span data-ttu-id="77401-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="77401-108">`text`: *String*</span></span>

<span data-ttu-id="77401-109">Tekstinė reikšmė, kuri nurodo IBAN.</span><span class="sxs-lookup"><span data-stu-id="77401-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="77401-110">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="77401-110">Return values</span></span>

<span data-ttu-id="77401-111">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="77401-111">*String*</span></span>

<span data-ttu-id="77401-112">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="77401-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="77401-113">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="77401-113">Example</span></span>

<span data-ttu-id="77401-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="77401-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="77401-115">`ISVALIDCHARACTERISO7064 ("AT61")` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="77401-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77401-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="77401-116">Additional resources</span></span>

[<span data-ttu-id="77401-117">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="77401-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]