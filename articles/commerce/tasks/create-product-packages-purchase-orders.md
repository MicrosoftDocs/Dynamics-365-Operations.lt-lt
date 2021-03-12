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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964675"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="02c5d-103"> Kurti pirkimo užsakymų produktų pakuotes</span><span class="sxs-lookup"><span data-stu-id="02c5d-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02c5d-104">Ši procedūra padės sukurti produktų paketą ir jį naudoti pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="02c5d-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="02c5d-105">Pirkimo užsakymas bus naudojamas iš anksto nustatytų produktų rinkinio užsakymui kurti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="02c5d-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="02c5d-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="02c5d-107">Produktų pakuotės kūrimas</span><span class="sxs-lookup"><span data-stu-id="02c5d-107">Create a product package</span></span>
1. <span data-ttu-id="02c5d-108">Eikite į Mažmeninė prekyba ir prekyba > Atsargų valdymas > Papildymas > Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="02c5d-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="02c5d-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="02c5d-109">Click New.</span></span>
3. <span data-ttu-id="02c5d-110">Lauke Pakuotės numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02c5d-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="02c5d-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="02c5d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="02c5d-112">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="02c5d-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="02c5d-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="02c5d-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-114">Click Add.</span></span>
8. <span data-ttu-id="02c5d-115">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="02c5d-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="02c5d-116">Lauke Dydis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="02c5d-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="02c5d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="02c5d-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="02c5d-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="02c5d-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-119">Click Add.</span></span>
13. <span data-ttu-id="02c5d-120">Lauke Prekės numeris įveskite „0160“.</span><span class="sxs-lookup"><span data-stu-id="02c5d-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="02c5d-121">Lauke Varianto numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="02c5d-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="02c5d-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="02c5d-123">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="02c5d-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="02c5d-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-124">Click Add.</span></span>
18. <span data-ttu-id="02c5d-125">Lauke Prekės numeris įveskite „0175“.</span><span class="sxs-lookup"><span data-stu-id="02c5d-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="02c5d-126">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="02c5d-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="02c5d-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-127">Click Save.</span></span>
21. <span data-ttu-id="02c5d-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="02c5d-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="02c5d-129">Pakuotės įtraukimas į pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="02c5d-129">Add package to purchase order</span></span>
1. <span data-ttu-id="02c5d-130">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="02c5d-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="02c5d-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="02c5d-131">Click New.</span></span>
3. <span data-ttu-id="02c5d-132">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="02c5d-133">Sąraše pasirinkite to patį tiekėją, kurio produktų pakuotė anksčiau buvo sukurta, jei tiekėjas buvo pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="02c5d-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="02c5d-134">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="02c5d-135">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="02c5d-136">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="02c5d-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="02c5d-137">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="02c5d-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="02c5d-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="02c5d-139">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="02c5d-139">Click OK.</span></span>
11. <span data-ttu-id="02c5d-140">Perjunkite dalies Išsami eilučių informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="02c5d-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="02c5d-141">Spustelėkite skirtuką Produktų pakuotės.</span><span class="sxs-lookup"><span data-stu-id="02c5d-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="02c5d-142">Spustelėkite Pirkimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="02c5d-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="02c5d-143">Spustelėkite Kurti pakuotės eilutes.</span><span class="sxs-lookup"><span data-stu-id="02c5d-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="02c5d-144">Sąraše raskite ir pasirinkite produktų pakuotę, sukurtą ankstesniame veiksme.</span><span class="sxs-lookup"><span data-stu-id="02c5d-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="02c5d-145">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="02c5d-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="02c5d-146">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-146">Click Create.</span></span>
18. <span data-ttu-id="02c5d-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="02c5d-147">Click Save.</span></span>

