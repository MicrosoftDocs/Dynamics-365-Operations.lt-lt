---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828919"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="3c464-103">„Human Resources“ programa platformoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="3c464-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3c464-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="3c464-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="3c464-105">Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu.</span><span class="sxs-lookup"><span data-stu-id="3c464-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="3c464-106">Skirtukas **Ne darbo laikas** suteikia išsamesnę informaciją. Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir„Pokalbiai” už „Human Resources” programėlės ribų.</span><span class="sxs-lookup"><span data-stu-id="3c464-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![„Human Resources Teams“ atostogų programos robotas](./media/hr-admin-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="3c464-110">Diegimas ir nustatymas</span><span class="sxs-lookup"><span data-stu-id="3c464-110">Install and setup</span></span>

<span data-ttu-id="3c464-111">Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="3c464-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="3c464-112">Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="3c464-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="3c464-113">Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="3c464-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="3c464-114">„Human Resources“ programos „Teams“ pranešimų įjungimas</span><span class="sxs-lookup"><span data-stu-id="3c464-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="3c464-115">Jei norite, kad vartotojai gautų atostogų užklausų pranešimus „Teams” programoje, turite įjungti pranešimus „Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="3c464-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="3c464-116">Pranešimus gaus tik tie vartotojai, kurie yra prisijungę prie „Teams” ir naudoja „Human Resources Teams” programą.</span><span class="sxs-lookup"><span data-stu-id="3c464-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="3c464-117">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="3c464-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="3c464-118">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="3c464-118">Select **Links**.</span></span>

3. <span data-ttu-id="3c464-119">Dalyje **Sąranka** pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3c464-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="3c464-120">Skirtuke **Bendra** nustatykite **Įjungti „Teams” programos pranešimus** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c464-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![„Teams” programos pranešimų įjungimas sistemos parametruose](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="3c464-122">Norėdami įjungti „Teams” pranešimus visiems vartotojams, paraginti pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3c464-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![„Teams” pranešimų įjungimas visiems vartotojams](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="3c464-124">„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams</span><span class="sxs-lookup"><span data-stu-id="3c464-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="3c464-125">Įjungę „Human Resources Teams” programos pranešimus, galite įjungti arba išjungti pranešimus atskiriems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="3c464-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="3c464-126">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="3c464-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="3c464-127">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="3c464-127">Select **Links**.</span></span>

3. <span data-ttu-id="3c464-128">Dalyje **Vartotojai** pasirinkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="3c464-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="3c464-129">Pasirinkite skirtuką **Darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="3c464-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="3c464-130">Nustatykite parinktį **Įjungti „Teams” programos pranešimus** į **Taip**, norėdami įjungti pranešimus vartotojui, arba į **Ne**, norėdami išjungti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="3c464-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![„Teams” programos pranešimų įjungimas darbo eigos skirtuke Vartotojo parinktys](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="3c464-132">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3c464-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="3c464-133">Žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="3c464-133">Known issues</span></span>

| <span data-ttu-id="3c464-134">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="3c464-134">Issue</span></span> | <span data-ttu-id="3c464-135">Būsena</span><span class="sxs-lookup"><span data-stu-id="3c464-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="3c464-136">Horizontalus slankiojimas neveikia „Android“ telefonuose</span><span class="sxs-lookup"><span data-stu-id="3c464-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="3c464-137">Horizontalus slankiojimas nėra problema „iOS“ ar stacionariuose prietaisuose.</span><span class="sxs-lookup"><span data-stu-id="3c464-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="3c464-138">Dirbame, kad ištaisytumėme šią problemą „Android“.</span><span class="sxs-lookup"><span data-stu-id="3c464-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="3c464-139">Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai.</span><span class="sxs-lookup"><span data-stu-id="3c464-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="3c464-140">Prognozavimas dar negalimas.</span><span class="sxs-lookup"><span data-stu-id="3c464-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="3c464-141">Rodomas dabartinio laikotarpio balansas.</span><span class="sxs-lookup"><span data-stu-id="3c464-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="3c464-142">Nepavyksta atšaukti užklausos **Peržiūrima**.</span><span class="sxs-lookup"><span data-stu-id="3c464-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="3c464-143">Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą.</span><span class="sxs-lookup"><span data-stu-id="3c464-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="3c464-144">Balanso informacija skaičiuojama iki šios dienos.</span><span class="sxs-lookup"><span data-stu-id="3c464-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="3c464-145">Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruotaa atostogų ir neatvykimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="3c464-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="3c464-146">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="3c464-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="3c464-147">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="3c464-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="3c464-148">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="3c464-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="3c464-149">Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="3c464-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="3c464-150">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="3c464-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="3c464-151">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra).</span><span class="sxs-lookup"><span data-stu-id="3c464-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="3c464-152">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="3c464-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="3c464-153">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="3c464-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="3c464-154">LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="3c464-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3c464-155">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą.</span><span class="sxs-lookup"><span data-stu-id="3c464-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="3c464-156">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="3c464-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="3c464-157">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="3c464-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="3c464-158">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3c464-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="3c464-159">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="3c464-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="3c464-160">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="3c464-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="3c464-161">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="3c464-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="3c464-162">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="3c464-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="3c464-163">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="3c464-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="3c464-164">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="3c464-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="3c464-165">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="3c464-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="3c464-166">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="3c464-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="3c464-167">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="3c464-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="3c464-168">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="3c464-168">See also</span></span> 

[<span data-ttu-id="3c464-169">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="3c464-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="3c464-170">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="3c464-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="3c464-171">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="3c464-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

