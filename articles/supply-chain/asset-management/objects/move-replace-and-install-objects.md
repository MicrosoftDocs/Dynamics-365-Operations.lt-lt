---
title: Turto perkėlimas, keitimas ir diegimas
description: Šioje temoje paaiškinta, kaip perkelti, pakeisti ir diegti turtą turto valdyme.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6d7a9c86029505602c562a3de4d2f52eace866f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808549"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="c95d5-103">Turto perkėlimas, keitimas ir diegimas</span><span class="sxs-lookup"><span data-stu-id="c95d5-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c95d5-104">Šioje temoje paaiškinta, kaip perkelti, pakeisti ir diegti turtą turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="c95d5-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="c95d5-105">Galima sukurti atskirą turtą, kuris neturi jokių ryšių su kitu turtu, arba galima sukurti turto struktūrą, apimančią pagrindinį turtą (aukščiausio lygio turtas) ir susijusį antrinį turtą (antrinis turtas).</span><span class="sxs-lookup"><span data-stu-id="c95d5-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="c95d5-106">Turto valdyme yra trys būdai kaip galima perkelti ir keisti turto vietą:</span><span class="sxs-lookup"><span data-stu-id="c95d5-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="c95d5-107">**Perkelti** – perkelkite turtą į kitą turto struktūrą arba į kitą tos pačios turto struktūros vietą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="c95d5-108">**Pakeisti** – laikinai pašalinkite turtą iš turto struktūros, kad jį būtų galima pataisyti arba atnaujinti, o vėliau vėl įtraukti atnaujintą turtą į turto struktūrą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="c95d5-109">Taip pat galima visam laikui pakeisti naudotą turtą nauju turtu.</span><span class="sxs-lookup"><span data-stu-id="c95d5-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="c95d5-110">**Diegti** – funkcinėje vietoje diekite pagrindinį turtą ir visus susijusius antrinius turtus.</span><span class="sxs-lookup"><span data-stu-id="c95d5-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="c95d5-111">Turtas, kurį perkeliate, pakeičiate arba įdiegiate, gali būti susijęs su kita funkcine vieta.</span><span class="sxs-lookup"><span data-stu-id="c95d5-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="c95d5-112">Tokiu atveju turtas gali naudoti funkcinei vietai skirtas finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="c95d5-113">Puslapyje **Funkcinių vietų tipai** nustatomas funkcinių vietų finansinių dimensijų valdymas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="c95d5-114">Turto perkėlimas</span><span class="sxs-lookup"><span data-stu-id="c95d5-114">Move asset</span></span>

<span data-ttu-id="c95d5-115">Norėdami perkelti turtą į kitą turto struktūrą arba į kitą tos pačios turto struktūros vietą naudokite funkciją **Perkelti turtą**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="c95d5-116">Taip pat galima perkelti turtą iš turto struktūros, kad jis taptų atskiru turtu be jokių struktūros ryšių.</span><span class="sxs-lookup"><span data-stu-id="c95d5-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="c95d5-117">Nenaudokite šios funkcijos, jei turtas atnaujinamas arba laikinai pakeičiamas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="c95d5-118">Vietoje jos naudokite funkciją **Pakeisti turtą**, kuri aprašytas toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="c95d5-119">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas** arba **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c95d5-120">Sąraše pasirinkite perkeliamą turtą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-120">In the list, select the asset to move.</span></span> <span data-ttu-id="c95d5-121">Jei turtas turi antrinį turtą, taip pat perkelsite ir tą turtą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="c95d5-122">Pasirinkite **Perkelti turtą**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="c95d5-123">Norėdami perkelti turtą taip, kad jis taptų turto struktūros dalimi, pasirinkite naują pagrindinį turtą lauke **Pagrindinis turtas**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="c95d5-124">Jei perkeliate antrinį turtą ir norite jį padaryti atskiru turtu, be jokių struktūros ryšių, lauką **Pagrindinis turtas** palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="c95d5-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="c95d5-125">Pagal numatytuosius nustatymus lauke **Galioja** nustatoma dabartinė data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="c95d5-126">Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti turto perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="c95d5-127">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="c95d5-128">Turto pakeitimas</span><span class="sxs-lookup"><span data-stu-id="c95d5-128">Replace asset</span></span>

<span data-ttu-id="c95d5-129">Funkciją **Pakeisti turtą** naudokite norėdami remontuoti, atnaujinti ar visam laikui pakeisti susidėvėjusį turtą nauju turtu.</span><span class="sxs-lookup"><span data-stu-id="c95d5-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="c95d5-130">Ši funkcija naudojama pakeisti antrinį turtą turto struktūroje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="c95d5-131">Pagrindiniam turtui (t. y. turtui, kuris šiuo metu neturi pagrindinio turto) šis pakeitimas atliekamas funkcinėje vietoje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="c95d5-132">Daugiau informacijos apie tai, kaip pakeisti pagrindinį turtą funkcinėje vietoje žr. [Turto diegimas funkcinėse vietose](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="c95d5-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c95d5-133">Jei remonto dirbtuvės susietos su gamybos skyriumi, galima kurti funkcines vietas, pvz. **Remonto dirbtuvės**, **Atliekos** ir **Saugykla**, kad būtų galima tvarkyti turto remontą ir pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="c95d5-134">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas** arba **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c95d5-135">Sąraše pasirinkite antrinį turtą, kurį norite pakeisti.</span><span class="sxs-lookup"><span data-stu-id="c95d5-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="c95d5-136">Jei turtas turi antrinį turtą, taip pat pakeičiamas ir tas turtas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="c95d5-137">Pasirinkite **Pakeisti turtą**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="c95d5-138">Lauke **Struktūros keitimas** rodoma paskutinė data ir laikas, kada pasirinktas turtas ir susijęs antrinis turtas buvo perkeltas į turto struktūrą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="c95d5-139">Lauko **Tikslinė funkcinė vieta** dalyje **Pasirinktas turtas** pasirinkite funkcinę vietą, į kurią norite perkelti turtą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="c95d5-140">Pavyzdžiui, pasirinkite vietą **Remonto dirbtuvės** arba **Atliekos**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="c95d5-141">**Pagrindinis turtas** dalies lauke **Galioja** pateikta paskutinė data ir laikas, kada dabartinėje funkcinėje vietoje buvo įdiegtas arba perkeltas pagrindinis turtas ir susijęs antrinis turtas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="c95d5-142">Dalies **Naujas turtas** lauke **Turtas** pasirinkite turtą, kurį norite įterpti kaip laikiną arba nuolatinį pakeičiamą turtą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="c95d5-143">Šis turtas šiuo metu gali būti kitoje funkcinėje vietoje, pvz. **Saugykla**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="c95d5-144">Pagal numatytuosius nustatymus lauke dalies **Galioja nuo** lauke **Galioja** nustatoma dabartinė data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="c95d5-145">Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti turto pakeitimas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="c95d5-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="c95d5-147">Turto diegimas</span><span class="sxs-lookup"><span data-stu-id="c95d5-147">Install asset</span></span>

<span data-ttu-id="c95d5-148">Naudokite funkciją **Diegti turtą**, kad įdiegtumėte turto struktūrą funkcinėje vietoje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="c95d5-149">Visada pasirinkite pagrindinį turtą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-149">Always select a parent asset.</span></span> <span data-ttu-id="c95d5-150">Pagrindinis turtas ir su juo susijęs antrinis turtas bus perkeltas į pasirinktą funkcinę vietą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="c95d5-151">Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas** arba **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="c95d5-152">Sąraše pasirinkite pagrindinį turtą, kurį norite įdiegti kitoje funkcinėje vietoje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="c95d5-153">Pasirinkite **Diegti turtą**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-153">Select **Install asset**.</span></span>

    <span data-ttu-id="c95d5-154">Dalyje **Atributai** pateikti pagrindiniam turtui nustatyti atributai.</span><span class="sxs-lookup"><span data-stu-id="c95d5-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="c95d5-155">Lauke **Funkcinė vieta** pasirinkite naują vietą.</span><span class="sxs-lookup"><span data-stu-id="c95d5-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="c95d5-156">Pagal numatytuosius nustatymus lauke **Galioja** nustatoma dabartinė data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="c95d5-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="c95d5-157">Tačiau galima pasirinkti kitą datą ir laiką, nuo kurio pradeda galioti diegimas turto struktūroje.</span><span class="sxs-lookup"><span data-stu-id="c95d5-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="c95d5-158">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c95d5-158">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]