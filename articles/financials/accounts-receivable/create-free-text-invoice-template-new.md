---
title: Kurti laisvos formos SF šabloną
description: Šia procedūra parodoma, kaip sukurti laisvos formos sąskaitos faktūros šabloną.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559508"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="ee849-103">Kurti laisvos formos SF šabloną</span><span class="sxs-lookup"><span data-stu-id="ee849-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee849-104">Su šia išsamia instrukcija naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="ee849-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="ee849-105">Ši procedūra yra skirta vartotojui, kuris yra atsakingas už A/R sąskaitų faktūrų valdymą ir apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="ee849-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="ee849-106">Kurti šabloną</span><span class="sxs-lookup"><span data-stu-id="ee849-106">Create a template</span></span>

1. <span data-ttu-id="ee849-107">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Pasikartojančios SF > Laisvos formos SF šablonai.</span><span class="sxs-lookup"><span data-stu-id="ee849-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="ee849-108">Naudokite šią formą, kad sukurtumėte laisvos formos SF šablonus, kurie gali apimti SF eilutes, mokesčius, apskaitos paskirstymo šabloną ir DK sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="ee849-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="ee849-109">Norėdami sukurti naują laisvos formos SF šabloną, spustelėkite „Naujas‟.</span><span class="sxs-lookup"><span data-stu-id="ee849-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="ee849-110">Lauke Šablono pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee849-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="ee849-111">„Šablono pavadinimas‟ unikaliai identifikuoja laisvos formos SF šabloną.</span><span class="sxs-lookup"><span data-stu-id="ee849-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="ee849-112">Tas pats „Šablono pavadinimas‟ negali būti dviejų šablonų pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="ee849-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="ee849-113">Lauke Aprašas įveskite šablono aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee849-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="ee849-114">Išplėskite skirtuką SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="ee849-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="ee849-115">Lauke Aprašas įveskite SF eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee849-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="ee849-116">Lauke Pagrindinė sąskaita pasirinkite įplaukų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="ee849-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="ee849-117">Bendrosios SF sumos kliento kredito korespondentinę operacijos sąskaitą galima apibrėžti puslapyje Kliento registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="ee849-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="ee849-118">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee849-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ee849-119">Dabartinės SF eilutės PVM grupė yra numatytoji kliento sąskaitos PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="ee849-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="ee849-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee849-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ee849-121">Lauke Prekių mokesčių grupė pasirinkite dabartinės SF eilutės prekių PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="ee849-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="ee849-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee849-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ee849-123">Lauke Vieneto kaina įvesti arba peržiūrėti SF eilutės vieno vieneto kainą</span><span class="sxs-lookup"><span data-stu-id="ee849-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="ee849-124">Ši suma dauginama iš lauko Kiekis, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="ee849-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="ee849-125">Į laisvos formos SF šabloną pridėkite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="ee849-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="ee849-126">Lauke Aprašas įveskite SF eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee849-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="ee849-127">Lauke Pagrindinė sąskaita pasirinkite įplaukų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="ee849-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="ee849-128">Bendrosios SF sumos kliento kredito korespondentinę operacijos sąskaitą galima apibrėžti puslapyje Kliento registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="ee849-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="ee849-129">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee849-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ee849-130">Dabartinės SF eilutės PVM grupė yra numatytoji kliento sąskaitos PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="ee849-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="ee849-131">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee849-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ee849-132">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ee849-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ee849-133">Dabartinės SF eilutės prekės PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="ee849-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="ee849-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee849-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="ee849-135">Įvesti arba peržiūrėti SF eilutės vienetų skaičių</span><span class="sxs-lookup"><span data-stu-id="ee849-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="ee849-136">Šis skaičius dauginamas iš lauko Vieneto kaina reikšmės, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="ee849-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="ee849-137">Įveskite arba peržiūrėkite SF eilutės vieneto kainą.</span><span class="sxs-lookup"><span data-stu-id="ee849-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="ee849-138">Ši suma dauginama iš lauko Kiekis reikšmės, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="ee849-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="ee849-139">Peržiūrėkite ir modifikuokite atskiros eilutės ir visų antrinių eilučių apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="ee849-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="ee849-140">Apskaitos paskirstymai apibrėžia, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="ee849-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="ee849-141">Atnaujinkite pasirinktos SF eilutės apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="ee849-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="ee849-142">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ee849-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="ee849-143">Kaip laisvos formos sąskaitą faktūrą įrašyti kaip šabloną</span><span class="sxs-lookup"><span data-stu-id="ee849-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="ee849-144">Esamą laisvos formos sąskaitą faktūrą taip galite įrašyti kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="ee849-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="ee849-145">Skirtuke Sąskaita faktūra pasirinkę Įrašyti į šabloną, nurodykite šablono pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ee849-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="ee849-146">Jei šablonas tokiu pavadinimu jau yra, matysite pranešimą, kad šablonas tokiu pavadinimu jau yra.</span><span class="sxs-lookup"><span data-stu-id="ee849-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="ee849-147">Vis tiek galite spustelėti Gerai ir jį pakeisti.</span><span class="sxs-lookup"><span data-stu-id="ee849-147">You can still click on Ok to replace it.</span></span> 
