---
title: Priežiūros užklausos ciklo būsenos
description: Šioje temoje aprašoma, kaip nustatyti priežiūros užklausos ciklo būsenas modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9022d866bf0da08a72ba9169587f87c1b77527a6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217226"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="e46d4-103">Priežiūros užklausos ciklo būsenos</span><span class="sxs-lookup"><span data-stu-id="e46d4-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e46d4-104">Priežiūros užklausos ciklo būsenos nurodo etapus, kuriuose gali būti užklausa.</span><span class="sxs-lookup"><span data-stu-id="e46d4-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="e46d4-105">Pavyzdžiui, **Sukurta**, **Aktyvi** ir **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="e46d4-106">Kai priežiūros užklausa konvertuojama į darbo užsakymą, priežiūros užklausos ciklo būsena turėtų būti atnaujinta į **Baigta** arba **Uždaryta**, siekiant nurodyti, kad priežiūros užklausa yra nebeaktyvi.</span><span class="sxs-lookup"><span data-stu-id="e46d4-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="e46d4-107">Sąrašo puslapyje **Visos priežiūros užklausos** galite matyti visas priežiūros užklausas, neatsižvelgiant į jų ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="e46d4-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="e46d4-108">Priežiūros užklausos ciklo būsenų nustatymas</span><span class="sxs-lookup"><span data-stu-id="e46d4-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="e46d4-109">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užsakymai** \> **Ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="e46d4-110">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="e46d4-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="e46d4-111">Lauke **Ciklo būsena** įveskite ciklo būsenos ID.</span><span class="sxs-lookup"><span data-stu-id="e46d4-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="e46d4-112">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e46d4-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e46d4-113">„FastTab“ skirtuko **Informacija** lauke **Ciklo modeliai** matysite priežiūros užklausų ciklo modelių, kurie naudoja šią ciklo būseną, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e46d4-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="e46d4-114">„FastTab" skirtuke **Bendra** nustatykite parinktį **Aktyvi** į **Taip**, jei priežiūros užklausa turėtų būti aktyvi, kol ji yra šioje ciklo būsenoje.</span><span class="sxs-lookup"><span data-stu-id="e46d4-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="e46d4-115">Nustatykite parinkties **Nustatyti faktinę pabaigą** reikšmę į **Taip**, jei faktinė pabaigos data ir laikas turėtų būti automatiškai įvedami į šioje ciklo būsenoje esančią priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="e46d4-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="e46d4-116">Nustatykite parinktį **Kurti darbo užsakymą** į **Taip**, jei darbo užsakymas gali būti sukurtas iš šioje ciklo būsenoje esančios priežiūros užklausos.</span><span class="sxs-lookup"><span data-stu-id="e46d4-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="e46d4-117">Nustatykite parinktį **Trinti** į **Taip**, jei priežiūros užklausa gali būti ištrinta jai esant šioje ciklo būsenoje.</span><span class="sxs-lookup"><span data-stu-id="e46d4-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="e46d4-118">„FastTab“ konteinerio **Atnaujinimas** dalyje **Turtas** esančios parinktys **Gaunama** ir **Siunčiama** yra svarbios, jei naudojate sandėlio remontą.</span><span class="sxs-lookup"><span data-stu-id="e46d4-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="e46d4-119">Nustatykite reikiamą parinktį į **Taip**, jei priežiūros užklausoje pasirinkta turto ciklo būsena turėtų būti automatiškai atnaujinta į **Gaunama** arba **Siunčiama**, kai tos priežiūros užklausos ciklo būsena nustatyta kaip **Gaunama** arba **Siunčiama**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="e46d4-120">Paveikslėlyje pavaizduotas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e46d4-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Priežiūros užklausos ciklo būsenų puslapis](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="e46d4-122">Priežiūros užklausos ciklo būsenos, ciklo būsenos grupės bei tipai yra susiję ir naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, ciklo būsenos grupės bei tipai.</span><span class="sxs-lookup"><span data-stu-id="e46d4-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="e46d4-123">Priežiūros užklausos ciklo modelių nustatymas</span><span class="sxs-lookup"><span data-stu-id="e46d4-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="e46d4-124">Sukūrę ciklo būsenas, kurios yra reikalingos jūsų priežiūros užklausoms, jas galite suskirstyti į ciklo būsenos grupes arba ciklo modelius.</span><span class="sxs-lookup"><span data-stu-id="e46d4-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="e46d4-125">Priežiūros užklausų ciklo modeliai naudojami norint sukurti srautą, kuris gali būti naudojamas įvairių tipų priežiūros užklausoms.</span><span class="sxs-lookup"><span data-stu-id="e46d4-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="e46d4-126">Turi būti sukuriamas mažiausiai vienas standartinis priežiūros užklausos ciklo modelis.</span><span class="sxs-lookup"><span data-stu-id="e46d4-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="e46d4-127">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Priežiūros užklausos** \> **Ciklo modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="e46d4-128">Pasirinkite **Naujas**, kad sukurtumėte priežiūros užklausos ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="e46d4-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="e46d4-129">Lauke **Ciklo modelis** įveskite ciklo modelio ID.</span><span class="sxs-lookup"><span data-stu-id="e46d4-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="e46d4-130">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e46d4-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e46d4-131">„FastTab“ skirtuko **Informacija** eilutėje **Ciklo būsenos** rodomas šiame ciklo modelyje pasirinktų ciklo būsenų skaičius.</span><span class="sxs-lookup"><span data-stu-id="e46d4-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="e46d4-132">Lauke **Priežiūros užklausos tipai** matysite šiame ciklo modelyje naudojamų priežiūros užklausos tipų skaičių.</span><span class="sxs-lookup"><span data-stu-id="e46d4-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="e46d4-133">„FastTab“ skirtuke **Ciklo būsenos** pasirinkite ciklo būsenas, kurios turėtų būti įtrauktos į šį ciklo modelį:</span><span class="sxs-lookup"><span data-stu-id="e46d4-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="e46d4-134">Norėdami į ciklo modelį įtraukti ciklo būseną, pasirinkite ją skyriuje **Likusios ciklo būsenos** ir spustelėkite dešiniosios rodyklės mygtuką ![Dešinioji rodyklė](media/03-setup-for-requests.png), kad ją perkeltumėte į skyrių **Pasirinktos ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e46d4-135">Norėdami į ciklo modelį įtraukti visas galimas ciklo būsenas, spustelėkite mygtuką **Pasirinkti visas galimas būsenas** ![Pasirinkti visas galimas būsenas](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="e46d4-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="e46d4-136">Visos ciklo būsenos bus perkeltos į skyrių **Pasirinktos ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e46d4-137">Norėdami ciklo būseną pašalinti iš ciklo modelio, ją pasirinkite skyriuje **Pasirinktos ciklo būsenos** ir spustelėkite kairiosios rodyklės mygtuką ![Kairioji rodyklė](media/05-setup-for-requests.png), kad ją perkeltumėte į skyrių **Likusios ciklo būsenos**.</span><span class="sxs-lookup"><span data-stu-id="e46d4-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="e46d4-138">„FastTab“ skirtuko **Bendra** skyriuje **Atnaujinimai** esantys laukai yra svarbūs, jei naudojate sandėlio remontą.</span><span class="sxs-lookup"><span data-stu-id="e46d4-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="e46d4-139">Lauke **Gauto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis gaunamas sandėlio remontui.</span><span class="sxs-lookup"><span data-stu-id="e46d4-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="e46d4-140">Lauke **Išsiųsto turto ciklo būsena** pasirinkite turto ciklo būseną, į kurią priežiūros užklausoje pasirinktas turtas turėtų būti atnaujintas automatiškai, kai jis bus sugrąžintas po remonto darbų.</span><span class="sxs-lookup"><span data-stu-id="e46d4-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="e46d4-141">Paveikslėlyje pateiktas puslapio **Priežiūros užklausos ciklo būsenos** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e46d4-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Priežiūros užklausos ciklo modelių puslapis](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]