---
title: Variantų grupės kūrimas
description: Šioje temoje aprašoma, kaip naudojant „Microsoft Dynamics 365 Commerce“ sukurti produkto variantų, besiskiriančių dydžiu, stiliumi ar spalva, grupę.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d9279e1076796bb455429e5ff004c89ec5829e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414345"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="391ca-103">Variantų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="391ca-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="391ca-104">Šioje temoje aprašoma, kaip naudojant „Microsoft Dynamics 365 Commerce“ sukurti produkto variantų, besiskiriančių dydžiu, stiliumi ar spalva, grupę.</span><span class="sxs-lookup"><span data-stu-id="391ca-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="391ca-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="391ca-105">Overview</span></span>

<span data-ttu-id="391ca-106">„Dynamics 365 Commerce“ palaikomi keli produktų variantai.</span><span class="sxs-lookup"><span data-stu-id="391ca-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="391ca-107">Ji puikiai tinka įvairių produktų kategorijų variantų grupėms nustatyti.</span><span class="sxs-lookup"><span data-stu-id="391ca-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="391ca-108">Pavyzdžiui, galima sukurti marškinėlių dydžių grupę, įtraukus labai mažą, mažą, vidutinį, didelį ir labai didelį dydžius, ar spalvų grupę, įtraukus visas galimas produkto spalvas.</span><span class="sxs-lookup"><span data-stu-id="391ca-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="391ca-109">Variantų grupes reikėtų įtraukti prieš įtraukiant produktus.</span><span class="sxs-lookup"><span data-stu-id="391ca-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="391ca-110">Šioje temoje bus sukurta ir sukonfigūruota dydžių grupė.</span><span class="sxs-lookup"><span data-stu-id="391ca-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="391ca-111">Panašiomis procedūromis galima vadovautis, norint įtraukti ir sukonfigūruoti stilių ir spalvų grupes.</span><span class="sxs-lookup"><span data-stu-id="391ca-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="391ca-112">Dydžių grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="391ca-112">Create a size group</span></span>

<span data-ttu-id="391ca-113">Norėdami sukurti dydžių grupę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="391ca-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="391ca-114">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Variantų grupės \> Dydžių grupės**.</span><span class="sxs-lookup"><span data-stu-id="391ca-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="391ca-115">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="391ca-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="391ca-116">Langelyje **Dydžių grupė** įveskite dydžių grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="391ca-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="391ca-117">Langelyje **Aprašas** įveskite tinkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="391ca-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="391ca-118">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="391ca-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="391ca-119">Atributų įtraukimas į dydžių grupę</span><span class="sxs-lookup"><span data-stu-id="391ca-119">Add attributes to the size group</span></span>

<span data-ttu-id="391ca-120">Norėdami į dydžių grupę įtraukti atributų, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="391ca-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="391ca-121">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Variantų grupės \> Dydžių grupės**</span><span class="sxs-lookup"><span data-stu-id="391ca-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="391ca-122">Naršymo srityje pasirinkite dydžių grupę.</span><span class="sxs-lookup"><span data-stu-id="391ca-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="391ca-123">Dalyje **Dydžių grupės eilutės** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="391ca-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="391ca-124">Langelyje **Dydis** įveskite dydį (pavyzdžiui, „XL“) nurodančią eilutę.</span><span class="sxs-lookup"><span data-stu-id="391ca-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="391ca-125">Langelyje **Dydžio pavadinimas** įveskite dydžio pavadinimą (pavyzdžiui, „Labai didelis“).</span><span class="sxs-lookup"><span data-stu-id="391ca-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="391ca-126">Langelyje **Papildymo svoris** įveskite skaičių, reiškiantį papildymo svorį.</span><span class="sxs-lookup"><span data-stu-id="391ca-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="391ca-127">Langelyje **Brūkšninio kodo skaičius** įveskite skaičių, reiškiantį brūkšninį kodą.</span><span class="sxs-lookup"><span data-stu-id="391ca-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="391ca-128">Langelyje **Rodymo tvarka** įveskite rodymo tvarką reiškiantį skaičių.</span><span class="sxs-lookup"><span data-stu-id="391ca-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="391ca-129">Įtraukę visus norimus dydžius, veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="391ca-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="391ca-130">Toliau pateiktame vaizde parodytas dydžių grupės pavyzdys „kasdienių marškinių dydžiai“.</span><span class="sxs-lookup"><span data-stu-id="391ca-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Dydžių grupės kūrimas](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="391ca-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="391ca-132">Additional resources</span></span>

[<span data-ttu-id="391ca-133">Produktų informacijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="391ca-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="391ca-134">Mažmeninės prekybos produktų nustatymas</span><span class="sxs-lookup"><span data-stu-id="391ca-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="391ca-135">Produktų dimensijos</span><span class="sxs-lookup"><span data-stu-id="391ca-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
