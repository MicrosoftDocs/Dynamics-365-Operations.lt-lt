--- 
title: " Tvarkyti mažmeninės prekybos kainos koregavimus"
description: "Ši procedūra padeda kurti mažmeninės prekybos kainos koregavimą."
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: edfb9a1515f0af7d3272ea3fbb362bd0e6b0f129
ms.contentlocale: lt-lt
ms.lasthandoff: 02/07/2018

---
# <a name="retail-price-adjustments"></a><span data-ttu-id="aa2d4-103"> Tvarkyti mažmeninės prekybos kainos koregavimus</span><span class="sxs-lookup"><span data-stu-id="aa2d4-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="aa2d4-104">Ši procedūra padeda kurti mažmeninės prekybos kainos koregavimą.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="aa2d4-105">Mažmeninės prekybos kainos koregavimas gali tiesiogiai nustatyti prekės pardavimo kainą arba modifikuoti jos bazinę pardavimo kainą ar prekybos sutarties pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="aa2d4-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="aa2d4-107">Spustelėkite Kainodaros ir nuolaidų valdymas.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="aa2d4-108">Spustelėkite skirtuką Kainų koregavimai.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="aa2d4-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-109">Click New.</span></span>
    * <span data-ttu-id="aa2d4-110">Čia galite kurti visas dažniausiai naudojamas kainų ir nuolaidų taisykles, įskaitant mažmeninės prekybos nuolaidų, kainų koregavimų, prekybos sutarčių žurnalų ir kategorijos kainų taisykles.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="aa2d4-111">Spustelėkite Kainos koregavimas.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="aa2d4-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="aa2d4-113">Išplėskite dalį Eilutės.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="aa2d4-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-114">Click Add.</span></span>
    * <span data-ttu-id="aa2d4-115">Šiuo atveju lauke Produktas įveskite „81126“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="aa2d4-116">Tada lauke Nuolaidos procentas įveskite „10,0“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="aa2d4-117">Nuolaidos procento tipo kainos koregavimas sumažins bazinę pardavimo kainą arba prekybos sutarties pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="aa2d4-118">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-118">Click Add.</span></span>
    * <span data-ttu-id="aa2d4-119">Šiuo atveju lauke Produktas įveskite „81125“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="aa2d4-120">Tada lauke Nuolaidos metodas pasirinkite „Mokėjimo nuolaidos suma“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="aa2d4-121">Galiausiai lauke Mokėjimo nuolaidos suma įveskite „5,0“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="aa2d4-122">Mokėjimo nuolaidos sumos nuolaidos tipas yra suma, atimama iš bazinės kainos arba prekybos sutarties kainos.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="aa2d4-123">Spustelėkite Kainų grupės.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-123">Click Price groups.</span></span>
    * <span data-ttu-id="aa2d4-124">Lauke Kainų grupė pasirinkite „RP-Houston“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="aa2d4-125">Tokiu būdu kainos koregavimas bus susietas su „Houston“ parduotuve.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="aa2d4-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-126">Click Save.</span></span>
11. <span data-ttu-id="aa2d4-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-127">Close the page.</span></span>
12. <span data-ttu-id="aa2d4-128">Lauke Būsena pasirinkite „Įjungta“.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="aa2d4-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-129">Click Save.</span></span>
14. <span data-ttu-id="aa2d4-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-130">Close the page.</span></span>
15. <span data-ttu-id="aa2d4-131">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-131">Refresh the page.</span></span>


