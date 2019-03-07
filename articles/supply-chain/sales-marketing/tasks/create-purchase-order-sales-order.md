---
title: Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą
description: Ši procedūra nurodo, kaip kurti pirkimo užsakymą, pagrįstą pardavimo užsakymu.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "325761"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="5be21-103">Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="5be21-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5be21-104">Ši procedūra nurodo, kaip kurti pirkimo užsakymą, pagrįstą pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="5be21-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="5be21-105">Produkto pirkimo užsakymo kiekiai tada nurodomi norint patenkinti pradinio pardavimo užsakymo poreikį.</span><span class="sxs-lookup"><span data-stu-id="5be21-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="5be21-106">Pardavimo poreikio vykdymas tokiu būdu yra išsamesnio ir optimizuoto metodo Platinimo poreikio planavimas alternatyva.</span><span class="sxs-lookup"><span data-stu-id="5be21-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="5be21-107">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="5be21-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="5be21-108">Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="5be21-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="5be21-109">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="5be21-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="5be21-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5be21-110">Click New.</span></span>
3. <span data-ttu-id="5be21-111">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5be21-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5be21-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5be21-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5be21-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="5be21-113">Click OK.</span></span>
6. <span data-ttu-id="5be21-114">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5be21-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5be21-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5be21-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5be21-116">Jei naudojate USMF, galite pasirinkti D0001.</span><span class="sxs-lookup"><span data-stu-id="5be21-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="5be21-117">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5be21-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="5be21-118">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="5be21-118">Click Add line.</span></span>
10. <span data-ttu-id="5be21-119">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5be21-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5be21-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5be21-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5be21-121">Jei naudojate USMF, galite pasirinkti T0020.</span><span class="sxs-lookup"><span data-stu-id="5be21-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="5be21-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5be21-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5be21-123">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5be21-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="5be21-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5be21-124">Click Save.</span></span>
15. <span data-ttu-id="5be21-125">Veiksmų srityje spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="5be21-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="5be21-126">Spustelėkite Pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="5be21-126">Click Purchase order.</span></span>
    * <span data-ttu-id="5be21-127">Puslapyje Kurti pirkimo pristatymą pateikiamos visos atvirų pardavimo užsakymų eilutės, kurios buvo nukopijuotos iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="5be21-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="5be21-128">Galite peržiūrėti užsakymo informaciją ir, jei reikia, galite modifikuoti pasirinktą informaciją, pvz., pirkimo kiekį ir kainų nustatymo sąlygas, prieš kurdami pirkimus.</span><span class="sxs-lookup"><span data-stu-id="5be21-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="5be21-129">Pasirinkite pasirinktį Įtraukti viską.</span><span class="sxs-lookup"><span data-stu-id="5be21-129">Select the Include all option.</span></span>
    * <span data-ttu-id="5be21-130">Jei pirkimo užsakymą norite sugeneruoti tik pardavimo užsakymo eilučių pogrupiui, pažymėkite jas atskirai.</span><span class="sxs-lookup"><span data-stu-id="5be21-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="5be21-131">Lauke Tiekėjo sąskaita gali būti įvestas arba dar nebūti įvestas tiekėjo numeris.</span><span class="sxs-lookup"><span data-stu-id="5be21-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="5be21-132">Jei yra nustatytas produkto numatytasis tiekėjas (susietame Prekės padengime), šis tiekėjas bus nukopijuotas į eilutę.</span><span class="sxs-lookup"><span data-stu-id="5be21-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="5be21-133">Priešingu atveju, tiekėją turite įvesti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="5be21-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="5be21-134">Šiame vadove, nepriklausomai nuo to, ar Tiekėjo sąskaitos lauke jau yra vertė ar ne, tolesni veiksmai nurodo, kaip pasirinkti naują tiekėją, kuris skiriasi kiekvienoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5be21-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="5be21-135">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5be21-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="5be21-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5be21-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="5be21-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5be21-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="5be21-138">Pasirinkite antrąją užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="5be21-138">Select the second order line.</span></span>
22. <span data-ttu-id="5be21-139">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5be21-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="5be21-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5be21-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="5be21-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5be21-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="5be21-142">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="5be21-142">Click Validate.</span></span>
26. <span data-ttu-id="5be21-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5be21-143">Click OK.</span></span>
    * <span data-ttu-id="5be21-144">Pranešimas informuoja, kad sukurtas vienas ar daugiau pirkimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="5be21-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="5be21-145">Kiekvienam tiekėjui, kurį nurodėte pardavimo užsakymo eilutėse, sistema sukuria po atskirą pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5be21-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="5be21-146">Tai reiškia, kad jei tas pats tiekėjas nurodytas keliose pardavimo užsakymo eilutėse, bus sugeneruotas vienas pirkimo užsakymą su keliomis eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="5be21-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="5be21-147">Peržiūrėti pirkimo užsakymus, sukurtus pagal pardavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="5be21-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="5be21-148">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="5be21-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="5be21-149">Spustelėkite Susiję užsakymai.</span><span class="sxs-lookup"><span data-stu-id="5be21-149">Click Related orders.</span></span>
    * <span data-ttu-id="5be21-150">Puslapyje Susiję užsakymai pateikiami visi užsakymai, sukurti iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="5be21-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="5be21-151">Šiame pavyzdyje yra du pirkimo užsakymai, sugeneruoti atitinkamai dviem skirtingiems tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="5be21-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="5be21-152">Spustelėkite, jei norite atidaryti lauke Pirkimo užsakymas esantį saitą.</span><span class="sxs-lookup"><span data-stu-id="5be21-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="5be21-153">Kiekviena pirkimo užsakymo eilutė susieta su pardavimo užsakymo eilute, dėl kurios buvo sukurtas pirkimas.</span><span class="sxs-lookup"><span data-stu-id="5be21-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="5be21-154">Ryšys su pardavimo užsakymu nurodytas skirtuke Produktas, esančiame Eilutės informacijos „FastTab“, laukuose Nuorodos tipas, Nuorodos numeris ir Nuoroda į partiją.</span><span class="sxs-lookup"><span data-stu-id="5be21-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="5be21-155">Išplėskite arba sutraukite dalį Išsami eilučių informacija.</span><span class="sxs-lookup"><span data-stu-id="5be21-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="5be21-156">Spustelėkite skirtuką Produktas.</span><span class="sxs-lookup"><span data-stu-id="5be21-156">Click the Product tab.</span></span>
    * <span data-ttu-id="5be21-157">Nuoroda į partiją užtikrina, kad esamo pirkimo išlaidos bus įtrauktos į pridėtą pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5be21-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="5be21-158">Atidarę saitą lauke Nuorodos numeris, galite pereiti į pradinį pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5be21-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

