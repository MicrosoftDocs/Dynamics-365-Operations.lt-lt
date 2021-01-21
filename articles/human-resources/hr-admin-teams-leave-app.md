---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
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
ms.openlocfilehash: 51f04e553da822c4e09d31bcd72c71b674ad1f1b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930022"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="a2e0f-103">„Human Resources“ programa platformoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="a2e0f-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a2e0f-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="a2e0f-105">Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="a2e0f-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="a2e0f-107">Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![„Human Resources Teams“ atostogų programos robotas](./media/hr-admin-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="a2e0f-111">Diegimas ir nustatymas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-111">Install and setup</span></span>

<span data-ttu-id="a2e0f-112">Programą „Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="a2e0f-113">Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="a2e0f-114">Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="a2e0f-115">„Human Resources“ programos „Teams“ pranešimų įjungimas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="a2e0f-116">Jei norite, kad vartotojai gautų atostogų užklausų pranešimus „Teams” programoje, turite įjungti pranešimus „Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="a2e0f-117">Pranešimus gaus tik tie vartotojai, kurie yra prisijungę prie „Teams” ir naudoja „Human Resources Teams” programą.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="a2e0f-118">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a2e0f-119">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-119">Select **Links**.</span></span>

3. <span data-ttu-id="a2e0f-120">Dalyje **Sąranka** pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="a2e0f-121">Skirtuke **Bendra** nustatykite **Įjungti „Teams” programos pranešimus** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![„Teams” programos pranešimų įjungimas sistemos parametruose](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="a2e0f-123">Norėdami įjungti „Teams” pranešimus visiems vartotojams, paraginti pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![„Teams” pranešimų įjungimas visiems vartotojams](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="a2e0f-125">„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams</span><span class="sxs-lookup"><span data-stu-id="a2e0f-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="a2e0f-126">Įjungę „Human Resources Teams” programos pranešimus, galite įjungti arba išjungti pranešimus atskiriems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="a2e0f-127">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a2e0f-128">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-128">Select **Links**.</span></span>

3. <span data-ttu-id="a2e0f-129">Dalyje **Vartotojai** pasirinkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="a2e0f-130">Pasirinkite skirtuką **Darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="a2e0f-131">Nustatykite parinktį **Įjungti „Teams” programos pranešimus** į **Taip**, norėdami įjungti pranešimus vartotojui, arba į **Ne**, norėdami išjungti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![„Teams” programos pranešimų įjungimas darbo eigos skirtuke Vartotojo parinktys](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="a2e0f-133">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="a2e0f-134">Žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="a2e0f-134">Known issues</span></span>

| <span data-ttu-id="a2e0f-135">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-135">Issue</span></span> | <span data-ttu-id="a2e0f-136">Būsena</span><span class="sxs-lookup"><span data-stu-id="a2e0f-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="a2e0f-137">Horizontalus slankiojimas neveikia „Android“ telefonuose</span><span class="sxs-lookup"><span data-stu-id="a2e0f-137">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="a2e0f-138">Horizontalus slankiojimas nėra problema „iOS“ ar stacionariuose prietaisuose.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-138">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="a2e0f-139">Dirbame, kad ištaisytumėme šią problemą „Android“.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-139">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="a2e0f-140">Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-140">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="a2e0f-141">Prognozavimas dar negalimas.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-141">Forecasting isn't yet available.</span></span> <span data-ttu-id="a2e0f-142">Rodomas dabartinio laikotarpio balansas.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-142">The balance displays for the current date.</span></span> |
| <span data-ttu-id="a2e0f-143">Nepavyksta atšaukti užklausos **Peržiūrima**.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-143">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="a2e0f-144">Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-144">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="a2e0f-145">Balanso informacija skaičiuojama iki šios dienos.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-145">Balance information is calculated as of today.</span></span> | <span data-ttu-id="a2e0f-146">Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruotaa atostogų ir neatvykimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-146">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="a2e0f-147">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-147">Troubleshooting</span></span>

<span data-ttu-id="a2e0f-148">Jei vartotojui kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-148">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="a2e0f-149">Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-149">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="a2e0f-150">Norėdami gauti daugiau informacijos, [Gauti pagalbos](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-150">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="a2e0f-151">Nepavyksta prisijungti prie „Teams“ programos „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="a2e0f-151">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="a2e0f-152">Jei vartotojas susisiekia su jumis, nes jis negali prisijungti prie programos, patikrinkite, ar vartotojas „Human Resources“ turi susijusį darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-152">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="a2e0f-153">Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="a2e0f-153">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="a2e0f-154">Jei vartotojas gauna klaidą bandydamas patvirtinti atostogų prašymą programoje „Teams“, atlikite šiuos trikčių šalinimo veiksmus:</span><span class="sxs-lookup"><span data-stu-id="a2e0f-154">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="a2e0f-155">Įsitikinkite, kad jo „Teams“ paskyra sutampa su naudojama prieigai prie „Human Resources“ paskyra.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-155">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="a2e0f-156">Patikrinkite, ar vartotojas gali patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-156">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="a2e0f-157">Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-157">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a2e0f-158">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-158">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a2e0f-159">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a2e0f-159">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a2e0f-160">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-160">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a2e0f-161">Vartotojo įvestis, pvz., „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų – „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-161">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a2e0f-162">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-162">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a2e0f-163">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra „Contoso“ paskyra).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-163">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a2e0f-164">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-164">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a2e0f-165">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure“ roboto sistemai apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-165">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a2e0f-166">LUIS tarnyba ir „Azure“ roboto sistema gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-166">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a2e0f-167">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išiųstas į LUIS tarnybą ir „Azure“ roboto sistemą.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-167">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a2e0f-168">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-168">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a2e0f-169">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-169">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a2e0f-170">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-170">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="a2e0f-171">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="a2e0f-171">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="a2e0f-172">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-172">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="a2e0f-173">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-173">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a2e0f-174">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-174">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a2e0f-175">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="a2e0f-176">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-176">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="a2e0f-177">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="a2e0f-177">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a2e0f-178">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-178">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="a2e0f-179">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a2e0f-179">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="a2e0f-180">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a2e0f-180">See also</span></span> 

[<span data-ttu-id="a2e0f-181">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="a2e0f-181">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a2e0f-182">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="a2e0f-182">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a2e0f-183">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="a2e0f-183">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)
