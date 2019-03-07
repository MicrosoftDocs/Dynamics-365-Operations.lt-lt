---
title: Kurti įsigijimo katalogą
description: Šiame vedlyje parodoma, kaip kurti įsigijimo katalogą.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "314698"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="f31f9-103">Kurti įsigijimo katalogą</span><span class="sxs-lookup"><span data-stu-id="f31f9-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f31f9-104">Šiame vedlyje parodoma, kaip kurti įsigijimo katalogą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="f31f9-105">Šią užduotį paprastai atlieka įsigijimo specialistas.</span><span class="sxs-lookup"><span data-stu-id="f31f9-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="f31f9-106">Taip pat sužinosite, kaip kurdami paraišką darbuotojai gali naudoti katalogą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="f31f9-107">Prieš kuriant katalogą, sistemoje turi būti nustatyta įsigijimo kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="f31f9-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="f31f9-108">Naujas katalogas perima hierarchiją ir visus hierarchijos produktus.</span><span class="sxs-lookup"><span data-stu-id="f31f9-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="f31f9-109">Šį vedlį galite naudoti demonstracinių duomenų įmonėje USMF, kurioje įgalinta įsigijimo kategorijų hierarchija, taip pat procedūros veiksmų pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="f31f9-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="f31f9-110">Įsitikinkite, kad įsigijimo kategorijų hierarchija nustatyta</span><span class="sxs-lookup"><span data-stu-id="f31f9-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="f31f9-111">Eikite į Įsigijimas ir šaltinio pasirinkimas > Įsigijimo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="f31f9-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="f31f9-112">Demonstracinių duomenų įmonėje USMF galima naudoti įsigijimo kategorijų hierarchiją, be to, produktai yra įtraukti į kategoriją Biuro mašinos / Kompiuteriai.</span><span class="sxs-lookup"><span data-stu-id="f31f9-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="f31f9-113">Jei šią procedūrą vykdote kaip užduočių vedlį, turėsite jį atrakinti, kad galėtumėte naršyti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="f31f9-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="f31f9-114">Jei hierarchija nesukurta, galite ją kurti spustelėdami Nauja.</span><span class="sxs-lookup"><span data-stu-id="f31f9-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="f31f9-115">Tai galima atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-115">This can only be done once.</span></span>  
2. <span data-ttu-id="f31f9-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f31f9-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="f31f9-117">Katalogo kūrimas</span><span class="sxs-lookup"><span data-stu-id="f31f9-117">Create a catalog</span></span>
1. <span data-ttu-id="f31f9-118">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Katalogai > Įsigijimo katalogai.</span><span class="sxs-lookup"><span data-stu-id="f31f9-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="f31f9-119">Spustelėdami Naujas įsigijimo katalogas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="f31f9-120">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f31f9-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f31f9-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="f31f9-121">Click OK.</span></span>
5. <span data-ttu-id="f31f9-122">Medyje išplėskite CORP ĮSIGIJIMO KATEGORIJOS.</span><span class="sxs-lookup"><span data-stu-id="f31f9-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="f31f9-123">Medyje išplėskite BIURO MAŠINOS.</span><span class="sxs-lookup"><span data-stu-id="f31f9-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="f31f9-124">Medyje pasirinkite Kompiuteriai.</span><span class="sxs-lookup"><span data-stu-id="f31f9-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="f31f9-125">Sąraše rodomi įsigijimo kategorijos produktai.</span><span class="sxs-lookup"><span data-stu-id="f31f9-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="f31f9-126">Jei į kategoriją norite įtraukti produktą, tai turite atlikti puslapyje Įsigijimo kategorijų hierarchija arba puslapyje Prekės informacija.</span><span class="sxs-lookup"><span data-stu-id="f31f9-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="f31f9-127">Numatytasis naujinimo tipas nustato, ar nauji į įsigijimo kategorijų hierarchiją įtraukti produktai yra iš karto matomi kataloge.</span><span class="sxs-lookup"><span data-stu-id="f31f9-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="f31f9-128">Jei naujinimo tipas nustatytas kaip Dinamiškas, keitimai matomi iš karto.</span><span class="sxs-lookup"><span data-stu-id="f31f9-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="f31f9-129">Jei naujinimo tipas nustatytas kaip Statinis, katalogą naudojantys asmenys naujus produktus matys tik tada, kai katalogas bus iš naujo publikuotas.</span><span class="sxs-lookup"><span data-stu-id="f31f9-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="f31f9-130">Veiksmas Publikuoti pateikiamas puslapio viršuje esančioje veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="f31f9-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="f31f9-131">Jei produktai pašalinami iš įsigijimo kategorijų hierarchijos, pakeitimas matomas iš karto, neatsižvelgiant į lauko Numatytasis naujinimo tipas reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f31f9-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="f31f9-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f31f9-133">Spustelėkite Slėpti.</span><span class="sxs-lookup"><span data-stu-id="f31f9-133">Click Hide.</span></span>
10. <span data-ttu-id="f31f9-134">Veiksmų srityje spustelėkite Kategorijos naršymas.</span><span class="sxs-lookup"><span data-stu-id="f31f9-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="f31f9-135">Spustelėkite Drausti.</span><span class="sxs-lookup"><span data-stu-id="f31f9-135">Click Disable.</span></span>
12. <span data-ttu-id="f31f9-136">Veiksmų srityje spustelėkite Kategorijos naršymas.</span><span class="sxs-lookup"><span data-stu-id="f31f9-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="f31f9-137">Spustelėkite Įgalinti.</span><span class="sxs-lookup"><span data-stu-id="f31f9-137">Click Enable.</span></span>
14. <span data-ttu-id="f31f9-138">Spustelėkite Aktyvinti katalogą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="f31f9-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f31f9-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="f31f9-140">Nustatyti katalogą kaip matomą</span><span class="sxs-lookup"><span data-stu-id="f31f9-140">Make the catalog visible</span></span>
1. <span data-ttu-id="f31f9-141">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="f31f9-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="f31f9-142">Pasirinkite Įsigijimo strategijos USMF.</span><span class="sxs-lookup"><span data-stu-id="f31f9-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="f31f9-143">Turite pasirinkti juridinio subjekto pirkimo strategiją, pagal kurią su jūsų vartotojo profilių susietas darbuotojas gali užsakyti produktus.</span><span class="sxs-lookup"><span data-stu-id="f31f9-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="f31f9-144">USMF demonstraciniuose duomenyse vartotojas administratorius yra susietas su darbuotoja, vardu Julia Funderburk, ir ji USMF produktus užsako pagal numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="f31f9-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="f31f9-145">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f31f9-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f31f9-146">Pasirinkite katalogą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="f31f9-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="f31f9-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f31f9-147">Click OK.</span></span>
6. <span data-ttu-id="f31f9-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f31f9-148">Close the page.</span></span>
7. <span data-ttu-id="f31f9-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f31f9-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="f31f9-150">Naudoti katalogą</span><span class="sxs-lookup"><span data-stu-id="f31f9-150">Use the catalog</span></span>
1. <span data-ttu-id="f31f9-151">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo paraiškos > Visos pirkimo paraiškos.</span><span class="sxs-lookup"><span data-stu-id="f31f9-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="f31f9-152">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f31f9-152">Click New.</span></span>
3. <span data-ttu-id="f31f9-153">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f31f9-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f31f9-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f31f9-154">Click OK.</span></span>
5. <span data-ttu-id="f31f9-155">Spustelėkite „Įtraukti produktus“.</span><span class="sxs-lookup"><span data-stu-id="f31f9-155">Click Add products.</span></span>
6. <span data-ttu-id="f31f9-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f31f9-157">Norėdami filtruoti produktus, galite naudoti kategorijų hierarchiją sąrašo kairėje pusėje arba filtrą sąrašo viršuje.</span><span class="sxs-lookup"><span data-stu-id="f31f9-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="f31f9-158">Spustelėkite „Įtraukti į eilutes“.</span><span class="sxs-lookup"><span data-stu-id="f31f9-158">Click Add to lines.</span></span>
8. <span data-ttu-id="f31f9-159">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f31f9-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f31f9-160">Spustelėkite „Įtraukti į eilutes“.</span><span class="sxs-lookup"><span data-stu-id="f31f9-160">Click Add to lines.</span></span>
10. <span data-ttu-id="f31f9-161">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f31f9-161">Click OK.</span></span>

