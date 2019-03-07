---
title: Savikainos įrašai
description: Šiame straipsnyje pateikiama informacija apie savikainos įrašus ir kada jie kuriami. Savikainos įrašas yra toks įrašas, kuris registruoja tam tikro įvykio kiekį ir išlaidas.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb1a218dd5e6ab3f8029788af359b89521d6afdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "325485"
---
# <a name="cost-entries"></a><span data-ttu-id="6df7a-104">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="6df7a-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6df7a-105">Šiame straipsnyje pateikiama informacija apie savikainos įrašus ir kada jie kuriami.</span><span class="sxs-lookup"><span data-stu-id="6df7a-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="6df7a-106">Savikainos įrašas yra toks įrašas, kuris registruoja tam tikro įvykio kiekį ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6df7a-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="6df7a-107">Išlaidų įrašai yra atsargų operacijų telkimai, įrašyti aktyviose finansinių atsargų dimensijose.</span><span class="sxs-lookup"><span data-stu-id="6df7a-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="6df7a-108">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="6df7a-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="6df7a-109">1 pavyzdys: nesukuriama jokių išlaidų įrašų</span><span class="sxs-lookup"><span data-stu-id="6df7a-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="6df7a-110">Registruojamas perkėlimo žurnalo įvykis.</span><span class="sxs-lookup"><span data-stu-id="6df7a-110">A transfer journal event is registered.</span></span> <span data-ttu-id="6df7a-111">Įvykis vieną prekės A vienetą perkelia iš vietos A į vietą B. Vietos atsargų dimensija nelaikoma išlaidų objekto dalimi.</span><span class="sxs-lookup"><span data-stu-id="6df7a-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="6df7a-112">Todėl įvykis sukuria dvi atsargų operacijas ir nė vieno išlaidų įrašo.</span><span class="sxs-lookup"><span data-stu-id="6df7a-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="6df7a-113">2 pavyzdys: sukuriama išlaidų įrašų</span><span class="sxs-lookup"><span data-stu-id="6df7a-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="6df7a-114">Registruojamas perkėlimo žurnalo įvykis.</span><span class="sxs-lookup"><span data-stu-id="6df7a-114">A transfer journal event is registered.</span></span> <span data-ttu-id="6df7a-115">Įvykis vieną prekės A vienetą perkelia iš 1 teritorijos į 2 teritoriją.</span><span class="sxs-lookup"><span data-stu-id="6df7a-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="6df7a-116">Teritorijos atsargų dimensija laikoma išlaidų objekto dalimi.</span><span class="sxs-lookup"><span data-stu-id="6df7a-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="6df7a-117">Todėl įvykis sukuria dvi atsargų operacijas ir du išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="6df7a-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="6df7a-118">3 pavyzdys: sukuriamas vienas išlaidų įrašas</span><span class="sxs-lookup"><span data-stu-id="6df7a-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="6df7a-119">Registruojamas pirkimo užsakymo produkto gavimo įvykis.</span><span class="sxs-lookup"><span data-stu-id="6df7a-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="6df7a-120">Įvykis užregistruoja 100 prekės A vienetų, kurio vieno kaina – 10,00 JAV dolerių (USD).</span><span class="sxs-lookup"><span data-stu-id="6df7a-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="6df7a-121">Kadangi prekė A naudoja serijos numerį sekti atsargų valdymo paskirčiai, sukuriamas unikalus kiekvienos gautos prekės serijos numeris.</span><span class="sxs-lookup"><span data-stu-id="6df7a-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="6df7a-122">Todėl įvykis sukuria 100 atsargų operacijų ir vieną išlaidų įrašą.</span><span class="sxs-lookup"><span data-stu-id="6df7a-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="6df7a-123">Išlaidų įrašų puslapis</span><span class="sxs-lookup"><span data-stu-id="6df7a-123">Cost entries page</span></span>
<span data-ttu-id="6df7a-124">Naujasis **Išlaidų įrašų** puslapis leidžia peržiūrėti ir valdyti kiekių bei išlaidų registravimą.</span><span class="sxs-lookup"><span data-stu-id="6df7a-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="6df7a-125">Šis puslapis papildo **Atsargų operacijos** ir **Atsargų sudengimo** puslapius.</span><span class="sxs-lookup"><span data-stu-id="6df7a-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="6df7a-126">Įvykio įrašai registruojami chronologine tvarka.</span><span class="sxs-lookup"><span data-stu-id="6df7a-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="6df7a-127">Todėl galite greitai rasti ir valdyti sukauptas konkretaus įvykio ar visų įvykių, susijusių su dokumentu, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6df7a-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="6df7a-128">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6df7a-128">Here is an example:</span></span>

-   <span data-ttu-id="6df7a-129">Registruojamas prekės A produkto gavimo įvykis. Gaunama šimtas vienetų, kurio vieno kaina – 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="6df7a-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="6df7a-130">Praėjus kelioms dienoms po SF įvykio registravimo, kaina padidėja iki 11,00 USD.</span><span class="sxs-lookup"><span data-stu-id="6df7a-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="6df7a-131">Todėl bendroji suma yra 1 100 USD.</span><span class="sxs-lookup"><span data-stu-id="6df7a-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="6df7a-132">Sukuriamas antrasis kvitas, atitinkantis 100 USD skirtumą.</span><span class="sxs-lookup"><span data-stu-id="6df7a-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="6df7a-133">Po kelių dienų pirkimo užsakyme registruojamos papildomos 15,00 USD išlaidos, skirtos padengti transportavimo išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="6df7a-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="6df7a-134">Kvitas</span><span class="sxs-lookup"><span data-stu-id="6df7a-134">Voucher</span></span> | <span data-ttu-id="6df7a-135">Data</span><span class="sxs-lookup"><span data-stu-id="6df7a-135">Date</span></span>       | <span data-ttu-id="6df7a-136">Nuoroda</span><span class="sxs-lookup"><span data-stu-id="6df7a-136">Reference</span></span>      | <span data-ttu-id="6df7a-137">Skaičius</span><span class="sxs-lookup"><span data-stu-id="6df7a-137">Number</span></span> | <span data-ttu-id="6df7a-138">Partijos numeris</span><span class="sxs-lookup"><span data-stu-id="6df7a-138">Lot ID</span></span>  | <span data-ttu-id="6df7a-139">Kiekis</span><span class="sxs-lookup"><span data-stu-id="6df7a-139">Quantity</span></span> | <span data-ttu-id="6df7a-140">Suma</span><span class="sxs-lookup"><span data-stu-id="6df7a-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="6df7a-141">00001</span><span class="sxs-lookup"><span data-stu-id="6df7a-141">00001</span></span>   | <span data-ttu-id="6df7a-142">2015-01-01</span><span class="sxs-lookup"><span data-stu-id="6df7a-142">01-01-2015</span></span> | <span data-ttu-id="6df7a-143">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6df7a-143">Purchase order</span></span> | <span data-ttu-id="6df7a-144">100001</span><span class="sxs-lookup"><span data-stu-id="6df7a-144">100001</span></span> | <span data-ttu-id="6df7a-145">0000101</span><span class="sxs-lookup"><span data-stu-id="6df7a-145">0000101</span></span> | <span data-ttu-id="6df7a-146">100,00</span><span class="sxs-lookup"><span data-stu-id="6df7a-146">100.00</span></span>   | <span data-ttu-id="6df7a-147">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6df7a-147">1000.00</span></span> |
| <span data-ttu-id="6df7a-148">00002</span><span class="sxs-lookup"><span data-stu-id="6df7a-148">00002</span></span>   | <span data-ttu-id="6df7a-149">2015-01-20</span><span class="sxs-lookup"><span data-stu-id="6df7a-149">20-01-2015</span></span> | <span data-ttu-id="6df7a-150">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="6df7a-150">Purchase order</span></span> | <span data-ttu-id="6df7a-151">100001</span><span class="sxs-lookup"><span data-stu-id="6df7a-151">100001</span></span> | <span data-ttu-id="6df7a-152">0000101</span><span class="sxs-lookup"><span data-stu-id="6df7a-152">0000101</span></span> |          | <span data-ttu-id="6df7a-153">100,00</span><span class="sxs-lookup"><span data-stu-id="6df7a-153">100.00</span></span>  |
| <span data-ttu-id="6df7a-154">00003</span><span class="sxs-lookup"><span data-stu-id="6df7a-154">00003</span></span>   | <span data-ttu-id="6df7a-155">2015-01-31</span><span class="sxs-lookup"><span data-stu-id="6df7a-155">31-01-2015</span></span> | <span data-ttu-id="6df7a-156">Koregavimas</span><span class="sxs-lookup"><span data-stu-id="6df7a-156">Adjustment</span></span>     | <span data-ttu-id="6df7a-157">100001</span><span class="sxs-lookup"><span data-stu-id="6df7a-157">100001</span></span> | <span data-ttu-id="6df7a-158">0000101</span><span class="sxs-lookup"><span data-stu-id="6df7a-158">0000101</span></span> |          | <span data-ttu-id="6df7a-159">15,00</span><span class="sxs-lookup"><span data-stu-id="6df7a-159">15.00</span></span>   |

<span data-ttu-id="6df7a-160">**Išlaidų įrašų** puslapyje galima filtruoti pagal dokumento ID ir dokumento datą.</span><span class="sxs-lookup"><span data-stu-id="6df7a-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="6df7a-161">Galimi tik [išlaidų objektų](cost-object.md) arba išleistų produktų išlaidų įrašai.</span><span class="sxs-lookup"><span data-stu-id="6df7a-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6df7a-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6df7a-162">Additional resources</span></span>
--------

[<span data-ttu-id="6df7a-163">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="6df7a-163">Cost objects</span></span>](cost-object.md)



