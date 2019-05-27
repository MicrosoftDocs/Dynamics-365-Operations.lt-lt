---
title: Faktiniai ir finansiniai atnaujinimai
description: Šioje temoje apžvelgiama, kokių tipų operacijos didina arba mažina atsargų kiekius.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547891"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="f8969-103">Faktiniai ir finansiniai atnaujinimai</span><span class="sxs-lookup"><span data-stu-id="f8969-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8969-104">Šioje temoje apžvelgiama, kokių tipų operacijos didina arba mažina atsargų kiekius.</span><span class="sxs-lookup"><span data-stu-id="f8969-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="f8969-105">Atsargų operacijas galima faktiškai ir finansiškai naujinti „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f8969-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="f8969-106">Kai kurių tipų faktinėse ir finansinėse operacijose atsargų kiekiai yra padidinami, o kitose – sumažinami.</span><span class="sxs-lookup"><span data-stu-id="f8969-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="f8969-107">Faktinis didėjimas</span><span class="sxs-lookup"><span data-stu-id="f8969-107">Physical increases</span></span>
<span data-ttu-id="f8969-108">Kai užregistruota faktinė operacija, operacijos įrašo būsena yra **Gauta**.</span><span class="sxs-lookup"><span data-stu-id="f8969-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="f8969-109">Toliau pateiktos operacijos laikomos faktiniais padidėjimais:</span><span class="sxs-lookup"><span data-stu-id="f8969-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="f8969-110">Pirkimo užsakymo gavimas</span><span class="sxs-lookup"><span data-stu-id="f8969-110">Purchase order receipt</span></span>
-   <span data-ttu-id="f8969-111">Pardavimo užsakymo važtaraščio grąžinimas</span><span class="sxs-lookup"><span data-stu-id="f8969-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="f8969-112">Gamybos užsakymo skelbimas baigtu</span><span class="sxs-lookup"><span data-stu-id="f8969-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="f8969-113">Šalutinis produktas gamybos užsakymo išrinkimo dokumente</span><span class="sxs-lookup"><span data-stu-id="f8969-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="f8969-114">Finansiniai padidėjimai</span><span class="sxs-lookup"><span data-stu-id="f8969-114">Financial increases</span></span>
<span data-ttu-id="f8969-115">Kai užregistruojama finansinė gavimo operacija, operacijos įrašo būsena, didinanti kiekį, yra **Nupirkta**.</span><span class="sxs-lookup"><span data-stu-id="f8969-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="f8969-116">Toliau pateiktos operacijos laikomos finansiniais padidėjimais:</span><span class="sxs-lookup"><span data-stu-id="f8969-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="f8969-117">Tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="f8969-117">Vendor invoice</span></span>
-   <span data-ttu-id="f8969-118">Pardavimo užsakymo grąžinimo SF</span><span class="sxs-lookup"><span data-stu-id="f8969-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="f8969-119">Gamybos užsakymo įkainojimas</span><span class="sxs-lookup"><span data-stu-id="f8969-119">Production order costing</span></span>
-   <span data-ttu-id="f8969-120">Teigiamo kiekio atsargų žurnalai, pvz., judėjimo, pelno ir nuostolio, inventorizacijos, KS, ir perkėlimo</span><span class="sxs-lookup"><span data-stu-id="f8969-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="f8969-121">Kiekį didinančios operacijos</span><span class="sxs-lookup"><span data-stu-id="f8969-121">Transactions that increase quantity</span></span>
<span data-ttu-id="f8969-122">Operacijos, kuriose kiekis padidinamas, registruojamos vykdoma vidutine savikaina.</span><span class="sxs-lookup"><span data-stu-id="f8969-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="f8969-123">„Finance and Operations“ apskaičiuoja naudojamą vidutinę savikainą, pagrįstą kiekvienos iš šių operacijų išlaidomis kiekvienai atsargų dimensijai, kuri sekama finansiškai.</span><span class="sxs-lookup"><span data-stu-id="f8969-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="f8969-124">Daugiau informacijos apie naudojamą vidutinę savikainą rasite dalyje [Naudojama vidutinė savikaina](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="f8969-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="f8969-125">Kiekį mažinančios operacijos</span><span class="sxs-lookup"><span data-stu-id="f8969-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="f8969-126">Kai užregistruojama kiekį mažinanti operacija, „Finance and Operations“ naudoja apskaičiuotą vykdomą vidutinę savikainą, nepriklausomai nuo to, koks atsargų modelis yra susietas su tomis atsargomis.</span><span class="sxs-lookup"><span data-stu-id="f8969-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="f8969-127">Kiekį mažinanti operacijos negali būti pažymėta kitai operacijai prieš registruojant.</span><span class="sxs-lookup"><span data-stu-id="f8969-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="f8969-128">Jei faktinės turimos atsargos tampa neigiamos, „Finance and Operations“ naudoja puslapyje **Prekė** prekei nustatytą atsargų savikainą.</span><span class="sxs-lookup"><span data-stu-id="f8969-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="f8969-129">**Pastaba:** jei įgalinta kelių teritorijų funkcija, ši savikaina bus atsargų savikaina, nustatyta teritorijai puslapyje **Numatytieji užsakymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f8969-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="f8969-130">Faktinis išdavimas ir finansinis išdavimas</span><span class="sxs-lookup"><span data-stu-id="f8969-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="f8969-131">Kai užregistruota faktinė išdavimo operacija, operacijos įrašo būsena yra **Paimta**.</span><span class="sxs-lookup"><span data-stu-id="f8969-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="f8969-132">Toliau pateiktos operacijos laikomos faktiniais išdavimais:</span><span class="sxs-lookup"><span data-stu-id="f8969-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="f8969-133">Gamybos užsakymo išrinkimo dokumentų žurnalas</span><span class="sxs-lookup"><span data-stu-id="f8969-133">Production order picking list journal</span></span>
-   <span data-ttu-id="f8969-134">Pardavimo užsakymo važtaraštis</span><span class="sxs-lookup"><span data-stu-id="f8969-134">Sales order packing slip</span></span>
-   <span data-ttu-id="f8969-135">Pirkimo užsakymo važtaraščio grąžinimas</span><span class="sxs-lookup"><span data-stu-id="f8969-135">Purchase order packing slip return</span></span>

<span data-ttu-id="f8969-136">Kai užregistruota finansinė operacija, operacijos įrašo būsena yra **Parduota**.</span><span class="sxs-lookup"><span data-stu-id="f8969-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="f8969-137">Toliau pateiktos operacijos laikomos finansiniais išdavimais:</span><span class="sxs-lookup"><span data-stu-id="f8969-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="f8969-138">Gamybos užsakymo baigimas</span><span class="sxs-lookup"><span data-stu-id="f8969-138">Ending a production order</span></span>
-   <span data-ttu-id="f8969-139">Pardavimo užsakymo SF</span><span class="sxs-lookup"><span data-stu-id="f8969-139">Sales order invoice</span></span>
-   <span data-ttu-id="f8969-140">Tiekėjo SF grąžinimas</span><span class="sxs-lookup"><span data-stu-id="f8969-140">Vendor invoice return</span></span>
-   <span data-ttu-id="f8969-141">Neigiamo kiekio atsargų žurnalai, pvz., judėjimo, pelno ir nuostolio, inventorizacijos, KS, ir perkėlimo</span><span class="sxs-lookup"><span data-stu-id="f8969-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="f8969-142">Operacijos, kurios mažina kiekį, registruojamos vykdoma vidutine savikaina.</span><span class="sxs-lookup"><span data-stu-id="f8969-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="f8969-143">Todėl norint sudengti išdavimo operacijas su gavimo operacijomis pagal kiekvienai prekei priskirtą atsargų modelį, reikia atlikti atsargų uždarymo procedūrą.</span><span class="sxs-lookup"><span data-stu-id="f8969-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>



