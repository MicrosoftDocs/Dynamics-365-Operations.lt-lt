---
title: "Kurti naują konsignacijos papildymo užsakymą"
description: "Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 6286e8f52b8131a8e4779f1e11d84233b8e0760e
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="1be38-103">Kurti naują konsignacijos papildymo užsakymą</span><span class="sxs-lookup"><span data-stu-id="1be38-103">Create a consignment replenishment order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1be38-104">Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą.</span><span class="sxs-lookup"><span data-stu-id="1be38-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="1be38-105">Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="1be38-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="1be38-106">Paprastai šią procedūrą atlieka įsigijimo specialistas.</span><span class="sxs-lookup"><span data-stu-id="1be38-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="1be38-107">Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="1be38-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="1be38-108">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="1be38-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="1be38-109">Kurti naują konsignacijos papildymo užsakymą</span><span class="sxs-lookup"><span data-stu-id="1be38-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="1be38-110">Eikite į Įsigijimas ir šaltinio pasirinkimas > Konsignacija > Konsignacijos papildymo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="1be38-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="1be38-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1be38-111">Click New.</span></span>
3. <span data-ttu-id="1be38-112">Lauke Tiekėjo kodas įveskite tiekėją US-104.</span><span class="sxs-lookup"><span data-stu-id="1be38-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="1be38-113">Turite pasirinkti tiekėją, kuris puslapyje Atsargų savininkai yra užregistruotas kaip savininkas.</span><span class="sxs-lookup"><span data-stu-id="1be38-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="1be38-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1be38-114">Click OK.</span></span>
5. <span data-ttu-id="1be38-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="1be38-115">Click Add line.</span></span>
6. <span data-ttu-id="1be38-116">Lauke Prekės numeris įveskite M9211CI.</span><span class="sxs-lookup"><span data-stu-id="1be38-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="1be38-117">Turite pasirinkti prekę, kuri nustatyta konsignacijos atsargose.</span><span class="sxs-lookup"><span data-stu-id="1be38-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="1be38-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1be38-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="1be38-119">Lauke Pageidaujama pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="1be38-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="1be38-120">MPP mechanizmas naudoja pageidaujamas ir patvirtintas datas, kad nustatytų numatomą prekių gavimo datą.</span><span class="sxs-lookup"><span data-stu-id="1be38-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="1be38-121">Lauke Patvirtinta pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="1be38-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="1be38-122">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="1be38-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="1be38-123">Spustelėkite skirtuką Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="1be38-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="1be38-124">Jei norite, kad puslapyje Atsargų dimensijų savininkas būtų rodomas savininkas, atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1be38-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="1be38-125">Dabar tiekėjas US-104 yra nurodytas kaip savininkas.</span><span class="sxs-lookup"><span data-stu-id="1be38-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="1be38-126">Atsargų operacijos būsenos patikra</span><span class="sxs-lookup"><span data-stu-id="1be38-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="1be38-127">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="1be38-127">Click Inventory.</span></span>
2. <span data-ttu-id="1be38-128">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="1be38-128">Click Transactions.</span></span>
3. <span data-ttu-id="1be38-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1be38-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1be38-130">Atkreipkite dėmesį, kad laukas Gavimas laukas nustatytas į parinktį Užsakytas.</span><span class="sxs-lookup"><span data-stu-id="1be38-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="1be38-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1be38-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="1be38-132">Gauti prekes</span><span class="sxs-lookup"><span data-stu-id="1be38-132">Receive items</span></span>
1. <span data-ttu-id="1be38-133">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="1be38-133">Click Product receipt.</span></span>
2. <span data-ttu-id="1be38-134">Lauke Išorinis produkto gavimo kvitas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1be38-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="1be38-135">Lauke Kiekis įveskite skaičių, kuris yra mažesnis nei čia rodomas kiekis.</span><span class="sxs-lookup"><span data-stu-id="1be38-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span>
4. <span data-ttu-id="1be38-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1be38-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="1be38-137">Turimų atsargų patikra</span><span class="sxs-lookup"><span data-stu-id="1be38-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="1be38-138">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="1be38-138">Click Inventory.</span></span>
2. <span data-ttu-id="1be38-139">Spustelėkite Turimas kiekis.</span><span class="sxs-lookup"><span data-stu-id="1be38-139">Click On-hand.</span></span>
3. <span data-ttu-id="1be38-140">Spustelėkite Apžvalga.</span><span class="sxs-lookup"><span data-stu-id="1be38-140">Click Overview.</span></span>
    * <span data-ttu-id="1be38-141">Prekės, kurios nebuvo gautos kaip tiekėjui priklausančios konsignacijos atsargos, yra turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="1be38-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="1be38-142">Likęs konsignacijos papildymo užsakymo kiekis rodomas lauke Užsakyta iš viso.</span><span class="sxs-lookup"><span data-stu-id="1be38-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="1be38-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1be38-143">Close the page.</span></span>
5. <span data-ttu-id="1be38-144">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="1be38-144">Click Close.</span></span>

