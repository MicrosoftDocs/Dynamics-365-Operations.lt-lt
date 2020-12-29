---
title: Inicijuoti atsargų lygius sandėlyje
description: Ši procedūra nurodo, kaip atnaujinti turimas atsargas rankiniu būdu, naudojant atsargų perkėlimo žurnalą.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03481ddc5bd12b3459b69d65b1cfaeb23c60dfd4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433855"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="b8381-103">Inicijuoti atsargų lygius sandėlyje</span><span class="sxs-lookup"><span data-stu-id="b8381-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8381-104">Ši procedūra nurodo, kaip atnaujinti turimas atsargas rankiniu būdu, naudojant atsargų perkėlimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b8381-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="b8381-105">(Turimas atsargas taip pat galima atnaujinti importuojant duomenų objektų operacijas.) Šį vadovą galite paleisti naudodami demonstracinių duomenų įmonę USMF, kurioje pateikiami visi būtinieji komponentai, pvz., žurnalo pavadinimas, prekių nustatymai, registravimo šablonai ir sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="b8381-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="b8381-106">Vadovas siūlo konkrečias naudojamos prekės ir dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b8381-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="b8381-107">Jei pasirinksite kitą prekę, gali reikėti įvesti kitų dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b8381-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="b8381-108">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės > Perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="b8381-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="b8381-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b8381-109">Click New.</span></span>
3. <span data-ttu-id="b8381-110">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8381-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b8381-111">Pasirinkite IMov.</span><span class="sxs-lookup"><span data-stu-id="b8381-111">Select IMov.</span></span>
    * <span data-ttu-id="b8381-112">Kitais verslo tikslais pravartu naudoti kitus žurnalo pavadinimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="b8381-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="b8381-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8381-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b8381-114">Lauke Korespondentinė sąskaita nurodykite reikšmes „140200“.</span><span class="sxs-lookup"><span data-stu-id="b8381-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="b8381-115">Ši korespondentinė sąskaita bus numatytoji žurnalo eilučių sąskaita.</span><span class="sxs-lookup"><span data-stu-id="b8381-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="b8381-116">Galima perrašyti numatytąją reikšmę ir eilutėms priskirti kitas korespondentines sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="b8381-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="b8381-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8381-117">Click OK.</span></span>
8. <span data-ttu-id="b8381-118">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b8381-118">Click New.</span></span>
9. <span data-ttu-id="b8381-119">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8381-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b8381-120">Pasirinkite prekę A0001.</span><span class="sxs-lookup"><span data-stu-id="b8381-120">Select item A0001.</span></span>
11. <span data-ttu-id="b8381-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8381-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b8381-122">Spustelėkite skirtuką Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="b8381-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="b8381-123">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8381-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b8381-124">Pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="b8381-124">Select site 1.</span></span>
15. <span data-ttu-id="b8381-125">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8381-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="b8381-126">Pasirinkite 13 sandėlį.</span><span class="sxs-lookup"><span data-stu-id="b8381-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="b8381-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b8381-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="b8381-128">Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b8381-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b8381-129">Pasirinkite 13 vietą.</span><span class="sxs-lookup"><span data-stu-id="b8381-129">Select location 13.</span></span>
20. <span data-ttu-id="b8381-130">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b8381-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="b8381-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b8381-131">Click Save.</span></span>
22. <span data-ttu-id="b8381-132">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="b8381-132">Click Post.</span></span>
23. <span data-ttu-id="b8381-133">Pažymėkite arba atžymėkite žymės langelį Perkelti visas registravimo klaidas į naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b8381-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="b8381-134">Jei įgalinsite šią parinktį, visos eilutės, kurių nepavyksta registruoti, bus nukopijuotos į naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b8381-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="b8381-135">Pasinaudodami žurnale esančia informacija galite ištaisyti klaidas ir iš naujo registruoti eilutes.</span><span class="sxs-lookup"><span data-stu-id="b8381-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="b8381-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b8381-136">Click OK.</span></span>
25. <span data-ttu-id="b8381-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8381-137">Close the page.</span></span>
26. <span data-ttu-id="b8381-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b8381-138">Close the page.</span></span>

