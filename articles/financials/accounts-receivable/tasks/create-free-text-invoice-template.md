--- 
title: "Kurti laisvos formos SF šabloną"
description: "Šiame įraše naudojama demonstracinė įmonė USMF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="1f3cc-103">Kurti laisvos formos SF šabloną</span><span class="sxs-lookup"><span data-stu-id="1f3cc-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f3cc-104">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="1f3cc-105">Įrašas yra skirtas naudotojui, kuris yra atsakingas už A/R SF valdymą ir apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="1f3cc-106">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Pasikartojančios SF > Laisvos formos SF šablonai.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="1f3cc-107">Naudokite šią formą, kad sukurtumėte laisvos formos SF šablonus, kurie gali apimti SF eilutes, mokesčius, apskaitos paskirstymo šabloną ir DK sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="1f3cc-108">Norėdami sukurti naują laisvos formos SF šabloną, spustelėkite „Naujas‟.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="1f3cc-109">Lauke Šablono pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="1f3cc-110">„Šablono pavadinimas‟ unikaliai identifikuoja laisvos formos SF šabloną.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="1f3cc-111">Tas pats „Šablono pavadinimas‟ negali būti dviejų šablonų pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="1f3cc-112">Lauke Aprašas įveskite šablono aprašą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="1f3cc-113">Išplėskite skirtuką SF eilutės.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="1f3cc-114">Lauke Aprašas įveskite SF eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="1f3cc-115">Lauke Pagrindinė sąskaita pasirinkite įplaukų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="1f3cc-116">Bendrosios SF sumos kliento kredito korespondentinę operacijos sąskaitą galima apibrėžti puslapyje Kliento registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="1f3cc-117">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1f3cc-118">Dabartinės SF eilutės PVM grupė yra numatytoji kliento sąskaitos PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="1f3cc-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1f3cc-120">Lauke Prekių mokesčių grupė pasirinkite dabartinės SF eilutės prekių PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="1f3cc-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1f3cc-122">Lauke Vieneto kaina įvesti arba peržiūrėti SF eilutės vieno vieneto kainą</span><span class="sxs-lookup"><span data-stu-id="1f3cc-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="1f3cc-123">Ši suma dauginama iš lauko Kiekis, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="1f3cc-124">Į laisvos formos SF šabloną pridėkite naują eilutę.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="1f3cc-125">Lauke Aprašas įveskite SF eilutės aprašą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="1f3cc-126">Lauke Pagrindinė sąskaita pasirinkite įplaukų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="1f3cc-127">Bendrosios SF sumos kliento kredito korespondentinę operacijos sąskaitą galima apibrėžti puslapyje Kliento registravimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="1f3cc-128">Lauke PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1f3cc-129">Dabartinės SF eilutės PVM grupė yra numatytoji kliento sąskaitos PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="1f3cc-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1f3cc-131">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1f3cc-132">Dabartinės SF eilutės prekės PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="1f3cc-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="1f3cc-134">Įvesti arba peržiūrėti SF eilutės vienetų skaičių</span><span class="sxs-lookup"><span data-stu-id="1f3cc-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="1f3cc-135">Šis skaičius dauginamas iš lauko Vieneto kaina reikšmės, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="1f3cc-136">Įveskite arba peržiūrėkite SF eilutės vieneto kainą.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="1f3cc-137">Ši suma dauginama iš lauko Kiekis reikšmės, kad būtų nustatyta SF eilutės suma.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="1f3cc-138">Peržiūrėkite ir modifikuokite atskiros eilutės ir visų antrinių eilučių apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="1f3cc-139">Apskaitos paskirstymai apibrėžia, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="1f3cc-140">Atnaujinkite pasirinktos SF eilutės apskaitos paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="1f3cc-141">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="1f3cc-141">Click Close.</span></span>


