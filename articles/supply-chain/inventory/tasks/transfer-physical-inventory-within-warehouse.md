---
title: Perkelti faktines atsargas sandėlyje
description: Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b3e91be8aeab10188b6d3925d44a9ec1106406
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "367299"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="f0e73-103">Perkelti faktines atsargas sandėlyje</span><span class="sxs-lookup"><span data-stu-id="f0e73-103">Transfer physical inventory within the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0e73-104">Ši procedūra jums padės kurti ir registruoti atsargų perkėlimo žurnalą, norint registruoti prekės judėjimą iš vienos sandėlio vietos į kitą.</span><span class="sxs-lookup"><span data-stu-id="f0e73-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="f0e73-105">Prieš pradedant atsargų perkėlimus, atsargų žurnalo pavadinimas turi būti nustatytas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="f0e73-106">Galite peržiūrėti šią procedūrą demonstracinių duomenų įmonės USMF naudodami rodomas pavyzdžio vertes, arba galite naudoti savo duomenis, esate nustatę produktus ir vietas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="f0e73-107">Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="f0e73-108">Kurkite atsargų perkėlimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="f0e73-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="f0e73-109">Eikite į Perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-109">Go to Transfer.</span></span>
2. <span data-ttu-id="f0e73-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-110">Click New.</span></span>
3. <span data-ttu-id="f0e73-111">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="f0e73-112">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f0e73-112">Click OK.</span></span>
    * <span data-ttu-id="f0e73-113">Yra galimybė kiekvienai žurnalo eilutei nurodyti dimensijas 'Nuo' ir 'Iki'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="f0e73-114">Tai būtina šiam žurnalo tipui.</span><span class="sxs-lookup"><span data-stu-id="f0e73-114">These are essential for this journal type.</span></span> <span data-ttu-id="f0e73-115">Galite perkelti elementus į vietas naudodami skirtingas taisykles.</span><span class="sxs-lookup"><span data-stu-id="f0e73-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="f0e73-116">Šiame pavyzdyje perkelsime tame pačiame sandėlyje esantį elementą, iš vietos, kuri yra kontroliuojama pagal numerio lentelę į vietą, nekontroliuojamą pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="f0e73-117">Žurnalo eilučių kūrimas</span><span class="sxs-lookup"><span data-stu-id="f0e73-117">Create journal lines</span></span>
1. <span data-ttu-id="f0e73-118">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f0e73-118">Click New.</span></span>
2. <span data-ttu-id="f0e73-119">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-120">Jei naudojate USMF, galite pasirinkti 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="f0e73-121">Lauke Iš teritorijos įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-122">Jei naudojate USMF, galite pasirinkti '2'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="f0e73-123">Lauke Į teritoriją įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-124">Jei naudojate USMF, galite pasirinkti '2'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="f0e73-125">Lauke Iš sandėlio įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-126">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="f0e73-127">Lauke Į sandėlį įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-128">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="f0e73-129">Lauke Iš vietos įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-130">Jei naudojate USMF, galite pasirinkti 'FL-001'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="f0e73-131">Lauke Į vietą įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-132">Jei naudojate USMF, galite pasirinkti 'BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="f0e73-133">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f0e73-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="f0e73-134">Spustelėkite skirtuką Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="f0e73-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="f0e73-135">Lauke Numerio lentelė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="f0e73-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="f0e73-136">Jei naudojate USMF, galite pasirinkti '24'.</span><span class="sxs-lookup"><span data-stu-id="f0e73-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="f0e73-137">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f0e73-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="f0e73-138">Registruokite atsargų perkėlimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="f0e73-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="f0e73-139">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="f0e73-139">Click Post.</span></span>
2. <span data-ttu-id="f0e73-140">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f0e73-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="f0e73-141">Peržiūrėti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="f0e73-141">View inventory transactions</span></span>
1. <span data-ttu-id="f0e73-142">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="f0e73-142">Click Inventory.</span></span>
2. <span data-ttu-id="f0e73-143">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="f0e73-143">Click Transactions.</span></span>
    * <span data-ttu-id="f0e73-144">Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="f0e73-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

