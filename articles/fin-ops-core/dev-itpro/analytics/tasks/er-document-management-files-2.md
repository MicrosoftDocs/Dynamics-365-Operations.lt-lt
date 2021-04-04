---
title: 'ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis – Duomenų modelio išplėtimas)'
description: Šioje temoje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų (ER) formatą, kad būtų galima naudoti dokumentų valdymo failus (priedus) ER išvestyje. (2 dalis)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559778"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="f1025-104">ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis – Duomenų modelio išplėtimas)</span><span class="sxs-lookup"><span data-stu-id="f1025-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1025-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="f1025-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f1025-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="f1025-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f1025-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus užduočių vedlyje „ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis. Duomenų modelio ruošimas)“.</span><span class="sxs-lookup"><span data-stu-id="f1025-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="f1025-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="f1025-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="f1025-109">Duomenų modelio išplėtimas, kad jame būtų pateikti dokumentų valdymo failai</span><span class="sxs-lookup"><span data-stu-id="f1025-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="f1025-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="f1025-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f1025-111">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f1025-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f1025-112">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="f1025-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="f1025-113">Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).</span><span class="sxs-lookup"><span data-stu-id="f1025-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="f1025-114">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f1025-114">Click Designer.</span></span>
6. <span data-ttu-id="f1025-115">Medyje pasirinkite Customer invoice(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="f1025-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="f1025-116">Išplėsime šį duomenų modelį, kad jame būtų rodomi visi failai, pridėti prie pardavimo užsakymo, kuris yra susijęs su elektroniniu būdu apdorojama SF.</span><span class="sxs-lookup"><span data-stu-id="f1025-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="f1025-117">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f1025-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f1025-118">Lauke Pavadinimas, įveskite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="f1025-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="f1025-119">SF priedai</span><span class="sxs-lookup"><span data-stu-id="f1025-119">Invoice attachments</span></span>  
9. <span data-ttu-id="f1025-120">Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.</span><span class="sxs-lookup"><span data-stu-id="f1025-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="f1025-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f1025-121">Click Add.</span></span>
11. <span data-ttu-id="f1025-122">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f1025-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="f1025-123">Lauke Pavadinimas įveskite Failo turinys.</span><span class="sxs-lookup"><span data-stu-id="f1025-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="f1025-124">Failo turinys</span><span class="sxs-lookup"><span data-stu-id="f1025-124">File content</span></span>  
13. <span data-ttu-id="f1025-125">Lauke Prekės tipas pasirinkite Konteineris.</span><span class="sxs-lookup"><span data-stu-id="f1025-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="f1025-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f1025-126">Click Add.</span></span>
15. <span data-ttu-id="f1025-127">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f1025-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="f1025-128">Lauke Pavadinimas įveskite Failo vardas.</span><span class="sxs-lookup"><span data-stu-id="f1025-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="f1025-129">Failo vardas</span><span class="sxs-lookup"><span data-stu-id="f1025-129">File name</span></span>  
17. <span data-ttu-id="f1025-130">Lauke „Prekės tipas“ pasirinkite „Eilutė“.</span><span class="sxs-lookup"><span data-stu-id="f1025-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="f1025-131">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f1025-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="f1025-132">Naujo duomenų modelio elementų susiejimas su duomenų šaltiniais</span><span class="sxs-lookup"><span data-stu-id="f1025-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="f1025-133">Spustelėkite „Susieti modelį su duomenų šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="f1025-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="f1025-134">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Aprašas pagal reikšmę InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="f1025-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="f1025-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="f1025-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="f1025-136">Susiesime naujo modelio elementus su tinkamais duomenų šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="f1025-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="f1025-137">Spustelėkite Konstruktorius.</span><span class="sxs-lookup"><span data-stu-id="f1025-137">Click Designer.</span></span>
4. <span data-ttu-id="f1025-138">Medyje pasirinkite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="f1025-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="f1025-139">Medyje išplėskite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="f1025-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="f1025-140">Medyje pasirinkite Invoice attachments\File name.</span><span class="sxs-lookup"><span data-stu-id="f1025-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="f1025-141">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f1025-141">Click Edit.</span></span>
8. <span data-ttu-id="f1025-142">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'.</span><span class="sxs-lookup"><span data-stu-id="f1025-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="f1025-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="f1025-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="f1025-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1025-144">Click Save.</span></span>
10. <span data-ttu-id="f1025-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-145">Close the page.</span></span>
11. <span data-ttu-id="f1025-146">Medyje pasirinkite Invoice attachments\File content.</span><span class="sxs-lookup"><span data-stu-id="f1025-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="f1025-147">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f1025-147">Click Edit.</span></span>
13. <span data-ttu-id="f1025-148">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="f1025-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="f1025-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="f1025-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="f1025-150">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1025-150">Click Save.</span></span>
15. <span data-ttu-id="f1025-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-151">Close the page.</span></span>
16. <span data-ttu-id="f1025-152">Medyje pasirinkite SF priedai.</span><span class="sxs-lookup"><span data-stu-id="f1025-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="f1025-153">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f1025-153">Click Edit.</span></span>
18. <span data-ttu-id="f1025-154">Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.</span><span class="sxs-lookup"><span data-stu-id="f1025-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="f1025-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="f1025-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="f1025-156">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1025-156">Click Save.</span></span>
20. <span data-ttu-id="f1025-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-157">Close the page.</span></span>
21. <span data-ttu-id="f1025-158">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f1025-158">Click Save.</span></span>
22. <span data-ttu-id="f1025-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-159">Close the page.</span></span>
23. <span data-ttu-id="f1025-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-160">Close the page.</span></span>
24. <span data-ttu-id="f1025-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f1025-161">Close the page.</span></span>
25. <span data-ttu-id="f1025-162">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="f1025-162">Click Change status.</span></span>
26. <span data-ttu-id="f1025-163">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="f1025-163">Click Complete.</span></span>
27. <span data-ttu-id="f1025-164">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1025-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]