---
title: Konfigūruoti darbo ir išlaidų standartines išlaidas
description: Šioje procedūroje nurodoma, kaip nustatyti standartinę projekto darbo ir išlaidų savikainą.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572401"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="e1edc-103">Konfigūruoti darbo ir išlaidų standartines išlaidas</span><span class="sxs-lookup"><span data-stu-id="e1edc-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1edc-104">Šioje procedūroje nurodoma, kaip nustatyti standartinę projekto darbo ir išlaidų savikainą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="e1edc-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="e1edc-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e1edc-106">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (valanda).</span><span class="sxs-lookup"><span data-stu-id="e1edc-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="e1edc-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e1edc-107">Click New.</span></span>
3. <span data-ttu-id="e1edc-108">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="e1edc-109">Lauke Savikaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e1edc-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="e1edc-110">Galite nustatyti standartinę projekto kategorijos savikainą arba nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokį jų derinį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="e1edc-111">Tada taikoma savikaina apibrėžiama išsamiausiai.</span><span class="sxs-lookup"><span data-stu-id="e1edc-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="e1edc-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e1edc-112">Click Save.</span></span>
6. <span data-ttu-id="e1edc-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-113">Close the page.</span></span>
7. <span data-ttu-id="e1edc-114">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (valanda).</span><span class="sxs-lookup"><span data-stu-id="e1edc-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="e1edc-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e1edc-115">Click New.</span></span>
9. <span data-ttu-id="e1edc-116">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="e1edc-117">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="e1edc-118">Lauke Kainos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e1edc-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="e1edc-119">Galite nustatyti standartinę valandinių operacijų pardavimo kainą ar projekto kategoriją.</span><span class="sxs-lookup"><span data-stu-id="e1edc-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="e1edc-120">Be to, pardavimo kainas galite nustatyti pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą ar bet kokį kitą jų derinį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="e1edc-121">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją valandiniame žurnale, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="e1edc-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e1edc-122">Pavyzdžiui, jei nustatyta tiek bendra pardavimų kaina, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="e1edc-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="e1edc-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e1edc-123">Click Save.</span></span>
13. <span data-ttu-id="e1edc-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-124">Close the page.</span></span>
14. <span data-ttu-id="e1edc-125">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Savikaina (išlaidos).</span><span class="sxs-lookup"><span data-stu-id="e1edc-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="e1edc-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e1edc-126">Click New.</span></span>
16. <span data-ttu-id="e1edc-127">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="e1edc-128">Lauke Savikaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e1edc-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="e1edc-129">Galima užpildyti kelis laukus, bet tai mažiausia, ką reikia atlikti, norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="e1edc-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e1edc-130">Click Save.</span></span>
19. <span data-ttu-id="e1edc-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-131">Close the page.</span></span>
20. <span data-ttu-id="e1edc-132">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (išlaidos).</span><span class="sxs-lookup"><span data-stu-id="e1edc-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="e1edc-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e1edc-133">Click New.</span></span>
22. <span data-ttu-id="e1edc-134">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="e1edc-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="e1edc-135">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="e1edc-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="e1edc-136">Lauke Kainos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="e1edc-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="e1edc-137">Faktinė pardavimo kaina, kuri taikoma darbuotojui įvedus operaciją į išlaidų žurnalą, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="e1edc-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e1edc-138">Pavyzdžiui, jei nustatyta tiek bendra, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="e1edc-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="e1edc-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e1edc-139">Click Save.</span></span>

