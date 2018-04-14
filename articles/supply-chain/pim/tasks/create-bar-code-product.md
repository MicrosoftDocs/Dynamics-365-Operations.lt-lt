--- 
title: "Produkto brūkšninio kodo kūrimas"
description: "Šioje procedūroje parodoma, kaip neautomatiniu būdu kurti brūkšninį kodą naudojant prekės numerį M0001 kaip pavyzdį."
author: YuyuScheller
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6a55e25205bc7e996b6ab8c6915e2e86b758ee7a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="5f7a5-103">Produkto brūkšninio kodo kūrimas</span><span class="sxs-lookup"><span data-stu-id="5f7a5-103">Create a bar code for a product</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f7a5-104">Šioje procedūroje parodoma, kaip neautomatiniu būdu kurti brūkšninį kodą naudojant prekės numerį M0001 kaip pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="5f7a5-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5f7a5-106">Spustelėkite Patvirtinto produkto priežiūra.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="5f7a5-107">Spustelėkite Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-107">Click Released products.</span></span>
3. <span data-ttu-id="5f7a5-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5f7a5-109">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="5f7a5-110">Spustelėkite Brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-110">Click Bar codes.</span></span>
6. <span data-ttu-id="5f7a5-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-111">Click New.</span></span>
7. <span data-ttu-id="5f7a5-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="5f7a5-113">Lauke Brūkšninio kodo nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="5f7a5-114">Lauke Brūkšninis kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="5f7a5-115">Lauke Brūkšninis kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="5f7a5-116">Paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="5f7a5-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-117">Close the page.</span></span>
12. <span data-ttu-id="5f7a5-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="5f7a5-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-119">Click Save.</span></span>
    * <span data-ttu-id="5f7a5-120">Kai spustelėsite Įrašyti, bus vykdoma brūkšninio kodo patikra ir šiuo atveju bus rodomas klaidos pranešimas, kad numatomas kontrolinis skaitmuo yra 8, o rastas skaitmuo yra 3.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="5f7a5-121">Neautomatiniu būdu atnaujinkite brūkšninio kodo numerį, kad paskutinis jo skaitmuo būtų 8.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="5f7a5-122">Lauke Brūkšninis kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="5f7a5-123">Lauke Brūkšninis kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="5f7a5-124">Paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="5f7a5-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-125">Close the page.</span></span>
17. <span data-ttu-id="5f7a5-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-126">Click Save.</span></span>
18. <span data-ttu-id="5f7a5-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5f7a5-127">Close the page.</span></span>


