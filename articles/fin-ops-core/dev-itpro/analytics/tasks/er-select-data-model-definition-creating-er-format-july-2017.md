---
title: Duomenų modelio aprašo pasirinkimas, kuriant formatus
description: Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184720"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="e77bd-103">Duomenų modelio aprašo pasirinkimas, kuriant formatus</span><span class="sxs-lookup"><span data-stu-id="e77bd-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e77bd-104">Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="e77bd-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="e77bd-105">Ši procedūra nurodo, kaip modelio šakninis elementas gali būti pasirinktas kaip duomenų modelio aprašas įterpiant elektroninių ataskaitų (ER) formato konfigūraciją, skirtą generuoti elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="e77bd-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="e77bd-106">Atlikdami šią procedūrą sukursite pavyzdinės įmonės „Litware, Inc.“ naują ER formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="e77bd-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="e77bd-107">Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="e77bd-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="e77bd-108">Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="e77bd-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="e77bd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e77bd-110">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="e77bd-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="e77bd-111">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų” veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e77bd-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="e77bd-112">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="e77bd-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="e77bd-113">Pridėkite naują ER duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="e77bd-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="e77bd-114">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="e77bd-115">Mes pridėjome naują ER modelio konfigūraciją, kurioje yra duomenų modelis, skirtas naudoti kaip duomenų šaltinis Intrastat ataskaitoms generuoti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="e77bd-116">Lauke „Pavadinimas“ įrašykite „Mokėjimo modelis (fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="e77bd-117">Mokėjimo modelis (fiktyvus)</span><span class="sxs-lookup"><span data-stu-id="e77bd-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="e77bd-118">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="e77bd-118">Click Create configuration.</span></span>
4. <span data-ttu-id="e77bd-119">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="e77bd-119">Click Designer.</span></span>
    * <span data-ttu-id="e77bd-120">Atidarykite ER kūrimo priemonę, norėdami nurodyti šios konfigūracijos duomenų modelio struktūrą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="e77bd-121">Tarkime, kad mes kuriame duomenų modelį mokėjimų verslo domenui, kad palaikytų 2 mokėjimo būdus – kredito pervedimo ir tiesioginio debeto.</span><span class="sxs-lookup"><span data-stu-id="e77bd-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="e77bd-122">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="e77bd-123">Lauke Pavadinimas įrašykite „Mokėjimai – kredito pervedimas“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="e77bd-124">Mokėjimai – kredito pervedimas</span><span class="sxs-lookup"><span data-stu-id="e77bd-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="e77bd-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-125">Click Add.</span></span>
8. <span data-ttu-id="e77bd-126">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="e77bd-127">Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.</span><span class="sxs-lookup"><span data-stu-id="e77bd-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="e77bd-128">Lauke Pavadinimas įrašykite „Mokėjimai – tiesioginis debetas“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="e77bd-129">Mokėjimai – tiesioginis debetas</span><span class="sxs-lookup"><span data-stu-id="e77bd-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="e77bd-130">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-130">Click Add.</span></span>
12. <span data-ttu-id="e77bd-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-131">Click Save.</span></span>
13. <span data-ttu-id="e77bd-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-132">Close the page.</span></span>
14. <span data-ttu-id="e77bd-133">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="e77bd-133">Click Change status.</span></span>
    * <span data-ttu-id="e77bd-134">Užbaikite modelio juodraščio versiją, kad jis būtų prieinamas naujo modelio susiejimams ir formatams.</span><span class="sxs-lookup"><span data-stu-id="e77bd-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="e77bd-135">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-135">Click Complete.</span></span>
16. <span data-ttu-id="e77bd-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e77bd-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="e77bd-137">Pradėkite įvesti naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="e77bd-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="e77bd-138">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e77bd-139">Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="e77bd-140">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e77bd-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="e77bd-141">Žinokite, kad visi pasirinkto duomenų modelio šakniniai elementai dabar prieinami pasirinkimui kaip duomenų modelio apibrėžtis.</span><span class="sxs-lookup"><span data-stu-id="e77bd-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="e77bd-142">Jūs galite ir toliau kurti savo formatą, naudodami bet kokius reikiamus šakninius duomenų modelio elementus.</span><span class="sxs-lookup"><span data-stu-id="e77bd-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="e77bd-143">Trūkstamas modelio susiejimas pasirinktam šakniniam elementui neužkerta jums kelio tęsti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="e77bd-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="e77bd-145">Pridėkite naują ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="e77bd-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="e77bd-146">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e77bd-147">Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="e77bd-148">Lauke „Pavadinimas“ įrašykite „Mokėjimo modelio susiejimai (fiktyvūs)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="e77bd-149">Mokėjimo modelio susiejimai (fiktyvūs)</span><span class="sxs-lookup"><span data-stu-id="e77bd-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="e77bd-150">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e77bd-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="e77bd-151">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="e77bd-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="e77bd-152">Sukurkite ER modelio susiejimus</span><span class="sxs-lookup"><span data-stu-id="e77bd-152">Design ER model mappings</span></span>
1. <span data-ttu-id="e77bd-153">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="e77bd-153">Click Designer.</span></span>
    * <span data-ttu-id="e77bd-154">Naudokite ER kūrimo priemonę nurodyti modelio susiejimus reikalingiems šakniniams elementams.</span><span class="sxs-lookup"><span data-stu-id="e77bd-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="e77bd-155">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="e77bd-155">Click Designer.</span></span>
    * <span data-ttu-id="e77bd-156">Modeliuokite pasirinktą modelio susiejimo nustatymą pasirinkto modelio šakniniam elementui.</span><span class="sxs-lookup"><span data-stu-id="e77bd-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="e77bd-157">Medyje pasirinkite Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="e77bd-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="e77bd-158">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-158">Click Add root.</span></span>
5. <span data-ttu-id="e77bd-159">Lauke Pavadinimas įveskite „Didžioji knyga“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="e77bd-160">Lauke „Lentelė“, įveskite „LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="e77bd-161">LedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="e77bd-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="e77bd-162">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e77bd-162">Click OK.</span></span>
8. <span data-ttu-id="e77bd-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e77bd-163">Click Save.</span></span>
9. <span data-ttu-id="e77bd-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-164">Close the page.</span></span>
10. <span data-ttu-id="e77bd-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="e77bd-166">Pradėkite įvesti kitą naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="e77bd-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="e77bd-167">Medyje pasirinkite „Payment model (fictitious)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="e77bd-168">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="e77bd-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="e77bd-169">Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Mokėjimo modelis (fiktyvus)“.</span><span class="sxs-lookup"><span data-stu-id="e77bd-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="e77bd-170">Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e77bd-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="e77bd-171">Žinokite, kad dabar tik vieną šakninį elementą galima susieti su programos duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="e77bd-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="e77bd-172">Kai bent vienas modelio susiejimas yra įvestas, tik modelio šakniniai elementai, susieti su programos duomenų šaltiniais, gali būti pasirinkti kaip modelio apibrėžtis, kai pridėtas ER formatas.</span><span class="sxs-lookup"><span data-stu-id="e77bd-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="e77bd-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e77bd-173">Close the page.</span></span>

