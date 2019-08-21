---
title: Kurti PVM operacijas dokumentuose
description: PVM dokumentuose skaičiuojamas dokumentų eilutėse nurodant PVM grupę ir prekių PVM grupę.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 653b93744f5b891655cade0cb669d34179fca9cd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846540"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="3089e-103">Kurti PVM operacijas dokumentuose</span><span class="sxs-lookup"><span data-stu-id="3089e-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3089e-104">PVM dokumentuose skaičiuojamas dokumentų eilutėse nurodant PVM grupę ir prekių PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="3089e-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="3089e-105">Pagal numatytąsias nuostatas grupės naudojamos tos pačios kaip ir bendruosiuose duomenyse, tačiau, jei reikia, jas galima keisti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3089e-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="3089e-106">Apskaičiuotąjį PVM galima patikrinti eilutės ir dokumento lygiu.</span><span class="sxs-lookup"><span data-stu-id="3089e-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="3089e-107">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="3089e-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3089e-108">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="3089e-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="3089e-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="3089e-109">Click New.</span></span>
3. <span data-ttu-id="3089e-110">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3089e-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3089e-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3089e-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3089e-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3089e-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3089e-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="3089e-113">Click OK.</span></span>
7. <span data-ttu-id="3089e-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3089e-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3089e-115">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3089e-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3089e-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3089e-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3089e-117">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3089e-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="3089e-118">Išplėskite arba sutraukite dalį Išsami eilučių informacija.</span><span class="sxs-lookup"><span data-stu-id="3089e-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="3089e-119">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="3089e-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="3089e-120">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3089e-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="3089e-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3089e-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3089e-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3089e-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3089e-123">Spustelėkite Finansai.</span><span class="sxs-lookup"><span data-stu-id="3089e-123">Click Financials.</span></span>
17. <span data-ttu-id="3089e-124">Spustelėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="3089e-124">Click Sales tax.</span></span>
18. <span data-ttu-id="3089e-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3089e-125">Click OK.</span></span>
19. <span data-ttu-id="3089e-126">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="3089e-126">Click Add line.</span></span>
20. <span data-ttu-id="3089e-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3089e-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="3089e-128">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3089e-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="3089e-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3089e-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="3089e-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3089e-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="3089e-131">Lauke Vieneto kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3089e-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="3089e-132">Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3089e-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="3089e-133">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3089e-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="3089e-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3089e-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="3089e-135">Veiksmų srityje spustelėkite Parduoti.</span><span class="sxs-lookup"><span data-stu-id="3089e-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="3089e-136">Spustelėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="3089e-136">Click Sales tax.</span></span>
30. <span data-ttu-id="3089e-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3089e-137">Click OK.</span></span>

