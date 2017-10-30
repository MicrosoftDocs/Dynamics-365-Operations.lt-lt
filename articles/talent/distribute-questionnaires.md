---
title: "Platinti ir pildyti klausimyną"
description: "Šioje temoje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: f7f1ea11fe2165218d62d4756ae226ff4de5df1b
ms.contentlocale: lt-lt
ms.lasthandoff: 10/30/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="00b8d-103">Platinti ir pildyti klausimyną</span><span class="sxs-lookup"><span data-stu-id="00b8d-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="00b8d-104">Šioje temoje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys.</span><span class="sxs-lookup"><span data-stu-id="00b8d-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="00b8d-105">Platinti klausimyną galima keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="00b8d-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="00b8d-106">Klausimyną pažymėkite kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="00b8d-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="00b8d-107">Tada klausimynas prieinamas visiems darbuotojams, nebent nustatyta klausimyno grupė, prie jo ribojanti prieigą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="00b8d-108">Priskirkite klausimyno grupės teises.</span><span class="sxs-lookup"><span data-stu-id="00b8d-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="00b8d-109">Tada klausimynas prieinamas visiems pasirinktos grupės nariams.</span><span class="sxs-lookup"><span data-stu-id="00b8d-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="00b8d-110">Kurkite suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-110">Create planned answer sessions.</span></span> <span data-ttu-id="00b8d-111">Tada klausimynas pasiekiamas tik tam tikram asmeniui.</span><span class="sxs-lookup"><span data-stu-id="00b8d-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="00b8d-112">Sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="00b8d-112">Create a schedule.</span></span> <span data-ttu-id="00b8d-113">Tada klausimynas gali būti prieinamas keliems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="00b8d-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="00b8d-114">Klausimyno pažymėjimas kaip aktyvaus</span><span class="sxs-lookup"><span data-stu-id="00b8d-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="00b8d-115">Puslapio **Klausimynai** lauką **Aktyvus** nustačius į **Taip**, klausimyną gali pildyti visi darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="00b8d-116">Respondentai klausimyną gali pildyti kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="00b8d-117">Ši funkcija yra naudinga, jei norite atsiliepimus rinkti visus metus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="00b8d-118">Pavyzdžiui, galite sukurti klausimyną, kurį darbuotojai naudotų teikti atsiliepimams apie valgyklos pietų paslaugą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="00b8d-119">Klausimynų grupės</span><span class="sxs-lookup"><span data-stu-id="00b8d-119">Questionnaire groups</span></span>
<span data-ttu-id="00b8d-120">Galite nustatyti klausimyno grupes ir tada įtraukti respondentus, kuriems klausimynas turėtų būti išplatintas.</span><span class="sxs-lookup"><span data-stu-id="00b8d-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="00b8d-121">Kurti klausimyno grupes galite tolesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="00b8d-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="00b8d-122">**Klausimyno grupės** – pasirinktą klausimyną gali pildyti tik klausimyno grupės asmenys.</span><span class="sxs-lookup"><span data-stu-id="00b8d-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="00b8d-123">Pavyzdžiui, jūsų tikslinė auditorija yra rangovai, todėl klausimyno grupę sukuriate konkrečiai tiems respondentams.</span><span class="sxs-lookup"><span data-stu-id="00b8d-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="00b8d-124">**Klausimyno grupės nariai** – į šias klausimyno grupes galite pridėti žmonių.</span><span class="sxs-lookup"><span data-stu-id="00b8d-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="00b8d-125">Norėdami klausimynui priskirti klausimyno grupę, puslapyje **Klausimynai** spustelėkite **Naudotojų teisės**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="00b8d-126">Klausimyną įrašius kaip aktyvų, jį gali pildyti klausimyno grupės nariai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="00b8d-127">Ši funkcija naudinga, norint klausimyną išbandyti su pasirinkta žmonių grupe ir tada jį naudoti su didesne grupe, arba norint klausimyną taikyti labai konkrečiai auditorijai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="00b8d-128">Klausimyno suplanuoti atsakymų seansai</span><span class="sxs-lookup"><span data-stu-id="00b8d-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="00b8d-129">Suplanuoti atsakymų seansai yra klausimynai, kuriuos sukūrėte ir kuriems pasirinkote respondentus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="00b8d-130">**Pastaba.** Prieš nustatydami suplanuotus atsakymų seansus, turite sukurti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="00b8d-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="00b8d-131">Puslapyje **Suplanuotas atsakymų seansas** galite kurti suplanuotą atsakymų seansą kiekvienam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="00b8d-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="00b8d-132">Puslapyje pateiktame sąraše rodomi visi suplanuoti klausimynai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="00b8d-133">Suplanuoti atsakymų seansai taip pat naudojami **Klausimyno grafikų** puslapyje, kuriame planuoti klausimynus galite keliems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="00b8d-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="00b8d-134">Darbuotojai</span><span class="sxs-lookup"><span data-stu-id="00b8d-134">Employees</span></span>
-   <span data-ttu-id="00b8d-135">Kurso dalyviai</span><span class="sxs-lookup"><span data-stu-id="00b8d-135">Course participants</span></span>
-   <span data-ttu-id="00b8d-136">Organizacijos vienetai</span><span class="sxs-lookup"><span data-stu-id="00b8d-136">Organizational units</span></span>

<span data-ttu-id="00b8d-137">Kiekvienas asmuo atsakyti į klausimyną gali tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="00b8d-138">Klausimyno planavimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="00b8d-139">Neprivaloma: klausimyną planuoti galite keliems respondentams.</span><span class="sxs-lookup"><span data-stu-id="00b8d-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="00b8d-140">Planavimo tipai</span><span class="sxs-lookup"><span data-stu-id="00b8d-140">Planning types</span></span>

<span data-ttu-id="00b8d-141">Jei suplanuotus atsakymų seansus norite planuoti keliems respondentams, reikalingi planavimo tipai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="00b8d-142">Planavimo tipai naudojami klasifikuoti klausimyno grafikams.</span><span class="sxs-lookup"><span data-stu-id="00b8d-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="00b8d-143">Pavyzdžiui, planuoti klausimynus galite tolesniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="00b8d-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="00b8d-144">Įvertinimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-144">Evaluation</span></span>
-   <span data-ttu-id="00b8d-145">Apklausa</span><span class="sxs-lookup"><span data-stu-id="00b8d-145">Survey</span></span>
-   <span data-ttu-id="00b8d-146">Bandymai</span><span class="sxs-lookup"><span data-stu-id="00b8d-146">Testing</span></span>

<span data-ttu-id="00b8d-147">Nurodyti klausimyno grafiko planavimo tipus galite **Klausimyno grafikų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="00b8d-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="00b8d-148">Klausimyno nuorodų tipai</span><span class="sxs-lookup"><span data-stu-id="00b8d-148">Reference types for questionnaire</span></span>

<span data-ttu-id="00b8d-149">Nuorodų tipus galite naudoti norėdami įvesti kriterijus respondentams, kuriuos galbūt pasirinksite planuodami klausimyną.</span><span class="sxs-lookup"><span data-stu-id="00b8d-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="00b8d-150">Norėdami nustatyti klausimyno nuorodų tipus, naudokite **Nuorodų tipų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b8d-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="00b8d-151">Kiekvienas nuorodos tipas atitinka lentelę programoje „Microsoft Dynamics 365 for Finance and Operations‟.</span><span class="sxs-lookup"><span data-stu-id="00b8d-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="00b8d-152">Kurdami klausimyno grafikus, galite nurodyti atskirus lentelės įrašus arba įrašų, su kuriais klausimynas bus susietas, intervalą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="00b8d-153">Pvz., jei pasirenkate Kursų lentelę, galite nuspręsti, kuriam konkrečiam kursui klausimynas bus skirtas.</span><span class="sxs-lookup"><span data-stu-id="00b8d-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="00b8d-154">Kai nustatote Kursų lentelės nuorodą, **Kursų** puslapyje tampa prieinami kai kurie laukai ir mygtukai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="00b8d-155">Klausimynų grafikai</span><span class="sxs-lookup"><span data-stu-id="00b8d-155">Questionnaire schedules</span></span>

<span data-ttu-id="00b8d-156">Klausimyno grafikus galite naudoti norėdami pagal nuorodos tipą naudotojų grupei generuoti kelis suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="00b8d-157">Puslapyje **Klausimyno grafikai** sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="00b8d-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="00b8d-158">Pasirinkite planavimo tipą grafikui kategorizuoti ir taip pat pasirinkite nuorodos tipą, kurį reikėtų naudoti sistemai teikiant užklausas apie konkrečius naudotojus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="00b8d-159">Pvz., jei nuorodos tipą nustatote į lentelė Kursai, **Nuorodos** lauke galite pasirinkti konkretų kursą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="00b8d-160">Norėdami pasirinkti klausimyną ir kitus kriterijus, spustelėkite **Sąrankos informacija**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="00b8d-161">Pavyzdžiui, jei klausimynas yra dėstytojo vertinimas, kaip kriterijų nurodykite dėstytojo vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="00b8d-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="00b8d-162">Jums baigus įvesti sąrankos informaciją, sistema sugeneruoja suplanuotus atsakymų seansus, skirtus naudotojams, įtrauktiems į užklausą.</span><span class="sxs-lookup"><span data-stu-id="00b8d-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="00b8d-163">Norėdami peržiūrėti grafiko atsakymų seansus, spustelėkite **Suplanuoti atsakymų seansai**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="00b8d-164">Tada galite rankiniu būdu kurti papildomų suplanuotų atsakymų seansų arba naikinti neatsakytus suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="00b8d-165">Norėdami, kad klausimynas būtų pasiekiamas susijusių suplanuotų atsakymų seansų naudotojams, spustelėkite **Funkcijos** &gt; **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="00b8d-166">Norėdami peržiūrėti užpildytus klausimyno atsakymus, spustelėkite **Atsakymai**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="00b8d-167">Neprivaloma: klausimyno grafikų nuostatas, suplanuotus atsakymų seansus ir atsakymus galite kopijuoti į naują klausimyno grafiką.</span><span class="sxs-lookup"><span data-stu-id="00b8d-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="00b8d-168">Respondentų informavimas apie jiems prieinamus klausimynus</span><span class="sxs-lookup"><span data-stu-id="00b8d-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="00b8d-169">Kai platinate klausimyną, turite informuoti respondentus, kad jiems prieinami klausimynai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="00b8d-170">Respondentų informavimas apie suplanuotą atsakymų seansą</span><span class="sxs-lookup"><span data-stu-id="00b8d-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="00b8d-171">Jei naudojate suplanuotą atsakymų seansą, asmenį turite informuoti tiesiogiai, pvz., telefonu ar elektroniniu paštu.</span><span class="sxs-lookup"><span data-stu-id="00b8d-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="00b8d-172">Respondentų informavimas apie planavimą</span><span class="sxs-lookup"><span data-stu-id="00b8d-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="00b8d-173">Naudodami puslapį **Klausimyno grafikai**, paruoškite ir nusiųskite el. laišką visiems respondentams, kurie priskirti klausimynui.</span><span class="sxs-lookup"><span data-stu-id="00b8d-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="00b8d-174">El. laiško tekstą įveskite skirtuke **Darbuotojų savitarnos el. paštas**. Kai grafikas pradėtas, spustelėkite **Funkcijos** &gt; **Siųsti el. laišką**, kad generuotumėte ir visiems respondentams nusiųstumėte el. laišką.</span><span class="sxs-lookup"><span data-stu-id="00b8d-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="00b8d-175">Tada respondentai gali prisijungti prie svetainės ir pildyti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="00b8d-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="00b8d-176">**Pastaba** Kad galėtumėte naudoti el. pašto funkcijas, **El. pašto parametrų** puslapyje jūsų IT administratorius turi įvesti el. pašto nuostatas.</span><span class="sxs-lookup"><span data-stu-id="00b8d-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="00b8d-177">Suplanuoto klausimyno baigimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="00b8d-178">Galite pabaigti suplanuotą klausimyną, kai visi respondentai užbaigė jiems priskirtus klausimų seansus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="00b8d-179">Kai suplanuotas klausimynas baigtas, jo nuostatų į naują grafiką kopijuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="00b8d-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="00b8d-180">**Pastaba** Jei vienas ar keli respondentai klausimyno neužpildė, bet jūs vis tiek norite užbaigti planavimą, pirmiausia **Suplanuoto atsakymų seanso** puslapyje turite iš sąrašo panaikinti tuos respondentus.</span><span class="sxs-lookup"><span data-stu-id="00b8d-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="00b8d-181">Tada galite baigti grafiką.</span><span class="sxs-lookup"><span data-stu-id="00b8d-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="00b8d-182">Klausimynų pildymas</span><span class="sxs-lookup"><span data-stu-id="00b8d-182">Completing questionnaires</span></span>
<span data-ttu-id="00b8d-183">Jums sukūrus ir išplatinus klausimyną, jį gali pildyti pasirinkti respondentai.</span><span class="sxs-lookup"><span data-stu-id="00b8d-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="00b8d-184">Galite užpildyti klausimynus, kuriuos galite pasiekti iš dviejų vietų:</span><span class="sxs-lookup"><span data-stu-id="00b8d-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="00b8d-185">Naršymo srityje spustelėkite **Klausimynai** &gt; **Platinti** &gt; **Pildyti klausimyną**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="00b8d-186">Darbuotojų savitarnoje spustelėkite **Pildytini klausimynai**.</span><span class="sxs-lookup"><span data-stu-id="00b8d-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="00b8d-187">Klausimynus galima padaryti prieinamus konkretiems naudotojams ar naudotojų grupėms arba visiems tinklo naudotojams.</span><span class="sxs-lookup"><span data-stu-id="00b8d-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="00b8d-188">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="00b8d-188">See also</span></span>
--------

[<span data-ttu-id="00b8d-189">Klausimynų kūrimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="00b8d-190">Klausimynų naudojimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="00b8d-191">Klausimyno rezultatų peržiūra ir vertinimas</span><span class="sxs-lookup"><span data-stu-id="00b8d-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



