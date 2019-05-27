---
title: Gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį
description: Šioje procedūroje nurodoma, kaip gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572378"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="03673-103">Gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį</span><span class="sxs-lookup"><span data-stu-id="03673-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03673-104">Šioje procedūroje nurodoma, kaip gauti pirkimo užsakyme pateiktas prekes pagal prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="03673-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="03673-105">Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.</span><span class="sxs-lookup"><span data-stu-id="03673-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="03673-106">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="03673-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="03673-107">Eikite į Projektų valdymas ir apskaita > Projektai > Visi projektai.</span><span class="sxs-lookup"><span data-stu-id="03673-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="03673-108">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03673-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="03673-109">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="03673-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="03673-110">Spustelėkite Prekių poreikis.</span><span class="sxs-lookup"><span data-stu-id="03673-110">Click Item requirements.</span></span>
5. <span data-ttu-id="03673-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="03673-111">Click New.</span></span>
6. <span data-ttu-id="03673-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="03673-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="03673-113">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03673-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="03673-114">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="03673-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="03673-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="03673-115">Click Save.</span></span>
10. <span data-ttu-id="03673-116">Veiksmų srityje spustelėkite Valdyti.</span><span class="sxs-lookup"><span data-stu-id="03673-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="03673-117">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="03673-117">Click Functions.</span></span>
12. <span data-ttu-id="03673-118">Spustelėkite Kurti pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="03673-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="03673-119">Pažymėkite žymės langelį Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="03673-119">Select the Include check box.</span></span>
14. <span data-ttu-id="03673-120">Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="03673-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="03673-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03673-121">Click OK.</span></span>
16. <span data-ttu-id="03673-122">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="03673-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="03673-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="03673-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="03673-124">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="03673-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="03673-125">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="03673-125">Click Confirm.</span></span>
20. <span data-ttu-id="03673-126">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="03673-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="03673-127">Spustelėkite Produkto gavimo kvitas.</span><span class="sxs-lookup"><span data-stu-id="03673-127">Click Product receipt.</span></span>
22. <span data-ttu-id="03673-128">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="03673-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="03673-129">Lauke Produkto gavimo kvitas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="03673-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="03673-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="03673-130">Click OK.</span></span>

