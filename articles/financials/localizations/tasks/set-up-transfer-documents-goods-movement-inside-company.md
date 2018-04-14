--- 
title: "Prekių perkėlimo įmonės viduje perkėlimo dokumentų nustatymas"
description: "Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f6698654dab6876e4c22c489eba65ebeb270ccef
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="af352-103">Prekių perkėlimo įmonės viduje perkėlimo dokumentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="af352-103">Set up the transfer documents for goods movement inside a company</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af352-104">Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="af352-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="af352-105">Šią procedūrą gali atlikti tik juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="af352-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="af352-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="af352-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="af352-107">Prieš atlikdami šią procedūrą, turite atlikti procedūrą „Prekių perkėlimo įmonės viduje perdavimo dokumentų nustatymas“.</span><span class="sxs-lookup"><span data-stu-id="af352-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="af352-108">Ši procedūra skirta atsargų buhalteriams.</span><span class="sxs-lookup"><span data-stu-id="af352-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="af352-109">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="af352-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="af352-110">Perdavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="af352-110">Create a transfer order</span></span>
1. <span data-ttu-id="af352-111">Pasirinkite Atsargų valdymas > Gaunami užsakymai > Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="af352-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="af352-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="af352-112">Click New.</span></span>
3. <span data-ttu-id="af352-113">Lauke Iš sandėlio įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="af352-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="af352-114">Lauke Į sandėlį įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="af352-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="af352-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="af352-115">Click Add.</span></span>
6. <span data-ttu-id="af352-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="af352-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="af352-117">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="af352-118">Perkėlimo užsakymo transportavimo informacijos įvedimas</span><span class="sxs-lookup"><span data-stu-id="af352-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="af352-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="af352-119">Click Save.</span></span>
2. <span data-ttu-id="af352-120">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="af352-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="af352-121">Spustelėkite Transportavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="af352-121">Click Transportation details.</span></span>
4. <span data-ttu-id="af352-122">Lauke Spausdinti transportavimo informaciją pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="af352-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="af352-123">Lauke Išduotos prekės įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="af352-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="af352-124">Lauke Paketas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="af352-125">Lauke Krovinio pavojingumas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="af352-126">Lauke Vežėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="af352-127">Lauke Modelis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="af352-128">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="af352-129">Lauke Priekabos registracijos numeris įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="af352-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="af352-130">Lauke Vairuotojas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="af352-131">Lauke Vairuotojo vardas ir pavardė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="af352-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="af352-132">Click Save.</span></span>
15. <span data-ttu-id="af352-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="af352-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="af352-134">Neužregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="af352-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="af352-135">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="af352-135">Click Packing slip.</span></span>
2. <span data-ttu-id="af352-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af352-136">Click OK.</span></span>
3. <span data-ttu-id="af352-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="af352-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="af352-138">Užregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="af352-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="af352-139">Veiksmų srityje spustelėkite Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="af352-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="af352-140">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="af352-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="af352-141">Spustelėkite Siuntimo perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="af352-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="af352-142">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="af352-142">Click the General tab.</span></span>
5. <span data-ttu-id="af352-143">Lauke Naujinti pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="af352-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="af352-144">Spustelėkite skirtuką Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="af352-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="af352-145">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af352-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="af352-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af352-146">Click OK.</span></span>
9. <span data-ttu-id="af352-147">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="af352-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="af352-148">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="af352-148">Click Packing slip.</span></span>
11. <span data-ttu-id="af352-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="af352-149">Click OK.</span></span>


