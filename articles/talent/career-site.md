---
title: „Attract“ karjeros svetainės funkcijos
description: Šioje temoje pateikiama „Attract“ kandidatams skirtos karjeros svetainės funkcijos apžvalga.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/13/2019
ms.locfileid: "389976"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="d8ce6-103">„Attract“ karjeros svetainės funkcijos</span><span class="sxs-lookup"><span data-stu-id="d8ce6-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d8ce6-104">Šioje temoje pateikiama „Microsoft Dynamics 365 for Talent: Attract“ kandidatams skirtos karjeros svetainės funkcijos apžvalga.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="d8ce6-105">Joje taip pat paaiškinama, kaip šią funkciją nustatyti.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="d8ce6-106">„Attract“ suteikia vieną karjeros svetainę kiekvienai nuomotojo aplinkai.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="d8ce6-107">Pvz., jei organizacija naudoja kūrimo aplinką ir tikrinimo aplinką, viena karjeros svetainė skiriama kūrimo aplinkai, o kita karjeros svetainė skiriama tikrinimo aplinkai.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="d8ce6-108">Kiekviena karjeros svetainė yra visiškai atskira ir joje veikia atskiras autentifikavimo mechanizmas.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="d8ce6-109">Darbai ir kandidatų profiliai nėra bendrinami karjeros svetainėse.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="d8ce6-110">Pagal numatytuosius parametrus karjeros svetainė yra vieša.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-110">By default, the career site is public.</span></span> <span data-ttu-id="d8ce6-111">Todėl kandidatai neprisijungę gali peržiūrėti visas užduotis, kurios pažymėtos kaip išorinės.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="d8ce6-112">Tačiau, norėdami atlikti visus kitus veiksmus, kandidatų turi prisijungti.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="d8ce6-113">Karjeros svetainės valdymas</span><span class="sxs-lookup"><span data-stu-id="d8ce6-113">Career site management</span></span>

<span data-ttu-id="d8ce6-114">Norėdami nustatyti toliau nurodytų elementų reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**. pateiktą meniu **Parametrai** (krumpliaračio simbolis), tada pasirinkite skirtuką **Įmonės informacija**.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="d8ce6-115">**Organizacijos pavadinimas:** organizacijos pavadinimas rodomas karjeros svetainės naršymo juostos viršuje.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="d8ce6-116">Pasirinkdami organizacijos pavadinimą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="d8ce6-117">**Organizacijos logotipas:** organizacijos logotipo vaizdas rodomas viršutiniame kairiajame karjeros svetainės kampe.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="d8ce6-118">Pasirinkdami organizacijos logotipo vaizdą kandidatai atidaro puslapį, kuriame išvardytos visos atviros užduotys.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="d8ce6-119">Logotipo vaizdo, kuris rodomas karjeros svetainėje, aukštis yra fiksuotas – 20 pikselių (piks.).</span><span class="sxs-lookup"><span data-stu-id="d8ce6-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="d8ce6-120">Vaizdo, kurį įtraukiate į administravimo centrą, dydis atitinkamai pritaikomas.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="d8ce6-121">Todėl, priklausomai nuo vaizdo, plotis gali keistis.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="d8ce6-122">Norėdami nustatyti toliau nurodytų elementų reikšmes, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**, pateiktą meniu **Parametrai**, tada pasirinkite skirtuką **Karjeros svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="d8ce6-123">**Ieškos mechanizmo optimizavimas** - įjungus, visų viešų darbų, paskelbtų „Attract“ karjeros svetainėje, bus galima ieškoti naudojant ieškos mechanizmus, pvz., „Bing“ ir „Google“.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="d8ce6-124">Įjungus šį parametrą ieškos rezultatai gali būti rodomi ne iš karto, priklausomai nuo naudojamo ieškos mechanizmo.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="d8ce6-125">Karjeros svetainės URL</span><span class="sxs-lookup"><span data-stu-id="d8ce6-125">Career site URLs</span></span>

<span data-ttu-id="d8ce6-126">Toliau nurodytame sąraše pateikiami dažnai naudojami karjeros svetainės URL ir nurodoma, kaip juos pasiekti.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="d8ce6-127">**Karjeros svetainės pagrindinio puslapio URL** – norėdami peržiūrėti karjeros svetainės pagrindinio puslapio URL, prisijunkite prie „Attract“ kaip administratorius, pasirinkite parinktį **Administravimo centras**, pateiktą meniu **Parametrai**, tada pasirinkite skirtuką **Karjeros svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="d8ce6-128">**Atskiro darbo skelbimo prašymo teikimo URL** – kai [registruojate išorinę užduotį](Creating-jobs-Attract.md#postings) pirmą kartą, galite kopijuoti saitą **Teikti prašymą** iš „Attract“ programos.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="d8ce6-129">Šio saito URL bus pateiktas tokiu formatu: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="d8ce6-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="d8ce6-130">**Atskiro darbo skelbimo URL** – darbo skelbimo URL yra antrinė prašymo teikimo URL eilutės eilutė.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="d8ce6-131">Ją sudaro visa informacija iki darbo numerio.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="d8ce6-132">Todėl prieš tai pateikto prašymo teikimo URL darbo skelbimo URL yra [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="d8ce6-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="d8ce6-133">Autentifikavimo parinktys</span><span class="sxs-lookup"><span data-stu-id="d8ce6-133">Authentication options</span></span>

<span data-ttu-id="d8ce6-134">Kandidatai gali naudoti toliau nurodytas prisijungimo prie „Attract“ karjeros svetainės parinktis.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="d8ce6-135">Asmeninė paskyra</span><span class="sxs-lookup"><span data-stu-id="d8ce6-135">Personal account:</span></span>

    -   <span data-ttu-id="d8ce6-136">„LinkedIn“</span><span class="sxs-lookup"><span data-stu-id="d8ce6-136">LinkedIn</span></span>

    -   <span data-ttu-id="d8ce6-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="d8ce6-137">Microsoft</span></span>

    -   <span data-ttu-id="d8ce6-138">Google</span><span class="sxs-lookup"><span data-stu-id="d8ce6-138">Google</span></span>

    -   <span data-ttu-id="d8ce6-139">„Facebook“</span><span class="sxs-lookup"><span data-stu-id="d8ce6-139">Facebook</span></span>

-   <span data-ttu-id="d8ce6-140">Darbo arba mokyklos paskyra</span><span class="sxs-lookup"><span data-stu-id="d8ce6-140">Work or school account:</span></span>

    -   <span data-ttu-id="d8ce6-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="d8ce6-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="d8ce6-142">„Azure AD“ prisijungimo funkcija skirta tik vidiniams kandidatams.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="d8ce6-143">Todėl ją gali naudoti tik vidiniai kandidatai, kurie naudoja savo įmonės „Azure AD“ kredencialus.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="d8ce6-144">Pavyzdžiui, kandidatas, kuris šiuo metu yra „Contoso, Ltd“ darbuotojas, nori kreiptis dėl darbo nesusijusioje įmonėje, „Alpine Ski House“.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="d8ce6-145">Tokiu atveju prisijungimas bus nesėkmingas, jei darbuotojas bandys naudoti savo „Azure AD“ kredencialus, priklausančius „Contoso, Ltd“.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="d8ce6-146">Profilio kūrimas ir tvarkymas</span><span class="sxs-lookup"><span data-stu-id="d8ce6-146">Create and maintain a profile</span></span>

<span data-ttu-id="d8ce6-147">Prisijungę prie karjeros svetainės, kandidatai gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Mano profilis**, norėdami kurti ir tvarkyti savo profilį.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="d8ce6-148">Profilis apima asmeninę informaciją, informaciją apie darbo patirtį, išsilavinimą, dokumentus, saitus ir informaciją apie įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="d8ce6-149">Sukūręs profilį kandidatas gali jį naudoti norėdamas kreiptis dėl dominančio darbo.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="d8ce6-150">Be to, naudodama profilius „Attract“ sistema kandidatams gali rekomenduoti tinkamus darbus.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="d8ce6-151">Jei kandidatas naudoja el. pašto ID, kad prisijungtų naudodamas vieną iš pirmiau pateiktų autentifikavimo teikėjų, to el. pašto ID bus nustatytas į kontakto el. pašto ID, susietą su profiliu.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="d8ce6-152">Tačiau pastarąjį galima keisti bet kuriuo metu ir jis yra visiškai nepriklausomas nuo pirmojo.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="d8ce6-153">Visuose el. laiškuose „Attract“ visada naudos kontakto el. pašto ID, kad susietų su jūsų profiliu.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="d8ce6-154">Tinkamo darbo paieška</span><span class="sxs-lookup"><span data-stu-id="d8ce6-154">Find the right job</span></span>

<span data-ttu-id="d8ce6-155">Darbų sąrašo puslapyje kandidatai gali ieškoti konkretaus darbo įvesdami ieškos terminus.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="d8ce6-156">Ieškos funkcija ieško paieškos terminų pareigų pavadinimuose ir užduočių aprašymuose bei rodo atitinkamas užduotis kaip rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="d8ce6-157">Kandidatai gali bet kuriuo metu filtruoti rezultatus pagal užduoties vietą arba užduoties funkciją.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="d8ce6-158">Kandidatai taip pat gali peržiūrėti rekomenduojamų užduočių rinkinį karjeros svetainėje.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="d8ce6-159">Užduotys rekomenduojamos kandidatams pagal kandidato ankstesnius prašymus, profilį ir CV.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="d8ce6-160">Užduočių rekomendacijos rodomos tik jei karjeros svetainėje užregistruota ne mažiau kaip 10 užduočių ir jei kandidatas yra užpildęs savo profilį.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="d8ce6-161">Kreipimasis dėl darbo</span><span class="sxs-lookup"><span data-stu-id="d8ce6-161">Apply for jobs</span></span>

<span data-ttu-id="d8ce6-162">Radę tinkamą darbą kandidatai gali teikti prašymą naudodami puslapio **Darbo informacija** mygtuką **Teikti prašymą**.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="d8ce6-163">Tuo metu kandidatai gali sukurti naują profilį arba peržiūrėti esamo profilio informaciją.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="d8ce6-164">Kandidatų taip pat gali nusiųsti CV, jei reikia, ir tada pateikti prašymą įdarbinti.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="d8ce6-165">Prašymo būsenos tikrinimas</span><span class="sxs-lookup"><span data-stu-id="d8ce6-165">Check application status</span></span>

<span data-ttu-id="d8ce6-166">Kai kandidatai pateikia prašymą dėl vieno arba kelių darbų, jie gali pasirinkti puslapio viršuje esančios naršymo juostos parinktį **Programos**, kad peržiūrėtų savo atidarytus ir uždarytus prašymus.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="d8ce6-167">Kai kandidatas atidaro vieną iš savo prašymų, jis mato dabartinį etapą ir visus veiksmų laukiančius elementus, kuriuos jie turi užpildyti.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="d8ce6-168">Pavyzdžiui, jei kandidatas turi nurodyti galimas asmeninio pokalbio datas, puslapyje rodomos galimos parinktys.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="d8ce6-169">Vidiniai darbai</span><span class="sxs-lookup"><span data-stu-id="d8ce6-169">Internal jobs</span></span>

<span data-ttu-id="d8ce6-170">Šiuo metu darbai, kurie pažymėti kaip vidiniai ir užregistruoti „Attract“ karjeros svetainėje, karjeros svetainėje nerodomi.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="d8ce6-171">Jie yra pasiekiami tik naudojant tiesioginį saito **Teikti prašymą** URL, kurį galima nukopijuoti iš „Attract“ programos.</span><span class="sxs-lookup"><span data-stu-id="d8ce6-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
