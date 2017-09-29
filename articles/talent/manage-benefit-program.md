---
title: "Išmokų programos nustatymas ir valdymas"
description: "Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus. Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti išmokas."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6de99fc6aea808fddbec047cc74e533c4e5f9ee9
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="15f5e-104">Išmokų programos nustatymas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="15f5e-104">Define and manage a benefits program</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="15f5e-105">Personalas pateikia įrankius, kuriuos galima naudoti norint nustatyti ir tvarkyti organizacijos savo darbuotojams siūlomas arba apdorojamas išmokas, atskaitymus ir darbuotojų kompensacijų planus.</span><span class="sxs-lookup"><span data-stu-id="15f5e-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="15f5e-106">Šioje temoje pateikiama informacija apie tai, kaip nustatyti ir tvarkyti išmokas.</span><span class="sxs-lookup"><span data-stu-id="15f5e-106">This topic provides information about how to set up an manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="15f5e-107">Išmokų nustatymas</span><span class="sxs-lookup"><span data-stu-id="15f5e-107">Benefit setup</span></span>
-------------

<span data-ttu-id="15f5e-108">Norėdami, kad darbuotojams būtų paskirtos išmokos, turite sukurti kiekvienos išmokos elementus.</span><span class="sxs-lookup"><span data-stu-id="15f5e-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="15f5e-109">Šie elementai sujungia panašius išmokų planus ir nustatyto numatytuosius parametrus, pvz., atskaitymo kursus ir apskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="15f5e-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="15f5e-110">Daugelį šių parametrų galima koreguoti vėliau, kai darbuotojams paskiriamos išmokos.</span><span class="sxs-lookup"><span data-stu-id="15f5e-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="15f5e-111">Kiekvienam išmokų planui organizacija gali pasiūlyti kelias registracijos pasirinktis arba darbuotojas gali atsisakyti registracijos plane.</span><span class="sxs-lookup"><span data-stu-id="15f5e-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="15f5e-112">[![Išmokos proceso srautas](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="15f5e-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="15f5e-113">Išmokos elementai</span><span class="sxs-lookup"><span data-stu-id="15f5e-113">Benefit elements</span></span>
<span data-ttu-id="15f5e-114">Prieš pradėdami kurti išmokas ir registruoti jose darbuotojus, turite nurodyti elementus, kurie sudaro išmoką: tipas, planas ir pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="15f5e-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="15f5e-115">**Tipas** – konkrečios išmokos, pvz., medicininės arba automobilio stovėjimo, planų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="15f5e-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="15f5e-116">**Planas** – konkreti išmoka, gaunama iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="15f5e-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="15f5e-117">**Parinktis** – aprėpties lygis, pvz., tik darbuotojas arba darbuotojas ir sutuoktinis / partneris.</span><span class="sxs-lookup"><span data-stu-id="15f5e-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="15f5e-118">Kiekvienam išmokos tipui, pvz., regėjimo ar dantų gydymo, organizacija savo darbuotojams gali pasiūlyti vieną ar kelis planus.</span><span class="sxs-lookup"><span data-stu-id="15f5e-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="15f5e-119">Kiekvienam planui organizacija gali pasiūlyti skirtingas pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="15f5e-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="15f5e-120">Pvz., darbuotojai, gali įsigyti papildomo laikotarpio gyvybės draudimą, kurio vertė atitinka vieną, du ar tris jų metinius atlyginimus.</span><span class="sxs-lookup"><span data-stu-id="15f5e-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="15f5e-121">Kiekvienas plano ir pasirinkčių derinys tampa išmoka, kurią gali gauti darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="15f5e-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="15f5e-122">[![išmokų paveikslėlis](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="15f5e-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="15f5e-123">Tinkamumas</span><span class="sxs-lookup"><span data-stu-id="15f5e-123">Eligibility</span></span>
<span data-ttu-id="15f5e-124">Darbuotojo tinkamumas įvairiems darbdavio siūlomiems išmokų tipams priklauso nuo daugelio faktorių.</span><span class="sxs-lookup"><span data-stu-id="15f5e-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="15f5e-125">Kai sukuriate „Microsoft Talent“ išmoką, galite nustatyti tai išmokai taikomą tinkamumo tipą.</span><span class="sxs-lookup"><span data-stu-id="15f5e-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="15f5e-126">Galite nustatyti, kad išmoka būtų prieinama visiems darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="15f5e-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="15f5e-127">Pavyzdžiui, kai kuriose įmonėse kaip papildoma išmoka siūlomi automobilių stovėjimo leidimai.</span><span class="sxs-lookup"><span data-stu-id="15f5e-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="15f5e-128">Sukūrę šią išmoką nustatote tinkamumo pasirinktį **Taikoma visiems darbuotojams**.</span><span class="sxs-lookup"><span data-stu-id="15f5e-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="15f5e-129">Kitoms išmokoms, pvz., pinigų arešto ir mokesčių, tinkamumas negalioja.</span><span class="sxs-lookup"><span data-stu-id="15f5e-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="15f5e-130">Kai kuriate šiuos išmokų tipus, galite nustatyti tinkamumo pasirinktį **Apeiti tinkamumo procesą**.</span><span class="sxs-lookup"><span data-stu-id="15f5e-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="15f5e-131">Galiausiai tinkamumas išmokai gali būti pagrįstas taisykle.</span><span class="sxs-lookup"><span data-stu-id="15f5e-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="15f5e-132">Pavyzdžiui, įmonė darbuotojams siūlo dviejų tipų gyvybės draudimo išmokas.</span><span class="sxs-lookup"><span data-stu-id="15f5e-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="15f5e-133">Vadovaujantys darbuotojai gali gauti vieną gyvybės draudimo planą, o visi kiti visu etatu dirbantys darbuotojai – kitą gyvybės draudimo planą.</span><span class="sxs-lookup"><span data-stu-id="15f5e-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="15f5e-134">Programoje „Talent“ norėdami rasti visus vadovaujančius darbuotojus, galite sukurti tinkamumo išmokai taisyklę, o norėdami rasti visus kitus visu etatu dirbančius darbuotojus – kitą taisyklę ir taikyti šias taisykles atitinkamai išmokai.</span><span class="sxs-lookup"><span data-stu-id="15f5e-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="15f5e-135">Registracija</span><span class="sxs-lookup"><span data-stu-id="15f5e-135">Enrollment</span></span>
<span data-ttu-id="15f5e-136">Sukūrę jūsų organizacijos siūlomas išmokas ir nustatę tinkamumą, galite registruoti darbuotojus išmokoms gauti.</span><span class="sxs-lookup"><span data-stu-id="15f5e-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="15f5e-137">Išmokoms gauti galite užregistruoti vieną darbuotoją, arba vienai arba kelioms išmokoms gauti galite užregistruoti daug darbuotojų vienu metu.</span><span class="sxs-lookup"><span data-stu-id="15f5e-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="15f5e-138">Kartais organizacija liaujasi siūliusi tam tikras išmokas.</span><span class="sxs-lookup"><span data-stu-id="15f5e-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="15f5e-139">Tokiu atveju turite atnaujinti išmoką ir darbuotojus, kurie užregistruoti jai gauti.</span><span class="sxs-lookup"><span data-stu-id="15f5e-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="15f5e-140">Visuotinės išmokos galiojimo pabaigos parinktis vienu metu leidžia keisti išmokos ir darbuotojų registracijos tai išmokai gauti galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="15f5e-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="15f5e-141">Taip pat galite pasirinkti kelis darbuotojus, kurie užregistruojami gauti išmoką, ir pakeisti taikymo pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="15f5e-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="15f5e-142">Be to, jei nusprendėte, kad išmoką norėsite pasiūlyti ilgesniam laikotarpiui negu buvo planuota, visuotinės išmokos plėtinys leidžia pratęsti išmokos ir darbuotojų registracijos tai išmokai gauti galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="15f5e-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="see-also"></a><span data-ttu-id="15f5e-143">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="15f5e-143">See also</span></span>
--------

[<span data-ttu-id="15f5e-144">Išmokų tinkamumo strategijos</span><span class="sxs-lookup"><span data-stu-id="15f5e-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)



