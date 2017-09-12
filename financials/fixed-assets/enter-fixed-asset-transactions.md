---
title: "Ilgalaikio turto operacijų parinktys"
description: "Šiame straipsnyje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 3d16b43eda0157e63a0d30fe806dac9a359d5fa4
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="e9338-103">Ilgalaikio turto operacijų parinktys</span><span class="sxs-lookup"><span data-stu-id="e9338-103">Fixed asset transaction options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e9338-104">Šiame straipsnyje aprašomi galimi skirtingi metodai ilgalaikio turto operacijoms kurti.</span><span class="sxs-lookup"><span data-stu-id="e9338-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="e9338-105">Galite nustatyti, kad ilgalaikis turtas būtų integruotas su mokėtinomis sumomis, gautinomis sumomis, paraiškomis ir didžiąja knyga.</span><span class="sxs-lookup"><span data-stu-id="e9338-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="e9338-106">Taip pat galite perkelti prekes atsargų valdyme į ilgalaikį turtą, jei norite tas prekes naudoti viduje.</span><span class="sxs-lookup"><span data-stu-id="e9338-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="e9338-107">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="e9338-107">Accounts payable</span></span>
<span data-ttu-id="e9338-108">Ilgalaikio turto operacijas Galite įvesti puslapyje Žurnalo kvitas.</span><span class="sxs-lookup"><span data-stu-id="e9338-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="e9338-109">Šį puslapį galima atidaryti iš puslapio SF žurnalas.</span><span class="sxs-lookup"><span data-stu-id="e9338-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="e9338-110">Žurnalo kvito puslapį taip pat galite atidaryti iš SF patvirtinimo žurnalo puslapio.</span><span class="sxs-lookup"><span data-stu-id="e9338-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="e9338-111">Korespondentinės sąskaitos tipo lauke pasirinkite Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="e9338-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="e9338-112">Tada lauke Korespondentinė sąskaita pasirinkite ilgalaikio turto numerį.</span><span class="sxs-lookup"><span data-stu-id="e9338-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="e9338-113">Skirtuke Ilgalaikis turtas įveskite reikšmes laukuose Operacijos tipas ir Knygos.</span><span class="sxs-lookup"><span data-stu-id="e9338-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="e9338-114">Gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="e9338-114">Accounts receivable</span></span>
<span data-ttu-id="e9338-115">Ilgalaikio turto operacijas galite įvesti puslapyje Laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="e9338-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="e9338-116">Puslapyje Laisvos formos SF, SF eilučių tinklelyje pasirinkite eilutės prekę.</span><span class="sxs-lookup"><span data-stu-id="e9338-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="e9338-117">Spustelėkite „FastTab‟ Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="e9338-117">Click the Line details FastTab.</span></span> <span data-ttu-id="e9338-118">Įveskite ilgalaikio turto numerį ir likvidavimo operacijos knygą.</span><span class="sxs-lookup"><span data-stu-id="e9338-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="e9338-119">Laisvos formos sąskaitų faktūrų ilgalaikio turto operacijos tipas visuomet yra Likvidavimas – pardavimas.</span><span class="sxs-lookup"><span data-stu-id="e9338-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="e9338-120">Paraiškos</span><span class="sxs-lookup"><span data-stu-id="e9338-120">Procurement and sourcing</span></span>
<span data-ttu-id="e9338-121">Ilgalaikio turto operacijas Galite įvesti puslapyje Pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="e9338-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="e9338-122">Norėdami sukurti pirkimo užsakymą, įveskite reikalingą informaciją ir spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="e9338-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="e9338-123">Pirkimo užsakymo puslapyje spustelėkite „FastTab‟ Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="e9338-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="e9338-124">Tada skirtuke Ilgalaikis turtas įveskite informaciją apie ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="e9338-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="e9338-125">Norėdami užregistruoti esančio ilgalaikio turto įsigijimo operaciją, nurodykite ilgalaikio turto numerį, knygą ir operacijos tipą.</span><span class="sxs-lookup"><span data-stu-id="e9338-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="e9338-126">Negalima registruoti ilgalaikio turto, jei šios informacijos nėra.</span><span class="sxs-lookup"><span data-stu-id="e9338-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="e9338-127">Norėdami registruoti naujo ilgalaikio turto įsigijimo operaciją, pasirinkite parinktį Naujas ilgalaikis turtas? ir pasirinkite ilgalaikio turto grupę, kuriai norite priskirti naują turtą.</span><span class="sxs-lookup"><span data-stu-id="e9338-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="e9338-128">Tačiau nebus galima nei viena iš ilgalaikio turto laukų eilučių, jei elementas bus atsargų modelių grupėje, kuriai naudojamas standartinių išlaidų atsargų modelis.</span><span class="sxs-lookup"><span data-stu-id="e9338-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="e9338-129">Be to, parinktys, apibrėžtos puslapyje Ilgalaikio turto parametrai, nustato, ar galite registruoti įsigijimo operacijas iš pirkimo modulių.</span><span class="sxs-lookup"><span data-stu-id="e9338-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="e9338-130">Kai pirkimo užsakymas arba Ilgalaikio turto atsargų žurnalas naudojami įsigyti ilgalaikiam turtui, pasikeičia atsargų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="e9338-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="e9338-131">Didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="e9338-131">General ledger</span></span>
<span data-ttu-id="e9338-132">Bet kokį ilgalaikio turto operacijos tipą galima registruoti puslapyje Bendrasis žurnalas.</span><span class="sxs-lookup"><span data-stu-id="e9338-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="e9338-133">Taip pat galite naudoti žurnalus ilgalaikio turto operacijoms registruoti.</span><span class="sxs-lookup"><span data-stu-id="e9338-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="e9338-134">Ilgalaikio turto operacijų tipų įvedimo pasirinktys</span><span class="sxs-lookup"><span data-stu-id="e9338-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="e9338-135">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="e9338-135">Transaction type</span></span>                    | <span data-ttu-id="e9338-136">Modulis</span><span class="sxs-lookup"><span data-stu-id="e9338-136">Module</span></span>                   | <span data-ttu-id="e9338-137">Pasirinktys</span><span class="sxs-lookup"><span data-stu-id="e9338-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="e9338-138">Įsigijimas, Įsigijimo koregavimas</span><span class="sxs-lookup"><span data-stu-id="e9338-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="e9338-139">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="e9338-139">Fixed assets</span></span>             | <span data-ttu-id="e9338-140">Ilgalaikis turtas, Atsargos į ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="e9338-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="e9338-141">Didžioji knyga</span><span class="sxs-lookup"><span data-stu-id="e9338-141">General ledger</span></span>           | <span data-ttu-id="e9338-142">Pagrindinis žurnalas</span><span class="sxs-lookup"><span data-stu-id="e9338-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="e9338-143">Mokėtinos sumos</span><span class="sxs-lookup"><span data-stu-id="e9338-143">Accounts payable</span></span>         | <span data-ttu-id="e9338-144">SF žurnalas, SF patvirtinimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="e9338-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="e9338-145">Paraiškos</span><span class="sxs-lookup"><span data-stu-id="e9338-145">Procurement and sourcing</span></span> | <span data-ttu-id="e9338-146">Pirkimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="e9338-146">Purchase order</span></span>                            |
| <span data-ttu-id="e9338-147">Nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="e9338-147">Depreciation</span></span>                        | <span data-ttu-id="e9338-148">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="e9338-148">Fixed assets</span></span>             | <span data-ttu-id="e9338-149">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="e9338-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="e9338-150">DK</span><span class="sxs-lookup"><span data-stu-id="e9338-150">General ledger</span></span>           | <span data-ttu-id="e9338-151">Pagrindinis žurnalas</span><span class="sxs-lookup"><span data-stu-id="e9338-151">General journal</span></span>                           |
| <span data-ttu-id="e9338-152">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="e9338-152">Disposal</span></span>                            | <span data-ttu-id="e9338-153">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="e9338-153">Fixed assets</span></span>             | <span data-ttu-id="e9338-154">Ilgalaikis turtas</span><span class="sxs-lookup"><span data-stu-id="e9338-154">Fixed assets</span></span>                              |
| <span data-ttu-id="e9338-155">** **</span><span class="sxs-lookup"><span data-stu-id="e9338-155">** **</span></span>                               | <span data-ttu-id="e9338-156">DK</span><span class="sxs-lookup"><span data-stu-id="e9338-156">General ledger</span></span>           | <span data-ttu-id="e9338-157">Pagrindinis žurnalas</span><span class="sxs-lookup"><span data-stu-id="e9338-157">General journal</span></span>                           |
| <span data-ttu-id="e9338-158">** **</span><span class="sxs-lookup"><span data-stu-id="e9338-158">** **</span></span>                               | <span data-ttu-id="e9338-159">Gautinos sumos</span><span class="sxs-lookup"><span data-stu-id="e9338-159">Accounts receivable</span></span>      | <span data-ttu-id="e9338-160">Laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="e9338-160">Free text invoice</span></span>                         |



<span data-ttu-id="e9338-161">Norėdami daugiau informacijos žr. [Ilgalaikio turto integravimas](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="e9338-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




