---
title: Trumpalaikio išrinkimo elementų perskirstymo nustatymas
description: Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916765"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="c047f-103">Trumpalaikio išrinkimo elementų perskirstymo nustatymas</span><span class="sxs-lookup"><span data-stu-id="c047f-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c047f-104">Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka.</span><span class="sxs-lookup"><span data-stu-id="c047f-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="c047f-105">Galima naudoti automatinio pakartotinio paskirstymo procesą, kuris naudoja vietos nurodymus prekėms gauti, jei jų yra kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="c047f-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="c047f-106">Kitu atveju, kai naudojamas neautomatinis pakartotinis paskirstymas, mobiliajame įrenginyje rodomas vietų su turimu kiekiu sąrašas, todėl sandėlio darbuotojas gali pasirinkti, kurios vietos atsargas naudoti.</span><span class="sxs-lookup"><span data-stu-id="c047f-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="c047f-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="c047f-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="c047f-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="c047f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="c047f-109">Nustatyti darbo išimtis</span><span class="sxs-lookup"><span data-stu-id="c047f-109">Set up work exceptions</span></span>
1. <span data-ttu-id="c047f-110">**Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbas > Darbo išimtys**.</span><span class="sxs-lookup"><span data-stu-id="c047f-110">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="c047f-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c047f-111">Click **New**.</span></span> <span data-ttu-id="c047f-112">Galima apibrėžti kelias darbo išimtis su skirtingomis prekių perskirstymo strategijomis, norint suteikti sandėlio darbuotojui galimybę strategiją pasirinkti pagal su jo apdorojama siunta susijusius poreikius.</span><span class="sxs-lookup"><span data-stu-id="c047f-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="c047f-113">Lauke **Darbo išimties kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c047f-113">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="c047f-114">Nurodykite darbo išimties pavadinimą nurodydami, kam ji naudojama.</span><span class="sxs-lookup"><span data-stu-id="c047f-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="c047f-115">Pavyzdžiui, Neautomatinis nevisiškas paėmimas.</span><span class="sxs-lookup"><span data-stu-id="c047f-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="c047f-116">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c047f-116">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="c047f-117">Lauke **Išimties tipas** pasirinkite Nevisiškas paėmimas.</span><span class="sxs-lookup"><span data-stu-id="c047f-117">In the **Exception** type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="c047f-118">Pažymėkite žymės langelį **Koreguoti atsargas**.</span><span class="sxs-lookup"><span data-stu-id="c047f-118">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="c047f-119">Ši parinktis nurodo, kad atsargų lygis bus automatiškai nustatytas į 0 vietoje, iš kurioje bus vykdomas nevisiškas paėmimas.</span><span class="sxs-lookup"><span data-stu-id="c047f-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="c047f-120">Lauke **Numatytojo koregavimo tipo kodas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c047f-120">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="c047f-121">Pavyzdžiui, USMF galite pasirinkti Šalinti Res Adj Out.</span><span class="sxs-lookup"><span data-stu-id="c047f-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="c047f-122">Lauke **Prekių perskirstymas** pasirinkite Neautomatinis.</span><span class="sxs-lookup"><span data-stu-id="c047f-122">In the **Item reallocation** field, select 'Manual'.</span></span> <span data-ttu-id="c047f-123">Jei pasirinksite Neautomatinis arba Automatinis ir neautomatinis, sandėlio darbuotojui reikia įjungti neautomatinio perskirstymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="c047f-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="c047f-124">Darbuotojo nustatymas naudoti neautomatinį perskirstymą</span><span class="sxs-lookup"><span data-stu-id="c047f-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="c047f-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c047f-125">Close the page.</span></span>
2. <span data-ttu-id="c047f-126">**Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="c047f-126">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="c047f-127">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="c047f-127">Click **Edit**.</span></span>
4. <span data-ttu-id="c047f-128">Sąraše pasirinkite 24 darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="c047f-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="c047f-129">Išplėskite „fastTab“ **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="c047f-129">Expand the **Work** fastTab.</span></span>
6. <span data-ttu-id="c047f-130">Lauke **Leisti neautomatinį prekių perskirstymą** pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c047f-130">Select 'Yes' in the **Allow manual item reallocation** field.</span></span>

