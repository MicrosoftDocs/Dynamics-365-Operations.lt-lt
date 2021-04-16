---
title: Koreguoti atsargų lygius sandėlyje (pagrindinis sandėliavimas)
description: Ši procedūra padės kurti ir registruoti atsargų koregavimo žurnalą, norint pakoreguoti produktų atsargų lygius sandėlyje.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834150"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="8ee3c-103">Koreguoti atsargų lygius sandėlyje (pagrindinis sandėliavimas)</span><span class="sxs-lookup"><span data-stu-id="8ee3c-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ee3c-104">Ši procedūra padės kurti ir registruoti atsargų koregavimo žurnalą, norint pakoreguoti produktų atsargų lygius sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="8ee3c-105">Prieš pradedant atsargų koregavimus, reikia turėti atsargų žurnalo pavadinimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="8ee3c-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8ee3c-107">Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="8ee3c-108">Atsargų koregavimo žurnalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="8ee3c-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="8ee3c-109">Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės > Atsargų koregavimas.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="8ee3c-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-110">Click New.</span></span>
3. <span data-ttu-id="8ee3c-111">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8ee3c-112">Sąraše spustelėkite atsargų koregavimo žurnalo pavadinimą, kurį norite naudoti.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="8ee3c-113">Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų koregavimo žurnalo pavadinimo nustatymą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="8ee3c-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="8ee3c-115">Žurnalo eilučių kūrimas</span><span class="sxs-lookup"><span data-stu-id="8ee3c-115">Create journal lines</span></span>
1. <span data-ttu-id="8ee3c-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-116">Click New.</span></span>
2. <span data-ttu-id="8ee3c-117">Sąraše pažymėkite prekės numerio lauką.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="8ee3c-118">Lauke Prekės numeris pasirinkite prekę.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="8ee3c-119">Jei naudojate demonstracinių duomenų įmonės USMF, įveskite „D0001“.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="8ee3c-120">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8ee3c-121">Sąraše pasirinkite vietą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-121">In the list, select a site.</span></span>
6. <span data-ttu-id="8ee3c-122">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8ee3c-123">Sąraše pasirinkite sandėlį.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="8ee3c-124">Jei pasirinkote prekę, kurios privaloma dimensija Vieta, čia turėtumėte nurodyti vietą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="8ee3c-125">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8ee3c-126">Savikainos lauke nurodoma vieneto kaina, skirta atsargų gavimams.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="8ee3c-127">Jei prekės numerio savikaina nenurodyta arba, jei norėjote ją pakeisti neautomatiniu būdu, padarykite tai čia.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="8ee3c-128">Atsargų koregavimo žurnalo tikrinimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="8ee3c-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="8ee3c-129">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-129">Click Validate.</span></span>
2. <span data-ttu-id="8ee3c-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-130">Click OK.</span></span>
3. <span data-ttu-id="8ee3c-131">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-131">Click Post.</span></span>
    * <span data-ttu-id="8ee3c-132">Registruojant tokį žurnalą, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="8ee3c-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-133">Click OK.</span></span>
5. <span data-ttu-id="8ee3c-134">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-134">Close the form.</span></span>
6. <span data-ttu-id="8ee3c-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ee3c-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]