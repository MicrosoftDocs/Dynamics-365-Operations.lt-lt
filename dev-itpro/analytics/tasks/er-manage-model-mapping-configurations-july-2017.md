--- 
title: "Modelių susiejimo konfigūracijų valdymas elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali valdyti elektroninių ataskaitų (ER) modelio susiejimus atskirose ER konfigūracijose."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 473cad588253b0eb42eb927834e186ccfa4c4f1e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a><span data-ttu-id="336f6-103">Modelių susiejimo konfigūracijų valdymas elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="336f6-103">Manage model mapping configurations for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="336f6-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali valdyti elektroninių ataskaitų (ER) modelio susiejimus atskirose ER konfigūracijose.</span><span class="sxs-lookup"><span data-stu-id="336f6-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="336f6-105">Šiame užduočių vedlyje kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Norėdami atlikti užduočių vedlio veiksmus, pirmiausia turite užbaigti užduočių vedlio „ER: konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="336f6-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="336f6-106">Kadangi įmonės dalijasi ER konfigūracijomis, galite baigti šį užduočių vedlį, naudodami jūsų pasirinktą įmonės duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="336f6-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="336f6-107">Šio užduočių vedlio funkcijas galima naudoti, jei įdiegėte vieną iš tolesnių karštųjų pataisų: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872, skirtą „Dynamics AX“ 7.0 versijai arba https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871, skirtą „Dynamics 365 for Operations“ versijai.</span><span class="sxs-lookup"><span data-stu-id="336f6-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="336f6-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="336f6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="336f6-109">Patikrinkite, ar pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra galimas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="336f6-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="336f6-110">Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti užduočių vedlio „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu” veiksmus.</span><span class="sxs-lookup"><span data-stu-id="336f6-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="336f6-111">Įtraukti naują ER modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="336f6-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="336f6-112">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="336f6-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="336f6-113">Pridėkite naują modelio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-113">Add a new model configuration.</span></span> <span data-ttu-id="336f6-114">Pavadinimas turi būti unikalus konfigūracijos medyje.</span><span class="sxs-lookup"><span data-stu-id="336f6-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="336f6-115">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="336f6-116">Lauke Pavadinimas įrašykite „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="336f6-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="336f6-117">Duomenų modelio pavyzdys</span><span class="sxs-lookup"><span data-stu-id="336f6-117">Sample data model</span></span>  
4. <span data-ttu-id="336f6-118">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-118">Click Create configuration.</span></span>
5. <span data-ttu-id="336f6-119">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-119">Click Designer.</span></span>
6. <span data-ttu-id="336f6-120">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="336f6-121">Lauke Pavadinimas įveskite Šaknis.</span><span class="sxs-lookup"><span data-stu-id="336f6-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="336f6-122">Šaknis</span><span class="sxs-lookup"><span data-stu-id="336f6-122">Root</span></span>  
8. <span data-ttu-id="336f6-123">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="336f6-123">Click Add.</span></span>
9. <span data-ttu-id="336f6-124">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="336f6-125">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="336f6-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="336f6-126">Įmonė</span><span class="sxs-lookup"><span data-stu-id="336f6-126">Company</span></span>  
11. <span data-ttu-id="336f6-127">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="336f6-127">Click Add.</span></span>
12. <span data-ttu-id="336f6-128">Lauke Aprašymas įveskite tekstą, juridinio subjekto arba įmonės, kurioje vartotojas prisijungęs vykdymo metu, aprašymą.</span><span class="sxs-lookup"><span data-stu-id="336f6-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="336f6-129">Juridinio subjekto arba įmonės, kurioje vartotojas prisijungęs vykdymo metu, aprašymas.</span><span class="sxs-lookup"><span data-stu-id="336f6-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="336f6-130">Spustelėkite Šakninė nuoroda.</span><span class="sxs-lookup"><span data-stu-id="336f6-130">Click Root reference.</span></span>
14. <span data-ttu-id="336f6-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-131">Click OK.</span></span>
15. <span data-ttu-id="336f6-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-132">Click Save.</span></span>
16. <span data-ttu-id="336f6-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-133">Close the page.</span></span>
17. <span data-ttu-id="336f6-134">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="336f6-134">Click Change status.</span></span>
18. <span data-ttu-id="336f6-135">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="336f6-135">Click Complete.</span></span>
19. <span data-ttu-id="336f6-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="336f6-137">Pridėkite naują ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="336f6-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="336f6-138">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="336f6-139">Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="336f6-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="336f6-140">Lauke Pavadinimas įrašykite „Susiejimo pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="336f6-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="336f6-141">Susiejimo pavyzdys</span><span class="sxs-lookup"><span data-stu-id="336f6-141">Sample mapping</span></span>  
4. <span data-ttu-id="336f6-142">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-142">Click Create configuration.</span></span>
5. <span data-ttu-id="336f6-143">Išplėskite sekciją Išankstiniai reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="336f6-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="336f6-144">Žinokite, kad išankstinių reikalavimų grupė „Įgyvendinimas“ pridėta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="336f6-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="336f6-145">Grupėje yra išankstinio reikalavimo komponentas, kuris nurodo pirminių duomenų modelio konfigūraciją ir yra pažymėtas kaip Įgyvendinimas.</span><span class="sxs-lookup"><span data-stu-id="336f6-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="336f6-146">Tai reiškia, kad ši susiejimo modelio pavyzdžio konfigūracija skirta duomenų modelio „Duomenų modelio pavyzdys“ įgyvendinimui.</span><span class="sxs-lookup"><span data-stu-id="336f6-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="336f6-147">Todėl šis komponentas privers ER atsisiųsti modelio susiejimo konfigūraciją „Susiejimo pavyzdys“ iš ER saugyklos kai bus atsisiunčiama modelio konfigūracija „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="336f6-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="336f6-148">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-148">Click Designer.</span></span>
    * <span data-ttu-id="336f6-149">Atkreipkite dėmesį, kad sukurto modelio susiejimo konfigūracijoje yra naujas tuščias susiejimas tokiu pačiu pavadinimu, kaip sukurta konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="336f6-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="336f6-150">Žinokite, kad kai pasirinktoje pirminio modelio konfigūracijoje yra modelio susiejimų, jie bus nukopijuoti į naują modelio susiejimo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="336f6-151">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-151">Click Designer.</span></span>
8. <span data-ttu-id="336f6-152">Medyje pasirinkite „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="336f6-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="336f6-153">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="336f6-153">Click Add root.</span></span>
10. <span data-ttu-id="336f6-154">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="336f6-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="336f6-155">Įmonė</span><span class="sxs-lookup"><span data-stu-id="336f6-155">Company</span></span>  
11. <span data-ttu-id="336f6-156">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="336f6-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="336f6-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="336f6-157">CompanyInfo</span></span>  
12. <span data-ttu-id="336f6-158">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-158">Click OK.</span></span>
13. <span data-ttu-id="336f6-159">Medyje išplėskite „Company“.</span><span class="sxs-lookup"><span data-stu-id="336f6-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="336f6-160">Medyje išplėskite „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="336f6-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="336f6-161">Medyje pasirinkite „Company\find()\Name“.</span><span class="sxs-lookup"><span data-stu-id="336f6-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="336f6-162">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="336f6-162">Click Bind.</span></span>
17. <span data-ttu-id="336f6-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-163">Click Save.</span></span>
18. <span data-ttu-id="336f6-164">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-164">Close the page.</span></span>
19. <span data-ttu-id="336f6-165">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-165">Close the page.</span></span>
20. <span data-ttu-id="336f6-166">Veiksmų srityje spustelėkite Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="336f6-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="336f6-167">Spustelėkite Vartotojo parametrai.</span><span class="sxs-lookup"><span data-stu-id="336f6-167">Click User parameters.</span></span>
22. <span data-ttu-id="336f6-168">Lauke Paleisti parametrus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="336f6-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="336f6-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-169">Click OK.</span></span>
24. <span data-ttu-id="336f6-170">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="336f6-170">Click Edit.</span></span>
25. <span data-ttu-id="336f6-171">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="336f6-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="336f6-172">Įtraukite naują ER formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="336f6-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="336f6-173">Medyje pasirinkite „Sample data model“.</span><span class="sxs-lookup"><span data-stu-id="336f6-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="336f6-174">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="336f6-175">Lauke Naujas įveskite „Formatas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="336f6-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="336f6-176">Lauke Pavadinimas įrašykite „Formato pavyzdys‟.</span><span class="sxs-lookup"><span data-stu-id="336f6-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="336f6-177">Formato pavyzdys</span><span class="sxs-lookup"><span data-stu-id="336f6-177">Sample format</span></span>  
5. <span data-ttu-id="336f6-178">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-178">Click Create configuration.</span></span>
6. <span data-ttu-id="336f6-179">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-179">Click Designer.</span></span>
7. <span data-ttu-id="336f6-180">Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="336f6-181">Medyje pasirinkite „Tekstas \ Eilutė‟.</span><span class="sxs-lookup"><span data-stu-id="336f6-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="336f6-182">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-182">Click OK.</span></span>
10. <span data-ttu-id="336f6-183">Spustelėkite skirtuką „Susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="336f6-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="336f6-184">Medyje išplėskite „modelis‟.</span><span class="sxs-lookup"><span data-stu-id="336f6-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="336f6-185">Medyje pasirinkite „model\Company“.</span><span class="sxs-lookup"><span data-stu-id="336f6-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="336f6-186">Spustelėkite Susieti.</span><span class="sxs-lookup"><span data-stu-id="336f6-186">Click Bind.</span></span>
14. <span data-ttu-id="336f6-187">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-187">Click Save.</span></span>
15. <span data-ttu-id="336f6-188">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-188">Close the page.</span></span>
    * <span data-ttu-id="336f6-189">Vykdykite sukurto formato projekto versiją bandymams.</span><span class="sxs-lookup"><span data-stu-id="336f6-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="336f6-190">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-190">Click Run.</span></span>
    * <span data-ttu-id="336f6-191">Versijos FastTab spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="336f6-192">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-192">Click OK.</span></span>
    * <span data-ttu-id="336f6-193">Peržiūrėkite išvestį, kurioje yra įmonės pavadinimas, kurioje vartotojas, kuris vykdo šią formato konfigūraciją, prisijungęs.</span><span class="sxs-lookup"><span data-stu-id="336f6-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="336f6-194">Žinokite, kad sukurtą modelio susiejimo konfigūraciją naudoja ši formato konfigūracija, nes yra tik viena konfigūracija, kurioje yra reikalingi modelio susiejimai.</span><span class="sxs-lookup"><span data-stu-id="336f6-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="336f6-195">Pridėkite alternatyvią ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="336f6-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="336f6-196">Medyje pasirinkite „Sample data model“.</span><span class="sxs-lookup"><span data-stu-id="336f6-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="336f6-197">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="336f6-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="336f6-198">Lauke Naujas įveskite „Modelio susiejimas, pagrįstas duomenų modeliu „Duomenų modelio pavyzdys“.</span><span class="sxs-lookup"><span data-stu-id="336f6-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="336f6-199">Lauke Pavadinimas įrašykite „Susiejimo pavyzdys (alternatyva)“.</span><span class="sxs-lookup"><span data-stu-id="336f6-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="336f6-200">Susiejimo pavyzdys (alternatyva)</span><span class="sxs-lookup"><span data-stu-id="336f6-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="336f6-201">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="336f6-201">Click Create configuration.</span></span>
6. <span data-ttu-id="336f6-202">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-202">Click Designer.</span></span>
7. <span data-ttu-id="336f6-203">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="336f6-203">Click Designer.</span></span>
8. <span data-ttu-id="336f6-204">Medyje pasirinkite „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="336f6-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="336f6-205">Spustelėkite „Įtraukti šaknį“.</span><span class="sxs-lookup"><span data-stu-id="336f6-205">Click Add root.</span></span>
10. <span data-ttu-id="336f6-206">Lauke „Pavadinimas“ įveskite „Įmonė“.</span><span class="sxs-lookup"><span data-stu-id="336f6-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="336f6-207">Įmonė</span><span class="sxs-lookup"><span data-stu-id="336f6-207">Company</span></span>  
11. <span data-ttu-id="336f6-208">Lauke „Lentelė“, įveskite „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="336f6-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="336f6-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="336f6-209">CompanyInfo</span></span>  
12. <span data-ttu-id="336f6-210">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-210">Click OK.</span></span>
13. <span data-ttu-id="336f6-211">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="336f6-211">Click Edit.</span></span>
14. <span data-ttu-id="336f6-212">Medyje pasirinkite „Eilutė \ SUJUNGTI“.</span><span class="sxs-lookup"><span data-stu-id="336f6-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="336f6-213">Spustelėkite „Įtraukti funkciją“.</span><span class="sxs-lookup"><span data-stu-id="336f6-213">Click Add function.</span></span>
16. <span data-ttu-id="336f6-214">Medyje išplėskite „Company“.</span><span class="sxs-lookup"><span data-stu-id="336f6-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="336f6-215">Medyje išplėskite „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="336f6-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="336f6-216">Medyje pasirinkite „Company\find()\Name“.</span><span class="sxs-lookup"><span data-stu-id="336f6-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="336f6-217">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="336f6-217">Click Add data source.</span></span>
20. <span data-ttu-id="336f6-218">Lauke „Formulė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="336f6-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="336f6-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="336f6-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="336f6-220">Medyje pasirinkite „Company\find()\Company(DataArea)“.</span><span class="sxs-lookup"><span data-stu-id="336f6-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="336f6-221">Spustelėkite „Įtraukti duomenų šaltinį“.</span><span class="sxs-lookup"><span data-stu-id="336f6-221">Click Add data source.</span></span>
23. <span data-ttu-id="336f6-222">Lauke „Formulė“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="336f6-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="336f6-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="336f6-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="336f6-224">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-224">Click Save.</span></span>
25. <span data-ttu-id="336f6-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-225">Close the page.</span></span>
26. <span data-ttu-id="336f6-226">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-226">Click Save.</span></span>
27. <span data-ttu-id="336f6-227">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-227">Close the page.</span></span>
28. <span data-ttu-id="336f6-228">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="336f6-228">Close the page.</span></span>
29. <span data-ttu-id="336f6-229">Lauke Paleisti juodraštį pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="336f6-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="336f6-230">Naudokite esamą ER modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="336f6-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="336f6-231">Medyje pasirinkite „Sample data model\Sample format“.</span><span class="sxs-lookup"><span data-stu-id="336f6-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="336f6-232">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-232">Click Run.</span></span>
    * <span data-ttu-id="336f6-233">Atkreipkite dėmesį, kad pasirinktos ER formato konfigūracijos projekto versijos vykdyti negalima, nes yra daugiau kaip viena modelio susiejimo konfigūracija, prieinama neapibrėžtam duomenų modeliui, kuris buvo pasirinktas kaip veikiančio ER formato duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="336f6-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="336f6-234">toliau jūs apibrėšite alternatyvią modelio susiejimo konfigūraciją, kaip tą, iš kurios bus naudojami modelio susiejimai kaip duomenų šaltiniai veikiančiam ER formatui.</span><span class="sxs-lookup"><span data-stu-id="336f6-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="336f6-235">Medyje pasirinkite „Sample data model\Sample mapping (alternative)“.</span><span class="sxs-lookup"><span data-stu-id="336f6-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="336f6-236">Lauke Numatytoji modelio susiejimo reikšmė pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="336f6-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="336f6-237">Medyje pasirinkite „Sample data model\Sample format“.</span><span class="sxs-lookup"><span data-stu-id="336f6-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="336f6-238">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="336f6-238">Click Run.</span></span>
7. <span data-ttu-id="336f6-239">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="336f6-239">Click OK.</span></span>
    * <span data-ttu-id="336f6-240">Atkreipkite dėmesį, kad numatytąją modelio susiejimo konfigūraciją naudoja ši formato konfigūracija elektroniniam dokumentui generuoti (sukurtoje išvestyje yra įmonės kodas).</span><span class="sxs-lookup"><span data-stu-id="336f6-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  


