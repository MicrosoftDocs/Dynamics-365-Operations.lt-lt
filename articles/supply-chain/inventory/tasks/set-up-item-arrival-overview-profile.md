---
title: Nustatyti gaunamų prekių apžvalgos profilį
description: Šios užduoties tikslas yra nustatyti gaunamų prekių apžvalgos profilį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555114"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="23218-103">Nustatyti gaunamų prekių apžvalgos profilį</span><span class="sxs-lookup"><span data-stu-id="23218-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23218-104">Šios užduoties tikslas yra nustatyti gaunamų prekių apžvalgos profilį.</span><span class="sxs-lookup"><span data-stu-id="23218-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="23218-105">Gaunamų prekių apžvalgos profilis yra rinkinys taisyklių, kurios taikomos, kai vartotojas atidaro puslapį „Gaunamų prekių apžvalga“.</span><span class="sxs-lookup"><span data-stu-id="23218-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="23218-106">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="23218-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="23218-107">Šią procedūrą paprastai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="23218-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="23218-108">Pasirinkite Atsargų valdymas > Nustatymas > Paskirstymas > Gaunamų prekių apžvalgos profiliai.</span><span class="sxs-lookup"><span data-stu-id="23218-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="23218-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="23218-109">Click New.</span></span>
    * <span data-ttu-id="23218-110">Beveik visada teks dirbti tame pačiame sandėlyje iškraunant krovinių pilnus sunkvežimius, todėl turėtumėte sukurti gaunamų prekių apžvalgos profilį, kad supaprastintumėte gautų prekių registravimo procesą.</span><span class="sxs-lookup"><span data-stu-id="23218-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="23218-111">Lauke „Gaunamų prekių apžvalgos profilio pavadinimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23218-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="23218-112">Lauke „Rodyti eilutes“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="23218-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="23218-113">Pasirinkite, kurias gaunamų prekių eilutes rodyti: Visos – rodyti visas eilutes, neatsižvelgiant į būseną.</span><span class="sxs-lookup"><span data-stu-id="23218-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="23218-114">Vykdoma – rodyti gaunamų prekių eilutes, kurių vykdymo būsena yra „Baigta“ arba „Iš dalies“.</span><span class="sxs-lookup"><span data-stu-id="23218-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="23218-115">Tai reiškia, kad kiekvienai eilutei gaunamų prekių žurnale užregistruotas visas kiekis arba dalis kiekio.</span><span class="sxs-lookup"><span data-stu-id="23218-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="23218-116">Nebaigta – rodyti gaunamų prekių eilutes, kurių vykdymo būsena yra „Nėra“ arba „Iš dalies“.</span><span class="sxs-lookup"><span data-stu-id="23218-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="23218-117">Tai reiškia, kad kiekvienai eilutei gavimo žurnale buvo užregistruota dalis kiekio arba kiekio užregistruota nebuvo.</span><span class="sxs-lookup"><span data-stu-id="23218-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="23218-118">Išplėskite arba sutraukite skyrių Gavimo parinktys.</span><span class="sxs-lookup"><span data-stu-id="23218-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="23218-119">Lauke „Dienos nuo šiandienos“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23218-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="23218-120">Nustato filtrą, kad būtų rodomos per artimiausias kelias dienas numatomų gauti gaunamų prekių eilutės (atsižvelgiant į jūsų nustatytą skaičių).</span><span class="sxs-lookup"><span data-stu-id="23218-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="23218-121">Lauke „Dienos iki šiandienos“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23218-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="23218-122">Nustato filtrą, kad būtų rodomos prieš kelias dienas numatytų gauti gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="23218-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="23218-123">Lauke „Sandėliai“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23218-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="23218-124">Filtruokite vieną ar daugiau sandėlių.</span><span class="sxs-lookup"><span data-stu-id="23218-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="23218-125">Lauke Pristatymo būdas pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="23218-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="23218-126">Nustato filtrą, kad būtų rodomos tik šio pristatymo būdo gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="23218-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="23218-127">Lauke Pavadinimas pasirinkite WHS.</span><span class="sxs-lookup"><span data-stu-id="23218-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="23218-128">Lauke Sandėlis pasirinkite 24-ąjį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="23218-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="23218-129">Tai numatytasis sandėlis, kuris bus naudojamas registruotoms šio profilio gaunamų prekių eilutėms.</span><span class="sxs-lookup"><span data-stu-id="23218-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="23218-130">Lauke Vieta pasirinkite Baydoor.</span><span class="sxs-lookup"><span data-stu-id="23218-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="23218-131">Tai numatytoji vieta, kuri bus naudojama registruotoms šio profilio gaunamų prekių eilutėms.</span><span class="sxs-lookup"><span data-stu-id="23218-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="23218-132">Išplėskite arba sutraukite skyrių Gavimo užklausos informacija.</span><span class="sxs-lookup"><span data-stu-id="23218-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="23218-133">Lauke Apribota teritorija pasirinkite 2-ąją teritoriją.</span><span class="sxs-lookup"><span data-stu-id="23218-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="23218-134">Nustato filtrą, kad būtų rodomos tik šios teritorijos gaunamų prekių eilutės.</span><span class="sxs-lookup"><span data-stu-id="23218-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="23218-135">Nustatykite parinktį Pirkimo užsakymai į Taip.</span><span class="sxs-lookup"><span data-stu-id="23218-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="23218-136">Pasirinkite gaunamų prekių eilutes iš pirkimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="23218-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="23218-137">Nustatykite parinktį Perkėlimo užsakymai į Taip.</span><span class="sxs-lookup"><span data-stu-id="23218-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="23218-138">Pasirinkite gaunamų prekių eilutes iš perkėlimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="23218-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="23218-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="23218-139">Click Save.</span></span>
18. <span data-ttu-id="23218-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="23218-140">Close the page.</span></span>

