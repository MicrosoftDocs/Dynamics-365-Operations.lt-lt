---
title: Nurodymai, kaip nustatyti dvigubą rašymą
description: Šioje temoje aprašomi scenarijai, palaikomi dvigubo rašymo nustatymui.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dee6bc52a0967dfd6134258d3a02dc18feb404a5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560230"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="ce02d-103">Nurodymai, kaip nustatyti dvigubą rašymą</span><span class="sxs-lookup"><span data-stu-id="ce02d-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ce02d-104">Galite nustatyti dvigubo rašymo ryšį tarp „Finance and Operations“ aplinkos ir „Dataverse“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="ce02d-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="ce02d-105">**„Finance and Operations“ aplinka** suteikia pamatinę platformą **„Finance and Operations“ programoms** (pvz., „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Commerce“ ir „Dynamics 365 Human Resources“).</span><span class="sxs-lookup"><span data-stu-id="ce02d-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="ce02d-106">**„Dataverse ”aplinka** suteikia pamatinę platformą **„customer engagement” programoms** („Dynamics 365 Sales“, „Dynamics 365 Customer Service“, „Dynamics 365 column Service“, „Dynamics 365 Marketing“ ir „Dynamics 365 Project Service Automation“).</span><span class="sxs-lookup"><span data-stu-id="ce02d-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce02d-107">Dvigubo rašymo ryšiai palaikomi „Dynamics 365 Finance” modulyje Personalas, tačiau ne „Dynamics 365 Human Resources” programoje.</span><span class="sxs-lookup"><span data-stu-id="ce02d-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="ce02d-108">Nustatymo mechanizmas skiriasi, atsižvelgiant į jūsų prenumeratą ir aplinką.</span><span class="sxs-lookup"><span data-stu-id="ce02d-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="ce02d-109">Naudojant naujus „Finance and Operations“ programų egzempliorius, dvigubo rašymo ryšio nustatymas pradedamas „Microsoft Dynamics“ aplinkoje „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="ce02d-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ce02d-110">Jei turite licenciją, skirtą „Microsoft Power Platform“, gausite naują „Dataverse“ aplinką, jei jūsų nuomotojas neturi aplinkos.</span><span class="sxs-lookup"><span data-stu-id="ce02d-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="ce02d-111">Esamose egzempliorių „Finance and Operations“ programose dvigubo rašymo ryšio nustatymas pradedamas „Finance and Operations“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ce02d-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="ce02d-112">Prieš pradėdami naudoti dvigubo rašymo funkciją objekte, galite paleisti pradinį sinchronizavimą, norėdami tvarkyti esamus duomenis abiejose „Finance and Operations” ir klientų įtraukimo programų pusėse.</span><span class="sxs-lookup"><span data-stu-id="ce02d-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="ce02d-113">Galite praleisti pradinį sinchronizavimą, jei jums nereikia sinchronizuoti dviejų aplinkų duomenų.</span><span class="sxs-lookup"><span data-stu-id="ce02d-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="ce02d-114">Pradinis sinchronizavimas leidžia dvikryptį esamų duomenų kopijavimą iš vienos programos į kitą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="ce02d-115">Galimi keli nustatymo scenarijai, atsižvelgiant į tai, kokias aplinkas jau turite ir kokio tipo duomenys yra jose.</span><span class="sxs-lookup"><span data-stu-id="ce02d-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="ce02d-116">Palaikomi toliau nurodyti nustatymo scenarijai:</span><span class="sxs-lookup"><span data-stu-id="ce02d-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="ce02d-117">Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="ce02d-118">Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="ce02d-119">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="ce02d-120">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="ce02d-121">Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="ce02d-122">Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="ce02d-123">Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="ce02d-124">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ce02d-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ce02d-125">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="ce02d-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="ce02d-126">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="ce02d-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ce02d-127">Parengta naujas tuščias klientų įtraukimo programos egzempliorius, kuriame įdiegtas „CRM“ pagrindinis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="ce02d-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="ce02d-128">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="ce02d-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ce02d-129">Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="ce02d-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ce02d-130">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="ce02d-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="ce02d-131">Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="ce02d-132">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje nėra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus [Dvigubo rašymo nustatymas „Lifecycle Services“](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ce02d-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="ce02d-133">Kai ryšio nustatymas baigiamas, automatiškai atsiranda šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="ce02d-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="ce02d-134">Parengta nauja tuščia „Finance and Operations“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="ce02d-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="ce02d-135">DAT įmonės duomenims sukurtas dvigubo rašymo ryšys.</span><span class="sxs-lookup"><span data-stu-id="ce02d-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="ce02d-136">Lentelių žemėlapiai įgalinami tiesioginiam sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="ce02d-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="ce02d-137">Abi aplinkos yra parengtos tiesiogiai sinchronizuoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="ce02d-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="ce02d-138">Norėdami sinchronizuoti esamus „Dataverse“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce02d-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ce02d-139">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ce02d-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ce02d-140">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ce02d-141">[Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių Tarptautinės standartizacijos organizacijos (ISO) įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="ce02d-142">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-143">Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example) toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="ce02d-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="ce02d-144">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="ce02d-145">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius](#new-new).</span><span class="sxs-lookup"><span data-stu-id="ce02d-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="ce02d-146">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce02d-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="ce02d-147">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="ce02d-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ce02d-148">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-149">Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).</span><span class="sxs-lookup"><span data-stu-id="ce02d-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="ce02d-150">Naujas „Finance and Operations“ programos egzempliorius, kuriame yra duomenų, ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="ce02d-151">Norėdami nustatyti dvigubo rašymo ryšį tarp naujo „Finance and Operations“ programos, kurioje yra duomenų, egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus, atlikite veiksmus, nurodytus ankščiau šioje temoje pateiktame skyriuje [Naujas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius](#new-existing).</span><span class="sxs-lookup"><span data-stu-id="ce02d-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="ce02d-152">Kai ryšio nustatymas baigiamas, jei norite sinchronizuoti duomenis su klientų įtraukimo programa, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce02d-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="ce02d-153">Atidarykite „Finance and Operations“ programą LCS puslapyje, prisijunkite, o tada pereikite prie **Duomenų tvarkymas \> Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="ce02d-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="ce02d-154">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-155">Norėdami sinchronizuoti esamus „Dataverse“ duomenis su „Finance and Operations“ programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce02d-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="ce02d-156">Sukurkite naują įmonę programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ce02d-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="ce02d-157">Įtraukite įmonę į dvigubo rašymo ryšio nustatymą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="ce02d-158">[Perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="ce02d-159">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-160">Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).</span><span class="sxs-lookup"><span data-stu-id="ce02d-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="ce02d-161">Esamas „Finance and Operations“ programos egzempliorius ir naujas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="ce02d-162">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir naujo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ce02d-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="ce02d-163">[Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="ce02d-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="ce02d-164">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-165">Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).</span><span class="sxs-lookup"><span data-stu-id="ce02d-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="ce02d-166">Esamas „Finance and Operations“ programos egzempliorius ir esamas klientų įtraukimo programos egzempliorius</span><span class="sxs-lookup"><span data-stu-id="ce02d-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="ce02d-167">Dvigubo rašymo ryšio nustatymas tarp esamo „Finance and Operations“ programos egzemplioriaus ir esamo klientų įtraukimo programos egzemplioriaus vykdomas „Finance and Operation“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ce02d-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="ce02d-168">[Nustatykite ryšį „Finance and Operations“ programoje](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="ce02d-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="ce02d-169">Norėdami sinchronizuoti esamus „Dataverse“ duomenis į „Finance and Operations“ programą, [perkraukite](bootstrap-company-data.md) „Dataverse“ duomenis naudodami trijų raidžių ISO įmonės kodą.</span><span class="sxs-lookup"><span data-stu-id="ce02d-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="ce02d-170">Paleiskite funkciją **Pradinis sinchronizavimas** lentelėms, kurių duomenis norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="ce02d-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="ce02d-171">Norėdami gauti saitą su pavyzdžiu ir alternatyviu metodu, žr. skyrių [Pavyzydys](#example).</span><span class="sxs-lookup"><span data-stu-id="ce02d-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="ce02d-172">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ce02d-172">Example</span></span>

<span data-ttu-id="ce02d-173">Pavyzdį rasite [Lentelių Klientai V3 ir Kontaktai schemos įgalinimas](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="ce02d-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="ce02d-174">Jei norite naudoti alternatyvų būdą, pagrįstą kiekvieno objekto, kuris turi vykdyti pradinį sinchronizavimą, duomenimis, žr. [Pradinės sinchronizacijos aplinkybės](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="ce02d-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]