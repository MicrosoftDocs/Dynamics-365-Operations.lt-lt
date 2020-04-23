---
title: Priežiūros užklausos ciklo būsenos
description: Šioje temoje aprašoma, kaip nustatyti priežiūros užklausos ciklo būsenas modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1e4412af0619b57467b5bcba75ea7259604d1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209012"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="e9baf-103">Priežiūros užklausos ciklo būsenos</span><span class="sxs-lookup"><span data-stu-id="e9baf-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e9baf-104">Priežiūros užklausos ciklo būsenos nurodo etapus, kuriuose gali būti užklausa.</span><span class="sxs-lookup"><span data-stu-id="e9baf-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="e9baf-105">Pavyzdžiui, **Sukurta**, **Aktyvi**ir **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="e9baf-106">Kai priežiūros užklausa konvertuojama į darbo užsakymą, priežiūros užklausos ciklo būsena turėtų būti atnaujinta į **Baigta** arba **Uždaryta**, siekiant nurodyti, kad priežiūros užklausa yra nebeaktyvi.</span><span class="sxs-lookup"><span data-stu-id="e9baf-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="e9baf-107">Sąrašo puslapyje **Visos priežiūros užklausos** galite matyti visas priežiūros užklausas, neatsižvelgiant į jų ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="e9baf-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="e9baf-108">Priežiūros užklausos ciklo būsenų nustatymas</span><span class="sxs-lookup"><span data-stu-id="e9baf-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="e9baf-109">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užsakymai** \> **Ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="e9baf-110">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="e9baf-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="e9baf-111">Lauke **Ciklo būsena** įveskite ciklo būsenos ID.</span><span class="sxs-lookup"><span data-stu-id="e9baf-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="e9baf-112">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e9baf-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e9baf-113">„FastTab“ skirtuko **Informacija** lauke **Ciklo modeliai** matysite priežiūros užklausų ciklo modelių, kurie naudoja šią ciklo būseną, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e9baf-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="e9baf-114">„FastTab" skirtuke **Bendra** nustatykite parinktį **Aktyvi** į **Taip**, jei priežiūros užklausa turėtų būti aktyvi, kol ji yra šioje ciklo būsenoje.</span><span class="sxs-lookup"><span data-stu-id="e9baf-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="e9baf-115">Nustatykite parinktį **Nustatyti faktinę pabaigą** į **Taip**, jei faktinė pabaigos data ir laikas turėtų būti automatiškai įvedami į šioje ciklo būsenoje esančią priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="e9baf-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="e9baf-116">Nustatykite parinktį **Kurti darbo užsakymą** į **Taip**, jei darbo užsakymas gali būti sukurtas iš šioje ciklo būsenoje esančios priežiūros užklausos.</span><span class="sxs-lookup"><span data-stu-id="e9baf-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="e9baf-117">Nustatykite parinktį **Trinti** į **Taip**, jei priežiūros užklausa gali būti ištrinta jai esant šioje ciklo būsenoje.</span><span class="sxs-lookup"><span data-stu-id="e9baf-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="e9baf-118">„FastTab“ skirtuke **Naujinimas**, parinktys **Gaunama** ir **Siunčiama**, esančios skyriuje **Turtas**, yra svarbios, jei naudojate sandėlio remontą. Nustatykite reikiamą parinktį į **Taip**, jei turto ciklo būsena, pasirinkta priežiūros užklausoje, turėtų būti automatiškai atnaujinta į **Gaunama** arba **Siunčiama**, kai priežiūros užklausos ciklo būsena nustatyta į **Gaunama** arba **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="e9baf-119">Paveikslėlyje pavaizduotas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e9baf-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Priežiūros užklausos ciklo būsenų puslapis](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="e9baf-121">Priežiūros užklausos ciklo būsenos, ciklo būsenos grupės bei tipai yra susiję ir naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, ciklo būsenos grupės bei tipai.</span><span class="sxs-lookup"><span data-stu-id="e9baf-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="e9baf-122">Priežiūros užklausos ciklo modelių nustatymas</span><span class="sxs-lookup"><span data-stu-id="e9baf-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="e9baf-123">Sukūrę ciklo būsenas, kurios yra reikalingos jūsų priežiūros užklausoms, jas galite suskirstyti į ciklo būsenos grupes arba ciklo modelius.</span><span class="sxs-lookup"><span data-stu-id="e9baf-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="e9baf-124">Priežiūros užklausų ciklo modeliai naudojami norint sukurti srautą, kuris gali būti naudojamas įvairių tipų priežiūros užklausoms.</span><span class="sxs-lookup"><span data-stu-id="e9baf-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="e9baf-125">Turi būti sukuriamas mažiausiai vienas standartinis priežiūros užklausos ciklo modelis.</span><span class="sxs-lookup"><span data-stu-id="e9baf-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="e9baf-126">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užklausos** \> **Ciklo modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="e9baf-127">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="e9baf-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="e9baf-128">Lauke **Ciklo modelis** įveskite ciklo modelio ID.</span><span class="sxs-lookup"><span data-stu-id="e9baf-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="e9baf-129">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e9baf-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e9baf-130">„FastTab“ skirtuko **Informacija** eilutėje **Ciklo būsenos** rodomas šiame ciklo modelyje pasirinktų ciklo būsenų skaičius.</span><span class="sxs-lookup"><span data-stu-id="e9baf-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="e9baf-131">Lauke **Priežiūros užklausos tipai** matysite šiame ciklo modelyje naudojamų priežiūros užklausos tipų skaičių.</span><span class="sxs-lookup"><span data-stu-id="e9baf-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="e9baf-132">„FastTab“ skirtuke **Ciklo būsenos** pasirinkite ciklo būsenas, kurios turėtų būti įtrauktos į šį ciklo modelį:</span><span class="sxs-lookup"><span data-stu-id="e9baf-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="e9baf-133">Norėdami į ciklo modelį įtraukti ciklo būseną, pasirinkite ją skyriuje **Likusios ciklo būsenos** ir spustelėkite dešiniosios rodyklės mygtuką ![Dešinioji rodyklė](media/03-setup-for-requests.png), kad ją perkeltumėte į skyrių **Pasirinktos ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e9baf-134">Norėdami į ciklo modelį įtraukti visas galimas ciklo būsenas, spustelėkite mygtuką **Pasirinkti visas galimas būsenas** ![Pasirinkti visas galimas būsenas](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="e9baf-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="e9baf-135">Visos ciklo būsenos bus perkeltos į skyrių **Pasirinktos ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e9baf-136">Norėdami ciklo būseną pašalinti iš ciklo modelio, ją pasirinkite skyriuje **Pasirinktos ciklo būsenos** ir spustelėkite kairiosios rodyklės mygtuką ![Kairioji rodyklė](media/05-setup-for-requests.png), kad ją perkeltumėte į skyrių **Likusios ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e9baf-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="e9baf-137">„FastTab“ skirtuko **Bendra** skyriuje **Atnaujinimai** esantys laukai yra svarbūs, jei naudojate sandėlio remontą.</span><span class="sxs-lookup"><span data-stu-id="e9baf-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="e9baf-138">Lauke **Gauto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis gaunamas sandėlio remontui.</span><span class="sxs-lookup"><span data-stu-id="e9baf-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="e9baf-139">Lauke **Išsiųsto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis bus sugrąžintas po remonto darbų.</span><span class="sxs-lookup"><span data-stu-id="e9baf-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="e9baf-140">Paveikslėlyje pateiktas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e9baf-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Priežiūros užklausos ciklo modelių puslapis](media/06-setup-for-requests.png)
