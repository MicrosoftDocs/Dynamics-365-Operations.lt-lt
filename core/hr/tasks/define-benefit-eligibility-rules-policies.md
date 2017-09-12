--- 
title: "Apibrėžti išmokų tinkamumo taisykles ir strategijas"
description: "Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 49d512c3093f97c9c6d8ab15d29119e7a3b9a455
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="3bbb7-103">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="3bbb7-103">Define benefit eligibility rules and policies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3bbb7-104">Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="3bbb7-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="3bbb7-106">Sukurti išmokų tinkamumo strategijos taisyklių tipą</span><span class="sxs-lookup"><span data-stu-id="3bbb7-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="3bbb7-107">Eikite į Žmogiškieji ištekliai > Išmokos > Tinkamumas > Išmokų tinkamumo strategijos taisyklių tipai.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="3bbb7-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-108">Click New.</span></span>
3. <span data-ttu-id="3bbb7-109">Lauke Taisyklės pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="3bbb7-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3bbb7-111">Lauke Užklausos pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3bbb7-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3bbb7-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-113">Click Save.</span></span>
8. <span data-ttu-id="3bbb7-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="3bbb7-115">Išmokos tinkamumo strategija</span><span class="sxs-lookup"><span data-stu-id="3bbb7-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="3bbb7-116">Eikite į Žmogiškieji ištekliai > Išmokos >Tinkamumas > Išmokų tinkamumo strategijos.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="3bbb7-117">Pasirinkite esamą išmokų strategiją.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="3bbb7-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3bbb7-119">Perjunkite dalies „Strategijos organizacijos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="3bbb7-120">Čia galite pridėti arba pašalinti organizacijas, kurias norite įtraukti į strategiją.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="3bbb7-121">Išplėskite arba sutraukite dalį Strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="3bbb7-122">Sąraše raskite anksčiau sukurtą strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="3bbb7-123">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="3bbb7-124">Lauke „Įsigaliojimo data“ įveskite norimą strategijos įsigaliojimo datą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="3bbb7-125">Įsigaliojimo ir pabaigos datų nustatymas leidžia daryti ateityje įsigaliojančius strategijos taisyklių pakeitimus – jums nebereikės grįžti į strategiją, kad šie pakeitimai įsigaliotų.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="3bbb7-126">Pvz., jei norite, kad taisyklė būtų taikoma tik pardavimo vadybininkams, galite sukurti „Kai“ sąlygą: kai pareigų aprašas – pardavimo vadybininkas.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="3bbb7-127">Kartu su „Kai“ sąlygomis taisyklėje galite naudoti keletą „Ir“ arba „Ar“.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="3bbb7-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-128">Click OK.</span></span>
11. <span data-ttu-id="3bbb7-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-129">Close the page.</span></span>
12. <span data-ttu-id="3bbb7-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="3bbb7-131">Priskirti išmokai taisyklę</span><span class="sxs-lookup"><span data-stu-id="3bbb7-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="3bbb7-132">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="3bbb7-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3bbb7-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3bbb7-135">Išplėskite arba sutraukite dalį Tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="3bbb7-136">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-136">Click Edit.</span></span>
6. <span data-ttu-id="3bbb7-137">Lauke „Tinkamumas“ pasirinkite „Pagal taisyklę iš sąrašo“.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="3bbb7-138">Lauke „Taisyklės tipas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="3bbb7-139">Sąraše raskite ir pasirinkite anksčiau sukurtą taisyklę.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="3bbb7-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3bbb7-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-141">Click Save.</span></span>
11. <span data-ttu-id="3bbb7-142">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="3bbb7-142">Close the form.</span></span>


