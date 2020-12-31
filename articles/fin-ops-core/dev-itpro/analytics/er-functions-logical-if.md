---
title: IF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama IF elektroninių ataskaitų (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687007"
---
# <a name="if-er-function"></a><span data-ttu-id="303da-103">IF ER funkcija</span><span class="sxs-lookup"><span data-stu-id="303da-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="303da-104">`IF` funkcija grąžina pirmą nurodytą reikšmę, jei nurodyta sąlyga yra tenkinama.</span><span class="sxs-lookup"><span data-stu-id="303da-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="303da-105">Kitu atveju ji pateikia antrą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="303da-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="303da-106">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="303da-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="303da-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="303da-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="303da-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="303da-108">Arguments</span></span>

<span data-ttu-id="303da-109">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="303da-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="303da-110">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="303da-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="303da-111">`first value`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="303da-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="303da-112">Rezultatas, kuris grąžinamas, jei sąlyga tenkinama.</span><span class="sxs-lookup"><span data-stu-id="303da-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="303da-113">`second value`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="303da-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="303da-114">Rezultatas, kuris grąžinamas, jei sąlyga netenkinama.</span><span class="sxs-lookup"><span data-stu-id="303da-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="303da-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="303da-115">Return values</span></span>

<span data-ttu-id="303da-116">*Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="303da-116">*Any of the supported data types*</span></span>

<span data-ttu-id="303da-117">Gauta bet kurio palaikomų duomenų tipo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="303da-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="303da-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="303da-118">Usage notes</span></span>

<span data-ttu-id="303da-119">Argumentai `first value` ir `second value` turi būti nurodyti naudojant tą patį duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="303da-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="303da-120">Jei sukonfigūruotų reikšmių duomenų tipai nesutampa, kūrimo metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="303da-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="303da-121">Jei pirmoji reikšmė ir antroji reikšmė yra duomenų tipo *Konteineris (įrašas)* arba *Įrašų sąrašas* reikšmės, rezultatai apima tik tuos laukus, kurie yra abiejose reikšmėse.</span><span class="sxs-lookup"><span data-stu-id="303da-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="303da-122">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="303da-122">Example</span></span>

<span data-ttu-id="303da-123">`IF (1=2, "condition is met", "condition is not met")` grąžina eilutę **„sąlyga netenkinama“**.</span><span class="sxs-lookup"><span data-stu-id="303da-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="303da-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="303da-124">Additional resources</span></span>

[<span data-ttu-id="303da-125">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="303da-125">Logical functions</span></span>](er-functions-category-logical.md)
