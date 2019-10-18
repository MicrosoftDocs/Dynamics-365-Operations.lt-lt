---
title: Projekto pirkimo užsakymai
description: Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų. Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174563"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="b0646-104">Projekto pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="b0646-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0646-105">Šiame straipsnyje aprašomi įvairūs metodai, kuriuos naudodami galite kurti projekto pirkimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="b0646-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="b0646-106">Jūsų naudojamas metodas priklauso nuo pirkimo užsakymo paskirties ir nuo to, kada įsigytos prekės suvartojamos bei priskiriamos projektui.</span><span class="sxs-lookup"><span data-stu-id="b0646-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="b0646-107">Pirkimo užsakymo kūrimo metodai</span><span class="sxs-lookup"><span data-stu-id="b0646-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="b0646-108">Galite naudoti vieną iš tolesnių metodų, norėdami sukurti pirkimo užsakymą naudodami projekto valdymą ir apskaitą.</span><span class="sxs-lookup"><span data-stu-id="b0646-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="b0646-109">Pirkimo užsakymo paskirtis lemia, kada pirkimo užsakymas turi būti įvykdytas ir, tuo pačiu, kada reikia sumokėti už projekto prekes.</span><span class="sxs-lookup"><span data-stu-id="b0646-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0646-110">Metodas</span><span class="sxs-lookup"><span data-stu-id="b0646-110">Method</span></span></th>
<th><span data-ttu-id="b0646-111">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="b0646-111">Purpose</span></span></th>
<th><span data-ttu-id="b0646-112">Prekių suvartojimas</span><span class="sxs-lookup"><span data-stu-id="b0646-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0646-113">Pirkimo užsakymo kūrimas tiesiai iš projekto.</span><span class="sxs-lookup"><span data-stu-id="b0646-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="b0646-114">Naudokite šį metodą, kad pirktumėte prekes iš išorinio tiekėjo suvartoti vykdant projektą.</span><span class="sxs-lookup"><span data-stu-id="b0646-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="b0646-115">Kurti pirkimo užsakymą galite tolesniais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="b0646-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="b0646-116">Iš paties projekto.</span><span class="sxs-lookup"><span data-stu-id="b0646-116">From the project itself.</span></span> <span data-ttu-id="b0646-117">Šiuo atveju pirkimo užsakymo projektas jau yra nustatytas.</span><span class="sxs-lookup"><span data-stu-id="b0646-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="b0646-118">Pereidami į projekto pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b0646-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="b0646-119">Turite pasirinkti ir tiekėją, ir projektą, kuriame reikia sukurti pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b0646-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="b0646-120">Prekės suvartojamos atnaujinus tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="b0646-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0646-121">Sukurkite pirkimo užsakymą pagal pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b0646-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="b0646-122">Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b0646-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="b0646-123">Prekės suvartojamos, kai klientui išrašoma pardavimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="b0646-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0646-124">Sukurkite pirkimo užsakymą pagal prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="b0646-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="b0646-125">Naudokite šį metodą, jei norite pirkti prekes, kai kuriate projekto prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="b0646-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="b0646-126">Prekės suvartojamos, kai atnaujinamas prekės poreikio važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="b0646-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="b0646-127">Kai atnaujinsite tiekėjo SF arba važtaraštį, jus paragins atnaujinti ir prekės poreikio važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="b0646-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="b0646-128">Daugiau informacijos žr. [Gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="b0646-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

