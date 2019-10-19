---
title: Apibrėžti išmokų tinkamumo taisykles ir strategijas
description: Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190562"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="48ea0-103">Apibrėžti išmokų tinkamumo taisykles ir strategijas</span><span class="sxs-lookup"><span data-stu-id="48ea0-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48ea0-104">Šis įrašas parodys, kaip sukurti išmokų tinkamumo taisykles ir strategijas, ir tada priskirti išmokoms taisykles.</span><span class="sxs-lookup"><span data-stu-id="48ea0-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="48ea0-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="48ea0-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="48ea0-106">Sukurti išmokų tinkamumo strategijos taisyklių tipą</span><span class="sxs-lookup"><span data-stu-id="48ea0-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="48ea0-107">Eikite į Žmogiškieji ištekliai > Išmokos > Tinkamumas > Išmokų tinkamumo strategijos taisyklių tipai.</span><span class="sxs-lookup"><span data-stu-id="48ea0-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="48ea0-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="48ea0-108">Click New.</span></span>
3. <span data-ttu-id="48ea0-109">Lauke Taisyklės pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="48ea0-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="48ea0-111">Lauke Užklausos pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="48ea0-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="48ea0-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="48ea0-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="48ea0-113">Click Save.</span></span>
8. <span data-ttu-id="48ea0-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="48ea0-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="48ea0-115">Išmokos tinkamumo strategija</span><span class="sxs-lookup"><span data-stu-id="48ea0-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="48ea0-116">Eikite į Žmogiškieji ištekliai > Išmokos >Tinkamumas > Išmokų tinkamumo strategijos.</span><span class="sxs-lookup"><span data-stu-id="48ea0-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="48ea0-117">Pasirinkite esamą išmokų strategiją.</span><span class="sxs-lookup"><span data-stu-id="48ea0-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="48ea0-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="48ea0-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="48ea0-119">Perjunkite dalies „Strategijos organizacijos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="48ea0-120">Čia galite pridėti arba pašalinti organizacijas, kurias norite įtraukti į strategiją.</span><span class="sxs-lookup"><span data-stu-id="48ea0-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="48ea0-121">Išplėskite arba sutraukite dalį Strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="48ea0-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="48ea0-122">Sąraše raskite anksčiau sukurtą strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="48ea0-123">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="48ea0-124">Lauke „Įsigaliojimo data“ įveskite norimą strategijos įsigaliojimo datą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="48ea0-125">Įsigaliojimo ir pabaigos datų nustatymas leidžia daryti ateityje įsigaliojančius strategijos taisyklių pakeitimus – jums nebereikės grįžti į strategiją, kad šie pakeitimai įsigaliotų.</span><span class="sxs-lookup"><span data-stu-id="48ea0-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="48ea0-126">Pvz., jei norite, kad taisyklė būtų taikoma tik pardavimo vadybininkams, galite sukurti „Kai“ sąlygą: kai pareigų aprašas – pardavimo vadybininkas.</span><span class="sxs-lookup"><span data-stu-id="48ea0-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="48ea0-127">Kartu su „Kai“ sąlygomis taisyklėje galite naudoti keletą „Ir“ arba „Ar“.</span><span class="sxs-lookup"><span data-stu-id="48ea0-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="48ea0-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="48ea0-128">Click OK.</span></span>
11. <span data-ttu-id="48ea0-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="48ea0-129">Close the page.</span></span>
12. <span data-ttu-id="48ea0-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="48ea0-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="48ea0-131">Priskirti išmokai taisyklę</span><span class="sxs-lookup"><span data-stu-id="48ea0-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="48ea0-132">Pasirinkite Personalas > Išmokos > Išmokos.</span><span class="sxs-lookup"><span data-stu-id="48ea0-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="48ea0-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="48ea0-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="48ea0-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="48ea0-135">Išplėskite arba sutraukite dalį Tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="48ea0-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="48ea0-136">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="48ea0-136">Click Edit.</span></span>
6. <span data-ttu-id="48ea0-137">Lauke „Tinkamumas“ pasirinkite „Pagal taisyklę iš sąrašo“.</span><span class="sxs-lookup"><span data-stu-id="48ea0-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="48ea0-138">Lauke „Taisyklės tipas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="48ea0-139">Sąraše raskite ir pasirinkite anksčiau sukurtą taisyklę.</span><span class="sxs-lookup"><span data-stu-id="48ea0-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="48ea0-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="48ea0-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="48ea0-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="48ea0-141">Click Save.</span></span>
11. <span data-ttu-id="48ea0-142">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="48ea0-142">Close the form.</span></span>

