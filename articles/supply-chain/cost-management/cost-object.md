---
title: Savikainos objektai
description: Šiame straipsnyje pateikiama informacija apie savikainos objektus ir paaiškinama, kaip kaupiamos savikainos ir kiekiai. Savikainos objektas yra objektas, kuriam kaupiamos išlaidos ir kiekiai. Savikainos objekto objektas gali būti produktas arba produkto variantas, pvz., stiliaus ir spalvos variantai.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65a0f72f8d97bda36bacd691d545807c413f8825
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967663"
---
# <a name="cost-objects"></a><span data-ttu-id="35275-105">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="35275-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35275-106">Šiame straipsnyje pateikiama informacija apie savikainos objektus ir paaiškinama, kaip kaupiamos savikainos ir kiekiai.</span><span class="sxs-lookup"><span data-stu-id="35275-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="35275-107">Savikainos objektas yra objektas, kuriam kaupiamos išlaidos ir kiekiai.</span><span class="sxs-lookup"><span data-stu-id="35275-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="35275-108">Savikainos objekto objektas gali būti produktas arba produkto variantas, pvz., stiliaus ir spalvos variantai.</span><span class="sxs-lookup"><span data-stu-id="35275-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="35275-109">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="35275-109">Cost objects</span></span>

<span data-ttu-id="35275-110">**Išlaidų objektų** puslapyje išvardyti visi registruoti produkto išlaidų objektai.</span><span class="sxs-lookup"><span data-stu-id="35275-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="35275-111">Išlaidų objektai apibrėžiami pagal duomenis iš tolesnių šaltinių.</span><span class="sxs-lookup"><span data-stu-id="35275-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="35275-112">Produktas</span><span class="sxs-lookup"><span data-stu-id="35275-112">Product</span></span>
-   <span data-ttu-id="35275-113">Produkto dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-113">Product dimension group</span></span>
-   <span data-ttu-id="35275-114">Saugojimo dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-114">Storage dimension group</span></span>
-   <span data-ttu-id="35275-115">Sekimo dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-115">Tracking dimension group</span></span>

<span data-ttu-id="35275-116">**Pastaba.** Išlaidų objektas atitinka tik **Tiesioginės medžiagos** tipo išlaidų elementą.</span><span class="sxs-lookup"><span data-stu-id="35275-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="35275-117">Išlaidų objektas ir atsargų objektas skiriasi tuo, kad išlaidų objektas apibrėžiamas pagal pasirinktas finansinių atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="35275-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="35275-118">Pavyzdžiui, prekės konfigūracija yra tokia, kokia pateikta toliau.</span><span class="sxs-lookup"><span data-stu-id="35275-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="35275-119">**Teritorija:** fizinės atsargos = taip, finansinės atsargos = taip</span><span class="sxs-lookup"><span data-stu-id="35275-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="35275-120">**Sandėlis:** fizinės atsargos = taip, finansinės atsargos = ne</span><span class="sxs-lookup"><span data-stu-id="35275-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="35275-121">**Paketo Nr.:** fizinės atsargos = taip, finansinės atsargos = ne</span><span class="sxs-lookup"><span data-stu-id="35275-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="35275-122">Toliau pateikiamoje lentelėje parodyta, kas yra išlaidų objektas ir kas yra atsargų objektas.</span><span class="sxs-lookup"><span data-stu-id="35275-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="35275-123">Objekto tipas</span><span class="sxs-lookup"><span data-stu-id="35275-123">Object type</span></span>      | <span data-ttu-id="35275-124">Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="35275-124">Item number</span></span> | <span data-ttu-id="35275-125">Svetainė</span><span class="sxs-lookup"><span data-stu-id="35275-125">Site</span></span> | <span data-ttu-id="35275-126">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="35275-126">Warehouse</span></span> | <span data-ttu-id="35275-127">Paketo nr.</span><span class="sxs-lookup"><span data-stu-id="35275-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="35275-128">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="35275-128">Cost object</span></span>      | <span data-ttu-id="35275-129">x</span><span class="sxs-lookup"><span data-stu-id="35275-129">x</span></span>           | <span data-ttu-id="35275-130">x</span><span class="sxs-lookup"><span data-stu-id="35275-130">x</span></span>    |           |           |
| <span data-ttu-id="35275-131">Atsargų objektas</span><span class="sxs-lookup"><span data-stu-id="35275-131">Inventory object</span></span> | <span data-ttu-id="35275-132">x</span><span class="sxs-lookup"><span data-stu-id="35275-132">x</span></span>           | <span data-ttu-id="35275-133">x</span><span class="sxs-lookup"><span data-stu-id="35275-133">x</span></span>    |  <span data-ttu-id="35275-134">x</span><span class="sxs-lookup"><span data-stu-id="35275-134">x</span></span>        | <span data-ttu-id="35275-135">x</span><span class="sxs-lookup"><span data-stu-id="35275-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="35275-136">Išlaidų ir kiekių kaupimas</span><span class="sxs-lookup"><span data-stu-id="35275-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="35275-137">Reikšmė **Vertės** lauke yra tolesnių reikšmių suma.</span><span class="sxs-lookup"><span data-stu-id="35275-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="35275-138">Fakt. išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="35275-138">Physical cost amount</span></span>
    -   <span data-ttu-id="35275-139">Fin. išlaidų suma</span><span class="sxs-lookup"><span data-stu-id="35275-139">Financial cost amount</span></span>
    -   <span data-ttu-id="35275-140">Koregavimai</span><span class="sxs-lookup"><span data-stu-id="35275-140">Adjustments</span></span>
-   <span data-ttu-id="35275-141">Reikšmė **Kiekio** lauke yra tolesnių reikšmių suma.</span><span class="sxs-lookup"><span data-stu-id="35275-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="35275-142">Gauta</span><span class="sxs-lookup"><span data-stu-id="35275-142">Received</span></span>
    -   <span data-ttu-id="35275-143">Išskaičiuota</span><span class="sxs-lookup"><span data-stu-id="35275-143">Deducted</span></span>
    -   <span data-ttu-id="35275-144">Užregistruotas kiekis</span><span class="sxs-lookup"><span data-stu-id="35275-144">Posted quantity</span></span>
-   <span data-ttu-id="35275-145">**Vidutinės vieneto savikainos** laukas yra apskaičiuotasis laukas.</span><span class="sxs-lookup"><span data-stu-id="35275-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="35275-146">Reikšmė apskaičiuojama **Vertės** reikšmę padalijus iš **Kiekio** reikšmės.</span><span class="sxs-lookup"><span data-stu-id="35275-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="35275-147">**Pastaba.** Ankstesniems skaičiavimams parametras **Įtraukti fizinę vertę** įtakos neturi.</span><span class="sxs-lookup"><span data-stu-id="35275-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="35275-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="35275-148">Additional resources</span></span>
--------

[<span data-ttu-id="35275-149">Produkto dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="35275-150">Saugojimo dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="35275-151">Sekimo dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="35275-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="35275-152">Kas nauja ar pasikeitė</span><span class="sxs-lookup"><span data-stu-id="35275-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="35275-153">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="35275-153">Cost entries</span></span>](cost-entries.md)



