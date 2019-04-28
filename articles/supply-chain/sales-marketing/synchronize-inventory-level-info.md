---
title: „Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“.
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
ms.openlocfilehash: 6b2bdf1ca6f6ae43cd85c8a1353ee8305052761d
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/14/2019
ms.locfileid: "842561"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="f25b2-103">„Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="f25b2-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f25b2-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="f25b2-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f25b2-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="f25b2-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f25b2-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="f25b2-106">Templates and tasks</span></span>
<span data-ttu-id="f25b2-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ turimų atsargų lygius su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="f25b2-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f25b2-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="f25b2-108">**Template in Data integration**</span></span>
- <span data-ttu-id="f25b2-109">Produktų atsargos („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="f25b2-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="f25b2-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="f25b2-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="f25b2-111">Produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="f25b2-111">Product inventory</span></span>

<span data-ttu-id="f25b2-112">Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="f25b2-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="f25b2-113">Sandėliai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="f25b2-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="f25b2-114">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)</span><span class="sxs-lookup"><span data-stu-id="f25b2-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="f25b2-115">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="f25b2-115">Entity set</span></span>

| <span data-ttu-id="f25b2-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="f25b2-116">Field Service</span></span>                      | <span data-ttu-id="f25b2-117">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="f25b2-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="f25b2-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="f25b2-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="f25b2-119">CDS turimos atsargos pagal sandėlį</span><span class="sxs-lookup"><span data-stu-id="f25b2-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="f25b2-120">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="f25b2-120">Entity flow</span></span>
<span data-ttu-id="f25b2-121">Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="f25b2-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="f25b2-122">Atsargų lygio informacija apima</span><span class="sxs-lookup"><span data-stu-id="f25b2-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="f25b2-123">Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)</span><span class="sxs-lookup"><span data-stu-id="f25b2-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="f25b2-124">Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, pvz., pardavimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="f25b2-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="f25b2-125">Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, pvz., pirkimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="f25b2-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="f25b2-126">Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.</span><span class="sxs-lookup"><span data-stu-id="f25b2-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="f25b2-127">„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems „Finance and Operations“ lygius, gauti.</span><span class="sxs-lookup"><span data-stu-id="f25b2-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="f25b2-128">„Finance and Operations“ veiks kaip atsargų lygių ruošinys.</span><span class="sxs-lookup"><span data-stu-id="f25b2-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="f25b2-129">Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į „Finance and Operations“, jei šis funkcionalumas naudojamas „Field Service“ kartu su „Finance and Operations“ atsargų lygių sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="f25b2-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="f25b2-130">Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal „Finance and Operations“, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).</span><span class="sxs-lookup"><span data-stu-id="f25b2-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="f25b2-131">Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="f25b2-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="f25b2-132">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tik siųstų naujinimus į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f25b2-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="f25b2-133">Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="f25b2-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="f25b2-134">Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="f25b2-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f25b2-135">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="f25b2-135">Field Service CRM solution</span></span>
<span data-ttu-id="f25b2-136">Objektas **Išorinio produkto atsargos** naudojamas tik atliekant vidinį integravimą.</span><span class="sxs-lookup"><span data-stu-id="f25b2-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="f25b2-137">Šis objektas gauna „Finance and Operations“ integravimo atsargų lygio reikšmes, kurios vėliau transformuojamos į atsargų žurnalus neautomatiniu būdu, o vėliau keičia atsargų produktus sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="f25b2-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f25b2-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="f25b2-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration-project"></a><span data-ttu-id="f25b2-139">Duomenų integravimo projektas</span><span class="sxs-lookup"><span data-stu-id="f25b2-139">Data integration project</span></span>
<span data-ttu-id="f25b2-140">Galite taikyti filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik tam tikri produktai ir sandėliai siųstų atsargų lygio informaciją iš „Finance and Operations“ į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="f25b2-140">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f25b2-141">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="f25b2-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="f25b2-142">Produktų atsargos („Finance and Operations“ su „Field Service“): produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="f25b2-142">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="f25b2-143">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="f25b2-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
