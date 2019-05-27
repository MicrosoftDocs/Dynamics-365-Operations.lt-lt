---
title: Transportavimo derinimas neautomatiniu būdu
description: Šioje procedūroje parodoma, kaip transportavimą derinti neautomatiniu būdu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556739"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="7d0e2-103">Transportavimo derinimas neautomatiniu būdu</span><span class="sxs-lookup"><span data-stu-id="7d0e2-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7d0e2-104">Šioje procedūroje parodoma, kaip transportavimą derinti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="7d0e2-105">Paprastai tą daro transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="7d0e2-106">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="7d0e2-107">Derintinos apkrovos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="7d0e2-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="7d0e2-108">Pasirinkite Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="7d0e2-109">Išvalykite žymės langelį Slėpti išsiųstus ir gautus.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="7d0e2-110">Sąraše pasirinkite krovinį, kurio krovinio ID yra 00006.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="7d0e2-111">Vežėjo SF kūrimas</span><span class="sxs-lookup"><span data-stu-id="7d0e2-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="7d0e2-112">Jei transportavimą derinate neautomatiniu būdu ir negaunate vežėjo SF automatiškai, galite kurti SF pagal transportavimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="7d0e2-113">Spustelėkite Susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-113">Click Related information.</span></span>
2. <span data-ttu-id="7d0e2-114">Spustelėkite Transportavimo sąskaitos informacija</span><span class="sxs-lookup"><span data-stu-id="7d0e2-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="7d0e2-115">Spustelėkite Generuoti krovinio atsiskaitymo SF.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="7d0e2-116">Lauke Sąskaita faktūra surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="7d0e2-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="7d0e2-118">SF derinimas</span><span class="sxs-lookup"><span data-stu-id="7d0e2-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="7d0e2-119">Vežėjo SF ir transportavimo sąskaitos derinimas atliekamas kiekvienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="7d0e2-120">Spustelėkite Gretinti transportavimo sąskaitas ir SF.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="7d0e2-121">Išplėskite skyrių SF informacija.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="7d0e2-122">Išplėskite skyrių Nesugretinta transportavimo sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="7d0e2-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="7d0e2-124">Spustelėkite Gretinti.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-124">Click Match.</span></span>
6. <span data-ttu-id="7d0e2-125">Išplėskite skyrių Sugretinta transportavimo sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="7d0e2-126">Pateikti SF patvirtinti</span><span class="sxs-lookup"><span data-stu-id="7d0e2-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="7d0e2-127">Spustelėkite Pateikti patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="7d0e2-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-128">Close the page.</span></span>
3. <span data-ttu-id="7d0e2-129">Išvalykite žymės langelį Slėpti patvirtintus.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="7d0e2-130">Spustelėkite Tiekėjo SF žurnalai.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="7d0e2-131">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Nuorodų žurnalo numeris.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="7d0e2-132">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="7d0e2-132">Click Lines.</span></span>

