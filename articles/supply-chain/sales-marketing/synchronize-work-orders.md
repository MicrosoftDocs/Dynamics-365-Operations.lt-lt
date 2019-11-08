---
title: „Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5c57b8d1e09fd57611accec83ec3da4bc596fd00
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627556"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="93a7c-103">„Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu</span><span class="sxs-lookup"><span data-stu-id="93a7c-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="93a7c-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="93a7c-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="93a7c-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="93a7c-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="93a7c-106">Naudojamas šablonas **Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)** yra paremtas šablonu **Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**.</span><span class="sxs-lookup"><span data-stu-id="93a7c-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="93a7c-107">Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su Tiekimo grandinės valdymo pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="93a7c-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="93a7c-108">Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.</span><span class="sxs-lookup"><span data-stu-id="93a7c-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="93a7c-109">**Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)**</span><span class="sxs-lookup"><span data-stu-id="93a7c-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="93a7c-110">**Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**</span><span class="sxs-lookup"><span data-stu-id="93a7c-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="93a7c-111">Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į Tiekimo grandinės valdyme sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="93a7c-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="93a7c-112">Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="93a7c-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="93a7c-113">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="93a7c-113">Templates and tasks</span></span>

<span data-ttu-id="93a7c-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="93a7c-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="93a7c-115">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)</span><span class="sxs-lookup"><span data-stu-id="93a7c-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="93a7c-116">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="93a7c-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="93a7c-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="93a7c-117">WorkOrderHeader</span></span>
- <span data-ttu-id="93a7c-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="93a7c-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="93a7c-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="93a7c-119">WorkOrderProduct</span></span>
- <span data-ttu-id="93a7c-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="93a7c-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="93a7c-121">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="93a7c-121">Field Service CRM solution</span></span>
<span data-ttu-id="93a7c-122">Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą.</span><span class="sxs-lookup"><span data-stu-id="93a7c-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="93a7c-123">Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas bus sujungtas su Tiekimo grandinės valdymo projektu.</span><span class="sxs-lookup"><span data-stu-id="93a7c-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="93a7c-124">Kai **Sistemos būsena** keičiama iš Atidarytas – vykdomas (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti reikšmės.</span><span class="sxs-lookup"><span data-stu-id="93a7c-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="93a7c-125">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="93a7c-125">Template mapping in Data integration</span></span>

<span data-ttu-id="93a7c-126">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="93a7c-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="93a7c-127">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="93a7c-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="93a7c-128">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="93a7c-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="93a7c-129">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="93a7c-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="93a7c-130">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="93a7c-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="93a7c-131">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="93a7c-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="93a7c-132">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="93a7c-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="93a7c-133">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="93a7c-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="93a7c-134">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="93a7c-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
