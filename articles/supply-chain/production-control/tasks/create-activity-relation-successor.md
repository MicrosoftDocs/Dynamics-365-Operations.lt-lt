---
title: Veiklos ryšio kūrimas – vėlesnė veikla
description: „Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 261bb1b99045cc78f0e74e1ed2ad7fa133d8ebe6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212347"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="b04b8-103">Veiklos ryšio kūrimas – vėlesnė veikla</span><span class="sxs-lookup"><span data-stu-id="b04b8-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b04b8-104">„Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais.</span><span class="sxs-lookup"><span data-stu-id="b04b8-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="b04b8-105">Šiame įraše nurodoma, kaip sukurti veiklos ryšį.</span><span class="sxs-lookup"><span data-stu-id="b04b8-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="b04b8-106">Išankstiniai reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="b04b8-106">Prerequisites:</span></span>

- <span data-ttu-id="b04b8-107">Gamybos eiga ir versija juodraščio režimu.</span><span class="sxs-lookup"><span data-stu-id="b04b8-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="b04b8-108">Dvi gamybos eigoje viena po kitos sekančios veiklos yra sukuriamos, bet nesusiejamos.</span><span class="sxs-lookup"><span data-stu-id="b04b8-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="b04b8-109">Kaip rasti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="b04b8-109">Find the production flow version</span></span> 
1. <span data-ttu-id="b04b8-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="b04b8-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b04b8-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b04b8-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b04b8-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b04b8-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b04b8-113">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b04b8-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b04b8-114">Sąraše pasirinkite juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="b04b8-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="b04b8-115">Veiklos ryšius galima įtraukti į gamybos eigos juodraščio arba aktyvias versijas.</span><span class="sxs-lookup"><span data-stu-id="b04b8-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="b04b8-116">Kaip atidaryti veiklos apžvalgą</span><span class="sxs-lookup"><span data-stu-id="b04b8-116">Open the activity overview</span></span>
1. <span data-ttu-id="b04b8-117">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="b04b8-117">Click Activities.</span></span>
    * <span data-ttu-id="b04b8-118">Atkreipkite dėmesį, kad formoje rodomos visos gamybos eigų, su kuriomis dirbate, versijai priskirtos gamybos eigos veiklos.</span><span class="sxs-lookup"><span data-stu-id="b04b8-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="b04b8-119">Kaip įtraukti vėlesnę veiklą</span><span class="sxs-lookup"><span data-stu-id="b04b8-119">Add a Successor</span></span>
1. <span data-ttu-id="b04b8-120">Spustelėkite Įtraukti vėlesnę veiklą.</span><span class="sxs-lookup"><span data-stu-id="b04b8-120">Click Add successor.</span></span>
2. <span data-ttu-id="b04b8-121">Lauke Veikla spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b04b8-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b04b8-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b04b8-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b04b8-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b04b8-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b04b8-124">Pažymėkite žymės langelį Apribojimas.</span><span class="sxs-lookup"><span data-stu-id="b04b8-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="b04b8-125">Lauke Apribojimo vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b04b8-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="b04b8-126">Apribojimo laikas yra laikas nuo suplanuotos ankstesnės veiklos pabaigos (termino data ir laikas) iki suplanuotos vėlesnės veiklos pradžios.</span><span class="sxs-lookup"><span data-stu-id="b04b8-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="b04b8-127">Lauke Vienetai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b04b8-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="b04b8-128">Lauke Ciklo laiko koeficientas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b04b8-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="b04b8-129">Jei tuo pačiu metu vykdomos abi veiklos, ciklo laiko koeficientas turi būti 1.</span><span class="sxs-lookup"><span data-stu-id="b04b8-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="b04b8-130">Jei ankstesnė veikla paleidžiama dvigubai greičiau už vėlesnę veiklą, koeficiantas turi būti 2.</span><span class="sxs-lookup"><span data-stu-id="b04b8-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="b04b8-131">Ciklo laiko santykiai naudojami, norint apskaičiuoti gamybos eigos veiklos ciklo laikus</span><span class="sxs-lookup"><span data-stu-id="b04b8-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="b04b8-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b04b8-132">Click OK.</span></span>
10. <span data-ttu-id="b04b8-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b04b8-133">Close the page.</span></span>
11. <span data-ttu-id="b04b8-134">Spustelėkite skirtuką GridPanel.</span><span class="sxs-lookup"><span data-stu-id="b04b8-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="b04b8-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b04b8-135">Close the page.</span></span>
13. <span data-ttu-id="b04b8-136">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b04b8-136">Refresh the page.</span></span>

