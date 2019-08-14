---
title: Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją
description: Šioje temoje aprašomas savikainos konfigūravimas naudojant „Microsoft Dynamics 365 for Retail“ paskirstytų užsakymų tvarkymo (DOM) funkciją.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 80e7a033467c3d94d55f06daa05f99bd27e19a29
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606784"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="ba151-103">Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją</span><span class="sxs-lookup"><span data-stu-id="ba151-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba151-104">Siekdamos nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymą, organizacijos apsvarsto keletą savikainos komponentų.</span><span class="sxs-lookup"><span data-stu-id="ba151-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="ba151-105">Kai kurie iš šių savikainos komponentų yra siuntimo savikaina, tvarkymo savikaina ir pakavimo savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="ba151-106">Siekiant nustatyti įvykdymo vietą, apskaičiuojamas šių savikainų derinys.</span><span class="sxs-lookup"><span data-stu-id="ba151-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="ba151-107">Kai, naudojant pirmąją „Microsoft Dynamics 365 for Retail“ paskirstytų užsakymų tvarkymo (DOM) funkciją, optimizuotas užsakymų priskyrimas įvykdymo vietoms, buvo atsižvelgiama tik į atstumą.</span><span class="sxs-lookup"><span data-stu-id="ba151-107">When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="ba151-108">Nors atstumas gali būti susijęs su savikaina, tai nėra tas pats.</span><span class="sxs-lookup"><span data-stu-id="ba151-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="ba151-109">Pavyzdžiui, kai atstumas yra toks pats, siuntimo naktį būdas kainuoja daugiau, nei siuntimas per tris dienas ar siuntimas per septynias dienas.</span><span class="sxs-lookup"><span data-stu-id="ba151-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="ba151-110">Savikainos konfigūravimo funkcija mažmenininkams leidžia nustatyti ir konfigūruoti papildomus savikainos komponentus, kurie bus apskaičiuojami ir į kuriuos bus atsižvelgiama siekiant nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymų eilutes.</span><span class="sxs-lookup"><span data-stu-id="ba151-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="ba151-111">Kai sukonfigūruojami savikainos komponentai, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė naudoja tik tas savikainos apibrėžtis.</span><span class="sxs-lookup"><span data-stu-id="ba151-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="ba151-112">Atstumo komponento ji nelaiko savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="ba151-113">Tačiau, jei savikainos komponentų nėra sukonfigūruota, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė atstumo komponentą kaip savikainą naudoja.</span><span class="sxs-lookup"><span data-stu-id="ba151-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="ba151-114">Savikainos komponentų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ba151-114">Set up cost components</span></span>

<span data-ttu-id="ba151-115">Sistemoje galima nustatyti du pagrindinius savikainos komponentų tipus: **Siuntimo** ir **Kitas**.</span><span class="sxs-lookup"><span data-stu-id="ba151-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="ba151-116">Abu savikainos komponentų tipai palaiko keletą skaičiavimo pagrindų, kaip parodyta tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="ba151-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ba151-117">Savikainos komponento tipas</span><span class="sxs-lookup"><span data-stu-id="ba151-117">Cost component type</span></span></th>
<th><span data-ttu-id="ba151-118">Skaičiavimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="ba151-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ba151-119">Siuntimo</span><span class="sxs-lookup"><span data-stu-id="ba151-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ba151-120">Paprastas</span><span class="sxs-lookup"><span data-stu-id="ba151-120">Simple</span></span></li>
<li><span data-ttu-id="ba151-121">Pakopinis</span><span class="sxs-lookup"><span data-stu-id="ba151-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ba151-122">Kitas</span><span class="sxs-lookup"><span data-stu-id="ba151-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ba151-123">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="ba151-123">Sales order</span></span></li>
<li><span data-ttu-id="ba151-124">Pardavimo eilutė</span><span class="sxs-lookup"><span data-stu-id="ba151-124">Sales line</span></span></li>
<li><span data-ttu-id="ba151-125">Vieta</span><span class="sxs-lookup"><span data-stu-id="ba151-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="ba151-126">Siuntimo savikainos komponento tipas</span><span class="sxs-lookup"><span data-stu-id="ba151-126">Shipping cost component type</span></span>

<span data-ttu-id="ba151-127">Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo **Siuntimo** derinį ir siuntimo savikainos skaičiavimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="ba151-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="ba151-128">Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.</span><span class="sxs-lookup"><span data-stu-id="ba151-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="ba151-129">Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Paprastas</span><span class="sxs-lookup"><span data-stu-id="ba151-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="ba151-130">Jei yra naudojamas savikainos komponento tipo **Siuntimo** ir skaičiavimo pagrindo **Paprastas** derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą.</span><span class="sxs-lookup"><span data-stu-id="ba151-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="ba151-131">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="ba151-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ba151-132">**Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ba151-133">**Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ba151-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ba151-134">**Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</span><span class="sxs-lookup"><span data-stu-id="ba151-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ba151-135">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ba151-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ba151-136">**Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="ba151-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ba151-137">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</span><span class="sxs-lookup"><span data-stu-id="ba151-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ba151-138">**Įmonė** – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="ba151-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ba151-139">Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="ba151-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ba151-140">**Pristatymo būdai** – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="ba151-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ba151-141">**Skaičiavimo tipas** – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="ba151-142">Palaikomi du tolesni skaičiavimo tipai.</span><span class="sxs-lookup"><span data-stu-id="ba151-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ba151-143">**Fiksuotasis** – pristatymo būdui naudojama fiksuotoji savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ba151-144">Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke **Savikaina**.</span><span class="sxs-lookup"><span data-stu-id="ba151-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ba151-145">**Pagal atstumo vienetą** – pristatymo būdo savikaina apskaičiuojama kaip lauke **Savikaina** nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.</span><span class="sxs-lookup"><span data-stu-id="ba151-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ba151-146">**Savikaina** – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku **Skaičiavimo tipas** apskaičiuojama pristatymo būdo savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="ba151-147">Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Pakopinis</span><span class="sxs-lookup"><span data-stu-id="ba151-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="ba151-148">Jei yra naudojamas savikainos komponento tipo **Siuntimo** ir skaičiavimo pagrindo **Pakopinis** derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą.</span><span class="sxs-lookup"><span data-stu-id="ba151-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="ba151-149">Tačiau šiame derinyje atstumas nustatomas pagal pakopinį atstumų intervalą.</span><span class="sxs-lookup"><span data-stu-id="ba151-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="ba151-150">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="ba151-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ba151-151">**Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ba151-152">**Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ba151-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ba151-153">**Numatytoji savikaina** – nurodykite pristatymo būdo savikainą, kuri turi būti naudojama, jei atstumas tarp pristatymo adreso ir vietos nepatenka į jokį iš pristatymo būdo pakopinių atstumų.</span><span class="sxs-lookup"><span data-stu-id="ba151-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="ba151-154">**Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</span><span class="sxs-lookup"><span data-stu-id="ba151-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ba151-155">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ba151-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ba151-156">**Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="ba151-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ba151-157">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</span><span class="sxs-lookup"><span data-stu-id="ba151-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ba151-158">**Įmonė** – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="ba151-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ba151-159">Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="ba151-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ba151-160">**Pristatymo būdai** – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="ba151-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ba151-161">**Atstumo tipas** – nurodykite, ar pakopinis atstumas apibrėžiamas kaip atstumas oru, ar atstumas keliais.</span><span class="sxs-lookup"><span data-stu-id="ba151-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="ba151-162">**Atstumo vienetai** – nurodyti vienetą, kuriuo matuojamas pakopinis atstumas.</span><span class="sxs-lookup"><span data-stu-id="ba151-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="ba151-163">**Atstumas nuo** – nurodykite pakopinio atstumo intervalo pradžią.</span><span class="sxs-lookup"><span data-stu-id="ba151-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="ba151-164">**Atstumas iki** – nurodykite pakopinio atstumo intervalo pabaigą.</span><span class="sxs-lookup"><span data-stu-id="ba151-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="ba151-165">**Skaičiavimo tipas** – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo ir pakopinio atstumo savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="ba151-166">Palaikomi du tolesni skaičiavimo tipai.</span><span class="sxs-lookup"><span data-stu-id="ba151-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ba151-167">**Fiksuotasis** – pristatymo būdui naudojama fiksuotoji savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ba151-168">Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke **Savikaina**.</span><span class="sxs-lookup"><span data-stu-id="ba151-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ba151-169">**Pagal atstumo vienetą** – pristatymo būdo ir pakopinio atstumo savikaina apskaičiuojama kaip lauke **Savikaina** nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.</span><span class="sxs-lookup"><span data-stu-id="ba151-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ba151-170">**Savikaina** – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku **Skaičiavimo tipas** apskaičiuojama pristatymo būdo savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="ba151-171">Kai nustatote pakopinius atstumus, sistema patikrina, kad atstumų netrūktų ir kad jie nepersidengtų.</span><span class="sxs-lookup"><span data-stu-id="ba151-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="ba151-172">Naudojamas tam tikro pristatymo būdo atstumo tipas turi būti toks pats visuose pakopiniuose atstumuose.</span><span class="sxs-lookup"><span data-stu-id="ba151-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="ba151-173">Savikainos komponento tipas Kitas</span><span class="sxs-lookup"><span data-stu-id="ba151-173">Other cost component type</span></span>

<span data-ttu-id="ba151-174">Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo **Kitas** derinį ir kitą su siuntimu nesusijusių savikainų tipą.</span><span class="sxs-lookup"><span data-stu-id="ba151-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="ba151-175">Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.</span><span class="sxs-lookup"><span data-stu-id="ba151-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="ba151-176">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="ba151-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="ba151-177">Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Pardavimo užsakymas** derinį, pardavimo užsakymo lygiu apibrėžiamos su siuntimu nesusijusios savikainos.</span><span class="sxs-lookup"><span data-stu-id="ba151-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="ba151-178">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="ba151-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ba151-179">**Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ba151-180">**Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ba151-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ba151-181">**Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</span><span class="sxs-lookup"><span data-stu-id="ba151-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ba151-182">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ba151-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ba151-183">**Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="ba151-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ba151-184">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</span><span class="sxs-lookup"><span data-stu-id="ba151-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ba151-185">**Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo lygiu.</span><span class="sxs-lookup"><span data-stu-id="ba151-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="ba151-186">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo eilutė</span><span class="sxs-lookup"><span data-stu-id="ba151-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="ba151-187">Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Pardavimo eilutė** derinį, pardavimo užsakymo eilutės lygiu apibrėžiamos su siuntimu nesusijusios savikainos.</span><span class="sxs-lookup"><span data-stu-id="ba151-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="ba151-188">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="ba151-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ba151-189">**Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ba151-190">**Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ba151-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ba151-191">**Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</span><span class="sxs-lookup"><span data-stu-id="ba151-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ba151-192">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ba151-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ba151-193">**Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="ba151-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ba151-194">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</span><span class="sxs-lookup"><span data-stu-id="ba151-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ba151-195">**Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo eilutės lygiu.</span><span class="sxs-lookup"><span data-stu-id="ba151-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="ba151-196">Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Vieta</span><span class="sxs-lookup"><span data-stu-id="ba151-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="ba151-197">Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Vieta** derinį, apibrėžiamos vietų grupės arba atskiros vietos su siuntimu nesusijusios savikainos.</span><span class="sxs-lookup"><span data-stu-id="ba151-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="ba151-198">Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="ba151-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ba151-199">**Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ba151-200">**Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="ba151-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ba151-201">**Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu.</span><span class="sxs-lookup"><span data-stu-id="ba151-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ba151-202">Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="ba151-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ba151-203">**Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="ba151-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ba151-204">DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.</span><span class="sxs-lookup"><span data-stu-id="ba151-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ba151-205">**Įvykdymo grupė** – nurodykite vietų grupę, kuriai apibrėžta su siuntimu nesusijusi savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="ba151-206">**Įvykdymo vieta** – nurodykite vietą, kuriai apibrėžta su siuntimu nesusijusi savikaina.</span><span class="sxs-lookup"><span data-stu-id="ba151-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba151-207">Toje pačioje vieta pagrįstų skaičiavimo kriterijų eilutėje negalite nurodyti ir įvykdymo grupės, ir įvykdymo vietos.</span><span class="sxs-lookup"><span data-stu-id="ba151-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="ba151-208">**Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę įvykdymo grupės lygiu arba įvykdymo vietos lygiu.</span><span class="sxs-lookup"><span data-stu-id="ba151-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba151-209">Norint, kad vykdoma DOM funkcija svarstytų šias savikainas, į atitinkamą įvykdymo profilį turite įtraukti savikainos faktorių.</span><span class="sxs-lookup"><span data-stu-id="ba151-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>