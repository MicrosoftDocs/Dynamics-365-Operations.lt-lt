---
title: Gamybos planavimas
description: Šioje temoje aprašomas gamybos planavimas ir paaiškinama, kaip modifikuoti suplanuotus gamybos užsakymus naudojant planavimo optimizavimą.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992400"
---
# <a name="production-planning"></a><span data-ttu-id="4a52c-103">Gamybos planavimas</span><span class="sxs-lookup"><span data-stu-id="4a52c-103">Production planning</span></span>

<span data-ttu-id="4a52c-104">Planavimo optimizavimas palaiko kelis gamybos scenarijus.</span><span class="sxs-lookup"><span data-stu-id="4a52c-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="4a52c-105">Jei pereinate iš esamo, įtaisyto bendrojo planavimo mechanizmo, svarbu žinoti apie pasikeitusį veikimo būdą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="4a52c-106">Suplanuoti gamybos užsakymai</span><span class="sxs-lookup"><span data-stu-id="4a52c-106">Planned production orders</span></span>

<span data-ttu-id="4a52c-107">Kai bendrasis planavimas sukuria suplanuotus užsakymus reikalavimų įgyvendinimui, užsakymo tipas nustatomas pagal lauko **Suplanuoto užsakymo tipas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a52c-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="4a52c-108">Jei lauke **Suplanuoto užsakymo tipas** nustatyta *Gamyba*, kuriami suplanuoti gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4a52c-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="4a52c-109">Į šiuos suplanuotus gamybos užsakymus įtraukta informacija apie aktyvias komplektavimo specifikacijas (KS) ir maršruto ID iš susijusios gamybos sąrankos.</span><span class="sxs-lookup"><span data-stu-id="4a52c-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="4a52c-110">KS reikalavimai</span><span class="sxs-lookup"><span data-stu-id="4a52c-110">Requirements from BOMs</span></span>

<span data-ttu-id="4a52c-111">Bendrojo planavimo metu atsižvelgiama į KS informaciją.</span><span class="sxs-lookup"><span data-stu-id="4a52c-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="4a52c-112">Plano išeiga apima medžiagų tiekimą, padengiantį susijusią medžiagų paklausą gamybai.</span><span class="sxs-lookup"><span data-stu-id="4a52c-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="4a52c-113">Bendrojo planavimo metu dabartinė ir aktyvi KS naudojama nustatyti gamybai reikalingas medžiagas.</span><span class="sxs-lookup"><span data-stu-id="4a52c-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="4a52c-114">Šis veiksmas atliekamas visuose KS struktūros lygiuose, susijusiuose su reikalaujamu gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="4a52c-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="4a52c-115">Medžiagų poreikis įvykdomas naudojant turimas atsargas, esamą tiekimą pagal užsakymą ir patvirtintus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="4a52c-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="4a52c-116">Jei bet kurioje vietoje reikia papildomos medžiagos, sukuriamas suplanuotas užsakymas poreikiui patenkinti.</span><span class="sxs-lookup"><span data-stu-id="4a52c-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="4a52c-117">Planavimas patvirtinimo metu</span><span class="sxs-lookup"><span data-stu-id="4a52c-117">Scheduling during firming</span></span>

<span data-ttu-id="4a52c-118">Suplanuoti gamybos užsakymai apima maršruto ID, kuris būtinas gamybai planavimui.</span><span class="sxs-lookup"><span data-stu-id="4a52c-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="4a52c-119">Tačiau planavimo vykdymo metu laukiama planavimo palaikymo patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="4a52c-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="4a52c-120">Maršruto ID yra naudojamas gamybos užsakymams planuoti patvirtinimo metu.</span><span class="sxs-lookup"><span data-stu-id="4a52c-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="4a52c-121">Todėl suplanuotų gamybos užsakymų gamybos laikas gali skirtis nuo iš jų sugeneruojamų, susijusių suplanuotų ar patvirtintų gamybos užsakymų, gamybos laiko, kaip aprašyta čia:</span><span class="sxs-lookup"><span data-stu-id="4a52c-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="4a52c-122">**Suplanuotas gamybos užsakymas** – gamybos laikas paremtas statiniu išleisto produkto gamybos laiku.</span><span class="sxs-lookup"><span data-stu-id="4a52c-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="4a52c-123">**Patvirtintas gamybos užsakymas** – gamybos laikas paremtas planavimu, naudojančiu maršruto informaciją ir susijusius išteklių apribojimus.</span><span class="sxs-lookup"><span data-stu-id="4a52c-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="4a52c-124">Norėdami gauti daugiau informacijos apie numatomą funkcijos prieinamumą, žiūrėkite [Planavimo optimizavimo pritaikymo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4a52c-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="4a52c-125">Jei jums reikalingos gamybos funkcijos, kurios dar nėra prieinamos planavimo optimizavime, galite toliau naudoti įtaisytąjį bendrojo planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="4a52c-126">Išimtis nebūtina.</span><span class="sxs-lookup"><span data-stu-id="4a52c-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="4a52c-127">Atidėjimai</span><span class="sxs-lookup"><span data-stu-id="4a52c-127">Delays</span></span>

<span data-ttu-id="4a52c-128">Jei reikiamos medžiagos gamybos laikas yra ilgesnis nei laikotarpis nuo šiandienos datos iki medžiagų poreikio datos, suplanuotas reikiamos medžiagos užsakymas ir susijęs gamybos užsakymas bus atidėti.</span><span class="sxs-lookup"><span data-stu-id="4a52c-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="4a52c-129">Suplanuotų užsakymų atidėjimas (dienomis) skaičiuojamas pagal išleisto produkto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="4a52c-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="4a52c-130">Atidėjimo informacija tada bus perduodama per visus KS struktūros lygius.</span><span class="sxs-lookup"><span data-stu-id="4a52c-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="4a52c-131">Todėl jūs galite sekti atidėtų žaliavų poveikį iki pat kliento pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="4a52c-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="4a52c-132">Suplanuotų užsakymų modifikavimas</span><span class="sxs-lookup"><span data-stu-id="4a52c-132">Modifying planned orders</span></span>

<span data-ttu-id="4a52c-133">Keisdami suplanuoto užsakymo informaciją, gausite tokį pranešimą: „Atkreipkite dėmesį, kad neautomatinių pakeitimų poveikis suplanuotiems užsakymams nebus rodomas likusioje plano srityje iki kito bendrojo planavimo vykdymo.”</span><span class="sxs-lookup"><span data-stu-id="4a52c-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="4a52c-134">Jei norite pakeisti suplanuoto užsakymo informaciją ir pamatyti poveikį susijusiems medžiagų reikalavimams, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4a52c-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="4a52c-135">Atnaujinkite suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-135">Update the planned order.</span></span>
2. <span data-ttu-id="4a52c-136">Patvirtinkite suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-136">Approve the planned order.</span></span>
3. <span data-ttu-id="4a52c-137">Vykdykite bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-137">Run master planning.</span></span>

<span data-ttu-id="4a52c-138">Kai vykdote bendrąjį planavimą, neturėtumėte naudoti filtrų, jeigu įtraukti suplanuoti gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4a52c-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="4a52c-139">Daugiau informacijos žiūrėkite tolesniame šios temos skyriuje [Filtrai](#filters).</span><span class="sxs-lookup"><span data-stu-id="4a52c-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="4a52c-140">Jei suplanuoto užsakymo pristatymo data pakeičiama į vėlesnę, poreikis gali būti iškviestas naujam suplanuotam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="4a52c-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="4a52c-141">Taip nutinka, kai dėl naujos tiekimo datos atidedamas iškviestas poreikis, tačiau atsižvelgiant į gamybos laiko parametrus, atidėjimo galima išvengti.</span><span class="sxs-lookup"><span data-stu-id="4a52c-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="4a52c-142">Išskleidimo puslapis</span><span class="sxs-lookup"><span data-stu-id="4a52c-142">Explosion page</span></span>

<span data-ttu-id="4a52c-143">Galite naudoti **Išskleidimo** puslapį analizuoti poreikiui, kuris reikalingas konkrečiam arba suplanuotam gamybos užsakymui, susijusiai aprėpčiai ir iškvietimo informacijai.</span><span class="sxs-lookup"><span data-stu-id="4a52c-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="4a52c-144">Informacija **Išskleidimo** puslapyje atnaujinama bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="4a52c-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="4a52c-145">Negalite atnaujinti informacijos tiesiogiai iš **Išskleidimo** puslapio.</span><span class="sxs-lookup"><span data-stu-id="4a52c-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="4a52c-146">Filtrai</span><span class="sxs-lookup"><span data-stu-id="4a52c-146">Filters</span></span>

<span data-ttu-id="4a52c-147">Planavimo scenarijuose, apimančiuose gamybą, rekomenduojame vengti vykdyti filtruotą bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="4a52c-148">Norėdami užtikrinti, kad planavimo optimizavimas turi teisingam rezultatui apskaičiuoti reikalingą informaciją, turite įtraukti visus produktus, kurie turi bet kokį ryšį su produktais visoje suplanuoto užsakymo KS struktūroje.</span><span class="sxs-lookup"><span data-stu-id="4a52c-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="4a52c-149">Nors priklausomos antrinės prekės yra automatiškai aptinkamos ir įtraukiamos į bendrojo planavimo vykdymą, kai naudojamas įtaisytasis bendrojo planavimo mechanizmas, planavimo optimizavimas neatlieka šio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="4a52c-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="4a52c-150">Pavyzdžiui, jei vienas varžtas iš produkto A KS struktūros taip pat naudojamas produktui B gaminti, visi A ir B produktų KS struktūros produktai turi būti įtraukti į filtrą.</span><span class="sxs-lookup"><span data-stu-id="4a52c-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="4a52c-151">Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4a52c-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
