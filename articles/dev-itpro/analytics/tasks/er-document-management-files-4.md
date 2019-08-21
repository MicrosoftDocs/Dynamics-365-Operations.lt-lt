---
title: Formato, skirto dokumentų valdymo failams naudoti ER išvestyje, taikymas
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų formatą, norėdamas dokumentų valdymo failus naudoti ER išvestyje.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850260"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a><span data-ttu-id="caf87-103">ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis: formato paleidimas)</span><span class="sxs-lookup"><span data-stu-id="caf87-103">ER Use Document Management files in format outputs (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="caf87-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="caf87-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="caf87-105">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="caf87-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="caf87-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (3 dalis: formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="caf87-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="caf87-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="caf87-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="caf87-108">Pridėkite reikiamus vienos SF pardavimo užsakymo priedus</span><span class="sxs-lookup"><span data-stu-id="caf87-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="caf87-109">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Atidarytos klientų SF.</span><span class="sxs-lookup"><span data-stu-id="caf87-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="caf87-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="caf87-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="caf87-111">Pvz., filtruokite lauką SF reikšme CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="caf87-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="caf87-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="caf87-112">CIV-000148</span></span>  
3. <span data-ttu-id="caf87-113">Spustelėkite norėdami sekti pažymėtos SF saitą.</span><span class="sxs-lookup"><span data-stu-id="caf87-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="caf87-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="caf87-114">CIV-000148</span></span>  
4. <span data-ttu-id="caf87-115">Spustelėkite, jei norite atidaryti lauke Pardavimo užsakymas esantį saitą.</span><span class="sxs-lookup"><span data-stu-id="caf87-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="caf87-116">000148</span><span class="sxs-lookup"><span data-stu-id="caf87-116">000148</span></span>  
5. <span data-ttu-id="caf87-117">Lauke Eilutės arba antraštė pasirinkite parinktį Antraštė.</span><span class="sxs-lookup"><span data-stu-id="caf87-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="caf87-118">Pasirinkite Antraštė, norėdami nurodyti, kad tai bus priedų pridėjimo paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="caf87-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="caf87-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="caf87-119">Click Attach.</span></span>
    * <span data-ttu-id="caf87-120">Įtraukite kelis failus kaip šio pardavimo užsakymo priedus.</span><span class="sxs-lookup"><span data-stu-id="caf87-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="caf87-121">Naudokite dokumentų tipų, kuriuos palaiko dokumentų valdymas, failus (su failų plėtiniais DOCX, DPF, XML, JPG, ir pan.).</span><span class="sxs-lookup"><span data-stu-id="caf87-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="caf87-122">Naršykite ir pasirinkite failus, kuriuos norite pridėti ir apdoroti su susijusia SF ER el. laiške.</span><span class="sxs-lookup"><span data-stu-id="caf87-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="caf87-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="caf87-123">Click New.</span></span>
8. <span data-ttu-id="caf87-124">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="caf87-124">Click File.</span></span>
9. <span data-ttu-id="caf87-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="caf87-125">Click New.</span></span>
10. <span data-ttu-id="caf87-126">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="caf87-126">Click File.</span></span>
11. <span data-ttu-id="caf87-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="caf87-127">Close the page.</span></span>
12. <span data-ttu-id="caf87-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="caf87-128">Close the page.</span></span>
13. <span data-ttu-id="caf87-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="caf87-129">Close the page.</span></span>
14. <span data-ttu-id="caf87-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="caf87-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="caf87-131">Paleiskite sukurtą pasirinktos SF ataskaitą</span><span class="sxs-lookup"><span data-stu-id="caf87-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="caf87-132">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="caf87-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="caf87-133">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="caf87-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="caf87-134">Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="caf87-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="caf87-135">Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="caf87-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="caf87-136">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="caf87-136">Click Run.</span></span>
6. <span data-ttu-id="caf87-137">Išplėskite dalį Įtrauktini įrašai ().</span><span class="sxs-lookup"><span data-stu-id="caf87-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="caf87-138">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="caf87-138">Click Filter.</span></span>
8. <span data-ttu-id="caf87-139">Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="caf87-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="caf87-140">Lauke Kriterijai įveskite 000148.</span><span class="sxs-lookup"><span data-stu-id="caf87-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="caf87-141">Kriterijų lauke Pardavimo užsakymas įveskite užsakymo numerį 000148.</span><span class="sxs-lookup"><span data-stu-id="caf87-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="caf87-142">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="caf87-142">Click OK.</span></span>
11. <span data-ttu-id="caf87-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="caf87-143">Click OK.</span></span>
    * <span data-ttu-id="caf87-144">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="caf87-144">Review the generated output.</span></span> <span data-ttu-id="caf87-145">Atkreipkite dėmesį, kad kiekvienam priedui sukuriamas vienas XML mazgas.</span><span class="sxs-lookup"><span data-stu-id="caf87-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="caf87-146">Priedo turinys įvedamas į XML išvestį MIME (base64) teksto formatu.</span><span class="sxs-lookup"><span data-stu-id="caf87-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

