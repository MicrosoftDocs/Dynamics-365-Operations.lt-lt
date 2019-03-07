---
title: „Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "329855"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="cea0c-103">„Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="cea0c-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cea0c-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="cea0c-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="cea0c-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cea0c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="cea0c-106">Naudojamas šablonas **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="cea0c-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="cea0c-107">Daugiau informacijos žr. [Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="cea0c-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="cea0c-108">Šioje temoje aprašomi tik skirtumai tarp šablonų **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** ir **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="cea0c-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="cea0c-109">Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į „Finance and Operations“ sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="cea0c-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="cea0c-110">Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="cea0c-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cea0c-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="cea0c-111">Templates and tasks</span></span>

<span data-ttu-id="cea0c-112">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="cea0c-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cea0c-113">Darbo užsakymai su projektu („Field Service“ su „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="cea0c-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="cea0c-114">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="cea0c-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cea0c-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="cea0c-115">WorkOrderHeader</span></span>
- <span data-ttu-id="cea0c-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="cea0c-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="cea0c-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="cea0c-117">WorkOrderProduct</span></span>
- <span data-ttu-id="cea0c-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="cea0c-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cea0c-119">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="cea0c-119">Field Service CRM solution</span></span>
<span data-ttu-id="cea0c-120">Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą.</span><span class="sxs-lookup"><span data-stu-id="cea0c-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="cea0c-121">Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Finance and Operations“ projekto.</span><span class="sxs-lookup"><span data-stu-id="cea0c-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="cea0c-122">Kai **Sistemos būsena** keičiama iš „Atidarytas – vykdomas“ (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.</span><span class="sxs-lookup"><span data-stu-id="cea0c-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cea0c-123">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="cea0c-123">Template mapping in Data integration</span></span>

<span data-ttu-id="cea0c-124">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="cea0c-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="cea0c-125">Darbo užsakymai su projektu („Field Service“ su „Finance and Operations“): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="cea0c-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="cea0c-126">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="cea0c-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="cea0c-127">Darbo užsakymai su projektu („Field Service“ su „Finance and Operations“): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="cea0c-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="cea0c-128">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="cea0c-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="cea0c-129">Darbo užsakymai su projektu („Field Service“ su „Finance and Operations“): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="cea0c-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="cea0c-130">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="cea0c-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="cea0c-131">Darbo užsakymai su projektu („Field Service“ su „Finance and Operations“): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="cea0c-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="cea0c-132">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="cea0c-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
