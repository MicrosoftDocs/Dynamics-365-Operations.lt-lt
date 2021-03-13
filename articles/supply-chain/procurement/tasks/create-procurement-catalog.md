---
title: Įsigijimo katalogo kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo eigą.
author: RichardLuan
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaf8b8d8b369aa704344d6984a0f111af6e4285b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016482"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="d48e6-103">Įsigijimo katalogo kūrimas</span><span class="sxs-lookup"><span data-stu-id="d48e6-103">Create a procurement catalog</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d48e6-104">Šioje temoje aiškinama, kaip sukurti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="d48e6-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="d48e6-105">Šią užduotį paprastai atlieka įsigijimo specialistas.</span><span class="sxs-lookup"><span data-stu-id="d48e6-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="d48e6-106">Taip pat sužinosite, kaip kurdami paraišką darbuotojai gali naudoti katalogą.</span><span class="sxs-lookup"><span data-stu-id="d48e6-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="d48e6-107">Prieš kuriant katalogą, sistemoje turi būti nustatyta įsigijimo kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="d48e6-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="d48e6-108">Naujas katalogas perima hierarchiją ir visus hierarchijos produktus.</span><span class="sxs-lookup"><span data-stu-id="d48e6-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="d48e6-109">Šį vedlį galite naudoti demonstracinių duomenų įmonėje USMF, kurioje įgalinta įsigijimo kategorijų hierarchija, taip pat procedūros veiksmų pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="d48e6-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="d48e6-110">Įsitikinkite, kad įsigijimo kategorijų hierarchija nustatyta</span><span class="sxs-lookup"><span data-stu-id="d48e6-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="d48e6-111">Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir šaltiniai > Įsigijimo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="d48e6-112">Demonstracinių duomenų įmonėje USMF galima naudoti įsigijimo kategorijų hierarchiją, be to, produktai yra įtraukti į kategoriją **Biuro mašinos arba kompiuteriai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="d48e6-113">Jei šią procedūrą vykdote kaip užduočių vedlį, turėsite jį atrakinti, kad galėtumėte naršyti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="d48e6-113">If you're running this procedure as a task guide, you'll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="d48e6-114">Jei hierarchija nesukurta, galite ją kurti spustelėdami **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-114">If a hierarchy was not available, you'd create it by clicking **New**.</span></span> <span data-ttu-id="d48e6-115">Tai galima atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="d48e6-115">This can only be done once.</span></span>  
2. <span data-ttu-id="d48e6-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d48e6-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="d48e6-117">Katalogo kūrimas</span><span class="sxs-lookup"><span data-stu-id="d48e6-117">Create a catalog</span></span>
1. <span data-ttu-id="d48e6-118">Pasirinkite **Naršymo sritis > Moduliai > įsigijimas ir šaltinio pasirinkimas > Katalogai > Įsigijimo katalogai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="d48e6-119">Spustelėdami **Naujas įsigijimo katalogas** atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="d48e6-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="d48e6-120">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d48e6-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d48e6-121">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-121">Select **OK**.</span></span>
5. <span data-ttu-id="d48e6-122">Medyje išplėskite **CORP ĮSIGIJIMO KATEGORIJOS**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="d48e6-123">Medyje išplėskite **BIURO MAŠINOS**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="d48e6-124">Medyje pasirinkite **Kompiuteriai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="d48e6-125">Sąraše rodomi įsigijimo kategorijos produktai.</span><span class="sxs-lookup"><span data-stu-id="d48e6-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="d48e6-126">Jei į kategoriją norite įtraukti produktą, tai turite atlikti puslapyje **Įsigijimo kategorijų hierarchija** arba puslapyje **Prekės informacija**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="d48e6-127">**Numatytasis** naujinimo tipas nustato, ar nauji į įsigijimo kategorijų hierarchiją įtraukti produktai yra iš karto matomi kataloge.</span><span class="sxs-lookup"><span data-stu-id="d48e6-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="d48e6-128">Jei naujinimo tipas nustatytas kaip **Dinamiškas**, keitimai matomi iš karto.</span><span class="sxs-lookup"><span data-stu-id="d48e6-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="d48e6-129">Jei naujinimo tipas nustatytas kaip **Statinis**, katalogą naudojantys asmenys naujus produktus matys tik tada, kai katalogas bus iš naujo publikuotas.</span><span class="sxs-lookup"><span data-stu-id="d48e6-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="d48e6-130">Veiksmas **Publikuoti** pateikiamas puslapio viršuje esančioje veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="d48e6-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="d48e6-131">Jei produktai pašalinami iš įsigijimo kategorijų hierarchijos, pakeitimas matomas iš karto, neatsižvelgiant į lauko **Numatytasis** naujinimo tipas reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d48e6-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="d48e6-132">Veiksmų srityje pasirinkite **Kategorijos naršymas** ir įsitikinkite, kad pasirinkta parinktis **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="d48e6-133">Pasirinkite **Suaktyvinti katalogą**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="d48e6-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d48e6-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="d48e6-135">Nustatyti katalogą kaip matomą</span><span class="sxs-lookup"><span data-stu-id="d48e6-135">Make the catalog visible</span></span>
1. <span data-ttu-id="d48e6-136">Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="d48e6-137">Pasirinkite **Įsigijimo strategijos USMF**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="d48e6-138">Turite pasirinkti juridinio subjekto pirkimo strategiją, pagal kurią su jūsų vartotojo profilių susietas darbuotojas gali užsakyti produktus.</span><span class="sxs-lookup"><span data-stu-id="d48e6-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="d48e6-139">USMF demonstraciniuose duomenyse vartotojas administratorius yra susietas su darbuotoja, vardu **Julia Funderburk**, ir ji USMF produktus užsako pagal numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="d48e6-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="d48e6-140">Pasirinkite katalogą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="d48e6-140">Select the catalog that you've just created.</span></span>
4. <span data-ttu-id="d48e6-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="d48e6-142">Naudoti katalogą</span><span class="sxs-lookup"><span data-stu-id="d48e6-142">Use the catalog</span></span>
1. <span data-ttu-id="d48e6-143">Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo paraiškos > Visos pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="d48e6-144">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-144">Select **New**.</span></span>
3. <span data-ttu-id="d48e6-145">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d48e6-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="d48e6-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-146">Select **OK**.</span></span>
5. <span data-ttu-id="d48e6-147">Pasirinkite **Įtraukti produktus**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-147">Select **Add products**.</span></span>
6. <span data-ttu-id="d48e6-148">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d48e6-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="d48e6-149">Norėdami filtruoti produktus, galite naudoti kategorijų hierarchiją sąrašo kairėje pusėje arba filtrą sąrašo viršuje.</span><span class="sxs-lookup"><span data-stu-id="d48e6-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="d48e6-150">Pasirinkite **Įtraukti į eilutes**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="d48e6-151">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d48e6-151">Select **OK**.</span></span>

