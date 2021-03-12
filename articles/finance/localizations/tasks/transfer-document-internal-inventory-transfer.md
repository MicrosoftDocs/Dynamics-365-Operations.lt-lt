---
title: Atsargų perkėlimo įmonės viduje perkėlimo dokumentų generavimas
description: Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ebc070f591b03256b6a9043e88967581394fe07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982074"
---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a><span data-ttu-id="c386c-103">Atsargų perkėlimo įmonės viduje perkėlimo dokumentų generavimas</span><span class="sxs-lookup"><span data-stu-id="c386c-103">Generate a transfer document for an internal inventory transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c386c-104">Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c386c-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="c386c-105">Šią procedūrą gali atlikti tik juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="c386c-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="c386c-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje.</span><span class="sxs-lookup"><span data-stu-id="c386c-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="c386c-107">Prieš baigdami šią procedūrą, turite atlikti procedūrą „Nustatyti prekių perkėlimo dokumentus įmonės viduje“.</span><span class="sxs-lookup"><span data-stu-id="c386c-107">Before you can complete this procedure, you must complete the "Set up transfer documents for goods movement inside a company" procedure.</span></span> <span data-ttu-id="c386c-108">Ši procedūra skirta atsargų buhalteriams.</span><span class="sxs-lookup"><span data-stu-id="c386c-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="c386c-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="c386c-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="c386c-110">Perdavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="c386c-110">Create a transfer order</span></span>
1. <span data-ttu-id="c386c-111">Pasirinkite Atsargų valdymas > Gaunami užsakymai > Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c386c-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="c386c-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c386c-112">Click New.</span></span>
3. <span data-ttu-id="c386c-113">Lauke Iš sandėlio įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c386c-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="c386c-114">Lauke Į sandėlį įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c386c-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="c386c-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="c386c-115">Click Add.</span></span>
6. <span data-ttu-id="c386c-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c386c-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c386c-117">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="c386c-118">Perkėlimo užsakymo transportavimo informacijos įvedimas</span><span class="sxs-lookup"><span data-stu-id="c386c-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="c386c-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c386c-119">Click Save.</span></span>
2. <span data-ttu-id="c386c-120">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="c386c-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c386c-121">Spustelėkite Transportavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="c386c-121">Click Transportation details.</span></span>
4. <span data-ttu-id="c386c-122">Lauke Spausdinti transportavimo informaciją pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c386c-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="c386c-123">Lauke Išduotos prekės įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c386c-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="c386c-124">Lauke Paketas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="c386c-125">Lauke Krovinio pavojingumas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="c386c-126">Lauke Vežėjas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="c386c-127">Lauke Modelis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="c386c-128">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="c386c-129">Lauke Priekabos registracijos numeris įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="c386c-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="c386c-130">Lauke Vairuotojas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="c386c-131">Lauke Vairuotojo vardas ir pavardė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="c386c-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c386c-132">Click Save.</span></span>
15. <span data-ttu-id="c386c-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c386c-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="c386c-134">Neužregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="c386c-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="c386c-135">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="c386c-135">Click Packing slip.</span></span>
2. <span data-ttu-id="c386c-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c386c-136">Click OK.</span></span>
3. <span data-ttu-id="c386c-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c386c-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="c386c-138">Užregistruoto perkėlimo užsakymo važtaraščio peržiūra</span><span class="sxs-lookup"><span data-stu-id="c386c-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="c386c-139">Veiksmų srityje spustelėkite Perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c386c-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="c386c-140">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="c386c-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="c386c-141">Spustelėkite Siuntimo perkėlimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c386c-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="c386c-142">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="c386c-142">Click the General tab.</span></span>
5. <span data-ttu-id="c386c-143">Lauke Naujinti pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c386c-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="c386c-144">Spustelėkite skirtuką Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="c386c-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="c386c-145">Lauke Važtaraštis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c386c-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="c386c-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c386c-146">Click OK.</span></span>
9. <span data-ttu-id="c386c-147">Veiksmų srityje spustelėkite Siųsti.</span><span class="sxs-lookup"><span data-stu-id="c386c-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="c386c-148">Spustelėkite Važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="c386c-148">Click Packing slip.</span></span>
11. <span data-ttu-id="c386c-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c386c-149">Click OK.</span></span>

