---
title: Konkrečių produktų tiekėjų tvirtinimas
description: Šia procedūra rodoma, kaip patvirtinti konkrečių produktų tiekėjus.
author: mkirknel
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d09a7388377899b7cfb11ba744232d06aa2c4db6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149808"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="db3f3-103">Konkrečių produktų tiekėjų tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="db3f3-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db3f3-104">Šia procedūra rodoma, kaip patvirtinti konkrečių produktų tiekėjus.</span><span class="sxs-lookup"><span data-stu-id="db3f3-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="db3f3-105">Taip galima valdyti, kurie tiekėjai gali būti naudojami, kai produktas įtraukiamas į pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="db3f3-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="db3f3-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="db3f3-107">Šią užduotį paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="db3f3-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="db3f3-108">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="db3f3-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="db3f3-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db3f3-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="db3f3-111">Išplėskite „FastTab“ skirtuką **Pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="db3f3-112">Jei lauke **Tiekėjas** rodomas pirminis tiekėjas, tada, atlikdami tolesnius veiksmus, šį tiekėją turite įtraukti kaip patvirtintą tiekėją.</span><span class="sxs-lookup"><span data-stu-id="db3f3-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="db3f3-113">Jei rodomas tiekėjo numeris, jį pasižymėkite.</span><span class="sxs-lookup"><span data-stu-id="db3f3-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="db3f3-114">Veiksmų srityje spustelėkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-114">On Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="db3f3-115">Spustelėkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-115">Click **Setup**.</span></span>
7. <span data-ttu-id="db3f3-116">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-116">Click **Add**.</span></span>
8. <span data-ttu-id="db3f3-117">Lauke Tiekėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db3f3-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="db3f3-118">Pasirinkite patvirtintą tiekėją.</span><span class="sxs-lookup"><span data-stu-id="db3f3-118">Select the approved vendor.</span></span> <span data-ttu-id="db3f3-119">Jei produkto įraše buvo pirminis tiekėjas, jis turi būti bent vienoje iš eilučių.</span><span class="sxs-lookup"><span data-stu-id="db3f3-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="db3f3-120">Jei anksčiau pasižymėjote tiekėjo numerį, jį čia pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="db3f3-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="db3f3-121">Lauke **Galiojimo pabaiga** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="db3f3-122">Pasirinkite datą už kelių mėnesių.</span><span class="sxs-lookup"><span data-stu-id="db3f3-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="db3f3-123">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-123">Click **Add**.</span></span>
11. <span data-ttu-id="db3f3-124">Lauke **Tiekėjas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db3f3-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="db3f3-125">Lauke **Galiojimo pabaiga** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="db3f3-126">Pasirinkite datą, kuri skiriasi nuo ankstesnės galiojimo datos.</span><span class="sxs-lookup"><span data-stu-id="db3f3-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="db3f3-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-127">Close the page.</span></span>
14. <span data-ttu-id="db3f3-128">Veiksmų srityje spustelėkite **Patvirtinti tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-128">On Action pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="db3f3-129">Lauke **Galiojimo pabaiga** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="db3f3-130">Ši data veikia kaip filtras, kad iki tam tikros datos galėtumėte matyti, kas yra patvirtinti tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="db3f3-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="db3f3-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-131">Close the page.</span></span>
17. <span data-ttu-id="db3f3-132">Veiksmų srityje spustelėkite **Galiojantis laikotarpis**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-132">On Action pane, click **Effective period**.</span></span>
18. <span data-ttu-id="db3f3-133">Lauke **Rodyti tiekėjus, baigusius galioti iki** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="db3f3-134">Naudodami šį puslapį, galite identifikuoti tiekėjus, kurių patvirtinimo būsena po tam tikros datos baigs galioti.</span><span class="sxs-lookup"><span data-stu-id="db3f3-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="db3f3-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-135">Close the page.</span></span>
20. <span data-ttu-id="db3f3-136">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-136">Click **Edit**.</span></span>
21. <span data-ttu-id="db3f3-137">Lauke **Patvirtintų tiekėjų tikrinimo metodas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="db3f3-138">Šiame lauke galima pasirinkti strategiją, kas turėtų vykti, jei produktas įtraukiamas į pirkimo užsakymo eilutę, kai tiekėjas nėra patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="db3f3-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="db3f3-139">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-139">Click **Save**.</span></span>
23. <span data-ttu-id="db3f3-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-140">Close the page.</span></span>
24. <span data-ttu-id="db3f3-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-141">Close the page.</span></span>
25. <span data-ttu-id="db3f3-142">Pasirinkite **Moduliai > Įsigijimas ir šaltinio pasirinkimas > Tiekėjai > Tiekėjų / prekių ryšiai > Patvirtintų tiekėjų sąrašas pagal prekę**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="db3f3-143">Šiame puslapyje apžvelgiami visi produktai ir patvirtinti tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="db3f3-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="db3f3-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-144">Close the page.</span></span>
27. <span data-ttu-id="db3f3-145">Naršymo srityje eikite į **Moduliai > Paraiškos > Tiekėjai > Visi tiekėjai.**</span><span class="sxs-lookup"><span data-stu-id="db3f3-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="db3f3-146">Taip pat galite pradėti nuo tiekėjo ir pereiti į to tiekėjo sąskaitos patvirtintų produktų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="db3f3-147">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="db3f3-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="db3f3-148">Veiksmų srityje spustelėkite **Įsigijimas**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-148">On Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="db3f3-149">Spustelėkite **Patvirtintų tiekėjų sąrašas pagal tiekėją**.</span><span class="sxs-lookup"><span data-stu-id="db3f3-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="db3f3-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-150">Close the page.</span></span>
32. <span data-ttu-id="db3f3-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db3f3-151">Close the page.</span></span>

