---
title: "„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="a812e-103">„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="a812e-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a812e-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="a812e-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a812e-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="a812e-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a812e-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="a812e-106">Templates and tasks</span></span>
<span data-ttu-id="a812e-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="a812e-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a812e-108">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="a812e-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="a812e-109">Projektai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="a812e-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="a812e-110">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="a812e-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="a812e-111">Projektai</span><span class="sxs-lookup"><span data-stu-id="a812e-111">Projects</span></span>

<span data-ttu-id="a812e-112">Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="a812e-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="a812e-113">Sąskaitos („Sales“ su „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="a812e-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="a812e-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="a812e-114">Entity set</span></span>
<span data-ttu-id="a812e-115">„Field Service“   „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="a812e-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="a812e-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="a812e-116">Field Service</span></span>           | <span data-ttu-id="a812e-117">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="a812e-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="a812e-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="a812e-118">msdynce_externalprojects</span></span> | <span data-ttu-id="a812e-119">Projektai</span><span class="sxs-lookup"><span data-stu-id="a812e-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="a812e-120">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="a812e-120">Entity flow</span></span>
<span data-ttu-id="a812e-121">„Finance and Operations“ sukurti projektai.</span><span class="sxs-lookup"><span data-stu-id="a812e-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="a812e-122">Projektai, kurių **Projekto tipas** – Laikas ir medžiagos, o **Projekto etapas** – Vykdoma, sinchronizuojami su „Field Service“ objektu **Išorinis objektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="a812e-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="a812e-123">**Išorinio projekto** sąrašas naudojamas „Field Service“ darbo užsakymams su „Finance and Operations“ projektais susieti.</span><span class="sxs-lookup"><span data-stu-id="a812e-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="a812e-124">„Field Service“ CRM sprendimas Išorinis projektas yra naujas objektas, gaunantis visus „Operations“ projektus.</span><span class="sxs-lookup"><span data-stu-id="a812e-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="a812e-125">Išorinio projekto laukas įtrauktas į darbo užsakymo objektą.</span><span class="sxs-lookup"><span data-stu-id="a812e-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="a812e-126">Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Operations“ projekto.</span><span class="sxs-lookup"><span data-stu-id="a812e-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="a812e-127">Kai sistemos būsena „Atidarytas – vykdomas“ (690,970,000) keičiama į aukštesnę būseną, išorinio projekto laukas užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.</span><span class="sxs-lookup"><span data-stu-id="a812e-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a812e-128">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="a812e-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="a812e-129">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="a812e-129">In Finance and Operations</span></span>
<span data-ttu-id="a812e-130">Įgalinti duomenų objekto projektų keitimų sekimą</span><span class="sxs-lookup"><span data-stu-id="a812e-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a812e-131">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="a812e-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="a812e-132">Projektai („Finance and Operations“ su „Field Service“): projektai</span><span class="sxs-lookup"><span data-stu-id="a812e-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="a812e-133">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="a812e-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

