---
title: Tiekimo grandinės valdymo sandėlių sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ sandėlius sinchronizuojant su „Dynamics 365 Field Service“.
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
ms.openlocfilehash: b55a0b9e54eabdcdbd3f858cf3725b8fe833f65d
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653399"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="14b35-103">Tiekimo grandinės valdymo sandėlių sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="14b35-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="14b35-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ sandėlius sinchronizuojant su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="14b35-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="14b35-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="14b35-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="14b35-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="14b35-106">Templates and tasks</span></span>
<span data-ttu-id="14b35-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdymo sandėlius su „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="14b35-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="14b35-108">**Šablonas naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="14b35-108">**Template in Data integration**</span></span>
- <span data-ttu-id="14b35-109">Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="14b35-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="14b35-110">**Užduotis projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="14b35-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="14b35-111">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="14b35-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="14b35-112">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="14b35-112">Entity set</span></span>
| <span data-ttu-id="14b35-113">„Field Service“</span><span class="sxs-lookup"><span data-stu-id="14b35-113">Field Service</span></span>    | <span data-ttu-id="14b35-114">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="14b35-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="14b35-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="14b35-115">msdyn_warehouses</span></span> | <span data-ttu-id="14b35-116">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="14b35-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="14b35-117">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="14b35-117">Entity flow</span></span>
<span data-ttu-id="14b35-118">Sandėlius, kurie kuriami ir tvarkomi Tiekimo grandinės valdyme, galima sinchronizuoti su „Field Service“ per „Common Data Service“ (CDS) duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="14b35-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="14b35-119">Pageidaujamus sandėlius, kurie sinchronizuojami su „Field Service“, galima valdyti projekte naudojant išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="14b35-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="14b35-120">Sandėliai, kurie sinchronizuojami iš Tiekimo grandinės valdymo, sukuriami „Field Service“, kurios lauke **Tvarkomas išoriškai** nustatoma **Taip**, o įrašas skirtas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="14b35-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="14b35-121">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="14b35-121">Field Service CRM solution</span></span>
<span data-ttu-id="14b35-122">Reikalinga papildoma „Field Service“ CRM sprendimo funkcija, kad būtų palaikomas „Field Service“ ir „Supply Chain Management“ integravimas.</span><span class="sxs-lookup"><span data-stu-id="14b35-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="14b35-123">Sprendimo laukas **Tvarkomas išoriškai** įtrauktas į objektą **Sandėlis (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="14b35-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="14b35-124">Šis laukas padeda nustatyti, ar sandėlis tvarkomas iš Tiekimo grandinės valdymo, ar jis yra tik „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="14b35-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="14b35-125">Šio lauko parametrai apima toliau nurodytas parinktis.</span><span class="sxs-lookup"><span data-stu-id="14b35-125">The settings for this field include:</span></span>
- <span data-ttu-id="14b35-126">**Taip** – sandėlis paimtas iš Tiekimo grandinės valdymo ir jo nebus galima redaguoti sprendime „Sales“.</span><span class="sxs-lookup"><span data-stu-id="14b35-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="14b35-127">**Ne** – sandėlis buvo įvestas tiesiogiai „Field Service“ ir tvarkomas čia.</span><span class="sxs-lookup"><span data-stu-id="14b35-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="14b35-128">Laukas **Tvarkomas išoriškai** padeda kontroliuoti atsargų lygių sinchronizavimą, koregavimą, perkėlimą ir naudojimą darbo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="14b35-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="14b35-129">Tik sandėlius, kurių parinktis **Tvarkomas išoriškai** nustatyta į **Taip**, galima naudoti norint tiesiogiai sinchronizuoti su tuo pačiu sandėliu kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="14b35-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="14b35-130">Galima sukurti keletą „Field Service“ sandėlių (esant **Tvarkomas išoriškai** = Ne), o tada juos susieti su vienu sandėliu, naudojant išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="14b35-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="14b35-131">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir į „Supply Chain Management“ siųstų tik naujinimus.</span><span class="sxs-lookup"><span data-stu-id="14b35-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="14b35-132">Šiuo atveju „Field Service“ negaus Tiekimo grandinės valdymo atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="14b35-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="14b35-133">Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="14b35-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="14b35-134">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="14b35-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="14b35-135">Duomenų integravimo projektas</span><span class="sxs-lookup"><span data-stu-id="14b35-135">Data Integration project</span></span>
<span data-ttu-id="14b35-136">Prieš sinchronizuojant sandėlius būtina atnaujinti projekto išplėstinę užklausą ir filtravimą, įtraukiant tik tuos sandėlius, kuriuos norima perkelti iš Tiekimo grandinės valdymo į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="14b35-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="14b35-137">Atkreipkite dėmesį, kad jums reikės „Field Service“ sandėlio, kurį būtų galima taikyti darbo užsakymams, koregavimui ir perkėlimui.</span><span class="sxs-lookup"><span data-stu-id="14b35-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="14b35-138">Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_warehouses**.</span><span class="sxs-lookup"><span data-stu-id="14b35-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="14b35-139">Pasirinkite Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="14b35-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="14b35-140">Pasirinkite skirtuką **Ryšio rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="14b35-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="14b35-141">Pasirinkite ryšio rinkinį, naudojamą darbo užsakymui sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="14b35-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="14b35-142">Pasirinkite skirtuką **Integravimo raktas**.</span><span class="sxs-lookup"><span data-stu-id="14b35-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="14b35-143">Raskite msdyn_warehouses ir patikrinkite, ar pridėtas raktas **msdyn_name (pavadinimas)**.</span><span class="sxs-lookup"><span data-stu-id="14b35-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="14b35-144">Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="14b35-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="14b35-145">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="14b35-145">Template mapping in Data integration</span></span>

<span data-ttu-id="14b35-146">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="14b35-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="14b35-147">Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“): sandėliai</span><span class="sxs-lookup"><span data-stu-id="14b35-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="14b35-148">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="14b35-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
