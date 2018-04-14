--- 
title: "Modelio susiejimo konfigūracijos kūrimas (ER)"
description: "Naudokite šią procedūrą norėdami sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a6bfea86ee0d299c634783d869e4828bcf3a9d38
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-model-mapping-configuration-er"></a><span data-ttu-id="1c167-103">Modelio susiejimo konfigūracijos kūrimas (ER)</span><span class="sxs-lookup"><span data-stu-id="1c167-103">Create a model mapping configuration (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c167-104">Naudokite šią procedūrą norėdami sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1c167-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="1c167-105">Šioje procedūroje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1c167-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="1c167-106">Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas.</span><span class="sxs-lookup"><span data-stu-id="1c167-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="1c167-107">Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="1c167-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="1c167-108">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="1c167-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="1c167-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="1c167-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="1c167-110">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="1c167-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="1c167-111">Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1c167-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="1c167-112">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="1c167-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1c167-113">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="1c167-113">Click Show filters.</span></span>
4. <span data-ttu-id="1c167-114">Lauke „Pavadinimas“ įveskite filtro reikšmę „Intrastat” ir naudokite filtro operatorių „prasideda”.</span><span class="sxs-lookup"><span data-stu-id="1c167-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="1c167-115">Taikykite šį filtrą norėdami rasti „Intrastat“ duomenų modelio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1c167-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="1c167-116">Šis modelis jau gali būti konfigūracijos medyje.</span><span class="sxs-lookup"><span data-stu-id="1c167-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="1c167-117">Jei taip atsitiktų, praleiskite kitą antrinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="1c167-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="1c167-118">Gaukite „Microsoft“ teikiamas Intrastat modelio konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="1c167-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="1c167-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c167-119">Close the page.</span></span>
2. <span data-ttu-id="1c167-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c167-120">Close the page.</span></span>
3. <span data-ttu-id="1c167-121">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="1c167-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="1c167-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1c167-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1c167-123">Pasirinkite plytelę „Microsoft“ teikėjas.</span><span class="sxs-lookup"><span data-stu-id="1c167-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="1c167-124">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="1c167-124">Click Repositories.</span></span>
    * <span data-ttu-id="1c167-125">Plytelėje „Microsoft“ teikėjas spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="1c167-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="1c167-126">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="1c167-126">Click Show filters.</span></span>
7. <span data-ttu-id="1c167-127">Lauke „Įveskite pavadinimą“ įveskite filtro reikšmę „ištekliai” ir naudokite filtro operatorių „apima”.</span><span class="sxs-lookup"><span data-stu-id="1c167-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="1c167-128">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="1c167-128">Click Open.</span></span>
9. <span data-ttu-id="1c167-129">Medyje pasirinkite „Intrastat model“ (Intrastat modelis).</span><span class="sxs-lookup"><span data-stu-id="1c167-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="1c167-130">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="1c167-130">Click Import.</span></span>
11. <span data-ttu-id="1c167-131">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="1c167-131">Click Yes.</span></span>
    * <span data-ttu-id="1c167-132">Importavote ER modelio konfigūraciją, kurioje yra duomenų modelis, kurį naudosite norėdami ištirti, kaip gali būti naudojama nauja ER funkcija.</span><span class="sxs-lookup"><span data-stu-id="1c167-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="1c167-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c167-133">Close the page.</span></span>
13. <span data-ttu-id="1c167-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c167-134">Close the page.</span></span>
14. <span data-ttu-id="1c167-135">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="1c167-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="1c167-136">Pridėti naują modelio susiejimo konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="1c167-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="1c167-137">Medyje pasirinkite „Intrastat model“ (Intrastat modelis).</span><span class="sxs-lookup"><span data-stu-id="1c167-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="1c167-138">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1c167-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="1c167-139">Lauke Naujas įveskite „Modelio susiejimas pagal duomenų modelio Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="1c167-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="1c167-140">Lauke Pavadinimas įveskite „Intrastat pavyzdžio susiejimas“.</span><span class="sxs-lookup"><span data-stu-id="1c167-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="1c167-141">„Intrastat“ pavyzdžio susiejimas</span><span class="sxs-lookup"><span data-stu-id="1c167-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="1c167-142">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1c167-142">Click Create configuration.</span></span>


