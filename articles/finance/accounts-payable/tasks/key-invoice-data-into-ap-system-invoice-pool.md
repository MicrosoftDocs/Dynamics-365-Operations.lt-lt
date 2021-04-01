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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227165"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="fe753-103">Pagrindiniai SF duomenys apie AP sistemą naudojant SF telkinį</span><span class="sxs-lookup"><span data-stu-id="fe753-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe753-104">Šioje temoje aprašoma, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="fe753-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="fe753-105">Tada naudodami SF telkinį sugretinkite SF su pirkimo užsakymu ir baikite išlaidas tiekėjo SF puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fe753-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="fe753-106">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe753-106">Create a purchase order</span></span>
1. <span data-ttu-id="fe753-107">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="fe753-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="fe753-108">Pasirinkite **Naujas**, kad sukurtumėte pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="fe753-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="fe753-109">Lauke **Tiekėjo sąskaita** išplečiamajame sąraše pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="fe753-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="fe753-110">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="fe753-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="fe753-111">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fe753-111">Select **OK**.</span></span>
5. <span data-ttu-id="fe753-112">Lauke **Prekės numeris** išplečiamajame sąraše pasirinkite paslaugų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="fe753-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="fe753-113">Pavyzdžiui, pasirinkite **S0001**.</span><span class="sxs-lookup"><span data-stu-id="fe753-113">For example, select **S0001**.</span></span> <span data-ttu-id="fe753-114">Grynoji suma yra 75,00.</span><span class="sxs-lookup"><span data-stu-id="fe753-114">The net amount is 75.00.</span></span>  <span data-ttu-id="fe753-115">Tai suma, kurios tikėsimės SF.</span><span class="sxs-lookup"><span data-stu-id="fe753-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="fe753-116">Veiksmų srityje pasirinkite **Pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="fe753-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="fe753-117">Pasirinkite **„Patvirtinti“**.</span><span class="sxs-lookup"><span data-stu-id="fe753-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="fe753-118">Kurti ir registruoti SF</span><span class="sxs-lookup"><span data-stu-id="fe753-118">Create and post and invoice</span></span>
1. <span data-ttu-id="fe753-119">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų registras**.</span><span class="sxs-lookup"><span data-stu-id="fe753-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="fe753-120">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fe753-120">Select **New**.</span></span>
3. <span data-ttu-id="fe753-121">Atidarykite peržvalgą, kad pasirinktumėte norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fe753-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="fe753-122">Pasirinkite norimo naudoti SF registro pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fe753-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="fe753-123">Pasirinkę **Eilutės**, atidarykite registrą ir įveskite išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="fe753-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="fe753-124">Peržvalgoje pasirinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="fe753-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="fe753-125">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="fe753-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="fe753-126">Lauke **Sąskaita faktūra** įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="fe753-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="fe753-127">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe753-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="fe753-128">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe753-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="fe753-129">Lauke **Pirkimo užsakymas** atidarykite išplečiamąjį sąrašą ir pasirinkite anksčiau sukurtą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="fe753-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="fe753-130">Lauke **Patvirtino** išplečiamajame sąraše pažymėkite tvirtintoją ir spustelėkite **Pasirinkti**, kad jį pasirinktumėte.</span><span class="sxs-lookup"><span data-stu-id="fe753-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="fe753-131">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="fe753-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="fe753-132">Atidarykite SF iš telkinio ir sugretinkite ją su pirkimo užsakymu, kad užbaigtumėte SF procesą</span><span class="sxs-lookup"><span data-stu-id="fe753-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="fe753-133">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų telkinys**.</span><span class="sxs-lookup"><span data-stu-id="fe753-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="fe753-134">Pasirinkę **Pirkimo užsakymas**, sukursite tiekėjo sąskaitą faktūrą pagal telkinyje esančią sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="fe753-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="fe753-135">Pasirinkite sąskaitą faktūrą, kurią norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="fe753-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="fe753-136">Pasirinkę **Naujinti gretinimo būseną**, užbaikite gretinimą.</span><span class="sxs-lookup"><span data-stu-id="fe753-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="fe753-137">Veiksmų srityje pasirinkite **Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="fe753-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="fe753-138">Pasirinkite **Keisti rodinį**.</span><span class="sxs-lookup"><span data-stu-id="fe753-138">Select **Change view**.</span></span>
7. <span data-ttu-id="fe753-139">Pasirinkite **Tinklelio rodinys**.</span><span class="sxs-lookup"><span data-stu-id="fe753-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="fe753-140">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="fe753-140">Select **Post**.</span></span>
9. <span data-ttu-id="fe753-141">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="fe753-141">Close the form.</span></span>
10. <span data-ttu-id="fe753-142">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Tiekėjai > Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="fe753-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="fe753-143">Pasirinkite tiekėją, kuris buvo ant pirkimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="fe753-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="fe753-144">Pavyzdžiui, pasirinkite tiekėją **1001**.</span><span class="sxs-lookup"><span data-stu-id="fe753-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="fe753-145">Veiksmų srityje pasirinkite **Tiekėjas**.</span><span class="sxs-lookup"><span data-stu-id="fe753-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="fe753-146">Pasirinkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="fe753-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="fe753-147">Pasirinkite savo sukurtą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="fe753-147">Select the invoice that you created.</span></span> <span data-ttu-id="fe753-148">SF registro kaupimas buvo atšauktas ir užregistruotas į atitinkamą išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="fe753-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]