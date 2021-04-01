---
title: " Tvarkyti mažmeninės prekybos kainos koregavimus"
description: Ši procedūra padės nustatyti prekybos kainą.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbd2f818930424313e1d76aea4a257efa7c7b3be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232790"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="8b1f8-103"> Tvarkyti mažmeninės prekybos kainos koregavimus</span><span class="sxs-lookup"><span data-stu-id="8b1f8-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b1f8-104">Ši procedūra padės nustatyti prekybos kainą.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="8b1f8-105">Kainos koregavimas gali tiesiogiai nustatyti prekės pardavimo kainą, pakeisti bazinę pardavimo kainą arba prekybos sutarties pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="8b1f8-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="8b1f8-107">Spustelėkite Kainodaros ir nuolaidų valdymas.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="8b1f8-108">Spustelėkite skirtuką Kainų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="8b1f8-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-109">Click New.</span></span>
    * <span data-ttu-id="8b1f8-110">Čia galite sukurti visas dažniausiai naudojamas kainų ir nuolaidų taisykles, įskaitant nuolaidas, kainų koregavimą, prekybos sutarčių žurnalus ir kategorijų kainų taisykles.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="8b1f8-111">Spustelėkite Kainos koregavimas.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="8b1f8-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="8b1f8-113">Išplėskite dalį Eilutės.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="8b1f8-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-114">Click Add.</span></span>
    * <span data-ttu-id="8b1f8-115">Šiuo atveju lauke Produktas įveskite „81126“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="8b1f8-116">Tada lauke Nuolaidos procentas įveskite „10,0“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="8b1f8-117">Nuolaidos procento tipo kainos koregavimas sumažins bazinę pardavimo kainą arba prekybos sutarties pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="8b1f8-118">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-118">Click Add.</span></span>
    * <span data-ttu-id="8b1f8-119">Šiuo atveju lauke Produktas įveskite „81125“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="8b1f8-120">Tada lauke Nuolaidos metodas pasirinkite „Mokėjimo nuolaidos suma“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="8b1f8-121">Galiausiai lauke Mokėjimo nuolaidos suma įveskite „5,0“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="8b1f8-122">Mokėjimo nuolaidos sumos nuolaidos tipas yra suma, atimama iš bazinės kainos arba prekybos sutarties kainos.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="8b1f8-123">Spustelėkite Kainų grupės.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-123">Click Price groups.</span></span>
    * <span data-ttu-id="8b1f8-124">Lauke Kainų grupė pasirinkite „RP-Houston“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="8b1f8-125">Tokiu būdu kainos koregavimas bus susietas su „Houston“ parduotuve.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="8b1f8-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-126">Click Save.</span></span>
11. <span data-ttu-id="8b1f8-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-127">Close the page.</span></span>
12. <span data-ttu-id="8b1f8-128">Lauke Būsena pasirinkite „Įjungta“.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="8b1f8-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-129">Click Save.</span></span>
14. <span data-ttu-id="8b1f8-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-130">Close the page.</span></span>
15. <span data-ttu-id="8b1f8-131">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8b1f8-131">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]