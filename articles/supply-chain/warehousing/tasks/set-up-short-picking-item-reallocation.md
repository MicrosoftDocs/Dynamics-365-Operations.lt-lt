---
title: Prekių perskirstymo nustatymas nevisiško paėmimo atveju
description: Ši procedūra padeda įgalinti sandėlio darbuotojus greitai surasti kitas vietas, jei toje vietoje, į kurią jie buvo nukreipti, nėra pakankamai atsargų.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015969"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="18bdf-103">Prekių perskirstymo nustatymas nevisiško paėmimo atveju</span><span class="sxs-lookup"><span data-stu-id="18bdf-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18bdf-104">Ši procedūra padeda įgalinti sandėlio darbuotojus greitai rasti kitas vietas, jei toje vietoje, į kurią jie buvo nukreipti, nėra pakankamai atsargų.</span><span class="sxs-lookup"><span data-stu-id="18bdf-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="18bdf-105">Perskirstymo procesą kontroliuoja **Darbo išimtys** ir naudoja sandėlio **darbuotojas.**</span><span class="sxs-lookup"><span data-stu-id="18bdf-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="18bdf-106">Galima naudoti Automatinius, Neautomatinius arba abu perskirstymo procesus:</span><span class="sxs-lookup"><span data-stu-id="18bdf-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="18bdf-107">Automatiniame perskirstyme naudojami vietos nurodymai siekiant sužinoti, ar prekės yra pasiekiamos kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="18bdf-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="18bdf-108">Jei įmanoma, darbas bus atnaujintas ir „Warehousing“ programos naudotojas bus nukreiptas į kitą vietą.</span><span class="sxs-lookup"><span data-stu-id="18bdf-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="18bdf-109">Neautomatinis perskirstymas leidžia „Warehousing“ programos naudototojui pasirinkti iš vienos ar daugiau vietų, kuriose yra nerezervuoti prekių kiekiai.</span><span class="sxs-lookup"><span data-stu-id="18bdf-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="18bdf-110">Automatinis ir neautomatinis – jei sistemai nepavyko atlikti automatinio perskirstymo, o vietos su nerezervuotais kiekiais yra pasiekiamos, naudotojas bus paragintas pasirinkti vietą.</span><span class="sxs-lookup"><span data-stu-id="18bdf-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="18bdf-111">Nustatyti užduočių išimtis</span><span class="sxs-lookup"><span data-stu-id="18bdf-111">Set up work exceptions</span></span>
<span data-ttu-id="18bdf-112">Galima apibrėžti keletą užduočių išimčių naudojant skirtingas prekių perskirstymo strategijas įgalinti sandėlio darbuotoją pasirinkti vieną iš jų, atsižvelgiant į jo apdorojamos siuntos specifikacijas.</span><span class="sxs-lookup"><span data-stu-id="18bdf-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="18bdf-113">Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="18bdf-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="18bdf-114">**Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Užduotys > Užduočių išimtys**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-114">In the **Navigation pane** , go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="18bdf-115">Spustelėkite **Naujas**</span><span class="sxs-lookup"><span data-stu-id="18bdf-115">Click **New**</span></span> 
3. <span data-ttu-id="18bdf-116">Lauke **Užduoties išimties kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18bdf-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="18bdf-117">Tai bus šios išimties pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="18bdf-117">This will be the title of this exception .</span></span> <span data-ttu-id="18bdf-118">Pavyzdžiui, Neautomatinis nevisiškas paėmimas.</span><span class="sxs-lookup"><span data-stu-id="18bdf-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="18bdf-119">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18bdf-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="18bdf-120">Tai bus trumpas šios išimties naudojimo aprašas.</span><span class="sxs-lookup"><span data-stu-id="18bdf-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="18bdf-121">Pavyzdžiui, „Trumpalaikis išrinkimas“ – prekė yra nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="18bdf-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="18bdf-122">**Išimties** tipo lauke pasirinkite **Trumpalaikis išrinkimas**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="18bdf-123">Pažymėkite žymės langelį **Koreguoti atsargas**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="18bdf-124">Ši parinktis automatiškai nustatys atsargų lygį į 0 toje vietoje, iš kurios bus vykdomas trumpalaikis išrinkimas.</span><span class="sxs-lookup"><span data-stu-id="18bdf-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="18bdf-125">Lauke **Numatytojo koregavimo tipo kodas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="18bdf-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="18bdf-126">Pavyzdžiui, programoje USMF galite pasirinkti **Pašalinti rezervacijas Adj Out**. Kiekviename koregavimo tipo kode yra keturios charakteristikos: pavadinimas, aprašas, atsargų žurnalo pavadinimas ir **Pašalinti rezervacijas**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="18bdf-127">Jei funkcija **Pašalinti rezervacijas** yra įjungta, trumpalaikio išrinkimo eilutės rezervacijos bus pašalintos.</span><span class="sxs-lookup"><span data-stu-id="18bdf-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="18bdf-128">Lauke **Prekių perskirstymas** pasirinkite reikšmę, pavyzdžiui, Neautomatinis.</span><span class="sxs-lookup"><span data-stu-id="18bdf-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="18bdf-129">Jei pasirinksite Neautomatinis arba Automatinis ir neautomatinis, reikia įgalinti sandėlio darbuotoją reikia naudoti neautomatinio perskirstymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="18bdf-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="18bdf-130">Darbuotojo nustatymas naudoti neautomatinį perskirstymą</span><span class="sxs-lookup"><span data-stu-id="18bdf-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="18bdf-131">Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="18bdf-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="18bdf-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="18bdf-132">Close the page.</span></span>
2. <span data-ttu-id="18bdf-133">**Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-133">In the **Navigation pane** , go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="18bdf-134">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-134">Click **Edit**.</span></span>
4. <span data-ttu-id="18bdf-135">Pasirinkite darbuotoją iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="18bdf-135">In the list, select worker.</span></span> <span data-ttu-id="18bdf-136">Pavyzdžiui, Julija Funderburk.</span><span class="sxs-lookup"><span data-stu-id="18bdf-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="18bdf-137">Išplėskite „FastTab“ skirtuką **Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="18bdf-138">Pasirinkite **Vartotojo ID** iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="18bdf-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="18bdf-139">Pavyzdžiui, 24.</span><span class="sxs-lookup"><span data-stu-id="18bdf-139">For example, 24.</span></span>
7. <span data-ttu-id="18bdf-140">Išplėskite „FastTab“ skirtuką **Užduotys**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="18bdf-141">Lauke **Leisti neautomatinį prekių perskirstymą** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="18bdf-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
