--- 
title: "ER: konfigūracijos importavimas iš „Lifecycle Services‟"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Lifecycle Services‟ (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---

# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="dc199-103">ER: konfigūracijos importavimas iš „Lifecycle Services‟</span><span class="sxs-lookup"><span data-stu-id="dc199-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc199-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Lifecycle Services‟ (LCS).</span><span class="sxs-lookup"><span data-stu-id="dc199-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="dc199-105">Šiame pavyzdyje pasirinksite pavyzdinės įmonės „Litware, Inc“ pageidaujamą ER konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="dc199-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="dc199-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „ER konfigūracijos nusiuntimas į „Lifecycle Services‟“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc199-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="dc199-107">Norint atlikti šiuos veiksmus, taip pat reikia prieigos prie LCS.</span><span class="sxs-lookup"><span data-stu-id="dc199-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="dc199-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="dc199-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="dc199-109">Spustelėkite „Konfigūracijos“.</span><span class="sxs-lookup"><span data-stu-id="dc199-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="dc199-110">Duomenų modelio konfigūracijos bendrai naudojamos versijos naikinimas</span><span class="sxs-lookup"><span data-stu-id="dc199-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="dc199-111">Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="dc199-112">Pirmoji modelio konfigūracijos pavyzdžio versija sukurta ir publikuota LCS portale atliekant procedūrą „ER konfigūracijos nusiuntimas į „Lifecycle Services‟‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="dc199-113">Atlikdami šią procedūrą, šią ER konfigūracijos versiją panaikinsite.</span><span class="sxs-lookup"><span data-stu-id="dc199-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="dc199-114">Ši pavyzdžio duomenų modelio konfigūracijos versija bus importuota vėliau iš LCS.</span><span class="sxs-lookup"><span data-stu-id="dc199-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="dc199-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dc199-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc199-116">Pasirinkite šios konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="dc199-117">Ši būsena nurodo, kad konfigūracija publikuota LCS portale.</span><span class="sxs-lookup"><span data-stu-id="dc199-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="dc199-118">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="dc199-118">Click Change status.</span></span>
4. <span data-ttu-id="dc199-119">Spustelėkite Nebenaudoti.</span><span class="sxs-lookup"><span data-stu-id="dc199-119">Click Discontinue.</span></span>
    * <span data-ttu-id="dc199-120">Kad galėtumėte pasirinktą versiją panaikinti, jos būseną pakeiskite iš „Bendrai naudojama" į „Nebenaudojama‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="dc199-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="dc199-121">Click OK.</span></span>
6. <span data-ttu-id="dc199-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dc199-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc199-123">Pasirinkite šios konfigūracijos versiją, kurios būsena – „Nebenaudojama‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="dc199-124">Spustelėkite Naikinti.</span><span class="sxs-lookup"><span data-stu-id="dc199-124">Click Delete.</span></span>
8. <span data-ttu-id="dc199-125">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dc199-125">Click Yes.</span></span>
    * <span data-ttu-id="dc199-126">Atkreipkite dėmesį, kad galima naudoti tik 2 pasirinktos duomenų modelio konfigūracijos juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="dc199-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="dc199-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dc199-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="dc199-128">Duomenų modelio konfigūracijos bendrai naudojamos versijos importavimas iš LCS</span><span class="sxs-lookup"><span data-stu-id="dc199-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="dc199-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dc199-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dc199-130">Atidarykite „Litware, Inc.‟ konfigūracijų teikėjo</span><span class="sxs-lookup"><span data-stu-id="dc199-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="dc199-131">saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="dc199-131">configuration provider.</span></span>  
2. <span data-ttu-id="dc199-132">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="dc199-132">Click Repositories.</span></span>
3. <span data-ttu-id="dc199-133">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="dc199-133">Click Open.</span></span>
    * <span data-ttu-id="dc199-134">Pasirinkite LCS saugyklą ir ją atidarykite.</span><span class="sxs-lookup"><span data-stu-id="dc199-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="dc199-135">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dc199-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dc199-136">Versijų sąraše pasirinkite pirmąją modelio konfigūracijos pavyzdžio versiją.</span><span class="sxs-lookup"><span data-stu-id="dc199-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="dc199-137">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="dc199-137">Click Import.</span></span>
6. <span data-ttu-id="dc199-138">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dc199-138">Click Yes.</span></span>
    * <span data-ttu-id="dc199-139">Patvirtinkite pasirinktos versijos importavimą iš LCS.</span><span class="sxs-lookup"><span data-stu-id="dc199-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="dc199-140">Atkreipkite dėmesį, kad informaciniu pranešimu (virš formos) patvirtinamas sėkmingas pasirinktos versijos importavimas.</span><span class="sxs-lookup"><span data-stu-id="dc199-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="dc199-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dc199-141">Close the page.</span></span>
8. <span data-ttu-id="dc199-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dc199-142">Close the page.</span></span>
9. <span data-ttu-id="dc199-143">Spustelėkite „Konfigūracijos“.</span><span class="sxs-lookup"><span data-stu-id="dc199-143">Click Configurations.</span></span>
10. <span data-ttu-id="dc199-144">Medyje pasirinkite „Modelio konfigūracijos pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="dc199-145">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dc199-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc199-146">Pasirinkite šios konfigūracijos versiją, kurios būsena – „Bendrai naudojama‟.</span><span class="sxs-lookup"><span data-stu-id="dc199-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="dc199-147">Atkreipkite dėmesį, kad dabar taip pat galima naudoti ir 1 pasirinktos duomenų modelio konfigūracijos bendrai naudojamą versiją.</span><span class="sxs-lookup"><span data-stu-id="dc199-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


