---
title: "Darbuotojų pasirinkimas naudojant „LinkedIn Recruiter“"
description: "Šioje temoje pateikiama informacija mašininio mokymo naudojimą norint gauti darbų ir kandidatų į darbo vietas rekomendacijas."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: lt-lt
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="7fcec-103">Darbuotojų pasirinkimas naudojant „LinkedIn Recruiter“</span><span class="sxs-lookup"><span data-stu-id="7fcec-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="7fcec-104">„LinkedIn“ yra didžiausia pasaulyje talentų duomenų bazė ir dažnai tai yra pagrindinė sistema, kurią naudodami darbdaviai ieško, bendrauja ir skiria užduotis kandidatams, kurie įdarbintojams reikalingi.</span><span class="sxs-lookup"><span data-stu-id="7fcec-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="7fcec-105">„LinkedIn Recruiter“ integravimas su „Dynamics 365 for Talent: Attract“ palengvina vartotojų samdos procesą ir sinchronizuoja duomenis abiejose sistemose.</span><span class="sxs-lookup"><span data-stu-id="7fcec-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="7fcec-106">Jums reikia išsamios įdarbinimo informacijos priedo ir „LinkedIn Recruiter“ vietų, kad galėtumėte naudoti „LinkedIn Recruiter“ integravimą su „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="7fcec-107">„LinkedIn Recruiter“ is „Attract“ nustatymas</span><span class="sxs-lookup"><span data-stu-id="7fcec-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="7fcec-108">Prieš naudodami „LinkedIn Recruiter“ galimybes, turite sukonfigūruoti sutarties lygio arba įmonės lygio prieigą su savo „Attract“ egzemplioriumi.</span><span class="sxs-lookup"><span data-stu-id="7fcec-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="7fcec-109">Norėdami atlikti konfigūravimo procesą, turite bendradarbiauti su vartotoju, kuris yra jūsų „LinkedIn Recruiter“ sutarties administratorius.</span><span class="sxs-lookup"><span data-stu-id="7fcec-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="7fcec-110">Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte „LinkedIn Recruiter“ su „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="7fcec-111">Prisijunkite prie „Attract“ kaip administratorius ir pasirinkite **Administravimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="7fcec-112">Kairiojoje srityje spustelėkite skirtuką **„LinkedIn integravimas**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="7fcec-113">[![„Attract“ administratoriaus rodinys, skirtas pradėti „LinkedIn Recruiter“ integravimą](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="7fcec-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="7fcec-114">Spustelėkite **Jungtis**, kad pradėtumėte nustatymą ir būtų teikiamos prisijungimo prie „LinkedIn“ proceso instrukcijos.</span><span class="sxs-lookup"><span data-stu-id="7fcec-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="7fcec-115">Jei turite vietų keliose „LinkedIn“ sutartyse, pasirinkite sutartį, kurią norėtumėte prijungti prie „Attract“ sistemos.</span><span class="sxs-lookup"><span data-stu-id="7fcec-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="7fcec-116">Jei turite tik vieną vietą „LinkedIn“ sutartyje, šis veiksmas nėra būtinas.</span><span class="sxs-lookup"><span data-stu-id="7fcec-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="7fcec-117">Tada „LinkedIn“ valdiklis bus įkeltas į jūsų administravimo parametrus ir bus rodomas integravimų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7fcec-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="7fcec-118">Skiltyje **„Recruiter“ sistemos prijungimas** spustelėkite **Teikti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="7fcec-119">[![„Attract“ administratoriaus rodinys, skirtas pateikti užlausą dėl „LinkedIn Recruiter“ integravimo](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7fcec-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="7fcec-120">Pateikus integravimo užklausą iš „Attract“, bus rodoma būsena **Partneris paruoštas** ir jį bus galima įjungti **„Recruiter“ administravimo parametruose**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="7fcec-121">Jei šiame puslapyje matote parinktį **Įspėti partnerį**, palaukite keletą sekundžių, spustelėkite **Įspėti partnerį**, tada atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7fcec-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="7fcec-122">Dabar turėtų būti rodoma būsena **Partneris paruoštas**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="7fcec-123">[![„Attract“ administratoriaus rodinys, skirtas nurodyti, kad „Attract“ pusės užklausos yra įvykdytos](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7fcec-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="7fcec-124">Norėdami atlikti kitą veiksmą, turite turėti administratoriaus teisę „LinkedIn Recruiter“ sutartyje.</span><span class="sxs-lookup"><span data-stu-id="7fcec-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="7fcec-125">Prisijunkite prie „LinkedIn“ naudodami administratoriaus paskyrą ir viršuje dešinėje atidarykite skiltį „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="7fcec-126">Ekrano viršuje esančiame meniu **Daugiau** spustelėkite **Administravimo parametrai**, tada spustelėkite skirtuką **ATS**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="7fcec-127">„Attract“ sistema bus nurodyta pateikiant kelias parinktis, kurias galima įjungti.</span><span class="sxs-lookup"><span data-stu-id="7fcec-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="7fcec-128">Jei norite įjungti tik 1 spustelėjimo eksportavimo parinktį, skirtą **ATS vidiniam indikatoriui** ir **ATS vidiniam profilio valdikliui**, pasirinkite **Įmonės lygio prieiga**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="7fcec-129">Jei norite įjungti visos įmonės lygio prieigos funkcijas ir „InMail“ retrospektyvos, pastabų retrospektyvos ir „InMail“ šaknelės profilio prieigą, pasirinkite **Sutarties lygio prieiga**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="7fcec-130">Įjunkite norimą prieigos lygį „LinkedIn Recruiter“ **Administravimo ATS** parametruose.</span><span class="sxs-lookup"><span data-stu-id="7fcec-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="7fcec-131">[![Įjunkite „Attract“ integravimą iš „LinkedIn Recruiter“ administratoriaus rodinio](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="7fcec-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="7fcec-132">Vėl atidarykite „Attract“ administravimo parametrus kaip „Attract“ administratorius ir pasirinkite skirtuką **„LinkedIn“ integravimas**. Dabar turėtumėte matyti įkeltą „LinkedIn“ valdiklį, nurodantį, kad pasirinkto lygio prieiga įjungta, ir rodantį būseną **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="7fcec-133">[![„LinkedIn Recruiter“ integravimas baigtas](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="7fcec-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="7fcec-134">„LinkedIn Recruiter“ galimybių naudojimas</span><span class="sxs-lookup"><span data-stu-id="7fcec-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="7fcec-135">Kai „Attract“ administratorius įjungia „LinkedIn Recruiter“ galimybes, jas gali pasiekti samdos vadovai ir įdarbintojai.</span><span class="sxs-lookup"><span data-stu-id="7fcec-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="7fcec-136">Norėdami naudoti šias galimybes, prijunkite „LinkedIn“ paskyrą skiltyje **Vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="7fcec-137">Kai administratoriaus ir vartotojo parametrai prijungiami, galima naudoti keletą galimybių.</span><span class="sxs-lookup"><span data-stu-id="7fcec-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="7fcec-138">Vidinio ATS profilio valdiklis</span><span class="sxs-lookup"><span data-stu-id="7fcec-138">In-ATS profile widget</span></span>

<span data-ttu-id="7fcec-139">Kandidato „LinkedIn“ profilį galite peržiūrėti „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="7fcec-140">„LinkedIn“ valdiklis rodys kandidato profilį, kai ATS informacija sutaps su „LinkedIn“ vartotojų informacija.</span><span class="sxs-lookup"><span data-stu-id="7fcec-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="7fcec-141">Norėdami peržiūrėti profilį, atidarykite kandidato profilį iš darbų arba talentų telkinio.</span><span class="sxs-lookup"><span data-stu-id="7fcec-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="7fcec-142">Kandidato profilyje pasirinkite skirtuką **LinkedIn** ir bus įkeltas profilio valdiklis.</span><span class="sxs-lookup"><span data-stu-id="7fcec-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="7fcec-143">Naudodami profilio valdiklį, nurodykite, ar tai teisingas atitikimas.</span><span class="sxs-lookup"><span data-stu-id="7fcec-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="7fcec-144">Jei ne, raskite tinkamą asmenį.</span><span class="sxs-lookup"><span data-stu-id="7fcec-144">If it is not, find the correct person.</span></span> <span data-ttu-id="7fcec-145">Taip pat galite įrašyti kandidatą savo „LinkedIn Recruiter“ projektuose šiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7fcec-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="7fcec-146">1 spustelėjimo eksportavimas</span><span class="sxs-lookup"><span data-stu-id="7fcec-146">1-click export</span></span> 

<span data-ttu-id="7fcec-147">Samdydami kandidatus „LinkedIn“ galite 1 spustelėjimu eksportuoti kandidatą į darbus, kurie šiuo metu atidaryti.</span><span class="sxs-lookup"><span data-stu-id="7fcec-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="7fcec-148">Atlikite tolesnius veiksmus, norėdami naudoti 1 spustelėjimo eksportavimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="7fcec-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="7fcec-149">Prieš baigdami šiuos veiksmus, įsitikinkite, kad jums priskirtas darbo samdos vadovo arba įdarbintojo vaidmuo, o darbo etapas yra **Potencialus klientas**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="7fcec-150">Kurkite darbus, priskirkite atitinkamiems vaidmenims ir aktyvinkite užduotis.</span><span class="sxs-lookup"><span data-stu-id="7fcec-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="7fcec-151">Kai užduotis yra suaktyvinta, atidarykite „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="7fcec-152">Rasti ieškomą kandidatą ir atidarykite jo profilį.</span><span class="sxs-lookup"><span data-stu-id="7fcec-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="7fcec-153">Naudodami darbo ieškos lauką kontakto kortelėje raskite darbą: naudokite pareigas arba užduoties ID, kuris buvo suaktyvintas „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="7fcec-154">Jei užduoties nerasite, spustelėkite **Keisti ATS**, kad rastumėte tinkamą „Attract“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="7fcec-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="7fcec-155">Pasirinkę darbą spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="7fcec-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="7fcec-156">Dabar kandidato duomenis nuskaito „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="7fcec-157">Atidarykite „Attract“ ir atidarykite atitinkamą darbą.</span><span class="sxs-lookup"><span data-stu-id="7fcec-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="7fcec-158">Eksportuotą kandidatą rasite etapo **Potencialus klientas** darbe.</span><span class="sxs-lookup"><span data-stu-id="7fcec-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="7fcec-159">Vidinio ATS indikatorius</span><span class="sxs-lookup"><span data-stu-id="7fcec-159">In-ATS indicator</span></span> 

<span data-ttu-id="7fcec-160">Naudodami „LinkedIn Recruiter“ galite sekti, ar kandidatas pateikė prašymą dėl kitų darbo vietų jūsų organizacijoje, pažiūrėti, kokie skirtingi jo prašymų dėl darbo etapai ir peržiūrėti atsiliepimus bei komentarus iš „Attract“ sistemoje „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="7fcec-161">Atidarykite „LinkedIn Recruiter“ ir suraskite ieškomo kandidato profilį.</span><span class="sxs-lookup"><span data-stu-id="7fcec-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="7fcec-162">Slinkite žemyn ir peržiūrėkite skiltį **Vidinis ATS**, pateiktą kandidato profilyje.</span><span class="sxs-lookup"><span data-stu-id="7fcec-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="7fcec-163">Šį valdiklį galite naudoti norėdami peržiūrėti visą informaciją apie kandidatą, kuris nurodytas „LinkedIn Recruiter“ rodinyje.</span><span class="sxs-lookup"><span data-stu-id="7fcec-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="7fcec-164">Pasirinkite skirtuką **Darbai ir būsenos** norėdami peržiūrėti sudėtinius darbus, naujausias būsenas ir tai, kaip sekasi vykdyti bet kurį iš darbų.</span><span class="sxs-lookup"><span data-stu-id="7fcec-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="7fcec-165">Pasirinkite skirtuką **Pokalbio atsiliepimas**, kad pamatytumėte atsiliepimą, kurį kalbintojai pateikė „Attract“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="7fcec-166">Pasirinkite skirtuką **Pastabos**, kad pamatytumėte „Attract“ užfiksuotas pastabas apie šį kandidatą.</span><span class="sxs-lookup"><span data-stu-id="7fcec-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="7fcec-167">„InMail“ retrospektyva</span><span class="sxs-lookup"><span data-stu-id="7fcec-167">InMail history</span></span>

<span data-ttu-id="7fcec-168">„LinkedIn InMail“ retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7fcec-169">Kai ji įjungta, galite peržiūrėti visą „InMail“ restrospektyvą, susijusią su kandidatais.</span><span class="sxs-lookup"><span data-stu-id="7fcec-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="7fcec-170">Taip pat galite peržiūrėti, kas dar iš jūsų organizacijos susirašinėjo su kandidatu naudodami „InMail“, tačiau negalite peržiūrėti jų žinučių.</span><span class="sxs-lookup"><span data-stu-id="7fcec-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="7fcec-171">Norėdami peržiūrėti „InMail“ retrospektyvą, atidarykite kandidato profilį, pasirinkite skirtuką **LinkedIn** ir slinkite į puslapio apačią, kad peržiūrėtumėte retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="7fcec-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="7fcec-172">„InMail“ retrospektyvą galite peržiūrėti tik jei kandidatas yra atsakė į jūsų užklausą ir pasirinkto su jumis bendrinti savo profilį naudodami „LinkedIn InMail“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="7fcec-173">Pranešimus iš „InMail“ sinchronizuojami su „Attract“ kas kelias valandas.</span><span class="sxs-lookup"><span data-stu-id="7fcec-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="7fcec-174">Pastabų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="7fcec-174">Notes history</span></span> 

<span data-ttu-id="7fcec-175">„LinkedIn“ pastabų retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7fcec-176">Kai ji įjungta, galite peržiūrėti pastabas, susietas su kandidatu ir užfiksuotas įvairių įdarbintojų iš jūsų organizacijos.</span><span class="sxs-lookup"><span data-stu-id="7fcec-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="7fcec-177">Norėdami peržiūrėti pastabų retrospektyvą, atidarykite kandidato profilį, pasirinkite skirtuką **LinkedIn** ir slinkite į puslapio apačią, kad peržiūrėtumėte retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="7fcec-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="7fcec-178">Visas pastabas apie kandidatą galite peržiūrėti iš „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="7fcec-179">„InMail“ šaknelės profilis</span><span class="sxs-lookup"><span data-stu-id="7fcec-179">InMail stub profile</span></span>

<span data-ttu-id="7fcec-180">„InMail“ šaknelės retrospektyva pateikiama su sutarties lygio prieiga prie „LinkedIn Recruiter“.</span><span class="sxs-lookup"><span data-stu-id="7fcec-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="7fcec-181">Jei kandidatai sutinka bendrinti savo „LinkedIn“ profilį su bet kuriuo vartotoju jūsų organizacijoje, galėsite sekti kandidatus „Attract“ bus sukurtas kiekvieno kandidato įrašas.</span><span class="sxs-lookup"><span data-stu-id="7fcec-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="7fcec-182">Norėdami peržiūrėti kandidatų sąrašą, pasirinkite **Talentų telkinius**, kad peržiūrėtumėte sistemos sukurtą „LinkedIn“ talentų telkinį.</span><span class="sxs-lookup"><span data-stu-id="7fcec-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="7fcec-183">Šiame talentų telkinyje kandidatai ir jų šaknelės profiliai pateikiami pagal „LinkedIn“ sistemą, kuriame rodomi kandidato vardas ir pavardė.</span><span class="sxs-lookup"><span data-stu-id="7fcec-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="7fcec-184">Kandidato el. pašto adreso ID bus rodomas, jei kandidatas pasirinko bendrinti savo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="7fcec-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

