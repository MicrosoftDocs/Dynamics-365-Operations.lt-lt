---
title: Darbininko išmokų planų kūrimas
description: Galite sukurti darbininkų išmokų planus programoje „Microsoft Dynamics 365 Human Resources“, norėdami pasirinkti darbuotojams skirtus išmokų planus ir patvirtinti išmokų planų pasirinkimus.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: baa131b3bcab73d29c7059f6595f1e8943f8164f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804942"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="e3cbd-103">Darbininko išmokų planų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-103">Create worker benefit plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e3cbd-104">Galite sukurti darbininkų išmokų planus programoje „Microsoft Dynamics 365 Human Resources“, norėdami pasirinkti darbuotojams skirtus išmokų planus ir patvirtinti išmokų planų pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="e3cbd-105">Paprastai darbuotojai patys pasirenka išmokų planus naudodami darbuotojų savitarnos paslaugą, o tada išmokų administratorius patvirtina pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="e3cbd-106">Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Darbininkų išmokų planai**.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="e3cbd-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-107">Select **New**.</span></span>

3. <span data-ttu-id="e3cbd-108">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="e3cbd-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e3cbd-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-109">Field</span></span> | <span data-ttu-id="e3cbd-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e3cbd-111">Laikotarpis</span><span class="sxs-lookup"><span data-stu-id="e3cbd-111">Period</span></span> | <span data-ttu-id="e3cbd-112">Nurodo išmokų laikotarpį, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį, kad galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="e3cbd-113">Pavyzdžiui, pasirinkite laikotarpį, kurį sukūrėte, pavadintą 2015 m., kad patvirtintumėte visus 2015 m. registracijos išmokoms pasirinkimus.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="e3cbd-114">Darbininkas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-114">Worker</span></span> | <span data-ttu-id="e3cbd-115">Nurodo darbininką, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-116">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-116">Legal entity</span></span> | <span data-ttu-id="e3cbd-117">Nurodo juridinį subjektą, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-118">Padengimo parinktis</span><span class="sxs-lookup"><span data-stu-id="e3cbd-118">Coverage option</span></span> | <span data-ttu-id="e3cbd-119">Nurodo draudimo parinktį, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-120">Numatytoji</span><span class="sxs-lookup"><span data-stu-id="e3cbd-120">Default</span></span> | <span data-ttu-id="e3cbd-121">Išmokų planai filtruojami pagal tai, ar jie yra numatytieji planai.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="e3cbd-122">Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-123">Būsena</span><span class="sxs-lookup"><span data-stu-id="e3cbd-123">Status</span></span> | <span data-ttu-id="e3cbd-124">Išmokų planai filtruojami pagal jų būseną.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="e3cbd-125">Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-126">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-126">Confirmation</span></span> | <span data-ttu-id="e3cbd-127">Nurodo patvirtinimo būseną, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-128">Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="e3cbd-128">Cancellation</span></span> | <span data-ttu-id="e3cbd-129">Nurodo atšaukimo būseną, naudotiną planams filtruoti sparčiajame skirtuke Planai. Filtruokite planus, kad būtų lengviau pasirinkti visų plano įrašų pogrupį ir galėtumėte patvirtinti pogrupį.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="e3cbd-130">Galiojančios datos filtras</span><span class="sxs-lookup"><span data-stu-id="e3cbd-130">Effective date filter</span></span> | <span data-ttu-id="e3cbd-131">Filtruoja planus pagal tai, ar jie nebegaliojantys, aktyvūs, ar bus aktyvūs ateityje.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="e3cbd-132">Pažymėkite žymės langelius, atitinkančius planus, kuriuos norite matyti sparčiajame skirtuke Planai.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="e3cbd-133">Planai</span><span class="sxs-lookup"><span data-stu-id="e3cbd-133">Plans</span></span> | <span data-ttu-id="e3cbd-134">Sparčiajame skirtuke Planai pateikiami planai, atitinkantys nurodytus filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="e3cbd-135">Atitinkamos konfigūracijos parinktys, kurias nustatė HR darbuotojai ir registracijos pasirinkimai, kuriuos pasirinko darbuotojai, yra įtraukti į kiekvieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="e3cbd-136">Apibrėžtas laukas nurodo, ar yra tikrinimo nesutapimų dėl plano pasirinkimo.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="e3cbd-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e3cbd-137">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]