---
title: Kurti pardavimo užsakymų sąskaitas faktūras
description: Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d2e1dd552f529d09756c1ddeec39fc54a1f073a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241591"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="7a402-103">Kurti pardavimo užsakymų sąskaitas faktūras</span><span class="sxs-lookup"><span data-stu-id="7a402-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a402-104">Šiame užduočių vadove aprašomas pardavimo užsakymo SF išrašymas, įskaitant SF suliejimą ir paketinį vykdymą.</span><span class="sxs-lookup"><span data-stu-id="7a402-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="7a402-105">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="7a402-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="7a402-106">Iš pardavimo užsakymo kurti SF</span><span class="sxs-lookup"><span data-stu-id="7a402-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="7a402-107">Eikite į **Naršymo sritis > Moduliai >Gautinos sumos > Užsakymai > Išsiųsti pardavimo užsakymai, kuriems neišrašytos SF**.</span><span class="sxs-lookup"><span data-stu-id="7a402-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="7a402-108">Sąraše pasirinkite pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="7a402-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="7a402-109">**Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="7a402-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="7a402-110">Atkreipkite dėmesį, kad su šiuo pardavimo užsakymu susieti keli važtaraščiai.</span><span class="sxs-lookup"><span data-stu-id="7a402-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="7a402-111">Vietoj važtaraščio numerio bus rodomas tik žodis  <multiple>.</span><span class="sxs-lookup"><span data-stu-id="7a402-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="7a402-112">Išplėskite skyrių **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="7a402-113">Norint užregistruoti SF, turi būti nustatyta registravimo parinktis Taip.</span><span class="sxs-lookup"><span data-stu-id="7a402-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="7a402-114">Taip pat galite išjungti registravimą ir tik spausdinti SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="7a402-115">Tačiau tą patį rezultatą galite pasiekti vietoj sąskaitos faktūros sukurdami išankstinę SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="7a402-116">Ši pasirinktis naudojama su paketinėmis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="7a402-116">This option is used for batch jobs.</span></span> <span data-ttu-id="7a402-117">Užklausa vykdoma paleidus paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="7a402-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="7a402-118">Lauke **Spausdinti** pasirinkite „Vėliau”.</span><span class="sxs-lookup"><span data-stu-id="7a402-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="7a402-119">Pasirinkite funkcijos **Spausdinti SF** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7a402-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="7a402-120">Naudojant spausdinimo valdymo funkciją, galima spausdinti kelias SF kopijas ir siųsti SF elektroniniu paštu kaip PDF failą.</span><span class="sxs-lookup"><span data-stu-id="7a402-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="7a402-121">Lauke **Spausdinti mokesčius** pasirinkite „Apibendrinti”.</span><span class="sxs-lookup"><span data-stu-id="7a402-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="7a402-122">Lauke **Tikrinti kredito limitą** pasirinkite „Balansas”.</span><span class="sxs-lookup"><span data-stu-id="7a402-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="7a402-123">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="7a402-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="7a402-124">Sujungti užsakymus į vieną SF</span><span class="sxs-lookup"><span data-stu-id="7a402-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="7a402-125">Eikite į **Valdymo skiltį > Moduliai > Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="7a402-126">Suraskite klientą, kurio atidarytos kelios SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="7a402-127">Pasirinkite kelis atvirus pardavimo užsakymus iš to paties kliento.</span><span class="sxs-lookup"><span data-stu-id="7a402-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="7a402-128">**Veiksmų srityje** spustelėkite **Sąskaita faktūra > Generuoti > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="7a402-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="7a402-129">Išplėskite skyrių **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="7a402-130">Lauke **Kiekis** pasirinkite „Visi‟.</span><span class="sxs-lookup"><span data-stu-id="7a402-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="7a402-131">Atkreipkite dėmesį, kad peržiūros dalyje pateikiamos dvi SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="7a402-132">Suliekime jas į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="7a402-133">Lauke **Suminis atnaujinimas** pasirinkite „SF sąskaita”.</span><span class="sxs-lookup"><span data-stu-id="7a402-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="7a402-134">Norėdami pardavimo užsakymus sulieti į vieną SF, spustelėkite **Išdėstyti**.</span><span class="sxs-lookup"><span data-stu-id="7a402-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="7a402-135">Šie du pardavimo užsakymai dabar sulieti į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="7a402-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="7a402-136">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="7a402-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="7a402-137">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7a402-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="7a402-138">Registruoti SF pakete</span><span class="sxs-lookup"><span data-stu-id="7a402-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="7a402-139">Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Sąskaitos faktūros > Paketinis SF išrašymas > Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="7a402-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="7a402-140">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="7a402-140">Click **Select**.</span></span>
3. <span data-ttu-id="7a402-141">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-141">Click **OK**.</span></span>
4. <span data-ttu-id="7a402-142">Spustelėkite **Paketas**.</span><span class="sxs-lookup"><span data-stu-id="7a402-142">Click **Batch**.</span></span>
5. <span data-ttu-id="7a402-143">Lange **Paketinis vykdymas**, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7a402-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="7a402-144">Spustelėkite **Pasikartojimas**.</span><span class="sxs-lookup"><span data-stu-id="7a402-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="7a402-145">Pasirinkite **Dienos**.</span><span class="sxs-lookup"><span data-stu-id="7a402-145">Select **Days**.</span></span>
8. <span data-ttu-id="7a402-146">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-146">Click **OK**.</span></span>
9. <span data-ttu-id="7a402-147">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7a402-147">Click **OK**.</span></span>
10. <span data-ttu-id="7a402-148">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="7a402-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="7a402-149">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7a402-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]