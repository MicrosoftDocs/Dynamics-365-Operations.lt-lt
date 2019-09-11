---
title: Konfigūruoti darbo ir išlaidų standartines išlaidas
description: Šioje temoje aiškinama, kaip nustatyti standartines darbo ir projekto kaštų išlaidas.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867731"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="a3bb3-103">Konfigūruoti darbo ir išlaidų standartines išlaidas</span><span class="sxs-lookup"><span data-stu-id="a3bb3-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3bb3-104">Šioje temoje aiškinama, kaip nustatyti standartines darbo ir projekto kaštų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="a3bb3-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a3bb3-106">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Kaštų kaina (valandomis)**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="a3bb3-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-107">Select **New**.</span></span>
3. <span data-ttu-id="a3bb3-108">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="a3bb3-109">Lauke **Kaštų kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a3bb3-110">Galite nustatyti standartinę projekto kategorijos savikainą arba nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokį jų derinį.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="a3bb3-111">Tada taikoma savikaina apibrėžiama išsamiausiai.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="a3bb3-112">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-112">Select **Save**.</span></span>
6. <span data-ttu-id="a3bb3-113">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (valandomis)**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="a3bb3-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-114">Select **New**.</span></span>
8. <span data-ttu-id="a3bb3-115">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="a3bb3-116">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="a3bb3-117">Lauke **Kainodara** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a3bb3-118">Galite nustatyti standartinę valandinių operacijų pardavimo kainą ar projekto kategoriją.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="a3bb3-119">Be to, pardavimo kainas galite nustatyti pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą ar bet kokį kitą jų derinį.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="a3bb3-120">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją valandiniame žurnale, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a3bb3-121">Pavyzdžiui, jei nustatyta tiek bendra pardavimų kaina, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="a3bb3-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-122">Select **Save**.</span></span>
12. <span data-ttu-id="a3bb3-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-123">Close the page.</span></span>
13. <span data-ttu-id="a3bb3-124">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Kaštų kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="a3bb3-125">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-125">Select **New**.</span></span>
15. <span data-ttu-id="a3bb3-126">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="a3bb3-127">Lauke **Kaštų kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a3bb3-128">Galima užpildyti kelis laukus, bet tai mažiausia, ką reikia atlikti, norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="a3bb3-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-129">Select **Save**.</span></span>
18. <span data-ttu-id="a3bb3-130">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="a3bb3-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-131">Select **New**.</span></span>
20. <span data-ttu-id="a3bb3-132">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="a3bb3-133">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="a3bb3-134">Lauke **Kainodara** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a3bb3-135">Faktinė pardavimo kaina, kuri taikoma darbuotojui įvedus operaciją į išlaidų žurnalą, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a3bb3-136">Pavyzdžiui, jei nustatyta tiek bendra, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="a3bb3-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a3bb3-137">Select **Save**.</span></span>

