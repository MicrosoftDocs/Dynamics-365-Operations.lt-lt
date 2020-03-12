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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041750"
---
# <span data-ttu-id="a5894-103"><a name="IF">IF ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="a5894-103"><a name="IF">IF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5894-104">`IF` funkcija grąžina pirmą nurodytą reikšmę, jei nurodyta sąlyga yra tenkinama.</span><span class="sxs-lookup"><span data-stu-id="a5894-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="a5894-105">Kitu atveju ji pateikia antrą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a5894-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="a5894-106">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a5894-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5894-107">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="a5894-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="a5894-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="a5894-108">Arguments</span></span>

<span data-ttu-id="a5894-109">`condition`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="a5894-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="a5894-110">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="a5894-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="a5894-111">`first value`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="a5894-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="a5894-112">Rezultatas, kuris grąžinamas, jei sąlyga tenkinama.</span><span class="sxs-lookup"><span data-stu-id="a5894-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="a5894-113">`second value`: *Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="a5894-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="a5894-114">Rezultatas, kuris grąžinamas, jei sąlyga netenkinama.</span><span class="sxs-lookup"><span data-stu-id="a5894-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5894-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="a5894-115">Return values</span></span>

<span data-ttu-id="a5894-116">*Bet kuris iš palaikomų duomenų tipų*</span><span class="sxs-lookup"><span data-stu-id="a5894-116">*Any of the supported data types*</span></span>

<span data-ttu-id="a5894-117">Gauta bet kurio palaikomų duomenų tipo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a5894-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a5894-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="a5894-118">Usage notes</span></span>

<span data-ttu-id="a5894-119">Argumentai `first value` ir `second value` turi būti nurodyti naudojant tą patį duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="a5894-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="a5894-120">Jei sukonfigūruotų reikšmių duomenų tipai nesutampa, kūrimo metu pateikiama išimtis.</span><span class="sxs-lookup"><span data-stu-id="a5894-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="a5894-121">Jei pirmoji reikšmė ir antroji reikšmė yra duomenų tipo *Konteineris (įrašas)* arba *Įrašų sąrašas* reikšmės, rezultatai apima tik tuos laukus, kurie yra abiejose reikšmėse.</span><span class="sxs-lookup"><span data-stu-id="a5894-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="a5894-122">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a5894-122">Example</span></span>

<span data-ttu-id="a5894-123">`IF (1=2, "condition is met", "condition is not met")` grąžina eilutę **„sąlyga netenkinama“**.</span><span class="sxs-lookup"><span data-stu-id="a5894-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5894-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a5894-124">Additional resources</span></span>

[<span data-ttu-id="a5894-125">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="a5894-125">Logical functions</span></span>](er-functions-category-logical.md)
