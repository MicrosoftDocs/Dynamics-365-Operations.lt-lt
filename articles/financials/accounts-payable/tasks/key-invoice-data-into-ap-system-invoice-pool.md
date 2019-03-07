---
title: Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį
description: Šis užduočių vadovas parodys, kaip naudoti registrą kurti SF.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b4e9a52a383d4acc0bf2adc669fd88c0c0f7402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "357455"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="bb0f4-103">Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį</span><span class="sxs-lookup"><span data-stu-id="bb0f4-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb0f4-104">Šis užduočių vadovas parodys, kaip naudoti registrą kurti SF.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="bb0f4-105">Tada naudodami SF telkinį sugretinkite SF su pirkimo užsakymu ir baikite išlaidas tiekėjo SF puslapyje.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bb0f4-106">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="bb0f4-106">Create a purchase order</span></span>
1. <span data-ttu-id="bb0f4-107">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="bb0f4-108">Spustelėkite Naujas, kad sukurtumėte pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="bb0f4-109">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="bb0f4-110">Iš sąrašo pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-110">Select the vendor from the list.</span></span> <span data-ttu-id="bb0f4-111">Pavyzdžiui, tiekėją 1001.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="bb0f4-112">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-112">Click OK.</span></span>
6. <span data-ttu-id="bb0f4-113">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="bb0f4-114">Sąraše raskite paslaugų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-114">Find the services item number in the list.</span></span> <span data-ttu-id="bb0f4-115">Pavyzdžiui, pasirinkite S0001.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-115">For example, select S0001.</span></span>
8. <span data-ttu-id="bb0f4-116">Spustelėkite ant prekės numerio ir jį pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="bb0f4-117">Grynoji suma yra 75,00.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-117">The net amount is 75.00.</span></span>  <span data-ttu-id="bb0f4-118">Tai suma, kurios tikėsimės SF.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="bb0f4-119">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="bb0f4-120">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="bb0f4-121">Kurti ir registruoti SF</span><span class="sxs-lookup"><span data-stu-id="bb0f4-121">Create and post and invoice</span></span>
1. <span data-ttu-id="bb0f4-122">Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF registras.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="bb0f4-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-123">Click New.</span></span>
3. <span data-ttu-id="bb0f4-124">Atidarykite peržvalgą, kad pasirinktumėte norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="bb0f4-125">Pasirinkite norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="bb0f4-126">Spustelėdami Eilutės atidarykite registrą ir įveskite išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="bb0f4-127">Peržvalgoje pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="bb0f4-128">Pavyzdžiui, spustelėkite ant tiekėjo 1001.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="bb0f4-129">Lauke Sąskaita faktūra įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="bb0f4-130">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="bb0f4-131">Lauke Kreditas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="bb0f4-132">Lauke Pirkimo užsakymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="bb0f4-133">Pasirinkite savo anksčiau sukurtą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="bb0f4-134">Lauke Patvirtino spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="bb0f4-135">Pažymėkite tvirtintoją ir spustelėkite Pasirinkti, kad tą tvirtintoją pasirinktumėte.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="bb0f4-136">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-136">Click Post.</span></span>
15. <span data-ttu-id="bb0f4-137">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-137">Close the form.</span></span>
16. <span data-ttu-id="bb0f4-138">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="bb0f4-139">Atidarykite SF iš telkinio ir sugretinkite ją su pirkimo užsakymu, kad užbaigtumėte SF procesą</span><span class="sxs-lookup"><span data-stu-id="bb0f4-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="bb0f4-140">Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF telkinys.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="bb0f4-141">Spustelėkite Pirkimo užsakymas, kad iš SF telkinyje sukurtumėte tiekėjo sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="bb0f4-142">Pasirinkite sąskaitą faktūrą, kurią norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="bb0f4-143">Spustelėkite Naujinti gretinimo būseną, kad užbaigtumėte gretinimą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="bb0f4-144">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="bb0f4-145">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-145">Click Change view.</span></span>
7. <span data-ttu-id="bb0f4-146">Spustelėkite Tinklelio rodinys.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-146">Click Grid view.</span></span>
8. <span data-ttu-id="bb0f4-147">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-147">Click Post.</span></span>
9. <span data-ttu-id="bb0f4-148">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-148">Close the form.</span></span>
10. <span data-ttu-id="bb0f4-149">Eikite į Mokėtinos sumos > Tiekėjai > Tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="bb0f4-150">Pasirinkite tiekėją, kuris buvo ant pirkimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="bb0f4-151">Pavyzdžiui, pasirinkite tiekėją 1001.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="bb0f4-152">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="bb0f4-153">Veiksmų srityje spustelėkite Tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="bb0f4-154">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-154">Click Transactions.</span></span>
15. <span data-ttu-id="bb0f4-155">Pasirinkite savo sukurtą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="bb0f4-156">SF registro kaupimas buvo atšauktas ir užregistruotas į atitinkamą išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="bb0f4-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

