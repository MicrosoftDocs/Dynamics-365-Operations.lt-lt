---
title: " Kurti pirkimo užsakymų produktų pakuotes"
description: Ši procedūra padės sukurti produktų paketą ir jį naudoti pirkimo užsakyme.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e1fd19c6a27739ce9f57a4ab33f61e6baaeb2e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023412"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="03358-103"> Kurti pirkimo užsakymų produktų pakuotes</span><span class="sxs-lookup"><span data-stu-id="03358-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="03358-104">Ši procedūra padės sukurti produktų paketą ir jį naudoti pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="03358-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="03358-105">Pirkimo užsakymas bus naudojamas iš anksto nustatytų produktų rinkinio užsakymui kurti.</span><span class="sxs-lookup"><span data-stu-id="03358-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="03358-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="03358-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="03358-107">Produktų pakuotės kūrimas</span><span class="sxs-lookup"><span data-stu-id="03358-107">Create a product package</span></span>
1. <span data-ttu-id="03358-108">Eikite į Mažmeninė prekyba ir prekyba > Atsargų valdymas > Papildymas > Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="03358-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="03358-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="03358-109">Click New.</span></span>
3. <span data-ttu-id="03358-110">Lauke Pakuotės numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03358-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="03358-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03358-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="03358-112">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="03358-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03358-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="03358-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="03358-114">Click Add.</span></span>
8. <span data-ttu-id="03358-115">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="03358-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="03358-116">Lauke Dydis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="03358-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03358-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="03358-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="03358-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="03358-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="03358-119">Click Add.</span></span>
13. <span data-ttu-id="03358-120">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="03358-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="03358-121">Lauke Varianto numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="03358-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03358-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="03358-123">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="03358-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="03358-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="03358-124">Click Add.</span></span>
18. <span data-ttu-id="03358-125">Lauke Prekės numeris įveskite „0175“.</span><span class="sxs-lookup"><span data-stu-id="03358-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="03358-126">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="03358-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="03358-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03358-127">Click Save.</span></span>
21. <span data-ttu-id="03358-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="03358-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="03358-129">Pakuotės įtraukimas į pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="03358-129">Add package to purchase order</span></span>
1. <span data-ttu-id="03358-130">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="03358-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="03358-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="03358-131">Click New.</span></span>
3. <span data-ttu-id="03358-132">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="03358-133">Sąraše pasirinkite to patį tiekėją, kurio produktų pakuotė anksčiau buvo sukurta, jei tiekėjas buvo pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="03358-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="03358-134">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="03358-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="03358-135">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="03358-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03358-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="03358-137">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="03358-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="03358-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03358-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="03358-139">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="03358-139">Click OK.</span></span>
11. <span data-ttu-id="03358-140">Perjunkite dalies Išsami eilučių informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="03358-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="03358-141">Spustelėkite skirtuką Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="03358-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="03358-142">Spustelėkite Pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="03358-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="03358-143">Spustelėkite Kurti pakuotės eilutes.</span><span class="sxs-lookup"><span data-stu-id="03358-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="03358-144">Sąraše raskite ir pasirinkite produktų pakuotę, sukurtą ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="03358-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="03358-145">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="03358-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="03358-146">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="03358-146">Click Create.</span></span>
18. <span data-ttu-id="03358-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03358-147">Click Save.</span></span>
