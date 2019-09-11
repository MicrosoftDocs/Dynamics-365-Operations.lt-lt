---
title: Kurti kliento tiesioginio debeto įgaliojimą
description: Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916374"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="7b5ac-103">Kurti kliento tiesioginio debeto įgaliojimą</span><span class="sxs-lookup"><span data-stu-id="7b5ac-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b5ac-104">Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="7b5ac-105">Kurti banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="7b5ac-105">Create a bank account</span></span>
1. <span data-ttu-id="7b5ac-106">**Naršymo srityje** eikite į **Moduliai > Gautinos sumos > Klientai > Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="7b5ac-107">Sąraše pažymėkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-107">In the list, select a record.</span></span> <span data-ttu-id="7b5ac-108">Pavyzdžiui, pasirinkite US-001</span><span class="sxs-lookup"><span data-stu-id="7b5ac-108">For example, select US-001</span></span>
3. <span data-ttu-id="7b5ac-109">Veiksmų srityje spustelėkite **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="7b5ac-110">Spustelėkite **Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="7b5ac-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-111">Click **New**.</span></span>
6. <span data-ttu-id="7b5ac-112">Lauke **Banko sąskaita** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="7b5ac-113">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="7b5ac-114">Lauke **IBAN** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="7b5ac-115">Lauke **Valiuta** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="7b5ac-116">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-116">Click **Save**.</span></span>
11. <span data-ttu-id="7b5ac-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-117">Close the page.</span></span>
12. <span data-ttu-id="7b5ac-118">**Naršymo sritis** eikite į **Moduliai > Pinigų ir banko valdymas > Banko sąskaitos > Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="7b5ac-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="7b5ac-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="7b5ac-121">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-121">Click **Edit**.</span></span>
16. <span data-ttu-id="7b5ac-122">Išplėskite „fastTab“ **Papildomas identifikavimas**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="7b5ac-123">Lauke **Tiesioginio debeto ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="7b5ac-124">Lauke **IBAN** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="7b5ac-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-125">Close the page.</span></span>
20. <span data-ttu-id="7b5ac-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="7b5ac-127">Apibrėžti elektroninio mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="7b5ac-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="7b5ac-128">**Naršymo sritis** eikite į **Moduliai > Gautinos sumos > Mokėjimų sąranką > Mokėjimo būdai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="7b5ac-129">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-129">Click **New**.</span></span>
3. <span data-ttu-id="7b5ac-130">Lauke **Mokėjimo būdas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="7b5ac-131">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7b5ac-132">Lauke **Mokėjimo tipas** įveskite „Elektroninis mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="7b5ac-133">Tiesioginio debeto įgaliojimo mokėjimo tipas turi būti Elektroninis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="7b5ac-134">Pažymėkite Taip lauke **Reikia įgaliojimo**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="7b5ac-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="7b5ac-136">Prie kliento pridėkite tiesioginio debeto įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="7b5ac-137">**Naršymo srityje** eikite į **Moduliai > Gautinos sumos > Klientai > Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="7b5ac-138">Sąraše pažymėkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-138">In the list, select a record.</span></span> <span data-ttu-id="7b5ac-139">Pavyzdžiui, pasirinkite US-001</span><span class="sxs-lookup"><span data-stu-id="7b5ac-139">For example, select US-001</span></span>
3. <span data-ttu-id="7b5ac-140">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-140">Click **Edit**.</span></span>
4. <span data-ttu-id="7b5ac-141">Išplėskite „fastTab“ **Numatytieji mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="7b5ac-142">Lauke **Mokėjimo metodas** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="7b5ac-143">Išplėskite „fastTab“ **Numatytieji mokėjimai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="7b5ac-144">Išplėskite „fastTab“ **Tiesioginio debeto įgaliojimai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="7b5ac-145">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-145">Click **Add**.</span></span>
9. <span data-ttu-id="7b5ac-146">Lauke **Banko sąskaita** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="7b5ac-147">Lauke **Kreditoriaus banko sąskaita** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="7b5ac-148">Lauke **Mokėjimo dažnumas** įveskite mokėjimų skaičių, kurį tikitės apdoroti pagal šį įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="7b5ac-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-149">Click **OK**.</span></span>
13. <span data-ttu-id="7b5ac-150">Spustelėkite **Spausdinti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-150">Click **Print**.</span></span>
14. <span data-ttu-id="7b5ac-151">Spustelėkite **Įgaliojimo ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="7b5ac-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-152">Close the page.</span></span>
16. <span data-ttu-id="7b5ac-153">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-153">Click **Edit**.</span></span>
17. <span data-ttu-id="7b5ac-154">Lauke **Parašo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="7b5ac-155">Spustelėkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-155">Click **Yes**.</span></span>
19. <span data-ttu-id="7b5ac-156">Įveskite vietą, kurioje buvo pasirašytas įgaliojimas.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="7b5ac-157">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-157">Click **OK**.</span></span>
21. <span data-ttu-id="7b5ac-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="7b5ac-159">Kurti laisvos formos SF su įgaliojimu</span><span class="sxs-lookup"><span data-stu-id="7b5ac-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="7b5ac-160">**Naršymo sritis** eikite į **Moduliai > Gautinos sumos > Sąskaita-faktūra > Visos laisvos formos sąskaitos-faktūros**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="7b5ac-161">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-161">Click **New**.</span></span>
3. <span data-ttu-id="7b5ac-162">Pasirinkite klientą, prie kurio pridėjote įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="7b5ac-163">Lauke **Tiesioginio debeto įgaliojimo ID** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7b5ac-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

