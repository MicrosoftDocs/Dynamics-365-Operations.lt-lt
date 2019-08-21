---
title: Pagrindiniai SF duomenys AP sistemoje naudojant tiekėjo SF
description: Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7abae6d680d899a0294ad3c298a4b0264ba01d0b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835435"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="0d992-103">Pagrindiniai SF duomenys AP sistemoje naudojant tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="0d992-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d992-104">Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0d992-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="0d992-105">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="0d992-105">Create a purchase order</span></span>
1. <span data-ttu-id="0d992-106">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0d992-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="0d992-107">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0d992-107">Click **New**.</span></span>
3. <span data-ttu-id="0d992-108">Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0d992-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0d992-109">Raskite tiekėją, kurį norite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="0d992-109">Find a vendor to select.</span></span> <span data-ttu-id="0d992-110">Pavyzdžiui, slinkite žemyn iki US-104.</span><span class="sxs-lookup"><span data-stu-id="0d992-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="0d992-111">Pasirinkite tiekėją US-104.</span><span class="sxs-lookup"><span data-stu-id="0d992-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="0d992-112">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0d992-112">Click **OK**.</span></span>
7. <span data-ttu-id="0d992-113">Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0d992-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0d992-114">Pasirinkite atsargų prekę.</span><span class="sxs-lookup"><span data-stu-id="0d992-114">Select an inventory item.</span></span> <span data-ttu-id="0d992-115">Pavyzdžiui, pasirinkite prekės numerį 1000.</span><span class="sxs-lookup"><span data-stu-id="0d992-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="0d992-116">Išplėskite FastTab **Line details**.</span><span class="sxs-lookup"><span data-stu-id="0d992-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="0d992-117">Spustelėkite skirtuką **Setup**. Galite netaikyti atitikimo politikos, kad nenaudotumėte atitikimo, dvipusio ar trijų krypčių atitikimo.</span><span class="sxs-lookup"><span data-stu-id="0d992-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="0d992-118">Veiksmų srityje spustelėkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="0d992-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="0d992-119">Spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="0d992-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="0d992-120">Produktų gavimas</span><span class="sxs-lookup"><span data-stu-id="0d992-120">Receive the products</span></span>
1. <span data-ttu-id="0d992-121">Veiksmų srityje spustelėkite **Gauti**.</span><span class="sxs-lookup"><span data-stu-id="0d992-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="0d992-122">Spustelėkite **Produkto gavimo kvitas**.</span><span class="sxs-lookup"><span data-stu-id="0d992-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="0d992-123">Lauke **Produkto gavimo kvitas** įveskite produkto gavimo kvito numerį.</span><span class="sxs-lookup"><span data-stu-id="0d992-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="0d992-124">Pavyzdžiui, įveskite PR123.</span><span class="sxs-lookup"><span data-stu-id="0d992-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="0d992-125">Spustelėkite **OK**, kad registruotumėte produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="0d992-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="0d992-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0d992-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="0d992-127">Kurti tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="0d992-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="0d992-128">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai gauti, bet SF neišrašyta**.</span><span class="sxs-lookup"><span data-stu-id="0d992-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="0d992-129">Pasirinkite savo sukurtą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0d992-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="0d992-130">Veiksmų srityje spustelėkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="0d992-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="0d992-131">Spustelėkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="0d992-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="0d992-132">Lauke **Numeris** įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="0d992-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="0d992-133">Lauke **Sąskaitos faktūros aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d992-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="0d992-134">Lauke **SF data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0d992-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="0d992-135">Lauke **Vieneto kaina** įveskite 1200.</span><span class="sxs-lookup"><span data-stu-id="0d992-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="0d992-136">Spustelėkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="0d992-136">Click **Add line**.</span></span>
10. <span data-ttu-id="0d992-137">Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0d992-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0d992-138">Sąraše raskite diegimo išlaidų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="0d992-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="0d992-139">Pavyzdžiui, S0001</span><span class="sxs-lookup"><span data-stu-id="0d992-139">For example, S0001</span></span>
12. <span data-ttu-id="0d992-140">Pasirinkite diegimo išlaidų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="0d992-140">Select the installation charge item number.</span></span> <span data-ttu-id="0d992-141">Atkreipkite dėmesį, kad nuo jūsų pakeitimų negretinta.</span><span class="sxs-lookup"><span data-stu-id="0d992-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="0d992-142">Spustelėkite **Naujinti gretinimo būseną**.</span><span class="sxs-lookup"><span data-stu-id="0d992-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="0d992-143">Veiksmų srityje spustelėkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="0d992-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="0d992-144">Spustelėkite **Gretinimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="0d992-144">Click **Matching details**.</span></span> <span data-ttu-id="0d992-145">Naujos eilutės su paslaugomis gretinti nereikia, todėl būsena yra „Neatlikta‟.</span><span class="sxs-lookup"><span data-stu-id="0d992-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="0d992-146">Pasirinkite atsargų prekės, kurią gavote, produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="0d992-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="0d992-147">Eilutė, kurioje yra produkto gavimo kvitas, buvo sugretinta, tačiau neatitinka kiekis arba kaina, todėl sugretinti nepavyko.</span><span class="sxs-lookup"><span data-stu-id="0d992-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="0d992-148">Lauke **Unit price** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d992-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="0d992-149">Dabar, kai vieneto kaina atitinka, būsena atnaujinama į Pavyko.</span><span class="sxs-lookup"><span data-stu-id="0d992-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="0d992-150">Jei jūsų strategija leidžia nesutapimus arba jei gretinimas yra tik įspėjimas, SF vis tiek galite registruoti.</span><span class="sxs-lookup"><span data-stu-id="0d992-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="0d992-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0d992-151">Close the page.</span></span>
19. <span data-ttu-id="0d992-152">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="0d992-152">Click **Post**.</span></span>
20. <span data-ttu-id="0d992-153">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="0d992-153">Close the form.</span></span> <span data-ttu-id="0d992-154">Atkreipkite dėmesį, kad pirkimo užsakymas pateikiamas nebe kaip gautas, o kaip užsakymas, kuriam neišrašyta SF.</span><span class="sxs-lookup"><span data-stu-id="0d992-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

