---
title: Tiekimo grandinės valdymo atsargų lygio informacijos sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
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
ms.openlocfilehash: 828dd1324c2692b7b3f4bc15c5e50b3dbee8b72c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010927"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="b9e18-103">Tiekimo grandinės valdymo atsargų lygio informacijos sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="b9e18-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b9e18-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b9e18-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="b9e18-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="b9e18-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b9e18-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="b9e18-106">Templates and tasks</span></span>
<span data-ttu-id="b9e18-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdyme turimų atsargų lygius su „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b9e18-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="b9e18-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b9e18-108">**Template in Data integration**</span></span>
- <span data-ttu-id="b9e18-109">Produktų atsargos (iš Tiekimo grandinės valdymo į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="b9e18-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="b9e18-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b9e18-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="b9e18-111">Produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="b9e18-111">Product inventory</span></span>

<span data-ttu-id="b9e18-112">Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="b9e18-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="b9e18-113">Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="b9e18-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="b9e18-114">„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="b9e18-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="b9e18-115">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="b9e18-115">Entity set</span></span>

| <span data-ttu-id="b9e18-116">„Field Service“</span><span class="sxs-lookup"><span data-stu-id="b9e18-116">Field Service</span></span>                      | <span data-ttu-id="b9e18-117">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="b9e18-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="b9e18-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="b9e18-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="b9e18-119">Turimos „Dataverse” atsargos sandėlyje</span><span class="sxs-lookup"><span data-stu-id="b9e18-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="b9e18-120">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="b9e18-120">Entity flow</span></span>
<span data-ttu-id="b9e18-121">Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b9e18-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="b9e18-122">Atsargų lygio informacija apima</span><span class="sxs-lookup"><span data-stu-id="b9e18-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="b9e18-123">Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)</span><span class="sxs-lookup"><span data-stu-id="b9e18-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="b9e18-124">Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, pvz., pardavimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="b9e18-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="b9e18-125">Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, pvz., pirkimo užsakymų kiekis)</span><span class="sxs-lookup"><span data-stu-id="b9e18-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="b9e18-126">Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.</span><span class="sxs-lookup"><span data-stu-id="b9e18-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="b9e18-127">„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems Tiekimo grandinės valdymo lygius, gauti.</span><span class="sxs-lookup"><span data-stu-id="b9e18-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="b9e18-128">Tiekimo grandinės valdymas veiks kaip atsargų lygių ruošinys.</span><span class="sxs-lookup"><span data-stu-id="b9e18-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="b9e18-129">Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į Tiekimo grandinės valdymą, jei šis funkcionalumas naudojamas „Field Service“ kartu su Tiekimo grandinės valdymo atsargų lygių sinchronizavimu.</span><span class="sxs-lookup"><span data-stu-id="b9e18-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="b9e18-130">Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal Tiekimo grandinės valdymą, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).</span><span class="sxs-lookup"><span data-stu-id="b9e18-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="b9e18-131">Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu Tiekimo grandinės valdymo sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="b9e18-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="b9e18-132">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tik siųstų naujinimus į Tiekimo grandinės valdymą.</span><span class="sxs-lookup"><span data-stu-id="b9e18-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="b9e18-133">Šiuo atveju „Field Service“ negaus Tiekimo grandinės valdymo atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="b9e18-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="b9e18-134">Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su Tiekimo grandinės valdymu](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su pardavimo užsakymais, susietais su Tiekimo grandinės valdymo projektu](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="b9e18-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b9e18-135">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="b9e18-135">Field Service CRM solution</span></span>
<span data-ttu-id="b9e18-136">Objektas **Išorinio produkto atsargos** naudojamas tik atliekant vidinį integravimą.</span><span class="sxs-lookup"><span data-stu-id="b9e18-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="b9e18-137">Šis objektas gauna tiekimo grandinės valdymo integravimo atsargų lygio reikšmes, kurios vėliau transformuojamos į atsargų žurnalus neautomatiniu būdu, o vėliau keičia atsargų produktus sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="b9e18-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b9e18-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="b9e18-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="b9e18-139">Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b9e18-139">Data integration</span></span>
<span data-ttu-id="b9e18-140">Norėdami, kad projektas veiktų, turite užtikrinti, kad būtų atnaujintas msdynce_externalproductinventories integravimo raktas.</span><span class="sxs-lookup"><span data-stu-id="b9e18-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="b9e18-141">Eikite į **Duomenų integravimas > Ryšio rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="b9e18-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="b9e18-142">Pasirinkite naudotą ryšio rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b9e18-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="b9e18-143">Skirtuke **Integravimo raktas** patikrinkite, ar šie raktai įtraukti į msdynce_externalproductinventories:</span><span class="sxs-lookup"><span data-stu-id="b9e18-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="b9e18-144">msdynce_productnumber (produkto numeris)</span><span class="sxs-lookup"><span data-stu-id="b9e18-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="b9e18-145">msdynce_warehouseid (sandėlio ID)</span><span class="sxs-lookup"><span data-stu-id="b9e18-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="b9e18-146">Duomenų integravimo projektas</span><span class="sxs-lookup"><span data-stu-id="b9e18-146">Data integration project</span></span>
<span data-ttu-id="b9e18-147">Galite taikyti filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik tam tikri produktai ir sandėliai siųstų atsargų lygio informaciją iš Tiekimo grandinės valdymo į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="b9e18-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b9e18-148">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b9e18-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="b9e18-149">Produktų atsargos (iš Tiekimo grandinės valdymo į „Field Service“): produktų atsargos</span><span class="sxs-lookup"><span data-stu-id="b9e18-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="b9e18-150">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="b9e18-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
