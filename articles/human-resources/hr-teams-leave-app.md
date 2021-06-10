---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097264"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="08c97-103">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="08c97-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="08c97-104">„Microsoft Teams“ veikianti programa „Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="08c97-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="08c97-105">Galite sąveikauti su robotu, kad prašytumėte informacijos ir pradėtumėte atostogų užklausą.</span><span class="sxs-lookup"><span data-stu-id="08c97-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="08c97-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="08c97-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="08c97-107">Galite taip pat nusiųsti asmenų informacija apie jūsų ateinantį nebuvimo laiką komandose ir pokalbius ne personalo programoje.</span><span class="sxs-lookup"><span data-stu-id="08c97-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="08c97-108">Programos diegimas</span><span class="sxs-lookup"><span data-stu-id="08c97-108">Install the app</span></span>

<span data-ttu-id="08c97-109">Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="08c97-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="08c97-110">„Microsoft Teams” pereikite į programų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="08c97-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="08c97-111">Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="08c97-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="08c97-112">Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="08c97-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="08c97-113">Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="08c97-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="08c97-114">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="08c97-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="08c97-115">Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="08c97-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="08c97-116">Programėlė dabar palaiko sistemos administratoriaus saugos vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="08c97-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="08c97-117">Roboto naudojimas</span><span class="sxs-lookup"><span data-stu-id="08c97-117">Use the bot</span></span>

<span data-ttu-id="08c97-118">Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.</span><span class="sxs-lookup"><span data-stu-id="08c97-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="08c97-119">Pirmą kartą bendraujant su robotu, gali reikėti prisijungti.</span><span class="sxs-lookup"><span data-stu-id="08c97-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="08c97-120">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="08c97-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="08c97-121">Roboto galite prašyti toliau pateiktų dalykų:</span><span class="sxs-lookup"><span data-stu-id="08c97-121">You can ask the bot to:</span></span>

- <span data-ttu-id="08c97-122">Peržiūrėti savo dabartinius atostogų balansus.</span><span class="sxs-lookup"><span data-stu-id="08c97-122">View your current leave balances.</span></span> <span data-ttu-id="08c97-123">Pavyzdžiui, išsiųskite pranešimą „Peržiūrėti atostogų balansus.”</span><span class="sxs-lookup"><span data-stu-id="08c97-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="08c97-124">Pateikti atostogų prašymą už jus.</span><span class="sxs-lookup"><span data-stu-id="08c97-124">Start a leave request for you.</span></span> <span data-ttu-id="08c97-125">Pavyzdžiui, išsiųskite pranešimą „Pasiimti ne darbo laiko” arba „Norėčiau pasiimti atostogas kitą ketvirtadienį ir penktadienį”, kad konkrečiau nurodytumėte prašomų atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="08c97-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Atostogų užklausos paleidimas komandos pokalbyje](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="08c97-127">Pokalbių robotas jums užpildys prašymą išeiti atostogų.</span><span class="sxs-lookup"><span data-stu-id="08c97-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="08c97-128">Pasirinkite **Prašyti išleisti iš darbo** ir redaguokite savo prašymo duomenis.</span><span class="sxs-lookup"><span data-stu-id="08c97-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="08c97-129">Jei norite pateikti kelių tos pačios datos atostogų tipų atostogų užklausas, pasirinkite **Skaidyti dieną** parinktį iš meniu **Daugiau parinkčių**.</span><span class="sxs-lookup"><span data-stu-id="08c97-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="08c97-130">Jei išeisite pusdieniui, kai atostogų užklausos vienetas pateiktas dienomis, galite nurodyti, ar norite prašyti laisvo laiko pirmoje, ar antroje dienos pusėje, pasirinkdami **Pusės dienos apibrėžimas** parinktį iš meniu **Daugiau parinkčių**.</span><span class="sxs-lookup"><span data-stu-id="08c97-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Pusės dienos apibrėžimai](./media/HalfDayDefinitions.png)

- <span data-ttu-id="08c97-132">Kai baigsite redaguoti savo prašymo išeiti atostogų duomenis, pasirinkite **Pateikti** ir pateikite jį patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="08c97-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Prašymo išeiti atostogų pateikimas](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="08c97-134">Atostogų valdymas programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="08c97-134">Manage your leave in Teams</span></span>

<span data-ttu-id="08c97-135">Skirtuke **Ne darbo laikas** galite peržiūrėti:</span><span class="sxs-lookup"><span data-stu-id="08c97-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="08c97-136">Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją</span><span class="sxs-lookup"><span data-stu-id="08c97-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="08c97-137">Būsimų atostogų prašymus</span><span class="sxs-lookup"><span data-stu-id="08c97-137">Upcoming leave requests</span></span>

- <span data-ttu-id="08c97-138">Prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="08c97-138">Time-off requests</span></span>

- <span data-ttu-id="08c97-139">Atostogų prašymų juodraščius</span><span class="sxs-lookup"><span data-stu-id="08c97-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="08c97-140">Naujo prašymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="08c97-140">Create a new request</span></span>

1. <span data-ttu-id="08c97-141">Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.</span><span class="sxs-lookup"><span data-stu-id="08c97-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="08c97-142">Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="08c97-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas](./media/TimeOffHours.png)

3. <span data-ttu-id="08c97-144">Jei reikia, įveskite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="08c97-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="08c97-145">Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.</span><span class="sxs-lookup"><span data-stu-id="08c97-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="08c97-146">Pasirinkite **Skaidyti dieną** parinktį iš meniu **Daugiau parinkčių**, jei norite pateikti kelių tos pačios datos atostogų tipų atostogų užklausas.</span><span class="sxs-lookup"><span data-stu-id="08c97-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="08c97-147">Pasirinkite **Pusės dienos apibrėžimas** parinktį, kad nurodytumėte, ar norite prašyti ne darbo laiko pirmojoje, ar antrojoje dienos pusėje.</span><span class="sxs-lookup"><span data-stu-id="08c97-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="08c97-148">Ši parinktis yra galima, kai atostogų užklausos vienetas pateikiamas dienomis, o prašoma suma yra 0,5 dienos.</span><span class="sxs-lookup"><span data-stu-id="08c97-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="08c97-149">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte ją patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="08c97-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="08c97-150">Jūs taip pat galite įvesti **Įrašyti kaip juodraštį**, kad grįžtumėte prie jos vėliau.</span><span class="sxs-lookup"><span data-stu-id="08c97-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="08c97-151">Prašymų juodraščių valdymas</span><span class="sxs-lookup"><span data-stu-id="08c97-151">Manage draft requests</span></span>

1. <span data-ttu-id="08c97-152">Pasirinkite skirtuką **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="08c97-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="08c97-153">Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="08c97-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="08c97-154">Atlikite reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="08c97-154">Make any necessary changes.</span></span> <span data-ttu-id="08c97-155">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="08c97-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="08c97-156">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="08c97-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="08c97-157">Atsakyti į „Teams” pranešimus</span><span class="sxs-lookup"><span data-stu-id="08c97-157">Respond to Teams notifications</span></span>

<span data-ttu-id="08c97-158">Kai jūs arba darbuotojas, kurio tvirtintojas esate jūs, pateikiate atostogų užklausą, gausite pranešimą „Human Resources“ programoje „Teams“.</span><span class="sxs-lookup"><span data-stu-id="08c97-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="08c97-159">Galite pasirinkti pranešimą, norėdami jį peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="08c97-159">You can select the notification to view it.</span></span> <span data-ttu-id="08c97-160">Pranešimai taip pat rodomi **pokalbių** srityje.</span><span class="sxs-lookup"><span data-stu-id="08c97-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="08c97-161">Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="08c97-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="08c97-162">Taip pat galite pateikti pasirinktinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="08c97-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="08c97-163">Siųsti būsimo ne darbo laiko informaciją savo bendradarbiams</span><span class="sxs-lookup"><span data-stu-id="08c97-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="08c97-164">Įdiegę „Human Resources” programėlę, pritaikytą „Teams”, galite lengvai siųsti informaciją apie savo būsimą ne darbo laiką savo bendradarbiams skiltyje „Komandos” arba „Pokalbiai”.</span><span class="sxs-lookup"><span data-stu-id="08c97-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="08c97-165">„Komandos” arba „Pokalbiai” skiltyje, esančiose programėlėje „Teams”, pasirinkite „Human Resources” mygtuką, esantį po pokalbio langu.</span><span class="sxs-lookup"><span data-stu-id="08c97-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![„Human Resources” mygtukas, esantis po pokalbio langu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="08c97-167">Pasirinkite atostogų užklausą, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="08c97-167">Select the leave request you want to share.</span></span> <span data-ttu-id="08c97-168">Jei norite bendrinti juodraštinę atostogų užklausą, pirmiausia pasirinkite **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="08c97-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="08c97-169">Jūsų atostogų užklausa bus rodoma pokalbiuose.</span><span class="sxs-lookup"><span data-stu-id="08c97-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="08c97-170">Jei bendrinote juodraštinę užklausą, ji bus rodoma kaip juodraštis.</span><span class="sxs-lookup"><span data-stu-id="08c97-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="08c97-171">Peržiūrėti komandos atostogų kalendorių</span><span class="sxs-lookup"><span data-stu-id="08c97-171">View your team's leave calendar</span></span>

<span data-ttu-id="08c97-172">Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="08c97-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="08c97-173">„Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="08c97-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="08c97-174">Pasirinkite **Komandos kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="08c97-174">Select **Team calendar**.</span></span> <span data-ttu-id="08c97-175">Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="08c97-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="08c97-176">Jei nematote komandos kalendoriaus, paprašykite savo administratoriaus, kad jį įjungtų</span><span class="sxs-lookup"><span data-stu-id="08c97-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="08c97-177">Daugiau informacijos žr. skyriuje [Diegimas ir sąranka](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="08c97-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="08c97-178">Palaikomos kalbos</span><span class="sxs-lookup"><span data-stu-id="08c97-178">Supported languages</span></span>

<span data-ttu-id="08c97-179">Programa „Dynamics 365 Human Resources“ komandose palaiko šias kalbas:</span><span class="sxs-lookup"><span data-stu-id="08c97-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="08c97-180">Vietos ID</span><span class="sxs-lookup"><span data-stu-id="08c97-180">Locale ID</span></span> | <span data-ttu-id="08c97-181">Kalba</span><span class="sxs-lookup"><span data-stu-id="08c97-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="08c97-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="08c97-182">de-DE</span></span> | <span data-ttu-id="08c97-183">Vokiečių (Vokietija)</span><span class="sxs-lookup"><span data-stu-id="08c97-183">German (Germany)</span></span> |
| <span data-ttu-id="08c97-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="08c97-184">es-ES</span></span> | <span data-ttu-id="08c97-185">Ispanų (Ispanija)</span><span class="sxs-lookup"><span data-stu-id="08c97-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="08c97-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="08c97-186">es-MX</span></span> | <span data-ttu-id="08c97-187">Ispanų (Meksika)</span><span class="sxs-lookup"><span data-stu-id="08c97-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="08c97-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="08c97-188">fr-CA</span></span> | <span data-ttu-id="08c97-189">Prancūzų (Kanada)</span><span class="sxs-lookup"><span data-stu-id="08c97-189">French (Canada)</span></span> |
| <span data-ttu-id="08c97-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="08c97-190">fr-FR</span></span> | <span data-ttu-id="08c97-191">Prancūzų (Prancūzija)</span><span class="sxs-lookup"><span data-stu-id="08c97-191">French (France)</span></span> |
| <span data-ttu-id="08c97-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="08c97-192">it-IT</span></span> | <span data-ttu-id="08c97-193">Italų (Italija)</span><span class="sxs-lookup"><span data-stu-id="08c97-193">Italian (Italy)</span></span> |
| <span data-ttu-id="08c97-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="08c97-194">nl-NL</span></span> | <span data-ttu-id="08c97-195">Olandų (Nyderlandai)</span><span class="sxs-lookup"><span data-stu-id="08c97-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="08c97-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="08c97-196">pt-BR</span></span> | <span data-ttu-id="08c97-197">Portugalų (Brazilija)</span><span class="sxs-lookup"><span data-stu-id="08c97-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="08c97-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="08c97-198">tr-TR</span></span> | <span data-ttu-id="08c97-199">Turkų (Turkija)</span><span class="sxs-lookup"><span data-stu-id="08c97-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="08c97-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="08c97-200">zh-CN</span></span> | <span data-ttu-id="08c97-201">Kinų (supaprastintoji)</span><span class="sxs-lookup"><span data-stu-id="08c97-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="08c97-202">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="08c97-202">Troubleshooting</span></span>

<span data-ttu-id="08c97-203">Jei kyla problemų prisijungiant arba naudojant „Dynamics 365 Human Resources“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="08c97-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="08c97-204">Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="08c97-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="08c97-205">Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="08c97-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="08c97-206">Nepavyksta prisijungti prie „Teams“ programos „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="08c97-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="08c97-207">Jei negalite prisijungti prie programos, gali būti, kad paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, nėra susieta su darbuotojo įrašu „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="08c97-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="08c97-208">Kreipkitės į sistemos administratorių, kad įsitikintumėte, kad jūsų darbuotojo įrašas yra tinkamai susietas.</span><span class="sxs-lookup"><span data-stu-id="08c97-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="08c97-209">Vertimai rodomi neteisingai</span><span class="sxs-lookup"><span data-stu-id="08c97-209">Translations don't display correctly</span></span>

<span data-ttu-id="08c97-210">Jei vertimai nerodomi taip, kaip turėtų, patikrinkite, ar kalba, kurią pasirinkote komandose, sutampa su kalba, kurią pasirinkote personalo skiltyje **Naudotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="08c97-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="08c97-211">Komandose peržiūrėkite **Programos kalba**, dalyje **Nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="08c97-211">In Teams, look at **App language** in **Settings**.</span></span>

![Komandų nustatymai](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="08c97-213">Personalo dalyje pasirinkite **Nustatymai**, o tada pasirinkite **Naudotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="08c97-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="08c97-214">Patikrinkite, ar laukelis **Kalba** sutampa su komandų laukeliu **Programos kalba**.</span><span class="sxs-lookup"><span data-stu-id="08c97-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Personalo naudotojo parinktys](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="08c97-216">Jei vis dar kyla problemų dėl vertimo, praneškite mums.</span><span class="sxs-lookup"><span data-stu-id="08c97-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="08c97-217">Išsamesnės informacijos, žr. skyriuje [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="08c97-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="08c97-218">Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="08c97-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="08c97-219">Jei gaunate klaidą, kai bandote patvirtinti atostogų užklausas „Teams“ programoje, pabandykite tolesnius trikčių šalinimo žingsnius:</span><span class="sxs-lookup"><span data-stu-id="08c97-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="08c97-220">Patikrinkite, ar paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, yra ta pati, kurią naudojate prieigai prie „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="08c97-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="08c97-221">Patikrinkite, ar jus galite patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus.</span><span class="sxs-lookup"><span data-stu-id="08c97-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="08c97-222">Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="08c97-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="08c97-223">Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti</span><span class="sxs-lookup"><span data-stu-id="08c97-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="08c97-224">Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti.</span><span class="sxs-lookup"><span data-stu-id="08c97-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="08c97-225">Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="08c97-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="08c97-226">Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="08c97-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="08c97-227">Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".</span><span class="sxs-lookup"><span data-stu-id="08c97-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="08c97-228">Jei problema išlieka, patikrinkite verslo įvykių sistemos paketinės užduoties būseną kaip sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="08c97-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="08c97-229">Jei jis yra laukimo ar vykdymo etape, po kelių minučių patikrinkite atgal.</span><span class="sxs-lookup"><span data-stu-id="08c97-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="08c97-230">Jei būsena nekinta, užregistruokite palaikymo bilietą, kad mūsų komanda galėtų padėti išspręsti problemą.</span><span class="sxs-lookup"><span data-stu-id="08c97-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="08c97-231">Sužinokite prieinamumo problemas</span><span class="sxs-lookup"><span data-stu-id="08c97-231">Known accessibility issues</span></span>

<span data-ttu-id="08c97-232">Žmogiškųjų išteklių programa „Teams“ turi tolesnes prieinamumo problemas, dėl kurių dirbame siekdami sutaisyti ateities versijose.</span><span class="sxs-lookup"><span data-stu-id="08c97-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="08c97-233">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="08c97-233">Issue</span></span> | <span data-ttu-id="08c97-234">Apėjimas ir paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="08c97-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="08c97-235">Priartinimas iki 400% darbastalyje paslepia kai kuriuos mygtukų veiksmus iš rodinio.</span><span class="sxs-lookup"><span data-stu-id="08c97-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="08c97-236">Rekomenduojame naudoti didinamąjį stiklą, kol palaikysime šį priartinimo lygį.</span><span class="sxs-lookup"><span data-stu-id="08c97-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="08c97-237">Skirtuke **Nebuvimo laikas** perėmimas praneša mygtuko veiksmą skaitant antraštę iš nebuvimo tinklelio.</span><span class="sxs-lookup"><span data-stu-id="08c97-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="08c97-238">Antraštė ir elementai tinklelyje yra sugrupuoti pagal metus ir jie gali pradingti.</span><span class="sxs-lookup"><span data-stu-id="08c97-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="08c97-239">Perėmimas interpretuoja tai kaip įjungiamą prekę, bet taip nėra.</span><span class="sxs-lookup"><span data-stu-id="08c97-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="08c97-240">Skirtuke **Nebuvimas** yra papildomas paslinkimo gestas naršant į **Priežasties kodą** naujame prašyme.</span><span class="sxs-lookup"><span data-stu-id="08c97-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="08c97-241">Nėra jokio paslėpto valdiklio, kurį bando gauti paslinkimo naršymas.</span><span class="sxs-lookup"><span data-stu-id="08c97-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="08c97-242">Skirtuke **Nebuvimas** jums paslinkus, kai yra atidarytas kalendorius, baigsite ne valdiklyje, o naujos užklausos viršuje arba redaguodami užklausą.</span><span class="sxs-lookup"><span data-stu-id="08c97-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="08c97-243">Jums pasiekus **Eiti šiandien**, pagalvokite apie valdiklio pabaigą ir paslinkite atgaline kryptimi, kad grįžtumėte į viršų.</span><span class="sxs-lookup"><span data-stu-id="08c97-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="08c97-244">Skirtuke **Pokalbis** koncentravimasis nušoka atgal į viršų jums įvedant datą ir naudojant padedantį įrankį ar klaviatūros naršymą.</span><span class="sxs-lookup"><span data-stu-id="08c97-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="08c97-245">Naudokite skirtuką, kol pasieksite savo įvesties sritį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="08c97-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="08c97-246">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="08c97-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="08c97-247">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="08c97-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="08c97-248">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="08c97-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="08c97-249">Vartotojo įvestis, pavyzdžiui, „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų, pavadinimu „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="08c97-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="08c97-250">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="08c97-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="08c97-251">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra paskyra, pavadinta „Contoso”).</span><span class="sxs-lookup"><span data-stu-id="08c97-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="08c97-252">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="08c97-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="08c97-253">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="08c97-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="08c97-254">LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="08c97-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="08c97-255">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išsiųstas į LUIS tarnybą ir „Azure bot framework“.</span><span class="sxs-lookup"><span data-stu-id="08c97-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="08c97-256">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="08c97-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="08c97-257">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="08c97-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="08c97-258">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="08c97-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="08c97-259">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="08c97-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="08c97-260">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="08c97-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="08c97-261">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="08c97-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="08c97-262">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="08c97-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="08c97-263">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="08c97-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="08c97-264">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="08c97-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="08c97-265">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="08c97-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="08c97-266">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="08c97-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="08c97-267">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="08c97-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="08c97-268">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="08c97-268">See also</span></span>

[<span data-ttu-id="08c97-269">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="08c97-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="08c97-270">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="08c97-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="08c97-271">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="08c97-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
