---
title: STRINGJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama STRINGJOIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041796"
---
# <span data-ttu-id="afe27-103"><a name="STRINGJOIN">STRINGJOIN ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="afe27-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afe27-104">`STRINGJOIN` funkcija grąžina *Eilutės* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytame sąraše, reikšmės.</span><span class="sxs-lookup"><span data-stu-id="afe27-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="afe27-105">Reikšmes galima skirti nurodytu skyrikliu.</span><span class="sxs-lookup"><span data-stu-id="afe27-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe27-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="afe27-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="afe27-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="afe27-107">Arguments</span></span>

<span data-ttu-id="afe27-108">`list`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="afe27-108">`list`: *Record list*</span></span>

<span data-ttu-id="afe27-109">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="afe27-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="afe27-110">`field`: *Laukas*</span><span class="sxs-lookup"><span data-stu-id="afe27-110">`field`: *Field*</span></span>

<span data-ttu-id="afe27-111">Tinkamas *Eilutės* duomenų tipo lauko maršrutas nurodytame sąraše.</span><span class="sxs-lookup"><span data-stu-id="afe27-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="afe27-112">`delimiter`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="afe27-112">`delimiter`: *String*</span></span>

<span data-ttu-id="afe27-113">Skyriklis, naudojamas antrinėms eilutėms atskirti.</span><span class="sxs-lookup"><span data-stu-id="afe27-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="afe27-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="afe27-114">Return values</span></span>

<span data-ttu-id="afe27-115">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="afe27-115">*String*</span></span>

<span data-ttu-id="afe27-116">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="afe27-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="afe27-117">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="afe27-117">Example</span></span>

<span data-ttu-id="afe27-118">Jei `SPLIT("abc" , 1)`įvesite kaip duomenų šaltinio **DS**, išraiška `STRINGJOIN (DS, DS.Value, "-")`grąžins **„a-b-c“**.</span><span class="sxs-lookup"><span data-stu-id="afe27-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afe27-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="afe27-119">Additional resources</span></span>

[<span data-ttu-id="afe27-120">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="afe27-120">List functions</span></span>](er-functions-category-list.md)
