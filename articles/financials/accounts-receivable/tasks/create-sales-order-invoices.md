---
title: Kurti pardavimo užsakymų sąskaitas faktūras
description: Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "353315"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="8706f-103">Kurti pardavimo užsakymų sąskaitas faktūras</span><span class="sxs-lookup"><span data-stu-id="8706f-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8706f-104">Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą.</span><span class="sxs-lookup"><span data-stu-id="8706f-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="8706f-105">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="8706f-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="8706f-106">Iš pardavimo užsakymo kurti SF</span><span class="sxs-lookup"><span data-stu-id="8706f-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="8706f-107">Eikite į Gautinos sumos > Užsakymai > Išsiųsti pardavimo užsakymai, kuriems neišrašytos SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="8706f-108">Sąraše pasirinkite pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8706f-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="8706f-109">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="8706f-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="8706f-110">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="8706f-110">Click Invoice.</span></span>
    * <span data-ttu-id="8706f-111">Atkreipkite dėmesį, kad su šiuo pardavimo užsakymu susieti keli važtaraščiai.</span><span class="sxs-lookup"><span data-stu-id="8706f-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="8706f-112">Vietoj važtaraščio numerio bus rodomas tik žodis  <multiple>.</span><span class="sxs-lookup"><span data-stu-id="8706f-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="8706f-113">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="8706f-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="8706f-114">Norint užregistruoti SF, turi būti nustatyta registravimo parinktis Taip.</span><span class="sxs-lookup"><span data-stu-id="8706f-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="8706f-115">Taip pat galite išjungti registravimą ir tik spausdinti SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="8706f-116">Tačiau tą patį rezultatą galite pasiekti vietoj sąskaitos faktūros sukurdami išankstinę SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="8706f-117">Ši pasirinktis naudojama su paketinėmis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="8706f-117">This option is used for batch jobs.</span></span> <span data-ttu-id="8706f-118">Užklausa vykdoma paleidus paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="8706f-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="8706f-119">Lauke Spausdinti pasirinkite „Vėliau‟.</span><span class="sxs-lookup"><span data-stu-id="8706f-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="8706f-120">Pasirinkite funkcijos Spausdinti SF parinktį Taip.</span><span class="sxs-lookup"><span data-stu-id="8706f-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="8706f-121">Naudojant spausdinimo valdymo funkciją, galima spausdinti kelias SF kopijas ir siųsti SF elektroniniu paštu kaip PDF failą.</span><span class="sxs-lookup"><span data-stu-id="8706f-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="8706f-122">Lauke Spausdinti mokesčius pasirinkite „Apibendrinti‟.</span><span class="sxs-lookup"><span data-stu-id="8706f-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="8706f-123">Lauke Tikrinti kredito limitą pasirinkite „Balansas‟.</span><span class="sxs-lookup"><span data-stu-id="8706f-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="8706f-124">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="8706f-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="8706f-125">Sujungti užsakymus į vieną SF</span><span class="sxs-lookup"><span data-stu-id="8706f-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="8706f-126">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="8706f-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8706f-127">Suraskite klientą, kurio atidarytos kelios SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="8706f-128">Pasirinkite atidarytą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8706f-128">Select an open sales order.</span></span>
4. <span data-ttu-id="8706f-129">Pasirinkite kitą atidarytą to paties kliento pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8706f-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="8706f-130">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="8706f-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="8706f-131">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="8706f-131">Click Invoice.</span></span>
7. <span data-ttu-id="8706f-132">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="8706f-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="8706f-133">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="8706f-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="8706f-134">Atkreipkite dėmesį, kad peržiūros dalyje pateikiamos dvi SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="8706f-135">Suliekime jas į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="8706f-136">Lauke Suminis atnaujinimas pasirinkite „SF sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="8706f-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="8706f-137">Norėdami pardavimo užsakymus sulieti į vieną SF, spustelėkite Išdėstyti.</span><span class="sxs-lookup"><span data-stu-id="8706f-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="8706f-138">Šie du pardavimo užsakymai dabar sulieti į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="8706f-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="8706f-139">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="8706f-139">Click Cancel.</span></span>
12. <span data-ttu-id="8706f-140">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8706f-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="8706f-141">Registruoti SF pakete</span><span class="sxs-lookup"><span data-stu-id="8706f-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="8706f-142">Eikite į Gautinos sumos > Sąskaitos faktūros > Paketinis SF išrašymas > Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="8706f-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="8706f-143">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="8706f-143">Click Select.</span></span>
3. <span data-ttu-id="8706f-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8706f-144">Click OK.</span></span>
4. <span data-ttu-id="8706f-145">Spustelėkite Paketas.</span><span class="sxs-lookup"><span data-stu-id="8706f-145">Click Batch.</span></span>
5. <span data-ttu-id="8706f-146">Jei norite įjungti paketinį vykdymą, spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8706f-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="8706f-147">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="8706f-147">Click Recurrence.</span></span>
7. <span data-ttu-id="8706f-148">Pasirinkite Dienos</span><span class="sxs-lookup"><span data-stu-id="8706f-148">Select Days</span></span>
8. <span data-ttu-id="8706f-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8706f-149">Click OK.</span></span>
9. <span data-ttu-id="8706f-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8706f-150">Click OK.</span></span>
10. <span data-ttu-id="8706f-151">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="8706f-151">Click Cancel.</span></span>
11. <span data-ttu-id="8706f-152">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8706f-152">Click Yes.</span></span>

