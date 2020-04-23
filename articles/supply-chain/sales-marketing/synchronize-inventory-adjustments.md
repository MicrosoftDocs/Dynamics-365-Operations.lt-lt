---
title: „Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų koregavimą ir perkėlimą su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204429"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="fb9a1-103">„Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su Tiekimo grandinės valdymu</span><span class="sxs-lookup"><span data-stu-id="fb9a1-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fb9a1-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų koregavimą ir perkėlimą su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="fb9a1-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="fb9a1-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fb9a1-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="fb9a1-106">Templates and tasks</span></span>
<span data-ttu-id="fb9a1-107">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Field Service“ atsargų koregavimą ir perkėlimą su Tiekimo grandinės valdymu.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="fb9a1-108">**Šablonai naudojant funkcija Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="fb9a1-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="fb9a1-109">Atsargų koregavimas (iš „Field Service“ į Tiekimo grandinės valdymą)</span><span class="sxs-lookup"><span data-stu-id="fb9a1-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="fb9a1-110">Atsargų perkėlimas (iš „Field Service“ į Tiekimo grandinės valdymą)</span><span class="sxs-lookup"><span data-stu-id="fb9a1-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="fb9a1-111">**Užduotys duomenų integravimo projektuose**</span><span class="sxs-lookup"><span data-stu-id="fb9a1-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="fb9a1-112">Atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-112">Inventory Adjustments</span></span>
- <span data-ttu-id="fb9a1-113">Atsargų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="fb9a1-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="fb9a1-114">Entity set</span></span>
| <span data-ttu-id="fb9a1-115">„Field Service“</span><span class="sxs-lookup"><span data-stu-id="fb9a1-115">Field Service</span></span>                     | <span data-ttu-id="fb9a1-116">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="fb9a1-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fb9a1-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="fb9a1-118">CDS atsargų koregavimo žurnalo antraštės ir eilutės</span><span class="sxs-lookup"><span data-stu-id="fb9a1-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="fb9a1-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="fb9a1-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="fb9a1-120">CDS atsargų perkėlimo žurnalo antraštės ir eilutės</span><span class="sxs-lookup"><span data-stu-id="fb9a1-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="fb9a1-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-121">Entity flow</span></span>
<span data-ttu-id="fb9a1-122">„Field Service“ atliktas atsargų koregavimas ir perkėlimas sinchronizuojamas su Tiekimo grandinės valdymu, kai **Registruoti būseną** pasikeičia iš **Sukurta** į **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="fb9a1-123">Tokiu atveju koregavimo arba perkėlimo užsakymas užrakinamas ir tampa tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="fb9a1-124">Tai reiškia, kad koregavimas ir perkėlimas gali būti registruojami Tiekimo grandinės valdyme, bet jų modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="fb9a1-125">Tiekimo grandinės valdyme galite nustatyti paketinę užduotį automatiškai registruoti koregavimą ir perkelti atsargų žurnalus, sugeneruotus atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="fb9a1-126">Išsamesnės būtinos informacijos apie tai, kaip įgalinti paketinę užduotį, žr. toliau.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="fb9a1-127">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-127">Field Service CRM solution</span></span> 
<span data-ttu-id="fb9a1-128">Laukas **Atsargų vienetas** įtrauktas į objektą **Produktas**.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="fb9a1-129">Šis laukas reikalingas, nes pardavimo ir atsargų vienetas Tiekimo grandinės valdyme ne visada yra tas pats, o atsargų vienetas reikalingas naudojant sandėlio atsargas Tiekimo grandinės valdyme.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="fb9a1-130">Nustatant į atsargų koregavimo produktą įtrauktą produktą, skirtą atsargų koregavimui ir atsargų perkėlimui, vieneto bus ieškoma pagal produktų atsargų produkto reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="fb9a1-131">Jei nustatoma vertė, atsargų koregavimo produkto laukas **Vienetas** užrakinamas.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="fb9a1-132">Laukas **Registruoti būseną** įtraukiamas į objektą **Atsargų koregavimas** ir į objektą **Atsargų perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="fb9a1-133">Šis laukas naudojamas kaip filtras siunčiant koregavimą ar perkėlimą į Tiekimo grandinės valdymą.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="fb9a1-134">Numatytoji šio lauko reikšmė yra Sukurta (1), tačiau ji nėra siunčiama į Tiekimo grandinės valdymą.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="fb9a1-135">Kai atnaujinate reikšmę į Užregistruota (2), ji siunčiama į Tiekimo grandinės valdymą, tačiau po to nebegalėsite atlikti jokių koregavimo ar perkėlimo keitimų arba įtraukti naujų eilučių.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="fb9a1-136">Laukas **Numeracija** įtrauktas į objektą **Atsargų koregavimo produktas**.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="fb9a1-137">Šis laukas užtikrina, kad integravimui būtų priskirtas unikalus numeris ir integravimas galėtų kurti bei atnaujinti koregavimą.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="fb9a1-138">Kuriant pirmąjį atsargų koregavimo produktą, sukuriamas naujas įrašas objekte **P2C automatinė numeracija**, kad būtų palaikoma numerių serija ir naudojamas prefiksas.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="fb9a1-139">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="fb9a1-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="fb9a1-140">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-140">Supply Chain Management</span></span>
<span data-ttu-id="fb9a1-141">Integravimo sugeneruotus integravimo atsargų žurnalus galima automatiškai registruoti naudojant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="fb9a1-142">Tai įgalinama iš: **Atsargų valdymas > Periodinės užduotys > CDS integravimas > Registruoti integravimo atsargų žurnalus**.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fb9a1-143">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-143">Template mapping in Data integration</span></span>

<span data-ttu-id="fb9a1-144">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="fb9a1-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="fb9a1-145">Atsargų koregavimas (iš „Field Service“ į Tiekimo grandinės valdymą): atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="fb9a1-146">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="fb9a1-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="fb9a1-147">Atsargų perkėlimas (iš „Field Service“ į Tiekimo grandinės valdymą): atsargų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="fb9a1-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="fb9a1-148">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="fb9a1-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
