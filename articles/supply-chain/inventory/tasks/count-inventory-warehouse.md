---
title: Skaičiuoti sandėlio atsargas
description: Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "353476"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="818df-103">Skaičiuoti sandėlio atsargas</span><span class="sxs-lookup"><span data-stu-id="818df-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="818df-104">Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="818df-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="818df-105">Procedūra taikoma „pagrindinio sandėliavimo“ funkcijai, kuri galima Atsargų valdymo modulyje, o ne sandėliavimo funkcijai, kuri galima Sandėlio valdymo modulyje.</span><span class="sxs-lookup"><span data-stu-id="818df-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="818df-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="818df-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="818df-107">Jei naudojate savo duomenis, įsitikinkite, kad nustatėte produktus ir teritorijas ir kad sukūrėte atsargų žurnalo pavadinimą, skirtą skaičiavimo žurnalams.</span><span class="sxs-lookup"><span data-stu-id="818df-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="818df-108">Atsargų inventorizaciją paprastai atlieka sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="818df-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="818df-109">Kurti atsargų inventorizacijos žurnalą</span><span class="sxs-lookup"><span data-stu-id="818df-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="818df-110">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės skaičiavimas > Skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="818df-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="818df-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="818df-111">Click New.</span></span>
3. <span data-ttu-id="818df-112">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="818df-113">Sąraše spustelėkite atsargų inventorizacijos žurnalo pavadinimą, kurį norite naudoti</span><span class="sxs-lookup"><span data-stu-id="818df-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="818df-114">Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų inventorizacijos žurnalo pavadinimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="818df-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="818df-115">Lauke Darbuotojas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="818df-116">Iš sąrašo pasirinkite naudotiną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="818df-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="818df-117">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="818df-117">Click Select.</span></span>
8. <span data-ttu-id="818df-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="818df-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="818df-119">Žurnalo eilučių kūrimas</span><span class="sxs-lookup"><span data-stu-id="818df-119">Create journal lines</span></span>
1. <span data-ttu-id="818df-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="818df-120">Click New.</span></span>
2. <span data-ttu-id="818df-121">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="818df-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818df-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818df-123">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="818df-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="818df-124">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="818df-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818df-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818df-126">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite teritoriją '2'.</span><span class="sxs-lookup"><span data-stu-id="818df-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="818df-127">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="818df-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818df-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818df-129">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite sandėlį '24'.</span><span class="sxs-lookup"><span data-stu-id="818df-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="818df-130">Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="818df-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="818df-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="818df-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="818df-132">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite vietą 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="818df-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="818df-133">Lauke Suskaičiuota įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="818df-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="818df-134">Jei įvesite apskaičiuotą numerį, kuris skiriasi nuo lauke Turimos atsargos rodomo skaičiaus, laukas Kiekis bus atnaujintas ir rodys neatitikimą.</span><span class="sxs-lookup"><span data-stu-id="818df-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="818df-135">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="818df-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="818df-136">Užregistruoti atsargų inventorizacijos žurnalą</span><span class="sxs-lookup"><span data-stu-id="818df-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="818df-137">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="818df-137">Click Post.</span></span>
    * <span data-ttu-id="818df-138">Kai registruojate atsargų inventorizacijos žurnalą, jei apskaičiuota suma skiriasi nuo sumos, kuri pateikta lauke Turimos atsargos, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.</span><span class="sxs-lookup"><span data-stu-id="818df-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="818df-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="818df-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="818df-140">Peržiūrėti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="818df-140">View inventory transactions</span></span>
1. <span data-ttu-id="818df-141">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="818df-141">Click Inventory.</span></span>
2. <span data-ttu-id="818df-142">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="818df-142">Click Transactions.</span></span>
    * <span data-ttu-id="818df-143">Čia galite pamatyti visas susijusias operacijas, kurios bus sukurtos registruojant atsargų inventorizacijos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="818df-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

