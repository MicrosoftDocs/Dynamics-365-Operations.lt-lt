---
title: Krovinių šablonai
description: Ši tema aprašo, kaip nustatyti krovinio šablonus ir kaip susieti krovinio šabloną su nauju kroviniu.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646416"
---
# <a name="load-templates"></a><span data-ttu-id="45d23-103">Krovinių šablonai</span><span class="sxs-lookup"><span data-stu-id="45d23-103">Load templates</span></span>

<span data-ttu-id="45d23-104">Jums sukūrus naują krovinį, galtie priskirti krovinio šabloną.</span><span class="sxs-lookup"><span data-stu-id="45d23-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="45d23-105">Krovinio šablone pateikta informacija apie įrangą ir apie matmenis, tokius kaip aukštis, plotis, gylis ir krovinio apimtis.</span><span class="sxs-lookup"><span data-stu-id="45d23-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="45d23-106">Ši tema aprašo, kaip nustatyti krovinio šablonus ir kaip susieti krovinio šabloną su nauju kroviniu.</span><span class="sxs-lookup"><span data-stu-id="45d23-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="45d23-107">Nustatyti krovinio šabloną</span><span class="sxs-lookup"><span data-stu-id="45d23-107">Set up a load template</span></span>

1. <span data-ttu-id="45d23-108">Eikite į **Gabenimo valdymas \> Nustatymai \> Krovinio kūrimas \> Krovinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="45d23-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="45d23-109">Veiksmų juostoje pasirinkite **Naujas** tam, kad įtrauktumėte naują šabloną arba **Redaguoti** tam, kad redaguotumėte esamą šabloną.</span><span class="sxs-lookup"><span data-stu-id="45d23-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="45d23-110">Eilutėje naujam ar esančiam šablonui, nustatykite tolesnius laukelius:</span><span class="sxs-lookup"><span data-stu-id="45d23-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="45d23-111">**Krovinio šablono ID** - Įveskite unikalų ID krovinio šablonui.</span><span class="sxs-lookup"><span data-stu-id="45d23-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="45d23-112">**Įranga** – Pasirinkite įrangą, kuri turi būti naudojama siekiant išsiųsti krovinį.</span><span class="sxs-lookup"><span data-stu-id="45d23-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="45d23-113">**Krovinio aukštis**, **Krovinio plotis** ir **Krovinio gylis** – Įveskite krovinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="45d23-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="45d23-114">**Maks. leidžiamas krovinio tūris** ir **Maks. leidžiamas krovinio plotis** – Įveskite maksimalų leistiną krovinio svorį ir tūrį.</span><span class="sxs-lookup"><span data-stu-id="45d23-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="45d23-115">**Maks. leidžiamas bendras svoris** – Įveskite maksimalų leistiną bendrą krovinio svorį.</span><span class="sxs-lookup"><span data-stu-id="45d23-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="45d23-116">Bendras krovinio svoris apima tiek pakuotės, tiek ir krovinio svorį.</span><span class="sxs-lookup"><span data-stu-id="45d23-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="45d23-117">**Maks. leidžiamas skaičius siunčiamų krovinio dalių** – Įveskite maksimalų skaičių krovinio dalių, kurios gali sudaryti krovinį.</span><span class="sxs-lookup"><span data-stu-id="45d23-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="45d23-118">**Padėkite krovinį ant grindų** – Pasirinkite šį žymimą laukelį, kad būtų naudojamas grindų krovinys.</span><span class="sxs-lookup"><span data-stu-id="45d23-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="45d23-119">Ant grindų krovinio scenarijaus atveju, dėžės yra padėtos ant grindų iki lubų ir nuo sienos iki sienos talpykloje siekiant maksimizuoti talpą.</span><span class="sxs-lookup"><span data-stu-id="45d23-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="45d23-120">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="45d23-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="45d23-121">Susiekite krovinio šabloną su naujų kroviniu</span><span class="sxs-lookup"><span data-stu-id="45d23-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="45d23-122">Eikite į **Gabenimo valdymas \> Planavimas \> Krovinio planavimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="45d23-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="45d23-123">Viršutinėje puslapio dalyje, pasirinkite vieną iš tolesnių skirtukų priklausomai nuo šaltinio dokumento tipo, kuriam kuriate krovinį: **Siuntimai**, **Pardavimo eilutės**, **Perdavimo eilutės** ar **Įsigijimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="45d23-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="45d23-124">Pasirinkite konkrečius dokumentus, kad suplanuotumėte krovinį.</span><span class="sxs-lookup"><span data-stu-id="45d23-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="45d23-125">Veiksmų srities **Tiekti ir pareikalauti** skirtuke **Pridėti** grupėje pasirinkite **Į naują krovinį**.</span><span class="sxs-lookup"><span data-stu-id="45d23-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="45d23-126">Teksto laukelyje **Krovinio šablonas** **Krovinio šablono ID** laukelyje pasirinkite taikomą šabloną.</span><span class="sxs-lookup"><span data-stu-id="45d23-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="45d23-127">Pasirinkite **GERAI** norėdami pritaikyti šabloną.</span><span class="sxs-lookup"><span data-stu-id="45d23-127">Select **OK** to apply the template.</span></span>
