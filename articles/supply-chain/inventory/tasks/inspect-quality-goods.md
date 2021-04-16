---
title: Prekių kokybės tikrinimas
description: Šioje temoje paaiškinama, kaip apdoroti kokybės užsakymą.
author: perlynne
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e7156e5c57d5f983564cc966b4108f1180ff8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825920"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="d2eca-103">Prekių kokybės tikrinimas</span><span class="sxs-lookup"><span data-stu-id="d2eca-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2eca-104">Šioje temoje paaiškinama, kaip apdoroti kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="d2eca-105">Šį vadovą galite vykdyti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="d2eca-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="d2eca-106">Prieš pradėdami šį procedūros pavyzdį, turite patvirtinti pirkimo užsakymą „000016“ ir užregistruoti produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="d2eca-107">Tai automatiškai sukurs kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-107">This will automatically create a quality order.</span></span> <span data-ttu-id="d2eca-108">Kokybės patikrinimus paprastai atlieka kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="d2eca-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="d2eca-109">Pasirinkti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="d2eca-109">Select a quality order</span></span>
1. <span data-ttu-id="d2eca-110">Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Periodinės užduotys > Kokybės valdymas > Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="d2eca-111">Pasirinkite kokybės užsakymą, sukurtą prieš jums pradedant šią procedūrą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="d2eca-112">Įrašyti tikrinimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="d2eca-112">Record test results</span></span>
1. <span data-ttu-id="d2eca-113">Pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-113">Select **Results**.</span></span>
2. <span data-ttu-id="d2eca-114">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-114">Select **Edit**.</span></span>
3. <span data-ttu-id="d2eca-115">Lauke **Rezultatų kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d2eca-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="d2eca-116">Lauke **Baigtis** išplečiamajame meniu pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="d2eca-117">Šiame pavyzdyje rezultatas priklauso nuo iš anksto nustatytos baigties.</span><span class="sxs-lookup"><span data-stu-id="d2eca-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="d2eca-118">Paprastai įrašomas konkretesnis bandymo rezultatas, pavyzdžiui, dydis ar kitas matmuo.</span><span class="sxs-lookup"><span data-stu-id="d2eca-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="d2eca-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-119">Select **Save**.</span></span>
6. <span data-ttu-id="d2eca-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d2eca-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="d2eca-121">Tikrinti kokybės užsakymą</span><span class="sxs-lookup"><span data-stu-id="d2eca-121">Validate the quality order</span></span>
1. <span data-ttu-id="d2eca-122">Pasirinkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-122">Select **Validate**.</span></span>
2. <span data-ttu-id="d2eca-123">Lauke **Patikrino** išplečiamajame meniu pasirinkite vartotoją, kuris atlieka patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="d2eca-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="d2eca-124">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-124">Click **Select**.</span></span>
4. <span data-ttu-id="d2eca-125">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d2eca-125">Select **OK**.</span></span>
5. <span data-ttu-id="d2eca-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d2eca-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]