---
title: Kurti bendrąjį produktą
description: Sukurkite iš anksto nustatytų variantų bendrąjį produktą.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb30b46a0e5a6d4fac997588dd47148f2664c03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433591"
---
# <a name="create-a-product-master"></a><span data-ttu-id="470c7-103">Kurti bendrąjį produktą</span><span class="sxs-lookup"><span data-stu-id="470c7-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="470c7-104">Sukurkite iš anksto nustatytų variantų bendrąjį produktą.</span><span class="sxs-lookup"><span data-stu-id="470c7-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="470c7-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="470c7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="470c7-106">Ši procedūra yra skirta produkto kūrėjui.</span><span class="sxs-lookup"><span data-stu-id="470c7-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="470c7-107">Naujo bendrojo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="470c7-107">Create a new product master</span></span>
1. <span data-ttu-id="470c7-108">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="470c7-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="470c7-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="470c7-109">Click **New**.</span></span>
3. <span data-ttu-id="470c7-110">Lauke **Produkto numeris** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="470c7-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="470c7-111">Numeris turi būti unikalus.</span><span class="sxs-lookup"><span data-stu-id="470c7-111">The number must be unique.</span></span> <span data-ttu-id="470c7-112">Lauke **Produkto numeris** galima nustatyti numerių seką.</span><span class="sxs-lookup"><span data-stu-id="470c7-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="470c7-113">Tokiu atveju vartotojui nereikia įvesti reikšmės.</span><span class="sxs-lookup"><span data-stu-id="470c7-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="470c7-114">Lauke **Produkto pavadinimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="470c7-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="470c7-115">Įveskite aprašomąjį produkto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="470c7-115">Enter a descriptive product name.</span></span> <span data-ttu-id="470c7-116">Numatytoji reikšmė yra paieškos pavadinimas, tačiau vartotojas ją gali pakeisti.</span><span class="sxs-lookup"><span data-stu-id="470c7-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="470c7-117">Lauke **Produkto dimensijos grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="470c7-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="470c7-118">Produkto dimensijų grupė nulemia, kurią iš 4 produkto dimensijų galima naudoti kuriant produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="470c7-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="470c7-119">Šiame pavyzdyje nurodyta grupė su spalva ir dydžiu.</span><span class="sxs-lookup"><span data-stu-id="470c7-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="470c7-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="470c7-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="470c7-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="470c7-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="470c7-122">Numatytoji **konfigūracijos technologija** yra iš anksto nustatytas variantas.</span><span class="sxs-lookup"><span data-stu-id="470c7-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="470c7-123">Jis bus naudojamas šiame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="470c7-123">This will be used for this example.</span></span>
8. <span data-ttu-id="470c7-124">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="470c7-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="470c7-125">Pasirinkti produkto dimensijų grupes</span><span class="sxs-lookup"><span data-stu-id="470c7-125">Select product dimension groups</span></span>
1. <span data-ttu-id="470c7-126">Lauke **Spalvų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="470c7-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="470c7-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="470c7-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="470c7-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="470c7-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="470c7-129">Lauke **Dydžių grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="470c7-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="470c7-130">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="470c7-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="470c7-131">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="470c7-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="470c7-132">Dimensijų grupių įtraukimas</span><span class="sxs-lookup"><span data-stu-id="470c7-132">Add dimension groups</span></span>
1. <span data-ttu-id="470c7-133">Dalyje **Veiksmų sritis** spustelėkite **Produktas**.</span><span class="sxs-lookup"><span data-stu-id="470c7-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="470c7-134">Spustelėdami **Dimensijų grupės** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="470c7-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="470c7-135">Lauke **Saugojimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="470c7-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="470c7-136">Sandėliavimo dimensijos padeda kontroliuoti, kaip prekės saugomos ir paimamos iš atsargų.</span><span class="sxs-lookup"><span data-stu-id="470c7-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="470c7-137">Pavyzdžiui, saugojimo dimensija gali būti Teritorija ir Sandėlis.</span><span class="sxs-lookup"><span data-stu-id="470c7-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="470c7-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="470c7-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="470c7-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="470c7-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="470c7-140">Lauke **Sekimo dimensijų grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="470c7-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="470c7-141">Sekimo dimensijų grupė nustato, kurias sekimo dimensijas galite pridėti prie produkto.</span><span class="sxs-lookup"><span data-stu-id="470c7-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="470c7-142">Pvz., paketo numeris ir serijos numeris yra naudojami atsargų prekėms sekti.</span><span class="sxs-lookup"><span data-stu-id="470c7-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="470c7-143">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="470c7-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="470c7-144">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="470c7-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="470c7-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="470c7-145">Click **OK**.</span></span>
10. <span data-ttu-id="470c7-146">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="470c7-146">Click **Save**.</span></span>
11. <span data-ttu-id="470c7-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="470c7-147">Close the page.</span></span>

