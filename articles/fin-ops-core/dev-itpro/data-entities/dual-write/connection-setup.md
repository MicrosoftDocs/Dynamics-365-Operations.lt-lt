---
title: Palaikomi dvigubo rašymo nustatymo scenarijai
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112486"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="375bf-103">Palaikomi dvigubo rašymo nustatymo scenarijai</span><span class="sxs-lookup"><span data-stu-id="375bf-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="375bf-104">Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Common Data Service“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="375bf-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="375bf-105">**„Finance and Operations“ aplinka** suteikia pamatinę platformą **„Finance and Operations“ programoms** (pvz., „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Retail“ ir „Dynamics 365 Human Resources“).</span><span class="sxs-lookup"><span data-stu-id="375bf-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="375bf-106">**„Common Data Service“ aplinka** suteikia pamatinę platformą **modeliu grįstoms „Dynamics 365“ programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 Field Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).</span><span class="sxs-lookup"><span data-stu-id="375bf-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="375bf-107">Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.</span><span class="sxs-lookup"><span data-stu-id="375bf-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="375bf-108">Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="375bf-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="375bf-109">Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Common Data Service“ aplinką, jei jūsų nuomotojas neturi aplinkos.</span><span class="sxs-lookup"><span data-stu-id="375bf-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="375bf-110">Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="375bf-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="375bf-111">Palaikomi toliau nurodyti nustatymo scenarijai:</span><span class="sxs-lookup"><span data-stu-id="375bf-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="375bf-112">Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="375bf-113">Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="375bf-114">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="375bf-115">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="375bf-116">Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="375bf-117">Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="375bf-118">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir naujo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="375bf-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="375bf-119">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="375bf-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="375bf-120">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="375bf-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="375bf-121">Parengta naujas tuščias modeliu grįstos programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="375bf-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="375bf-122">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="375bf-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="375bf-123">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="375bf-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="375bf-124">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="375bf-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="375bf-125">Naujas „Finance and Operations“ programos egzempliorius ir esantis modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="375bf-126">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kuri neturi duomenų, egzemplioriaus ir esamo modeliu grįsto egzemplioriaus „Dynamics 365“ programoje, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="375bf-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="375bf-127">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="375bf-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="375bf-128">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="375bf-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="375bf-129">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="375bf-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="375bf-130">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="375bf-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="375bf-131">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="375bf-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="375bf-132">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="375bf-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="375bf-133">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="375bf-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="375bf-134">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="375bf-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="375bf-135">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="375bf-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="375bf-136">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="375bf-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="375bf-137">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="375bf-138">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir naujo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstos programos egzempliorius](#new-new).</span><span class="sxs-lookup"><span data-stu-id="375bf-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="375bf-139">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="375bf-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="375bf-140">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="375bf-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="375bf-141">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="375bf-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="375bf-142">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra demonstraciniai duomenys, ir esamas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="375bf-143">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra demonstraciniai duomenys, egzemplioriaus ir esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas modeliu grįstos programos egzempliorius](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="375bf-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="375bf-144">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti demonstracinius duomenis su modeliu pagrįsta programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="375bf-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="375bf-145">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="375bf-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="375bf-146">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="375bf-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="375bf-147">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="375bf-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="375bf-148">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="375bf-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="375bf-149">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="375bf-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="375bf-150">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="375bf-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="375bf-151">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="375bf-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="375bf-152">Esamas „Finance and Operations“ programos egzempliorius ir naujas modeliu grįstas programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="375bf-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="375bf-153">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo arba esamo modeliu grįstos „Dynamics 365“ programos egzemplioriaus vyksta „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="375bf-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="375bf-154">Nustatykite ryšį „Finance and Operations“ programoje.</span><span class="sxs-lookup"><span data-stu-id="375bf-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="375bf-155">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="375bf-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="375bf-156">Kadangi dvigubo rašymo būsena yra tiesioginio sinchronizavimo režime, duomenys iš „Common Data Service“ automatiškai paleidžiami į „Finance and Operations“ programą.</span><span class="sxs-lookup"><span data-stu-id="375bf-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
