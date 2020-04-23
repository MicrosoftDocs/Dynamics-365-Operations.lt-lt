---
title: Priežiūros darbuotojai ir darbuotojų grupės
description: Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6cf7e8e796032b348cff5a77c10b376dbbeef974
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214785"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="9f833-103">Priežiūros darbuotojai ir darbuotojų grupės</span><span class="sxs-lookup"><span data-stu-id="9f833-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9f833-104">Šioje temoje aprašomi priežiūros darbuotojai ir darbuotojų grupės modulyje „Turto valdymas“.</span><span class="sxs-lookup"><span data-stu-id="9f833-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="9f833-105">Modulyje „Turto valdymas“ galite priskirti priežiūros darbuotojus prie funkcinių vietovių.</span><span class="sxs-lookup"><span data-stu-id="9f833-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="9f833-106">(Norėdami gauti daugiau informacijos apie funkcines vietas, žr. [Funkcinių vietų kūrimas](../functional-locations/create-functional-locations.md).) Ši funkcija gali būti naudinga, jei, pavyzdžiui, planuojate mašinos, kurios funkcinė vietovė yra 01, priežiūros užduotį ir norite priskirti priežiūros darbuotojus iš tos pačios vietovės užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="9f833-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="9f833-107">Taip pat galite kurti priežiūros darbuotojų grupes ir su jais susieti priežiūros darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="9f833-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="9f833-108">Ši funkcija naudinga, kai atliekate paprastą darbo užsakymo planavimą ir norite darbo užsakyme suplanuoti priežiūros darbuotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="9f833-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="9f833-109">Galite naudoti priežiūros darbuotojus ir priežiūrą atliekančių darbuotojų grupes, kad nustatytumėte pageidautinus priežiūros darbuotojus ir už priežiūrą atsakingus darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="9f833-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="9f833-110">Kurti darbininkus</span><span class="sxs-lookup"><span data-stu-id="9f833-110">Create workers</span></span>

1. <span data-ttu-id="9f833-111">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="9f833-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="9f833-112">Spustelėkite **Naujas**, norėdami į sąrašą įtraukti naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="9f833-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="9f833-113">Lauke **Darbuotojas** pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="9f833-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="9f833-114">Nustatykite parinktį **Aktyvus** į **Taip**, kad darbo užsakymams suplanuotumėte darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="9f833-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="9f833-115">„FastTab“ skirtuke **Bendra** laukai **Išteklius** ir **Aprašas** automatiškai užpildomi, jei darbuotojui buvo parinktas išteklius.</span><span class="sxs-lookup"><span data-stu-id="9f833-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="9f833-116">Laukas **Kalendorius** taip pat užpildomas automatiškai, jei darbuotoją nustatėte kaip išteklių ir tam ištekliui puslapyje **Ištekliai** priskyrėte kalendorių (**Organizacijos administravimas**\>**Ištekliai**\>**Ištekliai**).</span><span class="sxs-lookup"><span data-stu-id="9f833-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="9f833-117">„FastTab“ skirtuke **Grupės** pasirinkite **Pridėti**, tada darbuotojui parinkite priežiūros darbuotojų grupę.</span><span class="sxs-lookup"><span data-stu-id="9f833-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="9f833-118">Pardavimo grupėje gali būti daugiau nei vienas darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="9f833-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="9f833-119">Naudojant standartinę konfigūraciją, darbuotojo narystė grupėje įsigalios ir niekada nebaigs galioti nuo tos dienos, kai pridėsite grupę.</span><span class="sxs-lookup"><span data-stu-id="9f833-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="9f833-120">Ši data rodoma lauke **Galioja**.</span><span class="sxs-lookup"><span data-stu-id="9f833-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="9f833-121">Norėdami matyti lauką **Galioja** pasirinkite **Peržiūrėti** \> **Visi**.</span><span class="sxs-lookup"><span data-stu-id="9f833-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="9f833-122">Jei darbuotojo narystė grupėje turėtų būti apribota tam tikram laikotarpiui, norėdami nustatyti periodą, naudokite laukus **Galiojantis** ir **Galiojimo pabaiga**.</span><span class="sxs-lookup"><span data-stu-id="9f833-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="9f833-123">„FastTab“ skirtuke **Funkcinės vietovės** pasirinkite **Pridėti**ir pasirinkite priežiūros darbuotojo funkcinę grupę.</span><span class="sxs-lookup"><span data-stu-id="9f833-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="9f833-124">Taip pat nurodykite, kuri vietovė yra pirminė darbuotojo funkcinė vietovė.</span><span class="sxs-lookup"><span data-stu-id="9f833-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f833-125">Kai darbuotojui pridedate funkcinę vietovę, visas aktyvus turtas, kuris yra susijęs su tomis funkcinėmis vietovėmis, rodomas įvairiuose meniu elementuose, tokiuose kaip **Mano aktyvus turtas** ir **Mano aktyvios funkcinės vietovės**.</span><span class="sxs-lookup"><span data-stu-id="9f833-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="9f833-126">Jie taip pat rodomi turto peržvalgose, atsirandančiose kuriant naują turtą, priežiūros užklausą arba darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9f833-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="9f833-127">„FastTab“ skirtuko **Informacija** laukuose rodomas priežiūros darbuotojų grupių ir funkcinių vietovių, su kuriomis susijęs pasirinktas priežiūros darbuotojas, skaičius.</span><span class="sxs-lookup"><span data-stu-id="9f833-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="9f833-128">Darbuotojų grupių kūrimas</span><span class="sxs-lookup"><span data-stu-id="9f833-128">Create worker groups</span></span>

1. <span data-ttu-id="9f833-129">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbuotojai** \> **Priežiūros darbuotojų grupės**.</span><span class="sxs-lookup"><span data-stu-id="9f833-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="9f833-130">Spustelėkit **Naujas**, norėdami į sąrašą įtraukti naują darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="9f833-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="9f833-131">Lauke **Priežiūros darbuotojų grupė** įveskite grupės ID.</span><span class="sxs-lookup"><span data-stu-id="9f833-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="9f833-132">Tada lauke **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9f833-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="9f833-133">„FastTab“ skirtuke **Darbuotojai** pasirinkite **Pridėti**ir darbuotojų grupei pasirinkite priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="9f833-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="9f833-134">Norėdami sužinoti apie laukus **Galiojantis** ir **Galiojimo pabaiga**, žiūrėkite ankstesnės procedūros 6 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="9f833-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="9f833-135">Jei išteklių grupė turėtų būti susieta su pasirinkta priežiūros darbuotojų grupe, pasirinkite **Kopijuoti iš išteklių grupės**.</span><span class="sxs-lookup"><span data-stu-id="9f833-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="9f833-136">Lauke **Grupė** pasirinkite išteklių grupę, iš kurios kopijuosite kalendoriaus parametrus.</span><span class="sxs-lookup"><span data-stu-id="9f833-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="9f833-137">Po to, lauke **Darbuotojų grupė** pasirinkite darbuotojų grupę, kad į ją nukopijuotumėte išteklių grupės kalendoriaus parametrus.</span><span class="sxs-lookup"><span data-stu-id="9f833-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="9f833-138">Šis veiksmas svarbus tik tada, kai norite, kad planuojant darbo užsakymą, priežiūros darbuotojai galėtų naudoti su ištekliumi (darbo centru) susijusį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="9f833-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="9f833-139">„FastTab“ skirtuko **Informacija** lauke nurodomas priežiūros darbuotojų, kurie buvo pridėti į pasirinktą darbuotojų grupę, skaičius.</span><span class="sxs-lookup"><span data-stu-id="9f833-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
