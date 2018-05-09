--- 
title: "Pagrindiniai SF duomenys mokėtinose sumose naudojant tiekėjo SF"
description: "Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bdc0ef1c23bcbe60a126aacef9940acee84dce89
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a><span data-ttu-id="bdb39-103">Pagrindiniai SF duomenys mokėtinose sumose naudojant tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="bdb39-103">Key invoice data into accounts payable using a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdb39-104">Šis užduočių vadovas jums padės iš pirkimo užsakymo sukurti tiekėjo SF ir peržiūrėti pirkimo užsakymo, gavimo kvito ir SF gretinimo (trišalis gretinimas) rezultatus.</span><span class="sxs-lookup"><span data-stu-id="bdb39-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bdb39-105">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="bdb39-105">Create a purchase order</span></span>
1. <span data-ttu-id="bdb39-106">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="bdb39-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="bdb39-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bdb39-107">Click New.</span></span>
3. <span data-ttu-id="bdb39-108">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bdb39-109">Raskite tiekėją, kurį norite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-109">Find a vendor to select.</span></span> <span data-ttu-id="bdb39-110">Pavyzdžiui, slinkite žemyn iki US-104.</span><span class="sxs-lookup"><span data-stu-id="bdb39-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="bdb39-111">Pasirinkite tiekėją US-104.</span><span class="sxs-lookup"><span data-stu-id="bdb39-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="bdb39-112">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="bdb39-112">Click OK.</span></span>
7. <span data-ttu-id="bdb39-113">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bdb39-114">Pasirinkite atsargų prekę.</span><span class="sxs-lookup"><span data-stu-id="bdb39-114">Select an inventory item.</span></span> <span data-ttu-id="bdb39-115">Pavyzdžiui, pasirinkite prekės numerį 1000.</span><span class="sxs-lookup"><span data-stu-id="bdb39-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="bdb39-116">Išplėskite arba sutraukite dalį Išsami eilučių informacija.</span><span class="sxs-lookup"><span data-stu-id="bdb39-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="bdb39-117">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="bdb39-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="bdb39-118">Galite nepaisyti atitikimo strategijos ir jos nenaudoti, naudoti dvišalę arba trišalę atitikimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="bdb39-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="bdb39-119">Išplėskite arba sutraukite dalį Išsami eilučių informacija.</span><span class="sxs-lookup"><span data-stu-id="bdb39-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="bdb39-120">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="bdb39-121">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="bdb39-122">Produktų gavimas</span><span class="sxs-lookup"><span data-stu-id="bdb39-122">Receive the products</span></span>
1. <span data-ttu-id="bdb39-123">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="bdb39-124">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="bdb39-124">Click Product receipt.</span></span>
3. <span data-ttu-id="bdb39-125">Lauke Produkto gavimo kvitas įveskite produkto gavimo kvito numerį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="bdb39-126">Pavyzdžiui, įveskite PR123.</span><span class="sxs-lookup"><span data-stu-id="bdb39-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="bdb39-127">Spustelėkite Gerai, kad registruotumėte produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="bdb39-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="bdb39-129">Kurti tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="bdb39-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="bdb39-130">Pasirinkite Mokėtinos sumos > Pirkimo užsakymai > Gauti pirkimo užsakymai, kuriems neišrašytos SF.</span><span class="sxs-lookup"><span data-stu-id="bdb39-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="bdb39-131">Pasirinkite savo sukurtą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="bdb39-132">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="bdb39-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="bdb39-133">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="bdb39-133">Click Invoice.</span></span>
5. <span data-ttu-id="bdb39-134">Lauke Numeris įveskite SF numerį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="bdb39-135">Lauke Sąskaitos faktūros aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bdb39-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="bdb39-136">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="bdb39-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="bdb39-137">Lauke Vieneto kaina įveskite 1200.</span><span class="sxs-lookup"><span data-stu-id="bdb39-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="bdb39-138">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="bdb39-138">Click Add line.</span></span>
10. <span data-ttu-id="bdb39-139">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bdb39-140">Sąraše raskite diegimo išlaidų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="bdb39-141">Pavyzdžiui, S0001</span><span class="sxs-lookup"><span data-stu-id="bdb39-141">For example, S0001</span></span>
12. <span data-ttu-id="bdb39-142">Pasirinkite diegimo išlaidų prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="bdb39-143">Atkreipkite dėmesį, kad nuo jūsų pakeitimų negretinta.</span><span class="sxs-lookup"><span data-stu-id="bdb39-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="bdb39-144">Spustelėkite Naujinti gretinimo būseną.</span><span class="sxs-lookup"><span data-stu-id="bdb39-144">Click Update match status.</span></span>
14. <span data-ttu-id="bdb39-145">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="bdb39-146">Spustelėkite Gretinimo informacija.</span><span class="sxs-lookup"><span data-stu-id="bdb39-146">Click Matching details.</span></span>
    * <span data-ttu-id="bdb39-147">Naujos eilutės su paslaugomis gretinti nereikia, todėl būsena yra „Neatlikta‟.</span><span class="sxs-lookup"><span data-stu-id="bdb39-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="bdb39-148">Pasirinkite atsargų prekės, kurią gavote, produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="bdb39-149">Eilutė, kurioje yra produkto gavimo kvitas, buvo sugretinta, tačiau neatitinka kiekis arba kaina, todėl sugretinti nepavyko.</span><span class="sxs-lookup"><span data-stu-id="bdb39-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="bdb39-150">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bdb39-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="bdb39-151">Dabar, kai vieneto kaina atitinka, būsena atnaujinama į Pavyko.</span><span class="sxs-lookup"><span data-stu-id="bdb39-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="bdb39-152">Jei jūsų strategija leidžia nesutapimus arba jei gretinimas yra tik įspėjimas, SF vis tiek galite registruoti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="bdb39-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bdb39-153">Close the page.</span></span>
19. <span data-ttu-id="bdb39-154">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="bdb39-154">Click Post.</span></span>
20. <span data-ttu-id="bdb39-155">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="bdb39-155">Close the form.</span></span>
    * <span data-ttu-id="bdb39-156">Atkreipkite dėmesį, kad pirkimo užsakymas pateikiamas nebe kaip gautas, o kaip užsakymas, kuriam neišrašyta SF.</span><span class="sxs-lookup"><span data-stu-id="bdb39-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


