---
title: Kurti naują prekybos sutartį
description: Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a964b357ac9abb65cd097b084630a53f1553ad04
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146552"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="91fba-103">Kurti naują prekybos sutartį</span><span class="sxs-lookup"><span data-stu-id="91fba-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91fba-104">Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu.</span><span class="sxs-lookup"><span data-stu-id="91fba-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="91fba-105">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="91fba-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="91fba-106">Jei naudojate savo duomenis, prieš pradėdami šį vadovą turite įsitikinti, kad egzistuoja prekybos sutarčių žurnalo pavadinimas, kai numatytasis ryšys nustatytas kaip „Kaina (pardavimai)“.</span><span class="sxs-lookup"><span data-stu-id="91fba-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="91fba-107">Kurti ir registruoti naują prekybos sutarčių žurnalą</span><span class="sxs-lookup"><span data-stu-id="91fba-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="91fba-108">Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Kainos ir nuolaidos > Prekybos sutarčių žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="91fba-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="91fba-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="91fba-109">Click **New**.</span></span>
3. <span data-ttu-id="91fba-110">Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="91fba-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="91fba-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="91fba-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="91fba-112">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="91fba-112">On **Action pane**, click **Lines**.</span></span>
6. <span data-ttu-id="91fba-113">Lauke **Sąskaitos kodas** pasirinkite Lentelė.</span><span class="sxs-lookup"><span data-stu-id="91fba-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="91fba-114">Šiame pavyzdyje atnaujinate kainą konkrečiam klientui – tai reiškia, kad turite pasirinkti „Lentelė“.</span><span class="sxs-lookup"><span data-stu-id="91fba-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="91fba-115">Jei norėtumėte atnaujinti produkto kainų sąrašą, reikėtų rinktis Visi, kad naujoji kaina galiotų visiems klientams.</span><span class="sxs-lookup"><span data-stu-id="91fba-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="91fba-116">Jei norėtumėte diferencijuoti kainą skirtingiems klientų segmentams, tada reikėtų rinktis „Grupė“.</span><span class="sxs-lookup"><span data-stu-id="91fba-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="91fba-117">Norėdami pasirinkti „Grupė“, turite nustatyti klientų kainų grupes.</span><span class="sxs-lookup"><span data-stu-id="91fba-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="91fba-118">Lauke **Sąskaitos pasirinkimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="91fba-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="91fba-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="91fba-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="91fba-120">Lauke **Prekės kodas** pasirinkite Lentelė.</span><span class="sxs-lookup"><span data-stu-id="91fba-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="91fba-121">Kai įvedate Kaina (pardavimai) tipo prekybos sutartį, lauke **Prekės kodas** turite pasirinkti tik Lentelė.</span><span class="sxs-lookup"><span data-stu-id="91fba-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="91fba-122">Taip yra todėl, kad kaina yra absoliučioji reikšmė ir negali būti tokia pati visiems produktams ar produktų grupėms.</span><span class="sxs-lookup"><span data-stu-id="91fba-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="91fba-123">Lauke **Prekės ryšys** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="91fba-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="91fba-124">Sąraše pasirinkite produktą, kurį norite įtraukti į sutartį.</span><span class="sxs-lookup"><span data-stu-id="91fba-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="91fba-125">Užsirašykite, kokį produktą pasirinkote.</span><span class="sxs-lookup"><span data-stu-id="91fba-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="91fba-126">Lauke **Nuo** įveskite mažiausią kiekį.</span><span class="sxs-lookup"><span data-stu-id="91fba-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="91fba-127">Jei klientas turi užsakyti minimalų kiekį, kad jam būtų pasiūlyta nauja kaina, šį kiekį turite nurodyti čia.</span><span class="sxs-lookup"><span data-stu-id="91fba-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="91fba-128">Įveskite reikšmę lauke **Iki**, kad nurodytumėte didžiausią kiekį, kurį viršijus sutarties kaina negalios.</span><span class="sxs-lookup"><span data-stu-id="91fba-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="91fba-129">Jei siūlote kainas ir nuolaidas skirtingoms kiekių riboms, kiekvieną kiekio grupę nurodykite kaip mažiausią ir didžiausią kiekį laukuose **Nuo** ir **Iki**.</span><span class="sxs-lookup"><span data-stu-id="91fba-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="91fba-130">Lauke **Suma valiuta** įveskite kainą.</span><span class="sxs-lookup"><span data-stu-id="91fba-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="91fba-131">Skyriaus **Išsamiai** lauke **Pradžios data** įveskite datą, nuo kurios pradės galioti ši sutartis.</span><span class="sxs-lookup"><span data-stu-id="91fba-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="91fba-132">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="91fba-132">Click **Save**.</span></span>
16. <span data-ttu-id="91fba-133">Spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="91fba-133">Click **Validate**.</span></span>
17. <span data-ttu-id="91fba-134">Spustelėkite **Tikrinti pasirinktas eilutes**.</span><span class="sxs-lookup"><span data-stu-id="91fba-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="91fba-135">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91fba-135">Click **OK**.</span></span>
19. <span data-ttu-id="91fba-136">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="91fba-136">Click **Post**.</span></span>
20. <span data-ttu-id="91fba-137">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="91fba-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="91fba-138">Peržiūrėti produkto prekybos sutartis</span><span class="sxs-lookup"><span data-stu-id="91fba-138">View trade agreements for a product</span></span>
1. <span data-ttu-id="91fba-139">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="91fba-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="91fba-140">Sąraše raskite ir pasirinkite produktą, kurio kainą ką tik atnaujinote.</span><span class="sxs-lookup"><span data-stu-id="91fba-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="91fba-141">**Veiksmų srityje** spustelėkite **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="91fba-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="91fba-142">Spustelėkite **Peržiūrėti prekybos sutartis**.</span><span class="sxs-lookup"><span data-stu-id="91fba-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="91fba-143">Peržiūrėkite kainos prekybos sutarties informaciją, kurią ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="91fba-143">Review the details of the price trade agreement you have just created.</span></span>    

5. <span data-ttu-id="91fba-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="91fba-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91fba-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="91fba-145">Additional resources</span></span>
### <a name="community-blogs"></a><span data-ttu-id="91fba-146">Bendruomenės tinklaraščiai</span><span class="sxs-lookup"><span data-stu-id="91fba-146">Community blogs</span></span>
- [<span data-ttu-id="91fba-147">Pardavimo kainos „Dynamics 365 for Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="91fba-147">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
