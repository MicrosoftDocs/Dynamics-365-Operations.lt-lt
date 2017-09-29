--- 
title: "Palūkanų apdorojimas"
description: "Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="d4d85-103">Palūkanų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="d4d85-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4d85-104">Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="d4d85-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="d4d85-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="d4d85-106">Nustatyti palūkanas registravimo šablone</span><span class="sxs-lookup"><span data-stu-id="d4d85-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="d4d85-107">Pasirinkite Kreditas ir rinkiniai > Sąranka > Klientų registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="d4d85-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="d4d85-108">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d4d85-108">Click Edit.</span></span>
    * <span data-ttu-id="d4d85-109">Iš išplečiamojo sąrašo pasirinkite palūkanų kodą.</span><span class="sxs-lookup"><span data-stu-id="d4d85-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="d4d85-110">Jei nenorite skaičiuoti operacijų palūkanų naudodami šį registravimo šabloną, palikite lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="d4d85-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="d4d85-111">Naudojant skirtuką Lentelių apribojimai, galima keisti būdą, kuriuo apdorojamos palūkanos.</span><span class="sxs-lookup"><span data-stu-id="d4d85-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="d4d85-112">Jei šio lauko reikšmė nustatyta kaip Taip, bus skaičiuojamos šio registravimo šablono palūkanos.</span><span class="sxs-lookup"><span data-stu-id="d4d85-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="d4d85-113">Skaičiuoti palūkanas</span><span class="sxs-lookup"><span data-stu-id="d4d85-113">Calculate interest</span></span>
1. <span data-ttu-id="d4d85-114">Pasirinkite Kreditas ir rinkiniai > Palūkanos > Kurti delspinigių pažymas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="d4d85-115">Turite pasirinkti operacijų, kurių palūkanas skaičiuosite, tipus.</span><span class="sxs-lookup"><span data-stu-id="d4d85-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="d4d85-116">Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.</span><span class="sxs-lookup"><span data-stu-id="d4d85-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="d4d85-117">Jei pasirinksite Palūkanos, skaičiuosite palūkanų palūkanas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="d4d85-118">Prieš įtraukiant šias operacijas, rekomenduojama patikrinti įstatymus, kuriais reguliuojama, kaip skaičiuoti palūkanų palūkanas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="d4d85-119">Palūkanos bus skaičiuojamos nuo šios datos iki pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="d4d85-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="d4d85-120">Jei nenurodysite pradžios datos, tada visos neužregistruotos delspinigių pažymos bus atšauktos, o palūkanos bus perskaičiuotos nuo operacijos datos.</span><span class="sxs-lookup"><span data-stu-id="d4d85-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="d4d85-121">Įveskite delspinigių pažymos datą.</span><span class="sxs-lookup"><span data-stu-id="d4d85-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="d4d85-122">Galima naudoti tris registravimo šablono parinktis: Sąskaita – naudokite kiekvienos delspinigių pažymos kliento sąskaitai priskirtą registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="d4d85-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="d4d85-123">Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="d4d85-124">Operacija – naudokite atskirą registravimo šabloną iš operacijų, kuriose apskaičiuotos palūkanos kiekvienai delspinigių pažymai.</span><span class="sxs-lookup"><span data-stu-id="d4d85-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="d4d85-125">Operacijos, kurios neturi priskirtų registravimo šablonų, naudos registravimo šabloną, kuris nustatytas formos Gautinų sumų parametrai srityje DK ir PVM.</span><span class="sxs-lookup"><span data-stu-id="d4d85-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="d4d85-126">Pasirinkite registravimo šabloną čia, jei „Naudoti registravimo šabloną iš“ pakeitėte į „Pasirinkti“.</span><span class="sxs-lookup"><span data-stu-id="d4d85-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="d4d85-127">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4d85-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="d4d85-128">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="d4d85-128">Click Filter.</span></span>
5. <span data-ttu-id="d4d85-129">Lauke Kriterijai įveskite Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="d4d85-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="d4d85-130">Pvz., įveskite „US-001‟.</span><span class="sxs-lookup"><span data-stu-id="d4d85-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="d4d85-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d4d85-131">Click OK.</span></span>
7. <span data-ttu-id="d4d85-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d4d85-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="d4d85-133">Spausdinti delspinigių pažymas</span><span class="sxs-lookup"><span data-stu-id="d4d85-133">Print interest notes</span></span>
1. <span data-ttu-id="d4d85-134">Pasirinkite Kreditas ir rinkiniai > Palūkanos > Peržiūrėti ir apdoroti delspinigių pažymas.</span><span class="sxs-lookup"><span data-stu-id="d4d85-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="d4d85-135">Lauke Būsena pasirinkite „Sukurta‟.</span><span class="sxs-lookup"><span data-stu-id="d4d85-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="d4d85-136">Lauke Išspausdinta pasirinkite „Neišspausdinta‟.</span><span class="sxs-lookup"><span data-stu-id="d4d85-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="d4d85-137">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="d4d85-137">Click Print.</span></span>
5. <span data-ttu-id="d4d85-138">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4d85-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="d4d85-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d4d85-139">Click OK.</span></span>
7. <span data-ttu-id="d4d85-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d4d85-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="d4d85-141">Registruoti delspinigių pažymą</span><span class="sxs-lookup"><span data-stu-id="d4d85-141">Post the interest note</span></span>
1. <span data-ttu-id="d4d85-142">Pasirinkite delspinigių pažymą, kuri paruoštas registruoti (būsena yra Sukurta).</span><span class="sxs-lookup"><span data-stu-id="d4d85-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="d4d85-143">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="d4d85-143">Click Post.</span></span>
3. <span data-ttu-id="d4d85-144">Įveskite delspinigių pažymos registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="d4d85-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="d4d85-145">Pasirinkite Taip, jei norite sukurti kiekvienos delspinigių pažymos DK operaciją.</span><span class="sxs-lookup"><span data-stu-id="d4d85-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="d4d85-146">Jei Taip nepasirinksite, prireiks vienos operacijos, norint sukaupti ir užregistruoti DK visų kliento delspinigių pažymų delspinigius.</span><span class="sxs-lookup"><span data-stu-id="d4d85-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="d4d85-147">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4d85-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="d4d85-148">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d4d85-148">Click OK.</span></span>
6. <span data-ttu-id="d4d85-149">Lauke Būsena pasirinkite „Užregistruota‟.</span><span class="sxs-lookup"><span data-stu-id="d4d85-149">In the Status field, select 'Posted'.</span></span>

