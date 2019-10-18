---
title: Palūkanų apdorojimas
description: Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188768"
---
# <a name="process-interest"></a><span data-ttu-id="38ea7-103">Palūkanų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="38ea7-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38ea7-104">Ši procedūra nurodo, kaip kurti, spausdinti ir registruoti delspinigių pažymas.</span><span class="sxs-lookup"><span data-stu-id="38ea7-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="38ea7-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="38ea7-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="38ea7-106">Nustatyti palūkanas registravimo šablone</span><span class="sxs-lookup"><span data-stu-id="38ea7-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="38ea7-107">Parinktyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir mokesčių rinkimas > Sąranka > Kliento registravimo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="38ea7-108">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-108">Click **Edit**.</span></span>
3. <span data-ttu-id="38ea7-109">Parinktyje **Sąrankos „fastTab“**, lauke **Palūkanų kodas** išplečiamajame sąraše pasirinkite delspinigių kodą.</span><span class="sxs-lookup"><span data-stu-id="38ea7-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="38ea7-110">Jei nenorite skaičiuoti operacijų palūkanų naudodami šį registravimo šabloną, palikite lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="38ea7-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="38ea7-111">„FastTab“ **Lentelės apribojimai** leidžia jums keisti, kaip palūkanos apdorojamos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="38ea7-112">Jei šio lauko reikšmė nustatyta kaip Taip, bus skaičiuojamos šio registravimo šablono palūkanos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="38ea7-113">Skaičiuoti palūkanas</span><span class="sxs-lookup"><span data-stu-id="38ea7-113">Calculate interest</span></span>
1. <span data-ttu-id="38ea7-114">Skiltyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir mokesčių rinkimas > Palūkanos > Kurti delspinigių pažymas**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="38ea7-115">Turite pasirinkti operacijų, kurių palūkanas skaičiuosite, tipus.</span><span class="sxs-lookup"><span data-stu-id="38ea7-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="38ea7-116">Skaičiuojant bus įtrauktos visos atidarytos šių tipų operacijos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="38ea7-117">Jei nustatysite skiltyje **Palūkanos** reikšmę Taip, bus skaičiuojami palūkanų delspinigiai.</span><span class="sxs-lookup"><span data-stu-id="38ea7-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="38ea7-118">Prieš įtraukiant šias operacijas, rekomenduojama patikrinti įstatymus, kuriais reguliuojama, kaip skaičiuoti palūkanų palūkanas.</span><span class="sxs-lookup"><span data-stu-id="38ea7-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="38ea7-119">Lauke **Nuo datos** įveskite datą, nuo kurios bus pradėtos skaičiuoti palūkanos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="38ea7-120">Jei nenurodysite skiltyje **Nuo datos** reikšmę, tada visos neįregistruotos delspinigių pažymos bus atšauktos ir palūkanos bus perskaičiuojamos nuo operacijos datos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="38ea7-121">Lauke **Iki datos** įveskite datą, iki kurios palūkanos bus skaičiuojamos.</span><span class="sxs-lookup"><span data-stu-id="38ea7-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="38ea7-122">Lauke **Naudoti registravimo šabloną iš** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="38ea7-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="38ea7-123">Yra trys registravimo šablonų parinktys:</span><span class="sxs-lookup"><span data-stu-id="38ea7-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="38ea7-124">Sąskaita – naudokite registravimo šabloną, priskirtą kliento sąskaitai, kiekvienai delspinigių pažymai.</span><span class="sxs-lookup"><span data-stu-id="38ea7-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="38ea7-125">Pasirinkti – naudokite registravimo šabloną, kurį pasirenkate lauke Registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="38ea7-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="38ea7-126">Operacija – naudokite atskirą registravimo šabloną iš operacijų, kuriose apskaičiuotos palūkanos kiekvienai delspinigių pažymai.</span><span class="sxs-lookup"><span data-stu-id="38ea7-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="38ea7-127">Operacijos, kurios neturi priskirtų registravimo šablonų, naudos registravimo šabloną, kuris nustatytas formos Gautinų sumų parametrai srityje DK ir PVM.</span><span class="sxs-lookup"><span data-stu-id="38ea7-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="38ea7-128">Išplėskite „fastTab“ **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="38ea7-129">Spustelėkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-129">Click **Filter**.</span></span>
9. <span data-ttu-id="38ea7-130">Lauke **Kriterijai** įveskite Kliento ID.</span><span class="sxs-lookup"><span data-stu-id="38ea7-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="38ea7-131">Pvz., įveskite „US-001‟.</span><span class="sxs-lookup"><span data-stu-id="38ea7-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="38ea7-132">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-132">Click **OK**.</span></span>
7. <span data-ttu-id="38ea7-133">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="38ea7-134">Spausdinti delspinigių pažymas</span><span class="sxs-lookup"><span data-stu-id="38ea7-134">Print interest notes</span></span>
1. <span data-ttu-id="38ea7-135">Skiltyje **Naršymo sritis** eikite į **Moduliai > Kreditas ir Mokesčių rinkimas > Palūkanos > Peržiūrėti ir apdoroti delspinigių pažymas**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="38ea7-136">Lauke **Būsena** pasirinkite „Sukurta“.</span><span class="sxs-lookup"><span data-stu-id="38ea7-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="38ea7-137">Lauke **Išspausdinta** pasirinkite „Neišspausdinta“.</span><span class="sxs-lookup"><span data-stu-id="38ea7-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="38ea7-138">Spustelėkite **Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-138">Click **Print**.</span></span>
5. <span data-ttu-id="38ea7-139">Išplėskite „fastTab“ **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="38ea7-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-140">Click **OK**.</span></span>
7. <span data-ttu-id="38ea7-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="38ea7-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="38ea7-142">Registruoti delspinigių pažymą</span><span class="sxs-lookup"><span data-stu-id="38ea7-142">Post the interest note</span></span>
1. <span data-ttu-id="38ea7-143">Pasirinkite delspinigių pažymą, kuri paruoštas registruoti (būsena yra Sukurta).</span><span class="sxs-lookup"><span data-stu-id="38ea7-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="38ea7-144">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="38ea7-144">Click **Post**.</span></span>
3. <span data-ttu-id="38ea7-145">Įveskite delspinigių pažymos registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="38ea7-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="38ea7-146">Pasirinkite Taip, jei norite sukurti kiekvienos delspinigių pažymos DK operaciją.</span><span class="sxs-lookup"><span data-stu-id="38ea7-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="38ea7-147">Jei Taip nepasirinksite, prireiks vienos operacijos, norint sukaupti ir užregistruoti DK visų kliento delspinigių pažymų delspinigius.</span><span class="sxs-lookup"><span data-stu-id="38ea7-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="38ea7-148">Išplėskite „fastTab“ **Įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="38ea7-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="38ea7-149">Click **OK**.</span></span>
6. <span data-ttu-id="38ea7-150">Lauke **Būsena** pasirinkite „Įregistruota“.</span><span class="sxs-lookup"><span data-stu-id="38ea7-150">In the **Status** field, select 'Posted'.</span></span>

