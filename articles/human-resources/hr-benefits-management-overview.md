---
title: Išmokų valdymo apžvalga
description: Išmokų valdymo funkcijos programoje „Dynamics 365 Human Resources“ apžvalga. Siūlykite savo darbuotojams išplėstines išmokų parinktis naudodami paprastas naudoti internetines funkcijas.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464331"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="424a7-104">Išmokų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="424a7-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="424a7-105">Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="424a7-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="424a7-106">Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams.</span><span class="sxs-lookup"><span data-stu-id="424a7-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="424a7-107">Išmokų valdymas programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="424a7-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="424a7-108">„Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="424a7-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="424a7-109">Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas.</span><span class="sxs-lookup"><span data-stu-id="424a7-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="424a7-110">Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.</span><span class="sxs-lookup"><span data-stu-id="424a7-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="424a7-111">Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="424a7-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="424a7-112">Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="424a7-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="424a7-113">Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.</span><span class="sxs-lookup"><span data-stu-id="424a7-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="424a7-114">Tinkamo gyvenimo įvykio apdorojimas palaiko būsimus gyvenimo įvykius.</span><span class="sxs-lookup"><span data-stu-id="424a7-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="424a7-115">Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="424a7-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="424a7-116">Išmokų valdymo įjungimas</span><span class="sxs-lookup"><span data-stu-id="424a7-116">Enable Benefits management</span></span>

<span data-ttu-id="424a7-117">Šioje temoje aprašoma, kaip įjungti personalo valdymo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="424a7-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="424a7-118">Jame taip pat nurodoma, kurios esamos personalo valdymo funkcijos išmokų valdyme pakeičiamos arba kurios yra išjungiamos, kai įjungiate išmokų valdymą.</span><span class="sxs-lookup"><span data-stu-id="424a7-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="424a7-119">Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima.</span><span class="sxs-lookup"><span data-stu-id="424a7-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="424a7-120">Rekomenduojame įjungti ir testuoti išmokų valdymą **smėlio dėžės** aplinkoje prieš įjungiant jį **gamybos** aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="424a7-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="424a7-121">Yra reikšmingų skirtumų tarp pasenusių išmokų funkcijų ir naujų išmokų valdymo funkcijų – joms reikalingi papildomi nustatymai ir tikrinimai prieš įtraukiant į gamybos procesą.</span><span class="sxs-lookup"><span data-stu-id="424a7-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="424a7-122">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="424a7-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="424a7-123">Darbuotojų informacijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-123">Configure employee information</span></span>

<span data-ttu-id="424a7-124">Kad užregistruotumėte darbuotojus išmokoms gauti, turite pateikti reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="424a7-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="424a7-125">Turite užregistruoti darbuotoją į **pastoviosios atlyginimo dalies planą** jų darbo pradžios dieną ir pasirinkti **išmokų mokėjimo dažnumą** dalies **Įdarbinimo informacija** formoje **Darbininkas**.</span><span class="sxs-lookup"><span data-stu-id="424a7-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="424a7-126">Jei turite darbuotoją, kuris gauna papildomą užmokestį kaip komisinį mokestį, galite įtraukite **Metinio užmokesčio algos** sumą iš darbuotojo įrašo.</span><span class="sxs-lookup"><span data-stu-id="424a7-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="424a7-127">Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatydami padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą.</span><span class="sxs-lookup"><span data-stu-id="424a7-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="424a7-128">**Metinės algos išmokos** turi būti galiojančios nuo darbuotojo pradžios dienos arba nuo išmokos laikotarpio, priklausomai nuo to, kuri data yra vėlesnė.</span><span class="sxs-lookup"><span data-stu-id="424a7-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="424a7-129">Jei fiksuota alga ir metinės algos užmokesčio suma darbuotojui įrašoma, metinės algos užmokestis bus naudoojamas nustatant padengiamas sumas.</span><span class="sxs-lookup"><span data-stu-id="424a7-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="424a7-130">Kai kuriate išmokų planą, naudojantį tarifus, pagrįstus lytimi arba amžiumi, turite įvesti darbuotojo gimimo datą ir lytį, kad būtų apskaičiuota išmokų savikaina.</span><span class="sxs-lookup"><span data-stu-id="424a7-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="424a7-131">Išmokų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-131">Configure Benefits management</span></span>

<span data-ttu-id="424a7-132">Kad galėtumėte kurti savo darbuotojų išmokų planus, reikia konfigūruoti planų parinktis.</span><span class="sxs-lookup"><span data-stu-id="424a7-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="424a7-133">Išmokų valdymo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="424a7-134">Tinkamumo taisyklių ir parinkčių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="424a7-135">Asmeninio kontakto tinkamumo parinkčių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="424a7-136">Padengimo parinkčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="424a7-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="424a7-137">Mokėjimo dažnumo nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="424a7-138">Gyvenimo įvykių tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="424a7-139">Planų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="424a7-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="424a7-140">Priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="424a7-141">Pakopos kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="424a7-142">Tarifų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="424a7-143">Atskaitymų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="424a7-144">Laukimo dienų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="424a7-145">Laukimo laikotarpių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="424a7-146">Apvalinimo taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="424a7-147">Įdarbinimo kategorijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="424a7-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="424a7-148">Įdarbinimo tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="424a7-149">Darbuotojų savitarnos paslaugos konfugūravimas</span><span class="sxs-lookup"><span data-stu-id="424a7-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="424a7-150">Išmokų planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="424a7-150">Create benefit plans</span></span>

<span data-ttu-id="424a7-151">Šiuose straipsniuose nurodoma, kaip sukurti išmokų planus, įskaitant grupių ir lanksčiųjų kreditų programas.</span><span class="sxs-lookup"><span data-stu-id="424a7-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="424a7-152">Išmokų planų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="424a7-153">Lanksčių kredito programų nustatymas</span><span class="sxs-lookup"><span data-stu-id="424a7-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="424a7-154">Išmokų planų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-154">Process benefit plans</span></span>

<span data-ttu-id="424a7-155">Turite apdoroti kai kuriuos keitimus, kad jie būtų aktyvūs.</span><span class="sxs-lookup"><span data-stu-id="424a7-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="424a7-156">Tinkamumo registracijai apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="424a7-157">Gyvenimo įvykių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="424a7-158">Gyvenimo įvykio keitimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="424a7-159">Gyvenimo įvykio tinkamumo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="424a7-160">Tarifo pakeitimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="424a7-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]