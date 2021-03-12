---
title: Kanalo naršymo hierarchijos kūrimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972987"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="90792-103">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="90792-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="90792-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="90792-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="90792-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="90792-105">Overview</span></span>

<span data-ttu-id="90792-106">Kanalo naršymo hierarchija naudojama, norint grupuoti ir skirstyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="90792-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="90792-107">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="90792-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="90792-108">Norėdami sukurti kanalo naršymo hierarchiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="90792-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="90792-109">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="90792-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="90792-110">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="90792-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="90792-111">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="90792-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90792-112">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="90792-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90792-113">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="90792-113">Select **Create**.</span></span>
1. <span data-ttu-id="90792-114">Veiksmų srityje pasirinkę **Naujas kategorijos mazgas**, sukurkite šakninį mazgą.</span><span class="sxs-lookup"><span data-stu-id="90792-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="90792-115">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="90792-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90792-116">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="90792-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90792-117">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="90792-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="90792-118">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="90792-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90792-119">Toliau pateiktame vaizde parodytas šakninio mazgo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="90792-119">The following image shows a example root node.</span></span>

![Šakninio mazgo pavyzdys](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="90792-121">Naršymo kategorijos mazgų kūrimas</span><span class="sxs-lookup"><span data-stu-id="90792-121">Create navigation category nodes</span></span>

<span data-ttu-id="90792-122">Norėdami sukurti papildomų naršymo kategorijos mazgų, nurodančių kanalo produktų kategorijas, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="90792-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="90792-123">Naršymo srityje pasirinkite pirminį mazgą, į kurį norite įtraukti kategoriją.</span><span class="sxs-lookup"><span data-stu-id="90792-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="90792-124">Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.</span><span class="sxs-lookup"><span data-stu-id="90792-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="90792-125">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="90792-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90792-126">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="90792-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90792-127">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="90792-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="90792-128">Langelyje **Rodymo tvarka** įveskite rodymo tvarką (nebūtina).</span><span class="sxs-lookup"><span data-stu-id="90792-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="90792-129">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="90792-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90792-130">Toliau pateiktame vaizde parodytas baigtos kanalo naršymo hierarchijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="90792-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanalo hierarchijos pavyzdys](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="90792-132">Produktų įtraukimas į kategorijų mazgus</span><span class="sxs-lookup"><span data-stu-id="90792-132">Add products to category nodes</span></span>

<span data-ttu-id="90792-133">Norėdami įtraukti produktus į kategorijų mazgus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="90792-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="90792-134">Pasirinkite kategorijos mazgą.</span><span class="sxs-lookup"><span data-stu-id="90792-134">Select a category node.</span></span>
1. <span data-ttu-id="90792-135">Srityje **Produktai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="90792-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="90792-136">Raskite naują (-ų) produktą (-ų), kurį (-iuos) norite įtraukti pagal produkto numerį arba produkto pavadinimą, ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="90792-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="90792-137">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="90792-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="90792-138">Įtraukti produktus į mazgą kanalo naršymo hierarchijoje nepakanka, kad produktai būtų rodomi pasirinktame kanale, produktus taip pat reikia pateikti pagal produktą.</span><span class="sxs-lookup"><span data-stu-id="90792-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="90792-139">Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktais produktais.</span><span class="sxs-lookup"><span data-stu-id="90792-139">The following image shows an example node with products added.</span></span>

![Produktai, įtraukti į kategorijos mazgą](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="90792-141">Produktų atributų grupių įtraukimas į kategorijų mazgus</span><span class="sxs-lookup"><span data-stu-id="90792-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="90792-142">Atributų grupes būtina sukurti prieš jas įtraukiant į mazgą kanalo naršymo hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="90792-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="90792-143">Norėdami įtraukti produkto atributo grupę į kategorijos mazgą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="90792-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="90792-144">Pasirinkite kategorijos mazgą.</span><span class="sxs-lookup"><span data-stu-id="90792-144">Select a category node.</span></span>
1. <span data-ttu-id="90792-145">Dalyje **Produkto atributo grupė** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="90792-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="90792-146">Suraskite įtrauktiną (-as) atributo (-ų) grupę (-es) ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="90792-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="90792-147">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="90792-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90792-148">Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktomis produktų atributų grupėmis.</span><span class="sxs-lookup"><span data-stu-id="90792-148">The following image shows a sample node with product attribute groups added.</span></span>

![Produktų atributų grupės mazge](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="90792-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="90792-150">Additional resources</span></span>

[<span data-ttu-id="90792-151">Asortimentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="90792-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="90792-152">Atributų ir atributų grupių tvarkymas</span><span class="sxs-lookup"><span data-stu-id="90792-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)
