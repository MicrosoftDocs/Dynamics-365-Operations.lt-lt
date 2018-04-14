---
title: "Atsargų vietos"
description: "Atsargų vietos naudojamos su pagrindinio sandėliavimo (WMS I) funkcijomis ir jomis nustatoma, kur prekės saugomos ir iš kur prekės paimamos WMS I sandėlyje."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2a0af10d1d94f9ead2b024e1afd009d60ee13590
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="inventory-locations"></a><span data-ttu-id="cdd72-103">Atsargų vietos</span><span class="sxs-lookup"><span data-stu-id="cdd72-103">Inventory locations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="cdd72-104">Atsargų vietos naudojamos su pagrindinio sandėliavimo (WMS I) funkcijomis ir jomis nustatoma, kur prekės saugomos ir iš kur prekės paimamos WMS I sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="cdd72-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="cdd72-105">Ši tema taikoma priemonėms modulyje Atsargų valdymas.</span><span class="sxs-lookup"><span data-stu-id="cdd72-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="cdd72-106">Ji nėra taikoma priemonėms modulyje Sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="cdd72-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="cdd72-107">Terminas vieta reiškia vietą, kurioje laikomos ir iš kurios paimamos prekės.</span><span class="sxs-lookup"><span data-stu-id="cdd72-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="cdd72-108">Kiekvienai vietai taip pat galima nurodyti, kur prekę galima padėti.</span><span class="sxs-lookup"><span data-stu-id="cdd72-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="cdd72-109">Pagal numatytuosius parametrus, tai – ta pati vieta.</span><span class="sxs-lookup"><span data-stu-id="cdd72-109">By default, they are the same.</span></span> <span data-ttu-id="cdd72-110">Prekės paprastai padedamos ir paimamos iš tos pačios vietos pusės, bet ne visada.</span><span class="sxs-lookup"><span data-stu-id="cdd72-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="cdd72-111">Pavyzdžiui, stelažuose laikomos prekės padedamos viename perėjime, o paimamos iš kito.</span><span class="sxs-lookup"><span data-stu-id="cdd72-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="cdd72-112">Pagrindiniai duomenys teikia vietos pavadinimą, kuris paprastai nustatomas pagal jos koordinates: sandėlis, perėjimas, stelažas, lentynos ir talpyklos.</span><span class="sxs-lookup"><span data-stu-id="cdd72-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="cdd72-113">Šį pavadinimą arba ID galima įvesti rankiniu būdu arba generuoti naudojant vietos koordinates, pvz., 01-02-03-4 puslapyje Atsargų vietos reiškia 1 perėjimą, 2 stelažą, 3 lentyną, 4 talpyklą.</span><span class="sxs-lookup"><span data-stu-id="cdd72-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="cdd72-114">Vietos ypatybės</span><span class="sxs-lookup"><span data-stu-id="cdd72-114">Location properties</span></span>

<span data-ttu-id="cdd72-115">Vieta apibūdinama nurodant:</span><span class="sxs-lookup"><span data-stu-id="cdd72-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="cdd72-116">Dydis (aukštis, plotis, gylis, taigi ir tūris)</span><span class="sxs-lookup"><span data-stu-id="cdd72-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="cdd72-117">Sandėlio, perėjimo, stelažo, lentynos ir talpyklos vieta</span><span class="sxs-lookup"><span data-stu-id="cdd72-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="cdd72-118">Vietos tipas (buferinė vieta, paėmimo vieta, atvežimo rampa, pakrovimo rampa, gamybos įvesties vieta, tikrinimo vieta arba „kanban“ prekybos centras)</span><span class="sxs-lookup"><span data-stu-id="cdd72-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="cdd72-119">Norint patikrinti, ar operatorius konkrečiai prekei pasirinko tinkamą vietą, tinklo sistemose gali būti naudojamas tikrinimo tekstas.</span><span class="sxs-lookup"><span data-stu-id="cdd72-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="cdd72-120">Šį tikrinimo tekstą galima sukurti neautomatiniu būdu arba nustatyti kaip numatytąjį.</span><span class="sxs-lookup"><span data-stu-id="cdd72-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="cdd72-121">Rūšiavimo kodai</span><span class="sxs-lookup"><span data-stu-id="cdd72-121">Sort codes</span></span>
<span data-ttu-id="cdd72-122">Naudojant rūšiavimo kodus galima optimizuoti paėmimo eilučių, kuriose smulkiai aprašoma informacija, būtina prekėms iš atsargų paimti, tvarkymą, įskaitant išrinkimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="cdd72-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="cdd72-123">Rūšiavimo kodus galima nurodyti pagal perėjimus ir kitas koordinates arba priskirti vietai rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="cdd72-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="cdd72-124">Užblokuotos vietos</span><span class="sxs-lookup"><span data-stu-id="cdd72-124">Blocked locations</span></span>
<span data-ttu-id="cdd72-125">Kartais galite norėti nurodyti, kad tam tikram laikui vieta užblokuota, pvz., remontui.</span><span class="sxs-lookup"><span data-stu-id="cdd72-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="cdd72-126">Be to, vietą kartais gali tekti nurodyti kaip užblokuotą tik įeigai arba tik išeigai.</span><span class="sxs-lookup"><span data-stu-id="cdd72-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="cdd72-127">Medžio struktūra</span><span class="sxs-lookup"><span data-stu-id="cdd72-127">Tree structure</span></span>

<span data-ttu-id="cdd72-128">Puslapyje Atsargų vietos galite peržiūrėti medžio struktūros pagal atsargų vietų koordinates sandėlio maketą apibrėžto rodymo formatu.</span><span class="sxs-lookup"><span data-stu-id="cdd72-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="cdd72-129">Atsargų vietų tvarkymas naudojant sandėlio formą</span><span class="sxs-lookup"><span data-stu-id="cdd72-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="cdd72-130">Galima kopijuoti vietas iš vieno sandėlio į kitą ir kurti vietas naudojant vedlį.</span><span class="sxs-lookup"><span data-stu-id="cdd72-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="cdd72-131">Prieš paleisdami vedlį, turite įsitikinti, kad puslapyje Sandėlis nustatėte numatytuosius vietų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="cdd72-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="see-also"></a><span data-ttu-id="cdd72-132">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="cdd72-132">See also</span></span>
--------

[<span data-ttu-id="cdd72-133">Kurti naują sandėlio maketą (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="cdd72-133">Create a new warehouse layout (Task guide)</span></span>](tasks/create-new-warehouse-layout.md)

