---
title: Pirkimo paraiškos
description: Šioje temoje aprašoma, kaip pirkimo paraiškos yra palaikomos planavimo optimizavime.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8075f8d7c3868c6d6012edbce17dbbb4749209ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992350"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="f5ff8-103">Pirkimo paraiškos</span><span class="sxs-lookup"><span data-stu-id="f5ff8-103">Purchase requisitions</span></span>

<span data-ttu-id="f5ff8-104">Bendrasis planavimas gali papildyti patvirtintas pirkimo paraiškas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="f5ff8-105">Todėl norint padengti pirkimo paraiškas, vartotojams nereikia naudoti darbo eigos pirkimo užsakymų kūrimui.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="f5ff8-106">Vietoj to, pirkimo paraiškas gali atlikti bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="f5ff8-107">Dėl šios funkcijos, pirkimo paraiška gali sukurti pirkimo, perkėlimo arba gamybos užsakymą, atsižvelgiant į **Suplanuoto užsakymo tipo** vertę, nustatytą susijusiam produktui.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="f5ff8-108">Bendrųjų planų įgalinimas paraiškoms įtraukti</span><span class="sxs-lookup"><span data-stu-id="f5ff8-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="f5ff8-109">Norėdami įtraukti paraiškas bendrojo plano padengimo skaičiavimo metu, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="f5ff8-110">Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="f5ff8-111">Sukurkite arba pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="f5ff8-112">„FastTab“ **Bendra** nustatykite parinktį **Įtraukti paraiškas** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="f5ff8-113">Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, į kurį norite įtraukti paraiškas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="f5ff8-114">Patvirtintų paraiškų laiko riba</span><span class="sxs-lookup"><span data-stu-id="f5ff8-114">Approved requisitions time fence</span></span>

<span data-ttu-id="f5ff8-115">Skirtukas *Patvirtintų paraiškų laiko riba* nustato, kiek laiko (dienų) į bendrąjį planą bus įtrauktas patvirtintų papildymo paraiškų poreikis.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="f5ff8-116">Galite nustatyti patvirtintų paraiškų laiko ribas tiek padengimo grupės, tiek bendrojo plano lygiu.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="f5ff8-117">Patvirtintų paraiškų laiko ribos nustatymas padengimo grupei</span><span class="sxs-lookup"><span data-stu-id="f5ff8-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="f5ff8-118">Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupė**.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage group**.</span></span>
1. <span data-ttu-id="f5ff8-119">Kurkite arba pasirinkite padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="f5ff8-120">„FastTab” **Kita** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="f5ff8-121">Pakartokite 2 ir 3 veiksmus kiekvienai papildomai padengimo grupei, kuriai norite nustatyti patvirtintų paraiškų laiko ribas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="f5ff8-122">Patvirtintų paraiškų laiko ribos nustatymas individualiems bendriesiems planams</span><span class="sxs-lookup"><span data-stu-id="f5ff8-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="f5ff8-123">Kai nustatote patvirtintų paraiškų laiko ribas individualiam bendrajam planui, parametras pakeičia laiko ribos parametrą bet kuriai taikytinai padengimo grupei.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="f5ff8-124">Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="f5ff8-125">Sukurkite arba pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="f5ff8-126">„FastTab” **Laiko ribos dienomis** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="f5ff8-127">Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, kuriam norite nustatyti patvirtintų paraiškų laiko ribas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5ff8-128">**Jau greitai:** Patvirtintų paraiškų laiko ribos dar nepalaikomos planavimo optimizavime.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="f5ff8-129">Kol jos taps palaikomos, nepaisoma visų lauke **Patvirtintų paraiškų laiko ribos (dienos)** įvedamų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="f5ff8-130">Nepriklausomas tiekimas, nepaisant padengimo kodo</span><span class="sxs-lookup"><span data-stu-id="f5ff8-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="f5ff8-131">Pirkimo paraiškas visada padengia atskiri suplanuoti užsakymai, neatsižvelgiant į padengimo kodą.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="f5ff8-132">Taip užtikrinamas aiškus atsekamumas ir darbo eigos tarp pirkimo paraiškų ir papildymo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="f5ff8-133">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f5ff8-133">Example 1</span></span>

<span data-ttu-id="f5ff8-134">Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:</span><span class="sxs-lookup"><span data-stu-id="f5ff8-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="f5ff8-135">Turimų atsargų kiekis = 10.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="f5ff8-136">Mažiausias atsargų kiekis = 15.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="f5ff8-137">Didžiausias atsargų kiekis = 20.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="f5ff8-138">Yra vieno vieneto pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="f5ff8-139">Jos pageidaujama data yra šiandien.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-139">It has a requested date of today.</span></span>

<span data-ttu-id="f5ff8-140">Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – 10 vienetų papildyti atsargoms iki didžiausio kiekio, ir vienas – vienam vienetui papildyti pirkimo paraiškai.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="f5ff8-141">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f5ff8-141">Example 2</span></span>

<span data-ttu-id="f5ff8-142">Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:</span><span class="sxs-lookup"><span data-stu-id="f5ff8-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="f5ff8-143">Turimų atsargų kiekis = 17.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="f5ff8-144">Mažiausias atsargų kiekis = 15.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="f5ff8-145">Didžiausias atsargų kiekis = 20.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="f5ff8-146">Yra vieno vieneto pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="f5ff8-147">Jos pageidaujama data yra šiandien.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-147">It has a requested date of today.</span></span>

<span data-ttu-id="f5ff8-148">Kai vykdomas bendrasis planavimas, sukuriamas vieno vieneto suplanuotas užsakymas papildyti pirkimo paraiškai.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="f5ff8-149">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f5ff8-149">Example 3</span></span>

<span data-ttu-id="f5ff8-150">Produktas nustatytas taip, kad **Padengimo kodo** reikšmė yra *Laikotarpis,* o jo trukmė yra septynios dienos.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="f5ff8-151">Jo atsargų, pardavimo užsakymo ir paraiškos būsenos yra:</span><span class="sxs-lookup"><span data-stu-id="f5ff8-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="f5ff8-152">Turimų atsargų kiekis = 0.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="f5ff8-153">Yra penkių vienetų pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="f5ff8-154">Jos numatoma siuntimo data yra šiandien ir dar viena diena.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="f5ff8-155">Yra trijų vienetų pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="f5ff8-156">Jos pageidaujama data yra šiandien ir dar trys dienos.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="f5ff8-157">Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – trims vienetams papildyti pirkimo paraiškai ir vienas – penkiems vienetams papildyti pardavimo užsakymo poreikį.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="f5ff8-158">Kai patvirtinamas suplanuotas užsakymas, iškviestas pirkimo paraiškai, planavimo modulis išlaiko iškvietimą į pirkimo paraišką.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="f5ff8-159">Jei patvirtintame užsakyme vėliau pritrūksta tam tikro kiekio, reikalingo pirkimo paraiškai įvykdyti, sistema sukurs naują suplanuotą užsakymą skirtumui padengti.</span><span class="sxs-lookup"><span data-stu-id="f5ff8-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="f5ff8-160">Daugiau informacijos apie pirkimo paraiškas žiūrėkite [Pirkimo paraiškos apžvalga](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5ff8-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>