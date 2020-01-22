---
title: ER NUMBERVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NUMBERVALUE funkcija.
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916527"
---
# <span data-ttu-id="eb5ad-103"><a name="NUMBERVALUE">ER NUMBERVALUE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="eb5ad-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb5ad-104">`NUMBERVALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="eb5ad-105">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5ad-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="eb5ad-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="eb5ad-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="eb5ad-107">Arguments</span></span>

<span data-ttu-id="eb5ad-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb5ad-108">`text`: *String*</span></span>

<span data-ttu-id="eb5ad-109">Teksto reikšmė, kurią reikia konvertuoti į tipo *Realusis* skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="eb5ad-110">`decimal separator`: Eilutė</span><span class="sxs-lookup"><span data-stu-id="eb5ad-110">`decimal separator`: String</span></span>

<span data-ttu-id="eb5ad-111">Dešimtainis skyriklis.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-111">A decimal separator.</span></span> <span data-ttu-id="eb5ad-112">Jis naudojamas dešimtainio skaičiaus sveikajai ir trupmeninei dalims atskirti.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="eb5ad-113">`digit grouping separator`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb5ad-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="eb5ad-114">Skaitmenų grupavimo skyriklis.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-114">A digit grouping separator.</span></span> <span data-ttu-id="eb5ad-115">Jis naudojamas kaip tūkstančių skyriklis.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb5ad-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="eb5ad-116">Return values</span></span>

<span data-ttu-id="eb5ad-117">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="eb5ad-117">*Real*</span></span>

<span data-ttu-id="eb5ad-118">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="eb5ad-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="eb5ad-119">Example</span></span>

<span data-ttu-id="eb5ad-120">`NUMBERVALUE( "1 234,56", ",", " ")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="eb5ad-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb5ad-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eb5ad-121">Additional resources</span></span>

[<span data-ttu-id="eb5ad-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="eb5ad-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
