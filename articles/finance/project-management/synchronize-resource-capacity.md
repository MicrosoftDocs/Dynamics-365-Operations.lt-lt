---
title: Išteklių pajėgumų sinchronizavimas
description: Šioje temoje pateikiama informacija apie tai, kaip sinchronizuoti išteklių pajėgumą įvairiuose kalendoriuose ir projektuose.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760612"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4736c-103">Išteklių pajėgumų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="4736c-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4736c-104">Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija būtų perduodama bei naudojama ir planuojant projekto išteklius.</span><span class="sxs-lookup"><span data-stu-id="4736c-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4736c-105">Jei kalendorius pakinta, procesais pagal poreikį atnaujinamas projekto išteklių planavimas.</span><span class="sxs-lookup"><span data-stu-id="4736c-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4736c-106">Šie procesai taip pat padeda gerinti našumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto.</span><span class="sxs-lookup"><span data-stu-id="4736c-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4736c-107">Todėl greičiau atnaujinama išteklių planavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="4736c-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4736c-108">Rekomenduojame procesus planuoti kaip paketą, o ne po vieną.</span><span class="sxs-lookup"><span data-stu-id="4736c-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4736c-109">Kitu atveju atsiranda rizika, kad kažkas pamirš informacijos paskutinį sinchronizavimą apimančias datas.</span><span class="sxs-lookup"><span data-stu-id="4736c-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4736c-110">Jei apimančiosios datos nenaudojamos, sinchronizuojant datas gali atsirasti tarpų.</span><span class="sxs-lookup"><span data-stu-id="4736c-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4736c-112">Sinchronizuoti išteklių pajėgumų sumavimus</span><span class="sxs-lookup"><span data-stu-id="4736c-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4736c-113">Sinchronizavimo procesas skirtas sinchronizuoti visai išteklių kalendoriaus informacijai.</span><span class="sxs-lookup"><span data-stu-id="4736c-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4736c-114">Ši informacija apima pagrindinio kalendoriaus informaciją apie visus projekto išteklių kalendoriaus pajėgumo lentelės keitimus.</span><span class="sxs-lookup"><span data-stu-id="4736c-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4736c-115">Jei į projektą įtraukiama naujų išteklių, sinchronizavimas padeda užtikrinti, kad būtų prieinama atnaujinta kalendoriaus informacija.</span><span class="sxs-lookup"><span data-stu-id="4736c-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4736c-116">Šį sinchronizavimą galima atlikti bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="4736c-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4736c-117">Rekomenduojame naudoti paketą.</span><span class="sxs-lookup"><span data-stu-id="4736c-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4736c-118">Parinktys galimos sinchronizuojant pajėgumų rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="4736c-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4736c-119">Pasirinkite **Projektų valdymas ir apskaita** &gt; **Laikotarpio** &gt; **Pajėgumo sinchronizavimas** &gt; **Sinchronizuoti išteklių pajėgumų sumavimus**.</span><span class="sxs-lookup"><span data-stu-id="4736c-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4736c-120">Nustatykite tolesnėje lentelėje nurodytas parinktis.</span><span class="sxs-lookup"><span data-stu-id="4736c-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4736c-121">Parinktis</span><span class="sxs-lookup"><span data-stu-id="4736c-121">Option</span></span>      | <span data-ttu-id="4736c-122">aprašymas</span><span class="sxs-lookup"><span data-stu-id="4736c-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4736c-123">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="4736c-123">Period code</span></span> | <span data-ttu-id="4736c-124">Pasirenkama: pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="4736c-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4736c-125">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="4736c-125">Start date</span></span>  | <span data-ttu-id="4736c-126">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="4736c-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4736c-127">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="4736c-127">End date</span></span>    | <span data-ttu-id="4736c-128">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="4736c-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4736c-129">[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4736c-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
