---
title: Loginės kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie logines funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: a37b3341b05fde1283a21a0c52faec26cd1a7030
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686196"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="36ebd-103">Loginės kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="36ebd-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36ebd-104">Naudojant logines modulio Elektroninės ataskaitos (ER) funkcijas, galima dirbti su loginėmis reikšmėmis, norint viename reiškinyje atlikti daugiau nei vieną palyginimą arba patikrinti kelias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="36ebd-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="36ebd-105">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="36ebd-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="36ebd-106">Palaikomų funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="36ebd-106">List of supported functions</span></span>

| <span data-ttu-id="36ebd-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="36ebd-107">Function</span></span> | <span data-ttu-id="36ebd-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="36ebd-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="36ebd-109">Ir</span><span class="sxs-lookup"><span data-stu-id="36ebd-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="36ebd-110">Jei visos nurodytos sąlygos yra teisingos, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="36ebd-111">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="36ebd-112">Saugykla</span><span class="sxs-lookup"><span data-stu-id="36ebd-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="36ebd-113">Ši funkcija nurodyto reiškinio reikšmę įvertina pagal nurodytas alternatyvias parinktis ir pateikia pirmosios parinkties, kuri yra lygi nurodyto reiškinio reikšmei, rezultatą.</span><span class="sxs-lookup"><span data-stu-id="36ebd-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="36ebd-114">Kitu atveju ji pateikia pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas yra nurodytas kaip paskutinis iškviestos funkcijos argumentas, prieš kurį nėra parinkties.</span><span class="sxs-lookup"><span data-stu-id="36ebd-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="36ebd-115">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="36ebd-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="36ebd-116">Jei</span><span class="sxs-lookup"><span data-stu-id="36ebd-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="36ebd-117">Jei nurodyta sąlyga yra tenkinama, ši funkcija pateikia pirmą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36ebd-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="36ebd-118">Kitu atveju ji pateikia antrą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36ebd-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="36ebd-119">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="36ebd-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="36ebd-120">Ne</span><span class="sxs-lookup"><span data-stu-id="36ebd-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="36ebd-121">Ši funkcija pateikia nurodytos sąlygos atvirkštinę loginę reikšmę kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36ebd-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="36ebd-122">Or</span><span class="sxs-lookup"><span data-stu-id="36ebd-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="36ebd-123">Jei visos nurodytos sąlygos yra klaidingos, ši funkcija pateikia *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="36ebd-124">Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="36ebd-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="36ebd-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="36ebd-126">Ši funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36ebd-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="36ebd-127">Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="36ebd-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="36ebd-128">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="36ebd-129">ValueinLarge</span><span class="sxs-lookup"><span data-stu-id="36ebd-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="36ebd-130">Ši funkcija nustato, ar nurodyta *Int64* arba *Sveikojo skaičiaus* tipo įvestis atitinka bet kurią pateiktame sąraše nurodytos prekės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36ebd-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="36ebd-131">Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="36ebd-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="36ebd-132">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="36ebd-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="36ebd-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="36ebd-133">Additional resources</span></span>

[<span data-ttu-id="36ebd-134">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="36ebd-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="36ebd-135">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="36ebd-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="36ebd-136">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="36ebd-136">Electronic reporting formula language</span></span>](er-formula-language.md)
