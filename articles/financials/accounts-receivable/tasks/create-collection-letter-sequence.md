--- 
title: "Kurti priminimo laiškų seką"
description: "Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką."
author: mikefalkner
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 63f28194065821f898cc73678a9868ec9ee2c64b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="a5166-103">Kurti priminimo laiškų seką</span><span class="sxs-lookup"><span data-stu-id="a5166-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5166-104">Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="a5166-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="a5166-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a5166-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a5166-106">Pasirinkite Kreditas ir rinkiniai > Sąranka > Nustatyti priminimo laiškų seką.</span><span class="sxs-lookup"><span data-stu-id="a5166-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="a5166-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a5166-107">Click New.</span></span>
3. <span data-ttu-id="a5166-108">Lauke Priminimo laiškų seka įveskite sekos ID, kuris atitinka seką.</span><span class="sxs-lookup"><span data-stu-id="a5166-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="a5166-109">Jis bus naudojamas, kai nustatinėsite registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="a5166-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="a5166-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a5166-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a5166-111">Mokėjimo sąlygos nėra privalomos.</span><span class="sxs-lookup"><span data-stu-id="a5166-111">The terms of payment is optional.</span></span> <span data-ttu-id="a5166-112">Jei reikšmę įvesite čia, priminimo laiško mokesčio SF bus naudojamos šios mokėjimo sąlygos, o ne mokėjimo sąlygos, saugomos su klientu.</span><span class="sxs-lookup"><span data-stu-id="a5166-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="a5166-113">Priminimo laiško kodo lauke pasirinkite pirmojo priminimo laiško, kurį norite siųsti, kodą.</span><span class="sxs-lookup"><span data-stu-id="a5166-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="a5166-114">Sukuriamas pirmasis priminimo laiškas pagal SF nurodytą terminą, atidėjimo vertę, kurią įvedate šios eilutės lauke Dienos, ir kitą informaciją, kurią įvedate šioje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a5166-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="a5166-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a5166-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a5166-116">Mokesčio valiuta pagal numatytąsias nuostatas naudojama ir kaip kliento valiuta.</span><span class="sxs-lookup"><span data-stu-id="a5166-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="a5166-117">Šis valiutos kodas gali skirtis nuo SF valiutos.</span><span class="sxs-lookup"><span data-stu-id="a5166-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="a5166-118">Spustelėkite Pridėti, kad pridėtumėte kitą priminimo laišką, kuris bus siunčiamas sekoje</span><span class="sxs-lookup"><span data-stu-id="a5166-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="a5166-119">Daugeliu atvejų pirmasis priminimo laiškas yra tik perspėjimas.</span><span class="sxs-lookup"><span data-stu-id="a5166-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="a5166-120">Jei reikia, galite pridėti mokesčių.</span><span class="sxs-lookup"><span data-stu-id="a5166-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="a5166-121">Priminimo laiško kodo lauke pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.</span><span class="sxs-lookup"><span data-stu-id="a5166-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="a5166-122">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a5166-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a5166-123">Pagrindinės sąskaitos lauke pasirinkite įplaukų sąskaitą, kuri bus naudojama mokesčiams.</span><span class="sxs-lookup"><span data-stu-id="a5166-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="a5166-124">Įveskite mokestį, kuris bus taikomas registruojant šį priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="a5166-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="a5166-125">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a5166-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="a5166-126">Jei reikia apskaičiuoti mokesčio PVM, pasirinkite prekių PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="a5166-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="a5166-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a5166-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a5166-128">Įveskite mažiausią pradelstą balansą, kurio reikia prieš siunčiant priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="a5166-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="a5166-129">Įveskite leistinų atidėjimo dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="a5166-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="a5166-130">Tai yra dienų skaičius po termino, iki kurio galima generuoti priminimo laišką.</span><span class="sxs-lookup"><span data-stu-id="a5166-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="a5166-131">Terminas, naudojamas skaičiuojant, priklauso nuo priminimo laiško padėties priminimo laiškų sekoje: ⦁ 1 priminimo laiško atidėjimo laikotarpis yra susijęs su terminu SF.</span><span class="sxs-lookup"><span data-stu-id="a5166-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="a5166-132">⦁ 2 ir tolesnių priminimo laiškų atidėjimo laikotarpis yra susijęs su data, kada registruotas ar išspausdintas ankstesnis priminimo laiškas, atsižvelgiant į pasirinktį puslapio Gautinų sumų parametrai lauke Atnaujinti priminimo laiško kodą.</span><span class="sxs-lookup"><span data-stu-id="a5166-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="a5166-133">Spustelėkite Pridėti, kad pridėtumėte paskutinį priminimo laišką sekoje.</span><span class="sxs-lookup"><span data-stu-id="a5166-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="a5166-134">Galite pridėti iki penkių priminimo laiškų sekos priminimo laiškų.</span><span class="sxs-lookup"><span data-stu-id="a5166-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="a5166-135">Priminimo laiško kodo lauke pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.</span><span class="sxs-lookup"><span data-stu-id="a5166-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="a5166-136">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a5166-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="a5166-137">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="a5166-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="a5166-138">Lauke Mokestis valiuta įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a5166-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="a5166-139">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a5166-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a5166-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a5166-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="a5166-141">Lauke Mažiausias pradelstas balansas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a5166-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="a5166-142">Lauke Dienos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a5166-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="a5166-143">Pažymėkite šį žymės langelį, kad klientas daugiau negalėtų pristatyti ir išrašyti SF.</span><span class="sxs-lookup"><span data-stu-id="a5166-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="a5166-144">Norėdami atblokuoti sąskaitą, puslapio Klientai lauke SF išrašymo ir pristatymo sulaikymas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="a5166-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="a5166-145">Išplėskite „FastTab“ Pastabos.</span><span class="sxs-lookup"><span data-stu-id="a5166-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="a5166-146">Įveskite tekstą, kuris bus rodomas pasirinkto priminimo laiško kodo priminimo laiške.</span><span class="sxs-lookup"><span data-stu-id="a5166-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="a5166-147">Naudodami meniu Vertimai, esantį virš pastabų langelio, šį tekstą galite išversti į kelias kalbas.</span><span class="sxs-lookup"><span data-stu-id="a5166-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


