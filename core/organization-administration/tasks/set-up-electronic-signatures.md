--- 
title: "Elektroninių parašų nustatymas"
description: "Naudokite šią procedūrą norėdami nustatyti elektroninius parašus."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 11fee0b2358e6a2b84c221f8eb06e32c888e5f44
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="2b012-103">Elektroninių parašų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b012-103">Set up electronic signatures</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b012-104">Naudokite šią procedūrą norėdami nustatyti elektroninius parašus.</span><span class="sxs-lookup"><span data-stu-id="2b012-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="2b012-105">Elektroninis parašas patvirtina asmens, kuris ketina pradėti ar patvirtinti skaičiavimo procesą, tapatybę.</span><span class="sxs-lookup"><span data-stu-id="2b012-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="2b012-106">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DAT.</span><span class="sxs-lookup"><span data-stu-id="2b012-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="2b012-107">Elektroninio parašo konfigūracijos rakto įgalinimas</span><span class="sxs-lookup"><span data-stu-id="2b012-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="2b012-108">Pasirinkite Sistemos administravimas > Nustatymai > Licencijos konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="2b012-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="2b012-109">Medyje išplėskite „Administravimas“.</span><span class="sxs-lookup"><span data-stu-id="2b012-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="2b012-110">Patikrinkite, ar pažymėtas žymės langelis Elektroninis parašas.</span><span class="sxs-lookup"><span data-stu-id="2b012-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="2b012-111">Jei žymės langelis Elektroninis parašas nepažymėtas, turite įjungti techninės priežiūros režimą.</span><span class="sxs-lookup"><span data-stu-id="2b012-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="2b012-112">Priežiūros režimą galima įjungti šioje aplinkoje paleidžiant priežiūros užduotį iš „Lifecycle Services“ arba vietinėje sistemoje naudojant įrankį Deployment.Setup.</span><span class="sxs-lookup"><span data-stu-id="2b012-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="2b012-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b012-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="2b012-114">Elektroninio parašo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b012-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="2b012-115">Pasirinkite Organizacijos administravimas > Nustatymai > Elektroninis parašas > Elektroninio parašo parametrai.</span><span class="sxs-lookup"><span data-stu-id="2b012-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="2b012-116">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2b012-116">Click Edit.</span></span>
3. <span data-ttu-id="2b012-117">Lauke Pastaba įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b012-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="2b012-118">Įveskite pranešimą, kurį pasirašantieji gaus, kai bus reikalaujama parašo.</span><span class="sxs-lookup"><span data-stu-id="2b012-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="2b012-119">Galite įvesti bet kokį tekstą.</span><span class="sxs-lookup"><span data-stu-id="2b012-119">You can enter any text.</span></span> <span data-ttu-id="2b012-120">Paprastai šis tekstas nurodo vartotojui, ką reiškia elektroninis dokumento pasirašymas.</span><span class="sxs-lookup"><span data-stu-id="2b012-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="2b012-121">Jei norite įvesti pranešimo tekstą kitomis kalbomis, spustelėkite mygtuką Vertimai.</span><span class="sxs-lookup"><span data-stu-id="2b012-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="2b012-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2b012-122">Click Save.</span></span>
5. <span data-ttu-id="2b012-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b012-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="2b012-124">Elektroninių parašų priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b012-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="2b012-125">Pasirinkite Organizacijos administravimas > Nustatymai > Elektroninis parašas > Elektroninio parašo priežasčių kodai.</span><span class="sxs-lookup"><span data-stu-id="2b012-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="2b012-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2b012-126">Click New.</span></span>
    * <span data-ttu-id="2b012-127">Prieš naudodami elektroninius parašus turite nustatyti priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="2b012-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="2b012-128">Galiojantis priežasties kodas būtinas pasirašant dokumentą.</span><span class="sxs-lookup"><span data-stu-id="2b012-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="2b012-129">Pasirašantysis pasirenka priežasties kodą, siekdamas nurodyti elektroninio parašo paskirtį.</span><span class="sxs-lookup"><span data-stu-id="2b012-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="2b012-130">Pavyzdžiui, priežasties kodas gali būti naudojamas nurodyti teisėtą patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="2b012-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="2b012-131">Lauke Priežasties kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b012-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="2b012-132">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b012-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2b012-133">Jei reikia, įveskite papildomus priežasties kodus.</span><span class="sxs-lookup"><span data-stu-id="2b012-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="2b012-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2b012-134">Click Save.</span></span>
6. <span data-ttu-id="2b012-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b012-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="2b012-136">Elektroninių parašų prašymas esamiems procesams</span><span class="sxs-lookup"><span data-stu-id="2b012-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="2b012-137">Pasirinkite Organizacijos administravimas > Nustatymai > Elektroninis parašas > Elektroniniam parašui taikomi reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="2b012-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="2b012-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2b012-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2b012-139">Pasirinkti procesą, kuriam būtini elektroniniai parašai.</span><span class="sxs-lookup"><span data-stu-id="2b012-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="2b012-140">Pažymėkite arba išvalykite žymės langelį Būtinas parašas.</span><span class="sxs-lookup"><span data-stu-id="2b012-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="2b012-141">Pakartokite šiuos veiksmus su kiekvienu elektroninių parašų reikalaujančiu procesu.</span><span class="sxs-lookup"><span data-stu-id="2b012-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="2b012-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2b012-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="2b012-143">Pasirinktinio elektroninių parašų reikalavimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="2b012-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="2b012-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2b012-144">Click New.</span></span>
2. <span data-ttu-id="2b012-145">Pažymėkite arba išvalykite žymės langelį Būtinas parašas.</span><span class="sxs-lookup"><span data-stu-id="2b012-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="2b012-146">Lauke Pavadinimas įveskite proceso, kuriam būtinas elektroninis parašas, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2b012-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="2b012-147">Lauke Lentelės pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2b012-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2b012-148">Sąraše suraskite ir pasirinkite lentelę, kurioje saugomi pasirašytini duomenys.</span><span class="sxs-lookup"><span data-stu-id="2b012-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="2b012-149">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2b012-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2b012-150">Lauke Lauko pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2b012-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2b012-151">Sąraše suraskite ir pasirinkite norimą stebėti lentelės lauką.</span><span class="sxs-lookup"><span data-stu-id="2b012-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="2b012-152">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2b012-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2b012-153">Nustatykite, kada reikalingas parašas.</span><span class="sxs-lookup"><span data-stu-id="2b012-153">Specify when a signature is required.</span></span>     <span data-ttu-id="2b012-154">Pasirinkite Visada, jei parašo reikalaujama, kada lauke pakeičiami duomenys.</span><span class="sxs-lookup"><span data-stu-id="2b012-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="2b012-155">Pasirinkite Tik, jei parašo reikalaujama tik esant tam tikroms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="2b012-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="2b012-156">Jei pasirinksite Tik, taip pat turite pasirinkti vieną iš šių pasirinkčių: Kai įterpiamas įrašas, Kai atnaujinamas įrašas arba Kai panaikinamas įrašas.</span><span class="sxs-lookup"><span data-stu-id="2b012-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="2b012-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2b012-157">Click Save.</span></span>
11. <span data-ttu-id="2b012-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b012-158">Close the page.</span></span>


