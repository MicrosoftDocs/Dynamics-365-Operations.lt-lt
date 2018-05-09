--- 
title: "Kurti naują prekybos sutartį"
description: "Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d0e5c5d680fcbac5407883a1d6365a4f312dda9
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="70547-103">Kurti naują prekybos sutartį</span><span class="sxs-lookup"><span data-stu-id="70547-103">Create a new trade agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70547-104">Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu.</span><span class="sxs-lookup"><span data-stu-id="70547-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="70547-105">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="70547-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="70547-106">Jei naudojate savo duomenis, prieš pradėdami šį vadovą turite įsitikinti, kad egzistuoja prekybos sutarčių žurnalo pavadinimas, kai numatytasis ryšys nustatytas kaip „Kaina (pardavimai)“.</span><span class="sxs-lookup"><span data-stu-id="70547-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="70547-107">Kurti ir registruoti naują prekybos sutarčių žurnalą</span><span class="sxs-lookup"><span data-stu-id="70547-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="70547-108">Eikite į Pardavimas ir rinkodara > Kainos ir nuolaidos > Prekybos sutarčių žurnalai.</span><span class="sxs-lookup"><span data-stu-id="70547-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="70547-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="70547-109">Click New.</span></span>
3. <span data-ttu-id="70547-110">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="70547-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="70547-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="70547-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="70547-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="70547-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="70547-113">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="70547-113">Click Lines.</span></span>
7. <span data-ttu-id="70547-114">Lauke „Sąskaitos kodas“ pasirinkite „Lentelė“.</span><span class="sxs-lookup"><span data-stu-id="70547-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="70547-115">Šiame pavyzdyje atnaujinate kainą konkrečiam klientui – tai reiškia, kad turite pasirinkti „Lentelė“.</span><span class="sxs-lookup"><span data-stu-id="70547-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="70547-116">Jei norėtumėte atnaujinti produkto kainų sąrašą, reikėtų rinktis „Visi“, kad naujoji kaina galiotų visiems klientams.</span><span class="sxs-lookup"><span data-stu-id="70547-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="70547-117">Jei norėtumėte diferencijuoti kainą skirtingiems klientų segmentams, tada reikėtų rinktis „Grupė“.</span><span class="sxs-lookup"><span data-stu-id="70547-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="70547-118">Norėdami pasirinkti „Grupė“, turite nustatyti klientų kainų grupes.</span><span class="sxs-lookup"><span data-stu-id="70547-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="70547-119">Lauke „Sąskaitos pasirinkimas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="70547-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="70547-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="70547-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="70547-121">Lauke „Prekės kodas“ pasirinkite „Lenetelė“.</span><span class="sxs-lookup"><span data-stu-id="70547-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="70547-122">Kai įvedate „Kaina (pardavimai)“ tipo prekybos sutartį, turite pasirinkti tik „Lentelė“ lauke „Prekės kodas“.</span><span class="sxs-lookup"><span data-stu-id="70547-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="70547-123">Taip yra todėl, kad kaina yra absoliučioji reikšmė ir negali būti tokia pati visiems produktams ar produktų grupėms.</span><span class="sxs-lookup"><span data-stu-id="70547-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="70547-124">Lauke „Prekės ryšys“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="70547-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="70547-125">Sąraše pasirinkite produktą, kurį norite įtraukti į sutartį.</span><span class="sxs-lookup"><span data-stu-id="70547-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="70547-126">Užsirašykite, kokį produktą pasirinkote.</span><span class="sxs-lookup"><span data-stu-id="70547-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="70547-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="70547-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="70547-128">Lauke „Nuo“ įveskite mažiausią kiekį.</span><span class="sxs-lookup"><span data-stu-id="70547-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="70547-129">Jei klientas turi užsakyti minimalų kiekį, kad jam būtų pasiūlyta nauja kaina, šį kiekį turite nurodyti čia.</span><span class="sxs-lookup"><span data-stu-id="70547-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="70547-130">Įveskite reikšmę lauke „Iki“, kad nurodytumėte didžiausią kiekį, kurį viršijus sutarties kaina negalios.</span><span class="sxs-lookup"><span data-stu-id="70547-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="70547-131">Jei siūlote kainas ir nuolaidas skirtingoms kiekių riboms, kiekvieną kiekio grupę nurodykite kaip mažiausią ir didžiausią kiekį laukuose „Nuo“ ir „Iki“.</span><span class="sxs-lookup"><span data-stu-id="70547-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="70547-132">Lauke „Suma valiuta“ įveskite kainą.</span><span class="sxs-lookup"><span data-stu-id="70547-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="70547-133">Lauke „Pradžios data“ įveskite datą, nuo kurios pradės galioti ši sutartis.</span><span class="sxs-lookup"><span data-stu-id="70547-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="70547-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="70547-134">Click Save.</span></span>
18. <span data-ttu-id="70547-135">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="70547-135">Click Validate.</span></span>
19. <span data-ttu-id="70547-136">Spustelėkite „Tikrinti pasirinktas eilutes“.</span><span class="sxs-lookup"><span data-stu-id="70547-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="70547-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="70547-137">Click OK.</span></span>
21. <span data-ttu-id="70547-138">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="70547-138">Click Post.</span></span>
22. <span data-ttu-id="70547-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="70547-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="70547-140">Peržiūrėti produkto prekybos sutartis</span><span class="sxs-lookup"><span data-stu-id="70547-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="70547-141">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="70547-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="70547-142">Sąraše raskite ir pasirinkite produktą, kurio kainą ką tik atnaujinote.</span><span class="sxs-lookup"><span data-stu-id="70547-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="70547-143">Veiksmų srityje spustelėkite Parduoti.</span><span class="sxs-lookup"><span data-stu-id="70547-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="70547-144">Spustelėkite „Peržiūrėti prekybos sutartis“.</span><span class="sxs-lookup"><span data-stu-id="70547-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="70547-145">Peržiūrėkite kainos prekybos sutarties informaciją, kurią ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="70547-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="70547-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="70547-146">Close the page.</span></span>


