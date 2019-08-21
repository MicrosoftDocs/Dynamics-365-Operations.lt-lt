---
title: Priežiūros užklausos
description: Šioje temoje apžvelgiama, kaip valdyti priežiūros užklausas modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847441"
---
# <a name="maintenance-requests"></a><span data-ttu-id="433dc-103">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="433dc-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="433dc-104">Priežiūros užklausos yra pranešimai arba deklaracijos, sukurtos siekiant pranešti vadovui arba planuotojui, kad gali prireikti atlikti turto priežiūros arba remonto užduotį, nesukuriant darbo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="433dc-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="433dc-105">Jei priežiūros užklausos turinys laikomas tinkamu, remiantis priežiūros užklausa galima sukurti darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="433dc-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="433dc-106">Modulyje Turto valdymas galima kurti bet kurio turto priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="433dc-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="433dc-107">Atsižvelgiant į tai, kaip jūsų įmonėje naudojamos priežiūros užklausos, galima kurti įvairių tipų priežiūros užklausas.</span><span class="sxs-lookup"><span data-stu-id="433dc-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="433dc-108">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="433dc-108">Here are some examples:</span></span>

- <span data-ttu-id="433dc-109">Priežiūros užklausos</span><span class="sxs-lookup"><span data-stu-id="433dc-109">Maintenance requests</span></span>
- <span data-ttu-id="433dc-110">Pastabos</span><span class="sxs-lookup"><span data-stu-id="433dc-110">Notes</span></span>
- <span data-ttu-id="433dc-111">Taisymai arba patobulinimai</span><span class="sxs-lookup"><span data-stu-id="433dc-111">Corrections or enhancements</span></span>
- <span data-ttu-id="433dc-112">Investicijos</span><span class="sxs-lookup"><span data-stu-id="433dc-112">Investments</span></span>
- <span data-ttu-id="433dc-113">Sandėlio remontas (Šis tipas naudojamas, kai gaunate turtą iš kitos vietos, kad galėtumėte atlikti priežiūros arba remonto užduotį, ir paskui atlikę užduotį turtą grąžinate.)</span><span class="sxs-lookup"><span data-stu-id="433dc-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="433dc-114">Priežiūros užklausų peržiūra</span><span class="sxs-lookup"><span data-stu-id="433dc-114">View maintenance requests</span></span>

<span data-ttu-id="433dc-115">Norėdami peržiūrėti priežiūros užklausas, pasirinkite **Turto valdymas** \> **Dažnas** \> **Techninės priežiūros prašymai** \> **Visos priežiūros užklausos**, **Aktyvios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="433dc-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="433dc-116">Kiekviename sąrašo puslapyje pateikiama dalis informacijos, susijusios su priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="433dc-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![1 paveikslėlis](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="433dc-118">Sąrašo puslapyje **Mano funkcinės vietos priežiūros užklausos** galite peržiūrėti priežiūros užklausų, kuriose yra funkcinių vietų, su kuriomis esate susijęs kaip darbuotojas, arba turto, įdiegto funkcinėse vietose, su kuriomis esate susijęs kaip darbuotojas, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="433dc-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="433dc-119">(Informacijos apie tai, kaip nustatyti funkcines vietas priežiūros darbuotojams, rasite skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="433dc-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="433dc-120">Nors kliento abonemento informacija pasiekiama Turto tarnybos valdyme (išorinė priežiūra), ji nepasiekiama modulyje Turto valdymas (vidinė priežiūra).</span><span class="sxs-lookup"><span data-stu-id="433dc-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="433dc-121">Norėdami atidaryti įrašo išsamios informacijos rodinį, sąrašo puslapio **Visos priežiūros užklausos** tinklelio rodinyje pasirinkite saitą stulpelyje **Priežiūros užklausa**.</span><span class="sxs-lookup"><span data-stu-id="433dc-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![2 paveikslėlis](media/02-manage-maintenance-requests.png)

<span data-ttu-id="433dc-123">Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose.</span><span class="sxs-lookup"><span data-stu-id="433dc-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="433dc-124">Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.</span><span class="sxs-lookup"><span data-stu-id="433dc-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="433dc-125">Mygtuko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="433dc-125">Button name</span></span>                      | <span data-ttu-id="433dc-126">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="433dc-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="433dc-127">Redagavimas</span><span class="sxs-lookup"><span data-stu-id="433dc-127">Edit</span></span>                             | <span data-ttu-id="433dc-128">Redaguojama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="433dc-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-129">Naujos</span><span class="sxs-lookup"><span data-stu-id="433dc-129">New</span></span>                              | <span data-ttu-id="433dc-130">Sukuriama nauja priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="433dc-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="433dc-131">Naikinti</span><span class="sxs-lookup"><span data-stu-id="433dc-131">Delete</span></span>                           | <span data-ttu-id="433dc-132">Naikinama pasirinkta priežiūros užklausa.</span><span class="sxs-lookup"><span data-stu-id="433dc-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-133">Darbo užsakymų telkinys</span><span class="sxs-lookup"><span data-stu-id="433dc-133">Work order pool</span></span>                  | <span data-ttu-id="433dc-134">Pasirinkta priežiūros užklausa prijungiama prie darbo užsakymų telkinio.</span><span class="sxs-lookup"><span data-stu-id="433dc-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="433dc-135">Darbo užsakymas</span><span class="sxs-lookup"><span data-stu-id="433dc-135">Work order</span></span>                       | <span data-ttu-id="433dc-136">Darbo užsakymas sukuriamas pagal pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="433dc-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-137">Turto gedimas</span><span class="sxs-lookup"><span data-stu-id="433dc-137">Asset fault</span></span>                      | <span data-ttu-id="433dc-138">Spustelėjus **Turto gedimai**, galima sukurti pasirinktos priežiūros užklausos gedimo registravimą.</span><span class="sxs-lookup"><span data-stu-id="433dc-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-139">Darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="433dc-139">Work orders</span></span>                      | <span data-ttu-id="433dc-140">Rodomas visų darbo užsakymų, kurie yra susiję su pasirinkta priežiūros užklausa, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="433dc-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-141">Atnaujinti priežiūros užklausos būseną</span><span class="sxs-lookup"><span data-stu-id="433dc-141">Update maintenance request state</span></span> | <span data-ttu-id="433dc-142">Atnaujinama priežiūros užklausos būsena.</span><span class="sxs-lookup"><span data-stu-id="433dc-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="433dc-143">Ciklo būsenų žurnalas</span><span class="sxs-lookup"><span data-stu-id="433dc-143">Lifecycle state log</span></span>              | <span data-ttu-id="433dc-144">Pateikiamas žurnalas, kuriame registruojami pasirinktos priežiūros užklausos ciklo būsenos.</span><span class="sxs-lookup"><span data-stu-id="433dc-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-145">Išsami priežiūros užklausos informacija</span><span class="sxs-lookup"><span data-stu-id="433dc-145">Maintenance request details</span></span>      | <span data-ttu-id="433dc-146">Spausdinama ataskaita, kurioje pateikiama išsami informacija apie pasirinktą priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="433dc-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-147">Siųsti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="433dc-147">Send loan asset</span></span>                  | <span data-ttu-id="433dc-148">Pasirenkamas skolintas turtas, kuris turėtų laikinai pakeisti turtą, pasirinktą pasirinktoje priežiūros užklausoje.</span><span class="sxs-lookup"><span data-stu-id="433dc-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="433dc-149">Grąžinti skolintą turtą</span><span class="sxs-lookup"><span data-stu-id="433dc-149">Return loan asset</span></span>                | <span data-ttu-id="433dc-150">Registruojamas skolinto turto grąžinimas.</span><span class="sxs-lookup"><span data-stu-id="433dc-150">Register the loan asset as returned.</span></span> |

