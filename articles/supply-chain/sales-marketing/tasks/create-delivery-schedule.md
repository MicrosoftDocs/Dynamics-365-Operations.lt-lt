--- 
title: "Kurti pristatymo grafiką"
description: "Ši procedūra parodo, kaip kurti pardavimo užsakymo pristatymo grafiką."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 13add634e275a0156c2c0f87d1fec80385d62fea
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="99357-103">Kurti pristatymo grafiką</span><span class="sxs-lookup"><span data-stu-id="99357-103">Create a delivery schedule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99357-104">Ši procedūra parodo, kaip kurti pardavimo užsakymo pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="99357-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="99357-105">Pristatymo grafikas naudojamas, kai užsakymo arba pasiūlymo kiekį pageidaujama pristatyti keliomis siuntomis.</span><span class="sxs-lookup"><span data-stu-id="99357-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="99357-106">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="99357-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="99357-107">Kurti pristatymo grafiką</span><span class="sxs-lookup"><span data-stu-id="99357-107">Create delivery schedule</span></span>
1. <span data-ttu-id="99357-108">Eikite į Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="99357-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="99357-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="99357-109">Click New.</span></span>
3. <span data-ttu-id="99357-110">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99357-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="99357-111">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="99357-111">Click OK.</span></span>
5. <span data-ttu-id="99357-112">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99357-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="99357-113">Lauke Kiekis įveskite skaičių, kuris yra didesnis nei 1.</span><span class="sxs-lookup"><span data-stu-id="99357-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="99357-114">Spustelėkite eilutę Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="99357-114">Click Sales order line.</span></span>
8. <span data-ttu-id="99357-115">Spustelėkite Pristatymo grafikas.</span><span class="sxs-lookup"><span data-stu-id="99357-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="99357-116">Puslapis Pristatymo grafikas – tai vieta, kurioje galite nurodyti siuntų, kurių visas užsakymo eilutės kiekis bus pristatytas klientui, skaičių.</span><span class="sxs-lookup"><span data-stu-id="99357-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="99357-117">Pagal numatytąsias nuostatas sistema visą pradinės pardavimo eilutės kiekį ir kitą pristatymo informaciją kopijuoja į pirmąją pristatymo grafiko eilutę.</span><span class="sxs-lookup"><span data-stu-id="99357-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="99357-118">Šiame pavyzdyje sukursime dviejų siuntų grafiką, antrosios siuntos datą paslinkdami per savaitę nuo pirmosios.</span><span class="sxs-lookup"><span data-stu-id="99357-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="99357-119">Lauke Kiekis įveskite skaičių, kuris yra viso kiekio dalis.</span><span class="sxs-lookup"><span data-stu-id="99357-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="99357-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="99357-120">Click New.</span></span>
11. <span data-ttu-id="99357-121">Lauke Kiekis įveskite likusį kiekį.</span><span class="sxs-lookup"><span data-stu-id="99357-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="99357-122">Lauke Pageidaujama siuntimo data įveskite datą, kuri yra viena savaite į priekį nuo pirmosios pristatymo eilutės datos.</span><span class="sxs-lookup"><span data-stu-id="99357-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="99357-123">Dvi „FastTab‟ Išlaidų konvertavimas parinktys kontroliuoja, kaip išlaidas paskirstyti pristatymo grafiko eilutėse, kai jos priskirtos pradinei užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="99357-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="99357-124">Jei pasirenkate Kopijuoti bendras sumas, ta pati išlaidų suma kopijuojama į kiekvieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="99357-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="99357-125">Parinktis Paskirstyti į pristatymo eilutes išlaidas vienodai padalija visose pristatymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="99357-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="99357-126">Skirstyti galima tik fiksuotas išlaidas, o kintamosios išlaidos vis tiek bus kopijuojamos į eilutes.</span><span class="sxs-lookup"><span data-stu-id="99357-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="99357-127">Perkėlę žymeklį nuo antrosios pristatymo eilutės, atnaujinsite puslapį.</span><span class="sxs-lookup"><span data-stu-id="99357-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="99357-128">Sekti visą kiekį, paskirstytą pristatymo grafiko eilutėms, galite pažvelgę į laukus Iš viso ir Liko.</span><span class="sxs-lookup"><span data-stu-id="99357-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="99357-129">Kai likęs kiekis yra nulis, grafikui paskirstytas visas pradinės eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="99357-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="99357-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="99357-130">Click OK.</span></span>
    * <span data-ttu-id="99357-131">Pristatymo grafikas dabar nukopijuotas į užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="99357-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="99357-132">Pradinė užsakymo eilutė, vadinama komercine eilute, konvertuota į užsakymo eilutę, kurioje yra keli pristatymai.</span><span class="sxs-lookup"><span data-stu-id="99357-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="99357-133">Ji pažymėta atskira piktograma ir veikia kaip pristatymo eilučių antraštė.</span><span class="sxs-lookup"><span data-stu-id="99357-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="99357-134">Dvi naujosios eilutės, vadinamos pristatymo eilutėmis, sudaro vieną pristatymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="99357-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="99357-135">Užsakymas bus vykdomas pagal šias eilutes, o ne pradinę eilutę.</span><span class="sxs-lookup"><span data-stu-id="99357-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="99357-136">Jei spausdinami tokie dokumentai kaip patvirtinimo važtaraščiai, išrinkimo dokumentai, važtaraščiai ar SF, rodomos tik pristatymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="99357-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="99357-137">Pristatymo eilutėse gali skirtis pristatymo datos, kiekiai, pristatymo būdai ir saugojimo dimensijos, pvz., teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="99357-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="99357-138">Tačiau produkto dimensijos visada turi atitikti dimensijas komercinėje eilutėje, ir jų keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="99357-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="99357-139">Lauke Kiekis įveskite skaičių, kuris yra didesnis nei dabartinis.</span><span class="sxs-lookup"><span data-stu-id="99357-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="99357-140">Norėdami pamatyti kiekio perskaičiavimo poveikį, pasirinkite komercinę eilutę.</span><span class="sxs-lookup"><span data-stu-id="99357-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="99357-141">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="99357-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="99357-142">Spustelėkite Registruoti važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="99357-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="99357-143">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="99357-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="99357-144">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="99357-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="99357-145">Atkreipkite dėmesį, kad važtaraštis bus sukurtas dviem pristatymo grafiko eilutėms, o ne pradinei užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="99357-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="99357-146">Lauke Spausdinti važtaraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="99357-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="99357-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="99357-147">Click OK.</span></span>
23. <span data-ttu-id="99357-148">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="99357-148">Click Yes.</span></span>
24. <span data-ttu-id="99357-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="99357-149">Close the page.</span></span>


