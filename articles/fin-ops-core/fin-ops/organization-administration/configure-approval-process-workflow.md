---
title: Darbo eigos patvirtinimo procesų konfigūravimas
description: Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
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
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 927a41f39e9ba9c05a7af0b962972168afa7a1ea
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698296"
---
# <a name="configure-approval-processes-in-a-workflow"></a><span data-ttu-id="5fed1-103">Darbo eigos patvirtinimo procesų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5fed1-103">Configure approval processes in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fed1-104">Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.</span><span class="sxs-lookup"><span data-stu-id="5fed1-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="5fed1-105">Norėdami darbo eigos rengyklėje konfigūruoti patvirtinimo procesą, dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-the-approval-process"></a><span data-ttu-id="5fed1-106">Patvirtinimo proceso pavadinimas</span><span class="sxs-lookup"><span data-stu-id="5fed1-106">Name the approval process</span></span>

<span data-ttu-id="5fed1-107">Atlikite šiuos veiksmus, jei norite įvesti patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-107">Follow these steps to enter a name for the approval process.</span></span>

1. <span data-ttu-id="5fed1-108">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-108">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5fed1-109">Lauke **Pavadinimas** įveskite unikalų patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="5fed1-110">Nurodymas, kada sistema automatiškai atlieka veiksmą su dokumentu</span><span class="sxs-lookup"><span data-stu-id="5fed1-110">Specify when the system automatically acts on the document</span></span>

<span data-ttu-id="5fed1-111">Galite konfigūruoti sistemą, kad ji galėtų automatiškai vykdyti tam tikras sąlygas atitinkantį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="5fed1-112">Pvz., sistema gali patvirtinti išlaidų ataskaitas, kurių bendrosios sumos yra mažesnės nei 100 USD.</span><span class="sxs-lookup"><span data-stu-id="5fed1-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="5fed1-113">Atlikite šiuos veiksmus, norėdami nurodyti, kada sistema turi atlikti veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5fed1-113">Follow these steps to specify when the system acts on the document.</span></span>

1. <span data-ttu-id="5fed1-114">Kairiojoje srityje spustelėkite **Automatiniai veiksmai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-114">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="5fed1-115">Pažymėkite žymės langelį **Įjungti automatinius veiksmus**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-115">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="5fed1-116">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-116">Click **Add condition**.</span></span>
4. <span data-ttu-id="5fed1-117">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="5fed1-117">Enter a condition.</span></span>
5. <span data-ttu-id="5fed1-118">Jei reikia, įveskite papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-118">Enter additional conditions, if necessary.</span></span>
6. <span data-ttu-id="5fed1-119">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="5fed1-120">Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="5fed1-121">Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-121">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="5fed1-122">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-122">Click **Test**.</span></span> <span data-ttu-id="5fed1-123">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="5fed1-124">Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7. <span data-ttu-id="5fed1-125">Sąraše **Automatinio užbaigimo veiksmas** pasirinkite veiksmą, kurį su dokumentu turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="5fed1-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="5fed1-126">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="5fed1-126">Specify when notifications are sent</span></span>

<span data-ttu-id="5fed1-127">Pranešimus žmonėms galima siųsti, kai dokumentas yra patvirtintas, atmestas, perduotas ar perskirtas arba kai reikalaujama keitimo.</span><span class="sxs-lookup"><span data-stu-id="5fed1-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="5fed1-128">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="5fed1-129">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-129">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="5fed1-130">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-130">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="5fed1-131">**Perduoti** – kai dokumentas priskiriamas tvirtinti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="5fed1-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    - <span data-ttu-id="5fed1-132">**Perskirti** – kai priskirtas vartotojas per paskirtą laiką neatliko jokių veiksmų su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5fed1-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    - <span data-ttu-id="5fed1-133">**Patvirtinti** – kai dokumentas buvo patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-133">**Approve** – When a document has been approved.</span></span>
    - <span data-ttu-id="5fed1-134">**Atmesti** – kai dokumentas buvo atmestas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-134">**Reject** – When a document has been rejected.</span></span>
    - <span data-ttu-id="5fed1-135">**Reikalauti keitimo** – kai priskirtas vartotojas reikalauja keisti pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3. <span data-ttu-id="5fed1-136">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="5fed1-136">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="5fed1-137">Spustelėkite skirtuką **Pranešimo tekstas**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-137">Click the **Notification text** tab.</span></span>
5. <span data-ttu-id="5fed1-138">Teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-138">In the text box, enter the text for the notification.</span></span>
6. <span data-ttu-id="5fed1-139">Norėdami tekstą personalizuoti, galite įterpti vietos rezervavimo ženklus, kurie bus pakeičiami atitinkamais duomenimis, kai jie bus pateikiami vartotojams.</span><span class="sxs-lookup"><span data-stu-id="5fed1-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="5fed1-140">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-140">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="5fed1-141">Spustelėkite teksto lauką vietoje, kurioje turėtų atsirasti vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5fed1-142">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-142">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5fed1-143">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="5fed1-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5fed1-144">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-144">Click **Insert**.</span></span>

7. <span data-ttu-id="5fed1-145">Norėdami įtraukti pranešimų vertimų, spustelėkite **Vertimai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="5fed1-146">Rodomoje formoje atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-146">In the form that is displayed, follow these steps:</span></span>

    1. <span data-ttu-id="5fed1-147">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-147">Click **Add**.</span></span>
    2. <span data-ttu-id="5fed1-148">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3. <span data-ttu-id="5fed1-149">Teksto lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-149">In the **Translated text** text box, enter the text.</span></span>
    4. <span data-ttu-id="5fed1-150">Norėdami personalizuoti tekstą, įterpkite vietos rezervavimo ženklų.</span><span class="sxs-lookup"><span data-stu-id="5fed1-150">To personalize the text, insert placeholders.</span></span>
    5. <span data-ttu-id="5fed1-151">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-151">Click **Close**.</span></span>

8. <span data-ttu-id="5fed1-152">Spustelėkite skirtuką **Gavėjas**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-152">Click the **Recipient** tab.</span></span>
9. <span data-ttu-id="5fed1-153">Nurodykite, kam siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="5fed1-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="5fed1-154">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 10 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5fed1-155">Parinktis</span><span class="sxs-lookup"><span data-stu-id="5fed1-155">Option</span></span></th>
    <th><span data-ttu-id="5fed1-156">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="5fed1-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="5fed1-157">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="5fed1-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5fed1-158"><strong>Dalyvis</strong></span><span class="sxs-lookup"><span data-stu-id="5fed1-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="5fed1-159">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="5fed1-159">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5fed1-160">Pasirinkę <strong>Dalyvis</strong> spustelėkite skirtuką <strong>Pagal vaidmenį</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fed1-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="5fed1-161">Sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens, kuriam bus siunčiami pranešimai, grupę.</span><span class="sxs-lookup"><span data-stu-id="5fed1-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="5fed1-162">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="5fed1-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5fed1-163"><strong>Darbo eigos vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="5fed1-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="5fed1-164">Dabartinėje darbo eigoje dalyvaujantys vartotojai</span><span class="sxs-lookup"><span data-stu-id="5fed1-164">Users who participate in the current workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5fed1-165">Pasirinkę <strong>Darbo eigos vartotojas</strong>, spustelėkite skirtuką <strong>Darbo eigos vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fed1-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="5fed1-166">Sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="5fed1-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5fed1-167"><strong>Vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="5fed1-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="5fed1-168">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="5fed1-168">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5fed1-169">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fed1-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5fed1-170">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="5fed1-170">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="5fed1-171">Pakartokite veiksmus 3–9 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="5fed1-171">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="5fed1-172">Galutinio tvirtintojo nurodymas</span><span class="sxs-lookup"><span data-stu-id="5fed1-172">Specify a final approver</span></span>

<span data-ttu-id="5fed1-173">Galite nurodyti galutinį scenarijų, kuriuose tvirtintojas yra asmuo, pateikęs dokumentą patvirtinimui, ir naudojamas „Neleisti tvirtinti pateikėjui“, tvirtintoją.</span><span class="sxs-lookup"><span data-stu-id="5fed1-173">You can designate a final approver for scenarios where the approver is the person who submitted the document for approval and the "disallow approval by submitter" is being used.</span></span> <span data-ttu-id="5fed1-174">Norėdami nurodyti galutinį tvirtintoją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-174">Follow these steps to specify a final approver.</span></span>

1. <span data-ttu-id="5fed1-175">Darbo eigos rengyklėje dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą, tada pasirinkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-175">In the workflow editor, right-click the approval element, and then select **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="5fed1-176">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-176">In the left pane, click **Advanced settings**.</span></span>
3. <span data-ttu-id="5fed1-177">Pažymėkite žymės langelį **Naudoti galutinį tvirtintoją**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-177">Select the **Use final approver** check box.</span></span>
4. <span data-ttu-id="5fed1-178">Sąraše pasirinkite vartotoją, kuris bus galutinis tvirtintojas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-178">In the list, select a user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="5fed1-179">Laiko limito nustatymas</span><span class="sxs-lookup"><span data-stu-id="5fed1-179">Set a time limit</span></span>

<span data-ttu-id="5fed1-180">Jei patvirtinimo procesas turi būti baigtas per tam tikrą laiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fed1-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="5fed1-181">Parinktys, kurias pasirinkote atlikdami šiuos veiksmus, gali perrašyti parinktis, kurias pasirinkote kiekvieno patvirtinimo veiksmo srityse **Priskyrimas** ir **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-181">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span>

1. <span data-ttu-id="5fed1-182">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-182">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="5fed1-183">Pasirinkite žymės langelį **Nustatyti darbo eigos** **elemento laiko limitą**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-183">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3. <span data-ttu-id="5fed1-184">Lauke **Trukmė** nurodykite, kada patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-184">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="5fed1-185">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="5fed1-185">Select one of the following options:</span></span>

    - <span data-ttu-id="5fed1-186">**Valandos** – įveskite valandų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="5fed1-186">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="5fed1-187">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="5fed1-187">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5fed1-188">**Dienos** – įveskite dienų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="5fed1-188">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="5fed1-189">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="5fed1-189">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5fed1-190">**Savaitės** – įveskite savaičių, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="5fed1-190">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    - <span data-ttu-id="5fed1-191">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-191">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="5fed1-192">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas trečios mėnesio savaitės penktadienį.</span><span class="sxs-lookup"><span data-stu-id="5fed1-192">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5fed1-193">**Metai** – pasirinkite savaitę ir mėnesį, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="5fed1-193">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="5fed1-194">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas iki trečios gruodžio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="5fed1-194">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="5fed1-195">Jei viršijamas laiko limitas, sistema atliks veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5fed1-195">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="5fed1-196">Sąraše **Veiksmas** pasirinkite veiksmą, kurį turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="5fed1-196">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="5fed1-197">Nurodymas, kuriuos veiksmus vartotojas gali atlikti</span><span class="sxs-lookup"><span data-stu-id="5fed1-197">Specify which actions are available to the user</span></span>

<span data-ttu-id="5fed1-198">Vartotojas turi vykdyti dokumentą, kai dokumentas yra priskirtas vartotojui patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="5fed1-198">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="5fed1-199">Atlikite šiuos veiksmus, norėdami nurodyti, kuriuos veiksmus vartotojas gali atlikti su pateiktu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5fed1-199">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>

1. <span data-ttu-id="5fed1-200">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-200">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="5fed1-201">Jei norite, kad vartotojas galėtų tvirtinti dokumentą, pažymėkite žymės langelį **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-201">Select the **Approve** check box if the user can approve the document.</span></span>
3. <span data-ttu-id="5fed1-202">Jei norite, kad vartotojas galėtų atmesti dokumentą, pažymėkite žymės langelį **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-202">Select the **Reject** check box the user can reject the document.</span></span>
4. <span data-ttu-id="5fed1-203">Jei norite, kad vartotojai galėtų reikalauti dokumento keitimų, pažymėkite žymės langelį **Reikalauti keitimo**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-203">Select the **Request change** check box the user can request changes to the document.</span></span>
5. <span data-ttu-id="5fed1-204">Jei norite, kad vartotojas galėtų perduoti dokumentą kitam vartotojui, pažymėkite žymės langelį **Perduoti**.</span><span class="sxs-lookup"><span data-stu-id="5fed1-204">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

> [!NOTE]
> <span data-ttu-id="5fed1-205">Žymės langelio **Įjungti veiksmus iš darbų sąrašo įmonės portale** naudoti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="5fed1-205">The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="5fed1-206">Patvirtinimo veiksmų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5fed1-206">Configure the approval steps</span></span>

<span data-ttu-id="5fed1-207">Patvirtinimo procesą sudaro patvirtinimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="5fed1-207">An approval process consists of approval steps.</span></span> <span data-ttu-id="5fed1-208">Atlikite šią procedūrą, norėdami įtraukti veiksmų į patvirtinimo procesą ir veiksmus sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="5fed1-208">Complete the following procedure to add steps the approval process and configure the steps.</span></span>

1. <span data-ttu-id="5fed1-209">Darbo eigos rengyklėje dukart spustelėkite patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="5fed1-209">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="5fed1-210">Darbo eigos rengyklėje rodomi patvirtinimo proceso veiksmai.</span><span class="sxs-lookup"><span data-stu-id="5fed1-210">The workflow editor displays the steps of the approval process.</span></span>
2. <span data-ttu-id="5fed1-211">Norėdami įtraukti patvirtinimo veiksmą, vilkite veiksmą iš srities **Darbo eigos elementai** į drobę.</span><span class="sxs-lookup"><span data-stu-id="5fed1-211">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3. <span data-ttu-id="5fed1-212">Norėdami konfigūruoti patvirtinimo veiksmą, žr. [Patvirtinimo veiksmų konfigūravimas darbo eigoje](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="5fed1-212">To configure an approval step, see [Configure approval steps in a workflow](configure-approval-step-workflow.md).</span></span>
