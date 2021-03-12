---
title: Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus
description: Šioje procedūroje parodoma, kaip generuoti ISO20022 tiesioginio debeto mokėjimo failą klientui, turinčiam sukonfigūruotą tiesioginį debetą ir SF apmokėti.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 934d086661dbbf1c7ba1d868f90caafe5b0bebf2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964571"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="6306a-103">Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus</span><span class="sxs-lookup"><span data-stu-id="6306a-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6306a-104">Šioje procedūroje parodoma, kaip generuoti ISO20022 tiesioginio debeto mokėjimo failą klientui, turinčiam sukonfigūruotą tiesioginį debetą ir SF apmokėti.</span><span class="sxs-lookup"><span data-stu-id="6306a-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="6306a-105">SF kūrimas ir registravimas nėra būtinas.</span><span class="sxs-lookup"><span data-stu-id="6306a-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="6306a-106">Užuot nustatę, kad SF turi būti apmokėta, žurnale galite pasirinkti įgaliojimą prieš generuodami mokėjimo failą, kad būtų palaikomas kliento išankstinio mokėjimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="6306a-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="6306a-107">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.</span><span class="sxs-lookup"><span data-stu-id="6306a-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="6306a-108">Tai yra penktoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="6306a-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="6306a-109">Prieš atlikdami šią užduotį, turite baigti ankstesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="6306a-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="6306a-110">Pirmiausia turite importuoti kliento mokėjimo elektroninių ataskaitų konfigūracijas, sukonfigūruoti mokėjimų metodus ir nustatyti savo įmonės bei kliento informaciją.</span><span class="sxs-lookup"><span data-stu-id="6306a-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="6306a-111">Registruoti laisvos formos SF su tiesioginio debeto informacija</span><span class="sxs-lookup"><span data-stu-id="6306a-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="6306a-112">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="6306a-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="6306a-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6306a-113">Click New.</span></span>
3. <span data-ttu-id="6306a-114">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6306a-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="6306a-115">Pavyzdžiui, pasirinkite DE-010.</span><span class="sxs-lookup"><span data-stu-id="6306a-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="6306a-116">Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="6306a-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="6306a-117">Pavyzdžiui,</span><span class="sxs-lookup"><span data-stu-id="6306a-117">For example.</span></span> <span data-ttu-id="6306a-118">pasirinkite Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="6306a-118">select Electronic.</span></span>  
5. <span data-ttu-id="6306a-119">Lauke Tiesioginio debeto įgaliojimo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="6306a-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="6306a-120">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="6306a-120">Click Add line.</span></span>
7. <span data-ttu-id="6306a-121">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6306a-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="6306a-122">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="6306a-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="6306a-123">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="6306a-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="6306a-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="6306a-124">Click Post.</span></span>
11. <span data-ttu-id="6306a-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6306a-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="6306a-126">Kurti mokėjimą</span><span class="sxs-lookup"><span data-stu-id="6306a-126">Create a payment</span></span>
1. <span data-ttu-id="6306a-127">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="6306a-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="6306a-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6306a-128">Click New.</span></span>
3. <span data-ttu-id="6306a-129">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6306a-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="6306a-130">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="6306a-130">Click Lines.</span></span>
5. <span data-ttu-id="6306a-131">Spustelėkite Mokėjimo pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="6306a-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="6306a-132">Spustelėkite Kurti mokėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="6306a-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="6306a-133">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="6306a-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="6306a-134">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="6306a-134">Click Filter.</span></span>
9. <span data-ttu-id="6306a-135">Sąraše pasirinkite lentelės Kliento operacijos eilutę ir lauką Mokėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="6306a-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="6306a-136">Galite taikyti bet kokius kriterijus, norėdami pasirinkti, kurias kliento operacijas apmokėti.</span><span class="sxs-lookup"><span data-stu-id="6306a-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="6306a-137">Šiame pavyzdyje norėdami filtruoti operacijas naudokite apmokėjimo būdą Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="6306a-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="6306a-138">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6306a-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="6306a-139">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="6306a-139">Click OK.</span></span>
12. <span data-ttu-id="6306a-140">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="6306a-140">Click OK.</span></span>
13. <span data-ttu-id="6306a-141">Spustelėkite Kurti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="6306a-141">Click Create payments.</span></span>
