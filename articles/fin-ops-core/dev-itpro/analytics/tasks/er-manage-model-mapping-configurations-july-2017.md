---
title: Atskirų ER konfigūracijų ER modelio susiejimo valdymas
description: Šioje temoje aprašoma, kaip valdyti elektroninių ataskaitų (ER) modelių susiejimus atskirose ER konfigūracijose.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f1013cfc9f421525fb0661cd5ace5eeaa157f9a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093803"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="d63ae-103">Atskirų ER konfigūracijų ER modelio susiejimo valdymas</span><span class="sxs-lookup"><span data-stu-id="d63ae-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d63ae-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali valdyti elektroninių ataskaitų (ER) modelio susiejimus atskirose ER konfigūracijose.</span><span class="sxs-lookup"><span data-stu-id="d63ae-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="d63ae-105">Šiame užduočių vedlyje kursite reikiamas kaip pavyzdys pateiktos įmonės „Litware, Inc.“ ER konfigūracijas. Norėdami atlikti užduočių vedlio veiksmus, pirmiausia turite atlikti užduočių vedlio „ER: konfigūracijų teikėjo kūrimas ir pažymėjimas aktyviu“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d63ae-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="d63ae-106">Kadangi įmonės dalijasi ER konfigūracijomis, galite baigti šį užduočių vedlį, naudodami jūsų pasirinktą įmonės duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="d63ae-107">Šio užduočių vedlio funkcijas galima naudoti, jei įdiegėte vieną iš tolesnių karštųjų pataisų: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872, skirtą „Dynamics AX“ 7.0 versijai arba https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871, skirtą „Dynamics 365 for Operations“ versijai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="d63ae-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="d63ae-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d63ae-109">Patikrinkite, ar pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra galimas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="d63ae-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="d63ae-110">Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti užduočių vedlio „Konfigūracijų teikėjo kūrimas ir pažymėjimas aktyviu” veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d63ae-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="d63ae-111">Įtraukti naują ER modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="d63ae-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="d63ae-112">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="d63ae-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="d63ae-113">Pridėkite naują modelio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-113">Add a new model configuration.</span></span> <span data-ttu-id="d63ae-114">Pavadinimas turi būti unikalus konfigūracijos medyje.</span><span class="sxs-lookup"><span data-stu-id="d63ae-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="d63ae-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d63ae-116">Lauke Pavadinimas įrašykite „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="d63ae-117">Duomenų modelio pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d63ae-117">Sample data model</span></span>  
4. <span data-ttu-id="d63ae-118">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-118">Click Create configuration.</span></span>
5. <span data-ttu-id="d63ae-119">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-119">Click Designer.</span></span>
6. <span data-ttu-id="d63ae-120">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d63ae-121">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="d63ae-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="d63ae-122">Šaknis</span><span class="sxs-lookup"><span data-stu-id="d63ae-122">Root</span></span>  
8. <span data-ttu-id="d63ae-123">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-123">Click Add.</span></span>
9. <span data-ttu-id="d63ae-124">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="d63ae-125">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d63ae-126">Įmonė</span><span class="sxs-lookup"><span data-stu-id="d63ae-126">Company</span></span>  
11. <span data-ttu-id="d63ae-127">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-127">Click Add.</span></span>
12. <span data-ttu-id="d63ae-128">Lauke Aprašymas įveskite tekstą, juridinio subjekto arba įmonės, kurioje vartotojas prisijungęs vykdymo metu, aprašymą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="d63ae-129">Juridinio subjekto arba įmonės, kurioje vartotojas prisijungęs vykdymo metu, aprašymas.</span><span class="sxs-lookup"><span data-stu-id="d63ae-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="d63ae-130">Spustelėkite Šakninė nuoroda.</span><span class="sxs-lookup"><span data-stu-id="d63ae-130">Click Root reference.</span></span>
14. <span data-ttu-id="d63ae-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-131">Click OK.</span></span>
15. <span data-ttu-id="d63ae-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-132">Click Save.</span></span>
16. <span data-ttu-id="d63ae-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-133">Close the page.</span></span>
17. <span data-ttu-id="d63ae-134">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="d63ae-134">Click Change status.</span></span>
18. <span data-ttu-id="d63ae-135">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-135">Click Complete.</span></span>
19. <span data-ttu-id="d63ae-136">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="d63ae-137">Pridėkite naują ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="d63ae-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="d63ae-138">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d63ae-139">Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="d63ae-140">Lauke Pavadinimas įrašykite „Susiejimo pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="d63ae-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="d63ae-141">Susiejimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d63ae-141">Sample mapping</span></span>  
4. <span data-ttu-id="d63ae-142">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-142">Click Create configuration.</span></span>
5. <span data-ttu-id="d63ae-143">Išplėskite sekciją Išankstiniai reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="d63ae-144">Išankstinių reikalavimų grupė „Įgyvendinimas“ pridėta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="d63ae-145">Grupėje yra išankstinio reikalavimo komponentas, kuris nurodo pirminių duomenų modelio konfigūraciją ir yra pažymėtas kaip Įgyvendinimas.</span><span class="sxs-lookup"><span data-stu-id="d63ae-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="d63ae-146">Tai reiškia, kad ši susiejimo modelio pavyzdžio konfigūracija skirta duomenų modelio „Duomenų modelio pavyzdys“ įgyvendinimui.</span><span class="sxs-lookup"><span data-stu-id="d63ae-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="d63ae-147">Todėl šis komponentas privers ER atsisiųsti modelio susiejimo konfigūraciją „Susiejimo pavyzdys“ iš ER saugyklos kai bus atsisiunčiama modelio konfigūracija „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="d63ae-148">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-148">Click Designer.</span></span>
    * <span data-ttu-id="d63ae-149">Sukurto modelio susiejimo konfigūracijoje yra naujas tuščias susiejimas tokiu pačiu pavadinimu, kaip sukurta konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="d63ae-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="d63ae-150">Kai pasirinktoje pirminio modelio konfigūracijoje yra modelio susiejimų, jie bus nukopijuoti į naują modelio susiejimo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="d63ae-151">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-151">Click Designer.</span></span>
8. <span data-ttu-id="d63ae-152">Medyje pasirinkite Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="d63ae-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d63ae-153">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-153">Click Add root.</span></span>
10. <span data-ttu-id="d63ae-154">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d63ae-155">Įmonė</span><span class="sxs-lookup"><span data-stu-id="d63ae-155">Company</span></span>  
11. <span data-ttu-id="d63ae-156">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d63ae-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d63ae-157">CompanyInfo</span></span>  
12. <span data-ttu-id="d63ae-158">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-158">Click OK.</span></span>
13. <span data-ttu-id="d63ae-159">Medyje išplėskite „Company“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="d63ae-160">Medyje išplėskite „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="d63ae-161">Medyje pasirinkite „Company\find()\Name“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="d63ae-162">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-162">Click Bind.</span></span>
17. <span data-ttu-id="d63ae-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-163">Click Save.</span></span>
18. <span data-ttu-id="d63ae-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-164">Close the page.</span></span>
19. <span data-ttu-id="d63ae-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-165">Close the page.</span></span>
20. <span data-ttu-id="d63ae-166">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="d63ae-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="d63ae-167">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-167">Click User parameters.</span></span>
22. <span data-ttu-id="d63ae-168">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d63ae-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="d63ae-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-169">Click OK.</span></span>
24. <span data-ttu-id="d63ae-170">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-170">Click Edit.</span></span>
25. <span data-ttu-id="d63ae-171">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d63ae-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="d63ae-172">Įtraukite naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="d63ae-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="d63ae-173">Medyje pasirinkite „Sample data model“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d63ae-174">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d63ae-175">Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d63ae-176">Lauke Pavadinimas įrašykite „Formato pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="d63ae-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="d63ae-177">Formato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d63ae-177">Sample format</span></span>  
5. <span data-ttu-id="d63ae-178">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-178">Click Create configuration.</span></span>
6. <span data-ttu-id="d63ae-179">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-179">Click Designer.</span></span>
7. <span data-ttu-id="d63ae-180">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="d63ae-181">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="d63ae-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="d63ae-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-182">Click OK.</span></span>
10. <span data-ttu-id="d63ae-183">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="d63ae-184">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="d63ae-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="d63ae-185">Medyje pasirinkite „model\Company“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="d63ae-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-186">Click Bind.</span></span>
14. <span data-ttu-id="d63ae-187">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-187">Click Save.</span></span>
15. <span data-ttu-id="d63ae-188">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-188">Close the page.</span></span>
    * <span data-ttu-id="d63ae-189">Vykdykite sukurto formato projekto versiją bandymams.</span><span class="sxs-lookup"><span data-stu-id="d63ae-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="d63ae-190">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-190">Click Run.</span></span>
    * <span data-ttu-id="d63ae-191">Versijos FastTab spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="d63ae-192">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-192">Click OK.</span></span>
    * <span data-ttu-id="d63ae-193">Peržiūrėkite išvestį, kurioje yra įmonės pavadinimas, kurioje vartotojas, kuris vykdo šią formato konfigūraciją, prisijungęs.</span><span class="sxs-lookup"><span data-stu-id="d63ae-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="d63ae-194">Sukurtą modelio susiejimo konfigūraciją naudoja ši formato konfigūracija, nes yra tik viena konfigūracija, kurioje yra reikalingi modelio susiejimai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="d63ae-195">Pridėkite alternatyvią ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="d63ae-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="d63ae-196">Medyje pasirinkite „Sample data model“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="d63ae-197">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d63ae-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d63ae-198">Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="d63ae-199">Lauke Pavadinimas įrašykite „Susiejimo pavyzdys (alternatyva)“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="d63ae-200">Susiejimo pavyzdys (alternatyva)</span><span class="sxs-lookup"><span data-stu-id="d63ae-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="d63ae-201">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d63ae-201">Click Create configuration.</span></span>
6. <span data-ttu-id="d63ae-202">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-202">Click Designer.</span></span>
7. <span data-ttu-id="d63ae-203">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="d63ae-203">Click Designer.</span></span>
8. <span data-ttu-id="d63ae-204">Medyje pasirinkite Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="d63ae-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="d63ae-205">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-205">Click Add root.</span></span>
10. <span data-ttu-id="d63ae-206">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="d63ae-207">Įmonė</span><span class="sxs-lookup"><span data-stu-id="d63ae-207">Company</span></span>  
11. <span data-ttu-id="d63ae-208">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="d63ae-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="d63ae-209">CompanyInfo</span></span>  
12. <span data-ttu-id="d63ae-210">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d63ae-210">Click OK.</span></span>
13. <span data-ttu-id="d63ae-211">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-211">Click Edit.</span></span>
14. <span data-ttu-id="d63ae-212">Medyje pasirinkite „Eilutė \ SUJUNGTI“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="d63ae-213">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-213">Click Add function.</span></span>
16. <span data-ttu-id="d63ae-214">Medyje išplėskite „Company“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="d63ae-215">Medyje išplėskite „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="d63ae-216">Medyje pasirinkite „Company\find()\Name“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="d63ae-217">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-217">Click Add data source.</span></span>
20. <span data-ttu-id="d63ae-218">Lauke „Formulė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d63ae-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d63ae-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="d63ae-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="d63ae-220">Medyje pasirinkite „Company\find()\Company(DataArea)“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="d63ae-221">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-221">Click Add data source.</span></span>
23. <span data-ttu-id="d63ae-222">Lauke „Formulė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d63ae-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="d63ae-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="d63ae-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="d63ae-224">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-224">Click Save.</span></span>
25. <span data-ttu-id="d63ae-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-225">Close the page.</span></span>
26. <span data-ttu-id="d63ae-226">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-226">Click Save.</span></span>
27. <span data-ttu-id="d63ae-227">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-227">Close the page.</span></span>
28. <span data-ttu-id="d63ae-228">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d63ae-228">Close the page.</span></span>
29. <span data-ttu-id="d63ae-229">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d63ae-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="d63ae-230">Naudokite esamą ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="d63ae-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="d63ae-231">Medyje pasirinkite „Sample data model\Sample format“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="d63ae-232">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-232">Click Run.</span></span>
    * <span data-ttu-id="d63ae-233">Pasirinktos ER formato konfigūracijos projekto versijos vykdyti negalima, nes yra daugiau kaip viena modelio susiejimo konfigūracija, prieinama neapibrėžtam duomenų modeliui, kuris buvo pasirinktas kaip vykdomo ER formato duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="d63ae-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="d63ae-234">toliau jūs apibrėšite alternatyvią modelio susiejimo konfigūraciją, kaip tą, iš kurios bus naudojami modelio susiejimai kaip duomenų šaltiniai veikiančiam ER formatui.</span><span class="sxs-lookup"><span data-stu-id="d63ae-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="d63ae-235">Medyje pasirinkite „Sample data model\Sample mapping (alternative)“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="d63ae-236">Lauke Numatytoji modelio susiejimo reikšmė pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d63ae-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="d63ae-237">Medyje pasirinkite „Sample data model\Sample format“.</span><span class="sxs-lookup"><span data-stu-id="d63ae-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="d63ae-238">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d63ae-238">Click Run.</span></span>
7. <span data-ttu-id="d63ae-239">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="d63ae-239">Click OK.</span></span>
    * <span data-ttu-id="d63ae-240">Numatytąją modelio susiejimo konfigūraciją naudoja ši formato konfigūracija elektroniniam dokumentui generuoti (sukurtoje išvestyje yra įmonės kodas).</span><span class="sxs-lookup"><span data-stu-id="d63ae-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

