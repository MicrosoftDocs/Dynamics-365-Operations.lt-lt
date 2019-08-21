---
title: Kliento mokėjimų apžvalga
description: Šis užduoties vadovas žingsnis po žingsnio apžvelgia įvairius klientų mokėjimų įvedimo būdus.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2168dd4074b6bd6da84dcf79db4dada9ca4d0138
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842062"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="94f96-103">Kliento mokėjimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="94f96-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94f96-104">Šis užduoties vadovas žingsnis po žingsnio apžvelgia įvairius klientų mokėjimų įvedimo būdus.</span><span class="sxs-lookup"><span data-stu-id="94f96-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="94f96-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="94f96-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="94f96-106">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="94f96-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="94f96-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="94f96-107">Click New.</span></span>
3. <span data-ttu-id="94f96-108">Pasirinkite mokėjimų žurnalą, kuriame bus įrašomi klientų mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="94f96-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="94f96-109">Pasirinkite arba rankiniu būdu įveskite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="94f96-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="94f96-110">Spustelėkite Įvesti kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="94f96-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="94f96-111">„Įvesti kliento mokėjimus“ yra naudojama vienu metu įrašyti vieno kliento mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="94f96-112">Viršuje įveskite mokėjimo informaciją, tada galėsite pažymite sąskaitas faktūras, kurios buvo apmokėtos šiuo mokėjimu – visa tai atlikdami iš to paties puslapio.</span><span class="sxs-lookup"><span data-stu-id="94f96-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="94f96-113">Įveskite klientą, iš kurio gavote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="94f96-114">Jei nežinote kliento, bet žinote įvykdytą mokėjimo operaciją, galite įvesti mokėjimą lauke „Operacija“.</span><span class="sxs-lookup"><span data-stu-id="94f96-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="94f96-115">Įveskite arba pasirinkite sąskaitą faktūrą lauke „Operacija“.</span><span class="sxs-lookup"><span data-stu-id="94f96-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="94f96-116">Jums pasirinkus tą operaciją, klientas bus automatiškai rodomas pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="94f96-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="94f96-117">Lauke „Mokėjimo nuoroda“ įveskite mokėjimo nuorodą.</span><span class="sxs-lookup"><span data-stu-id="94f96-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="94f96-118">Mokėjimo nuoroda gali būti kliento čekio numeris arba nuoroda iš kliento elektroninio mokėjimo.</span><span class="sxs-lookup"><span data-stu-id="94f96-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="94f96-119">Mokėjimo nuorodos reikia tik tuomet, jei pažymėsite, kad mokėjimas būtų įtrauktas į mokėjimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="94f96-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="94f96-120">Pasirinkite, ar mokėjimas bus įtrauktas į mokėjimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="94f96-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="94f96-121">Įveskite kliento sumokėtą sumą.</span><span class="sxs-lookup"><span data-stu-id="94f96-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="94f96-122">Mokėjimo suma neatsiras kaip numatytoji.</span><span class="sxs-lookup"><span data-stu-id="94f96-122">The payment amount will not default.</span></span> <span data-ttu-id="94f96-123">Ji turi būti įvesta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="94f96-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="94f96-124">Pažymėkite kliento apmokėtas SF.</span><span class="sxs-lookup"><span data-stu-id="94f96-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="94f96-125">Jei mokėjimas yra išankstinis, jums nereikia pažymėti jokių sąskaitų faktūrų sudengimui.</span><span class="sxs-lookup"><span data-stu-id="94f96-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="94f96-126">Mokėjimą vis dar galima dar įrašyti ir registruoti.</span><span class="sxs-lookup"><span data-stu-id="94f96-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="94f96-127">Sudengti sąskaitą faktūrą bus galima vėliau..</span><span class="sxs-lookup"><span data-stu-id="94f96-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="94f96-128">Įveskite mokėjimo sumą, kurią reikia sudengti pagal pažymėtą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="94f96-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="94f96-129">Šį lauką galima naudoti, kai mokėjimas yra dalinis.</span><span class="sxs-lookup"><span data-stu-id="94f96-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="94f96-130">Jei neįvesite sumos, sudengimo suma bus nustatoma už jus automatiškai.</span><span class="sxs-lookup"><span data-stu-id="94f96-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="94f96-131">Spustelėkite „Įrašyti į žurnalą“.</span><span class="sxs-lookup"><span data-stu-id="94f96-131">Click Save in journal.</span></span>
    * <span data-ttu-id="94f96-132">Prieš įrašydami mokėjimą į žurnalą įsitikinkite, kad nurodyta korespondentinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="94f96-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="94f96-133">Žurnale paspaudus „Įrašyti“, mokėjimas bus įrašytas ir perkeltas į žurnalą.</span><span class="sxs-lookup"><span data-stu-id="94f96-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="94f96-134">Tuomet galite toliau įvesti kitą mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="94f96-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="94f96-135">Close the page.</span></span>
14. <span data-ttu-id="94f96-136">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="94f96-136">Click Lines.</span></span>
    * <span data-ttu-id="94f96-137">Atidarydami eilutes matysite visus mokėjimus, kuriuos įrašėte į puslapį „Įvesti klientų mokėjimus“ ir į žurnalą.</span><span class="sxs-lookup"><span data-stu-id="94f96-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="94f96-138">Taip pat galite naudoti šį puslapį norėdami įvesti naujus klientų mokėjimus arba redaguoti esamus klientų mokėjimus prieš juos registruodami.</span><span class="sxs-lookup"><span data-stu-id="94f96-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="94f96-139">Spustelėkite „Naujas“, kad sukurtumėte kitą mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="94f96-140">Pažymėkite klientą, iš kurio gavote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="94f96-141">Jei nežinote kliento, bet žinote įvykdytą mokėjimo operaciją, galite įvesti arba pažymėti sąskaitą faktūrą rankiniu būdu lauke „Sąskaita faktūra“.</span><span class="sxs-lookup"><span data-stu-id="94f96-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="94f96-142">Pasirinkus sąskaitą faktūrą klientas bus rodomas kaip numatytasis.</span><span class="sxs-lookup"><span data-stu-id="94f96-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="94f96-143">Spustelėkite „Sudengti operacijas“ norėdami pažymėti apmokėtas sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="94f96-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="94f96-144">Nereikia sudengti jokių sąskaitų faktūrų mokėjimo.</span><span class="sxs-lookup"><span data-stu-id="94f96-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="94f96-145">Jei tai išankstinis mokėjimas ar jei nežinote, kokia sąskaita faktūra buvo apmokėta, galite įvesti ir registruoti mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="94f96-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="94f96-146">Mokėjimą sudengti pagal sąskaitą faktūrą bus galima vėliau.</span><span class="sxs-lookup"><span data-stu-id="94f96-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="94f96-147">Pažymėkite sąskaitas faktūras, kurios buvo apmokėtos pasirinktu mokėjimu.</span><span class="sxs-lookup"><span data-stu-id="94f96-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="94f96-148">Įveskite mokėjimo sumą, kuri bus sudengta pagal sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="94f96-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="94f96-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="94f96-149">Click OK.</span></span>
21. <span data-ttu-id="94f96-150">Lauke „Mokėjimo nuoroda“ įveskite mokėjimo nuorodą.</span><span class="sxs-lookup"><span data-stu-id="94f96-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="94f96-151">.</span><span class="sxs-lookup"><span data-stu-id="94f96-151">.</span></span>
    * <span data-ttu-id="94f96-152">Mokėjimo nuorodos reikia tik tuomet, jei pažymėsite, kad mokėjimas būtų įtrauktas į mokėjimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="94f96-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="94f96-153">Registruokite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="94f96-153">Post the customer payments.</span></span> 

