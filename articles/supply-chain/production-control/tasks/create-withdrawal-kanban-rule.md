---
title: Kurti išėmimo „kanban“ taisyklę
description: Šioje procedūroje parodyta, ką ir kaip reikia nustatyti, norint sukurti medžiagos perkėlimo „lean‟ aplinkoje išėmimo „kanban“ taisyklę.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8647a88773b3d4c0193d64307426736d0d085d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837763"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="0fa0b-103">Kurti išėmimo „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="0fa0b-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0fa0b-104">Šioje procedūroje parodyta, ką ir kaip reikia nustatyti, norint sukurti medžiagos perkėlimo „lean‟ aplinkoje išėmimo „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="0fa0b-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0fa0b-106">Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos medžiagos papildymą.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="0fa0b-107">Naujos „kanban“ taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="0fa0b-107">Create new kanban rule</span></span>
1. <span data-ttu-id="0fa0b-108">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0fa0b-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-109">Click New.</span></span>
3. <span data-ttu-id="0fa0b-110">Lauke Tipas pasirinkite Išėmimas.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="0fa0b-111">„Kanban‟ taisyklių tipas Išėmimas naudojamas perkelti medžiagai ar prekėms.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="0fa0b-112">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="0fa0b-113">Pasirinkite ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="0fa0b-114">Ši veikla nustatyta perkelti komponentus iš 11-ojo sandėlio, 11-osios vietos į 12-ąjį sandėlį ir 12-ąją vietą.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="0fa0b-115">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0fa0b-116">Pažymėkite M0007.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-116">Select M0007.</span></span>  
6. <span data-ttu-id="0fa0b-117">Lauke Gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="0fa0b-118">Pavyzdžiui, 60.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-118">For example, 60.</span></span>  
7. <span data-ttu-id="0fa0b-119">Lauke Matavimo vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="0fa0b-120">Pavyzdžiui, Minutės.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="0fa0b-121">„Kanban‟ kiekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="0fa0b-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="0fa0b-122">Nustatykite pasirinkties Numatytasis kiekis reikšmę „5“.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="0fa0b-123">Tai kiekis, kuris bus perduotas kiekvienam „kanban“.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="0fa0b-124">Lauke Fiksuotas „kanban“ kiekis įveskite 2.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="0fa0b-125">Tai yra „kanbans“, kurie turi būti aktyvūs, suma.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="0fa0b-126">Šiuo atveju 2 „kanban“ signalai, iš kurių kiekvienas perkelia 5.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="0fa0b-127">Lauke Žemiausia įspėjimo riba įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="0fa0b-128">Naudojama norint sekti minimalią visų paskirties vietoje turinčių būti „kanbans“ sumą.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0fa0b-129">Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="0fa0b-130">Lauke Aukščiausia įspėjimo riba įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="0fa0b-131">Naudojama norint sekti maksimalią visų paskirties vietoje turinčių būti „kanbans“ sumą.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0fa0b-132">Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="0fa0b-133">Kurti „kanban“</span><span class="sxs-lookup"><span data-stu-id="0fa0b-133">Create kanbans</span></span>
1. <span data-ttu-id="0fa0b-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-134">Click Save.</span></span>
    * <span data-ttu-id="0fa0b-135">Tam, kad būtų galima kurti „kanbans“, turi būti įrašyta „kanban“ taisyklė.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="0fa0b-136">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-136">Click Add.</span></span>
    * <span data-ttu-id="0fa0b-137">Atkreipkite dėmesį, kad nėra jokių aktyvių „kanban“ signalų, nes siūlomas Naujų „kanban“ signalų skaičius yra 2, lygus fiksuotam „kanban“ kiekiui.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="0fa0b-138">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-138">Click Create.</span></span>
    * <span data-ttu-id="0fa0b-139">Taip sukursite du „kanban“ signalus.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="0fa0b-140">Atkreipkite dėmesį, kad 2 „kanban“ signalai, kiekvienas po 5, buvo sukurti šiai išėmimo „kanban“ taisyklei.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="0fa0b-141">Tai yra paskutinis šios procedūros veiksmas.</span><span class="sxs-lookup"><span data-stu-id="0fa0b-141">This is the last step in this procedure.</span></span>  

