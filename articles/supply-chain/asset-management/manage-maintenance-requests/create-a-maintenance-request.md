---
title: Priežiūros užklausos kūrimas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas sukurti priežiūros užklausą.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9a6b4daf1a29b032bb82f46aaabccb2231a83a8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205235"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="8c32c-103">Priežiūros užklausos kūrimas</span><span class="sxs-lookup"><span data-stu-id="8c32c-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8c32c-104">Priežiūros užklausas galima kurti tada, kai techninės priežiūros darbuotojai arba gamybos darbuotojai nustato, kad įrangą reikia taisyti, tačiau remonto atlikti iš karto negalima.</span><span class="sxs-lookup"><span data-stu-id="8c32c-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="8c32c-105">**Pavyzdžiui:** Pavyzdžiui, techninės priežiūros darbuotojas atlieka remonto darbus ir pamato, kad reikia sutaisyti toje pačioje vietoje esančią detalę.</span><span class="sxs-lookup"><span data-stu-id="8c32c-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="8c32c-106">Tačiau techninės priežiūros darbuotojas neturi laiko ar reikalingų atsarginių dalių, kad atliktų remonto darbus.</span><span class="sxs-lookup"><span data-stu-id="8c32c-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="8c32c-107">Todėl techninės priežiūros darbuotojas sukuria priežiūros užklausą ir trumpai aprašo problemą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="8c32c-108">Srities **Susijusi informacija**, esančios dešinėje puslapio **Visas turtas** arba **Aktyvus turtas** pusėje (**Turto valdymas**\>**Bendra**\>**Turtas**\>**Visas turtas** arba **Aktyvus turtas**), skyriuje **Aktyvios priežiūros užklausos** rodomos aktyviosios priežiūros užklausos, kurios pridėtos prie pasirinkto turto.</span><span class="sxs-lookup"><span data-stu-id="8c32c-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="8c32c-109">Pasirinkite**Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="8c32c-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-110">Select **New**.</span></span>
3. <span data-ttu-id="8c32c-111">Dialogo lange **Kurti užklausą**, lauke **Priežiūros užklausos tipas** pasirinkite priežiūros užklausos tipą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="8c32c-112">Rekomenduojamas numatytasis tipas.</span><span class="sxs-lookup"><span data-stu-id="8c32c-112">A default type is suggested.</span></span>
4. <span data-ttu-id="8c32c-113">Lauke **Aprašas** įrašykite užklausos pavadinimą, kuris apibūdintų priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="8c32c-114">Laukuose **Funkcinė vietovė** ir **Turtas** pasirinkite funkcinę vietovę, turtą arba funkcinės vietovės ir turto derinį.</span><span class="sxs-lookup"><span data-stu-id="8c32c-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="8c32c-115">Galite sukurti priežiūros užklausą nepasirinkdami turto, nes jį galimą pridėti prie priežiūros užklausos vėliau.</span><span class="sxs-lookup"><span data-stu-id="8c32c-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="8c32c-116">Jei prisijungęs priežiūros darbuotojas yra susijęs su ištekliais, kurie susiję su turtu, laukas **Turtas** nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="8c32c-116">If the maintenance worker who is signed in is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="8c32c-117">Jei priežiūros užklausa jau pridėta prie pasirinkto turto, dialogo lango **Kurti užklausą** viršuje pasirodo pranešimo juosta, kuri nurodo esamos priežiūros užklausos ID.</span><span class="sxs-lookup"><span data-stu-id="8c32c-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="8c32c-118">Pranešimo juosta taip pat įspėja apie garantijos sutartį.</span><span class="sxs-lookup"><span data-stu-id="8c32c-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="8c32c-119">Lauke **Aptarnavimo lygis** pasirinkite aptarnavimo lygį, nurodantį užklausos skubumą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="8c32c-120">Jei turtą pasirinkote 5 veiksme, gedimo registravimą galite sukurti naudodami laukus **Gedimo požymis**, **Gedimo sritis** ir **Gedimo tipas**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="8c32c-121">Jei vykdant priežiūros užklausą atsirado techninės priežiūros prastova, įveskite prastovos pradžios datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8c32c-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="8c32c-122">Lauke **Pradėta** automatiškai atsiranda jūsų vardas.</span><span class="sxs-lookup"><span data-stu-id="8c32c-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="8c32c-123">**Faktinis pradžios laikas** laukas automatiškai nustatomas į dabartinę datą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="8c32c-124">Tačiau šio lauko reikšmę galite keisti.</span><span class="sxs-lookup"><span data-stu-id="8c32c-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="8c32c-125">Lauke **Pastabos** įveskite papildomas pastabas.</span><span class="sxs-lookup"><span data-stu-id="8c32c-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="8c32c-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-126">Select **OK**.</span></span>

![Kurti priežiūros užklausą](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="8c32c-128">Vėlesnis priežiūros užklausų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8c32c-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="8c32c-129">Sukūrus priežiūros užklausą, joje reikia atnaujinti tam tikrą informaciją, tačiau tai reikia atlikti prieš sukonvertuojant užklausą į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="8c32c-130">Paprastai šią užduotį atlieka planuotojas arba administratorius.</span><span class="sxs-lookup"><span data-stu-id="8c32c-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="8c32c-131">Puslapyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos** pasirinkite norimą užklausą, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="8c32c-132">Išsamios informacijos rodinyje galite atnaujinti įvairią informaciją.</span><span class="sxs-lookup"><span data-stu-id="8c32c-132">In the details view, you can update various information.</span></span> <span data-ttu-id="8c32c-133">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="8c32c-133">Here are some examples:</span></span>

- <span data-ttu-id="8c32c-134">Pasirinkite ir patvirtinkite turtą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-134">Select and verify the asset.</span></span> <span data-ttu-id="8c32c-135">Jei vėliau norite pasirinkti kitą turtą, galite nustatyti parinktį **Turtas patvirtintas** į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="8c32c-136">Pasirinkite atsakingą darbuotojų grupę ir (arba) atsakingą priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="8c32c-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="8c32c-137">Daugiau informacijos apie būtiną konfigūraciją rasite [Už priežiūrą atsakingi darbininkai](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="8c32c-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="8c32c-138">Pasirinkite priežiūros užduoties tipą ir, jei reikia, atitinkamą priežiūros užduoties variantą ir prekybą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="8c32c-139">Laukuose **Platuma** ir **Ilguma** įveskite geografines koordinates.</span><span class="sxs-lookup"><span data-stu-id="8c32c-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="8c32c-140">Visos į priežiūros užklausą įtrauktos koordinatės automatiškai perkeliamos į atitinkamą darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Priežiūros užklausos atnaujinimas](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="8c32c-142">Jei kurdami priežiūros užklausą pasirenkate turtą, prie jo galite pridėti vieną gedimą.</span><span class="sxs-lookup"><span data-stu-id="8c32c-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="8c32c-143">Sukūrę priežiūros užklausą, pagal poreikius galite pridėti ir daugiau gedimų.</span><span class="sxs-lookup"><span data-stu-id="8c32c-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="8c32c-144">Norėdami pridėti daugiau gedimų, puslapyje **Visos priežiūros užklausos** pasirinkite **Turto gedimas**.</span><span class="sxs-lookup"><span data-stu-id="8c32c-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
