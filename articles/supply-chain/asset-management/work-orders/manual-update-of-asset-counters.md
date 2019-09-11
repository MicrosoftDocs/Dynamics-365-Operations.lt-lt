---
title: Neautomatinis turto skaitiklių atnaujinimas
description: Šioje temoje aprašomas turto skaitiklių naujinimas rankiniu būdu skiltyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875800"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="5467e-103">Neautomatinis turto skaitiklių atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="5467e-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="5467e-104">Skaitikliai naudojami kuriant turto registracijas, pvz., operacijos valandų skaičių arba pagamintų kiekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="5467e-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="5467e-105">Jei skaitikliui parinktas skaitiklio tipas nustatytas perimti skaitiklio reikšmes (**Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai** > **Bendra** „FastTab“ > **Perimti turto skaitiklio vertes** perjungiklis nustatytas į Taip), tada, kai kursite to tipo naują skaitiklio eilutę, kiekvienas antrinis turtas, naudojantis tą patį skaitiklio tipą, automatiškai naujinamas.</span><span class="sxs-lookup"><span data-stu-id="5467e-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="5467e-106">Skiltyje **Visas turtas** galite turtui sukurti valandų ar dydžio skaitiklių registracijų, atsižvelgiant į jūsų turto rodmenis.</span><span class="sxs-lookup"><span data-stu-id="5467e-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="5467e-107">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Turtas** > **Visas turtas**.</span><span class="sxs-lookup"><span data-stu-id="5467e-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="5467e-108">Sąraše pasirinkite turtą ir spustelėkite **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="5467e-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="5467e-109">Formoje **Turto skaitikliai** galite matyti visų buvusių skaitiklių registracijų pasirinktam turtui sąrašą.</span><span class="sxs-lookup"><span data-stu-id="5467e-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="5467e-110">Spustelėkite **Naujas**, kad sukurtumėte naują registraciją.</span><span class="sxs-lookup"><span data-stu-id="5467e-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="5467e-111">Turto ID įterpiamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="5467e-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="5467e-112">Lauke **Skaitiklis** pažymėkite susijusį skaitiklį.</span><span class="sxs-lookup"><span data-stu-id="5467e-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="5467e-113">Tik skaitikliai, susiję su turto tipu, pasirinktu tam turtui, yra pasiekiami.</span><span class="sxs-lookup"><span data-stu-id="5467e-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="5467e-114">Susijęs vienetas yra automatiškai įterpiamas į lauką **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="5467e-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="5467e-115">Skaitiklio registracijai nurodykite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="5467e-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="5467e-116">Lauke **Reikšmė** įterpkite paskutinio skaitiklio registracijos numerį arba, į lauką **Agreguota reikšmė** įterpkite bendrą skaitiklių numerį.</span><span class="sxs-lookup"><span data-stu-id="5467e-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="5467e-117">Jeigu įdiegėte turtui rankiniu būdu naują skaitiklį, turite užregistruoti pakeitimus turtui skiltyje **Turto skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="5467e-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="5467e-118">Po to, turite sukurti dvi registravimo eilutes, kurių laiko žymės sutampa, ir eilutėje, kurioje yra naujas skaitiklis, pasirinkti žymės langelį **Skaitiklio atkūrimas**.</span><span class="sxs-lookup"><span data-stu-id="5467e-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="5467e-119">Kai sukuriate dvi registravimo eilutes, pirmoje eilutėje turi būti skaitiklis, kurį keičiate.</span><span class="sxs-lookup"><span data-stu-id="5467e-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="5467e-120">Lauke **Iš viso** bendras skaitiklių skaičius yra visų to skaitiklio tipo užregistruotų reikšmių bendra skaitiklių suma.</span><span class="sxs-lookup"><span data-stu-id="5467e-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="5467e-121">Jei pasirinktas laukas **Skaitiklio atkūrimas**, naudojant priežiūros planą, kuriame yra intervalų tipas Pradėjus nuo... arba Pasiekus..., skaitiklis tebėra aktyvus naujoje skaitiklio eilutėje, nes sukuriate atskirą skaitiklio eilutę ir pradedate naujai numeruoti skaitiklius.</span><span class="sxs-lookup"><span data-stu-id="5467e-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![1 pav.](media/11-work-orders.png)


<span data-ttu-id="5467e-123">Jei jums reikia registruoti skaitiklį keliems ištekliams, tai galite atlikti pasirinkus **Turto valdymas** > **Užklausos** > **Turtas** > **Turto skaitikliai.**</span><span class="sxs-lookup"><span data-stu-id="5467e-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="5467e-124">Galite nustatyti intervalą, kad būtų apibrėžti nuokrypiai, kurie atsiranda rankiniu būdu registruojant skaitiklius, ir pranešimo tipas, kuris turi būti rodomas, jei registruojant nukrypstama nuo nurodyto intervalo.</span><span class="sxs-lookup"><span data-stu-id="5467e-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="5467e-125">Dėl skaitiklių sąrankos žr. temoje [Skaitikliai](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="5467e-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
