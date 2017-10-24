--- 
title: " Kurti pirkimo užsakymų produktų pakuotes"
description: "Ši procedūra padės sukurti produktų paketą ir jį naudoti pirkimo užsakyme."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="fffeb-103"> Kurti pirkimo užsakymų produktų pakuotes</span><span class="sxs-lookup"><span data-stu-id="fffeb-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="fffeb-104">Ši procedūra padės sukurti produktų paketą ir jį naudoti pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="fffeb-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="fffeb-105">Pirkimo užsakymas bus naudojamas iš anksto nustatytų produktų rinkinio užsakymui kurti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="fffeb-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="fffeb-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="fffeb-107">Produktų pakuotės kūrimas</span><span class="sxs-lookup"><span data-stu-id="fffeb-107">Create a product package</span></span>
1. <span data-ttu-id="fffeb-108">Pasirinkite Mažmeninė prekyba ir prekyba > Atsargų valdymas > Papildymas > Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="fffeb-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="fffeb-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fffeb-109">Click New.</span></span>
3. <span data-ttu-id="fffeb-110">Lauke Pakuotės numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fffeb-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="fffeb-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fffeb-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fffeb-112">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fffeb-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fffeb-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="fffeb-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-114">Click Add.</span></span>
8. <span data-ttu-id="fffeb-115">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="fffeb-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="fffeb-116">Lauke Dydis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fffeb-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fffeb-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="fffeb-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fffeb-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="fffeb-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-119">Click Add.</span></span>
13. <span data-ttu-id="fffeb-120">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="fffeb-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="fffeb-121">Lauke Varianto numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="fffeb-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fffeb-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="fffeb-123">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fffeb-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fffeb-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-124">Click Add.</span></span>
18. <span data-ttu-id="fffeb-125">Lauke Prekės numeris įveskite „0175“.</span><span class="sxs-lookup"><span data-stu-id="fffeb-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="fffeb-126">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fffeb-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="fffeb-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-127">Click Save.</span></span>
21. <span data-ttu-id="fffeb-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fffeb-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="fffeb-129">Pakuotės įtraukimas į pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="fffeb-129">Add package to puchase order</span></span>
1. <span data-ttu-id="fffeb-130">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="fffeb-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="fffeb-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fffeb-131">Click New.</span></span>
3. <span data-ttu-id="fffeb-132">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fffeb-133">Sąraše pasirinkite to patį tiekėją, kurio produktų pakuotė anksčiau buvo sukurta, jei tiekėjas buvo pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="fffeb-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="fffeb-134">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="fffeb-135">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fffeb-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fffeb-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fffeb-137">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="fffeb-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fffeb-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="fffeb-139">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="fffeb-139">Click OK.</span></span>
11. <span data-ttu-id="fffeb-140">Perjunkite dalies Išsami eilučių informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="fffeb-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="fffeb-141">Spustelėkite skirtuką Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="fffeb-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="fffeb-142">Spustelėkite Pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="fffeb-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="fffeb-143">Spustelėkite Kurti pakuotės eilutes.</span><span class="sxs-lookup"><span data-stu-id="fffeb-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="fffeb-144">Sąraše raskite ir pasirinkite produktų pakuotę, sukurtą ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="fffeb-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="fffeb-145">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fffeb-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fffeb-146">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-146">Click Create.</span></span>
18. <span data-ttu-id="fffeb-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fffeb-147">Click Save.</span></span>


