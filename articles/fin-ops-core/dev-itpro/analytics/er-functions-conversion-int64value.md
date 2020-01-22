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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916550"
---
# <span data-ttu-id="ffcbf-103"><a name="INT64VALUE">INT64VALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="ffcbf-103"><a name="INT64VALUE">INT64VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffcbf-104">`INT64VALUE` funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ffcbf-105">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ffcbf-105">Syntax 1</span></span>

```
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="ffcbf-106">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ffcbf-106">Syntax 2</span></span>

```
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="ffcbf-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="ffcbf-107">Arguments</span></span>

<span data-ttu-id="ffcbf-108">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ffcbf-108">`text`: *String*</span></span>

<span data-ttu-id="ffcbf-109">Teksto reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="ffcbf-110">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="ffcbf-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="ffcbf-111">Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int64* skaičių.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="ffcbf-112">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ffcbf-112">Return values</span></span>

<span data-ttu-id="ffcbf-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="ffcbf-113">*Int64*</span></span>

<span data-ttu-id="ffcbf-114">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ffcbf-115">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="ffcbf-115">Usage notes</span></span>

<span data-ttu-id="ffcbf-116">Visi skaičiai po kablelio pašalinami.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="ffcbf-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ffcbf-117">Example 1</span></span>

<span data-ttu-id="ffcbf-118">`INT64VALUE ("22565422744")` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ffcbf-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ffcbf-119">Example 2</span></span>

<span data-ttu-id="ffcbf-120">`INT64VALUE ( VALUE("22565422744.77"))` pateikia *Int64* reikšmę **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="ffcbf-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffcbf-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ffcbf-121">Additional resources</span></span>

[<span data-ttu-id="ffcbf-122">Tipų konvertavimo funkcijos</span><span class="sxs-lookup"><span data-stu-id="ffcbf-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
