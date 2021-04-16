---
title: Neautomatinis turto skaitiklių atnaujinimas
description: Šioje temoje aprašomas turto skaitiklių naujinimas rankiniu būdu skiltyje Turto valdymas.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4618ff2d6880f478683fbed0ed716af5ab8d4d9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842254"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="e129c-103">Neautomatinis turto skaitiklių atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="e129c-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e129c-104">Skaitikliai naudojami norint sukurti turto registracijas, pvz., registracijas apie turto operacijos valandų skaičių arba pagaminamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="e129c-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="e129c-105">Pasirenkamas skaitiklio tipas gali būti nustatytas perimti skaitiklio vertes.</span><span class="sxs-lookup"><span data-stu-id="e129c-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="e129c-106">Kitaip tariant, puslapio **Skaitikliai** „FastTab” **Bendra** esanti parinktis **Perimti turto skaitiklio vertes** nustatyta į **Taip** (**Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**).</span><span class="sxs-lookup"><span data-stu-id="e129c-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="e129c-107">Tokiu atveju, kai sukuriate naują šio tipo skaitiklio eilutę, kiekvienas antrinis turtas, kuris naudoja tą patį skaitiklio tipą, automatiškai atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="e129c-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="e129c-108">Puslapyje **Visas turtas** galite turtui sukurti valandų ar dydžio skaitiklių registracijų, atsižvelgiant į jūsų turto rodmenis.</span><span class="sxs-lookup"><span data-stu-id="e129c-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="e129c-109">Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="e129c-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="e129c-110">Pasirinkite turtą, o tada veiksmų srityje, skirtuke **Turtas**, grupėje **Prevencinis**, pasirinkite **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="e129c-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="e129c-111">Puslapyje **Turto skaitikliai** rodomas visų buvusių skaitiklių registracijų pasirinktam turtui sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e129c-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="e129c-112">Pasirinkite **Naujas**, kad sukurtumėte registraciją.</span><span class="sxs-lookup"><span data-stu-id="e129c-112">Select **New** to create a registration.</span></span> <span data-ttu-id="e129c-113">Turto ID automatiškai įvedamas lauke **Turtas**.</span><span class="sxs-lookup"><span data-stu-id="e129c-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="e129c-114">Lauke **Skaitiklis** pažymėkite susijusį skaitiklį.</span><span class="sxs-lookup"><span data-stu-id="e129c-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="e129c-115">Galima pasirinkti tik susijusius su turto tipu, pasirinktu tam turtui, skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="e129c-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="e129c-116">Susijęs vienetas yra automatiškai įvedamas į lauką **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="e129c-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="e129c-117">Lauke **Registruota** pasirinkite skaitiklio registravimo datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="e129c-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="e129c-118">Lauke **Vertė** įveskite paskutinio skaitiklio registracijos numerį.</span><span class="sxs-lookup"><span data-stu-id="e129c-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="e129c-119">Arba lauke **Agreguota vertė** įveskite bendrą skaitiklių skaičių.</span><span class="sxs-lookup"><span data-stu-id="e129c-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="e129c-120">Atkreipkite dėmesį į toliau nurodytus punktus.</span><span class="sxs-lookup"><span data-stu-id="e129c-120">Note the following points:</span></span>

- <span data-ttu-id="e129c-121">Jeigu įdiegėte turtui rankiniu būdu naują skaitiklį, turite užregistruoti pakeitimus turtui puslapyje **Turto skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="e129c-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="e129c-122">Tada turite sukurti dvi registravimo eilutes, kuriose yra vienodos laiko žymos.</span><span class="sxs-lookup"><span data-stu-id="e129c-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="e129c-123">Pirmoji eilutė turi būti skirta skaitikliui, kurį keičiate.</span><span class="sxs-lookup"><span data-stu-id="e129c-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="e129c-124">Eilutėje, kuri susijusi su nauju skaitikliu, pažymėkite žymės langelį **Skaitiklio atkūrimas**.</span><span class="sxs-lookup"><span data-stu-id="e129c-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="e129c-125">Lauke **Iš viso** bendras skaitiklių skaičius yra visų to skaitiklio tipo užregistruotų reikšmių bendra skaitiklių suma.</span><span class="sxs-lookup"><span data-stu-id="e129c-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="e129c-126">Jei pasirinktas laukas **Skaitiklio atkūrimas**, naudojant priežiūros planą, kuriame yra intervalų tipas Pradėjus nuo... arba Pasiekus..., skaitiklis tebėra aktyvus naujoje skaitiklio eilutėje, nes sukuriate atskirą skaitiklio eilutę ir pradedate naujai numeruoti skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="e129c-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="e129c-127">Toliau pateiktame paveikslėlyje parodytas puslapio **Turto skaitikliai** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e129c-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![1 pav.](media/11-work-orders.png)

<span data-ttu-id="e129c-129">Puslapyje **Turto skaitikliai** (**Turto valdymas** > **Užklausos** > **Turtas** > **Turto skaitikliai**) galite pagal poreikį tuo pačiu metu registruoti skaitiklius keliems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="e129c-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="e129c-130">Galite nustatyti intervalą, kad nustatytumėte nuokrypius, kurie atsiranda rankiniu būdu registruojant skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="e129c-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="e129c-131">Taip pat galite nurodyti pranešimo, kuris rodomas, jei registruojant nukrypstama nuo nurodyto intervalo, tipą.</span><span class="sxs-lookup"><span data-stu-id="e129c-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="e129c-132">Daugiau informacijos, kaip nustatyti skaitiklius, žr. [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="e129c-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]