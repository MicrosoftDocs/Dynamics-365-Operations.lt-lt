--- 
title: "Siųsti pardavimo užsakymus be sandėliavimo"
description: "Šiame vadove parodoma, kaip naujinti pardavimo užsakymą, kai produktai siunčiami klientui."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f1b9dd4b99bcbcc6cfbc5cfd8e3271fa80c628c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="51199-103">Siųsti pardavimo užsakymus be sandėliavimo</span><span class="sxs-lookup"><span data-stu-id="51199-103">Ship sales orders without warehousing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51199-104">Šiame vadove parodoma, kaip naujinti pardavimo užsakymą, kai produktai siunčiami klientui.</span><span class="sxs-lookup"><span data-stu-id="51199-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="51199-105">Vadovas taikomas vykdymo eigai, kuri nenustatyta sandėlio valdymui (nei pagrindiniam, nei papildomam sandėliui), ir todėl prieš siunčiant nereikia užregistruoti produkto išrinkimo.</span><span class="sxs-lookup"><span data-stu-id="51199-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="51199-106">Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="51199-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="51199-107">Abiem atvejais, prieš pradėdami šią užduotį, sukurkite inventorizuoto produkto, kurio kiekis didesnis negu 1, pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="51199-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="51199-108">Norėdami išvengti registravimo klaidos, turite patikrinti, ar šiuo metu užsakyme pasirinktoje vietoje ir sandėlyje turimo produkto kiekis sutampa su užsakymo kiekiu.</span><span class="sxs-lookup"><span data-stu-id="51199-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="51199-109">Užsakymo važtaraščio registravimas</span><span class="sxs-lookup"><span data-stu-id="51199-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="51199-110">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="51199-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="51199-111">Sąraše raskite ir pasirinkite šiai užduočiai sukurtą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="51199-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="51199-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="51199-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="51199-113">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="51199-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="51199-114">Spustelėkite Registruoti važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="51199-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="51199-115">Išplėskite arba sutraukite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="51199-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="51199-116">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="51199-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="51199-117">Kitos pasirinktys yra Pristatyti dabar arba Išrinkta.</span><span class="sxs-lookup"><span data-stu-id="51199-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="51199-118">Jei užsakymo eilutė siunčiama iš dalies, o užsakymo eilutės lauke Pristatyti dabar nurodytas kiekis, pasirinkite Pristatyti dabar.</span><span class="sxs-lookup"><span data-stu-id="51199-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="51199-119">Jei jūsų organizacijos vykdymo eigoje išrinkimas nurodytas kaip atskiras procesas, kuris valdomas ir registruojamas naudojant išrinkimo dokumentą, pasirinkite Išrinkta.</span><span class="sxs-lookup"><span data-stu-id="51199-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="51199-120">Patikrinkite, ar nustatyta parinkties Registravimas padėtis Taip.</span><span class="sxs-lookup"><span data-stu-id="51199-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="51199-121">Nustatykite pasirinkties Važtaraščio spausdinimas padėtį Taip.</span><span class="sxs-lookup"><span data-stu-id="51199-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="51199-122">Skirtuke Peržiūra yra atliekant šį registravimą turimų sugeneruoti važtaraščių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="51199-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="51199-123">Jei siunčiate individualų užsakymą, paprastai būna vienas važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="51199-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="51199-124">Tačiau jei to užsakymo eilutės turi būti siunčiamos iš skirtingų vietų, registravimas bus automatiškai padalintas į atitinkamą skaičių dokumentų.</span><span class="sxs-lookup"><span data-stu-id="51199-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="51199-125">Tai būtina sąlyga, kurios negalima keisti.</span><span class="sxs-lookup"><span data-stu-id="51199-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="51199-126">Be to, jei užsakymo eilutės turi būti siunčiamos skirtingais pristatymo adresais, o siuntimo strategijoje nustatyta, kad būtų reikalaujama padalinimo, registravimas bus taip pat padalintas į keletą dokumentų.</span><span class="sxs-lookup"><span data-stu-id="51199-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="51199-127">Skirtuke Eilutės pasirinkite siunčiamos užsakymo eilutės eilutę.</span><span class="sxs-lookup"><span data-stu-id="51199-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="51199-128">Lauke Atnaujinti įveskite už pradinio kiekio skaičių mažesnį skaičių.</span><span class="sxs-lookup"><span data-stu-id="51199-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="51199-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="51199-129">Click OK.</span></span>
12. <span data-ttu-id="51199-130">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="51199-130">Click Yes.</span></span>
13. <span data-ttu-id="51199-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51199-131">Close the page.</span></span>
14. <span data-ttu-id="51199-132">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="51199-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="51199-133">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="51199-133">Click Change view.</span></span>
16. <span data-ttu-id="51199-134">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="51199-134">Click Header view.</span></span>
    * <span data-ttu-id="51199-135">Jei visos užsakymo eilutės buvo visiškai išsiųstos, užsakymo būsena pasikeičia iš Atvira į Pristatyta.</span><span class="sxs-lookup"><span data-stu-id="51199-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="51199-136">Šiame pavyzdyje užsakymo eilutė išsiųsta iš dalies.</span><span class="sxs-lookup"><span data-stu-id="51199-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="51199-137">Todėl užsakymo būsena išlieka Atidarytas.</span><span class="sxs-lookup"><span data-stu-id="51199-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="51199-138">Nustatyta lauko Dokumento būsena padėtis Važtaraštis, nes išsiųsta bent viena užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="51199-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="51199-139">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="51199-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="51199-140">Spustelėkite Eilutės kiekis.</span><span class="sxs-lookup"><span data-stu-id="51199-140">Click Line quantity.</span></span>
19. <span data-ttu-id="51199-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="51199-141">Close the page.</span></span>
20. <span data-ttu-id="51199-142">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="51199-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="51199-143">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="51199-143">Click Packing slip.</span></span>
    * <span data-ttu-id="51199-144">Puslapyje Važtaraščio žurnalas pateikiami visi jūsų užsakymui sugeneruoti važtaraščio dokumentai.</span><span class="sxs-lookup"><span data-stu-id="51199-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="51199-145">Galite peržiūrėti kiekvieno dokumento informaciją ir, jei norite, ją atsispausdinti.</span><span class="sxs-lookup"><span data-stu-id="51199-145">You can review details of each document and print them, if you wish.</span></span>  


