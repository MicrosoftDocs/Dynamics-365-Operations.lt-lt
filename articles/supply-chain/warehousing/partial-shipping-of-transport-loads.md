---
title: Dalinis transportuojamo krovinio siuntimas
description: Šioje temoje paaiškinama, kaip galima siųsti krovinio dalį ir atidėti krovinio pajėgumo planavimą.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c172f1b66e56f60e89f56ea98910f8d0e4f3e36
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545272"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="8bdb9-103">Dalinis transportuojamo krovinio siuntimas</span><span class="sxs-lookup"><span data-stu-id="8bdb9-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8bdb9-104">Nustatę dalinį krovinių siuntimą, galite tvarkyti krovinius, kai pajėgumo negalima nustatyti, kol visos pardavimo eilutės nėra įtrauktos į krovinį.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="8bdb9-105">Tokiu atveju procesą galima baigti, kai žinomas tikslus padėklų skaičius.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="8bdb9-106">Todėl jūs neturite nuspręsti, kurie padėklai bus priskirti tam tikriems kroviniams iki to momento, kai krovinys bus faktiškai iškrautas iš etapais suskirstytų atsargų.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="8bdb9-107">Ši funkcija suteikia alternatyvą griežtesnei struktūrai, kurią naudojant turite nustatyti, kurie padėklai bus priskirti tam tikriems kroviniams, prieš sukuriant išrinkimo arba krovimo darbą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="8bdb9-108">Naudojant šią funkciją vartotojai gali konfigūruoti atskirus krovinių dalinio siuntimo patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="8bdb9-109">Tada gali būti vykdomi tų krovinių krovimo procesai.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="8bdb9-110">Todėl transportavimo planavimo padalinys gali planuoti krovinius neturėdamas atsižvelgti į atskirų krovinių pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="8bdb9-111">Pakrovimo metu darbuotojai gali nurodyti naują transportuojamą krovinį, į kurį galima pakrauti padėklą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="8bdb9-112">Taip pat jie gali nurodyti esamą transportuojamą krovinį.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="8bdb9-113">Šie duomenys gali būti įrašomi naudojant mobilųjį įrenginį.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="8bdb9-114">Todėl keli sandėlio darbuotojai gali įkelti atsargų iš tų pačių krovinių ar iš kitų krovinių į tą patį sunkvežimį.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="8bdb9-115">Tada krovinius galima visiškai arba iš dalies išsiųsti.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="8bdb9-116">Norint įkelti atsargas iš krovinio į konkrečią transporto priemonę ir iš dalies išsiųsti krovinį, reikia sugeneruoti darbą naudojant darbo šablono pakrovimo klasę.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="8bdb9-117">Įprastas paėmimo darbas, kurio tipas **Paėmimas**, negali būti įkeltas į transporto priemonę, pvz., sunkvežimį.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="8bdb9-118">Transportuojamų krovinių dalinio siuntimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="8bdb9-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="8bdb9-119">Transportuojamų krovinių dalinio siuntimo nustatymą sudaro dvi toliau nurodytos procedūros.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="8bdb9-120">Krovimo strategijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="8bdb9-120">Set the loading strategy</span></span>

<span data-ttu-id="8bdb9-121">Turite įjungti dalinį krovimą nustatydami krovimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="8bdb9-122">Sukūrę krovinį galite nustatyti krovimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="8bdb9-123">Pasirinkite **Sandėlio valdymas** \> **Kroviniai** \> **Visi kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="8bdb9-124">Pasirinkite krovinį, tada spustelėkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="8bdb9-125">Lauke **Krovimo strategija** pasirinkite **Leidžiamas dalinis krovinių siuntimas**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="8bdb9-126">Transporto priemonės krovimo meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="8bdb9-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="8bdb9-127">Turite sukurti naują meniu elementą, kad būtų galima pakrauti transporto priemones.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="8bdb9-128">Transporto priemonė suteikia galimybę grupuoti darbo eilutes iš vieno krovinio arba kelių krovinių.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="8bdb9-129">Visas į transporto priemonę pakrautas krovinys gali būti išsiųstas naudojant mobilųjį skaitytuvą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="8bdb9-130">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="8bdb9-131">Pasirinkite **Naujas**, tada lauke **Būdas** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="8bdb9-132">Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="8bdb9-133">Skirtuko **Bendra** lauke **Nukreipė** pasirinkite **Transportuojamų krovinių krovimas**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="8bdb9-134">Norėdami įjungti siuntos patvirtinimą mobiliajame skaitytuve, lauke **Leidžiamas siuntų patvirtinimo tipas** pasirinkite **Transportuojamas krovinys**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="8bdb9-135">Transportuojamo krovinio siuntimo patvirtinimas iš kliento</span><span class="sxs-lookup"><span data-stu-id="8bdb9-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="8bdb9-136">Šis sąranka suteikia galimybę patvirtinti transportuojamą krovinio, kuris apima visą krovinį arba iš dalies pakrautą krovinį, siuntimą.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="8bdb9-137">Pasirinkite **Sandėlio valdymas** \> **Kroviniai** \> **Transportuojami kroviniai**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="8bdb9-138">Veiksmų srities skirtuko **Siuntimas ir gavimas** grupėje **Patvirtinimas** spustelėkite **Transportas**.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
