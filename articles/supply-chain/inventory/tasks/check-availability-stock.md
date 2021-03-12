---
title: Tikrinti turimas atsargas
description: Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas.
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d04abae36e144b429b8ebc73b4c110389fecd1f0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000164"
---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="d404e-103">Tikrinti turimas atsargas</span><span class="sxs-lookup"><span data-stu-id="d404e-103">Check the availability of stock</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d404e-104">Ši procedūra parodo, kaip patikrinti konkretaus prekės numerio turimas ir faktinies turimas atsargas.</span><span class="sxs-lookup"><span data-stu-id="d404e-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="d404e-105">Ji taip pat parodo, kaip gauti tiekimo informacijos, susijusios su preke.</span><span class="sxs-lookup"><span data-stu-id="d404e-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="d404e-106">Faktinės turimos atsargos yra turimos atsargos, kurios yra prieinamos – t. y., nupirktos, gautos ir užregistruotos.</span><span class="sxs-lookup"><span data-stu-id="d404e-106">Physical on-hand inventory is the on-hand inventory that's available – that is, it's purchased, received and registered.</span></span> <span data-ttu-id="d404e-107">Turimos atsargos apima ne tik prieinamas turimas atsargas, bet ir atsargas, kurios užsakytos ir laukiamos, bet dar nėra gautos ar registruotos.</span><span class="sxs-lookup"><span data-stu-id="d404e-107">On-hand inventory includes the available on-hand inventory, but also the inventory that's been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="d404e-108">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="d404e-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="d404e-109">Jei naudojate USMF, galite naudoti rodomas pavyzdines reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d404e-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="d404e-110">Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="d404e-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="d404e-111">Patikrinti turimas prekės atsargas</span><span class="sxs-lookup"><span data-stu-id="d404e-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="d404e-112">Eikite į **Naršymo sritis > Moduliai > Atsargų valdymas > Užklausos ir ataskaitos > Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="d404e-112">Go to **Navigation pane > Modules > Inventory management > Inquiries and reports > On-hand inventory**.</span></span>
2. <span data-ttu-id="d404e-113">Pasirinkti eilutę **Prekių skaičius**.</span><span class="sxs-lookup"><span data-stu-id="d404e-113">Select the **Item number** row.</span></span> <span data-ttu-id="d404e-114">Norėdami teikti užklausą dėl turimų atsargų pagal prekės numerį, pasirinkite eilutę, kurioje lentelė nustatyta į **Turimos atsargos**, o laukas nustatytas į **Prekės** numeris.</span><span class="sxs-lookup"><span data-stu-id="d404e-114">To query the on-hand inventory by item number, select the row where the Table is set to **On-hand inventory** and Field is set to **Item** number.</span></span>
3. <span data-ttu-id="d404e-115">Lauke **Kriterijai** pasirinkite prekę, dėl kurios norite pateikti užklausą.</span><span class="sxs-lookup"><span data-stu-id="d404e-115">In the **Criteria** field, select the item you want to query.</span></span> <span data-ttu-id="d404e-116">Jei naudojate demonstracinių duomenų įmonę USMF, galite pasirinkti „M9201‟.</span><span class="sxs-lookup"><span data-stu-id="d404e-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="d404e-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d404e-117">Click **OK**.</span></span>
5. <span data-ttu-id="d404e-118">**Veiksmų srityje** spustelėkite **Dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="d404e-118">On the **Action Pane**, click **Dimensions**.</span></span> <span data-ttu-id="d404e-119">Skirtukas **Dimensijos** leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti.</span><span class="sxs-lookup"><span data-stu-id="d404e-119">The **Dimensions** tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="d404e-120">Jei reikia duomenų, susijusių su rezervavimu, turite vaizduoti visas prekių, naudojančių patobulintus sandėlio (WMS) procesus, atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d404e-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WMS) processes.</span></span>
6. <span data-ttu-id="d404e-121">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d404e-121">Click **OK**.</span></span>
7. <span data-ttu-id="d404e-122">**Veiksmų srityje** spustelėkite **Susijusi informacija**.</span><span class="sxs-lookup"><span data-stu-id="d404e-122">On the **Action Pane**, click **Related information**.</span></span> <span data-ttu-id="d404e-123">Jei tokios parinkties nematote, gali reikėti spustelėti ant elipsės mygtuko (...), kad matytumėte papildomų veiksmų srities parinkčių.</span><span class="sxs-lookup"><span data-stu-id="d404e-123">If you don't see this option, you may need to click on the Ellipsis button (…) to see additional Action Pane options.</span></span>
8. <span data-ttu-id="d404e-124">Spustelėkite **Tiekimo apžvalga**.</span><span class="sxs-lookup"><span data-stu-id="d404e-124">Click **Supply overview**.</span></span> <span data-ttu-id="d404e-125">Skirtuke **Tiekimo apžvalga** pateikiama konkrečios prekės tiekimo informacija, pvz., turimas kiekis, gamybos laikas ir tiekėjo informacija.</span><span class="sxs-lookup"><span data-stu-id="d404e-125">The **Supply overview** tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="d404e-126">Išplėskite sekciją **Turimas kiekis**.</span><span class="sxs-lookup"><span data-stu-id="d404e-126">Expand the **On-hand** section.</span></span>
10. <span data-ttu-id="d404e-127">Išplėskite skyrių **Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="d404e-127">Expand the **Vendors** section.</span></span>
11. <span data-ttu-id="d404e-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-128">Close the page.</span></span>
12. <span data-ttu-id="d404e-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="d404e-130">Tikrinti faktines turimas atsargas</span><span class="sxs-lookup"><span data-stu-id="d404e-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="d404e-131">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Užklausos ir ataskaitos > Faktinės turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="d404e-131">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > Physical on-hand inventory**.</span></span>
2. <span data-ttu-id="d404e-132">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="d404e-132">In the **Item number** field, type a value.</span></span> <span data-ttu-id="d404e-133">Galite naudoti laukus Teritorija ir Sandėlis, kad filtruotumėte prekių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d404e-133">You can use the Site and Warehouse fields to filter the list of items.</span></span> 
3. <span data-ttu-id="d404e-134">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-134">Refresh the page.</span></span>
4. <span data-ttu-id="d404e-135">**Veiksmų srityje** spustelėkite **Rodyti dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="d404e-135">On the **Action Pane**, click **Display Dimensions**.</span></span> <span data-ttu-id="d404e-136">Skirtukas Dimensijų rodymas leidžia pasirinkti, kiek informacijos apie turimas atsargas norite matyti.</span><span class="sxs-lookup"><span data-stu-id="d404e-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>
5. <span data-ttu-id="d404e-137">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d404e-137">Click **OK**.</span></span>
6. <span data-ttu-id="d404e-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="d404e-139">Tikrinti turimas atsargas pagal vietą</span><span class="sxs-lookup"><span data-stu-id="d404e-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="d404e-140">Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Užklausos ir ataskaitos > Turimos atsargos pagal vietą**.</span><span class="sxs-lookup"><span data-stu-id="d404e-140">Go to **Navigation pane > Modules > Warehouse management > Inquiries and reports > On hand by location**.</span></span>
2. <span data-ttu-id="d404e-141">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d404e-141">In the **Warehouse** field, type a value.</span></span> <span data-ttu-id="d404e-142">Jei naudojate demonstracinių duomenų įmonę USMF, galite naudoti „51‟.</span><span class="sxs-lookup"><span data-stu-id="d404e-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="d404e-143">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-143">Refresh the page.</span></span>
4. <span data-ttu-id="d404e-144">Spustelėkite **Rodyti dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="d404e-144">Click **Display Dimensions**.</span></span>
5. <span data-ttu-id="d404e-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d404e-145">Click **OK**.</span></span>
6. <span data-ttu-id="d404e-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d404e-146">Close the page.</span></span>

