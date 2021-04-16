---
title: Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ projektus sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5cb7f8b9a3107a7787c787ace71ab574457b1646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828496"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="b80de-103">Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="b80de-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b80de-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ projektus sinchronizuojant su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b80de-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="b80de-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b80de-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b80de-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="b80de-106">Templates and tasks</span></span>
<span data-ttu-id="b80de-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdymo projektus su „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b80de-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="b80de-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b80de-108">**Template in Data integration**</span></span>
- <span data-ttu-id="b80de-109">Projektai (iš Tiekimo grandinės valdymo į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="b80de-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="b80de-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b80de-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="b80de-111">Projektai</span><span class="sxs-lookup"><span data-stu-id="b80de-111">Projects</span></span>

<span data-ttu-id="b80de-112">Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="b80de-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="b80de-113">Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą)</span><span class="sxs-lookup"><span data-stu-id="b80de-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="b80de-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="b80de-114">Entity set</span></span>
| <span data-ttu-id="b80de-115">„Field Service“</span><span class="sxs-lookup"><span data-stu-id="b80de-115">Field Service</span></span>           | <span data-ttu-id="b80de-116">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="b80de-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="b80de-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="b80de-117">msdynce_externalprojects</span></span> | <span data-ttu-id="b80de-118">Projektai</span><span class="sxs-lookup"><span data-stu-id="b80de-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="b80de-119">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="b80de-119">Entity flow</span></span>
<span data-ttu-id="b80de-120">Projektai sukuriami Tiekimo grandinės valdyme.</span><span class="sxs-lookup"><span data-stu-id="b80de-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="b80de-121">Projektai, kurių **Projekto tipas** – **Laikas ir medžiagos**, o **Projekto etapas** – **Vykdoma**, sinchronizuojami su „Field Service“ objektu **Išorinis projektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="b80de-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="b80de-122">Sąrašas **Išorinis projektas** naudojamas „Field Service“ darbo užsakymams su Tiekimo grandinės valdymo projektais susieti.</span><span class="sxs-lookup"><span data-stu-id="b80de-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b80de-123">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="b80de-123">Field Service CRM solution</span></span>
<span data-ttu-id="b80de-124">**Išorinis projektas** yra objektas, gaunantis visus Tiekimo grandinės valdymo projektus.</span><span class="sxs-lookup"><span data-stu-id="b80de-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="b80de-125">Laukas **Išorinis projektas** įtrauktas į objektą **darbo užsakymo**.</span><span class="sxs-lookup"><span data-stu-id="b80de-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="b80de-126">Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas sujungiamas su Tiekimo grandinės valdymo projektu.</span><span class="sxs-lookup"><span data-stu-id="b80de-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="b80de-127">Kai **sistemos būsena** **Atidarytas – vykdomas (690,970,000)** keičiama į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.</span><span class="sxs-lookup"><span data-stu-id="b80de-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b80de-128">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="b80de-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="b80de-129">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="b80de-129">Supply Chain Management</span></span>
<span data-ttu-id="b80de-130">Įgalinti duomenų objekto projektų keitimų sekimą.</span><span class="sxs-lookup"><span data-stu-id="b80de-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b80de-131">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b80de-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="b80de-132">Projektai (iš Tiekimo grandinės valdymo į „Field Service“): projektai</span><span class="sxs-lookup"><span data-stu-id="b80de-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="b80de-133">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="b80de-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]