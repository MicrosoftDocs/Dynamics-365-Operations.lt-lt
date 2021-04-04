---
title: ER NUMBERVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NUMBERVALUE funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561427"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="51768-103">ER NUMBERVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="51768-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51768-104">`NUMBERVALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="51768-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="51768-105">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="51768-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="51768-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="51768-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="51768-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="51768-107">Arguments</span></span>

<span data-ttu-id="51768-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="51768-108">`text`: *String*</span></span>

<span data-ttu-id="51768-109">Teksto reikšmė, kurią reikia konvertuoti į tipo *Realusis* skaičių.</span><span class="sxs-lookup"><span data-stu-id="51768-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="51768-110">`decimal separator`: Eilutė</span><span class="sxs-lookup"><span data-stu-id="51768-110">`decimal separator`: String</span></span>

<span data-ttu-id="51768-111">Dešimtainis skyriklis.</span><span class="sxs-lookup"><span data-stu-id="51768-111">A decimal separator.</span></span> <span data-ttu-id="51768-112">Jis naudojamas dešimtainio skaičiaus sveikajai ir trupmeninei dalims atskirti.</span><span class="sxs-lookup"><span data-stu-id="51768-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="51768-113">`digit grouping separator`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="51768-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="51768-114">Skaitmenų grupavimo skyriklis.</span><span class="sxs-lookup"><span data-stu-id="51768-114">A digit grouping separator.</span></span> <span data-ttu-id="51768-115">Jis naudojamas kaip tūkstančių skyriklis.</span><span class="sxs-lookup"><span data-stu-id="51768-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="51768-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="51768-116">Return values</span></span>

<span data-ttu-id="51768-117">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="51768-117">*Real*</span></span>

<span data-ttu-id="51768-118">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="51768-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="51768-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="51768-119">Example</span></span>

<span data-ttu-id="51768-120">`NUMBERVALUE( "1 234,56", ",", " ")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="51768-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51768-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="51768-121">Additional resources</span></span>

[<span data-ttu-id="51768-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="51768-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]