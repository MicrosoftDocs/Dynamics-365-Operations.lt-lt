---
title: Darbo eigos patvirtinimo procesų konfigūravimas
description: Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08641eaac31813a8bee3231118f8e2bf802ea3e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555539"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="a3da4-103">Darbo eigos patvirtinimo procesų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a3da4-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3da4-104">Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.</span><span class="sxs-lookup"><span data-stu-id="a3da4-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="a3da4-105">Norėdami darbo eigos rengyklėje konfigūruoti patvirtinimo procesą, dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="a3da4-106">Patvirtinimo proceso pavadinimas</span><span class="sxs-lookup"><span data-stu-id="a3da4-106">Name the approval process</span></span>

<span data-ttu-id="a3da4-107">Atlikite šiuos veiksmus, jei norite įvesti patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="a3da4-108">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a3da4-109">Lauke **Pavadinimas** įveskite unikalų patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="a3da4-110">Nurodymas, kada sistema automatiškai atlieka veiksmą su dokumentu</span><span class="sxs-lookup"><span data-stu-id="a3da4-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="a3da4-111">Galite konfigūruoti sistemą, kad ji galėtų automatiškai vykdyti tam tikras sąlygas atitinkantį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="a3da4-112">Pvz., sistema gali patvirtinti išlaidų ataskaitas, kurių bendrosios sumos yra mažesnės nei 100 USD.</span><span class="sxs-lookup"><span data-stu-id="a3da4-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="a3da4-113">Atlikite šiuos veiksmus, norėdami nurodyti, kada sistema turi atlikti veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a3da4-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="a3da4-114">Kairiojoje srityje spustelėkite **Automatiniai veiksmai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="a3da4-115">Pažymėkite žymės langelį **Įjungti automatinius veiksmus**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="a3da4-116">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="a3da4-117">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="a3da4-117">Enter a condition.</span></span>
5. <span data-ttu-id="a3da4-118">Jei reikia, įveskite papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="a3da4-119">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="a3da4-120">Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="a3da4-121">Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="a3da4-122">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-122">Click **Test**.</span></span> <span data-ttu-id="a3da4-123">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="a3da4-124">Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="a3da4-125">Sąraše **Automatinio užbaigimo veiksmas** pasirinkite veiksmą, kurį su dokumentu turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="a3da4-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a3da4-126">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="a3da4-126">Specify when notifications are sent</span></span>

<span data-ttu-id="a3da4-127">Pranešimus žmonėms galima siųsti, kai dokumentas yra patvirtintas, atmestas, perduotas ar perskirtas arba kai reikalaujama keitimo.</span><span class="sxs-lookup"><span data-stu-id="a3da4-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="a3da4-128">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="a3da4-129">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="a3da4-130">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="a3da4-131">**Perduoti** – kai dokumentas priskiriamas tvirtinti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="a3da4-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="a3da4-132">**Perskirti** – kai priskirtas vartotojas per paskirtą laiką neatliko jokių veiksmų su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a3da4-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="a3da4-133">**Patvirtinti** – kai dokumentas buvo patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="a3da4-134">**Atmesti** – kai dokumentas buvo atmestas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="a3da4-135">**Reikalauti keitimo** – kai priskirtas vartotojas reikalauja keisti pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="a3da4-136">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="a3da4-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="a3da4-137">Spustelėkite skirtuką **Pranešimo tekstas**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="a3da4-138">Teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="a3da4-139">Norėdami tekstą personalizuoti, galite įterpti vietos rezervavimo ženklus, kurie bus pakeičiami atitinkamais duomenimis, kai jie bus pateikiami vartotojams.</span><span class="sxs-lookup"><span data-stu-id="a3da4-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="a3da4-140">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="a3da4-141">Spustelėkite teksto lauką vietoje, kurioje turėtų atsirasti vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a3da4-142">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a3da4-143">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="a3da4-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a3da4-144">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-144">Click **Insert**.</span></span>

7. <span data-ttu-id="a3da4-145">Norėdami įtraukti pranešimų vertimų, spustelėkite **Vertimai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="a3da4-146">Rodomoje formoje atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="a3da4-147">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-147">Click **Add**.</span></span>
    2. <span data-ttu-id="a3da4-148">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="a3da4-149">Teksto lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="a3da4-150">Norėdami personalizuoti tekstą, įterpkite vietos rezervavimo ženklų.</span><span class="sxs-lookup"><span data-stu-id="a3da4-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="a3da4-151">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-151">Click **Close**.</span></span>

8. <span data-ttu-id="a3da4-152">Spustelėkite skirtuką **Gavėjas**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="a3da4-153">Nurodykite, kam siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="a3da4-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="a3da4-154">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 10 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a3da4-155">Parinktis</span><span class="sxs-lookup"><span data-stu-id="a3da4-155">Option</span></span></th>
    <th><span data-ttu-id="a3da4-156">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="a3da4-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="a3da4-157">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="a3da4-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a3da4-158"><strong>Dalyvis</strong></span><span class="sxs-lookup"><span data-stu-id="a3da4-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="a3da4-159">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="a3da4-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3da4-160">Pasirinkę <strong>Dalyvis</strong> spustelėkite skirtuką <strong>Pagal vaidmenį</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3da4-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3da4-161">Sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens, kuriam bus siunčiami pranešimai, grupę.</span><span class="sxs-lookup"><span data-stu-id="a3da4-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a3da4-162">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="a3da4-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3da4-163"><strong>Darbo eigos vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="a3da4-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="a3da4-164">Dabartinėje darbo eigoje dalyvaujantys vartotojai</span><span class="sxs-lookup"><span data-stu-id="a3da4-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3da4-165">Pasirinkę <strong>Darbo eigos vartotojas</strong>, spustelėkite skirtuką <strong>Darbo eigos vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3da4-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3da4-166">Sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="a3da4-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a3da4-167"><strong>Vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="a3da4-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="a3da4-168">Konkretūs „Microsoft Dynamics 365 for Finance and Operations“ vartotojai</span><span class="sxs-lookup"><span data-stu-id="a3da4-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a3da4-169">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3da4-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="a3da4-170">Sąrašas <strong>Galimi vartotojai</strong> apima visus „Microsoft Dynamics 365 for Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="a3da4-171">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3da4-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="a3da4-172">Pakartokite veiksmus 3–9 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="a3da4-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="a3da4-173">Galutinio tvirtintojo nurodymas</span><span class="sxs-lookup"><span data-stu-id="a3da4-173">Specify a final approver</span></span>

<span data-ttu-id="a3da4-174">Galite nustatyti galutinį tvirtintoją tiems atvejams, kai tvirtintojas yra asmuo, kuris pateikė dokumentą tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a3da4-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="a3da4-175">Norėdami nurodyti galutinį tvirtintoją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-175">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="a3da4-176">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-176">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="a3da4-177">Pažymėkite žymės langelį **Naudoti galutinį tvirtintoją**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-177">Select the **Use final approver** check box.</span></span>
3. <span data-ttu-id="a3da4-178">Sąraše pasirinkite vartotoją, kuris bus galutinis tvirtintojas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="a3da4-179">Laiko limito nustatymas</span><span class="sxs-lookup"><span data-stu-id="a3da4-179">Set a time limit</span></span>

<span data-ttu-id="a3da4-180">Jei patvirtinimo procesas turi būti baigtas per tam tikrą laiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3da4-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="a3da4-181">Parinktys, kurias pasirinkote atlikdami šiuos veiksmus, gali perrašyti parinktis, kurias pasirinkote kiekvieno patvirtinimo veiksmo srityse **Priskyrimas** ir **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="a3da4-182">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="a3da4-183">Pasirinkite žymės langelį **Nustatyti darbo eigos** **elemento laiko limitą**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="a3da4-184">Lauke **Trukmė** nurodykite, kada patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="a3da4-185">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="a3da4-185">Select one of the following options:</span></span>

    - <span data-ttu-id="a3da4-186">**Valandos** – įveskite valandų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3da4-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="a3da4-187">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="a3da4-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3da4-188">**Dienos** – įveskite dienų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3da4-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="a3da4-189">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="a3da4-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="a3da4-190">**Savaitės** – įveskite savaičių, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="a3da4-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="a3da4-191">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="a3da4-192">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas trečios mėnesio savaitės penktadienį.</span><span class="sxs-lookup"><span data-stu-id="a3da4-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="a3da4-193">**Metai** – pasirinkite savaitę ir mėnesį, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="a3da4-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="a3da4-194">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas iki trečios gruodžio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="a3da4-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="a3da4-195">Jei viršijamas laiko limitas, sistema atliks veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a3da4-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="a3da4-196">Sąraše **Veiksmas** pasirinkite veiksmą, kurį turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="a3da4-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="a3da4-197">Nurodymas, kuriuos veiksmus vartotojas gali atlikti</span><span class="sxs-lookup"><span data-stu-id="a3da4-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="a3da4-198">Vartotojas turi vykdyti dokumentą, kai dokumentas yra priskirtas vartotojui patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a3da4-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="a3da4-199">Atlikite šiuos veiksmus, norėdami nurodyti, kuriuos veiksmus vartotojas gali atlikti su pateiktu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="a3da4-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="a3da4-200">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="a3da4-201">Jei norite, kad vartotojas galėtų tvirtinti dokumentą, pažymėkite žymės langelį **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="a3da4-202">Jei norite, kad vartotojas galėtų atmesti dokumentą, pažymėkite žymės langelį **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="a3da4-203">Jei norite, kad vartotojai galėtų reikalauti dokumento keitimų, pažymėkite žymės langelį **Reikalauti keitimo**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="a3da4-204">Jei norite, kad vartotojas galėtų perduoti dokumentą kitam vartotojui, pažymėkite žymės langelį **Perduoti**.</span><span class="sxs-lookup"><span data-stu-id="a3da4-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="a3da4-205">Žymės langelio **Įjungti veiksmus iš darbų sąrašo įmonės portale** naudoti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="a3da4-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="a3da4-206">Patvirtinimo veiksmų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a3da4-206">Configure the approval steps</span></span>

<span data-ttu-id="a3da4-207">Patvirtinimo procesą sudaro patvirtinimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="a3da4-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="a3da4-208">Atlikite šią procedūrą, norėdami įtraukti veiksmų į patvirtinimo procesą ir veiksmus sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="a3da4-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="a3da4-209">Darbo eigos rengyklėje dukart spustelėkite patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="a3da4-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="a3da4-210">Darbo eigos rengyklėje rodomi patvirtinimo proceso veiksmai.</span><span class="sxs-lookup"><span data-stu-id="a3da4-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="a3da4-211">Norėdami įtraukti patvirtinimo veiksmą, vilkite veiksmą iš srities **Darbo eigos elementai** į drobę.</span><span class="sxs-lookup"><span data-stu-id="a3da4-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="a3da4-212">Norėdami konfigūruoti patvirtinimo veiksmą, žr. puslapį [Patvirtinimo veiksmo konfigūravimas](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="a3da4-212">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>
