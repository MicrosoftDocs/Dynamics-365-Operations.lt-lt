---
title: Priežiūros grafikas
description: Šioje temoje aiškinama apie priežiūros grafikus skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d235a3797b1acee9c92c3d81e8b4a20e1f7c5c75
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017964"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="596ce-103">Priežiūros grafikas</span><span class="sxs-lookup"><span data-stu-id="596ce-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="596ce-104">Priežiūros grafike pateikiamas sąrašas visų numatomų prevencinių priežiūros planų, priežiūros užklausų ir atliktinų priežiūros ciklų. Kai kurios grafiko eilutės gali būti konvertuotos į darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="596ce-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="596ce-105">Keturi priežiūros grafiko rodiniai truputį skiriasi, priklausomai nuo priežiūros grafiko eilučių, kurias norite matyti.</span><span class="sxs-lookup"><span data-stu-id="596ce-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="596ce-106">Meniu elementas</span><span class="sxs-lookup"><span data-stu-id="596ce-106">Menu item</span></span>                  | <span data-ttu-id="596ce-107">Turinio aprašas</span><span class="sxs-lookup"><span data-stu-id="596ce-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="596ce-108">Visas priežiūros grafikas</span><span class="sxs-lookup"><span data-stu-id="596ce-108">All maintenance schedule</span></span>       | <span data-ttu-id="596ce-109">Visos priežiūros grafiko eilutės yra rodomos.</span><span class="sxs-lookup"><span data-stu-id="596ce-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="596ce-110">Mano turto grafikas</span><span class="sxs-lookup"><span data-stu-id="596ce-110">My asset schedule</span></span>        | <span data-ttu-id="596ce-111">Visos priežiūros grafiko eilutės, kuriose pateikiamas įdiegtas turtas funkcinei vietai, kurioje jūs dirbate kaip darbuotojas (sąranką žr. [Priežiūros darbuotojai ir darbo grupės](../setup-for-objects/workers-and-worker-groups.md)), rodomos sąraše.</span><span class="sxs-lookup"><span data-stu-id="596ce-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="596ce-112">Atidaryti priežiūros grafiko eilutes</span><span class="sxs-lookup"><span data-stu-id="596ce-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="596ce-113">Priežiūros grafiko eilutės, turinčios būseną „Sukurta“, rodomos šiame sąraše – jos dar nebuvo konvertuotos į darbo užsakymą arba panaikintos.</span><span class="sxs-lookup"><span data-stu-id="596ce-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="596ce-114">Atidaryti priežiūros grafiko telkinius</span><span class="sxs-lookup"><span data-stu-id="596ce-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="596ce-115">Šiame sąraše rodomos priežiūros grafiko eilutės, susijusios su darbo užsakymo telkiniu.</span><span class="sxs-lookup"><span data-stu-id="596ce-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="596ce-116">Jei priežiūros grafiko eilutė įtraukiama keliuose darbo užsakymų telkiniuose (žr. [Darbo užsakymų telkiniai](../work-orders/work-order-pools.md)), kiekvienam telkiniui skiltyje **Atidaryti priežiūros grafiko telkinius** rodomas vienas įrašas.</span><span class="sxs-lookup"><span data-stu-id="596ce-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="596ce-117">Taip siekiama optimizuoti darbo užsakymų telkinių filtravimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="596ce-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="596ce-118">Norėdami atidaryti priežiūros grafiką:</span><span class="sxs-lookup"><span data-stu-id="596ce-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="596ce-119">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros grafikas** > **Visi priežiūros grafikai** arba **Atidaryti priežiūros grafiko eilutes**, arba **Atidaryti priežiūros grafiko telkinius**.</span><span class="sxs-lookup"><span data-stu-id="596ce-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="596ce-120">Kad atnaujintumėte priežiūros grafiką, spustelėkite **Priežiūros planas** arba **Priežiūros ciklai**.</span><span class="sxs-lookup"><span data-stu-id="596ce-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="596ce-121">Galite redaguoti priežiūros grafiko eilutę ją pasirinkę ir spustelėję **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="596ce-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="596ce-122">Pavyzdžiui, galite lengvai atnaujinti aptarnavimo lygį arba už darbą atsakingą darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="596ce-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="596ce-123">Galite redaguoti tik tas priežiūros grafiko eilutes, kurios dar nebuvo susietos su darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="596ce-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="596ce-124">Galite panaikinti priežiūros grafiko eilutę ją pasirinkę sąrašo puslapyje ir spustelėję **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="596ce-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="596ce-125">Galite atsisakyti priežiūros grafiko eilutės ją pasirinkę sąrašo puslapyje ir spustelėję **Atsisakyti**.</span><span class="sxs-lookup"><span data-stu-id="596ce-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="596ce-126">Ši funkcija naudinga, pavyzdžiui, kai turtui numatytas 2 000 km priežiūros planas ir 10 000 km priežiūros planas.</span><span class="sxs-lookup"><span data-stu-id="596ce-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="596ce-127">Tokiu atveju, greičiausiai norėsite atsisakyti sukurtos eilutės iš 2 000 km priežiūros plano, kai ji sutaps su 10 000 km, 20 000 km, 30 000 km ir t. t.</span><span class="sxs-lookup"><span data-stu-id="596ce-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="596ce-128">Jei atsisakysite priežiūros plano eilutės, susijusios su priežiūros planu, tos eilutės daugiau nebematysite, kai planuosite tą priežiūros planą.</span><span class="sxs-lookup"><span data-stu-id="596ce-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="596ce-129">Galite pasirinkti kelias priežiūros grafiko skiltyje **Visi priežiūros grafikai** ir spustelėti **Darbo užsakymų telkinys**, jei norite įtraukti į tą patį darbo užsakymų telkinį visas pažymėtas eilutes.</span><span class="sxs-lookup"><span data-stu-id="596ce-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="596ce-130">Galite pasirinkti kelias priežiūros grafiko eilutes skiltyje **Visi priežiūros grafikai** arba **Atidaryti priežiūros grafiko eilutes**, arba **Atidaryti priežiūros grafikų telkinius** ir spustelėti **Koreguoti grafiką**, jei norite taikyti tas pačias korekcijas kelioms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="596ce-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="596ce-131">Galite keisti numatomas pradžios ir pabaigos datas, aptarnavimo lygį ir atsakingą priežiūros darbo grupę arba atsakingą priežiūros darbuotoją, susijusius su pasirinktomis priežiūros grafiko eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="596ce-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="596ce-132">Kai priežiūros grafiko eilutė susieta su darbo užsakymu, darbo užsakymo ID bus rodomas lauke **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="596ce-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="596ce-133">Išsamios informacijos rodinyje **Visas turtas** > „FastTab“ **Turto priežiūros planai** galite turtui pasirinkti priežiūros planus.</span><span class="sxs-lookup"><span data-stu-id="596ce-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="596ce-134">Vėliau, jei panaikinsite priežiūros plano eilutę, susijusią su turtu, skiltyje **Visas turtas**, taip pat galėsite automatiškai panaikinti visas priežiūros grafiko eilutes, turinčias būseną „Sukurta“ ir sukurtas pagal priežiūros planą.</span><span class="sxs-lookup"><span data-stu-id="596ce-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="596ce-135">Taip pat žr. [Sukurti turtą](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="596ce-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="596ce-136">Toliau pateiktame paveikslėlyje galite matyti sąrašo puslapį **Visas priežiūros grafikas**.</span><span class="sxs-lookup"><span data-stu-id="596ce-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![1 pav.](media/16-preventive-maintenance.png)

