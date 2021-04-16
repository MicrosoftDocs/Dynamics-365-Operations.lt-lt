---
title: CONCATENATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONCATENATE elektroninių ataskaitų (ER) funkcija
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746487"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="9b9e3-103">CONCATENATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9b9e3-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b9e3-104">`CONCATENATE` funkcija grąžina visas nurodytas teksto eilutes kaip *Eilutės* reikšmę, sujungus jas į vieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9e3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="9b9e3-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="9b9e3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9b9e3-106">Arguments</span></span>

<span data-ttu-id="9b9e3-107">`text 1`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b9e3-107">`text 1`: *String*</span></span>

<span data-ttu-id="9b9e3-108">Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9b9e3-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-109">This argument is required.</span></span>

<span data-ttu-id="9b9e3-110">`text N`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b9e3-110">`text N`: *String*</span></span>

<span data-ttu-id="9b9e3-111">Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9b9e3-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b9e3-113">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="9b9e3-113">Return values</span></span>

<span data-ttu-id="9b9e3-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b9e3-114">*String*</span></span>

<span data-ttu-id="9b9e3-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9b9e3-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9b9e3-116">Example</span></span>

<span data-ttu-id="9b9e3-117">`CONCATENATE ("abc", "def")`grąžina **„abcdef“**.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9b9e3-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9b9e3-118">Usage notes</span></span>

<span data-ttu-id="9b9e3-119">Išraiška `"abc" & "def"` taip pat grąžina **„abcdef“**.</span><span class="sxs-lookup"><span data-stu-id="9b9e3-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b9e3-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9b9e3-120">Additional resources</span></span>

[<span data-ttu-id="9b9e3-121">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="9b9e3-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]