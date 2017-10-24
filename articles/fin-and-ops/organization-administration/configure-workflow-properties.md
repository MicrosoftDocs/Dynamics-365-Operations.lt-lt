---
title: "Darbo eigos ypatybių konfigūravimas"
description: "Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6cad67d4108a81de545a1e633dc4e12a31af683b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="configure-the-properties-of-a-workflow"></a><span data-ttu-id="e4c4d-103">Darbo eigos ypatybių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-103">Configure the properties of a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e4c4d-104">Šioje temoje paaiškinama, kaip konfigūruoti įvairias darbo eigos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="e4c4d-105">Norėdami konfigūruoti darbo eigos ypatybes, atidarykite darbo eigą darbo eigos rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="e4c4d-106">Spustelėkite lauką darbo eigos rengyklėje ir spustelėkite **Ypatybės**, kad atidarytumėte puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="e4c4d-107">Tada galite naudoti šias procedūras norėdami konfigūruoti įvairias darbo eigos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="e4c4d-108">Pavadinimo darbo eigai sukūrimas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-108">Name the workflow</span></span>
<span data-ttu-id="e4c4d-109">Norėdami įvesti darbo eigos pavadinimą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="e4c4d-110">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e4c4d-111">Lauke **Pavadinimas** įveskite unikalų darbo eigos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="e4c4d-112">Pavyzdžiui, jei kuriate pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pirkimo paraiškos darbo eigą galite pavadinti **Pirkimo paraiškos Danijoje** arba **Pirkimo paraiškos Ispanijoje**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="e4c4d-113">Darbo eigos savininko nustatymas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-113">Specify the workflow owner</span></span>
<span data-ttu-id="e4c4d-114">Darbo eigos savininkas yra asmuo, kuris valdo ir prižiūri darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="e4c4d-115">Norėdami nustatyti darbo eigos savininką, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="e4c4d-116">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e4c4d-117">Sąraše **Savininkas** pasirinkite darbo eigą valdysiančio asmens vardą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="e4c4d-118">El. laiško šablono pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-118">Select an email template</span></span>
<span data-ttu-id="e4c4d-119">Atlikite šiuos veiksmus, norėdami pasirinkti el. laiško šabloną, kuris naudojamas pranešimams apie darbo eigą generuoti.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="e4c4d-120">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e4c4d-121">Sąraše **Darbo eigos pranešimų el. laiško šablonas** pasirinkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="e4c4d-122">Instrukcijų vartotojams įvedimas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-122">Enter instructions for users</span></span>
<span data-ttu-id="e4c4d-123">Galite pateikti instrukcijas vartotojams, kurie pateiks apdorotinus ir tvirtintinus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="e4c4d-124">Šie vartotojai taip pat nurodomi kaip *iniciatoriai*.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="e4c4d-125">Pavyzdžiui, jūs sukuriate pirkimo paraiškų darbo eigą ir įvedate instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="e4c4d-126">Tada tas instrukcijas gali peržiūrėti vartotojai, kurie pirkimo paraiškas įveda puslapyje **Pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="e4c4d-127">Norėdamas peržiūrėti instrukcijas, iniciatorius turi spustelėti darbo eigos pranešimų juostoje esančią piktogramą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="e4c4d-128">Norėdami vartotojams įvesti instrukcijas, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="e4c4d-129">Kairiojoje srityje spustelėkite **Pagrindiniai parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="e4c4d-130">Lauke **Pateikimo instrukcijos** įveskite instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="e4c4d-131">Norėdami instrukcijas personalizuoti, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="e4c4d-132">Instrukcijas rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="e4c4d-133">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="e4c4d-134">Spustelėkite lauką **Pateikimo instrukcijos**, norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="e4c4d-135">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="e4c4d-136">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="e4c4d-137">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="e4c4d-138">Norėdami įtraukti instrukcijų vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="e4c4d-139">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="e4c4d-140">Rodomame puslapyje spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="e4c4d-141">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="e4c4d-142">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="e4c4d-143">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e4c4d-144">Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 3 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="e4c4d-145">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="e4c4d-146">Nustatymas, kada naudojama ši darbo eiga</span><span class="sxs-lookup"><span data-stu-id="e4c4d-146">Specify when this workflow is used</span></span>
<span data-ttu-id="e4c4d-147">Galite sukurti kelias darbo eigas pagal tą patį tipą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="e4c4d-148">Pavyzdžiui, galite sukurti pirkimo paraiškos darbo eigą kiekvienai šaliai / regionui, kuriame veikia jūsų verslas, pavyzdžiui, Pirkimo paraiškos Danijoje ir Pirkimo paraiškos Ispanijoje.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="e4c4d-149">Sukūrus kelias darbo eigas pagal tą patį tipą, jums reikia nurodyti, kada kiekvienas šablonas bus naudojamas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="e4c4d-150">Aukščiau pateiktame pavyzdyje galite nurodyti tolesnes sąlygas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="e4c4d-151">Pirkimo paraiškos Danijoje naudojamos, kai: šalis / regionas = DK.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="e4c4d-152">Pirkimo paraiškos Ispanijoje naudojamos, kai: šalis / regionas = ES.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="e4c4d-153">Norėdami nustatyti, kada turėtų būti naudojama jūsų konfigūruojama darbo eiga, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="e4c4d-154">Kairiojoje srityje spustelėkite **Aktyvinimas**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="e4c4d-155">Pasirinkite žymės langelį **Nustatyti darbo eigos vykdymo sąlygas**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="e4c4d-156">Spustelėkite **Įtraukti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="e4c4d-157">Įveskite sąlygą</span><span class="sxs-lookup"><span data-stu-id="e4c4d-157">Enter a condition.</span></span>
5.  <span data-ttu-id="e4c4d-158">Įveskite visas reikalingas papildomas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="e4c4d-159">Norėdami patikrinti, kad sąlygos, kurias įvedėte yra nustatytos teisingai, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="e4c4d-160">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="e4c4d-161">Puslapio **Tikrinti darbo eigos sąlygą** srityje **Tikrinti sąlygą** pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="e4c4d-162">Spustelėkite **Išbandyti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-162">Click **Test**.</span></span> <span data-ttu-id="e4c4d-163">Įvertinusi įrašą sistema nustatys, ar jis tenkina jūsų nurodytas sąlygas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="e4c4d-164">Pavyzdžiui, jei kuriate pirkimo paraiškos darbo eigą Ispanijai, puslapio srityje **Tikrinti sąlygą** bus rodomas pirkimo paraiškų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="e4c4d-165">Spustelėjus **Tikrinti**, sistema įvertins pasirinktą pirkimo paraišką, siekdama nustatyti, ar šalis / regionas yra ES.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="e4c4d-166">Spustelėkite **Gerai** arba **Atšaukti**, kad grįžtumėte į puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e4c4d-167">Nurodymas, kada siunčiami pranešimai</span><span class="sxs-lookup"><span data-stu-id="e4c4d-167">Specify when notifications are sent</span></span>
<span data-ttu-id="e4c4d-168">Kai dokumentas pateikiamas apdoroti, sukuriamas darbo eigos egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="e4c4d-169">Pranešimus vartotojams galima siųsti, kai dėl klaidos paleidžiami, pabaigiami, atšaukiami arba sustabdomi darbo eigos egzemplioriai (remiantis darbo eiga).</span><span class="sxs-lookup"><span data-stu-id="e4c4d-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="e4c4d-170">Norėdami nustatyti, kada turėtų būti siunčiami pranešimai, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="e4c4d-171">Kairiojoje srityje spustelėkite **Pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="e4c4d-172">Pažymėkite žymės langelį kiekvienam įvykiui, kuriam įvykus turi būti suaktyvinti pranešimai.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="e4c4d-173">**Pradėta** – pranešimai siunčiami, kai darbo eigos egzempliorius paleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="e4c4d-174">**Sustabdyta** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl klaidos.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="e4c4d-175">**Baigta** – pranešimai siunčiami, kai darbo eigos egzempliorius pabaigiamas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="e4c4d-176">**Nepataisoma** – pranešimai siunčiami, kai darbo eigos egzempliorius sustabdomas dėl nepataisomos klaidos.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="e4c4d-177">**Nutraukta** – pranešimai siunčiami, kai darbo eigos egzempliorius nutraukiamas.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="e4c4d-178">Pasirinkite įvykio, kurį pasirinkote 2 veiksme, eilutę.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="e4c4d-179">Skirtuke **Pranešimo tekstas** įveskite pranešimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="e4c4d-180">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e4c4d-181">Tekstą rodant vartotojams, vietos rezervavimo ženklai pakeičiami tam tikrais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="e4c4d-182">Atlikite šiuos veiksmus, norėdami įterpti vietos rezervavimo ženklą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="e4c4d-183">Norėdami nurodyti, kur turėtų atsirasti vietos rezervavimo ženklas, spustelėkite lauką.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="e4c4d-184">Spustelėkite **Įterpti vietos rezervavimo ženklą**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="e4c4d-185">Rodomame sąraše pasirinkite vietos rezervavimo ženklus, kuriuos norite įterpti.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="e4c4d-186">Spustelėkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="e4c4d-187">Norėdami įtraukti teksto vertimų, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="e4c4d-188">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="e4c4d-189">Rodomame puslapyje spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="e4c4d-190">Rodomame sąraše pasirinkite kalbą, kuria įvedate tekstą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="e4c4d-191">Lauke **Išverstas tekstas** įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="e4c4d-192">Norėdami personalizuoti tekstą, galite įterpti vietos rezervavimo ženklus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e4c4d-193">Norėdami instrukcijų apie tai, kaip įvesti vietos rezervavimo ženklą, žr. 5 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="e4c4d-194">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-194">Click **Close**.</span></span>

7.  <span data-ttu-id="e4c4d-195">Skirtuke **Gavėjas** naudokite tolesnes parinktis, norėdami nurodyti, kas turėtų gauti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e4c4d-196">Parinktis</span><span class="sxs-lookup"><span data-stu-id="e4c4d-196">Option</span></span></th>
    <th><span data-ttu-id="e4c4d-197">Pranešimai siunčiami šiems vartotojams</span><span class="sxs-lookup"><span data-stu-id="e4c4d-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="e4c4d-198">Norėdami siųsti pranešimus, atlikite šiuos veiksmus</span><span class="sxs-lookup"><span data-stu-id="e4c4d-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e4c4d-199">Dalyvis</span><span class="sxs-lookup"><span data-stu-id="e4c4d-199">Participant</span></span></td>
    <td><span data-ttu-id="e4c4d-200">Vartotojai, kurie priskirti konkrečiai grupei arba vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="e4c4d-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e4c4d-201">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Dalyvis</strong>.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="e4c4d-202">Skirtuko <strong>Pagal vaidmenį</strong> sąraše <strong>Dalyvio tipas</strong> pasirinkite grupės arba vaidmens tipą, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e4c4d-203">Sąraše <strong>Dalyvis</strong> pasirinkite grupę arba vaidmenį, kuriam bus siunčiami pranešimai.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e4c4d-204">Darbo eigos vartotojas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-204">Workflow user</span></span></td>
    <td><span data-ttu-id="e4c4d-205">Vartotojai, kurie yra šios darbo eigos dalyviai</span><span class="sxs-lookup"><span data-stu-id="e4c4d-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e4c4d-206">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Darbo eigos vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="e4c4d-207">Skirtuko <strong>Darbo eigos vartotojas</strong> sąraše <strong>Darbo eigos vartotojas</strong> pasirinkite šios darbo eigos dalyvį.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e4c4d-208">Vartotojas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-208">User</span></span></td>
    <td><span data-ttu-id="e4c4d-209">Konkretūs „Finance and Operations” vartotojai</span><span class="sxs-lookup"><span data-stu-id="e4c4d-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="e4c4d-210">Skirtuke <strong>Gavėjas</strong> spustelėkite <strong>Vartotojas</strong>.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="e4c4d-211">Skirtuko <strong>Vartotojas</strong> sąrašas <strong>Galimi vartotojai</strong> apima visus „Finance and Operations“ vartotojus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="e4c4d-212">Pasirinkite, kuriems bus siunčiami pranešimai, ir tuos vartotojus perkelkite į sąrašą <strong>Pasirinkti vartotojai</strong>.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="e4c4d-213">Pakartokite veiksmus 3–7 kiekvienam įvykiui, kurį pasirinkote 2 veiksme.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="e4c4d-214">Komentarų apie atliktus darbo eigos pakeitimus įvedimas</span><span class="sxs-lookup"><span data-stu-id="e4c4d-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="e4c4d-215">Norėdami įvesti komentarų apie atliktus darbo eigos keitimus, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="e4c4d-216">Kairiojoje srityje spustelėkite **Pastabos**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="e4c4d-217">Lauke **Įvesti komentarus apie darbo eigą** įveskite savo komentarus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="e4c4d-218">Peržiūrėkite savo komentarus.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-218">Review your comments.</span></span> <span data-ttu-id="e4c4d-219">Įtraukę komentarus jų modifikuoti negalite.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="e4c4d-220">Spustelėkite **Įtraukti**, norėdami komentarų įtraukti į sritį **Komentarų retrospektyva**.</span><span class="sxs-lookup"><span data-stu-id="e4c4d-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





