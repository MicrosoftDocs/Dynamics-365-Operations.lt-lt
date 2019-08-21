---
title: Produktų ciklo būsenos
description: Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783451"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="cfc2b-103">Produktų ciklo būsenos</span><span class="sxs-lookup"><span data-stu-id="cfc2b-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="cfc2b-104">Šioje temoje paaiškinamos turto ciklo būsenos ir ciklo modeliai modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="cfc2b-105">Turto ciklo būsenos naudojamos apibrėžti, ar turtas aktyvus, ar neaktyvus.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="cfc2b-106">Pavyzdžiui, galite sukonfigūruoti tokias turto ciklo būsenas kaip **Sukurta**, **Aktyvi** ir **Nutraukta**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="cfc2b-107">Užklausų ciklo būsenos yra susietos su turto ciklo būsenomis.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="cfc2b-108">Todėl pakeitus užklausos būseną į naują užklausos ciklo būseną, turto, susieto su šia užklausa, būsena keičiama į naują turto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="cfc2b-109">Pavyzdžiui, jei užklausos ciklo būsena keičiama į **Gaunama**, susieto turto ciklo būsena keičiama į ciklo būseną, kuri yra pasirinkta lauke **Gaunamo turto ciklo būsena**, kuris yra puslapio **Turto ciklo būsenos modeliai** „FastTab“ skirtuke **Turto ciklo būsena**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="cfc2b-110">Turto ciklo būsenos gali būti nustatomos turto ciklo modeliuose, kuriuose galite apibrėžti reikiamas įvairių turto tipų ciklo būsenas.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="cfc2b-111">Pirmiausia nustatote ciklo būsenas.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-111">You first set up lifecycle states.</span></span> <span data-ttu-id="cfc2b-112">Tada sukuriate ciklo modelį ir pasirenkate jo ciklo būsenas.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="cfc2b-113">Pasirinkite **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="cfc2b-114">Pasirinkite **New**, kad sukurtumėte naują gyvavimo stadiją.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="cfc2b-115">Lauke **Ciklo būsena** įveskite ciklo būsenos stadijos ID.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="cfc2b-116">Lauke **Name** įveskite aprašomąjį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="cfc2b-117">Lauke **Ciklo modeliai** rodomas turto ciklo modelių, kurie naudoja turto ciklo būseną, skaičius.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="cfc2b-118">Nustatykite parinktį **Aktyvus** kaip **Taip**, jei ši ciklo būsena turėtų būti aktyvios ciklo būsenos (kitaip tariant, jei darbo užsakymai gali būti kuriami su turtu, esančiu šios ciklo būsenos).</span><span class="sxs-lookup"><span data-stu-id="cfc2b-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="cfc2b-119">Nustatykite parinktį **Naikinti atviras kalendoriaus eilutes** kaip **Taip**, jei atviros turto kalendoriaus eilutės, turinčios turto ciklo būsena **Sukurta**, turėtų būti naikinamos, kai yra šios ciklo būsenos.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="cfc2b-120">Šis parametras yra naudingas, jei norite išvalyti bet kokius atvirus priežiūros grafikus, kurie nebeatitinka turto (pvz., jei turtas nebeaktyvus).</span><span class="sxs-lookup"><span data-stu-id="cfc2b-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="cfc2b-121">Turto ciklo būsenos, turto ciklo modeliai ir turto tipai yra susieti.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="cfc2b-122">Jie yra naudojami taip pat, kaip ir darbo užsakymo ciklo būsenos, darbo užsakymo ciklo modeliai ir darbo užsakymų tipai.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="cfc2b-123">Sukūrę reikiamas turto ciklo būsenas, galite nustatyti ciklo būsenas turto ciklo modeliuose.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="cfc2b-124">Pasirinkite **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="cfc2b-125">Pasirinkite **New**, kad sukurtumėte naują turto ciklo modelį.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="cfc2b-126">Lauke **Ciklo būsena** įveskite ciklo modelio ID.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="cfc2b-127">Lauke **Name** įveskite aprašomąjį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="cfc2b-128">Lauke **Ciklo būsenos** rodomas turto ciklo būsenų, kurios yra pasirinktos turto ciklo modelyje, skaičius.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="cfc2b-129">Lauke **Turto tipai** rodomas ciklo modelį naudojančių turto tipų skaičius.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="cfc2b-130">„FastTab“ skirtuke **Ciklo būsenos** pasirinkite turto ciklo būsenas, kurias reikėtų įtraukti į turto ciklo modelį:</span><span class="sxs-lookup"><span data-stu-id="cfc2b-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="cfc2b-131">Norėdami naudoti modelio ciklo būseną, pasirinkite ją skyriuje **Lifecycle states remaining**, tada pasirinkite dešiniosios rodyklės mygtuką ![Dešinioji rodyklė](media/15-setup-for-objects.png), kad perkeltumėte ją į skyrių **Lifecycle states selected**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cfc2b-132">Norėdami naudoti visas pasiekiamas ciklo būsenas modelyje, pasirinkite mygtuką **All available lifecycle states**![Visos pasiekiamos ciklo būsenos](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="cfc2b-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="cfc2b-133">Visos būsenos perkeliamos į skyrių **Lifecycle states selected**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="cfc2b-134">Norėdami pašalinti ciklo būseną iš modelio, pasirinkite ją skyriuje **lifecycle states selected**, tada pasirinkite kairiosios rodyklės mygtuką ![Kairioji rodyklė](media/16-setup-for-objects.png), kad perkeltumėte ją į skyrių **Lifecycle states remaining**.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="cfc2b-135">Pasirinkite **Lifecycle state updates**, kad apibrėžtume turto ciklo būsenas, kurios gali eiti po pasirinktos ciklo būsenos.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="cfc2b-136">Galite naudoti „FastTab“ skirtuką **Asset state**, jei tvarkote turtą, kurį gaunate taisyti.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="cfc2b-137">Skyriuje **Gaunama / siunčiama** galite pasirinkti turto ciklo būsenas, kad nurodytumėte darbo eigą, susijusią su turtu, kurį gavote taisyti.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="cfc2b-138">Jei siūlote paskolos turtą klientams arba padaliniams, skyriuje **Paskola** galite pasirinkti paskolos turto ciklo būsenas.</span><span class="sxs-lookup"><span data-stu-id="cfc2b-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
