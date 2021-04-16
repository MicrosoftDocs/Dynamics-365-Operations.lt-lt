---
title: ER dokumentų valdymo failų naudojimas formato išvestyse (4 dalis – formato paleidimas)
description: Šioje temoje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų formatą, kad būtų galima naudoti dokumentų valdymo failus ER išvestyje. (4 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749122"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="dbc7b-104">ER dokumentų valdymo failų naudojimas formato išvestyse (4 dalis – formato paleidimas)</span><span class="sxs-lookup"><span data-stu-id="dbc7b-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbc7b-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="dbc7b-106">Šiuos veiksmus galima atlikti DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="dbc7b-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (3 dalis. Formato kūrimas)“.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="dbc7b-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="dbc7b-109">Pridėkite reikiamus vienos SF pardavimo užsakymo priedus</span><span class="sxs-lookup"><span data-stu-id="dbc7b-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="dbc7b-110">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Atidarytos klientų SF.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="dbc7b-111">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dbc7b-112">Pvz., filtruokite lauką SF reikšme CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="dbc7b-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="dbc7b-113">CIV-000148</span></span>  
3. <span data-ttu-id="dbc7b-114">Spustelėkite norėdami sekti pažymėtos SF saitą.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="dbc7b-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="dbc7b-115">CIV-000148</span></span>  
4. <span data-ttu-id="dbc7b-116">Spustelėkite, jei norite atidaryti lauke Pardavimo užsakymas esantį saitą.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="dbc7b-117">000148</span><span class="sxs-lookup"><span data-stu-id="dbc7b-117">000148</span></span>  
5. <span data-ttu-id="dbc7b-118">Lauke Eilutės arba antraštė pasirinkite parinktį Antraštė.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="dbc7b-119">Pasirinkite Antraštė, norėdami nurodyti, kad tai bus priedų pridėjimo paskirties vieta.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="dbc7b-120">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-120">Click Attach.</span></span>
    * <span data-ttu-id="dbc7b-121">Įtraukite kelis failus kaip šio pardavimo užsakymo priedus.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="dbc7b-122">Naudokite dokumentų tipų, kuriuos palaiko dokumentų valdymas, failus (su failų plėtiniais DOCX, DPF, XML, JPG, ir pan.).</span><span class="sxs-lookup"><span data-stu-id="dbc7b-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="dbc7b-123">Naršykite ir pasirinkite failus, kuriuos norite pridėti ir apdoroti su susijusia SF ER el. laiške.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="dbc7b-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-124">Click New.</span></span>
8. <span data-ttu-id="dbc7b-125">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-125">Click File.</span></span>
9. <span data-ttu-id="dbc7b-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-126">Click New.</span></span>
10. <span data-ttu-id="dbc7b-127">Spustelėkite Failas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-127">Click File.</span></span>
11. <span data-ttu-id="dbc7b-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-128">Close the page.</span></span>
12. <span data-ttu-id="dbc7b-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-129">Close the page.</span></span>
13. <span data-ttu-id="dbc7b-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-130">Close the page.</span></span>
14. <span data-ttu-id="dbc7b-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="dbc7b-132">Paleiskite sukurtą pasirinktos SF ataskaitą</span><span class="sxs-lookup"><span data-stu-id="dbc7b-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="dbc7b-133">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="dbc7b-134">Medyje išplėskite Kliento SF modelis.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="dbc7b-135">Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).</span><span class="sxs-lookup"><span data-stu-id="dbc7b-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="dbc7b-136">Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="dbc7b-137">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-137">Click Run.</span></span>
6. <span data-ttu-id="dbc7b-138">Išplėskite dalį Įtrauktini įrašai ().</span><span class="sxs-lookup"><span data-stu-id="dbc7b-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="dbc7b-139">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-139">Click Filter.</span></span>
8. <span data-ttu-id="dbc7b-140">Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="dbc7b-141">Lauke Kriterijai įveskite 000148.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="dbc7b-142">Kriterijų lauke „Pardavimo užsakymas“ įveskite užsakymo numerį 000148.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="dbc7b-143">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-143">Click OK.</span></span>
11. <span data-ttu-id="dbc7b-144">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-144">Click OK.</span></span>
    * <span data-ttu-id="dbc7b-145">Peržiūrėkite sugeneruotą išvestį.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-145">Review the generated output.</span></span> <span data-ttu-id="dbc7b-146">Atkreipkite dėmesį, kad kiekvienam priedui sukuriamas vienas XML mazgas.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="dbc7b-147">Priedo turinys įvedamas į XML išvestį MIME (base64) teksto formatu.</span><span class="sxs-lookup"><span data-stu-id="dbc7b-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]