---
title: 'ER: konfigūracijos nusiuntimas į „Lifecycle Services‟'
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir ją nusiųsti į „Microsoft Lifecycle Services‟ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5def757de8fb9d347f5fd0f828039dad5c989c19
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143296"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="9b559-103">ER: konfigūracijos nusiuntimas į „Lifecycle Services‟</span><span class="sxs-lookup"><span data-stu-id="9b559-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b559-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir ją nusiųsti į „Microsoft Lifecycle Services‟ (LCS).</span><span class="sxs-lookup"><span data-stu-id="9b559-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="9b559-105">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="9b559-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="9b559-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="9b559-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="9b559-107">Norint atlikti šiuos veiksmus, taip pat reikia prieigos prie LCS.</span><span class="sxs-lookup"><span data-stu-id="9b559-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="9b559-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="9b559-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9b559-109">Pasirinkite „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="9b559-109">Select 'Litware, Inc.'</span></span> <span data-ttu-id="9b559-110">ir nustatykite kaip aktyvią.</span><span class="sxs-lookup"><span data-stu-id="9b559-110">and set it as active.</span></span>
3. <span data-ttu-id="9b559-111">Spustelėkite „Konfigūracijos“.</span><span class="sxs-lookup"><span data-stu-id="9b559-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9b559-112">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="9b559-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="9b559-113">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9b559-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="9b559-114">Sukursite konfigūraciją, apimančią elektroninių dokumentų duomenų modelio pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="9b559-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="9b559-115">Ši duomenų modelio konfigūracija vėliau bus nusiųsta į LCS.</span><span class="sxs-lookup"><span data-stu-id="9b559-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="9b559-116">Lauke Pavadinimas įveskite „Modelio konfigūracijos pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="9b559-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9b559-117">Modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9b559-117">Sample model configuration</span></span>  
3. <span data-ttu-id="9b559-118">Lauke Aprašas įveskite „Modelio konfigūracijos pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="9b559-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9b559-119">Modelio konfigūracijos pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9b559-119">Sample model configuration</span></span>  
4. <span data-ttu-id="9b559-120">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9b559-120">Click Create configuration.</span></span>
5. <span data-ttu-id="9b559-121">Spustelėkite „Modelių kūrimo įrankis“.</span><span class="sxs-lookup"><span data-stu-id="9b559-121">Click Model designer.</span></span>
6. <span data-ttu-id="9b559-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9b559-122">Click New.</span></span>
7. <span data-ttu-id="9b559-123">Lauke Pavadinimas įveskite „Įvesties vieta“.</span><span class="sxs-lookup"><span data-stu-id="9b559-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="9b559-124">Įvesties taškas</span><span class="sxs-lookup"><span data-stu-id="9b559-124">Entry point</span></span>  
8. <span data-ttu-id="9b559-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="9b559-125">Click Add.</span></span>
9. <span data-ttu-id="9b559-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9b559-126">Click Save.</span></span>
10. <span data-ttu-id="9b559-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b559-127">Close the page.</span></span>
11. <span data-ttu-id="9b559-128">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9b559-128">Click Change status.</span></span>
12. <span data-ttu-id="9b559-129">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="9b559-129">Click Complete.</span></span>
13. <span data-ttu-id="9b559-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9b559-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="9b559-131">Naujos saugyklos registravimas</span><span class="sxs-lookup"><span data-stu-id="9b559-131">Register a new  repository</span></span>
1. <span data-ttu-id="9b559-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b559-132">Close the page.</span></span>
2. <span data-ttu-id="9b559-133">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="9b559-133">Click Repositories.</span></span>
    * <span data-ttu-id="9b559-134">Taip galima atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="9b559-135">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="9b559-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="9b559-136">Taip galima įtraukti naują saugyklą.</span><span class="sxs-lookup"><span data-stu-id="9b559-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="9b559-137">Lauke Konfigūracijų saugyklos tipas pasirinkite LCS.</span><span class="sxs-lookup"><span data-stu-id="9b559-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="9b559-138">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="9b559-138">Click Create repository.</span></span>
6. <span data-ttu-id="9b559-139">Lauke Projektas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9b559-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="9b559-140">Pasirinkite norimą LCS projektą.</span><span class="sxs-lookup"><span data-stu-id="9b559-140">Select the desired LCS project.</span></span> <span data-ttu-id="9b559-141">Turite turėti prieigos prie projekto teisę.</span><span class="sxs-lookup"><span data-stu-id="9b559-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="9b559-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9b559-142">Click OK.</span></span>
    * <span data-ttu-id="9b559-143">Baikite naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="9b559-144">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="9b559-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9b559-145">Pasirinkite LCS saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="9b559-146">Atkreipkite dėmesį, kad registruotą saugyklą pažymėjo dabartinis teikėjas, todėl perkelti į šią saugyklą ir vėliau nusiųsti į pasirinktą LCS projektą galima tik tam tiekėjui priklausančias konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="9b559-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="9b559-147">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="9b559-147">Click Open.</span></span>
    * <span data-ttu-id="9b559-148">Atidarę saugyklą galėsite peržiūrėti ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="9b559-149">Jei šis projektas dar nenaudotas bendrinant ER konfigūracijas, sąrašas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="9b559-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="9b559-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b559-150">Close the page.</span></span>
11. <span data-ttu-id="9b559-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b559-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="9b559-152">Konfigūracijos nusiuntimas į LCS</span><span class="sxs-lookup"><span data-stu-id="9b559-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="9b559-153">Spustelėkite „Konfigūracijos“.</span><span class="sxs-lookup"><span data-stu-id="9b559-153">Click Configurations.</span></span>
2. <span data-ttu-id="9b559-154">Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="9b559-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="9b559-155">Pasirinkite sukurtą, jau baigtą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9b559-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="9b559-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9b559-157">Pasirinkite pasirinktos konfigūracijos versiją, kurios būsena – „Baigta“.</span><span class="sxs-lookup"><span data-stu-id="9b559-157">Select the version of the selected configuration with the status of 'Completed'.</span></span>  
4. <span data-ttu-id="9b559-158">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="9b559-158">Click Change status.</span></span>
5. <span data-ttu-id="9b559-159">Spustelėkite Bendrinti.</span><span class="sxs-lookup"><span data-stu-id="9b559-159">Click Share.</span></span>
    * <span data-ttu-id="9b559-160">Kai konfigūracija bus publikuota LCS portale, jos būsena iš „Baigta“ pasikeis į „Bendrai naudojama“.</span><span class="sxs-lookup"><span data-stu-id="9b559-160">The configuration status will change from 'Completed' to 'Shared' when it is published in LCS.</span></span>  
6. <span data-ttu-id="9b559-161">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9b559-161">Click OK.</span></span>
7. <span data-ttu-id="9b559-162">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9b559-163">Pasirinkite konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟.</span><span class="sxs-lookup"><span data-stu-id="9b559-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="9b559-164">Atkreipkite dėmesį, kad pasirinktos versijos būsena pasikeitė iš „Baigta‟ į „Bendrai naudojama‟.</span><span class="sxs-lookup"><span data-stu-id="9b559-164">Note that the status of the selected version has changed from 'Completed' to 'Shared'.</span></span>  
8. <span data-ttu-id="9b559-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b559-165">Close the page.</span></span>
9. <span data-ttu-id="9b559-166">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="9b559-166">Click Repositories.</span></span>
    * <span data-ttu-id="9b559-167">Taip galima atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9b559-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="9b559-168">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="9b559-168">Click Open.</span></span>
    * <span data-ttu-id="9b559-169">Pasirinkite LCS saugyklą ir ją atidarykite.</span><span class="sxs-lookup"><span data-stu-id="9b559-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="9b559-170">Atkreipkite dėmesį, kad pasirinkta konfigūracija rodoma kaip pasirinkto LCS projekto turtas.</span><span class="sxs-lookup"><span data-stu-id="9b559-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="9b559-171">LCS galite atidaryti adresu https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="9b559-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="9b559-172">Atidarykite projektą, kuris buvo ankščiau naudotas registruojant saugyklas, atidarykite šio projekto „Turto biblioteka“ ir išskleiskite turto tipo „GER konfigūracija‟ turinį – bus galima naudoti įkeltą ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="9b559-172">Open a project that was used earlier for repository registration, open the 'Asset library' of this project, and expand the content of the 'GER configuration' asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="9b559-173">Atkreipkite dėmesį, kad, jei tiekėjai turi prieigą prie šio LCS projekto, nusiųstąją LCS konfigūraciją galima importuoti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="9b559-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

