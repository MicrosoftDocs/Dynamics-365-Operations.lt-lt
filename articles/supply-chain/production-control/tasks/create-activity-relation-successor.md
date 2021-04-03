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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f10ecb8e579975327440ede6ea383226645c8cf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255306"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="3fe36-103">Veiklos ryšio kūrimas – vėlesnė veikla</span><span class="sxs-lookup"><span data-stu-id="3fe36-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fe36-104">„Lean“ gamybos eigos veiklų srautas dokumentuojamas naudojantis veiklų ryšiais.</span><span class="sxs-lookup"><span data-stu-id="3fe36-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="3fe36-105">Šiame įraše nurodoma, kaip sukurti veiklos ryšį.</span><span class="sxs-lookup"><span data-stu-id="3fe36-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="3fe36-106">Išankstiniai reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="3fe36-106">Prerequisites:</span></span>

- <span data-ttu-id="3fe36-107">Gamybos eiga ir versija juodraščio režimu.</span><span class="sxs-lookup"><span data-stu-id="3fe36-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="3fe36-108">Dvi gamybos eigoje viena po kitos sekančios veiklos yra sukuriamos, bet nesusiejamos.</span><span class="sxs-lookup"><span data-stu-id="3fe36-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="3fe36-109">Kaip rasti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="3fe36-109">Find the production flow version</span></span> 
1. <span data-ttu-id="3fe36-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="3fe36-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="3fe36-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3fe36-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3fe36-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3fe36-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3fe36-113">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="3fe36-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="3fe36-114">Sąraše pasirinkite juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="3fe36-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="3fe36-115">Veiklos ryšius galima įtraukti į gamybos eigos juodraščio arba aktyvias versijas.</span><span class="sxs-lookup"><span data-stu-id="3fe36-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="3fe36-116">Kaip atidaryti veiklos apžvalgą</span><span class="sxs-lookup"><span data-stu-id="3fe36-116">Open the activity overview</span></span>
1. <span data-ttu-id="3fe36-117">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="3fe36-117">Click Activities.</span></span>
    * <span data-ttu-id="3fe36-118">Atkreipkite dėmesį, kad formoje rodomos visos gamybos eigų, su kuriomis dirbate, versijai priskirtos gamybos eigos veiklos.</span><span class="sxs-lookup"><span data-stu-id="3fe36-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="3fe36-119">Kaip įtraukti vėlesnę veiklą</span><span class="sxs-lookup"><span data-stu-id="3fe36-119">Add a Successor</span></span>
1. <span data-ttu-id="3fe36-120">Spustelėkite Įtraukti vėlesnę veiklą.</span><span class="sxs-lookup"><span data-stu-id="3fe36-120">Click Add successor.</span></span>
2. <span data-ttu-id="3fe36-121">Lauke Veikla spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3fe36-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3fe36-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="3fe36-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3fe36-123">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3fe36-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3fe36-124">Pažymėkite žymės langelį Apribojimas.</span><span class="sxs-lookup"><span data-stu-id="3fe36-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="3fe36-125">Lauke Apribojimo vertė įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3fe36-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="3fe36-126">Apribojimo laikas yra laikas nuo suplanuotos ankstesnės veiklos pabaigos (termino data ir laikas) iki suplanuotos vėlesnės veiklos pradžios.</span><span class="sxs-lookup"><span data-stu-id="3fe36-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="3fe36-127">Lauke Vienetai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3fe36-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="3fe36-128">Lauke Ciklo laiko koeficientas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="3fe36-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="3fe36-129">Jei tuo pačiu metu vykdomos abi veiklos, ciklo laiko koeficientas turi būti 1.</span><span class="sxs-lookup"><span data-stu-id="3fe36-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="3fe36-130">Jei ankstesnė veikla paleidžiama dvigubai greičiau už vėlesnę veiklą, koeficiantas turi būti 2.</span><span class="sxs-lookup"><span data-stu-id="3fe36-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="3fe36-131">Ciklo laiko santykiai naudojami, norint apskaičiuoti gamybos eigos veiklos ciklo laikus</span><span class="sxs-lookup"><span data-stu-id="3fe36-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="3fe36-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3fe36-132">Click OK.</span></span>
10. <span data-ttu-id="3fe36-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3fe36-133">Close the page.</span></span>
11. <span data-ttu-id="3fe36-134">Spustelėkite skirtuką GridPanel.</span><span class="sxs-lookup"><span data-stu-id="3fe36-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="3fe36-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3fe36-135">Close the page.</span></span>
13. <span data-ttu-id="3fe36-136">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3fe36-136">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]