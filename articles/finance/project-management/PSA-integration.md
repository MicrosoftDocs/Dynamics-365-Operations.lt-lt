---
title: „Project Service Automation“ apžvalga
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Service Automation“ ir „Dynamics 365 Finance“ integravimo sprendimą.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250558"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="90bff-103">„Project Service Automation“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="90bff-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="90bff-104">Integravimo iš „Project Service Automation“ į „Finance“ sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ sinchronizuojami duomenys „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="90bff-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="90bff-105">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas projektų, projekto sutarčių, projekto sutarčių eilučių, projekto sutarties eilutės etapų, projekto užduočių, išlaidų operacijų kategorijų, apytikslių grafiko reikšmių ir apytikslių išlaidų reikšmių srautas iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="90bff-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="90bff-106">Jei naudojate 7.3.0 versiją, turite įdiegti KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="90bff-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="90bff-107">Tada galėsite integruoti fiksuotos kainos projektus.</span><span class="sxs-lookup"><span data-stu-id="90bff-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="90bff-108">Jei naudojate 7.3.0 versiją ir atliekate mokesčio operacijas naudodami „Project Service Automation“, turite įdiegti KB 4345320, kad šie mokesčiai būtų įtraukti į projekto SF.</span><span class="sxs-lookup"><span data-stu-id="90bff-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="90bff-109">Jei naudojate 8.0 versiją, galėsite naudotis projekto užduoties integravimu, išlaidų operacijos kategorijomis, apytikslėmis grafiko reikšmėmis, apytikslėmis išlaidų reikšmėmis ir funkcijų užrakinimu.</span><span class="sxs-lookup"><span data-stu-id="90bff-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="90bff-110">Jei naudojate 8.0.1 arba naujesnę versiją, galėsite sinchronizuoti faktines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="90bff-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="90bff-111">Tam, kad būtų galima integruoti „Project Service Automation“ su „Finance“, būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="90bff-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="90bff-112">Norėdami gauti daugiau informacijos, žr. [„Project Service Automation“ integravimo parametrus](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="90bff-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="90bff-113">Naudojantis šiuo integravimo sprendimu galima tiesiogiai sinchronizuoti toliau nurodytais atvejais.</span><span class="sxs-lookup"><span data-stu-id="90bff-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="90bff-114">Išsaugoti „Project Service Automation“ projekto sutartis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutartis su „Finance“ projekto sutartimis.</span><span class="sxs-lookup"><span data-stu-id="90bff-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-115">Sukurti „Project Service Automation“ projektus ir tiesiogiai sinchronizuoti „Project Service Automation“ projektus su „Finance“ projektais.</span><span class="sxs-lookup"><span data-stu-id="90bff-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-116">Išsaugoti „Project Service Automation“ projekto sutarčių eilutes ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarčių eilutes su „Finance“ projekto sutarčių eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="90bff-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-117">Išsaugoti „Project Service Automation“ projekto sutarčių eilučių etapus ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarčių eilučių etapus su „Finance“ projekto sutarčių eilučių etapais.</span><span class="sxs-lookup"><span data-stu-id="90bff-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-118">Išsaugoti „Project Service Automation“ projekto užduotis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto užduotis su „Finance“ projekto užduotimis.</span><span class="sxs-lookup"><span data-stu-id="90bff-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-119">Išsaugoti „Finance“ išlaidų operacijos kategorijas ir tiesiogiai sinchronizuoti „Finance“ išlaidų operacijos kategorijas su „Project Service Automation“ išlaidų operacijos kategorijomis.</span><span class="sxs-lookup"><span data-stu-id="90bff-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="90bff-120">Sukurti „Project Service Automation“ apytiksles projekto grafiko reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto grafiko reikšmes su „Finance“ apytikslėmis projekto grafiko reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="90bff-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-121">Sukurti „Project Service Automation“ apytiksles projekto išlaidų reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto išlaidų reikšmes su „Finance“ apytikslėmis projekto išlaidų reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="90bff-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="90bff-122">Kurti projekto grafiko, išlaidų ir mokesčių faktines reikšmes naudodamiesi „Project Service Automation“, o projekto operacijas kurti „Project Service Automation“ integravimo žurnale, kad jos būtų paskelbtos „Finance“.</span><span class="sxs-lookup"><span data-stu-id="90bff-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="90bff-123">Duomenų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="90bff-123">Data synchronization</span></span>

<span data-ttu-id="90bff-124">Toliau esančiame paveikslėlyje rodoma, kaip sinchronizuojami duomenys atliekant „Project Service Automation“ ir „Finance“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="90bff-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="90bff-125">Šiuo metu galima naudotis ne visais šablonais.</span><span class="sxs-lookup"><span data-stu-id="90bff-125">Not all templates are currently available.</span></span> <span data-ttu-id="90bff-126">Šablonai bus išleisti juos baigus.</span><span class="sxs-lookup"><span data-stu-id="90bff-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="90bff-127">[![„Project Service Automation“ ir „Finance“ integravimas](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="90bff-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="90bff-128">„Finance“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="90bff-128">System requirements for Finance</span></span>

<span data-ttu-id="90bff-129">Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance“ sprendimu, turite įdiegti „Enterprise Edition 7.3“ su 12 ar naujesniu „Platform“ naujinimu.</span><span class="sxs-lookup"><span data-stu-id="90bff-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="90bff-130">„Project Service Automation“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="90bff-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="90bff-131">Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance“ sprendimu, turite įdiegti toliau nurodytus komponentus.</span><span class="sxs-lookup"><span data-stu-id="90bff-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="90bff-132">„Dynamics 365 Project Service Automation“ 9.0.0.0 arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="90bff-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="90bff-133">Sprendimui „Dynamics 365 Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai 1.14.0.0 (v14) arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="90bff-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="90bff-134">„Project Service Automation“ į „Finance“ sprendimas, skirtas „Dynamics 365 Project Service Automation“ 1.0.0.0 arba naujesnei versijai</span><span class="sxs-lookup"><span data-stu-id="90bff-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="90bff-135">„Project Service Automation“ integravimo į „Finance“ sprendimo diegimas „Project Service Automation“ egzemplioriuje</span><span class="sxs-lookup"><span data-stu-id="90bff-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="90bff-136">Atsisiųskite „Project Service Automation“ integravimo į „Finance“ sprendimą iš [„Microsoft“ atsisiuntimo centro](https://www.microsoft.com/download/details.aspx?id=57016) ir sekite prie sprendimo pridėtas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="90bff-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
