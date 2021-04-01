---
title: Registruoti periodinius žurnalus
description: Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai periodinis žurnalas nuskaitomas.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31c801658004f771df6f1ddf70194de131314a64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212160"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="d1f8a-103">Registruoti periodinius žurnalus</span><span class="sxs-lookup"><span data-stu-id="d1f8a-103">Post periodic journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d1f8a-104">Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai periodinis žurnalas nuskaitomas.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="d1f8a-105">Sukūrę periodinį žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="d1f8a-106">Šis užduočių vadovas sukurs tokį periodinį žurnalą, kurio pasikartojimas yra mėnesinis.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="d1f8a-107">Pasirinkę **Naršymo sritis, eikite į Moduliai > Didžioji knyga > Periodinės užduotys > Periodiniai žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="d1f8a-108">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-108">Click **New**.</span></span>
3. <span data-ttu-id="d1f8a-109">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="d1f8a-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d1f8a-111">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="d1f8a-112">Aprašą sudarys vėliau gauto periodinio žurnalo pavadinimas, todėl jį suteikite atitinkamą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="d1f8a-113">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="d1f8a-114">Periodinį žurnalą paprastai sudaro kelios eilutės.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="d1f8a-115">tačiau šis užduočių vadovas įtrauks tik vieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="d1f8a-116">Lauke **Data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="d1f8a-117">Lauke **Data** nurodyta kito perkėlimo į kasdienį žurnalą registravimo data.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="d1f8a-118">Žurnaluose, kurie bus gaunami kiekvieną mėnesį, rekomenduojama naudoti datą tame mėnesyje, kada žurnlas bus registruojamas – paprastai tai pirmoji arba paskutinioji laikotarpio data.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="d1f8a-119">Galima lauką Data palikti tuščią, ir datą nurodyti, kai gaunamas žurnalas, naudojant lauką Tuščia data.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="d1f8a-120">Kai operacijos nuskaitomos, laukas automatiškai atnaujinamas į kitą pasikartojančią datą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="d1f8a-121">Lauke **Sąskaita** nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="d1f8a-122">Lauke **Aprašas** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="d1f8a-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-123">Close the page.</span></span>
11. <span data-ttu-id="d1f8a-124">Lauke **Debetas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="d1f8a-125">Lauke **Korespondentinė sąskaita** nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="d1f8a-126">Lauke **Vienetas** pasirinkite „Mėnesiai‟.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="d1f8a-127">Lauke **Vienetų skaičius** įveskite „1‟.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="d1f8a-128">Lauke **Paskutinė data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="d1f8a-129">Paskutinę datą įvedus į ankstesnį laikotarpį, nebus galima pasikartojančio žurnalo netyčia sukurti neteisingame pradžios laikotarpyje.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="d1f8a-130">Paskutinė diena bus atnaujinama vėliau, kiekvieną kartą nuskaitant periodinį žurnalą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="d1f8a-131">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-131">Click **Save**.</span></span>
17. <span data-ttu-id="d1f8a-132">Eikite į **Naršymo sritis > Moduliai > Bendroji didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="d1f8a-133">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-133">Click **New**.</span></span>
19. <span data-ttu-id="d1f8a-134">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="d1f8a-135">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="d1f8a-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d1f8a-137">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="d1f8a-138">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="d1f8a-139">**Veiksmų srityje** spustelėkite **Periodinis žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="d1f8a-140">Spustelėkite **Nuskaityti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="d1f8a-141">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="d1f8a-142">**Pabaigos data** naudojama kaip periodinio kvito eilučių galutinė data.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="d1f8a-143">Atsižvelgiant į pasikartojimo nuostatą, paskutinę datą ir datą Iki, gautame žurnale ta pati eilutė gali būti įtraukta daugiau nei vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="d1f8a-144">Data Iki automatiškai atnaujinama pagal seanso datą, kada paskutinį kartą periodinė eilutė buvo perkelta į žurnalą.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="d1f8a-145">Lauke **Periodinio žurnalo numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="d1f8a-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="d1f8a-147">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-147">Click **OK**.</span></span> <span data-ttu-id="d1f8a-148">Laikotarpio žurnalą dabar galima peržiūrėti, patvirtinti arba registruoti – tai priklauso nuo poreikio ir nustatymo.</span><span class="sxs-lookup"><span data-stu-id="d1f8a-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]