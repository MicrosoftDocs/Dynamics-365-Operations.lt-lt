---
title: Kurti RFQ vertinimo būdą
description: Šioje procedūroje parodoma, kaip kurti vertinimo būdą.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbbc941b810cd8e5db5ba15a23dc6bd72a29506
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838075"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="c1f21-103">Kurti RFQ vertinimo būdą</span><span class="sxs-lookup"><span data-stu-id="c1f21-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c1f21-104">Šioje procedūroje parodoma, kaip kurti vertinimo būdą.</span><span class="sxs-lookup"><span data-stu-id="c1f21-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="c1f21-105">Vertinimo būdas yra kriterijų, kuriuos naudojant galima palyginti kainų pasiūlymus, siunčiamus atsakyme į pasiūlymo patvirtinimą (RFQ), rinkinys.</span><span class="sxs-lookup"><span data-stu-id="c1f21-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="c1f21-106">Pavyzdžiui, galbūt norite įvertinti tiekėją, remdamiesi jo ankstesne veika, arba įvertinti, ar įmonė yra draugiška aplinkai, ar gerai bendradarbiauja, arba galbūt norite palyginti kainų pasiūlymus pagal kainą.</span><span class="sxs-lookup"><span data-stu-id="c1f21-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="c1f21-107">Vertinimo būdas gali būti susietas su siūlymo tipu kaip numatytasis to tipo RFQ vertinimo būdas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="c1f21-108">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="c1f21-109">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="c1f21-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="c1f21-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Pasiūlymo patvirtinimas > Vertinimo būdas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="c1f21-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-111">Click New.</span></span>
3. <span data-ttu-id="c1f21-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c1f21-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c1f21-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c1f21-114">Click Save.</span></span>
6. <span data-ttu-id="c1f21-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-115">Click New.</span></span>
7. <span data-ttu-id="c1f21-116">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c1f21-117">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c1f21-118">Šis aprašymas rodomas kartu su vertinimo būdo pavadinimu, kai pasirenkamas RFQ vertinimo būdas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="c1f21-119">Lauke Diapazonas nuo įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f21-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="c1f21-120">Diapazonas riboja, ką įsigijimo specialistas gali įvesti kaip vertinimą.</span><span class="sxs-lookup"><span data-stu-id="c1f21-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="c1f21-121">Kai nustatyti keli RFQ vertinimo kriterijai, įvesti vertinimai yra sudedami ir rodoma suma, kad kainų pasiūlymus būtų galima palyginti.</span><span class="sxs-lookup"><span data-stu-id="c1f21-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="c1f21-122">Lauke Diapazonas iki įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f21-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="c1f21-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c1f21-123">Click New.</span></span>
12. <span data-ttu-id="c1f21-124">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="c1f21-125">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f21-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="c1f21-126">Lauke Diapazonas nuo įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f21-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="c1f21-127">Lauke Diapazonas iki įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f21-127">In the Range to field, enter a number.</span></span>

