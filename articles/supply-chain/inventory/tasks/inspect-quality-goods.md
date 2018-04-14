---
title: "Tikrinti prekių kokybę"
description: "Šioje procedūroje nurodoma, kaip apdoroti kokybės užsakymą."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ab536047340bdebecb7c8317e20208c87a4776f7
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="b199f-103">Tikrinti prekių kokybę</span><span class="sxs-lookup"><span data-stu-id="b199f-103">Inspect the quality of goods</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b199f-104">Šioje procedūroje nurodoma, kaip apdoroti kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b199f-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="b199f-105">Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="b199f-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="b199f-106">Prieš pradėdami šį procedūros pavyzdį, turite patvirtinti pirkimo užsakymą „000016“ ir užregistruoti produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="b199f-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="b199f-107">Tai automatiškai sukurs kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b199f-107">This will automatically create a quality order.</span></span> <span data-ttu-id="b199f-108">Kokybės patikrinimus paprastai atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="b199f-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="b199f-109">Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="b199f-109">Select a quality order</span></span>
1. <span data-ttu-id="b199f-110">Pasirinkite Atsargų valdymas > Periodinės užduotys > Kokybės valdymas > Kokybės užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b199f-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="b199f-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b199f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b199f-112">Pasirinkite kokybės užsakymą, sukurtą prieš jums pradedant šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="b199f-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="b199f-113">Įrašyti tikrinimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="b199f-113">Record test results</span></span>
1. <span data-ttu-id="b199f-114">Spustelėkite „Rezultatai“.</span><span class="sxs-lookup"><span data-stu-id="b199f-114">Click Results.</span></span>
2. <span data-ttu-id="b199f-115">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b199f-115">Click Edit.</span></span>
3. <span data-ttu-id="b199f-116">Lauke „Rezultatų kiekis“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b199f-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="b199f-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b199f-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b199f-118">Lauke „Baigtis“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b199f-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b199f-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b199f-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b199f-120">Šiame pavyzdyje rezultatas priklauso nuo iš anksto nustatytos baigties.</span><span class="sxs-lookup"><span data-stu-id="b199f-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="b199f-121">Paprastai įrašomas konkretesnis bandymo rezultatas, pavyzdžiui, dydis ar kitas matmuo.</span><span class="sxs-lookup"><span data-stu-id="b199f-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="b199f-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b199f-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b199f-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b199f-123">Click Save.</span></span>
9. <span data-ttu-id="b199f-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b199f-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="b199f-125">Tikrinti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="b199f-125">Validate the quality order</span></span>
1. <span data-ttu-id="b199f-126">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="b199f-126">Click Validate.</span></span>
2. <span data-ttu-id="b199f-127">Lauke „Patvirtino“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b199f-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b199f-128">Pasirinkite vartotoją, kuris atlieka patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="b199f-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="b199f-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b199f-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b199f-130">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="b199f-130">Click Select.</span></span>
5. <span data-ttu-id="b199f-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b199f-131">Click OK.</span></span>
6. <span data-ttu-id="b199f-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b199f-132">Close the page.</span></span>

