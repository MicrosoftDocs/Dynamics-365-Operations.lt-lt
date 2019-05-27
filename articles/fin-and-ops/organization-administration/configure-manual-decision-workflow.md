---
title: Neautomatinių darbo eigos sprendimų konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuoto sprendimo ypatybes.
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
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569364"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="03dae-103">Neautomatinių darbo eigos sprendimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="03dae-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03dae-104">Šioje temoje paaiškinama, kaip konfigūruoti neautomatizuoto sprendimo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="03dae-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="03dae-105">Norėdami darbo eigos rengyklėje konfigūruoti neautomatizuotą sprendimą, dešiniuoju pelės mygtuku spustelėkite neautomatizuotą sprendimą ir tada spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="03dae-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="03dae-106">Tada naudokite šias procedūras, norėdami konfigūruoti neautomatizuoto sprendimo ypatybes.</span><span class="sxs-lookup"><span data-stu-id="03dae-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="03dae-107">Sprendimo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="03dae-107">Name the decision</span></span>

<span data-ttu-id="03dae-108">Norėdami įvesti neautomatizuoto sprendimo pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="03dae-109">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="03dae-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="03dae-110">Lauke **Pavadinimas** įveskite unikalų neautomatizuoto sprendimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="03dae-111">Įveskite subjekto eilutę ir instrukcijas</span><span class="sxs-lookup"><span data-stu-id="03dae-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="03dae-112">Turite pateikti temos eilutę ir instrukcijas prie šio neautomatizuoto sprendimo priskirtiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="03dae-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="03dae-113">Pavyzdžiui, jei konfigūruojate pirkimo paraiškų sprendimą, sprendimui priskirtas vartotojas matys temos eilutę ir instrukcijas puslapyje **Pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="03dae-114">Temos eilutė rodoma puslapio pranešimo juostoje.</span><span class="sxs-lookup"><span data-stu-id="03dae-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="03dae-115">Tada, norėdamas peržiūrėti instrukcijas, vartotojas gali spustelėti piktogramą pranešimų juostoje.</span><span class="sxs-lookup"><span data-stu-id="03dae-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="03dae-116">Norėdami įvesti temos eilutę ir instrukcijas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="03dae-117">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="03dae-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="03dae-118">Skirtuko **Instrukcijos** lauke **Darbo elemento tema** įveskite temos eilutę.</span><span class="sxs-lookup"><span data-stu-id="03dae-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="03dae-119">Norėdami personalizuoti temos eilutę, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="03dae-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="03dae-120">Temos eilutę rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="03dae-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="03dae-121">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="03dae-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="03dae-122">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="03dae-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="03dae-123">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="03dae-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="03dae-124">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="03dae-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="03dae-125">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-125">Click **Insert**.</span></span>

4. <span data-ttu-id="03dae-126">Norėdami įtraukti temos eilutės vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="03dae-127">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="03dae-128">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="03dae-129">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="03dae-130">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="03dae-131">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 3 veiksme.</span><span class="sxs-lookup"><span data-stu-id="03dae-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="03dae-132">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-132">Click **Close**.</span></span>

5. <span data-ttu-id="03dae-133">Lauke **Darbo elemento instrukcijos** įveskite instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="03dae-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="03dae-134">Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="03dae-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="03dae-135">Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="03dae-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="03dae-136">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="03dae-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="03dae-137">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="03dae-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="03dae-138">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="03dae-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="03dae-139">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="03dae-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="03dae-140">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-140">Click **Insert**.</span></span>

7. <span data-ttu-id="03dae-141">Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="03dae-142">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="03dae-143">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="03dae-144">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="03dae-145">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="03dae-146">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 6 veiksme.</span><span class="sxs-lookup"><span data-stu-id="03dae-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="03dae-147">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="03dae-148">Nurodyti galimus sprendimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="03dae-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="03dae-149">Paprastai, kai dokumentas priskiriamas sprendimų priėmėjui, sprendimų priėmėjui užduodamas klausimas.</span><span class="sxs-lookup"><span data-stu-id="03dae-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="03dae-150">Atsakymas į šį klausimą paprastai yra **Taip** arba **Ne**, arba **Teisinga** arba **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="03dae-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="03dae-151">Atlikite šiuos veiksmus, norėdami nurodyti galimus neautomatizuoto sprendimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="03dae-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="03dae-152">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="03dae-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="03dae-153">Skirtuko **Rezultatai** lauke **1 rezultatas** įveskite rezultato pavadinimą arba parinktį.</span><span class="sxs-lookup"><span data-stu-id="03dae-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="03dae-154">Norėdami įtraukti rezultato vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="03dae-155">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="03dae-156">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="03dae-157">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="03dae-158">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="03dae-159">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-159">Click **Close**.</span></span>

4. <span data-ttu-id="03dae-160">Lauke **2 rezultatas** įveskite rezultato pavadinimą arba parinktį.</span><span class="sxs-lookup"><span data-stu-id="03dae-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="03dae-161">Norėdami įtraukti rezultato vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="03dae-162">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="03dae-163">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="03dae-164">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="03dae-165">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="03dae-166">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="03dae-167">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="03dae-167">Specify when notifications are sent</span></span>

<span data-ttu-id="03dae-168">Pranešimus žmonėms galima siųsti, kai sprendimas atliekamas, perduodamas arba perskiriamas.</span><span class="sxs-lookup"><span data-stu-id="03dae-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="03dae-169">Norėdami nustatyti, kada ir kam turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="03dae-170">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="03dae-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="03dae-171">Pažymėkite žymės langelį, esantį šalia įvykių, kuriems įvykus norite siųsti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="03dae-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="03dae-172">**\[1 pasirinkimas\]** – priskirtas vartotojas pasirinko **\[1 pasirinkimas\]**.</span><span class="sxs-lookup"><span data-stu-id="03dae-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="03dae-173">**\[2 pasirinkimas\]** – priskirtas vartotojas pasirinko **\[2 pasirinkimas\]**.</span><span class="sxs-lookup"><span data-stu-id="03dae-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="03dae-174">**Perduoti** – priskirtas vartotojas priskyrė sprendimą kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="03dae-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="03dae-175">**Perskirti** – priskirtas vartotojas sprendimo nepriėmė per skirtąjį laiką.</span><span class="sxs-lookup"><span data-stu-id="03dae-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="03dae-176">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="03dae-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="03dae-177">Skirtuko **Pranešimo tekstas** teksto lauke įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="03dae-178">Norėdami pranešimus pritaikyti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="03dae-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="03dae-179">Pranešimą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="03dae-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="03dae-180">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="03dae-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="03dae-181">Teksto lauke spustelėkite vietą, kurioje vietos rezervavimo ženklas turėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="03dae-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="03dae-182">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="03dae-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="03dae-183">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="03dae-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="03dae-184">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-184">Click **Insert**.</span></span>

6. <span data-ttu-id="03dae-185">Norėdami įtraukti pranešimų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="03dae-186">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="03dae-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="03dae-187">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="03dae-188">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="03dae-189">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="03dae-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="03dae-190">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus, kaip aprašyta 5 veiksme.</span><span class="sxs-lookup"><span data-stu-id="03dae-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="03dae-191">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="03dae-191">Click **Close**.</span></span>

7. <span data-ttu-id="03dae-192">Skirtuke **Gavėjas** nurodykite, kam pranešimai siunčiami.</span><span class="sxs-lookup"><span data-stu-id="03dae-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="03dae-193">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 8 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="03dae-194">Parinktis</span><span class="sxs-lookup"><span data-stu-id="03dae-194">Option</span></span></th>
    <th><span data-ttu-id="03dae-195">Pranešimo gavėjai</span><span class="sxs-lookup"><span data-stu-id="03dae-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="03dae-196">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="03dae-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="03dae-197">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="03dae-197">Participant</span></span></td>
    <td><span data-ttu-id="03dae-198">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="03dae-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-199">Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="03dae-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="03dae-200">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="03dae-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-201">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-201">Workflow user</span></span></td>
    <td><span data-ttu-id="03dae-202">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="03dae-203">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="03dae-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-204">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-204">User</span></span></td>
    <td><span data-ttu-id="03dae-205">Konkretūs „Microsoft Dynamics 365 for Finance and Operations“ vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-206">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dae-207">Skirtukas <strong>Galimi vartotojai</strong> apima visus „Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="03dae-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="03dae-208">Pasirinkite, kuriems bus siunčiami pranešimai, ir tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="03dae-209">Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="03dae-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="03dae-210">Sprendimo priskyrimas</span><span class="sxs-lookup"><span data-stu-id="03dae-210">Assign a decision</span></span>

<span data-ttu-id="03dae-211">Atlikite šiuos veiksmus, norėdami nurodyti, kam neautomatizuotas sprendimas turėtų būti priskirtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="03dae-212">Kairiojoje srityje spustelėkite **Priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="03dae-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="03dae-213">Skirtuke **Priskyrimo tipas** pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 3 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="03dae-214">Parinktis</span><span class="sxs-lookup"><span data-stu-id="03dae-214">Option</span></span></th>
    <th><span data-ttu-id="03dae-215">Vartotojai, kuriems priskirtas sprendimas</span><span class="sxs-lookup"><span data-stu-id="03dae-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="03dae-216">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="03dae-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="03dae-217">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="03dae-217">Participant</span></span></td>
    <td><span data-ttu-id="03dae-218">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="03dae-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-219">Pasirinkę <strong>Dalyvis</strong>, skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam norite priskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="03dae-220">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam norite priskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-221">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="03dae-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="03dae-222">Konkrečios organizacijos hierarchijos vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-223">Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite priskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="03dae-224">Sistema turi iš hierarchijos nuskaityti vartotojų vardus.</span><span class="sxs-lookup"><span data-stu-id="03dae-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="03dae-225">Šie vardai nurodo vartotojus, kuriems galima priskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="03dae-226">Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką.</span><span class="sxs-lookup"><span data-stu-id="03dae-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="03dae-227">Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="03dae-228">Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="03dae-229">Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</span><span class="sxs-lookup"><span data-stu-id="03dae-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="03dae-230">Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams sprendimas turėtų būti priskirtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="03dae-231"><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – sprendimas priskiriamas visiems vartotojams diapazone.</span><span class="sxs-lookup"><span data-stu-id="03dae-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="03dae-232"><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – sprendimas priskiriamas tik paskutiniam vartotojui diapazone.</span><span class="sxs-lookup"><span data-stu-id="03dae-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="03dae-233"><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – sprendimas nepriskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="03dae-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="03dae-234">Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-235">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-235">Workflow user</span></span></td>
    <td><span data-ttu-id="03dae-236">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="03dae-237">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="03dae-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-238">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-238">User</span></span></td>
    <td><span data-ttu-id="03dae-239">Konkretūs „Finance and Operations” vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-239">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-240">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dae-241">Skirtukas <strong>Galimi vartotojai</strong> apima visus „Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="03dae-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="03dae-242">Pasirinkite, kuriems vartotojams norite priskirti sprendimą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-243">Darbo grupė</span><span class="sxs-lookup"><span data-stu-id="03dae-243">Queue</span></span></td>
    <td><span data-ttu-id="03dae-244">Darbo elementų eilė</span><span class="sxs-lookup"><span data-stu-id="03dae-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-245">Pasirinkę <strong>Eilė</strong> spustelėkite skirtuką <strong>Pagal eilę</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dae-246">Norėdami priskirti sprendimą konkrečiai eilei, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="03dae-247">Sąraše <strong>Eilės tipas</strong> pasirinkite <strong>Darbo elemento eilės</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="03dae-248">Sąraše <strong>Eilės pavadinimas</strong> pasirinkite eilę.</span><span class="sxs-lookup"><span data-stu-id="03dae-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="03dae-249">Jei nuo tam tikros sąlygos turi priklausyti, kuriai eilei sprendimas turi būti priskirtas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="03dae-250">Sąraše <strong>Eilės tipas</strong> pasirinkite <strong>Sąlyginės darbo elemento eilės</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="03dae-251">Sąraše <strong>Eilės pavadinimas</strong> pasirinkite <strong>Sąlyginė eilė</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="03dae-252">Ši parinktis naudojama tik kelioms darbo eigoms, pvz., atvejų valdymui.</span><span class="sxs-lookup"><span data-stu-id="03dae-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="03dae-253">Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto sprendimui priimti.</span><span class="sxs-lookup"><span data-stu-id="03dae-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="03dae-254">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="03dae-254">Select one of the following options:</span></span>

    - <span data-ttu-id="03dae-255">**Valandos** – įveskite valandų, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="03dae-256">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-257">**Dienos** – įveskite dienų, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="03dae-258">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-259">**Savaitės** – įveskite savaičių, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="03dae-260">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių vartotojas turi priimti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="03dae-261">Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="03dae-262">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi priimti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="03dae-263">Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="03dae-264">Jei per skirtąjį laiką vartotojas sprendimo nepriims, sprendimas bus laikomas vėluojančiu.</span><span class="sxs-lookup"><span data-stu-id="03dae-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="03dae-265">Vėluojančiu laikomas sprendimas yra perskiriamas atsižvelgiant į parinktis, kurias pasirenkate puslapio srityje **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="03dae-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="03dae-266">Įvykių sprendimo vėlavimo atveju nurodymas</span><span class="sxs-lookup"><span data-stu-id="03dae-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="03dae-267">Jei per skirtąjį laiką vartotojas sprendimo nepriims, sprendimas bus laikomas vėluojančiu.</span><span class="sxs-lookup"><span data-stu-id="03dae-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="03dae-268">Vėluojantį sprendimą galima perskirti arba automatiškai priskirti kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="03dae-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="03dae-269">Atlikite tolesnius veiksmus, kad perskirtumėte sprendimą, jei jis vėluoja.</span><span class="sxs-lookup"><span data-stu-id="03dae-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="03dae-270">Kairiojoje srityje spustelėkite **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="03dae-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="03dae-271">Pasirinkite žymės langelį **Naudoti perskyrimo maršrutą**, norėdami kurti perskyrimo maršrutą.</span><span class="sxs-lookup"><span data-stu-id="03dae-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="03dae-272">Sistema automatiškai priskirs sprendimą perskyrimo sąraše pateiktiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="03dae-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="03dae-273">Pavyzdžiui, tolesnėje lentelėje pateikiamas perskyrimo maršrutas.</span><span class="sxs-lookup"><span data-stu-id="03dae-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="03dae-274">Seka</span><span class="sxs-lookup"><span data-stu-id="03dae-274">Sequence</span></span> | <span data-ttu-id="03dae-275">Perskyrimo maršrutas</span><span class="sxs-lookup"><span data-stu-id="03dae-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="03dae-276">1</span><span class="sxs-lookup"><span data-stu-id="03dae-276">1</span></span>        | <span data-ttu-id="03dae-277">Priskirti: Donna</span><span class="sxs-lookup"><span data-stu-id="03dae-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="03dae-278">2</span><span class="sxs-lookup"><span data-stu-id="03dae-278">2</span></span>        | <span data-ttu-id="03dae-279">Priskirti: Erin</span><span class="sxs-lookup"><span data-stu-id="03dae-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="03dae-280">3</span><span class="sxs-lookup"><span data-stu-id="03dae-280">3</span></span>        | <span data-ttu-id="03dae-281">Galutinis veiksmas: \[1 pasirinkimas\]</span><span class="sxs-lookup"><span data-stu-id="03dae-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="03dae-282">Tokiu atveju, sistema priskirs vėluojantį sprendimą Donna.</span><span class="sxs-lookup"><span data-stu-id="03dae-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="03dae-283">Jei Donna nepriims sprendimo per skirtąjį laiką, sistema priskirs sprendimą Erin.</span><span class="sxs-lookup"><span data-stu-id="03dae-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="03dae-284">Jei Erin nepriims sprendimo per skirtąjį laiką, sistema kaip sprendimą pasirinks **\[1 pasirinkimas\]**.</span><span class="sxs-lookup"><span data-stu-id="03dae-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="03dae-285">Norėdami vartotoją įtraukti į perskyrimo maršrutą, spustelėkite **Įtraukti perskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="03dae-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="03dae-286">Pasirinkite vieną iš tolesnės lentelės parinkčių ir tada, prieš vykdydami 4 veiksmą, atlikite papildomus tos parinkties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="03dae-287">Parinktis</span><span class="sxs-lookup"><span data-stu-id="03dae-287">Option</span></span></th>
    <th><span data-ttu-id="03dae-288">Vartotojai, kuriems perskiriamas sprendimas</span><span class="sxs-lookup"><span data-stu-id="03dae-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="03dae-289">Papildomi veiksmai</span><span class="sxs-lookup"><span data-stu-id="03dae-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="03dae-290">Hierarchija</span><span class="sxs-lookup"><span data-stu-id="03dae-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="03dae-291">Konkrečios organizacijos hierarchijos vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-292">Pasirinkę <strong>Hierarchija</strong>, skirtuko <strong>Hierarchijos pasirinkimas</strong> sąraše <strong>Hierarchijos tipas</strong> pasirinkite hierarchijos tipą, kuriam norite perskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="03dae-293">Sistema turi iš hierarchijos nuskaityti vartotojų vardus.</span><span class="sxs-lookup"><span data-stu-id="03dae-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="03dae-294">Šie vardai nurodo vartotojus, kuriems galima perskirti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="03dae-295">Atlikite tolesnius veiksmus, norėdami nurodyti vartotojų vardų, kuriuos sistema nuskaito, diapazono pradžios ir pabaigos tašką.</span><span class="sxs-lookup"><span data-stu-id="03dae-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="03dae-296">Norėdami nustatyti pradžios tašką, pasirinkite asmenį sąraše <strong>Pradėti nuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="03dae-297">Norėdami nustatyti pabaigos tašką, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="03dae-298">Tada įveskite sąlygą, kuri nurodo, kurioje hierarchijos vietoje sistema nutrauks vardų nuskaitymą.</span><span class="sxs-lookup"><span data-stu-id="03dae-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="03dae-299">Skirtuke <strong>Hierarchijos parinktys</strong> nurodykite, kuriems diapazono vartotojams sprendimas turėtų būti perskirtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="03dae-300"><strong>Priskirti visiems nuskaitytiems vartotojams</strong> – sprendimas perskiriamas visiems vartotojams diapazone.</span><span class="sxs-lookup"><span data-stu-id="03dae-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="03dae-301"><strong>Priskirti tik paskutiniam nuskaitytam darbuotojui</strong> – sprendimas perskiriamas tik paskutiniam vartotojui diapazone.</span><span class="sxs-lookup"><span data-stu-id="03dae-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="03dae-302"><strong>Neįtraukti vartotojų, kurie atitinka šią sąlygą</strong> – sprendimas neperskiriamas jokiems diapazono vartotojams, kurie atitinka tam tikrą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="03dae-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="03dae-303">Norėdami nustatyti sąlygą, spustelėkite <strong>Įtraukti sąlygą</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-304">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-304">Workflow user</span></span></td>
    <td><span data-ttu-id="03dae-305">Dabartinės darbo eigos vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="03dae-306">Pasirinkę <strong>Darbo eigos vartotojas</strong>, skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite vartotoją, kuris dalyvauja darbo eigoje.</span><span class="sxs-lookup"><span data-stu-id="03dae-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="03dae-307">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="03dae-307">User</span></span></td>
    <td><span data-ttu-id="03dae-308">Konkretūs „Finance and Operations” vartotojai</span><span class="sxs-lookup"><span data-stu-id="03dae-308">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="03dae-309">Pasirinkę <strong>Vartotojas</strong>, spustelėkite skirtuką <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="03dae-310">Skirtukas <strong>Galimi vartotojai</strong> apima visus „Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="03dae-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="03dae-311">Pasirinkite, kuriems vartotojams norite perskirti sprendimą, o tada tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="03dae-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="03dae-312">Skirtuko **Laiko limitas** lauke **Trukmė** nurodykite, kiek vartotojas turi laiko, skirto sprendimui priimti.</span><span class="sxs-lookup"><span data-stu-id="03dae-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="03dae-313">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="03dae-313">Select one of the following options:</span></span>

    - <span data-ttu-id="03dae-314">**Valandos** – įveskite valandų, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="03dae-315">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-316">**Dienos** – įveskite dienų, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="03dae-317">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-318">**Savaitės** – įveskite savaičių, per kurias vartotojas turi priimti sprendimą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="03dae-319">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių vartotojas turi priimti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="03dae-320">Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="03dae-321">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių vartotojas turi priimti sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="03dae-322">Pavyzdžiui, galbūt norite, kad vartotojas priimtų sprendimą iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="03dae-323">Pakartokite 3 ir 4 veiksmus su kiekvienu vartotoju, kuris turėtų būti įtrauktas į perskyrimo maršrutą.</span><span class="sxs-lookup"><span data-stu-id="03dae-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="03dae-324">Galite keisti vartotojų tvarką.</span><span class="sxs-lookup"><span data-stu-id="03dae-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="03dae-325">Jei perskyrimo maršrute esantys vartotojai per skirtąjį laiką nepriima sprendimo, sistema priims sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="03dae-326">Norėdami nurodyti parinktį, kurią sistema pasirinks, pasirinkite eilutę **Veiksmas** ir tada skirtuke **Pabaigos veiksmas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="03dae-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="03dae-327">Laiko limito nustatymas</span><span class="sxs-lookup"><span data-stu-id="03dae-327">Set a time limit</span></span>

<span data-ttu-id="03dae-328">Jei sprendimas turi būti priimtas per tam tikrą laiką, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="03dae-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="03dae-329">Šioje procedūroje pasirinktos parinktys gali perrašyti parinktis, kurias pasirinkote puslapio srityse **Priskyrimas** ir **Perskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="03dae-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="03dae-330">Kairiojoje srityje spustelėkite **Išplėstiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="03dae-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="03dae-331">Pasirinkite žymės langelį **Nustatyti darbo eigos elemento laiko limitą**.</span><span class="sxs-lookup"><span data-stu-id="03dae-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="03dae-332">Lauke **Trukmė** nurodykite, kada sprendimas turi būti priimtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="03dae-333">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="03dae-333">Select one of the following options:</span></span>

    - <span data-ttu-id="03dae-334">**Valandos** – įveskite valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="03dae-335">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-336">**Dienos** – įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="03dae-337">Tada pasirinkite jūsų organizacijos naudojamą kalendorių ir įveskite informaciją apie jūsų organizacijos darbo savaitę.</span><span class="sxs-lookup"><span data-stu-id="03dae-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="03dae-338">**Savaitės** – įveskite savaičių skaičių.</span><span class="sxs-lookup"><span data-stu-id="03dae-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="03dae-339">**Mėnesiai** – pasirinkite dieną ir savaitę, iki kurių sprendimas turi būti priimtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="03dae-340">Pavyzdžiui, galbūt norite, kad sprendimas būtų priimtas iki trečios mėnesio savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="03dae-341">**Metai** – pasirinkite dieną, savaitę ir mėnesį, iki kurių sprendimas turi būti priimtas.</span><span class="sxs-lookup"><span data-stu-id="03dae-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="03dae-342">Pavyzdžiui, galbūt norite, kad sprendimas būtų priimtas iki trečios gruodžio mėn. savaitės penktadienio.</span><span class="sxs-lookup"><span data-stu-id="03dae-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="03dae-343">Jei viršijamas laiko limitas, sistema priims sprendimą.</span><span class="sxs-lookup"><span data-stu-id="03dae-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="03dae-344">Sąraše **Veiksmas** pasirinkite parinktį, kurią sistema turi pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="03dae-344">In the **Action** list, select the option that the system should select.</span></span>
