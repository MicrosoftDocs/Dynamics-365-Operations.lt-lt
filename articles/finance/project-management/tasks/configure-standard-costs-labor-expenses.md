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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140098"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="a866c-103">Konfigūruoti darbo ir išlaidų standartines išlaidas</span><span class="sxs-lookup"><span data-stu-id="a866c-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a866c-104">Šioje temoje aiškinama, kaip nustatyti standartines darbo ir projekto kaštų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a866c-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="a866c-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="a866c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="a866c-106">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Kaštų kaina (valandomis)**.</span><span class="sxs-lookup"><span data-stu-id="a866c-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="a866c-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a866c-107">Select **New**.</span></span>
3. <span data-ttu-id="a866c-108">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a866c-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="a866c-109">Lauke **Kaštų kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a866c-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a866c-110">Galite nustatyti standartinę projekto kategorijos savikainą arba nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokį jų derinį.</span><span class="sxs-lookup"><span data-stu-id="a866c-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="a866c-111">Tada taikoma savikaina apibrėžiama išsamiausiai.</span><span class="sxs-lookup"><span data-stu-id="a866c-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="a866c-112">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a866c-112">Select **Save**.</span></span>
6. <span data-ttu-id="a866c-113">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (valandomis)**.</span><span class="sxs-lookup"><span data-stu-id="a866c-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="a866c-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a866c-114">Select **New**.</span></span>
8. <span data-ttu-id="a866c-115">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a866c-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="a866c-116">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a866c-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="a866c-117">Lauke **Kainodara** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a866c-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a866c-118">Galite nustatyti standartinę valandinių operacijų pardavimo kainą ar projekto kategoriją.</span><span class="sxs-lookup"><span data-stu-id="a866c-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="a866c-119">Be to, pardavimo kainas galite nustatyti pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą ar bet kokį kitą jų derinį.</span><span class="sxs-lookup"><span data-stu-id="a866c-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="a866c-120">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją valandiniame žurnale, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a866c-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a866c-121">Pavyzdžiui, jei nustatyta tiek bendra pardavimų kaina, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a866c-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="a866c-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a866c-122">Select **Save**.</span></span>
12. <span data-ttu-id="a866c-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a866c-123">Close the page.</span></span>
13. <span data-ttu-id="a866c-124">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Kaštų kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="a866c-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="a866c-125">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a866c-125">Select **New**.</span></span>
15. <span data-ttu-id="a866c-126">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a866c-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="a866c-127">Lauke **Kaštų kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a866c-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="a866c-128">Galima užpildyti kelis laukus, bet tai mažiausia, ką reikia atlikti, norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="a866c-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="a866c-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a866c-129">Select **Save**.</span></span>
18. <span data-ttu-id="a866c-130">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="a866c-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="a866c-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a866c-131">Select **New**.</span></span>
20. <span data-ttu-id="a866c-132">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="a866c-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="a866c-133">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a866c-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="a866c-134">Lauke **Kainodara** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a866c-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="a866c-135">Faktinė pardavimo kaina, kuri taikoma darbuotojui įvedus operaciją į išlaidų žurnalą, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a866c-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="a866c-136">Pavyzdžiui, jei nustatyta tiek bendra, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="a866c-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="a866c-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a866c-137">Select **Save**.</span></span>

