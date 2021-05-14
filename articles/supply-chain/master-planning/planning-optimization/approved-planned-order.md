---
title: Peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus
description: Šioje temoje pateikiama informacija apie tai, kaip valdyti, peržiūrėti ir patvirtinti suplanuotų užsakymų būseną „Planning Optimization“.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935662"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="80b4e-103">Peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus</span><span class="sxs-lookup"><span data-stu-id="80b4e-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80b4e-104">Šioje temoje pateikiama informacija apie tai, kaip valdyti, peržiūrėti ir patvirtinti suplanuotų užsakymų būseną „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="80b4e-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="80b4e-105">Peržiūrėti ir tvarkyti suplanuotus užsakymus</span><span class="sxs-lookup"><span data-stu-id="80b4e-105">View and manage planned orders</span></span>

<span data-ttu-id="80b4e-106">Galite peržiūrėti ir tvarkyti suplanuotus užsakymus bet kuriame suplanuotų užsakymų sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="80b4e-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="80b4e-107">Pereikite į vieną iš šių vietų, atsižvelgiant į suplanuotų užsakymų, su kuriuos norite dirbti, tipą:</span><span class="sxs-lookup"><span data-stu-id="80b4e-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="80b4e-108">Bendrojo planavimo \> darbo sričių \> bendrasis planavimas</span><span class="sxs-lookup"><span data-stu-id="80b4e-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="80b4e-109">Bendrasis planavimas \> Bendrasis planavimas \> Suplanuoti užsakymai</span><span class="sxs-lookup"><span data-stu-id="80b4e-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="80b4e-110">Eikite į Gamybos kontrolė \> Gamybos užsakymai \> Suplanuoti gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="80b4e-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="80b4e-111">Pasirinkite Įsigijimas ir šaltinio pasirinkimas \> pirkimo užsakymai \> Suplanuoti pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="80b4e-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="80b4e-112">Atsargų valdymas \> Gaunami užsakymai \> Suplanuoti perkėlimai</span><span class="sxs-lookup"><span data-stu-id="80b4e-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="80b4e-113">Atsargų valdymas \> Siunčiami užsakymai \> Suplanuoti perkėlimai</span><span class="sxs-lookup"><span data-stu-id="80b4e-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="80b4e-114">Peržiūrėkite ir redaguoti suplanuotų užsakymų būseną</span><span class="sxs-lookup"><span data-stu-id="80b4e-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="80b4e-115">Galite naudoti kiekvieno **suplanuoto** užsakymo lauką Būsena, kad būtų galima sekti progresą arba pakeisti suplanuoto užsakymo eigą.</span><span class="sxs-lookup"><span data-stu-id="80b4e-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="80b4e-116">Galimos šios **Būsenos** reikšmės:</span><span class="sxs-lookup"><span data-stu-id="80b4e-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="80b4e-117">**Neapdorota** - Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, pagal jų būseną.</span><span class="sxs-lookup"><span data-stu-id="80b4e-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="80b4e-118">Šios būsenos suplanuoti užsakymai bus panaikinti kito planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="80b4e-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="80b4e-119">**Baigta** – ši būsena nurodo, kad suplanuotas užsakymas baigtas.</span><span class="sxs-lookup"><span data-stu-id="80b4e-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="80b4e-120">Jei nenorite patvirtinti suplanuoto užsakymo, galite rankiniu būdu nustatyti būseną *Baigta*.</span><span class="sxs-lookup"><span data-stu-id="80b4e-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="80b4e-121">Atkreipkite dėmesį, kad sistema valdo *Neapdorota* ir *Baigta* būsenas vienodai.</span><span class="sxs-lookup"><span data-stu-id="80b4e-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="80b4e-122">**Patvirtinta** – ši būsena nurodo, kad suplanuotas užsakymas patvirtintas patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="80b4e-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="80b4e-123">Jei norite patvirtinti suplanuotą užsakymą, galite pakeisti būseną į *Patvirtinta*.</span><span class="sxs-lookup"><span data-stu-id="80b4e-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="80b4e-124">Jei norite palikti suplanuoto užsakymo redagavimus arba jei planuojate patvirtinti suplanuotą užsakymą, pakeiskite jo būseną į *Patvirtinta*.</span><span class="sxs-lookup"><span data-stu-id="80b4e-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="80b4e-125">Suplanuoti užsakymai, kurių būsena Yra *Patvirtinta*, bendrojo planavimo metu laikomi fiksuotais ir tikėtinais tiekimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="80b4e-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="80b4e-126">Todėl vėliau vykdant bendrąjį planavimą jos nėra modifikuojami ar naikinami.</span><span class="sxs-lookup"><span data-stu-id="80b4e-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="80b4e-127">Norint tai pasiekti, planavimo logika kopijuoja *patvirtintus* būseną turinčius suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="80b4e-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="80b4e-128">Atkreipkite dėmesį, kad suplanuoti užsakymai, kurių būsena yra *Patvirtinta*, laikomi numatyto tiekimo tik konkrečiame pagrindiniame plane.</span><span class="sxs-lookup"><span data-stu-id="80b4e-128">Note that planned orders that have a status of *Approved*\* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="80b4e-129">Norėdami pakeisti vieno suplanuoto užsakymo būseną, atidarykite bet kurį suplanuotų užsakymų sąrašo puslapį, atidarykite užsakymą ir [atlikite](#view-planned-orders) vieną iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="80b4e-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="80b4e-130">**Bendrajame** „FastTab“ pakeiskite lauko Būsena **vertę**.</span><span class="sxs-lookup"><span data-stu-id="80b4e-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="80b4e-131">Veiksmų juostoje skirtuke **Suplanuotą užsakymą** grupėje **Apdorojimas** grupėje rinkitės **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="80b4e-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="80b4e-132">Norėdami pažymėti užsakymą kaip patvirtintą, veiksmų srityje pasirinkite **Tvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="80b4e-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="80b4e-133">Norėdami vienu metu pakeisti kelių suplanuotų užsakymų būseną, atidarykite bet kurį suplanuotų užsakymų sąrašo puslapį, pažymėkite kiekvieno norimo keisti užsakymo žymės langelį, tada atlikite [vieną](#view-planned-orders) iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="80b4e-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="80b4e-134">Veiksmų juostoje skirtuke **Suplanuotą užsakymą** grupėje **Apdorojimas** grupėje rinkitės **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="80b4e-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="80b4e-135">Norėdami pažymėti užsakymus kaip patvirtintus, veiksmų srityje pasirinkite **Tvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="80b4e-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="80b4e-136">Suplanuotų užsakymų tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="80b4e-136">Approve planned orders</span></span>

<span data-ttu-id="80b4e-137">Atkreipkite dėmesį, kad suplanuotų užsakymų patvirtinimas yra pasirinktinis veiksmas, skirtas sukurti patvirtintą suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="80b4e-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="80b4e-138">Šioje iliustracijoje parodyta, kaip galite naudoti **būsenos** vertę, priskirtą kiekvienam suplanuotam užsakymui, norėdami įdiegti patvirtinimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="80b4e-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="80b4e-139">Norėdami įdiegti patvirtinimo procesą, rankiniu būdu koreguokite **kiekvieno** suplanuoto užsakymo būsenos vertę, kaip aprašyta ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="80b4e-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![Suplanuoto užsakymo srautas](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="80b4e-141">Rekomenduojame patvirtinti bet kuriuos modifikuotus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="80b4e-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="80b4e-142">Kitu atveju redagavimų bus nepaisoma ir perrašoma kito planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="80b4e-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80b4e-143">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="80b4e-143">Additional resources</span></span>

- [<span data-ttu-id="80b4e-144">Galutinai suplanuoti užsakymai</span><span class="sxs-lookup"><span data-stu-id="80b4e-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
