---
title: Gaunamų prekių apžvalgos profilio nustatymas
description: Šioje temoje aprašyta gaunamų prekių apžvalgos profilio sąranka.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55512c75445a5f3b9c1521376a20d48dd60e22c6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145530"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="fb177-103">Gaunamų prekių apžvalgos profilio nustatymas</span><span class="sxs-lookup"><span data-stu-id="fb177-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="fb177-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="fb177-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="fb177-105">Šioje temoje aprašyta gaunamų prekių apžvalgos profilio sąranka.</span><span class="sxs-lookup"><span data-stu-id="fb177-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="fb177-106">Gaunamų prekių apžvalgos profilis yra rinkinys taisyklių, kurios taikomos, kai vartotojas atidaro puslapį „Gaunamų prekių apžvalga“.</span><span class="sxs-lookup"><span data-stu-id="fb177-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="fb177-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="fb177-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="fb177-108">Šią procedūrą paprastai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="fb177-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="fb177-109">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Paskirstymas > Gaunamų prekių apžvalgos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="fb177-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="fb177-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fb177-110">Select **New**.</span></span> <span data-ttu-id="fb177-111">Beveik visada teks dirbti tame pačiame sandėlyje iškraunant krovinių pilnus sunkvežimius, todėl turėtumėte sukurti gaunamų prekių apžvalgos profilį, kad supaprastintumėte gautų prekių registravimo procesą.</span><span class="sxs-lookup"><span data-stu-id="fb177-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="fb177-112">Lauke **Gaunamų prekių apžvalgos profilio pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb177-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="fb177-113">Lauke **Rodyti eilutes** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fb177-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="fb177-114">Pasirinkite, kurias gaunamų prekių eilutes rodyti:</span><span class="sxs-lookup"><span data-stu-id="fb177-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="fb177-115">**Visos** – rodomos visos eilutės nepriklausomai nuo būsenos.</span><span class="sxs-lookup"><span data-stu-id="fb177-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="fb177-116">**Vykdoma** – rodomos gaunamų prekių, kurių eiga yra Baigta arba Iš dalies, eilutės.</span><span class="sxs-lookup"><span data-stu-id="fb177-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="fb177-117">Tai reiškia, kad kiekvienai eilutei gaunamų prekių žurnale užregistruotas visas kiekis arba dalis kiekio.</span><span class="sxs-lookup"><span data-stu-id="fb177-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="fb177-118">**Nebaigta** – rodomos gaunamų prekių, kurių eiga yra Nėra arba Iš dalies, eilutės.</span><span class="sxs-lookup"><span data-stu-id="fb177-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="fb177-119">Tai reiškia, kad kiekvienai eilutei gavimo žurnale buvo užregistruota dalis kiekio arba kiekio užregistruota nebuvo.</span><span class="sxs-lookup"><span data-stu-id="fb177-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="fb177-120">Išplėskite arba sutraukite skyrių **Gavimo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="fb177-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="fb177-121">Lauke **Dienos, skaičiuojant pirmyn** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb177-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="fb177-122">Nustato filtrą, kad būtų rodomos per artimiausias kelias dienas numatomų gauti gaunamų prekių eilutės (atsižvelgiant į jūsų nustatytą skaičių).</span><span class="sxs-lookup"><span data-stu-id="fb177-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="fb177-123">Lauke **Dienos, skaičiuojant atgal** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb177-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="fb177-124">Nustato filtrą, kad būtų rodomos prieš kelias dienas numatytų gauti gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="fb177-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="fb177-125">Lauke **Sandėliai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb177-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="fb177-126">Filtruokite vieną ar daugiau sandėlių.</span><span class="sxs-lookup"><span data-stu-id="fb177-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="fb177-127">Lauke **Pristatymo būdas** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb177-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="fb177-128">Nustato filtrą, kad būtų rodomos tik šio pristatymo būdo gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="fb177-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="fb177-129">Lauke **Pavadinimas** pasirinkite WHS.</span><span class="sxs-lookup"><span data-stu-id="fb177-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="fb177-130">Lauke **Sandėlys** pasirinkite 24 sandėlį.</span><span class="sxs-lookup"><span data-stu-id="fb177-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="fb177-131">Tai numatytasis sandėlis, kuris bus naudojamas registruotoms šio profilio gaunamų prekių eilutėms.</span><span class="sxs-lookup"><span data-stu-id="fb177-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="fb177-132">Lauke **Vieta** pasirinkite **Galinės durys**.</span><span class="sxs-lookup"><span data-stu-id="fb177-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="fb177-133">Tai numatytoji vieta, kuri bus naudojama registruotoms šio profilio gaunamų prekių eilutėms.</span><span class="sxs-lookup"><span data-stu-id="fb177-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="fb177-134">Išplėskite arba sutraukite skyrių **Gavimo užklausos informacija**.</span><span class="sxs-lookup"><span data-stu-id="fb177-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="fb177-135">Lauke **Apriboti į vietą** pasirinkite 2 vietą.</span><span class="sxs-lookup"><span data-stu-id="fb177-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="fb177-136">Nustato filtrą, kad būtų rodomos tik šios teritorijos gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="fb177-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="fb177-137">Nustatykite parinkties **Pirkimo užsakymai** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fb177-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="fb177-138">Pasirinkite gaunamų prekių eilutes iš pirkimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="fb177-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="fb177-139">Nustatykite parinkties **Perkėlimo užsakymai** nuostatą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fb177-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="fb177-140">Pasirinkite gaunamų prekių eilutes iš perkėlimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="fb177-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="fb177-141">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fb177-141">Select **Save**.</span></span>
18. <span data-ttu-id="fb177-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb177-142">Close the page.</span></span>

