---
title: Priežiūros užklausos
description: Šioje temoje apžvelgiama, kaip valdyti priežiūros užklausas modulyje Turto valdymas.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c72a16b8f3865129ad737c511e50eb34c9f2e91
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015883"
---
# <a name="maintenance-requests"></a><span data-ttu-id="c1845-103">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="c1845-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1845-104">Priežiūros užklausos yra pranešimai arba deklaracijos, sukurtos siekiant pranešti vadovui arba planuotojui, kad gali prireikti atlikti turto priežiūros arba remonto užduotį, nesukuriant darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="c1845-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="c1845-105">Jei priežiūros užklausos turinys laikomas tinkamu, remiantis priežiūros užklausa galima sukurti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c1845-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="c1845-106">Modulyje Turto valdymas galima kurti bet kurio turto priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="c1845-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="c1845-107">Atsižvelgiant į tai, kaip jūsų įmonėje naudojamos priežiūros užklausos, galima kurti įvairių tipų priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="c1845-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="c1845-108">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="c1845-108">Here are some examples:</span></span>

- <span data-ttu-id="c1845-109">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="c1845-109">Maintenance requests</span></span>
- <span data-ttu-id="c1845-110">Pastabos</span><span class="sxs-lookup"><span data-stu-id="c1845-110">Notes</span></span>
- <span data-ttu-id="c1845-111">Taisymai arba patobulinimai</span><span class="sxs-lookup"><span data-stu-id="c1845-111">Corrections or enhancements</span></span>
- <span data-ttu-id="c1845-112">Investicijos</span><span class="sxs-lookup"><span data-stu-id="c1845-112">Investments</span></span>
- <span data-ttu-id="c1845-113">Sandėlio remontas (Šis tipas naudojamas, kai gaunate turtą iš kitos vietos, kad galėtumėte atlikti priežiūros arba remonto užduotį, ir paskui atlikę užduotį turtą grąžinate.)</span><span class="sxs-lookup"><span data-stu-id="c1845-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="c1845-114">Priežiūros užklausų peržiūra</span><span class="sxs-lookup"><span data-stu-id="c1845-114">View maintenance requests</span></span>

<span data-ttu-id="c1845-115">Norėdami peržiūrėti priežiūros užklausas, pasirinkite **Turto valdymas** \> **Dažnas** \> **Techninės priežiūros prašymai** \> **Visos priežiūros užklausos**, **Aktyvios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="c1845-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="c1845-116">Kiekviename sąrašo puslapyje pateikiama dalis informacijos, susijusios su priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="c1845-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Peržiūrėti priežiūros užklausas](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="c1845-118">Sąrašo puslapyje **Mano funkcinės vietos priežiūros užklausos** galite peržiūrėti priežiūros užklausų, kuriose yra funkcinių vietų, su kuriomis esate susijęs kaip darbuotojas, arba turto, įdiegto funkcinėse vietose, su kuriomis esate susijęs kaip darbuotojas, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c1845-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="c1845-119">(Informacijos apie tai, kaip nustatyti funkcines vietas priežiūros darbuotojams, rasite skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="c1845-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="c1845-120">Nors kliento abonemento informacija pasiekiama Turto tarnybos valdyme (išorinė priežiūra), ji nepasiekiama modulyje Turto valdymas (vidinė priežiūra).</span><span class="sxs-lookup"><span data-stu-id="c1845-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="c1845-121">Norėdami atidaryti įrašo išsamios informacijos rodinį, sąrašo puslapio **Visos priežiūros užklausos** tinklelio rodinyje pasirinkite saitą stulpelyje **Priežiūros užklausa**.</span><span class="sxs-lookup"><span data-stu-id="c1845-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Peržiūrėti priežiūros užklausos informaciją](media/02-manage-maintenance-requests.png)

<span data-ttu-id="c1845-123">Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="c1845-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="c1845-124">Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.</span><span class="sxs-lookup"><span data-stu-id="c1845-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="c1845-125">Mygtuko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c1845-125">Button name</span></span>                      | <span data-ttu-id="c1845-126">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c1845-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="c1845-127">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="c1845-127">Edit</span></span>                             | <span data-ttu-id="c1845-128">Redaguojama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="c1845-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-129">Naujos</span><span class="sxs-lookup"><span data-stu-id="c1845-129">New</span></span>                              | <span data-ttu-id="c1845-130">Sukuriama nauja priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="c1845-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="c1845-131">Naikinti</span><span class="sxs-lookup"><span data-stu-id="c1845-131">Delete</span></span>                           | <span data-ttu-id="c1845-132">Naikinama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="c1845-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-133">Darbo užsakymų telkinys</span><span class="sxs-lookup"><span data-stu-id="c1845-133">Work order pool</span></span>                  | <span data-ttu-id="c1845-134">Pasirinkta priežiūros užklausa prijungiama prie darbo užsakymų telkinio.</span><span class="sxs-lookup"><span data-stu-id="c1845-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="c1845-135">Darbo užsakymas</span><span class="sxs-lookup"><span data-stu-id="c1845-135">Work order</span></span>                       | <span data-ttu-id="c1845-136">Darbo užsakymas sukuriamas pagal pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="c1845-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-137">Turto gedimas</span><span class="sxs-lookup"><span data-stu-id="c1845-137">Asset fault</span></span>                      | <span data-ttu-id="c1845-138">Spustelėjus **Turto gedimai**, galima sukurti pasirinktos priežiūros užklausos gedimo registravimą.</span><span class="sxs-lookup"><span data-stu-id="c1845-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-139">Darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="c1845-139">Work orders</span></span>                      | <span data-ttu-id="c1845-140">Rodomas visų darbo užsakymų, kurie yra susiję su pasirinkta priežiūros užklausa, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="c1845-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-141">Atnaujinti priežiūros užklausos būseną</span><span class="sxs-lookup"><span data-stu-id="c1845-141">Update maintenance request state</span></span> | <span data-ttu-id="c1845-142">Atnaujinama priežiūros užklausos būsena.</span><span class="sxs-lookup"><span data-stu-id="c1845-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="c1845-143">Ciklo būsenų žurnalas</span><span class="sxs-lookup"><span data-stu-id="c1845-143">Lifecycle state log</span></span>              | <span data-ttu-id="c1845-144">Pateikiamas žurnalas, kuriame registruojami pasirinktos priežiūros užklausos ciklo būsenos.</span><span class="sxs-lookup"><span data-stu-id="c1845-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-145">Išsami priežiūros užklausos informacija</span><span class="sxs-lookup"><span data-stu-id="c1845-145">Maintenance request details</span></span>      | <span data-ttu-id="c1845-146">Spausdinama ataskaita, kurioje pateikiama išsami informacija apie pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="c1845-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-147">Siųsti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="c1845-147">Send loan asset</span></span>                  | <span data-ttu-id="c1845-148">Pasirenkamas skolintas turtas, kuris turėtų laikinai pakeisti turtą, pasirinktą pasirinktoje priežiūros užklausoje.</span><span class="sxs-lookup"><span data-stu-id="c1845-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="c1845-149">Grąžinti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="c1845-149">Return loan asset</span></span>                | <span data-ttu-id="c1845-150">Registruojamas skolinto turto grąžinimas.</span><span class="sxs-lookup"><span data-stu-id="c1845-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]