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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f53de983389dd8cbfb2c29af84539f1a73dc0a85
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="ceb53-103">Produkto brūkšninio kodo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ceb53-103">Create a bar code for a product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ceb53-104">Šioje procedūroje parodoma, kaip neautomatiniu būdu kurti brūkšninį kodą naudojant prekės numerį M0001 kaip pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="ceb53-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="ceb53-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ceb53-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ceb53-106">Spustelėkite Patvirtinto produkto priežiūra.</span><span class="sxs-lookup"><span data-stu-id="ceb53-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="ceb53-107">Spustelėkite Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="ceb53-107">Click Released products.</span></span>
3. <span data-ttu-id="ceb53-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ceb53-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ceb53-109">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="ceb53-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="ceb53-110">Spustelėkite Brūkšniniai kodai.</span><span class="sxs-lookup"><span data-stu-id="ceb53-110">Click Bar codes.</span></span>
6. <span data-ttu-id="ceb53-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ceb53-111">Click New.</span></span>
7. <span data-ttu-id="ceb53-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ceb53-113">Lauke Brūkšninio kodo nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="ceb53-114">Lauke Brūkšninis kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="ceb53-115">Lauke Brūkšninis kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="ceb53-116">Paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="ceb53-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="ceb53-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ceb53-117">Close the page.</span></span>
12. <span data-ttu-id="ceb53-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ceb53-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="ceb53-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ceb53-119">Click Save.</span></span>
    * <span data-ttu-id="ceb53-120">Kai spustelėsite Įrašyti, bus vykdoma brūkšninio kodo patikra ir šiuo atveju bus rodomas klaidos pranešimas, kad numatomas kontrolinis skaitmuo yra 8, o rastas skaitmuo yra 3.</span><span class="sxs-lookup"><span data-stu-id="ceb53-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="ceb53-121">Neautomatiniu būdu atnaujinkite brūkšninio kodo numerį, kad paskutinis jo skaitmuo būtų 8.</span><span class="sxs-lookup"><span data-stu-id="ceb53-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="ceb53-122">Lauke Brūkšninis kodas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="ceb53-123">Lauke Brūkšninis kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ceb53-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="ceb53-124">Paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="ceb53-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="ceb53-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ceb53-125">Close the page.</span></span>
17. <span data-ttu-id="ceb53-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ceb53-126">Click Save.</span></span>
18. <span data-ttu-id="ceb53-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ceb53-127">Close the page.</span></span>


