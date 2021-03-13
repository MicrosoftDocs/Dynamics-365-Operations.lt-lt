---
title: Konsignacijos papildymo užsakymo kūrimas
description: Temoje aiškinama, kaip kurti siuntos papildymo užsakymą, kuriame galite stebėti numatytą pristatymą iš tiekėjo į jūsų siuntos atsargas.
author: RichardLuan
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b27b4d87add38fac29c9eba4ace08af91f9faca1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020159"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="781fd-103">Konsignacijos papildymo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="781fd-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="781fd-104">Temoje aiškinama, kaip kurti siuntos papildymo užsakymą, kuriame galite stebėti numatytą pristatymą iš tiekėjo į jūsų siuntos atsargas.</span><span class="sxs-lookup"><span data-stu-id="781fd-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="781fd-105">Joje taip pat parodoma, kaip įrašyti produktų gavimą, kad konsignacijos atsargos būtų užregistruotas tiekėjui priklausančios turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="781fd-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="781fd-106">Paprastai šią procedūrą atlieka įsigijimo specialistas.</span><span class="sxs-lookup"><span data-stu-id="781fd-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="781fd-107">Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="781fd-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="781fd-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="781fd-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="781fd-109">Konsignacijos papildymo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="781fd-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="781fd-110">Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Siunta > Siuntos papildymo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="781fd-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="781fd-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="781fd-111">Select **New**.</span></span>
3. <span data-ttu-id="781fd-112">Lauke **Tiekėjo sąskaita** pažymėkite tiekėją **US-104** (turite pažymėti tiekėją, kuris puslapyje **atsargų savininkai** registruotas kaip savininkas).</span><span class="sxs-lookup"><span data-stu-id="781fd-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="781fd-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="781fd-113">Select **OK**.</span></span>
5. <span data-ttu-id="781fd-114">Pasirinkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="781fd-114">Select **Add line**.</span></span>
6. <span data-ttu-id="781fd-115">Lauke **Elemento numeris** įveskite `M9211CI` (turite pažymėti elementą, kuris nustatytas siuntos atsargoms).</span><span class="sxs-lookup"><span data-stu-id="781fd-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="781fd-116">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="781fd-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="781fd-117">Lauke **Pageidaujama pristatymo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="781fd-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="781fd-118">MPP mechanizmas naudoja pageidaujamas ir patvirtintas datas, kad nustatytų numatomą prekių gavimo datą.</span><span class="sxs-lookup"><span data-stu-id="781fd-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="781fd-119">Lauke **Patvirtinta pristatymo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="781fd-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="781fd-120">Išplėskite skyrių **Eilutės informacija** section.</span><span class="sxs-lookup"><span data-stu-id="781fd-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="781fd-121">Pasirinkite skirtuką **Atsargų matmenys**.</span><span class="sxs-lookup"><span data-stu-id="781fd-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="781fd-122">Norėdami lauke **Atsargų matmenų savininkas** matyti savininką, atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="781fd-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="781fd-123">Dabar tiekėjas US-104 yra nurodytas kaip savininkas.</span><span class="sxs-lookup"><span data-stu-id="781fd-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="781fd-124">Atsargų operacijos būsenos patikra</span><span class="sxs-lookup"><span data-stu-id="781fd-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="781fd-125">Pasirinkite **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="781fd-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="781fd-126">Pasirinkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="781fd-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="781fd-127">Pageidaujamoje eilutėje pažymėkite, kad laukas **Gavimas** nustatytas kaip **Užsakyta**.</span><span class="sxs-lookup"><span data-stu-id="781fd-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="781fd-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="781fd-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="781fd-129">Gauti prekes</span><span class="sxs-lookup"><span data-stu-id="781fd-129">Receive items</span></span>
1. <span data-ttu-id="781fd-130">Pasirinkite **„Produkto gavimo kvitas“**.</span><span class="sxs-lookup"><span data-stu-id="781fd-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="781fd-131">Lauke **Išorinis produkto gavimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="781fd-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="781fd-132">Lauke **Kiekis** įveskite skaičių, kuris mažesnis nei čia parodytas skaičius.</span><span class="sxs-lookup"><span data-stu-id="781fd-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="781fd-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="781fd-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="781fd-134">Turimų atsargų patikra</span><span class="sxs-lookup"><span data-stu-id="781fd-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="781fd-135">Pasirinkite **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="781fd-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="781fd-136">Pažymėkite **Turima**.</span><span class="sxs-lookup"><span data-stu-id="781fd-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="781fd-137">Pažymėkite **Apžvalga**.</span><span class="sxs-lookup"><span data-stu-id="781fd-137">Select **Overview**.</span></span> <span data-ttu-id="781fd-138">Prekės, kurios nebuvo gautos kaip tiekėjui priklausančios konsignacijos atsargos, yra turimos atsargos.</span><span class="sxs-lookup"><span data-stu-id="781fd-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="781fd-139">Likęs siuntos atsargų užsakymo kiekis rodomas lauke **Iš viso užsakyta**.</span><span class="sxs-lookup"><span data-stu-id="781fd-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="781fd-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="781fd-140">Close the page.</span></span>

