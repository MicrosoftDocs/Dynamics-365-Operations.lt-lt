---
title: Konteinerių pakavimo strategijos
description: Šioje temoje aprašomi konteinerių pakavimo strategijų skirtumai ir pateikiami pavyzdžiai.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292766"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="ce42e-103">Konteinerių pakavimo strategijos</span><span class="sxs-lookup"><span data-stu-id="ce42e-103">Container packing strategies</span></span>

<span data-ttu-id="ce42e-104">*Konteinerių pakavimo strategija* yra strategija, kurią galite naudoti prekių paskirstymui tarp konteinerių apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="ce42e-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="ce42e-105">Šioje temoje paaiškinami skirtumai tarp *Pakuoti į visus atidarytus konteinerius* ir *Pakuoti tik į dabartinį konteinerį* strategijų.</span><span class="sxs-lookup"><span data-stu-id="ce42e-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="ce42e-106">**Pakuoti į visus atidarytus konteinerius** – sistema turi patikrinti visus atidarytus konteinerius, kurie jau buvo sukurti krovimo į konteinerius ciklo metu, kad įsitikintų, jog prekė tilps į vieną iš jų.</span><span class="sxs-lookup"><span data-stu-id="ce42e-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="ce42e-107">Pakavimo metu sistema patikrina kiekvieną prekę, kad nustatytų, ar ji tinka bet kuriam anksčiau sukurtam konteineriui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="ce42e-108">Jei prekė netilps į esamą konteinerį, sistema sukuria naują konteinerį ir taip tęsia toliau, kol užbaigia supakuoti visą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ce42e-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="ce42e-109">Pavyzdžiui, *n kiekiui* užsakytų prekių būtinas krovimas į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="ce42e-110">Blogiausiu atveju kiekvieną kartą sistemai apdorojant prekę, netelpančią į jokį esamą konteinerį, iš viso ji atliks (\[(*n-1*) × (*n+1*)\] ÷ 2) patikrinimų, jog įvertintų, ar prekė tilps į esamus konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="ce42e-111">**Pakuoti tik į dabartinį konteinerį** – sistema privalo patikrinti tik paskutinį sukurtą konteinerį, kad įsitikintų, jog prekė į jį tilps.</span><span class="sxs-lookup"><span data-stu-id="ce42e-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="ce42e-112">Pakavimo metu sistema patikrina kiekvieną prekę, kad nustatytų, ar ji tinka naujausiam sukurtam konteineriui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="ce42e-113">Jei prekė netilps į tą konteinerį, sistema sukuria naują konteinerį ir taip tęsia toliau, kol užbaigia supakuoti visą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ce42e-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="ce42e-114">Pavyzdžiui, *n kiekiui* užsakytų prekių būtinas krovimas į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="ce42e-115">Blogiausiu atveju sistema iš viso atliks (*n-1*) patikrinimų, jog įvertintų, ar prekė tilps į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="ce42e-116">Konteinerių pakavimo strategijų srauto pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ce42e-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="ce42e-117">Nustatote toliau pateiktas prekes krovimui į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="ce42e-118">Prekė</span><span class="sxs-lookup"><span data-stu-id="ce42e-118">Item</span></span> | <span data-ttu-id="ce42e-119">Faktinės dimensijos (plotis × gylis × aukštis)</span><span class="sxs-lookup"><span data-stu-id="ce42e-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="ce42e-120">Svoris</span><span class="sxs-lookup"><span data-stu-id="ce42e-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="ce42e-121">HDMI kabelis 6'</span><span class="sxs-lookup"><span data-stu-id="ce42e-121">HDMI Cable 6'</span></span> | <span data-ttu-id="ce42e-122">1×1×1</span><span class="sxs-lookup"><span data-stu-id="ce42e-122">1 × 1 × 1</span></span> | <span data-ttu-id="ce42e-123">1</span><span class="sxs-lookup"><span data-stu-id="ce42e-123">1</span></span> |
| <span data-ttu-id="ce42e-124">HDMI kabelis 12'</span><span class="sxs-lookup"><span data-stu-id="ce42e-124">HDMI Cable 12'</span></span> | <span data-ttu-id="ce42e-125">2×1×1</span><span class="sxs-lookup"><span data-stu-id="ce42e-125">2 × 1 × 1</span></span> | <span data-ttu-id="ce42e-126">1</span><span class="sxs-lookup"><span data-stu-id="ce42e-126">1</span></span> |
| <span data-ttu-id="ce42e-127">HDMI kabelis 18'</span><span class="sxs-lookup"><span data-stu-id="ce42e-127">HDMI Cable 18'</span></span> | <span data-ttu-id="ce42e-128">3×1×1</span><span class="sxs-lookup"><span data-stu-id="ce42e-128">3 × 1 × 1</span></span> | <span data-ttu-id="ce42e-129">2</span><span class="sxs-lookup"><span data-stu-id="ce42e-129">2</span></span> |

<span data-ttu-id="ce42e-130">Taip pat nustatote toliau pateiktą dėžę, kuri bus naudojama pakavimui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="ce42e-131">Konteineris</span><span class="sxs-lookup"><span data-stu-id="ce42e-131">Container</span></span> | <span data-ttu-id="ce42e-132">Faktinės dimensijos (ilgis × plotis × aukštis)</span><span class="sxs-lookup"><span data-stu-id="ce42e-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="ce42e-133">Svoris</span><span class="sxs-lookup"><span data-stu-id="ce42e-133">Weight</span></span> | <span data-ttu-id="ce42e-134">Tūris</span><span class="sxs-lookup"><span data-stu-id="ce42e-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="ce42e-135">Vidutinė dėžė</span><span class="sxs-lookup"><span data-stu-id="ce42e-135">Medium Box</span></span> | <span data-ttu-id="ce42e-136">6×3×2</span><span class="sxs-lookup"><span data-stu-id="ce42e-136">6 × 3 × 2</span></span> | <span data-ttu-id="ce42e-137">10</span><span class="sxs-lookup"><span data-stu-id="ce42e-137">10</span></span> | <span data-ttu-id="ce42e-138">100</span><span class="sxs-lookup"><span data-stu-id="ce42e-138">100</span></span> |

<span data-ttu-id="ce42e-139">Galiausiai, jūs nustatote užsakymą, kuriame yra šie produktai ir kiekiai.</span><span class="sxs-lookup"><span data-stu-id="ce42e-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="ce42e-140">Pardavimo užsakymo eilutė</span><span class="sxs-lookup"><span data-stu-id="ce42e-140">Sales order line</span></span> | <span data-ttu-id="ce42e-141">Kiekis</span><span class="sxs-lookup"><span data-stu-id="ce42e-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="ce42e-142">HDMI kabelis 12'</span><span class="sxs-lookup"><span data-stu-id="ce42e-142">HDMI Cable 12'</span></span> | <span data-ttu-id="ce42e-143">9</span><span class="sxs-lookup"><span data-stu-id="ce42e-143">9</span></span> |
| <span data-ttu-id="ce42e-144">HDMI kabelis 18'</span><span class="sxs-lookup"><span data-stu-id="ce42e-144">HDMI Cable 18'</span></span> | <span data-ttu-id="ce42e-145">8</span><span class="sxs-lookup"><span data-stu-id="ce42e-145">8</span></span> |
| <span data-ttu-id="ce42e-146">HDMI kabelis 6'</span><span class="sxs-lookup"><span data-stu-id="ce42e-146">HDMI Cable 6'</span></span> | <span data-ttu-id="ce42e-147">13</span><span class="sxs-lookup"><span data-stu-id="ce42e-147">13</span></span> |

<span data-ttu-id="ce42e-148">Toliau pateiktoje lentelėje apibendrinama, kaip veikia pakavimas į konteinerius, kai naudojate *Pakuoti į visus atidarytus konteinerius* strategiją ir kai naudojate *Pakuoti tik į dabartinį konteinerį* strategiją.</span><span class="sxs-lookup"><span data-stu-id="ce42e-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="ce42e-149">Pakuoti į visus atidarytus konteinerius</span><span class="sxs-lookup"><span data-stu-id="ce42e-149">Pack into all open containers</span></span> | <span data-ttu-id="ce42e-150">Pakuoti į dabartinį konteinerį</span><span class="sxs-lookup"><span data-stu-id="ce42e-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="ce42e-151">HDMI kabelis 12':</span><span class="sxs-lookup"><span data-stu-id="ce42e-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="ce42e-152">Sukurkite naują konteinerį, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="ce42e-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="ce42e-153">Įdėkite 9 vienetus į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="ce42e-154">HDMI kabelis 12':</span><span class="sxs-lookup"><span data-stu-id="ce42e-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="ce42e-155">Sukurkite naują konteinerį, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="ce42e-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="ce42e-156">Įdėkite 9 vienetus į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="ce42e-157">HDMI kabelis 18':</span><span class="sxs-lookup"><span data-stu-id="ce42e-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="ce42e-158">Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="ce42e-159">Sukurkite naują konteinerį, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="ce42e-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="ce42e-160">Įdėkite 5 vienetus į CONT0002 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="ce42e-161">Sukurkite naują konteinerį, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="ce42e-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="ce42e-162">Įdėkite 3 vienetus į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="ce42e-163">HDMI kabelis 18':</span><span class="sxs-lookup"><span data-stu-id="ce42e-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="ce42e-164">Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="ce42e-165">Sukurkite naują konteinerį, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="ce42e-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="ce42e-166">Įdėkite 5 vienetus į CONT0002 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="ce42e-167">Sukurkite naują konteinerį, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="ce42e-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="ce42e-168">Įdėkite 3 vienetus į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="ce42e-169">HDMI kabelis 6':</span><span class="sxs-lookup"><span data-stu-id="ce42e-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="ce42e-170">Patikrinkite, ar prekė gali tilpti į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="ce42e-171">Įdėkite 1 vienetą į CONT0001 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="ce42e-172">Patikrinkite, ar prekė gali tilpti į CONT0002 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="ce42e-173">Patikrinkite, ar prekė gali tilpti į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="ce42e-174">Įdėkite 4 vienetus į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="ce42e-175">Sukurkite naują konteinerį, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="ce42e-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="ce42e-176">Įdėkite 8 vienetus į CONT0004 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="ce42e-177">HDMI kabelis 6':</span><span class="sxs-lookup"><span data-stu-id="ce42e-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="ce42e-178">Patikrinkite, ar prekė gali tilpti į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="ce42e-179">Įdėkite 4 vienetus į CONT0003 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="ce42e-180">Sukurkite naują konteinerį, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="ce42e-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="ce42e-181">Įdėkite 9 vienetus į CONT0004 konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="ce42e-182">Pavyzdinis scenarijus: Vieno užsakymo pakavimas į vieną konteinerį</span><span class="sxs-lookup"><span data-stu-id="ce42e-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="ce42e-183">Šiame skyriuje pateikiamas scenarijus, kai sistema yra nustatyta konsoliduoti kelis užsakymus į vieną siuntą.</span><span class="sxs-lookup"><span data-stu-id="ce42e-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="ce42e-184">Todėl krovimas į konteinerius bus atliekamas iš pardavimo užsakymo, siekiant užtikrinti, kad kiekvienas užsakymas, kuriame yra keli produktai, būtų supakuotas į vieną konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="ce42e-185">Naudodami šią funkciją galite susitvarkyti su scenarijais, kuriuose turite supakuoti tik vieną pardavimo užsakymą kiekviename konteineryje, kad paskirstymo centras galėtų paskirstyti pilnus konteinerius tarp mažmeninės prekybos parduotuvių.</span><span class="sxs-lookup"><span data-stu-id="ce42e-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="ce42e-186">Be mažmeninės prekybos scenarijų (užsakymas pagal parduotuvę ir siuntimas į prekių skirstymo paskirstymo centrą), šis principas taip pat dažnai naudojamas „lean” tiekimo grandinėse (pardavimo užsakymas pagal „reikiamu laiku” gamybos eilutę).</span><span class="sxs-lookup"><span data-stu-id="ce42e-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="ce42e-187">Šiame scenarijuje rodoma, kaip galite sumažinti konteinerių, kurie įvertinami pakuojant, skaičių naudodami *Pakuoti tik į dabartinį konteinerį* krovimo į konteinerius strategiją.</span><span class="sxs-lookup"><span data-stu-id="ce42e-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ce42e-188">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="ce42e-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="ce42e-189">Siuntų konsolidavimo funkcijos įjungimas sistemoje</span><span class="sxs-lookup"><span data-stu-id="ce42e-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="ce42e-190">Šis scenarijus naudoja *Konsoliduoti siuntas* funkciją.</span><span class="sxs-lookup"><span data-stu-id="ce42e-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="ce42e-191">Jei ši funkcija dar negalima jūsų sistemoje, turite įjungti ją naudodami [Funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ce42e-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="ce42e-192">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-192">Make demo data available</span></span>

<span data-ttu-id="ce42e-193">Šis scenarijus nurodo reikšmes ir įrašus, įtrauktus į standartinius „Microsoft Dynamics 365 Supply Chain Management” demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ce42e-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ce42e-194">Jei norite naudoti čia pateiktas reikšmes atlikdami pratimus, įsitikinkite, kad dirbate aplinkoje, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami nustatykite juridinį subjektą į **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="ce42e-195">Konteinerių tipų tikrinimas ar kūrimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-195">Inspect or create container types</span></span>

<span data-ttu-id="ce42e-196">Norėdami patikrinti konteinerių tipus arba, jei reikia, sukurti naujus konteinerių tipus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-197">Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerių tipai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="ce42e-198">Įsitikinkite, kad kiekvienas iš toliau pateiktų konteinerio tipų yra galimas jūsų demonstraciniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="ce42e-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="ce42e-199">Redaguokite arba sukurkite konteinerių tipus, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="ce42e-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="ce42e-200">1 konteinerio tipas:</span><span class="sxs-lookup"><span data-stu-id="ce42e-200">Container type 1:</span></span>

        - <span data-ttu-id="ce42e-201">**Konteinerio tipo kodas:** *Didelė dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="ce42e-202">**Aprašas:** *Didelė dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="ce42e-203">**Didžiausias grynasis svoris:** *100*</span><span class="sxs-lookup"><span data-stu-id="ce42e-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="ce42e-204">**Tūris:** *400*</span><span class="sxs-lookup"><span data-stu-id="ce42e-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="ce42e-205">**Ilgis:** *4*</span><span class="sxs-lookup"><span data-stu-id="ce42e-205">**Length:** *4*</span></span>
        - <span data-ttu-id="ce42e-206">**Plotis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-206">**Width:** *10*</span></span>
        - <span data-ttu-id="ce42e-207">**Aukštis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-207">**Height:** *10*</span></span>

    - <span data-ttu-id="ce42e-208">2 konteinerio tipas:</span><span class="sxs-lookup"><span data-stu-id="ce42e-208">Container type 2:</span></span>

        - <span data-ttu-id="ce42e-209">**Konteinerio tipo kodas:** *Vidutinė dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="ce42e-210">**Aprašas:** *Vidutinė dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="ce42e-211">**Didžiausias grynasis svoris:** *50*</span><span class="sxs-lookup"><span data-stu-id="ce42e-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="ce42e-212">**Tūris:** *200*</span><span class="sxs-lookup"><span data-stu-id="ce42e-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="ce42e-213">**Ilgis:** *2*</span><span class="sxs-lookup"><span data-stu-id="ce42e-213">**Length:** *2*</span></span>
        - <span data-ttu-id="ce42e-214">**Plotis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-214">**Width:** *10*</span></span>
        - <span data-ttu-id="ce42e-215">**Aukštis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-215">**Height:** *10*</span></span>

    - <span data-ttu-id="ce42e-216">3 konteinerio tipas:</span><span class="sxs-lookup"><span data-stu-id="ce42e-216">Container type 3:</span></span>

        - <span data-ttu-id="ce42e-217">**Konteinerio tipo kodas:** *Maža dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="ce42e-218">**Aprašas:** *Maža dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="ce42e-219">**Didžiausias grynasis svoris:** *20*</span><span class="sxs-lookup"><span data-stu-id="ce42e-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="ce42e-220">**Tūris:** *100*</span><span class="sxs-lookup"><span data-stu-id="ce42e-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="ce42e-221">**Ilgis:** *1*</span><span class="sxs-lookup"><span data-stu-id="ce42e-221">**Length:** *1*</span></span>
        - <span data-ttu-id="ce42e-222">**Plotis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-222">**Width:** *10*</span></span>
        - <span data-ttu-id="ce42e-223">**Aukštis:** *10*</span><span class="sxs-lookup"><span data-stu-id="ce42e-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="ce42e-224">Konteinerių grupių tikrinimas arba kūrimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-224">Inspect or create container groups</span></span>

<span data-ttu-id="ce42e-225">Norėdami patikrinti konteinerių grupes arba, jei reikia, sukurti naujas konteinerių grupes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-226">Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerių grupės**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="ce42e-227">Įsitikinkite, kad toliau pateikta konteinerio grupė yra galima jūsų demonstraciniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="ce42e-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="ce42e-228">Jei ji negalima, pasirinkite **Nauja**, kad ją sukurtumėte.</span><span class="sxs-lookup"><span data-stu-id="ce42e-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="ce42e-229">**Konteinerių grupės ID:** *Dėžės*</span><span class="sxs-lookup"><span data-stu-id="ce42e-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="ce42e-230">**Aprašas:** *Dėžių dydžiai*</span><span class="sxs-lookup"><span data-stu-id="ce42e-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="ce42e-231">Įsitikinkite, kad „FastTab” **Išsami informacija** konteinerių grupei *Dėžės* yra toliau pateiktos eilutės.</span><span class="sxs-lookup"><span data-stu-id="ce42e-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="ce42e-232">Jei jų nėra, pasirinkite **Nauja**, kad jas įtrauktumėte.</span><span class="sxs-lookup"><span data-stu-id="ce42e-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="ce42e-233">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="ce42e-233">Line 1:</span></span>

        - <span data-ttu-id="ce42e-234">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="ce42e-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="ce42e-235">**Talpyklos tipas:** *Plati dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="ce42e-236">**Konteinerio efektyvumo procentas:** *100*</span><span class="sxs-lookup"><span data-stu-id="ce42e-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="ce42e-237">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="ce42e-237">Line 2:</span></span>

        - <span data-ttu-id="ce42e-238">**Sekos numeris:** *2*</span><span class="sxs-lookup"><span data-stu-id="ce42e-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="ce42e-239">**Konteinerio tipas:** *Vidutinė dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="ce42e-240">**Konteinerio efektyvumo procentas:** *100*</span><span class="sxs-lookup"><span data-stu-id="ce42e-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="ce42e-241">Eilutė 3:</span><span class="sxs-lookup"><span data-stu-id="ce42e-241">Line 3:</span></span>

        - <span data-ttu-id="ce42e-242">**Sekos numeris:** *3*</span><span class="sxs-lookup"><span data-stu-id="ce42e-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="ce42e-243">**Konteinerio tipas:** *Maža dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="ce42e-244">**Konteinerio efektyvumo procentas:** *100*</span><span class="sxs-lookup"><span data-stu-id="ce42e-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="ce42e-245">Sukurkite naują konteinerio kūrimo šabloną</span><span class="sxs-lookup"><span data-stu-id="ce42e-245">Create a new container build template</span></span>

<span data-ttu-id="ce42e-246">Norėdami sukurti naują konteinerio kūrimo šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-247">Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerio kūrimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="ce42e-248">Pasirinkite **Naujas** norėdami sukurti konteinerio kūrimo šabloną, kuris turi šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="ce42e-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="ce42e-249">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="ce42e-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ce42e-250">**Konteinerio šablono ID:** *Dėžė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="ce42e-251">**Konteinerių grupės ID:** *Dėžės*</span><span class="sxs-lookup"><span data-stu-id="ce42e-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="ce42e-252">**Pagrindiniai užklausų tipai:** *Pardavimų paskirstymo eilutė*</span><span class="sxs-lookup"><span data-stu-id="ce42e-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="ce42e-253">**Bangos veiksmo kodas:** *234*</span><span class="sxs-lookup"><span data-stu-id="ce42e-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="ce42e-254">**Leisti skaidyti paėmimus:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ce42e-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="ce42e-255">**Konteinerių pakavimo strategija:** *Pakuoti tik į dabartinį konteinerį*</span><span class="sxs-lookup"><span data-stu-id="ce42e-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="ce42e-256">**Paketas pagal krypties vienetą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="ce42e-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="ce42e-257">Kol naujo šablono eilutė vis dar pasirinkta, pasirinkite **Redaguoti užklausą** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="ce42e-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="ce42e-258">Atsiranda standartinis užklausų rengyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="ce42e-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="ce42e-259">Skirtuke **Rikiavimas** pasirinkite **Įtraukti** norėdami įtraukti eilutę, turinčią toliau pateiktus parametrus:</span><span class="sxs-lookup"><span data-stu-id="ce42e-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="ce42e-260">**Lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="ce42e-261">**Išvestinė lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="ce42e-262">**Laukas:** *Užsakymo numeris*</span><span class="sxs-lookup"><span data-stu-id="ce42e-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="ce42e-263">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="ce42e-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ce42e-264">Norėdami išvengti visų kitų atvirų konteinerių perkrovos ir pagreitinti procesą vienu metu pažymėdami vieną konteinerį, naudokite *Pakuoti tik į dabartinį konteinerį* strategiją bei rikiavimą pagal užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="ce42e-265">Šis derinys veiks kaip darbo skaidymas darbo šablone.</span><span class="sxs-lookup"><span data-stu-id="ce42e-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="ce42e-266">Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ce42e-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ce42e-267">Kol naujo šablono eilutė vis dar pasirinkta, pasirinkite **Konteinerių maišymo apribojimai** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="ce42e-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="ce42e-268">Dabar įtrauksite apribojimą, pagal kurį prekės iš vieno užsakymo bus kraunamos į vieną konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="ce42e-269">Prekės iš bet kurio kito užsakymo bus kraunamos į atskirą konteinerį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="ce42e-270">Pasirinkite **Naujas** norėdami sukurti maišymo apribojimą, kuris turi šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="ce42e-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="ce42e-271">**Lentelė:** *pardavimo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="ce42e-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="ce42e-272">**Lauko pasirinktis:** *Pardavimo Id* (Laukas bus rodomas kaip *Pardavimo užsakymas* tinklelyje.)</span><span class="sxs-lookup"><span data-stu-id="ce42e-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="ce42e-273">Pasirinkite **Gerai** norėdami įtraukti apribojimą.</span><span class="sxs-lookup"><span data-stu-id="ce42e-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="ce42e-274">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="ce42e-275">Krovimo į konteinerius bangos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce42e-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="ce42e-276">Norėdami nustatyti bangos šabloną atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-277">Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ce42e-278">Sąrašo srityje nustatykite **Bangos šablono tipo** laukelį į *Siuntimas*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="ce42e-279">Sąraše pasirinkite **63 krovimas į konteinerius** šabloną.</span><span class="sxs-lookup"><span data-stu-id="ce42e-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="ce42e-280">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ce42e-281">**Metodai** „FastTab“ **Pasirinkti metodai** stulpelyje suraskite šią eilutę:</span><span class="sxs-lookup"><span data-stu-id="ce42e-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="ce42e-282">**Metodo pavadinimas:** *pakavimas į konteinerius*</span><span class="sxs-lookup"><span data-stu-id="ce42e-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="ce42e-283">**Pavadinimas:** *Pakavimas į konteinerius*</span><span class="sxs-lookup"><span data-stu-id="ce42e-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="ce42e-284">Nustatykite **Bangos žingsnio kodo** lauką šiai eilutei į *234*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="ce42e-285">Darbo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce42e-285">Set up a work template</span></span>

<span data-ttu-id="ce42e-286">Norėdami nustatyti darbo šabloną atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-287">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ce42e-288">Nustatykite lauką **Darbo užsakymo tipas** į *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="ce42e-289">Tinklelyje **Peržiūra** raskite ir pasirinkite darbo šabloną, kuris turėtų būti naudojamas atskirų užsakymų pakavimui į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="ce42e-290">Šiame scenarijuje pasirinkite **63 paėmimo į konteinerį** šabloną.</span><span class="sxs-lookup"><span data-stu-id="ce42e-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="ce42e-291">Veiksmų srityje pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ce42e-292">Atsiranda standartinis užklausų rengyklės dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="ce42e-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="ce42e-293">Skirtuke **Rūšiavimas** įtraukite toliau pateiktas eilutes:</span><span class="sxs-lookup"><span data-stu-id="ce42e-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="ce42e-294">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="ce42e-294">Line 1:</span></span>

        - <span data-ttu-id="ce42e-295">**Lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-296">**Išvestinė lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-297">**Laukas:** *Siuntos ID*</span><span class="sxs-lookup"><span data-stu-id="ce42e-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="ce42e-298">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="ce42e-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="ce42e-299">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="ce42e-299">Line 2:</span></span>

        - <span data-ttu-id="ce42e-300">**Lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-301">**Išvestinė lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-302">**Laukas:** *Užsakymo numeris*</span><span class="sxs-lookup"><span data-stu-id="ce42e-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="ce42e-303">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="ce42e-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="ce42e-304">Eilutė 3:</span><span class="sxs-lookup"><span data-stu-id="ce42e-304">Line 3:</span></span>

        - <span data-ttu-id="ce42e-305">**Lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-306">**Išvestinė lentelė:** *Laikinos darbo operacijos*</span><span class="sxs-lookup"><span data-stu-id="ce42e-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="ce42e-307">**Laukas:** *Konteinerio ID*</span><span class="sxs-lookup"><span data-stu-id="ce42e-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="ce42e-308">**Paieškos kryptis:** *Didėjanti*</span><span class="sxs-lookup"><span data-stu-id="ce42e-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ce42e-309">Pasirinkite **Gerai** užklausos tvarkyklės teksto langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ce42e-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ce42e-310">Jūs gaunate šį pranešimą: „Grupavimas bus perkrautas, ar tęsti?“</span><span class="sxs-lookup"><span data-stu-id="ce42e-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="ce42e-311">Pasirinkite **Taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="ce42e-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="ce42e-312">Kol šablonas **63 paėmimas į konteinerį** vis dar pasirinktas, pasirinkite **Darbo antraštės lūžiai** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="ce42e-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="ce42e-313">Dabar pritaikysite parametrus norėdami skaidyti darbą, kad kiekvienas užsakymo konteineris būtų susietas su vienu darbo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ce42e-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="ce42e-314">Kiekvienai eilutei pasirinkite **Grupuoti pagal šį lauką** žymės langelį **Darbo antraštės lūžiai** puslapyje (**Siuntos ID**, **Užsakymo numeris** ir **Konteinerio ID**).</span><span class="sxs-lookup"><span data-stu-id="ce42e-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="ce42e-315">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="ce42e-316">Siuntos konsolidacijos strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce42e-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="ce42e-317">Norėdami nustatyti siuntos konsolidacijos strategiją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-318">Eikite į **Sandėlio valdymas \> Sąranka \> Išleidimas į sandėlį \> Siuntos konsolidacijos strategijos**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="ce42e-319">Sąrašo srityje nustatykite lauką **Strategijos tipas** į *Pardavimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="ce42e-320">Pasirinkite **Numatytąją** strategiją sąraše.</span><span class="sxs-lookup"><span data-stu-id="ce42e-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="ce42e-321">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ce42e-322">„FastTab” **Konsolidavimo laukai** sąraše **Pasirinkti laukai** pasirinkite eilutę, kurioje laukas **Lauko pavadinimas** nustatytas į *Užsakymo numeris*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="ce42e-323">Pasirinkite **Pašalinti** mygtuką ![Rodyklė kairėn](media/backward-button.png), kad perkeltumėte lauką į sąrašą **Likę laukai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="ce42e-324">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="ce42e-325">Faktinių produkto dimensijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ce42e-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="ce42e-326">Norėdami nustatyti faktines produktų, kurie bus naudojami šiame scenarijuje, dimensijas, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-327">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ce42e-328">Pasirinkite produktą, kurio laukas **Prekės numeris** nustatytas į *„A0001”*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="ce42e-329">Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="ce42e-330">Puslapyje **Faktinės dimensijos** turėtumėte matyti šią eilutę tinklelyje:</span><span class="sxs-lookup"><span data-stu-id="ce42e-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="ce42e-331">**Vienetas:** *vnt*</span><span class="sxs-lookup"><span data-stu-id="ce42e-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="ce42e-332">**Bruto svoris:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="ce42e-333">**Plotis:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="ce42e-334">**Gylis:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="ce42e-335">**Aukštis:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="ce42e-336">**Tūris:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="ce42e-337">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-337">Close the page.</span></span>
1. <span data-ttu-id="ce42e-338">Pasirinkite produktą, kurio **Prekės numerio** laukas nustatytas į *„A0002”*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="ce42e-339">Veiksmų juostoje, **Inventoriaus valdymo** skirtuke, **Sandėlio** grupėje, pasirinkite **Fiziniai matmenys**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="ce42e-340">Puslapyje **Faktinės dimensijos** turėtumėte matyti šią eilutę tinklelyje:</span><span class="sxs-lookup"><span data-stu-id="ce42e-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="ce42e-341">**Vienetas:** *vnt*</span><span class="sxs-lookup"><span data-stu-id="ce42e-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="ce42e-342">**Bruto svoris:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="ce42e-343">**Plotis:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="ce42e-344">**Gylis:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="ce42e-345">**Aukštis:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="ce42e-346">**Tūris:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="ce42e-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="ce42e-347">1 pardavimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-347">Create sales order 1</span></span>

<span data-ttu-id="ce42e-348">Norėdami sukurti pardavimo užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-349">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ce42e-350">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ce42e-351">Atsiranda dialogo langas, skirtas naujo pardavimo užsakymui kūrimui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="ce42e-352">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ce42e-352">Set the following values:</span></span>

    - <span data-ttu-id="ce42e-353">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ce42e-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ce42e-354">**Sandėlis:** *63*</span><span class="sxs-lookup"><span data-stu-id="ce42e-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ce42e-355">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ce42e-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ce42e-356">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ce42e-356">The new sales order is opened.</span></span> <span data-ttu-id="ce42e-357">„FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateiktas pardavimo eilutes:</span><span class="sxs-lookup"><span data-stu-id="ce42e-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="ce42e-358">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="ce42e-358">Line 1:</span></span>

        - <span data-ttu-id="ce42e-359">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ce42e-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ce42e-360">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="ce42e-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="ce42e-361">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="ce42e-361">Line 2:</span></span>

        - <span data-ttu-id="ce42e-362">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ce42e-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ce42e-363">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="ce42e-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="ce42e-364">Pasirinkite pirmą eilutę, o tada pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ce42e-365">**Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="ce42e-366">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-366">Then close the page.</span></span>
1. <span data-ttu-id="ce42e-367">Pakartokite pirmus du antrosios eilutės veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="ce42e-368">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="ce42e-369">Pardavimo užsakymo 2 sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-369">Create sales order 2</span></span>

<span data-ttu-id="ce42e-370">Norėdami sukurti antrą pardavimo užsakymą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-371">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ce42e-372">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ce42e-373">Atsiranda dialogo langas, skirtas naujo pardavimo užsakymui kūrimui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="ce42e-374">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ce42e-374">Set the following values:</span></span>

    - <span data-ttu-id="ce42e-375">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ce42e-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ce42e-376">**Sandėlis:** *63*</span><span class="sxs-lookup"><span data-stu-id="ce42e-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ce42e-377">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="ce42e-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ce42e-378">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="ce42e-378">The new sales order is opened.</span></span> <span data-ttu-id="ce42e-379">„FastTab” **Pardavimo užsakymo eilutės** įtraukite toliau pateiktas pardavimo eilutes:</span><span class="sxs-lookup"><span data-stu-id="ce42e-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="ce42e-380">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="ce42e-380">Line 1:</span></span>

        - <span data-ttu-id="ce42e-381">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ce42e-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ce42e-382">**Kiekis:** *4*</span><span class="sxs-lookup"><span data-stu-id="ce42e-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="ce42e-383">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="ce42e-383">Line 2:</span></span>

        - <span data-ttu-id="ce42e-384">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ce42e-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ce42e-385">**Kiekis:** *4*</span><span class="sxs-lookup"><span data-stu-id="ce42e-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="ce42e-386">Pasirinkite pirmą eilutę, o tada pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="ce42e-387">**Rezervacijos** puslapyje pasirinkite **Rezervavimo vieta**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="ce42e-388">Tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-388">Then close the page.</span></span>
1. <span data-ttu-id="ce42e-389">Pakartokite pirmus du antrosios eilutės veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="ce42e-390">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="ce42e-391">Krovinio kūrimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-391">Create the load</span></span>

<span data-ttu-id="ce42e-392">Norėdami sukurti krovinį kiekvienam šiame scenarijuje sukurtam užsakymui ir tada išleisti jį į sandėlį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="ce42e-393">Eikite į **Sandėlio valdymas \> Kroviniai \> Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="ce42e-394">Skirtuke **Pardavimo eilutės** raskite ir pasirinkite visas pardavimo užsakymo eilutes iš pardavimo užsakymų, sukurtų šiam scenarijui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="ce42e-395">Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="ce42e-396">Pasirinktos užsakymo eilutės įtraukiamos į naują krovinį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="ce42e-397">Dialogo lango **Krovinio šablono priskyrimas** lauke **Krovinio šablono ID** pasirinkite krovinio šabloną, pavyzdžiui, *40' konteineris*.</span><span class="sxs-lookup"><span data-stu-id="ce42e-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="ce42e-398">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ce42e-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ce42e-399">Dalyje **Kroviniai** raskite ir pasirinkite ką tik sukurtą krovinį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="ce42e-400">Pasirinkite **Išleisti \> Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="ce42e-401">Dialogo lange **Išleisti į sandėlį** pasirinkite **GERAI**, kad išleistumėte pasirinktą krovinį į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ce42e-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="ce42e-402">Siuntų ir konteinerių patikrinimas</span><span class="sxs-lookup"><span data-stu-id="ce42e-402">Verify the shipments and containers</span></span>

<span data-ttu-id="ce42e-403">Toliau pateikta procedūra jums leidžia patikrinti sukurtas siuntas.</span><span class="sxs-lookup"><span data-stu-id="ce42e-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="ce42e-404">Naudokite ją peržiūrėti užsakymui, kurį sukūrėte šiam scenarijui, kad įsitikintumėte gavę numatytus rezultatus.</span><span class="sxs-lookup"><span data-stu-id="ce42e-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="ce42e-405">Eikite į **Sandėlio valdymas \> Siuntos \> Visos siuntos**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="ce42e-406">Raskite ir pasirinkite siuntą, kuri buvo sukurta ką tik išleistam kroviniui.</span><span class="sxs-lookup"><span data-stu-id="ce42e-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="ce42e-407">Veiksmų srities skirtuke **Transportavimas** pasirinkite **Rodyti konteinerius**.</span><span class="sxs-lookup"><span data-stu-id="ce42e-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="ce42e-408">Patvirtinkite, kad prekės iš pardavimo užsakymų buvo sukrautos į du skirtingus konteinerius.</span><span class="sxs-lookup"><span data-stu-id="ce42e-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce42e-409">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ce42e-409">Additional resources</span></span>

- [<span data-ttu-id="ce42e-410">Krovimas į konteinerius</span><span class="sxs-lookup"><span data-stu-id="ce42e-410">Containerization</span></span>](wave-containerization.md)
