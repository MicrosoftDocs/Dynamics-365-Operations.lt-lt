---
title: Atostogų prašymų valdymas „Teams“
description: Šioje temoje parodyta, kaip prašyti išleisti iš darbo programoje „Dynamics 365 Human Resources“ naudojant „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766765"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="ded06-103">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="ded06-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ded06-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="ded06-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="ded06-105">Norėdami prašyti informacijos, galite bendrauti su robotu.</span><span class="sxs-lookup"><span data-stu-id="ded06-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="ded06-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="ded06-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="ded06-107">Programos diegimas</span><span class="sxs-lookup"><span data-stu-id="ded06-107">Install the app</span></span>

<span data-ttu-id="ded06-108">Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ded06-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="ded06-109">Programoje „Microsoft Teams“ pasirinkite daugtaškius.</span><span class="sxs-lookup"><span data-stu-id="ded06-109">In Microsoft Teams, select the ellipses.</span></span>

   ![„Human Resources Teams“ atostogų programos daugtaškiai](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="ded06-111">Raskite „Dynamics 365 Human Resources“ ir pasirinkite plytelę **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="ded06-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![„Human Resources Teams“ atostogų programos HR plytelė](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="ded06-113">Pasirinkite mygtuką **Įtraukti**, kad įdiegtumėte programą.</span><span class="sxs-lookup"><span data-stu-id="ded06-113">Select the **Add** button to install the app.</span></span>

   ![„Human Resources Teams“ atostogų programos diegimas](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="ded06-115">Jei programa automatiškai jūsų neprijungia, norėdami prisijungti pasirinkite skirtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ded06-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![„Human Resources Teams“ atostogų programos mygtukas Parametrai](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="ded06-117">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="ded06-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="ded06-118">Jei turite prieigą prie daugiau nei vieno „Human Resources“ egzemplioriaus, galite pasirinkti, kurią aplinką norite prijungti prie skirtuko **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ded06-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="ded06-119">Programa šiuo metu nepalaiko sistemos administratoriaus saugos vaidmens ir rodys klaidos pranešimą, jei prisijungsite naudodami sistemos administratoriaus paskyrą.</span><span class="sxs-lookup"><span data-stu-id="ded06-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="ded06-120">Norėdami prisijungti su kita paskyra, skirtuke **Parametrai** pasirinkite mygtuką **Perjungti paskyras**, tada prisijunkite naudodami vartotojo paskyrą, kuri neturi sistemos administratoriaus teisių.</span><span class="sxs-lookup"><span data-stu-id="ded06-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="ded06-121">Roboto naudojimas</span><span class="sxs-lookup"><span data-stu-id="ded06-121">Use the bot</span></span>

<span data-ttu-id="ded06-122">Kai programa įdiegiama, rodomas pasveikinimo pranešimas, kuriame informuojama, kokio tipo veiksmus jūsų vardu gali atlikti robotas.</span><span class="sxs-lookup"><span data-stu-id="ded06-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![„Human Resources Teams“ atostogų programos roboto pasveikinimo pranešimas](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="ded06-124">Pirmą kartą bendraujant su robotu, gali reikėti prisijungti.</span><span class="sxs-lookup"><span data-stu-id="ded06-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="ded06-125">Jei nematote prisijungimo dialogo lango, patikrinkite naršyklės parametrus, kad būtų leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="ded06-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="ded06-126">Roboto galite prašyti toliau pateiktų dalykų.</span><span class="sxs-lookup"><span data-stu-id="ded06-126">You can ask the bot to:</span></span>

- <span data-ttu-id="ded06-127">Rodyti kiekvieno atostogų tipo, kuriam esate užsiregistravę, ne darbo laiko balanso informaciją.</span><span class="sxs-lookup"><span data-stu-id="ded06-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![„Human Resources Teams“ atostogų programos rodomi balansai](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="ded06-129">Rodyti papildomą informaciją apie konkretų atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="ded06-129">Show additional details about a specific leave type.</span></span>

   ![„Human Resources Teams“ atostogų programos rodoma informacija](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="ded06-131">Pateikti atostogų prašymą už jus.</span><span class="sxs-lookup"><span data-stu-id="ded06-131">Start a leave request for you.</span></span>

   ![„Human Resources Teams“ atostogų programos atostogų prašymas](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="ded06-133">Pateikus atostogų užklausą, galite koreguoti dienas pačioje kortelėje.</span><span class="sxs-lookup"><span data-stu-id="ded06-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![„Human Resources Teams“ atostogų programos redagavimo prašymas](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="ded06-135">Kai užpildysite visą informaciją, pasirinkite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="ded06-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="ded06-136">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="ded06-136">You can also select **Save as draft** to come back to it later.</span></span>

![„Human Resources Teams“ atostogų programos prašymo pateikimas](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="ded06-138">Atostogų valdymas programoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="ded06-138">Manage your leave in Teams</span></span>

<span data-ttu-id="ded06-139">Skirtuke **Ne darbo laikas** galite peržiūrėti:</span><span class="sxs-lookup"><span data-stu-id="ded06-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="ded06-140">Kiekvieno atostogų tipo, kuriam esate užsiregistravę, balanso informaciją</span><span class="sxs-lookup"><span data-stu-id="ded06-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="ded06-141">Būsimų atostogų prašymus</span><span class="sxs-lookup"><span data-stu-id="ded06-141">Upcoming leave requests</span></span>

- <span data-ttu-id="ded06-142">Prašymus išleisti iš darbo</span><span class="sxs-lookup"><span data-stu-id="ded06-142">Time-off requests</span></span>

- <span data-ttu-id="ded06-143">Atostogų prašymų juodraščius</span><span class="sxs-lookup"><span data-stu-id="ded06-143">Draft leave requests</span></span>

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="ded06-145">Naujo prašymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ded06-145">Create a new request</span></span>

1. <span data-ttu-id="ded06-146">Norėdami kurti naują atostogų prašymą, pasirinkite **Naujas prašymas**.</span><span class="sxs-lookup"><span data-stu-id="ded06-146">To create a new leave request, select **New request**.</span></span>

   ![„Human Resources Teams“ atostogų programos naujas prašymas](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="ded06-148">Įveskite dieną ar dienas, kuriomis norite nedirbti, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="ded06-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![„Human Resources Teams“ atostogų programos ne darbo laiko įtraukimas](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="ded06-150">Jei reikia, įveskite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="ded06-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="ded06-151">Taip pat, jei reikia įveskite komentarus ir įtraukite priedus.</span><span class="sxs-lookup"><span data-stu-id="ded06-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="ded06-152">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="ded06-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="ded06-153">Taip pat galite įvesti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="ded06-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="ded06-154">Prašymų juodraščių valdymas</span><span class="sxs-lookup"><span data-stu-id="ded06-154">Manage draft requests</span></span>

1. <span data-ttu-id="ded06-155">Pasirinkite skirtuką **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="ded06-155">Select the **Drafts** tab.</span></span>

   ![„Human Resources Teams“ atostogų programos skirtukas Juodraščiai](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="ded06-157">Norėdami redaguoti prašymą pasirinkite pieštuką arba pasirinkite šiukšlinę, jei prašymą norite panaikinti.</span><span class="sxs-lookup"><span data-stu-id="ded06-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="ded06-158">Atlikite reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="ded06-158">Make any necessary changes.</span></span> <span data-ttu-id="ded06-159">Kai užpildysite visą informaciją, įveskite **Pateikti**, kad pateiktumėte patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="ded06-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="ded06-160">Taip pat galite pasirinkti **Įrašyti kaip juodraštį** ir grįžti prie jo vėliau.</span><span class="sxs-lookup"><span data-stu-id="ded06-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![„Human Resources Teams“ atostogų programos juodraščio redagavimas](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="ded06-162">„Teams” pranešimai</span><span class="sxs-lookup"><span data-stu-id="ded06-162">Teams notifications</span></span>

<span data-ttu-id="ded06-163">Kai jūs arba darbuotojas, kurio tvirtintojas esate jūs, pateikiate atostogų užklausą, gausite pranešimą „Human Resources“ programoje „Teams“.</span><span class="sxs-lookup"><span data-stu-id="ded06-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="ded06-164">Galite pasirinkti pranešimą, norėdami jį peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="ded06-164">You can select the notification to view it.</span></span> <span data-ttu-id="ded06-165">Pranešimai taip pat rodomi **pokalbių** srityje.</span><span class="sxs-lookup"><span data-stu-id="ded06-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="ded06-166">Jei esate tvirtintojas, pranešime galite pasirinkti **Patvirtinti** arba **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="ded06-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="ded06-167">Taip pat galite pateikti pasirinktinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ded06-167">You can also provide an optional message.</span></span>

![Atostogų užklausos pranešimas programoje „Human Resources Teams“](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="ded06-169">Peržiūrėti komandos atostogų kalendorių</span><span class="sxs-lookup"><span data-stu-id="ded06-169">View your team's leave calendar</span></span>

<span data-ttu-id="ded06-170">Jeigu esate vadovas, valdantis tiesiogines ataskaitas, galite peržiūrėti jūsų komandos patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="ded06-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="ded06-171">„Human Resources“ programoje „Teams“ pasirinkite **Ne darbo laikas**.</span><span class="sxs-lookup"><span data-stu-id="ded06-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="ded06-172">Pasirinkite **Komandos kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="ded06-172">Select **Team calendar**.</span></span>

   ![Kalendoriaus peržiūra „Human Resources Teams“ programoje](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="ded06-174">Kalendorius rodo jūsų tiesioginių ataskaitų patvirtintą ir laukiamą ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="ded06-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Ne darbo laiko kalendorius „Human Resources Teams“ programoje](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="ded06-176">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="ded06-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="ded06-177">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="ded06-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="ded06-178">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="ded06-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="ded06-179">Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="ded06-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="ded06-180">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="ded06-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="ded06-181">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra).</span><span class="sxs-lookup"><span data-stu-id="ded06-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="ded06-182">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="ded06-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="ded06-183">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="ded06-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="ded06-184">LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="ded06-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ded06-185">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą.</span><span class="sxs-lookup"><span data-stu-id="ded06-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="ded06-186">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="ded06-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="ded06-187">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="ded06-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="ded06-188">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="ded06-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="ded06-189">„Microsoft Azure” įvykių tinklelis ir „Microsoft Teams”</span><span class="sxs-lookup"><span data-stu-id="ded06-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="ded06-190">Naudojant pranešimų funkciją, skirtą „Dynamics 365 Human Resources” programai „Teams”, tam tikri kliento duomenys bus naudojami už geografinio regiono, kuriame įdiegta jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="ded06-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="ded06-191">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure Event Grid” ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="ded06-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="ded06-192">Šie duomenys gali būti saugomi iki 24 val. ir apdorojami Jungtinėse Valstijose, jie yra užšifruojami tranzito bei neaktyvioje būsenose ir „Microsoft” arba jos antriniai procesoriai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="ded06-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="ded06-193">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="ded06-193">See also</span></span>

[<span data-ttu-id="ded06-194">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="ded06-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="ded06-195">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="ded06-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="ded06-196">„Human Resources“ programa „Teams“</span><span class="sxs-lookup"><span data-stu-id="ded06-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
