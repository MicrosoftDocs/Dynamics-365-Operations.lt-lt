---
title: "Nusidėvėjimo metodai ir konvencijos"
description: "Šiame straipsnyje apžvelgiamos nusidėvėjimo konvencijos ir nusidėvėjimo metodai, kuriuos palaiko „Microsoft Dynamics 365 for Finance and Operations“."
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="61f22-103">Nusidėvėjimo metodai ir konvencijos</span><span class="sxs-lookup"><span data-stu-id="61f22-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61f22-104">Šiame straipsnyje apžvelgiamos nusidėvėjimo konvencijos ir nusidėvėjimo metodai, kuriuos palaiko „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="61f22-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="61f22-105">Galite pasirinkti įvairius nusidėvėjimo metodus bei konvencijas.</span><span class="sxs-lookup"><span data-stu-id="61f22-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="61f22-106">Metodų paskirtis yra paskirstyti ilgalaikio turto nusidėvėjimo vertę finansiniams laikotarpiams.</span><span class="sxs-lookup"><span data-stu-id="61f22-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="61f22-107">Ilgalaikio turto nusidėvėjimo vertė yra įsigijimo vertė, sumažėjusi dėl likvidacinės vertės (jei tokia buvo).</span><span class="sxs-lookup"><span data-stu-id="61f22-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="61f22-108">Jei taikote nusidėvėjimo konvenciją ir pakeičiate paskutinio turto nusidėvėjimo datą, dėl kurios praleidžiami keli nusidėvėjimai, praėjusių metų nusidėvėjimas gali būti didesnis arba mažesnis, nei buvo tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="61f22-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="61f22-109">Nusidėvėjimas yra koreguojamas nusidėvėjimo laikotarpių, kurios paveikė paskutinio nusidėvėjimo datos modifikavimas, skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="61f22-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="61f22-110">Pavyzdžiui, jei naudojate pusmečio nusidėvėjimo konvenciją trejus metus, nusidėvėjimas paprastai atsiranda per 3 1/2 metų.</span><span class="sxs-lookup"><span data-stu-id="61f22-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="61f22-111">Jei pakeičiate paskutinę nusidėvėjimo dieną per 3 1/2 metų, praėjusių metų nusidėvėjimas iškelia paveiktus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="61f22-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="61f22-112">Jei datą perkeliate per tris mėnesius, praėję metai turės devynių mėnesių vertės nusidėvėjimą, nors paprastai tai būtų šešių mėnesių vertės nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="61f22-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="61f22-113">Galite pasirinkti iš šių nusidėvėjimo konvencijų.</span><span class="sxs-lookup"><span data-stu-id="61f22-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="61f22-114">Pusmetis</span><span class="sxs-lookup"><span data-stu-id="61f22-114">Half year</span></span>
-   <span data-ttu-id="61f22-115">Visas mėnuo</span><span class="sxs-lookup"><span data-stu-id="61f22-115">Full month</span></span>
-   <span data-ttu-id="61f22-116">Ketvirčio vidurys</span><span class="sxs-lookup"><span data-stu-id="61f22-116">Mid quarter</span></span>
-   <span data-ttu-id="61f22-117">Mėnesio vidurys (mėnesio 1 d.)</span><span class="sxs-lookup"><span data-stu-id="61f22-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="61f22-118">Mėnesio vidurys (mėnesio 15 d.)</span><span class="sxs-lookup"><span data-stu-id="61f22-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="61f22-119">Pusė metų (metų pradžia)</span><span class="sxs-lookup"><span data-stu-id="61f22-119">Half year (start of year)</span></span>
-   <span data-ttu-id="61f22-120">Pusė metų (kiti metai)</span><span class="sxs-lookup"><span data-stu-id="61f22-120">Half year (next year)</span></span>

<span data-ttu-id="61f22-121">Galite pasirinkti šiuos nusidėvėjimo metodus:</span><span class="sxs-lookup"><span data-stu-id="61f22-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="61f22-122">Tiesiogiai proporcingas dėvėjimo laikas</span><span class="sxs-lookup"><span data-stu-id="61f22-122">Straight line service life</span></span>
-   <span data-ttu-id="61f22-123">Mažėjanti vertė</span><span class="sxs-lookup"><span data-stu-id="61f22-123">Reducing balance</span></span>
-   <span data-ttu-id="61f22-124">Rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="61f22-124">Manual</span></span>
-   <span data-ttu-id="61f22-125">Koeficientas</span><span class="sxs-lookup"><span data-stu-id="61f22-125">Factor</span></span>
-   <span data-ttu-id="61f22-126">Sunaudojimas</span><span class="sxs-lookup"><span data-stu-id="61f22-126">Consumption</span></span>
-   <span data-ttu-id="61f22-127">Likęs tiesiogiai proporcingas laikas</span><span class="sxs-lookup"><span data-stu-id="61f22-127">Straight line life remaining</span></span>
-   <span data-ttu-id="61f22-128">200% mažėjanti vertė</span><span class="sxs-lookup"><span data-stu-id="61f22-128">200% reducing balance</span></span>
-   <span data-ttu-id="61f22-129">175% mažėjanti vertė</span><span class="sxs-lookup"><span data-stu-id="61f22-129">175% reducing balance</span></span>
-   <span data-ttu-id="61f22-130">150% mažėjanti vertė</span><span class="sxs-lookup"><span data-stu-id="61f22-130">150% reducing balance</span></span>
-   <span data-ttu-id="61f22-131">125% mažėjanti vertė</span><span class="sxs-lookup"><span data-stu-id="61f22-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="61f22-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="61f22-132">Additional resources</span></span>
--------

[<span data-ttu-id="61f22-133">Ilgalaikio turto nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="61f22-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="61f22-134">Tiesiogiai proporcingas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="61f22-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="61f22-135">Mažėjančios vertės nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="61f22-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="61f22-136">Neautomatinis nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="61f22-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="61f22-137">Nusidėvėjimo faktorius</span><span class="sxs-lookup"><span data-stu-id="61f22-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="61f22-138">Produkcijos metodas</span><span class="sxs-lookup"><span data-stu-id="61f22-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="61f22-139">Tiesiogiai proporcingas likutinės vertės nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="61f22-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="61f22-140">125 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="61f22-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="61f22-141">150 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="61f22-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="61f22-142">175 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="61f22-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="61f22-143">200 procentų mažėjančios vertės metodas</span><span class="sxs-lookup"><span data-stu-id="61f22-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




