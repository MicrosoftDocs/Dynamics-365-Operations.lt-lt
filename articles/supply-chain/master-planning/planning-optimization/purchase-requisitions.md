---
title: Pirkimo paraiškos
description: Šioje temoje aprašoma, kaip pirkimo paraiškos yra palaikomos planavimo optimizavime.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808045"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="7db50-103">Pirkimo paraiškos</span><span class="sxs-lookup"><span data-stu-id="7db50-103">Purchase requisitions</span></span>

<span data-ttu-id="7db50-104">Bendrasis planavimas gali papildyti patvirtintas pirkimo paraiškas.</span><span class="sxs-lookup"><span data-stu-id="7db50-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="7db50-105">Todėl norint padengti pirkimo paraiškas, vartotojams nereikia naudoti darbo eigos pirkimo užsakymų kūrimui.</span><span class="sxs-lookup"><span data-stu-id="7db50-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="7db50-106">Vietoj to, pirkimo paraiškas gali atlikti bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="7db50-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="7db50-107">Dėl šios funkcijos, pirkimo paraiška gali sukurti pirkimo, perkėlimo arba gamybos užsakymą, atsižvelgiant į **Suplanuoto užsakymo tipo** vertę, nustatytą susijusiam produktui.</span><span class="sxs-lookup"><span data-stu-id="7db50-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="7db50-108">Bendrųjų planų įgalinimas paraiškoms įtraukti</span><span class="sxs-lookup"><span data-stu-id="7db50-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="7db50-109">Norėdami įtraukti paraiškas bendrojo plano padengimo skaičiavimo metu, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7db50-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="7db50-110">Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="7db50-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7db50-111">Sukurkite arba pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="7db50-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="7db50-112">„FastTab“ **Bendra** nustatykite parinktį **Įtraukti paraiškas** į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="7db50-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="7db50-113">Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, į kurį norite įtraukti paraiškas.</span><span class="sxs-lookup"><span data-stu-id="7db50-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="7db50-114">Patvirtintų paraiškų laiko riba</span><span class="sxs-lookup"><span data-stu-id="7db50-114">Approved requisitions time fence</span></span>

<span data-ttu-id="7db50-115">Skirtukas *Patvirtintų paraiškų laiko riba* nustato, kiek laiko (dienų) į bendrąjį planą bus įtrauktas patvirtintų papildymo paraiškų poreikis.</span><span class="sxs-lookup"><span data-stu-id="7db50-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="7db50-116">Galite nustatyti patvirtintų paraiškų laiko ribas tiek padengimo grupės, tiek bendrojo plano lygiu.</span><span class="sxs-lookup"><span data-stu-id="7db50-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="7db50-117">Patvirtintų paraiškų laiko ribos nustatymas padengimo grupei</span><span class="sxs-lookup"><span data-stu-id="7db50-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="7db50-118">Pasirinkite **Bendrasis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="7db50-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="7db50-119">Kurkite arba pasirinkite padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="7db50-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="7db50-120">„FastTab” **Kita** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="7db50-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7db50-121">Pakartokite 2 ir 3 veiksmus kiekvienai papildomai padengimo grupei, kuriai norite nustatyti patvirtintų paraiškų laiko ribas.</span><span class="sxs-lookup"><span data-stu-id="7db50-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="7db50-122">Patvirtintų paraiškų laiko ribos nustatymas individualiems bendriesiems planams</span><span class="sxs-lookup"><span data-stu-id="7db50-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="7db50-123">Kai nustatote patvirtintų paraiškų laiko ribas individualiam bendrajam planui, parametras pakeičia laiko ribos parametrą bet kuriai taikytinai padengimo grupei.</span><span class="sxs-lookup"><span data-stu-id="7db50-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="7db50-124">Eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="7db50-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7db50-125">Sukurkite arba pasirinkite bendrąjį planą.</span><span class="sxs-lookup"><span data-stu-id="7db50-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="7db50-126">„FastTab” **Laiko ribos dienomis** nustatykite lauką **Patvirtintų paraiškų laiko riba (dienos)** į laiko ribą norimų įtraukti dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="7db50-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7db50-127">Pakartokite 2 ir 3 veiksmus kiekvienam papildomam bendrajam planui, kuriam norite nustatyti patvirtintų paraiškų laiko ribas.</span><span class="sxs-lookup"><span data-stu-id="7db50-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7db50-128">**Jau greitai:** Patvirtintų paraiškų laiko ribos dar nepalaikomos planavimo optimizavime.</span><span class="sxs-lookup"><span data-stu-id="7db50-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="7db50-129">Kol jos taps palaikomos, nepaisoma visų lauke **Patvirtintų paraiškų laiko ribos (dienos)** įvedamų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="7db50-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="7db50-130">Nepriklausomas tiekimas, nepaisant padengimo kodo</span><span class="sxs-lookup"><span data-stu-id="7db50-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="7db50-131">Pirkimo paraiškas visada padengia atskiri suplanuoti užsakymai, neatsižvelgiant į padengimo kodą.</span><span class="sxs-lookup"><span data-stu-id="7db50-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="7db50-132">Taip užtikrinamas aiškus atsekamumas ir darbo eigos tarp pirkimo paraiškų ir papildymo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="7db50-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="7db50-133">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7db50-133">Example 1</span></span>

<span data-ttu-id="7db50-134">Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:</span><span class="sxs-lookup"><span data-stu-id="7db50-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7db50-135">Turimų atsargų kiekis = 10.</span><span class="sxs-lookup"><span data-stu-id="7db50-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="7db50-136">Mažiausias atsargų kiekis = 15.</span><span class="sxs-lookup"><span data-stu-id="7db50-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7db50-137">Didžiausias atsargų kiekis = 20.</span><span class="sxs-lookup"><span data-stu-id="7db50-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7db50-138">Yra vieno vieneto pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="7db50-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7db50-139">Jos pageidaujama data yra šiandien.</span><span class="sxs-lookup"><span data-stu-id="7db50-139">It has a requested date of today.</span></span>

<span data-ttu-id="7db50-140">Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – 10 vienetų papildyti atsargoms iki didžiausio kiekio, ir vienas – vienam vienetui papildyti pirkimo paraiškai.</span><span class="sxs-lookup"><span data-stu-id="7db50-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="7db50-141">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7db50-141">Example 2</span></span>

<span data-ttu-id="7db50-142">Produktas nustatytas taip, kad jo **Padengimo kodo** vertė būtų *„Min/maks”*. Jis turi šias atsargų ir paraiškų būsenas:</span><span class="sxs-lookup"><span data-stu-id="7db50-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7db50-143">Turimų atsargų kiekis = 17.</span><span class="sxs-lookup"><span data-stu-id="7db50-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="7db50-144">Mažiausias atsargų kiekis = 15.</span><span class="sxs-lookup"><span data-stu-id="7db50-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7db50-145">Didžiausias atsargų kiekis = 20.</span><span class="sxs-lookup"><span data-stu-id="7db50-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7db50-146">Yra vieno vieneto pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="7db50-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7db50-147">Jos pageidaujama data yra šiandien.</span><span class="sxs-lookup"><span data-stu-id="7db50-147">It has a requested date of today.</span></span>

<span data-ttu-id="7db50-148">Kai vykdomas bendrasis planavimas, sukuriamas vieno vieneto suplanuotas užsakymas papildyti pirkimo paraiškai.</span><span class="sxs-lookup"><span data-stu-id="7db50-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="7db50-149">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7db50-149">Example 3</span></span>

<span data-ttu-id="7db50-150">Produktas nustatytas taip, kad **Padengimo kodo** reikšmė yra *Laikotarpis,* o jo trukmė yra septynios dienos.</span><span class="sxs-lookup"><span data-stu-id="7db50-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="7db50-151">Jo atsargų, pardavimo užsakymo ir paraiškos būsenos yra:</span><span class="sxs-lookup"><span data-stu-id="7db50-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="7db50-152">Turimų atsargų kiekis = 0.</span><span class="sxs-lookup"><span data-stu-id="7db50-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="7db50-153">Yra penkių vienetų pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="7db50-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="7db50-154">Jos numatoma siuntimo data yra šiandien ir dar viena diena.</span><span class="sxs-lookup"><span data-stu-id="7db50-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="7db50-155">Yra trijų vienetų pirkimo paraiška.</span><span class="sxs-lookup"><span data-stu-id="7db50-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="7db50-156">Jos pageidaujama data yra šiandien ir dar trys dienos.</span><span class="sxs-lookup"><span data-stu-id="7db50-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="7db50-157">Kai vykdomas bendrasis planavimas, sukuriami du suplanuoti užsakymai: vienas – trims vienetams papildyti pirkimo paraiškai ir vienas – penkiems vienetams papildyti pardavimo užsakymo poreikį.</span><span class="sxs-lookup"><span data-stu-id="7db50-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="7db50-158">Kai patvirtinamas suplanuotas užsakymas, iškviestas pirkimo paraiškai, planavimo modulis išlaiko iškvietimą į pirkimo paraišką.</span><span class="sxs-lookup"><span data-stu-id="7db50-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="7db50-159">Jei patvirtintame užsakyme vėliau pritrūksta tam tikro kiekio, reikalingo pirkimo paraiškai įvykdyti, sistema sukurs naują suplanuotą užsakymą skirtumui padengti.</span><span class="sxs-lookup"><span data-stu-id="7db50-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="7db50-160">Daugiau informacijos apie pirkimo paraiškas žiūrėkite [Pirkimo paraiškos apžvalga](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7db50-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]