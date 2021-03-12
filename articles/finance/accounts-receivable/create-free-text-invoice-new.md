---
title: Laisvos formos sąskaitos faktūros kūrimas
description: Šioje temoje paaiškinama, kaip kurti laisvos formos SF.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 726d4979059417871a00626c55da32fa4286cb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991122"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="eb8a9-103">Laisvos formos sąskaitos faktūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="eb8a9-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb8a9-104">Šioje temoje paaiškinama, kaip kurti laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="eb8a9-105">Procedūrai atlikti naudokite demonstracinių duomenų įmonę **USMF**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="eb8a9-106">Kurti laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="eb8a9-106">Create a free text invoice</span></span>

1. <span data-ttu-id="eb8a9-107">Eikite į **Gautos paskyros (ar pardavimų sąskaitų knyga) \> Sąskaitos \> Visos nemokamo teksto sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-107">Go to **Accounts receivable (or Sales Ledger) \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="eb8a9-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-108">Select **New**.</span></span>
3. <span data-ttu-id="eb8a9-109">Lauke **Kliento sąskaita** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="eb8a9-110">Pagal numatytuosius parametrus paskyra, pasirinkta kaip kliento sąskaita, naudojama kaip SF sąskaita.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="eb8a9-111">Jei SF neužregistruota, pirmoji apskaitos būsena yra **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="eb8a9-112">SF numeris bus priskirtas užregistravus SF.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="eb8a9-113">Jei naudojate bendros mokėjimų eurais erdvės (SEPA) įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas įvedamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="eb8a9-114">Lauke **Aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="eb8a9-115">Lauke **Pagrindinė sąskaita** nurodykite sąskaitos numerį be dimensijų.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="eb8a9-116">Dimensijas įvesite vėliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="eb8a9-117">Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="eb8a9-118">Pasirinkite „FastTab“ **Eilutės informacija**, kad į pagrindinę sąskaitą įtrauktumėte dimensijų.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="eb8a9-119">Pasirinkite skirtuką **Finansinių dimensijų eilutė**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="eb8a9-120">Nurodytos tik pasirinktos eilutės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="eb8a9-121">PVM grupė užpildoma iš kliento duomenų.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="eb8a9-122">Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="eb8a9-123">Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="eb8a9-124">Jei pagrindinė sąskaita neturi prekių PVM grupės, naudojama prekių PVM grupė, nurodyta DK PVM parametruose.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="eb8a9-125">Pasirinktinai: lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="eb8a9-126">Pasirinktinai: Lauke **Vieneto kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="eb8a9-127">Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="eb8a9-128">Tačiau to skaičiavimo galite nepaisyti įvesdami sumą.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="eb8a9-129">Pasirinkite **PVM**, kad peržiūrėtumėte apskaičiuotą SF PVM.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="eb8a9-130">Galite peržiūrėti PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke **Koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="eb8a9-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-131">Select **OK**.</span></span>
12. <span data-ttu-id="eb8a9-132">Pasirinkite **Išlaidos**, kad į SF įtrauktumėte išlaidas.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="eb8a9-133">Lauke **Išlaidų kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="eb8a9-134">Lauke **Išlaidų vertė** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="eb8a9-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-135">Close the page.</span></span>
16. <span data-ttu-id="eb8a9-136">Pasirinkę **Bendrosios sumos**, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="eb8a9-137">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-137">Select **Close**.</span></span>
18. <span data-ttu-id="eb8a9-138">Pasirinkite **Registruoti**, kad užregistruotumėte SF.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="eb8a9-139">Vis dar turėsite galimybę atšaukti prieš užregistruodami faktiškai.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="eb8a9-140">Galite pakeisti SF spausdinimo laiką.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="eb8a9-141">Pasirinkite **Dabartinis**, kad būtų spausdinama kiekviena sąskaita faktūra ją atnaujinus.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="eb8a9-142">Pasirinkite **Vėliau**, norėdami spausdinti, kai atnaujinamos visos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="eb8a9-143">Norėdami keisti tai, kaip kliento kredito limitas yra tikrinamas prieš registruojant SF, pakeiskite reikšmę lauke **Kredito limito tipas**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="eb8a9-144">Norėdami spausdinti SF, nustatykite parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="eb8a9-145">Norėdami registruoti SF, nustatykite parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="eb8a9-146">Galite spausdinti SF jos neregistruodami.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="eb8a9-147">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="eb8a9-148">Kopijuoti eilutes</span><span class="sxs-lookup"><span data-stu-id="eb8a9-148">Copy lines</span></span>
<span data-ttu-id="eb8a9-149">Norėdami kopijuoti laisvos formos sąskaitos faktūros eilutes, pasirinkite vieną ar kelias eilutes, tada pasirinkite **Kopijuoti pasirinktas eilutes**.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="eb8a9-150">Galite nurodyti kopijų skaičių, taip pat galite kopijuoti pastabas ir priedus.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="eb8a9-151">Paskirstymus galite kopijuoti arba leisti juos sukurti iš naujo registruojant.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="eb8a9-152">Nukopijavę eilutes, galite pagal poreikį redaguoti informaciją.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="eb8a9-153">Laisvos formos sąskaitos faktūros kūrimas pagal šabloną</span><span class="sxs-lookup"><span data-stu-id="eb8a9-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="eb8a9-154">Laisvos formos sąskaitą faktūrą galite kurti pagal šabloną.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="eb8a9-155">Skirtuke **Sąskaita faktūra** pasirinkę **Nauja pagal šabloną**, galite pasirinkti naujosios laisvos formos sąskaitos faktūros šablono pavadinimą ir kliento sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="eb8a9-156">Numatytąsias reikšmes, pvz., mokėjimo sąlygas ir kliento mokėjimo būdą, galima automatiškai užpildyti iš kliento duomenų arba galima naudoti šablone įrašytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="eb8a9-157">Bus sukurta nauja laisvos formos SF ir galėsite redaguoti norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="eb8a9-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
