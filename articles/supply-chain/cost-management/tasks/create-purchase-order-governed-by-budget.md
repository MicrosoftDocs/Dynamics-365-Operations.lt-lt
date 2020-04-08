---
title: Kurti pirkimo užsakymus pagal biudžetą
description: Šią procedūrą naudokite norėdami kurti pirkimo užsakymą, kuriam tikrinama, ar pakankamas biudžetas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0054745394d6a21599d8f07605f78ffdd7f575ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150544"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="dec33-103">Kurti pirkimo užsakymus pagal biudžetą</span><span class="sxs-lookup"><span data-stu-id="dec33-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dec33-104">Šią procedūrą naudokite norėdami kurti pirkimo užsakymą, kuriam tikrinama, ar pakankamas biudžetas.</span><span class="sxs-lookup"><span data-stu-id="dec33-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="dec33-105">Šiame įraše naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="dec33-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="dec33-106">Peržiūrėkite biudžeto kontrolės konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="dec33-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="dec33-107">Eikite į Biudžetas > Sąranka > Biudžeto tikrinimas > Biudžeto tikrinimo konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="dec33-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="dec33-108">Spustelėkite skirtuką Prieinami biudžeto fondai.</span><span class="sxs-lookup"><span data-stu-id="dec33-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="dec33-109">Spustelėkite skirtuką Dokumentai ir žurnalai.</span><span class="sxs-lookup"><span data-stu-id="dec33-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="dec33-110">Spustelėkite skirtuką Apibrėžti biudžeto kontrolės taisykles.</span><span class="sxs-lookup"><span data-stu-id="dec33-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="dec33-111">Spustelėkite skirtuką Apibrėžti biudžeto grupes.</span><span class="sxs-lookup"><span data-stu-id="dec33-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="dec33-112">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dec33-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="dec33-113">Pirkimo užsakymo antraštės kūrimas</span><span class="sxs-lookup"><span data-stu-id="dec33-113">Create the purchase order header</span></span>
1. <span data-ttu-id="dec33-114">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="dec33-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="dec33-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dec33-115">Click New.</span></span>
3. <span data-ttu-id="dec33-116">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="dec33-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="dec33-117">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="dec33-117">Expand the General section.</span></span>
5. <span data-ttu-id="dec33-118">Lauke Apskaitos data, nustatykite datą „2016-01-01“.</span><span class="sxs-lookup"><span data-stu-id="dec33-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="dec33-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="dec33-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="dec33-120">Pirkimo užsakymo eilutės įtraukimas</span><span class="sxs-lookup"><span data-stu-id="dec33-120">Add a purchase order line</span></span>
1. <span data-ttu-id="dec33-121">Lauke Įsigijimo kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dec33-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="dec33-122">Kiekį nustatykite „2‟.</span><span class="sxs-lookup"><span data-stu-id="dec33-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="dec33-123">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dec33-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="dec33-124">Nustatykite Vieneto kainą „10000“.</span><span class="sxs-lookup"><span data-stu-id="dec33-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="dec33-125">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="dec33-125">Click Financials.</span></span>
6. <span data-ttu-id="dec33-126">Spustelėkite „Paskirstyti sumas“.</span><span class="sxs-lookup"><span data-stu-id="dec33-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="dec33-127">Lauke DK sąskaita nurodykite reikšmę „601300-001-023--“.</span><span class="sxs-lookup"><span data-stu-id="dec33-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="dec33-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dec33-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="dec33-129">Patikrinti biudžetą</span><span class="sxs-lookup"><span data-stu-id="dec33-129">Perform budget checking</span></span>
1. <span data-ttu-id="dec33-130">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="dec33-130">Click Financials.</span></span>
2. <span data-ttu-id="dec33-131">Spustelėkite Atlikti biudžeto tikrinimą.</span><span class="sxs-lookup"><span data-stu-id="dec33-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="dec33-132">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="dec33-132">Click Financials.</span></span>
4. <span data-ttu-id="dec33-133">Spustelėkite Biudžeto tikrinimo klaidos arba įspėjimai.</span><span class="sxs-lookup"><span data-stu-id="dec33-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="dec33-134">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="dec33-134">Click Close.</span></span>

