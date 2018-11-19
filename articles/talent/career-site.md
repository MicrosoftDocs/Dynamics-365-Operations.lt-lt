---
title: "„Attract“ karjeros svetainės funkcijos"
description: "Šiame straipsnyje pateikta kandidatams skirtos karjeros svetainės funkcijos programoje „Microsoft Dynamics 365 for Talent - Attract“ apžvalga. Jame taip pat paaiškinama, kaip šią funkciją nustatyti."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="fd2fe-104">„Attract“ karjeros svetainės funkcijos</span><span class="sxs-lookup"><span data-stu-id="fd2fe-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd2fe-105">Šiame straipsnyje pateikta kandidatams skirtos karjeros svetainės funkcijos programoje „Microsoft Dynamics 365 for Talent: Attract“ apžvalga.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="fd2fe-106">Jame taip pat paaiškinama, kaip šią funkciją nustatyti.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="fd2fe-107">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="fd2fe-107">Overview</span></span>

<span data-ttu-id="fd2fe-108">„Attract“ suteikia vieną karjeros svetainę kiekvienai nuomotojo aplinkai.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="fd2fe-109">Pvz., jei organizacija naudoja kūrimo aplinką ir tikrinimo aplinką, viena karjeros svetainė skiriama kūrimo aplinkai, o kita karjeros svetainė skiriama tikrinimo aplinkai.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="fd2fe-110">Kiekviena karjeros svetainė yra **visiškai atskira** ir joje veikia atskiras autentifikavimo mechanizmas.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="fd2fe-111">Darbai ir kandidatų profiliai nėra bendrinami karjeros svetainėse.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="fd2fe-112">Pagal numatytuosius parametrus karjeros svetainė yra vieša.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-112">By default, the career site is public.</span></span> <span data-ttu-id="fd2fe-113">Todėl kandidatai neprisijungę gali peržiūrėti visas užduotis, kurios pažymėtos kaip išorinės.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="fd2fe-114">Tačiau, norėdami atlikti visus kitus veiksmus, kandidatų turi prisijungti.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="fd2fe-115">Karjeros svetainės valdymas</span><span class="sxs-lookup"><span data-stu-id="fd2fe-115">Career site management</span></span>

<span data-ttu-id="fd2fe-116">Parametrai valdo toliau nurodytus karjeros svetainės elementus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="fd2fe-117">**Organizacijos pavadinimas:** organizacijos pavadinimas rodomas karjeros svetainės naršymo juostos viršuje.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="fd2fe-118">Pasirinkdami organizacijos pavadinimą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="fd2fe-119">**Organizacijos logotipas:** organizacijos logotipo vaizdas rodomas viršutiniame kairiajame karjeros svetainės kampe.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="fd2fe-120">Pasirinkdami organizacijos logotipo vaizdą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="fd2fe-121">Norėdami nustatyti organizacijos pavadinimo ir logotipo reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite **Administravimo centras** meniu **Parametrai** meniu (krumpliaračio simbolis), tada pasirinkite skirtuką **Įmonės informacija**.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="fd2fe-122">Logotipo vaizdo, kuris rodomas karjeros svetainėje, aukštis yra fiksuotas – 20 pikselių (piks.).</span><span class="sxs-lookup"><span data-stu-id="fd2fe-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="fd2fe-123">Vaizdo, kurį įtraukiate į administravimo centrą, dydis atitinkamai pritaikomas.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="fd2fe-124">Todėl, priklausomai nuo vaizdo, plotis gali keistis.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="fd2fe-125">Karjeros svetainės URL</span><span class="sxs-lookup"><span data-stu-id="fd2fe-125">Career site URL</span></span>

<span data-ttu-id="fd2fe-126">Kai [registruojate išorinę užduotį](./Creating-jobs-Attract.md#postings) pirmą kartą, galite kopijuoti saitą **Teikti prašymą** iš „Attract“ programos.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="fd2fe-127">Šio saito URL bus pateiktas tokiu formatu: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="fd2fe-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="fd2fe-128">Karjeros svetainės URL yra antrinė saito **Teikti prašymą** URL eilutė.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="fd2fe-129">Jį sudaro visa informacija iki įmonės pavadinimo (imtinai).</span><span class="sxs-lookup"><span data-stu-id="fd2fe-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="fd2fe-130">Todėl prieš tai pateikiamo nuorodos **Teikti prašymą** URL karjeros svetainės URL yra `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="fd2fe-131">Autentifikavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="fd2fe-131">Authentication options</span></span>

<span data-ttu-id="fd2fe-132">Kandidatai gali naudoti toliau nurodytas prisijungimo prie „Attract“ karjeros svetainės parinktis.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="fd2fe-133">Asmeninė paskyra</span><span class="sxs-lookup"><span data-stu-id="fd2fe-133">Personal account:</span></span>

    - <span data-ttu-id="fd2fe-134">„LinkedIn“</span><span class="sxs-lookup"><span data-stu-id="fd2fe-134">LinkedIn</span></span>
    - <span data-ttu-id="fd2fe-135">„Microsoft“</span><span class="sxs-lookup"><span data-stu-id="fd2fe-135">Microsoft</span></span>
    - <span data-ttu-id="fd2fe-136">Google</span><span class="sxs-lookup"><span data-stu-id="fd2fe-136">Google</span></span>
    - <span data-ttu-id="fd2fe-137">„Facebook“</span><span class="sxs-lookup"><span data-stu-id="fd2fe-137">Facebook</span></span>

- <span data-ttu-id="fd2fe-138">Darbo arba mokyklos paskyra</span><span class="sxs-lookup"><span data-stu-id="fd2fe-138">Work or school account:</span></span>

    - <span data-ttu-id="fd2fe-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="fd2fe-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="fd2fe-140">„Azure AD“ prisijungimo funkcija skirta tik vidiniams kandidatams.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="fd2fe-141">Todėl ją gali naudoti tik vidiniai kandidatai, kurie naudoja savo įmonės „Azure AD“ kredencialus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="fd2fe-142">Pavyzdžiui, kandidatas, kuris šiuo metu yra „Contoso, Ltd“ darbuotojas, nori kreiptis dėl darbo nesusijusioje įmonėje, „Alpine Ski House“.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="fd2fe-143">Tokiu atveju prisijungimas bus nesėkmingas, jei darbuotojas bandys naudoti savo „Azure AD“ kredencialus, priklausančius „Contoso, Ltd“.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="fd2fe-144">Profilio kūrimas ir tvarkymas</span><span class="sxs-lookup"><span data-stu-id="fd2fe-144">Create and maintain a profile</span></span>

<span data-ttu-id="fd2fe-145">Prisijungę prie karjeros svetainės, kandidatai gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Mano profilis**, norėdami kurti ir tvarkyti savo profilį.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="fd2fe-146">Profilis apima asmeninę informaciją, informaciją apie darbo patirtį, išsilavinimą, dokumentus, saitus ir informaciją apie įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="fd2fe-147">Sukūręs profilį kandidatas gali jį naudoti norėdamas kreiptis dėl dominančio darbo.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="fd2fe-148">Be to, naudodama profilius „Attract“ sistema kandidatams gali rekomenduoti tinkamus darbus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="fd2fe-149">Tinkamo darbo paieška</span><span class="sxs-lookup"><span data-stu-id="fd2fe-149">Find the right job</span></span>

<span data-ttu-id="fd2fe-150">Darbų sąrašo puslapyje kandidatai gali ieškoti konkretaus darbo įvesdami ieškos terminus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="fd2fe-151">Ieškos funkcija ieško paieškos terminų pareigų pavadinimuose ir užduočių aprašymuose bei rodo atitinkamas užduotis kaip rezultatus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="fd2fe-152">Kandidatai gali bet kuriuo metu filtruoti rezultatus pagal užduoties vietą arba užduoties funkciją.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="fd2fe-153">Kandidatai taip pat gali peržiūrėti rekomenduojamų užduočių rinkinį karjeros svetainėje.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="fd2fe-154">Užduotys rekomenduojamos kandidatams pagal kandidato ankstesnius prašymus, profilį ir CV.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="fd2fe-155">Užduočių rekomendacijos rodomos tik jei karjeros svetainėje užregistruota ne mažiau kaip 10 užduočių ir jei kandidatas yra užpildęs savo profilį.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="fd2fe-156">Kreipimasis dėl darbo</span><span class="sxs-lookup"><span data-stu-id="fd2fe-156">Apply for jobs</span></span>

<span data-ttu-id="fd2fe-157">Radę tinkamą darbą kandidatai gali teikti prašymą naudodami darbo informacijos puslapio mygtuką **Teikti prašymą**.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="fd2fe-158">Tuo metu kandidatai gali sukurti visiškai naują profilį arba peržiūrėti esamo profilio informaciją.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="fd2fe-159">Kandidatų taip pat gali nusiųsti CV, jei reikia, ir tada pateikti prašymą įdarbinti.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="fd2fe-160">Prašymo būsenos tikrinimas</span><span class="sxs-lookup"><span data-stu-id="fd2fe-160">Check application status</span></span>

<span data-ttu-id="fd2fe-161">Kai kandidatai pateikia prašymą dėl vieno arba kelių darbų, jie gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Programos**, kad peržiūrėtų savo atidarytus ir uždarytus prašymus.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="fd2fe-162">Kai kandidatas atidaro vieną iš savo prašymų, jis mato dabartinį etapą ir visus veiksmų laukiančius elementus, kuriuos jie turi užpildyti.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="fd2fe-163">Pavyzdžiui, jei kandidatas turi nurodyti galimas asmeninio pokalbio datas, puslapyje rodomos galimos parinktys.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="fd2fe-164">Vidiniai darbai</span><span class="sxs-lookup"><span data-stu-id="fd2fe-164">Internal jobs</span></span>

<span data-ttu-id="fd2fe-165">Šiuo metu darbai, kurie pažymėti kaip vidiniai ir užregistruoti „Attract“ karjeros svetainėje, karjeros svetainėje nerodomi.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="fd2fe-166">Jie yra pasiekiami tik naudojant tiesioginį saito **Teikti prašymą** URL, kurį galima nukopijuoti iš „Attract“ programos.</span><span class="sxs-lookup"><span data-stu-id="fd2fe-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

