---
title: „Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2019
ms.locfileid: "836447"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="ac310-103">„Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="ac310-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac310-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ac310-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ac310-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="ac310-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="ac310-106">Naudojamas šablonas **Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)** yra paremtas šablonu **Darbo užsakymai („Field Service“ su „Fin and Ops“)**.</span><span class="sxs-lookup"><span data-stu-id="ac310-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="ac310-107">Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ pardavimo užsakymais](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="ac310-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="ac310-108">Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.</span><span class="sxs-lookup"><span data-stu-id="ac310-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="ac310-109">**Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)**</span><span class="sxs-lookup"><span data-stu-id="ac310-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="ac310-110">**Darbo užsakymai („Field Service“ su „Fin and Ops“)**</span><span class="sxs-lookup"><span data-stu-id="ac310-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="ac310-111">Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į „Finance and Operations“ sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="ac310-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="ac310-112">Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="ac310-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ac310-113">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="ac310-113">Templates and tasks</span></span>

<span data-ttu-id="ac310-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="ac310-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ac310-115">Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="ac310-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="ac310-116">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="ac310-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ac310-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ac310-117">WorkOrderHeader</span></span>
- <span data-ttu-id="ac310-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ac310-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="ac310-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ac310-119">WorkOrderProduct</span></span>
- <span data-ttu-id="ac310-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ac310-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ac310-121">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="ac310-121">Field Service CRM solution</span></span>
<span data-ttu-id="ac310-122">Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą.</span><span class="sxs-lookup"><span data-stu-id="ac310-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="ac310-123">Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Finance and Operations“ projekto.</span><span class="sxs-lookup"><span data-stu-id="ac310-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="ac310-124">Kai **Sistemos būsena** keičiama iš „Atidarytas – vykdomas“ (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.</span><span class="sxs-lookup"><span data-stu-id="ac310-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ac310-125">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="ac310-125">Template mapping in Data integration</span></span>

<span data-ttu-id="ac310-126">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="ac310-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="ac310-127">Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ac310-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="ac310-128">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="ac310-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="ac310-129">Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ac310-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="ac310-130">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="ac310-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="ac310-131">Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ac310-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="ac310-132">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="ac310-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="ac310-133">Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ac310-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="ac310-134">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="ac310-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
