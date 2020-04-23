---
title: Perkelti faktines atsargas sandėlyje
description: Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cdb66620d5d57a42ce6a2dc443a9276a2e3ca0ae
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203991"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="3cfc2-103">Perkelti faktines atsargas sandėlyje</span><span class="sxs-lookup"><span data-stu-id="3cfc2-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cfc2-104">Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="3cfc2-105">Prieš pradedant atsargų perkėlimus, atsargų žurnalo pavadinimas turi būti nustatytas.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="3cfc2-106">Galite peržiūrėti šią procedūrą demonstracinių duomenų įmonės USMF naudodami rodomas pavyzdžio vertes, arba galite naudoti savo duomenis, esate nustatę produktus ir vietas.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="3cfc2-107">Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="3cfc2-108">Kurkite atsargų perkėlimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="3cfc2-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="3cfc2-109">**Naršymo srityje** eikite į **Atsargų valdymas > Žurnalo įrašai > Prekės > Perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="3cfc2-110">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-110">Click **New**.</span></span>
3. <span data-ttu-id="3cfc2-111">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="3cfc2-112">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-112">Click **OK**.</span></span> <span data-ttu-id="3cfc2-113">Yra galimybė kiekvienai žurnalo eilutei nurodyti dimensijas 'Nuo' ir 'Iki'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="3cfc2-114">Tai būtina šiam žurnalo tipui.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-114">These are essential for this journal type.</span></span> <span data-ttu-id="3cfc2-115">Galite perkelti elementus į vietas naudodami skirtingas taisykles.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="3cfc2-116">Šiame pavyzdyje perkelsime prekę į tą patį sandėlį iš numerio lentelės kontroliuojamos vietos į vietą, kurios nekontroliuoja numerio lentelė.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="3cfc2-117">Kurti žurnalo eilutes</span><span class="sxs-lookup"><span data-stu-id="3cfc2-117">Create journal lines</span></span>
1. <span data-ttu-id="3cfc2-118">„FastTab“ **Žurnalo eilutės** spustelėkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="3cfc2-119">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-120">Jei naudojate USMF, galite pasirinkti 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="3cfc2-121">Lauke **Vieta iš** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-122">Jei naudojate USMF, galite pasirinkti '2'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="3cfc2-123">Lauke **Vieta į** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-124">Jei naudojate USMF, galite pasirinkti '2'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="3cfc2-125">Lauke **Iš sandėlio** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-126">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="3cfc2-127">Lauke **Į sandėlį** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-128">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="3cfc2-129">Lauke **Iš vietos** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-130">Jei naudojate USMF, galite pasirinkti 'FL-001'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="3cfc2-131">Lauke **Į vietą** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-132">Jei naudojate USMF, galite pasirinkti 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="3cfc2-133">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="3cfc2-134">„fastTab“ **Eilutės informacija** spustelėkite skirtuką **Atsargų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="3cfc2-135">Lauko **Numerio lentelė** skiltyje **Iš atsargų dimensijų** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="3cfc2-136">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="3cfc2-137">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="3cfc2-138">Registruokite atsargų perkėlimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="3cfc2-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="3cfc2-139">**Veiksmų sritis** spustelėkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="3cfc2-140">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="3cfc2-141">Peržiūrėti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="3cfc2-141">View inventory transactions</span></span>
1. <span data-ttu-id="3cfc2-142">Spustelėkite **Atsargos**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="3cfc2-143">Spustelėkite **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-143">Click **Transactions**.</span></span> <span data-ttu-id="3cfc2-144">Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="3cfc2-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

