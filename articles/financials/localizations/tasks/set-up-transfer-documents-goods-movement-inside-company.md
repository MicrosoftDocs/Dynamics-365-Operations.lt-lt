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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f10f627f33108b8750a1d71d24a99763178e2ef
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="49468-103">Prekių perkėlimo įmonės viduje perkėlimo dokumentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="49468-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49468-104">Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="49468-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="49468-105">Šią procedūrą gali atlikti tik juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="49468-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="49468-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="49468-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="49468-107">Prieš atlikdami šią procedūrą, turite atlikti procedūrą „Prekių perkėlimo įmonės viduje perdavimo dokumentų nustatymas“.</span><span class="sxs-lookup"><span data-stu-id="49468-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="49468-108">Ši procedūra skirta atsargų buhalteriams.</span><span class="sxs-lookup"><span data-stu-id="49468-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="49468-109">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="49468-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="49468-110">Perdavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="49468-110">Create a transfer order</span></span>
1. <span data-ttu-id="49468-111">Pasirinkite Atsargų valdymas > Gaunami užsakymai > Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="49468-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="49468-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="49468-112">Click New.</span></span>
3. <span data-ttu-id="49468-113">Lauke Iš sandėlio įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="49468-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="49468-114">Lauke Į sandėlį įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="49468-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="49468-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="49468-115">Click Add.</span></span>
6. <span data-ttu-id="49468-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="49468-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="49468-117">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="49468-118">Perkėlimo užsakymo transportavimo informacijos įvedimas</span><span class="sxs-lookup"><span data-stu-id="49468-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="49468-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="49468-119">Click Save.</span></span>
2. <span data-ttu-id="49468-120">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="49468-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="49468-121">Spustelėkite Transportavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="49468-121">Click Transportation details.</span></span>
4. <span data-ttu-id="49468-122">Lauke Spausdinti transportavimo informaciją pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="49468-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="49468-123">Lauke Išduotos prekės įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="49468-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="49468-124">Lauke Paketas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="49468-125">Lauke Krovinio pavojingumas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="49468-126">Lauke Vežėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="49468-127">Lauke Modelis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="49468-128">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="49468-129">Lauke Priekabos registracijos numeris įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="49468-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="49468-130">Lauke Vairuotojas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="49468-131">Lauke Vairuotojo vardas ir pavardė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="49468-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="49468-132">Click Save.</span></span>
15. <span data-ttu-id="49468-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="49468-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="49468-134">Neužregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="49468-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="49468-135">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="49468-135">Click Packing slip.</span></span>
2. <span data-ttu-id="49468-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="49468-136">Click OK.</span></span>
3. <span data-ttu-id="49468-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="49468-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="49468-138">Užregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="49468-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="49468-139">Veiksmų srityje spustelėkite Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="49468-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="49468-140">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="49468-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="49468-141">Spustelėkite Siuntimo perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="49468-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="49468-142">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="49468-142">Click the General tab.</span></span>
5. <span data-ttu-id="49468-143">Lauke Naujinti pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="49468-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="49468-144">Spustelėkite skirtuką Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="49468-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="49468-145">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="49468-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="49468-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="49468-146">Click OK.</span></span>
9. <span data-ttu-id="49468-147">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="49468-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="49468-148">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="49468-148">Click Packing slip.</span></span>
11. <span data-ttu-id="49468-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="49468-149">Click OK.</span></span>


