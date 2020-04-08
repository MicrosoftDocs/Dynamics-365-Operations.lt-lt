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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 386c035fb84b1f88cf53837a1e875eb2aa8ba910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146312"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="a20f8-103">Krovinio derinimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="a20f8-103">Reconcile freight manually</span></span>

<span data-ttu-id="a20f8-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="a20f8-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="a20f8-105">Šioje procedūroje parodoma, kaip transportavimą derinti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="a20f8-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="a20f8-106">Paprastai tą daro transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="a20f8-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="a20f8-107">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="a20f8-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="a20f8-108">Derintinos apkrovos pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="a20f8-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="a20f8-109">Pasirinkite Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis.</span><span class="sxs-lookup"><span data-stu-id="a20f8-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="a20f8-110">Išvalykite žymės langelį Slėpti išsiųstus ir gautus.</span><span class="sxs-lookup"><span data-stu-id="a20f8-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="a20f8-111">Sąraše pasirinkite krovinį, kurio krovinio ID yra 00006.</span><span class="sxs-lookup"><span data-stu-id="a20f8-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="a20f8-112">Vežėjo SF kūrimas</span><span class="sxs-lookup"><span data-stu-id="a20f8-112">Create a carrier invoice</span></span>
<span data-ttu-id="a20f8-113">Jei transportavimą derinate neautomatiniu būdu ir negaunate vežėjo SF automatiškai, galite kurti SF pagal transportavimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="a20f8-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="a20f8-114">Spustelėkite Susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="a20f8-114">Click Related information.</span></span>
2. <span data-ttu-id="a20f8-115">Spustelėkite Transportavimo sąskaitos informacija</span><span class="sxs-lookup"><span data-stu-id="a20f8-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="a20f8-116">Spustelėkite Generuoti krovinio atsiskaitymo SF.</span><span class="sxs-lookup"><span data-stu-id="a20f8-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="a20f8-117">Lauke Sąskaita faktūra surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a20f8-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="a20f8-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a20f8-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="a20f8-119">SF derinimas</span><span class="sxs-lookup"><span data-stu-id="a20f8-119">Reconcile the invoice</span></span>
<span data-ttu-id="a20f8-120">Vežėjo SF ir transportavimo sąskaitos derinimas atliekamas kiekvienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a20f8-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="a20f8-121">Spustelėkite Gretinti transportavimo sąskaitas ir SF.</span><span class="sxs-lookup"><span data-stu-id="a20f8-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="a20f8-122">Išplėskite skyrių SF informacija.</span><span class="sxs-lookup"><span data-stu-id="a20f8-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="a20f8-123">Išplėskite skyrių Nesugretinta transportavimo sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="a20f8-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="a20f8-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a20f8-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a20f8-125">Spustelėkite Gretinti.</span><span class="sxs-lookup"><span data-stu-id="a20f8-125">Click Match.</span></span>
6. <span data-ttu-id="a20f8-126">Išplėskite skyrių Sugretinta transportavimo sąskaitos informacija.</span><span class="sxs-lookup"><span data-stu-id="a20f8-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="a20f8-127">Pateikti SF patvirtinti</span><span class="sxs-lookup"><span data-stu-id="a20f8-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="a20f8-128">Spustelėkite Pateikti patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a20f8-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="a20f8-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a20f8-129">Close the page.</span></span>
3. <span data-ttu-id="a20f8-130">Išvalykite žymės langelį Slėpti patvirtintus.</span><span class="sxs-lookup"><span data-stu-id="a20f8-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="a20f8-131">Spustelėkite Tiekėjo SF žurnalai.</span><span class="sxs-lookup"><span data-stu-id="a20f8-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="a20f8-132">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Nuorodų žurnalo numeris.</span><span class="sxs-lookup"><span data-stu-id="a20f8-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="a20f8-133">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="a20f8-133">Click Lines.</span></span>

