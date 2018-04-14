---
title: "Darbo eigos patvirtinimo proceso konfigūravimas"
description: "Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8e35b99a07d4c5eee9fae882b9d7f47ff6d63040
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="configure-an-approval-process-in-a-workflow"></a><span data-ttu-id="876ea-103">Darbo eigos patvirtinimo proceso konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="876ea-103">Configure an approval process in a workflow</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="876ea-104">Naudokite šią procedūrą, norėdami konfigūruoti patvirtinimo proceso ypatybes.</span><span class="sxs-lookup"><span data-stu-id="876ea-104">Use the following procedure to configure the properties of the approval process.</span></span>

<span data-ttu-id="876ea-105">Norėdami darbo eigos rengyklėje konfigūruoti patvirtinimo procesą, dešiniuoju pelės mygtuku spustelėkite patvirtinimo elementą ir tada spustelėkite **Ypatybės**, kad atidarytumėte formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="876ea-105">To configure an approval process, in the workflow editor, right-click the approval element, and then click **Properties** to open the **Properties** form.</span></span>
<span data-ttu-id="876ea-106">Patvirtinimo proceso pavadinimas</span><span class="sxs-lookup"><span data-stu-id="876ea-106">Name the approval process</span></span>
-------------------------

<span data-ttu-id="876ea-107">Atlikite šiuos veiksmus, jei norite įvesti patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="876ea-107">Follow these steps to enter a name for the approval process.</span></span>
1.  <span data-ttu-id="876ea-108">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-108">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="876ea-109">Lauke **Pavadinimas** įveskite unikalų patvirtinimo proceso pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="876ea-109">In the **Name** field, enter a unique name for the approval process.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a><span data-ttu-id="876ea-110">Nurodymas, kada sistema automatiškai atlieka veiksmą su dokumentu</span><span class="sxs-lookup"><span data-stu-id="876ea-110">Specify when the system automatically acts on the document</span></span>
<span data-ttu-id="876ea-111">Galite konfigūruoti sistemą, kad ji galėtų automatiškai vykdyti tam tikras sąlygas atitinkantį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="876ea-111">You can configure the system to automatically act on the document if specific conditions are met.</span></span> <span data-ttu-id="876ea-112">Pvz., sistema gali patvirtinti išlaidų ataskaitas, kurių bendrosios sumos yra mažesnės nei 100 USD.</span><span class="sxs-lookup"><span data-stu-id="876ea-112">For example, the system can approve expense reports that have total amounts that are less than USD 100.</span></span> <span data-ttu-id="876ea-113">Atlikite šiuos veiksmus, norėdami nurodyti, kada sistema turi atlikti veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="876ea-113">Follow these steps to specify when the system acts on the document.</span></span>
1.  <span data-ttu-id="876ea-114">Kairiojoje srityje spustelėkite **Automatiniai veiksmai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-114">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="876ea-115">Pažymėkite žymės langelį **Įjungti automatinius veiksmus**.</span><span class="sxs-lookup"><span data-stu-id="876ea-115">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="876ea-116">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="876ea-116">Click **Add condition**.</span></span>
4.  <span data-ttu-id="876ea-117">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="876ea-117">Enter a condition.</span></span>
5.  <span data-ttu-id="876ea-118">Jei reikia, įveskite papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="876ea-118">Enter additional conditions, if necessary.</span></span>
6.  <span data-ttu-id="876ea-119">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-119">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="876ea-120">Spustelėkite **Tikrinti**, norėdami atidaryti formą **Tikrinti darbo eigos sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="876ea-120">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="876ea-121">Formos srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="876ea-121">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="876ea-122">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-122">Click **Test**.</span></span> <span data-ttu-id="876ea-123">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="876ea-123">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="876ea-124">Spustelėkite **Gerai** arba **Atšaukti**, norėdami vėl atidaryti formą **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="876ea-124">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

7.  <span data-ttu-id="876ea-125">Sąraše **Automatinio užbaigimo veiksmas** pasirinkite veiksmą, kurį su dokumentu turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="876ea-125">In the **Auto complete action** list, select the action that the system should take on the document.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="876ea-126">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="876ea-126">Specify when notifications are sent</span></span>
<span data-ttu-id="876ea-127">Pranešimus žmonėms galima siųsti, kai dokumentas yra patvirtintas, atmestas, perduotas ar perskirtas arba kai reikalaujama keitimo.</span><span class="sxs-lookup"><span data-stu-id="876ea-127">You can send notifications to people when a document has been approved, rejected, delegated, or escalated, or when a change has been requested.</span></span> <span data-ttu-id="876ea-128">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-128">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>
1.  <span data-ttu-id="876ea-129">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-129">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="876ea-130">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="876ea-130">Select the check box next to the events to send notifications for:</span></span>
    -   <span data-ttu-id="876ea-131">**Perduoti** – kai dokumentas priskiriamas tvirtinti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="876ea-131">**Delegate** – When a document has been assigned to another user for approval.</span></span>
    -   <span data-ttu-id="876ea-132">**Perskirti** – kai priskirtas vartotojas per paskirtą laiką neatliko jokių veiksmų su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="876ea-132">**Escalate** – When the assigned user has not acted on a document in the allotted time.</span></span>
    -   <span data-ttu-id="876ea-133">**Patvirtinti** – kai dokumentas buvo patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="876ea-133">**Approve** – When a document has been approved.</span></span>
    -   <span data-ttu-id="876ea-134">**Atmesti** – kai dokumentas buvo atmestas.</span><span class="sxs-lookup"><span data-stu-id="876ea-134">**Reject** – When a document has been rejected.</span></span>
    -   <span data-ttu-id="876ea-135">**Reikalauti keitimo** – kai priskirtas vartotojas reikalauja keisti pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="876ea-135">**Request change** – When the assigned user has requested a change to a document that was submitted.</span></span>

3.  <span data-ttu-id="876ea-136">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="876ea-136">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="876ea-137">Spustelėkite skirtuką **Pranešimo tekstas**.</span><span class="sxs-lookup"><span data-stu-id="876ea-137">Click the **Notification text** tab.</span></span>
5.  <span data-ttu-id="876ea-138">Teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="876ea-138">In the text box, enter the text for the notification.</span></span>
6.  <span data-ttu-id="876ea-139">Norėdami tekstą personalizuoti, galite įterpti vietos rezervavimo ženklus, kurie bus pakeičiami atitinkamais duomenimis, kai jie bus pateikiami vartotojams.</span><span class="sxs-lookup"><span data-stu-id="876ea-139">To personalize the text, you can insert placeholders, which are replaced with the appropriate data when they are displayed to users.</span></span> <span data-ttu-id="876ea-140">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="876ea-140">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="876ea-141">Spustelėkite teksto lauką vietoje, kurioje turėtų atsirasti vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="876ea-141">Click in the text box at the location where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="876ea-142">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="876ea-142">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="876ea-143">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="876ea-143">In the list that is displayed, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="876ea-144">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-144">Click **Insert**.</span></span>

7.  <span data-ttu-id="876ea-145">Norėdami įtraukti pranešimų vertimų, spustelėkite **Vertimai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-145">To add translations of the notification, click **Translations**.</span></span> <span data-ttu-id="876ea-146">Rodomoje formoje atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-146">In the form that is displayed, follow these steps:</span></span>
    1.  <span data-ttu-id="876ea-147">Spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-147">Click **Add**.</span></span>
    2.  <span data-ttu-id="876ea-148">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="876ea-148">In the list that is displayed, select the language in which you will enter the text.</span></span>
    3.  <span data-ttu-id="876ea-149">Teksto lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="876ea-149">In the **Translated text** text box, enter the text.</span></span>
    4.  <span data-ttu-id="876ea-150">Norėdami personalizuoti tekstą, įterpkite vietos rezervavimo ženklų.</span><span class="sxs-lookup"><span data-stu-id="876ea-150">To personalize the text, insert placeholders.</span></span>
    5.  <span data-ttu-id="876ea-151">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-151">Click **Close**.</span></span>

8.  <span data-ttu-id="876ea-152">Spustelėkite skirtuką **Gavėjas**.</span><span class="sxs-lookup"><span data-stu-id="876ea-152">Click the **Recipient** tab.</span></span>
9.  <span data-ttu-id="876ea-153">Nurodykite, kam siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="876ea-153">Specify who the notifications are sent to.</span></span> <span data-ttu-id="876ea-154">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 10 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-154">Select one of the options in the following table, and then follow the additional steps for the option before you go to step 10.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="876ea-155">Parinktis</span><span class="sxs-lookup"><span data-stu-id="876ea-155">Option</span></span></th>
    <th><span data-ttu-id="876ea-156">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="876ea-156">Notification recipients</span></span></th>
    <th><span data-ttu-id="876ea-157">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="876ea-157">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="876ea-158"><strong>Dalyvis</strong></span><span class="sxs-lookup"><span data-stu-id="876ea-158"><strong>Participant</strong></span></span></td>
    <td><span data-ttu-id="876ea-159">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="876ea-159">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="876ea-160">Pasirinkę <strong>Dalyvis</strong> spustelėkite skirtuką <strong>Pagal vaidmenį</strong>.</span><span class="sxs-lookup"><span data-stu-id="876ea-160">After you select <strong>Participant</strong>, click the <strong>Role based</strong> tab.</span></span></li>
    <li><span data-ttu-id="876ea-161">Sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens, kuriam bus siunčiami pranešimai, grupę.</span><span class="sxs-lookup"><span data-stu-id="876ea-161">In the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="876ea-162">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="876ea-162">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="876ea-163"><strong>Darbo eigos vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="876ea-163"><strong>Workflow user</strong></span></span></td>
    <td><span data-ttu-id="876ea-164">Dabartinėje darbo eigoje dalyvaujantys vartotojai</span><span class="sxs-lookup"><span data-stu-id="876ea-164">Users who participate in the current workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="876ea-165">Pasirinkę <strong>Darbo eigos vartotojas</strong>, spustelėkite skirtuką <strong>Darbo eigos vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="876ea-165">After you select <strong>Workflow user</strong>, click the <strong>Workflow user</strong> tab.</span></span></li>
    <li><span data-ttu-id="876ea-166">Sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="876ea-166">In the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="876ea-167"><strong>Vartotojas</strong></span><span class="sxs-lookup"><span data-stu-id="876ea-167"><strong>User</strong></span></span></td>
    <td><span data-ttu-id="876ea-168">Konkretūs „Microsoft Dynamics 365 for Finance and Operations‟ vartotojai</span><span class="sxs-lookup"><span data-stu-id="876ea-168">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="876ea-169">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="876ea-169">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="876ea-170">Skirtukas <strong>Galimi vartotojai</strong> apima visus „Microsoft Dynamics 365 for Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="876ea-170">The <strong>Available users</strong>: list includes all Microsoft Dynamics 365 for Finance and Operations users.</span></span> <span data-ttu-id="876ea-171">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="876ea-171">Select the users to send notifications to, and then move these users to the <strong>Selected users</strong>: list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

10. <span data-ttu-id="876ea-172">Pakartokite veiksmus 3–9 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="876ea-172">Repeat steps 3 through 9 for each event that you selected in step 2.</span></span>

## <a name="specify-a-final-approver"></a><span data-ttu-id="876ea-173">Galutinio tvirtintojo nurodymas</span><span class="sxs-lookup"><span data-stu-id="876ea-173">Specify a final approver</span></span>
<span data-ttu-id="876ea-174">Galite nustatyti galutinį tvirtintoją tiems atvejams, kai tvirtintojas yra asmuo, kuris pateikė dokumentą tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="876ea-174">You may want to designate a final approver for scenarios where the approver is the person who submitted the document for approval.</span></span> <span data-ttu-id="876ea-175">Norėdami nurodyti galutinį tvirtintoją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-175">Follow these steps to specify a final approver.</span></span>
1.  <span data-ttu-id="876ea-176">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-176">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="876ea-177">Pažymėkite žymės langelį **Naudoti galutinį tvirtintoją**.</span><span class="sxs-lookup"><span data-stu-id="876ea-177">Select the **Use final approver** check box.</span></span>
3.  <span data-ttu-id="876ea-178">Sąraše pasirinkite vartotoją, kuris bus galutinis tvirtintojas.</span><span class="sxs-lookup"><span data-stu-id="876ea-178">In the list, select the user to be the final approver.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="876ea-179">Laiko limito nustatymas</span><span class="sxs-lookup"><span data-stu-id="876ea-179">Set a time limit</span></span>
<span data-ttu-id="876ea-180">Jei patvirtinimo procesas turi būti baigtas per tam tikrą laiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="876ea-180">Follow these steps if the approval process must be completed in a specific time.</span></span>

| <span data-ttu-id="876ea-181">**Pastaba.**</span><span class="sxs-lookup"><span data-stu-id="876ea-181">**Note**</span></span>                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="876ea-182">Parinktys, kurias pasirinkote atlikdami šiuos veiksmus, gali perrašyti parinktis, kurias pasirinkote kiekvieno patvirtinimo veiksmo srityse **Priskyrimas** ir **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="876ea-182">The options that you select in these steps override the options that you selected in the **Assignment** and **Escalation** areas of each approval step.</span></span> |

1.  <span data-ttu-id="876ea-183">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-183">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="876ea-184">Pasirinkite žymės langelį **Nustatyti darbo eigos** **elemento laiko limitą**.</span><span class="sxs-lookup"><span data-stu-id="876ea-184">Select the **Set a time limit for the workflow** **element** check box.</span></span>
3.  <span data-ttu-id="876ea-185">Lauke **Trukmė** nurodykite, kada patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="876ea-185">In the **Duration** field, specify when the approval process must be completed.</span></span> <span data-ttu-id="876ea-186">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="876ea-186">Select one of the following options:</span></span>
    -   <span data-ttu-id="876ea-187">**Valandos** – įveskite valandų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="876ea-187">**Hours** – Enter the number of hours in which the approval process must be completed.</span></span> <span data-ttu-id="876ea-188">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="876ea-188">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="876ea-189">**Dienos** – įveskite dienų, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="876ea-189">**Days** – Enter the number of days in which the approval process must be completed.</span></span> <span data-ttu-id="876ea-190">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="876ea-190">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="876ea-191">**Savaitės** – įveskite savaičių, per kurias patvirtinimo procesas turi būti baigtas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="876ea-191">**Weeks** – Enter the number of weeks in which the approval process must be completed.</span></span>
    -   <span data-ttu-id="876ea-192">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="876ea-192">**Months** – Select the day and week by which the approval process must be completed.</span></span> <span data-ttu-id="876ea-193">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas trečios mėnesio savaitės penktadienį.</span><span class="sxs-lookup"><span data-stu-id="876ea-193">For example, you may want the approval process to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="876ea-194">**Metai** – pasirinkite savaitę ir mėnesį, iki kurių patvirtinimo procesas turi būti baigtas.</span><span class="sxs-lookup"><span data-stu-id="876ea-194">**Years** – Select the day, week, and month by which the approval process must be completed.</span></span> <span data-ttu-id="876ea-195">Pavyzdžiui, galite norėti, kad patvirtinimo procesas būtų atliktas iki trečios gruodžio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="876ea-195">For example, you may want the approval process to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="876ea-196">Jei viršijamas laiko limitas, sistema atliks veiksmą su dokumentu.</span><span class="sxs-lookup"><span data-stu-id="876ea-196">If the time limit is exceeded, the system acts on the document.</span></span> <span data-ttu-id="876ea-197">Sąraše **Veiksmas** pasirinkite veiksmą, kurį turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="876ea-197">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="876ea-198">Nurodymas, kuriuos veiksmus vartotojas gali atlikti</span><span class="sxs-lookup"><span data-stu-id="876ea-198">Specify which actions are available to the user</span></span>
<span data-ttu-id="876ea-199">Vartotojas turi vykdyti dokumentą, kai dokumentas yra priskirtas vartotojui patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="876ea-199">When a document is assigned to a user for approval, the user must act on the document.</span></span> <span data-ttu-id="876ea-200">Atlikite šiuos veiksmus, norėdami nurodyti, kuriuos veiksmus vartotojas gali atlikti su pateiktu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="876ea-200">Follows these steps to specify which actions the user can take on the document that was submitted.</span></span>
1.  <span data-ttu-id="876ea-201">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="876ea-201">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="876ea-202">Jei norite, kad vartotojas galėtų tvirtinti dokumentą, pažymėkite žymės langelį **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-202">Select the **Approve** check box if the user can approve the document.</span></span>
3.  <span data-ttu-id="876ea-203">Jei norite, kad vartotojas galėtų atmesti dokumentą, pažymėkite žymės langelį **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-203">Select the **Reject** check box the user can reject the document.</span></span>
4.  <span data-ttu-id="876ea-204">Jei norite, kad vartotojai galėtų reikalauti dokumento keitimų, pažymėkite žymės langelį **Reikalauti keitimo**.</span><span class="sxs-lookup"><span data-stu-id="876ea-204">Select the **Request change** check box the user can request changes to the document.</span></span>
5.  <span data-ttu-id="876ea-205">Jei norite, kad vartotojas galėtų perduoti dokumentą kitam vartotojui, pažymėkite žymės langelį **Perduoti**.</span><span class="sxs-lookup"><span data-stu-id="876ea-205">Select the **Delegate** check box if the user can assign the document to another user for approval.</span></span>

<span data-ttu-id="876ea-206">**Pastaba**: žymės langelio **Įjungti veiksmus iš darbų sąrašo įmonės portale** naudoti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="876ea-206">**Note**: The **Enable actions from the work list in Enterprise Portal** check box has been deprecated.</span></span>

## <a name="configure-the-approval-steps"></a><span data-ttu-id="876ea-207">Patvirtinimo veiksmų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="876ea-207">Configure the approval steps</span></span>
<span data-ttu-id="876ea-208">Patvirtinimo procesą sudaro patvirtinimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="876ea-208">An approval process consists of approval steps.</span></span> <span data-ttu-id="876ea-209">Atlikite šią procedūrą, norėdami įtraukti veiksmų į patvirtinimo procesą ir veiksmus sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="876ea-209">Complete the following procedure to add steps the approval process and configure the steps.</span></span>
1.  <span data-ttu-id="876ea-210">Darbo eigos rengyklėje dukart spustelėkite patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="876ea-210">In the workflow editor, double-click the approval process.</span></span> <span data-ttu-id="876ea-211">Darbo eigos rengyklėje rodomi patvirtinimo proceso veiksmai.</span><span class="sxs-lookup"><span data-stu-id="876ea-211">The workflow editor displays the steps of the approval process.</span></span>
2.  <span data-ttu-id="876ea-212">Norėdami įtraukti patvirtinimo veiksmą, vilkite veiksmą iš srities **Darbo eigos elementai** į drobę.</span><span class="sxs-lookup"><span data-stu-id="876ea-212">To add an approval step, drag the step from the **Workflow elements** area to the canvas.</span></span>
3.  <span data-ttu-id="876ea-213">Norėdami konfigūruoti patvirtinimo veiksmą, žr. puslapį [Patvirtinimo veiksmo konfigūravimas](configure-approval-step-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="876ea-213">To configure an approval step, see [Configure an approval step](configure-approval-step-workflow.md).</span></span>






