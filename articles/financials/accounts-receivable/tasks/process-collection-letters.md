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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c146d6ef34137eb8eef3a5a5123ce0174df3033
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="6a58f-103">Apdoroti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="6a58f-103">Process collection letters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a58f-104">Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="6a58f-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="6a58f-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="6a58f-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="6a58f-106">Registravimo šablone nustatykite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="6a58f-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="6a58f-107">Pasirinkite Kreditas ir rinkiniai > Sąranka > Klientų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="6a58f-108">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="6a58f-108">Click Edit.</span></span>
    * <span data-ttu-id="6a58f-109">Išplečiamajame sąraše pasirinkite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="6a58f-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="6a58f-110">Jei nenorite generuoti operacijų priminimo laiškų naudodami šį registravimo šabloną, palikite lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="6a58f-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="6a58f-111">Naudojant lentelių apribojimų skirtuką galite keisti būdą, kuriuo apdorojami priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="6a58f-112">Jei šio lauko reikšmė nustatyta kaip Taip, bus kuriami šio registravimo šablono priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="6a58f-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a58f-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="6a58f-114">Kurti priminimo laiškus</span><span class="sxs-lookup"><span data-stu-id="6a58f-114">Create collection letters</span></span>
1. <span data-ttu-id="6a58f-115">Pasirinkite Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Kurti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="6a58f-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="6a58f-116">Turite pasirinkti operacijų, kurių laiškus rinksite, tipus.</span><span class="sxs-lookup"><span data-stu-id="6a58f-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="6a58f-117">Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.</span><span class="sxs-lookup"><span data-stu-id="6a58f-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="6a58f-118">Lauke Priminimo laiškas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="6a58f-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="6a58f-119">Įveskite priminimo laiško datą.</span><span class="sxs-lookup"><span data-stu-id="6a58f-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="6a58f-120">Galima naudoti dvi registravimo šablono parinktis: sąskaita – naudokite kiekvienos delspinigių pažymos kliento sąskaitai priskirtą registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="6a58f-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="6a58f-121">Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="6a58f-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="6a58f-122">Pasirinkite registravimo šabloną, jei „Naudoti registravimo šabloną iš“ pakeitėte į „Pasirinkti“.</span><span class="sxs-lookup"><span data-stu-id="6a58f-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="6a58f-123">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="6a58f-124">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="6a58f-124">Click Filter.</span></span>
6. <span data-ttu-id="6a58f-125">Lauke Kriterijai įveskite Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="6a58f-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="6a58f-126">Pvz., įveskite „US-001‟.</span><span class="sxs-lookup"><span data-stu-id="6a58f-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="6a58f-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6a58f-127">Click OK.</span></span>
8. <span data-ttu-id="6a58f-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6a58f-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="6a58f-129">Priminimo laiškų spausdinimas</span><span class="sxs-lookup"><span data-stu-id="6a58f-129">Print collection letters</span></span>
1. <span data-ttu-id="6a58f-130">Pasirinkite Kreditas ir mokėjimų priežiūra > Priminimo laiškas > Peržiūrėti ir apdoroti priminimo laiškus.</span><span class="sxs-lookup"><span data-stu-id="6a58f-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="6a58f-131">Lauke Būsena pasirinkite „Sukurta‟.</span><span class="sxs-lookup"><span data-stu-id="6a58f-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="6a58f-132">Lauke Išspausdinta pasirinkite „Neišspausdinta‟.</span><span class="sxs-lookup"><span data-stu-id="6a58f-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="6a58f-133">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="6a58f-133">Click Print.</span></span>
5. <span data-ttu-id="6a58f-134">Spustelėkite priminimo laiško pastabą.</span><span class="sxs-lookup"><span data-stu-id="6a58f-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="6a58f-135">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="6a58f-136">Įveskite registravimų galutinę datą</span><span class="sxs-lookup"><span data-stu-id="6a58f-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="6a58f-137">Spustelėkite Gerai, norėdami spausdinti priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="6a58f-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="6a58f-138">Priminimo laiškų registravimas</span><span class="sxs-lookup"><span data-stu-id="6a58f-138">Post the collection letter</span></span>
1. <span data-ttu-id="6a58f-139">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="6a58f-139">Click Post.</span></span>
2. <span data-ttu-id="6a58f-140">Įveskite priminimo laiško registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="6a58f-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="6a58f-141">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="6a58f-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="6a58f-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6a58f-142">Click OK.</span></span>
5. <span data-ttu-id="6a58f-143">Lauke Būsena pasirinkite „Užregistruota‟.</span><span class="sxs-lookup"><span data-stu-id="6a58f-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="6a58f-144">Lauke Išspausdinta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="6a58f-144">In the Printed field, select an option.</span></span>


