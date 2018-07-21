---
title: "„Project Service Automation“"
description: "Šiame sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ (CDS) sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Project Service Automation“ egzemplioriuose."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="4f193-103">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="4f193-103">Project Service Automation</span></span>

<span data-ttu-id="4f193-104">Integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ (CDS) sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Project Service Automation“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="4f193-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="4f193-105">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas projektų, projekto sutarčių, projekto sutarčių eilučių, projekto sutarties eilutės etapų, projekto užduočių, išlaidų operacijų kategorijų, apytikslių grafiko reikšmių ir apytikslių išlaidų reikšmių srautas iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4f193-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="4f193-106">Jei naudojate „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą 7.3.0, turite įdiegti KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="4f193-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="4f193-107">Taip galėsite integruoti fiksuotos kainos projektus.</span><span class="sxs-lookup"><span data-stu-id="4f193-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="4f193-108">Jei naudojate „Dynamics 365 for Finance and Operation“ versiją 8.0, galėsite naudotis projekto užduočių integravimu, išlaidų operacijos kategorijomis, apytikslėmis grafiko reikšmėmis, apytikslėmis išlaidų reikšmėmis ir funkcijų užrakinimu.</span><span class="sxs-lookup"><span data-stu-id="4f193-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="4f193-109">Jei naudojate „Dynamics 365 for Finance and Operations“ versiją 8.0.1, galėsite sinchronizuoti faktines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4f193-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="4f193-110">Jei naudojate „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą 7.3.0, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą.</span><span class="sxs-lookup"><span data-stu-id="4f193-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="4f193-111">Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="4f193-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="4f193-112">Tam, kad būtų galima integruoti „Project Service Automation“ su „Finance and Operations“, būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="4f193-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="4f193-113">Norėdami gauti daugiau informacijos, žr. „Project Service Automation“ integravimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="4f193-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="4f193-114">Naudojantis šiuo integravimo sprendimu galima tiesiogiai sinchronizuoti toliau nurodytais atvejais.</span><span class="sxs-lookup"><span data-stu-id="4f193-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="4f193-115">Išsaugoti „Project Service Automation“ projekto sutartis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutartis su „Finance and Operations“ projekto sutartimis.</span><span class="sxs-lookup"><span data-stu-id="4f193-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-116">Sukurti „Project Service Automation“ projektus ir tiesiogiai sinchronizuoti „Project Service Automation“ projektus su „Finance and Operations“ projektais.</span><span class="sxs-lookup"><span data-stu-id="4f193-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-117">Išsaugoti „Project Service Automation“ projekto sutarties eilutes ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarties eilutes su „Finance and Operations“ projekto sutarties eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="4f193-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-118">Išsaugoti „Project Service Automation“ projekto sutarties eilutės etapus ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarties eilutės etapus su „Finance and Operations“ projekto sutarties eilutės etapais.</span><span class="sxs-lookup"><span data-stu-id="4f193-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-119">Išsaugoti „Project Service Automation“ projekto užduotis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto užduotis su „Finance and Operations“ projekto užduotimis.</span><span class="sxs-lookup"><span data-stu-id="4f193-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-120">Išsaugoti „Finance and Operations“ išlaidų operacijos kategorijas ir tiesiogiai sinchronizuoti „Project Service Automation“ išlaidų operacijos kategorijas su „Finance and Operations“ išlaidų operacijos kategorijomis.</span><span class="sxs-lookup"><span data-stu-id="4f193-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="4f193-121">Sukurti „Project Service Automation“ apytiksles projekto grafiko reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto grafiko reikšmes su „Finance and Operations“ apytikslėmis projekto grafiko reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="4f193-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="4f193-122">Sukurti „Project Service Automation“ apytiksles projekto išlaidų reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto išlaidų reikšmes su „Finance and Operations“ apytikslėmis projekto išlaidų reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="4f193-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="4f193-123">Duomenų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="4f193-123">Data synchronization</span></span>
<span data-ttu-id="4f193-124">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys atliekant „Project Service Automation“ ir „Finance and Operations“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="4f193-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4f193-125">Šiuo metu galima naudotis ne visais šablonais.</span><span class="sxs-lookup"><span data-stu-id="4f193-125">Not all templates are currently available.</span></span> <span data-ttu-id="4f193-126">Šablonai bus išleisti juos baigus.</span><span class="sxs-lookup"><span data-stu-id="4f193-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="4f193-127">[![„Project Service Automation“ integravimas su „Finance and Operations“](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="4f193-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="4f193-128">„Finance and Operations“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="4f193-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="4f193-129">Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu, turite įdiegti „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą 7.3 su 12 ar naujesniu platformos naujinimu.</span><span class="sxs-lookup"><span data-stu-id="4f193-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="4f193-130">„Project Service Automation“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="4f193-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="4f193-131">Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu, turite įdiegti toliau nurodytus komponentus.</span><span class="sxs-lookup"><span data-stu-id="4f193-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="4f193-132">„Microsoft Dynamics 365 for Project Service Automation“ 9.0.0.0 arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="4f193-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="4f193-133">Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.14.0.0 (v14) arba naujesnė.</span><span class="sxs-lookup"><span data-stu-id="4f193-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="4f193-134">„Project Service Automation to Operations“ sprendimas, skirtas „Dynamics 365 for Project Service Automation“ 1.0.0.0 arba naujesniai versijai.</span><span class="sxs-lookup"><span data-stu-id="4f193-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="4f193-135">„Project Service Automation“ integravimo į „Finance and Operations“ sprendimo diegimas „Project Service Automation“ egzemplioriuje</span><span class="sxs-lookup"><span data-stu-id="4f193-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



