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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743404"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="f5d8b-103">ER NUMBERVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="f5d8b-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5d8b-104">`NUMBERVALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="f5d8b-105">Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d8b-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="f5d8b-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="f5d8b-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="f5d8b-107">Arguments</span></span>

<span data-ttu-id="f5d8b-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f5d8b-108">`text`: *String*</span></span>

<span data-ttu-id="f5d8b-109">Teksto reikšmė, kurią reikia konvertuoti į tipo *Realusis* skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="f5d8b-110">`decimal separator`: Eilutė</span><span class="sxs-lookup"><span data-stu-id="f5d8b-110">`decimal separator`: String</span></span>

<span data-ttu-id="f5d8b-111">Dešimtainis skyriklis.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-111">A decimal separator.</span></span> <span data-ttu-id="f5d8b-112">Jis naudojamas dešimtainio skaičiaus sveikajai ir trupmeninei dalims atskirti.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="f5d8b-113">`digit grouping separator`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f5d8b-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="f5d8b-114">Skaitmenų grupavimo skyriklis.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-114">A digit grouping separator.</span></span> <span data-ttu-id="f5d8b-115">Jis naudojamas kaip tūkstančių skyriklis.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5d8b-116">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="f5d8b-116">Return values</span></span>

<span data-ttu-id="f5d8b-117">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="f5d8b-117">*Real*</span></span>

<span data-ttu-id="f5d8b-118">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f5d8b-119">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f5d8b-119">Example</span></span>

<span data-ttu-id="f5d8b-120">`NUMBERVALUE( "1 234,56", ",", " ")` pateikia **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5d8b-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f5d8b-121">Additional resources</span></span>

[<span data-ttu-id="f5d8b-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f5d8b-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
