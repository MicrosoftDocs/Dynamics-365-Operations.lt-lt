---
title: Aptarnavimo lygis ir aprašas
description: Šioje temoje paaiškintas aptarnavimo lygis ir aprašas modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874652"
---
# <a name="service-level-and-description"></a><span data-ttu-id="1f394-103">Aptarnavimo lygis ir aprašas</span><span class="sxs-lookup"><span data-stu-id="1f394-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1f394-104">Sukūrę darbo užsakymą galbūt norėsite nustatyti darbo užsakymo aptarnavimo lygius ir į jį įtraukti bendrą aprašą.</span><span class="sxs-lookup"><span data-stu-id="1f394-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="1f394-105">Darbo užsakymo aptarnavimo lygius galite kurti puslapyje **Darbo užsakymo aptarnavimo lygiai**, o aprašus – puslapyje **Darbo užsakymo aprašas**.</span><span class="sxs-lookup"><span data-stu-id="1f394-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="1f394-106">Aptarnavimo lygio kūrimas</span><span class="sxs-lookup"><span data-stu-id="1f394-106">Create a service level</span></span>

1. <span data-ttu-id="1f394-107">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aptarnavimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="1f394-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="1f394-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f394-108">Select **New**.</span></span>
3. <span data-ttu-id="1f394-109">Lauke **Aptarnavimo lygis** įveskite aptarnavimo lygį (pvz., skaičių).</span><span class="sxs-lookup"><span data-stu-id="1f394-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="1f394-110">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1f394-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="1f394-111">„FastTab“ **Darbo užsakymai** galite nustatyti numatomas pradžios ir pabaigos datas ir laiką.</span><span class="sxs-lookup"><span data-stu-id="1f394-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="1f394-112">Šio „FastTab“ laukai nustato laikotarpį, kuriuo darbo užsakymai turėtų būti pradėti ir užbaigti.</span><span class="sxs-lookup"><span data-stu-id="1f394-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="1f394-113">Jie naudojami rankiniu būdu sukurtuose darbo užsakymuose ir darbo užsakymuose, kurie kuriami pagal priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="1f394-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="1f394-114">Lauke **Pradžios diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų prasidėti darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="1f394-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="1f394-115">Dienų skaičius skaičiuojamas nuo darbo užsakymo sukūrimo datos.</span><span class="sxs-lookup"><span data-stu-id="1f394-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="1f394-116">Pavyzdžiui, jei darbo užsakymas turėtų būti pradėtas jį sukūrus, įveskite **0**.</span><span class="sxs-lookup"><span data-stu-id="1f394-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="1f394-117">Jei darbo užsakymas turėtų būti pradėtas per vieną savaitę nuo jo sukūrimo, įveskite **7**.</span><span class="sxs-lookup"><span data-stu-id="1f394-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="1f394-118">Jei be darbo užsakymo pradžios datos norite nustatyti jo pradžios laiką, nustatykite parinkties **Nustatyti pradžios laiką** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1f394-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="1f394-119">Tada lauke **Pradžios laikas** įveskite pradžios laiką.</span><span class="sxs-lookup"><span data-stu-id="1f394-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="1f394-120">Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.</span><span class="sxs-lookup"><span data-stu-id="1f394-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="1f394-121">Lauke **Pabaigos diena** įveskite dienų skaičių, kad nustatytumėte laikotarpį, kuriuo turėtų pasibaigti darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="1f394-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="1f394-122">Dienų skaičius skaičiuojamas nuo darbo užsakymo pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="1f394-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="1f394-123">Pavyzdžiui, jei darbo užsakymas turėtų būti užbaigtas per vieną savaitę nuo jo pradžios datos, įveskite **7**.</span><span class="sxs-lookup"><span data-stu-id="1f394-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="1f394-124">Jei be darbo užsakymo pabaigos datos norite nustatyti jo pabaigos laiką, nustatykite parinkties **Nustatyti pabaigos laiką** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1f394-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="1f394-125">Tada lauke **Pabaigos laikas** įveskite pabaigos laiką.</span><span class="sxs-lookup"><span data-stu-id="1f394-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="1f394-126">Jei nustatysite parinkties nuostatą **Ne**, bus naudojamas dabartinis dienos laikas.</span><span class="sxs-lookup"><span data-stu-id="1f394-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="1f394-127">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f394-127">Select **Save**.</span></span>

![1 pav.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="1f394-129">Aprašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="1f394-129">Create a description</span></span>

1. <span data-ttu-id="1f394-130">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Aprašai**.</span><span class="sxs-lookup"><span data-stu-id="1f394-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="1f394-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1f394-131">Select **New**.</span></span>
3. <span data-ttu-id="1f394-132">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="1f394-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="1f394-133">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1f394-133">Select **Save**.</span></span>
