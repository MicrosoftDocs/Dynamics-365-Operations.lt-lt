---
title: Skirstyti produktus iš paskirstymo centro į parduotuvę naudojant skirstymą pirkėjams
description: Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti skirstymą pirkėjams, skirtą produktams iš vienos vietos į vieną ar kelias parduotuves paskirstyti.
author: rubencdelgado
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0fa48d7cd1af289cf455ebd0e0c14b047b4f1a4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802652"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="4be3f-103">Skirstyti produktus iš paskirstymo centro į parduotuvę naudojant skirstymą pirkėjams</span><span class="sxs-lookup"><span data-stu-id="4be3f-103">Push products from distribution center to store using buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be3f-104">Ši procedūra padeda atlikti žingsnius, norint kurti ir vykdyti skirstymą pirkėjams, skirtą produktams iš vienos vietos į vieną ar kelias parduotuves paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="4be3f-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="4be3f-105">Vartotojas gali nustatyti kelias konfigūracijas ir nurodyti sistemai siūlyti, kaip paskirstyti produktus, arba patys įvesti, kur produktai turi būti paskirstomi ir koks jų kiekis paskirstomas į kiekvieną parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="4be3f-106">Į šią procedūrą neįtraukiamas duomenų, kuriuos galima naudoti skirstyme pirkėjams, pvz., papildymo taisyklių, organizacijos hierarchijų ir parduotuvės reikšmės, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="4be3f-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="4be3f-107">Šioje procedūroje naudojama demonstracinė įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="4be3f-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4be3f-108">Pasirinkite Skirstymas pirkėjams.</span><span class="sxs-lookup"><span data-stu-id="4be3f-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="4be3f-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4be3f-109">Click New.</span></span>
3. <span data-ttu-id="4be3f-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="4be3f-111">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="4be3f-112">Lauke Sandėlis įveskite arba pasirinkite sandėlį, kuriame yra produktų su turimais kiekiais.</span><span class="sxs-lookup"><span data-stu-id="4be3f-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="4be3f-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4be3f-113">Click Add.</span></span>
7. <span data-ttu-id="4be3f-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4be3f-115">Lauke Prekės numeris įveskite arba pasirinkite produktą.</span><span class="sxs-lookup"><span data-stu-id="4be3f-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="4be3f-116">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4be3f-116">Click Add.</span></span>
10. <span data-ttu-id="4be3f-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="4be3f-118">Lauke Prekės numeris įveskite arba pasirinkite produkto variantą.</span><span class="sxs-lookup"><span data-stu-id="4be3f-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="4be3f-119">Įvedant produkto variantus, bus sukurtos kiekvieno varianto eilutės.</span><span class="sxs-lookup"><span data-stu-id="4be3f-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="4be3f-120">Sąraše pažymėkite eilutę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="4be3f-121">Lauke Paskirstytas kiekis įveskite, kokį pasirinkto produkto kiekį norite paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="4be3f-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="4be3f-122">Lauke Papildomas kiekis, kurį reikia paskirstyti įveskite produktų kiekį, kurį galima paskirstyti.</span><span class="sxs-lookup"><span data-stu-id="4be3f-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="4be3f-123">Lauke Paskirstymas įveskite „Vietos reikšmė“.</span><span class="sxs-lookup"><span data-stu-id="4be3f-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="4be3f-124">Galite pasirinkti kitus tipus ir naudoti kitas paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="4be3f-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="4be3f-125">Lauke Papildymo hierarchija pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4be3f-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="4be3f-126">Lauke Pagal asortimentus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4be3f-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="4be3f-127">Spustelėkite Skaičiuoti kiekius ir peržiūrėkite kiekius, įtrauktus į eilutes sekcijoje Sandėlis.</span><span class="sxs-lookup"><span data-stu-id="4be3f-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="4be3f-128">Spustelėkite Kurti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4be3f-128">Click Create order.</span></span>
20. <span data-ttu-id="4be3f-129">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4be3f-129">Click Yes.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]