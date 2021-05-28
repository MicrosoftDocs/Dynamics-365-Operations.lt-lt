---
title: Gabenimo konteineriai
description: Šioje temoje aprašoma, kaip nustatyti gabenimo konteinerius modulyje Iškrovimo kaina.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8f86f3603b64093214bb7cf7d165ba0fc2229ca3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021545"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="1a251-103">Gabenimo konteinerio nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a251-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a251-104">Šioje temoje aprašoma, kaip nustatyti gabenimo konteinerius modulyje **Iškrovimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="1a251-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="1a251-105">Gabenimo konteinerių tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a251-105">Set up shipping container types</span></span>

<span data-ttu-id="1a251-106">Gabenimo konteinerių tipai apibrėžia gabenimo konteinerių tipus, kuriuos galima naudoti siuntimų ir reisų metu.</span><span class="sxs-lookup"><span data-stu-id="1a251-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="1a251-107">Norėdami dirbti su gabenimo konteinerių tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Gabenimo konteinerių tipai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="1a251-108">Čia galite peržiūrėti, įtraukti ir pašalinti jūsų konteinerių tipų įrašus.</span><span class="sxs-lookup"><span data-stu-id="1a251-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="1a251-109">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="1a251-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a251-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="1a251-110">Field</span></span> | <span data-ttu-id="1a251-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-111">Description</span></span> |
|---|---|
| <span data-ttu-id="1a251-112">Gabenimo konteinerio tipas</span><span class="sxs-lookup"><span data-stu-id="1a251-112">Shipping container type</span></span> | <span data-ttu-id="1a251-113">Įveskite unikalų gabenimo konteinerio tipo identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="1a251-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="1a251-114">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-114">Description</span></span> | <span data-ttu-id="1a251-115">Įveskite gabenimo konteinerio tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="1a251-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="1a251-116">Tūris</span><span class="sxs-lookup"><span data-stu-id="1a251-116">Volume</span></span> | <span data-ttu-id="1a251-117">Įveskite didžiausią tūrį, leidžiamą šio tipo gabenimo konteineriuose.</span><span class="sxs-lookup"><span data-stu-id="1a251-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="1a251-118">Svarba</span><span class="sxs-lookup"><span data-stu-id="1a251-118">Weight</span></span> | <span data-ttu-id="1a251-119">Įveskite didžiausią svorį, leidžiamą šio tipo gabenimo konteineriuose.</span><span class="sxs-lookup"><span data-stu-id="1a251-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="1a251-120">Grąžinama</span><span class="sxs-lookup"><span data-stu-id="1a251-120">Returnable</span></span> | <span data-ttu-id="1a251-121">Nurodykite, ar šio tipo gabenimo konteineriai gali būti grąžinti tiekėjui po to, kai jie buvo naudoti reiso metu.</span><span class="sxs-lookup"><span data-stu-id="1a251-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="1a251-122">Jei ši parinktis nustatyta į *Taip*, gali būti taikomos papildomos išlaidos grąžinant šio tipo gabenimo konteinerius į kilmės uostą.</span><span class="sxs-lookup"><span data-stu-id="1a251-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="1a251-123">Gabenimo konteinerių nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a251-123">Set up shipping containers</span></span>

<span data-ttu-id="1a251-124">Gabenimo konteinerių įrašus galite naudoti kiekvienam konteineriui, kurį naudojate reiso metu, identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="1a251-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="1a251-125">Kai sukuriate reisą, galite pasirinkti konkretų konteinerį visų čia apibrėžtų gabenimo konteinerių įrašų sąraše.</span><span class="sxs-lookup"><span data-stu-id="1a251-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="1a251-126">Ši funkcija ypač naudinga, jei jūsų įmonė turi savo gabenimo konteinerių.</span><span class="sxs-lookup"><span data-stu-id="1a251-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="1a251-127">Jums nereikia įvesti gabenimo konteinerių, kurie bus naudojami tik vieną kartą, numerių.</span><span class="sxs-lookup"><span data-stu-id="1a251-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="1a251-128">Vietoje to galite įtraukti gabenimo konteinerio numerį, kai kuriate reisą.</span><span class="sxs-lookup"><span data-stu-id="1a251-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="1a251-129">Gabenimo konteinerių įrašai naudojami tik modulyje Iškrovimo kaina.</span><span class="sxs-lookup"><span data-stu-id="1a251-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="1a251-130">Jie negalimi standartiniame modulyje **Transportavimo valdymas** (TMS).</span><span class="sxs-lookup"><span data-stu-id="1a251-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="1a251-131">Norėdami dirbti su gabenimo konteineriais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Gabenimo konteineriai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="1a251-132">Čia galite peržiūrėti, įtraukti ir pašalinti jūsų gabenimo konteinerių įrašus.</span><span class="sxs-lookup"><span data-stu-id="1a251-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="1a251-133">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="1a251-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a251-134">Laukas</span><span class="sxs-lookup"><span data-stu-id="1a251-134">Field</span></span> | <span data-ttu-id="1a251-135">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-135">Description</span></span> |
|---|---|
| <span data-ttu-id="1a251-136">Gabenimo konteineris</span><span class="sxs-lookup"><span data-stu-id="1a251-136">Shipping container</span></span> | <span data-ttu-id="1a251-137">Įveskite unikalų gabenimo konteinerio identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="1a251-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="1a251-138">Gabenimo konteinerio tipas</span><span class="sxs-lookup"><span data-stu-id="1a251-138">Shipping container type</span></span> | <span data-ttu-id="1a251-139">Pasirinkite gabenimo konteinerio tipą.</span><span class="sxs-lookup"><span data-stu-id="1a251-139">Select the type of shipping container.</span></span> <span data-ttu-id="1a251-140">Daugiau informacijos žr. ankstesniame šios temos skyriuje [Gabenimo konteinerių tipų nustatymas](#shipping-container-types).</span><span class="sxs-lookup"><span data-stu-id="1a251-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="1a251-141">Gabenimo konteinerio nustatymas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="1a251-141">The shipping container setup is optional.</span></span> <span data-ttu-id="1a251-142">Paprastai jį naudosite tik tuo atveju, jei jūsų įmonė turi savo gabenimo konteinerių arba dažnai pakartotinai naudoja tuos pačius gabenimo konteinerius.</span><span class="sxs-lookup"><span data-stu-id="1a251-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="1a251-143">Nėra skaičiuojami gabenimo konteinerių numerių kontroliniai skaitmenys.</span><span class="sxs-lookup"><span data-stu-id="1a251-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="1a251-144">Vienetų tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a251-144">Set up unit types</span></span>

<span data-ttu-id="1a251-145">Vienetų tipai nustato papildomus gabenimo konteinerių grupavimus ir identifikavimo metodus.</span><span class="sxs-lookup"><span data-stu-id="1a251-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="1a251-146">Vieneto tipas paprastai naudojamas norint identifikuoti konteinerio, kuriame supakuotos prekės, tipą, pvz., padėklai ar statinės.</span><span class="sxs-lookup"><span data-stu-id="1a251-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="1a251-147">Galite pasirinkti vieneto tipą, kai nustatote konteinerį puslapyje **Visi gabenimo konteineriai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="1a251-148">Vienetų tipai naudojami tik modulyje Iškrovimo kaina.</span><span class="sxs-lookup"><span data-stu-id="1a251-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="1a251-149">Jie negalimi TMS.</span><span class="sxs-lookup"><span data-stu-id="1a251-149">They aren't available in TMS.</span></span>

<span data-ttu-id="1a251-150">Norėdami dirbti su vienetų tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Vienetų tipai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="1a251-151">Čia galite peržiūrėti, įtraukti ir pašalinti jūsų vienetų tipų įrašus.</span><span class="sxs-lookup"><span data-stu-id="1a251-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="1a251-152">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="1a251-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a251-153">Laukas</span><span class="sxs-lookup"><span data-stu-id="1a251-153">Field</span></span> | <span data-ttu-id="1a251-154">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-154">Description</span></span> |
|---|---|
| <span data-ttu-id="1a251-155">Vieneto tipas</span><span class="sxs-lookup"><span data-stu-id="1a251-155">Unit type</span></span> | <span data-ttu-id="1a251-156">Įveskite unikalų vieneto tipo identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="1a251-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="1a251-157">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-157">Description</span></span> | <span data-ttu-id="1a251-158">Įveskite vieneto tipo aprašymą.</span><span class="sxs-lookup"><span data-stu-id="1a251-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="1a251-159">Šaldymo tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1a251-159">Set up refrigeration types</span></span>

<span data-ttu-id="1a251-160">Šaldymo tipai nustato papildomus gabenimo konteinerių (paprastai šaldymo konteinerių) grupavimus ir identifikavimo metodus.</span><span class="sxs-lookup"><span data-stu-id="1a251-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="1a251-161">Galite pasirinkti šaldymo tipą, kai nustatote konteinerį puslapyje **Visi gabenimo konteineriai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="1a251-162">Norėdami dirbti su šaldymo tipais, eikite į **Iškrovimo kaina \> Konteinerių nustatymas \> Šaldymo tipai**.</span><span class="sxs-lookup"><span data-stu-id="1a251-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="1a251-163">Čia galite peržiūrėti, įtraukti ir pašalinti jūsų šaldymo tipų įrašus.</span><span class="sxs-lookup"><span data-stu-id="1a251-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="1a251-164">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="1a251-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a251-165">Laukas</span><span class="sxs-lookup"><span data-stu-id="1a251-165">Field</span></span> | <span data-ttu-id="1a251-166">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-166">Description</span></span> |
|---|---|
| <span data-ttu-id="1a251-167">Šaldymo tipas</span><span class="sxs-lookup"><span data-stu-id="1a251-167">Refrigeration type</span></span> | <span data-ttu-id="1a251-168">Įveskite unikalų šaldymo tipo identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="1a251-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="1a251-169">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1a251-169">Description</span></span> | <span data-ttu-id="1a251-170">Įveskite šaldymo tipo aprašymą.</span><span class="sxs-lookup"><span data-stu-id="1a251-170">Enter a description of the refrigeration type.</span></span> |
