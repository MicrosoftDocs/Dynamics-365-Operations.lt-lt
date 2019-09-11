---
title: Prekiaujančių subjektų rūšiavimo tvarkos keitimas
description: Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu Microsoft Dynamics 365 for Retail.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866166"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="de309-103">Prekiaujančių subjektų rūšiavimo tvarkos keitimas</span><span class="sxs-lookup"><span data-stu-id="de309-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="de309-104">Mažmenininkai produkto atradimą laiko pirminiu įrankiu, skirtu bendrauti su klientais visuose mažmeninės prekybos kanaluose.</span><span class="sxs-lookup"><span data-stu-id="de309-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="de309-105">Įvairios funkcijos gali padėti klientams lengviau atrasti produktus.</span><span class="sxs-lookup"><span data-stu-id="de309-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="de309-106">Pavyzdžiui, jie gali naršyti po kategorijas, ieškoti ir filtruoti.</span><span class="sxs-lookup"><span data-stu-id="de309-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="de309-107">Šioje temoje paaiškinama koncepcija, kuri yra susijusi su įvairių su prekyba susijusių subjektų rodymo tvarkos valdymu.</span><span class="sxs-lookup"><span data-stu-id="de309-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="de309-108">Čia taip pat aiškinama, kaip pakeisti rūšiavimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="de309-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="de309-109">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="de309-109">Overview</span></span>

<span data-ttu-id="de309-110">Patobulinta įvairių su prekybą susijusių subjektų rūšiavimo pagalba.</span><span class="sxs-lookup"><span data-stu-id="de309-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="de309-111">Ši pagalba dabar geriau suderinta su esamais klientų scenarijais, kuriems seniau reikėjo plėtinių iš diegimo partnerių.</span><span class="sxs-lookup"><span data-stu-id="de309-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="de309-112">Senesnėse nei 10.0.5 Microsoft Dynamics 365 for Retail versijose kategorijų rūšiavimas naršymo hierarchijoje buvo alfabetinis.</span><span class="sxs-lookup"><span data-stu-id="de309-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="de309-113">Naujos pasirinktinės rūšiavimo tvarkos funkcijos leidžia prekybos vadybininkams konfigūruoti įvairių su prekyba susijusių subjektų tvarką visuose galutiniuose klientuose.</span><span class="sxs-lookup"><span data-stu-id="de309-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="de309-114">Šiuos klientus sudaro centrinės būstinės (HQ) ir skambučių centrai.</span><span class="sxs-lookup"><span data-stu-id="de309-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="de309-115">Kategorijų mažmeninės prekybos produktų hierarchijoje rodymo tvarkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="de309-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="de309-116">Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="de309-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="de309-117">Eikite į **Mažmeninė prekyba \> Produktai ir kategorijos \> Mažmeninės prekybos produktų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="de309-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="de309-118">Spustelėkite **Redaguoti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="de309-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="de309-119">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="de309-119">Click **Edit**.</span></span>
4. <span data-ttu-id="de309-120">Medyje išplėskite **VISI \> Veiksmo sportas**.</span><span class="sxs-lookup"><span data-stu-id="de309-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="de309-121">Medyje išplėskite **VISI \> Komandinis sportas**.</span><span class="sxs-lookup"><span data-stu-id="de309-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="de309-122">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="de309-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="de309-123">(Skaičius gali būti neigiamas)</span><span class="sxs-lookup"><span data-stu-id="de309-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="de309-124">Bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti, pakartokite 4–6 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="de309-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="de309-125">Kanalų naršymo hierarchijos rodymo tvarka atsispindės mažmeninės prekybos produktų hierarchijos HQ ir pagal kategoriją išleistuose produktuose.</span><span class="sxs-lookup"><span data-stu-id="de309-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![Mažmeninės prekybos produktų hierarchijos pasirinktinis rūšiavimas su neigiamomis reikšmėmis](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Pagal kategoriją išleistų produktų pasirinktinis rūšiavimas pagal mažmeninės prekybos produktų hierarchiją](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="de309-128">Kategorijų kanalo naršymo hierarchijoje rodymo tvarkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="de309-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="de309-129">Prieš baigdami šią procedūrą, savo aplinkoje turi įdiegti demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="de309-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="de309-130">Eikite į **Mažmeninė prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="de309-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="de309-131">Sąraše pažymėkite hierarchiją **Mados naršymas**.</span><span class="sxs-lookup"><span data-stu-id="de309-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="de309-132">Spustelėkite **Redaguoti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="de309-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="de309-133">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="de309-133">Click **Edit**.</span></span>
5. <span data-ttu-id="de309-134">Medyje pažymėkite **Mada \> Drabužiai moterims \> Batai moterims**.</span><span class="sxs-lookup"><span data-stu-id="de309-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="de309-135">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="de309-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="de309-136">Medyje pažymėkite **Mada \> Drabužiai moterims \> Viršutiniai drabužiai**.</span><span class="sxs-lookup"><span data-stu-id="de309-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="de309-137">Panašiai galite apibrėžti rūšiavimo tvarką antrinėse kategorijose.</span><span class="sxs-lookup"><span data-stu-id="de309-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="de309-138">Medyje pažymėkite **Mada \> Drabužiai vyrams \> Laisvalaikio marškinėliai**.</span><span class="sxs-lookup"><span data-stu-id="de309-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="de309-139">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="de309-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="de309-140">Medyje pažymėkite **Mada \> Drabužiai vyrams \> Paltai ir švarkai**.</span><span class="sxs-lookup"><span data-stu-id="de309-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="de309-141">Lauke **Rodymo tvarka** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="de309-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="de309-142">Šiuos veiksmus pakartokite bet kuriai papildomai kategorijai, kurios tvarką norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="de309-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="de309-143">Kanalo naršymo hierarchijos rodymo tvarka atsispindi HQ, kataloge ir mažmeninės prekybos kanaluose.</span><span class="sxs-lookup"><span data-stu-id="de309-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![Kanalo naršymo hierarchijos pasirinktinis rūšiavimas](./media/ChannelNavCustomSorted.png)

![Katalogo naršymo hierarchijos pasirinktis rūšiavimas pagal kanalo naršymo hierarchiją](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS su pasirinktai surūšiuotomis kategorijomis](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="de309-147">Pagal numatytuosius parametrus, pasirinktinio rūšiavimo tvarka yra išjungta.</span><span class="sxs-lookup"><span data-stu-id="de309-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="de309-148">Kaip įjungti šią funkciją ir kitas funkcijas, žr. [Funkcijų valdymas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="de309-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
