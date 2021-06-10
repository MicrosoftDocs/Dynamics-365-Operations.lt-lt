---
title: „Human Resources“ programa platformoje „Teams“
description: Šioje temoje pristatoma „Microsoft Dynamics 365 Human Resources” programa, veikianti platformoje „Microsoft Teams“.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1cceb15d64215cb8d5c996df792e863d466f87d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053568"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="7bdab-103">„Human Resources“ programa platformoje „Teams“</span><span class="sxs-lookup"><span data-stu-id="7bdab-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7bdab-104">„Microsoft Teams“ veikianti programa „Microsoft Dynamics 365 Human Resources“ leidžia darbuotojams greitai prašyti išleisti iš darbo ir peržiūrėti savo ne darbo laiko balanso informaciją programoje „Microsoft Teams“.</span><span class="sxs-lookup"><span data-stu-id="7bdab-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="7bdab-105">Norėdami prašyti informacijos, darbuotojai gali bendrauti su robotu.</span><span class="sxs-lookup"><span data-stu-id="7bdab-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="7bdab-106">Skirtuke **Ne darbo laikas** pateikiama išsamesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="7bdab-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="7bdab-107">Be to, jie gali siųsti žmonėms informaciją apie būsimą ne darbo laiką skiltyse „Komandos” ir „Pokalbiai” už „Human Resources” programėlės ribų.</span><span class="sxs-lookup"><span data-stu-id="7bdab-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![„Human Resources Teams“ atostogų programos robotas](./media/hr-teams-leave-app-bot.png)

![„Human Resources Teams“ atostogų programos skirtukas Ne darbo laikas](./media/hr-teams-leave-app-timeoff-tab.png)

![„Human Resources” atostogų užklausos kortelė](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="7bdab-111">Diegimas ir nustatymas</span><span class="sxs-lookup"><span data-stu-id="7bdab-111">Install and setup</span></span>

<span data-ttu-id="7bdab-112">Programą „Dynamics 365 Human Resources“ galite rasti „Teams“ parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="7bdab-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="7bdab-113">Daugiau informacijos, kaip įdiegti „Teams“ programą, žr. [Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="7bdab-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="7bdab-114">Informacijos apie programų teisių valdymą „Teams“ žr. [Programų teisių strategijų valdymas programoje „Microsoft Teams“](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="7bdab-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="7bdab-115">Jei norite, kad jūsų naudotojai programėlėje peržiūrėti atostogų ir neatvykimo kalendorių, funkcijų valdymo srityje turėsite įjungti **Atostogų ir neatvykimo kalendorių komandose**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="7bdab-116">Daugiau informacijos apie funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="7bdab-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="7bdab-117">„Human Resources“ programos „Teams“ pranešimų įjungimas</span><span class="sxs-lookup"><span data-stu-id="7bdab-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="7bdab-118">Jei norite, kad vartotojai gautų atostogų užklausų pranešimus „Teams” programoje, turite įjungti pranešimus „Dynamics 365 Human Resources”.</span><span class="sxs-lookup"><span data-stu-id="7bdab-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7bdab-119">Pranešimus gaus tik tie vartotojai, kurie yra prisijungę prie „Teams” ir naudoja „Dynamics 365 Human Resources” programą.</span><span class="sxs-lookup"><span data-stu-id="7bdab-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="7bdab-120">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7bdab-121">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-121">Select **Links**.</span></span>

3. <span data-ttu-id="7bdab-122">Dalyje **Sąranka** pasirinkite **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="7bdab-123">Skirtuke **Bendra** nustatykite **Įjungti „Teams” programos pranešimus** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![„Teams” programos pranešimų įjungimas sistemos parametruose](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="7bdab-125">Norėdami įjungti „Teams” pranešimus visiems vartotojams, paraginti pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![„Teams” pranešimų įjungimas visiems vartotojams](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="7bdab-127">„Teams” pranešimų įjungimas arba išjungimas atskiriems vartotojams</span><span class="sxs-lookup"><span data-stu-id="7bdab-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="7bdab-128">Įjungę „Dynamics 365 Human Resources” komandų programos pranešimus, galite įjungti arba išjungti pranešimus atskiriems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7bdab-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="7bdab-129">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="7bdab-130">Pasirinkite **Nuorodos**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-130">Select **Links**.</span></span>

3. <span data-ttu-id="7bdab-131">Dalyje **Vartotojai** pasirinkite **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="7bdab-132">Pasirinkite skirtuką **Darbo eiga**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="7bdab-133">Nustatykite parinktį **Įjungti „Teams” programos pranešimus** į **Taip**, norėdami įjungti pranešimus vartotojui, arba į **Ne**, norėdami išjungti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="7bdab-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![„Teams” programos pranešimų įjungimas darbo eigos skirtuke Vartotojo parinktys](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="7bdab-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="7bdab-136">Palaikomos kalbos</span><span class="sxs-lookup"><span data-stu-id="7bdab-136">Supported languages</span></span>

<span data-ttu-id="7bdab-137">Programa „Dynamics 365 Human Resources“ komandose palaiko šias kalbas:</span><span class="sxs-lookup"><span data-stu-id="7bdab-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="7bdab-138">Vietos ID</span><span class="sxs-lookup"><span data-stu-id="7bdab-138">Locale ID</span></span> | <span data-ttu-id="7bdab-139">Kalba</span><span class="sxs-lookup"><span data-stu-id="7bdab-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="7bdab-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="7bdab-140">de-DE</span></span> | <span data-ttu-id="7bdab-141">Vokiečių (Vokietija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-141">German (Germany)</span></span> |
| <span data-ttu-id="7bdab-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="7bdab-142">es-ES</span></span> | <span data-ttu-id="7bdab-143">Ispanų (Ispanija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="7bdab-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="7bdab-144">es-MX</span></span> | <span data-ttu-id="7bdab-145">Ispanų (Meksika)</span><span class="sxs-lookup"><span data-stu-id="7bdab-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="7bdab-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="7bdab-146">fr-CA</span></span> | <span data-ttu-id="7bdab-147">Prancūzų (Kanada)</span><span class="sxs-lookup"><span data-stu-id="7bdab-147">French (Canada)</span></span> |
| <span data-ttu-id="7bdab-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="7bdab-148">fr-FR</span></span> | <span data-ttu-id="7bdab-149">Prancūzų (Prancūzija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-149">French (France)</span></span> |
| <span data-ttu-id="7bdab-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="7bdab-150">it-IT</span></span> | <span data-ttu-id="7bdab-151">Italų (Italija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-151">Italian (Italy)</span></span> |
| <span data-ttu-id="7bdab-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="7bdab-152">nl-NL</span></span> | <span data-ttu-id="7bdab-153">Olandų (Nyderlandai)</span><span class="sxs-lookup"><span data-stu-id="7bdab-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="7bdab-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="7bdab-154">pt-BR</span></span> | <span data-ttu-id="7bdab-155">Portugalų (Brazilija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="7bdab-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="7bdab-156">tr-TR</span></span> | <span data-ttu-id="7bdab-157">Turkų (Turkija)</span><span class="sxs-lookup"><span data-stu-id="7bdab-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="7bdab-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="7bdab-158">zh-CN</span></span> | <span data-ttu-id="7bdab-159">Kinų (supaprastintoji)</span><span class="sxs-lookup"><span data-stu-id="7bdab-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="7bdab-160">Pastabos</span><span class="sxs-lookup"><span data-stu-id="7bdab-160">Notes</span></span>

<span data-ttu-id="7bdab-161">Toliau nurodyti darbo elementai perduodami tolesniems leidimams:</span><span class="sxs-lookup"><span data-stu-id="7bdab-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="7bdab-162">Darbo elementas</span><span class="sxs-lookup"><span data-stu-id="7bdab-162">Work item</span></span> | <span data-ttu-id="7bdab-163">Būsena</span><span class="sxs-lookup"><span data-stu-id="7bdab-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="7bdab-164">Balansas yra netinkamas, kai ne darbo laikas pateikiamas būsimo laikotarpio datai.</span><span class="sxs-lookup"><span data-stu-id="7bdab-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="7bdab-165">Prognozavimas dar negalimas.</span><span class="sxs-lookup"><span data-stu-id="7bdab-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="7bdab-166">Rodomas dabartinio laikotarpio balansas.</span><span class="sxs-lookup"><span data-stu-id="7bdab-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="7bdab-167">Nepavyksta atšaukti užklausos **Peržiūrima**.</span><span class="sxs-lookup"><span data-stu-id="7bdab-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="7bdab-168">Ši funkcija šiuo metu nepalaikoma ir bus įtraukta į būsimą leidimą.</span><span class="sxs-lookup"><span data-stu-id="7bdab-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="7bdab-169">Balanso informacija skaičiuojama iki šios dienos.</span><span class="sxs-lookup"><span data-stu-id="7bdab-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="7bdab-170">Sistema šiuo metu nerodo balansų iki kaupimo laikotarpio, net jei tai sukonfigūruota atostogų ir neatvykimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="7bdab-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="7bdab-171">Trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="7bdab-171">Troubleshooting</span></span>

<span data-ttu-id="7bdab-172">Jei vartotojui kyla problemų prisijungiant arba naudojant „Human Resources Teams“ programą, bandykite vadovautis šiomis trikčių šalinimo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="7bdab-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="7bdab-173">Jei atlikus trikčių šalinimą problemų vis dar nepavyko išspręsti, kreipkitės į pagalbos tarnybą.</span><span class="sxs-lookup"><span data-stu-id="7bdab-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="7bdab-174">Norėdami gauti daugiau informacijos, [Gauti pagalbos](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="7bdab-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="7bdab-175">Nepavyksta prisijungti prie „Teams“ programos „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="7bdab-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="7bdab-176">Jei naudotojas susisiekia su jumis, nes jis negali prisijungti prie programos, patikrinkite, ar jis turi „Human Resources“ turi susijusį darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="7bdab-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="7bdab-177">Klaida tvirtinant atostogų prašymus „Teams“ programoje „Human Resources“</span><span class="sxs-lookup"><span data-stu-id="7bdab-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="7bdab-178">Jei vartotojas gauna klaidą bandydamas patvirtinti atostogų prašymą programoje „Teams“, išbandykite šiuos trikčių šalinimo veiksmus:</span><span class="sxs-lookup"><span data-stu-id="7bdab-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="7bdab-179">Įsitikinkite, kad jo „Teams“ paskyra sutampa su naudojama prieigai prie „Human Resources“ paskyra.</span><span class="sxs-lookup"><span data-stu-id="7bdab-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="7bdab-180">Patikrinkite, ar vartotojas gali patvirtinti prašymą, patikrindami atostogų patvirtinimo darbo eigos parametrus.</span><span class="sxs-lookup"><span data-stu-id="7bdab-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="7bdab-181">Norėdami gauti daugiau informacijos apie atostogų prašymo darbo eigas, žr. [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="7bdab-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="7bdab-182">Palikti tvirtintojams negauus pokalbių su „Teams“ pranešimais atostogų užklausoms patvirtinti</span><span class="sxs-lookup"><span data-stu-id="7bdab-182">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="7bdab-183">Užtikrinkite, kad aplinkos ir vartotojo pranešimai yra įgalinti.</span><span class="sxs-lookup"><span data-stu-id="7bdab-183">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="7bdab-184">Dėl daugiau informacijos, žiūrėkite [Įjungti „Human Resources“ programos pranešimus „Teams“](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ir [Įjungti „Teams“ pranešimus ir juos išjungti atskiriems vartotojams](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="7bdab-184">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="7bdab-185">Įsitikinkite, kad vartotojai yra prisiregistravę pokalbių skirtuke naudodami tą **pačią** prisijungimo informaciją, kuriuos jie naudoja atostogų užklausoms patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="7bdab-185">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="7bdab-186">Norėdami prisijungti naudodami tinkamą prisjungimo informaciją, naudokite pranešimus „atsijungti" ir „prisijungti".</span><span class="sxs-lookup"><span data-stu-id="7bdab-186">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="7bdab-187">Jei problema išlieka, patikrinkite verslo įvykių sistemos paketinės užduoties būseną kaip sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="7bdab-187">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="7bdab-188">Jei jis yra laukimo ar vykdymo etape, po kelių minučių patikrinkite atgal.</span><span class="sxs-lookup"><span data-stu-id="7bdab-188">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="7bdab-189">Jei būsena nekinta, užregistruokite palaikymo bilietą, kad mūsų komanda galėtų padėti išspręsti problemą.</span><span class="sxs-lookup"><span data-stu-id="7bdab-189">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="7bdab-190">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="7bdab-190">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="7bdab-191">„Microsoft Language Understanding Intelligent Service” (LUIS)</span><span class="sxs-lookup"><span data-stu-id="7bdab-191">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="7bdab-192">Naudojant „Dynamics 365 Human Resources“ robotą programoje „Microsoft Teams“, analizuojamos vartotojo tekstinės įvestys, kad būtų suprasta pagrindinė užklausa / ketinimas.</span><span class="sxs-lookup"><span data-stu-id="7bdab-192">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="7bdab-193">Vartotojo įvestis, pavyzdžiui, „Ieškoti Contoso paskyroje“, yra nukreipiama į vieną iš „Microsoft Cognitive Services“ tarnybų, pavadinimu „Language Understanding Intelligent Service“ (LUIS).</span><span class="sxs-lookup"><span data-stu-id="7bdab-193">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="7bdab-194">Daugiau apie LUIS skaitykite  [čia](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="7bdab-194">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="7bdab-195">LUIS tarnyba išaiškina arba supranta vartotojo įvesties ketinimą (šiuo atveju ketinimas yra rasti informaciją) ir paskirties objektą (šiuo atveju numatomas objektas yra paskyra, pavadinta „Contoso”).</span><span class="sxs-lookup"><span data-stu-id="7bdab-195">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="7bdab-196">Tada ši informacija perduodama į „Microsoft“  [„Azure Bot Framework“](https://azure.microsoft.com/services/bot-service/), kuri sąveikauja su duomenimis, gautais iš „Dynamics 365 Human Resources“, ir nuskaito reikiamą vartotojo užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="7bdab-196">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span>

<span data-ttu-id="7bdab-197">Įdiegdami ir suteikdami prieigos teisę naudoti robotą jūs sutinkate leisti LUIS tarnybai ir „Azure bot framework“ apdoroti įvesties ketinimą, o tai tampa patobulinta vartotojo šnekamąja patirtimi.</span><span class="sxs-lookup"><span data-stu-id="7bdab-197">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="7bdab-198">LUIS tarnyba ir „Azure bot framework“ gali turėti skirtingus atitikties lygius, palyginti su „Dynamics 365 Human Resources“.</span><span class="sxs-lookup"><span data-stu-id="7bdab-198">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7bdab-199">LUIS tarnyba turi prieigą tik prie vartotojo užklausų ir nėra skirta būti prijungta prie vartotojo „Dynamics 365 Human Resources“ duomenų ar paskyros, o „Dynamics 365 Human Resources“ roboto vartotojas gali savanoriškai įvesti užklausą su kliento duomenimis, asmens duomenimis arba kitais duomenimis, ir toks užklausos turinys gali būti išsiųstas į LUIS tarnybą ir „Azure bot framework“.</span><span class="sxs-lookup"><span data-stu-id="7bdab-199">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="7bdab-200">Vartotojo užklausų ir pranešimų turinys saugomas LUIS sistemoje ne ilgiau nei 30 dienų, neaktyvios būsenos duomenys yra užšifruojami ir nenaudojami mokymui ir tarnybos tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="7bdab-200">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="7bdab-201">Daugiau apie „Cognitive Services“ skaitykite  [čia](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="7bdab-201">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="7bdab-202">Jei norite programų administravimo parametrus valdyti platformoje „Microsoft Teams“, eikite į [„Microsoft Teams“ administravimo centrą](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="7bdab-202">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="7bdab-203">„Microsoft Teams”, „Azure” įvykių tinklelis ir „Azure Cosmos DB”</span><span class="sxs-lookup"><span data-stu-id="7bdab-203">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="7bdab-204">Naudojant „Dynamics 365 Human Resources” programą, esančią „Microsoft Teams”, tam tikri kliento duomenys gali būti naudojami už geografinio regiono, kuriame įdiegta Jūsų nuomotojo „Human Resources“ paslauga, ribų.</span><span class="sxs-lookup"><span data-stu-id="7bdab-204">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="7bdab-205">„Dynamics 365 Human Resources” perduoda darbuotojo atostogų užklausą ir darbo eigos užduoties informaciją į „Microsoft Azure” įvykių tinklelį ir „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="7bdab-205">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="7bdab-206">Šie duomenys gali būti saugomi iki 24 valandų „Microsoft Azure” įvykių tinklelyje ir apdorojami Jungtinėse Valstijose, užšifruojami transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jų nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="7bdab-206">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7bdab-207">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="7bdab-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="7bdab-208">Bendraudami su pokalbių robotu „Human Resources” programėlėje, pokalbio turinys gali būti saugomas „Azure Cosmos DB” ir perduodamas „Microsoft Teams”.</span><span class="sxs-lookup"><span data-stu-id="7bdab-208">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="7bdab-209">Šie duomenys gali būti saugomi „Azure Cosmos DB” iki 24 valandų ir gali būti apdorojami už geografinio regiono, kur įdiegta Jūsų nuomotojo „Human Resources” paslauga, ribų, užšifruojama transportuojant bei neaktyvioje būsenoje, o „Microsoft” arba jo pagalbiniai duomenų tvarkytojai jos nenaudoja mokymui ar paslaugų tobulinimui.</span><span class="sxs-lookup"><span data-stu-id="7bdab-209">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="7bdab-210">Norėdami suprasti, kur saugomi Jūsų duomenys programoje „Teams”, žr.: [Saugyklos vieta „Microsoft Teams”](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="7bdab-210">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="7bdab-211">Norėdami apriboti prieigą prie „Human Resources” programėlės, esančios „Microsoft Teams”, Jūsų organizacijai arba Jūsų organizacijos vartotojams, žr. [Programos teisių strategijų valdymas „Microsoft Teams”](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="7bdab-211">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="7bdab-212">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="7bdab-212">See also</span></span> 

[<span data-ttu-id="7bdab-213">„Microsoft Teams“ atsisiuntimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="7bdab-213">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="7bdab-214">„Microsoft Teams“ pagalbos centras</span><span class="sxs-lookup"><span data-stu-id="7bdab-214">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="7bdab-215">Atostogų prašymų valdymas „Teams“</span><span class="sxs-lookup"><span data-stu-id="7bdab-215">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]