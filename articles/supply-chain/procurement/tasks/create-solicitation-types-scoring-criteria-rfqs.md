---
title: Kurti RFQ siūlymo tipus ir vertinimo kriterijus
description: Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57abbab21a20278d77001a39e226af11994230be
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149644"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="295dc-103">Kurti RFQ siūlymo tipus ir vertinimo kriterijus</span><span class="sxs-lookup"><span data-stu-id="295dc-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="295dc-104">Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu.</span><span class="sxs-lookup"><span data-stu-id="295dc-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="295dc-105">Jame taip pat parodoma, kaip siūlymo tipą naudoti pasiūlymo patvirtinime (RFQ), kuris tada nustato numatytąjį vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="295dc-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="295dc-106">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="295dc-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="295dc-107">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="295dc-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="295dc-108">Prieš pradėdami, turite galėti naudoti vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="295dc-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="295dc-109">Siūlymo tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="295dc-109">Create a solicitation type</span></span>
1. <span data-ttu-id="295dc-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Pasiūlymo patvirtinimas > Siūlymo tipas.</span><span class="sxs-lookup"><span data-stu-id="295dc-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="295dc-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="295dc-111">Click New.</span></span>
3. <span data-ttu-id="295dc-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="295dc-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="295dc-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="295dc-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="295dc-114">Lauke Vertinimo būdas pasirinkite vertinimo būdą, kurį norite taikyti šiam siūlymo tipui.</span><span class="sxs-lookup"><span data-stu-id="295dc-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="295dc-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="295dc-115">Click Save.</span></span>
7. <span data-ttu-id="295dc-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="295dc-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="295dc-117">Naudoti siūlymo tipą</span><span class="sxs-lookup"><span data-stu-id="295dc-117">Use the solicitation type</span></span>
1. <span data-ttu-id="295dc-118">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="295dc-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="295dc-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="295dc-119">Click New.</span></span>
3. <span data-ttu-id="295dc-120">Lauke Siūlymo tipas pasirinkite siūlymo tipą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="295dc-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="295dc-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="295dc-121">Click OK.</span></span>
5. <span data-ttu-id="295dc-122">Spustelėkite Vertinimo kriterijai.</span><span class="sxs-lookup"><span data-stu-id="295dc-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="295dc-123">Rodomi vertinimo kriterijai yra nuskaityti iš vertinimo būdo, kurį susiejote su siūlymo tipu.</span><span class="sxs-lookup"><span data-stu-id="295dc-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="295dc-124">Šiame puslapyje galite įtraukti arba panaikinti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="295dc-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="295dc-125">Taip pat galite įtraukti naujų kriterijų kopijuodami juos iš kitų vertinimo būdų.</span><span class="sxs-lookup"><span data-stu-id="295dc-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="295dc-126">Spustelėkite Kopijuoti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="295dc-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="295dc-127">Lauke Vertinimo būdas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="295dc-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="295dc-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="295dc-128">Click OK.</span></span>
9. <span data-ttu-id="295dc-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="295dc-129">Close the page.</span></span>

