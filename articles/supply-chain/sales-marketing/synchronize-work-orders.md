---
title: „Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d2364378ce8992666e374ec6f665c180d2fa1981
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258028"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="38837-103">„Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu</span><span class="sxs-lookup"><span data-stu-id="38837-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="38837-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="38837-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="38837-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="38837-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="38837-106">Naudojamas šablonas **Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)** yra paremtas šablonu **Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**.</span><span class="sxs-lookup"><span data-stu-id="38837-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="38837-107">Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su Tiekimo grandinės valdymo pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="38837-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="38837-108">Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.</span><span class="sxs-lookup"><span data-stu-id="38837-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="38837-109">**Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)**</span><span class="sxs-lookup"><span data-stu-id="38837-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="38837-110">**Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**</span><span class="sxs-lookup"><span data-stu-id="38837-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="38837-111">Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į Tiekimo grandinės valdyme sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="38837-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="38837-112">Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="38837-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="38837-113">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="38837-113">Templates and tasks</span></span>

<span data-ttu-id="38837-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="38837-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="38837-115">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)</span><span class="sxs-lookup"><span data-stu-id="38837-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="38837-116">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="38837-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="38837-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="38837-117">WorkOrderHeader</span></span>
- <span data-ttu-id="38837-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="38837-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="38837-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="38837-119">WorkOrderProduct</span></span>
- <span data-ttu-id="38837-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="38837-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="38837-121">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="38837-121">Field Service CRM solution</span></span>
<span data-ttu-id="38837-122">Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą.</span><span class="sxs-lookup"><span data-stu-id="38837-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="38837-123">Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas bus sujungtas su Tiekimo grandinės valdymo projektu.</span><span class="sxs-lookup"><span data-stu-id="38837-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="38837-124">Kai **Sistemos būsena** keičiama iš Atidarytas – vykdomas (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti reikšmės.</span><span class="sxs-lookup"><span data-stu-id="38837-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="38837-125">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="38837-125">Template mapping in Data integration</span></span>

<span data-ttu-id="38837-126">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="38837-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="38837-127">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="38837-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="38837-128">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="38837-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="38837-129">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="38837-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="38837-130">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="38837-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="38837-131">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="38837-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="38837-132">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="38837-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="38837-133">Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="38837-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="38837-134">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="38837-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]