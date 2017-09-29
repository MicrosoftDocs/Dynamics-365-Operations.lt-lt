--- 
title: "Apdoroti priminimo laiškus"
description: "Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="becec-103">Apdoroti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="becec-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="becec-104">Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="becec-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="becec-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="becec-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="becec-106">Registravimo šablone nustatykite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="becec-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="becec-107">Pasirinkite Kreditas ir rinkiniai > Sąranka > Klientų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="becec-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="becec-108">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="becec-108">Click Edit.</span></span>
    * <span data-ttu-id="becec-109">Išplečiamajame sąraše pasirinkite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="becec-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="becec-110">Jei nenorite generuoti operacijų priminimo laiškų naudodami šį registravimo šabloną, palikite lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="becec-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="becec-111">Naudojant lentelių apribojimų skirtuką galite keisti būdą, kuriuo apdorojami priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="becec-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="becec-112">Jei šio lauko reikšmė nustatyta kaip Taip, bus kuriami šio registravimo šablono priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="becec-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="becec-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="becec-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="becec-114">Kurti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="becec-114">Create collection letters</span></span>
1. <span data-ttu-id="becec-115">Pasirinkite Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Kurti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="becec-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="becec-116">Turite pasirinkti operacijų, kurių laiškus rinksite, tipus.</span><span class="sxs-lookup"><span data-stu-id="becec-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="becec-117">Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.</span><span class="sxs-lookup"><span data-stu-id="becec-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="becec-118">Lauke Priminimo laiškas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="becec-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="becec-119">Įveskite priminimo laiško datą.</span><span class="sxs-lookup"><span data-stu-id="becec-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="becec-120">Galima naudoti dvi registravimo šablono parinktis: sąskaita – naudokite kiekvienos delspinigių pažymos kliento sąskaitai priskirtą registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="becec-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="becec-121">Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="becec-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="becec-122">Pasirinkite registravimo šabloną, jei „Naudoti registravimo šabloną iš“ pakeitėte į „Pasirinkti“.</span><span class="sxs-lookup"><span data-stu-id="becec-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="becec-123">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="becec-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="becec-124">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="becec-124">Click Filter.</span></span>
6. <span data-ttu-id="becec-125">Lauke Kriterijai įveskite Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="becec-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="becec-126">Pvz., įveskite „US-001‟.</span><span class="sxs-lookup"><span data-stu-id="becec-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="becec-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="becec-127">Click OK.</span></span>
8. <span data-ttu-id="becec-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="becec-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="becec-129">Priminimo laiškų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="becec-129">Print collection letters</span></span>
1. <span data-ttu-id="becec-130">Pasirinkite Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="becec-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="becec-131">Lauke Būsena pasirinkite „Sukurta‟.</span><span class="sxs-lookup"><span data-stu-id="becec-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="becec-132">Lauke Išspausdinta pasirinkite „Neišspausdinta‟.</span><span class="sxs-lookup"><span data-stu-id="becec-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="becec-133">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="becec-133">Click Print.</span></span>
5. <span data-ttu-id="becec-134">Spustelėkite priminimo laiško pastabą.</span><span class="sxs-lookup"><span data-stu-id="becec-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="becec-135">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="becec-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="becec-136">Įveskite registravimų galutinę datą</span><span class="sxs-lookup"><span data-stu-id="becec-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="becec-137">Spustelėkite Gerai, norėdami spausdinti priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="becec-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="becec-138">Priminimo laiškų registravimas</span><span class="sxs-lookup"><span data-stu-id="becec-138">Post the collection letter</span></span>
1. <span data-ttu-id="becec-139">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="becec-139">Click Post.</span></span>
2. <span data-ttu-id="becec-140">Įveskite priminimo laiško registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="becec-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="becec-141">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="becec-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="becec-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="becec-142">Click OK.</span></span>
5. <span data-ttu-id="becec-143">Lauke Būsena pasirinkite „Užregistruota‟.</span><span class="sxs-lookup"><span data-stu-id="becec-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="becec-144">Lauke Išspausdinta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="becec-144">In the Printed field, select an option.</span></span>


