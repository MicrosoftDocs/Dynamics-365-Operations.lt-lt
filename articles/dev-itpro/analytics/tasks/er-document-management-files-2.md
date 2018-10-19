--- 
title: "ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis – Duomenų modelio išplėtimas)"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="769cf-103">ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis: duomenų modelio išplėtimas)</span><span class="sxs-lookup"><span data-stu-id="769cf-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="769cf-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="769cf-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="769cf-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="769cf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="769cf-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus užduočių vedlyje „ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis: duomenų modelio ruošimas)“.</span><span class="sxs-lookup"><span data-stu-id="769cf-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="769cf-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="769cf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="769cf-108">Duomenų modelio išplėtimas, kad jame būtų pateikti dokumentų valdymo failai</span><span class="sxs-lookup"><span data-stu-id="769cf-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="769cf-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="769cf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="769cf-110">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="769cf-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="769cf-111">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="769cf-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="769cf-112">Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).</span><span class="sxs-lookup"><span data-stu-id="769cf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="769cf-113">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="769cf-113">Click Designer.</span></span>
6. <span data-ttu-id="769cf-114">Medyje pasirinkite Customer invoice(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="769cf-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="769cf-115">Išplėsime šį duomenų modelį, kad jame būtų rodomi visi failai, pridėti prie pardavimo užsakymo, kuris yra susijęs su elektroniniu būdu apdorojama SF.</span><span class="sxs-lookup"><span data-stu-id="769cf-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="769cf-116">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="769cf-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="769cf-117">Lauke Pavadinimas, įveskite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="769cf-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="769cf-118">SF priedai</span><span class="sxs-lookup"><span data-stu-id="769cf-118">Invoice attachments</span></span>  
9. <span data-ttu-id="769cf-119">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="769cf-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="769cf-120">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="769cf-120">Click Add.</span></span>
11. <span data-ttu-id="769cf-121">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="769cf-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="769cf-122">Lauke Pavadinimas įveskite Failo turinys.</span><span class="sxs-lookup"><span data-stu-id="769cf-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="769cf-123">Failo turinys</span><span class="sxs-lookup"><span data-stu-id="769cf-123">File content</span></span>  
13. <span data-ttu-id="769cf-124">Lauke Prekės tipas pasirinkite Konteineris.</span><span class="sxs-lookup"><span data-stu-id="769cf-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="769cf-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="769cf-125">Click Add.</span></span>
15. <span data-ttu-id="769cf-126">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="769cf-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="769cf-127">Lauke Pavadinimas įveskite Failo vardas.</span><span class="sxs-lookup"><span data-stu-id="769cf-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="769cf-128">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="769cf-128">File name</span></span>  
17. <span data-ttu-id="769cf-129">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="769cf-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="769cf-130">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="769cf-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="769cf-131">Naujų duomenų modelio elementų susiejimas su „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="769cf-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="769cf-132">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="769cf-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="769cf-133">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Aprašas pagal reikšmę InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="769cf-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="769cf-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="769cf-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="769cf-135">Susiesime naujo modelio elementus su tinkamais duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="769cf-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="769cf-136">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="769cf-136">Click Designer.</span></span>
4. <span data-ttu-id="769cf-137">Medyje pasirinkite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="769cf-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="769cf-138">Medyje išplėskite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="769cf-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="769cf-139">Medyje pasirinkite Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="769cf-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="769cf-140">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="769cf-140">Click Edit.</span></span>
8. <span data-ttu-id="769cf-141">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'.</span><span class="sxs-lookup"><span data-stu-id="769cf-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="769cf-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="769cf-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="769cf-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="769cf-143">Click Save.</span></span>
10. <span data-ttu-id="769cf-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-144">Close the page.</span></span>
11. <span data-ttu-id="769cf-145">Medyje pasirinkite Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="769cf-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="769cf-146">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="769cf-146">Click Edit.</span></span>
13. <span data-ttu-id="769cf-147">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="769cf-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="769cf-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="769cf-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="769cf-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="769cf-149">Click Save.</span></span>
15. <span data-ttu-id="769cf-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-150">Close the page.</span></span>
16. <span data-ttu-id="769cf-151">Medyje pasirinkite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="769cf-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="769cf-152">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="769cf-152">Click Edit.</span></span>
18. <span data-ttu-id="769cf-153">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.</span><span class="sxs-lookup"><span data-stu-id="769cf-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="769cf-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="769cf-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="769cf-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="769cf-155">Click Save.</span></span>
20. <span data-ttu-id="769cf-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-156">Close the page.</span></span>
21. <span data-ttu-id="769cf-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="769cf-157">Click Save.</span></span>
22. <span data-ttu-id="769cf-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-158">Close the page.</span></span>
23. <span data-ttu-id="769cf-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-159">Close the page.</span></span>
24. <span data-ttu-id="769cf-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="769cf-160">Close the page.</span></span>
25. <span data-ttu-id="769cf-161">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="769cf-161">Click Change status.</span></span>
26. <span data-ttu-id="769cf-162">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="769cf-162">Click Complete.</span></span>
27. <span data-ttu-id="769cf-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="769cf-163">Click OK.</span></span>


