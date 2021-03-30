---
title: „Planning Optimization“ apžvalga
description: Šioje temoje pateikiama „Planning Optimization“ funkcijos apžvalga.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: cf64c3dea6fe08c36388f5f7147795221cf85b8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224480"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="895ab-103">„Planning Optimization“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="895ab-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="895ab-104">„Planning Optimization“ papildinys, skirtas „Microsoft Dynamics 365 Supply Chain Management“, leidžia, kad pagrindinių duomenų skaičiavimas vyktų ne „Dynamics 365 Supply Chain Management“ ir susijusioje SQL duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="895ab-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="895ab-105">„Planning Optimization“ funkcijos privalumai yra geresnis veikimas ir minimalus poveikis SQL duomenų bazei pagrindinių planavimų vykdymų metu.</span><span class="sxs-lookup"><span data-stu-id="895ab-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="895ab-106">Greitą planavimo vykdymą galima atlikti netgi darbo valandomis, kad planuotojai galėtų nedelsiant reaguoti į poreikį ir parametrų keitimus.</span><span class="sxs-lookup"><span data-stu-id="895ab-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="895ab-107">Norėdami naudoti „Planning Optimization“, turite įdiegti „Planning Optimization“ papildinį iš savo projekto, esančio „Microsoft Dynamics Lifecycle Services“ (LCS), ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="895ab-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="895ab-108">Daugiau informacijos žr. [Darbo su „Planning Optimization“ pradžia](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="895ab-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="895ab-109">Toliau pateiktame paveiksle parodyta, kaip veikia „Planning Optimization“ funkcija darbo valandomis.</span><span class="sxs-lookup"><span data-stu-id="895ab-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![„Planning Optimization“ vykdymo darbo valandomis privalumas](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="895ab-111">Geresnis efektyvumas</span><span class="sxs-lookup"><span data-stu-id="895ab-111">Improved performance</span></span>

<span data-ttu-id="895ab-112">„Planning Optimization“ gali būti naudojama scenarijuose, kuriuose yra ilgai vykdomų bendrųjų planų.</span><span class="sxs-lookup"><span data-stu-id="895ab-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="895ab-113">Jis konkrečiai sukurtas itin greitiems skaičiavimams, kuriuose yra daug duomenų.</span><span class="sxs-lookup"><span data-stu-id="895ab-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="895ab-114">Kadangi jis yra sukurtas kaip aukšto mastelio multinuomotojų paslauga, keli egzemplioriai vienu metu gali dirbti kartu, kad apskaičiuotų planą.</span><span class="sxs-lookup"><span data-stu-id="895ab-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="895ab-115">Be to, planavimo paslauga pašalina bendrojo planavimo įkėlimą iš sistemos ir dirba su duomenų srautu, kuris sumažina serverio apkrovą.</span><span class="sxs-lookup"><span data-stu-id="895ab-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="895ab-116">„Planning Optimization“ funkcija gali padėti pasiekti toliau nurodytus tikslus.</span><span class="sxs-lookup"><span data-stu-id="895ab-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="895ab-117">Pagerinti planavimo efektyvumą per trumpesnį vykdymo laiką.</span><span class="sxs-lookup"><span data-stu-id="895ab-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="895ab-118">Sumažinti poveikį kitiems procesams bendrojo planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="895ab-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="895ab-119">Dažniau atlikti planavimo vykdymus.</span><span class="sxs-lookup"><span data-stu-id="895ab-119">Do more frequent planning runs.</span></span> <span data-ttu-id="895ab-120">(Neriboja dienos vykdymų skaičius.)</span><span class="sxs-lookup"><span data-stu-id="895ab-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="895ab-121">Užtikrinti, kad būsimas verslo augimas neperaugs planavimo sistemos.</span><span class="sxs-lookup"><span data-stu-id="895ab-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="895ab-122">Architektūra ir duomenų srautai</span><span class="sxs-lookup"><span data-stu-id="895ab-122">Architecture and data flow</span></span>

<span data-ttu-id="895ab-123">Kai „Planning Optimization“ papildinys įdiegtas iš LCS, sukuriamas saugus ryšys su „Planning Optimization“ paslauga.</span><span class="sxs-lookup"><span data-stu-id="895ab-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="895ab-124">Paslauga yra toje pačioje duomenų centro šalyje ar regione kaip ir susijęs „Supply Chain Management“ egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="895ab-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="895ab-125">Nustačius „Planning Optimization“, vykdant bendrąjį planavimą, pagrindiniai duomenys ir operacijų duomenys siunčiami iš „Supply Chain Management“ į „Planning Optimization“ tarnybą.</span><span class="sxs-lookup"><span data-stu-id="895ab-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="895ab-126">Jei išdiegiamas „Planning Optimization“ papildinys, pašalinami visi susiję „Planning Optimization“ paslaugos duomenys.</span><span class="sxs-lookup"><span data-stu-id="895ab-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="895ab-127">Aukšto lygio duomenų srautas, skirtas regeneravimo vykdymui</span><span class="sxs-lookup"><span data-stu-id="895ab-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="895ab-128">„Supply Chain Management“ klientas siunčia signalą, kad pateiktų užklausą dėl planavimo vykdymo iš „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="895ab-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="895ab-129">„Planning Optimization“ prašo reikiamų duomenų per integruotą jungtį.</span><span class="sxs-lookup"><span data-stu-id="895ab-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="895ab-130">SQL duomenų bazė siunčia prašomą informaciją apie nustatymus, pagrindinius ir operacijų duomenis į „Planning Optimization“ per jungtį.</span><span class="sxs-lookup"><span data-stu-id="895ab-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="895ab-131">Jungtis verčia informaciją tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos.</span><span class="sxs-lookup"><span data-stu-id="895ab-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="895ab-132">„Planning Optimization“ paslauga atmintyje turi su planavimu susijusių duomenų ir atlieka reikalingus skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="895ab-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="895ab-133">Planavimo rezultatas per jungtį siunčiamas į „Supply Chain Management“ duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="895ab-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="895ab-134">Rezultatuose pateikiama informacija, pvz., suplanuoti užsakymai ir iškvietimo informacija.</span><span class="sxs-lookup"><span data-stu-id="895ab-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="895ab-135">„Planning Optimization“ siunčia signalą į „Supply Chain Management“, kad nurodytų, jog planavimo vykdymas baigtas.</span><span class="sxs-lookup"><span data-stu-id="895ab-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="895ab-136">Jis taip pat siunčia visus susijusius pranešimus ir įspėjimus.</span><span class="sxs-lookup"><span data-stu-id="895ab-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="895ab-137">Tolesnėje iliustracijoje pavaizduotas duomenų srautas.</span><span class="sxs-lookup"><span data-stu-id="895ab-137">The following illustration shows the data flow.</span></span>

![Duomenų srautas, skirtas regeneravimo vykdymui](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="895ab-139">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="895ab-139">Related resources</span></span>

[<span data-ttu-id="895ab-140">Darbo su „Planning Optimization“ pradžia</span><span class="sxs-lookup"><span data-stu-id="895ab-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="895ab-141">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="895ab-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="895ab-142">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="895ab-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="895ab-143">Filtrų taikymas planui</span><span class="sxs-lookup"><span data-stu-id="895ab-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="895ab-144">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="895ab-144">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]