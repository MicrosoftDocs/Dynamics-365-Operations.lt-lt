---
title: Sandėlio atsargų skaičiavimas
description: Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 452822eaf26c26e4c9e00f909dbd18127f6fc781
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230109"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="66d23-103">Sandėlio atsargų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="66d23-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66d23-104">Ši procedūra padės kurti ir registruoti atsargų inventorizacijos žurnalą, norint suskaičiuoti tam tikrą prekę tam tikros teritorijos sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="66d23-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="66d23-105">Procedūra taikoma „pagrindinio sandėliavimo“ funkcijai, kuri galima Atsargų valdymo modulyje, o ne sandėliavimo funkcijai, kuri galima Sandėlio valdymo modulyje.</span><span class="sxs-lookup"><span data-stu-id="66d23-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="66d23-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="66d23-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="66d23-107">Jei naudojate savo duomenis, įsitikinkite, kad nustatėte produktus ir teritorijas ir kad sukūrėte atsargų žurnalo pavadinimą, skirtą skaičiavimo žurnalams.</span><span class="sxs-lookup"><span data-stu-id="66d23-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="66d23-108">Atsargų inventorizaciją paprastai atlieka sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="66d23-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="66d23-109">Kurti atsargų inventorizacijos žurnalą</span><span class="sxs-lookup"><span data-stu-id="66d23-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="66d23-110">Valdymo skiltyje pasirinkite **Naršymo sritis > Moduliai > Atsargų valdymas > Žurnalo įrašai > Prekės skaičiavimas > Skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="66d23-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="66d23-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="66d23-111">Select **New**.</span></span>
3. <span data-ttu-id="66d23-112">Lauke **Pavadinimas** paspauskite išplečiamąjį mygtuką, kad pasirinktumėte atsargų inventorizacijos žurnalo pavadinimą, kurį norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="66d23-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="66d23-113">Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų inventorizacijos žurnalo pavadinimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="66d23-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="66d23-114">Lauke **Darbuotojas** spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="66d23-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="66d23-115">Iš sąrašo **Pasirinkti** naudotiną darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="66d23-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="66d23-116">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="66d23-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="66d23-117">Kurti žurnalo eilutes</span><span class="sxs-lookup"><span data-stu-id="66d23-117">Create journal lines</span></span>
1. <span data-ttu-id="66d23-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="66d23-118">Select **New**.</span></span>
2. <span data-ttu-id="66d23-119">Lauke **Prekės numeris** pasirinkite norimą įrašą išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="66d23-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="66d23-120">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite **A0001**.</span><span class="sxs-lookup"><span data-stu-id="66d23-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="66d23-121">Lauke **Puslapis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="66d23-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="66d23-122">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite teritoriją **2**.</span><span class="sxs-lookup"><span data-stu-id="66d23-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="66d23-123">Lauke **Sandėlis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="66d23-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="66d23-124">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite sandėlį **24**.</span><span class="sxs-lookup"><span data-stu-id="66d23-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="66d23-125">Skirtuke **Vieta** iš išplečiamojo sąrašo pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="66d23-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="66d23-126">Jei naudojate demonstracinių duomenų įmonės USMF, pasirinkite vietą **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="66d23-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="66d23-127">Lauke Suskaičiuota įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="66d23-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="66d23-128">Jei įvesite apskaičiuotą numerį, kuris skiriasi nuo lauke **Turimos atsargos** rodomo skaičiaus, laukas **Kiekis** bus atnaujintas ir rodys neatitikimą.</span><span class="sxs-lookup"><span data-stu-id="66d23-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="66d23-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="66d23-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="66d23-130">Užregistruoti atsargų inventorizacijos žurnalą</span><span class="sxs-lookup"><span data-stu-id="66d23-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="66d23-131">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="66d23-131">Select **Post**.</span></span> <span data-ttu-id="66d23-132">Kai registruojate atsargų inventorizacijos žurnalą, jei apskaičiuota suma skiriasi nuo sumos, kuri pateikta lauke **Turimos atsargos**, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.</span><span class="sxs-lookup"><span data-stu-id="66d23-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="66d23-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="66d23-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="66d23-134">Peržiūrėti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="66d23-134">View inventory transactions</span></span>
1. <span data-ttu-id="66d23-135">Pasirinkite **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="66d23-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="66d23-136">Pasirinkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="66d23-136">Select **Transactions**.</span></span> <span data-ttu-id="66d23-137">Čia galite pamatyti visas susijusias operacijas, kurios bus sukurtos registruojant atsargų inventorizacijos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="66d23-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]