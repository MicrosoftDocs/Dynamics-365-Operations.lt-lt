---
title: Siuntimo informacijos sąranka
description: Šioje temoje aprašoma, kaip nustatyti siuntimo informaciją modulyje Iškrovimo kaina.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833694"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="63add-103">Siuntimo informacijos sąranka</span><span class="sxs-lookup"><span data-stu-id="63add-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63add-104">Šioje temoje aprašoma, kaip nustatyti siuntimo informaciją modulyje **Iškrovimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="63add-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="63add-105">Prekių aprašas</span><span class="sxs-lookup"><span data-stu-id="63add-105">Description of goods</span></span>

<span data-ttu-id="63add-106">Prekių aprašymai padeda identifikuoti reisą, gabenimo konteinerį arba prekių sąskaitos lapą ir jame aprašytas prekes.</span><span class="sxs-lookup"><span data-stu-id="63add-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="63add-107">Galite pasirinkti prekių aprašymą gabenimo konteinerio antraštėje arba sąskaitos lapo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="63add-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="63add-108">Norėdami dirbti su prekių aprašymais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Prekių aprašymas**.</span><span class="sxs-lookup"><span data-stu-id="63add-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="63add-109">Ten galite peržiūrėti, atidaryti, kurti ir naikinti prekių aprašymo įrašus.</span><span class="sxs-lookup"><span data-stu-id="63add-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="63add-110">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="63add-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="63add-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="63add-111">Field</span></span> | <span data-ttu-id="63add-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-112">Description</span></span> |
|---|---|
| <span data-ttu-id="63add-113">Prekių aprašas</span><span class="sxs-lookup"><span data-stu-id="63add-113">Description of goods</span></span> | <span data-ttu-id="63add-114">Įvesti unikalų prekių, kurioms bus naudojamas šis aprašymas, tipo identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="63add-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="63add-115">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-115">Description</span></span> | <span data-ttu-id="63add-116">Įveskite šios kategorijos prekių tipo aprašymą.</span><span class="sxs-lookup"><span data-stu-id="63add-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="63add-117">Transporto priemonės</span><span class="sxs-lookup"><span data-stu-id="63add-117">Vessels</span></span>

<span data-ttu-id="63add-118">Transporto priemonė yra unikalus transporto priemonės, kurią naudoja siuntimo įmonė ar agentūra, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="63add-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="63add-119">Kurdami reisą, visada turite pasirinkti arba įvesti jo transporto priemonės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="63add-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="63add-120">Jei dažnai naudojate tas pačias transporto priemones, galite greičiau ir paprasčiau sukurti naują reisą, sukurdami kiekvienos transporto priemonės įrašą ir taip leisdami vartotojams pasirinkti iš sąrašo, o ne kaskart rankiniu būdu įvesti pavadinimą arba numerį.</span><span class="sxs-lookup"><span data-stu-id="63add-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="63add-121">Norėdami dirbti su transporto priemonėmis, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Transporto priemonės**.</span><span class="sxs-lookup"><span data-stu-id="63add-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="63add-122">Ten galite peržiūrėti, atidaryti, kurti ir naikinti transporto priemonių įrašus.</span><span class="sxs-lookup"><span data-stu-id="63add-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="63add-123">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="63add-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="63add-124">Laukas</span><span class="sxs-lookup"><span data-stu-id="63add-124">Field</span></span> | <span data-ttu-id="63add-125">aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-125">Description</span></span> |
|---|---|
| <span data-ttu-id="63add-126">Transporto priemonė</span><span class="sxs-lookup"><span data-stu-id="63add-126">Vessel</span></span> | <span data-ttu-id="63add-127">Įvesti unikalų laivo, kuris bus naudojamas prekėms gabenti reiso metu, identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="63add-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="63add-128">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-128">Description</span></span> | <span data-ttu-id="63add-129">Įveskite transporto priemonės aprašą.</span><span class="sxs-lookup"><span data-stu-id="63add-129">Enter a description of the vessel.</span></span> <span data-ttu-id="63add-130">Paprastai šiame aprašyme nurodomas laivo pavadinimas ir siuntimo įmonė / agentūra.</span><span class="sxs-lookup"><span data-stu-id="63add-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="63add-131">Pristatymo būdas</span><span class="sxs-lookup"><span data-stu-id="63add-131">Mode of delivery</span></span> | <span data-ttu-id="63add-132">Pasirinkite transporto priemonės naudojamą pristatymo būdą (pvz., _Oru_, _Vandeniu_, or _Traukiniu_).</span><span class="sxs-lookup"><span data-stu-id="63add-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="63add-133">Eksportuotojai</span><span class="sxs-lookup"><span data-stu-id="63add-133">Exporters</span></span>

<span data-ttu-id="63add-134">Kiekvienas eksportuotojo įrašas identifikuoja tiekėją arba eksportuotoją, kurį galima nurodyti kaip reiso tiekėją.</span><span class="sxs-lookup"><span data-stu-id="63add-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="63add-135">Eksportuotojas gali būti susietas su reisu ir naudojamas ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="63add-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="63add-136">Norėdami dirbti su eksportuotojais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Eksportuotojai**.</span><span class="sxs-lookup"><span data-stu-id="63add-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="63add-137">Ten galite peržiūrėti, atidaryti, kurti ir naikinti eksportuotojų įrašus.</span><span class="sxs-lookup"><span data-stu-id="63add-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="63add-138">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="63add-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="63add-139">Laukas</span><span class="sxs-lookup"><span data-stu-id="63add-139">Field</span></span> | <span data-ttu-id="63add-140">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-140">Description</span></span> |
|---|---|
| <span data-ttu-id="63add-141">Eksportuotojas</span><span class="sxs-lookup"><span data-stu-id="63add-141">Exporter</span></span> | <span data-ttu-id="63add-142">Įvesti unikalų reiso metu gabenamų prekių eksportuotojo identifikavimo pavadinimą / numerį.</span><span class="sxs-lookup"><span data-stu-id="63add-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="63add-143">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-143">Description</span></span> | <span data-ttu-id="63add-144">Įveskite eksportuotojo aprašą.</span><span class="sxs-lookup"><span data-stu-id="63add-144">Enter a description of the exporter.</span></span> <span data-ttu-id="63add-145">Paprastai šiame aprašyme nurodomas pilnas siuntimo įmonės / agentūros pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="63add-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="63add-146">Prekių kodai</span><span class="sxs-lookup"><span data-stu-id="63add-146">Commodity codes</span></span>

<span data-ttu-id="63add-147">Prekių kodus naudojate norėdami padėti atlikti muitinės identifikavimą ir apskaičiuoti reiso prekių muito mokesčio tarifus.</span><span class="sxs-lookup"><span data-stu-id="63add-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="63add-148">Prekių kodus galite pasirinkti puslapyje **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="63add-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="63add-149">Norėdami dirbti su prekių kodais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Prekių kodai**.</span><span class="sxs-lookup"><span data-stu-id="63add-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="63add-150">Ten galite peržiūrėti, atidaryti, kurti ir naikinti prekių kodų įrašus.</span><span class="sxs-lookup"><span data-stu-id="63add-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="63add-151">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="63add-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="63add-152">Laukas</span><span class="sxs-lookup"><span data-stu-id="63add-152">Field</span></span> | <span data-ttu-id="63add-153">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-153">Description</span></span> |
|---|---|
| <span data-ttu-id="63add-154">Prekės kodas</span><span class="sxs-lookup"><span data-stu-id="63add-154">Commodity code</span></span> | <span data-ttu-id="63add-155">Įvesti unikalų šio prekės tipo kodą.</span><span class="sxs-lookup"><span data-stu-id="63add-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="63add-156">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-156">Description</span></span> | <span data-ttu-id="63add-157">Įveskite prekės tipo aprašymą.</span><span class="sxs-lookup"><span data-stu-id="63add-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="63add-158">Muitinės aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-158">Customs description</span></span>

<span data-ttu-id="63add-159">Muitinės aprašymai padeda identifikuoti prekes muitinės tikslais.</span><span class="sxs-lookup"><span data-stu-id="63add-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="63add-160">Muitinės aprašymą galite pasirinkti puslapyje **Išleisti produktai** arba pirkimo užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="63add-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="63add-161">Norėdami dirbti su muitinės aprašymais, eikite į **Iškrovimo kaina \> Siuntimo informacijos nustatymas \> Muitinės aprašymas**.</span><span class="sxs-lookup"><span data-stu-id="63add-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="63add-162">Ten galite peržiūrėti, atidaryti, kurti ir naikinti muitinės aprašymo įrašus.</span><span class="sxs-lookup"><span data-stu-id="63add-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="63add-163">Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.</span><span class="sxs-lookup"><span data-stu-id="63add-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="63add-164">Laukas</span><span class="sxs-lookup"><span data-stu-id="63add-164">Field</span></span> | <span data-ttu-id="63add-165">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-165">Description</span></span> |
|---|---|
| <span data-ttu-id="63add-166">Muitinės aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-166">Customs description</span></span> | <span data-ttu-id="63add-167">Įvesti unikalų šio muitinės klasifikavimo tipo kodą.</span><span class="sxs-lookup"><span data-stu-id="63add-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="63add-168">Dažnai šis kodas yra oficialus aprašymas, kurį pateikia muitinė, skirtas prekių aprašymui ir kokybinei vertei nustatyti.</span><span class="sxs-lookup"><span data-stu-id="63add-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="63add-169">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="63add-169">Description</span></span> | <span data-ttu-id="63add-170">Įveskite muitinės klasifikavimo aprašą.</span><span class="sxs-lookup"><span data-stu-id="63add-170">Enter a description of the customs classification.</span></span> |
