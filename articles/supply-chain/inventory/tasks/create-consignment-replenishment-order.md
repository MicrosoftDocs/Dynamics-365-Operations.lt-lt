---
title: Kurti naują konsignacijos papildymo užsakymą
description: Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cf2e8f742fee2dedaac72902d207af0081700ca
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845551"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="344e8-103">Kurti naują konsignacijos papildymo užsakymą</span><span class="sxs-lookup"><span data-stu-id="344e8-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="344e8-104">Šioje procedūroje parodoma, kaip kurti konsignacijos papildymo užsakymą, kuriame galite sekti numatomą tiekėjo prekių pristatymo į jūsų konsignacijos atsargas datą.</span><span class="sxs-lookup"><span data-stu-id="344e8-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="344e8-105">Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="344e8-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="344e8-106">Paprastai šią procedūrą atlieka įsigijimo specialistas.</span><span class="sxs-lookup"><span data-stu-id="344e8-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="344e8-107">Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="344e8-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="344e8-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="344e8-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="344e8-109">Konsignacijos papildymo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="344e8-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="344e8-110">Eikite į Įsigijimas ir šaltinio pasirinkimas > Konsignacija > Konsignacijos papildymo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="344e8-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="344e8-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="344e8-111">Click New.</span></span>
3. <span data-ttu-id="344e8-112">Lauke Tiekėjo kodas įveskite tiekėją US-104.</span><span class="sxs-lookup"><span data-stu-id="344e8-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="344e8-113">Turite pasirinkti tiekėją, kuris puslapyje Atsargų savininkai yra užregistruotas kaip savininkas.</span><span class="sxs-lookup"><span data-stu-id="344e8-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="344e8-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="344e8-114">Click OK.</span></span>
5. <span data-ttu-id="344e8-115">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="344e8-115">Click Add line.</span></span>
6. <span data-ttu-id="344e8-116">Lauke Prekės numeris įveskite M9211CI.</span><span class="sxs-lookup"><span data-stu-id="344e8-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="344e8-117">Turite pasirinkti prekę, kuri nustatyta konsignacijos atsargose.</span><span class="sxs-lookup"><span data-stu-id="344e8-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="344e8-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="344e8-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="344e8-119">Lauke Pageidaujama pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="344e8-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="344e8-120">MPP mechanizmas naudoja pageidaujamas ir patvirtintas datas, kad nustatytų numatomą prekių gavimo datą.</span><span class="sxs-lookup"><span data-stu-id="344e8-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="344e8-121">Lauke Patvirtinta pristatymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="344e8-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="344e8-122">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="344e8-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="344e8-123">Spustelėkite skirtuką Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="344e8-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="344e8-124">Jei norite, kad puslapyje Atsargų dimensijų savininkas būtų rodomas savininkas, atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="344e8-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="344e8-125">Dabar tiekėjas US-104 yra nurodytas kaip savininkas.</span><span class="sxs-lookup"><span data-stu-id="344e8-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="344e8-126">Atsargų operacijos būsenos patikra</span><span class="sxs-lookup"><span data-stu-id="344e8-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="344e8-127">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="344e8-127">Click Inventory.</span></span>
2. <span data-ttu-id="344e8-128">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="344e8-128">Click Transactions.</span></span>
3. <span data-ttu-id="344e8-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="344e8-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="344e8-130">Atkreipkite dėmesį, kad laukas Gavimas laukas nustatytas į parinktį Užsakytas.</span><span class="sxs-lookup"><span data-stu-id="344e8-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="344e8-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="344e8-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="344e8-132">Gauti prekes</span><span class="sxs-lookup"><span data-stu-id="344e8-132">Receive items</span></span>
1. <span data-ttu-id="344e8-133">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="344e8-133">Click Product receipt.</span></span>
2. <span data-ttu-id="344e8-134">Lauke Išorinis produkto gavimo kvitas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="344e8-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="344e8-135">Lauke Kiekis įveskite skaičių, kuris yra mažesnis nei čia rodomas kiekis.</span><span class="sxs-lookup"><span data-stu-id="344e8-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="344e8-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="344e8-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="344e8-137">Turimų atsargų patikra</span><span class="sxs-lookup"><span data-stu-id="344e8-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="344e8-138">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="344e8-138">Click Inventory.</span></span>
2. <span data-ttu-id="344e8-139">Spustelėkite Turimas kiekis.</span><span class="sxs-lookup"><span data-stu-id="344e8-139">Click On-hand.</span></span>
3. <span data-ttu-id="344e8-140">Spustelėkite Apžvalga.</span><span class="sxs-lookup"><span data-stu-id="344e8-140">Click Overview.</span></span>
    * <span data-ttu-id="344e8-141">Prekės, kurios nebuvo gautos kaip tiekėjui priklausančios konsignacijos atsargos, yra turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="344e8-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="344e8-142">Likęs konsignacijos papildymo užsakymo kiekis rodomas lauke Užsakyta iš viso.</span><span class="sxs-lookup"><span data-stu-id="344e8-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="344e8-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="344e8-143">Close the page.</span></span>
5. <span data-ttu-id="344e8-144">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="344e8-144">Click Close.</span></span>

