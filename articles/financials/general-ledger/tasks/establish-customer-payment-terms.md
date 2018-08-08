--- 
title: "Nustatyti kliento mokėjimo sąlygas"
description: "Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c35c608dc5e9b4790a81a8dadb716157fa740e8c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="76790-103">Nustatyti kliento mokėjimo sąlygas</span><span class="sxs-lookup"><span data-stu-id="76790-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76790-104">Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką.</span><span class="sxs-lookup"><span data-stu-id="76790-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="76790-105">Šiame užduočių vadove naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="76790-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="76790-106">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų dienos.</span><span class="sxs-lookup"><span data-stu-id="76790-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="76790-107">Mokėjimo sąlygų sąranka bendrinama su gautinomis sumomis ir mokėtinomis sumomis.</span><span class="sxs-lookup"><span data-stu-id="76790-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="76790-108">Jei ją nurodysite modulyje, ji bus prieinama ir kitame modulyje.</span><span class="sxs-lookup"><span data-stu-id="76790-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="76790-109">Šiame užduočių vadove visas mokėjimo sąlygas nustatau srityje Gautinos sumos.</span><span class="sxs-lookup"><span data-stu-id="76790-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="76790-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="76790-110">Click New.</span></span>
    * <span data-ttu-id="76790-111">Sukurkite mokėjimo dieną, jeigu mokėjimo sąlygose reikalaujama konkrečios savaitės dienos (pirmadienio, antradienio ir t. t) arba konkrečios mėnesio dienos (5 d., 10 d., ir t. t).</span><span class="sxs-lookup"><span data-stu-id="76790-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="76790-112">Lauke Mokėjimų diena įveskite mokėjimo dienos, nurodytos mokėjimo dienos lauke, ID.</span><span class="sxs-lookup"><span data-stu-id="76790-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="76790-113">Lauke Aprašas įveskite mokėjimų dienos aprašą.</span><span class="sxs-lookup"><span data-stu-id="76790-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="76790-114">Lauke Savaitė / Mėnuo pasirinkite arba Savaitė, arba Mėnuo.</span><span class="sxs-lookup"><span data-stu-id="76790-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="76790-115">Jei norite įvesti savaitės dieną, pvz., pirmadienį, pasirinkite Savaitė.</span><span class="sxs-lookup"><span data-stu-id="76790-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="76790-116">Jei norite įvesti mėnesio dieną, pvz., 10 d., pasirinkite Mėnuo.</span><span class="sxs-lookup"><span data-stu-id="76790-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="76790-117">Šiame pavyzdyje pasirinkite Mėnuo.</span><span class="sxs-lookup"><span data-stu-id="76790-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="76790-118">Lauke Mėnesio diena įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="76790-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="76790-119">Dieną reikėtų įvesti kaip skaičių, pvz., „10‟, o ne kaip „10 d.‟.</span><span class="sxs-lookup"><span data-stu-id="76790-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="76790-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="76790-120">Click Save.</span></span>
8. <span data-ttu-id="76790-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="76790-121">Close the page.</span></span>
9. <span data-ttu-id="76790-122">Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="76790-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="76790-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="76790-123">Click New.</span></span>
    * <span data-ttu-id="76790-124">Mokėjimo sąlygos naudojamos apibrėžti, kaip bus skaičiuojami terminai.</span><span class="sxs-lookup"><span data-stu-id="76790-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="76790-125">Mokėjimo nuolaidos datos sąranka apibrėžiama atskirame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="76790-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="76790-126">Lauke Mokėjimo sąlygos įveskite ID, esantį lauke Mokėjimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="76790-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="76790-127">Lauke Aprašas įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="76790-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="76790-128">Pasirinkite mokėjimo būdą, pvz., COD, Grynasis, Dabartinis mėnuo ir t. t.</span><span class="sxs-lookup"><span data-stu-id="76790-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="76790-129">Mokėjimo būdas naudojamas apibrėžti, kaip bus pradedami skaičiuoti terminai.</span><span class="sxs-lookup"><span data-stu-id="76790-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="76790-130">Pvz., Grynasis naudojamas, jei terminas visada yra nustatytas mėnesių ar dienų skaičius po SF datos.</span><span class="sxs-lookup"><span data-stu-id="76790-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="76790-131">COD galima naudoti, kai mokėti reikia gavus SF, todėl terminas nebūtų skaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="76790-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="76790-132">Pasirinkite Dabartinis mėnuo, kuris bus naudojamas šiame užduočių vadove.</span><span class="sxs-lookup"><span data-stu-id="76790-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="76790-133">Pasirinkite mokėjimo dieną, jei skaičiuojant įtraukiama konkreti savaitės diena ar data.</span><span class="sxs-lookup"><span data-stu-id="76790-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="76790-134">Atsižvelgiant į mokėjimo sąlygas, kiekį galite įvesti mėnesiais arba dienomis.</span><span class="sxs-lookup"><span data-stu-id="76790-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="76790-135">Arba galite naudoti mokėjimų grafiką ar mokėjimo dieną, kuriuos „pridėtumėte‟ prie mokėjimo būdo pabaigos.</span><span class="sxs-lookup"><span data-stu-id="76790-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="76790-136">Jei terminas visada bus kito mėnesio 10 d., mokėjimo dieną pasirinkite 10 d.</span><span class="sxs-lookup"><span data-stu-id="76790-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="76790-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="76790-137">Click Save.</span></span>
16. <span data-ttu-id="76790-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="76790-138">Close the page.</span></span>
17. <span data-ttu-id="76790-139">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimo nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="76790-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="76790-140">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="76790-140">Click New.</span></span>
    * <span data-ttu-id="76790-141">Šis puslapis naudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.</span><span class="sxs-lookup"><span data-stu-id="76790-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="76790-142">Lauke Mokėjimo nuolaida įveskite ID, esantį lauke Mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="76790-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="76790-143">Lauke Aprašas įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="76790-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="76790-144">Jei galima pakopinė mokėjimo nuolaida, pasirinkite kitą nuolaidos kodą, kuris yra aktualus po šios naujos mokėjimo nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="76790-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="76790-145">Įveskite dienų, naudojamų skaičiuoti mokėjimo nuolaidos datai, skaičių.</span><span class="sxs-lookup"><span data-stu-id="76790-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="76790-146">Jei pasirinktas grynasis principas, norint apskaičiuoti mokėjimo nuolaidos datą, dienų skaičius bus pridėtas prie SF datos.</span><span class="sxs-lookup"><span data-stu-id="76790-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="76790-147">Įveskite mokėjimo nuolaidos procentą.</span><span class="sxs-lookup"><span data-stu-id="76790-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="76790-148">Įveskite pagrindinę sąskaitą, kurioje bus registruojama klientų SF mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="76790-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="76790-149">Lauke Taikyti nuolaidą korespondentinėms sąskaitoms pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="76790-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="76790-150">Jei pasirinksite „Sąskaitos SF eilutėse‟, mokėjimo nuolaida bus registruojama toje pačioje turto / išlaidų pagrindinėje sąskaitoje, esančioje tiekėjo SF eilutėse.</span><span class="sxs-lookup"><span data-stu-id="76790-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="76790-151">Jei pasirinksite „Tiekėjo SF naudoti pagrindinę sąskaitą‟, mokėjimo nuolaida bus registruojama pagrindinėje sąskaitoje, apibrėžtoje srityje „Pagrindinė tiekėjų SF sąskaita‟.</span><span class="sxs-lookup"><span data-stu-id="76790-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="76790-152">Šiame pavyzdyje pasirinkite „Tiekėjų SF naudoti pagrindinę sąskaitą‟.</span><span class="sxs-lookup"><span data-stu-id="76790-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="76790-153">Įveskite pagrindinę sąskaitą, kurioje bus registruojama tiekėjų SF mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="76790-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="76790-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="76790-154">Click Save.</span></span>


