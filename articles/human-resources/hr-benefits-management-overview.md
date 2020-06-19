---
title: Išmokų valdymo apžvalga
description: Išmokų valdymo funkcijos programoje „Dynamics 365 Human Resources“ apžvalga. Siūlykite savo darbuotojams išplėstines išmokų parinktis naudodami paprastas naudoti internetines funkcijas.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 4157cb1f83d686d435f3d04e47c578df455376c9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429271"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="8b712-104">Išmokų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="8b712-104">Benefits management overview</span></span>

<span data-ttu-id="8b712-105">Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="8b712-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="8b712-106">Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams.</span><span class="sxs-lookup"><span data-stu-id="8b712-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="8b712-107">Išmokų valdymas programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="8b712-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="8b712-108">„Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="8b712-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="8b712-109">Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas.</span><span class="sxs-lookup"><span data-stu-id="8b712-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="8b712-110">Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.</span><span class="sxs-lookup"><span data-stu-id="8b712-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="8b712-111">Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="8b712-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="8b712-112">Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="8b712-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="8b712-113">Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.</span><span class="sxs-lookup"><span data-stu-id="8b712-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="8b712-114">Tinkamo gyvenimo įvykio apdorojimas palaiko būsimus gyvenimo įvykius.</span><span class="sxs-lookup"><span data-stu-id="8b712-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="8b712-115">Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.</span><span class="sxs-lookup"><span data-stu-id="8b712-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="8b712-116">Išmokų valdymo žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="8b712-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="8b712-117">Lanksčiųjų kreditų programos</span><span class="sxs-lookup"><span data-stu-id="8b712-117">Flex credit programs</span></span>

<span data-ttu-id="8b712-118">Bendra kreditų vertė, nustatyta lanksčiųjų kreditų programai, nėra rodoma formoje **Darbininkų išmokų planai**.</span><span class="sxs-lookup"><span data-stu-id="8b712-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="8b712-119">Be to, jei lanksčiųjų kreditų programoje esančią proporcingumo taisyklę nustatysite į **Nėra**, formoje **Darbininkų išmokų planai** pasirenkant ir patvirtinant planus gali kilti klaida.</span><span class="sxs-lookup"><span data-stu-id="8b712-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="8b712-120">Išmokų valdymo įjungimas</span><span class="sxs-lookup"><span data-stu-id="8b712-120">Enable Benefits management</span></span>

<span data-ttu-id="8b712-121">Šiame straipsnyje aprašoma, kaip įjungti „Human Resources“ funkcijas.</span><span class="sxs-lookup"><span data-stu-id="8b712-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="8b712-122">Jame taip pat nurodoma, kurios esamos „Human Resources“ funkcijos išmokų valdyme pakeičiamos arba kurios yra išjungiamos, kai įjungiate išmokų valdymą.</span><span class="sxs-lookup"><span data-stu-id="8b712-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8b712-123">Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima.</span><span class="sxs-lookup"><span data-stu-id="8b712-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="8b712-124">Rekomenduojame įjungti ir testuoti išmokų valdymą **smėlio dėžės** aplinkoje prieš įjungiant jį **gamybos** aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="8b712-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="8b712-125">Yra reikšmingų skirtumų tarp pasenusių išmokų funkcijų ir naujų išmokų valdymo funkcijų – joms reikalingi papildomi nustatymai ir tikrinimai prieš įtraukiant į gamybos procesą.</span><span class="sxs-lookup"><span data-stu-id="8b712-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="8b712-126">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="8b712-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="8b712-127">Darbuotojų informacijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-127">Configure employee information</span></span>

<span data-ttu-id="8b712-128">Kad užregistruotumėte darbuotojus išmokoms gauti, turite pateikti reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="8b712-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="8b712-129">Turite užregistruoti darbuotoją į **pastoviosios atlyginimo dalies planą** jų darbo pradžios dieną ir pasirinkti **išmokų mokėjimo dažnumą** dalies **Įdarbinimo informacija** formoje **Darbininkas**.</span><span class="sxs-lookup"><span data-stu-id="8b712-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="8b712-130">Kai kuriate išmokų planą, naudojantį tarifus, pagrįstus lytimi arba amžiumi, turite įvesti darbuotojo gimimo datą ir lytį, kad būtų apskaičiuota išmokų savikaina.</span><span class="sxs-lookup"><span data-stu-id="8b712-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="8b712-131">Išmokų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-131">Configure Benefits management</span></span>

<span data-ttu-id="8b712-132">Kad galėtumėte kurti savo darbuotojų išmokų planus, reikia konfigūruoti planų parinktis.</span><span class="sxs-lookup"><span data-stu-id="8b712-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="8b712-133">Išmokų valdymo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="8b712-134">Tinkamumo taisyklių ir parinkčių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="8b712-135">Asmeninio kontakto tinkamumo parinkčių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="8b712-136">Padengimo parinkčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="8b712-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="8b712-137">Mokėjimo dažnumo nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="8b712-138">Gyvenimo įvykių tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="8b712-139">Planų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="8b712-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="8b712-140">Priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="8b712-141">Pakopos kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="8b712-142">Tarifų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="8b712-143">Atskaitymų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="8b712-144">Laukimo dienų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="8b712-145">Laukimo laikotarpių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="8b712-146">Apvalinimo taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="8b712-147">Įdarbinimo kategorijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="8b712-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="8b712-148">Įdarbinimo tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="8b712-149">Darbuotojų savitarnos paslaugos konfugūravimas</span><span class="sxs-lookup"><span data-stu-id="8b712-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="8b712-150">Išmokų planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="8b712-150">Create benefit plans</span></span>

<span data-ttu-id="8b712-151">Šiuose straipsniuose nurodoma, kaip sukurti išmokų planus, įskaitant grupių ir lanksčiųjų kreditų programas.</span><span class="sxs-lookup"><span data-stu-id="8b712-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="8b712-152">Išmokų planų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="8b712-153">Lanksčių kredito programų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8b712-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="8b712-154">Išmokų planų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-154">Process benefit plans</span></span>

<span data-ttu-id="8b712-155">Turite apdoroti kai kuriuos keitimus, kad jie būtų aktyvūs.</span><span class="sxs-lookup"><span data-stu-id="8b712-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="8b712-156">Tinkamumo registracijai apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="8b712-157">Gyvenimo įvykių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="8b712-158">Gyvenimo įvykio keitimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="8b712-159">Gyvenimo įvykio tinkamumo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="8b712-160">Tarifo pakeitimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8b712-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

