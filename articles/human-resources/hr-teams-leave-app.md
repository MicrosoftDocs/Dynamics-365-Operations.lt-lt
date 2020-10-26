---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929998"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="2b91d-103">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="2b91d-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="2b91d-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="2b91d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="2b91d-105">Galite sąveikauti su robotu, kad prašytumėte informacijos ir pradėtumėte atostogų užklausą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="2b91d-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="2b91d-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="2b91d-107">Be to, galite siųsti žmonėms informaciją apie savo būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.</span><span class="sxs-lookup"><span data-stu-id="2b91d-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="2b91d-108">Programos diegimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-108">Install the app</span></span>

<span data-ttu-id="2b91d-109">Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="2b91d-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="2b91d-110">Programoje „Microsoft Teams“ pasirinkite daugtaškius.</span><span class="sxs-lookup"><span data-stu-id="2b91d-110">In Microsoft Teams, select the ellipses.</span></span>

   ![„Human Resources Teams“ atostogų programos daugtaškiai](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="2b91d-112">Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![„Human Resources Teams“ atostogų programos HR plytelė](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="2b91d-114">Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-114">Select the **Add** button to install the app.</span></span>

   ![„Human Resources Teams“ atostogų programos diegimas](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="2b91d-116">Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![„Human Resources Teams“ atostogų programos mygtukas Parametrai](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="2b91d-118">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="2b91d-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="2b91d-119">Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2b91d-120">Programėlė dabar palaiko sistemos administratoriaus saugos vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="2b91d-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="2b91d-121">Roboto naudojimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-121">Use the bot</span></span>

<span data-ttu-id="2b91d-122">Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.</span><span class="sxs-lookup"><span data-stu-id="2b91d-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![„Human Resources Teams“ atostogų programos roboto pasveikinimo pranešimas](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="2b91d-124">Pirmą kartą bendraujant su robotu, gali reikėti prisijungti.</span><span class="sxs-lookup"><span data-stu-id="2b91d-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="2b91d-125">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="2b91d-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="2b91d-126">Roboto galite prašyti toliau pateiktų dalykų.</span><span class="sxs-lookup"><span data-stu-id="2b91d-126">You can ask the bot to:</span></span>

- <span data-ttu-id="2b91d-127">Rodyti kiekvieno atostogų tipo, kuriam esate užsiregistravę, ne darbo laiko balanso informaciją.</span><span class="sxs-lookup"><span data-stu-id="2b91d-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![„Human Resources Teams“ atostogų programos rodomi balansai](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="2b91d-129">Rodyti papildomą informaciją apie konkretų atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-129">Show additional details about a specific leave type.</span></span>

   ![„Human Resources Teams“ atostogų programos rodoma informacija](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="2b91d-131">Pateikti atostogų prašymą už jus.</span><span class="sxs-lookup"><span data-stu-id="2b91d-131">Start a leave request for you.</span></span>

   ![„Human Resources Teams“ atostogų programos atostogų prašymas](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="2b91d-133">Pateikus atostogų užklausą, galite koreguoti dienas pačioje kortelėje.</span><span class="sxs-lookup"><span data-stu-id="2b91d-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![„Human Resources Teams“ atostogų programos redagavimo prašymas](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="2b91d-135">Kai užpildysite visą informaciją, pasirinkite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="2b91d-136">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="2b91d-136">You can also select **Save as draft** to come back to it later.</span></span>

![„Human Resources Teams“ atostogų programos prašymo pateikimas](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="2b91d-138">Atostogų valdymas programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="2b91d-138">Manage your leave in Teams</span></span>

<span data-ttu-id="2b91d-139">Skirtuke **Ne darbo laikas** galite peržiūrėti:</span><span class="sxs-lookup"><span data-stu-id="2b91d-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="2b91d-140">Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją</span><span class="sxs-lookup"><span data-stu-id="2b91d-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="2b91d-141">Būsimų atostogų prašymus</span><span class="sxs-lookup"><span data-stu-id="2b91d-141">Upcoming leave requests</span></span>

- <span data-ttu-id="2b91d-142">Prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="2b91d-142">Time-off requests</span></span>

- <span data-ttu-id="2b91d-143">Atostogų prašymų juodraščius</span><span class="sxs-lookup"><span data-stu-id="2b91d-143">Draft leave requests</span></span>

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="2b91d-145">Naujo prašymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-145">Create a new request</span></span>

1. <span data-ttu-id="2b91d-146">Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-146">To create a new leave request, select **New request**.</span></span>

   ![„Human Resources Teams“ atostogų programos naujas prašymas](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="2b91d-148">Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="2b91d-150">Jei reikia, įveskite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="2b91d-151">Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.</span><span class="sxs-lookup"><span data-stu-id="2b91d-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="2b91d-152">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2b91d-153">Taip pat galite įvesti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="2b91d-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="2b91d-154">Prašymų juodraščių valdymas</span><span class="sxs-lookup"><span data-stu-id="2b91d-154">Manage draft requests</span></span>

1. <span data-ttu-id="2b91d-155">Pasirinkite skirtuką **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-155">Select the **Drafts** tab.</span></span>

   ![„Human Resources Teams“ atostogų programos skirtukas Juodraščiai](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="2b91d-157">Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="2b91d-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="2b91d-158">Atlikite reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="2b91d-158">Make any necessary changes.</span></span> <span data-ttu-id="2b91d-159">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2b91d-160">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="2b91d-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![„Human Resources Teams“ atostogų programos juodraščio redagavimas](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="2b91d-162">Atsakyti į „Teams” pranešimus</span><span class="sxs-lookup"><span data-stu-id="2b91d-162">Respond to Teams notifications</span></span>

<span data-ttu-id="2b91d-163">Kai jūs arba darbuotojas, kurio tvirtintojas esate jūs, pateikiate atostogų užklausą, gausite pranešimą „Human Resources“ programoje „Teams“.</span><span class="sxs-lookup"><span data-stu-id="2b91d-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="2b91d-164">Galite pasirinkti pranešimą, norėdami jį peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="2b91d-164">You can select the notification to view it.</span></span> <span data-ttu-id="2b91d-165">Pranešimai taip pat rodomi **pokalbių** srityje.</span><span class="sxs-lookup"><span data-stu-id="2b91d-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="2b91d-166">Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="2b91d-167">Taip pat galite pateikti pasirinktinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-167">You can also provide an optional message.</span></span>

![Atostogų užklausos pranešimas programoje „Human Resources Teams“](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="2b91d-169">Siųsti būsimo ne darbo laiko informaciją savo bendradarbiams</span><span class="sxs-lookup"><span data-stu-id="2b91d-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="2b91d-170">Įdiegę „Human Resources” programėlę, pritaikytą „Teams”, galite lengvai siųsti informaciją apie savo būsimą ne darbo laiką savo bendradarbiams skiltyje „Komandos” arba „Pokalbiai”.</span><span class="sxs-lookup"><span data-stu-id="2b91d-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="2b91d-171">„Komandos” arba „Pokalbiai” skiltyje, esančiose programėlėje „Teams”, pasirinkite „Human Resources” mygtuką, esantį po pokalbio langu.</span><span class="sxs-lookup"><span data-stu-id="2b91d-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![„Human Resources” mygtukas, esantis po pokalbio langu](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="2b91d-173">Pasirinkite atostogų užklausą, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="2b91d-173">Select the leave request you want to share.</span></span> <span data-ttu-id="2b91d-174">Jei norite bendrinti juodraštinę atostogų užklausą, pirmiausia pasirinkite **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Pasirinkite būsimą atostogų užklausą bendrinimui](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="2b91d-176">Jūsų atostogų užklausa bus rodoma pokalbiuose.</span><span class="sxs-lookup"><span data-stu-id="2b91d-176">Your leave request will display in the chat.</span></span>

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="2b91d-178">Jei bendrinote juodraštinę užklausą, ji bus rodomas kaip juodraštis:</span><span class="sxs-lookup"><span data-stu-id="2b91d-178">If you shared a draft request, it will display as a draft:</span></span>

![„Human Resources” juodraštinės atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="2b91d-180">Peržiūrėti komandos atostogų kalendorių</span><span class="sxs-lookup"><span data-stu-id="2b91d-180">View your team's leave calendar</span></span>

<span data-ttu-id="2b91d-181">Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="2b91d-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="2b91d-182">„Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="2b91d-183">Pasirinkite **Komandos kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="2b91d-183">Select **Team calendar**.</span></span>

   ![Kalendoriaus peržiūra „Human Resources Teams“ programoje](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="2b91d-185">Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="2b91d-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Ne darbo laiko kalendorius „Human Resources Teams“ programoje](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="2b91d-187">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-187">Troubleshooting</span></span>

<span data-ttu-id="2b91d-188">Jei kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="2b91d-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="2b91d-189">Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="2b91d-190">Norėdami gauti daugiau informacijos, [Gauti pagalbos](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="2b91d-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="2b91d-191">Nepavyksta prisijungti prie „Teams“ programos „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="2b91d-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="2b91d-192">Jei negalite prisijungti prie programos, gali būti, kad paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, nėra susieta su darbuotojo įrašu „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="2b91d-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2b91d-193">Kreipkitės į sistemos administratorių, kad įsitikintumėte, kad jūsų darbuotojo įrašas yra tinkamai susietas.</span><span class="sxs-lookup"><span data-stu-id="2b91d-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="2b91d-194">Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="2b91d-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="2b91d-195">Jei gaunate klaidą bandydami patvirtinti atostogų prašymą programoje „Teams“, atlikite šiuos trikčių šalinimo veiksmus:</span><span class="sxs-lookup"><span data-stu-id="2b91d-195">If you receive an error when you're trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="2b91d-196">Patikrinkite, ar paskyra, kurią naudojate prisijungimui prie „Microsoft Teams“, yra ta pati, kurią naudojate prieigai prie „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="2b91d-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="2b91d-197">Patikrinkite, ar jus galite patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus.</span><span class="sxs-lookup"><span data-stu-id="2b91d-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="2b91d-198">Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="2b91d-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="2b91d-199">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-199">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="2b91d-200">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2b91d-200">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="2b91d-201">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="2b91d-201">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2b91d-202">Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="2b91d-202">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2b91d-203">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2b91d-203">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2b91d-204">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra).</span><span class="sxs-lookup"><span data-stu-id="2b91d-204">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2b91d-205">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="2b91d-205">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2b91d-206">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="2b91d-206">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2b91d-207">LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="2b91d-207">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2b91d-208">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą.</span><span class="sxs-lookup"><span data-stu-id="2b91d-208">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2b91d-209">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="2b91d-209">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2b91d-210">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2b91d-210">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2b91d-211">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2b91d-211">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="2b91d-212">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="2b91d-212">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="2b91d-213">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="2b91d-213">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="2b91d-214">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="2b91d-214">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="2b91d-215">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="2b91d-215">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2b91d-216">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2b91d-216">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="2b91d-217">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="2b91d-217">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="2b91d-218">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="2b91d-218">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2b91d-219">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2b91d-219">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="2b91d-220">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2b91d-220">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="2b91d-221">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="2b91d-221">See also</span></span>

[<span data-ttu-id="2b91d-222">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="2b91d-222">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2b91d-223">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="2b91d-223">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2b91d-224">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="2b91d-224">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
