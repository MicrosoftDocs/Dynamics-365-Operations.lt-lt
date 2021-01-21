---
title: Trikties šalinimo sandėlio konfigūravimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646112"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="62a35-103">Trikties šalinimo sandėlio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="62a35-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62a35-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti konfigūruodami „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="62a35-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="62a35-105">Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė ar vieta negalioja"</span><span class="sxs-lookup"><span data-stu-id="62a35-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-106">Issue description</span></span>

<span data-ttu-id="62a35-107">Gausite šį klaidos pranešimą jums nuskaitant licencijos lentelės ID ar vietą.</span><span class="sxs-lookup"><span data-stu-id="62a35-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-108">Issue resolution</span></span>

<span data-ttu-id="62a35-109">Įsitikinkite, kad licencijos lentelės ID nėra rezervuotas kieno nors kito.</span><span class="sxs-lookup"><span data-stu-id="62a35-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="62a35-110">Ši klaida naudojama siekiant atlikti veiksmus, kai vertę, kurią vartotojas nuskaitė sandėlio programoje buvo galiojanti vieta ir galiojantis licencijos lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="62a35-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="62a35-111">Nepaisant to, ši problema buvo išspręsta 10.0.11 versijoje.</span><span class="sxs-lookup"><span data-stu-id="62a35-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="62a35-112">Gaunu tolesnį klaidos pranešimą: „Licencijos lentelė turi būti nurodyta šiai vietai"</span><span class="sxs-lookup"><span data-stu-id="62a35-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-113">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-113">Issue description</span></span>

<span data-ttu-id="62a35-114">Gausite šį klaidos pranešimą, jei sukursite perdavimo užsakymą naudodami sandėlį, kuris yra įjungtas papildomam sandėlio valdymui (WMS) ir tuomet pabaigę darbą, bandysite patvirtinti siuntimą.</span><span class="sxs-lookup"><span data-stu-id="62a35-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-115">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-115">Issue resolution</span></span>

<span data-ttu-id="62a35-116">**Numatytoji gavimo vieta** laukelis yra tuščias ir skirtas perdavimo sandėliui „iš“ sandėlio.</span><span class="sxs-lookup"><span data-stu-id="62a35-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="62a35-117">Norėdami ištaisyti šią problemą, nurodykite nustatytąją gavimo vietą perdavimo sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="62a35-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="62a35-118">Įsitikinkite, kad šį vieta yra licencijos lentelės valdoma.</span><span class="sxs-lookup"><span data-stu-id="62a35-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="62a35-119">Gaunu tolesnį klaidos pranešimą: „Negalite sukurti darbo šablono eilutės inventoriaus būsenos keitimui dėl to, kad darbo tipas neglaioja.</span><span class="sxs-lookup"><span data-stu-id="62a35-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="62a35-120">Pasirinkite kitą darbo tipą."</span><span class="sxs-lookup"><span data-stu-id="62a35-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-121">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-121">Issue description</span></span>

<span data-ttu-id="62a35-122">Darbo šablonui, negalite pasirinkti *Inventoriaus būsenos keitimas* stulpelyje **Darbo tipas** skyriuje **Darbo šablono išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="62a35-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-123">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-123">Issue resolution</span></span>

<span data-ttu-id="62a35-124">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="62a35-124">This behavior is by design.</span></span> <span data-ttu-id="62a35-125">*Inventoriaus būsenos keitimo* darbo tipas yra naudojamas sistemos procesų.</span><span class="sxs-lookup"><span data-stu-id="62a35-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="62a35-126">Jo konfigūruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="62a35-126">It can't be configured.</span></span> <span data-ttu-id="62a35-127">Kadangi darbo tipų sąrašai yra fiksuoti kaip numeravimas, papildomi objektai negali būti filtruojami iš **Darbo tipo** iškrentančio meniu.</span><span class="sxs-lookup"><span data-stu-id="62a35-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="62a35-128">Gaunu tolesnį klaidos pranešimą: „Kiekis negalioja 1% vienetui."</span><span class="sxs-lookup"><span data-stu-id="62a35-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-129">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-129">Issue description</span></span>

<span data-ttu-id="62a35-130">Kiekis negalioja *ea* vienetui, kai yra paėmimo darbas turintis keletą licencijos lentelių vienoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="62a35-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-131">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-131">Issue resolution</span></span>

<span data-ttu-id="62a35-132">Patikrinkite, ar **Vieneto sekos grupės ID** ir **Vieneto pavertimų** laukeliai išleistame produkte ar produkto variante yra nustatyti tinkamai.</span><span class="sxs-lookup"><span data-stu-id="62a35-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="62a35-133">Atkreipkite dėmesį, kad klaidos pranešimas buvo pagerintas versijoje 10.0.15 (žr. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="62a35-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="62a35-134">Naujas klaidos pranešimas yra, „Kiekis negalioja.</span><span class="sxs-lookup"><span data-stu-id="62a35-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="62a35-135">Tikėtina %1 %2."</span><span class="sxs-lookup"><span data-stu-id="62a35-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="62a35-136">Vietos kryptys pardavimo užsakymo padėjimo darbe, kelių SKU parinktis nevertina kelių vietų krypčių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="62a35-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-137">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-137">Issue description</span></span>

<span data-ttu-id="62a35-138">Krypties vietos *Pardavimo užsakymų* darbo tvarkos tipas ir *Padėjimo* darbo tipas nevertina kelių vietos krypties veiksmų, kai **Kelių SKU** parinktis pasirenkama.</span><span class="sxs-lookup"><span data-stu-id="62a35-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="62a35-139">Tik pirmasis vietos krypties veiksmas yra vertinamas.</span><span class="sxs-lookup"><span data-stu-id="62a35-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-140">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-140">Issue resolution</span></span>

<span data-ttu-id="62a35-141">Nauja funkcija, *Vertinti visus veiksmus kelioms SKU vietos kryptims* buvo įtraukta į versiją 10.0.15 (žr. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="62a35-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="62a35-142">Ši funkcija vertina visus veiksmus kelioms SKU vietos kryptims.</span><span class="sxs-lookup"><span data-stu-id="62a35-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="62a35-143">Jei jums reikia šios funkcijos, naudokite [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad ją įjungtumėte.</span><span class="sxs-lookup"><span data-stu-id="62a35-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="62a35-144">Negaliu naudoti sandėlio programos, kad atlikčiau dalinį paėmimą.</span><span class="sxs-lookup"><span data-stu-id="62a35-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-145">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-145">Issue description</span></span>

<span data-ttu-id="62a35-146">Prekybos ir perdavimo užsakymams negalite praleisti prekių ir atlikti dalinio paėmimo.</span><span class="sxs-lookup"><span data-stu-id="62a35-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-147">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-147">Issue resolution</span></span>

<span data-ttu-id="62a35-148">Puslapyje **Mobilaus įrenginio meniu prekės** kiekvienai meniu prekei, kuri yra nustatyta siekiant apdoroti prekybos užsakymus ar perdavimo užsakymus, nustatykite **Leisti atskyrimo darbo** parinktį **Bendri** „FastTab“ į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="62a35-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="62a35-149">Kaip galiu atlikti inventoriaus būsenos keitimą daliniam kiekio darbui?</span><span class="sxs-lookup"><span data-stu-id="62a35-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="62a35-150">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="62a35-150">Issue description</span></span>

<span data-ttu-id="62a35-151">Norite atlikti inventoriaus būsenos keitimą daliniam bendram kiekiui.</span><span class="sxs-lookup"><span data-stu-id="62a35-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62a35-152">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="62a35-152">Issue resolution</span></span>

<span data-ttu-id="62a35-153">Norėdami leisti darbuotojams atlikti šį keitimą, galite sukurti meniu prekę sandėlio programai.</span><span class="sxs-lookup"><span data-stu-id="62a35-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="62a35-154">Puslapyje **Mobilaus įrenginio meniu prekės** sukurkite (ar redaguokite) meniu prekę, kuri turi tolesnius nustatymus:</span><span class="sxs-lookup"><span data-stu-id="62a35-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="62a35-155">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="62a35-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="62a35-156">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="62a35-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="62a35-157">**Darbo sukūrimo procesas:** *Judėjimas*</span><span class="sxs-lookup"><span data-stu-id="62a35-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="62a35-158">**Rodyti inventoriaus būseną:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="62a35-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="62a35-159">Galite nustatyti kitus laukelius puslapyje, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="62a35-159">You can set other fields on the page as you require.</span></span>