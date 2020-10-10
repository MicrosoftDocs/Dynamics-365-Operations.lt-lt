---
title: Priežiūros užklausos
description: Šioje temoje apžvelgiama, kaip valdyti priežiūros užklausas modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7038269c66092367a0faf147766cb45eb5364e1b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890134"
---
# <a name="maintenance-requests"></a><span data-ttu-id="2c29a-103">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="2c29a-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2c29a-104">Priežiūros užklausos yra pranešimai arba deklaracijos, sukurtos siekiant pranešti vadovui arba planuotojui, kad gali prireikti atlikti turto priežiūros arba remonto užduotį, nesukuriant darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="2c29a-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="2c29a-105">Jei priežiūros užklausos turinys laikomas tinkamu, remiantis priežiūros užklausa galima sukurti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="2c29a-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="2c29a-106">Modulyje Turto valdymas galima kurti bet kurio turto priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="2c29a-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="2c29a-107">Atsižvelgiant į tai, kaip jūsų įmonėje naudojamos priežiūros užklausos, galima kurti įvairių tipų priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="2c29a-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="2c29a-108">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="2c29a-108">Here are some examples:</span></span>

- <span data-ttu-id="2c29a-109">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="2c29a-109">Maintenance requests</span></span>
- <span data-ttu-id="2c29a-110">Pastabos</span><span class="sxs-lookup"><span data-stu-id="2c29a-110">Notes</span></span>
- <span data-ttu-id="2c29a-111">Taisymai arba patobulinimai</span><span class="sxs-lookup"><span data-stu-id="2c29a-111">Corrections or enhancements</span></span>
- <span data-ttu-id="2c29a-112">Investicijos</span><span class="sxs-lookup"><span data-stu-id="2c29a-112">Investments</span></span>
- <span data-ttu-id="2c29a-113">Sandėlio remontas (Šis tipas naudojamas, kai gaunate turtą iš kitos vietos, kad galėtumėte atlikti priežiūros arba remonto užduotį, ir paskui atlikę užduotį turtą grąžinate.)</span><span class="sxs-lookup"><span data-stu-id="2c29a-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="2c29a-114">Priežiūros užklausų peržiūra</span><span class="sxs-lookup"><span data-stu-id="2c29a-114">View maintenance requests</span></span>

<span data-ttu-id="2c29a-115">Norėdami peržiūrėti priežiūros užklausas, pasirinkite **Turto valdymas** \> **Dažnas** \> **Techninės priežiūros prašymai** \> **Visos priežiūros užklausos**, **Aktyvios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="2c29a-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="2c29a-116">Kiekviename sąrašo puslapyje pateikiama dalis informacijos, susijusios su priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="2c29a-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Peržiūrėti priežiūros užklausas](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="2c29a-118">Sąrašo puslapyje **Mano funkcinės vietos priežiūros užklausos** galite peržiūrėti priežiūros užklausų, kuriose yra funkcinių vietų, su kuriomis esate susijęs kaip darbuotojas, arba turto, įdiegto funkcinėse vietose, su kuriomis esate susijęs kaip darbuotojas, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="2c29a-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="2c29a-119">(Informacijos apie tai, kaip nustatyti funkcines vietas priežiūros darbuotojams, rasite skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="2c29a-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="2c29a-120">Nors kliento abonemento informacija pasiekiama Turto tarnybos valdyme (išorinė priežiūra), ji nepasiekiama modulyje Turto valdymas (vidinė priežiūra).</span><span class="sxs-lookup"><span data-stu-id="2c29a-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="2c29a-121">Norėdami atidaryti įrašo išsamios informacijos rodinį, sąrašo puslapio **Visos priežiūros užklausos** tinklelio rodinyje pasirinkite saitą stulpelyje **Priežiūros užklausa**.</span><span class="sxs-lookup"><span data-stu-id="2c29a-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Peržiūrėti priežiūros užklausos informaciją](media/02-manage-maintenance-requests.png)

<span data-ttu-id="2c29a-123">Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="2c29a-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="2c29a-124">Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.</span><span class="sxs-lookup"><span data-stu-id="2c29a-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="2c29a-125">Mygtuko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="2c29a-125">Button name</span></span>                      | <span data-ttu-id="2c29a-126">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="2c29a-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="2c29a-127">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="2c29a-127">Edit</span></span>                             | <span data-ttu-id="2c29a-128">Redaguojama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="2c29a-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-129">Naujos</span><span class="sxs-lookup"><span data-stu-id="2c29a-129">New</span></span>                              | <span data-ttu-id="2c29a-130">Sukuriama nauja priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="2c29a-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="2c29a-131">Naikinti</span><span class="sxs-lookup"><span data-stu-id="2c29a-131">Delete</span></span>                           | <span data-ttu-id="2c29a-132">Naikinama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="2c29a-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-133">Darbo užsakymų telkinys</span><span class="sxs-lookup"><span data-stu-id="2c29a-133">Work order pool</span></span>                  | <span data-ttu-id="2c29a-134">Pasirinkta priežiūros užklausa prijungiama prie darbo užsakymų telkinio.</span><span class="sxs-lookup"><span data-stu-id="2c29a-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="2c29a-135">Darbo užsakymas</span><span class="sxs-lookup"><span data-stu-id="2c29a-135">Work order</span></span>                       | <span data-ttu-id="2c29a-136">Darbo užsakymas sukuriamas pagal pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="2c29a-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-137">Turto gedimas</span><span class="sxs-lookup"><span data-stu-id="2c29a-137">Asset fault</span></span>                      | <span data-ttu-id="2c29a-138">Spustelėjus **Turto gedimai**, galima sukurti pasirinktos priežiūros užklausos gedimo registravimą.</span><span class="sxs-lookup"><span data-stu-id="2c29a-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-139">Darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="2c29a-139">Work orders</span></span>                      | <span data-ttu-id="2c29a-140">Rodomas visų darbo užsakymų, kurie yra susiję su pasirinkta priežiūros užklausa, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="2c29a-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-141">Atnaujinti priežiūros užklausos būseną</span><span class="sxs-lookup"><span data-stu-id="2c29a-141">Update maintenance request state</span></span> | <span data-ttu-id="2c29a-142">Atnaujinama priežiūros užklausos būsena.</span><span class="sxs-lookup"><span data-stu-id="2c29a-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="2c29a-143">Ciklo būsenų žurnalas</span><span class="sxs-lookup"><span data-stu-id="2c29a-143">Lifecycle state log</span></span>              | <span data-ttu-id="2c29a-144">Pateikiamas žurnalas, kuriame registruojami pasirinktos priežiūros užklausos ciklo būsenos.</span><span class="sxs-lookup"><span data-stu-id="2c29a-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-145">Išsami priežiūros užklausos informacija</span><span class="sxs-lookup"><span data-stu-id="2c29a-145">Maintenance request details</span></span>      | <span data-ttu-id="2c29a-146">Spausdinama ataskaita, kurioje pateikiama išsami informacija apie pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="2c29a-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-147">Siųsti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="2c29a-147">Send loan asset</span></span>                  | <span data-ttu-id="2c29a-148">Pasirenkamas skolintas turtas, kuris turėtų laikinai pakeisti turtą, pasirinktą pasirinktoje priežiūros užklausoje.</span><span class="sxs-lookup"><span data-stu-id="2c29a-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="2c29a-149">Grąžinti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="2c29a-149">Return loan asset</span></span>                | <span data-ttu-id="2c29a-150">Registruojamas skolinto turto grąžinimas.</span><span class="sxs-lookup"><span data-stu-id="2c29a-150">Register the loan asset as returned.</span></span> |

