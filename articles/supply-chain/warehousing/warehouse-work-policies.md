---
title: Sandėlio darbo strategijų apžvalga
description: Sandėlio darbo strategijos kontroliuoja, ar sandėlio darbą kuria gamybos sandėlio procesai, remdamiesi darbo užsakymo tipu, atsargų vieta ir produktu.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7476cf797685feb4c50e3cefef4c53ca37b82dff
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251413"
---
# <a name="warehouse-work-policies-overview"></a><span data-ttu-id="26893-103">Sandėlio darbo strategijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="26893-103">Warehouse work policies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26893-104">Sandėlio darbo strategijos kontroliuoja, ar sandėlio darbą kuria gamybos sandėlio procesai, remdamiesi darbo užsakymo tipu, atsargų vieta ir produktu.</span><span class="sxs-lookup"><span data-stu-id="26893-104">Warehouse work policies control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="26893-105">Ši darbo strategija nustato, ar kuriamas gamybos sandėlio procesų sandėlio darbas.</span><span class="sxs-lookup"><span data-stu-id="26893-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="26893-106">Galite nustatyti darbo strategiją naudodami **darbo užsakymų tipų**, **atsargų vietos** ir **produkto** derinį.</span><span class="sxs-lookup"><span data-stu-id="26893-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="26893-107">Pavyzdžiui, produktas L0101 paskelbtas pagamintu išeigos vietoje 001.</span><span class="sxs-lookup"><span data-stu-id="26893-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="26893-108">Vėliau pagaminta prekė panaudojama vykdant kitą gamybos užsakymą išeigos vietoje 001.</span><span class="sxs-lookup"><span data-stu-id="26893-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="26893-109">Šiuo atveju galite nustatyti darbo strategiją, kurią taikant bei produktą L0101 paskelbus pagamintu išeigos vietoje 001 nebus sukuriamas pagamintų prekių sandėliavimo darbas.</span><span class="sxs-lookup"><span data-stu-id="26893-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="26893-110">Darbo strategija yra atskiras objektas, kurį galima apibrėžti naudojant tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="26893-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="26893-111">**Darbo strategijos pavadinimas**(unikalus darbo strategijos identifikatorius)</span><span class="sxs-lookup"><span data-stu-id="26893-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="26893-112">**Darbo užsakymų tipai** ir **Darbo kūrimo metodas**</span><span class="sxs-lookup"><span data-stu-id="26893-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="26893-113">**Atsargų vietos**</span><span class="sxs-lookup"><span data-stu-id="26893-113">**Inventory locations**</span></span>
-   <span data-ttu-id="26893-114">**Produktai.**</span><span class="sxs-lookup"><span data-stu-id="26893-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="26893-115">Darbo užsakymo tipai</span><span class="sxs-lookup"><span data-stu-id="26893-115">Work order types</span></span>
<span data-ttu-id="26893-116">Galite rinktis iš tolesnių darbo užsakymų tipų.</span><span class="sxs-lookup"><span data-stu-id="26893-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="26893-117">Baigtos prekės atidėtos</span><span class="sxs-lookup"><span data-stu-id="26893-117">Finished goods put away</span></span>
-   <span data-ttu-id="26893-118">Sudėtinis produktas ir šalutinis produktas atidėti</span><span class="sxs-lookup"><span data-stu-id="26893-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="26893-119">Žaliavų paėmimas</span><span class="sxs-lookup"><span data-stu-id="26893-119">Raw material picking</span></span>

<span data-ttu-id="26893-120">Lauke **Darbo kūrimo metodas** nustatyta reikšmė **Niekada**.</span><span class="sxs-lookup"><span data-stu-id="26893-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="26893-121">Ši reikšmė nurodo, kad darbo strategija neleis sandėlyje kurti pasirinkto darbo užsakymo tipo darbo.</span><span class="sxs-lookup"><span data-stu-id="26893-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="26893-122">Atsargų vietos</span><span class="sxs-lookup"><span data-stu-id="26893-122">Inventory locations</span></span>
<span data-ttu-id="26893-123">Galite pasirinkti vietą, kuriai darbo strategija taikoma.</span><span class="sxs-lookup"><span data-stu-id="26893-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="26893-124">Jei su darbo strategija nesusiejama jokia vieta, darbo strategija netaikoma jokiam procesui.</span><span class="sxs-lookup"><span data-stu-id="26893-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="26893-125">Puslapyje **Vietos** galite pažymėti arba atžymėti tam tikros vietos darbo strategiją.</span><span class="sxs-lookup"><span data-stu-id="26893-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="26893-126">Produktai</span><span class="sxs-lookup"><span data-stu-id="26893-126">Products</span></span>
<span data-ttu-id="26893-127">Galite pasirinkti produktą, kuriam darbo strategija taikoma.</span><span class="sxs-lookup"><span data-stu-id="26893-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="26893-128">Darbo strategiją galite taikyti visiems produktams arba pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="26893-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="26893-129">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="26893-129">Example</span></span>
<span data-ttu-id="26893-130">Šiame pavyzdyje nurodyti du gamybos užsakymai, PRD-001 ir PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="26893-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="26893-131">Gamybos užsakymui PRD-001 priskirta operacija, pavadinimu **Surinkimas**, kurioje produktas SC1 yra paskelbiamas baigtu vietoje O1.</span><span class="sxs-lookup"><span data-stu-id="26893-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="26893-132">Gamybos užsakymui PRD-002 priskirta operacija, pavadinimu **Dažymas**, ir ją vykdant naudojamas produktas SC1 iš vietos O1.</span><span class="sxs-lookup"><span data-stu-id="26893-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="26893-133">Gamybos užsakymas PRD-002 taip pat naudoja žaliavas RM1 iš vietos O1.</span><span class="sxs-lookup"><span data-stu-id="26893-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="26893-134">RM1 saugomos sandėlio vietoje BULK-001 ir bus paimtos bei perkeltos į vietą O1, naudojant žaliavų paėmimo sandėlio darbą.</span><span class="sxs-lookup"><span data-stu-id="26893-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="26893-135">Paėmimo darbas yra generuojamas, kai bus paleidžiama gamyba PRD-002.</span><span class="sxs-lookup"><span data-stu-id="26893-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="26893-136">[![Sandėlio darbo strategijos](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="26893-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="26893-137">Kai šiuo atveju planuojate konfigūruoti sandėlio darbo strategiją, turėtumėte atsižvelgti į tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="26893-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="26893-138">Sandėlio darbas, skirtas pagamintoms prekėms atidėti, nėra būtinas, kai produktą SC1 skelbiate baigtu iš gamybos užsakymo PRD-001 į vietą O1.</span><span class="sxs-lookup"><span data-stu-id="26893-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="26893-139">Tai yra todėl, kad gamybos užsakymo PRD-002 operacija **dažymo** naudoja SC1 toje pačioje vietoje.</span><span class="sxs-lookup"><span data-stu-id="26893-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="26893-140">Žaliavų paėmimo sandėlio darbas yra būtinas, norint žaliavas RM1 perkelti iš sandėlio vietos BULK-001 į vietą O1.</span><span class="sxs-lookup"><span data-stu-id="26893-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="26893-141">Čia pateikiamas darbo strategijos, kurią galite nustatyti atsižvelgdami į šiuos aspektus, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="26893-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="26893-142"><strong>Darbo strategijos pavadinimas</strong></span><span class="sxs-lookup"><span data-stu-id="26893-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="26893-143"><strong>Darbo užsakymo tipai</strong></span><span class="sxs-lookup"><span data-stu-id="26893-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="26893-144">Sandėliavimo darbo nėra 01     \`</span><span class="sxs-lookup"><span data-stu-id="26893-144">No put away 01     \`</span></span>          |     <span data-ttu-id="26893-145">- Pagamintų prekių sandėliavimas</span><span class="sxs-lookup"><span data-stu-id="26893-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="26893-146"><strong>Vietos</strong></span><span class="sxs-lookup"><span data-stu-id="26893-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="26893-147">- O1</span><span class="sxs-lookup"><span data-stu-id="26893-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="26893-148"><strong>Produktai</strong></span><span class="sxs-lookup"><span data-stu-id="26893-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="26893-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="26893-149">- SC1</span></span>                 |

<span data-ttu-id="26893-150">Tolesnėse procedūrose pateikiamos nuoseklios instrukcijos apie tai, kaip nustatyti šio scenarijaus sandėlio darbo strategijos.</span><span class="sxs-lookup"><span data-stu-id="26893-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="26893-151">Taip pat aprašytas sąrankos pavyzdinis, kuriuo parodoma, kaip gamybos užsakymą skelbti baigtus vietoje, kuri nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="26893-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="26893-152">Sandėlio darbo strategijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="26893-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="26893-153">Sandėlio procesai ne visada apima sandėlio darbą.</span><span class="sxs-lookup"><span data-stu-id="26893-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="26893-154">Apibrėždami darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo.</span><span class="sxs-lookup"><span data-stu-id="26893-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="26893-155">Kuriant šią procedūrą naudota demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="26893-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="26893-156">VEIKSMAI (21)</span><span class="sxs-lookup"><span data-stu-id="26893-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="26893-157">1.</span><span class="sxs-lookup"><span data-stu-id="26893-157">1.</span></span>  | <span data-ttu-id="26893-158">Eikite į Sandėlio valdymas &gt; Nustatymas &gt; Darbas &gt; Darbo strategijos.</span><span class="sxs-lookup"><span data-stu-id="26893-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="26893-159">2.</span><span class="sxs-lookup"><span data-stu-id="26893-159">2.</span></span>  | <span data-ttu-id="26893-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="26893-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="26893-161">3.</span><span class="sxs-lookup"><span data-stu-id="26893-161">3.</span></span>  | <span data-ttu-id="26893-162">Lauke Darbo strategijos pavadinimas įveskite „Atidėjimo darbo nėra‟.</span><span class="sxs-lookup"><span data-stu-id="26893-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="26893-163">4.</span><span class="sxs-lookup"><span data-stu-id="26893-163">4.</span></span>  | <span data-ttu-id="26893-164">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="26893-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="26893-165">5.</span><span class="sxs-lookup"><span data-stu-id="26893-165">5.</span></span>  | <span data-ttu-id="26893-166">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="26893-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="26893-167">6.</span><span class="sxs-lookup"><span data-stu-id="26893-167">6.</span></span>  | <span data-ttu-id="26893-168">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="26893-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="26893-169">7.</span><span class="sxs-lookup"><span data-stu-id="26893-169">7.</span></span>  | <span data-ttu-id="26893-170">Lauke Darbo užsakymo tipas pasirinkite Baigtos prekės atidėtos.</span><span class="sxs-lookup"><span data-stu-id="26893-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="26893-171">8.</span><span class="sxs-lookup"><span data-stu-id="26893-171">8.</span></span>  | <span data-ttu-id="26893-172">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="26893-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="26893-173">9.</span><span class="sxs-lookup"><span data-stu-id="26893-173">9.</span></span>  | <span data-ttu-id="26893-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="26893-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="26893-175">10.</span><span class="sxs-lookup"><span data-stu-id="26893-175">10.</span></span> | <span data-ttu-id="26893-176">Lauke Darbo užsakymo tipas pasirinkite Sudėtinis produktas ir šalutinis produktas atidėti.</span><span class="sxs-lookup"><span data-stu-id="26893-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="26893-177">11.</span><span class="sxs-lookup"><span data-stu-id="26893-177">11.</span></span> | <span data-ttu-id="26893-178">Išplėskite dalį Atsargų vietos.</span><span class="sxs-lookup"><span data-stu-id="26893-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="26893-179">12.</span><span class="sxs-lookup"><span data-stu-id="26893-179">12.</span></span> | <span data-ttu-id="26893-180">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="26893-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="26893-181">13.</span><span class="sxs-lookup"><span data-stu-id="26893-181">13.</span></span> | <span data-ttu-id="26893-182">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="26893-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="26893-183">14.</span><span class="sxs-lookup"><span data-stu-id="26893-183">14.</span></span> | <span data-ttu-id="26893-184">Sandėlių sąraše įveskite „51‟.</span><span class="sxs-lookup"><span data-stu-id="26893-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="26893-185">15.</span><span class="sxs-lookup"><span data-stu-id="26893-185">15.</span></span> | <span data-ttu-id="26893-186">Lauke Vieta įveskite arba pasirinkite „001‟.</span><span class="sxs-lookup"><span data-stu-id="26893-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="26893-187">16.</span><span class="sxs-lookup"><span data-stu-id="26893-187">16.</span></span> | <span data-ttu-id="26893-188">Išplėskite sekciją Produktai.</span><span class="sxs-lookup"><span data-stu-id="26893-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="26893-189">17.</span><span class="sxs-lookup"><span data-stu-id="26893-189">17.</span></span> | <span data-ttu-id="26893-190">Lauke Produktų pasirinkimas pasirinkite Pasirinkta.</span><span class="sxs-lookup"><span data-stu-id="26893-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="26893-191">18.</span><span class="sxs-lookup"><span data-stu-id="26893-191">18.</span></span> | <span data-ttu-id="26893-192">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="26893-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="26893-193">19.</span><span class="sxs-lookup"><span data-stu-id="26893-193">19.</span></span> | <span data-ttu-id="26893-194">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="26893-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="26893-195">20.</span><span class="sxs-lookup"><span data-stu-id="26893-195">20.</span></span> | <span data-ttu-id="26893-196">Lauke Prekės numeris įveskite arba pasirinkite „L0101‟.</span><span class="sxs-lookup"><span data-stu-id="26893-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="26893-197">21.</span><span class="sxs-lookup"><span data-stu-id="26893-197">21.</span></span> | <span data-ttu-id="26893-198">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="26893-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="26893-199">Gamybos užsakymo skelbimas baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę</span><span class="sxs-lookup"><span data-stu-id="26893-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="26893-200">Šioje procedūroje parodytas skelbimo baigtu vietoje, kuri nėra kontroliuojama pagal numerio lentelę, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="26893-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="26893-201">Norint atlikti šią užduotį, būtina tinkama darbo strategija.</span><span class="sxs-lookup"><span data-stu-id="26893-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="26893-202">Kaip nustatyti darbo strategiją, parodyta ankstesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="26893-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="26893-203">VEIKSMAI (25)</span><span class="sxs-lookup"><span data-stu-id="26893-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="26893-204"><strong>Antrinė užduotis: išeigos vietos nustatymas.</strong></span><span class="sxs-lookup"><span data-stu-id="26893-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="26893-205">Eikite į Organizacijos administravimas &gt; Ištekliai &gt; Išteklių grupės.</span><span class="sxs-lookup"><span data-stu-id="26893-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="26893-206">Sąraše pasirinkite išteklių grupę &#39;5102&#39;.</span><span class="sxs-lookup"><span data-stu-id="26893-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="26893-207">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="26893-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="26893-208">Lauke Išeigos sandėlis įveskite &#39;51&#39;.</span><span class="sxs-lookup"><span data-stu-id="26893-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="26893-209">Lauke Išeigos vieta įveskite &#39;001&#39;.</span><span class="sxs-lookup"><span data-stu-id="26893-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="26893-210">001 vieta nėra kontroliuojama pagal numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="26893-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="26893-211">Ne pagal numerio lentelę kontroliuojamą išeigos vietą galite nustatyti tik jei yra tinkama vietos darbo strategija.</span><span class="sxs-lookup"><span data-stu-id="26893-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="26893-212"><strong>Antrinė užduotis: gamybos užsakymo sukūrimas ir jo skelbimas baigtu.</strong></span><span class="sxs-lookup"><span data-stu-id="26893-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="26893-213">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="26893-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="26893-214">Eikite į Gamybos kontrolė &gt; Gamybos užsakymai &gt; Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="26893-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="26893-215">Spustelėkite Naujas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="26893-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="26893-216">Lauke Prekės numeris įveskite &#39;L0101&#39;.</span><span class="sxs-lookup"><span data-stu-id="26893-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="26893-217">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="26893-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="26893-218">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="26893-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="26893-219">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="26893-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="26893-220">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="26893-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="26893-221">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="26893-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="26893-222">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="26893-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="26893-223">Lauke Automatinis KS suvartojimas pasirinkite &#39;Niekada&#39;.</span><span class="sxs-lookup"><span data-stu-id="26893-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="26893-224">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="26893-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="26893-225">Spustelėkite Paskelbti baigtu.</span><span class="sxs-lookup"><span data-stu-id="26893-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="26893-226">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="26893-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="26893-227">Lauke Leisti klaidą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="26893-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="26893-228">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="26893-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="26893-229">Veiksmų srityje spustelėkite Sandėlis.</span><span class="sxs-lookup"><span data-stu-id="26893-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="26893-230">Spustelėkite Darbo informacija.</span><span class="sxs-lookup"><span data-stu-id="26893-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="26893-231">Kai gamybos užsakymas buvo paskelbtas baigtu, nebuvo sugeneruota jokio padėjimo darbo.</span><span class="sxs-lookup"><span data-stu-id="26893-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="26893-232">Taip nutinka, nes yra apibrėžta darbo strategija, pagal kurią negalima generuoti darbo, kai produktas L0101 paskebiamas baigtu 001 vietoje.</span><span class="sxs-lookup"><span data-stu-id="26893-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



