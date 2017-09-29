--- 
title: "Kurti laisvos formos sąskaitą faktūrą"
description: "Šis užduočių vadovas parodo, kaip sukurti laisvos formos SF."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="2a1ce-103">Kurti laisvos formos sąskaitą faktūrą</span><span class="sxs-lookup"><span data-stu-id="2a1ce-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a1ce-104">Šis užduočių vadovas parodo, kaip sukurti laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="2a1ce-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2a1ce-106">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="2a1ce-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-107">Click New.</span></span>
3. <span data-ttu-id="2a1ce-108">Lauke Kliento sąskaita pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="2a1ce-109">Pagal numatytąsias nuostatas SF sąskaita bus ta pati, kuri naudojama kaip kliento sąskaita.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="2a1ce-110">Jei SF neužregistruota, pirmoji apskaitos būsena yra Vykdoma.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="2a1ce-111">SF numeris bus priskirtas užregistravus SF.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="2a1ce-112">Jei naudojate SEPA įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas bus automatiškai užpildytas įgaliojimu.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="2a1ce-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2a1ce-114">Lauke Pagrindinė sąskaita nurodykite sąskaitos numerį be dimensijų.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="2a1ce-115">Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="2a1ce-116">Dimensijas įvesite vėliau šiame vadove.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="2a1ce-117">Išplėtę „FastTab‟ Išsami eilutės informacija, galėsite į savo pagrindinę sąskaitą pridėti dimensijų.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="2a1ce-118">Spustelėkite skirtuką Finansinių dimensijų eilutė.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="2a1ce-119">Nurodytos tik pasirinktos eilutės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="2a1ce-120">PVM grupė automatiškai užpildoma pagal klientą.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="2a1ce-121">Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="2a1ce-122">Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="2a1ce-123">Jei pagrindinė sąskaita neturi prekių PVM grupės, tada naudojama prekių PVM grupė, esanti DK PVM parametruose.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="2a1ce-124">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2a1ce-125">Kiekis yra neprivalomas.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="2a1ce-126">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="2a1ce-127">Vieneto kaina yra neprivaloma.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="2a1ce-128">Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="2a1ce-129">Tačiau to skaičiavimo galite nepaisyti ir sumą įvesti.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="2a1ce-130">Spustelėję ant PVM, galėsite peržiūrėti apskaičiuotą SF PVM.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="2a1ce-131">Peržiūrėkite PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke Koregavimas.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="2a1ce-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-132">Click OK.</span></span>
12. <span data-ttu-id="2a1ce-133">Spustelėję Išlaidos, galėsite į savo sąskaitą faktūrą įtraukti išlaidų.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="2a1ce-134">Lauke Išlaidų kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="2a1ce-135">Lauke Išlaidų vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="2a1ce-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-136">Close the page.</span></span>
16. <span data-ttu-id="2a1ce-137">Spustelėję Bendrosios sumos, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="2a1ce-138">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-138">Click Close.</span></span>
18. <span data-ttu-id="2a1ce-139">Norėdami registruoti sąskaitą faktūrą, spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-139">Click Post to post the invoice.</span></span> <span data-ttu-id="2a1ce-140">Prieš registruodami galėsite atšaukti.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="2a1ce-141">Norėdami pakeisti laiką, kad spausdinamos jūsų SF: pasirinkus Iškart, atnaujinus kiekvieną SF ji iškart spausdinama, arba Vėliau (SF spausdinamos, kai atnaujintos visos SF).</span><span class="sxs-lookup"><span data-stu-id="2a1ce-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="2a1ce-142">Jei norite pakeisti, kaip prieš registruojant tikrinamas kliento kredito limitas, pakeiskite kredito limito tipą.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="2a1ce-143">Jei norite spausdinti sąskaitą faktūrą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="2a1ce-144">Jei norite registruoti sąskaitą faktūrą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="2a1ce-145">Galite spausdinti SF jos neregistruodami.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="2a1ce-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="2a1ce-146">Click OK.</span></span>

