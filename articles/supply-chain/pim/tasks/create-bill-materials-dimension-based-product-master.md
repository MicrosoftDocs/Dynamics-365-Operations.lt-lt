---
title: Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas
description: Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0db1c35779a468d9a86d18eb6c849d40bc8c03a3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820087"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="bcac8-103">Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="bcac8-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcac8-104">Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus.</span><span class="sxs-lookup"><span data-stu-id="bcac8-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="bcac8-105">Pirmaisiais 4 įrašais nustatomi duomenys, kurių reikia norint atlikti šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="bcac8-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="bcac8-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="bcac8-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bcac8-107">Šią užduotį paprastai atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="bcac8-108">Produkto pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="bcac8-108">Select the product</span></span>
1. <span data-ttu-id="bcac8-109">Spustelėkite Patvirtinto produkto priežiūra.</span><span class="sxs-lookup"><span data-stu-id="bcac8-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="bcac8-110">Spustelėkite Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="bcac8-110">Click Released products.</span></span>
3. <span data-ttu-id="bcac8-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bcac8-112">Raskite išleistą bendrąjį produktą su konfigūravimo pagal dimensijas technologija, kurį sukūrėte pirmajame šios sekos užduočių vadove.</span><span class="sxs-lookup"><span data-stu-id="bcac8-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="bcac8-113">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="bcac8-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="bcac8-114">Spustelėkite KS versijos.</span><span class="sxs-lookup"><span data-stu-id="bcac8-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="bcac8-115">Naujos KS ir KS versijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="bcac8-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="bcac8-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-116">Click New.</span></span>
2. <span data-ttu-id="bcac8-117">Spustelėkite KS ir KS versija.</span><span class="sxs-lookup"><span data-stu-id="bcac8-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="bcac8-118">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bcac8-119">Vietos nustatymas</span><span class="sxs-lookup"><span data-stu-id="bcac8-119">Setting a site</span></span>  
    * <span data-ttu-id="bcac8-120">Atlikdami šią procedūrą konkrečios KS vietos nenustatome.</span><span class="sxs-lookup"><span data-stu-id="bcac8-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="bcac8-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bcac8-121">Click OK.</span></span>
5. <span data-ttu-id="bcac8-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-122">Click New.</span></span>
    * <span data-ttu-id="bcac8-123">Atlikdami šią procedūrą, į KS įtrauksime keturias eilutes.</span><span class="sxs-lookup"><span data-stu-id="bcac8-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="bcac8-124">Dviejose eilutėse nurodomos laidų parinktys ir dviejose eilutėse nurodomos spintelių parinktys.</span><span class="sxs-lookup"><span data-stu-id="bcac8-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="bcac8-125">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="bcac8-126">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-127">Pasirinkite prekės numerį A0001, HDMI 6 pėd. laidai.</span><span class="sxs-lookup"><span data-stu-id="bcac8-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="bcac8-128">Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-129">Pasirinkite laidų konfigūracijos grupę, sukurtą 4-ajame šios sekos vadove.</span><span class="sxs-lookup"><span data-stu-id="bcac8-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="bcac8-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-130">Click New.</span></span>
    * <span data-ttu-id="bcac8-131">Pasirinkite prekės numerį A0002, HDMI 12 pėd. laidai.</span><span class="sxs-lookup"><span data-stu-id="bcac8-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="bcac8-132">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="bcac8-133">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="bcac8-134">Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-135">Vėl pasirinkite laidų konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="bcac8-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-136">Click New.</span></span>
14. <span data-ttu-id="bcac8-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="bcac8-138">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-139">Pasirinkite prekės numerį D0002 Spintelė.</span><span class="sxs-lookup"><span data-stu-id="bcac8-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="bcac8-140">Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-141">Pasirinkite šios KS eilutės spintelių konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="bcac8-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bcac8-142">Click New.</span></span>
18. <span data-ttu-id="bcac8-143">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="bcac8-144">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-145">Kaip paskutinę KS eilutę pasirinkite prekės numerį M0007 StandartinėSpintelė.</span><span class="sxs-lookup"><span data-stu-id="bcac8-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="bcac8-146">Lauke Konfigūracijos grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bcac8-147">Pasirinkite paskutinės KS eilutės spintelių konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="bcac8-148">Patvirtinti ir aktyvinti</span><span class="sxs-lookup"><span data-stu-id="bcac8-148">Approve and activate</span></span>
1. <span data-ttu-id="bcac8-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bcac8-149">Close the page.</span></span>
2. <span data-ttu-id="bcac8-150">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="bcac8-150">Click Approve.</span></span>
3. <span data-ttu-id="bcac8-151">Lauke Patvirtino įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="bcac8-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="bcac8-152">Lange Ar norite patvirtinti ir KS? pasirinkite Taip. nurodytas operacijos numeris.</span><span class="sxs-lookup"><span data-stu-id="bcac8-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="bcac8-153">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bcac8-153">Click OK.</span></span>
6. <span data-ttu-id="bcac8-154">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="bcac8-154">Click Activate.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]