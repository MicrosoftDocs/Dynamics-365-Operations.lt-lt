---
title: Palaikomi dvigubo rašymo nustatymo scenarijai
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706257"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="cdc83-103">Palaikomi dvigubo rašymo nustatymo scenarijai</span><span class="sxs-lookup"><span data-stu-id="cdc83-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="cdc83-104">Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Common Data Service“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="cdc83-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="cdc83-105">**„Finance and Operations” aplinka** suteikia esamą platformą **„Finance and Operations” programoms** (pavyzdžiui, „Microsoft Dynamics 365 Finance”, „Dynamics 365 Supply Chain Management” ir „Dynamics 365 Retail”).</span><span class="sxs-lookup"><span data-stu-id="cdc83-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="cdc83-106">**„Common Data Service“ aplinka** suteikia pamatinę platformą **modeliu grįstoms „Dynamics 365“ programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 Field Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).</span><span class="sxs-lookup"><span data-stu-id="cdc83-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="cdc83-107">Dvigubo rašymo ryšiai palaikomi „Finance and Operations” žmogiškuosiuose ištekliuose, tačiau ne „Dynamics 365 Human Resources” programoje.</span><span class="sxs-lookup"><span data-stu-id="cdc83-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="cdc83-108">Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.</span><span class="sxs-lookup"><span data-stu-id="cdc83-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="cdc83-109">Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="cdc83-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cdc83-110">Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Common Data Service“ aplinką, jei jūsų nuomotojas neturi aplinkos.</span><span class="sxs-lookup"><span data-stu-id="cdc83-110">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="cdc83-111">Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="cdc83-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="cdc83-112">Palaikomi toliau nurodyti nustatymo scenarijai:</span><span class="sxs-lookup"><span data-stu-id="cdc83-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="cdc83-113">Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="cdc83-114">Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="cdc83-115">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="cdc83-116">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="cdc83-117">Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="cdc83-118">Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="cdc83-119">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir naujo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cdc83-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="cdc83-120">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="cdc83-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="cdc83-121">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="cdc83-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="cdc83-122">Parengta naujas tuščias modeliu grįstos programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="cdc83-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="cdc83-123">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="cdc83-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="cdc83-124">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="cdc83-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="cdc83-125">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="cdc83-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="cdc83-126">Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="cdc83-127">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir esamo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="cdc83-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="cdc83-128">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="cdc83-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="cdc83-129">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="cdc83-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="cdc83-130">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="cdc83-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="cdc83-131">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="cdc83-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="cdc83-132">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="cdc83-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="cdc83-133">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cdc83-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="cdc83-134">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="cdc83-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="cdc83-135">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="cdc83-136">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="cdc83-137">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="cdc83-138">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="cdc83-139">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir naujo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstos programos egzempliorius](#new-new).</span><span class="sxs-lookup"><span data-stu-id="cdc83-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="cdc83-140">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cdc83-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="cdc83-141">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="cdc83-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="cdc83-142">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="cdc83-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="cdc83-143">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="cdc83-144">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas modeliu grįstos programos egzempliorius](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="cdc83-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="cdc83-145">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cdc83-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="cdc83-146">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="cdc83-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="cdc83-147">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="cdc83-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="cdc83-148">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cdc83-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="cdc83-149">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="cdc83-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="cdc83-150">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="cdc83-151">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="cdc83-152">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="cdc83-153">Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="cdc83-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="cdc83-154">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo arba esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus vyksta „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="cdc83-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="cdc83-155">Nustatykite ryšį „Finance and Operations“ programoje.</span><span class="sxs-lookup"><span data-stu-id="cdc83-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="cdc83-156">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="cdc83-157">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="cdc83-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
