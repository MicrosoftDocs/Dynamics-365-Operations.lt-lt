---
title: Kandidatų išteklių sekimas „Attract“
description: Šioje temoje pateikiama informacija apie kandidatų profilių ir prašymų šaltinio sekimą.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8860f508eebc377042c4e101eeb08a14a737ba0c
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832672"
---
# <a name="track-candidate-sources-in-attract"></a><span data-ttu-id="fcc69-103">Kandidatų išteklių sekimas „Attract“</span><span class="sxs-lookup"><span data-stu-id="fcc69-103">Track candidate sources in Attract</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="fcc69-104">Šioje temoje nurodytomis funkcijomis galima naudotis kaip peržiūros leidimo dalimi.</span><span class="sxs-lookup"><span data-stu-id="fcc69-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="fcc69-105">Turinys ir funkcijos gali būti keičiami.</span><span class="sxs-lookup"><span data-stu-id="fcc69-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="fcc69-106">Norėdami naudotis šia funkcija, paprašykite administratoriaus, kad įjungtų ją „Attract“ naudodamasis sritimi **Administratoriaus parametrai**.</span><span class="sxs-lookup"><span data-stu-id="fcc69-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="fcc69-107">Būsimame leidime bus pateiktos šaltinio sekimo ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="fcc69-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="fcc69-108">Daugiau informacijos rasite [Prieiga prie „Talent“ peržiūros funkcijų](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="fcc69-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="fcc69-109">Kai kandidatai kreipiasi dėl darbo, „Attract“ automatiškai seka jų prašymų šaltinį ir suteikia jums vertingos informacijos, kad galėtumėte tinkamai išnaudoti įdarbinimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fcc69-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="fcc69-110">Įdarbintojai ir samdos vadovai taip pat gali pasirinkti prašymo šaltinį, kai jie neautomatiškai įtraukia kandidatą į darbų arba talentų telkinį.</span><span class="sxs-lookup"><span data-stu-id="fcc69-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="fcc69-111">Prašymo šaltinį galite peržiūrėti prašymų veiklos informacijos skirtuke **Veiklos**, taip pat – prašymų retrospektyvoje, kuri pateikta talentų telkinių skiltyje **Profilis**.</span><span class="sxs-lookup"><span data-stu-id="fcc69-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="fcc69-112">Kandidato profilio šaltinį galite rasti kandidato informacijoje skirtuke **Profilis** tiek prašymų, tiek talentų telkiniuose.</span><span class="sxs-lookup"><span data-stu-id="fcc69-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="fcc69-113">Proceso šablonus galite rasti [išsamios įdarbinimo informacijos priede](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="fcc69-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="fcc69-114">Iš anksto sukonfigūruoti šaltiniai</span><span class="sxs-lookup"><span data-stu-id="fcc69-114">Pre-configured sources</span></span>

<span data-ttu-id="fcc69-115">Numatytajame šaltinių sąraše yra bendri prašymų šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="fcc69-115">The default source list contains common application sources.</span></span> <span data-ttu-id="fcc69-116">Kai kuriems šaltinių tipams, pvz., **Darbo skelbimų lenta** ir **Socialinis tinklas**, priskirta papildoma šaltinio informacija.</span><span class="sxs-lookup"><span data-stu-id="fcc69-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="fcc69-117">Pvz., tipas **Socialinis tinklas** apima „Facebook“ ir „Twitter“.</span><span class="sxs-lookup"><span data-stu-id="fcc69-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="fcc69-118">Šaltinio tipas **Rekomendacija** suteikia galimybę nurodyti vidinį darbuotoją kaip rekomendavusį asmenį.</span><span class="sxs-lookup"><span data-stu-id="fcc69-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="fcc69-119">Numatytajame šaltinių sąraše yra toliau nurodyti iš anksto sukonfigūruoti šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="fcc69-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="fcc69-120">„Attract“ karjeros svetainė</span><span class="sxs-lookup"><span data-stu-id="fcc69-120">Attract career site</span></span>

-   <span data-ttu-id="fcc69-121">Agentūra</span><span class="sxs-lookup"><span data-stu-id="fcc69-121">Agency</span></span>

-   <span data-ttu-id="fcc69-122">Karjeros mugė</span><span class="sxs-lookup"><span data-stu-id="fcc69-122">Career Fair</span></span>

-   <span data-ttu-id="fcc69-123">Įmonės rinkodara</span><span class="sxs-lookup"><span data-stu-id="fcc69-123">Company Marketing</span></span>

-   <span data-ttu-id="fcc69-124">Konferencijos ir prekybos parodos</span><span class="sxs-lookup"><span data-stu-id="fcc69-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="fcc69-125">Profesinė asociacija</span><span class="sxs-lookup"><span data-stu-id="fcc69-125">Professional Association</span></span>

-   <span data-ttu-id="fcc69-126">Darbo skelbimų lenta</span><span class="sxs-lookup"><span data-stu-id="fcc69-126">Job board</span></span>

    -   <span data-ttu-id="fcc69-127">Iš tikrųjų</span><span class="sxs-lookup"><span data-stu-id="fcc69-127">Indeed</span></span>

    -   <span data-ttu-id="fcc69-128">Ieškoti</span><span class="sxs-lookup"><span data-stu-id="fcc69-128">Seek</span></span>

    -   <span data-ttu-id="fcc69-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="fcc69-129">CareerBuilder</span></span>

    -   <span data-ttu-id="fcc69-130">„Google“ užduotys</span><span class="sxs-lookup"><span data-stu-id="fcc69-130">Google Jobs</span></span>

    -   <span data-ttu-id="fcc69-131">Xing</span><span class="sxs-lookup"><span data-stu-id="fcc69-131">Xing</span></span>

    -   <span data-ttu-id="fcc69-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="fcc69-132">Glassdoor</span></span>

    -   <span data-ttu-id="fcc69-133">„Monster“ užduotys</span><span class="sxs-lookup"><span data-stu-id="fcc69-133">Monster Jobs</span></span>

-   <span data-ttu-id="fcc69-134">Žurnalai ir publikacijos</span><span class="sxs-lookup"><span data-stu-id="fcc69-134">Magazines & Publications</span></span>

-   <span data-ttu-id="fcc69-135">Socialinis tinklas</span><span class="sxs-lookup"><span data-stu-id="fcc69-135">Social Network</span></span>

    -   <span data-ttu-id="fcc69-136">„Facebook“</span><span class="sxs-lookup"><span data-stu-id="fcc69-136">Facebook</span></span>

    -   <span data-ttu-id="fcc69-137">„Twitter“</span><span class="sxs-lookup"><span data-stu-id="fcc69-137">Twitter</span></span>

-   <span data-ttu-id="fcc69-138">Įdarbinimas universitete</span><span class="sxs-lookup"><span data-stu-id="fcc69-138">University Recruiting</span></span>

-   <span data-ttu-id="fcc69-139">„LinkedIn“</span><span class="sxs-lookup"><span data-stu-id="fcc69-139">LinkedIn</span></span>

-   <span data-ttu-id="fcc69-140">Suklasifikuota</span><span class="sxs-lookup"><span data-stu-id="fcc69-140">Classifieds</span></span>

-   <span data-ttu-id="fcc69-141">Rekomendacija</span><span class="sxs-lookup"><span data-stu-id="fcc69-141">Referral</span></span>

-   <span data-ttu-id="fcc69-142">Įtraukta įdarbintojo</span><span class="sxs-lookup"><span data-stu-id="fcc69-142">Added by Recruiter</span></span>

-   <span data-ttu-id="fcc69-143">Kitas</span><span class="sxs-lookup"><span data-stu-id="fcc69-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="fcc69-144">Šaltinių sąrašo tinkinimas</span><span class="sxs-lookup"><span data-stu-id="fcc69-144">Customize the source list</span></span> 

<span data-ttu-id="fcc69-145">Galite išplėsti šaltinių sąrašą ir įtraukti papildomų prašymų šaltinių.</span><span class="sxs-lookup"><span data-stu-id="fcc69-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="fcc69-146">Norėdami tinkinti šį sąrašą, vykdykite instrukcijas, pateiktas temoje [„Attract“ parinkčių rinkinių išplėtimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="fcc69-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="fcc69-147">Redaguokite objektą **TalentSource**, kad įtrauktumėte papildomų šaltinių.</span><span class="sxs-lookup"><span data-stu-id="fcc69-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="fcc69-148">Norėdami išvengti neigiamos įtakos vartotojo sąsajai (UI), neredaguokite ir nenaikinkite parinkties **TalentCategory** išvardijimo reikšmių (ne pavadinimų), skirtų toliau nurodytiems parametrams.</span><span class="sxs-lookup"><span data-stu-id="fcc69-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="fcc69-149">**Rekomendacija**</span><span class="sxs-lookup"><span data-stu-id="fcc69-149">**Referral**</span></span>
- <span data-ttu-id="fcc69-150">**„LinkedIn“**</span><span class="sxs-lookup"><span data-stu-id="fcc69-150">**LinkedIn**</span></span>
- <span data-ttu-id="fcc69-151">**Kitas**</span><span class="sxs-lookup"><span data-stu-id="fcc69-151">**Other**</span></span>

<span data-ttu-id="fcc69-152">Vietoj to galite išplėsti parinkties **TalentSource** išvardijimą, kad įtrauktumėte kitų šaltinių tipų.</span><span class="sxs-lookup"><span data-stu-id="fcc69-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
