---
title: Sukurti tiekėjo banko sąskaitą
description: Šia procedūra parodoma, kaip kurti tiekėjo banko kodą.
author: mkirknel
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8092ab7f960fd36515afb8448dfe1e262197595
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433459"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="4370a-103">Sukurti tiekėjo banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="4370a-103">Create a vendor bank account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4370a-104">Šia procedūra parodoma, kaip kurti tiekėjo banko kodą.</span><span class="sxs-lookup"><span data-stu-id="4370a-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="4370a-105">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="4370a-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="4370a-106">Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir išteklių paskirstymas > Tiekėjai > Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="4370a-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="4370a-107">Pasirinkite tiekėją, kuriam norite sukurti banko sąskaitą, tada spustelėkite saitą lauke **Tiekėjo kliento ID**.</span><span class="sxs-lookup"><span data-stu-id="4370a-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="4370a-108">**Veiksmų srityje** spustelėkite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="4370a-108">On the **Action Pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="4370a-109">Spustelėkite **Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="4370a-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="4370a-110">**Veiksmų srityje** spustelėkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="4370a-110">On the **Action Pane**, click **New**.</span></span>
6. <span data-ttu-id="4370a-111">Lauke **Banko sąskaita** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="4370a-112">Šis ID bus naudojamas siekiant identifikuoti tiekėjo įrašo banko kodą.</span><span class="sxs-lookup"><span data-stu-id="4370a-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="4370a-113">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="4370a-114">Lauke **Banko grupės** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="4370a-115">Lauke **Numerio tipo maršrutizavimas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="4370a-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="4370a-116">Tai yra banko kodo, naudojamo tarptautiniams mokėjimams atlikti, tipas.</span><span class="sxs-lookup"><span data-stu-id="4370a-116">This is the type of routing number that's used for international payments.</span></span>  
10. <span data-ttu-id="4370a-117">Lauke **Banko sąskaitos numeris** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="4370a-118">Lauke **SWIFT kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="4370a-119">Lauke **IBAN** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="4370a-120">IBAN numeris turi būti tinkamo formato.</span><span class="sxs-lookup"><span data-stu-id="4370a-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="4370a-121">Pavyzdžiui, galite naudoti DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="4370a-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="4370a-122">Banko sąskaitos būsena yra Aktyvi, jei pasiekta Aktyvinimo data, o galiojimo laikas dar nesibaigė.</span><span class="sxs-lookup"><span data-stu-id="4370a-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="4370a-123">Ji taip pat aktyvi, jei laukai Aktyvinimo data ir Galiojimo data yra nenurodyti.</span><span class="sxs-lookup"><span data-stu-id="4370a-123">It's also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="4370a-124">Jei datos nurodytos laukuose Aktyvinimo data ir Galiojimo data yra būsimos, elektroniniai mokėjimai nėra galimi.</span><span class="sxs-lookup"><span data-stu-id="4370a-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="4370a-125">Kiti mokėjimo tipai yra galimi ir banko sąskaita yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="4370a-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="4370a-126">Išplėskite skyrių **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="4370a-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="4370a-127">Lauke **Tekstinis kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="4370a-128">Šiame lauke nurodomas kodas, kuris bus rodomas gavėjo banko išraše.</span><span class="sxs-lookup"><span data-stu-id="4370a-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="4370a-129">Lauke **Pranešimas bankui** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="4370a-130">Lauke **Valiutos nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="4370a-131">Tai yra bet kurio būsimo ar fiksuoto valiutos kurso nuorodos numeris.</span><span class="sxs-lookup"><span data-stu-id="4370a-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="4370a-132">Lauke **Valiuta** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="4370a-133">Išduodant išankstinius pranešimus, šioje sekcijoje pateikiama jų būsenų (laukiama arba patvirtinta) apžvalga.</span><span class="sxs-lookup"><span data-stu-id="4370a-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="4370a-134">Išplėskite skyrių **Adresas**.</span><span class="sxs-lookup"><span data-stu-id="4370a-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="4370a-135">Išplėskite skyrių **Išankstinis pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="4370a-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="4370a-136">Išplėskite skyrių **Kontaktinė informacija**.</span><span class="sxs-lookup"><span data-stu-id="4370a-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="4370a-137">Lauke **Telefonas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4370a-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="4370a-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4370a-138">Close the page.</span></span>
23. <span data-ttu-id="4370a-139">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="4370a-139">Click **Edit**.</span></span>
24. <span data-ttu-id="4370a-140">Išplėskite skyrių **Mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="4370a-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="4370a-141">Lauke **Banko sąskaita** pažymėkite ką tik sukurtą sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="4370a-141">In the **Bank account** field, select the account that you've just created.</span></span>
26. <span data-ttu-id="4370a-142">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4370a-142">Click **Save**.</span></span> <span data-ttu-id="4370a-143">Adresą galima nuskaityti iš bankų grupės, jei ji nurodyta, arba galima jį įtraukti čia.</span><span class="sxs-lookup"><span data-stu-id="4370a-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

