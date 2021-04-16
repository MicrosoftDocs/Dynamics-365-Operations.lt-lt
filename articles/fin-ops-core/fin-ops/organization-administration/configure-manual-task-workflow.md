---
title: Neautomatizuotų darbo eigos užduočių konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuotos užduoties ypatybes.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4be7f0ee5e487185033b7ccb9a2b0a91eb4a36c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747860"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="490c8-103">Neautomatizuotų darbo eigos užduočių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="490c8-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="490c8-104">Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuotos užduoties ypatybes.</span><span class="sxs-lookup"><span data-stu-id="490c8-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="490c8-105">Norėdami darbo eigos rengyklėje konfigūruoti neautomatizuotą užduotį, dešiniuoju pelės mygtuku spustelėkite užduotį ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="490c8-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="490c8-106">Tada naudokite šias procedūras, norėdami konfigūruoti neautomatizuotos užduoties ypatybes.</span><span class="sxs-lookup"><span data-stu-id="490c8-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="490c8-107">Užduoties pavadinimas</span><span class="sxs-lookup"><span data-stu-id="490c8-107">Name the task</span></span>

<span data-ttu-id="490c8-108">Norėdami įvesti neautomatizuotos užduoties pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="490c8-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="490c8-110">Lauke **Pavadinimas** įveskite unikalų užduoties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="490c8-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="490c8-111">Įveskite subjekto eilutę ir instrukcijas</span><span class="sxs-lookup"><span data-stu-id="490c8-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="490c8-112">Turite pateikti temos eilutę ir instrukcijas šiai užduočiai priskirtiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="490c8-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="490c8-113">Pavyzdžiui, jei konfigūruojate pirkimo paraiškų užduotį, užduočiai priskirtas vartotojas matys temos eilutę ir instrukcijas puslapyje **Pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="490c8-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="490c8-114">Temos eilutė rodoma puslapio pranešimo juostoje.</span><span class="sxs-lookup"><span data-stu-id="490c8-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="490c8-115">Tada, norėdamas peržiūrėti instrukcijas, vartotojas gali spustelėti piktogramą pranešimų juostoje.</span><span class="sxs-lookup"><span data-stu-id="490c8-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="490c8-116">Norėdami įvesti temos eilutę ir instrukcijas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="490c8-117">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="490c8-118">Lauke **Darbo elemento tema** įveskite temos eilutę.</span><span class="sxs-lookup"><span data-stu-id="490c8-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="490c8-119">Norėdami personalizuoti temos eilutę, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="490c8-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="490c8-120">Temos eilutę rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="490c8-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="490c8-121">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="490c8-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="490c8-122">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="490c8-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="490c8-123">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="490c8-124">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="490c8-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="490c8-125">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-125">Click **Insert**.</span></span>

4. <span data-ttu-id="490c8-126">Norėdami įtraukti temos eilutės vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="490c8-127">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="490c8-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="490c8-128">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="490c8-129">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="490c8-130">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="490c8-131">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 3 veiksme.</span><span class="sxs-lookup"><span data-stu-id="490c8-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="490c8-132">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-132">Click **Close**.</span></span>

5. <span data-ttu-id="490c8-133">Lauke **Darbo elemento instrukcijos** įveskite instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="490c8-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="490c8-134">Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="490c8-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="490c8-135">Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="490c8-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="490c8-136">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="490c8-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="490c8-137">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="490c8-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="490c8-138">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="490c8-139">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="490c8-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="490c8-140">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-140">Click **Insert**.</span></span>

7. <span data-ttu-id="490c8-141">Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="490c8-142">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="490c8-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="490c8-143">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="490c8-144">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="490c8-145">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="490c8-146">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 6 veiksme.</span><span class="sxs-lookup"><span data-stu-id="490c8-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="490c8-147">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="490c8-148">Užduoties priskyrimas</span><span class="sxs-lookup"><span data-stu-id="490c8-148">Assign the task</span></span>

<span data-ttu-id="490c8-149">Atlikite šiuos veiksmus, norėdami nurodyti, kam neautomatizuota užduotis turėtų būti priskirta.</span><span class="sxs-lookup"><span data-stu-id="490c8-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="490c8-150">Kairiojoje srityje spustelėkite **Priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="490c8-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="490c8-151">Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 3 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="490c8-152">Parinktis</span><span class="sxs-lookup"><span data-stu-id="490c8-152">Option</span></span></th>
    <th><span data-ttu-id="490c8-153">Vartotojai, kuriems priskirta užduotis</span><span class="sxs-lookup"><span data-stu-id="490c8-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="490c8-154">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="490c8-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="490c8-155">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="490c8-155">Participant</span></span></td>
    <td><span data-ttu-id="490c8-156">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="490c8-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-157">Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam norite priskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="490c8-158">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam norite priskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-159">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="490c8-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="490c8-160">Konkrečios organizacijos hierarchijos vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-161">Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite priskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="490c8-162">Sistema turi iš hierarchijos nuskaityti vartotojų vardus.</span><span class="sxs-lookup"><span data-stu-id="490c8-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="490c8-163">Šie vardai nurodo vartotojus, kuriems galima priskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="490c8-164">Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką.</span><span class="sxs-lookup"><span data-stu-id="490c8-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="490c8-165">Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="490c8-166">Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="490c8-167">Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</span><span class="sxs-lookup"><span data-stu-id="490c8-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="490c8-168">Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams užduotis turėtų būti priskirta.</span><span class="sxs-lookup"><span data-stu-id="490c8-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="490c8-169"><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – užduotis priskiriama visiems vartotojams diapazone.</span><span class="sxs-lookup"><span data-stu-id="490c8-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="490c8-170"><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – užduotis priskiriama tik paskutiniam vartotojui diapazone.</span><span class="sxs-lookup"><span data-stu-id="490c8-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="490c8-171"><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – užduotis nepriskiriama diapazono vartotojams, kurie atitinka tam tikrą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="490c8-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="490c8-172">Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-173">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-173">Workflow user</span></span></td>
    <td><span data-ttu-id="490c8-174">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="490c8-175">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="490c8-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-176">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-176">User</span></span></td>
    <td><span data-ttu-id="490c8-177">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-178">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="490c8-179">Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus.</span><span class="sxs-lookup"><span data-stu-id="490c8-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="490c8-180">Pasirinkite, kuriems vartotojams norite priskirti užduotį, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-181">Darbo grupė</span><span class="sxs-lookup"><span data-stu-id="490c8-181">Queue</span></span></td>
    <td><span data-ttu-id="490c8-182">Darbo elementų eilė</span><span class="sxs-lookup"><span data-stu-id="490c8-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-183">Pasirinkę <strong>Eilė</strong> spustelėkite skirtuką <strong>Pagal eilę</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="490c8-184">Norėdami priskirti užduotį konkrečiai eilei, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="490c8-185">Sąraše <strong>Eilės tipas</strong> pasirinkite <strong>Darbo elemento eilės</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="490c8-186">Sąraše <strong>Eilės pavadinimas</strong> pasirinkite eilę.</span><span class="sxs-lookup"><span data-stu-id="490c8-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="490c8-187">Jei nuo tam tikros sąlygos turi priklausyti, kuriai eilei užduotis turi būti priskirta, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="490c8-188">Sąraše <strong>Eilės tipas</strong> pasirinkite <strong>Sąlyginės darbo elemento eilės</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="490c8-189">Sąraše <strong>Eilės pavadinimas</strong> pasirinkite <strong>Sąlyginė eilė</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="490c8-190">Ši parinktis naudojama tik kelioms darbo eigoms, pvz., atvejų valdymui.</span><span class="sxs-lookup"><span data-stu-id="490c8-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="490c8-191">Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto užduočiai baigti.</span><span class="sxs-lookup"><span data-stu-id="490c8-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="490c8-192">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="490c8-192">Select one of the following options:</span></span>

    - <span data-ttu-id="490c8-193">**Valandos** – įveskite valandų, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="490c8-194">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-195">**Dienos** – įveskite dienų, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="490c8-196">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-197">**Savaitės** – įveskite savaičių, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="490c8-198">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurios vartotojas turi baigti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="490c8-199">Pavyzdžiui, galbūt norite, kad vartotojas atliktų šią užduotį iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="490c8-200">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi baigti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="490c8-201">Pavyzdžiui, galbūt norite, kad vartotojas atliktų šią užduotį iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="490c8-202">Jei per skirtąjį laiką vartotojas užduoties nebaigs, užduotis bus laikoma vėluojančia.</span><span class="sxs-lookup"><span data-stu-id="490c8-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="490c8-203">Vėluojančia laikoma užduotis yra perskiriama atsižvelgiant į parinktis, kurias pasirenkate puslapio srityje **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="490c8-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="490c8-204">Įvykių užduoties vėlavimo atveju nurodymas</span><span class="sxs-lookup"><span data-stu-id="490c8-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="490c8-205">Jei per skirtąjį laiką vartotojas neautomatizuotos užduoties nebaigs, užduotis bus laikoma vėluojančia.</span><span class="sxs-lookup"><span data-stu-id="490c8-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="490c8-206">Vėluojančią užduotį galima perskirti arba automatiškai priskirti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="490c8-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="490c8-207">Atlikite tolesnius veiksmus, kad perskirtumėte užduotį, jei ji vėluoja.</span><span class="sxs-lookup"><span data-stu-id="490c8-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="490c8-208">Kairiojoje srityje spustelėkite **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="490c8-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="490c8-209">Pasirinkite žymės langelį **Naudoti perskyrimo maršrutą**, norėdami kurti perskyrimo maršrutą.</span><span class="sxs-lookup"><span data-stu-id="490c8-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="490c8-210">Sistema automatiškai priskirs užduotį perskyrimo sąraše pateiktiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="490c8-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="490c8-211">Pavyzdžiui, tolesnėje lentelėje pateikiamas perskyrimo maršrutas.</span><span class="sxs-lookup"><span data-stu-id="490c8-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="490c8-212">Seka</span><span class="sxs-lookup"><span data-stu-id="490c8-212">Sequence</span></span> | <span data-ttu-id="490c8-213">Perskyrimo maršrutas</span><span class="sxs-lookup"><span data-stu-id="490c8-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="490c8-214">1</span><span class="sxs-lookup"><span data-stu-id="490c8-214">1</span></span>        | <span data-ttu-id="490c8-215">Priskirti: Donna</span><span class="sxs-lookup"><span data-stu-id="490c8-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="490c8-216">2</span><span class="sxs-lookup"><span data-stu-id="490c8-216">2</span></span>        | <span data-ttu-id="490c8-217">Priskirti: Erin</span><span class="sxs-lookup"><span data-stu-id="490c8-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="490c8-218">3</span><span class="sxs-lookup"><span data-stu-id="490c8-218">3</span></span>        | <span data-ttu-id="490c8-219">Galutinis veiksmas: atmesti</span><span class="sxs-lookup"><span data-stu-id="490c8-219">Final action: Reject</span></span> |

    <span data-ttu-id="490c8-220">Tokiu atveju, sistema priskirs vėluojančią užduotį Donna.</span><span class="sxs-lookup"><span data-stu-id="490c8-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="490c8-221">Jei Donna nebaigs užduoties per skirtąjį laiką, sistema priskirs užduotį Erin.</span><span class="sxs-lookup"><span data-stu-id="490c8-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="490c8-222">Jei Erin nebaigs užduoties per skirtąjį laiką, sistema atmes dokumentą, pateiktą apdoroti.</span><span class="sxs-lookup"><span data-stu-id="490c8-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="490c8-223">Norėdami vartotoją įtraukti į perskyrimo maršrutą, spustelėkite **Įtraukti perskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="490c8-224">Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 4 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="490c8-225">Parinktis</span><span class="sxs-lookup"><span data-stu-id="490c8-225">Option</span></span></th>
    <th><span data-ttu-id="490c8-226">Vartotojai, kuriems perskirta užduotis</span><span class="sxs-lookup"><span data-stu-id="490c8-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="490c8-227">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="490c8-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="490c8-228">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="490c8-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="490c8-229">Konkrečios organizacijos hierarchijos vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-230">Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite perskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="490c8-231">Sistema turi iš hierarchijos nuskaityti vartotojų vardus.</span><span class="sxs-lookup"><span data-stu-id="490c8-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="490c8-232">Šie vardai nurodo vartotojus, kuriems galima perskirti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="490c8-233">Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką.</span><span class="sxs-lookup"><span data-stu-id="490c8-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="490c8-234">Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="490c8-235">Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="490c8-236">Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</span><span class="sxs-lookup"><span data-stu-id="490c8-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="490c8-237">Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams užduotis turėtų būti perskirta.</span><span class="sxs-lookup"><span data-stu-id="490c8-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="490c8-238"><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – užduotis perskiriama visiems vartotojams diapazone.</span><span class="sxs-lookup"><span data-stu-id="490c8-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="490c8-239"><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – užduotis perskiriama tik paskutiniam vartotojui diapazone.</span><span class="sxs-lookup"><span data-stu-id="490c8-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="490c8-240"><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – ši užduotis neperskiriama diapazono vartotojams, kurie atitinka tam tikrą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="490c8-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="490c8-241">Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-242">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-242">Workflow user</span></span></td>
    <td><span data-ttu-id="490c8-243">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="490c8-244">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="490c8-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-245">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-245">User</span></span></td>
    <td><span data-ttu-id="490c8-246">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-247">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="490c8-248">Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus.</span><span class="sxs-lookup"><span data-stu-id="490c8-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="490c8-249">Pasirinkite, kuriems vartotojams norite perskirti užduotį, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="490c8-250">Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto užduočiai baigti.</span><span class="sxs-lookup"><span data-stu-id="490c8-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="490c8-251">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="490c8-251">Select one of the following options:</span></span>

    - <span data-ttu-id="490c8-252">**Valandos** – įveskite valandų, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="490c8-253">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-254">**Dienos** – įveskite dienų, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="490c8-255">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-256">**Savaitės** – įveskite savaičių, per kurias vartotojas turi baigti užduotį, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="490c8-257">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurios vartotojas turi baigti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="490c8-258">Pavyzdžiui, galbūt norite, kad vartotojas atliktų šią užduotį iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="490c8-259">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi baigti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="490c8-260">Pavyzdžiui, galbūt norite, kad vartotojas atliktų šią užduotį iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="490c8-261">Pakartokite 3 ir 4 veiksmus su kiekvienu vartotoju, kuris turėtų būti įtrauktas į perskyrimo maršrutą.</span><span class="sxs-lookup"><span data-stu-id="490c8-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="490c8-262">Galite keisti vartotojų tvarką.</span><span class="sxs-lookup"><span data-stu-id="490c8-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="490c8-263">Jei perskyrimo maršrute esantys vartotojai per skirtąjį laiką nebaigia užduoties, sistema atliks veiksmą su užduotimi.</span><span class="sxs-lookup"><span data-stu-id="490c8-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="490c8-264">Norėdami nurodyti veiksmą, kurį sistema atliks, pasirinkite eilutę **Veiksmas** ir tada skirtuke **Pabaigos veiksmas** pasirinkite veiksmą.</span><span class="sxs-lookup"><span data-stu-id="490c8-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="490c8-265">Nurodymas, kada sistema automatiškai atlieka veiksmą su užduotimi</span><span class="sxs-lookup"><span data-stu-id="490c8-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="490c8-266">Galite konfigūruoti sistemą, kad ji atliktų veiksmą su neautomatizuota užduotimi konkrečiomis sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="490c8-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="490c8-267">Pvz., užduočiai atlikti reikia, kad išlaidų ataskaitų padalinio narys peržiūrėtų gavimus, pateikiamus kartu su išlaidų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="490c8-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="490c8-268">Atsižvelgiant į įmonės strategiją, ši užduotis turi būti atlikta, jei bendroji išlaidų ataskaitos suma yra didesnė nei 100 JAV dolerių.</span><span class="sxs-lookup"><span data-stu-id="490c8-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="490c8-269">Tokiu atveju galite konfigūruoti sistemą, kad ji automatiškai pažymėtų užduotį kaip **Atlikta**, kai bendroji suma yra mažesnė nei 100.</span><span class="sxs-lookup"><span data-stu-id="490c8-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="490c8-270">Atlikite šiuos veiksmus, norėdami nurodyti, kada sistema turi atlikti veiksmą su neautomatizuota užduotimi.</span><span class="sxs-lookup"><span data-stu-id="490c8-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="490c8-271">Kairiojoje srityje spustelėkite **Automatiniai veiksmai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="490c8-272">Pažymėkite žymės langelį **Įjungti automatinius veiksmus**.</span><span class="sxs-lookup"><span data-stu-id="490c8-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="490c8-273">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="490c8-274">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="490c8-274">Enter a condition.</span></span>
5. <span data-ttu-id="490c8-275">Įveskite visas reikalingas papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="490c8-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="490c8-276">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra sukonfigūruotos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="490c8-277">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-277">Click **Test**.</span></span>
    2. <span data-ttu-id="490c8-278">Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="490c8-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="490c8-279">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-279">Click **Test**.</span></span> <span data-ttu-id="490c8-280">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="490c8-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="490c8-281">Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="490c8-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="490c8-282">Sąraše **Automatinio užbaigimo veiksmas** pasirinkite veiksmą, kurį su užduotimi turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="490c8-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="490c8-283">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="490c8-283">Specify when notifications are sent</span></span>

<span data-ttu-id="490c8-284">Pranešimus žmonėms galima siųsti, kai neautomatizuota užduotis yra perduota, perskirta, baigta ar atmesta arba kai reikalaujamas keitimas.</span><span class="sxs-lookup"><span data-stu-id="490c8-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="490c8-285">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="490c8-286">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="490c8-287">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="490c8-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="490c8-288">**Perduoti** – užduotis priskirta kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="490c8-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="490c8-289">**Perskirti** – priskirtas vartotojas nebaigė užduoties per skirtąjį laiką.</span><span class="sxs-lookup"><span data-stu-id="490c8-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="490c8-290">**Baigti** – priskirtas vartotojas užduotį baigė.</span><span class="sxs-lookup"><span data-stu-id="490c8-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="490c8-291">**Atmesti** – priskirtas vartotojas atmetė pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="490c8-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="490c8-292">**Reikalauti keitimo** – priskirtas vartotojas reikalauja keisti pateiktą dokumentą.</span><span class="sxs-lookup"><span data-stu-id="490c8-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="490c8-293">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="490c8-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="490c8-294">Skirtuko **Pranešimo tekstas** teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="490c8-295">Norėdami pranešimus pritaikyti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="490c8-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="490c8-296">Pranešimą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikra informacija.</span><span class="sxs-lookup"><span data-stu-id="490c8-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="490c8-297">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="490c8-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="490c8-298">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="490c8-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="490c8-299">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="490c8-300">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="490c8-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="490c8-301">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-301">Click **Insert**.</span></span>

6. <span data-ttu-id="490c8-302">Norėdami įtraukti pranešimų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="490c8-303">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="490c8-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="490c8-304">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="490c8-305">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="490c8-306">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="490c8-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="490c8-307">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 5 veiksme.</span><span class="sxs-lookup"><span data-stu-id="490c8-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="490c8-308">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-308">Click **Close**.</span></span>

7. <span data-ttu-id="490c8-309">Skirtuke **Gavėjas** nurodykite, kam pranešimai siunčiami.</span><span class="sxs-lookup"><span data-stu-id="490c8-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="490c8-310">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 8 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="490c8-311">Parinktis</span><span class="sxs-lookup"><span data-stu-id="490c8-311">Option</span></span></th>
    <th><span data-ttu-id="490c8-312">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="490c8-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="490c8-313">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="490c8-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="490c8-314">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="490c8-314">Participant</span></span></td>
    <td><span data-ttu-id="490c8-315">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="490c8-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-316">Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="490c8-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="490c8-317">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="490c8-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-318">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-318">Workflow user</span></span></td>
    <td><span data-ttu-id="490c8-319">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="490c8-320">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="490c8-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="490c8-321">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="490c8-321">User</span></span></td>
    <td><span data-ttu-id="490c8-322">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="490c8-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="490c8-323">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="490c8-324">Sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus.</span><span class="sxs-lookup"><span data-stu-id="490c8-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="490c8-325">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="490c8-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="490c8-326">Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="490c8-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="490c8-327">Laiko limito nustatymas</span><span class="sxs-lookup"><span data-stu-id="490c8-327">Set a time limit</span></span>

<span data-ttu-id="490c8-328">Jei neautomatizuota užduotis turi būti baigta per tam tikrą laiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="490c8-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="490c8-329">Šioje procedūroje pasirinktos parinktys gali perrašyti parinktis, kurias pasirinkote puslapio srityse **Priskyrimas** ir **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="490c8-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="490c8-330">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="490c8-331">Pasirinkite žymės langelį **Nustatyti darbo eigos elemento laiko limitą**.</span><span class="sxs-lookup"><span data-stu-id="490c8-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="490c8-332">Lauke **Trukmė** nurodykite, kada užduotis turi būti baigta.</span><span class="sxs-lookup"><span data-stu-id="490c8-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="490c8-333">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="490c8-333">Select one of the following options:</span></span>

    - <span data-ttu-id="490c8-334">**Valandos** – įveskite valandų, per kurias ši užduotis turi būti baigta, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="490c8-335">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-336">**Dienos** – įveskite dienų, per kurias užduotis turi būti baigta, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="490c8-337">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="490c8-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="490c8-338">**Savaitės** – įveskite savaičių, per kurias užduotis turi būti baigta, skaičių.</span><span class="sxs-lookup"><span data-stu-id="490c8-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="490c8-339">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių užduotis turi būti baigta.</span><span class="sxs-lookup"><span data-stu-id="490c8-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="490c8-340">Pavyzdžiui, galbūt norite, kad užduotis būtų baigta iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="490c8-341">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių užduotis turi būti baigta.</span><span class="sxs-lookup"><span data-stu-id="490c8-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="490c8-342">Pavyzdžiui, galbūt norite, kad užduotis būtų baigta iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="490c8-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="490c8-343">Jei viršijamas laiko limitas, sistema atliks veiksmą su užduotimi.</span><span class="sxs-lookup"><span data-stu-id="490c8-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="490c8-344">Sąraše **Veiksmas** pasirinkite veiksmą, kurį turi atlikti sistema.</span><span class="sxs-lookup"><span data-stu-id="490c8-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="490c8-345">Nurodymas, kuriuos veiksmus vartotojas gali atlikti</span><span class="sxs-lookup"><span data-stu-id="490c8-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="490c8-346">Vartotojas turi atlikti veiksmą su užduotimi, kai neautomatizuota užduotis yra priskirta vartotojui.</span><span class="sxs-lookup"><span data-stu-id="490c8-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="490c8-347">Atlikite šiuos veiksmus, norėdami nurodyti, kuriuos veiksmus vartotojas gali atlikti su užduotimi.</span><span class="sxs-lookup"><span data-stu-id="490c8-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="490c8-348">Galimi veiksmai skiriasi: tai priklauso nuo to, kaip užduotis sukurta.</span><span class="sxs-lookup"><span data-stu-id="490c8-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="490c8-349">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="490c8-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="490c8-350">Jei norite, kad vartotojas galėtų pažymėti užduotį kaip **Baigta**, pažymėkite žymės langelį **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="490c8-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="490c8-351">Jei norite, kad vartotojas galėtų pateiktą dokumentą atmesti, pažymėkite žymės langelį **Atmesi**.</span><span class="sxs-lookup"><span data-stu-id="490c8-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="490c8-352">Jei norite, kad vartotojas galėtų reikalauti pateikto dokumento pakeitimų, pažymėkite žymės langelį **Reikalauti keitimo**.</span><span class="sxs-lookup"><span data-stu-id="490c8-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="490c8-353">Jei norite, kad vartotojas galėtų perduoti užduotį kitam vartotojui, pažymėkite žymės langelį **Perduoti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="490c8-354">Jei norite, kad vartotojas galėtų perskirti užduotį kitam darbo elementų eilės vartotojui, pažymėkite žymės langelį **Perskirti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="490c8-355">Jei norite, kad vartotojas galėtų išleisti užduotį darbo elementų eilei, pažymėkite žymės langelį **Išleisti**.</span><span class="sxs-lookup"><span data-stu-id="490c8-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="490c8-356">Tada kitas vartotojas galės baigti užduotį.</span><span class="sxs-lookup"><span data-stu-id="490c8-356">Another user can then complete the task.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]