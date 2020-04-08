---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis – Duomenų modelio ruošimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 800df13e1654bc01304411bfa52f4bbd04e6589a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142068"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="23a66-103">ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis – Duomenų modelio ruošimas)</span><span class="sxs-lookup"><span data-stu-id="23a66-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23a66-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="23a66-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="23a66-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="23a66-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="23a66-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="23a66-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="23a66-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="23a66-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="23a66-108">Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo</span><span class="sxs-lookup"><span data-stu-id="23a66-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="23a66-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="23a66-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="23a66-110">Įsitikinkite, kad teikėjas „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="23a66-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="23a66-111">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="23a66-111">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="23a66-112">Pasirinkite „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="23a66-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="23a66-113">„Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="23a66-113">provider.</span></span>
3. <span data-ttu-id="23a66-114">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="23a66-114">Click Repositories.</span></span>

    <span data-ttu-id="23a66-115">Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23a66-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="23a66-116">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="23a66-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="23a66-117">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="23a66-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="23a66-118">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="23a66-118">Click Create repository.</span></span>
7. <span data-ttu-id="23a66-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="23a66-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="23a66-120">Gaukite Kliento SF modelio konfigūracijas, kurias teikia „Microsoft“</span><span class="sxs-lookup"><span data-stu-id="23a66-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="23a66-121">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="23a66-121">Click Show filters.</span></span>
2. <span data-ttu-id="23a66-122">Taikykite toliau nurodytus filtrus: lauke Pavadinimas įveskite filtro reikšmę Operacijų ištekliai, naudodami filtro operatorių Prasideda; lauke Aprašas įveskite filtro reikšmę "", naudodami filtro operatorių Prasideda</span><span class="sxs-lookup"><span data-stu-id="23a66-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="23a66-123">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="23a66-123">Click Show filters.</span></span>
4. <span data-ttu-id="23a66-124">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="23a66-124">Click Open.</span></span>
5. <span data-ttu-id="23a66-125">Medyje pasirinkite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="23a66-125">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="23a66-126">Pasirinkite modelio konfigūraciją Kliento SF modelis, kad ją importuotumėte.</span><span class="sxs-lookup"><span data-stu-id="23a66-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="23a66-127">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="23a66-127">Click Import.</span></span>

    <span data-ttu-id="23a66-128">Spustelėkite Importuoti 1 pasirinktos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="23a66-128">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="23a66-129">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="23a66-129">Click Yes.</span></span>
8. <span data-ttu-id="23a66-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="23a66-130">Close the page.</span></span>
9. <span data-ttu-id="23a66-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="23a66-131">Close the page.</span></span>
10. <span data-ttu-id="23a66-132">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="23a66-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="23a66-133">Medyje pasirinkite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="23a66-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="23a66-134">Kurkite išvestinį modelį, norėdami palaikyti prieigą prie dokumentų valdymo failų.</span><span class="sxs-lookup"><span data-stu-id="23a66-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="23a66-135">Savo kliento SF modelio konfigūraciją sukursite pagal „Microsoft“ pateiktą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="23a66-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="23a66-136">Šią konfigūraciją galima naudoti norint suteikti prieigą prie dokumentų valdymo failų ir nustatyti, kad juos būtų galima naudoti elektroniniuose dokumentuose, kuriuos sukursite pagal šį modelį.</span><span class="sxs-lookup"><span data-stu-id="23a66-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="23a66-137">Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="23a66-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="23a66-138">Lauke Naujas įveskite Kildinti iš pavadinimo: kliento SF modelis, „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="23a66-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="23a66-139">Lauke Pavadinimas įveskite Kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="23a66-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="23a66-140">Spustelėkite Sukurti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="23a66-140">Click Create configuration.</span></span>

