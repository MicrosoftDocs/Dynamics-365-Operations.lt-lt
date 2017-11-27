---
title: "Pasikartojančių SF nustatymas ir apdorojimas"
description: "Šiame straipsnyje paaiškinta, kaip nustatyti ir apdoroti pasikartojančias SF. Pasikartojančias SF galite naudoti, jei klientams reguliariai turite išrašyti SF už tą pačią sumą."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c5fbe1791161b8d06cd1539b1717ba8690a8e05
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="76820-104">Pasikartojančių SF nustatymas ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="76820-104">Set up and process recurring invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76820-105">Šiame straipsnyje paaiškinta, kaip nustatyti ir apdoroti pasikartojančias SF.</span><span class="sxs-lookup"><span data-stu-id="76820-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="76820-106">Pasikartojančias SF galite naudoti, jei klientams reguliariai turite išrašyti SF už tą pačią sumą.</span><span class="sxs-lookup"><span data-stu-id="76820-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="76820-107">Periodinio laisvos formos SF šablono sukūrimas</span><span class="sxs-lookup"><span data-stu-id="76820-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="76820-108">Norėdami reguliariai siųsti klientams SF už tas pačias paslaugas, turite nustatyti laisvos formos SF šabloną, kurį būtų galima pakartotinai naudoti SF kurti.</span><span class="sxs-lookup"><span data-stu-id="76820-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="76820-109">Šiame šablone pateikiama ši informacija:</span><span class="sxs-lookup"><span data-stu-id="76820-109">This template contains the following information:</span></span>

-   <span data-ttu-id="76820-110">Antraštės informacija, pvz., mokesčių grupės, mokėjimo sąlygos ir mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="76820-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="76820-111">Eilutės informacija, pvz., aptarnavimo aprašymas, įplaukų sąskaitos, vieneto kaina ir SF suma</span><span class="sxs-lookup"><span data-stu-id="76820-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="76820-112">Siuntimo ar tvarkymo išlaidos</span><span class="sxs-lookup"><span data-stu-id="76820-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="76820-113">Apskaitos paskirstymai kartu su finansinės dimensijos informaciją, pvz., išlaidų centrai ir verslo vienetai</span><span class="sxs-lookup"><span data-stu-id="76820-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="76820-114">Iš esmės jūs sukuriate visą SF ir išsaugote ją kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="76820-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="76820-115">Galite nustatyti šablonus naudodami puslapį **Pasikartojančios SF**.</span><span class="sxs-lookup"><span data-stu-id="76820-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="76820-116">Pasikartojančio laisvos formos SF šablono priskyrimas klientui ir pasikartojančios informacijos įvedimas</span><span class="sxs-lookup"><span data-stu-id="76820-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="76820-117">Sukūrę šabloną, turite jį priskirti klientams, kuriems norite išrašyti SF.</span><span class="sxs-lookup"><span data-stu-id="76820-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="76820-118">Be to, turite nurodyti, kada ir kaip dažnai ši SF bus naudojama.</span><span class="sxs-lookup"><span data-stu-id="76820-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="76820-119">Galite priskirti šablonus puslapio **Klientai** skirtuke **SF**.</span><span class="sxs-lookup"><span data-stu-id="76820-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="76820-120">Įtraukite šabloną į sąrašą ir atnaujinkite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="76820-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="76820-121">Pasikartojančių sąskaitų teikimo pradžios data ir, pasirinktinai, pabaigos data</span><span class="sxs-lookup"><span data-stu-id="76820-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="76820-122">Kaip dažnai siunčiamos pasikartojančios sąskaitos (pvz., kiekvieną dieną arba vieną kartą per mėnesį)</span><span class="sxs-lookup"><span data-stu-id="76820-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="76820-123">Didžiausia sąskaitos suma (jei ši informacija yra būtina)</span><span class="sxs-lookup"><span data-stu-id="76820-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="76820-124">Klientas gali turėti kelis skirtingo dažnumo šablonus.</span><span class="sxs-lookup"><span data-stu-id="76820-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="76820-125">Pasikartojančių SF generavimas</span><span class="sxs-lookup"><span data-stu-id="76820-125">Generate the recurring invoices</span></span>
<span data-ttu-id="76820-126">Puslapyje **Pasikartojančios SF**yra užduotis, kuri apdoroja pasikartojančių SF šablonus.</span><span class="sxs-lookup"><span data-stu-id="76820-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="76820-127">Galite nurodyti SF datą ir šabloną, pagal kurį generuosite SF.</span><span class="sxs-lookup"><span data-stu-id="76820-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="76820-128">Bus sugeneruotos SF ir kiekvienai apdorotai SF grupei priskirtas atskiras pasikartojimo ID numeris.</span><span class="sxs-lookup"><span data-stu-id="76820-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>
<span data-ttu-id="76820-129">Pasikartojančių laisvos formos SF registravimas</span><span class="sxs-lookup"><span data-stu-id="76820-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="76820-130">Sugeneravus pasikartojančias SF, SF pasikartojimo ID rodomas registravimo užduotyje puslapyje **Pasikartojančios SF**.</span><span class="sxs-lookup"><span data-stu-id="76820-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="76820-131">Galite peržiūrėti visas pasikartojimo ID SF spustelėdami saitą.</span><span class="sxs-lookup"><span data-stu-id="76820-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="76820-132">Peržiūrėdami pasikartojimo ID SF galite panaikinti atskiras SF.</span><span class="sxs-lookup"><span data-stu-id="76820-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="76820-133">Kliento pasikartojimo parametrai tame šablone bus nustatyti iš naujo, kad vėliau jį būtų galima vėl sugeneruoti.</span><span class="sxs-lookup"><span data-stu-id="76820-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="76820-134">Galite registruoti vieną, kelias arba visas pasikartojimo ID SF.</span><span class="sxs-lookup"><span data-stu-id="76820-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="76820-135">Jei įgalintos darbo eigos, turite spustelėti **Pateikti**, tada galėsite registruoti SF.</span><span class="sxs-lookup"><span data-stu-id="76820-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>
<span data-ttu-id="76820-136">Pasikartojančių laisvos formos SF spausdinimas</span><span class="sxs-lookup"><span data-stu-id="76820-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="76820-137">Užregistravę pasikartojančias SF, galite spausdinti SF laisvos formos SF sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="76820-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="76820-138">Galite spausdinti SF, kurios yra pasirinktos, arba galite pasirinkti spausdinti SF diapazoną.</span><span class="sxs-lookup"><span data-stu-id="76820-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>




