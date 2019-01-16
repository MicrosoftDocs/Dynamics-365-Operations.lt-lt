---
title: "„Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="ff44f-103">„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="ff44f-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ff44f-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="ff44f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ff44f-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="ff44f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ff44f-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="ff44f-106">Templates and tasks</span></span>
<span data-ttu-id="ff44f-107">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ff44f-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ff44f-108">**Šablonų pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="ff44f-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="ff44f-109">Atsargų koregavimas („Field Service“ su „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="ff44f-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="ff44f-110">Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="ff44f-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="ff44f-111">**Užduočių pavadinimai projektuose Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="ff44f-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="ff44f-112">Atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-112">Inventory Adjustments</span></span>
- <span data-ttu-id="ff44f-113">Atsargų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="ff44f-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="ff44f-114">Entity set</span></span>
| <span data-ttu-id="ff44f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="ff44f-115">Field Service</span></span>                     | <span data-ttu-id="ff44f-116">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="ff44f-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="ff44f-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="ff44f-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="ff44f-118">CDS atsargų koregavimo žurnalo antraštės ir eilutės</span><span class="sxs-lookup"><span data-stu-id="ff44f-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="ff44f-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="ff44f-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="ff44f-120">CDS atsargų perkėlimo žurnalo antraštės ir eilutės</span><span class="sxs-lookup"><span data-stu-id="ff44f-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="ff44f-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="ff44f-121">Entity flow</span></span>
<span data-ttu-id="ff44f-122">„Field Service“ atliktas atsargų koregavimas ir perkėlimas sinchronizuojamas su „Finance and Operations“, kai **Registruoti būseną** pasikeičia iš Sukurta į Užregistruota.</span><span class="sxs-lookup"><span data-stu-id="ff44f-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="ff44f-123">Tokiu atveju koregavimo arba perkėlimo užsakymas užrakinamas ir tampa tik skaitomas, nes koregavimas ir perkėlimas gali būti registruojami „Finance and Operations“, todėl jų modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="ff44f-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="ff44f-124">„Finance and Operations“ galite nustatyti paketinę užduotį automatiškai registruoti koregavimą ir perkelti sugeneruotus atsargų žurnalus atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="ff44f-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="ff44f-125">Išsamesnės būtinos informacijos apie tai, kaip įgalinti paketinę užduotį, žr. toliau.</span><span class="sxs-lookup"><span data-stu-id="ff44f-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ff44f-126">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-126">Field Service CRM solution</span></span> 
<span data-ttu-id="ff44f-127">Atsargų vieneto laukas įtrauktas į produkto objektą.</span><span class="sxs-lookup"><span data-stu-id="ff44f-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="ff44f-128">Šis laukas reikalingas, nes pardavimo ir atsargų vienetas „Operations“ ne visada yra tas pats, o dėl sandėlio atsargų operacijų mums reikia atsargų vieneto.</span><span class="sxs-lookup"><span data-stu-id="ff44f-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="ff44f-129">Nustatant į atsargų koregavimo produktą įtrauktą produktą, skirtą atsargų koregavimui ir atsargų perkėlimui, vieneto bus ieškoma pagal produktų atsargų produkto vertę.</span><span class="sxs-lookup"><span data-stu-id="ff44f-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="ff44f-130">Jei nustatoma vertė, atsargų koregavimo produkto vieneto laukas užrakinamas</span><span class="sxs-lookup"><span data-stu-id="ff44f-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="ff44f-131">Laukas Registruoti būseną įtraukiamas į atsargų koregavimo objektą ir į atsargų perkėlimo objektą.</span><span class="sxs-lookup"><span data-stu-id="ff44f-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="ff44f-132">Šis laukas naudojamas kaip filtras siunčiant koregavimą ar perkėlimą į „Operations“.</span><span class="sxs-lookup"><span data-stu-id="ff44f-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="ff44f-133">Numatytasis laukas nustatomas į Sukurta (1) – tokiu atveju į „Operations“ nesiunčiama.</span><span class="sxs-lookup"><span data-stu-id="ff44f-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="ff44f-134">Kai keičiate į Užregistruota (2), siunčiama operacijoms, tačiau tada nebegalėsite atlikti jokių koregavimo ar perkėlimo keitimų arba į juos įtraukti naujų eilučių.</span><span class="sxs-lookup"><span data-stu-id="ff44f-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="ff44f-135">Numeracijos laukas įtrauktas į atsargų koregavimo produkto objektą.</span><span class="sxs-lookup"><span data-stu-id="ff44f-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="ff44f-136">Šis laukas padeda integravimui turėti unikalų numerį, todėl žinoma, kada kurti ir kada naujinti.</span><span class="sxs-lookup"><span data-stu-id="ff44f-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="ff44f-137">Kuriant pirmąjį atsargų koregavimo produktą, sukuriamas naujas įrašas P2C automatinės numeracijos objekte, kad būtų palaikoma numerių serija ir naudojamas prefiksas.</span><span class="sxs-lookup"><span data-stu-id="ff44f-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ff44f-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="ff44f-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="ff44f-139">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="ff44f-139">In Finance and Operations</span></span>
<span data-ttu-id="ff44f-140">Integravimo sugeneruotus integravimo atsargų žurnalus galima automatiškai registruoti naudojant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="ff44f-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="ff44f-141">Tai įgalinama iš: Atsargų valdymas > Periodinės užduotys > CDS integravimas > Registruoti integravimo atsargų žurnalus</span><span class="sxs-lookup"><span data-stu-id="ff44f-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ff44f-142">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-142">Template mapping in Data integration</span></span>

<span data-ttu-id="ff44f-143">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="ff44f-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="ff44f-144">Atsargų koregavimas („Field Service“ su „Finance and Operations“): atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="ff44f-145">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="ff44f-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="ff44f-146">Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“): atsargų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="ff44f-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="ff44f-147">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="ff44f-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

