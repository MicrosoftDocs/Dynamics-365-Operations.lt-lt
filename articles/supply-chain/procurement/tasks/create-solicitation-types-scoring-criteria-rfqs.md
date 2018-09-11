--- 
title: "Kurti RFQ siūlymo tipus ir vertinimo kriterijus"
description: "Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 5d2b0d1e998149a5045c655d74591c56bff81246
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="04a1f-103">Kurti RFQ siūlymo tipus ir vertinimo kriterijus</span><span class="sxs-lookup"><span data-stu-id="04a1f-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04a1f-104">Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu.</span><span class="sxs-lookup"><span data-stu-id="04a1f-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="04a1f-105">Jame taip pat parodoma, kaip siūlymo tipą naudoti pasiūlymo patvirtinime (RFQ), kuris tada nustato numatytąjį vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="04a1f-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="04a1f-106">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="04a1f-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="04a1f-107">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="04a1f-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="04a1f-108">Prieš pradėdami, turite galėti naudoti vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="04a1f-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="04a1f-109">Siūlymo tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="04a1f-109">Create a solicitation type</span></span>
1. <span data-ttu-id="04a1f-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Pasiūlymo patvirtinimas > Siūlymo tipas.</span><span class="sxs-lookup"><span data-stu-id="04a1f-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="04a1f-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04a1f-111">Click New.</span></span>
3. <span data-ttu-id="04a1f-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04a1f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="04a1f-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04a1f-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="04a1f-114">Lauke Vertinimo būdas pasirinkite vertinimo būdą, kurį norite taikyti šiam siūlymo tipui.</span><span class="sxs-lookup"><span data-stu-id="04a1f-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="04a1f-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04a1f-115">Click Save.</span></span>
7. <span data-ttu-id="04a1f-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="04a1f-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="04a1f-117">Naudoti siūlymo tipą</span><span class="sxs-lookup"><span data-stu-id="04a1f-117">Use the solicitation type</span></span>
1. <span data-ttu-id="04a1f-118">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="04a1f-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="04a1f-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04a1f-119">Click New.</span></span>
3. <span data-ttu-id="04a1f-120">Lauke Siūlymo tipas pasirinkite siūlymo tipą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="04a1f-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="04a1f-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="04a1f-121">Click OK.</span></span>
5. <span data-ttu-id="04a1f-122">Spustelėkite Vertinimo kriterijai.</span><span class="sxs-lookup"><span data-stu-id="04a1f-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="04a1f-123">Rodomi vertinimo kriterijai yra nuskaityti iš vertinimo būdo, kurį susiejote su siūlymo tipu.</span><span class="sxs-lookup"><span data-stu-id="04a1f-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="04a1f-124">Šiame puslapyje galite įtraukti arba panaikinti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="04a1f-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="04a1f-125">Taip pat galite įtraukti naujų kriterijų kopijuodami juos iš kitų vertinimo būdų.</span><span class="sxs-lookup"><span data-stu-id="04a1f-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="04a1f-126">Spustelėkite Kopijuoti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="04a1f-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="04a1f-127">Lauke Vertinimo būdas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04a1f-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="04a1f-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="04a1f-128">Click OK.</span></span>
9. <span data-ttu-id="04a1f-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="04a1f-129">Close the page.</span></span>


