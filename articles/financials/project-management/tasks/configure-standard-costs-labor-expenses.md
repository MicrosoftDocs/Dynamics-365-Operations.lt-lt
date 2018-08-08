--- 
title: "Konfigūruoti darbo ir išlaidų standartines išlaidas"
description: "Šioje procedūroje nurodoma, kaip nustatyti standartinę projekto darbo ir išlaidų savikainą."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c69fff5d9ec031d0ffa7d45f658317cd3296615f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="9a620-103">Konfigūruoti darbo ir išlaidų standartines išlaidas</span><span class="sxs-lookup"><span data-stu-id="9a620-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a620-104">Šioje procedūroje nurodoma, kaip nustatyti standartinę projekto darbo ir išlaidų savikainą.</span><span class="sxs-lookup"><span data-stu-id="9a620-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="9a620-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="9a620-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9a620-106">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (valanda).</span><span class="sxs-lookup"><span data-stu-id="9a620-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="9a620-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9a620-107">Click New.</span></span>
3. <span data-ttu-id="9a620-108">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9a620-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="9a620-109">Lauke Savikaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9a620-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="9a620-110">Galite nustatyti standartinę projekto kategorijos savikainą arba nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokį jų derinį.</span><span class="sxs-lookup"><span data-stu-id="9a620-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="9a620-111">Tada taikoma savikaina apibrėžiama išsamiausiai.</span><span class="sxs-lookup"><span data-stu-id="9a620-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="9a620-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9a620-112">Click Save.</span></span>
6. <span data-ttu-id="9a620-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a620-113">Close the page.</span></span>
7. <span data-ttu-id="9a620-114">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (valanda).</span><span class="sxs-lookup"><span data-stu-id="9a620-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="9a620-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9a620-115">Click New.</span></span>
9. <span data-ttu-id="9a620-116">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9a620-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="9a620-117">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="9a620-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="9a620-118">Lauke Kainos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9a620-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="9a620-119">Galite nustatyti standartinę valandinių operacijų pardavimo kainą ar projekto kategoriją.</span><span class="sxs-lookup"><span data-stu-id="9a620-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="9a620-120">Be to, pardavimo kainas galite nustatyti pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą ar bet kokį kitą jų derinį.</span><span class="sxs-lookup"><span data-stu-id="9a620-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="9a620-121">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją valandiniame žurnale, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="9a620-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9a620-122">Pavyzdžiui, jei nustatyta tiek bendra pardavimų kaina, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="9a620-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="9a620-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9a620-123">Click Save.</span></span>
13. <span data-ttu-id="9a620-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a620-124">Close the page.</span></span>
14. <span data-ttu-id="9a620-125">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Savikaina (išlaidos).</span><span class="sxs-lookup"><span data-stu-id="9a620-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="9a620-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9a620-126">Click New.</span></span>
16. <span data-ttu-id="9a620-127">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9a620-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="9a620-128">Lauke Savikaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9a620-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="9a620-129">Galima užpildyti kelis laukus, bet tai mažiausia, ką reikia atlikti, norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="9a620-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="9a620-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9a620-130">Click Save.</span></span>
19. <span data-ttu-id="9a620-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a620-131">Close the page.</span></span>
20. <span data-ttu-id="9a620-132">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Pardavimo kaina (išlaidos).</span><span class="sxs-lookup"><span data-stu-id="9a620-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="9a620-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9a620-133">Click New.</span></span>
22. <span data-ttu-id="9a620-134">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9a620-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="9a620-135">Lauke Galioja pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="9a620-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="9a620-136">Lauke Kainos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9a620-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="9a620-137">Faktinė pardavimo kaina, kuri taikoma darbuotojui įvedus operaciją į išlaidų žurnalą, yra išsamiausiai apibrėžta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="9a620-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9a620-138">Pavyzdžiui, jei nustatyta tiek bendra, tiek nuo konkretaus darbuotojo priklausanti pardavimo kaina, bus naudojama nuo konkretaus darbuotojo priklausanti pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="9a620-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="9a620-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9a620-139">Click Save.</span></span>


