--- 
title: "Fiksuoto kiekio „kanban“ gamybos taisyklės kūrimas"
description: "Šia procedūra sutelkiamas dėmesys į nustatymą, reikalingą norint „lean“ aplinkos darbo elemente sukurti fiksuotą gamybos „kanban“ taisyklę, skirtą transformavimo veiklos aktyvinimui."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7b84c4351834658537868445403835137c57db23
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="85c9d-103">Fiksuoto kiekio „kanban“ gamybos taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="85c9d-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85c9d-104">Šia procedūra sutelkiamas dėmesys į nustatymą, reikalingą norint „lean“ aplinkos darbo elemente sukurti fiksuotą gamybos „kanban“ taisyklę, skirtą transformavimo veiklos aktyvinimui.</span><span class="sxs-lookup"><span data-stu-id="85c9d-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="85c9d-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="85c9d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="85c9d-106">Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.</span><span class="sxs-lookup"><span data-stu-id="85c9d-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="85c9d-107">Naujos „kanban“ taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="85c9d-107">Create new kanban rule</span></span>
1. <span data-ttu-id="85c9d-108">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="85c9d-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="85c9d-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="85c9d-109">Click New.</span></span>
    * <span data-ttu-id="85c9d-110">Atkreipkite dėmesį, kad numatytasis tipas Gamybos ir papildymo strategija yra Fiksuotas.</span><span class="sxs-lookup"><span data-stu-id="85c9d-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="85c9d-111">Jums nereikia keisti šių parametrų.</span><span class="sxs-lookup"><span data-stu-id="85c9d-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="85c9d-112">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85c9d-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="85c9d-113">Tai veikla, kuri bus atliekama naudojant „kanbans“, sukurtus remiantis šia „kanban“ taisykle.</span><span class="sxs-lookup"><span data-stu-id="85c9d-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="85c9d-114">Pasirinkite „SpeakerTestAndPackaging“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="85c9d-115">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="85c9d-115">Expand the Details section.</span></span>
5. <span data-ttu-id="85c9d-116">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85c9d-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="85c9d-117">Pažymėkite L0050.</span><span class="sxs-lookup"><span data-stu-id="85c9d-117">Select L0050.</span></span>  
6. <span data-ttu-id="85c9d-118">Lauke Matavimo vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85c9d-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="85c9d-119">Pasirinkite minutes.</span><span class="sxs-lookup"><span data-stu-id="85c9d-119">Select minutes.</span></span>  
7. <span data-ttu-id="85c9d-120">Lauke Gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="85c9d-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="85c9d-121">Įveskite 5.</span><span class="sxs-lookup"><span data-stu-id="85c9d-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="85c9d-122">Kiekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="85c9d-122">Set quantities</span></span>
1. <span data-ttu-id="85c9d-123">Išplėskite skyrių Kiekiai.</span><span class="sxs-lookup"><span data-stu-id="85c9d-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="85c9d-124">Nustatykite pasirinkties Numatytasis kiekis reikšmę „10“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="85c9d-125">Tai kiekis, kuris bus perduotas kiekvienam „kanban“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="85c9d-126">Pažymėkite žymės langelį Produkto kiekio nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="85c9d-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="85c9d-127">Tokiu būdu pasirinktus „kanbans“ galima užbaigti su nuokrypiu nuo numatytojo kiekio.</span><span class="sxs-lookup"><span data-stu-id="85c9d-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="85c9d-128">Norėdami užbaigti „kanbans“, kai jų kiekio reikšmė nuo 8 iki 12, nustatykite abiejų nuokrypių reikšmes 2.</span><span class="sxs-lookup"><span data-stu-id="85c9d-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="85c9d-129">Nustatykite pasirinkties Nuokrypis mažesnis negu reikšmę „2“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="85c9d-130">Tai leis užbaigti mažėjant iki 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="85c9d-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="85c9d-131">Nustatykite pasirinkties Nuokrypis didesnis negu reikšmę „2“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="85c9d-132">Tai leis užbaigti didėjant iki 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="85c9d-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="85c9d-133">Lauke Fiksuotas „kanban“ kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="85c9d-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="85c9d-134">Tai yra „kanbans“, kurie turi būti aktyvūs, suma.</span><span class="sxs-lookup"><span data-stu-id="85c9d-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="85c9d-135">Šiuo atveju 5 „kanbans“, iš kurių kiekvienas apdoroja 10.</span><span class="sxs-lookup"><span data-stu-id="85c9d-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="85c9d-136">Lauke Žemiausia įspėjimo riba įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="85c9d-137">Naudojama norint sekti minimalią visų paskirties vietoje turinčių būti „kanbans“ sumą.</span><span class="sxs-lookup"><span data-stu-id="85c9d-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="85c9d-138">Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.</span><span class="sxs-lookup"><span data-stu-id="85c9d-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="85c9d-139">Lauke Aukščiausia įspėjimo riba įveskite „4“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="85c9d-140">Naudojama norint sekti maksimalią visų paskirties vietoje turinčių būti „kanbans“ sumą.</span><span class="sxs-lookup"><span data-stu-id="85c9d-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="85c9d-141">Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.</span><span class="sxs-lookup"><span data-stu-id="85c9d-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="85c9d-142">Lauke Automatinio planavimo kiekis įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="85c9d-143">Nustačius 1 reiškia, kad kiekvienas „kanban“ bus suplanuotas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="85c9d-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="85c9d-144">Jei įvedėme 3, „kanbans“ nebus planuojami, kol planavimui nebus paruošti 3 tušti „kanbans“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="85c9d-145">Tai naudinga grupuojant darbą ir norint išvengti per daug nustatymų.</span><span class="sxs-lookup"><span data-stu-id="85c9d-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="85c9d-146">„Kanbans“ kūrimas</span><span class="sxs-lookup"><span data-stu-id="85c9d-146">Create Kanbans</span></span>
1. <span data-ttu-id="85c9d-147">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="85c9d-148">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="85c9d-148">Click Save.</span></span>
    * <span data-ttu-id="85c9d-149">Tam, kad būtų galima kurti „kanbans“, turi būti įrašyta „kanban“ taisyklė.</span><span class="sxs-lookup"><span data-stu-id="85c9d-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="85c9d-150">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="85c9d-150">Click Add.</span></span>
    * <span data-ttu-id="85c9d-151">Atkreipkite dėmesį, kad nėra jokių aktyvių „kanbans“, todėl siūlomas „Naujų „kanbans“ skaičius“ yra 5.</span><span class="sxs-lookup"><span data-stu-id="85c9d-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="85c9d-152">Jis lygus „fiksuotam „kanban“ kiekiui“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="85c9d-153">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="85c9d-153">Click Create.</span></span>
    * <span data-ttu-id="85c9d-154">Taip sukursite 5 „kanbans“.</span><span class="sxs-lookup"><span data-stu-id="85c9d-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="85c9d-155">Atkreipkite dėmesį, kad 5 „kanbans“, kiekvienas po 10, buvo sukurti šiai gamybos „kanban“ taisyklei.</span><span class="sxs-lookup"><span data-stu-id="85c9d-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="85c9d-156">Tai yra paskutinis šios procedūros veiksmas.</span><span class="sxs-lookup"><span data-stu-id="85c9d-156">This is the last step in this procedure.</span></span>  


