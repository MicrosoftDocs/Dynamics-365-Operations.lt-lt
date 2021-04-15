---
title: Prekiaujančių subjektų rūšiavimo tvarkos keitimas
description: Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799474"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="5b916-103">Prekiaujančių subjektų rūšiavimo tvarkos keitimas</span><span class="sxs-lookup"><span data-stu-id="5b916-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5b916-104">Pardavėjai produktų atradimą laiko pirminiu įrankiu, skirtu bendrauti su klientais visuose kanaluose.</span><span class="sxs-lookup"><span data-stu-id="5b916-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="5b916-105">Įvairios funkcijos gali padėti klientams lengviau atrasti produktus.</span><span class="sxs-lookup"><span data-stu-id="5b916-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="5b916-106">Pavyzdžiui, jie gali naršyti po kategorijas, ieškoti ir filtruoti.</span><span class="sxs-lookup"><span data-stu-id="5b916-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="5b916-107">Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu.</span><span class="sxs-lookup"><span data-stu-id="5b916-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="5b916-108">Čia taip pat aiškinama, kaip pakeisti rūšiavimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="5b916-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="5b916-109">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="5b916-109">Overview</span></span>

<span data-ttu-id="5b916-110">Patobulinta įvairių su prekybą susijusių subjektų rūšiavimo pagalba.</span><span class="sxs-lookup"><span data-stu-id="5b916-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="5b916-111">Ši pagalba dabar geriau suderinta su esamais klientų scenarijais, kuriems seniau reikėjo plėtinių iš diegimo partnerių.</span><span class="sxs-lookup"><span data-stu-id="5b916-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="5b916-112">Senesnėse nei 10.0.5 „Retail” versijose kategorijų rūšiavimas naršymo hierarchijoje buvo alfabetinis.</span><span class="sxs-lookup"><span data-stu-id="5b916-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="5b916-113">Naujos pasirinktinės rūšiavimo tvarkos funkcijos leidžia prekybos vadybininkams konfigūruoti įvairių su prekyba susijusių subjektų tvarką visuose galutiniuose klientuose.</span><span class="sxs-lookup"><span data-stu-id="5b916-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="5b916-114">Šiuos klientus sudaro centrinės būstinės (HQ) ir skambučių centrai.</span><span class="sxs-lookup"><span data-stu-id="5b916-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="5b916-115">Produktų hierarchijos kategorijų rodymo tvarkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b916-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="5b916-116">Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="5b916-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="5b916-117">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Prekybos produktų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="5b916-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="5b916-118">Spustelėkite **Redaguoti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="5b916-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="5b916-119">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="5b916-119">Click **Edit**.</span></span>
4. <span data-ttu-id="5b916-120">Medyje išplėskite **VISI \> Veiksmo sportas**.</span><span class="sxs-lookup"><span data-stu-id="5b916-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="5b916-121">Medyje išplėskite **VISI \> Komandinis sportas**.</span><span class="sxs-lookup"><span data-stu-id="5b916-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="5b916-122">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b916-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="5b916-123">(Skaičius gali būti neigiamas)</span><span class="sxs-lookup"><span data-stu-id="5b916-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="5b916-124">Bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti, pakartokite 4–6 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5b916-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="5b916-125">Kanalo naršymo hierarchijos rodymo tvarka atsispindės prekybos produktų hierarchijos HQ ir pagal kategoriją išleistuose produktuose.</span><span class="sxs-lookup"><span data-stu-id="5b916-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Produktų hierarchijos pasirinktinis rūšiavimas su neigiamomis reikšmėmis](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Pagal kategoriją išleistų produktų pasirinktinis rūšiavimas pagal produktų hierarchiją](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="5b916-128">Kategorijų kanalo naršymo hierarchijoje rodymo tvarkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b916-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="5b916-129">Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="5b916-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="5b916-130">Eikite į **Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="5b916-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="5b916-131">Sąraše pažymėkite hierarchiją **Mados naršymas**.</span><span class="sxs-lookup"><span data-stu-id="5b916-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="5b916-132">Spustelėkite **Redaguoti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="5b916-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="5b916-133">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="5b916-133">Click **Edit**.</span></span>
5. <span data-ttu-id="5b916-134">Medyje pažymėkite **Mada \> Drabužiai moterims \> Batai moterims**.</span><span class="sxs-lookup"><span data-stu-id="5b916-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="5b916-135">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b916-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="5b916-136">Medyje pažymėkite **Mada \> Drabužiai moterims \> Viršutiniai drabužiai**.</span><span class="sxs-lookup"><span data-stu-id="5b916-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="5b916-137">Panašiai galite apibrėžti rūšiavimo tvarką antrinėse kategorijose.</span><span class="sxs-lookup"><span data-stu-id="5b916-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="5b916-138">Medyje pažymėkite **Mada \> Drabužiai vyrams \> Laisvalaikio marškinėliai**.</span><span class="sxs-lookup"><span data-stu-id="5b916-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="5b916-139">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b916-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="5b916-140">Medyje pažymėkite **Mada \> Drabužiai vyrams \> Paltai ir švarkai**.</span><span class="sxs-lookup"><span data-stu-id="5b916-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="5b916-141">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5b916-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="5b916-142">Šiuos veiksmus pakartokite bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="5b916-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="5b916-143">Kanalo naršymo hierarchijos rodymo tvarka atsispindi HQ, kataloge ir kanaluose.</span><span class="sxs-lookup"><span data-stu-id="5b916-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Kanalo naršymo hierarchijos pasirinktinis rūšiavimas](./media/ChannelNavCustomSorted.png)

![Katalogo naršymo hierarchijos pasirinktis rūšiavimas pagal kanalo naršymo hierarchiją](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS su pasirinktai surūšiuotomis kategorijomis](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="5b916-147">Pagal numatytuosius parametrus, pasirinktinio rūšiavimo tvarka yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="5b916-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="5b916-148">Kaip įjungti šią funkciją ir kitas funkcijas, žr. [Funkcijų valdymas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="5b916-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]