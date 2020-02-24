---
title: Naujo produkto kūrimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produktą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001972"
---
# <a name="create-a-new-product"></a><span data-ttu-id="02ce4-103">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="02ce4-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produktą.</span><span class="sxs-lookup"><span data-stu-id="02ce4-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="02ce4-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="02ce4-105">Overview</span></span>

<span data-ttu-id="02ce4-106">Produktą pirmiausia apibrėžia produkto numeris, pavadinimas ir aprašas.</span><span class="sxs-lookup"><span data-stu-id="02ce4-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="02ce4-107">Tačiau, norint apibūdinti produktą ar paslaugą, taip pat būtini kiti duomenys:</span><span class="sxs-lookup"><span data-stu-id="02ce4-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="02ce4-108">Naujo produkto kūrimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-108">Create a new product</span></span>

1. <span data-ttu-id="02ce4-109">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Produktai pagal kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="02ce4-110">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="02ce4-111">Išplečiamajame sąraše **Produkto tipas** pasirinkite **Prekė** arba **Paslauga**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="02ce4-112">Išplečiamajame sąraše **Produkto potipis** pasirinkite **Produktas** (jei nebus produkto variantų) arba **Bendrasis produktas** (jei bus produkto variantų).</span><span class="sxs-lookup"><span data-stu-id="02ce4-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="02ce4-113">Langelyje **Produkto numeris** įveskite produkto numerį, jei jis nėra iš anksto užpildytas.</span><span class="sxs-lookup"><span data-stu-id="02ce4-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="02ce4-114">Langelyje **Produkto pavadinimas** įveskite produkto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="02ce4-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="02ce4-115">Langelyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="02ce4-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="02ce4-116">Išplečiamajame sąraše **Mažmeninės prekybos kategorija** pasirinkite reikiamą kategoriją.</span><span class="sxs-lookup"><span data-stu-id="02ce4-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="02ce4-117">Jei produktas yra rinkinys, pasirinkite **Taip** parinktyje **Produktų rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="02ce4-118">Jei produkto potipis yra bendrasis produktas, parinktyje **Produkto dimensijų grupė** nustatykite, kad būtų įtraukti palaikomi variantai.</span><span class="sxs-lookup"><span data-stu-id="02ce4-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="02ce4-119">Tarp parinkčių yra **Spalva**, **Dydis**, **Stilius** ir **Konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="02ce4-120">Jei reikia, gali reikėti sukurti papildomų produktų dimensijų grupių.</span><span class="sxs-lookup"><span data-stu-id="02ce4-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="02ce4-121">Išplečiamajame sąraše **Konfigūracijos technologija** pasirinkite reikiamą parinktį.</span><span class="sxs-lookup"><span data-stu-id="02ce4-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="02ce4-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-122">Select **OK**.</span></span>

<span data-ttu-id="02ce4-123">Toliau pateiktame vaizde parodytas įtraukiamas produkto pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="02ce4-123">The following image shows an example product being added.</span></span>

![Produkto kūrimas](media/create-new-product.png)

<span data-ttu-id="02ce4-125">Įtraukus produktą, galima nustatyti jo papildomus duomenis, pvz., **Produkto aprašas**, **Variantų grupės**, **Dimensijų grupės**, **Produkto atributai** ir **Susiję produktai**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="02ce4-126">Toliau pateiktame vaizde parodyta papildoma produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="02ce4-126">The following image shows a product's additional details.</span></span>

![Produkto informacija](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="02ce4-128">Kurti produkto variantus</span><span class="sxs-lookup"><span data-stu-id="02ce4-128">Create product variants</span></span>

<span data-ttu-id="02ce4-129">Jei produkto potipis yra **Bendrasis produktas**, reikės sukurti konkrečių variantų.</span><span class="sxs-lookup"><span data-stu-id="02ce4-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="02ce4-130">Norėdami sukurti produkto variantų, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="02ce4-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="02ce4-131">Veiksmų srityje pasirinkite **Produkto variantai**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="02ce4-132">Jei variantų grupės pasirinktos veiksmų srityje, pasirinkite \**Variantų pasiūlymai*.</span><span class="sxs-lookup"><span data-stu-id="02ce4-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="02ce4-133">Pasirinkite palaikytinus produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="02ce4-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="02ce4-134">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="02ce4-135">Produkto išleidimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-135">Release a product</span></span>

<span data-ttu-id="02ce4-136">Norint parduoti produktą, jis pirmiausia turi būti pateiktas juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="02ce4-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="02ce4-137">Produkto puslapyje pasirinkite **Išleisti produktus**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-137">From the product page, select **Release products**.</span></span>

    ![Produkto išleidimas](media/create-new-product-3.png)

1. <span data-ttu-id="02ce4-139">Pasirinkite išleistiną produktą, tada pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-139">Select the product to release, and then select **Next**.</span></span>

    ![Išleistino produkto pasirinkimas](media/create-new-product-4.png)

1. <span data-ttu-id="02ce4-141">Pasirinkite išleistinų produkto variantų rinkinį, tada pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Išleistinų variantų pasirinkimas](media/create-new-product-5.png)

1. <span data-ttu-id="02ce4-143">Pasirinkite juridinį subjektą ir pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-143">Select the legal entity, and then select **Next**.</span></span>

    ![Pasirinkite juridinį subjektą](media/create-new-product-6.png)

1. <span data-ttu-id="02ce4-145">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-145">Select **Finish**.</span></span>

    ![Produkto išleidimo užbaigimas](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="02ce4-147">Išleisto produkto konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-147">Configure a released product</span></span>

<span data-ttu-id="02ce4-148">Išleidus produktą, reikės jį papildomai konfigūruoti, įskaitant produkto kainos nustatymą.</span><span class="sxs-lookup"><span data-stu-id="02ce4-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="02ce4-149">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Išleisti produktai pagal kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="02ce4-150">Pasirinkite išleisto produkto kategorijos mazgą ir produktų sąraše pasirinkite produktą.</span><span class="sxs-lookup"><span data-stu-id="02ce4-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="02ce4-151">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="02ce4-152">Skyriuje **Pirkimas** sukonfigūruokite visas būtinas ypatybes, įskaitant **Vienetas**, **Kaina** ir **Kiekis**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="02ce4-153">Norėdami užtikrinti, kad nėra klaidos pranešimų apie trūkstamus laukus, veiksmų srityje pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="02ce4-154">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="02ce4-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="02ce4-155">Toliau pateiktame vaizde parodytas išleisto produkto konfigūracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="02ce4-155">The following image shows an example configuration for a released product.</span></span>

![Išleisto produkto konfigūravimas](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="02ce4-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="02ce4-157">Additional resources</span></span>

[<span data-ttu-id="02ce4-158">Juridinių subjektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="02ce4-159">Variantų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="02ce4-159">Create a variant group</span></span>](create-variant-group.md) 
