---
title: "Veikiančios vidutinės prekės atsargų dimensijos sekimas"
description: "Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a88ec380810a9a2d7048d5a8773ebb5960e4cf86
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="6ba0c-104">Veikiančios vidutinės prekės atsargų dimensijos sekimas</span><span class="sxs-lookup"><span data-stu-id="6ba0c-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="6ba0c-105">Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="6ba0c-106">Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="6ba0c-107">Yra trys atsargų dimensijų tipai: produkto, saugojimo ir sekimo.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="6ba0c-108">Produkto dimensijos apima konfigūraciją, dydį ir spalvą.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="6ba0c-109">Produkto dimensijos visada sekamos finansiškai.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="6ba0c-110">Saugojimo ir sekimo dimensijos apima teritoriją, sandėlį, vietą, atsargų būseną, numerio lentelę, paketo numerį ir serijos numerį.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="6ba0c-111">Galite nuspręsti, kurias saugojimo ir sekimo dimensijas sekti finansiškai.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="6ba0c-112">**1 pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="6ba0c-112">**Example 1**</span></span> 

<span data-ttu-id="6ba0c-113">Jei prie prekės pridėta laikymo dimensijų grupė finansiškai sekama pagal sandėlį, apskaičiuojama kiekvieno sandėlio naudojama savikaina.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="6ba0c-114">Išrašytos šių pirkimo užsakymų sąskaitos faktūros:</span><span class="sxs-lookup"><span data-stu-id="6ba0c-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="6ba0c-115">Pirkimo užsakymas, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, išrašytas sandėliui GW.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="6ba0c-116">Pirkimo užsakymas, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, išrašytas sandėliui GW.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="6ba0c-117">Pirkimo užsakymas, kurio kiekis – 5 prekės, jų savikaina yra 15,00 USD, išrašytas sandėliui MW.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="6ba0c-118">Einamoji vidutinė sandėlio GW savikaina yra 11,20 USD, o einamoji sandėlio MW savikaina yra 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="6ba0c-119">Sandėliui GW užregistruojama pardavimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="6ba0c-120">Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 11,20 USD.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="6ba0c-121">Sandėliui MW užregistruojamas kitas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="6ba0c-122">Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="6ba0c-123">**2 pavyzdys** Jei prie prekės pridėta saugojimo dimensijų grupė finansiškai sekama pagal sandėlį ir sekimo dimensijų grupė finansiškai sekama pagal partijos numerį, einamoji savikaina apskaičiuojama kiekvienam paketui.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="6ba0c-124">**Pastaba.** Rekomenduojame visada peržiūrėti visų sekamų finansinių dimensijų savikainą.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="6ba0c-125">Išrašytos šių pirkimo užsakymų sąskaitos faktūros:</span><span class="sxs-lookup"><span data-stu-id="6ba0c-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="6ba0c-126">Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="6ba0c-127">Pirkimo užsakymo, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="6ba0c-128">Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 15,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui BBB.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="6ba0c-129">Einamoji vidutinė sandėlio GW ir paketo AAA savikaina yra 11,20 USD, o einamoji sandėlio MW ir paketo BBB savikaina yra 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="6ba0c-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>



