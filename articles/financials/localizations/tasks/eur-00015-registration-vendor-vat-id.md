--- 
title: "Registruoti tiekėjo PVM ID"
description: "Šioje procedūroje parodoma, kaip įtraukti PVM registracijos ID ir neapmokestinimo kodą į tiekėjo kodą."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a626d7b4ef4187d56b23efe5c28e986b11247562
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="register-a-vendor-vat-id"></a><span data-ttu-id="f3fc4-103">Registruoti tiekėjo PVM ID</span><span class="sxs-lookup"><span data-stu-id="f3fc4-103">Register a vendor VAT ID</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3fc4-104">Šioje procedūroje parodoma, kaip įtraukti PVM registracijos ID ir neapmokestinimo kodą į tiekėjo kodą.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="f3fc4-105">Šis procesas yra panašus ir kai naudojami juridiniai subjektai bei klientai.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="f3fc4-106">Prieš atlikdami šią procedūrą, turite nustatyti PVM ID.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="f3fc4-107">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="f3fc4-108">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="f3fc4-109">Ši procedūra yra skirta duomenų valdymo administratoriui, mokėtinų sumų vadovui arba gautinų sumų vadovui.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="f3fc4-110">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="f3fc4-111">Pasirinkite Mokėtinos sumos > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="f3fc4-112">Sąraše raskite ir pasirinkite tiekėją DE-01001</span><span class="sxs-lookup"><span data-stu-id="f3fc4-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="f3fc4-113">Spustelėkite Registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="f3fc4-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-114">Click Add.</span></span>
5. <span data-ttu-id="f3fc4-115">Pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-115">Select VAT ID.</span></span>
6. <span data-ttu-id="f3fc4-116">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="f3fc4-117">Nurodykite pasirinkto tiekėjo PVM ID Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="f3fc4-118">ID turi atitikti nurodytą registracijos tipo formatą.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="f3fc4-119">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-119">Click the General tab.</span></span>
8. <span data-ttu-id="f3fc4-120">Lauke Įsigalioja įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="f3fc4-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-121">Click Save.</span></span>
10. <span data-ttu-id="f3fc4-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-122">Click New.</span></span>
11. <span data-ttu-id="f3fc4-123">Lauke Pavadinimas arba aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="f3fc4-124">Pavyzdžiui, įveskite ITA.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="f3fc4-125">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="f3fc4-126">Pavyzdžiui, pasirinkite ITA.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="f3fc4-127">Lauke Pagrindinis šalies pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="f3fc4-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-128">Click Save.</span></span>
15. <span data-ttu-id="f3fc4-129">Spustelėkite skirtuką Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="f3fc4-130">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-130">Click Add.</span></span>
17. <span data-ttu-id="f3fc4-131">Lauke Registracijos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="f3fc4-132">Pavyzdžiui, pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="f3fc4-133">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="f3fc4-134">Pavyzdžiui, nurodykite PVM ID Italijoje.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="f3fc4-135">ID turi atitikti nurodytą registracijos tipo formatą.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="f3fc4-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-136">Click Save.</span></span>
20. <span data-ttu-id="f3fc4-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-137">Close the page.</span></span>
21. <span data-ttu-id="f3fc4-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f3fc4-139">Pavyzdžiui, pasirinkite DE-01001.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="f3fc4-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="f3fc4-141">Išplėskite skyrių SF ir pristatymas.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="f3fc4-142">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-142">Click Edit.</span></span>
25. <span data-ttu-id="f3fc4-143">Lauke Neapmokestinimo kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="f3fc4-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f3fc4-144">Click Save.</span></span>


