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
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470838"
---
# <a name="production-planning"></a><span data-ttu-id="3be1e-103">Gamybos planavimas</span><span class="sxs-lookup"><span data-stu-id="3be1e-103">Production planning</span></span>

<span data-ttu-id="3be1e-104">Planavimo optimizavimas palaiko kelis gamybos scenarijus.</span><span class="sxs-lookup"><span data-stu-id="3be1e-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="3be1e-105">Jei pereinate iš esamo, įtaisyto bendrojo planavimo mechanizmo, svarbu žinoti apie pasikeitusį veikimo būdą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="3be1e-106">Toliau pateiktame vaizdo įraše pateikiamas trumpas įvadas į kai kurias sąvokas, aptartas šioje temoje: [Dynamics 365 Supply Chain Management: Planavimo optimizavimo patobulinimai](https://youtu.be/u1pcmZuZBTw).</span><span class="sxs-lookup"><span data-stu-id="3be1e-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="3be1e-107">Suplanuoti gamybos užsakymai</span><span class="sxs-lookup"><span data-stu-id="3be1e-107">Planned production orders</span></span>

<span data-ttu-id="3be1e-108">Kai bendrasis planavimas sukuria suplanuotus užsakymus reikalavimų įgyvendinimui, užsakymo tipas nustatomas pagal lauko **Suplanuoto užsakymo tipas** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3be1e-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="3be1e-109">Jei lauke **Suplanuoto užsakymo tipas** nustatyta *Gamyba*, kuriami suplanuoti gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="3be1e-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="3be1e-110">Į šiuos suplanuotus gamybos užsakymus įtraukta informacija apie aktyvias komplektavimo specifikacijas (KS) ir maršruto ID iš susijusios gamybos sąrankos.</span><span class="sxs-lookup"><span data-stu-id="3be1e-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="3be1e-111">KS reikalavimai</span><span class="sxs-lookup"><span data-stu-id="3be1e-111">Requirements from BOMs</span></span>

<span data-ttu-id="3be1e-112">Bendrojo planavimo metu atsižvelgiama į KS informaciją.</span><span class="sxs-lookup"><span data-stu-id="3be1e-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="3be1e-113">Plano išeiga apima medžiagų tiekimą, padengiantį susijusią medžiagų paklausą gamybai.</span><span class="sxs-lookup"><span data-stu-id="3be1e-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="3be1e-114">Bendrojo planavimo metu dabartinė ir aktyvi KS naudojama nustatyti gamybai reikalingas medžiagas.</span><span class="sxs-lookup"><span data-stu-id="3be1e-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="3be1e-115">Šis veiksmas atliekamas visuose KS struktūros lygiuose, susijusiuose su reikalaujamu gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="3be1e-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="3be1e-116">Medžiagų poreikis įvykdomas naudojant turimas atsargas, esamą tiekimą pagal užsakymą ir patvirtintus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="3be1e-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="3be1e-117">Jei bet kurioje vietoje reikia papildomos medžiagos, sukuriamas suplanuotas užsakymas poreikiui patenkinti.</span><span class="sxs-lookup"><span data-stu-id="3be1e-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="3be1e-118">Planavimas patvirtinimo metu</span><span class="sxs-lookup"><span data-stu-id="3be1e-118">Scheduling during firming</span></span>

<span data-ttu-id="3be1e-119">Suplanuoti gamybos užsakymai apima maršruto ID, kuris būtinas gamybai planavimui.</span><span class="sxs-lookup"><span data-stu-id="3be1e-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="3be1e-120">Tačiau planavimo vykdymo metu laukiama planavimo palaikymo patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="3be1e-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="3be1e-121">Maršruto ID yra naudojamas gamybos užsakymams planuoti patvirtinimo metu.</span><span class="sxs-lookup"><span data-stu-id="3be1e-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="3be1e-122">Todėl suplanuotų gamybos užsakymų gamybos laikas gali skirtis nuo iš jų sugeneruojamų, susijusių suplanuotų ar patvirtintų gamybos užsakymų, gamybos laiko, kaip aprašyta čia:</span><span class="sxs-lookup"><span data-stu-id="3be1e-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="3be1e-123">**Suplanuotas gamybos užsakymas** – gamybos laikas paremtas statiniu išleisto produkto gamybos laiku.</span><span class="sxs-lookup"><span data-stu-id="3be1e-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="3be1e-124">**Patvirtintas gamybos užsakymas** – gamybos laikas paremtas planavimu, naudojančiu maršruto informaciją ir susijusius išteklių apribojimus.</span><span class="sxs-lookup"><span data-stu-id="3be1e-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="3be1e-125">Norėdami gauti daugiau informacijos apie numatomą funkcijos prieinamumą, žiūrėkite [Planavimo optimizavimo pritaikymo analizė](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3be1e-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="3be1e-126">Jei jums reikalingos gamybos funkcijos, kurios dar nėra prieinamos planavimo optimizavime, galite toliau naudoti įtaisytąjį bendrojo planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="3be1e-127">Išimtis nebūtina.</span><span class="sxs-lookup"><span data-stu-id="3be1e-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="3be1e-128">Atidėjimai</span><span class="sxs-lookup"><span data-stu-id="3be1e-128">Delays</span></span>

<span data-ttu-id="3be1e-129">Jei reikiamos medžiagos gamybos laikas yra ilgesnis nei laikotarpis nuo šiandienos datos iki medžiagų poreikio datos, suplanuotas reikiamos medžiagos užsakymas ir susijęs gamybos užsakymas bus atidėti.</span><span class="sxs-lookup"><span data-stu-id="3be1e-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="3be1e-130">Suplanuotų užsakymų atidėjimas (dienomis) skaičiuojamas pagal išleisto produkto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="3be1e-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="3be1e-131">Atidėjimo informacija tada bus perduodama per visus KS struktūros lygius.</span><span class="sxs-lookup"><span data-stu-id="3be1e-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="3be1e-132">Todėl jūs galite sekti atidėtų žaliavų poveikį iki pat kliento pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="3be1e-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="3be1e-133">Suplanuotų užsakymų modifikavimas</span><span class="sxs-lookup"><span data-stu-id="3be1e-133">Modifying planned orders</span></span>

<span data-ttu-id="3be1e-134">Keisdami suplanuoto užsakymo informaciją, gausite tokį pranešimą: „Atkreipkite dėmesį, kad neautomatinių pakeitimų poveikis suplanuotiems užsakymams nebus rodomas likusioje plano srityje iki kito bendrojo planavimo vykdymo.”</span><span class="sxs-lookup"><span data-stu-id="3be1e-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="3be1e-135">Jei norite pakeisti suplanuoto užsakymo informaciją ir pamatyti poveikį susijusiems medžiagų reikalavimams, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3be1e-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="3be1e-136">Atnaujinkite suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-136">Update the planned order.</span></span>
2. <span data-ttu-id="3be1e-137">Patvirtinkite suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-137">Approve the planned order.</span></span>
3. <span data-ttu-id="3be1e-138">Vykdykite bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-138">Run master planning.</span></span>

<span data-ttu-id="3be1e-139">Kai vykdote bendrąjį planavimą, neturėtumėte naudoti filtrų, jeigu įtraukti suplanuoti gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="3be1e-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="3be1e-140">Daugiau informacijos žiūrėkite tolesniame šios temos skyriuje [Filtrai](#filters).</span><span class="sxs-lookup"><span data-stu-id="3be1e-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="3be1e-141">Jei suplanuoto užsakymo pristatymo data pakeičiama į vėlesnę, poreikis gali būti iškviestas naujam suplanuotam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="3be1e-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="3be1e-142">Taip nutinka, kai dėl naujos tiekimo datos atidedamas iškviestas poreikis, tačiau atsižvelgiant į gamybos laiko parametrus, atidėjimo galima išvengti.</span><span class="sxs-lookup"><span data-stu-id="3be1e-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="3be1e-143">Išskleidimo puslapis</span><span class="sxs-lookup"><span data-stu-id="3be1e-143">Explosion page</span></span>

<span data-ttu-id="3be1e-144">Galite naudoti **Išskleidimo** puslapį analizuoti poreikiui, kuris reikalingas konkrečiam arba suplanuotam gamybos užsakymui, susijusiai aprėpčiai ir iškvietimo informacijai.</span><span class="sxs-lookup"><span data-stu-id="3be1e-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="3be1e-145">Informacija **Išskleidimo** puslapyje atnaujinama bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="3be1e-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="3be1e-146">Negalite atnaujinti informacijos tiesiogiai iš **Išskleidimo** puslapio.</span><span class="sxs-lookup"><span data-stu-id="3be1e-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="3be1e-147">Filtrai</span><span class="sxs-lookup"><span data-stu-id="3be1e-147">Filters</span></span>

<span data-ttu-id="3be1e-148">Planavimo scenarijuose, apimančiuose gamybą, rekomenduojame vengti vykdyti filtruotą bendrąjį planavimą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="3be1e-149">Norėdami užtikrinti, kad planavimo optimizavimas turi teisingam rezultatui apskaičiuoti reikalingą informaciją, turite įtraukti visus produktus, kurie turi bet kokį ryšį su produktais visoje suplanuoto užsakymo KS struktūroje.</span><span class="sxs-lookup"><span data-stu-id="3be1e-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="3be1e-150">Nors priklausomos antrinės prekės yra automatiškai aptinkamos ir įtraukiamos į bendrojo planavimo vykdymą, kai naudojamas įtaisytasis bendrojo planavimo mechanizmas, planavimo optimizavimas neatlieka šio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="3be1e-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="3be1e-151">Pavyzdžiui, jei vienas varžtas iš produkto A KS struktūros taip pat naudojamas produktui B gaminti, visi A ir B produktų KS struktūros produktai turi būti įtraukti į filtrą.</span><span class="sxs-lookup"><span data-stu-id="3be1e-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="3be1e-152">Kadangi gali būti labai sudėtinga užtikrinti, kad visi produktai būtų filtro dalis, rekomenduojame vengti filtruoto bendrojo planavimo vykdymo, kai įtraukiami gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="3be1e-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]