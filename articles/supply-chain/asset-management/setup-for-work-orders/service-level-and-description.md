---
title: Aptarnavimo lygis ir aprašas
description: Šioje temoje paaiškintas aptarnavimo lygis ir aprašas modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 647358fcdd53ba95b571185ae269bc8d6b869c18
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433644"
---
# <a name="service-level-and-description"></a><span data-ttu-id="86eef-103">Aptarnavimo lygis ir aprašas</span><span class="sxs-lookup"><span data-stu-id="86eef-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="86eef-104">Sukūrę darbo užsakymą galbūt norėsite nustatyti darbo užsakymo aptarnavimo lygius ir į jį įtraukti bendrą aprašą.</span><span class="sxs-lookup"><span data-stu-id="86eef-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="86eef-105">Darbo užsakymo aptarnavimo lygius galite kurti puslapyje **Darbo užsakymo aptarnavimo lygiai**, o aprašus – puslapyje **Darbo užsakymo aprašas**.</span><span class="sxs-lookup"><span data-stu-id="86eef-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="86eef-106">Aptarnavimo lygio kūrimas</span><span class="sxs-lookup"><span data-stu-id="86eef-106">Create a service level</span></span>

1. <span data-ttu-id="86eef-107">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="86eef-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="86eef-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="86eef-108">Select **New**.</span></span>
3. <span data-ttu-id="86eef-109">Lauke **Aptarnavimo lygis** įveskite aptarnavimo lygį (pvz., skaičių).</span><span class="sxs-lookup"><span data-stu-id="86eef-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="86eef-110">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="86eef-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="86eef-111">„FastTab“ **Darbo užsakymai** galite nustatyti numatomas pradžios ir pabaigos datas ir laiką.</span><span class="sxs-lookup"><span data-stu-id="86eef-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="86eef-112">Šio „FastTab“ laukai nustato laikotarpį, kuriuo darbo užsakymai turėtų būti pradėti ir užbaigti.</span><span class="sxs-lookup"><span data-stu-id="86eef-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="86eef-113">Jie naudojami rankiniu būdu sukurtuose darbo užsakymuose ir darbo užsakymuose, kurie kuriami pagal priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="86eef-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="86eef-114">Lauke **Pradžios diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų prasidėti darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="86eef-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="86eef-115">Dienų skaičius skaičiuojamas nuo darbo užsakymo sukūrimo datos.</span><span class="sxs-lookup"><span data-stu-id="86eef-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="86eef-116">Pavyzdžiui, jei darbo užsakymas turėtų būti pradėtas jį sukūrus, įveskite **0**.</span><span class="sxs-lookup"><span data-stu-id="86eef-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="86eef-117">Jei darbo užsakymas turėtų būti pradėtas per vieną savaitę nuo jo sukūrimo, įveskite **7**.</span><span class="sxs-lookup"><span data-stu-id="86eef-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="86eef-118">Jei be darbo užsakymo pradžios datos norite nustatyti jo pradžios laiką, nustatykite parinkties **Nustatyti pradžios laiką** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="86eef-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="86eef-119">Tada lauke **Pradžios laikas** įveskite pradžios laiką.</span><span class="sxs-lookup"><span data-stu-id="86eef-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="86eef-120">Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.</span><span class="sxs-lookup"><span data-stu-id="86eef-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="86eef-121">Lauke **Pabaigos diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų pasibaigti darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="86eef-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="86eef-122">Dienų skaičius skaičiuojamas nuo darbo užsakymo pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="86eef-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="86eef-123">Pavyzdžiui, jei darbo užsakymas turėtų būti užbaigtas per vieną savaitę nuo jo pradžios datos, įveskite **7**.</span><span class="sxs-lookup"><span data-stu-id="86eef-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="86eef-124">Jei be darbo užsakymo pabaigos datos norite nustatyti jo pabaigos laiką, nustatykite parinkties **Nustatyti pabaigos laiką** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="86eef-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="86eef-125">Tada lauke **Pabaigos laikas** įveskite pabaigos laiką.</span><span class="sxs-lookup"><span data-stu-id="86eef-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="86eef-126">Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.</span><span class="sxs-lookup"><span data-stu-id="86eef-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="86eef-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="86eef-127">Select **Save**.</span></span>

![Darbo užsakymų paslaugos lygio puslapis](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="86eef-129">Aprašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="86eef-129">Create a description</span></span>

1. <span data-ttu-id="86eef-130">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aprašai**.</span><span class="sxs-lookup"><span data-stu-id="86eef-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="86eef-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="86eef-131">Select **New**.</span></span>
3. <span data-ttu-id="86eef-132">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="86eef-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="86eef-133">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="86eef-133">Select **Save**.</span></span>
