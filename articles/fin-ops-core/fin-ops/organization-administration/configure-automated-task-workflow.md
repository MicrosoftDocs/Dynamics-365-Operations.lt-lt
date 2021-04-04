---
title: Automatizuotų darbo eigos užduočių konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b63a9a99c442b0fbe971bc2e8f05fc8c09ec3087
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567491"
---
# <a name="configure-automated-tasks-in-a-workflow"></a><span data-ttu-id="c655c-103">Automatizuotų darbo eigos užduočių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c655c-103">Configure automated tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c655c-104">Šioje temoje paaiškinama, kaip konfigūruoti automatizuotos užduoties ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c655c-104">This topic explains how to configure the properties for an automated task.</span></span>

<span data-ttu-id="c655c-105">Norėdami darbo eigos rengyklėje konfigūruoti automatizuotą užduotį, dešiniuoju pelės mygtuku spustelėkite užduotį ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="c655c-105">To configure an automated task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c655c-106">Tada naudokite šias procedūras, norėdami konfigūruoti automatizuotos užduoties ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c655c-106">Then use the following procedures to configure the properties for the automated task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="c655c-107">Užduoties pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c655c-107">Name the task</span></span>

<span data-ttu-id="c655c-108">Norėdami įvesti automatizuotos užduoties pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c655c-108">Follow these steps to enter a name for the automated task.</span></span>

1. <span data-ttu-id="c655c-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c655c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c655c-110">Lauke **Pavadinimas** įveskite unikalų užduoties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c655c-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c655c-111">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="c655c-111">Specify when notifications are sent</span></span>

<span data-ttu-id="c655c-112">Galite siųsti pranešimus žmonėms, kai automatizuota užduotis buvo vykdoma arba atšaukta.</span><span class="sxs-lookup"><span data-stu-id="c655c-112">You can send notifications to people when an automated task has been run or canceled.</span></span> <span data-ttu-id="c655c-113">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c655c-113">Follow these steps to specify when notifications are sent, and who they are sent to.</span></span>

1. <span data-ttu-id="c655c-114">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="c655c-114">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c655c-115">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="c655c-115">Select the check box next to the events to send notifications for:</span></span>

    - <span data-ttu-id="c655c-116">**Vykdymas** – pranešimai siunčiami užduotį vykdant.</span><span class="sxs-lookup"><span data-stu-id="c655c-116">**Execution** – Notifications are sent when the task has been run.</span></span>
    - <span data-ttu-id="c655c-117">**Atšaukimas** – pranešimai siunčiami užduotį atšaukus.</span><span class="sxs-lookup"><span data-stu-id="c655c-117">**Canceled** – Notifications are sent when the task has been canceled.</span></span>

3. <span data-ttu-id="c655c-118">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="c655c-118">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c655c-119">Skirtuko **Pranešimo tekstas** teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="c655c-119">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="c655c-120">Norėdami pranešimus pritaikyti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="c655c-120">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="c655c-121">Pranešimą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="c655c-121">Placeholders are replaced with appropriate data when the notification is shown to users.</span></span> <span data-ttu-id="c655c-122">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="c655c-122">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="c655c-123">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="c655c-123">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c655c-124">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="c655c-124">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c655c-125">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="c655c-125">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c655c-126">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="c655c-126">Click **Insert**.</span></span>

6. <span data-ttu-id="c655c-127">Norėdami įtraukti pranešimų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c655c-127">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="c655c-128">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="c655c-128">Click **Translations**.</span></span>
    2. <span data-ttu-id="c655c-129">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="c655c-129">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c655c-130">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="c655c-130">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="c655c-131">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="c655c-131">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c655c-132">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 5 veiksme.</span><span class="sxs-lookup"><span data-stu-id="c655c-132">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="c655c-133">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="c655c-133">Click **Close**.</span></span>

7. <span data-ttu-id="c655c-134">Skirtuke **Gavėjas** nurodykite, kam pranešimai siunčiami.</span><span class="sxs-lookup"><span data-stu-id="c655c-134">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="c655c-135">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 8 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c655c-135">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c655c-136">Parinktis</span><span class="sxs-lookup"><span data-stu-id="c655c-136">Option</span></span></th>
    <th><span data-ttu-id="c655c-137">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="c655c-137">Notification recipients</span></span></th>
    <th><span data-ttu-id="c655c-138">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="c655c-138">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c655c-139">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="c655c-139">Participant</span></span></td>
    <td><span data-ttu-id="c655c-140">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="c655c-140">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c655c-141">Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="c655c-141">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c655c-142">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="c655c-142">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c655c-143">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="c655c-143">Workflow user</span></span></td>
    <td><span data-ttu-id="c655c-144">Dabartinėje darbo eigoje dalyvaujantys vartotojai</span><span class="sxs-lookup"><span data-stu-id="c655c-144">Users who participate in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="c655c-145">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="c655c-145">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c655c-146">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="c655c-146">User</span></span></td>
    <td><span data-ttu-id="c655c-147">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="c655c-147">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c655c-148">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c655c-148">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c655c-149">Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus.</span><span class="sxs-lookup"><span data-stu-id="c655c-149">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c655c-150">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="c655c-150">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="c655c-151">Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="c655c-151">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]