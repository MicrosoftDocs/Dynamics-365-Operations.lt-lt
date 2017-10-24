--- 
title: "Kurti kliento tiesioginio debeto įgaliojimą"
description: "Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="25103-103">Kurti kliento tiesioginio debeto įgaliojimą</span><span class="sxs-lookup"><span data-stu-id="25103-103">Create a direct debit mandate for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25103-104">Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.</span><span class="sxs-lookup"><span data-stu-id="25103-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="25103-105">Kurti banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="25103-105">Create a bank account</span></span>
1. <span data-ttu-id="25103-106">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="25103-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="25103-107">Pavyzdžiui, pasirinkite US-001</span><span class="sxs-lookup"><span data-stu-id="25103-107">For example, select US-001</span></span>
3. <span data-ttu-id="25103-108">Veiksmų srityje spustelėkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="25103-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="25103-109">Spustelėkite Banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="25103-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="25103-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25103-110">Click New.</span></span>
6. <span data-ttu-id="25103-111">Lauke Banko sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="25103-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="25103-113">Lauke IBAN surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="25103-114">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="25103-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25103-115">Click Save.</span></span>
11. <span data-ttu-id="25103-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-116">Close the page.</span></span>
12. <span data-ttu-id="25103-117">Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.</span><span class="sxs-lookup"><span data-stu-id="25103-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="25103-118">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="25103-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="25103-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="25103-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="25103-120">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25103-120">Click Edit.</span></span>
16. <span data-ttu-id="25103-121">Išplėskite skyrių Papildoma identifikacija.</span><span class="sxs-lookup"><span data-stu-id="25103-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="25103-122">Lauke Tiesioginio debeto ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="25103-123">Lauke IBAN surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="25103-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-124">Close the page.</span></span>
20. <span data-ttu-id="25103-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="25103-126">Apibrėžti elektroninio mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="25103-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="25103-127">Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="25103-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="25103-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25103-128">Click New.</span></span>
3. <span data-ttu-id="25103-129">Lauke Mokėjimo būdas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="25103-130">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25103-131">Tiesioginio debeto įgaliojimo mokėjimo tipas turi būti Elektroninis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="25103-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="25103-132">Lauke Reikalauti įgaliojimo pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25103-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="25103-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="25103-134">Prie kliento pridėkite tiesioginio debeto įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="25103-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="25103-135">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="25103-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="25103-136">Pavyzdžiui, pasirinkite US-001</span><span class="sxs-lookup"><span data-stu-id="25103-136">For example, select US-001</span></span>
3. <span data-ttu-id="25103-137">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25103-137">Click Edit.</span></span>
4. <span data-ttu-id="25103-138">Išplėskite dalį Numatytosios mokėjimo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="25103-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="25103-139">Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25103-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="25103-140">Išplėskite dalį Numatytosios mokėjimo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="25103-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="25103-141">Išplėskite dalį Tiesioginio debeto įgaliojimai.</span><span class="sxs-lookup"><span data-stu-id="25103-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="25103-142">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25103-142">Click Add.</span></span>
9. <span data-ttu-id="25103-143">Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="25103-144">Lauke Kreditoriaus banko sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25103-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="25103-145">Įveskite šio įgaliojimo mokėjimų, kuriuos numatote apdoroti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="25103-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="25103-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="25103-146">Click OK.</span></span>
13. <span data-ttu-id="25103-147">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="25103-147">Click Print.</span></span>
14. <span data-ttu-id="25103-148">Spustelėkite Įgaliojimo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="25103-148">Click Mandate report.</span></span>
15. <span data-ttu-id="25103-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-149">Close the page.</span></span>
16. <span data-ttu-id="25103-150">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25103-150">Click Edit.</span></span>
17. <span data-ttu-id="25103-151">Lauke Pasirašymo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="25103-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="25103-152">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25103-152">Click Yes.</span></span>
19. <span data-ttu-id="25103-153">Įveskite vietą, kurioje buvo pasirašytas įgaliojimas.</span><span class="sxs-lookup"><span data-stu-id="25103-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="25103-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="25103-154">Click OK.</span></span>
21. <span data-ttu-id="25103-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25103-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="25103-156">Kurti laisvos formos SF su įgaliojimu</span><span class="sxs-lookup"><span data-stu-id="25103-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="25103-157">Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="25103-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="25103-158">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25103-158">Click New.</span></span>
3. <span data-ttu-id="25103-159">Pasirinkite klientą, prie kurio pridėjote įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="25103-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="25103-160">Lauke Tiesioginio debeto įgaliojimo ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25103-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


