---
title: Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 13 d.)
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. balandžio 13 d.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 729490e7516d8c7aef7232c9f5c227d3207dcd68
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712429"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="2d117-103">Kas nauja arba pasikeitė „Dynamics 365 Human Resources” (2020 m. balandžio 13 d.)</span><span class="sxs-lookup"><span data-stu-id="2d117-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="2d117-104">Šiame straipsnyje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="2d117-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2d117-105">Pakeitimai taikomi 8.1.3136 komponavimo versijai.</span><span class="sxs-lookup"><span data-stu-id="2d117-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="2d117-106">Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="2d117-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="2d117-107">Nauji gamybos išleidimo intervalai</span><span class="sxs-lookup"><span data-stu-id="2d117-107">New production release cadence</span></span>

<span data-ttu-id="2d117-108">Šios savaitės leidime „Human Resources“ išleidimo intervalai keičiasi iš naujinimo kas savaitę į naujinimą kas dvi savaites.</span><span class="sxs-lookup"><span data-stu-id="2d117-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="2d117-109">Siekiant užtikrinti derėjimą su saugiomis diegimo praktikomis ir išlaikyti aukštus paslaugos stabilumo ir patikimumo standartus, paslaugų naujinimų diegimo procesas, taikomas visiems regionams, dabar tampa dviejų savaičių išleidimu.</span><span class="sxs-lookup"><span data-stu-id="2d117-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="2d117-110">Atlikti papildomi testavimai ir stebėjimai, kad galėtume užtikrinti sėkmingą diegimą kiekviename proceso etape.</span><span class="sxs-lookup"><span data-stu-id="2d117-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="2d117-111">Daugiau informacijos apie išleidimo intervalus žr. [Naujinimo procesas](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="2d117-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="2d117-112">Lauko Apvalinimo tikslumas negalima redaguoti nurodžius apvalinimo tipą (435616)</span><span class="sxs-lookup"><span data-stu-id="2d117-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="2d117-113">Atlikus šį pakeitimą, laukas **Apvalinimo tikslumas** galimas po lauko **Apvalinimo tipas** atnaujinimo.</span><span class="sxs-lookup"><span data-stu-id="2d117-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="2d117-114">Negalima redaguoti atostogų registracijos pabaigos datos, kai atostogų plane nėra kaupimo laikotarpių (413628)</span><span class="sxs-lookup"><span data-stu-id="2d117-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="2d117-115">Dabar galite redaguoti registracijos pabaigos datą ir negauti klaidos „Būtina užpildyti lauką Kaupimo datos pagrindas”.</span><span class="sxs-lookup"><span data-stu-id="2d117-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="2d117-116">Įdarbinimo objektas nesinchronizuojamas su „Common Data Service” (430834)</span><span class="sxs-lookup"><span data-stu-id="2d117-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="2d117-117">Šis pakeitimas pataiso problemą dėl įdarbinimo duomenų nesinchronizavimo su „Common Data Service” pridėjus finansinių dimensijų.</span><span class="sxs-lookup"><span data-stu-id="2d117-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="2d117-118">Darbo kalendoriaus laiko intervalo objekto kelių pirminių elementų pašalinimas (431775)</span><span class="sxs-lookup"><span data-stu-id="2d117-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="2d117-119">Šis pakeitimas pašalina **darbo kalendoriaus laiko intervalo** objekto kelis pirminius elementus.</span><span class="sxs-lookup"><span data-stu-id="2d117-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="2d117-120">Filtras, kuriame yra CAST funkcija, neveikia „OData” iškvietimo darbininko pareigų priskyrimo objekte (431699)</span><span class="sxs-lookup"><span data-stu-id="2d117-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="2d117-121">Šiame naujinime yra keitimas, leidžiantis filtrui, kuriame yra CAST funkcija, veikti „OData” **darbininko pareigų priskyrimo** objekte.</span><span class="sxs-lookup"><span data-stu-id="2d117-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2d117-122">Peržiūroje</span><span class="sxs-lookup"><span data-stu-id="2d117-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="2d117-123">Atostogų sustabdymas</span><span class="sxs-lookup"><span data-stu-id="2d117-123">Leave suspension</span></span>

<span data-ttu-id="2d117-124">Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą.</span><span class="sxs-lookup"><span data-stu-id="2d117-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="2d117-125">Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus.</span><span class="sxs-lookup"><span data-stu-id="2d117-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="2d117-126">Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą.</span><span class="sxs-lookup"><span data-stu-id="2d117-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="2d117-127">Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="2d117-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2d117-128">Perkėlimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="2d117-128">Carry forward rules</span></span>

<span data-ttu-id="2d117-129">Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="2d117-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2d117-130">Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="2d117-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2d117-131">Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2d117-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2d117-132">Žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="2d117-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="2d117-133">Objektas Įdarbinimo informacija</span><span class="sxs-lookup"><span data-stu-id="2d117-133">Employment Details entity</span></span>

<span data-ttu-id="2d117-134">Objektas **Įdarbinimo informacija** atnaujintas toliau nurodytais laukais.</span><span class="sxs-lookup"><span data-stu-id="2d117-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="2d117-135">**Mokėjimo dažnumas**</span><span class="sxs-lookup"><span data-stu-id="2d117-135">**PayFrequency**</span></span>
- <span data-ttu-id="2d117-136">**Įdarbinimo kategorijos ID**</span><span class="sxs-lookup"><span data-stu-id="2d117-136">**Employment Category ID**</span></span>
- <span data-ttu-id="2d117-137">**Įdarbinimo tipas**</span><span class="sxs-lookup"><span data-stu-id="2d117-137">**Employment Type**</span></span>
- <span data-ttu-id="2d117-138">**Įdarbinimo tipo ID**</span><span class="sxs-lookup"><span data-stu-id="2d117-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="2d117-139">**Išmokų įdarbinimo būsena**</span><span class="sxs-lookup"><span data-stu-id="2d117-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="2d117-140">Šių laukų nustatymo duomenys priklauso nuo išmokų valdymo įjungimo darbo srityje **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="2d117-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="2d117-141">Neužpildykite ir nenaujinkite šių laukų objekte **Įdarbinimo informacija**, nes importavimo metu įvyks klaidų.</span><span class="sxs-lookup"><span data-stu-id="2d117-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="2d117-142">„SharePoint“ peržiūra neveikia kai kuriose aplinkose</span><span class="sxs-lookup"><span data-stu-id="2d117-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="2d117-143">Jei dokumentų peržiūra, skirta dokumentams, saugomiems „SharePoint“, neveikia, bandykite atlikti tolesnę procedūrą.</span><span class="sxs-lookup"><span data-stu-id="2d117-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="2d117-144">Patikrinkite, ar administratoriaus vartotojo paskyra turi el. pašto adresą, susietą su vartotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="2d117-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="2d117-145">Šią informaciją galima peržiūrėti puslapyje **Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="2d117-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="2d117-146">Jei el. pašto adresas nenustatytas, turite įtraukti el. pašto adresą ir tiekėją naudodami „OData Excel“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="2d117-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="2d117-147">Pagal numatytuosius parametrus, „Excel“ dizaine nėra el. pašto adreso.</span><span class="sxs-lookup"><span data-stu-id="2d117-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="2d117-148">Turėsite redaguoti „Excel“ dizainą, įtraukti visus laukus, taikyti ir atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="2d117-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="2d117-149">Atlikę šiuos veiksmus, galėsite naujinti administratoriaus paskyrą.</span><span class="sxs-lookup"><span data-stu-id="2d117-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="2d117-150">Susieję administratoriaus paskyrą su el. pašto paskyra, prisijunkite prie „Human Resources“ naudodami administratoriaus kredencialus.</span><span class="sxs-lookup"><span data-stu-id="2d117-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="2d117-151">Atidarykite priedą „SharePoint“, kad pradėtumėte dokumento peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="2d117-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="2d117-152">Prisijunkite su kito vartotojo paskyra, kuri turi prieigą prie priedų, ir patikrinkite, ar peržiūra veikia kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="2d117-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d117-153">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2d117-153">See also</span></span>

[<span data-ttu-id="2d117-154">Kas nauja ar pasikeitė „Human Resources”</span><span class="sxs-lookup"><span data-stu-id="2d117-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2d117-155">„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga</span><span class="sxs-lookup"><span data-stu-id="2d117-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2d117-156">Atnaujinimo procesas</span><span class="sxs-lookup"><span data-stu-id="2d117-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2d117-157">Funkcijų valdymas</span><span class="sxs-lookup"><span data-stu-id="2d117-157">Manage features</span></span>](hr-admin-manage-features.md)