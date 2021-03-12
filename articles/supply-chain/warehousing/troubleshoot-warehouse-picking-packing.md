---
title: Paėmimo ir pakavimo trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti paimdami ir pakuodami „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993939"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="db236-103">Paėmimo ir pakavimo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="db236-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db236-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti paimdami ir pakuodami „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="db236-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="db236-105">Gaunu tolesnį klaidos pranešimą: „Matmenų vietos negali būti paliktos tuščios, jei matmenų serijinis numeris yra nustatytas“.</span><span class="sxs-lookup"><span data-stu-id="db236-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-106">Issue description</span></span>

<span data-ttu-id="db236-107">Gausite šį klaidos pranešimą, jei sukursite perdavimo užsakymą serijinei prekei naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą, bandysite patvirtinti siuntimą.</span><span class="sxs-lookup"><span data-stu-id="db236-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-108">Issue resolution</span></span>

<span data-ttu-id="db236-109">**Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio.</span><span class="sxs-lookup"><span data-stu-id="db236-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="db236-110">Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="db236-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="db236-111">Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.</span><span class="sxs-lookup"><span data-stu-id="db236-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="db236-112">Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė negalioja."</span><span class="sxs-lookup"><span data-stu-id="db236-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-113">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-113">Issue description</span></span>

<span data-ttu-id="db236-114">Gausite šį klaidos pranešimą sandėlio programoje jums nuskaitant licencijos lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="db236-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-115">Issue resolution</span></span>

<span data-ttu-id="db236-116">Įsitikinkite, kad licencijos lentelės ID yra licencijos lentelės lentelėje ir kad prekės ir kiekiai licencijos lentelėje yra prieinami (kitaip tariant, jie nėra blokuojami).</span><span class="sxs-lookup"><span data-stu-id="db236-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="db236-117">Gaunu tolesnį klaidos pranšimą: „Laukelio krovinio svoris'(=-%1) gali būti sudarytas tik iš teigiamų skaičių.</span><span class="sxs-lookup"><span data-stu-id="db236-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="db236-118">Naujinimas buvo atšauktas."</span><span class="sxs-lookup"><span data-stu-id="db236-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-119">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-119">Issue description</span></span>

<span data-ttu-id="db236-120">Gaunate šį klaidos pranešimą, jei yra atviras darbas jums apdorojant darbą iš pakavimo vietų į parengimo vietas arba iš parengimo vietų į dokų vietas.</span><span class="sxs-lookup"><span data-stu-id="db236-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-121">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-121">Issue resolution</span></span>

<span data-ttu-id="db236-122">Norėdami ištaisyti šią problemą, eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenų bazė \> Nuoseklumos tikrinimas** ir vykdykite procesą **Sandėlio krovinio svorio nuoseklumo tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="db236-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="db236-123">Gaunu tolesnį klaidos pranešimą: „Kiekis negalioja %1 vienetui."</span><span class="sxs-lookup"><span data-stu-id="db236-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-124">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-124">Issue description</span></span>

<span data-ttu-id="db236-125">Gaunate šį klaidos pranešimą bandydami atlikti *atskyrimo paėmimo* darbą keliuose palaiduose kiekiuose.</span><span class="sxs-lookup"><span data-stu-id="db236-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-126">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-126">Issue resolution</span></span>

<span data-ttu-id="db236-127">Sandėlio darbuotojas privalo naudoti *Trumpo paėmimo* procesą sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="db236-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="db236-128">Jei bandote paimti keletą palaidų kiekių iš vienos vietos, galite taip pat naudoti **Visą** parinktį sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="db236-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="db236-129">Negaliu perkelti inventoriaus į vietą, kurią valdo licencijos plokštelė.</span><span class="sxs-lookup"><span data-stu-id="db236-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-130">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-130">Issue description</span></span>

<span data-ttu-id="db236-131">Negalite sumažinti paimto kiekio krovinyje.</span><span class="sxs-lookup"><span data-stu-id="db236-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-132">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-132">Issue resolution</span></span>

<span data-ttu-id="db236-133">Ankstesnėse versijose, negalite sumažinti paimto krovinio kiekio.</span><span class="sxs-lookup"><span data-stu-id="db236-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="db236-134">Nepaisant to, galite dabar nepaimti licencijso lentelės valdomos vietos.</span><span class="sxs-lookup"><span data-stu-id="db236-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="db236-135">Privalote nurodyti **Vietos** vertę ir **Licencijos lentelės** vertę apkrovos eilutei **Sumažinti paimtą kiekį** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="db236-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="db236-136">Ar galiu spausdinti pristatymo važtaraštį ar sandėlio pakavimo lapą?</span><span class="sxs-lookup"><span data-stu-id="db236-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-137">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-137">Issue description</span></span>

<span data-ttu-id="db236-138">Norite spausdinti pristatymo važtaraštį ar sandėlio pakavimo lapą ar saito **Darbo audito šablono eilutės naujinimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="db236-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-139">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-139">Issue resolution</span></span>

<span data-ttu-id="db236-140">Jums spausdinant dokumentą naudodami Spausdinimo valdymo nustatymus, norint apriboti tikslą (saito/sandėlio) per Spausdinimo valdymą, o ne pasirinkimą **Redaguoti spausdinimo nustatymus** puslapyje **Darbo audito šablono eilutės naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="db236-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="db236-141">Negaliu atšaukti paėmimo kvito po to, kai jis publikuotas prekybos užsakyme.</span><span class="sxs-lookup"><span data-stu-id="db236-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-142">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-142">Issue description</span></span>

<span data-ttu-id="db236-143">Paimant ir siunčiant procesus įjungtus WMS, negalite atšaukti pakavimo kvitą po to, kai jis publikuotas iš pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="db236-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-144">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-144">Issue resolution</span></span>

<span data-ttu-id="db236-145">Siekiant tinkamai publikuoti pakavimo kvitus prekėms, kurios bus įjungtos WMS, publikavimas turi vykti iš krovinio, o ne iš užsakymo.</span><span class="sxs-lookup"><span data-stu-id="db236-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="db236-146">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="db236-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="db236-147">Bendrrai, prekybos užsakymas, kuris buvo paimtas ir siųstas per sandėlio valdymo procesus gali būti supakuotas naujinant kvitą iš krovinio ar siuntimo ir prekybos užsakymo dokumente.</span><span class="sxs-lookup"><span data-stu-id="db236-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="db236-148">Nepaisant to, jei pakuojate kvito naujinimą prekybos užsakyme iš pardavimo užsakymo dokumento, pakavimo dokumento grąžinimas negali būti atliekamas iš krovinio ar prekybos užsakymo.</span><span class="sxs-lookup"><span data-stu-id="db236-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="db236-149">Dėl to, rekomenduojame jums naudoti pakavimo kvito publikavimą iš krovinio.</span><span class="sxs-lookup"><span data-stu-id="db236-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="db236-150">Tokiu atveju, grąžinimas turi būti atliekamas, kai įjungtas krovinys.</span><span class="sxs-lookup"><span data-stu-id="db236-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="db236-151">Gaunu tolesnį klaidos pranešimą: „Nepakankamas darbas gali būti randamas klasteryje."</span><span class="sxs-lookup"><span data-stu-id="db236-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="db236-152">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="db236-152">Issue description</span></span>

<span data-ttu-id="db236-153">Jums naudojant *Sistemos kreipiamą klasterio paėmimo* procesą, jei konfigūruojate klasterio profilį, kai pavyzdžiui, 10 padėčių gali būti paimtos, procesas veikia kaip planuota, kai yra pakankamai darbo siekiant paimti iki 10 padėčių.</span><span class="sxs-lookup"><span data-stu-id="db236-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="db236-154">Nepaisant to, jei yra tik aštuonios padėtys paėmimiui, gaunate šį klaidos pranešimą, nes nesama pakankamai darbo vienam klasteriui.</span><span class="sxs-lookup"><span data-stu-id="db236-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="db236-155">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="db236-155">Issue resolution</span></span>

<span data-ttu-id="db236-156">Siekiant ištaisyti šią problemą, redaguokite klasterio profilį ir nustatykite **Įjungti padėtis** parinktį į *Ne*.</span><span class="sxs-lookup"><span data-stu-id="db236-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>
