---
title: "„Finance and Operations“ sandėlių sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ sandėlius su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1d539-103">„Finance and Operations“ sandėlių sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="1d539-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1d539-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ sandėlius su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1d539-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1d539-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="1d539-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1d539-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="1d539-106">Templates and tasks</span></span>
<span data-ttu-id="1d539-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ sandėlius su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1d539-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1d539-108">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="1d539-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="1d539-109">Sandėliai („Finance and Operations“ su „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="1d539-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="1d539-110">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="1d539-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="1d539-111">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="1d539-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="1d539-112">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="1d539-112">Entity set</span></span>
| <span data-ttu-id="1d539-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="1d539-113">Field Service</span></span>    | <span data-ttu-id="1d539-114">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="1d539-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="1d539-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="1d539-115">msdyn_warehouses</span></span> | <span data-ttu-id="1d539-116">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="1d539-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="1d539-117">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="1d539-117">Entity flow</span></span>
<span data-ttu-id="1d539-118">Sandėlius, kurie kuriami ir tvarkomi „Finance and Operations“, galima sinchronizuoti su „Field Service“ per „Common Data Service“ (CDS) duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="1d539-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="1d539-119">Pageidaujamus sandėlius, kurie sinchronizuojami su „Field Service“, galima valdyti projekte naudojant išplėstinę užklausą ir filtravimą.</span><span class="sxs-lookup"><span data-stu-id="1d539-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="1d539-120">Sandėliai, kurie sinchronizuojami „Finance and Operations“, sukuriami „Field Service“, kurios laukas „Tvarkomas išoriškai“ nustatomas į Taip, o įrašas skirtas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="1d539-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="1d539-121">„Field Service“ CRM sprendimui reikalinga papildoma funkcija iš „Field Service“ CRM sprendimo, kad būtų palaikomas „Field Service“ ir „Finance and Operations“ integravimas.</span><span class="sxs-lookup"><span data-stu-id="1d539-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="1d539-122">Sprendimas apima toliau nurodytus keitimus.</span><span class="sxs-lookup"><span data-stu-id="1d539-122">The solution includes the following changes.</span></span>
<span data-ttu-id="1d539-123">Laukas **Tvarkomas išoriškai** įtrauktas į objektą **Sandėlis (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="1d539-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="1d539-124">Šis laukas padeda nustatyti, ar sandėlis tvarkomas iš „Operations“, ar jis yra tik „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1d539-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="1d539-125">Taip – sandėlis sukurtas „Finance and Operations“ ir jo nebus galima redaguoti „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1d539-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="1d539-126">Ne – sandėlis buvo įvestas tiesiogiai „Field Service“ ir tvarkomas čia.</span><span class="sxs-lookup"><span data-stu-id="1d539-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="1d539-127">Laukas **Tvarkomas išoriškai** padeda kontroliuoti atsargų lygių sinchronizavimą, koregavimą, perkėlimą ir naudojimą darbo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="1d539-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="1d539-128">Tik sandėlius, kurių parinktis **Tvarkomas išoriškai** = Taip, galima naudoti norint tiesiogiai sinchronizuoti su tuo pačiu sandėliu kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1d539-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="1d539-129">Pastaba. Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai** = Ne), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą.</span><span class="sxs-lookup"><span data-stu-id="1d539-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="1d539-130">Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tiesiog siųstų naujinimus į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="1d539-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="1d539-131">Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų.</span><span class="sxs-lookup"><span data-stu-id="1d539-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="1d539-132">Papildomos informacijos žr. „Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“ ir „Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais“.</span><span class="sxs-lookup"><span data-stu-id="1d539-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1d539-133">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="1d539-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="1d539-134">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="1d539-134">In the Data Integration project</span></span>
<span data-ttu-id="1d539-135">Prieš sinchronizuojant sandėlius būtina atnaujinti projekto išplėstinę užklausą ir filtravimą, įtraukiant tik tuos sandėlius, kuriuos norima perkelti iš „Finance and Operations“ į „Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1d539-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="1d539-136">Atkreipkite dėmesį, kad jums reikės „Field Service“ sandėlio, kurį būtų galima taikyti darbo užsakymams, koregavimui ir perkėlimui.</span><span class="sxs-lookup"><span data-stu-id="1d539-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="1d539-137">Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="1d539-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="1d539-138">Eikite į Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="1d539-138">Go to Data Integration</span></span>
2. <span data-ttu-id="1d539-139">Pasirinkite skirtuką **Ryšio rinkinys**</span><span class="sxs-lookup"><span data-stu-id="1d539-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="1d539-140">Pasirinkite Ryšio rinkinys, naudojamą Darbo užsakymui sinchronizuoti</span><span class="sxs-lookup"><span data-stu-id="1d539-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="1d539-141">Pasirinkite skirtuką **Integravimo raktas**</span><span class="sxs-lookup"><span data-stu-id="1d539-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="1d539-142">Raskite msdyn_warehouses ir patikrinkite, ar pridėtas raktas **msdyn_name (pavadinimas)**.</span><span class="sxs-lookup"><span data-stu-id="1d539-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="1d539-143">Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**</span><span class="sxs-lookup"><span data-stu-id="1d539-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1d539-144">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="1d539-144">Template mapping in Data integration</span></span>

<span data-ttu-id="1d539-145">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="1d539-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="1d539-146">Sandėliai („Finance and Operations“ su „Field Service“): sandėlis</span><span class="sxs-lookup"><span data-stu-id="1d539-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="1d539-147">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="1d539-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

