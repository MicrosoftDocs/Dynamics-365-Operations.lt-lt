---
title: Pagrindiniai SF duomenys apie AP sistemą naudojant SF telkinį
description: Šioje temoje aprašoma, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7d72c1d98100d1313109e8b5e55df02e2163174
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189366"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="9f1e2-103">Pagrindiniai SF duomenys apie AP sistemą naudojant SF telkinį</span><span class="sxs-lookup"><span data-stu-id="9f1e2-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f1e2-104">Šioje temoje aprašoma, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="9f1e2-105">Tada naudodami SF telkinį sugretinkite SF su pirkimo užsakymu ir baikite išlaidas tiekėjo SF puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="9f1e2-106">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="9f1e2-106">Create a purchase order</span></span>
1. <span data-ttu-id="9f1e2-107">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="9f1e2-108">Pasirinkite **Naujas**, kad sukurtumėte pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="9f1e2-109">Lauke **Tiekėjo sąskaita** išplečiamajame sąraše pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="9f1e2-110">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="9f1e2-111">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-111">Select **OK**.</span></span>
5. <span data-ttu-id="9f1e2-112">Lauke **Prekės numeris** išplečiamajame sąraše pasirinkite paslaugų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="9f1e2-113">Pavyzdžiui, pasirinkite **S0001**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-113">For example, select **S0001**.</span></span> <span data-ttu-id="9f1e2-114">Grynoji suma yra 75,00.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-114">The net amount is 75.00.</span></span>  <span data-ttu-id="9f1e2-115">Tai suma, kurios tikėsimės SF.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="9f1e2-116">Veiksmų srityje pasirinkite **Pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="9f1e2-117">Pasirinkite **„Patvirtinti“**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="9f1e2-118">Kurti ir registruoti SF</span><span class="sxs-lookup"><span data-stu-id="9f1e2-118">Create and post and invoice</span></span>
1. <span data-ttu-id="9f1e2-119">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų registras**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="9f1e2-120">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-120">Select **New**.</span></span>
3. <span data-ttu-id="9f1e2-121">Atidarykite peržvalgą, kad pasirinktumėte norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="9f1e2-122">Pasirinkite norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="9f1e2-123">Pasirinkę **Eilutės**, atidarykite registrą ir įveskite išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="9f1e2-124">Peržvalgoje pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="9f1e2-125">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="9f1e2-126">Lauke **Sąskaita faktūra** įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="9f1e2-127">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="9f1e2-128">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="9f1e2-129">Lauke **Pirkimo užsakymas** atidarykite išplečiamąjį sąrašą ir pasirinkite anksčiau sukurtą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="9f1e2-130">Lauke **Patvirtino** išplečiamajame sąraše pažymėkite tvirtintoją ir spustelėkite **Pasirinkti**, kad jį pasirinktumėte.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="9f1e2-131">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="9f1e2-132">Atidarykite SF iš telkinio ir sugretinkite ją su pirkimo užsakymu, kad užbaigtumėte SF procesą</span><span class="sxs-lookup"><span data-stu-id="9f1e2-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="9f1e2-133">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų telkinys**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="9f1e2-134">Pasirinkę **Pirkimo užsakymas**, sukursite tiekėjo sąskaitą faktūrą pagal telkinyje esančią sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="9f1e2-135">Pasirinkite sąskaitą faktūrą, kurią norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="9f1e2-136">Pasirinkę **Naujinti gretinimo būseną**, užbaikite gretinimą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="9f1e2-137">Veiksmų srityje pasirinkite **Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="9f1e2-138">Pasirinkite **Keisti rodinį**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-138">Select **Change view**.</span></span>
7. <span data-ttu-id="9f1e2-139">Pasirinkite **Tinklelio rodinys**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="9f1e2-140">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-140">Select **Post**.</span></span>
9. <span data-ttu-id="9f1e2-141">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-141">Close the form.</span></span>
10. <span data-ttu-id="9f1e2-142">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Tiekėjai > Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="9f1e2-143">Pasirinkite tiekėją, kuris buvo ant pirkimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="9f1e2-144">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="9f1e2-145">Veiksmų srityje pasirinkite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="9f1e2-146">Pasirinkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="9f1e2-147">Pasirinkite savo sukurtą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-147">Select the invoice that you created.</span></span> <span data-ttu-id="9f1e2-148">SF registro kaupimas buvo atšauktas ir užregistruotas į atitinkamą išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="9f1e2-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

