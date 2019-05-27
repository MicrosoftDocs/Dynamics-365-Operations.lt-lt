---
title: Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“
description: Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557929"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="71fac-103">Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="71fac-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="71fac-104">Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="71fac-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="71fac-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.</span><span class="sxs-lookup"><span data-stu-id="71fac-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="71fac-106">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą.</span><span class="sxs-lookup"><span data-stu-id="71fac-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="71fac-107">Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduotume įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="71fac-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="71fac-108">Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.</span><span class="sxs-lookup"><span data-stu-id="71fac-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="71fac-109">„Project Service Automation“ duomenų srautas į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="71fac-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="71fac-110">Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="71fac-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="71fac-111">Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto užduotis srautas iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="71fac-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="71fac-112">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="71fac-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="71fac-113">[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="71fac-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="71fac-114">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="71fac-114">Template and task</span></span>

<span data-ttu-id="71fac-115">Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="71fac-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="71fac-116">Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Project Service Automation“ projekto užduotis su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="71fac-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="71fac-117">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto užduotys (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="71fac-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="71fac-118">**Užduoties pavadinimas projekte:** projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="71fac-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="71fac-119">Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="71fac-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="71fac-120">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="71fac-120">Entity set</span></span>

| <span data-ttu-id="71fac-121">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="71fac-121">Project Service Automation</span></span> | <span data-ttu-id="71fac-122">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="71fac-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="71fac-123">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="71fac-123">Project Tasks</span></span>              | <span data-ttu-id="71fac-124">Projekto užduoties integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="71fac-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="71fac-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="71fac-125">Entity flow</span></span>

<span data-ttu-id="71fac-126">Projekto užduotys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto veiklos.</span><span class="sxs-lookup"><span data-stu-id="71fac-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="71fac-127">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="71fac-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="71fac-128">Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="71fac-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="71fac-129">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="71fac-129">Power Query</span></span>

<span data-ttu-id="71fac-130">Esant toliau nurodytai sąlygai filtruojant duomenis būtina naudoti „Microsoft Power Query“, skirtą „Excel“.</span><span class="sxs-lookup"><span data-stu-id="71fac-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="71fac-131">Projekto užduotyje yra konkrečiam ištekliui būdingų įrašų.</span><span class="sxs-lookup"><span data-stu-id="71fac-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="71fac-132">Jei naudojate „Power Query“, vykdykite šį nurodymą:</span><span class="sxs-lookup"><span data-stu-id="71fac-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="71fac-133">Projekto užduočių (PSA ir „Fin and Ops“) šablone naudojamas numatytasis filtras, kuris neįtraukia konkrečiam ištekliui būdingų projekto užduoties įrašų, nustatant **IsLineTask** filtro parinktį **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="71fac-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="71fac-134">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="71fac-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="71fac-135">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="71fac-135">Template mapping in Data integration</span></span>

<span data-ttu-id="71fac-136">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimų pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="71fac-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="71fac-137">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="71fac-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="71fac-138">[![Šablono susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="71fac-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
