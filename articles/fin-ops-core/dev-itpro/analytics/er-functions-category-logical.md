---
title: Loginės kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie logines funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916642"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="25bf5-103">Loginės kategorijos ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="25bf5-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25bf5-104">Naudojant logines modulio Elektroninės ataskaitos (ER) funkcijas, galima dirbti su loginėmis reikšmėmis, norint viename reiškinyje atlikti daugiau nei vieną palyginimą arba patikrinti kelias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="25bf5-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="25bf5-105">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="25bf5-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="25bf5-106">Palaikomų funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="25bf5-106">List of supported functions</span></span>

| <span data-ttu-id="25bf5-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="25bf5-107">Function</span></span> | <span data-ttu-id="25bf5-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="25bf5-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="25bf5-109">Ir</span><span class="sxs-lookup"><span data-stu-id="25bf5-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="25bf5-110">Jei visos nurodytos sąlygos yra teisingos, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="25bf5-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="25bf5-111">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="25bf5-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="25bf5-112">Saugykla</span><span class="sxs-lookup"><span data-stu-id="25bf5-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="25bf5-113">Ši funkcija nurodyto reiškinio reikšmę įvertina pagal nurodytas alternatyvias parinktis ir pateikia pirmosios parinkties, kuri yra lygi nurodyto reiškinio reikšmei, rezultatą.</span><span class="sxs-lookup"><span data-stu-id="25bf5-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="25bf5-114">Kitu atveju ji pateikia pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas yra nurodytas kaip paskutinis iškviestos funkcijos argumentas, prieš kurį nėra parinkties.</span><span class="sxs-lookup"><span data-stu-id="25bf5-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="25bf5-115">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25bf5-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="25bf5-116">Jei</span><span class="sxs-lookup"><span data-stu-id="25bf5-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="25bf5-117">Jei nurodyta sąlyga yra tenkinama, ši funkcija pateikia pirmą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25bf5-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="25bf5-118">Kitu atveju ji pateikia antrą nurodytą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25bf5-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="25bf5-119">Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25bf5-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="25bf5-120">Ne</span><span class="sxs-lookup"><span data-stu-id="25bf5-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="25bf5-121">Ši funkcija pateikia nurodytos sąlygos atvirkštinę loginę reikšmę kaip *Bulio logikos* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25bf5-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="25bf5-122">Or</span><span class="sxs-lookup"><span data-stu-id="25bf5-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="25bf5-123">Jei visos nurodytos sąlygos yra klaidingos, ši funkcija pateikia *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="25bf5-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="25bf5-124">Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="25bf5-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="25bf5-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="25bf5-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="25bf5-126">Ši funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25bf5-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="25bf5-127">Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui.</span><span class="sxs-lookup"><span data-stu-id="25bf5-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="25bf5-128">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="25bf5-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="25bf5-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="25bf5-129">Additional resources</span></span>

[<span data-ttu-id="25bf5-130">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="25bf5-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="25bf5-131">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="25bf5-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="25bf5-132">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="25bf5-132">Electronic reporting formula language</span></span>](er-formula-language.md)
