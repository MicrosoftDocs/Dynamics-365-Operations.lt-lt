---
title: Sandėlio atsargų koregavimas
description: Šioje temoje pateikiama informacija apie sandėlio atsargų koregavimo žurnalą ir apdorojimą, kai naudojate skalės vienetus.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271237"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="a03ad-103">Sandėlio atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="a03ad-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a03ad-104">Sandėlio atsargų keitimo funkcija yra naudojama, kai paleisti debesies ir kraštų [skalės vienetai, skirti gamybos darbo krūviui](cloud-edge-workload-manufacturing.md) ir [sandėlio valdymo darbo](cloud-edge-workload-warehousing.md) krūviui.</span><span class="sxs-lookup"><span data-stu-id="a03ad-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="a03ad-105">Kai darbuotojas koreguoja atsargas naudodamas sandėlio programą dėl skalės vieneto sandėlio valdymo darbo krūvio, sandėlio atsargų koregavimo žurnalo paketinė užduotis turi apdoroti faktiškai turimų atsargų atnaujinimą, kurį vykdote ir suplanuokite nueidami į  **Sandėlio** valdymas **> Periodinės užduotys > Sandėlio atsargų koregavimo** žurnalas.</span><span class="sxs-lookup"><span data-stu-id="a03ad-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="a03ad-106">Toliau nurodyti sandėlio programos darbo procesai šiuo metu naudoja **sandėlio atsargų koregavimo žurnalą** dėl skalės vieneto darbo krūvių:</span><span class="sxs-lookup"><span data-stu-id="a03ad-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="a03ad-107">Keitimas (į/iš)</span><span class="sxs-lookup"><span data-stu-id="a03ad-107">Adjustment in/out</span></span>
- <span data-ttu-id="a03ad-108">Ciklo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a03ad-108">Cycle counting</span></span>
- <span data-ttu-id="a03ad-109">Numerio lentelės įkėlimas</span><span class="sxs-lookup"><span data-stu-id="a03ad-109">License plate loading</span></span>

<span data-ttu-id="a03ad-110">Kelios atsargų operacijos sukuriamos kaip debesies ir kiekviena krašto dalis atsargų koregavimo procese, nes centro ir svarstyklių vienetų diegimas bendrai naudojamas atsargų įrašuose.</span><span class="sxs-lookup"><span data-stu-id="a03ad-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="a03ad-111">Atsargų koregavimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a03ad-111">Inventory adjustment example</span></span>

<span data-ttu-id="a03ad-112">Šiame pavyzdyje sandėlio darbuotojas naudojo sandėlio programą, kad galėtų užregistruoti turimų atsargų kiekį.</span><span class="sxs-lookup"><span data-stu-id="a03ad-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="a03ad-113">Pirma, skalės vieneto darbo krūvis sukuria teigiamo faktinio koregavimo sandėlio atsargų koregavimo operaciją, kuri tada sinchronizuojama su centru ir padidina turimų atsargų kiekį centre.</span><span class="sxs-lookup"><span data-stu-id="a03ad-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="a03ad-114">Tipas</span><span class="sxs-lookup"><span data-stu-id="a03ad-114">Type</span></span>                                    | <span data-ttu-id="a03ad-115">Skalės vienetas</span><span class="sxs-lookup"><span data-stu-id="a03ad-115">Scale unit</span></span> | <span data-ttu-id="a03ad-116">Kryptis</span><span class="sxs-lookup"><span data-stu-id="a03ad-116">Direction</span></span> | <span data-ttu-id="a03ad-117">Tranzito punktas</span><span class="sxs-lookup"><span data-stu-id="a03ad-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="a03ad-118">Sandėlio atsargų koregavimas</span><span class="sxs-lookup"><span data-stu-id="a03ad-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="a03ad-119">+1</span><span class="sxs-lookup"><span data-stu-id="a03ad-119">+1</span></span>         | ->        | <span data-ttu-id="a03ad-120">+1</span><span class="sxs-lookup"><span data-stu-id="a03ad-120">+1</span></span>  |

<span data-ttu-id="a03ad-121">Tada centras apdoroja skaičiavimo žurnalo registravimą, kuris gaunamas naudojant pranešimų [procesoriaus](cloud-edge-message-processor-messages.md) pranešimus.</span><span class="sxs-lookup"><span data-stu-id="a03ad-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="a03ad-122">Taip atnaujinamos papildomos turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="a03ad-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="a03ad-123">Siekiant išvengti dvigubo turimų atsargų kiekio, centras kaip šio proceso dalį sukuria korespondentinę operaciją ir pašalina anksčiau įrašytas turimų atsargų, susijusių su sandėlio atsargų koregavimu, atsargas.</span><span class="sxs-lookup"><span data-stu-id="a03ad-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="a03ad-124">Tipas</span><span class="sxs-lookup"><span data-stu-id="a03ad-124">Type</span></span>                                    | <span data-ttu-id="a03ad-125">Skalės vienetas</span><span class="sxs-lookup"><span data-stu-id="a03ad-125">Scale unit</span></span> | <span data-ttu-id="a03ad-126">Kryptis</span><span class="sxs-lookup"><span data-stu-id="a03ad-126">Direction</span></span> | <span data-ttu-id="a03ad-127">Tranzito punktas</span><span class="sxs-lookup"><span data-stu-id="a03ad-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="a03ad-128">Inventorizacija</span><span class="sxs-lookup"><span data-stu-id="a03ad-128">Counting</span></span>                                | <span data-ttu-id="a03ad-129">+1</span><span class="sxs-lookup"><span data-stu-id="a03ad-129">+1</span></span>         | <-        | <span data-ttu-id="a03ad-130">+1</span><span class="sxs-lookup"><span data-stu-id="a03ad-130">+1</span></span>  |
| <span data-ttu-id="a03ad-131">Sandėlio atsargų koregavimas (korespondentinė sąskaita)</span><span class="sxs-lookup"><span data-stu-id="a03ad-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="a03ad-132">-1</span><span class="sxs-lookup"><span data-stu-id="a03ad-132">-1</span></span>         | <-        | <span data-ttu-id="a03ad-133">-1</span><span class="sxs-lookup"><span data-stu-id="a03ad-133">-1</span></span>  |

<span data-ttu-id="a03ad-134">Kai svarstyklių vienetas sukuria sandėlio atsargų koregavimo žurnalą centre, galite peržiūrėti inventorizacijos žurnalą ir korespondentinį žurnalą, kurie kuriami centro kaip koregavimo **koregavimo** **proceso** **dalis**.</span><span class="sxs-lookup"><span data-stu-id="a03ad-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="a03ad-135">Galite peržiūrėti visus šiuos žurnalo įrašus ir „Supply Chain Management“ operaciją atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="a03ad-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="a03ad-136">Prisiregistruokite svarstyklių vienetais.</span><span class="sxs-lookup"><span data-stu-id="a03ad-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="a03ad-137">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Sandėlio atsargų reguliavimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="a03ad-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="a03ad-138">Sandėlio **atsargų koregavimo žurnalo puslapyje** raskite ir atidarykite žurnalą, kuriame įrašytas turimų atsargų pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="a03ad-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="a03ad-139">Žurnalo **eilučių skyriuje rodomi visi šio** žurnalo įrašyti koregavimai.</span><span class="sxs-lookup"><span data-stu-id="a03ad-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="a03ad-140">Prisiregistruoti prie centro.</span><span class="sxs-lookup"><span data-stu-id="a03ad-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="a03ad-141">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Sandėlio atsargų reguliavimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="a03ad-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="a03ad-142">Sandėlio atsargų koregavimo žurnalo puslapyje turite matyti tą patį žurnalą, jei **sinchronizuotas** centro ir svarstyklių vienetas.</span><span class="sxs-lookup"><span data-stu-id="a03ad-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="a03ad-143">Atidaryti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="a03ad-143">Open the journal.</span></span> <span data-ttu-id="a03ad-144">Jei pranešimų [procesoriaus pranešimai apdoroti, antraštėje matysite saitus su inventorizacijos](cloud-edge-message-processor-messages.md) **žurnalu** ir **korespondentinio** žurnalu.</span><span class="sxs-lookup"><span data-stu-id="a03ad-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="a03ad-145">Inventorizacijos **žurnale** turi būti tos pačios dimensijų vertės kaip žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="a03ad-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="a03ad-146">Korespondentinis **žurnalas** turi rodyti korespondentinę sąskaitą, kuri pašalina dvigubą atsargų koregavimą.</span><span class="sxs-lookup"><span data-stu-id="a03ad-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="a03ad-147">Kai visi sinchronizuojami ir apdorojami, inventorizacijos žurnalas ir korespondentinis **žurnalas** sinchronizuojami **atgal** į svarstyklių vienetą.</span><span class="sxs-lookup"><span data-stu-id="a03ad-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="a03ad-148">Juos taip pat galima peržiūrėti reikiamo **sandėlio atsargų koregavimo žurnalo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a03ad-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
