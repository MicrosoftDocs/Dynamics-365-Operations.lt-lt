---
title: "Projekto pirkimo užsakymai"
description: "Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 985a57ae9fb116b1c4514b836b35c5da0f8838fd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2017

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="19ff1-104">Projekto pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="19ff1-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19ff1-105">Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="19ff1-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="19ff1-106">Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.</span><span class="sxs-lookup"><span data-stu-id="19ff1-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="19ff1-107">„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidime kurti projekto pirkimo užsakymus galite keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="19ff1-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="19ff1-108">Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties, nuo to, kada įsigytos prekės suvartojamos ir kada įsigytos prekės priskiriamos projektui.</span><span class="sxs-lookup"><span data-stu-id="19ff1-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="19ff1-109">Pirkimo užsakymo kūrimo metodai</span><span class="sxs-lookup"><span data-stu-id="19ff1-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="19ff1-110">Galite naudoti vieną iš tolesnių metodų, norėdami sukurti pirkimo užsakymą naudodami projekto valdymą ir apskaitą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="19ff1-111">Pirkimo užsakymo paskirtis lemia, kada pirkimo užsakymas turi būti įvykdytas ir, tuo pačiu, kada reikia sumokėti už projekto prekes.</span><span class="sxs-lookup"><span data-stu-id="19ff1-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="19ff1-112">Metodas</span><span class="sxs-lookup"><span data-stu-id="19ff1-112">Method</span></span></th>
<th><span data-ttu-id="19ff1-113">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="19ff1-113">Purpose</span></span></th>
<th><span data-ttu-id="19ff1-114">Prekių suvartojimas</span><span class="sxs-lookup"><span data-stu-id="19ff1-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="19ff1-115">Pirkimo užsakymo kūrimas tiesiai iš projekto.</span><span class="sxs-lookup"><span data-stu-id="19ff1-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="19ff1-116">Naudokite šį metodą, kad pirktumėte prekes iš išorinio tiekėjo suvartoti vykdant projektą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="19ff1-117">Kurti pirkimo užsakymą galite tolesniais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="19ff1-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="19ff1-118">Iš paties projekto.</span><span class="sxs-lookup"><span data-stu-id="19ff1-118">From the project itself.</span></span> <span data-ttu-id="19ff1-119">Šiuo atveju pirkimo užsakymo projektas jau yra nustatytas.</span><span class="sxs-lookup"><span data-stu-id="19ff1-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="19ff1-120">Pereidami į projekto pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="19ff1-121">Turite pasirinkti ir tiekėją, ir projektą, kuriame reikia sukurti pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="19ff1-122">Prekės suvartojamos atnaujinus tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="19ff1-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="19ff1-123">Sukurkite pirkimo užsakymą pagal pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="19ff1-124">Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="19ff1-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="19ff1-125">Prekės suvartojamos, kai klientui išrašoma pardavimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="19ff1-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="19ff1-126">Sukurkite pirkimo užsakymą pagal prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="19ff1-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="19ff1-127">Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="19ff1-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="19ff1-128">Prekės suvartojamos, kai atnaujinamas prekės poreikio važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="19ff1-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="19ff1-129">Kai atnaujinsite tiekėjo SF arba važtaraštį, jus paragins atnaujinti ir prekės poreikio važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="19ff1-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="19ff1-130">Daugiau informacijos žr. [Gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="19ff1-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

