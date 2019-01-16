---
title: "„Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“."
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="6fa75-103">„Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="6fa75-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6fa75-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6fa75-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="6fa75-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6fa75-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="6fa75-106">Templates and tasks</span></span>
<span data-ttu-id="6fa75-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ turimų atsargų lygius su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="6fa75-108">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="6fa75-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="6fa75-109">Produktų atsargos („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="6fa75-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="6fa75-110">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="6fa75-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="6fa75-111">Produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="6fa75-111">Product inventory</span></span>

<span data-ttu-id="6fa75-112">Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="6fa75-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="6fa75-113">Sandėliai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="6fa75-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="6fa75-114">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)</span><span class="sxs-lookup"><span data-stu-id="6fa75-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="6fa75-115">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="6fa75-115">Entity set</span></span>

| <span data-ttu-id="6fa75-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="6fa75-116">Field Service</span></span>                      | <span data-ttu-id="6fa75-117">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="6fa75-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="6fa75-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="6fa75-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="6fa75-119">CDS turimos atsargos pagal sandėlį</span><span class="sxs-lookup"><span data-stu-id="6fa75-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="6fa75-120">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="6fa75-120">Entity flow</span></span>
<span data-ttu-id="6fa75-121">Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="6fa75-122">Atsargų lygio informacija apima:</span><span class="sxs-lookup"><span data-stu-id="6fa75-122">The inventory level information include:</span></span> 
- <span data-ttu-id="6fa75-123">Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)</span><span class="sxs-lookup"><span data-stu-id="6fa75-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="6fa75-124">Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, t. y. pardavimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="6fa75-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="6fa75-125">Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, t. y. pirkimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="6fa75-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="6fa75-126">Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.</span><span class="sxs-lookup"><span data-stu-id="6fa75-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="6fa75-127">„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems „Finance and Operations“ lygius, gauti.</span><span class="sxs-lookup"><span data-stu-id="6fa75-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="6fa75-128">„Finance and Operations“ veiks kaip atsargų lygių ruošinys.</span><span class="sxs-lookup"><span data-stu-id="6fa75-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="6fa75-129">Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į „Finance and Operations“, jei šis funkcionalumas naudojamas „Field Service“ kartu su „Finance and Operations“ atsargų lygių sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="6fa75-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="6fa75-130">Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal „Finance and Operations“, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).</span><span class="sxs-lookup"><span data-stu-id="6fa75-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="6fa75-131">Pastaba. Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį „Tvarkomas išoriškai = Ne“), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="6fa75-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="6fa75-132">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tiesiog siųstų naujinimus į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="6fa75-133">Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="6fa75-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="6fa75-134">Papildomos informacijos žr. „Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“ ir „Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="6fa75-135">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="6fa75-135">Field Service CRM solution</span></span>
<span data-ttu-id="6fa75-136">Išorinio produkto atsargų objektas yra naujas objektas, naudojamas tik vidiniam integravimui.</span><span class="sxs-lookup"><span data-stu-id="6fa75-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="6fa75-137">Gaunamos „Finance and Operations“ integravimo atsargų lygio vertės, kurios paskui transformuojamos į atsargų žurnalus rankiniu būdu, o vėliau keičia atsargų produktus sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="6fa75-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="6fa75-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="6fa75-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="6fa75-139">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="6fa75-139">In the Data Integration project</span></span>
<span data-ttu-id="6fa75-140">Taikykite filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik pageidaujami produktai ir sandėliai siųstų atsargų lygio informaciją iš „Finance and Operations“ į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="6fa75-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6fa75-141">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="6fa75-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="6fa75-142">Produktų atsargos („Finance and Operations“ su „Field Service“): produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="6fa75-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="6fa75-143">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="6fa75-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

