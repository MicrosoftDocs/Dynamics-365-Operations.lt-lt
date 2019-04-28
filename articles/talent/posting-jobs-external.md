---
title: Darbo skelbimų registravimas išorinėse karjeros svetainėse iš „Attract“
description: Šioje temoje paaiškinama, kaip naudoti „Dynamics 365 for Talent - Attract“ darbo skelbimams išorinėse įdarbinimo svetainėse registruoti
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/15/2019
ms.locfileid: "993673"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="b9b01-103">Darbo skelbimų registravimas išorinėse karjeros svetainėse iš „Attract“</span><span class="sxs-lookup"><span data-stu-id="b9b01-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b01-104">Juk norite, kad apie jūsų siūlomas laisvas pareigas sužinotų kiek įmanoma daugiau kvalifikuotų kandidatų.</span><span class="sxs-lookup"><span data-stu-id="b9b01-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="b9b01-105">Įdarbinimo svetainės, pvz., „Broadbean“ gali padėti šį tikslą pasiekti.</span><span class="sxs-lookup"><span data-stu-id="b9b01-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="b9b01-106">Naudodamiesi „Microsoft Dynamics 365 Talent: Attract“ dabar galite registruoti darbo skelbimus „Broadbean“ ir šioje srityje „Microsoft“ nuolat teikia naujų pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="b9b01-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="b9b01-107">Darbo skelbimų registravimas „Broadbean“</span><span class="sxs-lookup"><span data-stu-id="b9b01-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="b9b01-108">Norėdami registruoti darbo skelbimus „Broadbean“, turite sukonfigūruoti „Broadbean“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="b9b01-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="b9b01-109">Norėdami registruoti užduotis išorinėse svetainėse, turite turėti [išsamios įdarbinimo informacijos priedą](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="b9b01-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="b9b01-110">Šiuo metu ši funkcija yra peržiūrima.</span><span class="sxs-lookup"><span data-stu-id="b9b01-110">This feature is currently in preview.</span></span> <span data-ttu-id="b9b01-111">Jei norite ją išbandyti, turite [įjungti šią funkciją „Attract“ administratoriaus parametrų srityje](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="b9b01-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="b9b01-112">„Broadbean“ integravimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b9b01-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="b9b01-113">Prisijunkite prie „Attract“ kaip administratorius.</span><span class="sxs-lookup"><span data-stu-id="b9b01-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="b9b01-114">Paspauskite viršutiniame dešiniajame puslapio kampe esantį mygtuką **Parametrai** (krumpliaračio simbolis), o paskui pasirinkite **Administravimo centras**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="b9b01-115">Skirtuko **Darbo skelbimų lentos nustatymai** skyriuje **Įjungti „Broadbean“ integravimą** įjunkite integravimą.</span><span class="sxs-lookup"><span data-stu-id="b9b01-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="b9b01-116">Susisiekite su „Broadbean“ ir srityje **Vartotojo vardas, kliento ID, šifravimo raktas** įveskite savo informaciją.</span><span class="sxs-lookup"><span data-stu-id="b9b01-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="b9b01-117">Jūsų „Broadbean“ kredencialai yra slapta ir konfidenciali informacija.</span><span class="sxs-lookup"><span data-stu-id="b9b01-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="b9b01-118">Todėl juos saugodami ir bendrindami elkitės atsakingai.</span><span class="sxs-lookup"><span data-stu-id="b9b01-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="b9b01-119">Šiuos kredencialus gali matyti visi, kuriems suteiktas „Attract“ administratoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="b9b01-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="b9b01-120">„Microsoft“ ir „Attract“ šių verčių nekuria ir jų netvarko.</span><span class="sxs-lookup"><span data-stu-id="b9b01-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="b9b01-121">Jūs esate atsakingi už jų atnaujinimą „Attract“ ir už tai, kad naudojantis „Broadbean“ būtų išspręstos visos su jūsų kredencialais susijusios problemos.</span><span class="sxs-lookup"><span data-stu-id="b9b01-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="b9b01-122">Darbo skelbimo registravimas „Broadbean“</span><span class="sxs-lookup"><span data-stu-id="b9b01-122">Post a job to Broadbean</span></span>

<span data-ttu-id="b9b01-123">Įjungę „Broadbean“, darbdaviai ir administratoriai ten gali užregistruoti darbo skelbimą.</span><span class="sxs-lookup"><span data-stu-id="b9b01-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="b9b01-124">Turite turėti darbo skelbimo prašymo URL.</span><span class="sxs-lookup"><span data-stu-id="b9b01-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="b9b01-125">Naudodamiesi „Attract“, atidarykite darbo skelbimą, kurį norite užregistruoti „Broadbean“.</span><span class="sxs-lookup"><span data-stu-id="b9b01-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="b9b01-126">Skyriuje **Registravimai** paspauskite „Broadbean“ atitinkantį mygtuką **Registruoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="b9b01-127">Vadovaukitės „Broadbean“ lange pateikiamais nurodymais.</span><span class="sxs-lookup"><span data-stu-id="b9b01-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="b9b01-128">„Attract“ perduoda „Broadbean“ toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="b9b01-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="b9b01-129">Užklausos ID</span><span class="sxs-lookup"><span data-stu-id="b9b01-129">Request ID</span></span>
- <span data-ttu-id="b9b01-130">Pareigos</span><span class="sxs-lookup"><span data-stu-id="b9b01-130">Job title</span></span>
- <span data-ttu-id="b9b01-131">Darbo aprašas</span><span class="sxs-lookup"><span data-stu-id="b9b01-131">Job description</span></span>
- <span data-ttu-id="b9b01-132">Darbo vieta</span><span class="sxs-lookup"><span data-stu-id="b9b01-132">Job location</span></span>
- <span data-ttu-id="b9b01-133">Prašymo URL</span><span class="sxs-lookup"><span data-stu-id="b9b01-133">Apply URL</span></span>
- <span data-ttu-id="b9b01-134">Įdarbintojo informacija</span><span class="sxs-lookup"><span data-stu-id="b9b01-134">Recruiter information</span></span>

<span data-ttu-id="b9b01-135">„Broadbean“ sėkmingai užbaigus registravimą, „Attract“ darbo skelbimo skyriuje **Registravimai** rodoma „Broadbean“ būsena **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="b9b01-136">Naudojantis „Broadbean“ reikia užpildyti lauką **Rinka**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="b9b01-137">Šiuo metu pagal numatytuosius parametrus nustatyta šio lauko parinktis **IT**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="b9b01-138">Tačiau galite keisti šią vertę, „Broadbean“ darbo skelbimų registravimo lange nurodydami teisingą rinką.</span><span class="sxs-lookup"><span data-stu-id="b9b01-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="b9b01-139">Kol „Broadbean“ baigs registruoti jūsų darbo skelbimą visose jūsų pasirinktose darbo skelbimų lentose, praeis šiek tiek laiko.</span><span class="sxs-lookup"><span data-stu-id="b9b01-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="b9b01-140">Todėl „Attract“ gali šiek tiek vėluoti pateikti atnaujintą darbo skelbimo būseną.</span><span class="sxs-lookup"><span data-stu-id="b9b01-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="b9b01-141">„Broadbean“ darbo skelbimo registravimo peržiūra</span><span class="sxs-lookup"><span data-stu-id="b9b01-141">View a Broadbean job posting</span></span>

<span data-ttu-id="b9b01-142">Užregistravę darbo skelbimą „Broadbean“, galite jį peržiūrėti „Attract“.</span><span class="sxs-lookup"><span data-stu-id="b9b01-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="b9b01-143">Naudodamiesi „Attract“, atidarykite darbo skelbimą, kurį norite peržiūrėti „Broadbean“.</span><span class="sxs-lookup"><span data-stu-id="b9b01-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="b9b01-144">Skyriuje **Registravimai** paspauskite „Broadbean“ atitinkantį daugtaškio mygtuką (**...**), o paskui pasirinkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="b9b01-145">Užregistruotas „Broadbean“ darbo skelbimas rodomas naujame lange.</span><span class="sxs-lookup"><span data-stu-id="b9b01-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="b9b01-146">„Broadbean“ darbo skelbimo registravimo naujinimas</span><span class="sxs-lookup"><span data-stu-id="b9b01-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="b9b01-147">Norėdami atnaujinti užregistruotą „Broadbean“ darbo skelbimą, tai galite padaryti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="b9b01-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="b9b01-148">Naudodamiesi „Attract“, atidarykite darbo skelbimą, kurį norite atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="b9b01-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="b9b01-149">Skyriuje **Registravimai** paspauskite „Broadbean“ atitinkantį mygtuką **Naujinti skelbimą**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="b9b01-150">Redaguokite užregistruotą skelbimą „Broadbean“ lange.</span><span class="sxs-lookup"><span data-stu-id="b9b01-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="b9b01-151">arba,</span><span class="sxs-lookup"><span data-stu-id="b9b01-151">–or–</span></span>

1. <span data-ttu-id="b9b01-152">Naudodamiesi „Attract“, atidarykite darbo skelbimą, kurį norite peržiūrėti „Broadbean“.</span><span class="sxs-lookup"><span data-stu-id="b9b01-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="b9b01-153">Skyriuje **Registravimai** paspauskite „Broadbean“ atitinkantį daugtaškio mygtuką (**...**), o paskui pasirinkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="b9b01-154">„Broadbean“ lange redaguokite darbo skelbime nurodytą informaciją, o paskui iš naujo užregistruokite darbo skelbimą.</span><span class="sxs-lookup"><span data-stu-id="b9b01-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="b9b01-155">„Attract“ rodoma darbo skelbimo informacija nepasikeičia.</span><span class="sxs-lookup"><span data-stu-id="b9b01-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="b9b01-156">„Broadbean“ darbo skelbimo šalinimas</span><span class="sxs-lookup"><span data-stu-id="b9b01-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="b9b01-157">Prireikus galite pašalinti darbo skelbimą iš „Broadbean“.</span><span class="sxs-lookup"><span data-stu-id="b9b01-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="b9b01-158">Naudodamiesi „Attract“, atidarykite darbo skelbimą, kurį norite pašalinti.</span><span class="sxs-lookup"><span data-stu-id="b9b01-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="b9b01-159">Skyriuje **Registravimai** paspauskite „Broadbean“ atitinkantį daugtaškio mygtuką (**...**), o paskui pasirinkite **Pašalinti skelbimą**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="b9b01-160">„Broadbean“ pašalinus darbo skelbimą, „Attract“ esantis „Broadbean“ elementas turi mygtuką **Registruoti dabar**.</span><span class="sxs-lookup"><span data-stu-id="b9b01-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="b9b01-161">Jei yra šis mygtukas, tai reiškia, kad darbo skelbimas buvo pašalintas ir galima jį registruoti dar kartą.</span><span class="sxs-lookup"><span data-stu-id="b9b01-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="b9b01-162">„Broadbean“ integravimo trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="b9b01-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="b9b01-163">Susidūrę su problemomis registruodami darbo skelbimą „Broadbean“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b9b01-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="b9b01-164">Patikrinkite, ar „Attract“ įvesti teisingi „Broadbean“ kredencialai.</span><span class="sxs-lookup"><span data-stu-id="b9b01-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="b9b01-165">Jei kredencialai teisingi, susisiekite su [„Broadbean“ pagalbos tarnyba](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="b9b01-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="b9b01-166">Iškilus problemų, kreipkitės į [„Microsoft“ pagalbos tarnybą](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="b9b01-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
