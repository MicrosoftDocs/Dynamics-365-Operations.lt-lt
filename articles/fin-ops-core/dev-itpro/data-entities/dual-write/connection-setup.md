---
title: Nurodymai, kaip nustatyti dvigubą rašymą
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088511"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="21dfc-103">Nurodymai, kaip nustatyti dvigubą rašymą</span><span class="sxs-lookup"><span data-stu-id="21dfc-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="21dfc-104">Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Common Data Service“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="21dfc-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="21dfc-105">**„Finance and Operations” aplinka** suteikia esamą platformą **„Finance and Operations” programoms** (pavyzdžiui, „Microsoft Dynamics 365 Finance”, „Dynamics 365 Supply Chain Management” ir „Dynamics 365 Retail”).</span><span class="sxs-lookup"><span data-stu-id="21dfc-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="21dfc-106">**„Common Data Service“ aplinka** suteikia pamatinę platformą **klientų įtraukimo programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 Field Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).</span><span class="sxs-lookup"><span data-stu-id="21dfc-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="21dfc-107">Dvigubo rašymo ryšiai palaikomi „Finance and Operations” žmogiškuosiuose ištekliuose, tačiau ne „Dynamics 365 Human Resources” programoje.</span><span class="sxs-lookup"><span data-stu-id="21dfc-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="21dfc-108">Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.</span><span class="sxs-lookup"><span data-stu-id="21dfc-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="21dfc-109">Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="21dfc-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="21dfc-110">Jei turite licenciją, skirtą „Power Platform“, gausite naują „Common Data Service“ aplinką, jei jūsų nuomotojas neturi aplinkos.</span><span class="sxs-lookup"><span data-stu-id="21dfc-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="21dfc-111">Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="21dfc-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="21dfc-112">Prieš pradėdami naudoti dvigubo rašymo funkciją objekte, galite paleisti pradinį sinchronizavimą, norėdami tvarkyti esamus duomenis abiejose „Finance and Operations” ir klientų įtraukimo programų pusėse.</span><span class="sxs-lookup"><span data-stu-id="21dfc-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="21dfc-113">Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.</span><span class="sxs-lookup"><span data-stu-id="21dfc-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="21dfc-114">Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="21dfc-115">Galimi keli skirtingi nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra aplinkose.</span><span class="sxs-lookup"><span data-stu-id="21dfc-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="21dfc-116">Palaikomi toliau nurodyti nustatymo scenarijai:</span><span class="sxs-lookup"><span data-stu-id="21dfc-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="21dfc-117">Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="21dfc-118">Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="21dfc-119">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="21dfc-120">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="21dfc-121">Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="21dfc-122">Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="21dfc-123">Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="21dfc-124">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="21dfc-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="21dfc-125">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="21dfc-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="21dfc-126">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="21dfc-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="21dfc-127">Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="21dfc-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="21dfc-128">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="21dfc-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="21dfc-129">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="21dfc-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="21dfc-130">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="21dfc-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="21dfc-131">Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="21dfc-132">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="21dfc-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="21dfc-133">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="21dfc-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="21dfc-134">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="21dfc-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="21dfc-135">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="21dfc-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="21dfc-136">Objektų žemėlapiai įgalinami tiesioginiui sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="21dfc-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="21dfc-137">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="21dfc-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="21dfc-138">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21dfc-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="21dfc-139">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="21dfc-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="21dfc-140">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="21dfc-141">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="21dfc-142">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-143">Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).</span><span class="sxs-lookup"><span data-stu-id="21dfc-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="21dfc-144">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="21dfc-145">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new).</span><span class="sxs-lookup"><span data-stu-id="21dfc-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="21dfc-146">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21dfc-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="21dfc-147">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="21dfc-148">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-149">Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).</span><span class="sxs-lookup"><span data-stu-id="21dfc-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="21dfc-150">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="21dfc-151">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="21dfc-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="21dfc-152">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21dfc-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="21dfc-153">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="21dfc-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="21dfc-154">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-155">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21dfc-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="21dfc-156">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="21dfc-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="21dfc-157">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="21dfc-158">[Perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="21dfc-159">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-160">Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).</span><span class="sxs-lookup"><span data-stu-id="21dfc-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="21dfc-161">Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="21dfc-162">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="21dfc-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="21dfc-163">[Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="21dfc-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="21dfc-164">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-165">Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).</span><span class="sxs-lookup"><span data-stu-id="21dfc-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="21dfc-166">Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="21dfc-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="21dfc-167">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="21dfc-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="21dfc-168">Nustatykite ryšį „Finance and Operations“ programoje.</span><span class="sxs-lookup"><span data-stu-id="21dfc-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="21dfc-169">Norėdami sinchronizuoti esamus „Common Data Service“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Common Data Service“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="21dfc-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="21dfc-170">Paleiskite funkciją **Pradinis sinchronizavimas** objektams, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="21dfc-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="21dfc-171">Pavyzdį ir alternatyvų būdą rasite [Pavyzdys](#example).</span><span class="sxs-lookup"><span data-stu-id="21dfc-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="21dfc-172">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="21dfc-172">Example</span></span>

<span data-ttu-id="21dfc-173">Pavyzdį rasite [Objektų Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="21dfc-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="21dfc-174">Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="21dfc-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
