---
title: INT64VALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INT64VALUE funkcija.
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
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744844"
---
# <a name="int64value-er-function"></a><span data-ttu-id="29c14-103">INT64VALUE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="29c14-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29c14-104">`INT64VALUE` funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="29c14-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="29c14-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="29c14-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="29c14-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="29c14-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="29c14-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="29c14-107">Arguments</span></span>

<span data-ttu-id="29c14-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="29c14-108">`text`: *String*</span></span>

<span data-ttu-id="29c14-109">Teksto reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="29c14-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="29c14-110">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="29c14-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="29c14-111">Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="29c14-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="29c14-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="29c14-112">Return values</span></span>

<span data-ttu-id="29c14-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="29c14-113">*Int64*</span></span>

<span data-ttu-id="29c14-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="29c14-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="29c14-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="29c14-115">Usage notes</span></span>

<span data-ttu-id="29c14-116">Visi skaičiai po kablelio pašalinami.</span><span class="sxs-lookup"><span data-stu-id="29c14-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="29c14-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="29c14-117">Example 1</span></span>

<span data-ttu-id="29c14-118">`INT64VALUE ("22565422744")` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="29c14-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="29c14-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="29c14-119">Example 2</span></span>

<span data-ttu-id="29c14-120">`INT64VALUE ( VALUE("22565422744.77"))` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="29c14-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29c14-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="29c14-121">Additional resources</span></span>

[<span data-ttu-id="29c14-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="29c14-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
