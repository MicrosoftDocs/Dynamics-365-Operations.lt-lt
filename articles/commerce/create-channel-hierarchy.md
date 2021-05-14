---
title: Kanalo naršymo hierarchijos kūrimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951913"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="c8694-103">Kanalų naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8694-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c8694-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="c8694-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8694-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="c8694-105">Overview</span></span>

<span data-ttu-id="c8694-106">Kanalo naršymo hierarchija naudojama, norint grupuoti ir skirstyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="c8694-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="c8694-107">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8694-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="c8694-108">Norėdami sukurti kanalo naršymo hierarchiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8694-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c8694-109">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="c8694-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="c8694-110">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c8694-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8694-111">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8694-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="c8694-112">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="c8694-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="c8694-113">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-113">Select **Create**.</span></span>
1. <span data-ttu-id="c8694-114">Veiksmų srityje pasirinkę **Naujas kategorijos mazgas**, sukurkite šakninį mazgą.</span><span class="sxs-lookup"><span data-stu-id="c8694-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="c8694-115">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8694-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="c8694-116">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="c8694-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="c8694-117">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8694-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="c8694-118">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8694-119">Toliau pateiktame vaizde parodytas šakninio mazgo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c8694-119">The following image shows a example root node.</span></span>

![Šakninio mazgo pavyzdys](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="c8694-121">Naršymo kategorijos mazgų kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8694-121">Create navigation category nodes</span></span>

<span data-ttu-id="c8694-122">Norėdami sukurti papildomų naršymo kategorijos mazgų, nurodančių kanalo produktų kategorijas, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8694-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="c8694-123">Naršymo srityje pasirinkite pirminį mazgą, į kurį norite įtraukti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="c8694-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="c8694-124">Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.</span><span class="sxs-lookup"><span data-stu-id="c8694-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="c8694-125">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8694-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="c8694-126">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="c8694-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="c8694-127">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8694-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="c8694-128">Langelyje **Rodymo tvarka** įveskite rodymo tvarką (nebūtina).</span><span class="sxs-lookup"><span data-stu-id="c8694-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="c8694-129">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8694-130">Toliau pateiktame vaizde parodytas baigtos kanalo naršymo hierarchijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c8694-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanalo hierarchijos pavyzdys](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="c8694-132">Produktų įtraukimas į kategorijų mazgus</span><span class="sxs-lookup"><span data-stu-id="c8694-132">Add products to category nodes</span></span>

<span data-ttu-id="c8694-133">Norėdami įtraukti produktus į kategorijų mazgus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8694-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="c8694-134">Pasirinkite kategorijos mazgą.</span><span class="sxs-lookup"><span data-stu-id="c8694-134">Select a category node.</span></span>
1. <span data-ttu-id="c8694-135">Srityje **Produktai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="c8694-136">Raskite naują (-ų) produktą (-ų), kurį (-iuos) norite įtraukti pagal produkto numerį arba produkto pavadinimą, ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c8694-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="c8694-137">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="c8694-138">Įtraukti produktus į mazgą kanalo naršymo hierarchijoje nepakanka, kad produktai būtų rodomi pasirinktame kanale, produktus taip pat reikia pateikti pagal produktą.</span><span class="sxs-lookup"><span data-stu-id="c8694-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="c8694-139">Daugiau informacijos apie asortimentus ieškokite [asortimento](assortments.md) valdymas.</span><span class="sxs-lookup"><span data-stu-id="c8694-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="c8694-140">Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktais produktais.</span><span class="sxs-lookup"><span data-stu-id="c8694-140">The following image shows an example node with products added.</span></span>

![Produktai, įtraukti į kategorijos mazgą](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="c8694-142">Produktų atributų grupių įtraukimas į kategorijų mazgus</span><span class="sxs-lookup"><span data-stu-id="c8694-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="c8694-143">Atributų grupes būtina sukurti prieš jas įtraukiant į mazgą kanalo naršymo hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="c8694-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="c8694-144">Norėdami įtraukti produkto atributo grupę į kategorijos mazgą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8694-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="c8694-145">Pasirinkite kategorijos mazgą.</span><span class="sxs-lookup"><span data-stu-id="c8694-145">Select a category node.</span></span>
1. <span data-ttu-id="c8694-146">Dalyje **Produkto atributo grupė** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="c8694-147">Suraskite įtrauktiną (-as) atributo (-ų) grupę (-es) ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c8694-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="c8694-148">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c8694-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8694-149">Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktomis produktų atributų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="c8694-149">The following image shows a sample node with product attribute groups added.</span></span>

![Produktų atributų grupės mazge](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="c8694-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c8694-151">Additional resources</span></span>

[<span data-ttu-id="c8694-152">Asortimentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="c8694-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="c8694-153">Atributų ir atributų grupių tvarkymas</span><span class="sxs-lookup"><span data-stu-id="c8694-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
