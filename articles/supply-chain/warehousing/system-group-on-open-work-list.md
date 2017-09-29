---
title: "Sistemos grupavimas atidarytame darbų sąraše"
description: "Šioje temoje aprašoma, kaip mobiliajame įrenginyje filtruoti atidarytą darbų sąrašą."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="b7a21-103">Sistemos grupavimas atidarytame darbų sąraše</span><span class="sxs-lookup"><span data-stu-id="b7a21-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7a21-104">Naudodami sistemos grupavimo lauką, atidarytą darbų sąrašą galite filtruoti neredaguodami mobiliojo įrenginio meniu elemento.</span><span class="sxs-lookup"><span data-stu-id="b7a21-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="b7a21-105">Kai sistemos grupavimo funkcija taikytina, ją naudojant darbų sąrašą galima filtruoti viename darbo antraštės lauke.</span><span class="sxs-lookup"><span data-stu-id="b7a21-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="b7a21-106">Sistemos grupavimo funkcijos negalite naudoti filtruodami eilutės lygio laukuose.</span><span class="sxs-lookup"><span data-stu-id="b7a21-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="b7a21-107">Sistemos grupavimo funkcijos nustatymas atidarytame darbų sąraše</span><span class="sxs-lookup"><span data-stu-id="b7a21-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="b7a21-108">Norėdami sistemos grupavimo funkciją nustatyti atidarytame darbų sąraše, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7a21-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="b7a21-109">Mobiliojo įrenginio meniu elemente pasirinkite **Režimas: Netiesioginis** ir **Veiklos kodas: Rodyti atidarytą darbų sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="b7a21-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="b7a21-110">Tada galima rinktis iš tolesnių parinkčių.</span><span class="sxs-lookup"><span data-stu-id="b7a21-110">The following options become available.</span></span> <span data-ttu-id="b7a21-111">Norint sistemos grupavimo funkciją naudoti atidarytame darbų sąraše, šios parinktys yra būtinos.</span><span class="sxs-lookup"><span data-stu-id="b7a21-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="b7a21-112">Parinktis</span><span class="sxs-lookup"><span data-stu-id="b7a21-112">Option</span></span>        | <span data-ttu-id="b7a21-113">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b7a21-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="b7a21-114">Leisti naudoti sistemos grupavimo funkciją</span><span class="sxs-lookup"><span data-stu-id="b7a21-114">Allow system grouping</span></span>   | <span data-ttu-id="b7a21-115">Sistemos grupavimo funkciją galima naudoti su pasirinktu darbų sąrašo meniu elementu.</span><span class="sxs-lookup"><span data-stu-id="b7a21-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="b7a21-116">Sistemos grupavimo laukas</span><span class="sxs-lookup"><span data-stu-id="b7a21-116">System grouping field</span></span>   | <span data-ttu-id="b7a21-117">Galima naudoti tik jei **Leisti sistemos darbą** nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b7a21-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="b7a21-118">Pasirinkite lauką, nustatantį, kaip bus grupuojamas darbuotojų paėmimo darbas.</span><span class="sxs-lookup"><span data-stu-id="b7a21-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="b7a21-119">Pavyzdžiui, jei pasirinksite lauką **ShipmentId**, norėdamas grupuoti išrinkimo darbus, darbuotojas nuskaitys siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="b7a21-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="b7a21-120">Tada visi siuntos darbai priskiriami darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="b7a21-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="b7a21-121">Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus.</span><span class="sxs-lookup"><span data-stu-id="b7a21-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="b7a21-122">Naudokite lauką **Sistemos grupavimo žyma**, kad darbuotoją informuotumėte, ką reikia nuskaityti.</span><span class="sxs-lookup"><span data-stu-id="b7a21-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="b7a21-123">Sistemos grupavimo žyma</span><span class="sxs-lookup"><span data-stu-id="b7a21-123">System grouping label</span></span>   | <span data-ttu-id="b7a21-124">Galima naudoti tik jei **Leisti sistemos darbą** nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b7a21-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="b7a21-125">Įveskite informaciją darbuotojui apie tai, ką reikia nuskaityti, kai paėmimo darbas yra sugrupuotas.</span><span class="sxs-lookup"><span data-stu-id="b7a21-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="b7a21-126">Pavyzdžiui, jei naudojate lauką **ShipmentId** norėdami grupuoti paėmimo darbą pagal siuntą, lauke galite įvesti Siuntos ID.</span><span class="sxs-lookup"><span data-stu-id="b7a21-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="b7a21-127">Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus.</span><span class="sxs-lookup"><span data-stu-id="b7a21-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="b7a21-128">Be to, lauke **Sistemos grupavimas** reikia pasirinkti lauką, pagal kurį grupuosite.</span><span class="sxs-lookup"><span data-stu-id="b7a21-128">You must also select the field to group by in the **System grouping** field.</span></span>|

