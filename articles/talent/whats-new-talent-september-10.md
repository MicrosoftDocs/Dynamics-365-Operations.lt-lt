---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. rugsėjo 10 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896755"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="a061f-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. rugsėjo 10 d.)</span><span class="sxs-lookup"><span data-stu-id="a061f-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="a061f-104">**8.1.138.0 versija**</span><span class="sxs-lookup"><span data-stu-id="a061f-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="a061f-105">Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent: Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="a061f-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="a061f-106">Leiskite nedarbo laiko užklausose naudoti konkretų dienos laiką (pusdieniai)</span><span class="sxs-lookup"><span data-stu-id="a061f-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="a061f-107">Jei atostogos ir neatvykimas nustatomas taip, kad nedarbo laiko pateikiamas dienomis, dabar galite įjungti pusės dienos apibrėžtį.</span><span class="sxs-lookup"><span data-stu-id="a061f-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="a061f-108">Tada, kai vartotojai pateikia nedarbo laiko užklausas, jie gali nurodyti, ar jie teikia užklausą dėl pirmosios, ar dėl antrosios dienos pusės.</span><span class="sxs-lookup"><span data-stu-id="a061f-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="a061f-109">Pagal numatytuosius parametrus ši parinktis yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="a061f-109">By default, this option is turned off.</span></span> <span data-ttu-id="a061f-110">Tam, kad darbuotojai galėtų kreiptis dėl pirmosios arba antrosios dienos pusės, turite įjungti šią parinktį personalo parametrų srityje **Atostogos ir neatvykimas**.</span><span class="sxs-lookup"><span data-stu-id="a061f-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="a061f-111">Šios funkcijos saugos teisė yra Tvarkyti personalo parametrus.</span><span class="sxs-lookup"><span data-stu-id="a061f-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="a061f-112">Atostogų ir neatvykimo įrašų tikrinimas</span><span class="sxs-lookup"><span data-stu-id="a061f-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="a061f-113">Atsižvelgiant į tai, kaip sukonfigūruotos atostogos, darbuotojai, kurie bando teikti užklausą dėl nedarbo laiko, kuris ilgesnis už jų darbo dieną, gaus įspėjamąjį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="a061f-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="a061f-114">Kitaip tariant, jie įspėjami, jei jie bando pateikti ilgesnio nei bet kuri visa darbo diena nedarbo laiko užklausą.</span><span class="sxs-lookup"><span data-stu-id="a061f-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="a061f-115">Šis tikrinimas yra visada įjungtas.</span><span class="sxs-lookup"><span data-stu-id="a061f-115">This validation is always turned on.</span></span> <span data-ttu-id="a061f-116">Kai tik darbuotojai viršija nurodytą darbo dienos ribą, teikdami nedarbo laiko užklausą jie gauna įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="a061f-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="a061f-117">Darbo eigų sąlyginių sakinių papildomi laukai</span><span class="sxs-lookup"><span data-stu-id="a061f-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="a061f-118">Papildomi laukai įtraukti į sąlyginius sakinius ir vietos rezervavimo ženklus keliose „Core HR“ darbo eigose.</span><span class="sxs-lookup"><span data-stu-id="a061f-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="a061f-119">Toliau nurodyti lauki įtraukti į kompensacijos, atleidimo ir perkėlimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="a061f-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="a061f-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="a061f-120">EmploymentType</span></span>
- <span data-ttu-id="a061f-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="a061f-121">LegalEntity</span></span>
- <span data-ttu-id="a061f-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="a061f-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="a061f-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="a061f-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="a061f-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="a061f-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="a061f-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="a061f-125">TransitionDate</span></span>
- <span data-ttu-id="a061f-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="a061f-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="a061f-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="a061f-127">WorkerStartDate</span></span>
- <span data-ttu-id="a061f-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="a061f-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="a061f-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="a061f-129">ProbationEndDate</span></span>
- <span data-ttu-id="a061f-130">Pozicija</span><span class="sxs-lookup"><span data-stu-id="a061f-130">Position</span></span>
- <span data-ttu-id="a061f-131">Sąjunga</span><span class="sxs-lookup"><span data-stu-id="a061f-131">Union</span></span>
- <span data-ttu-id="a061f-132">Skyrius</span><span class="sxs-lookup"><span data-stu-id="a061f-132">Department</span></span>
- <span data-ttu-id="a061f-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="a061f-133">PositionType</span></span>
- <span data-ttu-id="a061f-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="a061f-134">CompLocation</span></span>
- <span data-ttu-id="a061f-135">Pareigos</span><span class="sxs-lookup"><span data-stu-id="a061f-135">Title</span></span>
- <span data-ttu-id="a061f-136">Darbas</span><span class="sxs-lookup"><span data-stu-id="a061f-136">Job</span></span>
- <span data-ttu-id="a061f-137">JobType</span><span class="sxs-lookup"><span data-stu-id="a061f-137">JobType</span></span>
- <span data-ttu-id="a061f-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="a061f-138">JobFamily</span></span>
- <span data-ttu-id="a061f-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="a061f-139">JobFunction</span></span>

<span data-ttu-id="a061f-140">Toliau nurodyti lauki įtraukti į pareigų darbo eigą</span><span class="sxs-lookup"><span data-stu-id="a061f-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="a061f-141">Pozicija</span><span class="sxs-lookup"><span data-stu-id="a061f-141">Position</span></span>
- <span data-ttu-id="a061f-142">Sąjunga</span><span class="sxs-lookup"><span data-stu-id="a061f-142">Union</span></span>
- <span data-ttu-id="a061f-143">Skyrius</span><span class="sxs-lookup"><span data-stu-id="a061f-143">Department</span></span>
- <span data-ttu-id="a061f-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="a061f-144">PositionType</span></span>
- <span data-ttu-id="a061f-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="a061f-145">CompLocation</span></span>
- <span data-ttu-id="a061f-146">Pareigos</span><span class="sxs-lookup"><span data-stu-id="a061f-146">Title</span></span>
- <span data-ttu-id="a061f-147">Darbas</span><span class="sxs-lookup"><span data-stu-id="a061f-147">Job</span></span>
- <span data-ttu-id="a061f-148">JobType</span><span class="sxs-lookup"><span data-stu-id="a061f-148">JobType</span></span>
- <span data-ttu-id="a061f-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="a061f-149">JobFamily</span></span>
- <span data-ttu-id="a061f-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="a061f-150">JobFunction</span></span>

<span data-ttu-id="a061f-151">Sąlyginių sakinių ir vietos rezervavimo ženklų laukai pasiekiami visiems vartotojams, kurie turi teisę konfigūruoti pirmiau minėtas darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="a061f-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="a061f-152">„Attract“ atidarymas personalo valdymo srities</span><span class="sxs-lookup"><span data-stu-id="a061f-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="a061f-153">Jei „Attract“ nenustatyta, personalo valdymo sritis **Samdytini kandidatai** nurodo vartotojams pradėti „Attract“, o ne parodo pranešimą „Turinio, kurį būtų galima pateikti, nerasta.“</span><span class="sxs-lookup"><span data-stu-id="a061f-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="a061f-154">Kiti pakeitimai</span><span class="sxs-lookup"><span data-stu-id="a061f-154">Other changes</span></span>

<span data-ttu-id="a061f-155">Šiame leidime įtraukti keli papildomi klaidų ištaisymai.</span><span class="sxs-lookup"><span data-stu-id="a061f-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="a061f-156">Kai pasamdomas rangovas, skirtukas **Kompensacija** nebus rodomas užklausos / veiksmo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a061f-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="a061f-157">Atleidimo užklausos proceso metu negalima tęsti tol, kol visuose būtinuose laukuose bus duomenų.</span><span class="sxs-lookup"><span data-stu-id="a061f-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="a061f-158">Rikiavimo tvarkos ir datos rodymo problemos personalo valdymo analizėje išspręstos.</span><span class="sxs-lookup"><span data-stu-id="a061f-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
