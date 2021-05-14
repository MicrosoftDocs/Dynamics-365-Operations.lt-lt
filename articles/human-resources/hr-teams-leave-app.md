---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953417"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="26ffb-103">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="26ffb-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="26ffb-104">„Microsoft Teams“ veikianti programa „Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="26ffb-105">Galite sąveikauti su robotu, kad prašytumėte informacijos ir pradėtumėte atostogų užklausą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="26ffb-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="26ffb-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="26ffb-107">Galite taip pat nusiųsti asmenų informacija apie jūsų ateinantį nebuvimo laiką komandose ir pokalbius ne personalo programoje.</span><span class="sxs-lookup"><span data-stu-id="26ffb-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="26ffb-108">Programos diegimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-108">Install the app</span></span>

<span data-ttu-id="26ffb-109">Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="26ffb-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="26ffb-110">Programoje „Microsoft Teams“ pasirinkite daugtaškius.</span><span class="sxs-lookup"><span data-stu-id="26ffb-110">In Microsoft Teams, select the ellipses.</span></span>

   ![„Human Resources Teams“ atostogų programos daugtaškiai](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="26ffb-112">Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![„Human Resources Teams“ atostogų programos HR plytelė](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="26ffb-114">Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-114">Select the **Add** button to install the app.</span></span>

   ![„Human Resources Teams“ atostogų programos diegimas](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="26ffb-116">Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![„Human Resources Teams“ atostogų programos mygtukas Parametrai](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="26ffb-118">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="26ffb-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="26ffb-119">Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="26ffb-120">Programėlė dabar palaiko sistemos administratoriaus saugos vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="26ffb-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="26ffb-121">Roboto naudojimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-121">Use the bot</span></span>

<span data-ttu-id="26ffb-122">Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.</span><span class="sxs-lookup"><span data-stu-id="26ffb-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![„Human Resources Teams“ atostogų programos roboto pasveikinimo pranešimas](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="26ffb-124">Pirmą kartą bendraujant su robotu, gali reikėti prisijungti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="26ffb-125">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="26ffb-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="26ffb-126">Roboto galite prašyti toliau pateiktų dalykų.</span><span class="sxs-lookup"><span data-stu-id="26ffb-126">You can ask the bot to:</span></span>

- <span data-ttu-id="26ffb-127">Pateikti atostogų prašymą už jus.</span><span class="sxs-lookup"><span data-stu-id="26ffb-127">Start a leave request for you.</span></span>

  ![Atostogų užklausos paleidimas komandos pokalbyje](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="26ffb-129">Pokalbių robotas jums užpildys prašymą išeiti atostogų.</span><span class="sxs-lookup"><span data-stu-id="26ffb-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="26ffb-130">Pasirinkite **Prašyti išleisti iš darbo** ir redaguokite savo prašymo duomenis.</span><span class="sxs-lookup"><span data-stu-id="26ffb-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Prašymo išeiti atostogų duomenų redagavimas](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="26ffb-132">Kai baigsite redaguoti savo prašymo išeiti atostogų duomenis, pasirinkite **Pateikti** ir pateikite jį patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Prašymo išeiti atostogų pateikimas](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="26ffb-134">Atostogų valdymas programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="26ffb-134">Manage your leave in Teams</span></span>

<span data-ttu-id="26ffb-135">Skirtuke **Ne darbo laikas** galite peržiūrėti:</span><span class="sxs-lookup"><span data-stu-id="26ffb-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="26ffb-136">Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją</span><span class="sxs-lookup"><span data-stu-id="26ffb-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="26ffb-137">Būsimų atostogų prašymus</span><span class="sxs-lookup"><span data-stu-id="26ffb-137">Upcoming leave requests</span></span>

- <span data-ttu-id="26ffb-138">Prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="26ffb-138">Time-off requests</span></span>

- <span data-ttu-id="26ffb-139">Atostogų prašymų juodraščius</span><span class="sxs-lookup"><span data-stu-id="26ffb-139">Draft leave requests</span></span>

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="26ffb-141">Naujo prašymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-141">Create a new request</span></span>

1. <span data-ttu-id="26ffb-142">Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-142">To create a new leave request, select **New request**.</span></span>

   ![„Human Resources Teams“ atostogų programos naujas prašymas](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="26ffb-144">Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="26ffb-146">Jei reikia, įveskite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="26ffb-147">Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.</span><span class="sxs-lookup"><span data-stu-id="26ffb-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="26ffb-148">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="26ffb-149">Taip pat galite įvesti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="26ffb-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="26ffb-150">Prašymų juodraščių valdymas</span><span class="sxs-lookup"><span data-stu-id="26ffb-150">Manage draft requests</span></span>

1. <span data-ttu-id="26ffb-151">Pasirinkite skirtuką **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-151">Select the **Drafts** tab.</span></span>

   ![„Human Resources Teams“ atostogų programos skirtukas Juodraščiai](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="26ffb-153">Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="26ffb-154">Atlikite reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="26ffb-154">Make any necessary changes.</span></span> <span data-ttu-id="26ffb-155">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="26ffb-156">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="26ffb-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![„Human Resources Teams“ atostogų programos juodraščio redagavimas](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="26ffb-158">Atsakyti į „Teams” pranešimus</span><span class="sxs-lookup"><span data-stu-id="26ffb-158">Respond to Teams notifications</span></span>

<span data-ttu-id="26ffb-159">Kai jūs arba darbuotojas, kurio tvirtintojas esate jūs, pateikiate atostogų užklausą, gausite pranešimą „Human Resources“ programoje „Teams“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="26ffb-160">Galite pasirinkti pranešimą, norėdami jį peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-160">You can select the notification to view it.</span></span> <span data-ttu-id="26ffb-161">Pranešimai taip pat rodomi **pokalbių** srityje.</span><span class="sxs-lookup"><span data-stu-id="26ffb-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="26ffb-162">Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="26ffb-163">Taip pat galite pateikti pasirinktinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-163">You can also provide an optional message.</span></span>

![Atostogų užklausos pranešimas programoje „Human Resources Teams“](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="26ffb-165">Siųsti būsimo ne darbo laiko informaciją savo bendradarbiams</span><span class="sxs-lookup"><span data-stu-id="26ffb-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="26ffb-166">Įdiegę „Human Resources” programėlę, pritaikytą „Teams”, galite lengvai siųsti informaciją apie savo būsimą ne darbo laiką savo bendradarbiams skiltyje „Komandos” arba „Pokalbiai”.</span><span class="sxs-lookup"><span data-stu-id="26ffb-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="26ffb-167">„Komandos” arba „Pokalbiai” skiltyje, esančiose programėlėje „Teams”, pasirinkite „Human Resources” mygtuką, esantį po pokalbio langu.</span><span class="sxs-lookup"><span data-stu-id="26ffb-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![„Human Resources” mygtukas, esantis po pokalbio langu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="26ffb-169">Pasirinkite atostogų užklausą, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-169">Select the leave request you want to share.</span></span> <span data-ttu-id="26ffb-170">Jei norite bendrinti juodraštinę atostogų užklausą, pirmiausia pasirinkite **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Pasirinkite būsimą atostogų užklausą bendrinimui](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="26ffb-172">Jūsų atostogų užklausa bus rodoma pokalbiuose.</span><span class="sxs-lookup"><span data-stu-id="26ffb-172">Your leave request will display in the chat.</span></span>

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="26ffb-174">Jei bendrinote juodraštinę užklausą, ji bus rodomas kaip juodraštis:</span><span class="sxs-lookup"><span data-stu-id="26ffb-174">If you shared a draft request, it will display as a draft:</span></span>

![„Human Resources” juodraštinės atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="26ffb-176">Peržiūrėti komandos atostogų kalendorių</span><span class="sxs-lookup"><span data-stu-id="26ffb-176">View your team's leave calendar</span></span>

<span data-ttu-id="26ffb-177">Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="26ffb-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="26ffb-178">„Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="26ffb-179">Pasirinkite **Komandos kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-179">Select **Team calendar**.</span></span> <span data-ttu-id="26ffb-180">Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="26ffb-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Kalendoriaus peržiūra „Human Resources Teams“ programoje](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="26ffb-182">Jei nematote komandos kalendoriaus, paprašykite savo administratoriaus, kad jį įjungtų</span><span class="sxs-lookup"><span data-stu-id="26ffb-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="26ffb-183">Daugiau informacijos žr. skyriuje [Diegimas ir sąranka](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="26ffb-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="26ffb-184">Palaikomos kalbos</span><span class="sxs-lookup"><span data-stu-id="26ffb-184">Supported languages</span></span>

<span data-ttu-id="26ffb-185">Programa „Dynamics 365 Human Resources“ komandose palaiko šias kalbas:</span><span class="sxs-lookup"><span data-stu-id="26ffb-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="26ffb-186">Vietos ID</span><span class="sxs-lookup"><span data-stu-id="26ffb-186">Locale ID</span></span> | <span data-ttu-id="26ffb-187">Kalba</span><span class="sxs-lookup"><span data-stu-id="26ffb-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="26ffb-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="26ffb-188">de-DE</span></span> | <span data-ttu-id="26ffb-189">Vokiečių (Vokietija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-189">German (Germany)</span></span> |
| <span data-ttu-id="26ffb-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="26ffb-190">es-ES</span></span> | <span data-ttu-id="26ffb-191">Ispanų (Ispanija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="26ffb-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="26ffb-192">es-MX</span></span> | <span data-ttu-id="26ffb-193">Ispanų (Meksika)</span><span class="sxs-lookup"><span data-stu-id="26ffb-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="26ffb-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="26ffb-194">fr-CA</span></span> | <span data-ttu-id="26ffb-195">Prancūzų (Kanada)</span><span class="sxs-lookup"><span data-stu-id="26ffb-195">French (Canada)</span></span> |
| <span data-ttu-id="26ffb-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="26ffb-196">fr-FR</span></span> | <span data-ttu-id="26ffb-197">Prancūzų (Prancūzija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-197">French (France)</span></span> |
| <span data-ttu-id="26ffb-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="26ffb-198">it-IT</span></span> | <span data-ttu-id="26ffb-199">Italų (Italija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-199">Italian (Italy)</span></span> |
| <span data-ttu-id="26ffb-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="26ffb-200">nl-NL</span></span> | <span data-ttu-id="26ffb-201">Olandų (Nyderlandai)</span><span class="sxs-lookup"><span data-stu-id="26ffb-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="26ffb-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="26ffb-202">pt-BR</span></span> | <span data-ttu-id="26ffb-203">Portugalų (Brazilija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="26ffb-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="26ffb-204">tr-TR</span></span> | <span data-ttu-id="26ffb-205">Turkų (Turkija)</span><span class="sxs-lookup"><span data-stu-id="26ffb-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="26ffb-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="26ffb-206">zh-CN</span></span> | <span data-ttu-id="26ffb-207">Kinų (supaprastintoji)</span><span class="sxs-lookup"><span data-stu-id="26ffb-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="26ffb-208">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-208">Troubleshooting</span></span>

<span data-ttu-id="26ffb-209">Jei kyla problemų prisijungiant arba naudojant „Dynamics 365 Human Resources“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="26ffb-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="26ffb-210">Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="26ffb-211">Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="26ffb-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="26ffb-212">Nepavyksta prisijungti prie „Teams“ programos „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="26ffb-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="26ffb-213">Jei negalite prisijungti prie programos, gali būti, kad paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, nėra susieta su darbuotojo įrašu „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="26ffb-214">Kreipkitės į sistemos administratorių, kad įsitikintumėte, kad jūsų darbuotojo įrašas yra tinkamai susietas.</span><span class="sxs-lookup"><span data-stu-id="26ffb-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="26ffb-215">Vertimai rodomi neteisingai</span><span class="sxs-lookup"><span data-stu-id="26ffb-215">Translations don't display correctly</span></span>

<span data-ttu-id="26ffb-216">Jei vertimai nerodomi taip, kaip turėtų, patikrinkite, ar kalba, kurią pasirinkote komandose, sutampa su kalba, kurią pasirinkote personalo skiltyje **Naudotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="26ffb-217">Komandose peržiūrėkite **Programos kalba**, dalyje **Nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-217">In Teams, look at **App language** in **Settings**.</span></span>

![Komandų nustatymai](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="26ffb-219">Personalo dalyje pasirinkite **Nustatymai**, o tada pasirinkite **Naudotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="26ffb-220">Patikrinkite, ar laukelis **Kalba** sutampa su komandų laukeliu **Programos kalba**.</span><span class="sxs-lookup"><span data-stu-id="26ffb-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Personalo naudotojo parinktys](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="26ffb-222">Jei vis dar kyla problemų dėl vertimo, praneškite mums.</span><span class="sxs-lookup"><span data-stu-id="26ffb-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="26ffb-223">Išsamesnės informacijos, žr. skyriuje [Gauti pagalbą „Finance and Operations“ programoms arba „Lifecycle Services (LCS)“](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="26ffb-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="26ffb-224">Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="26ffb-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="26ffb-225">Jei gaunate klaidą, kai bandote patvirtinti atostogų užklausas „Teams“ programoje, pabandykite tolesnius trikčių šalinimo žingsnius:</span><span class="sxs-lookup"><span data-stu-id="26ffb-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="26ffb-226">Patikrinkite, ar paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, yra ta pati, kurią naudojate prieigai prie „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="26ffb-227">Patikrinkite, ar jus galite patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus.</span><span class="sxs-lookup"><span data-stu-id="26ffb-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="26ffb-228">Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="26ffb-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="26ffb-229">Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti</span><span class="sxs-lookup"><span data-stu-id="26ffb-229">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="26ffb-230">Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-230">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="26ffb-231">Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="26ffb-231">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="26ffb-232">Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-232">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="26ffb-233">Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".</span><span class="sxs-lookup"><span data-stu-id="26ffb-233">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="26ffb-234">Jei problema išlieka, patikrinkite verslo įvykių sistemos paketinės užduoties būseną kaip sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="26ffb-234">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="26ffb-235">Jei jis yra laukimo ar vykdymo etape, po kelių minučių patikrinkite atgal.</span><span class="sxs-lookup"><span data-stu-id="26ffb-235">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="26ffb-236">Jei būsena nekinta, užregistruokite palaikymo bilietą, kad mūsų komanda galėtų padėti išspręsti problemą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-236">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="26ffb-237">Sužinokite prieinamumo problemas</span><span class="sxs-lookup"><span data-stu-id="26ffb-237">Known accessibility issues</span></span>

<span data-ttu-id="26ffb-238">Žmogiškųjų išteklių programa „Teams“ turi tolesnes prieinamumo problemas, dėl kurių dirbame siekdami sutaisyti ateities versijose.</span><span class="sxs-lookup"><span data-stu-id="26ffb-238">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="26ffb-239">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-239">Issue</span></span> | <span data-ttu-id="26ffb-240">Apėjimas ir paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-240">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="26ffb-241">Priartinimas iki 400% darbastalyje paslepia kai kuriuos mygtukų veiksmus iš rodinio.</span><span class="sxs-lookup"><span data-stu-id="26ffb-241">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="26ffb-242">Rekomenduojame naudoti didinamąjį stiklą, kol palaikysime šį priartinimo lygį.</span><span class="sxs-lookup"><span data-stu-id="26ffb-242">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="26ffb-243">Skirtuke **Nebuvimo laikas** perėmimas praneša mygtuko veiksmą skaitant antraštę iš nebuvimo tinklelio.</span><span class="sxs-lookup"><span data-stu-id="26ffb-243">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="26ffb-244">Antraštė ir elementai tinklelyje yra sugrupuoti pagal metus ir jie gali pradingti.</span><span class="sxs-lookup"><span data-stu-id="26ffb-244">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="26ffb-245">Perėmimas interpretuoja tai kaip įjungiamą prekę, bet taip nėra.</span><span class="sxs-lookup"><span data-stu-id="26ffb-245">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="26ffb-246">Skirtuke **Nebuvimas** yra papildomas paslinkimo gestas naršant į **Priežasties kodą** naujame prašyme.</span><span class="sxs-lookup"><span data-stu-id="26ffb-246">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="26ffb-247">Nėra jokio paslėpto valdiklio, kurį bando gauti paslinkimo naršymas.</span><span class="sxs-lookup"><span data-stu-id="26ffb-247">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="26ffb-248">Skirtuke **Nebuvimas** jums paslinkus, kai yra atidarytas kalendorius, baigsite ne valdiklyje, o naujos užklausos viršuje arba redaguodami užklausą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-248">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="26ffb-249">Jums pasiekus **Eiti šiandien**, pagalvokite apie valdiklio pabaigą ir paslinkite atgaline kryptimi, kad grįžtumėte į viršų.</span><span class="sxs-lookup"><span data-stu-id="26ffb-249">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="26ffb-250">Skirtuke **Pokalbis** koncentravimasis nušoka atgal į viršų jums įvedant datą ir naudojant padedantį įrankį ar klaviatūros naršymą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-250">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="26ffb-251">Naudokite skirtuką, kol pasieksite savo įvesties sritį dar kartą.</span><span class="sxs-lookup"><span data-stu-id="26ffb-251">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="26ffb-252">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-252">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="26ffb-253">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="26ffb-253">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="26ffb-254">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="26ffb-254">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="26ffb-255">Vartotojo įvestis, pavyzdžiui, „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų, pavadinimu „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="26ffb-255">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="26ffb-256">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="26ffb-256">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="26ffb-257">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra paskyra, pavadinta „Contoso”).</span><span class="sxs-lookup"><span data-stu-id="26ffb-257">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="26ffb-258">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="26ffb-258">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="26ffb-259">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="26ffb-259">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="26ffb-260">LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-260">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="26ffb-261">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išsiųstas į LUIS tarnybą ir „Azure bot framework“.</span><span class="sxs-lookup"><span data-stu-id="26ffb-261">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="26ffb-262">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="26ffb-262">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="26ffb-263">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="26ffb-263">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="26ffb-264">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="26ffb-264">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="26ffb-265">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="26ffb-265">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="26ffb-266">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="26ffb-266">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="26ffb-267">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="26ffb-267">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="26ffb-268">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="26ffb-268">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="26ffb-269">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="26ffb-269">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="26ffb-270">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="26ffb-270">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="26ffb-271">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="26ffb-271">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="26ffb-272">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="26ffb-272">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="26ffb-273">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="26ffb-273">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="26ffb-274">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="26ffb-274">See also</span></span>

[<span data-ttu-id="26ffb-275">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="26ffb-275">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="26ffb-276">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="26ffb-276">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="26ffb-277">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="26ffb-277">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]