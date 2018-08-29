--- 
title: "Įrašo šablonų kūrimas siekiant paprastesnio duomenų įvedimo"
description: "Šioje procedūroje parodoma, kaip sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių."
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: afe2da72ef6a6451e797ed6098df164e765e503e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="create-record-templates-to-facilitate-data-entry"></a><span data-ttu-id="94333-103">Įrašo šablonų kūrimas siekiant paprastesnio duomenų įvedimo</span><span class="sxs-lookup"><span data-stu-id="94333-103">Create record templates to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94333-104">Šioje procedūroje parodoma, kaip sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="94333-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="94333-105">Atlikdami šią procedūrą sukursite naują įrašą apie naujus nešiojamuosius kompiuterius, kurie turėtų būti įtraukti į jūsų ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="94333-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="94333-106">Šioje procedūroje naudojama pavyzdinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="94333-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="94333-107">Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="94333-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="94333-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="94333-108">Click New.</span></span>
3. <span data-ttu-id="94333-109">Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="94333-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="94333-111">Pavyzdžiui, įveskite „Įmonės pagrindinis nešiojamasis kompiuteris”.</span><span class="sxs-lookup"><span data-stu-id="94333-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="94333-112">Lauke Ieškos pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="94333-113">Pavyzdžiui, įveskite „nešiojamasis kompiuteris.”</span><span class="sxs-lookup"><span data-stu-id="94333-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="94333-114">Išplėskite dalį Techninė informacija.</span><span class="sxs-lookup"><span data-stu-id="94333-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="94333-115">Lauke Gamintojas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="94333-116">Lauke Modelis įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="94333-117">Lauke Modelio metai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="94333-118">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="94333-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="94333-119">Spustelėkite Įrašo informacija.</span><span class="sxs-lookup"><span data-stu-id="94333-119">Click Record info.</span></span>
12. <span data-ttu-id="94333-120">Spustelėkite Vartotojo šablonas.</span><span class="sxs-lookup"><span data-stu-id="94333-120">Click User template.</span></span>
13. <span data-ttu-id="94333-121">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="94333-122">Pavyzdžiui, įveskite „Įmonės nešiojamasis kompiuteris.”</span><span class="sxs-lookup"><span data-stu-id="94333-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="94333-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94333-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="94333-124">Pavyzdžiui, įveskite „Įmonės nešiojamasis kompiuteris”.</span><span class="sxs-lookup"><span data-stu-id="94333-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="94333-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="94333-125">Click OK.</span></span>
16. <span data-ttu-id="94333-126">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="94333-126">Click Close.</span></span>


