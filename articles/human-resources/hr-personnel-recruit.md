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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669181"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="5ea57-103">Įdarbinti darbo kandidatai</span><span class="sxs-lookup"><span data-stu-id="5ea57-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5ea57-104">„Dynamics 365 Human Resources“ jums padeda valdyti įdarbinimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="5ea57-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="5ea57-105">Ji taip pat padeda jums be požymių perkelti darbo užklausas darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="5ea57-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="5ea57-106">Jei jūsų organizacija naudoja atskirą įdarbinimo paraišką, jūsų įdarbinimo procesas gali apimti šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="5ea57-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="5ea57-107">Įveskite savo įdarbinimo užklausą žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="5ea57-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="5ea57-108">Gaukite kandidato nuorodas žmogiškuosiuose ištekliuose iš įdarbinimo parašikos.</span><span class="sxs-lookup"><span data-stu-id="5ea57-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="5ea57-109">Užbaikite kandaidato patvirtinimo procesą žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="5ea57-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="5ea57-110">Jei nenaudojate atskiros įdarbinimo parašikos, galite taip pat rankiniu būdu valdyti kandidatus žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="5ea57-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="5ea57-111">Jei esate administratorius ar kūrėjas ir norite integruoti žmogiškiuosius išteklius su trečiosios šalies įdarbinimo paraiška, žr. [Konfigūruoti „Common Data Service“ integravimą](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="5ea57-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="5ea57-112">Galite taip pat surasti įdarbinimo integravimo programas [„AppSource“](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="5ea57-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="5ea57-113">Pabandykite peržiūros funkciją integravimui su „LinkedIn Talent Hub“, žr. [integruoti su „LinkedIn Talent Hub“](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="5ea57-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="5ea57-114">Įjungti įdarbinimo užklausas</span><span class="sxs-lookup"><span data-stu-id="5ea57-114">Enable recruiting requests</span></span>

<span data-ttu-id="5ea57-115">Jei norite pateikti įdarbinimo užklausas žmogiškuosiuos ištekliuose, pirma turite įjungti funkciją **Žmogiškųjų išteklių parametruose**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="5ea57-116">Darbo erdvėje **Personalo valdymas** rinkitės **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="5ea57-117">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="5ea57-118">Skirtuke **Bendri** skyriuje **ĮDARBINIMAS**, nustatykite **Įjungti įdarbinimo užklausas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Įjungti įdarbinimo užklausas](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="5ea57-120">Įtrauktei įdarbinimo užklausos vietą</span><span class="sxs-lookup"><span data-stu-id="5ea57-120">Add a recruiting request location</span></span>

<span data-ttu-id="5ea57-121">Jei jūsų organizacija turi kelias vietas, galite įtraukti jas taip, kad besikreipiantys galėtų pasirinkti vietą, kruioje naujas įdarbinimas veiks.</span><span class="sxs-lookup"><span data-stu-id="5ea57-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="5ea57-122">Vieta bus įtraukta į darbo skelbimą.</span><span class="sxs-lookup"><span data-stu-id="5ea57-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="5ea57-123">Paieškos juostoje įveskite **įdarbinimo užklausos vieta**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="5ea57-124">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-124">Select **New**.</span></span>

3. <span data-ttu-id="5ea57-125">Laukelyje **Įdarbinimo užklausos vieta** įveskite vietos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5ea57-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Įtrauktei įdarbinimo užklausos vietą](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="5ea57-127">**Aprašas** laukelyje įveskite vietos aprašą.</span><span class="sxs-lookup"><span data-stu-id="5ea57-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="5ea57-128">Skyriuje **Vietą**, rinkitės **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="5ea57-129">Jei iššoka **Naujas adresas** įveskite adresą vietai.</span><span class="sxs-lookup"><span data-stu-id="5ea57-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Įvesti adresą](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="5ea57-131">Skyriuje **Kontaktinė informacija**, įveskite informaciją vietos kontaktui.</span><span class="sxs-lookup"><span data-stu-id="5ea57-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="5ea57-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="5ea57-133">Įtrauktei įdarbinimo užklausą</span><span class="sxs-lookup"><span data-stu-id="5ea57-133">Add a recruiting request</span></span>

<span data-ttu-id="5ea57-134">Vadovai gali pateikti įdarbinimo užklausas žmogiškuosiuose ištekliuose.</span><span class="sxs-lookup"><span data-stu-id="5ea57-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="5ea57-135">Jei naudojate atskirą įdarbinimo užklausą, šių žingsnių užbaigimas nusiųs įdarbinimo užklausą ir pradės įdarbinimo procesą toje paraiškoje.</span><span class="sxs-lookup"><span data-stu-id="5ea57-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="5ea57-136">Kitu atveju, užbaikite šią procedūrą, kad pradėtumėte darbo eigą jūsų vidiniam įdarbinimo procesui.</span><span class="sxs-lookup"><span data-stu-id="5ea57-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="5ea57-137">Rinkitės **Darbuotojo savitarna**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="5ea57-138">Rinkitės **Mano komanda** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="5ea57-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="5ea57-139">pasirinkite **Prašyti įdarbinti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-139">Select  **Request to recruit**.</span></span>

   ![Pradėti įdarbinimo užklausą](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="5ea57-141">Užbaikite **Aprašas**, **Darbas** ir **Apskaičiuota pradžios data** laukelius.</span><span class="sxs-lookup"><span data-stu-id="5ea57-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Užbaikite įdarbinimo užklausą](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="5ea57-143">Pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-143">Select **Continue**.</span></span> <span data-ttu-id="5ea57-144">Įdarbinimo užklausa rodoma jūsų vietai.</span><span class="sxs-lookup"><span data-stu-id="5ea57-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="5ea57-145">Skyriuje **Bendri**, pasirinkite įdarbintoją iš **Įdarbintojo** iškrentančio meniu ir pasirinkite vietą iš **Įdarbinimo užklausos vietos** iškrentančio meniu.</span><span class="sxs-lookup"><span data-stu-id="5ea57-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="5ea57-146">Skyriuje **Darbas**, pakeiskite visą būtiną informaciją ir rinkitės **Sukurti išsamią informaciją darbui**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Kuri išsamią informaciją iš užduoties](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="5ea57-148">Likusi įdarbinimo prašymo dalis bus užpildyta nustatąja informacijas darbui, kurį įvedėte.</span><span class="sxs-lookup"><span data-stu-id="5ea57-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="5ea57-149">Skyriuje **Išorinis aprašas**, įveskite išorėje matomo darbo aprašą.</span><span class="sxs-lookup"><span data-stu-id="5ea57-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="5ea57-150">Skyriuje **Pareigos**, rinkitės **Įtraukti** ir tada pasirinkite darbą šiam įdarbinimo prašymui.</span><span class="sxs-lookup"><span data-stu-id="5ea57-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Įtraukite pareigas](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="5ea57-152">Skyriuje **Įgūdžiai**, pasirinkite **Įtraukti** ir tada rinkitės įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="5ea57-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="5ea57-153">Skyriuje **Išsilavinimo reikalavimai**, Rinkitės **Įtraukiti** ir tada rinkitės vertes iš **Išsilavinimas** ir **Išsilavinimo lygio** iškrentančių meniu.</span><span class="sxs-lookup"><span data-stu-id="5ea57-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Įtraukti išsilavinimo reikalavimus](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="5ea57-155">Skyriuje **Komentaras**, įtraukite komentarus, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="5ea57-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="5ea57-156">Skyriuje **Užmokestis**, pasirinkite iš iškrentančio meniu **Lygį** ir tad akeiskite **Apatinis slenkstis**, **Patikros taškas** ir **Viršutinis slenkstis** kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="5ea57-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="5ea57-157">Kai jūsų jūsų įdarbinimo užklausa yra užbaigta ir esate pasirengęs pradėti įdarbinimo procesą, pasirinkite **Įjungti** meniu juostoje.</span><span class="sxs-lookup"><span data-stu-id="5ea57-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Įjungti įdarbinimo užklausą](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="5ea57-159">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="5ea57-160">Peržiūrėti ir redaguoti jūsų įdarbinimo užklausas</span><span class="sxs-lookup"><span data-stu-id="5ea57-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="5ea57-161">Jei esate vadovas ir norite peržiūrėti savo turimas užklausas:</span><span class="sxs-lookup"><span data-stu-id="5ea57-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="5ea57-162">Rinkitės **Darbuotojo savitarna**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="5ea57-163">Rinkitės **Mano komanda** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="5ea57-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="5ea57-164">Skyriuje **Mano komandos informacija**, rinkitės skirtuką **Įdarbinimo užklausos**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Pasirinkite įdarbinimo užklausų skirtuką](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="5ea57-166">Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="5ea57-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="5ea57-167">Jei esate žmogiškųjų išteklių profesionalas ir norite peržiūrėti visas įdarbinimo užklausas:</span><span class="sxs-lookup"><span data-stu-id="5ea57-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="5ea57-168">Rinkitės **Personalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="5ea57-169">Pasirinkite **įdarbinimo užklausos**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-169">Select **Recruiting requests**.</span></span>

   ![Peržiūrėti įdarbinimo užklausas personalo valdyme](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="5ea57-171">Norėdami peržiūrėti ar redaguoti įdarbinimo užklausą, pasirinkite ją tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="5ea57-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="5ea57-172">Įtraukti ar redaguoti kandidato profilį</span><span class="sxs-lookup"><span data-stu-id="5ea57-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="5ea57-173">Jei jūsų organizacija integravo su kita programa siekiant valdyti įdarbinimo užklausas, įdarbinimo užklausos persiunčiamos tai programai.</span><span class="sxs-lookup"><span data-stu-id="5ea57-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="5ea57-174">Įdarbinimo programa tada siunčia kandidato informaciją atgal žmogiškiesiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="5ea57-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="5ea57-175">Kitu atveju, galite sekti savo turimus vidaus įdarbinimo procesus ir įvesti kandidato informaciją rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="5ea57-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="5ea57-176">Rinkitės **Personalo valdymas**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="5ea57-177">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-177">Select **Links**.</span></span>

3. <span data-ttu-id="5ea57-178">Skyriuje **Įdarbinimas**, rinkitės **Kandidatai**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Peržiūrėti kandidatus](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="5ea57-180">Norėdami įtraukti kandidatą, rinkitės **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="5ea57-181">Norėdami redaguoti esamą kandidatą, rinkitės jį iš sąrašo ir tada rinkitės **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="5ea57-182">Rodomas kandidato profilis.</span><span class="sxs-lookup"><span data-stu-id="5ea57-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="5ea57-183">Skyriuje **Kandidato suvestinė**, įveskite ar redaguokite kandidato informaciją, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="5ea57-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="5ea57-184">Skyriuje **Įdarbinimo užklausa**, rinkitės įdarbinimo užklausą siekiant susieti su kandidatu.</span><span class="sxs-lookup"><span data-stu-id="5ea57-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="5ea57-185">Tuomet užbaikite **Apskaičiuota pradžios data**, **Įdarbinimo vadovas**, **Pareigos** ir **Aprašymo laukeliai** kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="5ea57-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Susiekite su įdarbinimo užklausa](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="5ea57-187">Užbaikite visą informaciją tolesnėse srityse, kurias norite įtraukti į kandidato įrašą:</span><span class="sxs-lookup"><span data-stu-id="5ea57-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="5ea57-188">**Komentarai**</span><span class="sxs-lookup"><span data-stu-id="5ea57-188">**Comments**</span></span>
   - <span data-ttu-id="5ea57-189">**Profesinė patirtis**</span><span class="sxs-lookup"><span data-stu-id="5ea57-189">**Professional experience**</span></span>
   - <span data-ttu-id="5ea57-190">**Kontaktinė informacija**</span><span class="sxs-lookup"><span data-stu-id="5ea57-190">**Contact information**</span></span>
   - <span data-ttu-id="5ea57-191">**Išsilavinimas**</span><span class="sxs-lookup"><span data-stu-id="5ea57-191">**Education**</span></span>
   - <span data-ttu-id="5ea57-192">**Įgūdžiai**</span><span class="sxs-lookup"><span data-stu-id="5ea57-192">**Skills**</span></span>
   - <span data-ttu-id="5ea57-193">**Sertifikatai**</span><span class="sxs-lookup"><span data-stu-id="5ea57-193">**Certificates**</span></span>
   - <span data-ttu-id="5ea57-194">**Atrankos**</span><span class="sxs-lookup"><span data-stu-id="5ea57-194">**Screenings**</span></span>

8. <span data-ttu-id="5ea57-195">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="5ea57-196">Samdyti kandidatą</span><span class="sxs-lookup"><span data-stu-id="5ea57-196">Hire a candidate</span></span>

<span data-ttu-id="5ea57-197">Kai esate pasirengę samdyti kandidatą, atlikite šią procedūrą siekiant perkelti kandidatą į darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="5ea57-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="5ea57-198">Kandidato formoje rinkitės **Samdyti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-198">On the candidate form, select **Hire**.</span></span>

   ![Samdyti kandidatą](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="5ea57-200">Formoje **Samdyti naują darbuotoją** skyriuje **Išsami informacija**, užbaikite visus laukelius.</span><span class="sxs-lookup"><span data-stu-id="5ea57-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Įveskite naujo įdarbinto asmens išsamią informaciją](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="5ea57-202">Skyriuje **Pareigų išsami informacija**, patikrinkite ir keiskite informaciją, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="5ea57-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="5ea57-203">Skyriuje **Įtraukti tikrinimo sąrašai**, pasirinkite atitinkamus įtrauktus tikrinimo sąrašus šiam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="5ea57-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="5ea57-204">Rinkitės **Tęsti** norėdami sukurti darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="5ea57-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="5ea57-205">Priklausomai nuo jūsų organizacijos darbo eigų, kandidato įrašas gali praeiti pro papildomus patvirtinimo žingsnius prieš tai, kai taps darbuotojo įrašu.</span><span class="sxs-lookup"><span data-stu-id="5ea57-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="5ea57-206">Sprendimas nesamdyti kandidato</span><span class="sxs-lookup"><span data-stu-id="5ea57-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="5ea57-207">Jei nusprendžiate nesamdyti kandidato, laikykitės šios procedūros siekiant pašalinti jį iš vertinimo proceso.</span><span class="sxs-lookup"><span data-stu-id="5ea57-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="5ea57-208">Kandidato formoje rinkitės **Nesamdyti**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-208">On the candidate form, select **Do not hire**.</span></span>

   ![Nesamdyti kandidato](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="5ea57-210">Rinkitės **Priežasties kodą** ir įtraukite visus komentarus.</span><span class="sxs-lookup"><span data-stu-id="5ea57-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="5ea57-211">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="5ea57-212">Atmesti kandidatą</span><span class="sxs-lookup"><span data-stu-id="5ea57-212">Dismiss a candidate</span></span>

<span data-ttu-id="5ea57-213">Jei reikia, galite atmesti kandidatą po jo pasamdymo.</span><span class="sxs-lookup"><span data-stu-id="5ea57-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="5ea57-214">Pavyzdžiui, kandidatas gali atsisakyti pasiūlymo arba nepasirodyti pirmąją dieną.</span><span class="sxs-lookup"><span data-stu-id="5ea57-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="5ea57-215">Kandidato formoje rinkitės **Atmesti kandidatą**.</span><span class="sxs-lookup"><span data-stu-id="5ea57-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Atmesti kandidatą](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="5ea57-217">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="5ea57-217">See also</span></span>

[<span data-ttu-id="5ea57-218">„Common Data Service“ virtualių objektų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5ea57-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="5ea57-219">Darbo jėgos organizavimas</span><span class="sxs-lookup"><span data-stu-id="5ea57-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="5ea57-220">Užduoties komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="5ea57-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)