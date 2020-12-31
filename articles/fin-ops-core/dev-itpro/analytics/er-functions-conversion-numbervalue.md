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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685984"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="71646-103">ER NUMBERVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="71646-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71646-104">`NUMBERVALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="71646-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="71646-105">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="71646-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="71646-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="71646-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="71646-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="71646-107">Arguments</span></span>

<span data-ttu-id="71646-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71646-108">`text`: *String*</span></span>

<span data-ttu-id="71646-109">Teksto reikšmė, kurią reikia konvertuoti į tipo *Realusis* skaičių.</span><span class="sxs-lookup"><span data-stu-id="71646-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="71646-110">`decimal separator`: Eilutė</span><span class="sxs-lookup"><span data-stu-id="71646-110">`decimal separator`: String</span></span>

<span data-ttu-id="71646-111">Dešimtainis skyriklis.</span><span class="sxs-lookup"><span data-stu-id="71646-111">A decimal separator.</span></span> <span data-ttu-id="71646-112">Jis naudojamas dešimtainio skaičiaus sveikajai ir trupmeninei dalims atskirti.</span><span class="sxs-lookup"><span data-stu-id="71646-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="71646-113">`digit grouping separator`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71646-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="71646-114">Skaitmenų grupavimo skyriklis.</span><span class="sxs-lookup"><span data-stu-id="71646-114">A digit grouping separator.</span></span> <span data-ttu-id="71646-115">Jis naudojamas kaip tūkstančių skyriklis.</span><span class="sxs-lookup"><span data-stu-id="71646-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="71646-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="71646-116">Return values</span></span>

<span data-ttu-id="71646-117">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="71646-117">*Real*</span></span>

<span data-ttu-id="71646-118">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="71646-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="71646-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="71646-119">Example</span></span>

<span data-ttu-id="71646-120">`NUMBERVALUE( "1 234,56", ",", " ")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="71646-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71646-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="71646-121">Additional resources</span></span>

[<span data-ttu-id="71646-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="71646-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
