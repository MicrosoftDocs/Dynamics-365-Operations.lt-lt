---
title: Įdarbinti darbo kandidatai
description: Ši tema rodo, kaip įdarbinti kandidatus „Dynamics 365 Human Resources“.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478289"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="a979a-103">Įdarbinti darbo kandidatai</span><span class="sxs-lookup"><span data-stu-id="a979a-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a979a-104">„Dynamics 365 Human Resources“ jums padeda valdyti įdarbinimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="a979a-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="a979a-105">Ji taip pat padeda jums be požymių perkelti darbo užklausas darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="a979a-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="a979a-106">Jei jūsų organizacija naudoja atskirą įdarbinimo paraišką, jūsų įdarbinimo procesas gali apimti šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="a979a-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="a979a-107">Įveskite savo įdarbinimo užklausą žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="a979a-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="a979a-108">Gaukite kandidato nuorodas žmogiškuosiuose ištekliuose iš įdarbinimo parašikos.</span><span class="sxs-lookup"><span data-stu-id="a979a-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="a979a-109">Užbaikite kandaidato patvirtinimo procesą žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="a979a-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="a979a-110">Jei nenaudojate atskiros įdarbinimo parašikos, galite taip pat rankiniu būdu valdyti kandidatus žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="a979a-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="a979a-111">Jei esate administratorius ar kūrėjas ir norite integruoti „Human Resources“ su trečiosios šalies įdarbinimo programa, žr. [Konfigūruoti „Dataverse“ integravimą](hr-admin-integration-common-data-service.md) ir [Konfigūruoti „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="a979a-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="a979a-112">Galite taip pat surasti įdarbinimo integravimo programas [„AppSource“](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="a979a-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="a979a-113">Pabandykite peržiūros funkciją integravimui su „LinkedIn Talent Hub“, žr. [integruoti su „LinkedIn Talent Hub“](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="a979a-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="a979a-114">Įjungti įdarbinimo užklausas</span><span class="sxs-lookup"><span data-stu-id="a979a-114">Enable recruiting requests</span></span>

<span data-ttu-id="a979a-115">Jei norite pateikti įdarbinimo užklausas „Human Resources“, pirmiausia turite įjungti funkcijas **Žmogiškųjų išteklių bendrintuose parametruose**.</span><span class="sxs-lookup"><span data-stu-id="a979a-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="a979a-116">Darbo erdvėje **Personalo valdymas** rinkitės **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="a979a-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="a979a-117">Skyriuje **Nustatymai**, Rinkitės **žmogiškųjų išteklių bendrinti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a979a-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="a979a-118">Skirtuke **Įdarbinimas** skyriuje **ĮDARBINIMAS**, nustatykite **Įjungti įdarbinimo užklausas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a979a-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="a979a-119">Įtrauktei įdarbinimo užklausos vietą</span><span class="sxs-lookup"><span data-stu-id="a979a-119">Add a recruiting request location</span></span>

<span data-ttu-id="a979a-120">Jei jūsų organizacija turi kelias vietas, galite įtraukti jas taip, kad besikreipiantys galėtų pasirinkti vietą, kruioje naujas įdarbinimas veiks.</span><span class="sxs-lookup"><span data-stu-id="a979a-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="a979a-121">Vieta bus įtraukta į darbo skelbimą.</span><span class="sxs-lookup"><span data-stu-id="a979a-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="a979a-122">Paieškos juostoje įveskite **įdarbinimo užklausos vieta**.</span><span class="sxs-lookup"><span data-stu-id="a979a-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="a979a-123">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a979a-123">Select **New**.</span></span>

3. <span data-ttu-id="a979a-124">Laukelyje **Įdarbinimo užklausos vieta** įveskite vietos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a979a-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Įtrauktei įdarbinimo užklausos vietą](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="a979a-126">**Aprašas** laukelyje įveskite vietos aprašą.</span><span class="sxs-lookup"><span data-stu-id="a979a-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="a979a-127">Skyriuje **Vietą**, rinkitės **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="a979a-128">Jei iššoka **Naujas adresas** įveskite adresą vietai.</span><span class="sxs-lookup"><span data-stu-id="a979a-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Įvesti adresą](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="a979a-130">Skyriuje **Kontaktinė informacija**, įveskite informaciją vietos kontaktui.</span><span class="sxs-lookup"><span data-stu-id="a979a-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="a979a-131">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="a979a-132">Įtrauktei įdarbinimo užklausą</span><span class="sxs-lookup"><span data-stu-id="a979a-132">Add a recruiting request</span></span>

<span data-ttu-id="a979a-133">Vadovai gali pateikti įdarbinimo užklausas žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="a979a-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="a979a-134">Jei naudojate atskirą įdarbinimo užklausą, šių žingsnių užbaigimas nusiųs įdarbinimo užklausą ir pradės įdarbinimo procesą toje paraiškoje.</span><span class="sxs-lookup"><span data-stu-id="a979a-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="a979a-135">Kitu atveju, užbaikite šią procedūrą, kad pradėtumėte darbo eigą jūsų vidiniam įdarbinimo procesui.</span><span class="sxs-lookup"><span data-stu-id="a979a-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="a979a-136">Rinkitės **Darbuotojo savitarna**.</span><span class="sxs-lookup"><span data-stu-id="a979a-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="a979a-137">Rinkitės **Mano komanda** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="a979a-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="a979a-138">pasirinkite **Prašyti įdarbinti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-138">Select  **Request to recruit**.</span></span>

   ![Pradėti įdarbinimo užklausą](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="a979a-140">Užbaikite **Aprašas**, **Darbas** ir **Apskaičiuota pradžios data** laukelius.</span><span class="sxs-lookup"><span data-stu-id="a979a-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Užbaikite įdarbinimo užklausą](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="a979a-142">Pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-142">Select **Continue**.</span></span> <span data-ttu-id="a979a-143">Įdarbinimo užklausa rodoma jūsų vietai.</span><span class="sxs-lookup"><span data-stu-id="a979a-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="a979a-144">Skyriuje **Bendri**, pasirinkite įdarbintoją iš **Įdarbintojo** iškrentančio meniu ir pasirinkite vietą iš **Įdarbinimo užklausos vietos** iškrentančio meniu.</span><span class="sxs-lookup"><span data-stu-id="a979a-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="a979a-145">Skyriuje **Darbas**, pakeiskite visą būtiną informaciją ir rinkitės **Sukurti išsamią informaciją darbui**.</span><span class="sxs-lookup"><span data-stu-id="a979a-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Kuri išsamią informaciją iš užduoties](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="a979a-147">Likusi įdarbinimo prašymo dalis bus užpildyta nustatąja informacijas darbui, kurį įvedėte.</span><span class="sxs-lookup"><span data-stu-id="a979a-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="a979a-148">Skyriuje **Išorinis aprašas**, įveskite išorėje matomo darbo aprašą.</span><span class="sxs-lookup"><span data-stu-id="a979a-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="a979a-149">Skyriuje **Pareigos**, rinkitės **Įtraukti** ir tada pasirinkite darbą šiam įdarbinimo prašymui.</span><span class="sxs-lookup"><span data-stu-id="a979a-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Įtraukite pareigas](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="a979a-151">Skyriuje **Įgūdžiai**, pasirinkite **Įtraukti** ir tada rinkitės įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="a979a-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="a979a-152">Skyriuje **Išsilavinimo reikalavimai**, Rinkitės **Įtraukiti** ir tada rinkitės vertes iš **Išsilavinimas** ir **Išsilavinimo lygio** iškrentančių meniu.</span><span class="sxs-lookup"><span data-stu-id="a979a-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Įtraukti išsilavinimo reikalavimus](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="a979a-154">Skyriuje **Komentaras**, įtraukite komentarus, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="a979a-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="a979a-155">Skyriuje **Užmokestis**, pasirinkite iš iškrentančio meniu **Lygį** ir tad akeiskite **Apatinis slenkstis**, **Patikros taškas** ir **Viršutinis slenkstis** kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="a979a-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="a979a-156">Kai jūsų jūsų įdarbinimo užklausa yra užbaigta ir esate pasirengęs pradėti įdarbinimo procesą, pasirinkite **Įjungti** meniu juostoje.</span><span class="sxs-lookup"><span data-stu-id="a979a-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Įjungti įdarbinimo užklausą](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="a979a-158">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="a979a-159">Peržiūrėti ir redaguoti jūsų įdarbinimo užklausas</span><span class="sxs-lookup"><span data-stu-id="a979a-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="a979a-160">Jei esate vadovas ir norite peržiūrėti savo turimas užklausas:</span><span class="sxs-lookup"><span data-stu-id="a979a-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="a979a-161">Rinkitės **Darbuotojo savitarna**.</span><span class="sxs-lookup"><span data-stu-id="a979a-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="a979a-162">Rinkitės **Mano komanda** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="a979a-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="a979a-163">Skyriuje **Mano komandos informacija**, rinkitės skirtuką **Įdarbinimo užklausos**.</span><span class="sxs-lookup"><span data-stu-id="a979a-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Pasirinkite įdarbinimo užklausų skirtuką](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="a979a-165">Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="a979a-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="a979a-166">Jei esate žmogiškųjų išteklių profesionalas ir norite peržiūrėti visas įdarbinimo užklausas:</span><span class="sxs-lookup"><span data-stu-id="a979a-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="a979a-167">Rinkitės **Personalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="a979a-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="a979a-168">Pasirinkite **įdarbinimo užklausos**.</span><span class="sxs-lookup"><span data-stu-id="a979a-168">Select **Recruiting requests**.</span></span>

   ![Peržiūrėti įdarbinimo užklausas personalo valdyme](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="a979a-170">Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="a979a-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="a979a-171">Įtraukti ar redaguoti kandidato profilį</span><span class="sxs-lookup"><span data-stu-id="a979a-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="a979a-172">Jei jūsų organizacija integravo su kita programa siekiant valdyti įdarbinimo užklausas, įdarbinimo užklausos persiunčiamos tai programai.</span><span class="sxs-lookup"><span data-stu-id="a979a-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="a979a-173">Įdarbinimo programa tada siunčia kandidato informaciją atgal žmogiškiesiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="a979a-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="a979a-174">Kitu atveju, galite sekti savo turimus vidaus įdarbinimo procesus ir įvesti kandidato informaciją rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="a979a-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="a979a-175">Rinkitės **Personalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="a979a-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="a979a-176">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="a979a-176">Select **Links**.</span></span>

3. <span data-ttu-id="a979a-177">Skyriuje **Įdarbinimas**, rinkitės **Kandidatai**.</span><span class="sxs-lookup"><span data-stu-id="a979a-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Peržiūrėti kandidatus](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="a979a-179">Norėdami įtraukti kandidatą, rinkitės **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a979a-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="a979a-180">Norėdami redaguoti esamą kandidatą, rinkitės jį iš sąrašo ir tada rinkitės **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="a979a-181">Rodomas kandidato profilis.</span><span class="sxs-lookup"><span data-stu-id="a979a-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="a979a-182">Skyriuje **Kandidato suvestinė**, įveskite ar redaguokite kandidato informaciją, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="a979a-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="a979a-183">Skyriuje **Įdarbinimo užklausa**, rinkitės įdarbinimo užklausą siekiant susieti su kandidatu.</span><span class="sxs-lookup"><span data-stu-id="a979a-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="a979a-184">Tuomet užbaikite **Apskaičiuota pradžios data**, **Įdarbinimo vadovas**, **Pareigos** ir **Aprašymo laukeliai** kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="a979a-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Susiekite su įdarbinimo užklausa](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="a979a-186">Užbaikite visą informaciją tolesnėse srityse, kurias norite įtraukti į kandidato įrašą:</span><span class="sxs-lookup"><span data-stu-id="a979a-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="a979a-187">**Komentarai**</span><span class="sxs-lookup"><span data-stu-id="a979a-187">**Comments**</span></span>
   - <span data-ttu-id="a979a-188">**Profesinė patirtis**</span><span class="sxs-lookup"><span data-stu-id="a979a-188">**Professional experience**</span></span>
   - <span data-ttu-id="a979a-189">**Kontaktinė informacija**</span><span class="sxs-lookup"><span data-stu-id="a979a-189">**Contact information**</span></span>
   - <span data-ttu-id="a979a-190">**Išsilavinimas**</span><span class="sxs-lookup"><span data-stu-id="a979a-190">**Education**</span></span>
   - <span data-ttu-id="a979a-191">**Įgūdžiai**</span><span class="sxs-lookup"><span data-stu-id="a979a-191">**Skills**</span></span>
   - <span data-ttu-id="a979a-192">**Sertifikatai**</span><span class="sxs-lookup"><span data-stu-id="a979a-192">**Certificates**</span></span>
   - <span data-ttu-id="a979a-193">**Atrankos**</span><span class="sxs-lookup"><span data-stu-id="a979a-193">**Screenings**</span></span>

8. <span data-ttu-id="a979a-194">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="a979a-195">Samdyti kandidatą</span><span class="sxs-lookup"><span data-stu-id="a979a-195">Hire a candidate</span></span>

<span data-ttu-id="a979a-196">Kai esate pasirengę samdyti kandidatą, atlikite šią procedūrą siekiant perkelti kandidatą į darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="a979a-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="a979a-197">Kandidato formoje rinkitės **Samdyti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-197">On the candidate form, select **Hire**.</span></span>

   ![Samdyti kandidatą](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="a979a-199">Formoje **Samdyti naują darbuotoją** skyriuje **Išsami informacija**, užbaikite visus laukelius.</span><span class="sxs-lookup"><span data-stu-id="a979a-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Įveskite naujo įdarbinto asmens išsamią informaciją](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="a979a-201">Skyriuje **Pareigų išsami informacija**, patikrinkite ir keiskite informaciją, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="a979a-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="a979a-202">Skyriuje **Įtraukti tikrinimo sąrašai**, pasirinkite atitinkamus įtrauktus tikrinimo sąrašus šiam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="a979a-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="a979a-203">Rinkitės **Tęsti** norėdami sukurti darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="a979a-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="a979a-204">Priklausomai nuo jūsų organizacijos darbo eigų, kandidato įrašas gali praeiti pro papildomus patvirtinimo žingsnius prieš tai, kai taps darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="a979a-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="a979a-205">Sprendimas nesamdyti kandidato</span><span class="sxs-lookup"><span data-stu-id="a979a-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="a979a-206">Jei nusprendžiate nesamdyti kandidato, laikykitės šios procedūros siekiant pašalinti jį iš vertinimo proceso.</span><span class="sxs-lookup"><span data-stu-id="a979a-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="a979a-207">Kandidato formoje rinkitės **Nesamdyti**.</span><span class="sxs-lookup"><span data-stu-id="a979a-207">On the candidate form, select **Do not hire**.</span></span>

   ![Nesamdyti kandidato](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="a979a-209">Rinkitės **Priežasties kodą** ir įtraukite visus komentarus.</span><span class="sxs-lookup"><span data-stu-id="a979a-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="a979a-210">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a979a-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="a979a-211">Atmesti kandidatą</span><span class="sxs-lookup"><span data-stu-id="a979a-211">Dismiss a candidate</span></span>

<span data-ttu-id="a979a-212">Jei reikia, galite atmesti kandidatą po jo pasamdymo.</span><span class="sxs-lookup"><span data-stu-id="a979a-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="a979a-213">Pavyzdžiui, kandidatas gali atsisakyti pasiūlymo arba nepasirodyti pirmąją dieną.</span><span class="sxs-lookup"><span data-stu-id="a979a-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="a979a-214">Kandidato formoje rinkitės **Atmesti kandidatą**.</span><span class="sxs-lookup"><span data-stu-id="a979a-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Atmesti kandidatą](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="a979a-216">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a979a-216">See also</span></span>

[<span data-ttu-id="a979a-217">Konfigūruokite „Dataverse“ virtualias lenteles</span><span class="sxs-lookup"><span data-stu-id="a979a-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a979a-218">Darbo jėgos organizavimas</span><span class="sxs-lookup"><span data-stu-id="a979a-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="a979a-219">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a979a-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
