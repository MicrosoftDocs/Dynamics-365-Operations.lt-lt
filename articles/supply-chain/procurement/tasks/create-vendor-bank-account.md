--- 
title: "Sukurti tiekėjo banko sąskaitą"
description: "Šia procedūra parodoma, kaip kurti tiekėjo banko kodą."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2bdd1264f92b73aed2eeb6ab13e435bb3c0dde19
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="8a4c6-103">Sukurti tiekėjo banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="8a4c6-103">Create a vendor bank account</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a4c6-104">Šia procedūra parodoma, kaip kurti tiekėjo banko kodą.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="8a4c6-105">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="8a4c6-106">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="8a4c6-107">Pasirinkite tiekėją, kuriam norite kurti banko kodą, o tada spustelėkite tiekėjo kodo ID saitą.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="8a4c6-108">Veiksmų srityje spustelėkite Tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="8a4c6-109">Spustelėkite Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="8a4c6-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-110">Click New.</span></span>
6. <span data-ttu-id="8a4c6-111">Lauke Banko sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="8a4c6-112">Šis ID bus naudojamas siekiant identifikuoti tiekėjo įrašo banko kodą.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="8a4c6-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="8a4c6-114">Lauke Bankų grupės įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="8a4c6-115">Lauke Banko kodo tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="8a4c6-116">Tai yra banko kodo, naudojamo tarptautiniams mokėjimams atlikti, tipas.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="8a4c6-117">Lauke Banko sąskaitos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="8a4c6-118">Lauke SWIFT kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="8a4c6-119">Lauke IBAN surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="8a4c6-120">IBAN numeris turi būti tinkamo formato.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="8a4c6-121">Pavyzdžiui, galite naudoti DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="8a4c6-122">Banko sąskaitos būsena yra Aktyvi, jei pasiekta Aktyvinimo data, o galiojimo laikas dar nesibaigė.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="8a4c6-123">Ji taip pat aktyvi, jei laukai Aktyvinimo data ir Galiojimo data yra nenurodyti.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="8a4c6-124">Jei datos nurodytos laukuose Aktyvinimo data ir Galiojimo data yra būsimos, elektroniniai mokėjimai nėra galimi.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="8a4c6-125">Kiti mokėjimo tipai yra galimi ir banko sąskaita yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="8a4c6-126">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="8a4c6-127">Lauke Teksto kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="8a4c6-128">Šiame lauke nurodomas kodas, kuris bus rodomas gavėjo banko išraše.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="8a4c6-129">Lauke Pranešimas bankui įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="8a4c6-130">Lauke Kurso keitimo nuoroda įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="8a4c6-131">Tai yra bet kurio būsimo ar fiksuoto valiutos kurso nuorodos numeris.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="8a4c6-132">Lauke Valiuta įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="8a4c6-133">Išduodant išankstinius pranešimus, šioje sekcijoje pateikiama jų būsenų (laukiama arba patvirtinta) apžvalga.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="8a4c6-134">Išplėskite dalį Adresas.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-134">Expand the Address section.</span></span>
19. <span data-ttu-id="8a4c6-135">Išplėskite sekciją Išankstiniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="8a4c6-136">Išplėskite skyrių „Kontaktinė informacija“.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="8a4c6-137">Lauke Telefonas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="8a4c6-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-138">Close the page.</span></span>
23. <span data-ttu-id="8a4c6-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-139">Click Edit.</span></span>
24. <span data-ttu-id="8a4c6-140">Išplėskite skyrių „Mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="8a4c6-141">Lauke Banko kodas pasirinkite ką tik sukurtą kodą.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="8a4c6-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-142">Click Save.</span></span>
    * <span data-ttu-id="8a4c6-143">Adresą galima nuskaityti iš bankų grupės, jei ji nurodyta, arba galima jį įtraukti čia.</span><span class="sxs-lookup"><span data-stu-id="8a4c6-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  


