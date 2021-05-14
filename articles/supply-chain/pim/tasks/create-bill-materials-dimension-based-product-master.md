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
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920710"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="bc7f4-103">Dimensijomis paremto bendrojo produkto komplektavimo specifikacijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="bc7f4-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc7f4-104">Norėdami atlikti šią procedūrą, turite būti atlikę ankstesnius 4 šios aštuonių įrašų sekos vadovus.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="bc7f4-105">Pirmaisiais 4 įrašais nustatomi duomenys, kurių reikia norint atlikti šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="bc7f4-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bc7f4-107">Šią užduotį paprastai atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="bc7f4-108">Produkto pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="bc7f4-108">Select the product</span></span>

1. <span data-ttu-id="bc7f4-109">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="bc7f4-110">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bc7f4-111">Raskite išleistą bendrąjį produktą su konfigūravimo pagal dimensijas technologija, kurį sukūrėte pirmajame šios sekos užduočių vadove.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="bc7f4-112">Veiksmų srityje pasirinkite **Inžinierius**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="bc7f4-113">Pasirinkti **BOM versijas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="bc7f4-114">Naujos KS ir KS versijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="bc7f4-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="bc7f4-115">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-115">Select **New**.</span></span>
1. <span data-ttu-id="bc7f4-116">Pasirinkite **BOM ir BOM** versiją.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="bc7f4-117">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="bc7f4-118">Vietos nustatymas</span><span class="sxs-lookup"><span data-stu-id="bc7f4-118">Setting a site</span></span>  
    * <span data-ttu-id="bc7f4-119">Atlikdami šią procedūrą konkrečios KS vietos nenustatome.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="bc7f4-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-120">Select **OK**.</span></span>
1. <span data-ttu-id="bc7f4-121">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-121">Select **New**.</span></span>
    * <span data-ttu-id="bc7f4-122">Atlikdami šią procedūrą, į KS įtrauksime keturias eilutes.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="bc7f4-123">Dviejose eilutėse nurodomos laidų parinktys ir dviejose eilutėse nurodomos spintelių parinktys.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="bc7f4-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bc7f4-125">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-126">Pasirinkite prekės numerį A0001, HDMI 6 pėd. laidai.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="bc7f4-127">Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-128">Pasirinkite laido konfigūracijos grupę, sukurtą 4-ajame šios sekos vadove.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="bc7f4-129">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-129">Select **New**.</span></span>
    * <span data-ttu-id="bc7f4-130">Pasirinkite prekės numerį A0002, HDMI 12 pėd. laidai.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="bc7f4-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bc7f4-132">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="bc7f4-133">Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-134">Vėl pasirinkite laido konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="bc7f4-135">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-135">Select **New**.</span></span>
1. <span data-ttu-id="bc7f4-136">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bc7f4-137">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-138">Pasirinkite prekės numerį D0002 Spintelė.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="bc7f4-139">Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-140">Pasirinkite spintos konfigūracijos grupę šiai BOM eilutei.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="bc7f4-141">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-141">Select **New**.</span></span>
1. <span data-ttu-id="bc7f4-142">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bc7f4-143">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-144">Kaip paskutinę KS eilutę pasirinkite prekės numerį M0007 StandartinėSpintelė.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="bc7f4-145">Lauke **Konfigūracijos grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bc7f4-146">Pasirinkite paskutinės BOM eilutės spintelių konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="bc7f4-147">Patvirtinti ir aktyvinti</span><span class="sxs-lookup"><span data-stu-id="bc7f4-147">Approve and activate</span></span>

1. <span data-ttu-id="bc7f4-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-148">Close the page.</span></span>
1. <span data-ttu-id="bc7f4-149">Pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-149">Select **Approve**.</span></span>
1. <span data-ttu-id="bc7f4-150">Lauke **Patvirtino** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="bc7f4-151">Rinkitės *Taip* laukelyje **Ar norite patvirtinti ir medžiagų važtaraštį?**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="bc7f4-152">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-152">Select **OK**.</span></span>
1. <span data-ttu-id="bc7f4-153">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="bc7f4-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]