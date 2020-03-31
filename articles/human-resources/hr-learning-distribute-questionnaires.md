---
title: Klausimynų platinimas ir planavimas
description: Šiame straipsnyje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5372841c841e82d116381d7ce8fe48af8ddfb036
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009925"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="630b3-103">Klausimynų platinimas ir planavimas</span><span class="sxs-lookup"><span data-stu-id="630b3-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="630b3-104">Šiame straipsnyje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys.</span><span class="sxs-lookup"><span data-stu-id="630b3-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="630b3-105">Platinti klausimyną galima keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="630b3-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="630b3-106">Klausimyną pažymėkite kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="630b3-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="630b3-107">Tada klausimynas prieinamas visiems darbuotojams, nebent nustatyta klausimyno grupė, prie jo ribojanti prieigą.</span><span class="sxs-lookup"><span data-stu-id="630b3-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="630b3-108">Priskirkite klausimyno grupės teises.</span><span class="sxs-lookup"><span data-stu-id="630b3-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="630b3-109">Tada klausimynas prieinamas visiems pasirinktos grupės nariams.</span><span class="sxs-lookup"><span data-stu-id="630b3-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="630b3-110">Kurkite suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="630b3-110">Create planned answer sessions.</span></span> <span data-ttu-id="630b3-111">Tada klausimynas pasiekiamas tik tam tikram asmeniui.</span><span class="sxs-lookup"><span data-stu-id="630b3-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="630b3-112">Sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="630b3-112">Create a schedule.</span></span> <span data-ttu-id="630b3-113">Tada klausimynas gali būti prieinamas keliems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="630b3-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="630b3-114">Klausimyno pažymėjimas kaip aktyvaus</span><span class="sxs-lookup"><span data-stu-id="630b3-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="630b3-115">Puslapio **Klausimynai** lauką **Aktyvus** nustačius į **Taip**, klausimyną gali pildyti visi darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="630b3-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="630b3-116">Respondentai klausimyną gali pildyti kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="630b3-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="630b3-117">Ši funkcija yra naudinga, jei norite atsiliepimus rinkti visus metus.</span><span class="sxs-lookup"><span data-stu-id="630b3-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="630b3-118">Pavyzdžiui, galite sukurti klausimyną, kurį darbuotojai naudotų teikti atsiliepimams apie valgyklos pietų paslaugą.</span><span class="sxs-lookup"><span data-stu-id="630b3-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="630b3-119">Klausimynų grupės</span><span class="sxs-lookup"><span data-stu-id="630b3-119">Questionnaire groups</span></span>

<span data-ttu-id="630b3-120">Galite nustatyti klausimyno grupes ir tada įtraukti respondentus, kuriems klausimynas turėtų būti išplatintas.</span><span class="sxs-lookup"><span data-stu-id="630b3-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="630b3-121">Kurti klausimyno grupes galite tolesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="630b3-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="630b3-122">**Klausimyno grupės** – pasirinktą klausimyną gali pildyti tik klausimyno grupės asmenys.</span><span class="sxs-lookup"><span data-stu-id="630b3-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="630b3-123">Pavyzdžiui, jūsų tikslinė auditorija yra rangovai, todėl klausimyno grupę sukuriate konkrečiai tiems respondentams.</span><span class="sxs-lookup"><span data-stu-id="630b3-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="630b3-124">**Klausimyno grupės nariai** – į šias klausimyno grupes galite pridėti žmonių.</span><span class="sxs-lookup"><span data-stu-id="630b3-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="630b3-125">Norėdami klausimynui priskirti klausimyno grupę, puslapyje **Klausimynai** spustelėkite **Naudotojų teisės**.</span><span class="sxs-lookup"><span data-stu-id="630b3-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="630b3-126">Klausimyną įrašius kaip aktyvų, jį gali pildyti klausimyno grupės nariai.</span><span class="sxs-lookup"><span data-stu-id="630b3-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="630b3-127">Ši funkcija naudinga, norint klausimyną išbandyti su pasirinkta žmonių grupe ir tada jį naudoti su didesne grupe, arba norint klausimyną taikyti labai konkrečiai auditorijai.</span><span class="sxs-lookup"><span data-stu-id="630b3-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="630b3-128">Klausimyno suplanuoti atsakymų seansai</span><span class="sxs-lookup"><span data-stu-id="630b3-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="630b3-129">Suplanuoti atsakymų seansai yra klausimynai, kuriuos sukūrėte ir kuriems pasirinkote respondentus.</span><span class="sxs-lookup"><span data-stu-id="630b3-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="630b3-130">Prieš nustatydami suplanuotus atsakymų seansus, turite sukurti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="630b3-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="630b3-131">Puslapyje **Suplanuotas atsakymų seansas** galite kurti suplanuotą atsakymų seansą kiekvienam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="630b3-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="630b3-132">Puslapyje pateiktame sąraše rodomi visi suplanuoti klausimynai.</span><span class="sxs-lookup"><span data-stu-id="630b3-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="630b3-133">Suplanuoti atsakymų seansai taip pat naudojami **Klausimyno grafikų** puslapyje, kuriame planuoti klausimynus galite keliems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="630b3-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="630b3-134">Darbuotojai</span><span class="sxs-lookup"><span data-stu-id="630b3-134">Employees</span></span>
-   <span data-ttu-id="630b3-135">Kurso dalyviai</span><span class="sxs-lookup"><span data-stu-id="630b3-135">Course participants</span></span>
-   <span data-ttu-id="630b3-136">Organizacijos vienetai</span><span class="sxs-lookup"><span data-stu-id="630b3-136">Organizational units</span></span>

<span data-ttu-id="630b3-137">Kiekvienas asmuo atsakyti į klausimyną gali tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="630b3-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="630b3-138">Klausimyno planavimas</span><span class="sxs-lookup"><span data-stu-id="630b3-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="630b3-139">Neprivaloma: klausimyną planuoti galite keliems respondentams.</span><span class="sxs-lookup"><span data-stu-id="630b3-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="630b3-140">Planavimo tipai</span><span class="sxs-lookup"><span data-stu-id="630b3-140">Planning types</span></span>

<span data-ttu-id="630b3-141">Jei suplanuotus atsakymų seansus norite planuoti keliems respondentams, reikalingi planavimo tipai.</span><span class="sxs-lookup"><span data-stu-id="630b3-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="630b3-142">Planavimo tipai naudojami klasifikuoti klausimyno grafikams.</span><span class="sxs-lookup"><span data-stu-id="630b3-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="630b3-143">Pavyzdžiui, planuoti klausimynus galite tolesniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="630b3-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="630b3-144">Įvertinimas</span><span class="sxs-lookup"><span data-stu-id="630b3-144">Evaluation</span></span>
-   <span data-ttu-id="630b3-145">Apklausa</span><span class="sxs-lookup"><span data-stu-id="630b3-145">Survey</span></span>
-   <span data-ttu-id="630b3-146">Bandymai</span><span class="sxs-lookup"><span data-stu-id="630b3-146">Testing</span></span>

<span data-ttu-id="630b3-147">Nurodyti klausimyno grafiko planavimo tipus galite **Klausimyno grafikų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="630b3-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="630b3-148">Klausimyno nuorodų tipai</span><span class="sxs-lookup"><span data-stu-id="630b3-148">Reference types for questionnaire</span></span>

<span data-ttu-id="630b3-149">Nuorodų tipus galite naudoti norėdami įvesti kriterijus respondentams, kuriuos galbūt pasirinksite planuodami klausimyną.</span><span class="sxs-lookup"><span data-stu-id="630b3-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="630b3-150">Norėdami nustatyti klausimyno nuorodų tipus, naudokite **Nuorodų tipų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="630b3-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="630b3-151">Kiekvienas nuorodos tipas atitinka lentelę programoje „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="630b3-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="630b3-152">Kurdami klausimyno grafikus, galite nurodyti atskirus lentelės įrašus arba įrašų, su kuriais klausimynas bus susietas, intervalą.</span><span class="sxs-lookup"><span data-stu-id="630b3-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="630b3-153">Pvz., jei pasirenkate Kursų lentelę, galite nuspręsti, kuriam konkrečiam kursui klausimynas bus skirtas.</span><span class="sxs-lookup"><span data-stu-id="630b3-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="630b3-154">Kai nustatote Kursų lentelės nuorodą, **Kursų** puslapyje tampa prieinami kai kurie laukai ir mygtukai.</span><span class="sxs-lookup"><span data-stu-id="630b3-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="630b3-155">Klausimynų grafikai</span><span class="sxs-lookup"><span data-stu-id="630b3-155">Questionnaire schedules</span></span>

<span data-ttu-id="630b3-156">Klausimyno grafikus galite naudoti norėdami pagal nuorodos tipą naudotojų grupei generuoti kelis suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="630b3-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="630b3-157">Puslapyje **Klausimyno grafikai** sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="630b3-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="630b3-158">Pasirinkite planavimo tipą grafikui kategorizuoti ir taip pat pasirinkite nuorodos tipą, kurį reikėtų naudoti sistemai teikiant užklausas apie konkrečius naudotojus.</span><span class="sxs-lookup"><span data-stu-id="630b3-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="630b3-159">Pvz., jei nuorodos tipą nustatote į lentelė Kursai, **Nuorodos** lauke galite pasirinkti konkretų kursą.</span><span class="sxs-lookup"><span data-stu-id="630b3-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="630b3-160">Norėdami pasirinkti klausimyną ir kitus kriterijus, spustelėkite **Sąrankos informacija**.</span><span class="sxs-lookup"><span data-stu-id="630b3-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="630b3-161">Pavyzdžiui, jei klausimynas yra dėstytojo vertinimas, kaip kriterijų nurodykite dėstytojo vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="630b3-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="630b3-162">Jums baigus įvesti sąrankos informaciją, sistema sugeneruoja suplanuotus atsakymų seansus, skirtus naudotojams, įtrauktiems į užklausą.</span><span class="sxs-lookup"><span data-stu-id="630b3-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="630b3-163">Norėdami peržiūrėti grafiko atsakymų seansus, spustelėkite **Suplanuoti atsakymų seansai**.</span><span class="sxs-lookup"><span data-stu-id="630b3-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="630b3-164">Tada galite rankiniu būdu kurti papildomų suplanuotų atsakymų seansų arba naikinti neatsakytus suplanuotus atsakymų seansus.</span><span class="sxs-lookup"><span data-stu-id="630b3-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="630b3-165">Norėdami, kad klausimynas būtų pasiekiamas susijusių suplanuotų atsakymų seansų naudotojams, spustelėkite **Funkcijos** &gt; **Pradėti**.</span><span class="sxs-lookup"><span data-stu-id="630b3-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="630b3-166">Norėdami peržiūrėti užpildytus klausimyno atsakymus, spustelėkite **Atsakymai**.</span><span class="sxs-lookup"><span data-stu-id="630b3-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="630b3-167">Neprivaloma: klausimyno grafikų nuostatas, suplanuotus atsakymų seansus ir atsakymus galite kopijuoti į naują klausimyno grafiką.</span><span class="sxs-lookup"><span data-stu-id="630b3-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="630b3-168">Respondentų informavimas apie jiems prieinamus klausimynus</span><span class="sxs-lookup"><span data-stu-id="630b3-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="630b3-169">Kai platinate klausimyną, turite informuoti respondentus, kad jiems prieinami klausimynai.</span><span class="sxs-lookup"><span data-stu-id="630b3-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="630b3-170">Respondentų informavimas apie suplanuotą atsakymų seansą</span><span class="sxs-lookup"><span data-stu-id="630b3-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="630b3-171">Jei naudojate suplanuotą atsakymų seansą, asmenį turite informuoti tiesiogiai, pvz., telefonu ar elektroniniu paštu.</span><span class="sxs-lookup"><span data-stu-id="630b3-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="630b3-172">Respondentų informavimas apie planavimą</span><span class="sxs-lookup"><span data-stu-id="630b3-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="630b3-173">Naudodami puslapį **Klausimyno grafikai**, paruoškite ir nusiųskite el. laišką visiems respondentams, kurie priskirti klausimynui.</span><span class="sxs-lookup"><span data-stu-id="630b3-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="630b3-174">El. laiško tekstą įveskite skirtuke **Darbuotojų savitarnos el. paštas**. Kai grafikas pradėtas, spustelėkite **Funkcijos** &gt; **Siųsti el. laišką**, kad generuotumėte ir visiems respondentams nusiųstumėte el. laišką.</span><span class="sxs-lookup"><span data-stu-id="630b3-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="630b3-175">Tada respondentai gali prisijungti prie svetainės ir pildyti klausimyną.</span><span class="sxs-lookup"><span data-stu-id="630b3-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="630b3-176">Kad galėtumėte naudoti el. pašto funkcijas, puslapyje **El. pašto parametrai** jūsų IT administratorius turi įvesti el. pašto nuostatas.</span><span class="sxs-lookup"><span data-stu-id="630b3-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="630b3-177">Suplanuoto klausimyno baigimas</span><span class="sxs-lookup"><span data-stu-id="630b3-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="630b3-178">Galite pabaigti suplanuotą klausimyną, kai visi respondentai užbaigė jiems priskirtus klausimų seansus.</span><span class="sxs-lookup"><span data-stu-id="630b3-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="630b3-179">Kai suplanuotas klausimynas baigtas, jo nuostatų į naują grafiką kopijuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="630b3-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="630b3-180">Jei vienas ar keli respondentai klausimyno neužpildė, bet jūs vis tiek norite užbaigti planavimą, pirmiausia puslapyje **Planuojamas atsakymų seansas** turite iš sąrašo panaikinti tuos respondentus.</span><span class="sxs-lookup"><span data-stu-id="630b3-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="630b3-181">Tada galite baigti grafiką.</span><span class="sxs-lookup"><span data-stu-id="630b3-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="630b3-182">Klausimynų pildymas</span><span class="sxs-lookup"><span data-stu-id="630b3-182">Completing questionnaires</span></span>

<span data-ttu-id="630b3-183">Jums sukūrus ir išplatinus klausimyną, jį gali pildyti pasirinkti respondentai.</span><span class="sxs-lookup"><span data-stu-id="630b3-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="630b3-184">Galite užpildyti klausimynus, kuriuos galite pasiekti iš dviejų vietų:</span><span class="sxs-lookup"><span data-stu-id="630b3-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="630b3-185">Naršymo srityje spustelėkite **Klausimynai** &gt; **Platinti** &gt; **Pildyti klausimyną**.</span><span class="sxs-lookup"><span data-stu-id="630b3-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="630b3-186">Darbuotojų savitarnoje spustelėkite **Pildytini klausimynai**.</span><span class="sxs-lookup"><span data-stu-id="630b3-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="630b3-187">Klausimynus galima padaryti prieinamus konkretiems naudotojams ar naudotojų grupėms arba visiems tinklo naudotojams.</span><span class="sxs-lookup"><span data-stu-id="630b3-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

