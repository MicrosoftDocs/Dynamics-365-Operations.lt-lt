---
title: Taisyti atsargų sekimo informaciją
description: Ši procedūra padės kūrimo ir atsargų perkėlimo žurnalo registravimo proceso metu, kad pakoreguotumėte atsargų sekimo informaciją.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433861"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="01b13-103">Taisyti atsargų sekimo informaciją</span><span class="sxs-lookup"><span data-stu-id="01b13-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01b13-104">Ši procedūra padės kūrimo ir atsargų perkėlimo žurnalo registravimo proceso metu, kad pakoreguotumėte atsargų sekimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="01b13-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="01b13-105">Šiame pavyzdyje atnaujinsime paketo valdomos prekės informaciją, pakeitę neteisingai užregistruotą paketą į kitą paketą.</span><span class="sxs-lookup"><span data-stu-id="01b13-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="01b13-106">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonės USPI arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="01b13-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="01b13-107">Jei naudojate savo duomenis, jums reikia turėti prekę, kurios paketas įgalintas ir jis neturi būti kontroliuojamas pagal vietą.</span><span class="sxs-lookup"><span data-stu-id="01b13-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="01b13-108">Be to, norint atlikti atsargų perkėlimą, turi būti nustatytas atsargų žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="01b13-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="01b13-109">Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="01b13-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="01b13-110">Kurkite atsargų perkėlimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="01b13-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="01b13-111">Eikite į Perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="01b13-111">Go to Transfer.</span></span>
2. <span data-ttu-id="01b13-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="01b13-112">Click New.</span></span>
3. <span data-ttu-id="01b13-113">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01b13-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="01b13-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="01b13-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="01b13-115">Žurnalo eilučių kūrimas</span><span class="sxs-lookup"><span data-stu-id="01b13-115">Create journal lines</span></span>
1. <span data-ttu-id="01b13-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="01b13-116">Click New.</span></span>
2. <span data-ttu-id="01b13-117">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01b13-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="01b13-118">Jei naudojate USPI, pasirinkite M5003.</span><span class="sxs-lookup"><span data-stu-id="01b13-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="01b13-119">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="01b13-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="01b13-120">Spustelėkite skirtuką Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="01b13-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="01b13-121">Lauke Paketo numeris įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="01b13-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="01b13-122">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01b13-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="01b13-123">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="01b13-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="01b13-124">Lauke Paketo numeris įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="01b13-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="01b13-125">Registruoti žurnalą</span><span class="sxs-lookup"><span data-stu-id="01b13-125">Post the journal</span></span>
1. <span data-ttu-id="01b13-126">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="01b13-126">Click Post.</span></span>
2. <span data-ttu-id="01b13-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="01b13-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="01b13-128">Tikrinti sekimo informaciją</span><span class="sxs-lookup"><span data-stu-id="01b13-128">Check tracing information</span></span>
1. <span data-ttu-id="01b13-129">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="01b13-129">Click Inventory.</span></span>
2. <span data-ttu-id="01b13-130">Spustelėkite Sekti.</span><span class="sxs-lookup"><span data-stu-id="01b13-130">Click Trace.</span></span>
3. <span data-ttu-id="01b13-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="01b13-131">Click OK.</span></span>
    * <span data-ttu-id="01b13-132">Naudodami šią sekimo informaciją galite sekti pagal paketą, pagal kurį ištaisėte atsargas.</span><span class="sxs-lookup"><span data-stu-id="01b13-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="01b13-133">Taip pat galite naudoti Prekės sekimo puslapį norėdami pamatyti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="01b13-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="01b13-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="01b13-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="01b13-135">Tikrinti atsargų operacijas</span><span class="sxs-lookup"><span data-stu-id="01b13-135">Check inventory transactions</span></span>
1. <span data-ttu-id="01b13-136">Spustelėkite Atsargos.</span><span class="sxs-lookup"><span data-stu-id="01b13-136">Click Inventory.</span></span>
2. <span data-ttu-id="01b13-137">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="01b13-137">Click Transactions.</span></span>
    * <span data-ttu-id="01b13-138">Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="01b13-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

