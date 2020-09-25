---
title: TRANSLATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRANSLATE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744244"
---
# <a name="translate-er-function"></a><span data-ttu-id="3956c-103">TRANSLATE ER funkcija</span><span class="sxs-lookup"><span data-stu-id="3956c-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3956c-104">`TRANSLATE` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas kito pateikto rinkinio nurodyto teksto simbolių pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="3956c-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3956c-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="3956c-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="3956c-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="3956c-106">Arguments</span></span>

<span data-ttu-id="3956c-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3956c-107">`text`: *String*</span></span>

<span data-ttu-id="3956c-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="3956c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="3956c-109">`pattern`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3956c-109">`pattern`: *String*</span></span>

<span data-ttu-id="3956c-110">Tekstas, kuris turi būti pakeistas.</span><span class="sxs-lookup"><span data-stu-id="3956c-110">The text that must be replaced.</span></span>

<span data-ttu-id="3956c-111">`replacement`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3956c-111">`replacement`: *String*</span></span>

<span data-ttu-id="3956c-112">Tekstas, kurį norite naudoti kaip pakaitą.</span><span class="sxs-lookup"><span data-stu-id="3956c-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="3956c-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="3956c-113">Return values</span></span>

<span data-ttu-id="3956c-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3956c-114">*String*</span></span>

<span data-ttu-id="3956c-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="3956c-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3956c-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="3956c-116">Usage notes</span></span>

<span data-ttu-id="3956c-117">`TRANSLATE` funkcija vienu metu pakeičia vieną simbolį.</span><span class="sxs-lookup"><span data-stu-id="3956c-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="3956c-118">Funkcija pakeičia pirmą `text` argumento simbolį pirmu `pattern` argumento simboliu, tada pakeičia antrą simbolį ir naudoja tokią pačią gamybos eigą, kol užbaigia darbą.</span><span class="sxs-lookup"><span data-stu-id="3956c-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="3956c-119">Kai `text` ir `pattern` argumentų simboliai sutampa, jie pakeičiami `replacement` argumento simboliu, kuris yra tokioje pačioje vietoje kaip ir `pattern` argumento simbolis.</span><span class="sxs-lookup"><span data-stu-id="3956c-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="3956c-120">Jei `pattern` argumente simbolis rodomas kelis kartus, naudojamas `replacement` argumento susiejimas, atitinkantis pirmą šio simbolio atvejį.</span><span class="sxs-lookup"><span data-stu-id="3956c-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="3956c-121">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3956c-121">Example 1</span></span>

<span data-ttu-id="3956c-122">`TRANSLATE ("abcdef", "cd", "GH")` pakeičia nurodyto teksto **„abcdef”** simbolį **c** `replacement` teksto simboliu **G** dėl toliau pateiktų priežasčių.</span><span class="sxs-lookup"><span data-stu-id="3956c-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="3956c-123">Simbolis **c** pateikiamas pirmoje `pattern` teksto vietoje.</span><span class="sxs-lookup"><span data-stu-id="3956c-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="3956c-124">Pirmoje `replacement` teksto vietoje yra simbolis **G**.</span><span class="sxs-lookup"><span data-stu-id="3956c-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="3956c-125">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3956c-125">Example 2</span></span>

<span data-ttu-id="3956c-126">`TRANSLATE ("abcdef", "ccd", "GH")` grąžina **„abGdef“**.</span><span class="sxs-lookup"><span data-stu-id="3956c-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="3956c-127">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3956c-127">Example 3</span></span>

<span data-ttu-id="3956c-128">`TRANSLATE ("abccba", "abc", "123")` grąžina **„123321“**.</span><span class="sxs-lookup"><span data-stu-id="3956c-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3956c-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3956c-129">Additional resources</span></span>

[<span data-ttu-id="3956c-130">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="3956c-130">Text functions</span></span>](er-functions-category-text.md)
