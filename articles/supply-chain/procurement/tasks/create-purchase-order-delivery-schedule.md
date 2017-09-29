--- 
title: "Kurti pirkimo užsakymą su pristatymo grafiku"
description: "Ši procedūra parodo, kaip kurti pirkimo užsakymo pristatymo grafiką."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="e3319-103">Kurti pirkimo užsakymą su pristatymo grafiku</span><span class="sxs-lookup"><span data-stu-id="e3319-103">Create a purchase order with a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3319-104">Ši procedūra parodo, kaip kurti pirkimo užsakymo pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="e3319-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="e3319-105">Pristatymo grafikas naudojamas, kai užsakymo arba žurnalo kiekį pageidaujama pristatyti keliomis siuntomis.</span><span class="sxs-lookup"><span data-stu-id="e3319-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="e3319-106">Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="e3319-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="e3319-107">Paprastai šią procedūrą atlieka pirkimo agentas.</span><span class="sxs-lookup"><span data-stu-id="e3319-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="e3319-108">Kurti pristatymo grafiką</span><span class="sxs-lookup"><span data-stu-id="e3319-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="e3319-109">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="e3319-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e3319-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e3319-110">Click New.</span></span>
3. <span data-ttu-id="e3319-111">Lauke Tiekėjo kodas įveskite US-101.</span><span class="sxs-lookup"><span data-stu-id="e3319-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="e3319-112">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3319-112">Click OK.</span></span>
5. <span data-ttu-id="e3319-113">Lauke Prekės numeris įveskite M0001.</span><span class="sxs-lookup"><span data-stu-id="e3319-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="e3319-114">Lauke Kiekis įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="e3319-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="e3319-115">Spustelėkite Pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="e3319-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="e3319-116">Spustelėkite Pristatymo grafikas.</span><span class="sxs-lookup"><span data-stu-id="e3319-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="e3319-117">Puslapyje Pristatymo grafikas galima nurodyti siuntų, kurių visas užsakymo eilutės kiekis bus pristatytas iš tiekėjo, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e3319-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="e3319-118">Pagal numatytąsias nuostatas sistema visą pradinės pirkimo eilutės kiekį ir kitą pristatymo informaciją kopijuoja į pirmąją pristatymo grafiko eilutę.</span><span class="sxs-lookup"><span data-stu-id="e3319-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="e3319-119">Šiame pavyzdyje sukursime dviejų siuntų grafiką, antrosios siuntos datą paslinkdami per savaitę nuo pirmosios.</span><span class="sxs-lookup"><span data-stu-id="e3319-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="e3319-120">Lauke Kiekis pakeiskite kiekį į 4.</span><span class="sxs-lookup"><span data-stu-id="e3319-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="e3319-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e3319-121">Click New.</span></span>
11. <span data-ttu-id="e3319-122">Lauke Kiekis įveskite 6 kaip likusį kiekį.</span><span class="sxs-lookup"><span data-stu-id="e3319-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="e3319-123">Lauke Pristatymo data pasirinkite datą, kuri yra viena savaite vėliau nei pirmosios pristatymo eilutės data.</span><span class="sxs-lookup"><span data-stu-id="e3319-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="e3319-124">Sekti visą kiekį, paskirstytą pristatymo grafiko eilutėms, galite pažvelgę į laukus Iš viso ir Liko.</span><span class="sxs-lookup"><span data-stu-id="e3319-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="e3319-125">Kai likęs kiekis yra nulis, grafikui paskirstytas visas pradinės eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="e3319-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="e3319-126">Išplėskite sekciją Išlaidų konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="e3319-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="e3319-127">Ši parinktis suteikia galimybę kontroliuoti, kaip norite išlaidas paskirstyti pristatymo grafiko eilutėse.</span><span class="sxs-lookup"><span data-stu-id="e3319-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="e3319-128">Jei pasirenkate Kopijuoti bendras sumas, pradinės užsakymo eilutės išlaidų suma kopijuojama į kiekvieną pristatymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="e3319-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="e3319-129">Parinktis Paskirstyti į pristatymo eilutes pradinės eilutės išlaidas padalija pagal kiekį kiekvienoje pristatymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e3319-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="e3319-130">Suskleiskite sekciją Išlaidų konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="e3319-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="e3319-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3319-131">Click OK.</span></span>
    * <span data-ttu-id="e3319-132">Pristatymo grafikas dabar yra pritaikytas užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e3319-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="e3319-133">Pradinė užsakymo eilutė, dabar vadinama komercine eilute, konvertuota į užsakymo eilutę, kurioje yra keli pristatymai.</span><span class="sxs-lookup"><span data-stu-id="e3319-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="e3319-134">Ji pažymėta atskira piktograma ir veikia kaip pristatymo eilučių antraštė.</span><span class="sxs-lookup"><span data-stu-id="e3319-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="e3319-135">Pasirinkite antrąją užsakymo eilutę, kuri yra pirmoji iš dviejų pristatymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="e3319-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="e3319-136">Dvi naujosios eilutės, vadinamos pristatymo eilutėmis, sudaro vieną pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="e3319-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="e3319-137">Užsakymas bus vykdomas pagal šias eilutes, o ne pradinę eilutę.</span><span class="sxs-lookup"><span data-stu-id="e3319-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="e3319-138">Jei spausdinami tokie dokumentai kaip patvirtinimai, produktų gavimo kvitų žurnalai ar SF, rodomos tik pristatymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3319-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="e3319-139">Keisti pristatymo grafiką</span><span class="sxs-lookup"><span data-stu-id="e3319-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="e3319-140">Galite keisti pristatymo eilučių kiekį.</span><span class="sxs-lookup"><span data-stu-id="e3319-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="e3319-141">Jei taip padarote, komercinė eilutė automatiškai atnaujinama į visą pristatymo eilučių kiekį.</span><span class="sxs-lookup"><span data-stu-id="e3319-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="e3319-142">Pirmosios pristatymo eilutės lauko Kiekis reikšmę pakeiskite iš 4 į 5.</span><span class="sxs-lookup"><span data-stu-id="e3319-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="e3319-143">Pasirinkite pirmąją užsakymo eilutę (komercinę eilutę).</span><span class="sxs-lookup"><span data-stu-id="e3319-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="e3319-144">Komercinės eilutės kiekis pakeistas į 11.</span><span class="sxs-lookup"><span data-stu-id="e3319-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="e3319-145">Apdoroti produkto gavimą naudojant pristatymo grafikus</span><span class="sxs-lookup"><span data-stu-id="e3319-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="e3319-146">Pirkimo užsakymas turi būti patvirtintas, kad produkto gavimą būtų galima apdoroti.</span><span class="sxs-lookup"><span data-stu-id="e3319-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="e3319-147">Šiame pavyzdyje gavimas užregistruojamas tiesiai pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="e3319-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="e3319-148">Gavimą taip pat buvo galima užregistruoti, kai prekės buvo pristatytos į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="e3319-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="e3319-149">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="e3319-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="e3319-150">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="e3319-150">Click Confirm.</span></span>
3. <span data-ttu-id="e3319-151">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="e3319-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="e3319-152">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="e3319-152">Click Product receipt.</span></span>
5. <span data-ttu-id="e3319-153">Lauke Produkto gavimo kvitas įveskite bet kokią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3319-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="e3319-154">Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.</span><span class="sxs-lookup"><span data-stu-id="e3319-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="e3319-155">Lauke Kiekis pasirinkite Užsakytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="e3319-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="e3319-156">Pasirinkus šią parinktį bus apdorojamas toks gavimo kiekis, kurį naudojant buvo sukurtos užsakymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3319-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="e3319-157">Įsitikinkite, kad lauko Spausdinti produkto gavimo kvitą parinktis nustatyta kaip Ne.</span><span class="sxs-lookup"><span data-stu-id="e3319-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="e3319-158">Šiame pavyzdyje spausdinti nereikia.</span><span class="sxs-lookup"><span data-stu-id="e3319-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="e3319-159">Išplėskite dalį Eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3319-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="e3319-160">Atkreipkite dėmesį, kad kuriamas dviejų pristatymo eilučių, o ne pradinės užsakymo eilutės produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="e3319-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="e3319-161">Jei gavimas užregistruotas sandėlyje, jis bus taip pat užregistruotas pristatymo grafiko eilutėse.</span><span class="sxs-lookup"><span data-stu-id="e3319-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="e3319-162">Sutraukite sekciją Eilutės.</span><span class="sxs-lookup"><span data-stu-id="e3319-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="e3319-163">Spustelėkite Gerai, kad registruotumėte gavimą.</span><span class="sxs-lookup"><span data-stu-id="e3319-163">Click OK to post the receipt.</span></span>

