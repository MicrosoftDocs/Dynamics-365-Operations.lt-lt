--- 
title: "Kurti laisvos formos sąskaitą faktūrą"
description: "Šiame straipsnyje parodoma, kaip sukurti laisvos formos sąskaitą faktūrą."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="1d502-103">Kurti laisvos formos sąskaitą faktūrą</span><span class="sxs-lookup"><span data-stu-id="1d502-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d502-104">Šiame straipsnyje parodoma, kaip sukurti laisvos formos sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="1d502-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="1d502-105">Šiai procedūrai atlikti naudokite demonstracinių duomenų įmonę USMF.</span><span class="sxs-lookup"><span data-stu-id="1d502-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="1d502-106">Kurti laisvos formos sąskaitą faktūrą</span><span class="sxs-lookup"><span data-stu-id="1d502-106">Create a free text invoice</span></span>

1. <span data-ttu-id="1d502-107">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="1d502-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="1d502-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1d502-108">Click New.</span></span>
3. <span data-ttu-id="1d502-109">Lauke Kliento sąskaita pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1d502-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="1d502-110">Pagal numatytąsias nuostatas SF sąskaita bus ta pati, kuri naudojama kaip kliento sąskaita.</span><span class="sxs-lookup"><span data-stu-id="1d502-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="1d502-111">Jei SF neužregistruota, pirmoji apskaitos būsena yra Vykdoma.</span><span class="sxs-lookup"><span data-stu-id="1d502-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="1d502-112">SF numeris bus priskirtas užregistravus SF.</span><span class="sxs-lookup"><span data-stu-id="1d502-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="1d502-113">Jei naudojate SEPA įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas bus automatiškai užpildytas įgaliojimu.</span><span class="sxs-lookup"><span data-stu-id="1d502-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="1d502-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1d502-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d502-115">Lauke Pagrindinė sąskaita nurodykite sąskaitos numerį be dimensijų.</span><span class="sxs-lookup"><span data-stu-id="1d502-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="1d502-116">Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1d502-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="1d502-117">Dimensijas įvesite vėliau šiame vadove.</span><span class="sxs-lookup"><span data-stu-id="1d502-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="1d502-118">Išplėtę „FastTab‟ Išsami eilutės informacija, galėsite į savo pagrindinę sąskaitą pridėti dimensijų.</span><span class="sxs-lookup"><span data-stu-id="1d502-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="1d502-119">Spustelėkite skirtuką Finansinių dimensijų eilutė.</span><span class="sxs-lookup"><span data-stu-id="1d502-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="1d502-120">Nurodytos tik pasirinktos eilutės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="1d502-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="1d502-121">PVM grupė automatiškai užpildoma pagal klientą.</span><span class="sxs-lookup"><span data-stu-id="1d502-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="1d502-122">Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="1d502-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="1d502-123">Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1d502-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="1d502-124">Jei pagrindinė sąskaita neturi prekių PVM grupės, tada naudojama prekių PVM grupė, esanti DK PVM parametruose.</span><span class="sxs-lookup"><span data-stu-id="1d502-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="1d502-125">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1d502-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1d502-126">Kiekis yra neprivalomas.</span><span class="sxs-lookup"><span data-stu-id="1d502-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="1d502-127">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1d502-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="1d502-128">Vieneto kaina yra neprivaloma.</span><span class="sxs-lookup"><span data-stu-id="1d502-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="1d502-129">Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos.</span><span class="sxs-lookup"><span data-stu-id="1d502-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="1d502-130">Tačiau to skaičiavimo galite nepaisyti ir sumą įvesti.</span><span class="sxs-lookup"><span data-stu-id="1d502-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="1d502-131">Spustelėję ant PVM, galėsite peržiūrėti apskaičiuotą SF PVM.</span><span class="sxs-lookup"><span data-stu-id="1d502-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="1d502-132">Peržiūrėkite PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke Koregavimas.</span><span class="sxs-lookup"><span data-stu-id="1d502-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="1d502-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1d502-133">Click OK.</span></span>
12. <span data-ttu-id="1d502-134">Spustelėję Išlaidos, galėsite į savo sąskaitą faktūrą įtraukti išlaidų.</span><span class="sxs-lookup"><span data-stu-id="1d502-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="1d502-135">Lauke Išlaidų kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1d502-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="1d502-136">Lauke Išlaidų vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1d502-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="1d502-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1d502-137">Close the page.</span></span>
16. <span data-ttu-id="1d502-138">Spustelėję Bendrosios sumos, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="1d502-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="1d502-139">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="1d502-139">Click Close.</span></span>
18. <span data-ttu-id="1d502-140">Norėdami registruoti sąskaitą faktūrą, spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="1d502-140">Click Post to post the invoice.</span></span> <span data-ttu-id="1d502-141">Prieš registruodami galėsite atšaukti.</span><span class="sxs-lookup"><span data-stu-id="1d502-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="1d502-142">Norėdami pakeisti laiką, kad spausdinamos jūsų SF: pasirinkus Iškart, atnaujinus kiekvieną SF ji iškart spausdinama, arba Vėliau (SF spausdinamos, kai atnaujintos visos SF).</span><span class="sxs-lookup"><span data-stu-id="1d502-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="1d502-143">Jei norite pakeisti, kaip prieš registruojant tikrinamas kliento kredito limitas, pakeiskite kredito limito tipą.</span><span class="sxs-lookup"><span data-stu-id="1d502-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="1d502-144">Jei norite spausdinti sąskaitą faktūrą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="1d502-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="1d502-145">Jei norite registruoti sąskaitą faktūrą, pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="1d502-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="1d502-146">Galite spausdinti SF jos neregistruodami.</span><span class="sxs-lookup"><span data-stu-id="1d502-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="1d502-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1d502-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="1d502-148">Kopijuoti eilutes</span><span class="sxs-lookup"><span data-stu-id="1d502-148">Copy lines</span></span>
<span data-ttu-id="1d502-149">Norėdami kopijuoti laisvos formos sąskaitos faktūros eilutes, pasirinkite vieną ar kelias eilutes, tada spustelėkite Kopijuoti pasirinktas eilutes.</span><span class="sxs-lookup"><span data-stu-id="1d502-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="1d502-150">Galite nurodyti norimą kopijų skaičių, taip pat galite kopijuoti pastabas ir priedus.</span><span class="sxs-lookup"><span data-stu-id="1d502-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="1d502-151">Paskirstymus galite kopijuoti arba leisti juos sukurti iš naujo registruojant.</span><span class="sxs-lookup"><span data-stu-id="1d502-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="1d502-152">Nukopijavę eilutes, galite pagal poreikį redaguoti informaciją.</span><span class="sxs-lookup"><span data-stu-id="1d502-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="1d502-153">Laisvos formos sąskaitos faktūros kūrimas pagal šabloną</span><span class="sxs-lookup"><span data-stu-id="1d502-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="1d502-154">Laisvos formos sąskaitą faktūrą galite kurti pagal šabloną.</span><span class="sxs-lookup"><span data-stu-id="1d502-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="1d502-155">Skirtuke Sąskaita faktūra pasirinkę Nauja pagal šabloną, galite pasirinkti naujosios laisvos formos sąskaitos faktūros šablono pavadinimą ir kliento sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1d502-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="1d502-156">Taip pat galite pasirinkti numatytąsias reikšmes, pvz., mokėjimo sąlygas ir kliento mokėjimo būdą, arba naudoti su šablonu įrašytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="1d502-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="1d502-157">Bus sukurta nauja laisvos formos sąskaita faktūra ir galėsite redaguoti jos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="1d502-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


