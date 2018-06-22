---
title: "„Project Service Automation“ projekto užduočių sinchronizavimas"
description: "Šioje temoje aprašomas šablonas ir pagrindinė užduotis, naudojama „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="e473f-103">„Project Service Automation“ tiesioginis sinchronizavimas su „Finance and Operations“ projekto veiklomis</span><span class="sxs-lookup"><span data-stu-id="e473f-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="e473f-104">Šioje temoje aprašomas šablonas ir pagrindinė užduotis, naudojama „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e473f-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e473f-105">Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.</span><span class="sxs-lookup"><span data-stu-id="e473f-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e473f-106">„Project Service Automation“ duomenų srautas į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="e473f-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="e473f-107">Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="e473f-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="e473f-108">Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto užduotis srautas iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e473f-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e473f-109">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e473f-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="e473f-110">[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e473f-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="e473f-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="e473f-111">Template and task</span></span>

<span data-ttu-id="e473f-112">Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="e473f-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e473f-113">Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Project Service Automation“ projekto užduotis su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e473f-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="e473f-114">-**Duomenų integravimo šablono pavadinimas:** Projekto užduotys (PSA ir „Fin and Ops“) -**Projekto užduoties pavadinimas:** Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="e473f-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="e473f-115">Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="e473f-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="e473f-116">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="e473f-116">Entity set</span></span>

|<span data-ttu-id="e473f-117">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="e473f-117">Project Service Automation</span></span>               | <span data-ttu-id="e473f-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="e473f-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="e473f-119">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="e473f-119">Project Tasks</span></span>                           | <span data-ttu-id="e473f-120">Projekto užduoties integravimo objektas.</span><span class="sxs-lookup"><span data-stu-id="e473f-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="e473f-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="e473f-121">Entity flow</span></span>

<span data-ttu-id="e473f-122">Projekto užduotys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto veiklos.</span><span class="sxs-lookup"><span data-stu-id="e473f-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e473f-123">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="e473f-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="e473f-124">Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="e473f-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="e473f-125">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="e473f-125">Power Query</span></span>

<span data-ttu-id="e473f-126">Esant toliau nurodytoms sąlygoms filtruojant duomenis būtina naudoti „Microsoft Power Query“.</span><span class="sxs-lookup"><span data-stu-id="e473f-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="e473f-127">Esama konkrečiam ištekliui būdingų projekto užduoties įrašų.</span><span class="sxs-lookup"><span data-stu-id="e473f-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="e473f-128">Jei naudojate „Power Query“, vykdykite toliau išvardytus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="e473f-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="e473f-129">Projekto užduočių (PSA ir „Fin and Ops“) šablone naudojamas numatytasis filtras, skirtas neįtraukti konkrečiam ištekliui būdingų projekto užduoties įrašų, nustatant **IsLineTask** filtro parinktį **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="e473f-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="e473f-130">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="e473f-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e473f-131">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="e473f-131">Template mapping in Data integration</span></span>

<span data-ttu-id="e473f-132">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimų pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="e473f-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="e473f-133">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e473f-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="e473f-134">[![Šablono susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="e473f-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


