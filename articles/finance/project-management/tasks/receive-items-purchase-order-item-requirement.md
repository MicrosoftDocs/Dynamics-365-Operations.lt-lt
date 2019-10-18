---
title: Pirkimo užsakyme pateiktų prekių gavimas pagal prekių poreikį
description: Šioje temoje paaiškinta, kaip pagal prekių poreikį gauti pirkimo užsakyme pateiktas prekes.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174425"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="022dc-103">Pirkimo užsakyme pateiktų prekių gavimas pagal prekių poreikį</span><span class="sxs-lookup"><span data-stu-id="022dc-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="022dc-104">Šioje temoje paaiškinta, kaip pagal prekių poreikį gauti pirkimo užsakyme pateiktas prekes.</span><span class="sxs-lookup"><span data-stu-id="022dc-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="022dc-105">Naudodami prekės poreikį vietoje prekės operacijos, galite planuoti pristatymą prieš faktiškai naudojant prekę, kurti pirkimo užsakymą, įtraukti prekę į prekybos sutarties sistemą bei įtraukti prekės poreikį į gamybos planavimą.</span><span class="sxs-lookup"><span data-stu-id="022dc-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="022dc-106">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="022dc-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="022dc-107">Naršymo srityje eikite į **Moduliai > Projekto valdymas ir apskaita > Projektai > Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="022dc-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="022dc-108">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="022dc-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="022dc-109">Veiksmų srityje pasirinkite **Planas**.</span><span class="sxs-lookup"><span data-stu-id="022dc-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="022dc-110">Pasirinkite **Prekių poreikis**</span><span class="sxs-lookup"><span data-stu-id="022dc-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="022dc-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="022dc-111">Select **New**.</span></span>
6. <span data-ttu-id="022dc-112">Naujoje eilutėje lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="022dc-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="022dc-113">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="022dc-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="022dc-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="022dc-114">Select **Save**.</span></span>
9. <span data-ttu-id="022dc-115">Veiksmų srityje pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="022dc-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="022dc-116">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="022dc-116">Select **Functions**.</span></span>
11. <span data-ttu-id="022dc-117">Pasirinkite **Kurti pirkimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="022dc-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="022dc-118">Pažymėkite žymės langelį **Įtraukti visus**.</span><span class="sxs-lookup"><span data-stu-id="022dc-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="022dc-119">Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="022dc-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="022dc-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="022dc-120">Select **OK**.</span></span>
15. <span data-ttu-id="022dc-121">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="022dc-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="022dc-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="022dc-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="022dc-123">Veiksmų srityje pasirinkite **Pirkimas**.</span><span class="sxs-lookup"><span data-stu-id="022dc-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="022dc-124">Pasirinkite **„Patvirtinti“**.</span><span class="sxs-lookup"><span data-stu-id="022dc-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="022dc-125">Veiksmų srityje pasirinkite **„Gauti“**.</span><span class="sxs-lookup"><span data-stu-id="022dc-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="022dc-126">Pasirinkite **„Produkto gavimo kvitas“**.</span><span class="sxs-lookup"><span data-stu-id="022dc-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="022dc-127">Lauke **Produkto gavimo kvitas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="022dc-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="022dc-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="022dc-128">Select **OK**.</span></span>

