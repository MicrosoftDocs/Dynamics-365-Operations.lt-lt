---
title: Teisės į išmoką taisyklių ir strategijų nustatymas
description: Šiame straipsnyje sužinosite, kaip sukurti išmokų tinkamumo taisykles bei strategijas ir priskirti išmokoms taisykles.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053158"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="11edc-103">Teisės į išmoką taisyklių ir strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="11edc-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="11edc-104">Šioje temoje parodyta, kaip galite sukurti teisių į išmoką taisykles ir politiką bei priskirti taisykles išmokoms.</span><span class="sxs-lookup"><span data-stu-id="11edc-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="11edc-105">Sukurti išmokų tinkamumo strategijos taisyklių tipą</span><span class="sxs-lookup"><span data-stu-id="11edc-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="11edc-106">Eikite į **Žmogiškieji ištekliai > Išmokos > Teisės > Politikos taisyklių tipai teisėms į išmokas**.</span><span class="sxs-lookup"><span data-stu-id="11edc-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="11edc-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="11edc-107">Select **New**.</span></span>
3. <span data-ttu-id="11edc-108">Laukelyje **Taisyklės pavadinimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="11edc-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="11edc-109">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="11edc-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="11edc-110">Laukelyje **Užklausos pavadinimas** rinkitės iškrentantį meniu mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="11edc-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="11edc-111">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11edc-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="11edc-112">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="11edc-112">Select **Save**.</span></span>
8. <span data-ttu-id="11edc-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11edc-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="11edc-114">Išmokos tinkamumo strategija</span><span class="sxs-lookup"><span data-stu-id="11edc-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="11edc-115">Eikite į **Žmogiškieji ištekliai > Išmokos > Teisės > Teisių į išmokas politikos**.</span><span class="sxs-lookup"><span data-stu-id="11edc-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="11edc-116">Pasirinkite esamą išmokų strategiją.</span><span class="sxs-lookup"><span data-stu-id="11edc-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="11edc-117">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11edc-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="11edc-118">Įjunkite plėtinį **Politnės organizacijos** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="11edc-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="11edc-119">Galite įtraukti ar pašalinti bet kurią norimą organizaciją, kurią norite įtraukti į politiką.</span><span class="sxs-lookup"><span data-stu-id="11edc-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="11edc-120">Išplėskite arba sutraukite sekciją **Strategijos taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="11edc-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="11edc-121">Sąraše raskite politikos taisyklę, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="11edc-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="11edc-122">Pasirinkite **Kurti strategijos taisyklę**.</span><span class="sxs-lookup"><span data-stu-id="11edc-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="11edc-123">Laukelyje **Įsigaliojimo data** įveskite datą, nuo kurios įsigalios jūsų politika.</span><span class="sxs-lookup"><span data-stu-id="11edc-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="11edc-124">Nustatydami įsigaliojimo pabaigos datas galėsite atlikti keitimus ateityje politikos taisyklėms tam, kad nebereikėtų grįžti į politiką, kai norėsite pradėti keitimų įsigaliojimą.</span><span class="sxs-lookup"><span data-stu-id="11edc-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="11edc-125">Jei reikia, įtraukite sąlygą **Įtraukti sąlygą** į laukelį.</span><span class="sxs-lookup"><span data-stu-id="11edc-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="11edc-126">Pavyzdžiui, jei norite, kad taisyklė būtų tiakoma tik prekybos vadovams, galite sukurti sąlygą sakančią: Kai pareigų aprašas yra lygus pardavimo vadovui.</span><span class="sxs-lookup"><span data-stu-id="11edc-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="11edc-127">Galite įtraukti kelis pareiškimus kartu su taisykle.</span><span class="sxs-lookup"><span data-stu-id="11edc-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="11edc-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="11edc-128">Select **OK**.</span></span>
11. <span data-ttu-id="11edc-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="11edc-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="11edc-130">Priskirti išmokai taisyklę</span><span class="sxs-lookup"><span data-stu-id="11edc-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="11edc-131">Eikite į **Žmogiškieji ištekliai > Išmokos > Išmokos**.</span><span class="sxs-lookup"><span data-stu-id="11edc-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="11edc-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="11edc-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="11edc-133">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11edc-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="11edc-134">Išplėskite ar sutraukite **Teisių taisyklės** skyrių.</span><span class="sxs-lookup"><span data-stu-id="11edc-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="11edc-135">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="11edc-135">Select **Edit**.</span></span>
6. <span data-ttu-id="11edc-136">Laukelyje **Teisės** rinkitės taisyklę.</span><span class="sxs-lookup"><span data-stu-id="11edc-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="11edc-137">Laukelyje **Taisyklės tipas** rinkitės anksčiau sukurtą taisyklę.</span><span class="sxs-lookup"><span data-stu-id="11edc-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="11edc-138">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="11edc-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="11edc-139">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="11edc-139">Select **Save**.</span></span>
11. <span data-ttu-id="11edc-140">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="11edc-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]