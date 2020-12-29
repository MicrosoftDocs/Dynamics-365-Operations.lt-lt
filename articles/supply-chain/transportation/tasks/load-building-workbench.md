---
title: Krovinio kūrimo darbo sritis
description: Ši tema aprašo, kaip dirbti su krovinio kūrimo darbo sritimi.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 429a8bac5491a342ecbc8b67c59c71715a4b0889
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646417"
---
# <a name="load-building-workbench"></a><span data-ttu-id="95466-103">Krovinio kūrimo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="95466-103">Load building workbench</span></span>

<span data-ttu-id="95466-104">Krovinio kūrimo darbo sritis leidžia jums taikyti krovinio kūrimo strategijas kuriant krovinius.</span><span class="sxs-lookup"><span data-stu-id="95466-104">The load building workbench lets you apply load building strategies when you create loads.</span></span>

## <a name="create-a-load-building-strategy"></a><span data-ttu-id="95466-105">Sukurkite krovinio kūrimo strategiją</span><span class="sxs-lookup"><span data-stu-id="95466-105">Create a load building strategy</span></span>

<span data-ttu-id="95466-106">Naudojate krovinio kūrimo strategijas automatiniu būdu sukurti krovinius.</span><span class="sxs-lookup"><span data-stu-id="95466-106">You use load building strategies to automatically build loads.</span></span> <span data-ttu-id="95466-107">Ši funkcija gali būti naudinga tolesnėse situacijose:</span><span class="sxs-lookup"><span data-stu-id="95466-107">This capability can be beneficial in the following situations:</span></span>

- <span data-ttu-id="95466-108">Jei reguliariai sunčiate konkretų produktų rinkinį, krovinio strategijos padės sutaupyti laiko, nes jums nereikės sukurti to paties krovinio kas kartą.</span><span class="sxs-lookup"><span data-stu-id="95466-108">If you regularly ship a specific set of products, load strategies help save time, because you don't have to build the same load every time.</span></span>
- <span data-ttu-id="95466-109">Jei norite išvengti pusiau pilnų krovinių siekiant maksimizuoti efektyvumą, krovinio strategijos gali padėti užpildyti kiekvieną krovinį kaip įmanoma labiau.</span><span class="sxs-lookup"><span data-stu-id="95466-109">If you want to avoid half-full loads to maximize efficiency, load strategies can help fill each load as much as possible.</span></span>

<span data-ttu-id="95466-110">Krovinio kūrimo strategijos klasė pavadinimu `TMSLoadBuildingVolumeStrategy` suteikia krovinio kūrimo strategiją pavadinimu *Apimtimi pagrįsta krovinio kūrimo strategija*.</span><span class="sxs-lookup"><span data-stu-id="95466-110">A load building strategy class that is named `TMSLoadBuildingVolumeStrategy` provides a load building strategy that is named *Volume-based load building strategy*.</span></span> <span data-ttu-id="95466-111">Naudojant šią strategiją galima naudoti maksimalias aukščio ir svorio reikšmes, nurodytas krovinio šablone, arba galima nepaisyti parametrų įvedant naujas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="95466-111">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="95466-112">Ši strategija yra tik strategija įtraukta nestandartiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="95466-112">This strategy is the only strategy that is included out of the box.</span></span> <span data-ttu-id="95466-113">(Nepaisant to, galite turėti tinkintas strategijas.)</span><span class="sxs-lookup"><span data-stu-id="95466-113">(However, you might have some custom strategies.)</span></span>

<span data-ttu-id="95466-114">Norėdami naudoti nestandartinę *Apimtimi grįsta krovinio kūrimo strategiją* strategiją pasirinkite **Krovinio kūrimo strategijos** laukelį **Krovinio kūrimo darbo srities** puslapyje (**Gabenimo valdymas &gt; Planavimas &gt; Krovinio kūrimo darbo strategija**).</span><span class="sxs-lookup"><span data-stu-id="95466-114">To use the out-of-box *Volume-based load building strategy* strategy, select it in the **Load building strategy** field on the **Load building workbench** page (**Transportation management &gt; Planning &gt; Load building workbench**).</span></span>

<span data-ttu-id="95466-115">Norėdami sukurti krovinio kūrimo strategiją, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="95466-115">To create a load building strategy, follow these steps.</span></span>

1. <span data-ttu-id="95466-116">Eikite į **Gabenimo valdymas &gt; Nustatymai &gt; Krovinio kūrimas &gt; Krovinio kūrimo strategijos**.</span><span class="sxs-lookup"><span data-stu-id="95466-116">Go to **Transportation management &gt; Setup &gt; Load building &gt; Load building strategies**.</span></span>
1. <span data-ttu-id="95466-117">Veiksmų juostoje pasirinkite **Sukurti klasės sąrašą** tam, kad įsitikintumėte, kad turite naujausias esamų klasių versijas.</span><span class="sxs-lookup"><span data-stu-id="95466-117">On the Action Pane, select **Generate class list** to make sure that you have the latest versions of all available classes.</span></span>
1. <span data-ttu-id="95466-118">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="95466-118">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="95466-119">Įveskite unikalų strategijos pavadinimą, pasirinkite krovinio kūrimo strategijos klasę jam ir įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="95466-119">Enter a unique name for the strategy, select the load building strategy class for it, and enter a description.</span></span>
1. <span data-ttu-id="95466-120">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="95466-120">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="95466-121">Veiksmų srityje pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="95466-121">On the Action Pane, select **Parameters**.</span></span>
1. <span data-ttu-id="95466-122">Puslapyje **Krovinio kūrimo strategijos parametrai** puslapyje rinkitės **Apimties talpa** sąraše ir tada **Vertės** laujelyje įveskite krovinio bendros apimties pajėgumo procentą, kuris turi būti taikomas naujai krovinio kūrimo strategijai.</span><span class="sxs-lookup"><span data-stu-id="95466-122">On the **Load building strategy parameters** page, select **Volume capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total volume capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="95466-123">Pasirinkite **Krovinio pajėgumas** sąraše ir tada **Vertės** laukelyje įveskite krovinio bendro svorio pajėgumo procentą, kuris turi būti taikomas naujai krovinio kūrimo strategijai.</span><span class="sxs-lookup"><span data-stu-id="95466-123">Select **Weight capacity** in the list, and then, in the **Value** field, enter the percentage of the load's total weight capacity that should be applied for the new load building strategy.</span></span>
1. <span data-ttu-id="95466-124">Uždarykite **Krovinio kūrimo strategijos parametrų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="95466-124">Close the **Load building strategy parameters** page.</span></span>
1. <span data-ttu-id="95466-125">Uždarykite **Krovinio kūrimo strategijų parametrų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="95466-125">Close the **Load building strategies** page.</span></span>

<span data-ttu-id="95466-126">Dabar galite priskirti krovinio kūrimo strategiją tam, kad sukurtumėte krovinio šabloną.</span><span class="sxs-lookup"><span data-stu-id="95466-126">You can now assign the load building strategy to a load building template.</span></span> <span data-ttu-id="95466-127">Kitu atveju, galite naudoti jį tiesiogiai krovinio planavimo darbo srtiyje.</span><span class="sxs-lookup"><span data-stu-id="95466-127">Alternatively, you can use it directly in the load planning workbench.</span></span>

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a><span data-ttu-id="95466-128">Naudokite krovinio kūrimo strategiją krovinio kūrimo darbo srityje</span><span class="sxs-lookup"><span data-stu-id="95466-128">Use a load building strategy in the load building workbench</span></span>

1. <span data-ttu-id="95466-129">Eikite į **Gabenimo valdymas &gt; Planavimas &gt; Krovinio kūrimo darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="95466-129">Go to **Transportation management &gt; Planning &gt; Load building workbench**.</span></span>
1. <span data-ttu-id="95466-130">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="95466-130">Follow one of these steps:</span></span>

    - <span data-ttu-id="95466-131">Pasirinkite strategiją **Krovinio kūrimo strategijos** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="95466-131">Select a strategy in the **Load building strategy** field.</span></span>
    - <span data-ttu-id="95466-132">Jei nustatote krovinio kūrimo šabloną ir jai priskiriate krovinio kūrimo strategiją, veiksmų juostoje, **Valdyti šablonus** skirtuke, rinkitės **Taikyti šabloną**.</span><span class="sxs-lookup"><span data-stu-id="95466-132">If you've defined a load building template and assigned the load building strategy to it, on the Action Pane, on the **Manage templates** tab, select **Apply template**.</span></span> <span data-ttu-id="95466-133">Tada **Taikyti krovinio kūrimo šabloną** iškrentančiame teksto laukelyje pasirinkite šabloną **Krovinio kūrimo šablono pavadinimo** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="95466-133">Then, in the **Apply load building template** drop-down dialog box, select a template in the **Load building template name** field.</span></span>

1. <span data-ttu-id="95466-134">„FastTab“ **Krovinio šablonų seka** pasirinktie vieną ar daugiau [krovinio šablonų](load-template.md).</span><span class="sxs-lookup"><span data-stu-id="95466-134">On the **Load templates sequence** FastTab, select one or more [load templates](load-template.md).</span></span> <span data-ttu-id="95466-135">Darbo sritis bandys priderinti krovinį prie šių talpyklų tipų čia nurodyta seka.</span><span class="sxs-lookup"><span data-stu-id="95466-135">The workbench will try to fit the load into these types of containers, in the sequence that is specified here.</span></span> <span data-ttu-id="95466-136">Dažniausiai, galite padėti mažiausias talpyklas sąrašo viršuje, kad užtikrintumėte, jog mažiausias galimas konteineris yra pasirinktas pirma.</span><span class="sxs-lookup"><span data-stu-id="95466-136">Typically, you should put the smallest containers at the top of the list to ensure that the smallest possible container is selected first.</span></span>
1. <span data-ttu-id="95466-137">Veiksmų juosoje rinkitės **Siūlyti krovinius**.</span><span class="sxs-lookup"><span data-stu-id="95466-137">On the Action Pane, select **Propose loads**.</span></span>
1. <span data-ttu-id="95466-138">Peržiūrėkite siūlomus krovinius ir krovinių eilutes.</span><span class="sxs-lookup"><span data-stu-id="95466-138">Review the proposed loads and proposed load lines.</span></span>
1. <span data-ttu-id="95466-139">Veiksmų juostoje rinkitės **Kurti krovinius** tam, kad sukurtumėte krovinius pagrįstus šaltinio dokumentų linijoje **Siūlomų krovinių linijų** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="95466-139">On the Action Pane, select **Create loads** to create loads that are based on the source document lines on the **Proposed load lines** FastTab.</span></span>
1. <span data-ttu-id="95466-140">Uždarykite **Krovinio kūrimo darbo srities** puslapį.</span><span class="sxs-lookup"><span data-stu-id="95466-140">Close the **Load building workbench** page.</span></span>
