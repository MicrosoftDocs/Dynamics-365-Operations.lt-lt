---
title: Kurti RFQ siūlymo tipus ir vertinimo kriterijus
description: Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d28cb4bf20ba50aae6b85e835339e2df711c99d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812067"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="6b93d-103">Kurti RFQ siūlymo tipus ir vertinimo kriterijus</span><span class="sxs-lookup"><span data-stu-id="6b93d-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b93d-104">Šiame vedlyje parodoma, kaip kurti siūlymo tipą ir susieti jį su vertinimo būdu.</span><span class="sxs-lookup"><span data-stu-id="6b93d-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="6b93d-105">Jame taip pat parodoma, kaip siūlymo tipą naudoti pasiūlymo patvirtinime (RFQ), kuris tada nustato numatytąjį vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="6b93d-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="6b93d-106">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="6b93d-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="6b93d-107">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="6b93d-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6b93d-108">Prieš pradėdami, turite galėti naudoti vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="6b93d-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="6b93d-109">Siūlymo tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="6b93d-109">Create a solicitation type</span></span>
1. <span data-ttu-id="6b93d-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Pasiūlymo patvirtinimas > Siūlymo tipas.</span><span class="sxs-lookup"><span data-stu-id="6b93d-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="6b93d-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6b93d-111">Click New.</span></span>
3. <span data-ttu-id="6b93d-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b93d-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6b93d-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b93d-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6b93d-114">Lauke Vertinimo būdas pasirinkite vertinimo būdą, kurį norite taikyti šiam siūlymo tipui.</span><span class="sxs-lookup"><span data-stu-id="6b93d-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="6b93d-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6b93d-115">Click Save.</span></span>
7. <span data-ttu-id="6b93d-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6b93d-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="6b93d-117">Naudoti siūlymo tipą</span><span class="sxs-lookup"><span data-stu-id="6b93d-117">Use the solicitation type</span></span>
1. <span data-ttu-id="6b93d-118">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="6b93d-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="6b93d-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6b93d-119">Click New.</span></span>
3. <span data-ttu-id="6b93d-120">Lauke Siūlymo tipas pasirinkite siūlymo tipą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="6b93d-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
    *   
4. <span data-ttu-id="6b93d-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6b93d-121">Click OK.</span></span>
5. <span data-ttu-id="6b93d-122">Spustelėkite Vertinimo kriterijai.</span><span class="sxs-lookup"><span data-stu-id="6b93d-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="6b93d-123">Rodomi vertinimo kriterijai yra nuskaityti iš vertinimo būdo, kurį susiejote su siūlymo tipu.</span><span class="sxs-lookup"><span data-stu-id="6b93d-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="6b93d-124">Šiame puslapyje galite įtraukti arba panaikinti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="6b93d-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="6b93d-125">Taip pat galite įtraukti naujų kriterijų kopijuodami juos iš kitų vertinimo būdų.</span><span class="sxs-lookup"><span data-stu-id="6b93d-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="6b93d-126">Spustelėkite Kopijuoti kriterijus.</span><span class="sxs-lookup"><span data-stu-id="6b93d-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="6b93d-127">Lauke Vertinimo būdas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6b93d-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="6b93d-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6b93d-128">Click OK.</span></span>
9. <span data-ttu-id="6b93d-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6b93d-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]