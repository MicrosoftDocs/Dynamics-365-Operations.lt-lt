---
title: „Finance and Operations“ sandėlių sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ sandėlius sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835675"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1e042-103">„Finance and Operations“ sandėlių sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="1e042-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1e042-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ sandėlius sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1e042-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1e042-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="1e042-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1e042-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="1e042-106">Templates and tasks</span></span>
<span data-ttu-id="1e042-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ sandėlius su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1e042-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1e042-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="1e042-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1e042-109">Sandėliai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="1e042-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="1e042-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="1e042-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1e042-111">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="1e042-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="1e042-112">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="1e042-112">Entity set</span></span>
| <span data-ttu-id="1e042-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="1e042-113">Field Service</span></span>    | <span data-ttu-id="1e042-114">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="1e042-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="1e042-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="1e042-115">msdyn_warehouses</span></span> | <span data-ttu-id="1e042-116">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="1e042-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="1e042-117">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="1e042-117">Entity flow</span></span>
<span data-ttu-id="1e042-118">Sandėlius, kurie kuriami ir tvarkomi „Finance and Operations“, galima sinchronizuoti su „Field Service“ per „Common Data Service“ (CDS) duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="1e042-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="1e042-119">Pageidaujamus sandėlius, kurie sinchronizuojami su „Field Service“, galima valdyti projekte naudojant išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="1e042-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="1e042-120">Sandėliai, kurie sinchronizuojami „Finance and Operations“, sukuriami „Field Service“, kurios laukas **Tvarkomas išoriškai** nustatomas į **Taip**, o įrašas skirtas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="1e042-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1e042-121">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e042-121">Field Service CRM solution</span></span>
<span data-ttu-id="1e042-122">Reikalinga papildoma funkcija iš „Field Service“ CRM sprendimo, kad būtų palaikomas „Field Service ir „Finance and Operations“ integravimas.</span><span class="sxs-lookup"><span data-stu-id="1e042-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="1e042-123">Sprendimo laukas **Tvarkomas išoriškai** įtrauktas į objektą **Sandėlis (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="1e042-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="1e042-124">Šis laukas padeda nustatyti, ar sandėlis tvarkomas iš „Finance and Operations“, ar jis yra tik „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1e042-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="1e042-125">Šio lauko parametrai apima toliau nurodytas parinktis.</span><span class="sxs-lookup"><span data-stu-id="1e042-125">The settings for this field include:</span></span>
- <span data-ttu-id="1e042-126">**Taip** – sandėlis sukurtas „Finance and Operations“ ir jo nebus galima redaguoti „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1e042-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="1e042-127">**Ne** – sandėlis buvo įvestas tiesiogiai „Field Service“ ir tvarkomas čia.</span><span class="sxs-lookup"><span data-stu-id="1e042-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="1e042-128">Laukas **Tvarkomas išoriškai** padeda kontroliuoti atsargų lygių sinchronizavimą, koregavimą, perkėlimą ir naudojimą darbo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="1e042-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="1e042-129">Tik sandėlius, kurių parinktis **Tvarkomas išoriškai** nustatyta į **Taip**, galima naudoti norint tiesiogiai sinchronizuoti su tuo pačiu sandėliu kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1e042-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="1e042-130">Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="1e042-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="1e042-131">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tiesiog siųstų naujinimus į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="1e042-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="1e042-132">Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="1e042-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="1e042-133">Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="1e042-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1e042-134">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="1e042-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="1e042-135">Duomenų integravimo projektas</span><span class="sxs-lookup"><span data-stu-id="1e042-135">Data Integration project</span></span>
<span data-ttu-id="1e042-136">Prieš sinchronizuojant sandėlius būtina atnaujinti projekto išplėstinę užklausą ir filtravimą, įtraukiant tik tuos sandėlius, kuriuos norima perkelti iš „Finance and Operations“ į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1e042-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="1e042-137">Atkreipkite dėmesį, kad jums reikės „Field Service“ sandėlio, kurį būtų galima taikyti darbo užsakymams, koregavimui ir perkėlimui.</span><span class="sxs-lookup"><span data-stu-id="1e042-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="1e042-138">Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_warehouses**.</span><span class="sxs-lookup"><span data-stu-id="1e042-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="1e042-139">Pasirinkite Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="1e042-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="1e042-140">Pasirinkite skirtuką **Ryšio rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="1e042-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="1e042-141">Pasirinkite ryšio rinkinį, naudojamą darbo užsakymui sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="1e042-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="1e042-142">Pasirinkite skirtuką **Integravimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="1e042-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="1e042-143">Raskite msdyn_warehouses ir patikrinkite, ar pridėtas raktas **msdyn_name (pavadinimas)**.</span><span class="sxs-lookup"><span data-stu-id="1e042-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="1e042-144">Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1e042-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1e042-145">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="1e042-145">Template mapping in Data integration</span></span>

<span data-ttu-id="1e042-146">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="1e042-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="1e042-147">Sandėliai („Finance and Operations“ su „Field Service“): sandėliai</span><span class="sxs-lookup"><span data-stu-id="1e042-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="1e042-148">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="1e042-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
