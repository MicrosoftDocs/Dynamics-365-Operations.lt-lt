---
title: Kiekio mažinti negalima atšaukus pardavimo užsakymą
description: Kiekio mažinti negalima atšaukus pardavimo užsakymą.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230841"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="1c876-103">Kiekio mažinti negalima atšaukus pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="1c876-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="1c876-104">Klaidos kodas: SYS138831</span><span class="sxs-lookup"><span data-stu-id="1c876-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="1c876-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="1c876-105">Symptoms</span></span>

<span data-ttu-id="1c876-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="1c876-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1c876-107">Kiekio negalima sumažinti.</span><span class="sxs-lookup"><span data-stu-id="1c876-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="1c876-108">Užsakytas atsargų operacijų kiekis per mažas, nes kiekį arba jo dalį nurodo išeigos užsakymas arba gamybos užsakymas arba jis yra pažymėtas pagal kitas operacijas.</span><span class="sxs-lookup"><span data-stu-id="1c876-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="1c876-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="1c876-109">Cause</span></span>

<span data-ttu-id="1c876-110">Jei darbas susietas su pardavimo užsakymu, negalite atšaukti pardavimo užsakymo, kol darbas nebus atšauktas.</span><span class="sxs-lookup"><span data-stu-id="1c876-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="1c876-111">Šis reikalavimas taikomas, net jei darbas, susietas su pardavimo užsakymu, yra uždarytas.</span><span class="sxs-lookup"><span data-stu-id="1c876-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="1c876-112">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="1c876-112">Resolution</span></span>

<span data-ttu-id="1c876-113">Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:</span><span class="sxs-lookup"><span data-stu-id="1c876-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="1c876-114">Atšaukti atidarytą darbą.</span><span class="sxs-lookup"><span data-stu-id="1c876-114">Cancel open work.</span></span>
1. <span data-ttu-id="1c876-115">Panaikinkite krovinį.</span><span class="sxs-lookup"><span data-stu-id="1c876-115">Delete the load.</span></span>
1. <span data-ttu-id="1c876-116">Paimto kiekio sumažinimas.</span><span class="sxs-lookup"><span data-stu-id="1c876-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="1c876-117">Atšaukti atidarytą darbą</span><span class="sxs-lookup"><span data-stu-id="1c876-117">Cancel open work</span></span>

<span data-ttu-id="1c876-118">Norėdami atidaryti darbą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="1c876-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="1c876-119">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="1c876-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="1c876-120">Laukelyje **Darbo ID** nurodykite darbo ID, kurį norite atšaukti ir tai, kad dabar **Darbo būsenos** vertė *Atidaryta*, *Vykdoma*, *Atšaukta*, *Kombinuota* ar *Uždaryta*.</span><span class="sxs-lookup"><span data-stu-id="1c876-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="1c876-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1c876-121">Select **OK**.</span></span>
1. <span data-ttu-id="1c876-122">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="1c876-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="1c876-123">Panaikinkite krovinį</span><span class="sxs-lookup"><span data-stu-id="1c876-123">Delete the load</span></span>

<span data-ttu-id="1c876-124">Norėdami panaikinti krovinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1c876-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="1c876-125">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1c876-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1c876-126">Atidarykite reikalingą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1c876-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="1c876-127">„FastTab“ **Pardavimo užsakymo eilutės** rinkitės **Sandėlis \> Darbo informacija**.</span><span class="sxs-lookup"><span data-stu-id="1c876-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="1c876-128">Puslapyje **Darbas** veiksmų juostoje, skirtuke **Darbas** grupėje **Darbas** rinkitės **Atšaukti darbą**.</span><span class="sxs-lookup"><span data-stu-id="1c876-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="1c876-129">Patvirtinkite, kad **Darbo būsena** nustatyta į *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="1c876-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="1c876-130">Uždarykite puslapį **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="1c876-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="1c876-131">Išsamios pardavimo užsakymo informacijos puslapio **pardavimo užsakymo eilučių** „FastTab“, pasirinkite **Sandėlio \> krovinio informacija**.</span><span class="sxs-lookup"><span data-stu-id="1c876-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="1c876-132">Rinkitės **Naikinti** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="1c876-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="1c876-133">Pasirinkite **Taip**, kad patvirtintumėte, kad norite naikinti krovinį.</span><span class="sxs-lookup"><span data-stu-id="1c876-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="1c876-134">Uždarykite puslapį **Krovinys**.</span><span class="sxs-lookup"><span data-stu-id="1c876-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="1c876-135">Paimto kiekio sumažinimas</span><span class="sxs-lookup"><span data-stu-id="1c876-135">Reduce the picked quantity</span></span>

<span data-ttu-id="1c876-136">Kai visas darbas atšauktas, atlikite šiuos veiksmus, norėdami sumažinti paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="1c876-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="1c876-137">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1c876-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1c876-138">Atidarykite reikalingą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1c876-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="1c876-139">„FastTab“ **Pardavimo užsakymo eilutėse** , rinkitės **Naujinti eilutę \> Paėmimas** įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="1c876-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="1c876-140">Puslapyje **Paimti** skyriuje **Operacijos** pasirinkite eilutę, kurioje **Problemos būsenos** laukelis yra nustatyta *Paimtas*.</span><span class="sxs-lookup"><span data-stu-id="1c876-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="1c876-141">Skyriuje **Operacijos** rinkitės **Įtraukti paėmimo eilutę** iš įrankių juostos.</span><span class="sxs-lookup"><span data-stu-id="1c876-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="1c876-142">Skyriuje **Paėmimo eilutės** rinkitės **Tvirtinti paėmimo eilutę** iš įrankių juostos.</span><span class="sxs-lookup"><span data-stu-id="1c876-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="1c876-143">Uždarykite puslapį **Paėmimas**.</span><span class="sxs-lookup"><span data-stu-id="1c876-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="1c876-144">Puslapio Pardavimo užsakymas veiksmų srities skirtuke **Prekybos užsakymas** skirtuke **Palaikyti** grupę rinkitės **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="1c876-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="1c876-145">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1c876-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
