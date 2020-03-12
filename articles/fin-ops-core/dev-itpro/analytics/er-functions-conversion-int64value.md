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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042693"
---
# <span data-ttu-id="79ca4-103"><a name="INT64VALUE">INT64VALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="79ca4-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79ca4-104">`INT64VALUE` funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="79ca4-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="79ca4-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="79ca4-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="79ca4-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="79ca4-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="79ca4-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="79ca4-107">Arguments</span></span>

<span data-ttu-id="79ca4-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="79ca4-108">`text`: *String*</span></span>

<span data-ttu-id="79ca4-109">Teksto reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="79ca4-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="79ca4-110">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="79ca4-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="79ca4-111">Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="79ca4-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="79ca4-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="79ca4-112">Return values</span></span>

<span data-ttu-id="79ca4-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="79ca4-113">*Int64*</span></span>

<span data-ttu-id="79ca4-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="79ca4-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="79ca4-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="79ca4-115">Usage notes</span></span>

<span data-ttu-id="79ca4-116">Visi skaičiai po kablelio pašalinami.</span><span class="sxs-lookup"><span data-stu-id="79ca4-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="79ca4-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="79ca4-117">Example 1</span></span>

<span data-ttu-id="79ca4-118">`INT64VALUE ("22565422744")` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="79ca4-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="79ca4-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="79ca4-119">Example 2</span></span>

<span data-ttu-id="79ca4-120">`INT64VALUE ( VALUE("22565422744.77"))` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="79ca4-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79ca4-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="79ca4-121">Additional resources</span></span>

[<span data-ttu-id="79ca4-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="79ca4-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
