---
title: "Darbo krūvio pajėgumo planavimas"
description: "Šioje temoje paaiškinama, kaip nustatyti ir planuoti sandėlio darbuotojų arba visą sandėlio darbo krūvio pajėgumą."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: 1b1334dcba7d12f2da301f70e21a08fceb88e2b4
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2018

---

# <a name="schedule-workload-capacity"></a><span data-ttu-id="d254e-103">Darbo krūvio pajėgumo planavimas</span><span class="sxs-lookup"><span data-stu-id="d254e-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d254e-104">Galite planuoti darbo krūvio pajėgumus sandėliuose, taip pat prognozuoti dabartinius ir būsimus darbuotojų darbo krūvius atskiruose sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="d254e-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="d254e-105">Galite prognozuoti viso sandėlio darbo krūvį arba galite prognozuoti darbo krūvį atskirai pagal įeinančio ir išeinančio darbo krūvius.</span><span class="sxs-lookup"><span data-stu-id="d254e-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="d254e-106">Norint prognozuoti darbo krūvį pasirinktuose sandėliuose, turi būti prieinami tų sandėlių bendrojo planavimo duomenys.</span><span class="sxs-lookup"><span data-stu-id="d254e-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="d254e-107">Daugiau informacijos rasite faile [Bendrieji planai](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="d254e-107">For more information, see [Master plans](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="d254e-108">Planuoti ir peržiūrėti darbo krūvius sandėlyje</span><span class="sxs-lookup"><span data-stu-id="d254e-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="d254e-109">Norėdami suplanuoti darbo krūvį sandėliui, galite sukurti darbo krūvio nustatymą vienam ar keliems sandėliams, ir tada susieti darbo krūvio nustatymą su pagrindiniu planu.</span><span class="sxs-lookup"><span data-stu-id="d254e-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="d254e-110">Atlikdami darbo krūvio pajėgumo sąranką galite nustatyti įeinančių ir išeinančių operacijų ribas svoriui arba tūriui.</span><span class="sxs-lookup"><span data-stu-id="d254e-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="d254e-111">Taip pat galite sukurti daugiau nei vieną kiekvieno sandėlio nustatymą, o po to susieti tą nustatymą su atskirais bendraisiais planais.</span><span class="sxs-lookup"><span data-stu-id="d254e-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="d254e-112">Pavyzdžiui, naudodamiesi šiuo metodu galite prisitaikyti prie sezoninių darbo jėgos pokyčių.</span><span class="sxs-lookup"><span data-stu-id="d254e-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="d254e-113">Jei sandėlio darbininkai dirba ir su įeinančio, ir su išeinančio darbo krūvio operacijomis, sandėlio pajėgumų nustatymą galite sukonfigūruoti taip, kad galėtumėte prognozuoti bendrą darbo krūvį.</span><span class="sxs-lookup"><span data-stu-id="d254e-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="d254e-114">Norėdami planuoti ir peržiūrėti sandėlių darbo krūvius, turite atlikti toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="d254e-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="d254e-115">Sukurti darbo krūvio pajėgumų nustatymą ir apibrėžti darbo krūvio pajėgumų ribas viename ar keliuose sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="d254e-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="d254e-116">Susieti darbo krūvio pajėgumų nustatymą su pagrindinį planu, kad sukurtumėte darbo krūvio prognozes ir nurodytumėte, kiek laiko tos prognozės bus taikomos.</span><span class="sxs-lookup"><span data-stu-id="d254e-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="d254e-117">Sukurti darbo krūvio pajėgumų nustatymą sandėliui</span><span class="sxs-lookup"><span data-stu-id="d254e-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="d254e-118">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Sandėlio stebėjimas** \> **Darbo krūvio pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="d254e-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="d254e-119">Veiksmų srityje pasirinkę **Nauja** sukurkite darbo krūvio pajėgumų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="d254e-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="d254e-120">„FastTab“ skirtuke **Sandėliai** pasirinkite **Naujas**, po to eilutėje įveskite reikšmes, kad susietumėte sandėlį su darbo krūvio pajėgumų nustatymu.</span><span class="sxs-lookup"><span data-stu-id="d254e-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="d254e-121">Jei ataskaitoje **Darbo krūvio pajėgumas** viename rodinyje turėtų būti rodomos įeinančios ir išeinančios operacijos, pažymėkite žymės langelį **Bendras gaunamas ir siunčiamas darbo krūvis**.</span><span class="sxs-lookup"><span data-stu-id="d254e-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="d254e-122">„FastTab“ skirtuke **Operacijų tipai** pasirinkite įeinančių ir išeinančių operacijų tipus, kuriems bus taikomos darbo krūvio ribos.</span><span class="sxs-lookup"><span data-stu-id="d254e-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d254e-123">Turite pasirinkti bent vieną įeinančio ir išeinančio darbo krūvio operacijos tipą.</span><span class="sxs-lookup"><span data-stu-id="d254e-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="d254e-124">Nustatykite tūrio ir svorio ribas</span><span class="sxs-lookup"><span data-stu-id="d254e-124">Define limits for volume or weight</span></span>

<span data-ttu-id="d254e-125">Galite nustatyti tūrio ar svorio ribas, priklausomai nuo to, koks apribojimas taikomas sandėlio darbo jėgai.</span><span class="sxs-lookup"><span data-stu-id="d254e-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="d254e-126">Apribojimai, kuriuos nurodote, yra įtraukti į darbo krūvio pajėgumų prognozę, kurią galite peržiūrėti ataskaitoje **Darbo krūvio pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="d254e-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="d254e-127">Norint prognozuoti informaciją apie prekių tūrį ir svorį, visiems produktams turi būti nurodytas standartinis atsargų prekės tūris ir vienos atsargų prekės svoris.</span><span class="sxs-lookup"><span data-stu-id="d254e-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="d254e-128">Reikiamus laukus galima rasti toliau nurodytose puslapio **Patvirtinto produkto informacija** „FastTab“ skirtuko **Atsargų tvarkymas** laukų grupėse.</span><span class="sxs-lookup"><span data-stu-id="d254e-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="d254e-129">Tvarkymas</span><span class="sxs-lookup"><span data-stu-id="d254e-129">Handling</span></span>
- <span data-ttu-id="d254e-130">Faktinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="d254e-130">Physical dimensions</span></span>
- <span data-ttu-id="d254e-131">Svorio matavimai</span><span class="sxs-lookup"><span data-stu-id="d254e-131">Weight measurements</span></span>

<span data-ttu-id="d254e-132">Jei nurodyta klaidinga informacija, kurdami ataskaitą **Darbo krūvio pajėgumas** gausite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="d254e-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="d254e-133">Tada ataskaitoje galėsite įsigilinti į informaciją ir nustatyti, kokios informacijos trūksta norint prognozuoti būsimą darbo krūvį.</span><span class="sxs-lookup"><span data-stu-id="d254e-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="d254e-134">Susieti darbo krūvio pajėgumų nustatymą su bendruoju planu</span><span class="sxs-lookup"><span data-stu-id="d254e-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="d254e-135">Pasirinkite **Atsargų valdymas** \> **Periodinis** \> **Darbo krūvio planavimas**.</span><span class="sxs-lookup"><span data-stu-id="d254e-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="d254e-136">Lauke **Bendrasis planas** pasirinkite bendrąjį planą, kurį norite naudoti prognozuodami darbo krūvį.</span><span class="sxs-lookup"><span data-stu-id="d254e-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="d254e-137">Lauke **Dienų skaičius** nurodykite dienų, kurioms parengta darbo krūvio prognozė, skaičių.</span><span class="sxs-lookup"><span data-stu-id="d254e-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="d254e-138">Lauke **Darbo krūvis** pasirinkite darbo krūvio nustatymą, kurį norite susieti su bendruoju planu.</span><span class="sxs-lookup"><span data-stu-id="d254e-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="d254e-139">Peržiūrėti darbo krūvio pajėgumus</span><span class="sxs-lookup"><span data-stu-id="d254e-139">View workload capacity</span></span>

1. <span data-ttu-id="d254e-140">Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Fizinės atsargų ataskaitos** \> **Darbo krūvio pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="d254e-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="d254e-141">Lauke **Stulpelių skaičius** nurodykite ataskaitoje rodomų stulpelių skaičių.</span><span class="sxs-lookup"><span data-stu-id="d254e-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="d254e-142">Lauke **Užsakymo tipas** pasirinkę **Suplanuotas ir patvirtintas**, **Suplanuotas** arba **Patvirtintas** nurodykite užsakymų tipą, kurio prognozės pateikiamos ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="d254e-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="d254e-143">Lauke **Load type** pasirinkę apkrovos tipą nurodykite, ar turėtų būti prognozuojami tūrio ar svorio darbo krūvio pajėgumai.</span><span class="sxs-lookup"><span data-stu-id="d254e-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="d254e-144">Lauke **Darbo krūvio pajėgumas** pasirinkite darbo krūvio pajėgumų nustatymą.</span><span class="sxs-lookup"><span data-stu-id="d254e-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>

