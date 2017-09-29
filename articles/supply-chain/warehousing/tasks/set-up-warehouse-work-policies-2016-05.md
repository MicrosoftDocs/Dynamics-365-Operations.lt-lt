--- 
title: "Nustatyti sandėlio darbo strategijas "
description: "Sandėlio procesai ne visada apima sandėlio darbą."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b7d579ca7e2b9ca8cbead74b2c2ababfd142f171
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="ce9f1-103">Nustatyti sandėlio darbo strategijas </span><span class="sxs-lookup"><span data-stu-id="ce9f1-103">Set up warehouse work policies</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce9f1-104">Sandėlio procesai ne visada apima sandėlio darbą.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="ce9f1-105">Apibrėždami darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="ce9f1-106">Kuriant šį įrašą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="ce9f1-107">Norint atlikti šį užduoties vediklį, reikia „Dynamics AX‟ programos 7.0.1 arba naujesnės versijos.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="ce9f1-108">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo strategijos.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="ce9f1-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-109">Click New.</span></span>
3. <span data-ttu-id="ce9f1-110">Lauke Darbo strategijos pavadinimas įveskite „Atidėjimo darbo nėra‟.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="ce9f1-111">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-111">Click Save.</span></span>
5. <span data-ttu-id="ce9f1-112">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-112">Click Add.</span></span>
6. <span data-ttu-id="ce9f1-113">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="ce9f1-114">Lauke Darbo užsakymo tipas pasirinkite Baigtos prekės atidėtos.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="ce9f1-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-115">Click Add.</span></span>
9. <span data-ttu-id="ce9f1-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="ce9f1-117">Lauke Darbo užsakymo tipas pasirinkite Sudėtinis produktas ir šalutinis produktas atidėti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="ce9f1-118">Išplėskite dalį Atsargų vietos.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="ce9f1-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-119">Click Add.</span></span>
13. <span data-ttu-id="ce9f1-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ce9f1-121">Sandėlių sąraše įveskite „51‟.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="ce9f1-122">Lauke Vieta įveskite arba pasirinkite „001‟.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="ce9f1-123">Išplėskite sekciją Produktai.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-123">Expand the Products section.</span></span>
17. <span data-ttu-id="ce9f1-124">Lauke Produktų pasirinkimas pasirinkite Pasirinkta.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="ce9f1-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-125">Click Add.</span></span>
19. <span data-ttu-id="ce9f1-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="ce9f1-127">Lauke Prekės numeris įveskite arba pasirinkite „L0101‟.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="ce9f1-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ce9f1-128">Click Save.</span></span>

