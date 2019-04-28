---
title: „Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ projektus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/14/2019
ms.locfileid: "842609"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cb1d4-103">„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="cb1d4-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cb1d4-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ projektus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cb1d4-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cb1d4-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cb1d4-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="cb1d4-106">Templates and tasks</span></span>
<span data-ttu-id="cb1d4-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cb1d4-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="cb1d4-108">**Template in Data integration**</span></span>
- <span data-ttu-id="cb1d4-109">Projektai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="cb1d4-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="cb1d4-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="cb1d4-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="cb1d4-111">Projektai</span><span class="sxs-lookup"><span data-stu-id="cb1d4-111">Projects</span></span>

<span data-ttu-id="cb1d4-112">Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="cb1d4-113">Sąskaitos (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="cb1d4-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="cb1d4-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="cb1d4-114">Entity set</span></span>
| <span data-ttu-id="cb1d4-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cb1d4-115">Field Service</span></span>           | <span data-ttu-id="cb1d4-116">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="cb1d4-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="cb1d4-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="cb1d4-117">msdynce_externalprojects</span></span> | <span data-ttu-id="cb1d4-118">Projektai</span><span class="sxs-lookup"><span data-stu-id="cb1d4-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="cb1d4-119">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="cb1d4-119">Entity flow</span></span>
<span data-ttu-id="cb1d4-120">„Finance and Operations“ sukurti projektai.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="cb1d4-121">Projektai, kurių **Projekto tipas** – **Laikas ir medžiagos**, o **Projekto etapas** – **Vykdoma**, sinchronizuojami su „Field Service“ objektu **Išorinis projektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="cb1d4-122">Sąrašas **Išorinis projektas** naudojamas „Field Service“ darbo užsakymams su „Finance and Operations“ projektais susieti.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cb1d4-123">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="cb1d4-123">Field Service CRM solution</span></span>
<span data-ttu-id="cb1d4-124">**Išorinis projektas** yra objektas, gaunantis visus „Finance and Operations“ projektus.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="cb1d4-125">Laukas **Išorinis projektas** įtrauktas į objektą **darbo užsakymo**.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="cb1d4-126">Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Finance and Operations“ projekto.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="cb1d4-127">Kai **sistemos būsena** **Atidarytas – vykdomas (690,970,000)** keičiama į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cb1d4-128">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="cb1d4-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="cb1d4-129">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="cb1d4-129">Finance and Operations</span></span>
<span data-ttu-id="cb1d4-130">Įgalinti duomenų objekto projektų keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="cb1d4-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cb1d4-131">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="cb1d4-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="cb1d4-132">Projektai („Finance and Operations“ su „Field Service“): projektai</span><span class="sxs-lookup"><span data-stu-id="cb1d4-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="cb1d4-133">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="cb1d4-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
