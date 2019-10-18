---
title: Darbo eigos ypatybių konfigūravimas
description: Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190125"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="c9b8e-103">Darbo eigos ypatybių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9b8e-104">Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="c9b8e-105">Norėdami konfigūruoti darbo eigos ypatybes, atidarykite darbo eigą darbo eigos rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="c9b8e-106">Spustelėkite lauką darbo eigos rengyklėje ir spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c9b8e-107">Tada galite naudoti šias procedūras norėdami konfigūruoti įvairias darbo eigos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="c9b8e-108">Pavadinimo darbo eigai sukūrimas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-108">Name the workflow</span></span>

<span data-ttu-id="c9b8e-109">Norėdami įvesti darbo eigos pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="c9b8e-110">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c9b8e-111">Lauke **Pavadinimas** įveskite unikalų darbo eigos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="c9b8e-112">Pavyzdžiui, jei kuriate pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pirkimo paraiškos darbo eigą galite pavadinti **Pirkimo paraiškos Danijoje** arba **Pirkimo paraiškos Ispanijoje**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="c9b8e-113">Darbo eigos savininko nustatymas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-113">Specify the workflow owner</span></span>

<span data-ttu-id="c9b8e-114">Darbo eigos savininkas yra asmuo, kuris valdo ir prižiūri darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="c9b8e-115">Norėdami nustatyti darbo eigos savininką, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="c9b8e-116">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c9b8e-117">Sąraše **Savininkas** pasirinkite darbo eigą valdysiančio asmens vardą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="c9b8e-118">El. laiško šablono pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-118">Select an email template</span></span>

<span data-ttu-id="c9b8e-119">Atlikite šiuos veiksmus, norėdami pasirinkti el. laiško šabloną, kuris naudojamas pranešimams apie darbo eigą generuoti.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="c9b8e-120">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c9b8e-121">Sąraše **Darbo eigos pranešimų el. laiško šablonas** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="c9b8e-122">Instrukcijų vartotojams įvedimas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-122">Enter instructions for users</span></span>

<span data-ttu-id="c9b8e-123">Galite pateikti instrukcijas vartotojams, kurie pateiks apdorotinus ir tvirtintinus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="c9b8e-124">Šie vartotojai taip pat nurodomi kaip *iniciatoriai*.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="c9b8e-125">Pavyzdžiui, jūs sukuriate pirkimo paraiškų darbo eigą ir įvedate instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="c9b8e-126">Tada tas instrukcijas gali peržiūrėti vartotojai, kurie pirkimo paraiškas įveda puslapyje **Pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c9b8e-127">Norėdamas peržiūrėti instrukcijas, iniciatorius turi spustelėti darbo eigos pranešimų juostoje esančią piktogramą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="c9b8e-128">Norėdami vartotojams įvesti instrukcijas, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="c9b8e-129">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c9b8e-130">Lauke **Pateikimo instrukcijos** įveskite instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="c9b8e-131">Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c9b8e-132">Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c9b8e-133">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="c9b8e-134">Spustelėkite lauką **Pateikimo instrukcijos**, norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c9b8e-135">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c9b8e-136">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c9b8e-137">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-137">Click **Insert**.</span></span>

4. <span data-ttu-id="c9b8e-138">Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="c9b8e-139">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="c9b8e-140">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c9b8e-141">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="c9b8e-142">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c9b8e-143">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c9b8e-144">Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 3 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="c9b8e-145">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="c9b8e-146">Nustatymas, kada naudojama ši darbo eiga</span><span class="sxs-lookup"><span data-stu-id="c9b8e-146">Specify when this workflow is used</span></span>

<span data-ttu-id="c9b8e-147">Galite sukurti kelias darbo eigas pagal tą patį tipą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="c9b8e-148">Pavyzdžiui, galite sukurti pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pavyzdžiui, Pirkimo paraiškos Danijoje ir Pirkimo paraiškos Ispanijoje.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="c9b8e-149">Sukūrus kelias darbo eigas pagal tą patį tipą, jums reikia nurodyti, kada kiekvienas šablonas bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="c9b8e-150">Aukščiau pateiktame pavyzdyje galite nurodyti tolesnes sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="c9b8e-151">Pirkimo paraiškos Danijoje naudojamos, kai: šalis / regionas = DK.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="c9b8e-152">Pirkimo paraiškos Ispanijoje naudojamos, kai: šalis / regionas = ES.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="c9b8e-153">Norėdami nustatyti, kada turėtų būti naudojama jūsų konfigūruojama darbo eiga, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="c9b8e-154">Kairiojoje srityje spustelėkite **Aktyvinimas**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="c9b8e-155">Pasirinkite žymės langelį **Nustatyti darbo eigos vykdymo sąlygas**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="c9b8e-156">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="c9b8e-157">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="c9b8e-157">Enter a condition.</span></span>
5. <span data-ttu-id="c9b8e-158">Įveskite visas reikalingas papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="c9b8e-159">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra nustatytos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="c9b8e-160">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-160">Click **Test**.</span></span>
    2. <span data-ttu-id="c9b8e-161">Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="c9b8e-162">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-162">Click **Test**.</span></span> <span data-ttu-id="c9b8e-163">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="c9b8e-164">Pavyzdžiui, jei kuriate pirkimo paraiškos darbo eigą Ispanijai, puslapio srityje **Tikrinti sąlygą** bus rodomas pirkimo paraiškų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="c9b8e-165">Spustelėjus **Tikrinti**, sistema įvertins pasirinktą pirkimo paraišką, siekdama nustatyti, ar šalis / regionas yra ES.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="c9b8e-166">Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c9b8e-167">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="c9b8e-167">Specify when notifications are sent</span></span>

<span data-ttu-id="c9b8e-168">Kai dokumentas pateikiamas apdoroti, sukuriamas darbo eigos egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="c9b8e-169">Pranešimus vartotojams galima siųsti, kai dėl klaidos paleidžiami, pabaigiami, atšaukiami arba sustabdomi darbo eigos egzemplioriai (remiantis darbo eiga).</span><span class="sxs-lookup"><span data-stu-id="c9b8e-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="c9b8e-170">Norėdami nustatyti, kada turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="c9b8e-171">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c9b8e-172">Pažymėkite žymės langelį kiekvienam įvykiui, kuriam įvykus turi būti suaktyvinti pranešimai.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="c9b8e-173">**Pradėta** – pranešimai siunčiami, kai darbo eigos egzempliorius paleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="c9b8e-174">**Sustabdyta** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl klaidos.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="c9b8e-175">**Baigta** – pranešimai siunčiami, kai darbo eigos egzempliorius pabaigiamas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="c9b8e-176">**Nepataisoma** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl nepataisomos klaidos.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="c9b8e-177">**Nutraukta** – pranešimai siunčiami, kai darbo eigos egzempliorius nutraukiamas.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="c9b8e-178">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c9b8e-179">Skirtuke **Pranešimo tekstas** įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="c9b8e-180">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c9b8e-181">Tekstą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="c9b8e-182">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="c9b8e-183">Norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas, spustelėkite lauką.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c9b8e-184">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c9b8e-185">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c9b8e-186">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="c9b8e-187">Bendras **Pranešimo teksto** rezervavimo ženklas, kurį reikia įtraukti, yra „Last Notes: %Workflow.Last note%“, kuris parodo visus komentarus iš ankstesniojo veiksmo.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="c9b8e-188">Norėdami įtraukti teksto vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="c9b8e-189">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="c9b8e-190">Rodomame puslapyje spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="c9b8e-191">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="c9b8e-192">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c9b8e-193">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c9b8e-194">Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 5 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="c9b8e-195">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-195">Click **Close**.</span></span>

7. <span data-ttu-id="c9b8e-196">Skirtuke **Gavėjas** naudokite tolesnes parinktis, norėdami nurodyti, kas turėtų gauti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c9b8e-197">Parinktis</span><span class="sxs-lookup"><span data-stu-id="c9b8e-197">Option</span></span></th>
    <th><span data-ttu-id="c9b8e-198">Pranešimai siunčiami šiems vartotojams</span><span class="sxs-lookup"><span data-stu-id="c9b8e-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="c9b8e-199">Norėdami siųsti pranešimus, atlikite šiuos veiksmus</span><span class="sxs-lookup"><span data-stu-id="c9b8e-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c9b8e-200">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="c9b8e-200">Participant</span></span></td>
    <td><span data-ttu-id="c9b8e-201">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="c9b8e-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c9b8e-202">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Dalyvis</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="c9b8e-203">Skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c9b8e-204">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c9b8e-205">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-205">Workflow user</span></span></td>
    <td><span data-ttu-id="c9b8e-206">Vartotojai, kurie yra šios darbo eigos dalyviai</span><span class="sxs-lookup"><span data-stu-id="c9b8e-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c9b8e-207">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Darbo eigos vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="c9b8e-208">Skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite šios darbo eigos dalyvį.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c9b8e-209">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-209">User</span></span></td>
    <td><span data-ttu-id="c9b8e-210">Konkretūs vartotojai</span><span class="sxs-lookup"><span data-stu-id="c9b8e-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c9b8e-211">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="c9b8e-212">Skirtuko <strong>Vartotojas</strong> sąrašas <strong>Galimi vartotojai</strong> apima visus vartotojus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c9b8e-213">Pasirinkite, kuriems bus siunčiami pranešimai, ir tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="c9b8e-214">Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="c9b8e-215">Komentarų apie atliktus darbo eigos pakeitimus įvedimas</span><span class="sxs-lookup"><span data-stu-id="c9b8e-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="c9b8e-216">Norėdami įvesti komentarų apie atliktus darbo eigos keitimus, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="c9b8e-217">Kairiojoje srityje spustelėkite **Pastabos**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="c9b8e-218">Lauke **Įvesti komentarus apie darbo eigą** įveskite savo komentarus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="c9b8e-219">Peržiūrėkite savo komentarus.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-219">Review your comments.</span></span> <span data-ttu-id="c9b8e-220">Įtraukę komentarus jų modifikuoti negalite.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="c9b8e-221">Spustelėkite **Įtraukti**, norėdami komentarų įtraukti į sritį **Komentarų retrospektyva**.</span><span class="sxs-lookup"><span data-stu-id="c9b8e-221">Click **Add** to add your comments to the **Comment history** area.</span></span>
