---
title: Siuntimų ir krovinio kūrimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami krovinio kūrimu ir siuntimu „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828207"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="4ab07-103">Siuntimų ir krovinio kūrimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ab07-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami krovinio kūrimu ir siuntimu „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="4ab07-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="4ab07-105">Gaunu tolesnį klaidos pranešimą: „Negalite sukurti krovinio eilutės šiam užsakymo eilutei, nes joje esantys inventoriaus matmenys negalioja...“</span><span class="sxs-lookup"><span data-stu-id="4ab07-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4ab07-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4ab07-106">Issue description</span></span>

<span data-ttu-id="4ab07-107">Gaunate tolesnį klaidos pranešimą bandydami išleisti grąžinimo prekybos užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ab07-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="4ab07-108">Gaunu tolesnį klaidos pranešimą: „Negalite sukurti krovinio eilutės šiam užsakymo eilutei, nes joje esantys inventoriaus matmenys negalioja.</span><span class="sxs-lookup"><span data-stu-id="4ab07-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="4ab07-109">Negalite susieti inventoriaus matmenų, kurios yra nustatytos po vietos matmenimis rezervacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="4ab07-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="4ab07-110">Pašalinkite negaliojančius matmenis iš prekybos eilutės.</span><span class="sxs-lookup"><span data-stu-id="4ab07-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4ab07-111">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-111">Issue resolution</span></span>

<span data-ttu-id="4ab07-112">Deja, produktas nepalaiko krovinio apdorojimo prekybos grąžinimo procese.</span><span class="sxs-lookup"><span data-stu-id="4ab07-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="4ab07-113">Dėl to, negalite išleisti grąžinimo prekybos užsakymo į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ab07-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="4ab07-114">Prekybos užsakymo perlaidose, negalite nurodyti inventoriaus matmenų, kurie yra žemiau **Vietos** matmenų rezervacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="4ab07-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="4ab07-115">Išsprendimas skirtas pašalinti negaliojančius matmenis iš prekybos eilutės.</span><span class="sxs-lookup"><span data-stu-id="4ab07-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="4ab07-116">Gaunu tolesnį klaidos pranešimą: „Viena iš eilučių jau yra krovinyje.</span><span class="sxs-lookup"><span data-stu-id="4ab07-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="4ab07-117">Negali išleisti į sandėlį.“</span><span class="sxs-lookup"><span data-stu-id="4ab07-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4ab07-118">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4ab07-118">Issue description</span></span>

<span data-ttu-id="4ab07-119">Jei rankiniu būdu sukuriate krovinius arba jei nustatote procesą taip, kad kroviniai jau sukuriami prieš prekybos užsakymo eilutės objektą, prielaida yra tokia, kad tolesnis išleidimas bus atliktas rankiniu būdu ir kad maršrutas bei kainos iš krovinio bus naudojamos.</span><span class="sxs-lookup"><span data-stu-id="4ab07-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="4ab07-120">Kitu galimu scenarijumi, bandote atlikti automatinį paleidimą į sandėlį, tačiau bangos procesui nepavyko sukurti darbą.</span><span class="sxs-lookup"><span data-stu-id="4ab07-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="4ab07-121">Dėl to, atviras siuntimas ar krovinys vis dar yra sukurtas.</span><span class="sxs-lookup"><span data-stu-id="4ab07-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="4ab07-122">Šis atviras siuntimas arba krovinys tuomet užblokuoja vėlesnius bandymus automatiškai paleisti užsakymą iki tol, kol panaikinsite atvirą siuntimą ar krovinį, arba rankiniu būdu iš naujo apdorosite bangą.</span><span class="sxs-lookup"><span data-stu-id="4ab07-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4ab07-123">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-123">Issue resolution</span></span>

<span data-ttu-id="4ab07-124">Galite išleisti iš prekybos užsakymo puslapio ar automatinis paleidimas gali būti atliktas iš išleidimo prekybos užsakymo puslapio tik jei nėra jokio krovinio prieš išleidimą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ab07-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="4ab07-125">Krovinys bus sukuriamas automatiniu būdu po bangos apdorojimo.</span><span class="sxs-lookup"><span data-stu-id="4ab07-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="4ab07-126">Gaunu tolesnį klaidos pranešimą: „Pristatymo važtaraščio koregavimas negali būti apdorojamas.</span><span class="sxs-lookup"><span data-stu-id="4ab07-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="4ab07-127">Pristatymo važtaraštyje yra tik prekės, kurias veikia sandėlio valdymo procesai, nes jų nepalaiko pristatymo pažymos koregavimas.”</span><span class="sxs-lookup"><span data-stu-id="4ab07-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="4ab07-128">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4ab07-128">Issue description</span></span>

<span data-ttu-id="4ab07-129">Po to, kai publikuojate pristatymo važtaraštį, nebegalite jo atšaukti, nes **Atšaukimo** mygtukas yra neprieinamas.</span><span class="sxs-lookup"><span data-stu-id="4ab07-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="4ab07-130">Taip pat, negali koreguoti pristatymo važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="4ab07-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="4ab07-131">Jei bandote, gausite šį klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="4ab07-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4ab07-132">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-132">Issue resolution</span></span>

<span data-ttu-id="4ab07-133">Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios įjungtos išplėstiniam sandėlio valdymui (WMS), privalote publikuoti iš krovinio, o ne tiesiogiai iš užsakymo.</span><span class="sxs-lookup"><span data-stu-id="4ab07-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="4ab07-134">Kaip galiu sukurti darbą iš išvesties krovinių, o ne bangų?</span><span class="sxs-lookup"><span data-stu-id="4ab07-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="4ab07-135">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4ab07-135">Issue description</span></span>

<span data-ttu-id="4ab07-136">Pateikiamas vienas iš būdų pakartotinai sukurti šią problemą.</span><span class="sxs-lookup"><span data-stu-id="4ab07-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="4ab07-137">Sukurkite išvesties krovinį naudodami prekybos užsakymą ar perdavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4ab07-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="4ab07-138">Išleiskite krovinį į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ab07-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="4ab07-139">Atkreipkite dėmesį, kad dar nebuvo sukurtas joks paėmimo darbas.</span><span class="sxs-lookup"><span data-stu-id="4ab07-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4ab07-140">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-140">Issue resolution</span></span>

<span data-ttu-id="4ab07-141">Jei darbas turi būti sukurtas nedelsiant, kai krovinys paleidžiamas, turite atitinkamai sukonfigūruoti bangos šabloną.</span><span class="sxs-lookup"><span data-stu-id="4ab07-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="4ab07-142">Bangos šablone, nustatykite tolesnes parinktis į *Taip*:</span><span class="sxs-lookup"><span data-stu-id="4ab07-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="4ab07-143">Automatiškai kurti bangą</span><span class="sxs-lookup"><span data-stu-id="4ab07-143">Automate wave creation</span></span>
- <span data-ttu-id="4ab07-144">Apdoroti bangą išleidžiant ją į sandėlį</span><span class="sxs-lookup"><span data-stu-id="4ab07-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="4ab07-145">Automatizuoti bangos išleidimą</span><span class="sxs-lookup"><span data-stu-id="4ab07-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="4ab07-146">Negaliu išleisti dalinio siųsto krovinio.</span><span class="sxs-lookup"><span data-stu-id="4ab07-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4ab07-147">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4ab07-147">Issue description</span></span>

<span data-ttu-id="4ab07-148">Negalite išleisti dalinio siųsto krovinio į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ab07-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="4ab07-149">Jums atliekant išleidimą į sandėlį, rodomas pranešimas „Veiksmas užbaigtas“, bet nieko nevyksta ir likusiam kiekiui nėra sukuriamas joks darbas.</span><span class="sxs-lookup"><span data-stu-id="4ab07-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="4ab07-150">Ši problema atsitinka jums naudojant transportavimo krovinio funkciją ir kai yra nebaigta rezervacija.</span><span class="sxs-lookup"><span data-stu-id="4ab07-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4ab07-151">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4ab07-151">Issue resolution</span></span>

<span data-ttu-id="4ab07-152">[KB problema 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) („Dalinai siunčiami kroviniai gali būti iš naujo suplanuojami bangai arba pakartotinai apdorojami") yra ištaisyta [versijoje 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="4ab07-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]