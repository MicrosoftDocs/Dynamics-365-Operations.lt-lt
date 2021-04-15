---
title: Fiktyvios prekės
description: Šioje temoje išsamiai aprašoma, kaip eilutės tipą Fiktyvi galima naudoti komplektavimo specifikacijos (KS) ir formulės eilutėms programoje „Dynamics 365 Supply Chain Management“.
author: ShylaThompson
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1118d7334602e450e5d503632895f73ba19066a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814783"
---
# <a name="phantom-items"></a><span data-ttu-id="6fb0a-103">Fiktyvios prekės</span><span class="sxs-lookup"><span data-stu-id="6fb0a-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fb0a-104">Šioje temoje aprašoma, išsamiai, kaip eilutės tipą Fiktyvi galima naudoti komplektavimo specifikacijos (KS) ir formulės eilutėms.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="6fb0a-105">Toliau pateiktoje iliustracijoje (a) yra produkto H (F ir G dalių) KS, o (b) yra produkto H (F dalies) maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Produktas H, F dalis](media/product-H-part-F.png)


<span data-ttu-id="6fb0a-107">Šioje iliustracijoje rodomas dviejų lygių KS struktūros pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="6fb0a-108">Užbaigtas produktas H atitinka mašinos rinkinio produktą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="6fb0a-109">Mašinos rinkinys sudarytas iš dviejų dalių: elektros įrenginio (F), kuris turi dvi medžiagas (A ir B), ir pakavimo medžiagų grupės (G), kuri taip pat turi dvi medžiagas (C ir D).</span><span class="sxs-lookup"><span data-stu-id="6fb0a-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="6fb0a-110">Kita medžiaga (E) naudojama atliekant bendrąjį mašinos surinkimą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Produktas H, F dalis](media/product-H-part-B.png)

<span data-ttu-id="6fb0a-112">Pirmesnėje iliustracijoje vaizduojama produkto H inžinerinė KS. Ši struktūra suteikia galimybę peržiūrėti viso mašinos rinkinio dalis ir komponentus.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="6fb0a-113">Tačiau, nors produkto kūrėjams toks KS atvaizdavimas gali pasirodyti priimtinesnis, kuriant šią struktūrą gali būti nepakankamai atsižvelgta į tai, kaip mašina stovi ant parduotuvės grindų.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="6fb0a-114">Pavyzdžiui, pirmesnėje iliustracijoje vaizduojamoje inžinerinėje KS matoma, kad elektrinis įrenginys F surinktas kaip atskira dalis atskirame darbo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="6fb0a-115">Tačiau renkant elektrinį įrenginį ant parduotuvės grindų gali būti tikslingiau jį surinkti kaip bendro mašinos rinkinio dalį, ne kaip atskirą darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="6fb0a-116">Šioje inžinerinėje KS taip pat vaizduojama, kad G dalis yra atskira dalis.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="6fb0a-117">Tačiau šioje struktūroje G dalis yra ne fizinė dalis, o pakavimo medžiagų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="6fb0a-118">Todėl, nors inžinerinė KS yra itin naudinga kuriant produktą ir jį plėtojant, tai gali būti ne pats logiškiausias būdas produkto gamybos vykdymo procesui palaikyti.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="6fb0a-119">Priešingai, gamybos KS yra geriausias būdas sukurti produktą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="6fb0a-120">Toliau pateiktoje iliustracijoje vaizduojama, kaip inžinerinė KS perkeliama į gamybos KS.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="6fb0a-121">Šioje iliustracijoje (a) yra produkto H KS, o b yra produkto H maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="6fb0a-122">Šioje struktūroje galite matyti, kad visiškai neliko F ir G dalių, o medžiagos, iš kurių šios dalys sudarytos, perkeltos į kitą KS lygį.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="6fb0a-123">Priešingai negu inžinerinėje KS, kurioje buvo du operacijų lapai, gamybos KS yra tik vienas operacijų lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="6fb0a-124">Su G dalimi susieta pakuotės operacija taip pat perkelta ir dabar yra produkto H operacijų lapo dalis. Elektros įrenginio surinkimas yra pirmoji operacija.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="6fb0a-125">Ši tvarka racionali, nes šis įrenginys naudojamas kitoje operacijoje, kuri yra mašinos surinkimas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="6fb0a-126">Paskutinė operacija yra pakavimo operacija, kurią atliekant naudojamos dvi pakavimo medžiagos (C ir D).</span><span class="sxs-lookup"><span data-stu-id="6fb0a-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="6fb0a-127">Perėjimą nuo inžinerinės KS prie gamybos KS galima atlikti naudojant fiktyvios KS eilutės tipą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="6fb0a-128">Kaip galima spręsti iš termino „fiktyvi“ reikšmės, pereinant nuo vieno KS tipo prie kito, F ir G dalių neliko.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="6fb0a-129">Šiame pavyzdyje fiktyvios eilutės tipas taikomas inžinerinės KS F ir G dalių KS eilutėms.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="6fb0a-130">Sukūrus gamybos arba paketo užsakymą inžinerinė KS nukopijuojama į gamybos arba paketo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="6fb0a-131">Tada, kai nustatoma apytikslė užsakymo vertė, įvyksta perėjimas iš inžinerinės KS į gamybos KS, kaip pavaizduota pirmesnėse iliustracijose.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="6fb0a-132">Antroje iliustracijoje vaizduojamame operacijų lape pakavimo medžiagos C ir D yra operacijos įvestis.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="6fb0a-133">Kelių lygių fiktyvios KS struktūros</span><span class="sxs-lookup"><span data-stu-id="6fb0a-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="6fb0a-134">Fiktyvios eilutės tipą galima naudoti kelių lygių KS struktūrose, kaip vaizduojama toliau pateiktoje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="6fb0a-135">Šioje iliustracijoje (a) yra produkto G KS, o (b) yra E ir F dalių ir produkto G maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Produktas G, F dalis su maršruto lapais](media/product-G-route-sheet-G.png)


<span data-ttu-id="6fb0a-137">Toliau pateiktoje iliustracijoje vaizduojama gamybos KS ir maršruto lapas, jei E ir F dalių KS eilutės sukonfigūruotos taip, kad eilutės tipas yra Fiktyvi.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="6fb0a-138">Šioje iliustracijoje (a) yra produkto G KS, o (b) yra produkto G maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Produktas G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="6fb0a-140">Fiktyvus elementas ir maršruto tinklas</span><span class="sxs-lookup"><span data-stu-id="6fb0a-140">Phantom and route network</span></span>
<span data-ttu-id="6fb0a-141">Fiktyvi KS taip pat gali būti naudojama maršruto tinklą turinčiai KS.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="6fb0a-142">Maršruto tinkle viena ar kelios operacijos vykdomos lygiagrečiai.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="6fb0a-143">Toliau pateiktoje iliustracijoje vaizduojamas kelių lygių KS naudojamo maršruto tinklo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="6fb0a-144">Šioje iliustracijoje (a) yra produkto G ir F dalies KS, o (b) yra produkto G ir F dalies, kurioje yra maršruto tinklas, maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Produktas G, F dalis](media/product-G-part-F.png)


<span data-ttu-id="6fb0a-146">Toliau pateiktoje iliustracijoje (a) yra produkto G ir F dalies KS, o (b) yra produkto G ir F dalies maršruto lapas.</span><span class="sxs-lookup"><span data-stu-id="6fb0a-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Produktas G, F dalis su maršruto lapais](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]